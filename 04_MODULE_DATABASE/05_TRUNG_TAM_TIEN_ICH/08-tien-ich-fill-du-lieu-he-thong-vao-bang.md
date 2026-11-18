## Tổng quan Tiện ích Fill Dữ liệu hệ thống vào Bảng

Tiện ích **Fill Dữ liệu hệ thống vào Bảng** là công cụ quản trị cấp cao trên **RedAI Database**, cho phép trích xuất tự động danh sách người dùng trong hệ thống (System Users) hoặc dữ liệu vận hành theo các bộ lọc phân khúc chuyên sâu và đổ trực tiếp vào Bảng Động. Tiện ích hỗ trợ hai phương thức đích: ghi bổ sung vào bảng hiện có (kèm cơ chế chống trùng lặp Upsert) hoặc tự động tạo một bảng dữ liệu mới hoàn toàn tương thích với cấu trúc nguồn.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Chọn nguồn dữ liệu hệ thống** | **Menu chọn nguồn trích xuất** | Chọn nguồn thông tin cần lấy dữ liệu (ví dụ: `Danh sách Người dùng Hệ thống - System Users`). Hệ thống chỉ mở quyền tính năng này cho người dùng có quyền quản trị tương ứng. |
| **2. Bộ lọc phân khúc đối tượng** | • **Lọc theo Thẻ người dùng (User Tags):** | Chọn các nhãn phân loại tài khoản (ví dụ: `Khách hàng VIP`, `Cộng tác viên`, `Học viên mới`). |
| | • **Lọc theo Gói thuê bao (Subscription Plan):** | Chọn người dùng đang kích hoạt gói dịch vụ cụ thể trong danh mục đăng ký. |
| | • **Lọc theo Khoảng ngày đăng ký:** | Chọn ngày bắt đầu và kết thúc tạo tài khoản qua bộ chọn lịch tương tác. |
| | • **Lọc theo Trạng thái tài khoản:** | Tùy chọn lọc: `Tất cả`, `Đang hoạt động (Active)` hoặc `Đã khóa`. |
| | • **Thanh tìm kiếm nhanh:** | Nhập từ khóa tên hoặc email để lọc danh sách người dùng mục tiêu. |
| **3. Chọn phương thức đích nhận dữ liệu** | • <img src="https://api.iconify.design/lucide:table.svg?color=%23ff3333" width="16" alt="" /> **Ghi vào Bảng hiện tại:** | Đổ dữ liệu thẳng vào bảng dữ liệu bạn đang mở ngoài Grid View. |
| | • <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tự động tạo Bảng mới:** | Hệ thống tự động khởi tạo một bảng dữ liệu mới trong Không gian làm việc, đặt tên bảng theo ngày giờ trích xuất và tự động tạo đầy đủ các cột tương thích với thông tin người dùng hệ thống. |
| **4. Bảng ánh xạ trường tự động (Field Mapping)** | • **Nút 'Gợi ý ánh xạ tự động':** | Thuật toán thông minh tự động ghép nối các cột nguồn (ID, Tên người dùng, Email, SĐT, Ngày tạo, Gói đăng ký) với các cột đích có tên hoặc kiểu dữ liệu tương ứng trong bảng. |
| | • **Khóa định danh chống trùng (Upsert Key):** | Chỉ định trường định danh duy nhất (ví dụ: `Email` hoặc `Số điện thoại`): Nếu bản ghi đã tồn tại trong bảng thì tự động cập nhật thông tin mới thay vì tạo dòng trùng lặp. |
| **5. Bảng xem trước dữ liệu trích xuất** | **Xem trước có phân trang** | Hiển thị danh sách người dùng được lọc ra với đầy đủ ảnh đại diện (Avatar), Họ tên, Email, SĐT và Gói dịch vụ kèm tổng số bản ghi dự kiến sẽ đổ vào bảng. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Fill Dữ liệu hệ thống vào Bảng]
                     │
                     ▼
[Thiết lập Bộ lọc người dùng (Thẻ nhãn, Gói thuê bao, Ngày tạo)]
                     │
                     ▼
[Chọn Phương thức đích: Ghi vào Bảng hiện tại HOẶC Tự tạo Bảng mới]
                     │
                     ▼
[Bấm "Gợi ý ánh xạ tự động" & Chọn Khóa chống trùng lặp]
                     │
                     ▼
[Kiểm tra Bảng xem trước danh sách người dùng]
                     │
                     ▼
[Bấm "Bắt đầu đổ dữ liệu vào bảng" ➔ Hệ thống cập nhật bảng tính]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **Fill Dữ liệu hệ thống vào Bảng**. |
| **2** | **Lọc đối tượng** | Chọn thẻ người dùng (ví dụ: `Khách hàng VIP`) và chọn gói dịch vụ cần trích xuất danh sách. |
| **3** | **Chọn bảng đích** | Chọn *Ghi vào Bảng hiện tại* (hoặc chọn *Tự động tạo Bảng mới* và nhập tên bảng mong muốn). |
| **4** | **Khớp nối ánh xạ cột** | Nhấp nút **Gợi ý ánh xạ tự động**. Đối soát từng dòng để đảm bảo cột Email của người dùng khớp với cột Email của bảng. |
| **5** | **Thực thi đồng bộ** | Nhấp nút **Bắt đầu đổ dữ liệu vào bảng**. Hệ thống xử lý ngầm và hiển thị thông báo thành công khi hoàn tất. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Dữ liệu trong bảng đích** | Bảng tính xuất hiện đầy đủ các dòng người dùng mới với thông tin tên, email, SĐT và gói đăng ký chuẩn xác. |
| **Hiệu lực chống trùng** | Các tài khoản đã có sẵn trong bảng trước đó được cập nhật thông tin mới nhất mà không bị tạo thêm dòng nhân bản. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Tài khoản có quyền quản trị và quyền tạo bản ghi (`RECORD_CREATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Đổ danh sách người dùng hệ thống vào Bảng Động** | `createRecords`, `bulkColumns` | *"Hãy trích xuất danh sách toàn bộ người dùng hệ thống có thẻ 'Khách hàng thân thiết' và ghi vào bảng 'Danh Bạ Chăm Sóc' với các trường Họ tên, Email và Số điện thoại."* |
| **Tự động tạo bảng mới và điền dữ liệu tài khoản** | `createTable`, `createRecords` | *"Hãy tạo một bảng mới mang tên 'Khách Hàng Nâng Cấp Gói' và điền toàn bộ người dùng đã mua gói Subscription trong tháng này vào bảng."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm đổ dữ liệu vào bảng trên giao diện | Gọi `listRecords` trên bảng đích thấy các dòng mới có thông tin người dùng hệ thống tương ứng. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent ghi dữ liệu người dùng vào bảng | Người dùng mở bảng tính ngoài Grid View, danh sách người dùng hệ thống hiển thị ngay lập tức. |
