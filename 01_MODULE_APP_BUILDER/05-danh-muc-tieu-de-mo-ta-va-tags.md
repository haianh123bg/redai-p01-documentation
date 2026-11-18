## App Builder - Quy trình khởi tạo ứng dụng và quản lý trang trên App Studio

**Tên file:** `01-quy-trinh-khoi-tao-ung-dung-va-quan-ly-trang-tren-app-studio.md`

**Tiêu đề:** App Builder - Quy trình khởi tạo ứng dụng và quản lý trang trên App Studio

**Mô tả:** Hướng dẫn chi tiết 3 phương án khởi tạo ứng dụng trên App Builder (tạo App mới từ đầu chỉ với `Tên App *` và `Mô tả ngắn`, sử dụng mẫu từ `Mẫu Template App Builder` để tạo App mới hoặc `Tải lẻ các trang vào 1 App`, và `Import App từ file ZIP` tối đa 50MB); kết nối `Nguồn dữ liệu & APIs` (`Custom Tools` / `Dynamic Tables`) vào ứng dụng; quản lý danh sách trang qua hộp thoại `Quản Lý Trang` (đổi tên/mô tả trang, nhân bản sang App khác, xóa trang), ghép trang từ `Thư viện App & Trang Mẫu`; kiểm thử trực tiếp trên màn hình xem trước độc lập kèm `Nút bong bóng nổi RedAI` và khắc phục lỗi bằng nút `Sửa lỗi với AI`, kết hợp hướng dẫn điều khiển tự động qua trợ lý ảo AI Agent với kỹ năng `RedAI - Module - App Builder`.

**Agent nên truy xuất khi:** Người dùng muốn tạo ứng dụng MiniApp/Dashboard mới, tải hoặc ghép trang từ Kho Template/Thư viện App, import ứng dụng từ tệp `.zip`, gắn nguồn dữ liệu API vào ứng dụng, quản lý trang trong App Studio hoặc nhờ AI Agent lập trình giao diện ứng dụng trên hệ thống tệp ảo VFS.

**Không dùng khi:** Người dùng chỉ hỏi cách viết kịch bản Agent Semantic View, phân quyền vai trò Agent, biên dịch bản phát hành (Release), tạo liên kết chia sẻ hoặc cấu hình tên miền tùy chỉnh.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> Tạo App → khởi tạo → Ứng dụng MiniApp mới`; `<img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> Tải mẫu (UseAppTemplateModal) → nhân bản nguyên App hoặc ghép trang lẻ vào → MiniApp đích`; `<img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> Import App từ file ZIP → giải nén cây VFS thành → Ứng dụng mới`; `<img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> Nguồn dữ liệu & APIs → cấp quyền gọi Custom Tools trong → /apis.json`; `Kỹ năng RedAI - Module - App Builder (58f36f44-2e1c-4aaf-8ca7-d73008169e95) → thực thi → Bộ công cụ VFS & App Builder (d16e4656-c070-43b6-b234-abcff883fd61)`.

**Tags (10):** `app-builder/tao-app`, `app-builder/mau-template`, `app-builder/import-zip`, `app-builder/app-studio`, `app-builder/quan-ly-trang`, `app-builder/thu-vien-app`, `app-builder/nguon-du-lieu-api`, `app-builder/xem-truoc-app`, `app-builder/sua-loi-voi-ai`, `app-builder/ai-agent-vfs`

---

## App Builder - Quy trình thiết lập Agent Semantic View và liên kết AI Agent

**Tên file:** `02-quy-trinh-thiet-lap-agent-semantic-view-va-lien-ket-ai-agent.md`

**Tiêu đề:** App Builder - Quy trình thiết lập Agent Semantic View và liên kết AI Agent

**Mô tả:** Hướng dẫn thiết lập `Agent Semantic View` cho từng trang bằng nút `Ask AI Sinh Agent View (VFS Playground)` hoặc cấu hình thủ công (`Tool Name`, `Cache TTL`, `Mô tả Prompt`, `Transform Script (JS)`, `Input Schema`, `Test Params`) để xuất báo cáo `Runtime Markdown View` cho AI Agent; tạo `Hồ sơ cấu hình` giới hạn `Phân quyền tính năng (Feature Scope & Capabilities)` và `JSON Settings`; thiết lập `Phân quyền Vai trò` (`Scope-Role` ↔ `Kỹ năng AI`); và gắn ứng dụng vào `AI Agent liên kết` theo chế độ `Tự động thích ứng` hoặc vai trò cố định, kèm hướng dẫn điều khiển qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn cấu hình để AI Agent đọc được dữ liệu trên trang ứng dụng dưới dạng Markdown, muốn tạo Hồ sơ cấu hình bật/tắt tính năng (`capabilities`), gán quyền vai trò (`Scope-Role`) với Skill hoặc liên kết ứng dụng vào một AI Agent.

**Không dùng khi:** Người dùng chỉ muốn tạo ứng dụng mới, ghép trang mẫu, biên dịch bản phát hành hoặc cấu hình DNS cho tên miền tùy chỉnh.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> Agent Semantic View + Transform Script (JS) → kết xuất → Runtime Markdown View cho AI Agent`; `<img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> Ask AI Sinh Agent View → tự động sinh → Script & Schema`; `Hồ sơ cấu hình → quy định → Feature Scope & Capabilities + JSON Settings`; `Phân quyền Vai trò → ánh xạ → Scope-Role ↔ Kỹ năng AI (Skill)`; `AI Agent liên kết → gắn ứng dụng + Hồ sơ cấu hình + Vai trò đảm nhiệm vào → AI Agent`.

**Tags (10):** `app-builder/agent-semantic-view`, `app-builder/transform-script`, `app-builder/input-schema`, `app-builder/runtime-markdown-view`, `app-builder/ho-so-cau-hinh`, `app-builder/capabilities`, `app-builder/phan-quyen-vai-tro`, `app-builder/scope-role`, `app-builder/ai-agent-lien-ket`, `app-builder/page-data-reader`

---

## App Builder - Quy trình biên dịch phát hành, chia sẻ và gắn tên miền tùy chỉnh

**Tên file:** `03-quy-trinh-bien-dich-phat-hanh-chia-se-va-gan-ten-mien-tuy-chinh.md`

**Tiêu đề:** App Builder - Quy trình biên dịch phát hành, chia sẻ và gắn tên miền tùy chỉnh

**Mô tả:** Hướng dẫn đóng gói bản phát hành chính thức (`Biên dịch SWC & Phát hành`) trong mục `Lịch sử phiên bản`, đối chiếu thay đổi giữa hai phiên bản (`So sánh khác biệt với bản khác`) và khôi phục ứng dụng (`Rollback`); tạo `Liên kết chia sẻ` kèm `Mã QR Code truy cập nhanh`, mật khẩu bảo vệ, ngày hết hạn, danh sách IP Whitelist/Blacklist và 5 quyền hạn người xem; chỉnh sửa `Đường dẫn các trang (Routing)`, kết nối `Tên miền tùy chỉnh (Custom Domain)` qua 4 bước cấu hình DNS (`CNAME` trỏ về `dashboard-app.redai.vn` và `TXT`) và thiết lập `Quyền riêng tư & Bảo mật` toàn ứng dụng, kèm hướng dẫn thao tác qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn biên dịch và phát hành phiên bản mới (Compile Release), xem lịch sử phiên bản, so sánh Diff, Rollback về bản cũ, tạo link chia sẻ có mật khẩu/mã QR hoặc gắn tên miền riêng (Custom Domain) cho ứng dụng.

**Không dùng khi:** Người dùng chỉ muốn tạo trang mới trong App Studio, gắn thêm nguồn dữ liệu API hoặc cấu hình Agent Semantic View.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> Biên dịch SWC & Phát hành → tạo phiên bản → Đang hoạt động (Active)`; `<img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> Rollback → khôi phục toàn bộ App về → Bản phát hành đã chọn`; `<img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> Liên kết chia sẻ → cấp đường dẫn công khai kèm → Mã QR Code + Mật khẩu + Ngày hết hạn + IP Whitelist/Blacklist`; `<img src="https://api.iconify.design/lucide:globe-2.svg?color=%23ff3333" width="16" alt="" /> Tên miền tùy chỉnh + Bản ghi CNAME & TXT → kích hoạt → Định tuyến HTTPS & SSL`.

**Tags (10):** `app-builder/lich-su-phien-ban`, `app-builder/bien-dich-swc`, `app-builder/rollback-phien-ban`, `app-builder/so-sanh-phien-ban`, `app-builder/lien-ket-chia-se`, `app-builder/ma-qr-code`, `app-builder/duong-dan-trang`, `app-builder/ten-mien-tuy-chinh`, `app-builder/xac-thuc-dns`, `app-builder/bao-mat-app`

---

## App Builder - Quản lý danh sách ứng dụng, giao diện, biến môi trường và thống kê

**Tên file:** `04-quan-ly-danh-sach-ung-dung-giao-dien-bien-moi-truong-va-thong-ke.md`

**Tiêu đề:** App Builder - Quản lý danh sách ứng dụng, giao diện, biến môi trường và thống kê

**Mô tả:** Hướng dẫn tìm kiếm, lọc ứng dụng theo thẻ và sử dụng hàng nút thao tác nhanh trên từng thẻ App (`Ghim lên Trang chủ`, `Export toàn bộ App ra file ZIP (VFS)`, `Gắn Thẻ (Tags)`, `Mở toàn màn hình (Preview)`, `Cài đặt`, `Xóa App`); quản lý kho thẻ phân loại (`Quản lý Thẻ App`); cập nhật `Thông tin & Nhận diện` (`Tên App`, `Mô tả App`, `Avatar` 512x512px, `Favicon` 16x16–128x128px); tùy biến `Theme & Giao diện` (`Light Mode / Dark Mode` & `Theme Studio`); quản lý `Nguồn dữ liệu & APIs`; thiết lập `Môi trường & Biến (Env)` (`Active Environment` & `Biến nội bộ {{env.KEY}}`); theo dõi `Thống kê & Lưu lượng truy cập` và phân biệt phạm vi ảnh hưởng khi xóa/gỡ tài nguyên, kèm hướng dẫn điều khiển qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng cần tìm kiếm, lọc theo thẻ, ghim, xuất gói `.zip` hoặc xóa ứng dụng; đổi tên, Avatar, Favicon, bảng màu Theme; cài đặt biến môi trường `{{env.KEY}}`; xem thống kê lưu lượng truy cập hoặc chạy bộ công cụ kiểm thử tự động giao diện (`pageValidation`).

**Không dùng khi:** Người dùng muốn xem quy trình từng bước khởi tạo ứng dụng mới từ mẫu Template, thiết lập Agent Semantic View hoặc cấu hình 4 bước DNS cho tên miền tùy chỉnh.

**Thực thể và quan hệ:** `Thẻ App + <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" /> Ghim lên Trang chủ → hiển thị lối tắt tại → Trang chủ Workspace`; `<img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> Quản lý Thẻ App → phân loại → Các ứng dụng trong Workspace`; `<img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> Thông tin & Nhận diện → lưu trữ → Tên App, Mô tả, Avatar & Favicon`; `<img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> Môi trường & Biến (Env) → kết hợp → Môi trường liên kết Workspace + Biến nội bộ App`; `<img src="https://api.iconify.design/lucide:bar-chart-2.svg?color=%23ff3333" width="16" alt="" /> Thống kê → giám sát → Hiệu suất App & Nhật ký lưu lượng truy cập`.

**Tags (10):** `app-builder/danh-sach-app`, `app-builder/quan-ly-the-app`, `app-builder/ghim-trang-chu`, `app-builder/export-zip-vfs`, `app-builder/avatar-favicon`, `app-builder/theme-studio`, `app-builder/moi-truong-bien-env`, `app-builder/thong-ke-luu-luong`, `app-builder/kiem-thu-giao-dien`, `app-builder/xoa-app`

---

## Định tuyến nhanh

| Ý định truy vấn | Tài liệu ưu tiên |
| :--- | :--- |
| Tạo App mới, tải mẫu từ Kho Template, ghép trang lẻ, Import file ZIP, gắn Nguồn dữ liệu & APIs và quản lý trang trên App Studio | **01-quy-trinh-khoi-tao-ung-dung-va-quan-ly-trang-tren-app-studio.md** |
| Thiết lập Agent Semantic View (đọc báo cáo Markdown), tạo Hồ sơ cấu hình (Capabilities), Phân quyền Vai trò và liên kết AI Agent | **02-quy-trinh-thiet-lap-agent-semantic-view-va-lien-ket-ai-agent.md** |
| Biên dịch phát hành phiên bản (SWC Build), so sánh Diff, Rollback, tạo Liên kết chia sẻ, Mã QR Code và gắn Tên miền tùy chỉnh | **03-quy-trinh-bien-dich-phat-hanh-chia-se-va-gan-ten-mien-tuy-chinh.md** |
| Tìm kiếm, lọc theo thẻ, ghim App, xuất ZIP, đổi Avatar/Favicon, chỉnh Theme, cấu hình Biến môi trường (Env), xem Thống kê lưu lượng và Kiểm thử tự động | **04-quan-ly-danh-sach-ung-dung-giao-dien-bien-moi-truong-va-thong-ke.md** |
