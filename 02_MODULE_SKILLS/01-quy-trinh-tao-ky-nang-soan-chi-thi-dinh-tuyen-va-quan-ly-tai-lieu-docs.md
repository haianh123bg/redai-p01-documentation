## Mở khu vực Thư viện Kỹ năng và Chi tiết Kỹ năng

Để khởi tạo một Kỹ năng (Skill) mới cho trợ lý ảo AI Agent, biên soạn chỉ thị định tuyến (`Nội dung Skill`), xây dựng kho tài liệu chuyên sâu (`Docs`) và cấu hình biến môi trường (`Skill Variables`), bạn truy cập vào hai màn hình sau:

1. **Thư viện Kỹ năng (`/skills`)**: Chọn mục **Skills** trên thanh điều hướng bên trái. Màn hình bao gồm:
   - **Các tab phân vùng Kỹ năng**: Người dùng tiêu chuẩn có 2 tab <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(Cá nhân)** và <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Hệ thống)** (Tài khoản Quản trị viên có các tab <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Hệ thống)**, <img src="https://api.iconify.design/lucide:briefcase.svg?color=%23ff3333" width="16" alt="" /> **(Không gian riêng)**, <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(User)** và <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **(Admin)**).
   - **Thanh công cụ phía trên (`MenuIconBar`)**: Ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm skill...)**, nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo skill mới)**, nút <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo thẻ)**, nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải lại dữ liệu)**, nút <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý snapshots)** và nút <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import package)**.
2. **Chi tiết Kỹ năng (`/skills/:skillId`)**: Nhấp trực tiếp vào một thẻ Kỹ năng trên danh sách để mở trang chi tiết. Tại đây bao gồm:
   - **Thẻ tổng quan Kỹ năng (Overview Card)**: Hiển thị Logo, Tên Skill, Mô tả, các thẻ (Tags) và nút <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** để mở hộp thoại **Cập Nhật Skill**.
   - **4 tab tài nguyên thành phần**: <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Docs)**, <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)**, <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(MCPs)** và <img src="https://api.iconify.design/lucide:workflow.svg?color=%23ff3333" width="16" alt="" /> **(Workflows)**.

---

## Các bước thực hiện

### Chọn chế độ khởi tạo Kỹ năng phù hợp

Khi bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo skill mới)**, hộp thoại **Tạo Skill Mới** cho phép bạn chuyển đổi giữa 2 chế độ khởi tạo:

| Chế độ khởi tạo | Khi nào nên sử dụng | Cách hoạt động |
| :--- | :--- | :--- |
| **Chế độ 1 — Tạo thường (Thủ công)** (<img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" />) | Khi bạn đã có sẵn nội dung chỉ thị định tuyến (`Nội dung Skill`) hoặc muốn tự biên tập từng mục tên, mô tả, thẻ, logo và nội dung Markdown. | Bạn điền trực tiếp 5 trường thông tin trên biểu mẫu và sử dụng phím tắt `@` để chèn liên kết tài liệu/công cụ vào nội dung Skill. |
| **Chế độ 2 — Tạo bằng AI** (<img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" />) | Khi bạn muốn hệ thống AI tự động phân tích danh sách `Tools`, `MCPs`, `Workflows` được chọn và tự sinh ra cấu trúc Kỹ năng kèm các tài liệu hướng dẫn chuẩn. | Bạn chỉ cần mô tả yêu cầu tại ô `Instruction` và chọn các tài nguyên liên quan, hệ thống sẽ tự động khởi tạo và biên soạn Kỹ năng trong nền. |

---

### Giai đoạn 1 — Khởi tạo Kỹ năng mới

#### Phương án 1 — Tạo thường (Chế độ Thủ công)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Tạo Skill Mới** | Tại màn hình **Thư viện Kỹ năng** (`/skills`), bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo skill mới)** trên thanh công cụ và giữ nguyên ở tab <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo thường)**. |
| **2. Điền 5 trường thông tin của Kỹ năng** | Điền đầy đủ các trường hiển thị trên hộp thoại:<br>1. **Tên Skill**: Nhập tên kỹ năng (ví dụ: `Quản lý Đơn hàng & Kho vận`).<br>2. **Mô tả**: Nhập mô tả tóm tắt nhiệm vụ của kỹ năng để AI Agent nhận diện ngữ cảnh kích hoạt.<br>3. **Thẻ / Tags**: Nhấp vào ô `Chọn các thẻ phù hợp cho skill` để gắn một hoặc nhiều thẻ phân loại.<br>4. **Logo**: Bấm vào vùng <img src="https://api.iconify.design/lucide:image.svg?color=%23ff3333" width="16" alt="" /> **(Tải logo từ máy)** để chọn ảnh biểu tượng từ máy tính (sau khi tải lên có thể bấm **Đổi logo** hoặc **Xóa**).<br>5. **Nội dung Skill**: Nhập nội dung chỉ thị định tuyến Markdown tại trình soạn thảo (sử dụng thanh công cụ định dạng `Bold`, `Italic`, `Heading`, `List`, `Code`, `Link`, `Quote`, nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Preview**, hoặc gõ ký tự **`@`** để mở danh sách gợi ý chèn nhanh đường dẫn `docs/...`, `tools/...`). |
| **3. Lưu khởi tạo Kỹ năng** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Skill)** ở góc dưới bên phải hộp thoại (khi chỉnh sửa kỹ năng đã có qua nút <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)**, nút xác nhận sẽ là <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu thay đổi)**). |

#### Phương án 2 — Tạo bằng AI (Chế độ Tự động)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Chuyển sang chế độ Tạo bằng AI** | Trong hộp thoại **Tạo Skill Mới**, bấm chọn tab <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Tạo bằng AI)** (hoặc <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Cập nhật bằng AI)** khi đang mở hộp thoại cập nhật). |
| **2. Nhập yêu cầu tại ô Instruction** | Tại trường **Instruction**, mô tả chi tiết mục tiêu nghiệp vụ, quy trình xử lý và các quy tắc bạn muốn AI Agent tuân thủ (tối đa `5000` ký tự). |
| **3. Chọn tài nguyên đầu vào cho AI** | Bấm vào nút **Chọn tài nguyên** (`Chọn tools, MCPs, workflows` <img src="https://api.iconify.design/lucide:chevron-right.svg?color=%23ff3333" width="16" alt="" />) để mở hộp thoại **Chọn tài nguyên tạo Skill bằng AI**:<br>• Lần lượt duyệt qua 3 tab **(Tools)**, **(MCPs)**, **(Workflows)**.<br>• Sử dụng bộ lọc nguồn (`Của tôi`, `Hệ thống`), lọc theo nhóm `Project Schema` ở cột trái và tích chọn các công cụ/quy trình ở cột phải.<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận ({tổng số đã chọn}))**. |
| **4. Kích hoạt tiến trình sinh Kỹ năng** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo bằng AI)** ở góc dưới bên phải. Hệ thống sẽ xử lý trong nền và hiển thị thông báo ngay khi Kỹ năng cùng bộ tài liệu được tạo xong. |

---

### Giai đoạn 2 — Biên soạn tài liệu hướng dẫn chuyên sâu trong tab Docs

Tại trang **Chi tiết Kỹ năng** (`/skills/:skillId`), tab <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Docs)** hiển thị thẻ đầu tiên **Create New** với 3 nút tròn tương ứng 3 cách thêm tài liệu:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Tạo tài liệu mới trực tiếp (`Create new doc`)** | Bấm vào nút tròn ở dưới <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create new doc)** trên thẻ đầu tiên để mở hộp thoại **Create Doc**, sau đó điền 3 trường:<br>1. **Path**: Nhập đường dẫn định danh của tài liệu (mặc định là `docs/template.md`, ví dụ: `docs/lanes/order-workflow.md`).<br>2. **Phân quyền tính năng (Feature Scope)**: Để trống hoặc bấm chip **(Dùng chung (Toàn quyền))** nếu tài liệu luôn được phép đọc; hoặc nhập/bấm chọn nhanh các chip mã quyền như `business.order`, `business.qr`, `business.shipping`, `business.voucher` để chỉ cho phép nạp tài liệu khi ứng dụng bật tính năng tương ứng (có thể bấm nút **`?`** bên cạnh để xem hướng dẫn cơ chế *Dynamic Doc Pruning*).<br>3. **Content**: Soạn thảo nội dung Markdown chi tiết (hỗ trợ gõ **`@`** để chèn tham chiếu tài nguyên khác trong Skill).<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Save)** để lưu tài liệu. |
| **2. Tải tệp Markdown từ máy tính (`Import markdown file`)** | Bấm vào nút tròn bên trái <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import markdown file)** trên thẻ đầu tiên, sau đó chọn một hoặc nhiều tệp `.md`, `.markdown`, `.txt` từ máy tính. Hệ thống sẽ tự động tạo các thẻ tài liệu tương ứng với tên tệp. |
| **3. Gắn tài liệu từ kho có sẵn (`Thêm docs có sẵn`)** | Bấm vào nút tròn bên phải <img src="https://api.iconify.design/lucide:folder-plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm docs có sẵn)** để mở hộp thoại **Thêm tài liệu có sẵn vào kỹ năng**, tìm kiếm theo đường dẫn hoặc nội dung, tích chọn các tài liệu cần dùng rồi bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Gắn {số lượng} tài liệu)**. |
| **4. Chỉnh sửa hoặc xóa tài liệu Docs** | • Để chỉnh sửa một tài liệu: Bấm vào biểu tượng <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> trên góc thẻ tài liệu đó để mở hộp thoại **Edit Doc**.<br>• Để xóa một hoặc nhiều tài liệu: Tích vào ô vuông trên góc các thẻ tài liệu cần xóa, sau đó bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Delete)** trên thanh công cụ phía trên. |

---

### Giai đoạn 3 — Thiết lập Môi trường & Biến cấu hình (Skill Variables)

Khi các tài liệu hướng dẫn hoặc công cụ trong Kỹ năng cần sử dụng các biến động (như `{{STORE_ID}}`, `{{API_KEY}}`, `{{WEBHOOK_URL}}`), bạn thiết lập tại hộp thoại **Biến môi trường**:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Biến môi trường** | Trên thanh công cụ phía trên của trang **Chi tiết Kỹ năng** (`/skills/:skillId`), bấm vào nút <img src="https://api.iconify.design/lucide:braces.svg?color=%23ff3333" width="16" alt="" /> **(Biến môi trường)**. |
| **2. Chọn Môi trường Kích hoạt (Active Environment)** | Tại phần **1. Lựa chọn Môi trường Kích hoạt (Active Environment)**:<br>• Chọn một môi trường dùng chung của Workspace trong danh sách thả xuống (hoặc chọn `-- Không sử dụng (Chỉ dùng biến nội bộ của App) --`).<br>• Bấm nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> bên cạnh nếu muốn mở cửa sổ quản lý môi trường chung của Workspace. |
| **3. Khai báo Biến nội bộ & Ghi đè cục bộ của Skill** | Tại phần **2. Biến nội bộ & Ghi đè cục bộ của Skill (Local Variables / Overrides)**:<br>• Bạn có thể chuyển đổi linh hoạt giữa chế độ xem **Bảng ({số lượng})** và chế độ soạn thảo **JSON**.<br>• Ở chế độ **Bảng**: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm biến)** (hoặc **Thêm dòng biến mới**), sau đó điền cột **TÊN BIẾN (KEY)** và cột **GIÁ TRỊ (VALUE)**.<br>• Tại cột **BẢO MẬT**: Bấm biểu tượng <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> để đánh dấu biến bí mật (giá trị sẽ được ẩn bằng dấu chấm tròn và có nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="16" alt="" /> để hiện/ẩn) hoặc <img src="https://api.iconify.design/lucide:unlock.svg?color=%23ff3333" width="16" alt="" /> cho biến thông thường.<br>• Tại cột **THAO TÁC** (hoặc dãy chip phía trên bảng): Bấm vào chip `{{KEY}}` hoặc nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> để sao chép nhanh cú pháp biến, hoặc bấm <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> để xóa dòng biến. |
| **4. Lưu cấu hình biến** | Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cấu hình)** ở góc dưới bên phải hộp thoại. |

---

## Kiểm tra kết quả

1. **Tại Thẻ tổng quan Kỹ năng (`/skills/:skillId`)**: Hiển thị đúng **Tên Skill**, **Mô tả**, **Logo** và các **Thẻ / Tags** đã chọn; khi bấm <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** và bật chế độ <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Preview**, nội dung định tuyến hiển thị rõ ràng cùng các liên kết `docs/...` hợp lệ.
2. **Tại tab Docs**: Các thẻ tài liệu mới hiển thị đầy đủ đường dẫn `path`, nhãn phân quyền tính năng (`Dùng chung (Toàn quyền)` hoặc `Quyền: {mã quyền}`) và đoạn xem trước nội dung Markdown.
3. **Tại hộp thoại Biến môi trường**: Các biến nội bộ và biến bí mật được lưu trữ chính xác, cho phép sao chép nhanh cú pháp `{{KEY}}` để dán vào tài liệu hoặc cấu hình công cụ.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động lấy mẫu chuẩn (`Skill Template`), khởi tạo Kỹ năng mới, biên soạn chỉ thị định tuyến `SKILL.md` và tạo trọn bộ tài liệu `Docs` thông qua bộ công cụ quản trị Kỹ năng.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Skill` (ID: `57cc282f-a2d2-4dfc-9981-153fe58f7cf5`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - Skill` (ID: `7534d86e-8a3c-4e74-aaec-5f0da403ec41`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền tạo và quản lý Kỹ năng trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Lấy mẫu cấu trúc chuẩn và phân loại trước khi tạo Kỹ năng | `getSkillTemplate`, `getSkillTypes` | Lấy khung mẫu `skillBody` chuẩn kiến trúc Router-First và danh sách loại Kỹ năng trên hệ thống. |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo skill mới)** và điền Tên, Mô tả, Thẻ, Nội dung Skill | `createSkill` | Khởi tạo một Kỹ năng mới với tên, mô tả, nội dung định tuyến (`skillBody`) và danh sách thẻ. |
| Bấm <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** để cập nhật thông tin và Nội dung Skill | `updateSkill`, `getSkillDetail` | Lấy thông tin chi tiết hiện tại và cập nhật tên, mô tả, nội dung định tuyến của Kỹ năng. |
| Mở tab <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Docs)** để xem danh sách và chi tiết từng tài liệu | `getSkillDocs`, `getDocs`, `getDocDetail` | Liệt kê tất cả các tài liệu đang gắn trong Kỹ năng, tìm kiếm kho Docs và đọc toàn문 nội dung một tài liệu. |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create new doc)** hoặc <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> để tạo/sửa tài liệu | `createDoc`, `updateDoc` | Tạo mới hoặc cập nhật tài liệu `Docs` với `path`, `content` và mã phân quyền `capability` (Feature Scope). |
| Tích chọn tài liệu và bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Delete)** | `deleteDocs` | Xóa một hoặc nhiều tài liệu khỏi hệ thống. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi khởi tạo một Kỹ năng (Skill) mới kèm bộ tài liệu hướng dẫn (Docs) theo quy trình chuẩn:

1. Bối cảnh và Mục tiêu:
- Tôi cần tạo một Kỹ năng mới theo kiến trúc Progressive Disclosure (Router-First) để hướng dẫn AI Agent xử lý quy trình chăm sóc khách hàng và tra cứu đơn hàng.

2. Dữ liệu cung cấp:
- Tên Skill: "Trợ Lý Chăm Sóc Khách Hàng & Tra Cứu Đơn"
- Mô tả: "Kỹ năng định tuyến xử lý câu hỏi thường gặp, kiểm tra trạng thái đơn hàng và hỗ trợ đổi trả cho khách hàng."
- Danh sách tài liệu Docs cần tạo:
  + docs/overview/fast-routes.md (Phân quyền: Dùng chung / để trống capability)
  + docs/lanes/order-lookup.md (Phân quyền capability: "business.order")

3. Các bước yêu cầu thực hiện:
- Bước 1: Gọi getSkillTemplate để lấy khung cấu trúc chuẩn của một Skill trên RedAI.
- Bước 2: Gọi createSkill để tạo Kỹ năng mới với Tên và Mô tả trên.
- Bước 3: Gọi createDoc để tạo 2 tài liệu "docs/overview/fast-routes.md" và "docs/lanes/order-lookup.md" và gắn vào Kỹ năng vừa tạo.
- Bước 4: Gọi updateSkill để cập nhật lại Nội dung Skill (skillBody) trỏ chính xác tới 2 đường dẫn docs vừa tạo.

4. Yêu cầu phản hồi:
- Báo cáo lại ID của Kỹ năng (skillId), danh sách các tài liệu Docs đã tạo kèm ID và hiển thị nội dung định tuyến đã cập nhật.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Truy cập `/skills`, nhấp vào thẻ Kỹ năng **Trợ Lý Chăm Sóc Khách Hàng & Tra Cứu Đơn** vừa tạo để kiểm tra các thẻ tài liệu trong tab <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Docs)** và bấm <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** để xem nội dung định tuyến. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getSkillDetail` và `getSkillDocs` cho Kỹ năng vừa tạo để xác nhận toàn bộ tài liệu và nội dung định tuyến đã khớp 100%."* |
