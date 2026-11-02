## Mở khu vực Quản lý Đơn hàng

Để khởi tạo đơn hàng bán lẻ mới, xuất mã thanh toán động `VietQR`, duyệt chốt đơn, cập nhật mã vận đơn giao hàng hoặc hủy đơn hoàn tồn kho, bạn truy cập vào trang **Đơn hàng** của ứng dụng **RedAI Business**:

1. Trên thanh điều hướng chính ở đầu ứng dụng, bấm vào nút thứ hai <img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> **(Đơn hàng)** (`/orders`).
2. Giao diện **Quản lý Đơn hàng** bao gồm:
   - **Thanh công cụ phía trên**:
     - Bộ chọn **Cấu hình:** (<img src="https://api.iconify.design/lucide:store.svg?color=%23ff3333" width="16" alt="" />): Cho phép lọc đơn hàng theo **Tất cả ({số lượng})** hoặc từng cấu hình cửa hàng cụ thể.
     - Ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm đơn hàng)**: Tra cứu tức thì theo mã đơn, tên khách hàng hoặc số điện thoại.
     - Nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo đơn hàng mới)**: Mở hộp thoại lên đơn bán lẻ trực tiếp.
     - Nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới danh sách)**: Đồng bộ lại dữ liệu đơn hàng mới nhất.
   - **6 tab lọc theo trạng thái vòng đời đơn hàng**: **(Tất cả ({số lượng}))**, **(Chờ xác nhận)**, **(Đã xác nhận)**, **(Đang giao)**, **(Đã giao)** và **(Đã hủy)**.

---

## Các bước thực hiện

### Chọn phương thức thanh toán và xử lý đơn hàng

Khi tạo đơn hàng mới ở Giai đoạn 1, bạn có thể chọn một trong hai phương thức thanh toán tùy theo thỏa thuận với khách hàng:

| Phương thức thanh toán | Khi nào nên sử dụng | Quy trình xử lý tiếp theo ở Giai đoạn 2 & 3 |
| :--- | :--- | :--- |
| **Chuyển khoản ngân hàng (`BANK_TRANSFER` / `VietQR`)** | Khi khách hàng thanh toán toàn bộ giá trị đơn hàng qua chuyển khoản ngân hàng hoặc quét mã QR. | Sau khi tạo đơn, bạn bấm nút <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **(Mã VietQR chuyển khoản)** ngay trên dòng đơn hàng để gửi mã QR (đã nhúng sẵn số tiền và nội dung chuyển khoản chuẩn) cho khách. |
| **Thu hộ COD khi nhận hàng (`COD`)** | Khi khách hàng thanh toán tiền mặt cho bưu tá lúc nhận hàng (hoặc đặt cọc trước một phần theo quy tắc Cọc COD của cửa hàng). | Sau khi kiểm tra thông tin khách hàng (hoặc nhận đủ tiền cọc nếu có), bạn bấm nút <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **(Duyệt chốt đơn)** và <img src="https://api.iconify.design/lucide:truck.svg?color=%23ff3333" width="16" alt="" /> **(Cập nhật mã vận đơn)**. |

---

### Giai đoạn 1 — Khởi tạo Đơn hàng bán lẻ mới

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Tạo Đơn Hàng Bán Lẻ Mới** | Tại trang `/orders`, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo đơn hàng mới)** trên thanh công cụ phía trên. |
| **2. Chọn Cấu hình bán hàng và điền Thông tin Khách hàng** | Trong hộp thoại **Tạo Đơn Hàng Bán Lẻ Mới**:<br>1. **Cấu Hình Bán Hàng \***: Chọn cửa hàng/chi nhánh ghi nhận đơn hàng này.<br>2. Tại khối **Thông Tin Khách Hàng & Giao Nhận**:<br>   • **Điền nhanh từ Khách quen CRM (Tùy chọn)**: Nếu cửa hàng đã có dữ liệu khách hàng, bạn có thể chọn nhanh khách hàng từ ô **Khách quen CRM** (`Điền nhanh`) để hệ thống tự động điền Họ tên, Số điện thoại, Email và Địa chỉ.<br>   • **Hoặc nhập trực tiếp**: Điền **Họ và tên khách hàng \***, **Số điện thoại \***, **Email (Tùy chọn)**.<br>   • **Phương thức thanh toán**: Chọn `Thu hộ COD khi nhận hàng` hoặc `Chuyển khoản ngân hàng`.<br>   • **Địa chỉ giao hàng**: Nhập địa chỉ nhận hàng của khách (nếu bạn để trống ô này, hệ thống sẽ tự động ghi nhận là `"Nhận tại cửa hàng"`). |
| **3. Chọn sản phẩm từ kho vào Giỏ hàng** | Tại khối **Giỏ Hàng & Sản Phẩm**:<br>• Nhấp vào ô **Thêm sản phẩm từ kho** (`Gõ tên sản phẩm hoặc mã SKU để thêm vào đơn...`) và chọn mặt hàng khách mua (danh sách hiển thị rõ tên sản phẩm, mã SKU, số lượng tồn kho khả dụng và đơn giá).<br>• Điều chỉnh số lượng mua của từng dòng sản phẩm bằng nút <img src="https://api.iconify.design/lucide:minus.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> hoặc bấm <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> để xóa mặt hàng khỏi giỏ.<br>• Nhập lưu ý đóng gói hoặc giờ giao hàng vào ô **Ghi chú đơn hàng** bên dưới. |
| **4. Hoàn tất tạo đơn** | Kiểm tra lại số tiền tại mục **Tổng thanh toán:** ở chân hộp thoại, sau đó bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Hoàn tất tạo đơn)** (hoặc bấm <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> **(Hủy bỏ)** nếu muốn đóng lại). |

---

### Giai đoạn 2 — Xuất mã thanh toán VietQR, Xem chi tiết và Duyệt chốt đơn

Trên bảng danh sách đơn hàng tại `/orders`, cột **Thao tác** ở cuối mỗi dòng đơn hàng cung cấp các nút biểu tượng xử lý trực tiếp theo từng trạng thái:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Xuất mã thanh toán VietQR gửi cho khách hàng** | • Bấm vào biểu tượng <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **(Mã VietQR chuyển khoản)** ngay trên dòng đơn hàng để mở ngăn kéo **Mã Thanh Toán VietQR**.<br>• Ngăn kéo hiển thị hình ảnh mã QR động kèm bảng thông tin: **Ngân hàng**, **Số tài khoản**, **Chủ tài khoản**, **Số tiền cần chuyển** và **Nội dung chuyển khoản (Bắt buộc)**.<br>• Bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép thông tin chuyển khoản)** để gửi toàn bộ nội dung thanh toán cho khách hàng qua khung chat. |
| **2. Xem chi tiết toàn diện đơn hàng** | Bấm vào biểu tượng con mắt <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem chi tiết đơn)** trên dòng đơn hàng để mở ngăn kéo **Chi Tiết Đơn {Mã đơn}**, hiển thị đầy đủ 4 khối thông tin: **Khách Hàng & Giao Nhận**, **Thanh Toán & Vận Chuyển**, **Danh Sách Sản Phẩm ({số lượng})** và **Tổng cộng thanh toán**. |
| **3. Duyệt chốt đơn hàng (`Chờ xác nhận` $\rightarrow$ `Đã xác nhận`)** | Đối với các đơn hàng đang ở trạng thái **Chờ xác nhận**, sau khi bạn đã kiểm tra thông tin với khách hàng, hãy bấm vào nút tròn màu xanh lá <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **(Duyệt chốt đơn)** ngay tại cột **Thao tác**. Trạng thái đơn hàng sẽ lập tức chuyển sang **Đã xác nhận**. |

---

### Giai đoạn 3 — Cập nhật mã vận đơn giao hàng hoặc Hủy đơn hàng

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Cập nhật mã vận đơn (`Đã xác nhận` $\rightarrow$ `Đang giao`)** | 1. Đối với đơn hàng đang ở trạng thái **Đã xác nhận**, bấm vào nút biểu tượng xe tải màu xanh dương <img src="https://api.iconify.design/lucide:truck.svg?color=%23ff3333" width="16" alt="" /> **(Cập nhật mã vận đơn)** tại cột **Thao tác**.<br>2. Trong ngăn kéo **Cập Nhật Mã Vận Đơn**, điền 2 trường thông tin:<br>   • **Đơn vị vận chuyển**: Chọn một trong các đơn vị (`Giao Hàng Nhanh (GHN)`, `Giao Hàng Tiết Kiệm (GHTK)`, `Viettel Post`, `J&T Express`, hoặc `Tự giao hàng (Nội bộ)`).<br>   • **Mã vận đơn (Tracking Code) \***: Nhập mã vận đơn (ví dụ: `GHN89234712...`).<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận giao hàng)**. Đơn hàng sẽ chuyển sang trạng thái **Đang giao** và gắn mã vận đơn lên dòng đơn hàng. |
| **2. Hủy đơn hàng và hoàn tồn kho (`Đã hủy`)** | 1. Đối với đơn hàng chưa hoàn tất giao và chưa hủy, bấm vào nút biểu tượng màu đỏ <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **(Hủy đơn hàng)** tại cột **Thao tác**.<br>2. Trong ngăn kéo **Xác Nhận Hủy Đơn Hàng**, nhập lý do vào ô **Lý do hủy đơn \*** (ví dụ: `Khách đổi ý, đặt nhầm sản phẩm, quá hạn giữ hàng...`).<br>3. Bấm nút <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận hủy đơn)**. Hệ thống sẽ chuyển đơn sang trạng thái **Đã hủy** và tự động hoàn trả số lượng tồn kho đã giữ về bảng Sản phẩm. |

---

## Kiểm tra kết quả

1. **Tại bảng Danh sách Đơn hàng (`/orders`)**: Đơn hàng mới xuất hiện trên đầu bảng với đầy đủ **Mã đơn**, **Khách hàng**, **Sản phẩm**, **Tổng tiền**, nhãn trạng thái **Thanh toán** (`Đã TT`, `Đã cọc`, `Chưa TT`), nhãn **Trạng thái đơn** và số lượng tại 6 tab trạng thái phía trên được cập nhật tương ứng.
2. **Tại trang Sản phẩm (`/products`)**: Số lượng tồn kho của các mặt hàng trong đơn được trừ giữ chỗ chính xác khi tạo đơn và được cộng hoàn lại ngay khi đơn bị hủy.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Quy trình tư vấn sản phẩm, tính phí giao hàng, áp mã giảm giá, lên đơn hàng mới, sinh mã thanh toán `VietQR` cũng như duyệt đơn, cập nhật vận đơn và hủy đơn đều có thể thực hiện tự động thông qua **trợ lý ảo AI Agent**.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Tùy theo vai trò của trợ lý ảo AI Agent (Agent bán hàng trực tiếp với khách hay Agent quản trị vận hành nội bộ), bạn trang bị một trong hai kỹ năng sau:

- **Dành cho AI Agent Tư vấn & Chốt đơn với Khách hàng (Frontline / Tuyến đầu)**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Operations` (ID: `0a1c2aec-78f6-419c-8e70-d7ce019ba210`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Operations` (ID: `b736f624-fb7e-425d-9e3b-6e216887604d`)
- **Dành cho AI Agent Quản trị & Xử lý Đơn hàng Nội bộ (Back-office / Quản lý)**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Setup` (ID: `75e8c472-fbe2-4a26-8e4e-5cdaabdc590d`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Setup` (ID: `b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63`)
- **Quyền hạn tài khoản**: Tài khoản nhân viên bán hàng hoặc quản lý cửa hàng trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Kiểm tra chính sách thanh toán, cọc COD và tồn kho sản phẩm trước khi lên đơn | `getBusinessOperatingPolicy`, `searchCommerceProducts`, `getCommerceProductDetail` *(Operations)* | Đọc chính sách vận hành của cửa hàng và tìm kiếm sản phẩm, đơn giá, tồn kho khả dụng. |
| Kiểm tra mã giảm giá và ước tính phí vận chuyển cho địa chỉ khách hàng | `getAvailableCommerceVouchers`, `validateCommerceVoucher`, `smartSearchLocation`, `estimateShippingFee` *(Operations)* | Kiểm tra điều kiện áp dụng Voucher, chuẩn hóa địa chỉ giao hàng và tính phí vận chuyển dự kiến. |
| Điền biểu mẫu **Tạo Đơn Hàng Bán Lẻ Mới** và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Hoàn tất tạo đơn)** | `quickCreateOrder` *(Operations)* hoặc `createBusinessOrder` *(Setup)* | Tạo đơn hàng mới, tự động trừ giữ chỗ tồn kho và tính toán tổng thanh toán/tiền cọc. |
| Bấm <img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> **(Mã VietQR chuyển khoản)** trên dòng đơn hàng | `getOrderQrPayment` *(Có ở cả 2 Skill)* | Sinh mã thanh toán động VietQR kèm số tài khoản, số tiền và nội dung chuyển khoản chuẩn của đơn hàng. |
| Bấm <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem chi tiết đơn)** hoặc lọc danh sách đơn hàng | `getCurrentOrder`, `getBusinessOrderDetail` *(Operations)* / `listBusinessOrders`, `getBusinessOrderDetail` *(Setup)* | Tra cứu danh sách đơn hàng và xem chi tiết toàn bộ thông tin một đơn hàng. |
| Bấm <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **(Duyệt chốt đơn)** | `confirmBusinessOrder` *(Setup)* | Xác nhận duyệt chốt đơn hàng từ trạng thái `PENDING` sang `CONFIRMED`. |
| Bấm <img src="https://api.iconify.design/lucide:truck.svg?color=%23ff3333" width="16" alt="" /> **(Cập nhật mã vận đơn)** | `updateBusinessOrderShipping` *(Setup)* | Cập nhật đơn vị vận chuyển, mã vận đơn (`trackingCode`) và chuyển trạng thái đơn sang `SHIPPING`. |
| Bấm <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **(Hủy đơn hàng)** | `cancelCurrentOrder` *(Operations)* hoặc `cancelBusinessOrder`, `deleteBusinessOrder` *(Setup)* | Hủy đơn hàng kèm lý do hủy và tự động hoàn lại số lượng tồn kho đã giữ chỗ. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi kiểm tra tồn kho, tạo đơn hàng mới cho khách và xuất mã thanh toán VietQR theo thông tin sau:

1. Bối cảnh và Mục tiêu:
- Khách hàng vừa nhắn tin đặt mua sản phẩm và chọn hình thức chuyển khoản ngân hàng. Tôi cần lên đơn nhanh và lấy thông tin VietQR gửi cho khách.

2. Dữ liệu cung cấp:
- Họ và tên khách hàng: "Nguyễn Minh Tuấn"
- Số điện thoại: "0987654321"
- Địa chỉ giao hàng: "45 Lê Lợi, Phường Bến Nghé, TP. Hồ Chí Minh"
- Sản phẩm đặt mua: Tìm sản phẩm có từ khóa "[Tên sản phẩm hoặc SKU]", số lượng: 2
- Phương thức thanh toán: "BANK_TRANSFER" (Chuyển khoản ngân hàng)

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng searchCommerceProducts để tìm sản phẩm và kiểm tra số lượng tồn kho khả dụng.
- Bước 2: Dùng smartSearchLocation và estimateShippingFee để chuẩn hóa địa chỉ và tính phí giao hàng (nếu cửa hàng yêu cầu vận chuyển).
- Bước 3: Dùng quickCreateOrder (hoặc createBusinessOrder) để khởi tạo đơn hàng cho khách hàng "Nguyễn Minh Tuấn".
- Bước 4: Dùng getOrderQrPayment để lấy mã QR và thông tin chuyển khoản ngân hàng của đơn hàng vừa tạo.

4. Yêu cầu phản hồi:
- Báo cáo mã đơn hàng (orderCode), chi tiết tiền hàng, phí vận chuyển, tổng số tiền cần thanh toán và hiển thị ảnh mã VietQR kèm thông tin tài khoản nhận tiền.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở trang `/orders` trên ứng dụng **RedAI Business**, kiểm tra đơn hàng mới của khách **Nguyễn Minh Tuấn** đã xuất hiện trên bảng và bấm <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem chi tiết đơn)** để đối chiếu. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getBusinessOrderDetail` cho mã đơn hàng vừa tạo để kiểm tra lại trạng thái đơn và trạng thái thanh toán hiện tại."* |
