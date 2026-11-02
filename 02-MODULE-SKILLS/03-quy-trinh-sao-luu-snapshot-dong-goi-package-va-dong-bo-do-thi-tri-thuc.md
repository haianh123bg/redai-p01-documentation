## Mở khu vực Quản lý Snapshots, Đóng gói Package và Đồ thị Tri thức

Để sao lưu trạng thái Kỹ năng trước khi chỉnh sửa lớn, di chuyển Kỹ năng giữa các môi trường (Staging / Production) hoặc đồng bộ tri thức lên hệ thống **Đồ thị Tri thức (Knowledge Graph / Skill Graph RAG v2.0)**, bạn sử dụng các nút công cụ tại hai màn hình sau:

1. **Tại màn hình Thư viện Kỹ năng (`/skills`)**:
   - **Trên thanh công cụ phía trên (`MenuIconBar`)**:
     - Nút <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý snapshots)**: Chuyển sang trang quản lý tập trung toàn bộ bản chụp trạng thái (`/skills/snapshots`).
     - Nút <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import package)**: Nhập gói Kỹ năng từ tệp `.json` hoặc `.zip` trên máy tính.
   - **Trên thanh nút thao tác góc dưới bên phải của từng Thẻ Kỹ năng (hiển thị khi di chuột vào thẻ)**:
     - Nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Snapshots)**: Mở hộp thoại chụp nhanh trạng thái hiện tại của Kỹ năng đó.
     - Nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export package)**: Tải gói Kỹ năng về máy tính.
     - Nút <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **(Xem Đồ thị Tri thức (Knowledge Graph))**: Mở cửa sổ trực quan hóa và đồng bộ Đồ thị Tri thức của Kỹ năng.
2. **Tại thanh công cụ của trang Chi tiết Kỹ năng (`/skills/:skillId`)**:
   - Cũng tích hợp sẵn nút <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **(Xem Đồ thị Tri thức (Knowledge Graph))** và nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export package)** để bạn thao tác ngay trong lúc đang biên tập Kỹ năng.

---

## Các bước thực hiện

### Chọn công cụ sao lưu, di chuyển hoặc đồng bộ tri thức phù hợp

| Công cụ | Khi nào nên sử dụng | Kết quả nhận được |
| :--- | :--- | :--- |
| **Chụp trạng thái (`Snapshot`)** (<img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" />) | Khi bạn chuẩn bị thay đổi cấu trúc định tuyến, chỉnh sửa nhiều tài liệu `Docs` hoặc cập nhật bằng AI và muốn có một mốc lưu trữ ngay trên máy chủ để khôi phục lại bất cứ lúc nào. | Lưu trữ một bản chụp tức thời trên hệ thống, hiển thị trong trang `/skills/snapshots` kèm dung lượng, ngày tạo và cho phép **Import vào skill** chỉ với 1 cú nhấp chuột. |
| **Đóng gói & Nhập gói (`Export / Import package`)** (<img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" />) | Khi bạn muốn tải toàn bộ Kỹ năng về máy tính để lưu trữ ngoại tuyến hoặc chuyển Kỹ năng từ môi trường thử nghiệm sang môi trường vận hành chính thức. | Xuất ra tệp gói Kỹ năng hoặc khôi phục từ tệp `.json` / `.zip` vào Workspace đích. |
| **Đồ thị Tri thức (`Skill Graph RAG v2.0`)** (<img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" />) | Sau khi bạn thêm mới hoặc cập nhật các tài liệu `Docs`, `Tools`, `Workflows` và muốn hệ thống AI Agent truy xuất ngữ nghĩa chính xác qua mạng lưới thực thể và Vector Embeddings. | Trích xuất các nút (`Kỹ năng`, `Tài liệu`, `Công cụ`, `Khái niệm`, `Quy trình`), thiết lập liên kết đa tài nguyên và tính toán Vector 1024 chiều. |

---

### Giai đoạn 1 — Tạo bản chụp trạng thái (Snapshot) và khôi phục vào Kỹ năng

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Tạo bản chụp trạng thái mới (`Tạo snapshot`)** | 1. Tại màn hình `/skills`, di chuột vào thẻ của Kỹ năng cần sao lưu và bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Snapshots)** ở góc dưới bên phải thẻ.<br>2. Trong hộp thoại **Tạo snapshot**, hệ thống tự động điền sẵn trường duy nhất **Tên snapshot** theo định dạng `{Tên Skill} - YYYY-MM-DD HH:mm` (bạn có thể sửa lại tên gợi nhớ nếu muốn).<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận)** để hoàn tất chụp trạng thái. |
| **2. Tra cứu danh sách tại trang Quản lý Snapshots** | Bấm nút <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý snapshots)** trên thanh công cụ của màn hình `/skills` để mở trang `/skills/snapshots`. Tại đây bạn có thể:<br>• Tìm kiếm theo tên tại ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm...)** hoặc bấm nút <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> để lọc các bản chụp của một Kỹ năng cụ thể.<br>• Theo dõi bảng danh sách gồm 7 cột: Ô tích chọn, **Snapshot** (tên & mã ID), **Skill** (bấm vào tên để mở Kỹ năng gốc), **Nguồn**, **Dung lượng**, **Ngày tạo** và **Actions**. |
| **3. Khôi phục từ Snapshot (`Import vào skill`) hoặc xóa bản cũ** | • **Để khôi phục**: Tại cột **Actions** ở cuối dòng bản chụp muốn dùng, bấm vào biểu tượng <img src="https://api.iconify.design/lucide:ellipsis-vertical.svg?color=%23ff3333" width="16" alt="" /> và chọn <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import vào skill)**. Hệ thống sẽ ngay lập tức khôi phục dữ liệu từ bản chụp đó và tự động chuyển hướng bạn tới trang Chi tiết Kỹ năng vừa khôi phục.<br>• **Để xóa các bản chụp cũ**: Tích chọn vào ô vuông đầu dòng của các bản chụp cần dọn dẹp, sau đó bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xóa các mục đã chọn)** trên thanh công cụ. |

---

### Giai đoạn 2 — Xuất gói (Export package) và Nhập gói (Import package)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Xuất gói Kỹ năng về máy tính (`Export package`)** | Di chuột vào thẻ Kỹ năng trên màn hình `/skills` (hoặc mở trang Chi tiết Kỹ năng `/skills/:skillId`) rồi bấm vào nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Export package)**. Trình duyệt sẽ tự động tải tệp đóng gói của Kỹ năng về máy tính của bạn. |
| **2. Nhập gói Kỹ năng từ máy tính (`Import package`)** | Tại thanh công cụ phía trên của màn hình **Thư viện Kỹ năng** (`/skills`), bấm nút <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Import package)**, sau đó chọn tệp `.json` hoặc `.zip` từ máy tính. Hệ thống sẽ tự động đọc cấu trúc gói, khởi tạo Kỹ năng cùng các tài liệu đi kèm và làm mới lại danh sách. |

---

### Giai đoạn 3 — Trực quan hóa và Đồng bộ Đồ thị Tri thức Kỹ năng (Skill Graph RAG v2.0)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở cửa sổ Đồ thị tri thức Kỹ năng** | Bấm vào nút <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **(Xem Đồ thị Tri thức (Knowledge Graph))** trên thẻ Kỹ năng hoặc trên thanh công cụ của trang Chi tiết Kỹ năng. |
| **2. Khám phá và tra cứu các thực thể trên Đồ thị** | Trong cửa sổ **Đồ thị tri thức Kỹ năng**:<br>• Sử dụng ô tìm kiếm `Tìm kiếm node...` hoặc các nút lọc loại thực thể: **(Tất cả)**, **(Kỹ năng)**, **(Tài liệu)**, **(Công cụ)**, **(Khái niệm)**, **(Quy trình)**.<br>• Nhấp vào một nút (node) bất kỳ trên đồ thị để xem thông tin chi tiết, các mối quan hệ định tuyến và thuộc tính ở bảng bên phải (có thể bấm <img src="https://api.iconify.design/lucide:maximize-2.svg?color=%23ff3333" width="16" alt="" /> để mở rộng toàn màn hình hoặc <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> để làm mới đồ thị). |
| **3. Cấu hình và chạy Đồng bộ Đồ thị Tri thức v2.0** | Khi bạn vừa chỉnh sửa tài liệu hoặc gắn thêm công cụ mới, bấm nút **(Đồng bộ)** trên thanh tiêu đề của cửa sổ đồ thị để mở hộp thoại **Đồng bộ Đồ thị tri thức Kỹ năng (Skill Graph RAG) v2.0** và thiết lập 3 mục:<br>1. **Phạm vi tài nguyên:**: Chọn **(Toàn bộ tài nguyên)** (`Đồng bộ tất cả Docs, Tools, Workflows`) hoặc chọn **(Tùy chọn tài nguyên)** để tích chọn riêng từng mục cần cập nhật.<br>2. **Chế độ đồng bộ:**: Chọn **(Đồng bộ gia số)** (`Incremental - Chỉ xử lý phần thay đổi`, khuyên dùng để tối ưu tốc độ) hoặc chọn **(Tái lập toàn bộ)** (`Full Rebuild - Xóa graph cũ & dựng lại`).<br>3. **Tùy chọn nâng cao**: Tích chọn **Lập luận liên kết đa tài nguyên (Cross-resource Linking)** và **Tính toán Vector Embeddings 1024-dim**.<br>• Bấm nút **(Bắt đầu đồng bộ)** và theo dõi tiến trình 5 bước (`Khởi tạo phiên đồng bộ` $\rightarrow$ `Phân tích cấu trúc SKILL.md & Docs` $\rightarrow$ `Trích xuất thực thể & liên kết công cụ` $\rightarrow$ `Tính toán Vector Embeddings` $\rightarrow$ `Cập nhật Neo4j Knowledge Graph`) cho đến khi báo hoàn tất 100%. |

---

## Kiểm tra kết quả

1. **Tại trang Quản lý Snapshots (`/skills/snapshots`)**: Bản chụp vừa tạo xuất hiện ở dòng đầu tiên của bảng với đầy đủ thông tin dung lượng (KB), thời gian tạo và nút hành động **Import vào skill**.
2. **Tại cửa sổ Đồ thị tri thức Kỹ năng**: Sơ đồ mạng lưới hiển thị đầy đủ nút trung tâm **Kỹ năng** nối tới các nút **Tài liệu**, **Công cụ**, **Quy trình** và **Khái niệm** vừa được đồng bộ.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động chụp bản sao lưu trạng thái (`createSkillSnapshot`) trước khi chỉnh sửa Kỹ năng hoặc kiểm tra thông tin Kỹ năng sau khi khôi phục.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Skill` (ID: `57cc282f-a2d2-4dfc-9981-153fe58f7cf5`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - Skill` (ID: `7534d86e-8a3c-4e74-aaec-5f0da403ec41`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản lý Kỹ năng và Snapshots trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Snapshots)** trên thẻ Kỹ năng và bấm **Xác nhận** | `createSkillSnapshot` | Chụp và lưu trữ một bản sao lưu trạng thái toàn diện của Kỹ năng tại thời điểm hiện tại. |
| Kiểm tra thông tin chi tiết Kỹ năng và tài nguyên trước/sau khi sao lưu | `getSkillDetail`, `getSkillDocs`, `getSkillTools`, `getSkillMcps`, `getSkillWorkflows` | Đọc toàn bộ cấu trúc định tuyến và danh sách tài nguyên thành phần của Kỹ năng. |
| Nhân bản Kỹ năng để tạo bản sao thử nghiệm độc lập | `duplicateSkill` | Tạo một bản sao Kỹ năng mới từ Kỹ năng hiện có trong Workspace. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi chụp một bản sao lưu trạng thái (Snapshot) an toàn trước khi cập nhật nội dung cho Kỹ năng:

1. Bối cảnh và Mục tiêu:
- Tôi chuẩn bị nâng cấp nội dung định tuyến và tài liệu cho Kỹ năng hiện tại nên cần tạo một bản Snapshot để có thể khôi phục ngay nếu cần.

2. Dữ liệu cung cấp:
- ID Kỹ năng (skillId): "[Điền ID Kỹ năng của bạn]"
- Tên bản chụp (Snapshot Name): "Sao lưu trước khi nâng cấp v2.0"

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng getSkillDetail để kiểm tra thông tin hiện tại của Kỹ năng.
- Bước 2: Dùng công cụ createSkillSnapshot để tạo bản chụp trạng thái mới cho Kỹ năng với tên "Sao lưu trước khi nâng cấp v2.0".

4. Yêu cầu phản hồi:
- Báo cáo lại ID của bản chụp Snapshot vừa tạo, tên bản chụp và thời gian khởi tạo thành công.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Truy cập `/skills/snapshots` (hoặc bấm nút <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý snapshots)** tại `/skills`) để kiểm tra bản chụp **Sao lưu trước khi nâng cấp v2.0** đã xuất hiện trên bảng danh sách. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy xác nhận lại trạng thái chi tiết của Kỹ năng bằng công cụ `getSkillDetail`."* |
