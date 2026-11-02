## Mở khu vực Danh sách App và Trình xem App Studio

Để bắt đầu khởi tạo ứng dụng thu nhỏ (MiniApp / Dashboard), ghép trang từ kho mẫu và quản lý cấu trúc trang trên **App Builder**, bạn truy cập vào một trong các đường dẫn sau trên thanh điều hướng bên trái của hệ thống **RedAI**:

1. **Danh sách App (`/app-builder`)**: Hiển thị toàn bộ các ứng dụng trong không gian làm việc (Workspace) hiện tại. Trên thanh công cụ phía trên cùng bao gồm:
   - Ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm App theo tên hoặc ID...)**.
   - Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo App)** để mở hộp thoại khởi tạo ứng dụng mới.
   - Nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới)** và nút <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo Thẻ)**.
   - Các nút điều hướng và tiện ích mở rộng: <img src="https://api.iconify.design/lucide:layout.svg?color=%23ff3333" width="16" alt="" /> **(Mẫu Template App Builder)**, <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ff3333" width="16" alt="" /> **(App của hệ thống)**, <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Môi trường Workspace (Environments))**, <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý tên miền Workspace)**, <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import App từ file ZIP)** và <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Thẻ App)**.
2. **Trình xem App / App Studio (`/app-builder/:appId`)**: Nhấp trực tiếp vào một thẻ ứng dụng bất kỳ trên danh sách để mở không gian làm việc của ứng dụng đó. Thanh tiêu đề phía trên cùng của trình xem được bố trí như sau:
   - **Cụm điều khiển bên trái**:
     - Nút <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **(Quản Lý Trang)**: Mở hộp thoại quản lý danh sách trang của ứng dụng.
     - **Tên App**: Bạn có thể **nhấp đúp chuột (double-click)** trực tiếp vào tên ứng dụng trên thanh tiêu đề để đổi tên nhanh tại chỗ (nhấn phím `Enter` để lưu hoặc `Escape` để hủy).
   - **Cụm 11 nút công cụ bên phải**:
     - <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)**: Mở ngăn chọn và gắn công cụ API (Custom Tools / Dynamic Tables) vào ứng dụng.
     - <img src="https://api.iconify.design/lucide:store.svg?color=%23ff3333" width="16" alt="" /> **(Thư viện App)**: Mở hộp thoại **Thư viện App & Trang Mẫu** để áp dụng nguyên gói mẫu hoặc ghép từng trang lẻ vào ứng dụng đang mở.
     - <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải Lại)**: Làm mới lại khung hiển thị ứng dụng.
     - <img src="https://api.iconify.design/lucide:bar-chart.svg?color=%23ff3333" width="16" alt="" /> **(Thống kê)**: Xem nhanh số liệu thống kê của ứng dụng.
     - <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)**: Xem và quản lý các bản phát hành của ứng dụng.
     - <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình Theme)**: Mở trình chỉnh sửa bảng màu và giao diện.
     - <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình AI Agent đọc dữ liệu App)**: Mở cấu hình Agent Semantic View.
     - <img src="https://api.iconify.design/lucide:share.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết chia sẻ)**: Mở hộp thoại quản lý đường dẫn chia sẻ và mã QR.
     - <img src="https://api.iconify.design/lucide:maximize.svg?color=%23ff3333" width="16" alt="" /> **(Toàn màn hình)** / <img src="https://api.iconify.design/lucide:minimize.svg?color=%23ff3333" width="16" alt="" /> **(Thoát toàn màn hình)**: Mở rộng khung xem ứng dụng ngay trong tab hiện tại.
     - <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **(Mở tab xem toàn màn hình (Live Realtime))**: Mở trang `/app-builder/:appId/preview` ở một tab trình duyệt mới kèm nút bong bóng điều khiển nổi RedAI.
     - <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt)**: Chuyển sang trang cài đặt toàn diện của ứng dụng (`/app-builder/:appId/settings`).
   - **Nút tự động hỗ trợ khi gặp lỗi hiển thị**: Nếu mã nguồn trang gặp sự cố trong lúc chạy (Runtime Error), góc dưới bên phải khung xem sẽ tự động xuất hiện nút nổi màu đỏ <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Sửa lỗi với AI)** để bạn gửi toàn bộ ngữ cảnh lỗi cho trợ lý AI khắc phục ngay lập tức.

---

## Các bước thực hiện

### Chọn phương án khởi tạo ứng dụng phù hợp

Trước khi bắt đầu ở Giai đoạn 1, hãy chọn phương án khởi tạo phù hợp với nhu cầu của bạn:

| Phương án khởi tạo | Khi nào nên sử dụng | Kết quả nhận được |
| :--- | :--- | :--- |
| **Phương án 1 — Tạo App mới từ đầu** | Khi bạn muốn tạo một không gian ứng dụng trống để tự thiết kế hoặc nhờ trợ lý ảo AI Agent lập trình giao diện theo yêu cầu riêng. | Một ứng dụng mới được khởi tạo ngay lập tức với tên và mô tả bạn đã nhập. |
| **Phương án 2 — Sử dụng mẫu từ Kho Template** | Khi bạn muốn nhân bản nhanh một ứng dụng mẫu hoàn chỉnh có sẵn trên hệ thống hoặc chỉ lấy một vài trang lẻ từ mẫu ghép vào ứng dụng đang có. | Tạo ra một ứng dụng độc lập có đầy đủ trang và giao diện mẫu, hoặc thêm các trang đã chọn vào ứng dụng đích. |
| **Phương án 3 — Import App từ file ZIP** | Khi bạn có sẵn gói mã nguồn VFS định dạng `.zip` (tối đa 50MB) được xuất ra từ một ứng dụng hoặc môi trường RedAI khác. | Hệ thống tự động kiểm tra cấu trúc VFS, giải nén toàn bộ các trang, thành phần giao diện và tạo thành ứng dụng mới. |

---

### Giai đoạn 1 — Khởi tạo ứng dụng mới

#### Phương án 1 — Tạo App mới từ đầu

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Tạo App mới** | Tại màn hình **Danh sách App** (`/app-builder`), bấm vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo App)** trên thanh công cụ phía trên. |
| **2. Nhập thông tin cơ bản** | Trong hộp thoại **Tạo App mới**, điền 2 trường thông tin:<br>• **Tên App \***: Nhập tên ứng dụng của bạn (ví dụ: `RedAI E-Commerce App...`).<br>• **Mô tả ngắn**: Nhập mô tả mục đích và chức năng của ứng dụng. |
| **3. Xác nhận khởi tạo** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo)** ở góc dưới bên phải hộp thoại (hoặc bấm <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> **(Hủy)** nếu muốn đóng lại). |

#### Phương án 2 — Sử dụng mẫu từ Kho Template hoặc ghép trang lẻ

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở Kho Mẫu Template** | Tại màn hình **Danh sách App** (`/app-builder`), bấm nút <img src="https://api.iconify.design/lucide:layout.svg?color=%23ff3333" width="16" alt="" /> **(Mẫu Template App Builder)** trên thanh công cụ để chuyển sang trang `/app-builder/templates`. |
| **2. Xem trước mẫu đa thiết bị (Tùy chọn)** | Trên thẻ của mẫu muốn kiểm tra, bấm nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem trước)**. Trong hộp thoại xem trước:<br>• Chuyển đổi kích thước khung nhìn bằng 3 nút: <img src="https://api.iconify.design/lucide:monitor.svg?color=%23ff3333" width="16" alt="" /> **(Máy tính)**, <img src="https://api.iconify.design/lucide:tablet.svg?color=%23ff3333" width="16" alt="" /> **(Máy tính bảng)** (`768 × 1024`), <img src="https://api.iconify.design/lucide:smartphone.svg?color=%23ff3333" width="16" alt="" /> **(Điện thoại)** (`390 × 844`).<br>• Chuyển đổi các trang trong mẫu tại mục <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Trang:** hoặc bấm <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải lại)**.<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Chọn)** ở góc dưới bên phải để chuyển sang hộp thoại tải mẫu. |
| **3. Chọn chế độ tải mẫu** | Khi bấm <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải mẫu)** trên thẻ Template (hoặc bấm **Chọn** từ cửa sổ xem trước), hộp thoại hiển thị 2 tab:<br>• **Nếu muốn tạo thành một ứng dụng mới hoàn chỉnh**: Giữ nguyên ở tab <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải về (Tạo App mới))** rồi bấm nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải về tạo App mới)** ở góc dưới bên phải.<br>• **Nếu chỉ muốn lấy một số trang ghép vào ứng dụng đang có**: Chuyển sang tab <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Tải lẻ các trang vào 1 App)**, chọn ứng dụng đích tại mục **1. Chọn MiniApp đích muốn ghép trang:**, tích chọn các trang muốn lấy tại mục **2. Chọn các trang mẫu cần thêm (X/Y):** (có thể dùng nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Chọn tất cả các trang)**), sau đó bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Thêm {số lượng} trang vào App)**. |

#### Phương án 3 — Import App từ file ZIP (Dành cho Không gian Hệ thống)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Import ZIP** | Tại màn hình **Danh sách App** (`/app-builder`), bấm nút <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import App từ file ZIP)** trên thanh công cụ. |
| **2. Tải lên và kiểm tra cấu trúc gói** | Kéo thả tệp `.zip` (tối đa 50MB) vào vùng <img src="https://api.iconify.design/lucide:upload-cloud.svg?color=%23ff3333" width="16" alt="" /> **(Kéo thả file .zip vào đây hoặc click để chọn)**. Hệ thống sẽ tự động phân tích và hiển thị bảng thông tin gồm: **Tên App phát hiện**, **Số trang (Pages)**, **Components** và **Các đường dẫn (Routes)**. |
| **3. Đặt tên ghi đè và bắt đầu Import** | Bạn có thể nhập tên mới vào ô **Tên App ghi đè (Tùy chọn)** (nếu để trống, hệ thống sẽ lấy theo tên gốc trong tệp `app.json` của gói ZIP). Sau đó bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Bắt đầu Import)** và bấm <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Mở App ngay)** sau khi hoàn tất. |

---

### Giai đoạn 2 — Kết nối Nguồn dữ liệu & APIs cho ứng dụng

Để ứng dụng hiển thị và thao tác với dữ liệu thực tế từ **Bảng dữ liệu động (Dynamic Tables)** hoặc các dịch vụ bên ngoài, bạn cần gắn các công cụ API (Custom Tools) vào ứng dụng:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở ngăn Nguồn dữ liệu & APIs** | Tại màn hình Trình xem App (`/app-builder/:appId`), bấm nút <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)** trên thanh tiêu đề phía trên (hoặc vào **Cài đặt** $\rightarrow$ mục <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)** $\rightarrow$ bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gắn thêm API)**). |
| **2. Tìm và lọc công cụ API** | Trong cửa sổ **Nguồn dữ liệu & APIs**:<br>• Chọn tab nguồn công cụ: **(Cá nhân)** hoặc **(Hệ thống)**.<br>• Sử dụng ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm công cụ...)** hoặc bấm các nút lọc nhanh theo phương thức HTTP: **(GET)**, **(POST)**, **(PUT)**, **(PATCH)**, **(DELETE)**. |
| **3. Chọn nhóm Project Schema và từng API** | Nhấp vào từng nhóm dự án công cụ (<img src="https://api.iconify.design/lucide:package.svg?color=%23ff3333" width="16" alt="" /> Project Schema) để mở rộng danh sách các hàm API bên trong. Tích chọn từng công cụ (<img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" />) cần cấp quyền cho ứng dụng hoặc bấm **(Chọn cả nhóm)** để chọn toàn bộ API của bảng dữ liệu đó. |
| **4. Lưu danh sách API liên kết** | Kiểm tra số lượng tại dòng **Đã chọn: {số lượng} API**, sau đó bấm nút **(Lưu)** ở góc dưới bên phải cửa sổ. |

---

### Giai đoạn 3 — Quản lý trang, ghép trang từ Thư viện App và kiểm thử giao diện

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Quản lý danh sách trang hiện có** | Trên thanh tiêu đề bên trái của Trình xem App, bấm nút <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **(Quản Lý Trang)**. Tại đây bạn có thể:<br>• Nhấp trực tiếp vào một dòng trang bất kỳ để chuyển khung nhìn sang trang đó.<br>• Bấm vào biểu tượng <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)** ở cuối dòng trang để thực hiện 1 trong 3 hành động:<br>  1. <img src="https://api.iconify.design/lucide:pencil.svg?color=%23ff3333" width="16" alt="" /> **(Cập nhật thông tin trang)**: Sửa **Tên trang** và **Mô tả trang**, sau đó bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu)**.<br>  2. <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Nhân bản sang APP khác)**: Chọn một ứng dụng đích trong Workspace để sao chép trang này sang.<br>  3. <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa trang)**: Xóa trang khỏi ứng dụng hiện tại. |
| **2. Ghép thêm trang mẫu hoặc áp dụng gói mẫu ngay trong App** | Bấm nút <img src="https://api.iconify.design/lucide:store.svg?color=%23ff3333" width="16" alt="" /> **(Thư viện App)** trên thanh tiêu đề để mở hộp thoại **Thư viện App & Trang Mẫu**:<br>• Tab <img src="https://api.iconify.design/lucide:package.svg?color=%23ff3333" width="16" alt="" /> **(Gói App Mẫu)**: Bấm <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem trước)** hoặc bấm <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Áp dụng gói)** để ghi đè toàn bộ ứng dụng hiện tại bằng gói mẫu.<br>• Tab <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(Từng Trang Lẻ)**: Tìm trang lẻ cần dùng, bấm <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem trước trang)** hoặc bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Ghép vào App)** để chèn trang đó vào ứng dụng đang mở. |
| **3. Xem trước độc lập và điều khiển bằng Nút bong bóng nổi RedAI** | Bấm nút <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **(Mở tab xem toàn màn hình (Live Realtime))** trên thanh tiêu đề để mở trang `/app-builder/:appId/preview`. Trên màn hình này có **Nút bong bóng nổi RedAI** (có thể kéo thả tự do). Khi nhấp vào nút bong bóng, bạn có 4 công cụ điều khiển nhanh:<br>• <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent)**: Mở ngăn trò chuyện `ChatPanel` ngay bên phải màn hình để ra lệnh cho AI chỉnh sửa giao diện trực tiếp.<br>• <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải Lại)**: Tải lại hệ thống tệp ảo VFS của ứng dụng.<br>• <img src="https://api.iconify.design/lucide:sun.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:moon.svg?color=%23ff3333" width="16" alt="" /> **(Đổi giao diện (Sáng/Tối))**: Kiểm tra giao diện ứng dụng ở cả hai chế độ Light Mode và Dark Mode.<br>• <img src="https://api.iconify.design/lucide:layout-template.svg?color=%23ff3333" width="16" alt="" /> **(App Studio)**: Quay trở về màn hình quản lý `/app-builder/:appId`. |

---

## Kiểm tra kết quả

Sau khi hoàn tất các giai đoạn trên, bạn kiểm tra lại ứng dụng theo các tiêu chí sau:

1. **Tại màn hình Danh sách App (`/app-builder`)**: Thẻ ứng dụng mới xuất hiện trên lưới danh sách với đúng **Tên App**, **Mô tả ngắn** và hiển thị tổng số lượng trang ở góc dưới bên trái (<img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> `{N} Trang`).
2. **Tại hộp thoại Quản Lý Trang**: Tất cả các trang trong ứng dụng hiển thị đầy đủ đường dẫn (`routePath`), số lượng API liên kết (`{N} APIs`) và số lượng thành phần (`{N} components`).
3. **Tại màn hình Xem trước (`/app-builder/:appId/preview`)**: Các trang chuyển hướng mượt mà, dữ liệu từ API hiển thị chính xác trên bảng/biểu đồ, giao diện tương thích tốt khi bấm nút đổi chế độ **Sáng / Tối** và không xuất hiện nút báo lỗi đỏ <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Sửa lỗi với AI)**.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Toàn bộ quy trình từ khởi tạo ứng dụng, gắn bảng dữ liệu/API cho đến lập trình giao diện đa trang trên hệ thống tệp ảo (VFS) và kiểm thử tự động đều có thể giao cho **trợ lý ảo AI Agent** thực hiện hoàn toàn.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Trước khi ra lệnh, hãy đảm bảo trợ lý ảo AI Agent của bạn đã được gắn kỹ năng sau:

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - App Builder` (ID: `58f36f44-2e1c-4aaf-8ca7-d73008169e95`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - App Builder` (ID: `d16e4656-c070-43b6-b234-abcff883fd61`)
- **Quyền hạn tài khoản**: Tài khoản người dùng trong Workspace có quyền tạo và chỉnh sửa MiniApp.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo App)** và điền Tên App, Mô tả ngắn | `app_createApp` | Khởi tạo một ứng dụng MiniApp mới trong Workspace và trả về `appId`. |
| Mở <img src="https://api.iconify.design/lucide:layout.svg?color=%23ff3333" width="16" alt="" /> **(Mẫu Template App Builder)** và bấm <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải mẫu)** | `app_useTemplate` | Nhân bản ứng dụng mới hoặc ghép trang từ một mẫu Template có sẵn. |
| Tra cứu thư viện được phép sử dụng trong mã nguồn VFS | `appCatalog_getLibraries` | Lấy danh sách các thư viện chuẩn (React, Lucide, ECharts, Shadcn UI...) được hỗ trợ trên trình xem. |
| Mở <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)** để tìm và gắn API vào ứng dụng | `listProjectSchemas`, `listCustomTools`, `getCustomToolDetail`, `executeResource_execute` | Tìm kiếm nhóm Project Schema, liệt kê Custom Tools, đọc cấu trúc đầu vào/đầu ra và chạy thử API lấy dữ liệu mẫu thật. |
| Kiểm tra cấu trúc tệp và các trang trong <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **(Quản Lý Trang)** | `agentAppVfs_tree`, `agentAppVfs_summary`, `agentAppVfs_search`, `agentAppVfs_read` | Duyệt cây thư mục ảo VFS (`/app.json`, `/apis.json`, `/pages/...`, `/components/...`) và đọc nội dung từng tệp. |
| Tạo mới, chỉnh sửa hoặc xóa trang và thành phần giao diện | `agentAppVfs_create`, `agentAppVfs_write`, `agentAppVfs_edit`, `agentAppVfs_delete` | Tạo tệp mới, ghi đè nội dung, chỉnh sửa từng đoạn mã nguồn hoặc xóa tệp trong hệ thống VFS của ứng dụng. |
| Bấm <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Sửa lỗi với AI)** hoặc kiểm tra lỗi biên dịch & hiển thị | `pageValidation_validateJsx`, `pageValidation_diagnose`, `pageValidation_getConsoleLogs`, `pageValidation_traceNetwork` | Kiểm tra cú pháp JSX/TSX, chẩn đoán lỗi runtime, đọc nhật ký Console và kiểm tra các lệnh gọi mạng trên trang. |

### Câu lệnh mẫu (Prompt mẫu)

Bạn có thể sao chép mẫu câu lệnh dưới đây, thay đổi tên ứng dụng và yêu cầu nghiệp vụ của mình rồi gửi cho trợ lý ảo AI Agent:

```text
Hãy giúp tôi khởi tạo và xây dựng một ứng dụng MiniApp mới trên App Builder theo quy trình sau:

1. Bối cảnh và Mục tiêu:
- Tôi cần xây dựng ứng dụng quản lý và theo dõi số liệu vận hành theo chuẩn giao diện phẳng (Flat & Borderless), hỗ trợ cả 2 chế độ Sáng (Light Mode) và Tối (Dark Mode).

2. Dữ liệu cung cấp:
- Tên App: "Bảng Điều Khiển Vận Hành Kinh Doanh"
- Mô tả ngắn: "Ứng dụng theo dõi KPI doanh thu, danh sách đơn hàng và biểu đồ tăng trưởng thời gian thực."
- Nguồn dữ liệu: Hãy tìm trong danh sách Project Schemas và Custom Tools của tôi các API liên quan đến đơn hàng và sản phẩm để gắn vào /apis.json của ứng dụng.

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng công cụ app_createApp để tạo ứng dụng mới với tên và mô tả trên.
- Bước 2: Dùng listProjectSchemas, listCustomTools và executeResource_execute để kiểm tra dữ liệu thực tế từ API, sau đó đăng ký các API cần thiết vào tệp /apis.json.
- Bước 3: Thiết kế thanh điều hướng dùng chung (/components/SharedNavbar.tsx) và các trang chính trong /pages/ sử dụng dữ liệu thật 100% từ API.
- Bước 4: Dùng pageValidation_validateJsx và pageValidation_diagnose để kiểm tra toàn bộ các trang, đảm bảo không có lỗi cú pháp hay lỗi runtime.

4. Yêu cầu phản hồi:
- Báo cáo lại ID ứng dụng (appId), danh sách các đường dẫn trang (routePath) đã tạo, danh sách API đã kết nối và kết quả kiểm tra cú pháp/hiển thị của từng trang.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

Sau khi trợ lý ảo AI Agent thông báo đã hoàn thành, bạn có thể kiểm tra lại theo 2 cách:

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Truy cập `/app-builder`, nhấp vào thẻ ứng dụng **Bảng Điều Khiển Vận Hành Kinh Doanh** vừa được tạo, bấm <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **(Quản Lý Trang)** để xem danh sách các trang và bấm <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **(Mở tab xem toàn màn hình (Live Realtime))** để trải nghiệm trực tiếp. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent chụp ảnh và kiểm chứng** | Gửi câu lệnh: *"Hãy dùng công cụ `pageValidation_captureScreenshot` và `pageValidation_diagnose` kiểm tra tất cả các trang của ứng dụng vừa tạo và gửi báo cáo cho tôi."* |
