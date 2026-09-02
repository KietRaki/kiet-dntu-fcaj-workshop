---
title: "Blog 1"
date: 2026-08-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
<!-- {{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}} -->

# Xây dựng Pipeline Serverless: Import dữ liệu từ S3 đến DynamoDB

Xin chào mọi người, mình là Nguyễn Vũ Tuấn Kiệt, hiện đang thực tập với vị trí Data Analyst. Tôi đã thực tập được 2 tháng thì trong quá trình thực tập, mình có cơ hội tìm hiểu sâu hơn về các dịch vụ AWS, đặc biệt là những dịch vụ liên quan đến lưu trữ, xử lý và phân tích dữ liệu. Bên cạnh việc học lý thuyết, mình cũng muốn tự xây dựng các bài lab nhỏ để hiểu rõ hơn cách những dịch vụ này được kết hợp trong một hệ thống thực tế.

Trong bài viết này, mình sẽ chia sẻ một lab mà mình đã thực hiện với mục tiêu xây dựng một pipeline xử lý dữ liệu đơn giản theo kiến trúc serverless. Những ai mà đi theo hướng Data như tôi thì có thể làm theo để biết các dịch vụ AWS hoạt động như thế nào. Cụ thể, mình sử dụng Amazon S3 để lưu file CSV, AWS Lambda để đọc và xử lý dữ liệu, Amazon DynamoDB để lưu dữ liệu sau khi xử lý và Amazon CloudWatch để theo dõi log. Khi một file CSV mới được upload lên S3, Lambda sẽ tự động được kích hoạt, đọc dữ liệu, kiểm tra tính hợp lệ của từng record và ghi những record hợp lệ vào DynamoDB.

**1. Tổng quan về bài lab**

Trong các hệ thống xử lý dữ liệu, một quy trình khá phổ biến là nhận dữ liệu từ một nguồn bên ngoài, kiểm tra và xử lý dữ liệu, sau đó lưu dữ liệu vào một hệ thống để ứng dụng có thể sử dụng. Với bài lab này, mình mô phỏng một tình huống đơn giản trong đó dữ liệu sản phẩm được cung cấp dưới dạng file CSV.

Kiến trúc mình xây dựng gồm bốn thành phần chính:
<br>&emsp;&#8211; Amazon S3.
<br>&emsp;&#8211; AWS Lambda.
<br>&emsp;&#8211; Amazon DynamoDB.
<br>&emsp;&#8211; Amazon CloudWatch.

S3 đóng vai trò lưu trữ file đầu vào. Khi file CSV được upload vào một thư mục cụ thể trong S3, S3 sẽ phát sinh sự kiện và kích hoạt Lambda. Lambda sau đó đọc file CSV, xử lý từng dòng dữ liệu và kiểm tra một số điều kiện như product_id phải tồn tại, price phải là số hợp lệ và stock không được âm. Những record hợp lệ sẽ được ghi vào DynamoDB, còn những record không hợp lệ sẽ được bỏ qua và ghi thông tin cảnh báo vào CloudWatch Logs.

![Import from S3 to DynamoDB](/images/3-BlogsPosted/blog1/Serverless-Pipeline_Import-from-S3-to-DynamoDB.drawio.png)

**2. Chuẩn bị dữ liệu trên Amazon S3**

Đầu tiên, mình tạo một S3 bucket để lưu trữ dữ liệu đầu vào. Trong bucket, mình sử dụng thư mục input/ để chứa các file CSV cần xử lý. Việc sử dụng prefix này giúp mình kiểm soát những file nào sẽ kích hoạt Lambda, thay vì để mọi object trong bucket đều tạo ra một sự kiện.

File dữ liệu mẫu có cấu trúc như sau:
```
product_id,product_name,category,price,stock
P001,Laptop Dell,Electronics,1200,15
P002,Wireless Mouse,Accessories,25,100
P003,Mechanical Keyboard,Accessories,75,50
P004,Monitor 27 inch,Electronics,350,30
P005,USB-C Hub,Accessories,45,80
P006,Webcam HD,Electronics,60,40
P007,Headphones,Audio,120,25
P008,Smartphone,Electronics,800,20
P009,Desk Lamp,Home,35,60
P010,Office Chair,Home,250,10
```

đặt tên là `products-test.csv`.

Sau khi upload file vào input/, S3 sẽ tạo một Object Created event. Event này chứa những thông tin quan trọng như tên bucket và object key của file vừa được upload. Lambda có thể sử dụng những thông tin này để xác định chính xác file nào cần được đọc và xử lý.

**3. AWS Lambda xử lý dữ liệu**

Phần chính của bài lab nằm ở Lambda. Mình sử dụng Python và boto3 để Lambda có thể tương tác với S3 và DynamoDB. Khi nhận được S3 event, Lambda lấy tên bucket và object key, sau đó sử dụng `s3.get_object()` để đọc nội dung file CSV trực tiếp từ S3.

Sau khi đọc file, Lambda sử dụng `csv.DictReader` để chuyển từng dòng trong CSV thành một dictionary. Từ đó, mình có thể dễ dàng lấy các trường như product_id, product_name, category, price và stock để thực hiện validation trước khi ghi dữ liệu vào DynamoDB.

Một vấn đề mình gặp trong quá trình thực hiện là DynamoDB thông qua boto3 không hỗ trợ Python **float** khi ghi dữ liệu. Ban đầu mình sử dụng `float(row["price"])`, nhưng Lambda trả về lỗi `Float types are not supported`. Sau khi kiểm tra lỗi, mình chuyển sang sử dụng **Decimal** từ Python decimal module. Đây là một lỗi khá hữu ích trong quá trình làm lab vì nó giúp mình hiểu rõ hơn về cách boto3 xử lý kiểu dữ liệu Number khi làm việc với DynamoDB.

**4. Kiểm tra và xử lý dữ liệu không hợp lệ**

Mình không muốn một record bị lỗi làm toàn bộ file CSV không thể import. Vì vậy, Lambda được thiết kế để kiểm tra từng record riêng biệt. Nếu **product_id** bị thiếu, Lambda sẽ ghi cảnh báo và bỏ qua record đó. Tương tự, nếu price không thể chuyển thành **Decimal**, hoặc stock không thể chuyển thành số nguyên, record cũng sẽ được đánh dấu là **invalid**.

Ví dụ, tạo 1 file CSV có dữ liệu như sau:

```
product_id,product_name,category,price,stock
P011,Tablet,Electronics,500,35
P012,Gaming Mouse,Accessories,55,70
P013,USB Microphone,Audio,90,25
P014,Invalid Product,Electronics,ABC,20
,Missing ID,Electronics,100,10
P015,Negative Price,Electronics,-50,20
```

đặt tên là `products-test-2.csv`.

Lambda sẽ xử lý từng dòng. P011, P012 và P013 là những record hợp lệ nên được ghi vào DynamoDB. P014 có `price = ABC` nên bị bỏ qua. Record không có product_id cũng bị bỏ qua. P015 có giá âm nên cũng không được đưa vào DynamoDB.

Điểm mình thay đổi sau khi test là đưa `batch_writer()` vào trong quá trình xử lý file. Nhờ vậy, những record hợp lệ có thể được đưa vào batch để ghi vào DynamoDB, trong khi những record lỗi được bỏ qua bằng **continue**. CloudWatch Logs cũng ghi lại thông tin để mình biết tổng số record, số record hợp lệ và số record không hợp lệ.

**5. Lưu dữ liệu vào Amazon DynamoDB**

Sau khi validation hoàn tất cho từng record, Lambda sử dụng DynamoDB `batch_writer()` để ghi dữ liệu. Mình tạo một table có tên **products** và sử dụng **product_id** làm Partition Key.

Một item trong DynamoDB có dạng:
```
{
    "product_id": "P011",
    "product_name": "Tablet",
    "category": "Electronics",
    "price": 500,
    "stock": 35
}
```

Việc sử dụng `batch_writer()` giúp code phù hợp hơn với trường hợp có nhiều records cần import. Trong bài lab nhỏ, số lượng dữ liệu chưa lớn, nhưng cách tiếp cận này giúp mình làm quen với việc xử lý nhiều records thay vì thực hiện từng request riêng lẻ.

Sau khi Lambda chạy thành công, mình có thể vào **DynamoDB → Tables → Chọn table đã tạo → Explore table items** để kiểm tra dữ liệu. Với file test ở trên, chỉ những sản phẩm hợp lệ mới xuất hiện trong table.

**6. Theo dõi Lambda bằng CloudWatch**

Trong quá trình thực hiện, **Amazon CloudWatch Logs** là công cụ mình sử dụng khá nhiều để kiểm tra Lambda có hoạt động đúng hay không. Mình thêm các log như bucket name, object key, số lượng records và trạng thái của từng record để dễ dàng theo dõi quá trình xử lý.

Ví dụ, khi một record không hợp lệ, log có thể hiển thị:

```[WARNING] Invalid price or stock. Skipping record: {...}```

Còn với record hợp lệ:

```[INFO] Successfully processed: P011```

Cuối quá trình xử lý, Lambda ghi lại một summary:
```
========== Processing Summary ==========
[INFO] Total records: 8
[INFO] Valid records: 4
[INFO] Invalid records: 4
========================================
```

Việc có log rõ ràng giúp mình dễ dàng xác định vấn đề khi pipeline không hoạt động như mong muốn.

**7. Những gì mình học được**

Qua bài lab này, mình hiểu rõ hơn cách xây dựng một pipeline event-driven serverless trên AWS. Trước đây, mình chủ yếu tiếp cận các dịch vụ AWS ở mức khái niệm, nhưng khi tự kết nối S3, Lambda và DynamoDB, mình có thể thấy rõ cách dữ liệu di chuyển qua từng thành phần trong hệ thống.

Mình cũng có thêm kinh nghiệm với IAM khi phải cấp quyền `s3:GetObject` cho Lambda và quyền ghi dữ liệu vào DynamoDB. Đây là phần mình thấy khá quan trọng vì Lambda có thể chạy bình thường nhưng vẫn không thể xử lý dữ liệu nếu Execution Role không có permission phù hợp.

Ngoài ra, quá trình xử lý dữ liệu lỗi giúp mình nhận ra rằng data pipeline cần có validation và error handling ngay từ đầu. Thay vì để một dòng dữ liệu sai làm Lambda thất bại hoàn toàn, mình có thể xác định record lỗi, ghi log và tiếp tục xử lý những record còn lại.

**8. Những lỗi mình gặp phải trong quá trình làm việc**

Trong quá trình làm lab, mình gặp một số lỗi khá thực tế.

Đầu tiên là lỗi **AccessDenied** khi Lambda đọc file từ S3. Nguyên nhân là Lambda Execution Role chưa có quyền `s3:GetObject`. Sau khi kiểm tra CloudWatch Logs và IAM Role, mình thêm permission cho đúng S3 bucket và prefix `input/*`.

Tiếp theo là lỗi:
```
TypeError: Float types are not supported.
Use Decimal types instead.
```

Lỗi này xảy ra khi mình chuyển price thành Python float trước khi ghi vào DynamoDB. Mình đã thay **float()** bằng **Decimal()** và import **InvalidOperation** để có thể xử lý cả trường hợp giá trị không hợp lệ như ABC.

Cuối cùng là vấn đề xử lý các record lỗi. Ban đầu, nếu một record gây exception thì Lambda có thể dừng trước khi ghi những record hợp lệ còn lại. Sau khi thay đổi cấu trúc code và xử lý exception ngay trong vòng lặp, Lambda có thể bỏ qua record lỗi và tiếp tục xử lý những record phía sau.

**9. Kết luận**

Với mình, bài lab này cũng là một bước nhỏ trong quá trình thực tập tại Amazon Web Services Việt Nam. Thay vì chỉ học từng service riêng lẻ, mình muốn tiếp tục xây dựng những bài lab có kiến trúc hoàn chỉnh hơn để hiểu được cách các dịch vụ AWS phối hợp với nhau trong một bài toán thực tế. Từ pipeline hiện tại, mình có thể phát triển thêm các thành phần như Amazon EventBridge, Amazon SNS, Step Functions hoặc CloudWatch Alarms để xây dựng một hệ thống có khả năng monitoring và xử lý lỗi tốt hơn.