## Tổng quan Trung Tâm Tiện Ích và Cơ chế Điều khiển Thanh công cụ

**Trung Tâm Tiện Ích (Utilities Center)** là trung tâm điều hành mở rộng của **RedAI Database**, tích hợp hệ sinh thái 19 công cụ chuyên sâu giúp người dùng giải quyết toàn diện các nghiệp vụ: làm sạch và khử trùng lặp dữ liệu, in ấn tem nhãn mã QR, xuất bản tài liệu báo cáo PDF, sinh dữ liệu mẫu, cào dữ liệu ngoại bộ và phát động các chiến dịch tiếp thị đa kênh tự động trực tiếp từ Bảng Động.

---

## Các tính năng điều khiển và cá nhân hóa giao diện

### 1. Quy trình mở Trung Tâm Tiện Ích từ Dạng xem bảng tính (Grid View)

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Thanh công cụ Grid View** | Trên thanh công cụ chính của Dạng xem bảng tính, nhấp vào nút <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung Tâm Tiện Ích** (hoặc mở menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung Tâm Tiện Ích**). |
| **2** | **Hộp thoại danh mục trung tâm** | Màn hình hiển thị hộp thoại pop-up kích thước lớn (`size="lg"`), chứa thanh tìm kiếm, bộ chọn danh mục phân loại và danh sách các thẻ tiện ích có thể cuộn độc lập. |

---

### 2. Tìm kiếm tiện ích tức thời theo từ khóa

- **Thanh tìm kiếm:** Ô nhập văn bản có biểu tượng kính lúp <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> và dòng gợi ý: `Q Tìm kiếm tiện ích theo tên hoặc mô tả...`.
- **Cơ chế lọc theo thời gian thực:** Ngay khi gõ từng ký tự, danh sách bên dưới sẽ tự động so khớp từ khóa với cả **Tiêu đề** và **Mô tả nghiệp vụ** của từng tiện ích.
- **Nút xóa nhanh từ khóa:** Khi ô có nội dung, xuất hiện nút <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> ở góc phải ô tìm kiếm để người dùng xóa trắng chỉ bằng 1 cú nhấp.
- **Trạng thái không có kết quả:** Nếu không tìm thấy tiện ích phù hợp, hệ thống hiển thị thông báo trung tâm: *"Không tìm thấy tiện ích phù hợp với từ khóa '{từ khóa}'"*.

---

### 3. Bộ lọc danh mục chức năng

Menu chọn danh mục phía trên bên phải hỗ trợ 6 chế độ phân loại:

| Tùy chọn danh mục | Phạm vi hiển thị tiện ích |
| :--- | :--- |
| **Tất cả danh mục** | Hiển thị toàn bộ các tiện ích đang hoạt động (ngoại trừ các tiện ích đã bị ẩn). |
| **Làm sạch & Trùng lặp** | Gom nhóm 3 công cụ: *Chuẩn hóa & Làm sạch dữ liệu*, *Quét & Xử lý Trùng lặp tự động*, *Báo cáo Sức khỏe & Chất lượng dữ liệu*. |
| **In ấn & Mã QR** | Gom nhóm 3 công cụ: *In Tem Nhãn & Tạo Mã QR Hàng Loạt*, *Xuất Markdown Long Text*, *Xuất báo cáo Tài liệu mẫu (PDF)*. |
| **Tự động hóa & Tiện ích** | Gom nhóm 6 công cụ: *Sinh Dữ Liệu Mẫu (Mock Data)*, *Fill Dữ liệu hệ thống vào Bảng*, *Tìm kiếm dữ liệu địa điểm (Google Maps Crawl)*, *Danh sách lịch sử chạy ngầm (SysJobs)*, *Thu thập thông tin Group Zalo từ link*, *Tạo mã Coupon / Khuyến mãi hàng loạt*. |
| **Chiến dịch tiếp thị** | Gom nhóm 7 công cụ: *Chiến dịch SMS*, *Tạo chiến dịch Email*, *Chiến dịch Email Marketing User hệ thống*, *Tạo chiến dịch Zalo Personal*, *Tạo chiến dịch Zalo ZNS*, *Tạo chiến dịch Đánh giá Google Maps*, *Tạo chiến dịch gửi tin nhắn đa kênh*. |
| **Đã ẩn** | Khu vực chuyên biệt hiển thị các tiện ích mà bạn đã chủ động ẩn đi. Các thẻ tiện ích tại đây có viền nét đứt màu xám và huy hiệu `Đã ẩn`. |

---

### 4. Cơ chế Ghim tiện ích lên thanh công cụ (Tối đa 5 tiện ích)

- **Mục đích:** Đưa những tiện ích thường xuyên sử dụng ra thẳng thanh công cụ ngoài của Grid View để kích hoạt nhanh 1 cú nhấp mà không cần mở hộp thoại Trung Tâm Tiện Ích.
- **Cách thao tác:** Trên thẻ của tiện ích mong muốn, nhấp vào biểu tượng chiếc ghim <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" /> ở góc phải.
- **Trạng thái hiển thị:**
  - Tiện ích chưa ghim: Biểu tượng ghim màu xám mờ.
  - Tiện ích đã ghim: Biểu tượng ghim xoay nghiêng 45 độ, chuyển sang màu đỏ thương hiệu.
  - Ngoài thanh công cụ Grid View xuất hiện một nút bấm mang tên và biểu tượng của tiện ích đó.
- **Giới hạn số lượng:** Mỗi người dùng chỉ được ghim tối đa **5 tiện ích**. Nếu cố tình ghim tiện ích thứ 6, hệ thống hiển thị thông báo cảnh báo nổi: *"Chỉ có thể ghim tối đa 5 tiện ích lên thanh công cụ"*.
- **Lưu trữ độc lập theo ngữ cảnh:** Cấu hình ghim được lưu trữ riêng biệt theo từng Không gian làm việc (Workspace) và từng Cơ sở dữ liệu (Base).

---

### 5. Cơ chế Ẩn và Bỏ ẩn tiện ích cá nhân hóa

- **Ẩn tiện ích không có nhu cầu dùng:**
  - Nhấp vào biểu tượng con mắt gạch chéo <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="16" alt="" /> trên thẻ tiện ích.
  - Tiện ích sẽ tự động bị bỏ ghim (nếu đang được ghim) và ẩn khỏi danh sách chính.
  - Hệ thống hiển thị thông báo: *"Đã ẩn tiện ích '{Tên tiện ích}'. Bạn có thể xem lại tại danh mục 'Đã ẩn'"*.
- **Bỏ ẩn (Khôi phục hiển thị):**
  - Chuyển bộ lọc danh mục sang **Đã ẩn**.
  - Tìm thẻ tiện ích cần khôi phục, nhấp vào biểu tượng con mắt màu vàng <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" />.
  - Hệ thống hiển thị thông báo: *"Đã hiển thị lại tiện ích '{Tên tiện ích}'"* và đưa tiện ích trở lại danh mục tương ứng.

---

## Danh mục liên kết 19 tài liệu tiện ích chi tiết

Nhấp vào các tài liệu chuyên sâu dưới đây để xem hướng dẫn chi tiết từng tiện ích:

1. [01 — Chuẩn hóa & Làm sạch dữ liệu](./01-tien-ich-chuan-hoa-va-lam-sach-du-lieu.md)
2. [02 — Quét & Xử lý Trùng lặp tự động](./02-tien-ich-quet-va-xu-ly-trung-lap-tu-dong.md)
3. [03 — Báo Cáo Sức khỏe & Chất lượng dữ liệu](./03-tien-ich-bao-cao-suc-khoe-va-chat-luong-du-lieu.md)
4. [04 — In Tem Nhãn & Tạo Mã QR Hàng Loạt](./04-tien-ich-in-tem-nhan-va-tao-ma-qr-hang-loat.md)
5. [05 — Xuất Markdown Long Text & Đồng bộ Knowledge Base](./05-tien-ich-xuat-markdown-long-text-va-dong-bo-knowledge-base.md)
6. [06 — Xuất báo cáo Tài liệu mẫu (PDF Template Designer)](./06-tien-ich-thiet-ke-mau-bao-cao-tai-lieu-pdf.md)
7. [07 — Sinh Dữ Liệu Mẫu (Mock Data)](./07-tien-ich-sinh-du-lieu-mau-mock-data.md)
8. [08 — Fill Dữ liệu hệ thống vào Bảng](./08-tien-ich-fill-du-lieu-he-thong-vao-bang.md)
9. [09 — Thu thập thông tin Group Zalo từ link](./09-tien-ich-thu-thap-thong-tin-group-zalo-tu-link.md)
10. [10 — Tạo mã Coupon / Khuyến mãi hàng loạt](./10-tien-ich-tao-ma-coupon-khuyen-mai-hang-loat.md)
11. [11 — Tìm kiếm dữ liệu địa điểm (Google Maps Crawl)](./11-tien-ich-tim-kiem-du-lieu-dia-diem-google-maps.md)
12. [12 — Danh sách lịch sử chạy ngầm (SysJobs History)](./12-tien-ich-danh-sach-lich-su-chay-ngam-sysjobs.md)
13. [13 — Chiến dịch SMS Marketing & CSKH](./13-tien-ich-chien-dich-sms-marketing.md)
14. [14 — Tạo chiến dịch Email Marketing từ Bảng Động](./14-tien-ich-chien-dich-email-marketing-bang-dong.md)
15. [15 — Chiến dịch Email Marketing User hệ thống (30+ Phân khúc)](./15-tien-ich-chien-dich-email-marketing-user-he-thong.md)
16. [16 — Tạo chiến dịch Zalo Personal](./16-tien-ich-chien-dich-zalo-personal.md)
17. [17 — Tạo chiến dịch Zalo ZNS Chăm sóc khách hàng](./17-tien-ich-chien-dich-zalo-zns.md)
18. [18 — Tạo chiến dịch Đánh giá & Bình luận Google Maps](./18-tien-ich-chien-dich-danh-gia-google-maps.md)
19. [19 — Tạo chiến dịch gửi tin nhắn đa kênh (Omnichannel Campaign Wizard 4 Bước)](./19-tien-ich-chien-dich-gui-tin-nhan-da-kenh-omnichannel.md)
