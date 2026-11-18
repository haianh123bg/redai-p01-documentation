## Tổng quan Tiện ích Chuẩn hóa & Làm sạch dữ liệu

Tiện ích **Chuẩn hóa & Làm sạch dữ liệu** là công cụ giúp chuẩn hóa hàng loạt các ô tính có dữ liệu bị sai lệch, không đồng nhất định dạng hoặc chứa ký tự rác. Tiện ích chạy trực tiếp trên các dòng dữ liệu của Bảng Động với khả năng xử lý thông minh theo từng lô 50 bản ghi (batch 50), hỗ trợ xem trước bản so sánh trước/sau (Diff Preview) theo thời gian thực và đảm bảo an toàn tuyệt đối cho cơ sở dữ liệu.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

Hộp thoại cấu hình gồm các phân khu chức năng trực quan:

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Cột dữ liệu mục tiêu** | **Menu chọn cột cần chuẩn hóa** | Hệ thống tự động lọc danh sách chỉ hiển thị các cột có kiểu dữ liệu phù hợp và có quyền ghi (`Writable`): `Văn bản (Text)`, `Văn bản dài (Long Text)`, `Số điện thoại (Phone)`, `Email`, `Đường dẫn (URL)`. Mặc định ưu tiên tự chọn cột kiểu SĐT hoặc Email nếu bảng có sẵn. |
| **2. Nhóm chuyển đổi Số điện thoại** | • **Số quốc nội chuẩn (vd: 0912345678):** | Tự động đưa về dạng đầu số 0 quốc nội (National format), loại bỏ mã quốc gia `+84` hoặc khoảng trắng thừa ở giữa số. |
| | • **Số quốc tế chuẩn E.164 (vd: +84912345678):** | Tự động phân tích theo thư viện viễn thông quốc tế, bổ sung tiền tố mã quốc gia `+84` để phục vụ gửi SMS hoặc ZNS quốc tế. |
| | • **Lọc bỏ ký tự thừa (chỉ giữ số và +):** | Quét sạch các dấu chấm (`.`), dấu gạch ngang (`-`), dấu cách (` `) hoặc ký tự chữ bị nhập nhầm trong ô số điện thoại. |
| **3. Nhóm chuyển đổi Email** | • **Chuẩn hóa Email (chữ thường & bỏ khoảng trắng):** | Đưa toàn bộ địa chỉ hòm thư về chữ in thường (lowercase) và cắt bỏ khoảng trắng đầu/cuối chuỗi để tránh lỗi gửi thư. |
| **4. Nhóm chuyển đổi Văn bản** | • **Viết hoa chữ cái đầu mỗi từ (Title Case):** | Tự động viết hoa chữ cái đầu tiên của từng từ và viết thường các chữ cái còn lại (ví dụ: `nguyễn văn a` $\rightarrow$ `Nguyễn Văn A`), chuẩn hóa họ tên danh từ riêng. |
| | • **Viết hoa toàn bộ (UPPERCASE):** | Chuyển toàn bộ ký tự thành chữ in hoa, phục vụ chuẩn hóa mã chứng từ, mã vạch hoặc biển số xe. |
| | • **Viết thường toàn bộ (lowercase):** | Chuyển toàn bộ chuỗi về chữ in thường. |
| | • **Bỏ khoảng trắng thừa (Trim spaces):** | Gom các khoảng trắng kép, tab giữa các từ thành 1 khoảng trắng đơn duy nhất, xóa sạch khoảng trắng ở hai đầu chuỗi. |
| | • **Loại bỏ dấu tiếng Việt:** | Chuyển đổi toàn bộ ký tự tiếng Việt có dấu thành không dấu (ví dụ: `Trần Thị Mai` $\rightarrow$ `Tran Thi Mai`, `đ/Đ` $\rightarrow$ `d/D`). |
| **5. Phạm vi áp dụng** | • <img src="https://api.iconify.design/lucide:check-square.svg?color=%23ff3333" width="16" alt="" /> **Chỉ áp dụng cho {N} bản ghi đang chọn** | Chỉ xử lý các dòng được người dùng tích chọn ngoài bảng tính. |
| | • <img src="https://api.iconify.design/lucide:table.svg?color=%23ff3333" width="16" alt="" /> **Áp dụng cho toàn bộ bản ghi trong Dạng xem** | Áp dụng cho tất cả các dòng hiện có theo bộ lọc của View hiện tại (xem trước tối đa 200 dòng). |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Hộp thoại Chuẩn hóa dữ liệu] 
           │
           ▼
[Chọn Cột dữ liệu mục tiêu (SĐT / Email / Họ tên)]
           │
           ▼
[Chọn Quy tắc chuyển đổi định dạng tương ứng]
           │
           ▼
[Chọn Phạm vi áp dụng (Bản ghi đang chọn vs Toàn bộ View)]
           │
           ▼
[Quan sát Bảng so sánh trước/sau (Diff Preview)]
           │
           ▼
[Bấm "Bắt đầu chuẩn hóa dữ liệu" (Xử lý Batch 50 bản ghi/lần)]
           │
           ▼
[Hoàn tất & Tự động làm mới bảng tính ngoài Grid View]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Chuẩn hóa & Làm sạch dữ liệu**. Hộp thoại cấu hình làm sạch xuất hiện. |
| **2** | **Chọn cột và quy tắc** | Chọn cột mục tiêu tại menu thả xuống và nhấp chọn 1 trong 9 quy tắc chuyển đổi định dạng tương ứng. |
| **3** | **Chọn phạm vi** | Tích chọn giữa *Chỉ bản ghi đang chọn* hoặc *Toàn bộ bản ghi trong View*. |
| **4** | **Kiểm tra Bản xem trước thay đổi (Diff Preview)** | Khung xem trước hiển thị danh sách 8 bản ghi tiêu biểu gồm 3 cột đối soát trực quan:<br>• **Dữ liệu gốc:** Giá trị hiện tại trong cơ sở dữ liệu.<br>• **Sau khi chuẩn hóa:** Giá trị dự kiến sau khi áp dụng quy tắc.<br>• **Trạng thái:** Huy hiệu màu xanh báo hiệu ô tính có sự thay đổi giá trị. Đọc kỹ dòng tóm tắt: *"Dự kiến có {N} bản ghi sẽ được thay đổi giá trị"*. Nếu không có bản ghi nào bị sai, hệ thống báo *"Không có bản ghi nào cần thay đổi giá trị"*. |
| **5** | **Thực thi chuẩn hóa** | Bấm nút <img src="https://api.iconify.design/lucide:wand-2.svg?color=%23ff3333" width="16" alt="" /> **Bắt đầu chuẩn hóa dữ liệu** ở góc dưới bên phải. Hệ thống hiển thị thanh tiến độ phần trăm thời gian thực chạy tuần tự qua từng lô 50 bản ghi để chống nghẽn mạng. Khi hoàn tất, hệ thống gửi thông báo nổi: *"Đã chuẩn hóa thành công {N} bản ghi!"* và tự động đóng hộp thoại, cập nhật lại bảng tính. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Dữ liệu cột Số điện thoại** | Toàn bộ các số hiển thị đồng nhất đầu `09x` (nếu chọn quốc nội) hoặc `+84` (nếu chọn E.164), không còn dấu chấm, dấu gạch nối hoặc khoảng trắng thừa. |
| **Dữ liệu cột Họ và tên** | Chữ cái đầu mỗi từ được viết hoa chỉn chu (ví dụ: `Nguyễn Hoàng Long`), khoảng trắng kép bị triệt tiêu hoàn toàn. |
| **Dữ liệu cột Email** | Toàn bộ chữ cái chuyển thành in thường, không còn lỗi khoảng trắng ở đầu hoặc cuối chuỗi. |
| **Thông báo hệ thống** | Thông báo nổi màu xanh góc màn hình xác nhận số lượng bản ghi đã được cập nhật thành công. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) có quyền chỉnh sửa bản ghi (`RECORD_UPDATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Chuẩn hóa số điện thoại sang chuẩn quốc tế E.164 (+84)** | `listRecords`, `updateRecords` | *"Hãy kiểm tra toàn bộ các bản ghi trong bảng 'Khách Hàng', chuẩn hóa cột 'Số điện thoại' sang định dạng quốc tế chuẩn E.164 (+84) và cập nhật lại vào bảng."* |
| **Chuẩn hóa viết hoa họ tên và bỏ khoảng trắng thừa** | `listRecords`, `updateRecords` | *"Hãy quét cột 'Họ và tên' trong bảng 'Học Viên', viết hoa chữ cái đầu mỗi từ và loại bỏ khoảng trắng thừa ở giữa các từ."* |
| **Đưa toàn bộ địa chỉ email về chữ thường** | `listRecords`, `updateRecords` | *"Hãy rà soát cột 'Email' trong bảng 'Đối Tác', chuyển đổi toàn bộ địa chỉ hòm thư về chữ thường và xóa khoảng trắng ở hai đầu."* |
| **Loại bỏ dấu tiếng Việt để đồng bộ hệ thống ngoại bộ** | `listRecords`, `updateRecords` | *"Hãy lấy dữ liệu cột 'Tên sản phẩm' trong bảng 'Kho Hàng', chuyển thành chuỗi tiếng Việt không dấu và cập nhật vào cột 'Mã tìm kiếm'."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm nút **Bắt đầu chuẩn hóa** trên giao diện | Gọi `listRecords` thấy trường dữ liệu của các bản ghi đã cập nhật sang định dạng chuẩn mới. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `updateRecords` cập nhật dữ liệu | Mở Dạng xem bảng tính (Grid View), các ô tính hiển thị ngay định dạng mới mà không cần thao tác tay. |
