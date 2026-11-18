## Tổng quan Tiện ích Tìm kiếm dữ liệu địa điểm (Google Maps Crawl)

Tiện ích **Tìm kiếm dữ liệu địa điểm (Google Maps Crawl)** là giải pháp thu thập dữ liệu doanh nghiệp và cửa hàng tự động trên **RedAI Database**. Tiện ích cho phép người dùng nhập từ khóa ngành nghề kết hợp khu vực địa lý, quét trực tiếp từ bản đồ Google Maps để bóc tách thông tin liên hệ (Tên cửa hàng, Số điện thoại, Địa chỉ chi tiết, Điểm đánh giá sao, Số lượng đánh giá, Website và Tọa độ GPS), sau đó đổ trực tiếp vào các cột tương ứng trong Bảng Động qua hệ thống tác vụ ngầm an toàn.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Cấu hình tìm kiếm địa điểm** | • **Từ khóa tìm kiếm (Keyword):** | Nhập từ khóa ngành nghề kết hợp địa phương (ví dụ: `quán cà phê Quận 1`, `phòng khám nha khoa Cầu Giấy`, `khách sạn 4 sao Đà Nẵng`). |
| | • **Số lượng địa điểm cần lấy:** | Nhập số lượng kết quả mong muốn (tối đa 100 địa điểm cho mỗi đợt quét). |
| | • **Bán kính quét (Radius):** | Giới hạn phạm vi tìm kiếm quanh tọa độ trung tâm (tính bằng km). |
| **2. Bảng ánh xạ trường dữ liệu (Field Mapping)** | • **Tên địa điểm (Place Name):** | Khớp nối vào cột Tên cơ sở hoặc Tên đối tác trong bảng. |
| | • **Số điện thoại (Phone):** | Tự động bóc tách và làm sạch số hotline đưa vào cột SĐT. |
| | • **Địa chỉ đầy đủ (Address):** | Ghi địa chỉ chi tiết kèm quận/huyện, tỉnh/thành phố. |
| | • **Điểm đánh giá (Rating):** | Điểm số sao trung bình trên Google Maps (từ 1.0 đến 5.0). |
| | • **Số lượt đánh giá (Reviews Count):** | Tổng số bài đánh giá của người dùng. |
| | • **Trang web (Website):** | Đường dẫn URL trang chủ của doanh nghiệp. |
| | • **Đường link Google Maps:** | Liên kết trực tiếp tới vị trí của địa điểm trên Google Maps. |
| **3. Khởi chạy tác vụ ngầm** | **Nút 'Bắt đầu tìm kiếm'** | Tác vụ được đưa vào hệ thống xử lý ngầm (SysJobs), tự động lọc trùng lặp và tạo mới các dòng bản ghi vào Bảng Động. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm dữ liệu địa điểm**. |
| **2** | **Nhập từ khóa & Khu vực** | Nhập từ khóa ngành nghề và địa bàn cần khảo sát (ví dụ: `Spa làm đẹp Đống Đa`). |
| **3** | **Ánh xạ cột bảng tính** | Khớp nối các trường thông tin cào được vào các cột tương ứng trong bảng của bạn. |
| **4** | **Bắt đầu quét dữ liệu** | Nhấp nút **Bắt đầu tìm kiếm**. Hệ thống thông báo tác vụ ngầm đã khởi tạo thành công. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Theo dõi tác vụ ngầm** | Mở tiện ích *Danh sách lịch sử chạy ngầm*, tác vụ Google Maps Crawl hiển thị trạng thái `COMPLETED (Hoàn thành)`. |
| **Dữ liệu trong bảng tính** | Ngoài Grid View xuất hiện đầy đủ danh sách các cơ sở kinh doanh với tên gọi, số điện thoại hotline, địa chỉ và điểm đánh giá sao chuẩn xác. |

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
| **Ghi nhận danh sách địa điểm cào được vào bảng** | `createRecords` | *"Hãy lưu danh sách 20 phòng khám nha khoa vừa thu thập từ Google Maps vào bảng 'Danh Bạ Phòng Khám' với các cột Tên, Hotline, Địa chỉ và Điểm đánh giá sao."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Chạy tác vụ cào Google Maps trên giao diện | Gọi `listRecords` thấy các dòng địa điểm mới xuất hiện với đầy đủ thông tin hotline và địa chỉ. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent ghi dữ liệu địa điểm vào bảng | Người dùng mở Dạng xem bảng tính (Grid View), các dòng địa điểm hiển thị trực tiếp trên màn hình. |
