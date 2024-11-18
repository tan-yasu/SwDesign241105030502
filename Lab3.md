I Subsystem context diagrams
Hãy vẽ biểu đồ ngữ cảnh của các hệ thống con và giải thích.
![Diagram](http://www.plantuml.com/plantuml/png/encoded-diagram-text)
1 Biểu đồ cho hệ thống con Hệ thống Ngân hàng (BankSystem)


![Diagram](http:////www.plantuml.com/plantuml/png/SoWkIImgAStDuKhEIImkLd1wk7lcaGcP3tStbdfd0AdcFAU7knRdfViSst1iOLwwGZMN0X2KP3pSlJ7P0oZVdkUSyN3NmaeKLHgQNBLSN9bv9Qb5QOd9gGgUxfc9-IvWrNxfXnVbUHnU03Sg_U7kjPaX80lpD99GhB9IG35K1sZhuIrvwI6PS4F0Ya8mHK7MG_tZ0RGq1EZQYNdfTBOQrGY863OTN5o4mbnNrmv745gX-46J2xigcnfTNUm1WKq3n49ar-DJXzL73gbvAQ0a1G00)


PayrollController: Là bộ điều khiển chính, chịu trách nhiệm khởi chạy quy trình bảng lương.
IBankSystem: Giao diện định nghĩa phương thức deposit() để chuyển tiền vào tài khoản ngân hàng.
BankSystem: Hệ thống ngân hàng thực thi giao diện IBankSystem và xử lý các giao dịch gửi tiền.
Paycheck: Đại diện cho phiếu lương cần được xử lý.
BankInformation: Thông tin chi tiết về ngân hàng nơi phiếu lương sẽ được gửi.

 2. Biểu đồ cho hệ thống con PrintService

![Diagram](http://www.plantuml.com/plantuml/png/jL7B2i8m4BplL-on1VC3HQGN3zuA_O8OLooc3vEj4DH_Dobh8NesfyaCCplBrfwruxctOAps7XiTt6Xj6pnJZm_0-1pTPl8SfPRdO-EwWOiINW0Ha3jhGtXOs9RSlJCajYbHOYged-mOYB32lS0DJZgO2vbh91k1ALUg_2DIAFb-R03vsahjlZQgyj4bvFBsgLJMDzUNm7NshxJsg6aufLky0G00)

PayrollSystem: Hệ thống bảng lương gửi yêu cầu in phiếu lương.
IPrintService: Giao diện định nghĩa phương thức printPayStub() để in phiếu lương.
PrintService: Thực thi giao diện IPrintService, xử lý logic in ấn.
Paycheck: Dữ liệu bảng lương được in trên phiếu lương.
Employee: Thông tin về nhân viên nhận phiếu lương.

3. Biểu đồ cho hệ thống con ProjectManagementDatabase

![Diagram](http://www.plantuml.com/plantuml/png/pPBFJe0m3CRlVOeT8N4lG8p1H1Czc91uy5n74NL_o5OEH7rtDrmG4jbPJYtzlkxNRcrWz3mR3KfZ2AB3nJkj7vV0PCG7YFWDn6hil7iZnJV8U6tx9-VVxzpiGrN35y2hPV83AXBtMVU05b_8a5qTpnZef5b5Pj9k8HADkCrX7UETPFNDKuzCsxb_sIx4c4hnJ-H9N7cc_uUqrNEwxmp7Av3oghJKveS-vLKD1U7bfvJdcoWv8y4lRrbt6AGbswU71Ty0)

PayrollSystem: Hệ thống bảng lương yêu cầu lấy dữ liệu dự án và cập nhật giờ làm việc của nhân viên.
IProjectManagementDatabase: Giao diện cho cơ sở dữ liệu quản lý dự án, định nghĩa các phương thức fetchProjectData() và updateWorkHours().
ProjectManagementDatabase: Thực thi giao diện IProjectManagementDatabase, xử lý dữ liệu dự án và giờ làm việc.
Employee: Thông tin chi tiết về nhân viên liên quan đến dự án.
ProjectData: Dữ liệu cụ thể của dự án mà nhân viên tham gia.


II.Analysis class to design element map


1. Hệ thống con: BankSystem

| **Analysis Class**      | **Design Element**            | **Giải thích**                                                                 |
|--------------------------|-------------------------------|--------------------------------------------------------------------------------|
| PayrollController        | PayrollController            | Lớp điều khiển chính được giữ nguyên vì nó đã được định nghĩa rõ ràng trong phân tích. |
| IBankSystem              | IBankSystem (Interface)      | Được ánh xạ trực tiếp thành một giao diện vì nó định nghĩa các chức năng cần triển khai. |
| BankSystem               | BankSystem (Class)           | Lớp thực thi cụ thể giao diện `IBankSystem`.                                   |
| Paycheck                 | Paycheck (Entity Class)      | Được ánh xạ giữ nguyên vì đây là một lớp dữ liệu.                              |
| BankInformation          | BankInformation (Entity Class) | Được giữ nguyên trong thiết kế vì nó chứa dữ liệu tĩnh về ngân hàng.            |


2. Hệ thống con: PrintService

| **Analysis Class**      | **Design Element**            | **Giải thích**                                                                 |
|--------------------------|-------------------------------|--------------------------------------------------------------------------------|
| PayrollSystem            | PayrollSystem                | Lớp chính xử lý các quy trình liên quan đến bảng lương, được giữ nguyên.       |
| IPrintService            | IPrintService (Interface)    | Giao diện định nghĩa các chức năng in phiếu lương.                             |
| PrintService             | PrintService (Class)         | Lớp thực thi giao diện `IPrintService`.                                        |
| Employee                 | Employee (Entity Class)      | Lớp dữ liệu cho nhân viên, giữ nguyên từ phân tích sang thiết kế.              |
| Paycheck                 | Paycheck (Entity Class)      | Giữ nguyên vì nó là một phần quan trọng của phiếu lương.                       |


3. Hệ thống con: ProjectManagementDatabase

| **Analysis Class**           | **Design Element**                      | **Giải thích**                                                                 |
|-------------------------------|-----------------------------------------|--------------------------------------------------------------------------------|
| PayrollSystem                 | PayrollSystem                          | Lớp chính điều khiển, được giữ nguyên từ mô hình phân tích.                    |
| IProjectManagementDatabase    | IProjectManagementDatabase (Interface) | Giao diện định nghĩa các chức năng quản lý dữ liệu dự án.                      |
| ProjectManagementDatabase     | ProjectManagementDatabase (Class)      | Thực thi các chức năng được định nghĩa trong `IProjectManagementDatabase`.     |
| Employee                      | Employee (Entity Class)                | Lớp đại diện cho nhân viên, giữ nguyên từ phân tích sang thiết kế.             |
| ProjectData                   | ProjectData (Entity Class)             | Lớp lưu trữ thông tin chi tiết về các dự án của nhân viên.                     |


