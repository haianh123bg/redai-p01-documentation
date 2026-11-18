## Skills - Tổng quan và cách hoạt động

**Tên file:** `1. Skills - Tổng quan và cách hoạt động.md`

**Tiêu đề:** Skills - Tổng quan và cách hoạt động

**Mô tả:** Giải thích Skill là gì; vai trò cốt lõi của `skill.md`; sự khác nhau giữa Skill hệ thống và Skill User; các thành phần Docs, Tools, MCPs, Workflows; phạm vi dữ liệu; điều kiện để Agent kích hoạt Workflow qua Skill; và khả năng nhận template Skill đã phát hành trên RedHub.

**Agent nên truy xuất khi:** Cần giải thích khái niệm, thành phần, phạm vi hoặc cách Skill cung cấp chỉ dẫn và tài nguyên cho Agent; cần phân biệt Skill hệ thống với Skill User; hoặc cần xác định Workflow nào có thể được Agent kích hoạt qua Skill.

**Không dùng khi:** Người dùng yêu cầu một quy trình cụ thể như tạo, sửa, nhân bản, quản lý tài nguyên, tạo Snapshot, Import hoặc Export.

**Thực thể và quan hệ:** `Skill → có thành phần cốt lõi → skill.md`; `Skill hệ thống → dùng chung → mọi tài khoản/Workspace/Base`; `Skill User → thuộc → Workspace và Base`; `Skill → liên kết → Docs, Tools, MCPs, Workflows`; `Workflow được Agent kích hoạt qua Skill → có node đầu tiên → Kích hoạt Click | Kích hoạt Hệ thống Tùy chỉnh | Kích hoạt Tin nhắn`; `template Skill đã phát hành → được nhận từ → RedHub`.

**Tags (10):** `skills/tong-quan`, `skills/skill-md`, `skills/skill-he-thong`, `skills/skill-user`, `skills/pham-vi-workspace-base`, `skills/tai-nguyen-lien-ket`, `skills/workflow-trigger`, `skills/kich-hoat-click`, `skills/kich-hoat-he-thong-tuy-chinh`, `skills/kich-hoat-tin-nhan`

## Skills - Tạo và cập nhật Skill

**Tên file:** `2. Skills - Tạo và cập nhật Skill.md`

**Tiêu đề:** Skills - Tạo và cập nhật Skill

**Mô tả:** Hướng dẫn tạo Skill User thủ công hoặc bằng AI; nhập chỉ dẫn vào `skill.md`; yêu cầu Agent Orchestrator hoặc Agent do người dùng tạo có gắn Skill `RedAI - Module - Skill` tạo Skill; tạo qua Telegram Bot, Zalo OA, Zalo Personal hoặc Facebook bằng cách mở cấu hình Agent, chọn `Kênh`, chọn kênh đầu ra, đặt người dùng trong cuộc hội thoại thành `Chủ sở hữu` và bảo đảm quyền cho phép AI trả lời không bị tắt; đồng thời hướng dẫn cập nhật Skill trực tiếp hoặc bằng AI.

**Agent nên truy xuất khi:** Người dùng muốn tạo Skill mới, chưa biết viết `skill.md`, muốn AI tạo tự động, muốn tạo Skill qua Chat Panel hoặc kênh giao tiếp ngoài, hoặc cần sửa Skill User đã có.

**Không dùng khi:** Người dùng chỉ muốn liên kết tài nguyên, nhân bản Skill, quản lý Snapshot, Import hoặc Export gói Skill.

**Thực thể và quan hệ:** `Tạo thường → tạo → Skill User`; `Tạo bằng AI → sinh nội dung → skill.md`; `Agent Orchestrator (RedAI - Agent Default) → có thể tạo → Skill`; `Agent do người dùng tạo + RedAI - Module - Skill → có thể tạo trong app → Skill`; `cấu hình Agent → Kênh → kênh đầu ra → Quyền AI theo hội thoại`; `người dùng trong cuộc hội thoại + vai trò Chủ sở hữu + quyền AI trả lời không bị tắt → có thể yêu cầu tạo Skill qua → Telegram Bot | Zalo OA | Zalo Personal | Facebook`; `Cập nhật bằng AI → sửa → nội dung Skill`.

**Tags (10):** `skills/tao-skill`, `skills/tao-thuong`, `skills/tao-bang-ai`, `skills/agent-orchestrator`, `skills/redai-module-skill`, `skills/agent-user-tao-skill`, `skills/quyen-ai-theo-hoi-thoai`, `skills/vai-tro-chu-so-huu`, `skills/sua-skill`, `skills/skill-md`

## Skills - Quản lý Skill và tài nguyên liên kết

**Tên file:** `3. Skills - Quản lý Skill và tài nguyên liên kết.md`

**Tiêu đề:** Skills - Quản lý Skill và tài nguyên liên kết

**Mô tả:** Hướng dẫn dùng đúng các nút `Tìm kiếm`, `Lọc`, `Chọn tất cả`, `Xóa`, `Export package`, `Tải lại dữ liệu` và các nút trên thẻ Skill; sửa, nhân bản, xóa Skill; thêm, sửa hoặc xóa Docs; liên kết hoặc xóa liên kết Tools, MCPs, Workflows; phân biệt chức năng của nút thùng rác theo ngữ cảnh; và kiểm tra node đầu tiên của Workflow trước khi dùng qua Skill.

**Agent nên truy xuất khi:** Người dùng cần thao tác với thanh công cụ trang chi tiết hoặc thẻ Skill; dùng các nút `Snapshots`, `Export package`, `Sửa`, `Nhân bản`, `Xóa`; quản lý Docs; liên kết hoặc xóa liên kết Tools/MCPs/Workflows; hoặc phân biệt xóa Skill với xóa tài nguyên đã chọn.

**Không dùng khi:** Người dùng chỉ hỏi khái niệm tổng quan hoặc muốn quản lý Snapshot, phát hành lên RedHub, Import hay Export gói Skill.

**Thực thể và quan hệ:** `Skill hệ thống hoặc Skill User → Nhân bản → Skill User mới`; `Skill → chứa → Docs`; `Skill → liên kết → Tools, MCPs, Workflows`; `xóa liên kết Tool/MCP/Workflow → không xóa → tài nguyên gốc`; `chọn Docs + <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> Xóa → xóa → Docs đã chọn`; `không chọn tài nguyên + <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> Xóa skill → xóa → Skill User`.

**Tags (10):** `skills/quan-ly-skill`, `skills/thanh-cong-cu`, `skills/nhan-ban-skill`, `skills/quan-ly-docs`, `skills/xoa-docs`, `skills/xoa-skill`, `skills/lien-ket-tools`, `skills/lien-ket-mcp`, `skills/lien-ket-workflows`, `skills/go-tai-nguyen`

## Skills - Quản lý Snapshot và gói Skill

**Tên file:** `4. Skills - Quản lý Snapshot và gói Skill.md`

**Tiêu đề:** Skills - Quản lý Snapshot và gói Skill

**Mô tả:** Hướng dẫn nhấn `Snapshots` trên thẻ Skill để tạo Snapshot; tìm, lọc, xóa Snapshot; dùng `Import vào skill` để tạo một Skill User mới; dùng Snapshot làm nguồn phát hành Skill lên RedHub; Export gói Skill xuống thiết bị; và dùng `Import package` để nhập gói Skill từ tệp `.json`.

**Agent nên truy xuất khi:** Người dùng muốn lưu trạng thái Skill, tìm hoặc xóa Snapshot, tạo lại Skill từ Snapshot, chuẩn bị nguồn phát hành Skill lên RedHub, tải gói Skill xuống hoặc nhập gói Skill từ thiết bị.

**Không dùng khi:** Người dùng muốn sửa `skill.md` hoặc quản lý Docs, Tools, MCPs và Workflows trong Skill.

**Thực thể và quan hệ:** `Snapshots trên thẻ Skill → mở → Snapshot của Skill`; `Snapshot → lưu → trạng thái Skill`; `Import vào skill → tạo → Skill User mới`; `Snapshot → làm nguồn dữ liệu cho → Skill phát hành trên RedHub`; `Export package → tải xuống → gói Skill`; `Import package + tệp .json → tạo → Skill User mới`; `Skill User mới → thuộc → Workspace/Base hiện tại`.

**Tags (10):** `skills/snapshot`, `skills/tao-snapshot`, `skills/import-vao-skill`, `skills/xoa-snapshot`, `skills/nguon-phat-hanh-redhub`, `skills/phat-hanh-skill`, `skills/export-package`, `skills/import-package`, `skills/import-json`, `skills/skill-user-moi`

## Định tuyến nhanh

| Ý định truy vấn | Tài liệu ưu tiên |
| --- | --- |
| Hiểu Skill, `skill.md`, loại Skill, thành phần và phạm vi | **1. Skills - Tổng quan và cách hoạt động.md** |
| Tạo hoặc cập nhật Skill bằng giao diện, AI hay Agent | **2. Skills - Tạo và cập nhật Skill.md** |
| Quản lý Skill, nhân bản, Docs, Tools, MCPs và Workflows | **3. Skills - Quản lý Skill và tài nguyên liên kết.md** |
| Snapshot, tạo Skill từ Snapshot, phát hành RedHub, Import hoặc Export | **4. Skills - Quản lý Snapshot và gói Skill.md** |
