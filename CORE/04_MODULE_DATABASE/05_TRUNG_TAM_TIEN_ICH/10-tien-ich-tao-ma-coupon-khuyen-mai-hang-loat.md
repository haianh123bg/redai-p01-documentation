## Tổng quan Tiện ích Tạo mã Coupon / Khuyến mãi hàng loạt

Tiện ích **Tạo mã Coupon / Khuyến mãi hàng loạt** là công cụ phát hành và quản lý mã ưu đãi tài chính tập trung trên **RedAI Database**. Tiện ích cho phép doanh nghiệp khởi tạo hàng loạt mã voucher điểm thưởng R-Point hoặc mã kích hoạt/giảm giá gói thuê bao Subscription, tùy biến chiết khấu theo phần trăm hoặc số tiền cố định, thiết lập điều kiện áp dụng chặt chẽ và tự động đồng bộ toàn bộ danh sách mã vừa sinh vào Bảng Động để theo dõi và đối soát.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Phân loại mã khuyến mãi** | • **Mã điểm thưởng R-Point:** | Dùng để nạp điểm thưởng thanh toán nội bộ trên nền tảng. |
| | • **Mã gói dịch vụ Subscription:** | Dùng để giảm giá hoặc tặng quyền lợi kích hoạt các gói đăng ký dịch vụ. |
| **2. Hình thức và Mức chiết khấu** | • **Giảm theo tỷ lệ phần trăm (%):** | Nhập tỷ lệ chiết khấu (từ 1% đến 100%) kèm ô **Mức giảm tối đa (Max Discount)** để tránh thâm hụt ngân sách. |
| | • **Giảm theo số tiền cố định (VND):** | Nhập số tiền giảm trực tiếp trên đơn hàng (ví dụ: `100.000 VNĐ`). |
| | • **Tặng quyền lợi gói (Benefit Mode):** | Áp dụng riêng cho Subscription: mã dùng để nâng cấp thẳng gói dịch vụ mà không cần thanh toán. |
| **3. Điều kiện ràng buộc an toàn** | • **Hạn sử dụng:** | Chọn ngày và giờ hết hạn chính xác qua bộ chọn lịch tương tác (`DateTimePicker`). |
| | • **Giới hạn số lượt dùng:** | Tổng số lần tối đa mà mã có thể được nhập và kích hoạt trên hệ thống. |
| | • **Giá trị đơn hàng tối thiểu:** | Đơn hàng phải đạt giá trị tối thiểu mới được phép áp dụng voucher. |
| **4. Cấu hình sinh mã định danh** | • **Chế độ sinh tự động:** | Nhập tiền tố mã (ví dụ: `SALE2026-`), hệ thống tự động sinh chuỗi ký tự ngẫu nhiên phía sau đảm bảo tính độc nhất. |
| | • **Số lượng mã cần tạo:** | Nhập số lượng mã cần phát hành (ví dụ: `50`, `100`, `500` mã). |
| | • **Chế độ nhập tay thủ công:** | Dán danh sách các mã tự đặt ngăn cách bằng dấu xuống dòng. |
| **5. Đồng bộ trực tiếp vào Bảng Động** | • **Tạo dòng bản ghi mới (create_rows):** | Mỗi mã coupon sinh ra sẽ tự động tạo thành một dòng mới trong bảng tính. |
| | • **Cập nhật vào dòng hiện có:** | Điền mã vào các dòng đang chọn, các dòng có ô mã coupon còn trống, hoặc toàn bộ dòng. |
| | • **Bảng ánh xạ cột đích:** | Khớp nối các giá trị: Cột Mã coupon, ID coupon, Mô tả, Giá trị giảm, Loại giảm, Ngày hết hạn và Trạng thái mã. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **Tạo mã Coupon / Khuyến mãi hàng loạt**. |
| **2** | **Cấu hình loại mã & Mức giảm** | Chọn loại coupon `R-Point`, chọn hình thức giảm tiền `100.000 VNĐ` và nhập số lượt dùng tối đa là `1`. |
| **3** | **Thiết lập hạn dùng & Số lượng** | Chọn ngày hết hạn qua bộ lịch và nhập số lượng cần tạo là `50` mã kèm tiền tố `TRIAN-`. |
| **4** | **Cấu hình đồng bộ vào bảng** | Chọn *Tạo dòng bản ghi mới* và chỉ định cột nhận Mã coupon cùng cột Giá trị giảm trong bảng. |
| **5** | **Thực thi phát hành** | Bấm nút **Phát hành mã hàng loạt**. Hệ thống đăng ký mã vào phân hệ thanh toán và tự động điền danh sách mã vào Bảng Động. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Danh sách mã trong Bảng Động** | Bảng tính xuất hiện đúng số lượng dòng bản ghi mới, mỗi dòng chứa một mã coupon độc nhất kèm thông tin hạn dùng và giá trị giảm. |
| **Kích hoạt thử nghiệm** | Nhập thử một mã coupon trên giao diện thanh toán của hệ thống, mã được ghi nhận hợp lệ và trừ đúng số tiền chiết khấu đã cấu hình. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Tài khoản có quyền quản trị mã khuyến mãi (`COUPON_SYSTEM_MANAGE`) và quyền tạo bản ghi (`RECORD_CREATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Ghi nhận danh sách mã coupon vào Bảng Động** | `createRecords` | *"Hãy tạo 20 dòng bản ghi chứa danh sách mã coupon giảm giá 50k vào bảng 'Kho Voucher' với các cột Mã coupon, Giá trị giảm và Trạng thái 'Chưa sử dụng'."* |
| **Cập nhật mã coupon cho khách hàng đạt điều kiện** | `updateRecords` | *"Hãy điền mã voucher 'VIP-TRIAN' vào cột 'Mã ưu đãi' cho những khách hàng có tổng chi tiêu trên 10 triệu đồng trong bảng 'Khách Hàng'."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát hành mã coupon trên giao diện | Gọi `listRecords` trên bảng thấy danh sách các mã mới xuất hiện đầy đủ thông tin. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent điền mã coupon vào bảng | Người dùng mở Dạng xem bảng tính (Grid View), các ô mã ưu đãi hiển thị đúng giá trị mà Agent vừa cập nhật. |
