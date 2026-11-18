## Tổng quan Tiện ích Báo Cáo Sức khỏe & Chất lượng dữ liệu

Tiện ích **Báo Cáo Sức khỏe & Chất lượng dữ liệu** đóng vai trò như một bảng điều khiển kiểm toán sức khỏe (Health Audit Dashboard) cho cơ sở dữ liệu trên **RedAI Database**. Tiện ích tự động quét toàn bộ các bản ghi trong Dạng xem (tối đa 1.000 dòng), tính toán Thang điểm Hoàn thiện tổng thể (0–100%), bóc tách tỷ lệ lấp đầy của từng cột dữ liệu, phát hiện các ô tính bị bỏ trống hoặc sai định dạng cú pháp (Email, SĐT) và tích hợp các nút chuyển tiếp 1 cú nhấp tới công cụ xử lý tương ứng.

---

## Chi tiết các chỉ số và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết đo lường & Phản hồi trực quan |
| :--- | :--- | :--- |
| **1. Điểm số Sức khỏe Tổng thể** | **Vòng tròn điểm chất lượng (0–100%)** | Điểm số trung bình cộng độ hoàn thiện của toàn bộ các cột trong bảng:<br>• `90% – 100% (Màu xanh lá)`: Cơ sở dữ liệu đạt chuẩn hoàn hảo, tỷ lệ lấp đầy cao, không có lỗi định dạng.<br>• `70% – 89% (Màu vàng/cam)`: Dữ liệu ở mức khá, có một số ô trống hoặc cảnh báo cần bổ sung.<br>• `< 70% (Màu đỏ)`: Dữ liệu thiếu hụt nghiêm trọng, cần tiến hành chuẩn hóa hoặc bổ sung thông tin khẩn cấp. |
| **2. Bộ lọc theo nhóm cảnh báo** | • **Thẻ tab 'Tất cả các cột':** | Hiển thị toàn cảnh các trường dữ liệu trong bảng. |
| | • **Thẻ tab 'Cột có cảnh báo định dạng':** | Lọc riêng các cột Số điện thoại hoặc Email có chứa dữ liệu sai lệch cấu trúc regex viễn thông. |
| | • **Thẻ tab 'Cột có ô trống dữ liệu':** | Lọc các cột có tỷ lệ lấp đầy dưới 100% để người dùng nhanh chóng xác định các trường bị thiếu sót. |
| **3. Bảng phân tích chi tiết từng cột** | • **Cột dữ liệu:** | Tên cột kèm biểu tượng kiểu dữ liệu (Văn bản, Số, SĐT, Email...). |
| | • **Thanh tiến độ % hoàn thiện:** | Đo lường tỷ lệ phần trăm số dòng có dữ liệu so với tổng số dòng của bảng. |
| | • **Chỉ số Ô đã điền / Ô trống:** | Hiển thị số lượng ô cụ thể (ví dụ: `480/500 ô đã điền, 20 ô trống`). |
| | • **Chỉ số Giá trị duy nhất:** | Thống kê số lượng giá trị không trùng nhau trong cột (Unique Count). |
| | • **Huy hiệu cảnh báo lỗi định dạng:** | Hiển thị số lượng ô sai cú pháp (ví dụ: email thiếu `@` hoặc `.`, SĐT không đủ 9-12 chữ số). |
| **4. Nút tắt xử lý nhanh 1 cú nhấp** | • <img src="https://api.iconify.design/lucide:wand-2.svg?color=%23ff3333" width="16" alt="" /> **Làm sạch ngay** | Mở thẳng tiện ích *Chuẩn hóa & Làm sạch dữ liệu* với cột đó được chọn sẵn. |
| | • <img src="https://api.iconify.design/lucide:git-merge.svg?color=%23ff3333" width="16" alt="" /> **Quét trùng lặp** | Mở ngay tiện ích *Quét trùng lặp* đối với trường dữ liệu tương ứng. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:alert-circle.svg?color=%23ff3333" width="16" alt="" /> **Báo cáo Sức khỏe & Chất lượng dữ liệu**. |
| **2** | **Quan sát Thang điểm tổng thể** | Xem xét điểm số phần trăm ở đầu trang để đánh giá nhanh chất lượng tệp dữ liệu. |
| **3** | **Lọc theo tab cảnh báo** | Nhấp vào tab `Cột có cảnh báo định dạng` để xem các trường có nguy cơ gây lỗi gửi thư hoặc gửi tin nhắn. |
| **4** | **Điều hướng xử lý tức thì** | Bấm vào nút **Làm sạch ngay** tại dòng cột có cảnh báo. Hệ thống tự động chuyển tiếp sang giao diện làm sạch để người dùng chọn quy tắc và bấm thực thi ngay mà không cần cấu hình lại từ đầu. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Điểm chất lượng sau khi xử lý** | Sau khi thực hiện làm sạch hoặc điền bổ sung dữ liệu, mở lại báo cáo, điểm số tăng lên (tiệm cận 100%). |
| **Trạng thái cảnh báo** | Huy hiệu cảnh báo màu đỏ biến mất, danh sách tab `Cột có cảnh báo định dạng` trống rỗng. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền đọc bản ghi (`RECORD_READ`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Đo lường độ hoàn thiện & phát hiện ô trống dữ liệu** | `countRecords`, `listRecords` | *"Hãy kiểm tra chất lượng dữ liệu của bảng 'Khách Hàng', tính toán tỷ lệ phần trăm các ô có dữ liệu trên từng cột và lập danh sách các bản ghi bị khuyết trường 'Email'."* |
| **Kiểm tra cú pháp định dạng số điện thoại & email** | `listRecords` | *"Hãy quét toàn bộ cột 'Số điện thoại' trong bảng 'Học Viên', phát hiện các số điện thoại sai định dạng (dưới 9 số hoặc chứa ký tự đặc biệt) và báo cáo lại."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Xem bảng báo cáo sức khỏe trên giao diện | Gọi `countRecords` và `listRecords` thấy tỷ lệ các dòng có dữ liệu khớp hoàn toàn với con số hiển thị trên giao diện. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent phát hiện và điền bổ sung dữ liệu | Mở Hộp thoại Báo cáo sức khỏe, điểm chất lượng dữ liệu tăng lên và tỷ lệ hoàn thiện hiển thị 100%. |
