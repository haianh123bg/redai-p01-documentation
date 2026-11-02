## Tổng quan Bộ Tài liệu Hướng dẫn Sử dụng & Điều khiển qua AI Agent trên RedAI

Bộ tài liệu này được biên soạn theo đúng chuẩn mực hợp nhất của hệ thống **RedAI** (tương tự chuẩn `integration-hub`):

1. **Bám sát 100% giao diện thực tế (Frontend-Driven UI Guide)**:
   - Chỉ hướng dẫn các màn hình, thanh điều hướng, tab, hộp thoại (Modal), ngăn kéo (Drawer), nút bấm và các trường nhập liệu **thực sự hiển thị trên giao diện người dùng (Frontend)**.
   - Loại bỏ hoàn toàn các trường dữ liệu tự sinh ở tầng máy chủ (Backend DTO) không xuất hiện trên màn hình.
   - Toàn bộ nút bấm và biểu tượng thao tác đều được nhúng trực tiếp icon SVG Lucide màu đỏ chuẩn `#ff3333` theo cú pháp `<img src="https://api.iconify.design/lucide:<icon>.svg?color=%23ff3333" width="16" alt="" /> **(Tên nút)**`.
2. **Hợp nhất Hướng dẫn Giao diện và Hướng dẫn Thao tác qua Trợ lý ảo AI Agent trong cùng một tài liệu**:
   - Không tách rời thư mục hướng dẫn sử dụng và tài liệu kỹ thuật.
   - Cuối mỗi bài hướng dẫn đều tích hợp mục **`## Hướng dẫn thao tác qua trợ lý ảo AI Agent`**, chỉ rõ **Kỹ năng (Skill) chính thức trên RedAI**, **ID Kỹ năng**, **Bộ công cụ (Tool Suite) đi kèm**, bảng ánh xạ từ thao tác trên giao diện sang tên công cụ của AI Agent, **Câu lệnh mẫu (Prompt mẫu)** và bảng kiểm tra kết quả hai chiều.

---

## Danh sách Kỹ năng (Skills) và Bộ công cụ (Tools) theo từng Phân hệ

| Phân hệ (Module) | Kỹ năng (Skill) trên RedAI | Mã định danh Kỹ năng (`skillId`) | Bộ công cụ (`Project Schema`) đi kèm | Mã định danh Bộ công cụ (`projectSchemaId`) |
| :--- | :--- | :--- | :--- | :--- |
| **01. Module App Builder** (`01-MODULE-APP-BUILDER`) | `RedAI - Module - App Builder` | `58f36f44-2e1c-4aaf-8ca7-d73008169e95` | `RedAI - Module - App Builder` | `d16e4656-c070-43b6-b234-abcff883fd61` |
| **02. Module Skills** (`02-MODULE-SKILLS`) | `RedAI - Module - Skill` | `57cc282f-a2d2-4dfc-9981-153fe58f7cf5` | `RedAI - Module - Skill` | `7534d86e-8a3c-4e74-aaec-5f0da403ec41` |
| **03. Module App Business** (`03-MODULE-APP-BUSINESS`) — *Thiết lập & Quản trị* | `RedAI - Business Setup` | `75e8c472-fbe2-4a26-8e4e-5cdaabdc590d` | `RedAI - Business Setup` | `b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63` |
| **03. Module App Business** (`03-MODULE-APP-BUSINESS`) — *Tư vấn & Lên đơn* | `RedAI - Business Operations` | `0a1c2aec-78f6-419c-8e70-d7ce019ba210` | `RedAI - Business Operations` | `b736f624-fb7e-425d-9e3b-6e216887604d` |
| **04. Module Database** (`04-MODULE-DATABASE`) | `RedAI - Module - Database` | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` | `RedAI - Module - Database` | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **05. Module Multichannel Chat** (`05-MODULE-MULTICHANNEL-CHAT`) | `RedAI - OmniAI Chat` | `d274fc72-b5d7-4aff-bf25-7eb20fba0eea` | `RedAI - Module - OmniAI Chat` | `71230a76-f1ab-4bdf-8e56-9fe1d8b6fd1a` |
| **06. Module Profile & User Account** (`06-MODULE-PROFILE`) | `RedAI - User Profile & Account` | `c8319e04-7a1b-4f92-91ef-8d5421ac0721` | `RedAI - Module - User & Account` | `387d45d1-3e2a-4ec5-9572-218d70618d5c` |
| **07. Module Workspace & Workbase Management** (`07-MODULE-WORKSPACE`) | `RedAI - Workbase & Workspace Management` | `4fa87112-9b2c-46ea-8822-1d187e59b201` | `RedAI - Module - Workbase` | `71c42938-16e5-4d29-9e87-251f9a84b102` |

---

## Cấu trúc danh mục tệp tài liệu theo từng Phân hệ

### Phân hệ 01 — Module App Builder (`01-MODULE-APP-BUILDER/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-khoi-tao-ung-dung-va-quan-ly-trang-tren-app-studio.md` | Loại A (Quy trình) | Khởi tạo App (tạo mới, tải mẫu Template, ghép trang lẻ, Import ZIP), kết nối Nguồn dữ liệu & APIs, quản lý trang trên App Studio và điều khiển qua AI Agent |
| **02** | `02-quy-trinh-thiet-lap-agent-semantic-view-va-lien-ket-ai-agent.md` | Loại A (Quy trình) | Cấu hình Agent Semantic View (`Transform Script`, `Input Schema`, `Test Params`), tạo Hồ sơ cấu hình (`Capabilities`), Phân quyền Vai trò và liên kết AI Agent |
| **03** | `03-quy-trinh-bien-dich-phat-hanh-chia-se-va-gan-ten-mien-tuy-chinh.md` | Loại A (Quy trình) | Biên dịch bản phát hành (`Biên dịch SWC & Phát hành`), so sánh Diff, Rollback, tạo Liên kết chia sẻ kèm Mã QR Code và gắn Tên miền tùy chỉnh (`Custom Domain`) |
| **04** | `04-quan-ly-danh-sach-ung-dung-giao-dien-bien-moi-truong-va-thong-ke.md` | Loại B (Tính năng) | Quản lý Danh sách App, Thẻ (Tags), Ghim App, Export ZIP, Thông tin & Nhận diện (Avatar/Favicon), Theme Studio, Biến môi trường (`Env`) và Thống kê lưu lượng |
| **05** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module App Builder |

---

### Phân hệ 02 — Module Skills (`02-MODULE-SKILLS/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-tao-ky-nang-soan-chi-thi-dinh-tuyen-va-quan-ly-tai-lieu-docs.md` | Loại A (Quy trình) | Khởi tạo Kỹ năng (`Tạo thường` 5 trường / `Tạo bằng AI`), soạn `Nội dung Skill`, quản lý tài liệu `Docs` (`Create new doc`, `Import markdown file`, `Thêm docs có sẵn`) và Biến môi trường |
| **02** | `02-quy-trinh-lien-ket-tools-mcps-workflows-va-phan-quyen-tinh-nang.md` | Loại A (Quy trình) | Liên kết `Tools`, `MCPs`, `Workflows` vào Kỹ năng, cài đặt Phân quyền tính năng (`Capability Tag`) phục vụ lọc công cụ tự động và mở nhanh Project Tools |
| **03** | `03-quy-trinh-sao-luu-snapshot-dong-goi-package-va-dong-bo-do-thi-tri-thuc.md` | Loại A (Quy trình) | Chụp bản sao lưu `Snapshot`, khôi phục `Import vào skill`, xuất/nhập gói `.json`/`.zip` và đồng bộ Đồ thị Tri thức (`Skill Graph RAG v2.0`) |
| **04** | `04-quan-ly-thu-vien-ky-nang-nhan-ban-phan-loai-the-va-gan-ky-nang-mac-dinh.md` | Loại B (Tính năng) | Quản lý Thư viện Kỹ năng, Nhân bản (`Duplicate Skill`), Gắn Thẻ (Tags), gỡ hàng loạt tài nguyên và cấu hình Kỹ năng Mặc định cho Trợ lý Hệ thống |
| **05** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module Skills |

---

### Phân hệ 03 — Module App Business (`03-MODULE-APP-BUSINESS/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-thiet-lap-cau-hinh-ban-hang-5-buoc-va-quan-ly-kho-hang.md` | Loại A (Quy trình) | Quản lý Kho hàng & Chi nhánh (địa chỉ hành chính 2 cấp Tỉnh/Thành phố $\rightarrow$ Phường/Xã) và thiết lập Cấu hình Bán hàng 5 bước (`Cơ bản`, `Ánh xạ cột`, `Thanh toán & Kho bãi`, `Cọc COD`, `Thông báo`) |
| **02** | `02-quy-trinh-tao-va-xu-ly-vong-doi-don-hang-ban-le.md` | Loại A (Quy trình) | Tạo đơn hàng bán lẻ mới (điền nhanh từ `Khách quen CRM`), xuất mã `VietQR`, xem chi tiết đơn, `Duyệt chốt đơn`, `Cập nhật mã vận đơn` và `Hủy đơn hàng` |
| **03** | `03-quan-ly-tong-quan-doanh-nghiep-va-phan-tich-khach-hang-rfm.md` | Loại B (Tính năng) | Khai thác bảng điều khiển Tổng quan (`/home`), bộ lọc Cấu hình & Thời gian, 5 thẻ KPI chiến lược, 4 biểu đồ kinh doanh và phân tích khách hàng theo mô hình RFM |
| **04** | `04-quan-ly-san-pham-ton-kho-va-ho-so-khach-hang-crm.md` | Loại B (Tính năng) | Theo dõi KPI & bảng Danh mục Mặt hàng (`/products`), sao chép SKU/ID, quản lý danh sách Khách hàng (`/customers`), xem Hồ sơ Khách hàng 360° và lịch sử đơn hàng |
| **05** | `05-quy-trinh-tao-va-quan-ly-chuong-trinh-khuyen-mai-voucher.md` | Loại A (Quy trình) | Tạo chương trình khuyến mãi & mã giảm giá Voucher qua 5 khối cấu hình (3 loại giảm giá: `%`, `VNĐ`, `Free Shipping`), chống spam theo SĐT/Phiên chat và bật/tắt nhanh |
| **06** | `06-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module App Business |

---

### Phân hệ 04 — Module Database (`04-MODULE-DATABASE/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Loại A (Quy trình) | Khởi tạo bảng dữ liệu (4 phương án: bảng trống, Hỏi AI Blueprint, nhân bản bảng, import CSV/Excel/JSON), quản lý danh mục phân loại, vận hành thùng rác 10 ngày và điều khiển qua AI Agent |
| **02** | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Loại A (Quy trình) | Cấu hình chuyên sâu các kiểu dữ liệu (Text, Number, Currency, Date, Datetime, Select, Multi-select, Boolean, Relation liên kết bảng 1-1/1-N/N-N, Lookup, Rollup, Formula, Phone, URL, Attachment), ràng buộc Not Null, Unique, Validation rules và điều khiển qua AI Agent |
| **03** | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | Loại A (Quy trình) | Thiết lập và chuyển đổi 5 dạng xem cốt lõi (Grid View, Kanban View, Form View, Calendar View, Gallery View), bộ công cụ lọc Filter, sắp xếp Sort, gom nhóm Group by, chiều cao dòng, chi tiết dòng và điều khiển qua AI Agent |
| **04** | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | Loại B (Tính năng) | Quản lý sơ đồ quan hệ tương tác (Relations ERD canvas), ma trận phân quyền bảng 9 phạm vi, phân quyền cột, bảo mật cấp bản ghi theo vai trò/người dùng, tự động hóa Webhooks & Scheduled Hooks sang Workflow và điều khiển qua AI Agent |
| **05** | `05-trung-tam-tien-ich-in-tem-nhan-qr-va-bao-cao-tai-lieu.md` | Loại B (Tính năng) | Khai thác trọn bộ 10 công cụ Trung Tâm Tiện Ích: in tem nhãn & tạo mã QR hàng loạt, thiết kế mẫu báo cáo PDF kéo thả biến bảng dữ liệu, quy trình ánh xạ nhập dữ liệu (Import mapping 3 cột), làm sạch định dạng, quét xử lý trùng lặp và điều khiển qua AI Agent |
| **06** | `06-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho toàn bộ Phân hệ 04 — Module Database |

---

### Phân hệ 05 — Module Multichannel Chat (`05-MODULE-MULTICHANNEL-CHAT/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-tiep-nhan-dieu-phoi-va-quan-ly-inbox-da-kenh.md` | Loại A (Quy trình) | Tiếp nhận và điều phối inbox đa kênh (chọn tài khoản Zalo OA/Zalo Cá nhân/Facebook/Gmail, lọc Chưa đọc/Nhóm, tìm kiếm nâng cao, đồng bộ tin nhắn lịch sử và tạo cuộc trò chuyện mới) |
| **02** | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` | Loại A (Quy trình) | Soạn tin nhắn đa phương tiện (văn bản rich text, giọng nói voice, tệp đính kèm, sticker, thư viện đa kênh), tương tác tin nhắn (thả biểu cảm, trích dẫn, thu hồi) và kiểm soát chính sách gửi tin 24h/7 ngày an toàn |
| **03** | `03-quy-trinh-tom-tat-ai-phan-tich-dong-thoi-gian-va-nhoi-ky-uc-do-thi.md` | Loại A (Quy trình) | Khai thác trí tuệ nhân tạo chuyên sâu: Tóm tắt hội thoại AI, lịch sử tóm tắt, nhồi ký ức vào Đồ thị Tri thức (Graph RAG Memory), phân tích Dòng thời gian, cảnh báo khoảng lặng và gợi ý chăm sóc lại |
| **04** | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Loại B (Tính năng) | Quản trị thẻ nhãn (Tags), phân công CSKH & AI Chat, chỉnh sửa trường dữ liệu, Trung tâm Tiện ích 2 cấp độ, ghim tối đa 2 tiện ích, trọn bộ 5 tiện ích: Templates, Campaigns, Cào Group Zalo (15 trường ánh xạ vào Database), Đồng bộ Nhãn Zalo và Đồng bộ Tên hiển thị Zalo |
| **05** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module Multichannel Chat |

---

### Phân hệ 06 — Module Profile & User Account (`06-MODULE-PROFILE/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | Loại A (Quy trình) | Quản lý ảnh bìa (Cover Image tải lên S3), đổi và nén ảnh đại diện Avatar WebP (tối đa 2MB), điền thông tin cá nhân (Họ tên, Giới tính, Ngày sinh, Địa chỉ) và xác thực Email / Số điện thoại qua mã OTP 6 số |
| **02** | `02-thiet-lap-bao-mat-xac-thuc-hai-buoc-va-quan-ly-phien-dang-nhap.md` | Loại A (Quy trình) | Đổi mật khẩu tài khoản (kiểm tra độ mạnh, icon ẩn/hiện mắt), kích hoạt xác thực 2 bước 2FA (SMS, Email, Google Authenticator với mã QR và OTP 6 số) và quản lý phiên đăng nhập thiết bị (`/settings/security`), thu hồi phiên từ xa |
| **03** | `03-quan-ly-thong-tin-doanh-nghiep-tai-khoan-ngan-hang-va-hop-dong.md` | Loại B (Tính năng) | Nâng cấp tài khoản Doanh nghiệp (tên công ty, MST, người đại diện), cấu hình tài khoản ngân hàng thụ hưởng (bộ chọn NAPAS/VietQR tiếng Việt không dấu, tên in hoa) và quản lý 2 hợp đồng số (Hợp đồng nguyên tắc & Hợp đồng Affiliate kèm ký số và tải PDF) |
| **04** | `04-kham-pha-ky-uc-ai-nhat-ky-thiet-bi-va-tuy-chon-thong-bao.md` | Loại B (Tính năng) | Khám phá Bộ nhớ cá nhân & Đồ thị Ký ức AI, mở toàn màn hình hộp thoại Đồ thị Ký ức trực quan hóa 3D, xem bảng nhật ký thiết bị đăng nhập và tùy biến 6 kênh thông báo qua Email với tự động lưu |
| **05** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module Profile & User Account |

---

### Phân hệ 07 — Module Workspace & Workbase Management (`07-MODULE-WORKSPACE/`)

| STT | Tên tệp tài liệu | Loại bài | Nội dung trọng tâm |
| :---: | :--- | :---: | :--- |
| **01** | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | Loại A (Quy trình) | Khám phá Trình duyệt Không gian làm việc, chuyển đổi ngữ cảnh an toàn (dọn dẹp cache), khởi tạo Workspace mới (Tên, Slug, Mô tả), sao chép Workspace ID và rời khỏi workspace |
| **02** | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Loại B (Tính năng) | Quản lý thành viên (chủ sở hữu, admin, thành viên), mời qua email kèm cấp Base, kiểm soát hạn mức thành viên (Addon slots), quản lý lời mời đang chờ, duyệt yêu cầu tham gia và liên kết mời |
| **03** | `03-he-thong-phan-quyen-vai-tro-va-danh-sach-role-da-mien.md` | Loại A (Quy trình) | Hệ thống phân quyền hai tầng (Workspace/Base), tra cứu Quyền của tôi, quản lý danh sách Role quyền theo ma trận 32 Miền nghiệp vụ & 17 Loại hành động, tạo role mới và gán quyền nhân sự |
| **04** | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Loại B (Tính năng) | Khởi tạo Base mới, nhân bản & lưu trữ Base, khôi phục kho lưu trữ, Cài đặt chung (tải Logo nén tự động, Múi giờ Timezone), di chuyển tài nguyên thông minh (Preview Transfer), Trung tâm Lịch sử sử dụng (5 thẻ con: Gói dịch vụ, R-Point, Trợ lý AI, Addons quy đổi GB, AI Models), biến môi trường và Vùng nguy hiểm |
| **05** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` | Danh mục & Định tuyến | Bảng siêu dữ liệu (Metadata), điều kiện truy xuất ngữ cảnh, thực thể quan hệ, bộ 10 Tags và định tuyến nhanh cho Module Workspace & Workbase Management |
