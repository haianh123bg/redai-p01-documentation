## Mở khu vực Lịch sử phiên bản, Liên kết chia sẻ và Đường dẫn trang

Khi ứng dụng đã hoàn thiện giao diện và kết nối dữ liệu, bạn có thể biên dịch bản phát hành chính thức, tạo liên kết chia sẻ kèm mã QR hoặc gắn tên miền riêng thông qua hai lối vào:

1. **Mở nhanh từ thanh tiêu đề Trình xem App (`/app-builder/:appId`)**:
   - Bấm biểu tượng <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)** để mở cửa sổ quản lý bản phát hành.
   - Bấm biểu tượng <img src="https://api.iconify.design/lucide:share.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết chia sẻ)** để mở cửa sổ tạo link chia sẻ và mã QR.
2. **Mở đầy đủ tại trang Cài đặt App (`/app-builder/:appId/settings`)**:
   - Nhấp vào mục <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)** (`?tab=versions`) ở cột danh mục bên trái.
   - Nhấp vào mục <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết chia sẻ)** (`?tab=shares`).
   - Nhấp vào mục <img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> **(Đường dẫn trang)** (`?tab=paths`) để thiết lập đường dẫn URL từng trang, gắn **Tên miền tùy chỉnh (Custom Domain)** và cài đặt **Quyền riêng tư & Bảo mật**.
   - Ngoài ra, để quản lý tập trung tên miền của toàn bộ các ứng dụng trong Workspace, bạn có thể bấm nút <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý tên miền Workspace)** ngay trên thanh công cụ của màn hình **Danh sách App** (`/app-builder`).

---

## Các bước thực hiện

### Chọn hình thức xuất bản và phân phối ứng dụng

Bạn có thể kết hợp cả 3 giai đoạn dưới đây hoặc lựa chọn hình thức phân phối phù hợp với đối tượng người dùng:

| Hình thức phân phối | Khi nào nên sử dụng | Đặc điểm bảo mật & vận hành |
| :--- | :--- | :--- |
| **Giai đoạn 1 — Biên dịch bản phát hành (AOT Build)** | Khi bạn muốn đóng băng mã nguồn ổn định thành một phiên bản chính thức và có thể khôi phục (Rollback) bất cứ lúc nào. | Hệ thống kiểm tra liên kết tĩnh (Static Linker), biên dịch trước toàn bộ các trang bằng SWC giúp tốc độ tải trang tức thì và không ảnh hưởng khi bạn đang sửa bản nháp. |
| **Giai đoạn 2 — Tạo Liên kết chia sẻ & Mã QR Code** | Khi bạn muốn gửi nhanh ứng dụng cho đối tác, khách hàng hoặc nhân viên qua đường dẫn rút gọn `/s/:uuid` hoặc quét mã QR. | Mỗi liên kết có thể cài đặt riêng mật khẩu, ngày hết hạn, danh sách IP cho phép/chặn (Whitelist/Blacklist) và 5 công tắc quyền hạn người xem. |
| **Giai đoạn 3 — Gắn Tên miền tùy chỉnh (Custom Domain)** | Khi doanh nghiệp muốn chạy ứng dụng trên tên miền thương hiệu riêng (ví dụ: `pos.congtycuaban.vn`). | Hỗ trợ xác thực DNS qua cặp bản ghi `CNAME` + `TXT`, tự động cấp chứng chỉ bảo mật `SSL/HTTPS` và cấu hình bảo mật toàn ứng dụng. |

---

### Giai đoạn 1 — Biên dịch bản phát hành mới (AOT Build), so sánh và Rollback phiên bản

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở biểu mẫu tạo phiên bản mới** | Tại mục <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)**, bấm vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo phiên bản mới)** ở góc phải thanh tiêu đề để mở biểu mẫu **Biên dịch & Đóng gói bản phát hành mới (AOT Build)**. |
| **2. Điền thông tin bản phát hành** | Nhập 3 trường thông tin trên biểu mẫu:<br>• **Phiên bản (Ví dụ: 1.0.1, 1.1.0)**: Nhập mã phiên bản theo chuẩn Semantic Versioning (hoặc để trống để hệ thống tự động tăng số phiên bản tiếp theo).<br>• **Tiêu đề tóm tắt**: Nhập tiêu đề ngắn gọn (ví dụ: `Bản cập nhật giao diện & biểu đồ mới`).<br>• **Ghi chú phát hành (Release Notes)**: Mô tả chi tiết những thay đổi trong phiên bản này. |
| **3. Biên dịch SWC & Phát hành** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Biên dịch SWC & Phát hành)**. Hệ thống sẽ biên dịch toàn bộ cây VFS và gắn nhãn **Đang hoạt động (Active)** cho phiên bản vừa tạo. |
| **4. So sánh khác biệt (Diff) và Khôi phục (Rollback) khi cần** | Trên danh sách dòng thời gian phiên bản, mỗi bản phát hành cung cấp các nút thao tác trực tiếp:<br>• <img src="https://api.iconify.design/lucide:git-compare.svg?color=%23ff3333" width="16" alt="" /> **(So sánh khác biệt với bản khác)**: Mở hộp thoại đối chiếu giữa **Phiên bản gốc:** và **Phiên bản so sánh:**, thống kê 4 chỉ số (`Trang thêm mới`, `Trang đã xóa`, `Trang sửa đổi`, `APIs thay đổi`) và hiển thị chi tiết từng dòng mã thay đổi.<br>• <img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> **(Khôi phục toàn bộ App về bản phát hành này (Rollback))**: Hiển thị trên các bản lưu trữ cũ; khi bấm vào và chọn **(Xác nhận khôi phục)**, hệ thống sẽ đưa toàn bộ ứng dụng quay về đúng trạng thái của phiên bản đó.<br>• <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa bản phát hành này)**: Xóa phiên bản lưu trữ không còn sử dụng. |

---

### Giai đoạn 2 — Tạo Liên kết chia sẻ, Mã QR Code và phân quyền người xem

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở biểu mẫu Tạo liên kết mới** | Tại mục <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết chia sẻ)**, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo liên kết mới)** trên thanh công cụ. |
| **2. Thiết lập tên, mật khẩu, thời hạn và giới hạn IP** | Điền các trường kiểm soát truy cập cho liên kết:<br>• **Tên liên kết**: Nhập tên gợi nhớ (ví dụ: `Liên kết đối tác, Xem trước khách hàng...`).<br>• **Bảo vệ bằng mật khẩu**: Bật công tắc nếu muốn yêu cầu mật khẩu khi mở link, sau đó nhập mật khẩu vào ô **Mật khẩu truy cập**.<br>• **Ngày hết hạn (Expiry Date)**: Chọn ngày hết hạn theo định dạng `dd/MM/yyyy` (hoặc để trống nếu không giới hạn ngày).<br>• **Danh sách IP được phép (Whitelist)**: Nhập mỗi địa chỉ IP trên một dòng nếu chỉ cho phép các mạng nội bộ nhất định truy cập.<br>• **Danh sách IP bị chặn (Blacklist)**: Nhập mỗi địa chỉ IP trên một dòng để từ chối truy cập từ các IP đó. |
| **3. Bật/tắt 5 quyền hạn hiển thị của người xem** | Tùy chỉnh 5 công tắc quyền hạn cho người mở liên kết:<br>1. **Cho phép sao chép nội dung**<br>2. **Cho phép tải xuống dữ liệu**<br>3. **Cho phép chia sẻ lại liên kết**<br>4. **Hiển thị thanh tiêu đề App**<br>5. **Cho phép người xem đổi giao diện Sáng / Tối** |
| **4. Lưu liên kết và lấy Mã QR Code** | Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Tạo liên kết)**. Sau khi tạo xong, trên dòng liên kết (hoặc khi bấm **Cấu hình →** để mở lại chi tiết), bạn có thể:<br>• Bấm <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép link chia sẻ)** để gửi URL cho người dùng.<br>• Bấm <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **(Xem mã QR Code)** / **(Phóng to QR)** và bấm <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải ảnh QR)** để tải mã QR định dạng ảnh về máy. |

---

### Giai đoạn 3 — Cấu hình Đường dẫn trang, Tên miền tùy chỉnh (Custom Domain) và Bảo mật toàn App

Tại mục <img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> **(Đường dẫn trang)** (`/app-builder/:appId/settings?tab=paths`), màn hình được chia làm 3 khối thiết lập:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Chỉnh sửa Đường dẫn các trang (Routing)** | Tại khối đầu tiên **Đường dẫn các trang (Routing)**:<br>• Kiểm tra bảng danh sách gồm cột **Tên trang** và cột **Đường dẫn URL** (ví dụ: `/home`, `/orders`).<br>• Sau khi chỉnh sửa đường dẫn URL của các trang (hoặc bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ khỏi App)** nếu muốn gỡ trang), bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu đường dẫn)** ở góc phải trên của khối. |
| **2. Kết nối Tên miền tùy chỉnh (Custom Domain) qua 4 bước** | Tại khối thứ hai **Tên miền tùy chỉnh (Custom Domain)**, thực hiện theo hướng dẫn 4 bước hiển thị trên màn hình:<br>• **Bước 1 (Nhập Subdomain)**: Nhập tên miền phụ của bạn vào ô `app.yourdomain.com (ví dụ: dashboard.mycompany.vn)` rồi bấm nút <img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> **(Kết nối tên miền)**.<br>• **Bước 2 & Bước 3 (Cấu hình bản ghi CNAME & TXT trên trang quản trị tên miền)**: Xem bảng **Danh sách bản ghi DNS cần tạo trên Quản trị tên miền**, bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép toàn bộ bản ghi DNS)** (hoặc bấm <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép đích)** tại mục **Máy chủ hệ thống (CNAME Target):** `dashboard-app.redai.vn`) để thêm bản ghi `CNAME` và bản ghi xác thực `TXT` tại nhà cung cấp tên miền (Cloudflare, Tenten, Nhân Hòa, MatBao...).<br>• **Bước 4 (Xác thực & Kích hoạt)**: Quay lại màn hình RedAI và bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra & Xác thực DNS)**. Khi DNS hợp lệ, trạng thái sẽ chuyển sang **Hoạt động (Active)** kèm chứng chỉ **SSL/HTTPS**. |
| **3. Thiết lập Quyền riêng tư & Bảo mật cho toàn bộ App** | Tại khối thứ ba **Quyền riêng tư & Bảo mật**:<br>• Bật công tắc **Bảo vệ toàn bộ App bằng mật khẩu** và nhập **Mật khẩu truy cập** nếu muốn khóa mật khẩu chung cho ứng dụng.<br>• Điền **Danh sách IP được phép (Whitelist)** và **Danh sách IP bị chặn (Blacklist)**.<br>• Bật/tắt 2 công tắc giao diện chung: **Hiển thị thanh header của App** và **Cho phép người dùng đổi giao diện**.<br>• Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cấu hình)** để áp dụng. |

---

## Kiểm tra kết quả

1. **Tại mục Lịch sử phiên bản**: Phiên bản vừa biên dịch hiển thị nhãn màu xanh **Đang hoạt động (Active)** cùng đầy đủ thống kê `{N} trang VFS`, `{N} tệp VFS` và `Route chính`.
2. **Tại mục Liên kết chia sẻ**: Khi mở đường dẫn chia sẻ ở cửa sổ ẩn danh của trình duyệt, hệ thống kiểm tra đúng mật khẩu (nếu bật), hiển thị đúng các quyền sao chép/đổi giao diện đã cấp và mã QR quét được trực tiếp bằng điện thoại.
3. **Tại mục Đường dẫn trang**: Khối **Tên miền tùy chỉnh (Custom Domain)** hiển thị nhãn **Hoạt động (Active)** ở cả hai mục **DNS / Định tuyến** và **Chứng chỉ SSL/HTTPS**.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động biên dịch bản phát hành mới (`Compile Release`), kiểm tra lịch sử phiên bản, khôi phục phiên bản cũ (`Rollback`), tạo mã QR truy cập ứng dụng hoặc xuất gói ứng dụng mà không cần thao tác tay trên giao diện.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - App Builder` (ID: `58f36f44-2e1c-4aaf-8ca7-d73008169e95`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - App Builder` (ID: `d16e4656-c070-43b6-b234-abcff883fd61`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản trị và phát hành ứng dụng trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Điền biểu mẫu phiên bản và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Biên dịch SWC & Phát hành)** | `appRelease_compile` | Kiểm tra liên kết mã nguồn, biên dịch AOT bằng SWC và phát hành phiên bản mới cho ứng dụng. |
| Mở mục <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)** để xem danh sách và bản đang hoạt động | `appRelease_list`, `appRelease_getActive`, `appRelease_getDetail` | Liệt kê tất cả các bản phát hành, lấy thông tin bản `Active` hiện tại và xem chi tiết từng bản phát hành. |
| Bấm <img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> **(Khôi phục toàn bộ App về bản phát hành này (Rollback))** | `appRelease_rollback` | Khôi phục toàn bộ cây mã nguồn VFS và cấu hình ứng dụng về một bản phát hành trước đó. |
| Bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa bản phát hành này)** | `appRelease_delete` | Xóa một bản phát hành lưu trữ không còn sử dụng. |
| Bấm <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **(Xem mã QR Code)** để sinh mã QR truy cập nhanh | `appQrCode_generateAppQrCode` | Sinh mã QR Code cho ứng dụng để chia sẻ nhanh. |
| Xuất đóng gói toàn bộ ứng dụng | `appPackage_exportAppPackage` | Đóng gói và xuất toàn bộ cấu hình cùng mã nguồn VFS của ứng dụng. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi kiểm tra chất lượng mã nguồn, biên dịch bản phát hành mới và tạo mã QR cho ứng dụng trên App Builder:

1. Bối cảnh và Mục tiêu:
- Tôi vừa hoàn thiện các trang giao diện của ứng dụng và muốn đóng gói thành bản phát hành chính thức (Active Release) để gửi mã QR cho đội ngũ vận hành.

2. Dữ liệu cung cấp:
- ID ứng dụng (appId): "[Điền ID ứng dụng của bạn]"
- Phiên bản phát hành: "1.1.0"
- Tiêu đề tóm tắt: "Hoàn thiện Dashboard và danh sách đơn hàng"
- Ghi chú phát hành (Release Notes): "Cập nhật biểu đồ doanh thu thực thu, bộ lọc thời gian và tối ưu hiển thị Dark Mode."

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng pageValidation_validateJsx kiểm tra nhanh toàn bộ các trang để đảm bảo không có lỗi cú pháp trước khi biên dịch.
- Bước 2: Dùng công cụ appRelease_compile để biên dịch và phát hành phiên bản "1.1.0" với tiêu đề và ghi chú phát hành ở trên.
- Bước 3: Dùng appRelease_getActive để xác nhận phiên bản "1.1.0" đã trở thành bản Đang hoạt động (Active).
- Bước 4: Dùng appQrCode_generateAppQrCode để tạo mã QR truy cập ứng dụng.

4. Yêu cầu phản hồi:
- Báo cáo trạng thái biên dịch, thông tin phiên bản Active hiện tại (ID bản phát hành, thời gian phát hành, số lượng trang/tệp VFS) và đường dẫn/mã QR truy cập ứng dụng.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở `/app-builder/:appId/settings?tab=versions` để kiểm tra phiên bản `1.1.0` đã hiện nhãn **Đang hoạt động (Active)** trên đầu danh sách dòng thời gian. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `appRelease_list` cho ứng dụng này để liệt kê toàn bộ lịch sử phiên bản và trạng thái Active hiện tại."* |
