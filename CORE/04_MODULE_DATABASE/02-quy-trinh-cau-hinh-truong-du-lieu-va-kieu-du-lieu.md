## Mở khu vực Cấu hình Trường dữ liệu (Table Fields)

Trường dữ liệu (Fields / Columns) định nghĩa cấu trúc lưu trữ và kiểu thông tin của từng bản ghi trong bảng dữ liệu **RedAI Database**. Người dùng có thể truy cập và quản trị hệ thống trường qua 2 phương thức trực quan trên giao diện:

| Phương thức truy cập | Thao tác thực hiện | Giao diện hiển thị |
| :--- | :--- | :--- |
| **Phương thức 1 — Màn hình chuyên sâu Table Fields** | Tại danh sách bảng, rê chuột vào dòng bảng cần cấu hình → Bấm nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> → Chọn <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Trường**. | Hệ thống điều hướng sang trang quản trị cột: `Trang chủ > Database > Table Fields`. Hiển thị danh sách toàn bộ các trường kèm panel cấu hình chi tiết bên phải. |
| **Phương thức 2 — Thao tác nhanh trên tiêu đề cột (Grid View)** | Mở dạng xem bảng tính (`Trang chủ > Database > View Details`), rê chuột vào tiêu đề của bất kỳ cột nào và bấm biểu tượng menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> trên header cột. | Xuất hiện menu popover cho phép bấm <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> **Sửa trường**, hoặc bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> ở cột ngoài cùng bên phải để thêm trường mới. |

---

### Bố cục màn hình chuyên sâu Table Fields

Giao diện `Trang chủ > Database > Table Fields` được thiết kế tối ưu cho việc tổ chức cấu trúc dữ liệu tổng thể:

| Phân vùng | Thành phần giao diện | Ý nghĩa & Chức năng |
| :--- | :--- | :--- |
| **Thanh tiêu đề (Top Bar)** | Biểu tượng mũi tên <img src="https://api.iconify.design/lucide:arrow-left.svg?color=%23ff3333" width="16" alt="" /> **(Quay lại)** | Bấm để trở về danh sách bảng dữ liệu. |
| | Tiêu đề **FIELDS** | Hiển thị tên định danh của bảng đang cấu hình (ví dụ: `FIELDS 01_CoSo`). |
| | Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo trường)** | Nút màu đỏ ở góc phải trên cùng, dùng để khởi tạo nhanh một trường dữ liệu mới. |
| | Nút <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới)** | Tải lại danh sách trường dữ liệu mới nhất. |
| **Cột bên trái (Danh sách trường)** | Ô tìm kiếm `Q Tìm trường` | Nhập từ khóa để định vị nhanh cột cần chỉnh sửa trong bảng có nhiều trường. |
| | Tiêu đề **DANH SÁCH TRƯỜNG ({N})** | Hiển thị tổng số lượng cột hiện có trong bảng kèm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm**. |
| | Danh sách các dòng trường | Mỗi dòng gồm biểu tượng tay cầm kéo vị trí, biểu tượng loại dữ liệu và tên trường (ví dụ: Người tạo, Người cập nhật, Thứ tự dòng, ID Cơ Sở, Tên cơ sở, Hotline, Website...). |
| **Panel cấu hình bên phải** | Khung **Tạo trường / Sửa trường** | Khu vực thiết lập chi tiết thuộc tính, kiểu dữ liệu, ràng buộc giá trị và kiểm tra tính hợp lệ của trường đang chọn. |

---

## Các bước thực hiện

### Giai đoạn 1 — Khởi tạo và thiết lập thuộc tính cơ bản của trường dữ liệu

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Mở biểu mẫu cấu hình** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo trường)** trên thanh tiêu đề hoặc nút `+ Thêm` trên danh sách cột. | Panel bên phải mở ra khung **Tạo trường**. |
| **2. Đặt tên trường** | Nhập tên trường rõ nghĩa vào ô `Tên trường` (ví dụ: `Mã Nhân Viên`, `Họ Và Tên`, `Mức Lương Cơ Bản`). | Định danh hiển thị cho cột trong bảng tính và các biểu mẫu. |
| **3. Chọn loại dữ liệu** | Nhấp vào danh sách thả xuống **Loại dữ liệu** và chọn kiểu dữ liệu phù hợp với thông tin cần lưu trữ. | Xác định định dạng nhập liệu và phương thức xử lý của hệ thống. |
| **4. Cấu hình độ dài hoặc thuộc tính riêng** | Tùy thuộc vào loại dữ liệu được chọn, hệ thống hiển thị thêm các thông số tương ứng (ví dụ: nhập `Độ dài tối đa` cho kiểu văn bản). | Giới hạn số lượng ký tự nhập liệu để tối ưu bộ nhớ. |
| **5. Nhập mô tả hướng dẫn** | Nhấp vào mục `+ Mô tả` để mở khung nhập ghi chú. | Hiển thị chú thích trợ giúp người dùng khi nhập liệu vào trường này. |
| **6. Cấu hình ràng buộc toàn vẹn** | • Công tắc **Bắt buộc nhập (Not Null)**: Bật công tắc nếu trường không được phép để trống khi tạo hoặc sửa bản ghi.<br>• Công tắc **Giá trị duy nhất (Unique)**: Bật công tắc để đảm bảo không có hai bản ghi nào bị trùng lặp giá trị trong cột này. | Ngăn chặn sai sót nhập thiếu hoặc trùng lặp dữ liệu quan trọng. |
| **7. Thiết lập giá trị mặc định** | Nhấp vào mục `+ Giá trị mặc định` để điền giá trị có sẵn. | Tự động điền giá trị này khi có bản ghi mới được tạo mà người dùng chưa nhập liệu. |
| **8. Thiết lập quy tắc kiểm tra (Validation Rules)** | Nhấp vào mục `+ Add validation rules (Regex / Min / Max)` để bổ sung điều kiện kiểm tra dữ liệu đầu vào theo biểu thức chính quy hoặc khoảng giá trị. | Ngăn chặn nhập sai cú pháp (như số điện thoại, mã số thuế, email). |
| **9. Lưu cấu hình trường** | Bấm vào biểu tượng chữ V màu đỏ <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> ở góc trên bên phải panel để lưu (hoặc bấm `X` để hủy bỏ). | Trường mới xuất hiện ngay trên danh sách cột và bảng tính. |

---

### Giai đoạn 2 — Danh mục các kiểu dữ liệu và ứng dụng thực tế

Hệ thống **RedAI Database** hỗ trợ phân hệ kiểu dữ liệu chuyên sâu phục vụ đa dạng bài toán quản trị doanh nghiệp:

| Nhóm kiểu dữ liệu | Kiểu dữ liệu cụ thể | Mục đích & Nghiệp vụ phù hợp |
| :--- | :--- | :--- |
| **Văn bản & Mô tả** | Single line text, Long text, HTML | Lưu trữ tiêu đề ngắn, họ tên, ghi chú chi tiết, mô tả hợp đồng có định dạng văn bản giàu. |
| **Định lượng & Tài chính** | Number, Currency, Percent, Rating | Quản lý số lượng tồn kho, đơn giá bán buôn/lẻ, chiết khấu phần trăm và điểm số đánh giá từ 1 đến 5 sao. |
| **Lựa chọn & Cờ logic** | Select, Multi-select, Boolean | Phân loại trạng thái xử lý đơn hàng, danh mục phòng ban, cờ bật/tắt (Đúng/Sai). |
| **Liên lạc & Mạng lưới** | Phone, Email, URL, Location | Lưu số hotline, email liên hệ đối tác, đường dẫn website và địa chỉ tọa độ địa lý. |
| **Mốc thời gian** | Date, Datetime, Time, Duration | Quản lý ngày sinh, mốc giờ họp, hạn chót thanh toán và thời lượng thực thi dự án. |
| **Khóa tự tăng & Quan hệ** | Auto Number, Relation, Lookup, Rollup | Tạo mã định danh tự tăng (ví dụ: `HD-0001`), liên kết dữ liệu giữa các bảng, tra cứu cột tham chiếu và tính tổng hợp tự động. |
| **Tính toán & Tự động hóa** | Formula, Button, User, Attachment | Trình biên soạn biểu thức toán học tự động, nút kích hoạt webhook hoặc workflow, gán nhân sự phụ trách và lưu tệp đính kèm. |

---

### Giai đoạn 3 — Thao tác nhanh trên tiêu đề cột (Grid View Header)

Tại giao diện bảng tính Grid View (`Trang chủ > Database > View Details`), nhấp vào biểu tượng menu ba chấm trên thanh tiêu đề của bất kỳ cột nào sẽ mở bảng chức năng:

| Lệnh thao tác | Biểu tượng | Tác vụ chi tiết |
| :--- | :--- | :--- |
| **Sửa trường** | <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> | Mở khung chỉnh sửa thuộc tính của trường trực tiếp mà không cần rời bảng tính. |
| **Nhân bản trường** | <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> | Tạo ra một bản sao cột mới kế thừa toàn bộ cấu hình, kiểu dữ liệu và quy tắc kiểm tra của cột hiện tại. |
| **Đặt làm trường hiển thị chính** | <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> | Thiết lập cột làm nhãn đại diện chính (Primary Display Field) cho bản ghi khi hiển thị trong quan hệ bảng và tìm kiếm. |
| **Căn trái** | <img src="https://api.iconify.design/lucide:align-left.svg?color=%23ff3333" width="16" alt="" /> | Căn lề trái toàn bộ dữ liệu hiển thị trong cột (phù hợp với chuỗi ký tự, văn bản, họ tên). |
| **Căn giữa** | <img src="https://api.iconify.design/lucide:align-center.svg?color=%23ff3333" width="16" alt="" /> | Căn lề giữa nội dung ô tính trong cột (phù hợp với mã định danh, trạng thái, ngày tháng). |

---

### Giai đoạn 4 — Cấu hình chuyên sâu cho các kiểu dữ liệu liên kết và tính toán

#### 1. Kiểu dữ liệu Quan hệ liên kết bảng (Relation)
- **Bảng liên kết đích**: Chọn bảng muốn tạo quan hệ dữ liệu trong cơ sở dữ liệu.
- **Loại quan hệ**: Chọn mô hình liên kết `Một - Nhiều (1:N)`, `Nhiều - Một (N:1)`, `Nhiều - Nhiều (N:N)` hoặc `Một - Một (1:1)`.
- **Trường đối ứng**: Tự động tạo một cột tham chiếu ngược ở bảng đích để đảm bảo khả năng liên kết dữ liệu hai chiều.

#### 2. Kiểu dữ liệu Tra cứu (Lookup) và Tổng hợp (Rollup)
- **Tra cứu (Lookup)**: Dựa vào trường Relation đã có để kéo dữ liệu từ một cột khác ở bảng liên kết về bảng hiện tại mà không cần nhập lại.
- **Tổng hợp (Rollup)**: Tính toán tổng hợp dữ liệu trên các bản ghi liên kết qua các hàm chuẩn: `SUM` (Tổng cộng), `AVG` (Trung bình cộng), `COUNT` (Đếm số lượng), `MIN` (Nhỏ nhất), `MAX` (Lớn nhất).

#### 3. Kiểu dữ liệu Công thức tính toán (Formula)
- Hỗ trợ trình soạn thảo công thức với khả năng tham chiếu trực tiếp đến các cột khác trong dòng bằng ký hiệu `{Tên_Cột}`.
- Các phép toán số học: `+`, `-`, `*`, `/`.
- Các hàm điều kiện logic: `IF(điều_kiện, giá_trị_đúng, giá_trị_sai)`, `AND()`, `OR()`.
- Các hàm xử lý chuỗi và thời gian: `CONCAT()`, `DATE_DIFF()`, `TODAY()`.

---

## Kiểm tra kết quả

Sau khi hoàn tất quy trình cấu hình trường dữ liệu, người dùng kiểm tra lại:

| Hạng mục kiểm tra | Tiêu chí đạt chuẩn |
| :--- | :--- |
| **1. Cột trên Bảng tính Grid View** | Tên cột hiển thị đúng vị trí; biểu tượng kiểu dữ liệu tương ứng xuất hiện cạnh tên cột. |
| **2. Hành vi nhập liệu ô tính** | Nhấp đúp vào ô thuộc cột để nhập dữ liệu; ô hiển thị đúng trình biên tập (ví dụ: bảng chọn lịch với kiểu Date, danh sách thẻ màu với kiểu Select, khung tải tệp với kiểu Attachment). |
| **3. Ràng buộc Not Null & Unique** | Thử để trống hoặc nhập trùng lặp giá trị trong cột Unique; hệ thống hiển thị cảnh báo từ chối lưu bản ghi. |
| **4. Công thức & Tham chiếu** | Thay đổi giá trị ở các cột đầu vào; kết quả tại các cột Formula, Lookup và Rollup được cập nhật tức thì. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động khởi tạo cấu trúc trường dữ liệu, cấu hình các kiểu dữ liệu nâng cao (tiền tệ, ngày tháng, công thức, liên kết bảng quan hệ), đặt trường hiển thị chính và thiết lập quy tắc kiểm tra tính hợp lệ thông qua bộ công cụ quản trị Database.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Database` (ID: `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6`)
- **Bộ công cụ (Tool Suite) đi kèm**: `RedAI - Module - Database` (ID: `eb8a7504-5844-4e6e-ba7f-7645f104c0af`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản trị cơ sở dữ liệu trong Workspace (Member, Editor, Admin hoặc Owner).

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Mở trang `Table Fields` để xem cấu hình cột | `getColumn`, `getTable` | Đọc cấu hình chi tiết của một cột theo tên hiển thị (`fieldName`) hoặc lấy toàn bộ danh sách cột của bảng. |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo trường** (cột văn bản ngắn) | `createOrUpdateTextColumn` | Khởi tạo hoặc cập nhật cột văn bản ngắn (Single line text) kèm độ dài tối đa và giá trị mặc định. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Văn bản dài** | `createOrUpdateLongTextColumn` | Khởi tạo hoặc cập nhật cột văn bản dài nhiều dòng (Long text / Rich text). |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Số** hoặc **Tiền tệ** | `createOrUpdateNumberColumn`, `createOrUpdateCurrencyColumn` | Thiết lập cột định lượng số nguyên/số thực hoặc cột tiền tệ có định dạng đơn vị (VND, USD...). |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Ngày tháng / Ngày giờ** | `createOrUpdateDateColumn`, `createOrUpdateDatetimeColumn` | Thiết lập cột lưu mốc ngày hoặc ngày giờ với định dạng hiển thị chuẩn. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Lựa chọn / Chọn nhiều** | `createOrUpdateEnumColumn`, `createOrUpdateMultiSelectColumn` | Cấu hình danh mục tùy chọn (Select / Multi-select) với danh sách các nhãn hiển thị và màu sắc. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Quan hệ (Relation)** | `createOrUpdateRelationColumn` | Thiết lập liên kết bảng hai chiều giữa hai bảng dữ liệu theo mô hình 1-1, 1-N hoặc N-N. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Tra cứu (Lookup)** | `createOrUpdateLookupColumn` | Kéo tự động dữ liệu từ một cột ở bảng liên kết thông qua trường Relation đã thiết lập. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Tổng hợp (Rollup)** | `createOrUpdateRollupColumn` | Tự động tính toán tổng hợp (SUM, COUNT, AVG, MIN, MAX) trên các bản ghi liên kết. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Công thức (Formula)** | `createOrUpdateFormulaColumn` | Thiết lập biểu thức tính toán tự động giữa các cột trong dòng theo cú pháp `{Tên_Cột}`. |
| Bấm **Tạo trường** $\rightarrow$ Chọn kiểu **Số điện thoại, URL, Đính kèm** | `createOrUpdatePhoneColumn`, `createOrUpdateUrlColumn`, `createOrUpdateAttachmentColumn` | Cấu hình các cột lưu trữ hotline, đường dẫn website và tệp tài liệu đính kèm. |
| Header cột $\rightarrow$ <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> **Đặt làm trường hiển thị chính** | `setPrimaryColumn` | Thiết lập cột làm nhãn đại diện chính (Primary Column) khi tìm kiếm và hiển thị quan hệ. |
| Kéo thả sắp xếp lại thứ tự cột | `reorderColumns` | Sắp xếp lại thứ tự hiển thị của các cột trong bảng theo danh sách `columnNames`. |
| Header cột $\rightarrow$ Chọn lệnh xóa trường | `deleteColumn` | Xóa vĩnh viễn một trường dữ liệu khỏi bảng theo tên hiển thị `fieldName`. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi cấu hình hệ thống cột dữ liệu chuyên sâu cho bảng "Đơn Đặt Hàng" trên RedAI Database:

1. Bối cảnh và Mục tiêu:
- Tôi cần thiết lập các cột quản lý đơn hàng bao gồm mã đơn tự động, số tiền, ngày tạo, trạng thái đơn và liên kết sang bảng khách hàng.

2. Dữ liệu cung cấp:
- Tên bảng: "Đơn Đặt Hàng"
- Cột 1: Tên "Mã Đơn Hàng", kiểu văn bản ngắn (Text), bắt buộc nhập (required: true), đặt làm trường hiển thị chính (Primary Column).
- Cột 2: Tên "Tổng Tiền", kiểu tiền tệ (Currency), đơn vị tiền tệ "VND", bắt buộc nhập (required: true).
- Cột 3: Tên "Trạng Thái", kiểu lựa chọn đơn (Enum/Select), danh sách tùy chọn gồm: "Chờ xác nhận", "Đang xử lý", "Hoàn thành", "Đã hủy".
- Cột 4: Tên "Ngày Đặt", kiểu ngày tháng (Date).
- Cột 5: Tên "Khách Hàng", kiểu quan hệ (Relation), liên kết sang bảng "Khách Hàng Doanh Nghiệp".

3. Các bước yêu cầu thực hiện:
- Bước 1: Gọi getTable để kiểm tra cấu trúc hiện tại của bảng "Đơn Đặt Hàng".
- Bước 2: Gọi createOrUpdateTextColumn để tạo cột "Mã Đơn Hàng" và sau đó gọi setPrimaryColumn để gán làm cột đại diện chính.
- Bước 3: Gọi createOrUpdateCurrencyColumn để tạo cột "Tổng Tiền" với đơn vị "VND".
- Bước 4: Gọi createOrUpdateEnumColumn để tạo cột "Trạng Thái" với danh sách options đã cung cấp.
- Bước 5: Gọi createOrUpdateDateColumn để tạo cột "Ngày Đặt".
- Bước 6: Gọi createOrUpdateRelationColumn để thiết lập liên kết sang bảng "Khách Hàng Doanh Nghiệp".
- Bước 7: Gọi getTable để đọc lại toàn bộ schema xác nhận tất cả các cột đã được lưu thành công.

4. Yêu cầu phản hồi:
- Báo cáo danh sách chi tiết các cột vừa tạo kèm kiểu dữ liệu, cờ bắt buộc nhập và trường hiển thị chính đã thiết lập.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Truy cập `Trang chủ > Database > Table Fields` của bảng **Đơn Đặt Hàng**, kiểm tra danh sách cột bên trái hiển thị đầy đủ các trường mới với đúng biểu tượng kiểu dữ liệu; mở Grid View thấy các header cột xuất hiện theo đúng thứ tự. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getTable` và `getColumn` cho các cột vừa tạo của bảng 'Đơn Đặt Hàng' để xác nhận cấu hình kiểu dữ liệu và trường hiển thị chính."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Thêm cột mới trong panel Tạo trường trên UI | Gọi `getColumn` thấy thuộc tính cột xuất hiện đúng tên, loại dữ liệu và ràng buộc `required`. |
| Bấm đặt cột làm trường hiển thị chính (Ngôi sao) | Gọi `getTable` thấy trường `primaryColumn` trùng khớp với cột vừa chọn. |
| Xóa một cột trên menu tiêu đề cột | Gọi `getTable` kiểm tra danh sách cột thấy trường đã bị xóa hoàn toàn. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createOrUpdateCurrencyColumn` | Mở bảng tính Grid View, xuất hiện ngay cột Tiền tệ có biểu tượng đồng tiền cạnh tên cột. |
| Agent gọi `createOrUpdateRelationColumn` | Header cột xuất hiện biểu tượng liên kết mạng lưới, nhấp vào ô hiển thị danh sách chọn bản ghi từ bảng liên kết. |
| Agent gọi `setPrimaryColumn` | Tên cột trên tiêu đề xuất hiện biểu tượng ngôi sao màu vàng nhận diện cột đại diện chính. |
