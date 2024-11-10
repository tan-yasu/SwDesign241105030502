1. Đăng Nhập (Login)
Mô tả: Nhân viên hoặc quản trị viên đăng nhập vào hệ thống.
Tác nhân: Nhân viên, Quản trị viên bảng lương
Luồng:
Nhân viên/Quản trị viên nhập tên đăng nhập và mật khẩu.
Hệ thống xác nhận và cho phép đăng nhập nếu thông tin hợp lệ.


![Diagram](http://www.plantuml.com/plantuml/png/RP3F2e904CRl-nHpD6HVG294l2L29D5rq6LtGMT3Tw2mtZq5_sGrnzytpFTZuivZwxcfHLbZrq6ksTcKIKClO1W9Nb6Af7E3jmZElhMafwH1VpJ86nf2DIq7kmWIvsg595vYFc-GBbOHz2ixCLBHsX4dI3fZH_ep7p8oLyuUiyQa5i8Toy9m6T0i7Qt-s_O5m_ufvQBnpV-fYDz-AGzhaOWLLUC3tm00)


2. Quản Lý Thông Tin Nhân Viên (Maintain Employee Information)
Mô tả: Quản trị viên quản lý thông tin nhân viên (thêm, cập nhật, xóa).
Tác nhân: Quản trị viên bảng lương
Luồng:
Quản trị viên chọn chức năng (Thêm, Cập nhật, Xóa nhân viên).
Cung cấp thông tin yêu cầu.
Hệ thống thực hiện chức năng tương ứng.

![Diagram](http//www.plantuml.com/plantuml/png/ZP2n2i8m443tVCMDIkaFE4Z1LGInT3_IqZjeBz8aOX7_tGX9m7GnuxkNuoMDTRWuFqzAJsWjN0Ybuq7WfI2S6cPCw00tjx2CSK2ctR2UyKHSG4rUT_u7LZ3XsfAHiML9-tVxxBnLpBbwbFDQH5NWQ9ZpDSbz2OL53yDzb3NUmy3zxJyDPdVx-kI6n2Akhezvese6wR-_-W40)




3. Tạo Báo Cáo Hành Chính (Create Administrative Report)
Mô tả: Quản trị viên tạo báo cáo hành chính.
Tác nhân: Quản trị viên bảng lương
Luồng:
Quản trị viên chọn loại báo cáo (Tổng giờ làm hoặc Tổng lương tính đến hiện tại).
Hệ thống tạo báo cáo và lưu lại nếu được yêu cầu.


![Diagram](http://www.plantuml.com/plantuml/png/TP113i8W44Ntd6AMDOOBDCOqQkAcExd0n3P80anIg8cftbsGia1Ibe__PZvqpkFaPwFPNQDpS48w8y7281mE1XDeuUOdPUMAhSINYFI2VlonFNYab6rsBJn93Up3Yg5NHJqQMCfyvbjMFvELbPHmxOXGyY5ogDOQJQZoOuATQFHNu_3clEXRNwJTx6yLvySyhHlj47_q2m00)




4. Tạo Báo Cáo Nhân Viên (Create Employee Report)
Mô tả: Nhân viên tạo báo cáo cho các hạng mục như Tổng số giờ làm hoặc Nghỉ phép còn lại.
Tác nhân: Nhân viên
Luồng:
Nhân viên chọn loại báo cáo.
Hệ thống hiển thị báo cáo và cho phép lưu nếu cần.


![Diagram](http://www.plantuml.com/plantuml/png/VP712eCm38RlVOeS7QCl86F8TjXbo62oUvXY2zeChRkulVigaa4iscE_V7-JDEizTdve6_LiiE_XX7H6oWswXwqSZ0h2qT3Y35Au-yww-d_DbGBimIFDGh9BuKssL5ybNYZ8rHTBC4g1mQgNryRUJFMAHIPhvdK8oJcsiSaaDeimaYcGv5RY12P9GsXv5I5DqYbtaNJuQ2qtib714swKy2XgfNEjZykciigLq___0000)



5. Quản Lý Đơn Hàng Mua (Maintain Purchase Order)
Mô tả: Nhân viên nhận hoa hồng quản lý đơn hàng mua (thêm, sửa, xóa).
Tác nhân: Nhân viên nhận hoa hồng
Luồng:
Nhân viên chọn chức năng (Thêm, Cập nhật, Xóa đơn hàng).
Cung cấp thông tin đơn hàng.
Hệ thống thực hiện chức năng tương ứng.

![Diagram](http://www.plantuml.com/plantuml/png/ZP0n3e8m58RtdkAD6i8560o3WmCn6hZ0apQqIVjgQ6ianhiBvjK49Xa_llxvsZf476DoLlGMGu2ZfnFI02y1yrU2GoOLj74qD32FYbgaYqQt-H5ya_oY6ugC1eCLI9zkLdr90HQdJizMPuZdT_lVpbjmopKXDTEwg82ebSk7P6vZC8yyl95izdW_Qup_oK-FMTpUEPjBsRgfB0zvJTIAvFAE7m00)


6. Chạy Bảng Lương (Run Payroll)
Mô tả: Hệ thống tự động chạy bảng lương vào mỗi thứ Sáu và ngày làm việc cuối tháng.
Tác nhân: Hệ thống Bảng Lương (tự động)
Luồng:
Hệ thống chọn danh sách nhân viên cần được trả lương.
Tính toán lương và các khoản khấu trừ.
Gửi lệnh trả lương hoặc tạo phiếu lương.


![Diagram](http://www.plantuml.com/plantuml/png/PP2n3i8W48PtdkB66jCNw60Q7NGmBXBtioM5XDubBPYOndSN34M9RDp7z_z0EpkSd1-jw2pECrmqqiqeWaL0M3MCk8uQkBh9q920zKo3r8gFXXlesT-j-aK7tYCLO0lEa3v7M6qoUObKVL9I1nIiuNC6bcHr6fznciq7c_xhoH0g6QcKN9fMj5u_lwte_ckjwrqPAOfTv3b9j8hw-7bl)


7. Chọn Phương Thức Thanh Toán (Select Payment Method)
Mô tả: Nhân viên chọn phương thức thanh toán (nhận tại văn phòng, chuyển khoản, hoặc gửi qua bưu điện).
Tác nhân: Nhân viên
Luồng:
Nhân viên chọn phương thức thanh toán.
Hệ thống cập nhật thông tin thanh toán của nhân viên.



![Diagram](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuKhEIImkLl3BICmBoqpDKwZcKW02NONSH9YGbK9mIL5cNZfKeY2ZD3ylFIIZD3a4g20Z93yHg280Kn2iN5iXEIC_3uki1i8OhBerhHJAyZDJk6gve0x4L8FiLeGiccjBKlDmo6ahv2HMXcI0f3Bp4ExIX2a2MGqF5LrTEwn-T4ZDIm458W00)
