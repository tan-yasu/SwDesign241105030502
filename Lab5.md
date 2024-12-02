I.biểu đồ hệ thống con (Subsystem Design) cho hệ thống Payroll System dựa vào kết quả phân tích trong Lab 4.


![Diagram](http://www.plantuml.com/plantuml/png/encoded-diagram-text)



![Diagram](http://www.plantuml.com/plantuml/png/hPJFQiCm3CRlUGgJUrzWXr7sXx73e2nz0SqH8JIHWwqEmjYxBo9E1IPnDfYF-dxw-2gfEGO6pzU-AmQm5sZGb2SOlUiwKus1iI_DLs6cTvEV-w5p8w9v0veAFHARwleHb8xFTX22yZFkoorTXQJ370xtjvgvC-LSd_dl8gPBmf-yinX2IqqsNCGZxNov0iWlV086rPAkEQ6I825VaD03RyGyjprQyFNlXgZy-X1LLq4xT8XBRM-83q0NyqgCZGTk7MMZ2VpeYD3ozlpE7YY05JD5j9DrXWajKIkaUZteEmxEiv5PxoUDT8GrQw9hEU4bOQojBNZAjlVV48FyXOhn97osDUh9pyUdD_CVvejPDCytYdV-AkAMbWN-mJMxGWsSE1-HQlbe_G00)



Employee Management Subsystem:

Nhiệm vụ: Quản lý thông tin nhân viên như tên, mã số nhân viên, phòng ban.
Lớp chính:
EmployeeManager: Thực hiện các thao tác thêm, sửa, xóa nhân viên.
Employee: Đại diện cho thông tin nhân viên.
Payroll Processing Subsystem:

Nhiệm vụ: Tính toán lương dựa trên dữ liệu nhân viên và bảng chấm công.
Lớp chính:
PayrollProcessor: Xử lý các quy trình liên quan đến tính toán lương.
PaymentData: Chứa dữ liệu thanh toán đã xử lý.
Timecard Management Subsystem:

Nhiệm vụ: Quản lý bảng chấm công của nhân viên.
Lớp chính:
TimecardManager: Ghi nhận thời gian làm việc, duyệt thẻ chấm công.
Timecard: Đại diện cho dữ liệu chấm công của nhân viên.
Bank Integration Subsystem:

Nhiệm vụ: Gửi dữ liệu thanh toán đến ngân hàng.
Lớp chính:
BankConnector: Kết nối và gửi dữ liệu thanh toán.
PaymentTransaction: Đại diện cho giao dịch thanh toán.
Report Generation Subsystem:

Nhiệm vụ: Tạo báo cáo về các thông tin như lương, chấm công, và thanh toán.
Lớp chính:
ReportGenerator: Xử lý việc tạo báo cáo.
Report: Đại diện cho nội dung báo cáo.Employee Management Subsystem:

Nhiệm vụ: Quản lý thông tin nhân viên như tên, mã số nhân viên, phòng ban.
Lớp chính:
EmployeeManager: Thực hiện các thao tác thêm, sửa, xóa nhân viên.
Employee: Đại diện cho thông tin nhân viên.
Payroll Processing Subsystem:

Nhiệm vụ: Tính toán lương dựa trên dữ liệu nhân viên và bảng chấm công.
Lớp chính:
PayrollProcessor: Xử lý các quy trình liên quan đến tính toán lương.
PaymentData: Chứa dữ liệu thanh toán đã xử lý.
Timecard Management Subsystem:

Nhiệm vụ: Quản lý bảng chấm công của nhân viên.
Lớp chính:
TimecardManager: Ghi nhận thời gian làm việc, duyệt thẻ chấm công.
Timecard: Đại diện cho dữ liệu chấm công của nhân viên.
Bank Integration Subsystem:

Nhiệm vụ: Gửi dữ liệu thanh toán đến ngân hàng.
Lớp chính:
BankConnector: Kết nối và gửi dữ liệu thanh toán.
PaymentTransaction: Đại diện cho giao dịch thanh toán.
Report Generation Subsystem:

Nhiệm vụ: Tạo báo cáo về các thông tin như lương, chấm công, và thanh toán.
Lớp chính:
ReportGenerator: Xử lý việc tạo báo cáo.
Report: Đại diện cho nội dung báo cáo.




II.biểu đồ riêng cho từng hệ thống con trong Payroll System, được minh họa theo từng Subsystem
1. Employee Management Subsystem



![Diagram](http://www.plantuml.com/plantuml/png/RP0n3i8m34NtdCBA14Az00Fg00C3KqzW6gkgID8eTeSAzUwq2eK8ul6zB_tyr2mOPNHM1MmVs17eYmjsc8ZWXdu1Zhn0CzvvOY6duQbWkTOYypUReZ7PT0T0OpQ_ssTy30Q5YigGfJyrbnhpgWheJQzdE48ZiVTTPZqwAl4mS2_zu4lEKC0ew_ZSRe_vsGrLTVgm9QyJrsfMDNcpVgzw0G00)



EmployeeManager chịu trách nhiệm quản lý danh sách nhân viên, bao gồm thêm, sửa, xóa thông tin.
Employee lưu trữ thông tin của từng nhân viên.




2. Payroll Processing Subsystem



 
![Diagram](http://www.plantuml.com/plantuml/png/NT312iCW30RWkqyHF6sCli0EeuV2sAtG9qXTA6DHYyQ3ZBxxBBH5cek7BoQ_jb4mIBAiPZHVd0XqZpbuPkY3DnJZnqqmf37cA6Gr_1IKCemn7grRfmyxhtK3WsmIez20Z25VhfLDv2WKAXCiEUbGSFFbj63dUdO3Q7ro0dVeV1gPAY4xiyz4hwxe8A7ahtG-1bBXzQYMdfy3JVE0AaAvePzRSAqMrP9xhr_t1m00)



PayrollProcessor thực hiện tính toán lương dựa trên dữ liệu nhân viên và bảng chấm công.
PaymentData chứa thông tin thanh toán, bao gồm số tiền, mã nhân viên, và ngày thanh toán.



3. Timecard Management Subsystem


 
![Diagram](http://www.plantuml.com/plantuml/png/RP3DQeGm483lUOeXfvRY2_HGF7Znq9E5dgV9O4NpmsGiIF7TDwBkXiKvVj-N8KcT15bcDwc8PiIUG7yDZWooXK_q6JZo0jtyavOav3JyAyXZ9apfqUufdtQRDs0oWUsMlBmM66Fay4VdqSEjLslBVHN8GTi6tg4J7dnVM79n2WlHjVqDCwVlm2FPh5ilr1CNtg9G5WqA5TTvUXvKrSUTvLhlNAjLrUJjzeit)



TimecardManager quản lý các thẻ chấm công của nhân viên, ghi nhận và duyệt thời gian làm việc.
Timecard chứa thông tin từng thẻ chấm công, bao gồm mã thẻ, giờ làm việc, và ngày chấm công.



4. Bank Integration Subsystem



 
![Diagram](http://www.plantuml.com/plantuml/png/PP31Ii0m38RlVOhGao9x0GyoTPVTXFa2MHV6s9fAanw6xDtjh637SYdq-p_wDwqeHar-Cr_eLfm9x1lo2ZqhpH5r2Gn36cKN9M_Xsq0Ujw582Ru7Pd8QOc5bda28fm_SFR4-FFxU7xNvXpuZig0x7wdr1lGVz1qymw1nuRaAe0-9DPCkf76ZYep8wwjp1Tz5KTGaLrAgNNu3JVC2zvRPimFnPCrXsdoUU_i1)




BankConnector kết nối với hệ thống ngân hàng để gửi thông tin thanh toán.
PaymentTransaction lưu chi tiết giao dịch thanh toán, bao gồm số tiền, tài khoản, và trạng thái.








5. Report Generation Subsystem




 
![Diagram](http://www.plantuml.com/plantuml/png/RP312i8m343l_OhGaoBx0G-oWoBUnFa3TOOnx9gIPeSY-tUThU3SSdplqT2KGGnBtrdbJVqm3OA-e2SMEA93DjAIWwg_XHW4EmrF1U-fhGdXM-QGEDaq6sWInaFdBKN45A_M2ydPH2Ph9yKmN_JxVW7yOQSzRA4IRbq)



ReportGenerator tạo các báo cáo liên quan đến nhân viên hoặc bảng lương.
Report lưu trữ nội dung của từng báo cáo, bao gồm loại báo cáo và nội dung chi tiết.


