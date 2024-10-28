Phân Tích Kiến Trúc, Cơ Chế, và Ca Sử Dụng cho Payroll System

Mục tiêu: Cung cấp phân tích kiến trúc và các ca sử dụng chính của hệ thống Payroll System nhằm đảm bảo tính chính xác và hiệu quả trong quản lý bảng chấm công và chi trả lương.

1. Phân Tích Kiến Trúc
1.1 Đề Xuất Kiến Trúc
Kiến trúc của Payroll System được thiết kế dựa trên mô hình phân lớp nhằm đảm bảo tính linh hoạt và dễ dàng bảo trì. Hệ thống gồm hai lớp chính:

Application Layer: Xử lý các yêu cầu từ người dùng và giao diện, bao gồm các lựa chọn phương thức thanh toán và chấm công.
Business Services Layer: Thực hiện các quy trình nghiệp vụ chính, quản lý logic thanh toán và tính toán giờ làm.
Lý do: Mô hình phân lớp giúp tách biệt rõ ràng giữa các phần khác nhau của hệ thống, giúp tăng tính ổn định và dễ bảo trì. Việc tách các lớp cũng giúp dễ dàng cập nhật hoặc thay thế một phần mà không ảnh hưởng đến các phần còn lại.
biểu đồ Package UML : 


![Diagram](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuIf8JCvEJ4zLK0f8h2pApybH2AuiBadDLLAevb800hYqOq51JcPoOabcVfw2Js9bQX5O1HH4ksScvYkaP3xStPwda9T-RCF3tNCp5L8ExynBZmKhgWMJg2OwbHPdvgKM5oi4fnQLPIQd5cCnr-NXxkxa38MoXxkN0itD05bG0ER1ZAtbuiBcD5rTEpmMM2cuFzpT2tGWmdGkXzIy561u0000)


2. Cơ Chế Phân Tích
Các cơ chế chính để hỗ trợ nghiệp vụ của Payroll System bao gồm:

Persistence (Lưu Trữ): Đảm bảo các thông tin quan trọng, như bảng chấm công và thanh toán, được lưu trữ an toàn và dễ dàng truy xuất.
Security (Bảo Mật): Bảo vệ dữ liệu nhạy cảm của nhân viên và ngăn chặn truy cập trái phép vào hệ thống.
Legacy Interface (Giao Diện Tích Hợp Hệ Thống Cũ): Tích hợp các hệ thống cũ như BankSystem và ProjectManagementDatabase để đảm bảo việc chuyển khoản và quản lý mã dự án diễn ra trơn tru.
Giải thích: Cơ chế Persistence và Security giúp quản lý dữ liệu ổn định và an toàn, trong khi Legacy Interface đảm bảo hệ thống mới tương thích và có thể sử dụng dữ liệu từ các hệ thống cũ.
3. Phân Tích Ca Sử Dụng: Select Payment Method
Mô Tả Ca Sử Dụng
Trong ca sử dụng này, Employee có thể chọn phương thức nhận thanh toán. Có ba phương thức chính:

Nhận trực tiếp: Nhân viên nhận phiếu lương trực tiếp tại công ty.
Gửi bưu điện: Phiếu lương được gửi qua bưu điện đến địa chỉ nhân viên cung cấp.
Chuyển khoản: Thanh toán được chuyển trực tiếp vào tài khoản ngân hàng của nhân viên.
Các Bước Phân Tích
Khởi đầu: Nhân viên bắt đầu quy trình chọn phương thức thanh toán.
Hiển thị Lựa Chọn: Hệ thống hiển thị ba phương thức thanh toán để nhân viên lựa chọn.
Xử lý yêu cầu:
Nếu chọn “nhận trực tiếp,” không cần thông tin bổ sung.
Nếu chọn “gửi bưu điện,” hệ thống yêu cầu địa chỉ gửi.
Nếu chọn “chuyển khoản,” hệ thống yêu cầu tên ngân hàng và số tài khoản.
Cập nhật Thông Tin: Hệ thống lưu phương thức thanh toán của nhân viên vào hồ sơ cá nhân.

Biểu Đồ Lớp cho Ca Sử Dụng Payment :


![Diagram](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuKhEIImkLd3DBSZ9hqnDLQZcKb3GLSWzlDWlu_2YlB3Cmwloh1I2IueoyzB1CYNe0WKPnpOSMvYN7fBnSFVAv92CnBoCaFp32r4L7PduS7TteZDGIIU6QNxfG8iy3Y_8IqUHAdwuUsB8uGMPtXdv3tSjHXXN2tLnG69bSaPgSZR2nGYxCGtAVBYx4IZibfEVM0An6UYMkPdkcOb0KPV4abIukKw9UTd1bSKbgRbWaxN1AZScUm1DQCzppYYjVBYxEG_gA8rKQB1vki2ir558pCqlpIk1sgK9D1SUjag6IWgwkWfAMae8rrifb3pSjJ0VNP4TY4PsYnN87siLKXxkNWhqbqDgNWeeyW00)


4. Phân Tích Ca Sử Dụng: Maintain Timecard
Mô Tả Ca Sử Dụng
Trong ca sử dụng này, Employee có thể ghi lại số giờ làm việc và các dự án liên quan trong bảng chấm công.

Các Bước Phân Tích
Khởi đầu: Nhân viên bắt đầu ghi giờ làm trên bảng chấm công.
Hiển thị mã dự án: Hệ thống lấy danh sách mã dự án từ ProjectManagementDatabase và hiển thị cho nhân viên chọn.
Ghi nhận giờ làm: Nhân viên chọn mã dự án và nhập số giờ làm cho từng ngày.
Lưu và nộp bảng chấm công: Sau khi ghi đủ giờ làm, nhân viên nộp bảng chấm công và hệ thống xác thực dữ liệu, chuyển trạng thái bảng chấm công thành “đã nộp”.

Biểu Đồ Lớp cho Ca Sử Dụng Maintain Timecard :


![Diagram](http://www.plantuml.com/plantuml/png/TL71IlD06BpdAJvoQlysX_yQIYbDHSHM18ltRRfiLh9VIx8z5F7W6tZr8BQM8WXI14-RWuVrHRutCMtQH0MlC_FDpCvsKiqIFLEn4yOiJU58JUF9d7EuTW0yK7Pr5jadl9Js1Nsuq8b4iMFqRs14PeKYYCYiLM3VKVZGbwbk3QNY8Kl6RUTcdt50genk4FpmGc4NyowPZVwy8_Cyyw77DA-eKp8VUXXP4tvZT49cYIA7bx9oAm9wbBtPsxpmW4rR1TM44zHSyAITYneW8daiANlesuMgxK8AwoQ8BUmVrFMT6YcxdzRgvPFEayaL3_M08HDSSTJvAHknjDYn0J6PzNnGzgZLz-CKLRRJbCEx_rtmF73_kTLGFgIKFK94sMRcbAZdjVyEBcvUOKpP6eNJuJZU_l8N)



5. Hợp Nhất Kết Quả Phân Tích
Trong hệ thống Payroll, cả hai ca sử dụng đều lấy Employee làm trung tâm. Các lớp Employee, Timecard, và Paycheck liên kết chặt chẽ, đảm bảo hệ thống có thể quản lý thông tin bảng chấm công và thanh toán chính xác. Kết quả hợp nhất giúp đảm bảo dữ liệu giữa các quy trình được đồng bộ và quản lý tập trung.
