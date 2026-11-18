## Mở khu vực Trung Tâm Tiện Ích và Bộ công cụ xử lý dữ liệu nâng cao

**Trung Tâm Tiện Ích (Utilities Center)** là trung tâm điều hành và mở rộng sức mạnh chuyên sâu của **RedAI Database**, tích hợp hệ sinh thái 19 công cụ tự động hóa, làm sạch, in ấn, thu thập dữ liệu và khởi tạo chiến dịch tiếp thị trực tiếp từ các dòng bản ghi của Bảng Động.

> [!NOTE]
> Để đảm bảo mức độ chuyên sâu và chi tiết đến tận cùng của từng tính năng, toàn bộ 19 tiện ích đã được biên soạn thành **19 tệp tài liệu hướng dẫn độc lập** trong thư mục `05-TRUNG-TAM-TIEN-ICH/`. Bạn có thể nhấp trực tiếp vào danh mục bên dưới để xem hướng dẫn chi tiết của từng tiện ích.

---

### Quy trình mở Trung Tâm Tiện Ích và cá nhân hóa thanh công cụ

| Bước | Thao tác thực hiện trên giao diện | Chi tiết hiển thị & Phản hồi hệ thống |
| :---: | :--- | :--- |
| **1** | **Mở Dạng xem bảng tính (Grid View):** Tại danh sách bảng dữ liệu, nhấp chọn bảng và dạng xem cần thao tác (ví dụ: `Trang chủ > Database > Khách Hàng Doanh Nghiệp`). | Toàn bộ bảng tính hiển thị cùng thanh công cụ chức năng ở phía trên. |
| **2** | **Mở Hộp thoại Trung Tâm Tiện Ích:** Trên thanh công cụ chính của Dạng xem bảng tính, nhấp vào nút <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung Tâm Tiện Ích** (hoặc mở menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung Tâm Tiện Ích**). | Hệ thống mở **Hộp thoại Trung Tâm Tiện Ích** ở chế độ danh mục trung tâm, hiển thị thanh tìm kiếm, bộ lọc danh mục và danh sách các thẻ tiện ích. |
| **3** | **Tìm kiếm tiện ích tức thời:** Nhập từ khóa tại ô `Q Tìm kiếm tiện ích theo tên hoặc mô tả...`. | Danh sách tiện ích tự động lọc theo thời gian thực theo tiêu đề hoặc nội dung mô tả nghiệp vụ. Khi có chữ, xuất hiện nút <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> để xóa nhanh từ khóa. |
| **4** | **Lọc theo danh mục chức năng:** Nhấp vào menu chọn danh mục phía trên bên phải để lọc nhanh: *Tất cả danh mục*, *Làm sạch & Trùng lặp*, *In ấn & Mã QR*, *Tự động hóa & Tiện ích*, *Chiến dịch tiếp thị*, *Đã ẩn*. | Danh sách bên dưới chuyển đổi tức thì theo nhóm phân loại được chọn. |
| **5** | **Ghim tiện ích lên thanh công cụ (Tối đa 5 tiện ích):** Trên thẻ của tiện ích mong muốn, nhấp vào biểu tượng chiếc ghim <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" /> ở góc phải thẻ. | Chiếc ghim đổi sang trạng thái xoay nghiêng màu đỏ. Tiện ích đó lập tức xuất hiện thành một nút bấm độc lập ngay trên thanh công cụ của Grid View. Nếu đạt giới hạn 5 tiện ích, hệ thống báo: *"Chỉ có thể ghim tối đa 5 tiện ích lên thanh công cụ"*. |
| **6** | **Ẩn hoặc Hiển thị lại tiện ích:** Nhấp vào biểu tượng con mắt gạch chéo <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="16" alt="" /> để ẩn tiện ích vào mục **Đã ẩn**; hoặc vào mục **Đã ẩn** bấm biểu tượng con mắt <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> để khôi phục. | Tinh gọn thanh công cụ và giao diện làm việc theo nhu cầu cá nhân của từng nhân sự. |

---

## Danh mục chi tiết 19 Tài liệu Tiện ích độc lập

### Nhóm 1 — Làm sạch & Quản lý chất lượng dữ liệu
- [01 — Tiện ích Chuẩn hóa & Làm sạch dữ liệu](./05-TRUNG-TAM-TIEN-ICH/01-tien-ich-chuan-hoa-va-lam-sach-du-lieu.md): Chuẩn hóa SĐT (quốc nội 09x, quốc tế E.164 +84, lọc số), Email chữ thường, viết hoa họ tên (Title Case), gom khoảng trắng thừa, loại bỏ dấu tiếng Việt, xem trước so sánh (Diff Preview), xử lý batch 50 bản ghi.
- [02 — Tiện ích Quét & Xử lý Trùng lặp tự động](./05-TRUNG-TAM-TIEN-ICH/02-tien-ich-quet-va-xu-ly-trung-lap-tu-dong.md): Quét đa cột (SĐT, Email, Tên), gom cụm trùng lặp (Clusters), 3 cơ chế xử lý hàng loạt: Giữ cũ nhất, Giữ mới nhất và **Gộp thông minh (Smart Merge)** bảo toàn dữ liệu.
- [03 — Tiện ích Báo Cáo Sức khỏe & Chất lượng dữ liệu](./05-TRUNG-TAM-TIEN-ICH/03-tien-ich-bao-cao-suc-khoe-va-chat-luong-du-lieu.md): Thang điểm sức khỏe tổng thể (0–100%), tỷ lệ lấp đầy từng cột, phát hiện ô trống, cảnh báo lỗi cú pháp regex kèm nút tắt xử lý nhanh 1 cú nhấp.

### Nhóm 2 — In ấn, Xuất dữ liệu & Thiết kế biểu mẫu
- [04 — Tiện ích In Tem Nhãn & Tạo Mã QR Hàng Loạt](./05-TRUNG-TAM-TIEN-ICH/04-tien-ich-in-tem-nhan-va-tao-ma-qr-hang-loat.md): Mã hóa link bản ghi, mã ID hoặc cột bất kỳ; dàn trang in Lưới A4 (3 cột), Decal cuộn, Thẻ thông tin; in trực tiếp qua trình duyệt hoặc xuất file nén ZIP chứa toàn bộ ảnh vector SVG mã QR.
- [05 — Tiện ích Xuất Markdown Long Text & Đồng bộ Knowledge Base](./05-TRUNG-TAM-TIEN-ICH/05-tien-ich-xuat-markdown-long-text-va-dong-bo-knowledge-base.md): Đóng gói cột Rich Text/HTML thành file Markdown `.md`, tải về file ZIP hoặc đẩy thẳng vào Cơ sở Tri thức AI (Knowledge Base) kèm gắn nhãn Tags để huấn luyện AI RAG.
- [06 — Tiện ích Xuất báo cáo Tài liệu mẫu (PDF Template Designer)](./05-TRUNG-TAM-TIEN-ICH/06-tien-ich-thiet-ke-mau-bao-cao-tai-lieu-pdf.md): Tải lên PDF mẫu biểu của doanh nghiệp, kéo thả biến bảng và biến tự do theo tọa độ trực quan, tùy biến phông chữ tiếng Việt, cỡ chữ, màu sắc, mã QR, chữ ký và xuất PDF hàng loạt.

### Nhóm 3 — Tự động hóa, Thu thập & Sinh dữ liệu
- [07 — Tiện ích Sinh Dữ Liệu Mẫu (Mock Data)](./05-TRUNG-TAM-TIEN-ICH/07-tien-ich-sinh-du-lieu-mau-mock-data.md): Sinh nhanh 5–50 dòng bản ghi giả lập thử nghiệm với họ tên tiếng Việt, số điện thoại, địa chỉ các tỉnh thành, email, tiền tệ chuẩn xác, hỗ trợ làm mới seed dữ liệu.
- [08 — Tiện ích Fill Dữ liệu hệ thống vào Bảng](./05-TRUNG-TAM-TIEN-ICH/08-tien-ich-fill-du-lieu-he-thong-vao-bang.md): Trích xuất danh sách người dùng hệ thống (System Users) theo thẻ (Tags) và gói thuê bao, ghi vào bảng hiện có hoặc tự động tạo bảng mới kèm gợi ý ánh xạ trường tự động và chống trùng lặp.
- [09 — Tiện ích Thu thập thông tin Group Zalo từ link](./05-TRUNG-TAM-TIEN-ICH/09-tien-ich-thu-thap-thong-tin-group-zalo-tu-link.md): Đọc link nhóm Zalo trong bảng, sử dụng tài khoản Zalo cá nhân liên kết để cào thông tin nhóm, danh sách thành viên, tự động gắn thẻ hội thoại và cập nhật ngược lại vào Bảng Động.
- [10 — Tiện ích Tạo mã Coupon / Khuyến mãi hàng loạt](./05-TRUNG-TAM-TIEN-ICH/10-tien-ich-tao-ma-coupon-khuyen-mai-hang-loat.md): Phát hành hàng loạt mã voucher R-Point hoặc gói Subscription, chiết khấu theo % hoặc số tiền cố định, thiết lập hạn dùng và tự động đồng bộ vào Bảng Động.
- [11 — Tiện ích Tìm kiếm dữ liệu địa điểm (Google Maps Crawl)](./05-TRUNG-TAM-TIEN-ICH/11-tien-ich-tim-kiem-du-lieu-dia-diem-google-maps.md): Thu thập thông tin cơ sở kinh doanh từ Google Maps theo từ khóa ngành nghề và bán kính khu vực, bóc tách tên, hotline, địa chỉ, số sao và lưu thẳng vào Bảng Động.
- [12 — Tiện ích Danh sách lịch sử chạy ngầm (SysJobs History)](./05-TRUNG-TAM-TIEN-ICH/12-tien-ich-danh-sach-lich-su-chay-ngam-sysjobs.md): Bảng điều khiển giám sát tiến độ thời gian thực của các tác vụ chạy ngầm, theo dõi % hoàn thành, trạng thái PENDING/PROCESSING/COMPLETED/FAILED và tra cứu nhật ký lỗi chi tiết.

### Nhóm 4 — Chiến dịch Tiếp thị chuyên sâu từ Bảng Động
- [13 — Tiện ích Chiến dịch SMS Marketing & CSKH](./05-TRUNG-TAM-TIEN-ICH/13-tien-ich-chien-dich-sms-marketing.md): Gửi tin nhắn SMS Brandname FPT/Viettel, đo lường độ dài ký tự GSM-7 (160 ký tự) vs Unicode có dấu (70 ký tự), ánh xạ biến `{placeholder}`, cài đặt độ trễ và hẹn giờ gửi.
- [14 — Tiện ích Tạo chiến dịch Email Marketing từ Bảng Động](./05-TRUNG-TAM-TIEN-ICH/14-tien-ich-chien-dich-email-marketing-bang-dong.md): Gửi email hàng loạt kèm cơ chế xoay vòng máy chủ (Load Balancing SMTP/SES/SendGrid), ánh xạ biến mẫu HTML, lọc danh sách chặn (Suppression List) và kích hoạt chuỗi hành động khi khách mở mail/bấm link CTA.
- [15 — Tiện ích Chiến dịch Email Marketing User hệ thống (30+ Phân khúc)](./05-TRUNG-TAM-TIEN-ICH/15-tien-ich-chien-dich-email-marketing-user-he-thong.md): Phân khúc người dùng toàn hệ thống theo hơn 30 tiêu chí lọc sâu: xác thực KYC, gói thuê bao, đếm ngược hạn gói (7, 15, 30 ngày), số dư điểm R-Point, sinh nhật trong tháng và hành vi sử dụng tính năng.
- [16 — Tiện ích Tạo chiến dịch Zalo Personal](./05-TRUNG-TAM-TIEN-ICH/16-tien-ich-chien-dich-zalo-personal.md): Gửi tin nhắn cá nhân hóa trực tiếp từ tài khoản Zalo cá nhân, thiết kế chuỗi tin nhắn đa hành động (Văn bản $\rightarrow$ Ảnh $\rightarrow$ Link) kèm cơ chế giãn cách an toàn chống khóa nick (Random Delay 10–30s).
- [17 — Tiện ích Tạo chiến dịch Zalo ZNS Chăm sóc khách hàng](./05-TRUNG-TAM-TIEN-ICH/17-tien-ich-chien-dich-zalo-zns.md): Gửi thông báo dịch vụ chính thức qua Zalo OA bằng mẫu ZNS có tích xanh kiểm duyệt, tự động bóc tách và khớp nối các tham số `<param>` từ Bảng Động và đối soát chi phí ZCA.
- [18 — Tiện ích Tạo chiến dịch Đánh giá & Bình luận Google Maps](./05-TRUNG-TAM-TIEN-ICH/18-tien-ich-chien-dich-danh-gia-google-maps.md): Đăng bình luận và chấm điểm số sao cho danh sách địa điểm, hỗ trợ xoay vòng tài khoản, thời gian hồi chiêu (Cooldown 300s) và **ghi ngược kết quả (Result Write-Back: Trạng thái, Thời gian, Tên tài khoản)** trực tiếp vào bảng tính.
- [19 — Tiện ích Tạo chiến dịch gửi tin nhắn đa kênh (Omnichannel Campaign Wizard 4 Bước)](./05-TRUNG-TAM-TIEN-ICH/19-tien-ich-chien-dich-gui-tin-nhan-da-kenh-omnichannel.md): Trình hướng dẫn 4 bước tự động điều phối gửi tin đa kênh (Zalo OA, Fanpage, Zalo cá nhân), áp dụng chiến lược xoay vòng mẫu tin (ROUND_ROBIN/RANDOM để A/B Testing), thiết lập giá trị dự phòng (Fallback Value) cho ô rỗng và **tự động bật trợ lý ảo AI Agent tiếp quản tư vấn ngay khi khách nhắn lại**.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) có quyền thao tác trong Workspace. |

### Bảng ánh xạ tổng quan tính năng & Công cụ AI Agent

| Nhóm nghiệp vụ | Công cụ AI Agent sử dụng | Nhiệm vụ chính của công cụ |
| :--- | :--- | :--- |
| **Chuẩn hóa dữ liệu ô tính** | `listRecords`, `updateRecords` | Quét các ô dữ liệu, chuẩn hóa định dạng số điện thoại (+84/09x), viết hoa họ tên và cập nhật lại vào bảng. |
| **Quét và gộp trùng lặp** | `listRecords`, `mergeRecords` | Phát hiện các bản ghi trùng lặp theo số điện thoại hoặc email, gộp thông minh các ô trống vào bản ghi gốc và xóa dòng thừa. |
| **Kiểm toán chất lượng dữ liệu** | `countRecords`, `listRecords` | Đo lường tỷ lệ hoàn thiện (% completeness), đếm số ô trống và phát hiện các ô sai định dạng cú pháp. |
| **Sinh dữ liệu mẫu thử nghiệm** | `createRecords` | Tự động sinh từ 5 đến 50 dòng bản ghi giả lập tiếng Việt hợp lệ theo cấu trúc cột của bảng. |
| **Trích xuất dữ liệu in ấn & xuất PDF** | `listRecords`, `getRecord` | Đọc toàn bộ giá trị các trường để điền tự động vào tem nhãn mã QR hoặc biểu mẫu tài liệu PDF theo tọa độ. |
| **Xuất văn bản dài sang Markdown** | `listRecords` | Trích xuất toàn bộ nội dung từ các cột Rich Text/HTML để lưu trữ hoặc nạp vào Cơ sở Tri thức AI. |
| **Tổng hợp số liệu theo lô** | `bulkGroupBy`, `bulkAggregateRecords` | Gom nhóm bản ghi và tính toán số liệu tổng hợp phục vụ báo cáo quản trị. |
