## Tổng quan Tiện ích Danh sách lịch sử chạy ngầm (SysJobs History)

Tiện ích **Danh sách lịch sử chạy ngầm (SysJobs History)** là trung tâm giám sát và quản lý tác vụ ngầm tập trung trên **RedAI Database**. Khi người dùng thực thi các tiến trình xử lý dữ liệu lớn (nhập file Excel dung lượng lớn, cào thông tin nhóm Zalo, cào dữ liệu Google Maps hoặc xuất bản hàng loạt tài liệu PDF), hệ thống sẽ đưa tác vụ vào hàng đợi chạy ngầm (SysJobs) để tránh làm đơ giao diện người dùng. Tiện ích này cung cấp bảng điều khiển theo dõi tiến độ thời gian thực, quản lý trạng thái, tra cứu nhật ký lỗi chi tiết và hủy các tác vụ đang treo.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Bộ lọc trạng thái tác vụ** | • **Tất cả trạng thái:** | Hiển thị toàn cảnh các tác vụ ngầm trong Không gian làm việc. |
| | • **Chờ xử lý (PENDING):** | Tác vụ đang xếp hàng đợi tài nguyên máy chủ. |
| | • **Đang xử lý (PROCESSING):** | Tác vụ đang chạy thực thi dữ liệu theo thời gian thực. |
| | • **Hoàn thành (COMPLETED):** | Tác vụ đã thực thi 100% dữ liệu thành công. |
| | • **Thất bại (FAILED):** | Tác vụ gặp sự cố kỹ thuật hoặc dữ liệu đầu vào không hợp lệ. |
| **2. Bảng theo dõi tiến độ chi tiết** | • **Tên & Loại tác vụ:** | Định danh loại tiến trình (ví dụ: `Cào dữ liệu Google Maps`, `Thu thập thành viên Zalo Group`, `Nhập khẩu bảng tính`). |
| | • **Thanh tiến độ phần trăm (%):** | Hiển thị tỷ lệ hoàn thành thực tế (ví dụ: `85% - 85/100 bản ghi`). |
| | • **Thời gian bắt đầu / Kết thúc:** | Ghi nhận chính xác mốc thời gian phát động và thời lượng chạy tiến trình. |
| | • **Người khởi tạo:** | Tên và ảnh đại diện của nhân sự đã phát động tác vụ. |
| **3. Tra cứu nhật ký lỗi (Error Logs)** | **Biểu tượng xem nhật ký lỗi** | Đối với các tác vụ có trạng thái `FAILED`, nhấp vào biểu tượng thông tin để mở hộp thoại đọc toàn văn thông báo lỗi hệ thống (Error StackTrace), giúp kỹ thuật viên nhanh chóng phát hiện nguyên nhân gốc rễ. |
| **4. Các nút thao tác quản trị** | • <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Nút 'Làm mới danh sách':** | Tải lại trạng thái các tác vụ mới nhất theo thời gian thực. |
| | • <img src="https://api.iconify.design/lucide:stop-circle.svg?color=%23ff3333" width="16" alt="" /> **Nút 'Hủy tác vụ':** | Cho phép quản trị viên dừng khẩn cấp các tiến trình đang chạy hoặc đang chờ trong hàng đợi. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:clock.svg?color=%23ff3333" width="16" alt="" /> **Danh sách lịch sử chạy ngầm**. Bảng theo dõi tác vụ ngầm xuất hiện. |
| **2** | **Lọc theo trạng thái** | Chọn lọc `Đang xử lý (PROCESSING)` để xem các tiến trình đang chạy ngoài nền. |
| **3** | **Theo dõi tiến độ** | Quan sát thanh phần trăm tiến trình đang tăng dần. Nhấp nút **Làm mới** nếu cần cập nhật tức thời. |
| **4** | **Xử lý sự cố lỗi** | Nếu có tác vụ báo đỏ `FAILED`, nhấp vào xem chi tiết lỗi để nắm rõ lý do (ví dụ: *Tài khoản Zalo bị đăng xuất*, *Mất kết nối mạng*). |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Trạng thái hoàn thành** | Dòng tác vụ chuyển sang huy hiệu màu xanh **COMPLETED (Hoàn thành)**, thanh tiến độ đạt 100%. |
| **Dữ liệu đồng bộ** | Sau khi tác vụ báo hoàn tất, mở bảng dữ liệu đích thấy toàn bộ các bản ghi đã được ghi đầy đủ và đồng bộ. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền đọc cơ sở dữ liệu (`BASE_READ`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Kiểm tra trạng thái tác vụ chạy ngầm của bảng** | `getTable`, `listRecords` | *"Hãy kiểm tra xem tác vụ cào dữ liệu Google Maps vừa khởi chạy đã hoàn tất chưa và có bản ghi mới nào được tạo trong bảng không."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Tác vụ chuyển sang `COMPLETED` trên giao diện | Gọi `countRecords` thấy tổng số bản ghi trong bảng tăng lên tương ứng với số lượng dữ liệu đã xử lý. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent kiểm tra tiến trình hoàn tất | Người dùng mở tiện ích Lịch sử chạy ngầm, dòng tác vụ hiển thị trạng thái hoàn thành màu xanh. |
