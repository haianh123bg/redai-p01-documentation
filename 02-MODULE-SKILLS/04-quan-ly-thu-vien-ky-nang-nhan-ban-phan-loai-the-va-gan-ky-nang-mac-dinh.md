## Mở khu vực Thư viện Kỹ năng và Cấu hình Kỹ năng Mặc định

Để tra cứu, phân loại, nhân bản các Kỹ năng trong Workspace hoặc cấu hình danh sách Kỹ năng mặc định tự động trang bị cho các Trợ lý Hệ thống, bạn truy cập vào các đường dẫn sau:

1. **Thư viện Kỹ năng (`/skills`)**: Trung tâm quản lý toàn bộ Kỹ năng của bạn và kho Kỹ năng hệ thống.
2. **Chi tiết Kỹ năng (`/skills/:skillId`)**: Quản lý, tìm kiếm, lọc và gỡ hàng loạt các tài nguyên (`Docs`, `Tools`, `MCPs`, `Workflows`) bên trong một Kỹ năng.
3. **Cấu hình Kỹ năng Mặc định (`/admin/skills-config/bindings`)** *(Dành cho Quản trị viên Hệ thống)*: Thiết lập danh sách các Kỹ năng Hệ thống (`System Skills`) sẽ tự động gắn vào từng loại Trợ lý Hệ thống.

---

## Các tính năng

### Tìm kiếm, lọc theo thẻ và chuyển đổi phân vùng Kỹ năng

Trên màn hình **Thư viện Kỹ năng** (`/skills`), bạn có thể chuyển đổi giữa các phân vùng lưu trữ và lọc nhanh Kỹ năng thông qua thanh điều khiển:

| Thành phần giao diện | Cách sử dụng |
| :--- | :--- |
| **Các tab phân vùng Kỹ năng** | • Đối với tài khoản người dùng tiêu chuẩn: Chuyển đổi giữa 2 tab <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(Cá nhân)** (các Kỹ năng do bạn tạo hoặc nhân bản về) và <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Hệ thống)** (kho Kỹ năng mẫu do hệ thống cung cấp).<br>• Đối với tài khoản Quản trị viên: Hiển thị đầy đủ các tab <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(Hệ thống)**, <img src="https://api.iconify.design/lucide:briefcase.svg?color=%23ff3333" width="16" alt="" /> **(Không gian riêng)**, <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(User)** và <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **(Admin)**. |
| **Ô tìm kiếm Kỹ năng** (<img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" />) | Nhập tên hoặc từ khóa mô tả vào ô `Tìm kiếm skill...` trên thanh công cụ để lọc danh sách ngay lập tức. |
| **Bộ lọc theo Thẻ** (<img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo thẻ)**) | Bấm vào nút phễu lọc, nhập tên thẻ vào ô `Tìm kiếm thẻ...` và tích chọn một hoặc nhiều thẻ để lọc các Kỹ năng thuộc lĩnh vực đó (bấm **(Xóa bộ lọc)** để hiển thị lại toàn bộ). |
| **Tải lại dữ liệu** (<img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải lại dữ liệu)**) | Làm mới lại danh sách Kỹ năng trên màn hình. |

---

### Thao tác nhanh trên Thẻ Kỹ năng (Nhân bản, Gắn Thẻ, Chỉnh sửa, Chuyển quyền, Xóa)

Khi bạn di chuột vào một thẻ Kỹ năng trên màn hình `/skills`, góc dưới bên phải của thẻ sẽ hiển thị hàng nút biểu tượng thao tác trực tiếp:

| Nút biểu tượng trên Thẻ Kỹ năng | Cách thực hiện |
| :--- | :--- |
| <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Snapshots)** | Mở hộp thoại **Tạo snapshot** để chụp nhanh bản sao lưu trạng thái của Kỹ năng. |
| <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export package)** | Tải gói Kỹ năng về máy tính. |
| <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** / <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem)** | Mở hộp thoại **Cập Nhật Skill** để sửa tên, mô tả, thẻ, logo, nội dung định tuyến (hoặc xem chi tiết đối với Kỹ năng hệ thống chỉ đọc). |
| <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Nhân bản)** | Mở hộp thoại **Nhân bản Skill** để tạo một bản sao Kỹ năng mới. |
| <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **(Xem Đồ thị Tri thức (Knowledge Graph))** | Mở cửa sổ trực quan hóa và đồng bộ **Skill Graph RAG v2.0**. |
| <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Gắn Thẻ (Tags))** | Mở hộp thoại gắn hoặc gỡ các thẻ phân loại cho Kỹ năng. |
| <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa)** | Mở hộp thoại xác nhận **Xóa Kỹ năng** để xóa vĩnh viễn Kỹ năng khỏi thư viện. |
| *Các nút dành riêng cho Quản trị viên Hệ thống* | • <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:user.svg?color=%23ff3333" width="16" alt="" />: Chuyển quyền sở hữu Kỹ năng giữa cấp `System`, `Admin` và `User` (trong hộp thoại **Chuyển quyền sở hữu Kỹ năng**, bạn có thể chọn **Chuyển trực tiếp (Move)** hoặc **Tạo bản sao mới (Clone)** kèm tùy chọn chuyển cả các tài nguyên con).<br>• <img src="https://api.iconify.design/lucide:power-off.svg?color=%23ff3333" width="16" alt="" /> **(Bật skill / Tắt skill)**: Kích hoạt hoặc tạm ngưng Kỹ năng trên toàn hệ thống. |

---

### Nhân bản Kỹ năng (Duplicate Skill)

Khi bạn muốn tùy biến một Kỹ năng có sẵn (đặc biệt là các Kỹ năng mẫu trong tab **Hệ thống**) mà không làm ảnh hưởng đến bản gốc:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Nhân bản Skill** | Di chuột vào thẻ Kỹ năng muốn sao chép và bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Nhân bản)** ở góc dưới bên phải thẻ. |
| **2. Tùy chọn nhân bản kèm cấu hình tài nguyên** | Trong hộp thoại **Nhân bản Skill**, tích chọn vào ô **Nhân bản kèm cấu hình (Tools, MCPs, Workflows)** nếu bạn muốn bản sao mới giữ nguyên toàn bộ các liên kết công cụ, máy chủ MCP và quy trình của bản gốc (hoặc bỏ tích nếu chỉ muốn lấy nội dung định tuyến và tài liệu `Docs`). |
| **3. Xác nhận nhân bản** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Nhân bản ngay)**. Bản sao mới sẽ xuất hiện ngay trong tab **Cá nhân** của bạn. |

---

### Quản lý Danh mục Thẻ và Gắn Thẻ cho Kỹ năng

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Gắn hoặc gỡ Thẻ cho một Kỹ năng** | 1. Bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Gắn Thẻ (Tags))** ở góc dưới bên phải thẻ Kỹ năng.<br>2. Trong hộp thoại **Gắn Thẻ (Tags) cho Kỹ năng**:<br>   • Tab **(Kho thẻ)**: Tìm thẻ và bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gắn vào Kỹ năng)**.<br>   • Tab **(Đã gắn ({số lượng}))**: Xem các thẻ hiện tại của Kỹ năng và bấm <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Gỡ thẻ khỏi Kỹ năng)** nếu muốn bỏ bớt.<br>   • Để tạo thẻ mới và gắn luôn: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo & Gắn thẻ mới)** trên thanh công cụ của hộp thoại, điền **Tên Thẻ (Tag) \***, **Mô tả ý nghĩa** và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo và Gắn ngay)**. |
| **Quản lý Danh mục Thẻ Hệ thống** *(Chỉ hiển thị ở System Workspace)* | Bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình Danh mục RedHub (System))** trên thanh công cụ của màn hình `/skills` để thêm mới, sửa tên/mô tả hoặc xóa các thẻ phân loại chuẩn của hệ thống. |

---

### Tìm kiếm, lọc và gỡ hàng loạt tài nguyên trong Chi tiết Kỹ năng

Trên thanh công cụ phía trên của trang **Chi tiết Kỹ năng** (`/skills/:skillId`), hệ thống cung cấp bộ công cụ quản lý nhanh cho cả 4 tab (`Docs`, `Tools`, `MCPs`, `Workflows`):

| Nút công cụ trên trang Chi tiết Kỹ năng | Cách sử dụng |
| :--- | :--- |
| **Ô tìm kiếm tài nguyên** (<img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" />) | Lọc nhanh các thẻ `Docs`, `Tools`, `MCPs` hoặc `Workflows` đang hiển thị trong tab hiện tại. |
| **Bộ lọc theo Project Schema** (<img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo Project Schema)**) | Hiển thị khi bạn đang mở tab **Tools**; cho phép chọn một nhóm dự án để chỉ xem các công cụ thuộc dự án đó. |
| **Chọn tất cả / Bỏ chọn tất cả** (<img src="https://api.iconify.design/lucide:list-check.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:square.svg?color=%23ff3333" width="16" alt="" />) | Tích chọn hoặc bỏ chọn toàn bộ các thẻ tài nguyên trong tab hiện tại chỉ với một cú nhấp chuột. |
| **Gỡ tài nguyên đã chọn vs Xóa Kỹ năng** (<img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" />) | • **Khi đã tích chọn $\ge 1$ thẻ tài nguyên**: Nút thùng rác mang nhãn **(Delete)** dùng để gỡ các tài nguyên đã chọn khỏi Kỹ năng.<br>• **Khi không tích chọn thẻ tài nguyên nào**: Nút thùng rác mang nhãn **(Xóa skill)** dùng để xóa toàn bộ Kỹ năng hiện tại. |

---

### Cấu hình Kỹ năng Mặc định cho Trợ lý Hệ thống (Default Skill Bindings)

Đối với Quản trị viên Hệ thống tại đường dẫn `/admin/skills-config/bindings`, màn hình **Cấu hình Kỹ năng Mặc định (System Skills)** giúp quy định những Kỹ năng nào sẽ luôn được gắn sẵn cho từng loại Trợ lý AI của nền tảng:

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Chọn loại Trợ lý Hệ thống** | Quan sát 2 thẻ chỉ số tổng quan (**Loại Trợ lý Hệ thống** và **Tổng Liên kết Đang Bật**), sau đó nhấp chọn một loại trợ lý tại cột bên trái **Danh sách Trợ lý Hệ thống**. |
| **Gắn thêm Kỹ năng mặc định** | Tại cột bên phải **Kỹ năng được gắn**, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gắn thêm Kỹ năng)**, tìm và chọn một Kỹ năng Hệ thống trong hộp thoại **Gắn Kỹ năng Mặc định mới**, sau đó bấm **(Gắn Kỹ năng)**. |
| **Bật/tắt hoặc gỡ liên kết Kỹ năng mặc định** | Trên từng dòng Kỹ năng đã gắn ở cột bên phải, gạt công tắc để bật/tắt trạng thái kích hoạt hoặc bấm biểu tượng <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> để gỡ Kỹ năng đó khỏi Trợ lý Hệ thống. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Toàn bộ các tính năng tra cứu thư viện Kỹ năng, nhân bản Kỹ năng, gắn/gỡ thẻ phân loại (Tags) và gỡ bớt tài nguyên khỏi Kỹ năng đều có thể giao cho trợ lý ảo AI Agent thực hiện.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Skill` (ID: `57cc282f-a2d2-4dfc-9981-153fe58f7cf5`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - Skill` (ID: `7534d86e-8a3c-4e74-aaec-5f0da403ec41`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản lý Kỹ năng trong Workspace.

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Tìm kiếm và liệt kê danh sách Kỹ năng trong Thư viện

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Tìm kiếm và lọc trên màn hình **Thư viện Kỹ năng** (`/skills`) |
| **Công cụ Agent sử dụng** | `getSkills`, `getSkillDetail` |
| **Thông tin cần cung cấp** | Từ khóa tìm kiếm, thẻ phân loại hoặc mã định danh `skillId` |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ getSkills để liệt kê danh sách tất cả các Kỹ năng hiện có trong thư viện của tôi, sau đó dùng getSkillDetail để xem thông tin chi tiết của Kỹ năng "[Tên Skill hoặc skillId]".
```

#### 2. Nhân bản một Kỹ năng có sẵn (Duplicate Skill)

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Nhân bản)** trên thẻ Kỹ năng và chọn **Nhân bản ngay** |
| **Công cụ Agent sử dụng** | `duplicateSkill` |
| **Thông tin cần cung cấp** | Mã định danh `skillId` của Kỹ năng gốc cần nhân bản |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ duplicateSkill để nhân bản Kỹ năng có ID "[Điền skillId gốc]" thành một bản sao mới trong Workspace của tôi để tôi tùy biến riêng.
```

#### 3. Gắn thêm hoặc gỡ Thẻ phân loại (Tags) cho Kỹ năng

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm nút <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **(Gắn Thẻ (Tags))** trên thẻ Kỹ năng để cập nhật hoặc gỡ thẻ |
| **Công cụ Agent sử dụng** | `updateSkillTags`, `detachSkillTag` |
| **Thông tin cần cung cấp** | Mã định danh `skillId` và danh sách tên thẻ/ID thẻ cần gắn hoặc cần gỡ |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ updateSkillTags để gắn các thẻ ["ban-le", "don-hang", "vietqr"] cho Kỹ năng có ID "[Điền skillId]", và dùng detachSkillTag nếu cần gỡ thẻ cũ không còn phù hợp.
```

#### 4. Gỡ hàng loạt tài nguyên không còn sử dụng khỏi Kỹ năng

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Tích chọn các thẻ tài nguyên trong trang `/skills/:skillId` và bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Delete)** |
| **Công cụ Agent sử dụng** | `removeSkillResources` |
| **Thông tin cần cung cấp** | Mã định danh `skillId` và danh sách `toolIds`, `mcpIds`, `workflowIds` hoặc `docIds` cần gỡ khỏi Kỹ năng |

**Câu lệnh mẫu (Prompt):**

```text
Hãy kiểm tra danh sách công cụ của Kỹ năng "[Điền skillId]" bằng getSkillTools, sau đó dùng công cụ removeSkillResources để gỡ các công cụ có ID ["[toolId_cu_1]", "[toolId_cu_2]"] ra khỏi Kỹ năng này.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Tải lại dữ liệu)** trên màn hình `/skills` hoặc `/skills/:skillId` để kiểm tra bản sao Kỹ năng mới, các thẻ (Tags) vừa gắn và danh sách tài nguyên sau khi thu gọn. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getSkillDetail` và `getSkillTools` để hiển thị lại thông tin thẻ (Tags) cùng danh sách tài nguyên hiện tại của Kỹ năng."* |
