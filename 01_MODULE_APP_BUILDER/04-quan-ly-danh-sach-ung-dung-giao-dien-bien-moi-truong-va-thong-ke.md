## Mở khu vực Danh sách App và Cài đặt chuyên sâu

Để quản lý danh sách toàn bộ ứng dụng trong Workspace, phân loại theo thẻ (Tag), tùy chỉnh nhận diện thương hiệu (Avatar, Favicon, Theme), cài đặt biến môi trường (`Env`) và theo dõi nhật ký lưu lượng truy cập, bạn sử dụng hai khu vực sau:

1. **Màn hình Danh sách App (`/app-builder`)**: Quản lý tập trung tất cả các ứng dụng, lọc theo thẻ, ghim ứng dụng lên Trang chủ, xuất gói ZIP VFS hoặc quản lý kho thẻ phân loại.
2. **Màn hình Cài đặt App (`/app-builder/:appId/settings`)**: Bấm vào biểu tượng <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt)** ở góc dưới bên phải của thẻ ứng dụng (hoặc trên thanh tiêu đề Trình xem App) để mở 10 danh mục cài đặt chuyên sâu ở cột bên trái:
   - <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Thông tin & Nhận diện)** (`?tab=branding`)
   - <img src="https://api.iconify.design/lucide:bar-chart-2.svg?color=%23ff3333" width="16" alt="" /> **(Thống kê)** (`?tab=analytics`)
   - <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **(Lịch sử phiên bản)** (`?tab=versions`)
   - <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết chia sẻ)** (`?tab=shares`)
   - <img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> **(Đường dẫn trang)** (`?tab=paths`)
   - <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **(Agent Semantic View)** (`?tab=agentView`)
   - <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **(Theme & Giao diện)** (`?tab=theme`)
   - <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)** (`?tab=datasources`)
   - <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **(Môi trường & Biến (Env))** (`?tab=environment`)
   - <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent, Năng lực & Cấu hình)** (`?tab=blueprint`)

---

## Các tính năng

### Tìm, lọc và nhận biết trạng thái trên Danh sách App

Tại màn hình `/app-builder`, bạn có thể tra cứu nhanh các ứng dụng thông qua thanh công cụ và các thông tin hiển thị trực tiếp trên từng thẻ ứng dụng:

| Thành phần giao diện | Cách sử dụng & Ý nghĩa hiển thị |
| :--- | :--- |
| **Ô tìm kiếm ứng dụng** (<img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" />) | Nhập tên ứng dụng hoặc mã định danh (ID) vào ô `Tìm kiếm App theo tên hoặc ID...` để lọc danh sách theo thời gian thực. |
| **Bộ lọc theo Thẻ** (<img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo Thẻ)**) | Bấm vào biểu tượng phễu lọc, nhập tên thẻ vào ô `Tìm thẻ...` và chọn một thẻ màu sắc để lọc các ứng dụng thuộc nhóm đó (bấm **(Xóa lọc)** hoặc **(Tất cả thẻ)** để xem lại toàn bộ). |
| **Sao chép nhanh ID ứng dụng** (<img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép ID)**) | Ngay bên dưới tên ứng dụng trên mỗi thẻ có nút sao chép mã định danh `appId` chỉ với một cú nhấp chuột. |
| **Nhãn trạng thái & Số lượng trang** | • Nhãn **Hệ thống**: Ứng dụng lõi thuộc cấp độ hệ thống.<br>• Nhãn **Template**: Ứng dụng đang được đánh dấu làm mẫu trong Kho Template.<br>• Nhãn <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" /> **Đã ghim**: Ứng dụng đang được ghim lối tắt lên Trang chủ.<br>• Chỉ số góc dưới bên trái (<img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> `{N} Trang`): Cho biết tổng số trang hiện có trong ứng dụng. |

---

### Thao tác nhanh trên từng Thẻ App (Ghim, Export ZIP, Gắn Thẻ, Xem trước, Xóa)

Ở góc dưới bên phải của mỗi thẻ ứng dụng trên màn hình `/app-builder` là hàng nút biểu tượng thao tác trực tiếp:

| Nút biểu tượng trên Thẻ App | Cách thực hiện |
| :--- | :--- |
| <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" /> **(Ghim lên Trang chủ)** / <img src="https://api.iconify.design/lucide:pin-off.svg?color=%23ff3333" width="16" alt="" /> **(Bỏ ghim khỏi Trang chủ)** | Bấm để ghim ứng dụng thường dùng lên khu vực truy cập nhanh ở Trang chủ Workspace hoặc gỡ ghim khi không cần thiết. |
| <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export toàn bộ App ra file ZIP (VFS))** | Bấm để đóng gói và tải toàn bộ cây thư mục mã nguồn VFS (`/app.json`, `/apis.json`, `/pages/...`, `/components/...`) của ứng dụng về máy tính dưới dạng tệp `.zip`. |
| <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Gắn Thẻ (Tags))** | Mở hộp thoại gắn hoặc gỡ các thẻ phân loại màu sắc cho ứng dụng đó. |
| <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **(Mở toàn màn hình (Preview))** | Mở ngay giao diện chạy thực tế của ứng dụng (`/app-builder/:appId/preview`) ở một tab trình duyệt mới. |
| <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt)** | Mở trực tiếp trang **Cài đặt App** (`/app-builder/:appId/settings`). |
| <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa App)** | Mở hộp thoại xác nhận **Xóa Ứng dụng (App)** để xóa vĩnh viễn ứng dụng khỏi Workspace. |
| *Các nút dành riêng cho Quản trị Hệ thống (System Workspace)* | • <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ff3333" width="16" alt="" /> **(Chuyển đổi / Cấu hình App SYSTEM)**: Đưa ứng dụng lên cấp độ App Hệ thống.<br>• <img src="https://api.iconify.design/lucide:layout-grid.svg?color=%23ff3333" width="16" alt="" /> **(Chuyển đổi thành App TEMPLATE)** / **(Hủy trạng thái App Template)**: Đưa ứng dụng vào hoặc gỡ khỏi Kho Mẫu Template. |

---

### Quản lý Thẻ App và Gắn Thẻ phân loại

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Quản lý danh mục Thẻ chung của Workspace** | 1. Trên thanh công cụ của màn hình `/app-builder`, bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Thẻ App)**.<br>2. Chọn phân vùng thẻ: tab <img src="https://api.iconify.design/lucide:briefcase.svg?color=%23ff3333" width="16" alt="" /> **(Của không gian riêng)** hoặc tab <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Của hệ thống)**.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm thẻ mới)**, nhập **Tên Thẻ \***, chọn **Màu sắc hiển thị**, nhập **Mô tả (tùy chọn)** rồi bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Thẻ)**.<br>4. Để sửa hoặc xóa thẻ hiện có, bấm biểu tượng chỉnh sửa hoặc xóa ngay trên dòng thẻ đó. |
| **Gắn hoặc gỡ Thẻ cho một ứng dụng cụ thể** | 1. Bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Gắn Thẻ (Tags))** ở góc dưới bên phải thẻ ứng dụng.<br>2. Trong hộp thoại **Gắn Thẻ cho App**:<br>   • Tại tab **(Kho thẻ)**: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gắn vào App)** bên cạnh các thẻ muốn gắn.<br>   • Tại tab **(Đã gắn ({số lượng}))**: Kiểm tra các thẻ đang gắn và bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ thẻ khỏi App)** nếu muốn bỏ bớt.<br>   • Bạn cũng có thể bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo & Gắn thẻ mới)** trên thanh công cụ của hộp thoại để vừa tạo thẻ mới vừa gắn ngay vào ứng dụng. |

---

### Cập nhật Thông tin & Nhận diện (Tên App, Mô tả, Avatar, Favicon)

Tại trang **Cài đặt App** (`/app-builder/:appId/settings?tab=branding`), mục <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Thông tin & Nhận diện)** gồm 3 khối:

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Cập nhật Tên App và Mô tả App** | Tại khối **Thông tin cơ bản**, chỉnh sửa nội dung ở ô **Tên App \*** và ô **Mô tả App**, sau đó bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu thay đổi)** ở góc phải trên của khối. |
| **Tải lên hoặc gỡ Ảnh đại diện App (Avatar)** | Tại khối **Ảnh đại diện App (Avatar)** (khuyến nghị kích thước `512x512px`):<br>• Nhấp trực tiếp vào ô ảnh đại diện (<img src="https://api.iconify.design/lucide:camera.svg?color=%23ff3333" width="16" alt="" /> **Tải lên** / **Đổi ảnh**) để chọn tệp hình ảnh từ máy tính.<br>• Nếu muốn xóa ảnh hiện tại, bấm nút <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ ảnh)** và xác nhận trong hộp thoại **Gỡ ảnh đại diện App**. |
| **Tải lên hoặc gỡ Biểu tượng Tab trình duyệt (Favicon)** | Tại khối **Biểu tượng Tab trình duyệt (Favicon)** (khuyến nghị từ `16x16` đến `128x128px`):<br>• Nhấp vào ô biểu tượng (<img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **Tải** / **Đổi**) để tải tệp icon hiển thị trên tab trình duyệt khi mở ứng dụng.<br>• Bấm nút <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ)** nếu muốn quay về biểu tượng mặc định. |

---

### Tùy biến Theme & Giao diện (Light Mode / Dark Mode)

Tại mục <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **(Theme & Giao diện)** (`/app-builder/:appId/settings?tab=theme`):

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Xem bảng màu chi tiết và chuyển đổi Light / Dark Mode** | • Quan sát 3 thẻ tổng quan phía trên: **Chế độ Màu Mặc định**, **Font chữ & Kích thước** và **Hình khối & Bo góc**.<br>• Tại khung bên trái **Bảng Màu Chi Tiết (Light Mode / Dark Mode)**, bấm nút <img src="https://api.iconify.design/lucide:sun.svg?color=%23ff3333" width="16" alt="" /> **(Light)** hoặc <img src="https://api.iconify.design/lucide:moon.svg?color=%23ff3333" width="16" alt="" /> **(Dark)** để kiểm tra 10 mã màu hệ thống (`Primary`, `Secondary`, `Background`, `Surface`, `Foreground`, `Muted`, `Border`, `Success`, `Warning`, `Danger`) cùng **Dải màu Biểu đồ (Chart Palette)**.<br>• Đối chiếu trực tiếp kết quả hiển thị tại khung bên phải **Xem trước Giao diện**. |
| **Mở Trình Soạn Thảo Theme Studio** | Bấm vào nút <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **(Mở Trình Soạn Thảo Theme Studio)** ở góc phải trên cùng (hoặc nút <img src="https://api.iconify.design/lucide:palette.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình Theme)** trên thanh tiêu đề Trình xem App) để tùy chỉnh bộ màu sắc, font chữ, độ bo góc và lưu áp dụng cho toàn bộ ứng dụng. |

---

### Quản lý Nguồn dữ liệu & APIs liên kết

Tại mục <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Nguồn dữ liệu & APIs)** (`/app-builder/:appId/settings?tab=datasources`):

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Tra cứu và lọc danh sách API đang gắn trong App** | • Xem 3 thẻ chỉ số tổng quan: **Tổng số API liên kết**, **Số trang App sử dụng API**, **Phương thức HTTP**.<br>• Lọc nhanh theo hàng nút phương thức: **(Tất cả)**, **(GET)**, **(POST)**, **(PUT)**, **(PATCH)**, **(DELETE)** hoặc tìm kiếm tại ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm API, endpoint, trang, schema...)**.<br>• Nhấp vào tên nhóm tại cột **Nguồn dữ liệu (Schema)** để mở trực tiếp trang quản lý Project Schema (`/tools/projects/:projectSchemaId`) nếu cần kiểm tra cấu hình gốc của API. |
| **Gắn thêm hoặc gỡ hàng loạt API khỏi App** | • Để gắn thêm công cụ mới: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gắn thêm API)** trên thanh công cụ.<br>• Để gỡ bớt các API không còn sử dụng: Tích chọn vào ô vuông đầu dòng của các API muốn gỡ trên bảng, sau đó bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ {số lượng} API đã chọn)** trên thanh công cụ. |

---

### Cấu hình Môi trường & Biến (Environments & Variables)

Tại mục <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **(Môi trường & Biến (Env))** (`/app-builder/:appId/settings?tab=environment`), bạn có thể khai báo các biến cấu hình dùng chung hoặc biến ghi đè riêng cho ứng dụng:

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Liên kết Môi trường kích hoạt của Workspace** | Tại khối **1. Lựa chọn Môi trường Kích hoạt (Active Environment)**:<br>• Chọn một môi trường dùng chung tại ô **Môi trường liên kết** (hoặc chọn `-- Chế độ Độc lập (Chỉ dùng biến riêng của MiniApp) --`).<br>• Nếu muốn tạo hoặc sửa bộ biến môi trường cấp Workspace, bấm nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Môi trường)** ở góc phải trên cùng. |
| **Thêm và bảo mật Biến nội bộ của App** | Tại khối **2. Biến nội bộ & Ghi đè cục bộ của App (Local Variables / Overrides)**:<br>1. Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm biến)** để thêm một dòng mới vào bảng.<br>2. Nhập tên biến vào cột **TÊN BIẾN (KEY)** (ví dụ: `API_BASE_URL`, `STORE_ID`) và giá trị vào cột **GIÁ TRỊ (VALUE)**.<br>3. Tại cột **BẢO MẬT**, bấm nút <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> **(Biến bí mật (Mã hóa an toàn trong DB))** để ẩn và mã hóa giá trị nhạy cảm, hoặc để ở trạng thái <img src="https://api.iconify.design/lucide:unlock.svg?color=%23ff3333" width="16" alt="" /> **(Biến công khai (Plain text))**.<br>4. Tại cột **THAO TÁC**, bấm <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Copy cú pháp {{env.KEY}})** để lấy cú pháp tham chiếu biến, hoặc bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa dòng)** để xóa biến.<br>5. Hoàn tất bằng cách bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cấu hình)** ở góc phải trên cùng. |

---

### Theo dõi Thống kê & Lưu lượng truy cập

Tại mục <img src="https://api.iconify.design/lucide:bar-chart-2.svg?color=%23ff3333" width="16" alt="" /> **(Thống kê)** (`/app-builder/:appId/settings?tab=analytics`), bạn có 2 tab con để giám sát hoạt động của ứng dụng:

| Tab con | Các chỉ số & Công cụ tra cứu trên giao diện |
| :--- | :--- |
| **Tab <img src="https://api.iconify.design/lucide:bar-chart-2.svg?color=%23ff3333" width="16" alt="" /> `(Tổng quan)`** | Hiển thị khối **Tổng quan hiệu suất App** với 3 thẻ chỉ số: **Tổng số trang**, **Trang đã xuất bản** và **Trạng thái Tên miền**. |
| **Tab <img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> `(Lưu lượng truy cập)`** | • **4 thẻ KPI thời gian thực**:<br>  1. <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **Tổng lượt truy cập** (`Tất cả kênh & domain`)<br>  2. <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **Truy cập thành công** (`Trang hiện tại`)<br>  3. <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> **Bị từ chối / Chặn** (`IP blacklist / sai mật khẩu`)<br>  4. <img src="https://api.iconify.design/lucide:clock.svg?color=%23ff3333" width="16" alt="" /> **Tốc độ trung bình** (`Thời gian phản hồi API`)<br>• **Thanh công cụ lọc nhật ký**: Sử dụng ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm IP, User-Agent, Mã lỗi...)** và nút <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc sự kiện & kết quả)** để lọc theo **Loại sự kiện** (`Tất cả sự kiện`, `Xem trang`, `Thực thi API`, `Sai mật khẩu`, `IP ngoài Whitelist`, `Chặn IP`) và **Kết quả** (`Tất cả kết quả`, `Thành công`, `Thất bại`, `Bị từ chối`, `Đã chặn`).<br>• **Bảng nhật ký truy cập**: Hiển thị chi tiết 7 cột gồm `Thời gian`, `Sự kiện`, `Kết quả`, `Địa chỉ IP`, `Thiết bị` (`Mobile` / `Desktop`), `Phản hồi` (`ms`) và `Mã lỗi`. |

---

### Phân biệt phạm vi ảnh hưởng khi Xóa và Gỡ tài nguyên

Trước khi thực hiện các thao tác xóa hoặc gỡ trong **App Builder**, hãy lưu ý bảng phạm vi ảnh hưởng dưới đây để tránh mất dữ liệu ngoài ý muốn:

| Thao tác trên giao diện | Vị trí thực hiện | Phạm vi dữ liệu bị ảnh hưởng |
| :--- | :--- | :--- |
| <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ {N} API đã chọn)** | Cài đặt App $\rightarrow$ **Nguồn dữ liệu & APIs** | Chỉ ngắt quyền gọi API đó khỏi ứng dụng hiện tại. **Không** xóa Custom Tool gốc hay Bảng dữ liệu động trong hệ thống. |
| <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ tên miền)** | Cài đặt App $\rightarrow$ **Đường dẫn trang** (hoặc **Quản lý tên miền Workspace**) | Chỉ ngắt kết nối tên miền tùy chỉnh khỏi ứng dụng. Ứng dụng vẫn hoạt động bình thường trên đường dẫn nội bộ và các liên kết chia sẻ. |
| <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa bản phát hành này)** | Cài đặt App $\rightarrow$ **Lịch sử phiên bản** | Chỉ xóa phiên bản lưu trữ đã chọn khỏi lịch sử. Không ảnh hưởng đến phiên bản **Đang hoạt động (Active)** hay mã nguồn VFS hiện tại. |
| <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa trang)** | Trình xem App $\rightarrow$ **Quản Lý Trang** $\rightarrow$ Menu **Thao tác** | Xóa tệp trang tương ứng trong thư mục `/pages/` của ứng dụng. Các trang khác trong ứng dụng không bị ảnh hưởng. |
| <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa App)** | Góc dưới bên phải Thẻ App tại màn hình `/app-builder` | **Xóa vĩnh viễn** toàn bộ ứng dụng, bao gồm cây mã nguồn VFS, lịch sử phiên bản và các liên kết chia sẻ của ứng dụng đó (hãy bấm <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export toàn bộ App ra file ZIP (VFS))** để sao lưu trước khi xóa). |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Toàn bộ các tính năng quản lý danh sách ứng dụng, cập nhật thông tin, quản lý thẻ phân loại (Tags), xuất gói ứng dụng và kiểm thử tự động giao diện đều có thể thực hiện thông qua trợ lý ảo AI Agent.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - App Builder` (ID: `58f36f44-2e1c-4aaf-8ca7-d73008169e95`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - App Builder` (ID: `d16e4656-c070-43b6-b234-abcff883fd61`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản lý ứng dụng trong Workspace.

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Tra cứu danh sách ứng dụng và xem chi tiết cấu hình App

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Tìm kiếm trên màn hình `/app-builder` và mở chi tiết ứng dụng `/app-builder/:appId/settings` |
| **Công cụ Agent sử dụng** | `app_getUserApps`, `app_getAppDetail` |
| **Thông tin cần cung cấp** | Từ khóa tên ứng dụng (tùy chọn) hoặc mã định danh `appId` |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ app_getUserApps để liệt kê toàn bộ các ứng dụng MiniApp hiện có trong Workspace của tôi, sau đó dùng app_getAppDetail để xem thông tin chi tiết của ứng dụng "[Tên App hoặc appId]".
```

#### 2. Cập nhật tên, mô tả và cấu hình nhận diện ứng dụng

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Sửa **Tên App**, **Mô tả App** và cấu hình tại mục <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Thông tin & Nhận diện)** |
| **Công cụ Agent sử dụng** | `app_updateApp` |
| **Thông tin cần cung cấp** | `appId`, tên ứng dụng mới, mô tả mới hoặc các thuộc tính cấu hình cần cập nhật |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ app_updateApp để cập nhật ứng dụng có ID "[Điền appId]" với tên mới là "Hệ Thống Quản Trị Bán Lẻ Đa Kênh" và mô tả mới là "Dashboard điều hành doanh thu, đơn hàng, tồn kho và phân khúc khách hàng RFM".
```

#### 3. Quản lý danh mục Thẻ (Tags) của ứng dụng

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Thẻ App)** trên thanh công cụ để tạo, sửa, xóa thẻ phân loại |
| **Công cụ Agent sử dụng** | `appTag_findAll`, `appTag_create`, `appTag_update`, `appTag_remove` |
| **Thông tin cần cung cấp** | Tên thẻ, mã màu hiển thị (HEX), mô tả thẻ hoặc ID thẻ cần cập nhật/xóa |

**Câu lệnh mẫu (Prompt):**

```text
Hãy kiểm tra danh sách thẻ App hiện có bằng appTag_findAll. Nếu chưa có thẻ "Vận hành Bán lẻ", hãy dùng appTag_create tạo thẻ mới với tên "Vận hành Bán lẻ", màu "#ff3333" và mô tả "Nhóm ứng dụng phục vụ bán hàng và quản lý kho".
```

#### 4. Xuất đóng gói ứng dụng và xóa ứng dụng không còn sử dụng

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export toàn bộ App ra file ZIP (VFS))** và nút <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa App)** trên thẻ ứng dụng |
| **Công cụ Agent sử dụng** | `appPackage_exportAppPackage`, `app_deleteApp` |
| **Thông tin cần cung cấp** | Mã định danh `appId` của ứng dụng cần xuất gói hoặc cần xóa |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ appPackage_exportAppPackage để xuất gói sao lưu cho ứng dụng có ID "[Điền appId]", sau đó xóa ứng dụng thử nghiệm có ID "[Điền appId cần xóa]" bằng công cụ app_deleteApp.
```

#### 5. Kiểm thử tự động toàn diện giao diện, mạng và tương tác trên trang (Page Validation Suite)

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Mở từng trang để kiểm tra hiển thị, bấm các nút tương tác, kiểm tra lỗi runtime và chụp ảnh màn hình |
| **Công cụ Agent sử dụng** | `pageValidation_validateJsx`, `pageValidation_diagnose`, `pageValidation_getConsoleLogs`, `pageValidation_traceNetwork`, `pageValidation_captureScreenshot`, `pageValidation_runInteractionTest`, `pageValidation_fuzzTest` |
| **Thông tin cần cung cấp** | Mã định danh `appId` và đường dẫn trang `routePath` cần kiểm thử |

**Câu lệnh mẫu (Prompt):**

```text
Hãy thực hiện kiểm thử toàn diện cho ứng dụng có ID "[Điền appId]" trên tất cả các trang:
1. Dùng pageValidation_validateJsx và pageValidation_diagnose để kiểm tra lỗi cú pháp và lỗi runtime.
2. Dùng pageValidation_traceNetwork và pageValidation_getConsoleLogs để kiểm tra các lệnh gọi API và log trình duyệt.
3. Dùng pageValidation_runInteractionTest hoặc pageValidation_fuzzTest để kiểm thử các nút bấm, bộ lọc và biểu mẫu trên trang.
4. Dùng pageValidation_captureScreenshot chụp ảnh giao diện và tổng hợp báo cáo kết quả cho tôi.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Làm mới (<img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" />) màn hình **Danh sách App** (`/app-builder`) hoặc trang **Cài đặt App** (`/app-builder/:appId/settings`) để xác nhận tên ứng dụng, danh sách thẻ và trạng thái các trang đã được cập nhật. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent xác nhận** | Gửi câu lệnh: *"Hãy gọi `app_getAppDetail` và `appTag_findAll` để hiển thị lại thông tin mới nhất của ứng dụng và danh sách thẻ hiện có."* |
