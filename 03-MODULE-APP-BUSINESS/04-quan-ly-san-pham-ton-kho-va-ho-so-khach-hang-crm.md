## Mở khu vực Sản phẩm và Khách hàng

Để theo dõi danh mục mặt hàng, giám sát số lượng tồn kho đồng bộ trực tiếp từ Bảng dữ liệu động (`Dynamic Tables`), cũng như tra cứu danh sách khách hàng và **Hồ sơ Khách hàng & CRM 360°**, bạn sử dụng hai mục tương ứng trên thanh điều hướng chính của ứng dụng **RedAI Business**:

1. **Màn hình Sản phẩm (`/products`)**: Bấm vào nút thứ ba <img src="https://api.iconify.design/lucide:boxes.svg?color=%23ff3333" width="16" alt="" /> **(Sản phẩm)** trên thanh điều hướng.
2. **Màn hình Khách hàng (`/customers`)**: Bấm vào nút thứ tư <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **(Khách hàng)** trên thanh điều hướng.

---

## Các tính năng

### Tìm kiếm, lọc và theo dõi KPI Danh mục Sản phẩm & Tồn kho

Tại màn hình **Sản phẩm** (`/products`), bạn có thể kiểm soát tức thì tình trạng hàng hóa trong kho thông qua thanh công cụ và hàng thẻ KPI phía trên:

| Thành phần giao diện | Cách sử dụng & Ý nghĩa hiển thị |
| :--- | :--- |
| **Thanh công cụ lọc Sản phẩm** | • **Bộ chọn `Cấu hình:`** (<img src="https://api.iconify.design/lucide:store.svg?color=%23ff3333" width="16" alt="" />): Chuyển đổi giữa các cấu hình bán hàng để xem bảng sản phẩm tương ứng.<br>• **Ô tìm kiếm** (<img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm sản phẩm)**): Nhập tên mặt hàng hoặc mã SKU (`Tìm theo tên sản phẩm, mã SKU...`) để lọc tức thì.<br>• **Làm mới** (<img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới danh mục sản phẩm)**): Đồng bộ lại tồn kho mới nhất từ Bảng dữ liệu gốc. |
| **Các thẻ chỉ số KPI Tồn kho** | 1. <img src="https://api.iconify.design/lucide:package.svg?color=%23ff3333" width="16" alt="" /> **Tổng Sản Phẩm**: Tổng số mặt hàng hiện có trong danh mục.<br>2. <img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> **Khả Dụng Bán**: Số lượng mặt hàng đang mở bán và còn tồn kho (`> 0`).<br>3. <img src="https://api.iconify.design/lucide:alert-circle.svg?color=%23ff3333" width="16" alt="" /> **Hết Hàng**: Số lượng mặt hàng có tồn kho bằng `0` (cần nhập thêm hàng).<br>4. <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **Ngừng Bán** *(hiển thị khi có mặt hàng tạm khóa)*: Số lượng mặt hàng đang tạm ngưng kinh doanh. |

---

### Tra cứu Bảng Danh Mục Mặt Hàng và Sao chép mã SKU / ID

Bảng **Danh Mục Mặt Hàng** tại `/products` hiển thị chi tiết từng sản phẩm với 6 cột thông tin:

| Cột dữ liệu / Thao tác | Chi tiết hiển thị trên giao diện |
| :--- | :--- |
| **1. Sản phẩm** | Hiển thị ảnh thu nhỏ của mặt hàng (hoặc biểu tượng <img src="https://api.iconify.design/lucide:image.svg?color=%23ff3333" width="16" alt="" />), tên sản phẩm và dòng mô tả ngắn. |
| **2. Mã SKU** | Mã định danh hàng hóa (SKU) phục vụ tìm kiếm và quét mã nhanh. |
| **3. Đơn giá** | Giá bán lẻ niêm yết theo đơn vị tiền tệ của cấu hình bán hàng. |
| **4. Tồn kho** | Số lượng tồn kho thực tế hiện tại trong Bảng Sản phẩm. |
| **5. Trạng thái** | Tự động gắn nhãn màu trực quan theo số lượng tồn kho và trạng thái mở bán:<br>• **Còn hàng** (Xanh lá): Tồn kho dồi dào.<br>• **Sắp hết** (Vàng cam): Tồn kho chạm ngưỡng cảnh báo thấp.<br>• **Hết hàng** (Đỏ): Tồn kho bằng `0`.<br>• **Ngừng bán** (Xám): Mặt hàng đang bị khóa trạng thái bán. |
| **6. Thao tác** (<img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" />) | Bấm vào nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> ở cuối dòng sản phẩm để mở menu tiện ích nhanh:<br>• <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép SKU)**: Sao chép mã SKU của sản phẩm.<br>• <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép ID)**: Sao chép mã định danh bản ghi (`recordId`) của sản phẩm để dùng khi cấu hình quy tắc đặt cọc riêng hoặc giới hạn sản phẩm áp dụng Voucher. |

---

### Tìm kiếm, lọc và theo dõi KPI Danh sách Khách hàng CRM

Khi chuyển sang màn hình **Khách hàng** (`/customers`), phần đầu trang cung cấp thanh công cụ lọc và **3 thẻ KPI tổng hợp**:

| Thành phần giao diện | Cách sử dụng & Ý nghĩa hiển thị |
| :--- | :--- |
| **Thanh công cụ lọc Khách hàng** | • **Bộ chọn `Cấu hình:`** (<img src="https://api.iconify.design/lucide:store.svg?color=%23ff3333" width="16" alt="" />): Chọn xem tệp khách hàng của **Tất cả ({số lượng})** hoặc từng cấu hình bán hàng riêng biệt.<br>• **Ô tìm kiếm** (<img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm khách hàng)**): Tìm nhanh theo tên, số điện thoại, email hoặc địa chỉ (`Tìm tên, SĐT, email, địa chỉ...`).<br>• **Làm mới** (<img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới dữ liệu)**): Cập nhật lại danh sách khách hàng và số liệu tích lũy. |
| **3 Thẻ chỉ số KPI Khách hàng** | 1. <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Tổng khách hàng**: Tổng số hồ sơ khách hàng trong hệ thống CRM.<br>2. <img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> **Tổng đơn tích lũy**: Tổng số đơn hàng đã mua của toàn bộ tệp khách hàng.<br>3. <img src="https://api.iconify.design/lucide:credit-card.svg?color=%23ff3333" width="16" alt="" /> **Tổng chi tiêu toàn khách**: Tổng giá trị chi tiêu tích lũy của toàn bộ khách hàng. |

---

### Khai thác Bảng Khách hàng, Hồ sơ Khách hàng 360° và Lịch sử Đơn hàng

Bảng danh sách tại màn hình `/customers` gồm 9 cột (`#`, `Khách hàng`, `Số điện thoại`, `Email`, `Địa chỉ`, `Số đơn`, `Tổng chi tiêu`, `Lần mua cuối`, `Hành động`):

| Tính năng | Cách thực hiện |
| :--- | :--- |
| **Sao chép nhanh Số điện thoại và Email** | Ngay bên cạnh số điện thoại (ở cột `Số điện thoại`) và địa chỉ thư điện tử (ở cột `Email`) của mỗi khách hàng đều có nút biểu tượng <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> để bạn sao chép nhanh thông tin liên hệ chỉ với 1 cú nhấp chuột. |
| **Xem chi tiết Hồ sơ Khách hàng & CRM 360°** | 1. Nhấp trực tiếp vào dòng khách hàng hoặc bấm nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> ở cột **Hành động** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **(Xem chi tiết hồ sơ)**.<br>2. Hộp thoại **Hồ sơ Khách hàng & CRM** sẽ mở ra hiển thị:<br>   • Thông tin định danh, nhãn xếp hạng **Khách hàng thân thiết**, số điện thoại, email, địa chỉ.<br>   • 3 ô thống kê nổi bật: **Tổng số đơn**, **Tổng chi tiêu** và **Lần mua cuối**.<br>   • Khối **Chi tiết dữ liệu hồ sơ gốc**: Hiển thị toàn bộ các trường thông tin chi tiết được lưu trong Bảng Khách hàng.<br>   • Nút <img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> **(Tra cứu lịch sử đơn hàng)** ở chân hộp thoại. |
| **Tra cứu toàn bộ Lịch sử đơn hàng của một khách** | Bấm nút <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> ở cột **Hành động** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> **(Xem lịch sử đơn hàng)** (hoặc bấm nút **Tra cứu lịch sử đơn hàng** từ trong hộp thoại hồ sơ). Hệ thống sẽ chuyển thẳng sang trang `/orders` và tự động lọc riêng toàn bộ đơn hàng của số điện thoại khách đó. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tra cứu thông tin sản phẩm, kiểm tra cấu trúc trường dữ liệu hàng hóa, thống kê tồn kho cũng như quản lý sổ địa chỉ và hồ sơ khách hàng hoàn toàn tự động.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Để tra cứu, tìm kiếm và thống kê Sản phẩm & Địa chỉ khách đang chat**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Operations` (ID: `0a1c2aec-78f6-419c-8e70-d7ce019ba210`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Operations` (ID: `b736f624-fb7e-425d-9e3b-6e216887604d`)
- **Để quản trị toàn bộ danh sách Khách hàng & Sổ địa chỉ CRM**:
  - **Kỹ năng (Skill) cần trang bị**: `RedAI - Business Setup` (ID: `75e8c472-fbe2-4a26-8e4e-5cdaabdc590d`)
  - **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Business Setup` (ID: `b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63`)
- **Quyền hạn tài khoản**: Tài khoản nhân viên bán hàng hoặc quản lý cửa hàng trong Workspace.

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Tìm kiếm sản phẩm, xem chi tiết mặt hàng và cấu trúc cột Sản phẩm

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Tìm kiếm tại ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm sản phẩm)** và xem bảng **Danh Mục Mặt Hàng** trên trang `/products` |
| **Công cụ Agent sử dụng** | `searchCommerceProducts`, `getCommerceProductDetail`, `getCommerceProductFields` *(Skill `RedAI - Business Operations`)* |
| **Thông tin cần cung cấp** | Từ khóa tên sản phẩm, mã SKU, khoảng giá hoặc ID sản phẩm cần xem chi tiết |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ searchCommerceProducts để tìm tất cả các sản phẩm có từ khóa "[Tên sản phẩm]", sau đó dùng getCommerceProductDetail để hiển thị chi tiết đơn giá, mã SKU và số lượng tồn kho của từng mặt hàng.
```

#### 2. Thống kê tổng hợp số liệu Sản phẩm & Tồn kho (`Aggregate Products`)

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Theo dõi các thẻ KPI **Tổng Sản Phẩm**, **Khả Dụng Bán**, **Hết Hàng** trên trang `/products` |
| **Công cụ Agent sử dụng** | `aggregateCommerceProducts` *(Skill `RedAI - Business Operations`)* |
| **Thông tin cần cung cấp** | Tiêu chí gom nhóm hoặc thống kê (tổng số mặt hàng, tổng tồn kho, giá trung bình...) |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ aggregateCommerceProducts để tính tổng số lượng sản phẩm khả dụng bán và liệt kê các sản phẩm có tồn kho dưới 5 đơn vị để tôi lên kế hoạch nhập hàng.
```

#### 3. Tra cứu và quản lý Hồ sơ & Sổ địa chỉ Khách hàng CRM

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Tra cứu trên bảng `/customers` và mở hộp thoại **Hồ sơ Khách hàng & CRM** |
| **Công cụ Agent sử dụng** | • Trên `RedAI - Business Setup`: `getCustomerAddressesPaginated`, `getCustomerAddresses`, `getCustomerAddressById`, `getDefaultUserAddress`, `createCustomerAddress`, `updateCustomerAddress`, `setDefaultCustomerAddress`, `deleteCustomerAddress`<br>• Trên `RedAI - Business Operations`: `getCurrentCustomerAddress`, `saveCustomerAddress` |
| **Thông tin cần cung cấp** | Tên khách hàng, số điện thoại, địa chỉ giao hàng (Tỉnh/Thành phố, Phường/Xã, địa chỉ chi tiết) |

**Câu lệnh mẫu (Prompt):**

```text
Hãy dùng công cụ getCustomerAddressesPaginated để tìm hồ sơ khách hàng có số điện thoại "0987654321", hoặc dùng createCustomerAddress để lưu mới địa chỉ giao hàng mặc định cho khách hàng này.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở trang `/products` hoặc `/customers` trên ứng dụng **RedAI Business**, bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **(Làm mới)** để đối chiếu danh mục sản phẩm và hồ sơ khách hàng. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getCustomerAddresses` cho khách hàng vừa lưu để xác nhận địa chỉ mặc định đã được cập nhật chính xác."* |
