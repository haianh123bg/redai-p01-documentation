## Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Profile & User Account

Tài liệu này đóng vai trò là danh mục điều hướng trung tâm (Catalog Index) của Phân hệ **06 — Module Profile & User Account** trên hệ thống **RedAI**. Bảng tổng hợp siêu dữ liệu dưới đây giúp người dùng, quản trị viên và đặc biệt là các trợ lý ảo AI Agent nhanh chóng xác định đúng tài liệu nghiệp vụ cần tham chiếu theo từng tình huống thiết lập hồ sơ, bảo mật tài khoản, thông tin pháp nhân và quản trị phiên làm việc cụ thể.

---

## Bảng tổng hợp siêu dữ liệu các tài liệu nghiệp vụ

| Thuộc tính | Chi tiết tài liệu 01 | Chi tiết tài liệu 02 |
| :--- | :--- | :--- |
| **Tên file** | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | `02-thiet-lap-bao-mat-xac-thuc-hai-buoc-va-quan-ly-phien-dang-nhap.md` |
| **Tiêu đề tài liệu** | Quy trình quản lý hồ sơ cá nhân và xác thực thông tin | Thiết lập bảo mật tài khoản, xác thực hai bước và quản lý phiên đăng nhập |
| **Mô tả nghiệp vụ** | Hướng dẫn mở trang Hồ sơ cá nhân (`/profile`), đổi ảnh bìa Cover Image (tải ảnh S3, xem trước thời gian thực), đổi và nén ảnh đại diện Avatar WebP (tối đa 2MB), điền thông tin định danh (Họ tên, Giới tính, Ngày sinh với bộ chọn ngày sinh dạng lịch, Địa chỉ) và xác thực Email / Số điện thoại qua mã OTP 6 số. | Hướng dẫn đổi mật khẩu đăng nhập (mật khẩu hiện tại, mật khẩu mới, kiểm tra độ mạnh, icon ẩn/hiện mắt), kích hoạt Xác thực 2 bước (2FA qua SMS, 2FA qua Email, Google Authenticator với mã QR và OTP 6 số), mở trang Bảo mật phiên (`/settings/security`), theo dõi danh sách thiết bị và thu hồi phiên từ xa. |
| **Agent nên đọc khi** | Cần tra cứu hoặc cập nhật thông tin cá nhân của người dùng, kiểm tra trạng thái xác thực email/SĐT, gửi mã OTP xác minh liên hệ hoặc hướng dẫn đổi avatar. | Cần đổi mật khẩu, kiểm tra trạng thái kích hoạt 2FA, bật/tắt các kênh OTP, hoặc kiểm tra danh sách thiết bị/IP lạ đang đăng nhập để thu hồi phiên khẩn cấp. |
| **Không dùng khi** | Cần nâng cấp tài khoản doanh nghiệp hoặc quản lý tài khoản ngân hàng thụ hưởng. | Cần thao tác chỉnh sửa thông tin họ tên, ngày sinh hoặc xem đồ thị ký ức AI. |
| **Thực thể & Quan hệ** | `UserProfile`, `AvatarMedia`, `CoverImageMedia`, `ContactVerification`. Gắn liền với danh tính Người dùng trên hệ thống. | `UserSecurity`, `TwoFactorAuth`, `BrowserSession`, `PasswordCredential`. Quản trị an ninh truy cập tài khoản. |
| **10 Tags chuẩn hóa** | `user-profile`, `profile-header`, `cover-image`, `avatar-upload`, `personal-info`, `date-picker`, `verify-email`, `verify-phone`, `otp-verification`, `user-identity` | `account-security`, `change-password`, `two-factor-auth`, `sms-2fa`, `email-2fa`, `google-authenticator`, `totp-qr`, `session-security`, `revoke-session`, `device-management` |

---

| Thuộc tính | Chi tiết tài liệu 03 | Chi tiết tài liệu 04 |
| :--- | :--- | :--- |
| **Tên file** | `03-quan-ly-thong-tin-doanh-nghiep-tai-khoan-ngan-hang-va-hop-dong.md` | `04-kham-pha-ky-uc-ai-nhat-ky-thiet-bi-va-tuy-chon-thong-bao.md` |
| **Tiêu đề tài liệu** | Quản lý thông tin doanh nghiệp, tài khoản ngân hàng và hợp đồng | Khám phá ký ức AI, nhật ký thiết bị và tùy chọn thông báo |
| **Mô tả nghiệp vụ** | Hướng dẫn nâng cấp tài khoản Cá nhân lên Doanh nghiệp (Biểu mẫu Nâng cấp tài khoản Doanh nghiệp: tên công ty, MST, người đại diện, chức vụ, địa chỉ trụ sở), cấu hình Tài khoản Ngân hàng thụ hưởng (Thẻ Thông tin ngân hàng với bộ chọn NAPAS/VietQR tiếng Việt không dấu, tên in hoa), và quản lý 2 hợp đồng số (Hợp đồng nguyên tắc & Hợp đồng Affiliate kèm ký số và tải PDF). | Hướng dẫn khai thác Bộ nhớ cá nhân & Đồ thị Ký ức AI (Thẻ Bộ nhớ cá nhân), mở toàn màn hình hộp thoại Đồ thị Ký ức khám phá mạng lưới tri thức 3D, xem bảng nhật ký thiết bị và lịch sử xác thực, và tùy biến 6 kênh thông báo qua Email với cơ chế tự động lưu. |
| **Agent nên đọc khi** | Cần hỗ trợ người dùng điền thông tin doanh nghiệp, tra cứu mã số thuế, cài đặt tài khoản ngân hàng để nhận tiền hoa hồng, hoặc kiểm tra trạng thái ký kết hợp đồng số. | Cần tra cứu mạng lưới ký ức AI về người dùng, kích hoạt đồng bộ ký ức đồ thị, kiểm tra lịch sử đăng nhập/IP trong nhật ký thiết bị hoặc bật/tắt nhận email thông báo. |
| **Không dùng khi** | Cần đổi mật khẩu tài khoản hoặc xác thực số điện thoại cá nhân. | Cần ký hợp đồng pháp lý hoặc cập nhật thông tin tài khoản ngân hàng. |
| **Thực thể & Quan hệ** | `BusinessInfo`, `BankInfo`, `RuleContract`, `AffiliateContract`, `DigitalSignature`. Dành riêng cho User Workspace. | `UserMemory`, `ActorMemoryGraph`, `AuthVerificationLog`, `NotificationSettings`. Cá nhân hóa và giám sát an ninh. |
| **10 Tags chuẩn hóa** | `business-info`, `upgrade-business`, `tax-code`, `bank-info`, `vietqr-banks`, `account-holder`, `contract-management`, `principle-contract`, `affiliate-contract`, `digital-signature` | `user-memories`, `ai-knowledge-graph`, `unified-graph-modal`, `3d-memory-graph`, `memory-sync`, `auth-logs`, `device-audit`, `notification-settings`, `email-notifications`, `auto-save-settings` |

---

| Thuộc tính | Chi tiết tài liệu 05 |
| :--- | :--- |
| **Tên file** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` |
| **Tiêu đề tài liệu** | Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Profile & User Account |
| **Mô tả nghiệp vụ** | Bảng tổng hợp siêu dữ liệu, bản đồ từ khóa và quy tắc định tuyến thông minh giữa người dùng, hệ thống tài liệu và trợ lý ảo AI Agent cho toàn bộ Phân hệ 06 — Module Profile & User Account. |
| **Agent nên đọc khi** | Cần định vị nhanh tài liệu phù hợp khi tiếp nhận yêu cầu từ người dùng liên quan đến thông tin tài khoản, mật khẩu, 2FA, doanh nghiệp, ngân hàng, ký ức AI hoặc thiết bị đăng nhập. |
| **Không dùng khi** | Đã xác định được chính xác nghiệp vụ cụ thể cần thực hiện trong 4 tài liệu chuyên sâu 01, 02, 03, 04. |
| **Thực thể & Quan hệ** | `DocumentationCatalog`, `ModuleMetadata`, `AIAgentRouting`. |
| **10 Tags chuẩn hóa** | `profile-catalog`, `account-metadata`, `agent-routing`, `identity-guide`, `security-guide`, `business-guide`, `memory-guide`, `profile-module`, `user-settings`, `redai-documentation` |

---

## Bảng định tuyến nhanh theo tình huống thực tế

Dưới đây là bảng tra cứu phản xạ nhanh giúp người dùng và trợ lý ảo AI Agent chọn ngay tài liệu cần thiết:

| Tình huống thực tế phát sinh | Tài liệu cần mở ngay | Công cụ / Đường dẫn trọng tâm |
| :--- | :--- | :--- |
| Muốn đổi ảnh đại diện hoặc thay ảnh bìa hồ sơ cá nhân | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | Khu vực Ảnh đại diện & Ảnh bìa, `updateAvatar` |
| Cần cập nhật lại họ tên đầy đủ, ngày sinh và giới tính | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | Thẻ Thông tin cá nhân, `updatePersonalProfile` |
| Muốn xác thực địa chỉ email để nhận thông báo an toàn | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | Hộp thoại Xác thực Email, `sendEmailVerificationOtp` |
| Muốn xác thực số điện thoại để bật bảo mật 2 lớp | `01-quy-trinh-quan-ly-ho-so-ca-nhan-va-xac-thuc-thong-tin.md` | Hộp thoại Xác thực Số điện thoại, `sendPhoneVerificationOtp` |
| Cần đổi mật khẩu tài khoản vì nghi ngờ bị lộ | `02-thiet-lap-bao-mat-xac-thuc-hai-buoc-va-quan-ly-phien-dang-nhap.md` | Khối Đổi mật khẩu, `changePassword` |
| Muốn bật xác thực 2 bước bằng mã Google Authenticator | `02-thiet-lap-bao-mat-xac-thuc-hai-buoc-va-quan-ly-phien-dang-nhap.md` | Khối Google Authenticator, `setupGoogleAuth` |
| Nghi ngờ có người lạ đăng nhập, muốn đăng xuất tất cả thiết bị khác | `02-thiet-lap-bao-mat-xac-thuc-hai-buoc-va-quan-ly-phien-dang-nhap.md` | Trang `/settings/security`, `revokeOtherBrowserSessions` |
| Muốn nâng cấp tài khoản từ Cá nhân lên Doanh nghiệp có MST | `03-quan-ly-thong-tin-doanh-nghiep-tai-khoan-ngan-hang-va-hop-dong.md` | Biểu mẫu Nâng cấp tài khoản Doanh nghiệp, `upgradeToBusiness` |
| Cần thêm số tài khoản ngân hàng Vietcombank để nhận hoa hồng | `03-quan-ly-thong-tin-doanh-nghiep-tai-khoan-ngan-hang-va-hop-dong.md` | Thẻ Thông tin ngân hàng, `updateBankInfo` |
| Muốn mở xem và ký Hợp đồng đối tác kinh doanh Affiliate | `03-quan-ly-thong-tin-doanh-nghiep-tai-khoan-ngan-hang-va-hop-dong.md` | Thẻ Quản lý hợp đồng, `/contract-affiliate` |
| Muốn xem trợ lý ảo AI Agent đang ghi nhớ những gì về mình | `04-kham-pha-ky-uc-ai-nhat-ky-thiet-bi-va-tuy-chon-thong-bao.md` | Thẻ Bộ nhớ cá nhân, Hộp thoại Đồ thị Ký ức |
| Cần tra cứu lịch sử 10 lần đăng nhập gần nhất xem IP ở đâu | `04-kham-pha-ky-uc-ai-nhat-ky-thiet-bi-va-tuy-chon-thong-bao.md` | Thẻ Lịch sử đăng nhập & Thiết bị, `getAuthVerificationLogs` |
| Không muốn nhận email quảng cáo và khuyến mãi từ hệ thống | `04-kham-pha-ky-uc-ai-nhat-ky-thiet-bi-va-tuy-chon-thong-bao.md` | Thẻ Tùy chọn thông báo, `updateUserNotificationSettings` |

---

## Danh mục từ khóa tìm kiếm (Keyword Index)

- **Hồ sơ & Nhận diện**: `hồ sơ cá nhân`, `profile page`, `ảnh bìa cover`, `avatar người dùng`, `nén ảnh webp`, `họ và tên`, `giới tính`, `ngày sinh date picker`, `địa chỉ`, `xác thực email`, `xác thực sđt`, `otp 6 số`, `tích xanh verified`, `phone input country`.
- **Bảo mật & Phiên đăng nhập**: `đổi mật khẩu`, `mật khẩu hiện tại`, `mật khẩu mới`, `ẩn hiện mật khẩu`, `xác thực 2 bước`, `2fa`, `sms otp`, `email otp`, `google authenticator`, `totp qr code`, `secret key`, `quản lý phiên`, `phiên hiện tại`, `ip address`, `user agent`, `thu hồi phiên`, `đăng xuất các phiên khác`, `settings security`.
- **Doanh nghiệp, Ngân hàng & Hợp đồng**: `tài khoản doanh nghiệp`, `nâng cấp doanh nghiệp`, `tên công ty`, `mã số thuế mst`, `người đại diện`, `chức vụ`, `địa chỉ trụ sở`, `tài khoản ngân hàng`, `chọn ngân hàng vietqr`, `napas`, `số tài khoản`, `tên chủ tài khoản in hoa`, `chi nhánh`, `quản lý hợp đồng`, `hợp đồng nguyên tắc`, `hợp đồng affiliate`, `chữ ký điện tử`, `tải pdf hợp đồng`.
- **Ký ức AI, Thiết bị & Thông báo**: `bộ nhớ cá nhân`, `user memories`, `actor memory panel`, `đồ thị ký ức 3d`, `unified graph modal`, `đồng bộ ký ức`, `nhật ký xác thực`, `auth verification logs`, `lịch sử đăng nhập`, `lọc date range`, `tùy chọn thông báo`, `email thông báo`, `hóa đơn billing`, `tính năng mới`, `affiliate email`, `khuyến mãi promotional`, `auto-save settings`.
