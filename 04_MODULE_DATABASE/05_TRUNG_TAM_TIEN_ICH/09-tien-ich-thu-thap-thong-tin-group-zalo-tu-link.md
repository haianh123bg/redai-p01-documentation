## Tổng quan Tiện ích Thu thập thông tin Group Zalo từ link

Tiện ích **Thu thập thông tin Group Zalo từ link** là công cụ cào dữ liệu cộng đồng chuyên biệt trên **RedAI Database**. Tiện ích tự động quét danh sách các đường dẫn nhóm Zalo lưu trong bảng, sử dụng tài khoản Zalo cá nhân đã liên kết để truy cập và bóc tách thông tin nhóm (Tên nhóm, UID nhóm, Số lượng thành viên, Ảnh đại diện nhóm) cùng toàn bộ danh sách thành viên trong nhóm (UID Zalo cá nhân, Tên hiển thị, Ảnh đại diện), đồng thời hỗ trợ tự động gắn Thẻ hội thoại (Conversation Tags) và lưu ngược lại vào Bảng Động qua hệ thống tác vụ ngầm an toàn.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Tài khoản Zalo thực thi** | **Menu chọn tài khoản Zalo kết nối** | Chọn tài khoản Zalo cá nhân đã quét mã QR kết nối thành công trong phân hệ *Tích hợp (Integrations)* để thực hiện thao tác cào dữ liệu. |
| **2. Cột chứa liên kết nhóm Zalo** | **Menu chọn cột URL nguồn** | Hệ thống tự động lọc các cột kiểu `URL` có chứa các đường dẫn dạng `https://zalo.me/g/...`. |
| **3. Chế độ thu thập thông tin** | • **Chỉ thu thập thông tin nhóm:** | Thu thập thông tin tổng quan của các nhóm: Tên nhóm, Mã định danh UID nhóm Zalo, Số lượng thành viên hiện tại, Đường dẫn ảnh đại diện nhóm và Link tham gia nhóm. |
| | • **Thu thập toàn bộ thành viên nhóm:** | Đi sâu bóc tách danh sách từng thành viên trong nhóm: Mã UID Zalo thành viên, Tên hiển thị cá nhân, Ảnh đại diện thành viên và Mã hội thoại đa kênh tương ứng. |
| **4. Tự động gắn thẻ hội thoại (Conversation Tags)** | • **Công tắc 'Tự động gắn thẻ':** | Bật công tắc để hệ thống tự động gán thẻ phân loại cho các thành viên được cào về. |
| | • **Menu chọn Thẻ nhãn:** | Chọn một hoặc nhiều thẻ nhãn (ví dụ: `Thành viên Nhóm Bất Động Sản`, `Cộng đồng Khởi Nghiệp`). |
| **5. Bảng đích lưu trữ dữ liệu** | • **Cập nhật vào Bảng hiện tại:** | Ghi đè thông tin nhóm cào được vào các cột tương ứng trên cùng dòng bản ghi có chứa link Zalo. |
| | • **Lưu sang Bảng Động đích riêng:** | Thích hợp khi chọn chế độ cào thành viên: mỗi thành viên trong nhóm sẽ trở thành một dòng bản ghi mới trong Bảng Động danh bạ khách hàng. |
| **6. Khởi chạy tác vụ ngầm (SysJobs)** | **Nút 'Bắt đầu thu thập dữ liệu'** | Chuyển tác vụ vào hàng đợi chạy ngầm của hệ thống để thực hiện tuần tự, có khoảng trễ ngẫu nhiên giữa các nhóm để đảm bảo an toàn tuyệt đối cho tài khoản Zalo. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Thu thập thông tin Group Zalo từ link**. |
| **2** | **Chọn tài khoản và cột link** | Chọn tài khoản Zalo cá nhân thực thi và chọn cột chứa các đường dẫn nhóm Zalo trong bảng. |
| **3** | **Chọn chế độ và gắn thẻ** | Chọn chế độ cào mong muốn (Thông tin nhóm hoặc Danh sách thành viên). Nếu cần phân loại, bật công tắc gắn thẻ và chọn thẻ tương ứng. |
| **4** | **Chọn bảng nhận dữ liệu** | Khớp nối các trường thông tin cào được vào các cột của bảng đích. |
| **5** | **Khởi chạy tiến trình** | Nhấp nút **Bắt đầu thu thập dữ liệu nhóm**. Hệ thống thông báo tác vụ đã được tạo thành công và cung cấp liên kết mở tiện ích *Danh sách lịch sử chạy ngầm* để theo dõi tiến độ. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Tiến độ trong Lịch sử chạy ngầm** | Mở tiện ích *Danh sách lịch sử chạy ngầm*, dòng tác vụ Zalo Group Crawl hiển thị tiến độ tăng dần và chuyển sang trạng thái `COMPLETED (Hoàn thành)`. |
| **Dữ liệu trong Bảng Động** | Bảng đích hiển thị đầy đủ tên nhóm, số lượng thành viên hoặc danh sách các thành viên Zalo kèm mã UID và ảnh đại diện. |
| **Thẻ hội thoại trong OmniChat** | Mở phân hệ Chat Đa Kênh, các liên hệ mới xuất hiện kèm đúng thẻ nhãn đã cấu hình. |

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
| **Truy vấn danh sách link nhóm Zalo để chuẩn bị cào dữ liệu** | `listRecords` | *"Hãy đọc danh sách các đường dẫn nhóm Zalo từ cột 'Link Group' trong bảng 'Nguồn Nhóm Khách Hàng' để kiểm tra tính hợp lệ của các liên kết."* |
| **Cập nhật thông tin thành viên nhóm Zalo vào Bảng Động** | `createRecords`, `updateRecords` | *"Hãy ghi danh sách 50 thành viên nhóm Zalo vừa cào được vào bảng 'Danh Bạ Zalo' gồm đầy đủ UID Zalo, Tên hiển thị và Thẻ 'Thành viên Zalo Group'."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Chạy tác vụ cào nhóm Zalo trên giao diện | Gọi `listRecords` trên bảng đích thấy các dòng thành viên mới xuất hiện với đầy đủ UID Zalo. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent ghi dữ liệu thành viên nhóm vào bảng | Người dùng mở bảng tính ngoài Grid View, danh sách thành viên Zalo hiển thị đầy đủ thông tin. |
