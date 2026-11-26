---
title: "Blog 2"
date: 2026-11-26
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Xây dựng một Kho dữ liệu Phi máy chủ với Amazon Redshift

Chào mọi người, khoảng 2 tháng trước tôi có đăng một bài blog về **Xây dựng Pipeline Serverless: Import dữ liệu từ S3 đến DynamoDB**, theo tôi thấy cái lab mà tôi từng làm này dễ quá và không có tính an toàn và lưu trữ. Cho nên trong quá trình thực tập tôi có học và làm quen một dịch vụ khá là hay chính là Amazon Redshift, là dịch vụ kho dữ liệu trên nền tảng điện toán đám mây của AWS, được quản lý hoàn toàn để lưu trữ và phân tích dữ liệu quy mô lớn.

Trong bài blog này, tôi sẽ chia sẻ một cái lab tên là **Xây dựng Data Warehouse với Amazon Redshift Serverless**. Trong quá trình tìm hiểu về Data Analytics, tôi nhận thấy dữ liệu đóng vai trò quan trọng trong hoạt động của doanh nghiệp. Dữ liệu được sử dụng để phân tích, hỗ trợ ra quyết định và quản lý các hoạt động kinh doanh. Vì vậy, việc lưu trữ và bảo vệ dữ liệu an toàn là một yêu cầu cần thiết.

Trong thực tế, dữ liệu có thể bị mất do nhiều nguyên nhân như vô tình xóa nhầm, lỗi hệ thống hoặc sự cố trong quá trình xử lý. Nếu không có phương án sao lưu phù hợp, doanh nghiệp có thể mất nhiều thời gian và chi phí để khôi phục dữ liệu. Do đó, tôi lựa chọn bài lab này để tìm hiểu cách xây dựng kho dữ liệu trên AWS, đồng thời thực hành các phương pháp backup và recovery bằng Amazon Redshift.

## Quá trình làm lab

### 1. Chuẩn bị và lưu trữ dữ liệu trên Amazon S3

Đầu tiên, tôi tạo một S3 Bucket để lưu trữ dataset `Prices.csv`. File CSV này chứa 155 bản ghi và 8 cột dữ liệu liên quan đến giá thực phẩm, bao gồm tên sản phẩm, hình thức sản phẩm, giá bán lẻ và giá tương đương theo đơn vị đo.

Sau khi tạo Bucket, tôi tải file lên thư mục raw/ và bật tính năng Versioning để lưu giữ các phiên bản khác nhau của object. Điều này giúp bảo vệ dữ liệu gốc trong trường hợp file bị ghi đè hoặc xóa nhầm.

### 2. Cấu hình IAM và Amazon Redshift Serverless

Tiếp theo, tôi tạo IAM Role với quyền truy cập cần thiết để Amazon Redshift có thể đọc dữ liệu từ S3. Tôi sử dụng quyền truy cập giới hạn cho Bucket phục vụ bài Lab thay vì cấp quyền quá rộng.

Sau đó, tôi tạo Redshift Serverless với namespace `prices-namespace` và workgroup `prices-workgroup`. Đây là thành phần chính của hệ thống, chịu trách nhiệm lưu trữ và xử lý dữ liệu.

Sau khi cấu hình hoàn tất, tôi liên kết IAM Role với Redshift để cho phép dịch vụ truy cập file CSV trên S3.

### 3. Nạp và phân tích dữ liệu bằng Query Editor v2

Tôi sử dụng Amazon Redshift Query Editor v2 để kết nối đến Data Warehouse, tạo schema `food_analytics` và bảng `prices`.

Sau khi cấu hình lệnh COPY để nạp dữ liệu từ S3, tôi kiểm tra kết quả và xác nhận bảng đã có đủ 155 bản ghi.

Tiếp theo, tôi thực hành các câu lệnh SQL để phân tích dữ liệu, chẳng hạn như:
<br>&emsp;&#8211; Đếm số lượng sản phẩm theo từng nhóm Fresh, Canned, Frozen, Dried và Juice.
<br>&emsp;&#8211; Tính giá bán trung bình, giá thấp nhất và giá cao nhất.
<br>&emsp;&#8211; Tìm 10 sản phẩm có giá bán cao nhất.
<br>&emsp;&#8211; So sánh giá giữa các hình thức sản phẩm.
<br>&emsp;&#8211; Tìm những sản phẩm có Cup Equivalent Price thấp.

Ngoài ra, tôi tạo View `vw_price_summary` để lưu kết quả tổng hợp và thử tạo biểu đồ trong Query Editor v2 nhằm trực quan hóa dữ liệu.

### 4. Sử dụng AWS Glue để quản lý metadata

Sau khi hoàn thành phần xử lý dữ liệu trong Redshift, tôi tiếp tục thực hành với AWS Glue.

Tôi tạo database `prices_catalog` và crawler `prices_csv_crawler`, sau đó cấu hình crawler đọc dữ liệu từ thư mục `raw/` trong S3.

Khi crawler chạy thành công, AWS Glue tự động thu thập thông tin về cấu trúc file CSV và tạo metadata trong Data Catalog. Qua đó, tôi hiểu rõ hơn vai trò của Glue trong việc quản lý metadata của dữ liệu.

### 5. Theo dõi hệ thống bằng Amazon CloudWatch

Ở phần monitoring, tôi sử dụng Amazon CloudWatch để theo dõi hoạt động của Redshift Serverless.

Tôi tìm hiểu và lựa chọn một số metrics quan trọng như QueryDuration, QueriesCompletedPerSecond, QueriesRunning, QueriesSucceeded, ComputeCapacity, ComputeSeconds, DatabaseConnections và DataStorage.

Sau đó, tôi tạo một dashboard `Redshift-Prices-Monitoring` với các nhóm biểu đồ về hiệu suất truy vấn, mức sử dụng compute, kết nối database, dung lượng lưu trữ và thời gian thực thi truy vấn.

Tôi cũng thực hiện thêm một số câu lệnh SQL để tạo hoạt động cho Redshift và quan sát sự thay đổi của các metrics trên CloudWatch. Qua phần này, tôi hiểu rõ hơn cách theo dõi hiệu suất và kiểm tra tình trạng hoạt động của Data Warehouse.

### 6. Thực hiện Backup và Disaster Recovery

Đây là phần quan trọng nhất của bài lab. Tôi thực hiện sao lưu dữ liệu bằng tính năng Manual Snapshot của Amazon Redshift Serverless với tên `prices-before-disaster`.

Sau khi snapshot hoàn tất, tôi giả lập một sự cố bằng cách xóa bảng `food_analytics.prices` thông qua lệnh SQL `DROP TABLE`. Khi kiểm tra lại, truy vấn không thể thực hiện vì bảng dữ liệu đã bị xóa.

Tiếp theo, tôi sử dụng snapshot đã tạo để khôi phục hệ thống. Quá trình restore tạo ra một namespace mới, vì vậy tôi cần kết nối Query Editor v2 đến workgroup tương ứng để kiểm tra dữ liệu sau khi phục hồi.

Kết quả kiểm tra cho thấy bảng `prices` đã được khôi phục với đầy đủ 155 bản ghi. View `vw_price_summary` cũng được kiểm tra lại để xác nhận dữ liệu đã phục hồi.

Ngoài ra, tôi thực hành sử dụng AWS Backup để quản lý hoạt động sao lưu cho Redshift Serverless, kết quả cũng tương tự như Redshift. Qua đó, tôi có thêm kinh nghiệm với việc quản lý Backup Plan và Recovery Points.

## Sơ đồ kiến trúc AWS

{{< img src="images/3-BlogsPosted/blog2/Building-a-Serverless-Data-Warehouse-with-Amazon-Redshift.png" alt="Building a Serverless Data Warehouse with Amazon Redshift" >}}

## Kết luận

Sau khi hoàn thành bài lab, tôi có thể khẳng định rằng việc xây dựng một hệ thống kho dữ liệu trên AWS có thể mang lại nhiều lợi ích khi phát triển các trang web hoặc ứng dụng có lượng dữ liệu lớn trong database. Thay vì chỉ lưu trữ và truy vấn dữ liệu trực tiếp từ database của ứng dụng, doanh nghiệp có thể sử dụng kho dữ liệu để tập trung dữ liệu, thực hiện các truy vấn phân tích và hỗ trợ quá trình đưa ra quyết định.

Bài lab giúp tôi có cái nhìn thực tế hơn về cách các dịch vụ AWS phối hợp với nhau trong một hệ thống dữ liệu. Qua đó, tôi muốn tiếp tục tìm hiểu về Data Analytics, nhưng không chỉ dừng lại ở đó mà còn có Data Engineering để có thể áp dụng những kiến thức đã học vào các dự án thực tế trong tương lai.

Tôi khuyến khích những bạn đang học AWS hoặc muốn tìm hiểu về Data Analytics hay Engineering nên thử thực hiện bài lab này. Bài thực hành có thể giúp các bạn làm quen với Amazon Redshift Serverless, S3, IAM, Glue và CloudWatch thông qua một quy trình xử lý dữ liệu tương đối hoàn chỉnh.

Nếu có cơ hội thực hiện, các bạn nên chú ý đến quyền IAM, cấu hình dịch vụ và chi phí sử dụng AWS. Hãy kiểm tra các tài nguyên sau khi hoàn thành để tránh phát sinh chi phí ngoài dự kiến nhé.