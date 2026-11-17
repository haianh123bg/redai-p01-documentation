## Tổng quan Quản lý Nguồn dữ liệu (Database Sources)

Trong kiến trúc cơ sở dữ liệu động **RedAI Database**, **Nguồn dữ liệu (Database Sources)** đóng vai trò là cầu nối vật lý và tầng trừu tượng hóa liên kết giữa Không gian làm việc (**Base**) với các hệ quản trị cơ sở dữ liệu (DBMS) mạnh mẽ bên ngoài cũng như các kết nối nội bộ. Thay vì bị giới hạn trong một kho lưu trữ duy nhất, tính năng này cho phép doanh nghiệp kết nối trực tiếp các cụm cơ sở dữ liệu chuyên dụng, đồng bộ schema, phân tách lưu trữ và tối ưu hóa hiệu năng truy vấn cho từng phân hệ nghiệp vụ.

Hệ thống hỗ trợ kết nối đa dạng với các nhà cung cấp cơ sở dữ liệu tiêu chuẩn công nghiệp:
- **PostgreSQL**: Cơ sở dữ liệu quan hệ mã nguồn mở mạnh mẽ, hỗ trợ mở rộng và toàn vẹn dữ liệu giao dịch phức tạp.
- **MySQL / MariaDB**: Hệ quản trị cơ sở dữ liệu quan hệ phổ biến cho các ứng dụng web và thương mại điện tử tốc độ cao.
- **SQL Server (MSSQL)**: Hệ quản trị cơ sở dữ liệu doanh nghiệp của Microsoft dành cho các hệ thống ERP, kế toán và tài chính.
- **Oracle Database**: Nền tảng dữ liệu hiệu năng cao quy mô tập đoàn lớn.
- **MongoDB**: Cơ sở dữ liệu tài liệu NoSQL linh hoạt, tối ưu cho dữ liệu phi cấu trúc và biến động nhanh.
- **Redis**: Bộ nhớ đệm (In-memory Cache / Key-Value Store) siêu tốc phục vụ tra cứu tức thời.
- **SQLite**: Cơ sở dữ liệu nhúng nhẹ gọn cho các môi trường kiểm thử hoặc ứng dụng độc lập.

---

### Các lợi ích cốt lõi của tính năng Nguồn dữ liệu

| Lợi ích nghiệp vụ | Ý nghĩa vận hành chi tiết |
| :--- | :--- |
| **Quản lý đa kết nối (Multi-Source Hub)** | Cho phép một Base liên kết đồng thời nhiều máy chủ cơ sở dữ liệu khác nhau, phân chia bảng dữ liệu theo từng mục đích (ví dụ: Bảng khách hàng lưu trên PostgreSQL chính, Bảng log lịch sử lưu trên MongoDB, Dữ liệu cache lưu trên Redis). |
| **Cơ chế Nguồn mặc định (Default Source)** | Chỉ định một nguồn dữ liệu làm kho lưu trữ vật lý ưu tiên. Khi tạo bảng mới trong Base, hệ thống sẽ tự động trỏ vị trí lưu trữ vào nguồn mặc định này mà người dùng không cần phải chọn thủ công. |
| **Kiểm soát vòng đời và độ sẵn sàng** | Cho phép quản trị viên chủ động chuyển đổi trạng thái **Bật** hoặc **Tắt** nguồn dữ liệu để phục vụ công tác bảo trì định kỳ, nâng cấp hạ tầng mà không làm gián đoạn cấu trúc bảng. |
| **Tích hợp liền mạch qua Integration Hub** | Tận dụng cơ chế xác thực an toàn, mã hóa thông tin xác thực (Credential Encryption) và kết nối proxy bảo mật đã được thiết lập trước từ phân hệ Tích hợp (**Integration Hub**). |
| **Tương thích hoàn hảo với AI Agent** | Cung cấp định danh duy nhất (`Source ID`) để trợ lý ảo AI Agent có thể truy vấn danh mục bảng, kiểm tra độ sẵn sàng của kết nối và hỗ trợ tự động hóa luồng dữ liệu thời gian thực. |

---

## Mở khu vực Quản lý Nguồn dữ liệu

Người dùng có thể truy cập khu vực Quản lý Nguồn dữ liệu bằng một trong ba cách sau:

| Phương thức truy cập | Thao tác thực hiện trên màn hình |
| :--- | :--- |
| **Cách 1 — Thanh công cụ Database** | Tại màn hình làm việc chính `Trang chủ > Database`, nhấp vào biểu tượng <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Tùy chọn khác)** ở góc trên bên phải thanh công cụ $\rightarrow$ chọn mục <img src="https://api.iconify.design/lucide:plug.svg?color=%23ff3333" width="16" alt="" /> **Nguồn dữ liệu**. |
| **Cách 2 — Thanh điều hướng Breadcrumb** | Nhấp vào đường dẫn điều hướng phía trên tiêu đề trang: `Trang chủ > Database > Nguồn dữ liệu`. |
| **Cách 3 — Đường dẫn URL trực tiếp** | Nhập trực tiếp đường dẫn URL quản trị vào trình duyệt: `https://app.redai.vn/w/<workspaceId>/b/<baseId>/database/sources` (trong đó `<workspaceId>` và `<baseId>` là định danh của Không gian làm việc và Base hiện tại). |

---

## Bố cục giao diện Quản lý Nguồn dữ liệu

Màn hình Quản lý Nguồn dữ liệu được thiết kế trực quan, phân chia thành 2 khu vực chức năng chính:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ Q Tìm theo tên nguồn hoặc connection... ]             [ + Tạo nguồn dữ liệu ]  [ ↻ Tải lại ]│
├────────────────────────────────────────────────────────────────────────────────────────────────┤
│  TÊN NGUỒN                  TRẠNG THÁI          KẾT NỐI             SOURCE ID          THAO TÁC│
│  CSDL Sản xuất  [Mặc định]  ● Đang hoạt động    [Icon] PostgreSQL   2c8b7...-4a1       [ ⋯ ]   │
│  PostgreSQL Kho Dữ Liệu     ● Đang hoạt động    [Icon] PostgreSQL   9a1f4...-9b2       [ ⋯ ]   │
│  MongoDB Log Sự Kiện        ○ Ngừng hoạt động   [Icon] MongoDB      e4d21...-8c3       [ ⋯ ]   │
└────────────────────────────────────────────────────────────────────────────────────────────────┘
```

1. **Thanh công cụ quản trị nguồn dữ liệu (Toolbar phía trên)**:
   - **Ô tìm kiếm**: `Tìm theo tên nguồn hoặc connection` — lọc tức thì danh sách nguồn dữ liệu theo từ khóa tên gợi nhớ, mã định danh hoặc loại kết nối máy chủ.
   - Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo nguồn dữ liệu** (Nút màu đỏ nổi bật): Mở hộp thoại cấu hình và khởi tạo nguồn dữ liệu mới.
   - Nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Tải lại**: Làm mới trạng thái kết nối và danh sách nguồn dữ liệu theo thời gian thực từ máy chủ.

2. **Bảng danh sách nguồn dữ liệu (Table)**:
   - Cột **Tên nguồn**: Hiển thị tên định danh gợi nhớ của nguồn (`alias`). Nếu nguồn này đang được cấu hình làm nguồn chính của Base, hệ thống sẽ hiển thị thêm huy hiệu màu tím/đỏ <span style="background-color: rgba(255, 51, 51, 0.1); color: #ff3333; padding: 2px 8px; border-radius: 9999px; font-size: 11px; font-weight: 600;">Mặc định</span>.
   - Cột **Trạng thái**:
     - <span style="color: #059669; font-weight: 500;">● Đang hoạt động</span> (kèm chấm tròn xanh ngọc): Nguồn dữ liệu sẵn sàng tiếp nhận các thao tác đọc và ghi bảng.
     - <span style="color: #6b7280; font-weight: 500;">○ Ngừng hoạt động</span> (kèm chấm tròn xám): Nguồn dữ liệu đang tạm tắt, tạm ngưng các thao tác ghi mới.
   - Cột **Kết nối**: Hiển thị biểu tượng logo đại diện của hệ quản trị cơ sở dữ liệu (PostgreSQL, MySQL, MariaDB, SQL Server, Oracle, MongoDB, Redis, SQLite), Tên kết nối tích hợp và Nhãn loại CSDL tương ứng.
   - Cột **Source ID**: Mã UUID định danh duy nhất của nguồn dữ liệu trong hệ thống, phục vụ tích hợp API và điều phối qua AI Agent.
   - Cột **Thao tác**: Nút mở menu ba chấm <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> chứa các lệnh quản trị chuyên sâu.

3. **Khung hiển thị trạng thái chưa có dữ liệu (Empty State)**:
   - Xuất hiện khi Base chưa liên kết với bất kỳ nguồn dữ liệu nào: Biểu tượng <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="32" alt="" />, Tiêu đề `Chưa có nguồn dữ liệu`, đi kèm lời nhắc: *"Tạo nguồn dữ liệu mới từ một connection database để bắt đầu đồng bộ."*

---

## Các tính năng và quy trình thao tác chi tiết

### Quy trình 1 — Khởi tạo nguồn dữ liệu mới từ Connection Database

Để liên kết một nguồn cơ sở dữ liệu mới vào Base hiện tại, người dùng thực hiện theo các bước sau:

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :--- | :--- | :--- |
| **1. Mở biểu mẫu tạo mới** | Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo nguồn dữ liệu** | Trên thanh công cụ, nhấp vào nút **Tạo nguồn dữ liệu** màu đỏ để mở hộp thoại cấu hình. |
| **2. Đặt tên nguồn dữ liệu** | Ô nhập liệu **Tên \*** | Nhập tên gợi nhớ có ý nghĩa nghiệp vụ vào ô `Nhập tên nguồn dữ liệu` (ví dụ: `PostgreSQL Máy Chủ Chính`, `CSDL Bán Hàng E-Commerce`).<br>*Trường này bắt buộc điền để người dùng và AI Agent dễ dàng nhận diện.* |
| **3. Chọn Connection Database** | Ô chọn **Connection \*** | Nhấp vào danh sách thả xuống `Chọn connection` để chọn một kết nối database đã được tích hợp sẵn trong Không gian làm việc.<br>• Mỗi mục trong danh sách hiển thị rõ biểu tượng logo, tên kết nối và loại CSDL (PostgreSQL, MySQL, MSSQL...).<br>• Hỗ trợ gõ phím để tìm kiếm nhanh kết nối mong muốn.<br>*Lưu ý: Nếu chưa có kết nối nào trong danh sách, người dùng cần truy cập phân hệ **Integration Hub** để thiết lập thông tin đăng nhập máy chủ database trước.* |
| **4. Xác nhận khởi tạo** | Nút **Tạo** | Nhấp vào nút **Tạo** màu đỏ ở góc dưới bên phải hộp thoại (hoặc bấm nút **Hủy** nếu muốn hủy bỏ thao tác). |

---

### Quy trình 2 — Bật hoặc Tắt trạng thái hoạt động của nguồn dữ liệu

Trong quá trình vận hành, khi cần bảo trì máy chủ dữ liệu hoặc tạm thời đóng băng quyền tạo mới bảng trên một cụm CSDL, quản trị viên có thể chuyển đổi trạng thái hoạt động:

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :--- | :--- | :--- |
| **1. Mở menu thao tác** | Nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên dòng nguồn | Di chuyển đến dòng nguồn dữ liệu cần cấu hình, nhấp vào nút menu ba chấm ở cột **Thao tác**. |
| **2. Chuyển đổi trạng thái** | Lệnh **Tắt source** / **Bật source** | • Nếu nguồn đang ở trạng thái hoạt động: Nhấp vào lệnh <img src="https://api.iconify.design/lucide:toggle-left.svg?color=%23ff3333" width="16" alt="" /> **Tắt source** để chuyển sang `Ngừng hoạt động`.<br>• Nếu nguồn đang tạm tắt: Nhấp vào lệnh <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="16" alt="" /> **Bật source** để kích hoạt lại trạng thái `Đang hoạt động`. |
| **3. Kiểm tra thông báo** | Thông báo nổi (Toast) | Hệ thống hiển thị thông báo góc trên màn hình: `Tắt source thành công` hoặc `Bật source thành công`. Nhãn trạng thái trên bảng lập tức đổi màu tương ứng. |

---

### Quy trình 3 — Thiết lập Nguồn dữ liệu làm Mặc định (Default Source)

Mỗi Base nên có một nguồn dữ liệu chỉ định làm mặc định. Khi người dùng hoặc AI Agent khởi tạo bảng mới mà không chỉ định rõ đích lưu trữ, bảng sẽ tự động được tạo trên nguồn dữ liệu mặc định này:

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :--- | :--- | :--- |
| **1. Mở menu thao tác** | Nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên dòng nguồn | Tại dòng nguồn dữ liệu mong muốn, nhấp vào nút menu ba chấm ở cột **Thao tác**. |
| **2. Chọn lệnh đặt mặc định** | Lệnh <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> **Đặt làm mặc định** | Nhấp vào mục **Đặt làm mặc định** (nếu nguồn này đã là mặc định, mục này sẽ chuyển thành biểu tượng <img src="https://api.iconify.design/lucide:check-circle.svg?color=%23ff3333" width="16" alt="" /> **Source mặc định** và ở trạng thái vô hiệu hóa). |
| **3. Ghi nhận thay đổi** | Huy hiệu **Mặc định** | Hệ thống tự động chuyển huy hiệu <span style="background-color: rgba(255, 51, 51, 0.1); color: #ff3333; padding: 2px 8px; border-radius: 9999px; font-size: 11px; font-weight: 600;">Mặc định</span> sang dòng nguồn dữ liệu mới và gỡ bỏ trạng thái mặc định của nguồn cũ trước đó trong cùng Base. |

---

### Quy trình 4 — Xóa nguồn dữ liệu (Xóa an toàn)

Khi một kết nối cơ sở dữ liệu không còn được sử dụng trong Base, quản trị viên có thể tiến hành xóa nguồn:

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :--- | :--- | :--- |
| **1. Chọn lệnh xóa** | Lệnh <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa source** | Nhấp vào menu ba chấm <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên dòng nguồn cần xóa $\rightarrow$ chọn lệnh **Xóa source**. |
| **2. Xác nhận trong hộp thoại** | Hộp thoại **Xóa source** | Hộp thoại cảnh báo xuất hiện với thông điệp: *"Bạn có chắc chắn muốn xóa source này?"* kèm theo tên định danh hoặc mã ID của nguồn dữ liệu. |
| **3. Xác nhận xóa vĩnh viễn** | Nút **Xóa** (Màu đỏ) | Nhấp vào nút **Xóa** màu đỏ để thực thi (hoặc nhấp nút **Hủy** để giữ lại nguồn dữ liệu). Dòng nguồn dữ liệu sẽ biến mất khỏi bảng danh sách ngay khi tiến trình xóa hoàn tất. |

---

## Kiểm tra kết quả

Sau khi thực hiện các thao tác quản trị trên giao diện Nguồn dữ liệu, người dùng kiểm chứng kết quả thành công thông qua các dấu hiệu trực quan sau:

| Thao tác vừa thực hiện | Dấu hiệu kiểm chứng trực quan trên giao diện |
| :--- | :--- |
| **Khởi tạo nguồn mới** | Thông báo nổi màu xanh: `Tạo nguồn dữ liệu thành công`. Dòng nguồn dữ liệu mới xuất hiện ngay trên đầu bảng với tên gợi nhớ, trạng thái `Đang hoạt động` và logo hệ quản trị CSDL chuẩn xác. |
| **Bật / Tắt nguồn** | Thông báo nổi: `Bật source thành công` hoặc `Tắt source thành công`. Chấm tròn trạng thái chuyển đổi tức thời giữa màu xanh ngọc (Đang hoạt động) và màu xám (Ngừng hoạt động). |
| **Đặt nguồn mặc định** | Thông báo nổi: `Đặt source mặc định thành công`. Huy hiệu `Mặc định` xuất hiện bên cạnh tên nguồn vừa chọn; các nguồn còn lại tự động mất huy hiệu này. |
| **Xóa nguồn dữ liệu** | Thông báo nổi: `Xóa source thành công`. Dòng nguồn biến mất hoàn toàn khỏi danh sách. Nếu không còn nguồn nào, giao diện tự động chuyển về trạng thái trống `Chưa có nguồn dữ liệu`. |
| **Tìm kiếm / Làm mới** | Khi gõ từ khóa vào ô tìm kiếm, bảng lập tức lọc chỉ hiển thị các nguồn thỏa mãn điều kiện. Bấm nút `Tải lại` xuất hiện vòng xoay làm mới và thông báo `Tải lại thành công`. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động tra cứu danh sách nguồn dữ liệu, kiểm tra trạng thái hoạt động của các máy chủ cơ sở dữ liệu và chỉ định nguồn dữ liệu lưu trữ khi khởi tạo các bảng nghiệp vụ.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản Không gian làm việc (Member, Editor, Admin hoặc Owner) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Xem danh sách nguồn dữ liệu và trạng thái hoạt động** | `listSources` | *"Hãy kiểm tra toàn bộ danh sách nguồn dữ liệu (Database Sources) hiện có trong Base này, liệt kê rõ tên nguồn, trạng thái bật/tắt và nguồn nào đang là mặc định."* |
| **Tra cứu danh mục bảng dữ liệu trực thuộc nguồn cụ thể** | `listTables` | *"Hãy liệt kê tất cả các bảng dữ liệu đang được lưu trữ trên nguồn dữ liệu 'PostgreSQL Máy Chủ Chính' và báo cáo số lượng bản ghi của từng bảng."* |
| **Chỉ định nguồn dữ liệu vật lý khi khởi tạo bảng mới** | `createTable` | *"Hãy tạo một bảng dữ liệu mới có tên 'Nhật Ký Giao Dịch API' và đặt nguồn lưu trữ dữ liệu tại source ID '2c8b7...-4a1' (nguồn PostgreSQL)."* |

---

### Câu lệnh mẫu chuyên sâu (Full Prompt Workflow)

```text
Hãy hỗ trợ tôi rà soát hạ tầng cơ sở dữ liệu và khởi tạo bảng dữ liệu trên nguồn chỉ định:

1. Bối cảnh & Yêu cầu:
- Tôi muốn kiểm tra tình trạng các nguồn cơ sở dữ liệu đang kết nối vào Base này trước khi triển khai phân hệ quản lý tài chính.
- Bảng mới cần được lưu trữ trên nguồn PostgreSQL chuyên dụng thay vì nguồn mặc định dùng chung.

2. Các bước thực hiện:
- Bước 1: Gọi công cụ listSources để lấy toàn bộ danh sách nguồn dữ liệu hiện có trong Base.
- Bước 2: Xác định nguồn dữ liệu có tên "PostgreSQL Máy Chủ Chính" hoặc loại "POSTGRESQL", kiểm tra xem trạng thái có đang là "enabled" (Đang hoạt động) hay không và ghi nhận Source ID tương ứng.
- Bước 3: Gọi công cụ createTable để khởi tạo bảng dữ liệu mới mang tên "Sổ Cái Kế Toán 2026" với mô tả "Lưu trữ toàn bộ chứng từ thu chi và bút toán hạch toán tài chính", đồng thời trỏ nguồn lưu trữ vào đúng Source ID đã tìm thấy ở Bước 2.
- Bước 4: Gọi getTable để đọc lại cấu hình và xác nhận bảng đã được liên kết chính xác với nguồn cơ sở dữ liệu chỉ định.

3. Kết quả báo cáo:
- Tóm tắt danh sách các nguồn dữ liệu đang hoạt động trong Base.
- Cung cấp mã định danh bảng, tên bảng và tên nguồn lưu trữ vật lý của bảng vừa tạo.
```

---

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo nguồn dữ liệu** và điền tên, chọn connection | Gọi `listSources` lập tức thấy xuất hiện bản ghi nguồn dữ liệu mới với đúng `alias`, `fkIntegrationId` và trạng thái `enabled: true`. |
| Chọn **Tắt source** trong menu ba chấm của một nguồn | Gọi `listSources` thấy trường `enabled` của nguồn đó chuyển thành `false`. |
| Chọn **Đặt làm mặc định** cho một nguồn dữ liệu | Gọi `listSources` thấy trường `isDefault: true` tại nguồn được chọn và toàn bộ các nguồn khác có `isDefault: false`. |
| Chọn **Xóa source** và xác nhận trên hộp thoại | Gọi `listSources` không còn tìm thấy bản ghi nguồn đó trong danh sách kết quả trả về. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent thực hiện các thao tác quản trị nguồn dữ liệu | Truy cập màn hình `Nguồn dữ liệu` (`/database/sources`) hoặc bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Tải lại**, danh sách nguồn dữ liệu cập nhật theo thời gian thực đúng với cấu hình Agent đã xử lý. |
| Agent khởi tạo bảng mới trỏ vào nguồn cụ thể | Mở danh sách bảng tại `Trang chủ > Database`, mở hộp thoại chi tiết hoặc cấu hình bảng, nguồn lưu trữ của bảng hiển thị đúng tên nguồn CSDL đã được Agent gán. |
