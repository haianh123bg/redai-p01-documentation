## Mở khu vực Thiết lập & Kho bãi

Để thiết lập hệ thống cửa hàng bán lẻ, ánh xạ bảng dữ liệu động (`Dynamic Tables`), cài đặt phương thức thanh toán (`VietQR` / `COD`), quy tắc đặt cọc, kịch bản thông báo tự động đa kênh và quản lý danh sách kho xuất hàng, bạn truy cập vào trang **Thiết lập** của ứng dụng **RedAI Business**:

1. Trên thanh điều hướng chính ở đầu ứng dụng **RedAI Business** (gồm 6 mục theo đúng thứ tự: <img src="https://api.iconify.design/lucide:layout-dashboard.svg?color=%23ff3333" width="16" alt="" /> **(Tổng quan)**, <img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> **(Đơn hàng)**, <img src="https://api.iconify.design/lucide:boxes.svg?color=%23ff3333" width="16" alt="" /> **(Sản phẩm)**, <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(Khách hàng)**, <img src="https://api.iconify.design/lucide:ticket-percent.svg?color=%23ff3333" width="16" alt="" /> **(Voucher)**, <img src="https://api.iconify.design/lucide:settings-2.svg?color=%23ff3333" width="16" alt="" /> **(Thiết lập)**), bấm vào nút <img src="https://api.iconify.design/lucide:settings-2.svg?color=%23ff3333" width="16" alt="" /> **(Thiết lập)** (`/settings`).
2. Màn hình **Thiết lập & Kho bãi** được chia thành **2 tab chính**:
   - Tab <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình Bán hàng ({số lượng}))**: Quản lý toàn bộ các cấu hình cửa hàng/chi nhánh thông qua trình thuật sĩ thiết lập 5 bước.
   - Tab <img src="https://api.iconify.design/lucide:warehouse.svg?color=%23ff3333" width="16" alt="" /> **(Kho hàng & Chi nhánh ({số lượng}))**: Quản lý địa chỉ kho xuất hàng và đồng bộ điểm lấy hàng vận chuyển.

---

## Các bước thực hiện

### Chọn phương thức khởi tạo Bảng dữ liệu ở Bước 1

Khi tạo mới một **Cấu hình Bán hàng**, ở **Bước 1 (`1. Cơ bản`)**, hệ thống cung cấp 2 phương thức khởi tạo cơ sở dữ liệu để bạn lựa chọn:

| Phương thức khởi tạo | Khi nào nên sử dụng | Kết quả nhận được |
| :--- | :--- | :--- |
| **Phương thức 1 — Khởi tạo nhanh từ mẫu** (<img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" />) | Khi bạn thiết lập cửa hàng lần đầu và chưa có sẵn các bảng dữ liệu trong Database. | Bạn chỉ cần chọn một mẫu ngành hàng (Thời trang, Mỹ phẩm, F&B, Điện máy...), hệ thống sẽ **tự động tạo mới đủ 4 bảng dữ liệu chuẩn** (`Đơn hàng`, `Chi tiết Đơn hàng`, `Sản phẩm`, `Khách hàng`) kèm dữ liệu mẫu và tự động khớp toàn bộ cột. |
| **Phương thức 2 — Chọn bảng có sẵn** (<img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" />) | Khi doanh nghiệp của bạn đã tạo sẵn các Bảng dữ liệu động (`Dynamic Tables`) và muốn kết nối trực tiếp vào ứng dụng bán hàng. | Bạn chủ động chọn 4 bảng dữ liệu hiện có và sử dụng công cụ **Tự động khớp gợi ý** ở Bước 2 để ánh xạ các cột dữ liệu. |

---

### Giai đoạn 1 — Thiết lập Kho hàng & Chi nhánh xuất hàng

Để có sẵn kho xuất hàng mặc định gắn vào cấu hình bán hàng và tính phí vận chuyển tự động, bạn nên thêm kho hàng trước:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở ngăn kéo Thêm Kho Hàng Mới** | Tại trang `/settings`, chuyển sang tab thứ hai <img src="https://api.iconify.design/lucide:warehouse.svg?color=%23ff3333" width="16" alt="" /> **(Kho hàng & Chi nhánh)**, sau đó bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm Kho Hàng Mới)** trên thanh công cụ. |
| **2. Điền thông tin liên hệ và địa chỉ hành chính 2 cấp** | Trong ngăn kéo **Thêm Kho Hàng & Chi Nhánh Mới**, điền đầy đủ các trường trên giao diện:<br>1. **Tên kho hàng / Chi nhánh \***: Nhập tên kho hoặc cửa hàng (ví dụ: `Kho Tổng TP.HCM - Quận 1`).<br>2. **Số điện thoại liên hệ \***: Nhập số điện thoại của thủ kho/cửa hàng để bưu tá liên hệ khi lấy hàng.<br>3. **Tỉnh / Thành phố \***: Chọn Tỉnh/Thành phố từ danh sách có ô tìm kiếm.<br>4. **Phường / Xã \***: Chọn Phường/Xã tương ứng với Tỉnh/Thành phố vừa chọn *(hệ thống sử dụng chuẩn địa giới hành chính 2 cấp Tỉnh/Thành phố $\rightarrow$ Phường/Xã trực tiếp)*.<br>5. **Địa chỉ chi tiết (Số nhà, tên đường) \***: Nhập số nhà, ngõ/hẻm, tên đường.<br>6. **Đặt làm kho xuất hàng mặc định**: Gạt công tắc bật nếu muốn ưu tiên xuất hàng từ kho này. |
| **3. Lưu và tự động đồng bộ kho vận** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo kho hàng)**. Hệ thống sẽ tự động chuẩn hóa tọa độ GPS và đồng bộ mã cửa hàng vận chuyển (`GHN Shop ID`). Trên danh sách kho, bạn có thể bấm <img src="https://api.iconify.design/lucide:star.svg?color=%23ff3333" width="16" alt="" /> **(Đặt mặc định)**, <img src="https://api.iconify.design/lucide:edit-3.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** hoặc tích chọn để <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa đã chọn)**. |

---

### Giai đoạn 2 — Thiết lập Cấu hình Bán hàng qua trình thuật sĩ 5 bước

Tại tab đầu tiên <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình Bán hàng)**, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Cấu Hình Mới)** để mở hộp thoại **Tạo Cấu Hình Bán Hàng Mới** gồm 5 bước tuần tự:

| Bước | Cách thực hiện |
| :--- | :--- |
| **Bước 1 — <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> `1. Cơ bản` (Thông tin định danh & Bảng dữ liệu)** | 1. Chọn chế độ khởi tạo bảng: <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> **(Chọn bảng có sẵn)** hoặc <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Khởi tạo nhanh từ mẫu)** (nếu chọn từ mẫu, hãy nhấp chọn một thẻ mẫu ngành hàng trong danh sách).<br>2. Điền các trường định danh cấu hình:<br>   • **Mã cấu hình (Code) \***: Nhập mã viết liền (hoặc bấm nút <img src="https://api.iconify.design/lucide:wand-2.svg?color=%23ff3333" width="16" alt="" /> **(Tự sinh mã)** để hệ thống điền tự động).<br>   • **Tên cấu hình bán hàng \***: Nhập tên hiển thị của cửa hàng/chi nhánh.<br>   • **Đơn vị tiền tệ**: Chọn `VND — Việt Nam Đồng (₫)` hoặc `USD — Đô la Mỹ ($)`.<br>   • **Đặt làm cấu hình mặc định**: Gạt công tắc bật nếu đây là cửa hàng chính.<br>   • **Mô tả ghi chú**: Nhập mô tả quy định hoặc phạm vi áp dụng của cấu hình.<br>3. Nếu đang ở chế độ **Chọn bảng có sẵn**, chọn đủ 4 bảng tại khối liên kết bảng dữ liệu: **Bảng Đơn hàng \***, **Bảng Chi tiết Đơn hàng**, **Bảng Sản phẩm**, **Bảng Khách hàng**.<br>4. Bấm nút <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Tiếp theo)**. |
| **Bước 2 — <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> `2. Ánh xạ cột` (Đồng bộ vai trò cột dữ liệu)** | 1. Lần lượt kiểm tra 4 tab bảng: **(Bảng Đơn Hàng)**, **(Chi Tiết Đơn)**, **(Bảng Sản Phẩm)** và **(Bảng Khách Hàng)**.<br>2. Trên mỗi tab, bấm nút <img src="https://api.iconify.design/lucide:wand-2.svg?color=%23ff3333" width="16" alt="" /> **(Tự động khớp gợi ý)** để hệ thống tự động nối các vai trò nghiệp vụ (như Mã đơn, Tổng tiền, Tên sản phẩm, Tồn kho, Số điện thoại...) với tên cột thực tế trong bảng.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra & Lưu ánh xạ)**, sau đó bấm <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Tiếp theo)**. |
| **Bước 3 — <img src="https://api.iconify.design/lucide:credit-card.svg?color=%23ff3333" width="16" alt="" /> `3. Thanh toán & Kho bãi`** | Điền các thiết lập vận hành thanh toán và giao nhận:<br>1. **Kho xuất hàng mặc định**: Chọn kho hàng đã tạo ở Giai đoạn 1 (hoặc bấm nút **+ Tạo kho mới** ngay bên cạnh).<br>2. **Phương thức thanh toán chấp nhận \***: Tích chọn một hoặc cả hai phương thức: **Chuyển khoản ngân hàng (VietQR)** và **Giao hàng thu tiền hộ (COD)**.<br>3. **Phương thức thanh toán mặc định**: Chọn phương thức ưu tiên khi tạo đơn mới.<br>4. **Tài khoản ngân hàng nhận thanh toán**: Khi có bật VietQR, chọn kết nối tài khoản ngân hàng/SePay đã tích hợp trong danh sách thả xuống.<br>5. **Yêu cầu vận chuyển (Shipping Required)**: Bật công tắc nếu đơn hàng cần giao nhận và tính phí vận chuyển.<br>6. **Thời gian giữ hàng chờ thanh toán (Phút)**: Nhập số phút giữ tồn kho cho đơn chờ thanh toán (mặc định là `30` phút).<br>7. Bấm <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Tiếp theo)**. |
| **Bước 4 — <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> `4. Cọc COD` (Chính sách đặt cọc đơn thu hộ)** | 1. Bật công tắc **Yêu cầu đặt cọc với đơn COD** nếu bạn muốn khách mua COD phải chuyển khoản đặt cọc trước một phần.<br>2. Khi bật công tắc, thiết lập các trường:<br>   • **Hình thức tính tiền cọc \***: Chọn `Theo phần trăm giá trị đơn hàng (%)` hoặc `Số tiền cố định (VNĐ)`.<br>   • **Tỷ lệ cọc mặc định (%) \*** / **Số tiền cọc mặc định (VNĐ) \***: Nhập mức cọc áp dụng chung.<br>   • **Quy tắc đặt cọc riêng theo từng Sản phẩm (Tùy chọn)**: Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm quy tắc)** để chọn riêng những mặt hàng giá trị cao có tỷ lệ/số tiền cọc khác biệt.<br>3. Bấm <img src="https://api.iconify.design/lucide:arrow-right.svg?color=%23ff3333" width="16" alt="" /> **(Tiếp theo)**. |
| **Bước 5 — <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" /> `5. Thông báo` (Kịch bản tin nhắn tự động đa kênh)** | 1. Tại khối **Kịch bản Tin nhắn Tự động Đa kênh (Omnichannel Templates)**, bạn có thể gắn mẫu tin nhắn tự động gửi cho khách hàng ứng với 6 sự kiện vòng đời đơn hàng:<br>   • **Khi tạo đơn hàng mới**<br>   • **Khi xác nhận đơn hàng**<br>   • **Khi thanh toán / đặt cọc thành công**<br>   • **Khi bắt đầu giao hàng**<br>   • **Khi hủy đơn hàng**<br>   • **Khi hết thời gian giữ hàng / quá hạn thanh toán**<br>2. Ở mỗi sự kiện, chọn một mẫu có sẵn trong danh sách hoặc bấm **+ Tạo mẫu mới** / **Sửa mẫu đang chọn** để biên soạn nội dung tin nhắn kèm các biến động (`{{orderCode}}`, `{{customerName}}`, `{{totalAmount}}`...) và xem trước trực quan.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo cấu hình mới)** (hoặc **(Lưu toàn bộ cấu hình)** khi chỉnh sửa) ở góc dưới bên phải để hoàn tất. |

---

### Giai đoạn 3 — Kiểm tra tính hợp lệ và kích hoạt Cấu hình Bán hàng

Trên lưới danh sách tại tab **Cấu hình Bán hàng**, mỗi thẻ cấu hình cung cấp các nút kiểm tra và điều khiển nhanh:

| Thao tác trên Thẻ Cấu hình | Cách thực hiện |
| :--- | :--- |
| **Bật / Tắt hoạt động** | Gạt công tắc trạng thái ở góc trên bên phải thẻ cấu hình để chuyển giữa trạng thái **Đang hoạt động** và **Tắt**. |
| **Kiểm tra hợp lệ (`Validate`)** | Bấm nút <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra hợp lệ)** trên thẻ để hệ thống rà soát toàn bộ kết nối 4 bảng dữ liệu và các cột ánh xạ bắt buộc. |
| **Chỉnh sửa hoặc Xóa cấu hình** | Bấm nút <img src="https://api.iconify.design/lucide:edit-3.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** để mở lại trình thuật sĩ 5 bước hoặc bấm <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Xóa)** để xóa cấu hình không còn sử dụng. |

---

## Kiểm tra kết quả

1. **Tại tab Kho hàng & Chi nhánh**: Kho hàng vừa tạo hiển thị nhãn **Mặc định**, đầy đủ địa chỉ 2 cấp (`Phường/Xã, Tỉnh/Thành phố`), tọa độ GPS và trạng thái **Đã đồng bộ GHN** màu xanh lá.
2. **Tại tab Cấu hình Bán hàng**: Thẻ cấu hình mới hiển thị trạng thái **Đang hoạt động**, nhãn **Mặc định**, hiển thị đủ 4 bảng dữ liệu liên kết; khi bấm <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra hợp lệ)**, hệ thống thông báo cấu hình hợp lệ 100%.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể giao toàn bộ quy trình từ tra cứu địa giới hành chính, tạo kho xuất hàng, khởi tạo cấu hình bán hàng từ mẫu ngành hàng, kiểm tra tính hợp lệ cho đến kích hoạt cấu hình cho **trợ lý ảo AI Agent** thực hiện tự động.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Setup` (ID: `75e8c472-fbe2-4a26-8e4e-5cdaabdc590d`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Setup` (ID: `b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63`)
- **Quyền hạn tài khoản**: Tài khoản Quản trị viên hoặc Quản lý cửa hàng có quyền thiết lập cấu hình kinh doanh trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Chọn **Tỉnh / Thành phố \*** và **Phường / Xã \*** trong ngăn kéo thêm kho | `getProvinces`, `getWards` | Tra cứu danh mục Tỉnh/Thành phố và Phường/Xã chuẩn 2 cấp để lấy mã địa giới hành chính. |
| Điền thông tin kho và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo kho hàng)** | `createShopAddress`, `getShopAddresses`, `updateShopAddress`, `setDefaultShopAddress`, `deleteMultipleShops` | Tạo mới kho xuất hàng (tự động đồng bộ GPS & GHN), xem danh sách kho, cập nhật hoặc đặt làm kho mặc định. |
| Chọn **Khởi tạo nhanh từ mẫu** hoặc **Chọn bảng có sẵn** ở Bước 1 | `listIndustryTemplates`, `listTables`, `getRolesAndKeys` | Liệt kê các mẫu ngành hàng có sẵn, danh sách bảng dữ liệu động và danh mục các vai trò cột cần ánh xạ. |
| Chọn **Tài khoản ngân hàng nhận thanh toán** ở Bước 3 | `listPaymentIntegrations` | Lấy danh sách các kết nối thanh toán ngân hàng/VietQR/SePay đang hoạt động trong Workspace. |
| Hoàn tất 5 bước và bấm <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo cấu hình mới)** | `createConfiguration`, `updateConfiguration`, `getConfiguration`, `listConfigurations` | Khởi tạo mới hoặc cập nhật toàn diện cấu hình bán hàng (bảng dữ liệu, ánh xạ cột, thanh toán, cọc COD, thông báo). |
| Cấu hình 6 kịch bản tin nhắn ở **Bước 5 (`5. Thông báo`)** | `listOmnichannelTemplates`, `getOmnichannelTemplateDetail`, `createOmnichannelTemplate`, `updateOmnichannelTemplate`, `previewOmnichannelTemplate` | Quản lý và xem trước các mẫu tin nhắn tự động đa kênh gắn với từng sự kiện đơn hàng. |
| Bấm <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra hợp lệ)** và gạt công tắc **Đang hoạt động** | `validateConfiguration`, `enableConfiguration`, `disableConfiguration` | Kiểm tra tính hợp lệ của ánh xạ bảng/cột và bật/tắt trạng thái hoạt động của cấu hình bán hàng. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi thiết lập mới một Kho xuất hàng mặc định và một Cấu hình Bán hàng hoàn chỉnh theo quy trình sau:

1. Bối cảnh và Mục tiêu:
- Tôi cần mở mới một chi nhánh bán lẻ trên RedAI Business, khởi tạo nhanh 4 bảng dữ liệu từ mẫu ngành hàng và bật sẵn thanh toán VietQR + COD.

2. Dữ liệu cung cấp:
- Thông tin Kho hàng:
  + Tên kho: "Kho Trung Tâm TP.HCM"
  + Số điện thoại: "0901234567"
  + Địa chỉ: "123 Nguyễn Huệ", Phường Bến Nghé, TP. Hồ Chí Minh (Đặt làm kho mặc định)
- Thông tin Cấu hình Bán hàng:
  + Mã cấu hình (Code): "STORE_HCM_01"
  + Tên cấu hình: "Cửa Hàng Bán Lẻ TP.HCM"
  + Đơn vị tiền tệ: "VND"
  + Phương thức thanh toán chấp nhận: ["BANK_TRANSFER", "COD"], mặc định: "BANK_TRANSFER"
  + Thời gian giữ hàng chờ thanh toán: 30 phút

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng getProvinces và getWards để tìm đúng mã Tỉnh/Thành phố và Phường/Xã, sau đó gọi createShopAddress để tạo "Kho Trung Tâm TP.HCM" làm kho mặc định.
- Bước 2: Dùng listIndustryTemplates để lấy mẫu ngành hàng phù hợp và dùng listPaymentIntegrations để lấy ID kết nối thanh toán VietQR hiện có.
- Bước 3: Dùng createConfiguration để khởi tạo cấu hình "STORE_HCM_01" gắn với kho mặc định và tài khoản thanh toán vừa tìm được.
- Bước 4: Dùng validateConfiguration và enableConfiguration để kiểm tra tính hợp lệ và kích hoạt cấu hình bán hàng.

4. Yêu cầu phản hồi:
- Báo cáo lại ID kho hàng, ID cấu hình bán hàng, danh sách 4 bảng dữ liệu đã liên kết và kết quả kiểm tra tính hợp lệ (validateConfiguration).
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở trang `/settings` trên ứng dụng **RedAI Business**, kiểm tra thẻ **Cửa Hàng Bán Lẻ TP.HCM** trong tab **Cấu hình Bán hàng** và kho **Kho Trung Tâm TP.HCM** trong tab **Kho hàng & Chi nhánh**. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getConfiguration` và `validateConfiguration` cho cấu hình `STORE_HCM_01` để xác nhận mọi thiết lập đã hoạt động tốt."* |
