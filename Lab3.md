I Subsystem context diagrams
Hãy vẽ biểu đồ ngữ cảnh của các hệ thống con và giải thích.

1 Biểu đồ cho hệ thống con Hệ thống Ngân hàng (BankSystem)




![Diagram](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuKhEIImkLd1wk7lcaGcP3tStbdfd0AdcFAU7knRdfViSst1iOLwwGZMN0X2KP3pSlJ7P0oZVdkUSyN3NmaeKLHgQNBLSN9bv9Qb5QOd9gGgUxfc9-IvWrNxfXnVbUHnU03Sg_U7kjPaX80lpD99GhB9IG35K1sZhuIrvwI6PS4F0Ya8mHK7MG_tZ0RGq1EZQYNdfTBOQrGY863OTN5o4mbnNrmv745gX-46J2xigcnfTNUm1WKq3n49ar-DJXzL73gbvAQ0a1G00)


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

III Design Element to Owning Package Map

## BankSystem

| **Design Element**      | **Owning Package**   | **Giải thích**                                                                 |
|--------------------------|----------------------|--------------------------------------------------------------------------------|
| `PayrollController`      | `BankSystem.Control`| Được đặt trong package điều khiển (control) vì nó xử lý logic chính liên quan đến bảng lương. |
| `IBankSystem`            | `BankSystem.Interface` | Được đặt trong package giao diện vì nó chỉ định các chức năng phải được triển khai. |
| `BankSystem`             | `BankSystem.Implementation` | Lớp thực thi nằm trong package triển khai.                                     |
| `Paycheck`               | `BankSystem.Entity` | Lớp đại diện dữ liệu nằm trong package thực thể.                              |
| `BankInformation`        | `BankSystem.Entity` | Lớp lưu thông tin ngân hàng nằm trong package thực thể.                       |

## PrintService

| **Design Element**      | **Owning Package**         | **Giải thích**                                                                 |
|--------------------------|----------------------------|--------------------------------------------------------------------------------|
| `PayrollSystem`          | `PrintService.Control`    | Lớp chính điều khiển, được đặt trong package điều khiển.                      |
| `IPrintService`          | `PrintService.Interface`  | Đặt trong package giao diện vì định nghĩa các chức năng in ấn.                 |
| `PrintService`           | `PrintService.Implementation` | Đặt trong package triển khai vì thực thi các chức năng in ấn.                 |
| `Employee`               | `PrintService.Entity`     | Lớp dữ liệu cho nhân viên thuộc package thực thể.                             |
| `Paycheck`               | `PrintService.Entity`     | Lớp dữ liệu cho phiếu lương thuộc package thực thể.                           |

## ProjectManagementDatabase

| **Design Element**           | **Owning Package**             | **Giải thích**                                                                 |
|-------------------------------|---------------------------------|--------------------------------------------------------------------------------|
| `PayrollSystem`               | `ProjectManagement.Control`    | Lớp chính điều khiển thuộc package điều khiển.                                |
| `IProjectManagementDatabase`  | `ProjectManagement.Interface` | Giao diện định nghĩa các chức năng quản lý dự án, thuộc package giao diện.    |
| `ProjectManagementDatabase`   | `ProjectManagement.Implementation` | Lớp thực thi các chức năng quản lý dự án, thuộc package triển khai.          |
| `Employee`                    | `ProjectManagement.Entity`     | Lớp dữ liệu đại diện cho nhân viên thuộc package thực thể.                   |
| `ProjectData`                 | `ProjectManagement.Entity`     | Lớp dữ liệu lưu trữ thông tin dự án thuộc package thực thể.                  |


IV Architectural layers and their dependencies


![Diagram](http://www.plantuml.com/plantuml/png/VT0nJyCm40NWtR_YvBrYHrNKHB2nb8W9CHpE4rWaZl6T4G7ntyabS-l9p_wURDr9b8lMQNIPmmU_WNo_Y6AYjeJtg0XQ2ppzEbfNcASy9oIbv-Dnv0MbQQZDUOo1DSxfXLWiNyPTbPWWGZtALmoGhTB5dykLErQcDgnsnvQlwrSMxBHp9krBT3WqzWxTak-H1dh4PuMeU1DsOsAh6pbNbENcAG-is0vtPhlTTQRkln7g2lhp0raZGhpxSoUamKRg_W40)


Application Layer

Là tầng đầu tiên, nhận tất cả yêu cầu từ người dùng.
Có thể bao gồm các giao diện đồ họa (GUI) hoặc giao diện dòng lệnh (CLI).
Business Services Layer

Chịu trách nhiệm thực thi toàn bộ logic nghiệp vụ của hệ thống, ví dụ: tính toán tiền lương, quản lý dự án.
Phối hợp dữ liệu từ tầng Data Access và gửi lại kết quả cho Application.
Data Access Layer

Tầng trung gian giữa Business Services và Database.
Thực hiện các tác vụ như xử lý giao tiếp với cơ sở dữ liệu hoặc các API bên ngoài.
Database Layer

Nơi lưu trữ dữ liệu.
Hỗ trợ các hệ quản trị cơ sở dữ liệu như MySQL, PostgreSQL, hoặc Oracle DB.

