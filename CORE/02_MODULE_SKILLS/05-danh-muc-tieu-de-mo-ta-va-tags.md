## Module Skills - Quy trình tạo kỹ năng, soạn chỉ thị định tuyến và quản lý tài liệu Docs

**Tên file:** `01-quy-trinh-tao-ky-nang-soan-chi-thi-dinh-tuyen-va-quan-ly-tai-lieu-docs.md`

**Tiêu đề:** Module Skills - Quy trình tạo kỹ năng, soạn chỉ thị định tuyến và quản lý tài liệu Docs

**Mô tả:** Hướng dẫn chi tiết 2 chế độ khởi tạo Kỹ năng trên màn hình `/skills` (chế độ `Tạo thường` với đúng 5 trường giao diện: `Tên Skill`, `Mô tả`, `Thẻ / Tags`, `Logo`, `Nội dung Skill` hỗ trợ gõ `@` chèn liên kết tài nguyên; và chế độ `Tạo bằng AI` qua ô `Instruction` kèm hộp thoại `Chọn tài nguyên tạo Skill bằng AI`); quản lý tài liệu chuyên sâu trong tab `Docs` qua 3 nút tròn (`Create new doc` gồm 3 trường `Path`, `Phân quyền tính năng (Feature Scope)`, `Content`; `Import markdown file`; `Thêm docs có sẵn`); và thiết lập `Môi trường & Biến cấu hình (Skill Variables)` (`Active Environment` & `Biến nội bộ {{KEY}}`), kèm hướng dẫn thao tác qua trợ lý ảo AI Agent với kỹ năng `RedAI - Module - Skill`.

**Agent nên truy xuất khi:** Người dùng muốn tạo mới hoặc cập nhật một Kỹ năng (thủ công hoặc bằng AI), soạn thảo chỉ thị định tuyến `Nội dung Skill`, tạo/nhập/gắn tài liệu `Docs`, phân quyền tính năng (`Feature Scope`) cho tài liệu hoặc cài đặt biến môi trường `{{KEY}}` cho Kỹ năng.

**Không dùng khi:** Người dùng chỉ hỏi cách gắn công cụ `Tools`/`MCPs`/`Workflows`, chụp bản sao lưu `Snapshot`, xuất/nhập gói Package hoặc đồng bộ Đồ thị Tri thức `Skill Graph RAG`.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> Tạo skill mới (Tạo thường / Tạo bằng AI) → khởi tạo → Kỹ năng (Skill) & Chỉ thị định tuyến`; `<img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> Create new doc / Import markdown file / Thêm docs có sẵn → gắn tài liệu kèm Feature Scope vào → Tab Docs`; `<img src="https://api.iconify.design/lucide:braces.svg?color=%23ff3333" width="16" alt="" /> Biến môi trường → cấu hình → Active Environment & Local Variables ({{KEY}})`; `Kỹ năng RedAI - Module - Skill (57cc282f-a2d2-4dfc-9981-153fe58f7cf5) → thực thi → Bộ công cụ quản trị Skill & Docs (7534d86e-8a3c-4e74-aaec-5f0da403ec41)`.

**Tags (10):** `skills/tao-skill-moi`, `skills/tao-bang-ai`, `skills/noi-dung-skill`, `skills/quan-ly-docs`, `skills/import-markdown`, `skills/feature-scope-doc`, `skills/dynamic-doc-pruning`, `skills/bien-moi-truong`, `skills/skill-variables`, `skills/redai-module-skill`

---

## Module Skills - Quy trình liên kết Tools, MCPs, Workflows và phân quyền tính năng

**Tên file:** `02-quy-trinh-lien-ket-tools-mcps-workflows-va-phan-quyen-tinh-nang.md`

**Tiêu đề:** Module Skills - Quy trình liên kết Tools, MCPs, Workflows và phân quyền tính năng

**Mô tả:** Hướng dẫn quy trình tích hợp các tài nguyên thực thi vào Kỹ năng tại trang `/skills/:skillId` qua 3 tab `Tools` (lọc theo nhóm `Project Schema`, chọn cả nhóm hoặc từng công cụ), `MCPs` và `Workflows`; thiết lập `Cài đặt phân quyền tính năng (Capability Tag)` (`Dùng chung (Toàn quyền - Core)` hoặc `business.order`, `business.qr`, `business.shipping`, `business.voucher`) trên từng thẻ công cụ để kích hoạt cơ chế lọc công cụ tự động (*Dynamic Tool Pruning*); mở nhanh trang `Project Tools` gốc và cập nhật liên kết `@tools/...` vào `Nội dung Skill`, kèm hướng dẫn điều khiển qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn gắn hoặc gỡ `Tools`, `MCPs`, `Workflows` trong một Kỹ năng, muốn cài đặt mã phân quyền tính năng (`Capability Tag`) cho công cụ hoặc mở nhanh Project Schema từ thẻ công cụ.

**Không dùng khi:** Người dùng chỉ muốn tạo tài liệu `Docs`, cấu hình biến môi trường, chụp bản sao lưu `Snapshot` hoặc đồng bộ Đồ thị Tri thức.

**Thực thể và quan hệ:** `Tab Tools / MCPs / Workflows + <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> Create New → liên kết → Công cụ API, Máy chủ MCP & Quy trình tự động vào Kỹ năng`; `<img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> Cài đặt phân quyền tính năng (updateSkillToolCapability) → gán Capability Tag phục vụ → Dynamic Tool Pruning`; `<img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> Mở project tools → điều hướng tới → Trang quản lý Project Schema (/tools/projects/:id)`.

**Tags (10):** `skills/lien-ket-tools`, `skills/lien-ket-mcps`, `skills/lien-ket-workflows`, `skills/project-schema`, `skills/phan-quyen-tinh-nang`, `skills/capability-tag`, `skills/dynamic-tool-pruning`, `skills/add-skill-resources`, `skills/remove-skill-resources`, `skills/mo-project-tools`

---

## Module Skills - Quy trình sao lưu Snapshot, đóng gói Package và đồng bộ Đồ thị Tri thức

**Tên file:** `03-quy-trinh-sao-luu-snapshot-dong-goi-package-va-dong-bo-do-thi-tri-thuc.md`

**Tiêu đề:** Module Skills - Quy trình sao lưu Snapshot, đóng gói Package và đồng bộ Đồ thị Tri thức

**Mô tả:** Hướng dẫn chụp bản sao lưu trạng thái Kỹ năng qua nút `Snapshots` (trường `Tên snapshot`), tra cứu bảng 7 cột tại trang `/skills/snapshots` và khôi phục tức thì bằng thao tác `Import vào skill`; xuất gói Kỹ năng (`Export package`) và nhập gói từ tệp `.json`/`.zip` (`Import package`); trực quan hóa mạng lưới thực thể (`Kỹ năng`, `Tài liệu`, `Công cụ`, `Khái niệm`, `Quy trình`) và chạy `Đồng bộ Đồ thị tri thức Kỹ năng (Skill Graph RAG) v2.0` (`Toàn bộ tài nguyên` / `Tùy chọn tài nguyên`, `Đồng bộ gia số` / `Tái lập toàn bộ`, `Cross-resource Linking`, `Vector Embeddings 1024-dim`), kèm hướng dẫn thao tác qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn chụp bản sao lưu `Snapshot` cho Kỹ năng, khôi phục Kỹ năng từ một bản `Snapshot` cũ, xuất/nhập gói Kỹ năng (`.json`, `.zip`) hoặc mở và đồng bộ Đồ thị Tri thức (`Knowledge Graph / Skill Graph RAG v2.0`).

**Không dùng khi:** Người dùng chỉ muốn biên tập nội dung tài liệu `Docs` hoặc gắn thêm công cụ vào Kỹ năng.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> Snapshots (createSkillSnapshot) → lưu bản chụp tại → Trang Quản lý Snapshots (/skills/snapshots)`; `<img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> Import vào skill → khôi phục toàn bộ trạng thái Kỹ năng từ → Bản chụp Snapshot`; `<img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> Export package & <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> Import package → di chuyển gói Kỹ năng (.json, .zip) giữa → Các môi trường`; `<img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> Đồng bộ Đồ thị tri thức Kỹ năng v2.0 → trích xuất thực thể & tính toán Vector 1024-dim lên → Neo4j Knowledge Graph`.

**Tags (10):** `skills/tao-snapshot`, `skills/quan-ly-snapshots`, `skills/import-vao-skill`, `skills/export-package`, `skills/import-package`, `skills/do-thi-tri-thuc`, `skills/knowledge-graph`, `skills/skill-graph-rag`, `skills/dong-bo-gia-so`, `skills/vector-embeddings`

---

## Module Skills - Quản lý thư viện kỹ năng, nhân bản, phân loại thẻ và gắn kỹ năng mặc định

**Tên file:** `04-quan-ly-thu-vien-ky-nang-nhan-ban-phan-loai-the-va-gan-ky-nang-mac-dinh.md`

**Tiêu đề:** Module Skills - Quản lý thư viện kỹ năng, nhân bản, phân loại thẻ và gắn kỹ năng mặc định

**Mô tả:** Hướng dẫn tìm kiếm, lọc theo thẻ và chuyển đổi giữa các tab phân vùng (`Cá nhân`, `Hệ thống`, `Không gian riêng`, `User`, `Admin`) trên màn hình `/skills`; sử dụng thanh nút thao tác trên từng thẻ Kỹ năng (`Snapshots`, `Export package`, `Chỉnh sửa`, `Nhân bản`, `Xem Đồ thị Tri thức`, `Gắn Thẻ (Tags)`, `Chuyển quyền sở hữu`, `Bật/Tắt skill`, `Xóa`); nhân bản Kỹ năng kèm tùy chọn `Nhân bản kèm cấu hình (Tools, MCPs, Workflows)`; lọc theo `Project Schema` và gỡ hàng loạt tài nguyên trong `/skills/:skillId`; và cấu hình `Kỹ năng Mặc định (System Skills)` cho các Trợ lý Hệ thống tại `/admin/skills-config/bindings`, kèm hướng dẫn thao tác qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng cần tìm kiếm, lọc theo thẻ, nhân bản một Kỹ năng có sẵn, gắn/gỡ thẻ phân loại (Tags), xóa Kỹ năng, gỡ hàng loạt tài nguyên trong Kỹ năng hoặc cấu hình Kỹ năng mặc định cho Trợ lý Hệ thống.

**Không dùng khi:** Người dùng muốn xem quy trình chi tiết tạo mới tài liệu `Docs`, cài đặt biến môi trường hoặc đồng bộ Đồ thị Tri thức `Skill Graph RAG v2.0`.

**Thực thể và quan hệ:** `Thẻ Kỹ năng + <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> Nhân bản (duplicateSkill) → tạo bản sao Kỹ năng mới kèm → Tools, MCPs, Workflows`; `<img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> Gắn Thẻ (Tags) (updateSkillTags / detachSkillTag) → phân loại → Kỹ năng trong Thư viện`; `<img src="https://api.iconify.design/lucide:list-check.svg?color=%23ff3333" width="16" alt="" /> Chọn tất cả + <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> Delete (removeSkillResources) → gỡ hàng loạt → Tài nguyên được chọn khỏi Kỹ năng`; `Cấu hình Kỹ năng Mặc định (/admin/skills-config/bindings) → tự động trang bị System Skills cho → Trợ lý Hệ thống`.

**Tags (10):** `skills/thu-vien-ky-nang`, `skills/nhan-ban-skill`, `skills/duplicate-skill`, `skills/gan-the-tags`, `skills/danh-muc-redhub`, `skills/chuyen-quyen-so-huu`, `skills/loc-project-schema`, `skills/go-tai-nguyen`, `skills/ky-nang-mac-dinh`, `skills/default-skill-bindings`

---

## Định tuyến nhanh

| Ý định truy vấn | Tài liệu ưu tiên |
| :--- | :--- |
| Tạo Kỹ năng mới (Tạo thường hoặc Tạo bằng AI), soạn Nội dung Skill, tạo/nhập tài liệu Docs và cài đặt Biến môi trường (`Skill Variables`) | **01-quy-trinh-tao-ky-nang-soan-chi-thi-dinh-tuyen-va-quan-ly-tai-lieu-docs.md** |
| Liên kết Công cụ (`Tools`), Máy chủ `MCPs`, Quy trình `Workflows` vào Kỹ năng và cài đặt Phân quyền tính năng (`Capability Tag`) | **02-quy-trinh-lien-ket-tools-mcps-workflows-va-phan-quyen-tinh-nang.md** |
| Chụp bản sao lưu `Snapshot`, khôi phục `Import vào skill`, xuất/nhập gói `.json`/`.zip` và đồng bộ Đồ thị Tri thức (`Skill Graph RAG v2.0`) | **03-quy-trinh-sao-luu-snapshot-dong-goi-package-va-dong-bo-do-thi-tri-thuc.md** |
| Tìm kiếm, lọc theo thẻ, nhân bản Kỹ năng, gắn/gỡ Thẻ (Tags), gỡ hàng loạt tài nguyên và cấu hình Kỹ năng Mặc định cho Trợ lý Hệ thống | **04-quan-ly-thu-vien-ky-nang-nhan-ban-phan-loai-the-va-gan-ky-nang-mac-dinh.md** |
