## Mở khu vực Mã giảm giá & Voucher

Để thiết kế các chiến dịch khuyến mãi, phát hành mã giảm giá (`Voucher`), giới hạn lượt sử dụng chống gian lận (Anti-Fraud) và quy định phạm vi sản phẩm áp dụng, bạn truy cập vào trang **Voucher** của ứng dụng **RedAI Business**:

1. Trên thanh điều hướng chính ở đầu ứng dụng, bấm vào nút thứ năm <img src="https://api.iconify.design/lucide:ticket-percent.svg?color=%23ff3333" width="16" alt="" /> **(Voucher)** (`/vouchers`).
2. Giao diện **Mã giảm giá & Voucher** bao gồm:
   - **3 thẻ chỉ số KPI phía trên**:
     1. <img src="https://api.iconify.design/lucide:ticket-percent.svg?color=%23ff3333" width="16" alt="" /> **Tổng Số Voucher**: Tổng số mã khuyến mãi đã tạo.
     2. <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **Đang Kích Hoạt**: Số lượng mã đang mở và còn hiệu lực sử dụng.
     3. <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **Tạm Ngừng Chạy**: Số lượng mã đang tạm tắt hoặc đã hết hạn/hết lượt.
   - **Thanh công cụ điều khiển**: Bộ chọn cửa hàng (`Tất cả cấu hình bán hàng`), ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm mã giảm giá)**, nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Voucher Mới)** và nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới danh sách)**.

---

## Các bước thực hiện

### Chọn loại giảm giá và chính sách áp dụng sản phẩm phù hợp

Khi khởi tạo một mã giảm giá mới, bạn cần lựa chọn **Loại giảm giá** (ở Khối 2) và **Chính sách áp dụng sản phẩm** (ở Khối 5) phù hợp với mục tiêu chương trình khuyến mãi:

| Tiêu chí lựa chọn | Các tùy chọn trên giao diện | Cách hệ thống tính toán & kiểm tra |
| :--- | :--- | :--- |
| **Loại giảm giá \*** | 1. **Giảm theo tỷ lệ phần trăm (%)**<br>2. **Giảm số tiền cố định (VNĐ)**<br>3. **Miễn phí vận chuyển (Free Shipping)** | • Nếu chọn **Giảm theo tỷ lệ phần trăm (%)**: Bạn nhập **Mức giảm (%) \*** và có thể giới hạn trần qua ô **Mức giảm tối đa (VNĐ)**.<br>• Nếu chọn **Giảm số tiền cố định (VNĐ)**: Bạn nhập số tiền trừ thẳng vào đơn tại ô **Số tiền giảm (VNĐ) \***.<br>• Nếu chọn **Miễn phí vận chuyển (Free Shipping)**: Hệ thống tự động miễn phí giao hàng cho đơn đủ điều kiện mà không cần nhập ô mức giảm. |
| **Chính sách áp dụng sản phẩm \*** | 1. **Áp dụng cho toàn bộ sản phẩm trong cửa hàng** (`ALL`)<br>2. **Chỉ áp dụng cho các sản phẩm chỉ định** (`APPLICABLE`)<br>3. **Áp dụng tất cả, TRỪ các sản phẩm chỉ định** (`EXCLUDED`) | • `ALL`: Mọi mặt hàng trong giỏ đều được tính hưởng khuyến mãi.<br>• `APPLICABLE`: Chỉ những sản phẩm được bạn tích chọn mới được áp dụng mã.<br>• `EXCLUDED`: Áp dụng cho toàn cửa hàng ngoại trừ các sản phẩm nằm trong danh sách loại trừ. |

---

### Giai đoạn 1 — Khởi tạo Mã giảm giá mới qua 5 khối cấu hình

Tại trang `/vouchers`, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Voucher Mới)** trên thanh công cụ để mở ngăn kéo **Tạo Mã Giảm Giá Mới** và điền lần lượt 5 khối thông tin:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Thiết lập Khối 1 — `Phạm Vi & Cấu Hình Áp Dụng`** | Điền các trường định danh chương trình khuyến mãi:<br>• **Cấu hình bán hàng \***: Chọn một cấu hình bán hàng cụ thể hoặc chọn `Áp dụng toàn bộ cấu hình (Global)`.<br>• **Tên chương trình khuyến mãi \***: Nhập tên chiến dịch (ví dụ: `Siêu Sale Mùa Hè - Giảm 20%`).<br>• **Mã giảm giá (Code) \***: Nhập mã viết liền không dấu (ví dụ: `SUMMER20`, hệ thống tự động chuyển thành chữ in hoa).<br>• **Mô tả chương trình**: Nhập điều kiện hoặc thể lệ tóm tắt để nhân viên và AI Agent tư vấn cho khách. |
| **2. Thiết lập Khối 2 — `Mức Giảm Giá & Điều Kiện Đơn Hàng`** | • **Loại giảm giá \***: Chọn 1 trong 3 loại (`Giảm theo tỷ lệ phần trăm (%)`, `Giảm số tiền cố định (VNĐ)`, hoặc `Miễn phí vận chuyển (Free Shipping)`).<br>• **Mức giảm (%) \*** hoặc **Số tiền giảm (VNĐ) \***: Nhập giá trị giảm tương ứng (trường này tự động ẩn nếu bạn chọn `Miễn phí vận chuyển`).<br>• **Mức giảm tối đa (VNĐ)**: Nhập số tiền giảm tối đa cho phép khi dùng loại giảm theo `%` (để trống nếu không giới hạn).<br>• **Giá trị đơn hàng tối thiểu (VNĐ)**: Nhập mức tổng tiền hàng tối thiểu để khách được phép áp dụng mã này (mặc định là `0`). |
| **3. Thiết lập Khối 3 — `Giới Hạn Lượt Dùng & Cơ Chế Chống Spam (Anti-Fraud)`** | • **Cơ chế định danh khách hàng (Limit Mode) \***: Chọn `Theo Số Điện Thoại (PHONE) — Khuyên dùng` (kiểm soát số lần dùng theo SĐT người nhận) hoặc `Theo Phiên Chat (CONVERSATION)` (kiểm soát theo từng cuộc hội thoại).<br>• **Tổng lượt dùng tối đa**: Nhập tổng ngân sách số lượt mã được phép sử dụng trên toàn hệ thống (để trống nếu không giới hạn).<br>• **Lượt dùng / khách**: Nhập số lần tối đa một khách hàng được dùng mã này (mặc định là `1`). |
| **4. Thiết lập Khối 4 — `Thời Gian Bắt Đầu & Hết Hạn Hiệu Lực`** | • **Thời điểm bắt đầu**: Chọn ngày và giờ bắt đầu mở mã.<br>• **Thời điểm hết hạn**: Chọn ngày và giờ kết thúc chương trình (để trống nếu mã không có thời hạn kết thúc). |
| **5. Thiết lập Khối 5 — `Phạm Vi Sản Phẩm Áp Dụng` và Lưu khởi tạo** | • **Chính sách áp dụng sản phẩm \***: Chọn `Áp dụng cho toàn bộ sản phẩm trong cửa hàng`, `Chỉ áp dụng cho các sản phẩm chỉ định`, hoặc `Áp dụng tất cả, TRỪ các sản phẩm chỉ định`.<br>• Nếu chọn chỉ định hoặc loại trừ sản phẩm: Tìm kiếm mặt hàng tại ô `Tìm theo tên hoặc mã SKU để tích chọn...` và tích vào các sản phẩm trong danh sách (hoặc nhập ID sản phẩm vào ô `Nhập ID cách nhau bằng dấu phẩy rồi nhấn Enter...` và bấm **(Thêm)**).<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo mã giảm giá)** ở góc dưới bên phải ngăn kéo để hoàn tất. |

---

### Giai đoạn 2 — Bật/tắt nhanh, chỉnh sửa và xóa Voucher trên danh sách

Trên bảng **Danh Sách Mã Giảm Giá** (gồm 7 cột: `Mã Voucher`, `Mức giảm`, `Đơn tối thiểu`, `Lượt sử dụng`, `Thời hạn hiệu lực`, `Trạng thái`, `Thao tác`), bạn có thể điều khiển vòng đời từng mã ngay lập tức:

| Thao tác trên dòng Voucher | Cách thực hiện |
| :--- | :--- |
| **Sao chép nhanh Mã Voucher** | Nhấp vào biểu tượng <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> ngay bên cạnh mã code tại cột **Mã Voucher** để sao chép và gửi cho khách hàng. |
| **Bật / Tắt nhanh trạng thái kích hoạt** | Tại cột **Trạng thái**, gạt trực tiếp công tắc **Switch** (`Bật` / `Tắt`) để kích hoạt hoặc tạm dừng mã giảm giá ngay lập tức mà không cần mở cửa sổ chỉnh sửa. |
| **Chỉnh sửa thông tin Voucher** | Bấm nút <img src="https://api.iconify.design/lucide:edit-3.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa voucher)** tại cột **Thao tác** để mở ngăn kéo **Chỉnh Sửa Mã Giảm Giá**, cập nhật các thông số rồi bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cập nhật)**. |
| **Xóa Voucher** | Bấm nút <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa voucher)** tại cột **Thao tác**, sau đó bấm <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận xóa)** trong hộp thoại **Xác Nhận Xóa Voucher**. |

---

## Kiểm tra kết quả

1. **Trên bảng Danh Sách Mã Giảm Giá (`/vouchers`)**: Mã giảm giá vừa tạo xuất hiện với nhãn loại giảm giá (`%`, `VNĐ` hoặc `Free Ship`), thanh tiến trình **Lượt sử dụng** (`0 / {tổng lượt}`), thời hạn hiệu lực và công tắc trạng thái đang ở chế độ **Bật**.
2. **Trên 3 thẻ KPI đầu trang**: Chỉ số **Tổng Số Voucher** và **Đang Kích Hoạt** tăng thêm 1 đơn vị.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động phát hành mã giảm giá mới, bật/tắt nhanh trạng thái chương trình khuyến mãi, hoặc tự động kiểm tra và áp mã giảm giá tối ưu cho khách hàng trong lúc tư vấn.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Dành cho AI Agent Quản trị & Phát hành Khuyến mãi**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Setup` (ID: `75e8c472-fbe2-4a26-8e4e-5cdaabdc590d`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Setup` (ID: `b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63`)
- **Dành cho AI Agent Tư vấn & Kiểm tra Mã giảm giá cho Khách hàng**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Operations` (ID: `0a1c2aec-78f6-419c-8e70-d7ce019ba210`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Operations` (ID: `b736f624-fb7e-425d-9e3b-6e216887604d`)
- **Quyền hạn tài khoản**: Tài khoản Quản lý cửa hàng (đối với tạo/sửa/xóa Voucher) hoặc Nhân viên bán hàng (đối với tra cứu và áp mã).

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Xem bảng **Danh Sách Mã Giảm Giá** và chi tiết từng Voucher | `listCommerceVouchers`, `getCommerceVoucherDetail` *(Setup)* | Liệt kê toàn bộ mã giảm giá theo cửa hàng và xem chi tiết cấu hình một Voucher. |
| Điền 5 khối thông tin và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo mã giảm giá)** | `createCommerceVoucher` *(Setup)* | Tạo mới chương trình mã giảm giá với đầy đủ điều kiện đơn tối thiểu, giới hạn lượt dùng, thời hạn và phạm vi sản phẩm. |
| Bấm <img src="https://api.iconify.design/lucide:edit-3.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa voucher)** và lưu cập nhật | `updateCommerceVoucher` *(Setup)* | Cập nhật thông tin, mức giảm, hạn dùng hoặc phạm vi sản phẩm của Voucher hiện có. |
| Gạt công tắc **Switch** (`Bật` / `Tắt`) tại cột **Trạng thái** | `toggleCommerceVoucherActive` *(Setup)* | Bật kích hoạt hoặc tạm dừng nhanh một mã giảm giá. |
| Bấm <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa voucher)** | `deleteCommerceVoucher` *(Setup)* | Xóa mã giảm giá khỏi hệ thống. |
| Tra cứu các mã khuyến mãi khả dụng và kiểm tra tính hợp lệ khi lên đơn cho khách | `getAvailableCommerceVouchers`, `validateCommerceVoucher` *(Operations)* | Lấy danh sách Voucher khách có thể dùng và tính toán số tiền được giảm thực tế trên giỏ hàng. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi tạo mới một chương trình Mã giảm giá (Voucher) trên RedAI Business theo thông tin sau:

1. Bối cảnh và Mục tiêu:
- Tôi muốn phát hành mã khuyến mãi giảm giá theo phần trăm cho khách hàng mua sắm trong tháng này, có giới hạn số tiền giảm tối đa và chống spam theo số điện thoại.

2. Dữ liệu cung cấp:
- Tên chương trình khuyến mãi: "Ưu Đãi Khách Hàng Thân Thiết Giảm 15%"
- Mã giảm giá (Code): "VIP15"
- Loại giảm giá: Giảm theo tỷ lệ phần trăm ("PERCENTAGE"), mức giảm: 15%
- Mức giảm tối đa: 100.000 VNĐ
- Giá trị đơn hàng tối thiểu: 500.000 VNĐ
- Cơ chế định danh (Limit Mode): "PHONE" (Theo Số Điện Thoại)
- Tổng lượt dùng tối đa: 200 lượt, giới hạn mỗi khách: 1 lượt
- Phạm vi sản phẩm: Áp dụng cho toàn bộ sản phẩm ("ALL")

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng listConfigurations để lấy ID cấu hình bán hàng mặc định hiện tại (hoặc áp dụng toàn cục).
- Bước 2: Dùng công cụ createCommerceVoucher để khởi tạo mã giảm giá "VIP15" với đầy đủ các thông số trên.
- Bước 3: Dùng getCommerceVoucherDetail (hoặc validateCommerceVoucher) để kiểm tra lại thông tin và trạng thái kích hoạt của mã "VIP15".

4. Yêu cầu phản hồi:
- Báo cáo ID của Voucher vừa tạo, mã Code, mức giảm, điều kiện đơn tối thiểu, giới hạn lượt dùng và trạng thái hoạt động hiện tại.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở trang `/vouchers` trên ứng dụng **RedAI Business**, kiểm tra mã **VIP15** đã xuất hiện trên bảng **Danh Sách Mã Giảm Giá** với trạng thái **Bật**. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra thử trên giỏ hàng** | Gửi câu lệnh: *"Hãy dùng `validateCommerceVoucher` kiểm tra thử mã `VIP15` cho một đơn hàng trị giá 600.000 VNĐ của số điện thoại `0987654321` xem được giảm bao nhiêu tiền."* |
