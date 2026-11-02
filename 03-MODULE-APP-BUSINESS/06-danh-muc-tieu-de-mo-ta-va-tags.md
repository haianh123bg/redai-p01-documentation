## App Business - Quy trình thiết lập cấu hình bán hàng 5 bước và quản lý kho hàng

**Tên file:** `01-quy-trinh-thiet-lap-cau-hinh-ban-hang-5-buoc-va-quan-ly-kho-hang.md`

**Tiêu đề:** App Business - Quy trình thiết lập cấu hình bán hàng 5 bước và quản lý kho hàng

**Mô tả:** Hướng dẫn thiết lập hệ thống cửa hàng tại trang `/settings` với 2 tab chính: quản lý `Kho hàng & Chi nhánh` (địa chỉ hành chính **2 cấp Tỉnh/Thành phố $\rightarrow$ Phường/Xã**, tự động đồng bộ tọa độ GPS & `GHN Shop ID`) và khởi tạo `Cấu hình Bán hàng` qua trình thuật sĩ 5 bước (`1. Cơ bản` chọn từ mẫu ngành hàng hoặc bảng có sẵn; `2. Ánh xạ cột` tự động khớp gợi ý 4 bảng; `3. Thanh toán & Kho bãi` cấu hình VietQR, COD, thời gian giữ hàng; `4. Cọc COD` theo `%`, số tiền cố định và quy tắc riêng từng sản phẩm; `5. Thông báo` gắn 6 kịch bản tin nhắn đa kênh Omnichannel Templates), kèm hướng dẫn điều khiển qua trợ lý ảo AI Agent với kỹ năng `RedAI - Business Setup`.

**Agent nên truy xuất khi:** Người dùng muốn thêm kho xuất hàng mới, tạo hoặc chỉnh sửa Cấu hình Bán hàng 5 bước, khởi tạo nhanh 4 bảng dữ liệu bán lẻ từ mẫu ngành hàng, ánh xạ cột dữ liệu, cài đặt thanh toán VietQR/COD, quy tắc đặt cọc COD hoặc mẫu tin nhắn thông báo đơn hàng tự động.

**Không dùng khi:** Người dùng chỉ muốn tạo đơn hàng bán lẻ hàng ngày, xem biểu đồ doanh thu hoặc tra cứu danh sách sản phẩm/khách hàng.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:warehouse.svg?color=%23ff3333" width="16" alt="" /> Thêm Kho Hàng Mới (Địa chỉ 2 cấp Tỉnh/Thành phố → Phường/Xã) → tự động đồng bộ → GPS & GHN Shop ID`; `<img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> Khởi tạo nhanh từ mẫu → tự động sinh & ánh xạ → 4 Bảng dữ liệu (Đơn hàng, Chi tiết đơn, Sản phẩm, Khách hàng)`; `Trình thuật sĩ 5 bước (createConfiguration) → thiết lập → Ánh xạ cột + Thanh toán VietQR/COD + Cọc COD + 6 Kịch bản Omnichannel Templates`; `Kỹ năng RedAI - Business Setup (75e8c472-fbe2-4a26-8e4e-5cdaabdc590d) → thực thi → Bộ công cụ thiết lập bán lẻ (b5722b13-7dc5-4f6c-aa25-d0f6b64e7e63)`.

**Tags (10):** `app-business/thiet-lap-cua-hang`, `app-business/cau-hinh-ban-hang`, `app-business/kho-hang-chi-nhanh`, `app-business/dia-chi-2-cap`, `app-business/khoi-tao-tu-mau`, `app-business/anh-xa-cot`, `app-business/thanh-toan-vietqr`, `app-business/coc-cod`, `app-business/omnichannel-templates`, `app-business/business-setup`

---

## App Business - Quy trình tạo và xử lý vòng đời đơn hàng bán lẻ

**Tên file:** `02-quy-trinh-tao-va-xu-ly-vong-doi-don-hang-ban-le.md`

**Tiêu đề:** App Business - Quy trình tạo và xử lý vòng đời đơn hàng bán lẻ

**Mô tả:** Hướng dẫn quy trình tạo đơn hàng mới tại `/orders` qua hộp thoại `Tạo Đơn Hàng Bán Lẻ Mới` (chọn `Cấu Hình Bán Hàng`, điền nhanh từ `Khách quen CRM` hoặc nhập `Họ và tên`, `Số điện thoại`, `Email`, `Phương thức thanh toán` COD/Chuyển khoản, `Địa chỉ giao hàng`, chọn mặt hàng tại `Thêm sản phẩm từ kho` và `Ghi chú đơn hàng`); xử lý vòng đời đơn hàng qua 5 nút hành động trực tiếp trên dòng đơn (`Mã VietQR chuyển khoản`, `Xem chi tiết đơn`, `Duyệt chốt đơn`, `Cập nhật mã vận đơn` GHN/GHTK/Viettel Post/J&T/Nội bộ, và `Hủy đơn hàng` tự động hoàn kho), kèm hướng dẫn thao tác qua trợ lý ảo AI Agent với cả 2 kỹ năng `RedAI - Business Operations` và `RedAI - Business Setup`.

**Agent nên truy xuất khi:** Người dùng muốn lên đơn hàng mới cho khách, xuất mã thanh toán `VietQR`, xem chi tiết đơn hàng, duyệt chốt đơn (`Chờ xác nhận` $\rightarrow$ `Đã xác nhận`), cập nhật mã vận đơn giao hàng (`Đang giao`) hoặc hủy đơn hoàn tồn kho (`Đã hủy`).

**Không dùng khi:** Người dùng chỉ muốn cấu hình 5 bước thiết lập cửa hàng, tạo mã giảm giá Voucher hoặc xem biểu đồ phân khúc khách hàng RFM.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> Tạo đơn hàng mới (quickCreateOrder / createBusinessOrder) → trừ giữ chỗ tồn kho & khởi tạo → Đơn hàng Chờ xác nhận`; `<img src="https://api.iconify.design/lucide:qr-code.svg?color=%23ff3333" width="16" alt="" /> Mã VietQR chuyển khoản (getOrderQrPayment) → sinh mã QR động nhúng sẵn → Số tiền & Nội dung chuyển khoản`; `<img src="https://api.iconify.design/lucide:check-circle-2.svg?color=%23ff3333" width="16" alt="" /> Duyệt chốt đơn (confirmBusinessOrder) → chuyển trạng thái sang → Đã xác nhận`; `<img src="https://api.iconify.design/lucide:truck.svg?color=%23ff3333" width="16" alt="" /> Cập nhật mã vận đơn (updateBusinessOrderShipping) → chuyển trạng thái sang → Đang giao`; `<img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> Hủy đơn hàng (cancelBusinessOrder) → hoàn trả tồn kho & chuyển sang → Đã hủy`.

**Tags (10):** `app-business/quan-ly-don-hang`, `app-business/tao-don-hang-moi`, `app-business/khach-quen-crm`, `app-business/ma-vietqr-chuyen-khoan`, `app-business/duyet-chot-don`, `app-business/cap-nhat-ma-van-don`, `app-business/huy-don-hoan-kho`, `app-business/vong-doi-don-hang`, `app-business/business-operations`, `app-business/quick-create-order`

---

## App Business - Quản lý tổng quan doanh nghiệp và phân tích khách hàng RFM

**Tên file:** `03-quan-ly-tong-quan-doanh-nghiep-va-phan-tich-khach-hang-rfm.md`

**Tiêu đề:** App Business - Quản lý tổng quan doanh nghiệp và phân tích khách hàng RFM

**Mô tả:** Hướng dẫn khai thác bảng điều khiển `/home` với bộ lọc `Cấu hình:` và `Thời gian:` (`Hôm nay`, `7 ngày qua`, `30 ngày qua`, `Từ - Đến`); theo dõi 5 thẻ KPI chiến lược (`Doanh Thu Thực Thu`, `Tổng Số Đơn Hàng`, `Tỷ Lệ Thanh Toán`, `Danh Mục Kho`, `Voucher Đang Chạy`); phân tích 4 biểu đồ kinh doanh (`Xu Hướng Doanh Thu Bán Lẻ`, `Cơ Cấu Trạng Thái Đơn`, `Hiệu Quả Từng Cấu Hình / Chi Nhánh`, `Cơ Cấu Phương Thức Thanh Toán`); khai thác khối `Phân Tích & Thống Kê Khách Hàng` với 4 chỉ số CRM, biểu đồ `Phân Khúc Khách Hàng (RFM)` (`Khách VIP`, `Thân thiết`, `Tiềm năng`, `Khách mới`), bảng `Top Khách Hàng Chi Tiêu & Gắn Bó Nhất` và `Đơn Hàng Gần Đây`, kèm hướng dẫn tổng hợp báo cáo qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn xem báo cáo tổng quan doanh thu, số lượng đơn hàng, tỷ lệ thanh toán, so sánh hiệu quả giữa các chi nhánh hoặc phân tích tệp khách hàng theo mô hình RFM (`Khách VIP`, `Thân thiết`, `Tiềm năng`, `Khách mới`).

**Không dùng khi:** Người dùng muốn xem hướng dẫn chi tiết từng bước cài đặt kho hàng hoặc tạo mã giảm giá mới.

**Thực thể và quan hệ:** `Bộ lọc Cấu hình & Thời gian → lọc dữ liệu thời gian thực cho → 5 Thẻ KPI Chiến lược & 4 Biểu đồ Kinh doanh`; `Khối Phân Tích & Thống Kê Khách Hàng → phân nhóm tự động theo mô hình RFM thành → Khách VIP, Thân thiết, Tiềm năng, Khách mới`; `Công cụ getBusinessOrdersStatistics & aggregateCommerceProducts → tổng hợp số liệu báo cáo cho → Trợ lý ảo AI Agent`.

**Tags (10):** `app-business/tong-quan-doanh-nghiep`, `app-business/doanh-thu-thuc-thu`, `app-business/ty-le-thanh-toan`, `app-business/xu-huong-doanh-thu`, `app-business/hieu-qua-chi-nhanh`, `app-business/phan-tich-khach-hang`, `app-business/phan-khuc-rfm`, `app-business/khach-vip`, `app-business/top-khach-hang`, `app-business/thong-ke-ai-agent`

---

## App Business - Quản lý sản phẩm tồn kho và hồ sơ khách hàng CRM

**Tên file:** `04-quan-ly-san-pham-ton-kho-va-ho-so-khach-hang-crm.md`

**Tiêu đề:** App Business - Quản lý sản phẩm tồn kho và hồ sơ khách hàng CRM

**Mô tả:** Hướng dẫn tra cứu danh mục hàng hóa tại `/products` với các thẻ KPI tồn kho (`Tổng Sản Phẩm`, `Khả Dụng Bán`, `Hết Hàng`, `Ngừng Bán`), bảng `Danh Mục Mặt Hàng` 6 cột và menu tiện ích `Sao chép SKU` / `Sao chép ID`; quản lý danh sách khách hàng tại `/customers` với 3 thẻ KPI (`Tổng khách hàng`, `Tổng đơn tích lũy`, `Tổng chi tiêu toàn khách`), bảng khách hàng 9 cột, hộp thoại `Hồ sơ Khách hàng & CRM` (xem toàn bộ trường dữ liệu gốc) và tính năng chuyển hướng tra cứu `Xem lịch sử đơn hàng` theo số điện thoại, kèm hướng dẫn thao tác qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng cần tìm kiếm sản phẩm, kiểm tra số lượng tồn kho, sao chép mã SKU/ID sản phẩm, tra cứu thông tin liên hệ khách hàng, xem Hồ sơ Khách hàng 360°, quản lý sổ địa chỉ giao hàng hoặc xem lịch sử mua hàng của một khách.

**Không dùng khi:** Người dùng chỉ muốn thiết lập cấu hình cửa hàng 5 bước hoặc phát hành chương trình khuyến mãi Voucher.

**Thực thể và quan hệ:** `Trang Sản phẩm (/products) → đồng bộ trực tiếp tồn kho & trạng thái từ → Bảng Sản phẩm (Dynamic Table)`; `Menu Thao tác trên dòng sản phẩm → sao chép nhanh → Mã SKU & Bản ghi ID`; `Trang Khách hàng (/customers) + Xem chi tiết hồ sơ → hiển thị → Hồ sơ Khách hàng & CRM 360°`; `<img src="https://api.iconify.design/lucide:shopping-bag.svg?color=%23ff3333" width="16" alt="" /> Xem lịch sử đơn hàng → lọc toàn bộ đơn theo SĐT tại → Trang Đơn hàng (/orders)`.

**Tags (10):** `app-business/san-pham-ton-kho`, `app-business/danh-muc-mat-hang`, `app-business/sao-chep-sku`, `app-business/canh-bao-het-hang`, `app-business/khach-hang-crm`, `app-business/ho-so-khach-hang`, `app-business/lich-su-don-hang`, `app-business/so-dia-chi-khach`, `app-business/search-commerce-products`, `app-business/aggregate-products`

---

## App Business - Quy trình tạo và quản lý chương trình khuyến mãi Voucher

**Tên file:** `05-quy-trinh-tao-va-quan-ly-chuong-trinh-khuyen-mai-voucher.md`

**Tiêu đề:** App Business - Quy trình tạo và quản lý chương trình khuyến mãi Voucher

**Mô tả:** Hướng dẫn khởi tạo và vận hành chương trình khuyến mãi tại `/vouchers` qua ngăn kéo `Tạo Mã Giảm Giá Mới` gồm 5 khối thiết lập (`Phạm Vi & Cấu Hình Áp Dụng`; `Mức Giảm Giá & Điều Kiện Đơn Hàng` với **3 loại giảm giá**: `Giảm theo tỷ lệ phần trăm (%)`, `Giảm số tiền cố định (VNĐ)`, `Miễn phí vận chuyển (Free Shipping)`; `Giới Hạn Lượt Dùng & Cơ Chế Chống Spam (Anti-Fraud)` theo `Số Điện Thoại (PHONE)` hoặc `Phiên Chat (CONVERSATION)`; `Thời Gian Bắt Đầu & Hết Hạn Hiệu Lực`; và `Phạm Vi Sản Phẩm Áp Dụng` `ALL` / `APPLICABLE` / `EXCLUDED`), cùng thao tác bật/tắt nhanh `Switch`, chỉnh sửa và xóa Voucher trên danh sách, kèm hướng dẫn điều khiển qua trợ lý ảo AI Agent.

**Agent nên truy xuất khi:** Người dùng muốn tạo mã giảm giá mới (theo `%`, số tiền cố định hoặc miễn phí vận chuyển), cài đặt giới hạn lượt dùng chống spam theo SĐT/Phiên chat, giới hạn sản phẩm được áp dụng mã, bật/tắt nhanh Voucher hoặc kiểm tra tính hợp lệ của mã giảm giá trên đơn hàng.

**Không dùng khi:** Người dùng chỉ muốn tạo kho xuất hàng, cập nhật mã vận đơn giao hàng hoặc xem báo cáo RFM.

**Thực thể và quan hệ:** `<img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> Tạo Voucher Mới (createCommerceVoucher) → thiết lập → 3 Loại giảm giá (%, VNĐ, Free Shipping) + Limit Mode (PHONE / CONVERSATION) + Phạm vi sản phẩm (ALL / APPLICABLE / EXCLUDED)`; `Công tắc Switch trên bảng Voucher (toggleCommerceVoucherActive) → bật/tắt tức thì → Trạng thái kích hoạt của mã giảm giá`; `Công cụ validateCommerceVoucher → kiểm tra điều kiện & tính số tiền giảm cho → Giỏ hàng của khách`.

**Tags (10):** `app-business/quan-ly-voucher`, `app-business/tao-ma-giam-gia`, `app-business/mien-phi-van-chuyen`, `app-business/chong-spam-voucher`, `app-business/limit-mode-phone`, `app-business/pham-vi-san-pham`, `app-business/bat-tat-voucher`, `app-business/kiem-tra-voucher`, `app-business/create-commerce-voucher`, `app-business/validate-commerce-voucher`

---

## Định tuyến nhanh

| Ý định truy vấn | Tài liệu ưu tiên |
| :--- | :--- |
| Thêm kho xuất hàng (địa chỉ 2 cấp), khởi tạo Cấu hình Bán hàng 5 bước, ánh xạ 4 bảng dữ liệu, cài đặt VietQR/COD, Cọc COD và Tin nhắn tự động | **01-quy-trinh-thiet-lap-cau-hinh-ban-hang-5-buoc-va-quan-ly-kho-hang.md** |
| Tạo đơn hàng bán lẻ mới, xuất mã thanh toán VietQR, xem chi tiết đơn, duyệt chốt đơn, cập nhật mã vận đơn giao hàng và hủy đơn hoàn kho | **02-quy-trinh-tao-va-xu-ly-vong-doi-don-hang-ban-le.md** |
| Xem bảng điều khiển Tổng quan Doanh nghiệp, 5 thẻ KPI, 4 biểu đồ kinh doanh và phân tích phân khúc khách hàng theo mô hình RFM | **03-quan-ly-tong-quan-doanh-nghiep-va-phan-tich-khach-hang-rfm.md** |
| Tra cứu danh mục Sản phẩm & Tồn kho, sao chép SKU/ID, quản lý danh sách Khách hàng, xem Hồ sơ Khách hàng 360° và lịch sử đơn hàng | **04-quan-ly-san-pham-ton-kho-va-ho-so-khach-hang-crm.md** |
| Tạo chương trình khuyến mãi & mã giảm giá Voucher (`%`, `VNĐ`, `Free Shipping`), cấu hình chống spam, giới hạn sản phẩm và bật/tắt Voucher | **05-quy-trinh-tao-va-quan-ly-chuong-trinh-khuyen-mai-voucher.md** |
