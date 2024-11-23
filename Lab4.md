I Thiết kế biểu đồ ca sử dụng (Use Case Diagram)



![Diagram](http://www.plantuml.com/plantuml/png/TPBBJiCm44Nt_efHzn5gIxj021Kg12mGLKe_OEfCMwj-XB6pY13_JfmcZi8ZgoJdwCxesYiVa4Dbj40P7CFaqPJQrKGJG0zaolx_SmwlQF58t98Jzs23DJkjuUrmKBAZhdrFoWFQCsnh7yYqUDzy2y4a0zgZffIHd4y1pLDvakWRV1aC_MgGatHS-3PhjvwEvJLgMMaC15lKo7LdpSRM4rdYA3MZvOdakTFcVqv-LuOaSj59rsDfmqwIzp7Aa0sTjFXdO4wbuz0llnHVGf0f8SlkOZBSm6HRxOqAmr1nuWvF8xulYgjTMSIiT5ZYqdZlpQBtObLGGm_G5wES_UdFe_-x4X59DEA1jPkHBKPu0RTPbl3QsODYaueO5bz6dDD7HJwa1iIgYOjNxni0)
 Use Case: Manage Employee Records
![Diagram](http://www.plantuml.com/plantuml/png/TSzD2i8m4CNnVKunPDyhI5q8sGWIyG13ykWc7oKp5O9uT-kYe1PdEJ_umnj5kUcIa-6WjP5rdivSU4Apn4BEcuQWNAO4iXVkhQP4rowAREbXQBr545XMFiP8fpodsW7xJRSvikAVUkHw_zIdCSxJC1n-ejjtrzjWdnfHudl)



HR Manager thực hiện thêm, cập nhật, hoặc xóa thông tin nhân viên.
Tất cả các hành động này được thực hiện trực tiếp thông qua hệ thống "Payroll System".










 Use Case: Calculate Salary





 
![Diagram](http://www.plantuml.com/plantuml/png/RT312i8m30RWUvyYzBuNy20JHV6aE5yWT9aMicwawQ68x-va3b7QKmaVVtvIHqNHrBD1fuE0FMEMWHbENUSTYGMCozy8ESLmO_go9aUbtiB3mFHI98UHmEv9tHsklYU7qi8E5Usls8mZPsYGKJ9S4bFy0mSA9AYqc3dZQSod3LJLkhm8Ld0CNZqgmHRP9KRrGp1bFCMKsvI6iovNgocqxqE-0000)



Payroll Officer bắt đầu quá trình tính toán lương.
Hệ thống truy xuất dữ liệu từ bảng chấm công, áp dụng quy tắc tính lương, và tạo dữ liệu lương cuối cùng.





 Use Case: Generate Paycheck


 
![Diagram](http://www.plantuml.com/plantuml/png/RO_Dgi9038NtUOh3xFi2Tt4fxbmfz0b2J6jnEYEPT574TxVrHn6xIiZtSSAfYxFvE4HYyMm8UvuinuXTs_QY5i3bjPEfEASkwaThfk8w15m80CQYmcN1fcSsnQp9KUKKld6ZwV1cy8mDfzcv4ZrVeQh-rr9-JmzpFH1_zubjSksClS-9wjbSwju0)


Payroll Officer chuẩn bị phiếu lương dựa trên dữ liệu lương đã tính.
Phiếu lương được gửi trực tiếp đến ngân hàng để xử lý thanh toán.


 Use Case: Manage Timecard



 
![Diagram](http://www.plantuml.com/plantuml/png/ROz12i9034NtESLdzhs02waBmQLOBn3R88LCfsHIOH3lxaWtIbtclIIVtsPdyoKgSU_948vnrbH40ZYZ3cJIEqzt5OGp5qkgw4fsYG5F0e0bIy-vwcwvnT5n7MC5DeHVUvXdIm_vqY-Y6e2csV-vtP1rR_C5EvmkM34hjJ8DdpPl)


Employee gửi bảng chấm công cho hệ thống.
Hệ thống chuyển dữ liệu bảng chấm công đến bộ phận HR để phê duyệt.





 Use Case: Process Payment


 
![Diagram](http://www.plantuml.com/plantuml/png/TP1Foi903CNtEKMOVI_mBJwA22ujz0HXJ4MSFv2aYoBUtUdW81OxgybxlpoIz6eaDiS0v2qBke4MoI7WUPfkdiKXQVitv43fZkEYnh7QQmt2tYXT0tyY6l80B6zMzgJ5Fd5Y8MCiNEHaU2GZzysCd2uR_mdmd)



Payroll Officer kích hoạt quá trình xử lý thanh toán.
Hệ thống tạo dữ liệu thanh toán và gửi đến ngân hàng thông qua tích hợp hệ thống.

 Use Case: Generate Reports

 
![Diagram](http://www.plantuml.com/plantuml/png/RSynoiCm30NWNQTuUCy5_k4dMxEKbgGN4EaZY-C4MHv2wTthG2cKHkFJ9mcrsTMyp55qzCKGkXvdJJhH0ZIZwyKukgOf4k6gcoqnOjYoSmvu26gLp55pRG-CrQBdkfZZjgqCt-34H5FdcmHvYjI3JVD_F7mKxlft4_xmYIx5r-BICjttnru0)


HR Manager chọn loại báo cáo cần tạo (chấm công, bảng lương...).
Hệ thống tạo báo cáo theo định dạng được yêu cầu.
