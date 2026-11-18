## Tổng quan Tiện ích Tạo chiến dịch Đánh giá & Bình luận Google Maps

Tiện ích **Tạo chiến dịch Đánh giá & Bình luận Google Maps** là giải pháp nâng tầm uy tín địa điểm kinh doanh trên **RedAI Database**. Tiện ích tự động hóa việc đăng tải bình luận và chấm điểm số sao cho danh sách cơ sở kinh doanh, chi nhánh hoặc đối tác lưu trong bảng, hỗ trợ xoay vòng nhiều tài khoản Google, thiết lập thời gian hồi chiêu nghiêm ngặt để vượt qua thuật toán kiểm duyệt của Google và **ghi ngược kết quả thực thi (Result Write-Back)** trực tiếp vào các cột trong Bảng Động để theo dõi tiến độ thời gian thực.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Khai báo định danh chiến dịch** | • **Tiêu đề chiến dịch:** | Tên định danh (ví dụ: `Chiến dịch Đánh giá 5 sao Chuỗi Cửa Hàng Hà Nội`). |
| | • **Bảng nguồn & Dạng xem:** | Chọn bảng dữ liệu và View lọc các địa điểm cần đánh giá. |
| | • **Giới hạn số lượng (Limit):** | Số lượng địa điểm tối đa cần xử lý trong đợt này (mặc định: `1.000` dòng). |
| **2. Bảng ánh xạ trường dữ liệu địa điểm** | • **Cột URL Google Maps (bắt buộc):** | Chứa đường dẫn địa điểm dạng `https://maps.app.goo.gl/...` hoặc `https://www.google.com/maps/place/...`. |
| | • **Cột Điểm đánh giá (Rating):** | Cột số chứa số sao đánh giá (từ 1 đến 5 sao). |
| | • **Cột Nội dung bình luận (Comment):** | Cột chứa văn bản nhận xét trải nghiệm thực tế. |
| | • **Cột Hình ảnh đính kèm (Photos):** | Cột chứa đường link ảnh chụp sản phẩm hoặc không gian để đăng kèm bài viết. |
| | • **Cột Đánh giá chi tiết (Tùy chọn):** | Khớp nối các cột điểm số chuyên sâu: *Đồ ăn (Food)*, *Dịch vụ (Service)*, *Không gian (Atmosphere)*. |
| **3. Chế độ nội dung bài viết** | • **Chế độ Trực tiếp (DIRECT):** | Lấy trực tiếp câu bình luận đã soạn sẵn trong ô tính của từng dòng. |
| | • **Chế độ Mẫu (TEMPLATE):** | Chọn mẫu đánh giá chung có chứa biến `{{ten_dia_diem}}`, `{{dich_vu}}` để hệ thống tự động sinh nội dung tự nhiên cho từng địa điểm. |
| **4. Quản lý Tài khoản Google Maps** | • **Chọn tài khoản thực thi:** | Cho phép tích chọn đồng thời nhiều tài khoản Google đã liên kết để xoay vòng người viết đánh giá. |
| | • <img src="https://api.iconify.design/lucide:log-in.svg?color=%23ff3333" width="16" alt="" /> **Đăng nhập tài khoản Google mới:** | Hỗ trợ đăng nhập bảo mật tài khoản Google trực tiếp từ hộp thoại popup. |
| **5. Cấu hình Giãn cách an toàn & Hồi chiêu (Safety & Delays)** | • **Khoảng trễ ngẫu nhiên (Min/Max Delay):** | Giãn cách từ `60` đến `300` giây giữa mỗi lượt đánh giá để mô phỏng hành vi người dùng thật. |
| | • **Thời gian hồi chiêu tối thiểu (Cooldown):** | Đặt tối thiểu `300` giây nghỉ cho mỗi tài khoản Google sau khi hoàn thành 1 bài đánh giá. |
| | • **Giới hạn số lượt đánh giá/ngày:** | Giới hạn từ `3` đến `5` bài đánh giá/ngày cho mỗi tài khoản để giữ an toàn tuyệt đối. |
| | • **Cho phép cập nhật lại (Allow Update):** | Bật công tắc nếu muốn chỉnh sửa bài đánh giá cũ nếu địa điểm đó đã từng được tài khoản đó chấm điểm trước đây. |
| **6. Ghi ngược kết quả vào Bảng Động (Result Write-Back)** | • **Cột Trạng thái (Status Field):** | Tự động ghi chữ `SUCCESS` (Thành công) hoặc `FAILED` (Thất bại). |
| | • **Cột Thời gian đánh giá (Reviewed At):** | Tự động điền ngày giờ hoàn tất bài viết. |
| | • **Cột Tài khoản đánh giá:** | Ghi tên tài khoản Google đã thực hiện viết bài. |
| | • **Cột Chi tiết lỗi (Error Field):** | Ghi thông báo lỗi nếu không đánh giá được (ví dụ: *Link địa điểm bị lỗi*, *Địa điểm đã đóng cửa vĩnh viễn*). |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Tạo chiến dịch Đánh giá Google Maps]
                       │
                       ▼
[Khớp nối Cột URL Google Maps, Điểm sao & Bình luận]
                       │
                       ▼
[Chọn Tài khoản Google thực thi (Xoay vòng đa tài khoản)]
                       │
                       ▼
[Thiết lập Giãn cách ngẫu nhiên 60-300s & Thời gian hồi chiêu]
                       │
                       ▼
[Bật "Ghi ngược kết quả" ➔ Chỉ định Cột Trạng thái, Ngày giờ, Tài khoản]
                       │
                       ▼
[Bấm "Tạo chiến dịch" ➔ Tiến trình tự động chạy ngầm và ghi kết quả]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch Đánh giá Google Maps**. |
| **2** | **Ánh xạ cột** | Chọn cột URL Google Maps, chọn cột Điểm sao và chọn cột Nội dung nhận xét trong bảng tính. |
| **3** | **Chọn tài khoản** | Tích chọn danh sách tài khoản Google tham gia chiến dịch để hệ thống phân bổ luân phiên. |
| **4** | **Cài đặt an toàn & Ghi ngược** | Thiết lập giãn cách từ 60 đến 180 giây. Bật tính năng *Ghi ngược kết quả* và chọn các cột Trạng thái, Thời gian đánh giá trong bảng tính. |
| **5** | **Khởi chạy tiến trình** | Nhấp nút **Tạo chiến dịch**. Hệ thống tiếp nhận tác vụ chạy ngầm và tự động cập nhật tiến độ vào Bảng Động. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Hiển thị trên Google Maps** | Mở link địa điểm trên Google Maps, bài đánh giá kèm số sao và hình ảnh đã xuất hiện công khai trên trang của địa điểm. |
| **Dữ liệu ghi ngược vào Bảng Động** | Cột `Trạng thái` ngoài Grid View tự động hiển thị chữ `SUCCESS` màu xanh, cột `Thời gian` được điền mốc ngày giờ thực hiện và cột `Tài khoản` ghi rõ tên người viết. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền tiếp thị (`MARKETING_CREATE`) và quyền chỉnh sửa bản ghi (`RECORD_UPDATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Lọc danh sách địa điểm cần đánh giá** | `listRecords` | *"Hãy truy vấn bảng 'Chi Nhánh Đối Tác', lấy danh sách các cơ sở chưa có trạng thái đánh giá, trích xuất cột URL Google Maps và Tên cơ sở."* |
| **Ghi nhận trạng thái hoàn thành đánh giá vào bảng** | `updateRecords` | *"Hãy cập nhật cột 'Trạng thái đánh giá' thành 'SUCCESS' và điền thời gian hiện tại vào cột 'Thời gian hoàn tất' cho 5 bản ghi vừa được đánh giá."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Chạy chiến dịch đánh giá Google Maps có ghi ngược | Gọi `listRecords` thấy cột Trạng thái chuyển sang `SUCCESS` và cột Tài khoản ghi nhận đúng tên tài khoản thực hiện. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent cập nhật kết quả đánh giá | Người dùng mở Dạng xem bảng tính (Grid View), các ô tính hiển thị trạng thái hoàn thành màu xanh đồng bộ. |
