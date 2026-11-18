## Tổng quan các tính năng Quản trị nâng cao

Bên cạnh các thao tác bảng tính và dạng xem thông thường, **RedAI Database** cung cấp một hệ thống công cụ quản trị cấp cao toàn diện nhằm phục vụ kiến trúc dữ liệu liên kết phức tạp, tự động hóa quy trình thời gian thực và bảo mật dữ liệu nhiều tầng. Người dùng truy cập các tính năng này trực tiếp từ menu ngữ cảnh ba chấm <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> trên từng dòng bảng dữ liệu:

| Tính năng quản trị | Lệnh menu tương ứng | Phạm vi & Nghiệp vụ giải quyết |
| :--- | :--- | :--- |
| **1. Sơ đồ Quan hệ bảng (Relations ERD)** | <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **Quan hệ** | Mở canvas tương tác trực quan `Trang chủ > Database > Quan hệ`, thể hiện toàn bộ lược đồ liên kết giữa các bảng, khóa chính (PK), khóa ngoại (FK) và kéo thả tạo dây nối quan hệ. |
| **2. Phân quyền cấp Bảng (Table Permissions)** | <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Quyền bảng** | Mở ngăn kéo kiểm soát 9 phạm vi quyền thao tác: xem bảng, sửa schema, xóa bảng, đọc/thêm/sửa/xóa bản ghi, xuất dữ liệu và chia sẻ view. |
| **3. Phân quyền cấp Cột (Field Permissions)** | <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> **Quyền trường** | Mở ngăn kéo thiết lập quyền xem và quyền sửa riêng biệt cho từng cột dữ liệu nhạy cảm trong bảng. |
| **4. Bảo mật cấp Bản ghi (Row-level Security)** | <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> **Bảo mật cấp bản ghi** | Thiết lập quy tắc phân quyền Xem, Xuất, Sửa, Xóa bản ghi theo vai trò, người dùng cụ thể và bộ lọc điều kiện. |
| **5. Tự động hóa Webhooks & Lập lịch** | <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> **Webhooks** | Mở hộp thoại `Tạo Webhook mới 🦉` cấu hình bắn dữ liệu tự động sang Agentic Workflow hoặc lập lịch định kỳ. |

---

## Hướng dẫn chi tiết từng tính năng

### Tính năng 1 — Sơ đồ Quan hệ bảng tương tác (Database Relations ERD)

Giao diện `Trang chủ > Database > Quan hệ` (Tiêu đề tab: `Relations`) trực quan hóa cấu trúc dữ liệu toàn hệ thống dưới dạng sơ đồ mạng lưới tương tác:

| Khu vực | Thành phần giao diện | Chức năng chi tiết |
| :--- | :--- | :--- |
| **Thanh công cụ sơ đồ (Top Toolbar)** | Menu lọc danh mục | Mặc định hiển thị `Tất cả bảng người dùng...`, cho phép lọc theo từng danh mục cụ thể để canvas gọn gàng. |
| | Huy hiệu số lượng bảng | Hiển thị tổng số bảng đang có mặt trên canvas (ví dụ: `1 bảng`, `12 bảng`). |
| | Ô tìm kiếm bảng | `Q Tìm bảng trong...`: Định vị nhanh khối bảng cần quan sát. |
| | Hộp kiểm `Hiển thị trường` | Tích chọn để hiển thị danh sách các cột dữ liệu bên trong từng khối bảng. |
| | Hộp kiểm `Chỉ hiện PK / FK` | Tích chọn để thu gọn chỉ hiển thị các trường Khóa chính (Primary Key) và Khóa ngoại (Foreign Key). |
| | Nút <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> (Làm mới) | Tải lại toàn bộ dữ liệu quan hệ mới nhất. |
| | Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> (Tạo bảng) | Khởi tạo bảng mới ngay trên màn hình sơ đồ quan hệ. |
| **Không gian Canvas trực quan** | Khối thẻ bảng (Node) | Mỗi bảng hiển thị biểu tượng Database, Tên bảng, Danh mục trực thuộc, slug định danh, huy hiệu số bản ghi, nút thông tin `(i)` và nút `+ Thêm trường`. |
| | Điểm nối kéo thả (Handles) | Các chấm tròn màu xanh bố trí ở hai cạnh trái và phải của khối bảng. Người dùng nhấp giữ chuột vào điểm nối của bảng này, kéo và thả vào điểm nối của bảng khác để tạo đường dây liên kết quan hệ tức thì. |
| | Cụm điều khiển góc dưới bên trái | • <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:minus.svg?color=%23ff3333" width="16" alt="" />: Phóng to hoặc thu nhỏ khung nhìn canvas.<br>• <img src="https://api.iconify.design/lucide:maximize.svg?color=%23ff3333" width="16" alt="" /> **(Căn vừa khung nhìn)**: Tự động căn chỉnh toàn bộ các khối bảng nằm gọn trong tầm nhìn màn hình. |

---

### Tính năng 2 — Phân quyền cấp Bảng (Table Permissions)

Khi chọn <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Quyền bảng**, ngăn kéo bên phải mở ra hệ thống kiểm soát 9 phạm vi quyền hạn độc lập:

| Phạm vi quyền | Ý nghĩa kiểm soát | Cấu hình ngoại lệ |
| :--- | :--- | :--- |
| **1. Ai có thể xem bảng** | Kiểm soát ai được mở và đọc nội dung bảng này. | Mỗi phạm vi quyền có:<br>• Danh sách chọn nhanh: `Mọi người (mặc định hệ thống)` hoặc giới hạn quyền.<br>• Biểu tượng bánh răng cài đặt <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" />: Mở hộp thoại cấu hình sâu gồm:<br>&nbsp;&nbsp;- **Mặc định**: Chọn `Mọi người` hoặc `Không ai`.<br>&nbsp;&nbsp;- **Từ chối ngoại lệ**: Chọn vai trò hoặc đối tượng hội thoại cụ thể bị loại trừ.<br>&nbsp;&nbsp;- Nút **Hủy** và nút **Lưu** màu đỏ. |
| **2. Cập nhật schema bảng** | Kiểm soát ai được đổi tên, thêm/sửa/xóa cột trong bảng. | |
| **3. Xóa bảng** | Kiểm soát ai có quyền xóa vĩnh viễn bảng khỏi hệ thống. | |
| **4. Ai có thể đọc bản ghi** | Kiểm soát ai được xem dữ liệu các dòng bản ghi trong bảng. | |
| **5. Ai có thể thêm bản ghi** | Kiểm soát ai được quyền tạo thêm bản ghi mới. | |
| **6. Ai có thể sửa bản ghi** | Kiểm soát ai được quyền cập nhật giá trị các ô dữ liệu. | |
| **7. Ai có thể xóa bản ghi** | Kiểm soát ai được quyền xóa bản ghi khỏi bảng. | |
| **8. Ai có thể xuất dữ liệu** | Kiểm soát ai được phép export dữ liệu ra file bảng tính. | |
| **9. Ai có thể chia sẻ view** | Kiểm soát ai được tạo liên kết công khai cho dạng xem. | |

---

### Tính năng 3 — Phân quyền cấp Cột dữ liệu (Field-level Permissions)

Khi chọn <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> **Quyền trường**, ngăn kéo bên phải liệt kê danh sách toàn bộ các cột trong bảng (ví dụ: `Tên nhân sự`, `Nhiệm vụ hôm nay`, `Thời điểm hoàn thành`, `Loại xử lý`...):

| Thuộc tính phân quyền cột | Mô tả kiểm soát | Thiết lập chi tiết |
| :--- | :--- | :--- |
| **Ai có thể sửa dữ liệu cột** | Biểu tượng chỉnh sửa. Kiểm soát ai có thể nhập liệu hoặc thay đổi dữ liệu của riêng cột này. | Menu chọn đối tượng: `Mọi người (mặc định hệ thống)`, hoặc chỉ định các vai trò quản lý. |
| **Ai có thể xem dữ liệu cột** | Biểu tượng con mắt. Kiểm soát ai có thể nhìn thấy nội dung dữ liệu của cột (nếu bị chặn, cột sẽ ẩn hoàn toàn đối với vai trò đó). | Phù hợp bảo vệ các cột nhạy cảm như giá vốn, lương thưởng, số điện thoại cá nhân. |

---

### Tính năng 4 — Bảo mật cấp Bản ghi (Row-level Security)

Khi chọn <img src="https://api.iconify.design/lucide:lock.svg?color=%23ff3333" width="16" alt="" /> **Bảo mật cấp bản ghi**, ngăn kéo hiển thị tiêu đề và lời nhắc: *"Thiết lập dữ liệu từng người hoặc vai trò được xem, xuất, sửa và xóa. AI Agent không xuất hiện trong màn này."*

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Khởi tạo quy tắc mới** | Tại mục **Quy tắc theo người**, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm quy tắc**. | Mở khung nhập thông số cho quy tắc phân quyền mới. |
| **2. Đặt tên quy tắc** | Nhập tên gợi nhớ vào ô nhập liệu (ví dụ: `Nhóm kinh doanh Miền Bắc`). | Định danh mục đích phân quyền cho nhóm đối tượng. |
| **3. Chọn phạm vi thao tác áp dụng** | Chọn 1 hoặc nhiều tab thao tác bằng nút bấm nổi bật:<br>• **Xem dữ liệu** (*Được đánh dấu đỏ khi chọn*).<br>• **Xuất dữ liệu**.<br>• **Sửa dữ liệu**.<br>• **Xóa dữ liệu**. | Xác định chính xác hành động nào được kiểm soát bởi quy tắc này. |
| **4. Thiết lập giá trị mặc định** | Tại menu **Mặc định**, chọn `Không ai` hoặc `Mọi người`. | Đặt cơ chế kiểm soát ban đầu trước khi xét danh sách cho phép. |
| **5. Chỉ định đối tượng được cấp phép** | Tại mục **Cho phép các đối tượng**:<br>• **Vai trò**: Nhấp vào menu thả xuống để chọn vai trò được quyền thao tác (ví dụ: `Trưởng phòng`, `Nhân viên kinh doanh`).<br>• **Người dùng**: Chọn danh sách tài khoản thành viên cụ thể. | Cấp quyền đích danh cho người hoặc nhóm đối tượng. |
| **6. Thiết lập bộ lọc điều kiện bản ghi** | Tại mục **Điều kiện**, bấm thêm điều kiện lọc bản ghi (ví dụ: `Khu vực` bằng `Miền Bắc`). | Chỉ những bản ghi thỏa mãn điều kiện lọc mới chịu sự điều chỉnh của quy tắc này. |

---

### Tính năng 5 — Tự động hóa Webhooks & Scheduled Hooks

Khi chọn <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> **Webhooks**, hộp thoại **Tạo Webhook mới 🦉** xuất hiện:

| Trường thông số | Tùy chọn cấu hình | Ý nghĩa & Nghiệp vụ |
| :--- | :--- | :--- |
| **Tiêu đề** | Nhập tên Webhook (ví dụ: `Bắn thông báo đơn hàng mới sang Workflow`). | Đặt tên gợi nhớ cho luồng kích hoạt tự động. |
| **Trạng thái** | Menu thả xuống: `Hoạt động` hoặc `Tạm dừng`. | Bật hoặc tạm ngắt luồng tự động hóa khi đang bảo trì hệ thống. |
| **Loại hook** | Chọn 1 trong 2 loại:<br>• **Webhook**: Kích hoạt thời gian thực tức thì khi có biến động dữ liệu.<br>• **Lập lịch theo thời gian**: Kích hoạt định kỳ theo mốc thời gian thiết lập trước (Scheduled Hook). | Lựa chọn phương thức kích hoạt theo sự kiện hoặc theo chu kỳ. |
| **Kích hoạt (Trigger)** | • **Sự kiện kích hoạt**: Chọn thao tác gây biến động (`Cập nhật bản ghi`, `Tạo bản ghi mới`, `Xóa bản ghi`).<br>• Công tắc **Chỉ kích hoạt khi thỏa mãn điều kiện**: Bật để thêm bộ lọc điều kiện (ví dụ: chỉ gửi khi trạng thái là `Đã thanh toán`).<br>• Công tắc **Chỉ kích hoạt khi các trường cụ thể thay đổi**: Bật để chỉ định các cột mục tiêu (ví dụ: chỉ gửi khi cột `Trạng thái` thay đổi giá trị). | Tối ưu hóa số lần gọi webhook, tránh gửi tín hiệu dư thừa. |
| **Hành động (Action)** | • **Hành động**: Chọn `Từ Workflow`.<br>• **Chọn Webhook Workflow**: Nhấp vào menu thả xuống để chọn Agentic Workflow tiếp nhận và xử lý gói dữ liệu. | Kết nối bảng dữ liệu trực tiếp vào quy trình tự động hóa thông minh của RedAI. |

---

## Kiểm tra kết quả

Sau khi cấu hình các tính năng quản trị nâng cao, người dùng kiểm tra lại:

| Hạng mục kiểm tra | Tiêu chí đạt chuẩn |
| :--- | :--- |
| **1. Sơ đồ Quan hệ (Relations)** | Các đường dây nối giữa các khối bảng hiển thị chính xác; bấm vào bảng mở ra đầy đủ danh sách trường và chỉ số khóa chính/khóa ngoại. |
| **2. Phân quyền Bảng & Bản ghi** | Đăng nhập tài khoản thành viên bị giới hạn; kiểm tra các nút Thêm/Sửa/Xóa bản ghi hoặc xuất dữ liệu bị khóa hoặc ẩn theo đúng ma trận quyền đã thiết lập. |
| **3. Phân quyền Cột** | Cột nhạy cảm bị ẩn hoàn toàn hoặc hiển thị ở chế độ chỉ đọc không thể chỉnh sửa đối với nhân sự không được phân quyền. |
| **4. Webhook kích hoạt** | Tạo hoặc cập nhật một bản ghi thỏa mãn điều kiện lọc; kiểm tra Workflow đích nhận được gói tin dữ liệu tương ứng ngay lập tức. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động khám phá cấu trúc mạng lưới quan hệ bảng, thiết lập liên kết dữ liệu giữa các bảng, cấu hình luồng kích hoạt Webhooks thời gian thực sang Workflow và giám sát nhật ký thực thi thông qua bộ công cụ quản trị Database.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Database` (ID: `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6`)
- **Bộ công cụ (Tool Suite) đi kèm**: `RedAI - Module - Database` (ID: `eb8a7504-5844-4e6e-ba7f-7645f104c0af`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản trị cơ sở dữ liệu trong Workspace (Admin hoặc Owner).

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Mở màn hình `Quan hệ` (Relations ERD) để xem mạng lưới liên kết | `listTables`, `getTable`, `listSources` | Khám phá toàn bộ danh sách bảng, các khóa quan hệ PK/FK và các nguồn cơ sở dữ liệu trong Base. |
| Kéo thả điểm nối (Handles) tạo đường dây liên kết giữa 2 bảng | `createOrUpdateRelationColumn` | Thiết lập cột quan hệ liên kết hai chiều giữa hai bảng theo mô hình 1-1, 1-N hoặc N-N. |
| Xem danh sách các bản ghi đang được liên kết | `listLinkedRecords` | Truy xuất danh sách các dòng bản ghi từ bảng liên kết ứng với một bản ghi cụ thể. |
| Liên kết hoặc bỏ liên kết nhiều bản ghi cùng lúc | `linkRecordsBulk`, `unlinkRecordsBulk` | Thực hiện gán hoặc hủy gán mối liên kết giữa các dòng bản ghi theo lô. |
| Rê chuột vào bảng $\rightarrow$ <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> **Webhooks** | `hookList` | Liệt kê toàn bộ các Webhook và Scheduled Hook đang được cấu hình trên bảng. |
| Bấm **Tạo Webhook mới 🦉** để cấu hình sự kiện bắn sang Workflow | `hookCreateOrUpdate` | Tạo mới hoặc cập nhật Webhook kích hoạt theo sự kiện (tạo/sửa/xóa bản ghi) hoặc lập lịch theo chu kỳ. |
| Bấm nút **Kiểm thử Webhook** để gửi thử dữ liệu | `hookTest` | Gửi gói tin giả lập kiểm tra tính khả dụng của luồng kết nối mà không làm ảnh hưởng dữ liệu thật. |
| Kích hoạt webhook thực tế | `hookTrigger` | Thực thi kích hoạt luồng webhook với dữ liệu thực tế. |
| Bấm xem **Nhật ký Webhook** để kiểm tra lịch sử kích hoạt | `hookLogList`, `hookLogDetail` | Tra cứu danh sách nhật ký thực thi, trạng thái HTTP trả về (200 OK / 4xx / 5xx) và chi tiết gói tin gửi đi. |
| Xóa Webhook hoặc dọn dẹp nhật ký cũ | `hookDelete`, `hookLogBulkDelete` | Xóa luồng Webhook không còn sử dụng hoặc dọn dẹp các bản ghi nhật ký thực thi đã qua. |
| Kiểm tra quyền hạn thành viên | `listBaseMembersMinimal` | Liệt kê danh sách các thành viên trong Base để đối chiếu với các quy tắc phân quyền đã thiết lập trên UI. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi thiết lập quan hệ liên kết bảng và cấu hình Webhook tự động hóa trên RedAI Database theo quy trình chuẩn:

1. Bối cảnh và Mục tiêu:
- Tôi cần thiết lập mối quan hệ liên kết Một - Nhiều giữa bảng "Khách Hàng Doanh Nghiệp" và bảng "Đơn Đặt Hàng", đồng thời tạo một Webhook tự động bắn dữ liệu sang Workflow khi có đơn hàng mới phát sinh.

2. Dữ liệu cung cấp:
- Bảng nguồn: "Khách Hàng Doanh Nghiệp"
- Bảng đích: "Đơn Đặt Hàng"
- Tên trường quan hệ: "Khách Hàng" (loại 1:N)
- Tên Webhook mới: "Thông Báo Đơn Hàng Mới Sang Workflow"
- Sự kiện kích hoạt: Tạo bản ghi mới (On Create Record)
- Hành động: Bắn sang Workflow xử lý đơn hàng

3. Các bước yêu cầu thực hiện:
- Bước 1: Gọi tool getTable cho cả 2 bảng "Khách Hàng Doanh Nghiệp" và "Đơn Đặt Hàng" để kiểm tra schema.
- Bước 2: Gọi tool createOrUpdateRelationColumn trên bảng "Đơn Đặt Hàng" để tạo trường quan hệ liên kết sang bảng "Khách Hàng Doanh Nghiệp".
- Bước 3: Gọi tool hookCreateOrUpdate trên bảng "Đơn Đặt Hàng" để khởi tạo Webhook với sự kiện On Create và liên kết với Workflow xử lý đơn.
- Bước 4: Gọi tool hookTest để kiểm thử gửi gói tin mẫu và xác nhận endpoint phản hồi thành công.
- Bước 5: Gọi tool hookList để đọc lại cấu hình hook vừa tạo.

4. Yêu cầu phản hồi:
- Báo cáo chi tiết kết quả thiết lập quan hệ hai chiều và trạng thái kiểm thử của Webhook kèm mã phản hồi HTTP.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở `Trang chủ > Database > Quan hệ`, quan sát sơ đồ ERD thấy đường dây liên kết tự động vẽ nối giữa 2 bảng; rê chuột vào bảng **Đơn Đặt Hàng** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:webhook.svg?color=%23ff3333" width="16" alt="" /> **Webhooks**, thấy Webhook mới ở trạng thái `Hoạt động`. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `hookList` và `hookLogList` của bảng 'Đơn Đặt Hàng' để kiểm tra danh sách hook và lịch sử kiểm thử."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Kéo dây nối quan hệ giữa 2 bảng trên canvas Quan hệ | Gọi `getTable` thấy xuất hiện cột kiểu Relation tham chiếu chính xác giữa 2 bảng. |
| Tạo Webhook mới trong hộp thoại Webhooks | Gọi `hookList` thấy xuất hiện Webhook mới với đúng sự kiện trigger và trạng thái Hoạt động. |
| Bấm nút Kiểm thử trên hộp thoại Webhook | Gọi `hookLogList` thấy dòng nhật ký chạy thử với trạng thái thành công và mã phản hồi 200. |
| Cấu hình phân quyền bảng hoặc cột trên ngăn kéo | AI Agent gọi các thao tác ghi với tài khoản bị giới hạn quyền sẽ nhận thông báo từ chối truy cập 403. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createOrUpdateRelationColumn` | Mở màn hình `Quan hệ`, đường dây liên kết giữa 2 khối bảng lập tức hiển thị trên canvas. |
| Agent gọi `hookCreateOrUpdate` tạo Webhook | Mở Cài đặt Webhooks của bảng, thấy thẻ Webhook mới với đúng tên và biểu tượng cú vọ 🦉. |
| Agent gọi `hookTest` kiểm thử | Chuyển sang tab Nhật ký Webhook, xuất hiện dòng ghi nhận kiểm thử mới nhất kèm dấu tích xanh. |
