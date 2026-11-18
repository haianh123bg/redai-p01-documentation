## Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Workspace & Workbase Management

Tài liệu này đóng vai trò là danh mục điều hướng trung tâm (Catalog Index) của Phân hệ **07 — Module Workspace & Workbase Management** trên hệ thống **RedAI**. Bảng tổng hợp siêu dữ liệu dưới đây giúp người dùng, quản trị viên tổ chức và đặc biệt là các trợ lý ảo AI Agent nhanh chóng xác định đúng tài liệu nghiệp vụ cần tham chiếu theo từng tình huống khởi tạo không gian, điều phối thành viên, phân quyền đa miền, quản trị cơ sở dữ liệu Base và di chuyển tài nguyên cụ thể.

---

## Bảng tổng hợp siêu dữ liệu các tài liệu nghiệp vụ

| Thuộc tính | Chi tiết tài liệu 01 | Chi tiết tài liệu 02 |
| :--- | :--- | :--- |
| **Tên file** | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` |
| **Tiêu đề tài liệu** | Quy trình khởi tạo, chuyển đổi ngữ cảnh và điều hướng Workspace | Quản lý thành viên, lời mời, yêu cầu tham gia và liên kết mời |
| **Mô tả nghiệp vụ** | Hướng dẫn mở Trình duyệt Không gian làm việc từ thanh điều hướng hoặc bảng chat AI, duyệt danh mục Workspace và các Base trực thuộc, chuyển đổi ngữ cảnh làm việc an toàn (dọn dẹp cache và reset phiên chat), tạo mới Workspace (Tên, Slug, Mô tả), sao chép Workspace ID vào clipboard, tra cứu nhanh quyền hạn và quy trình rời khỏi Workspace cộng tác. | Hướng dẫn quản trị nhân sự trong Workspace: xem bảng danh sách thành viên, mời thành viên mới qua Email kèm cấp quyền Base trực tiếp, giám sát hạn mức thành viên (Member Limit) và mua thêm slot Addon, đổi vai trò thành viên, xóa thành viên, quản lý danh sách lời mời đang chờ (gửi lại, thu hồi, xóa hàng loạt), duyệt/từ chối yêu cầu tham gia, và cấu hình tham gia qua liên kết mời công khai. |
| **Agent nên đọc khi** | Cần hỗ trợ người dùng tạo Workspace mới, kiểm tra tính khả dụng của Slug, chuyển đổi ngữ cảnh làm việc hoặc lấy mã Workspace ID để cấu hình hệ thống. | Cần tra cứu danh sách thành viên, gửi lời mời gia nhập qua email, nâng/hạ vai trò thành viên, thu hồi lời mời gửi nhầm hoặc quản lý liên kết mời tham gia. |
| **Không dùng khi** | Cần thiết lập phân quyền chi tiết từng bảng dữ liệu hoặc di chuyển workflow giữa các Base. | Cần tạo vai trò phân quyền tùy chỉnh (Custom Roles) hoặc xóa vĩnh viễn Workspace. |
| **Thực thể & Quan hệ** | `Workspace`, `WorkspaceContext`, `WorkspaceSlug`, `BaseScope`. Tổ chức phân cấp cấp cao nhất của hệ thống. | `WorkspaceMember`, `WorkspaceInvite`, `JoinRequest`, `InviteLink`. Quản trị nguồn nhân lực và cộng tác. |
| **10 Tags chuẩn hóa** | `workspace-management`, `workspace-browser`, `create-workspace`, `workspace-slug`, `context-switch`, `scope-navigation`, `workspace-id`, `my-permissions`, `leave-workspace`, `active-context` | `workspace-members`, `invite-member`, `member-roles`, `member-limit`, `addon-slots`, `pending-invites`, `join-requests`, `invite-links`, `regenerate-link`, `revoke-invite` |

---

| Thuộc tính | Chi tiết tài liệu 03 | Chi tiết tài liệu 04 |
| :--- | :--- | :--- |
| **Tên file** | `03-he-thong-phan-quyen-vai-tro-va-danh-sach-role-da-mien.md` | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` |
| **Tiêu đề tài liệu** | Hệ thống phân quyền, vai trò và danh sách role đa miền | Quản lý không gian Base, di chuyển tài nguyên, lịch sử sử dụng và vùng nguy hiểm |
| **Mô tả nghiệp vụ** | Hướng dẫn cơ chế kiểm soát truy cập dựa trên khả năng đa miền (CBAC) của RedAI: tra cứu Quyền của tôi trên Workspace/Base, mở Trung tâm Danh sách role quyền, lọc theo 32 Miền nghiệp vụ và 17 Loại hành động, khởi tạo Role tùy chỉnh mới (Mã code, Tên, Phạm vi Workspace/Base, Mô tả), chọn năng lực chi tiết (Capabilities) và gán Role cho từng thành viên. | Hướng dẫn quản trị vòng đời cơ sở dữ liệu Base trong Workspace: tạo Base mới (Tên, Icon, Màu sắc), sao chép Base ID, nhân bản Base, lưu trữ Base, quản lý kho Không gian đã lưu trữ (hoàn tác khôi phục hoặc xóa vĩnh viễn), cài đặt chung Workspace (tải Logo với cơ chế nén tự động, cập nhật tên, mô tả, cấu hình Múi giờ Timezone), di chuyển tài nguyên thông minh giữa các Base có phân tích trước (Preview Transfer), khai thác Trung tâm Lịch sử sử dụng (5 thẻ con: Gói dịch vụ, R-Point, Trợ lý AI, Addons quy đổi GB, AI Models), quản lý Biến môi trường toàn cục, và thao tác Vùng nguy hiểm (xóa vĩnh viễn Workspace). |
| **Agent nên đọc khi** | Cần tạo vai trò phân quyền tùy chỉnh, tra cứu danh mục quyền hạn của một thành viên, kiểm tra quyền hạn hiện tại của người dùng hoặc gán quyền bảo mật cho nhân sự. | Cần tạo mới cơ sở dữ liệu Base, nhân bản cấu hình Base, khôi phục Base bị lưu trữ, cập nhật Logo nhận diện, kiểm tra lịch sử thanh toán, xem mức tiêu hao điểm Trợ lý AI, giám sát dung lượng Cloud Storage, di chuyển tài nguyên giữa các Base hoặc cấu hình múi giờ Workspace. |
| **Không dùng khi** | Cần gửi lời mời thành viên qua email hoặc bật/tắt liên kết mời tham gia. | Cần tạo mới Workspace hoặc quản lý danh sách lời mời đang chờ. |
| **Thực thể & Quan hệ** | `ScopeRole`, `Capability`, `DomainPermission`, `UserRoleAssignment`. Kiểm soát an ninh truy cập hai tầng. | `WorkspaceBase`, `ArchivedBase`, `WorkspaceLogo`, `ResourceTransfer`, `UsageHistory`, `SubscriptionHistory`, `RPointHistory`, `AssistantSpending`, `AddonUsage`, `ModelCombo`, `EnvironmentVariable`, `DangerZone`. |
| **10 Tags chuẩn hóa** | `role-management`, `workspace-roles`, `base-roles`, `capability-acl`, `32-domains`, `custom-roles`, `assign-role`, `role-capabilities`, `security-permissions`, `scope-roles` | `base-management`, `workspace-logo`, `archived-bases`, `resource-transfer`, `usage-history`, `subscription-history`, `assistant-spending`, `addon-usages`, `model-combos`, `danger-zone-delete` |

---

| Thuộc tính | Chi tiết tài liệu 05 |
| :--- | :--- |
| **Tên file** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` |
| **Tiêu đề tài liệu** | Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Workspace & Workbase Management |
| **Mô tả nghiệp vụ** | Bảng tổng hợp siêu dữ liệu, bản đồ từ khóa và quy tắc định tuyến thông minh giữa người dùng, hệ thống tài liệu và trợ lý ảo AI Agent cho toàn bộ Phân hệ 07 — Module Workspace & Workbase Management. |
| **Agent nên đọc khi** | Cần định vị nhanh tài liệu phù hợp khi tiếp nhận yêu cầu từ người dùng liên quan đến không gian làm việc, tạo workspace, mời thành viên, phân quyền vai trò, quản lý base hoặc di chuyển dữ liệu. |
| **Không dùng khi** | Đã xác định được chính xác nghiệp vụ cụ thể cần thực hiện trong 4 tài liệu chuyên sâu 01, 02, 03, 04. |
| **Thực thể & Quan hệ** | `DocumentationCatalog`, `ModuleMetadata`, `AIAgentRouting`. |
| **10 Tags chuẩn hóa** | `workspace-catalog`, `workbase-metadata`, `agent-routing`, `workspace-guide`, `member-guide`, `permission-guide`, `base-guide`, `transfer-guide`, `workbase-module`, `redai-documentation` |

---

## Bảng định tuyến nhanh theo tình huống thực tế

Dưới đây là bảng tra cứu phản xạ nhanh giúp người dùng và trợ lý ảo AI Agent chọn ngay tài liệu cần thiết:

| Tình huống thực tế phát sinh | Tài liệu cần mở ngay | Công cụ / Đường dẫn trọng tâm |
| :--- | :--- | :--- |
| Muốn tạo một Workspace mới cho chi nhánh hoặc phòng ban | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | `createWorkspace`, `/workspaces/create` |
| Cần chuyển sang làm việc tại một Workspace hoặc Base khác | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | Trình duyệt Không gian làm việc, `switchWorkspaceContext` |
| Cần sao chép mã Workspace ID để dán vào cấu hình tích hợp | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | Menu ba chấm Workspace, `copyWorkspaceId` |
| Muốn rời khỏi một Workspace cộng tác mà mình không còn tham gia | `01-quy-trinh-khoi-tao-chuyen-doi-ngu-canh-va-dieu-huong-workspace.md` | Tùy chọn Rời khỏi workspace, `leaveWorkspace` |
| Cần mời nhân viên mới vào Workspace qua email | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Thẻ Thành viên, `inviteWorkspaceMember` |
| Workspace hết slot thành viên, muốn kiểm tra và mua thêm | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Khối Giới hạn thành viên, Mua thêm slot |
| Muốn thu hồi lời mời gửi nhầm hoặc gửi lại lời mời đã hết hạn | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Thẻ Lời mời đang chờ, `revokeWorkspaceInvite` |
| Muốn lấy liên kết mời công khai để gửi vào nhóm chat nội bộ | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Thẻ Liên kết mời, `getWorkspaceInviteLink` |
| Cần duyệt đơn đăng ký tham gia Workspace của nhân sự | `02-quan-ly-thanh-vien-loi-moi-yeu-cau-tham-gia-va-lien-ket-moi.md` | Thẻ Yêu cầu tham gia, `approveJoinRequest` |
| Muốn kiểm tra tài khoản của mình được phép làm những gì | `03-he-thong-phan-quyen-vai-tro-va-danh-sach-role-da-mien.md` | Hộp thoại Quyền của tôi, `getMyScopeCapabilities` |
| Cần tạo một Role mới chỉ cho phép nhân viên xem và sửa bảng dữ liệu | `03-he-thong-phan-quyen-vai-tro-va-danh-sach-role-da-mien.md` | Hộp thoại Danh sách role quyền, `createScopeRole` |
| Cần đổi quyền hạn hoặc gán vai trò mới cho một thành viên | `03-he-thong-phan-quyen-vai-tro-va-danh-sach-role-da-mien.md` | Nút Sửa quyền thành viên, `assignScopeRoleToUser` |
| Muốn tạo thêm một cơ sở dữ liệu Base mới trong Workspace | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Tùy chọn Thêm không gian, `createWorkspaceBase` |
| Cần nhân bản nguyên vẹn một Base để làm mẫu cho dự án mới | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Menu ba chấm Base, `duplicateWorkspaceBase` |
| Muốn khôi phục một Base đã lưu trữ quay trở lại hoạt động | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Không gian đã lưu trữ, `restoreArchivedBase` |
| Cần đổi múi giờ Workspace sang GMT+7 cho công thức và webhook | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Cài đặt chung, `updateWorkspaceSettings` |
| Muốn tải ảnh đại diện Logo mới cho thương hiệu Workspace | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Cài đặt chung, `uploadWorkspaceLogo` |
| Cần tra cứu lịch sử thanh toán và hóa đơn gói cước Workspace | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Lịch sử sử dụng / Gói dịch vụ, `getWorkspaceSubscriptionHistory` |
| Muốn kiểm tra số điểm R-Point đã tiêu tốn cho từng Trợ lý AI & Model | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Lịch sử sử dụng / Trợ lý AI, `getWorkspaceAssistantSpending` |
| Cần giám sát định mức dung lượng lưu trữ Cloud Storage (GB) & Addon | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Lịch sử sử dụng / Addons, `getWorkspaceAddonUsages` |
| Muốn xem danh mục các gói Combo Model AI được cấp phát | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Lịch sử sử dụng / AI Models, `getWorkspaceModelCombos` |
| Muốn chuyển một Workflow hoặc Bảng dữ liệu từ Base A sang Base B | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Di chuyển dữ liệu, `executeResourceTransfer` |
| Cần cấu hình biến môi trường API Key dùng chung cho toàn Workspace | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Hộp thoại Quản lý biến môi trường, `setWorkspaceEnvironmentVariable` |
| Muốn xóa vĩnh viễn toàn bộ Workspace và hủy toàn bộ dữ liệu | `04-quan-ly-khong-gian-base-di-chuyen-tai-nguyen-va-vung-nguy-hiem.md` | Thẻ Vùng nguy hiểm, `deleteWorkspacePermanent` |

---

## Danh mục từ khóa tìm kiếm (Keyword Index)

- **Không gian & Điều hướng**: `không gian làm việc`, `workspace`, `trình duyệt không gian`, `chuyển đổi workspace`, `active context`, `slug workspace`, `workspace id`, `tạo workspace mới`, `rời workspace`, `hệ thống phân cấp`.
- **Thành viên & Kết nối**: `quản lý thành viên`, `thêm thành viên`, `mời qua email`, `chủ sở hữu`, `quản trị viên workspace`, `thành viên workspace`, `giới hạn thành viên`, `mua thêm slot`, `lời mời đang chờ`, `gửi lại lời mời`, `thu hồi lời mời`, `xóa lời mời hàng loạt`, `yêu cầu tham gia`, `duyệt gia nhập`, `liên kết mời`, `tạo liên kết mới`, `sao chép link mời`.
- **Phân quyền & Vai trò**: `phân quyền workspace`, `quyền của tôi`, `danh sách role quyền`, `tạo role mới`, `gán quyền thành viên`, `mã code role`, `32 miền nghiệp vụ`, `bảng động dynamic table`, `trợ lý ai`, `workflow`, `17 hành động`, `xem read`, `tạo mới create`, `xóa delete`, `quản lý manage`, `capabilities`, `acl`.
- **Cơ sở dữ liệu Base & Vận hành**: `tạo base mới`, `không gian nhóm`, `nhân bản base`, `sao chép base id`, `lưu trữ base`, `kho lưu trữ`, `khôi phục base`, `xóa vĩnh viễn base`, `cài đặt chung`, `logo workspace`, `tải logo`, `múi giờ timezone`, `gmt+7`, `lịch sử sử dụng`, `gói dịch vụ`, `hóa đơn thanh toán`, `r-point`, `tiêu hao trợ lý ai`, `định mức addon`, `dung lượng cloud storage gb`, `combo model ai`, `di chuyển dữ liệu`, `resource transfer`, `preview phân tích`, `biến môi trường workspace`, `vùng nguy hiểm`, `xóa workspace vĩnh viễn`.
