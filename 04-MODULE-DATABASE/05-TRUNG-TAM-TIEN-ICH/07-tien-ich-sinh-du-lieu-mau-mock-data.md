## Tổng quan Tiện ích Sinh Dữ Liệu Mẫu (Mock Data)

Tiện ích **Sinh Dữ Liệu Mẫu (Mock Data)** là công cụ hỗ trợ đắc lực cho các nhà phát triển, quản trị viên và người thiết kế ứng dụng trên **RedAI Database**. Tiện ích tự động phân tích cấu trúc cột của bảng dữ liệu hiện tại, nhận diện thông minh ngữ nghĩa từng trường (Họ tên tiếng Việt, số điện thoại hợp lệ đầu số Việt Nam, hòm thư email, địa chỉ hành chính các tỉnh thành, số tiền doanh thu, ngày tháng và trạng thái) để sinh ra từ 5 đến 50 dòng bản ghi giả lập có ý nghĩa thực tế cao, phục vụ kiểm thử dạng xem (Kanban, Grid, Calendar) và thử nghiệm quy trình tự động hóa.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Chọn số lượng dòng cần sinh** | **Các thẻ tab số lượng dòng** | Cung cấp 4 mức số lượng lựa chọn nhanh:<br>• `5 dòng`: Phục vụ kiểm tra nhanh cấu trúc cột.<br>• `10 dòng`: Mức mặc định tối ưu để kiểm thử dạng xem Grid View.<br>• `20 dòng`: Thử nghiệm các bộ lọc và sắp xếp dữ liệu.<br>• `50 dòng`: Đánh giá hiệu năng tải trang và phân trang bảng tính. |
| **2. Thuật toán nhận diện ngữ nghĩa cột tự động** | • **Cột Họ và tên:** | Sinh họ và tên người Việt Nam tự nhiên, đa dạng (ví dụ: *Nguyễn Hoàng Long*, *Trần Thị Mai*, *Lê Minh Tuấn*). |
| | • **Cột Số điện thoại:** | Sinh số di động 10 chữ số đúng đầu mạng viễn thông Việt Nam (`09x`, `08x`, `03x`). |
| | • **Cột Email:** | Sinh địa chỉ email hợp lệ dựa trên họ tên tương ứng (ví dụ: `long.nguyen@example.com`). |
| | • **Cột Địa chỉ:** | Sinh địa chỉ hành chính có thật tại Việt Nam (kèm tên đường, quận/huyện, tỉnh/thành phố: Hà Nội, TP.HCM, Đà Nẵng, Cần Thơ...). |
| | • **Cột Tiền tệ / Doanh số:** | Sinh số tiền ngẫu nhiên từ hàng trăm nghìn đến hàng chục triệu đồng. |
| | • **Cột Ngày tháng:** | Sinh các mốc thời gian hợp lý xung quanh ngày hiện tại. |
| | • **Cột Lựa chọn (Select):** | Chọn ngẫu nhiên trong danh sách các giá trị tùy chọn đã cấu hình cho cột đó. |
| **3. Khung Xem trước dữ liệu giả lập** | **Bảng đối soát trực tiếp** | Hiển thị bảng mô phỏng dữ liệu chuẩn bị được tạo với đầy đủ các cột có thể ghi dữ liệu. |
| **4. Nút Làm mới hạt giống ngẫu nhiên** | <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Đổi dữ liệu khác (Re-roll seed)** | Nhấp vào nút này để hệ thống tạo một hạt giống ngẫu nhiên mới, làm mới toàn bộ dữ liệu mẫu trong khung xem trước nếu bạn chưa ưng ý bộ dữ liệu hiện tại. |
| **5. Nút Thực thi tạo bản ghi** | <img src="https://api.iconify.design/lucide:plus-circle.svg?color=%23ff3333" width="16" alt="" /> **Tạo {N} bản ghi mẫu** | Gửi lệnh ghi hàng loạt toàn bộ các dòng dữ liệu mẫu vào Bảng Động và tự động làm mới giao diện bảng tính. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **Sinh Dữ Liệu Mẫu (Mock Data)**. |
| **2** | **Chọn số lượng dòng** | Nhấp chọn thẻ số lượng dòng mong muốn (ví dụ: chọn `10 dòng`). |
| **3** | **Kiểm tra và làm mới dữ liệu** | Quan sát bảng xem trước. Nếu muốn đổi sang danh sách tên và địa chỉ khác, nhấp nút **Đổi dữ liệu khác**. |
| **4** | **Tạo bản ghi vào bảng** | Nhấp nút **Tạo 10 bản ghi mẫu** ở góc dưới bên phải. Hệ thống ghi dữ liệu vào bảng và gửi thông báo nổi: *"Đã sinh thành công 10 bản ghi mẫu!"*. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Số lượng dòng ngoài Grid View** | Thanh trạng thái đếm tổng số dòng ở góc dưới bảng tính tăng thêm chính xác bằng số lượng dòng vừa chọn sinh. |
| **Chất lượng dữ liệu hiển thị** | Các dòng dữ liệu mới xuất hiện ngay trên bảng tính với đầy đủ họ tên, SĐT, email, địa chỉ tiếng Việt hợp lệ và đồng bộ với các cột. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền tạo bản ghi (`RECORD_CREATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tự động sinh dữ liệu mẫu tiếng Việt vào bảng** | `createRecords` | *"Hãy tạo 10 dòng bản ghi dữ liệu mẫu tiếng Việt vào bảng 'Khách Hàng Tiềm Năng' gồm đầy đủ Họ tên, Số điện thoại Việt Nam hợp lệ, Email, Địa chỉ và Trạng thái 'Mới tiếp cận' để kiểm thử giao diện."* |
| **Sinh dữ liệu đơn hàng giả lập để kiểm thử tính toán** | `createRecords` | *"Hãy tạo 5 dòng bản ghi mẫu vào bảng 'Đơn Hàng' với các cột Tên khách hàng, Số lượng, Đơn giá và Ngày mua để kiểm tra công thức tính cột Thành tiền."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm tạo 10 bản ghi mẫu trên giao diện | Gọi `countRecords` thấy tổng số dòng tăng thêm 10; gọi `listRecords` thấy dữ liệu mẫu tiếng Việt vừa sinh. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createRecords` sinh dữ liệu | Người dùng mở Dạng xem bảng tính (Grid View), các dòng dữ liệu mới xuất hiện ngay lập tức trên màn hình. |
