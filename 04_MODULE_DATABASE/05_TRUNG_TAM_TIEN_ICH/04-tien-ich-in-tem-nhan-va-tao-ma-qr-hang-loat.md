## Tổng quan Tiện ích In Tem Nhãn & Tạo Mã QR Hàng Loạt

Tiện ích **In Tem Nhãn & Tạo Mã QR Hàng Loạt** là giải pháp tự động hóa kết nối giữa dữ liệu số trên **RedAI Database** với môi trường vật lý. Tiện ích tự động tạo mã QR hai chiều sắc nét (định dạng vector SVG) từ liên kết bản ghi, mã định danh duy nhất hoặc bất kỳ trường thông tin nào trong bảng, hỗ trợ các bố cục dàn trang in tiêu chuẩn văn phòng (A4) hoặc máy in mã vạch nhiệt chuyên dụng (Decal cuộn) và cung cấp tùy chọn xuất file nén ZIP chứa toàn bộ ảnh QR độc lập.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Phạm vi áp dụng** | • <img src="https://api.iconify.design/lucide:check-square.svg?color=%23ff3333" width="16" alt="" /> **Chỉ áp dụng cho {N} bản ghi đang chọn:** | Chỉ in tem cho các dòng đang được tích chọn ngoài bảng tính. |
| | • <img src="https://api.iconify.design/lucide:table.svg?color=%23ff3333" width="16" alt="" /> **Áp dụng cho toàn bộ bản ghi trong Dạng xem:** | In ấn hàng loạt cho toàn bộ dòng dữ liệu của View hiện tại (hỗ trợ tối đa 100 tem/đợt). |
| **2. Nguồn dữ liệu mã hóa QR** | **Menu chọn nguồn mã hóa** | • `🔗 Link trực tiếp tới bản ghi (__RECORD_URL__)`: Quét mã bằng camera điện thoại sẽ mở trực tiếp trang chi tiết bản ghi trên nền tảng RedAI.<br>• `🆔 Mã ID bản ghi (__RECORD_ID__)`: Mã hóa chuỗi định danh duy nhất của dòng dữ liệu.<br>• `Cột dữ liệu tùy chọn`: Chọn bất kỳ cột nào trong bảng (ví dụ: Cột `Mã sản phẩm`, `Số điện thoại`, `Số CCCD`, `Số Serial`, `Link thanh toán`). |
| **3. Cấu hình chữ hiển thị trên tem** | • **Tiêu đề trên tem (Dòng chữ trên):** | Chọn trường hiển thị chữ in đậm ở phía trên mã QR (ví dụ: `Tên sản phẩm`, `Họ và tên khách hàng`). |
| | • **Thông tin phụ dưới tem (Dòng chữ dưới):** | Chọn trường hiển thị thông tin bổ trợ phía dưới mã QR (ví dụ: `Đơn giá`, `Hotline`, `Ngày hết hạn`). |
| **4. Bố cục dàn trang in ấn** | • <img src="https://api.iconify.design/lucide:grid.svg?color=%23ff3333" width="16" alt="" /> **Lưới A4 (3 cột x nhiều dòng):** | Căn chỉnh vừa khít khổ giấy A4 văn phòng tiêu chuẩn, 3 tem trên một hàng ngang. |
| | • <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **Tem nhãn đơn (Decal Sticker):** | Dành riêng cho máy in mã vạch nhiệt dạng cuộn hoặc giấy decal bóc dán từng con tem. |
| | • <img src="https://api.iconify.design/lucide:credit-card.svg?color=%23ff3333" width="16" alt="" /> **Thẻ thông tin (2 cột):** | Bố cục dạng thẻ chữ nhật nằm ngang kèm thông tin mở rộng, phù hợp làm thẻ nhân viên hoặc thẻ kiểm kê kho bãi. |
| **5. Khung xem trước trực tiếp (Live Preview)** | **Mô phỏng bản in thực tế** | Hiển thị chính xác kích thước con tem, độ sắc nét của mã QR và các dòng chữ đã cấu hình. |
| **6. Phương thức xuất kết quả** | • <img src="https://api.iconify.design/lucide:printer.svg?color=%23ff3333" width="16" alt="" /> **Nút 'In tem nhãn'** | Kích hoạt lệnh in của trình duyệt (`window.print()`), mở hộp thoại in của hệ điều hành. |
| | • <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **Nút 'Tải file ZIP ảnh QR'** | Đóng gói toàn bộ các mã QR dưới dạng tệp ảnh vector `.svg` độc lập được nén trong file `.zip`. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Hộp thoại In Tem Nhãn & Tạo Mã QR]
                  │
                  ▼
[Chọn Phạm vi (Dòng đang chọn vs Toàn bộ View)]
                  │
                  ▼
[Chọn Nguồn dữ liệu mã hóa QR (Link bản ghi / ID / Cột)]
                  │
                  ▼
[Chọn Tiêu đề trên & Thông tin phụ dưới con tem]
                  │
                  ▼
[Chọn Bố cục dàn trang (Lưới A4 / Decal đơn / Thẻ 2 cột)]
                  │
                  ▼
[Quan sát Khung Xem trước trực tiếp (Live Preview)]
                  │
     ┌────────────┴────────────┐
     ▼                         ▼
[Bấm "In tem nhãn"]     [Bấm "Tải file ZIP ảnh QR"]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:printer.svg?color=%23ff3333" width="16" alt="" /> **In Tem Nhãn & Tạo Mã QR Hàng Loạt**. |
| **2** | **Cấu hình nguồn và văn bản** | Chọn nguồn mã hóa (ví dụ: chọn cột `Mã sản phẩm`), sau đó chọn tiêu đề trên tem là `Tên sản phẩm` và thông tin phụ dưới tem là `Giá bán`. |
| **3** | **Chọn bố cục in** | Chọn `Lưới A4 (3 cột)` nếu dùng máy in văn phòng, hoặc chọn `Tem nhãn đơn (Decal Sticker)` nếu dùng máy in tem nhãn cuộn nhiệt. |
| **4** | **Kiểm tra bản in xem trước** | Quan sát các con tem trong khung Live Preview, dùng camera điện thoại quét thử trực tiếp trên màn hình máy tính để kiểm chứng. |
| **5** | **Thực hiện in hoặc tải file** | Nhấp nút **In tem nhãn** để mở hộp thoại in, chọn máy in đích và bấm **In**; hoặc nhấp **Tải file ZIP ảnh QR** để lưu trữ kho ảnh mã vạch trên máy tính. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Quét thử mã QR thực tế** | Sử dụng camera điện thoại hoặc máy quét mã vạch chuyên dụng quét thử: mã đọc được ngay lập tức, hiển thị đúng đường dẫn hoặc mã số tương ứng. |
| **Bố cục trang in** | Khi mở hộp thoại in của trình duyệt, các con tem dàn đều theo đúng khổ giấy đã chọn, không bị tràn viền hoặc cắt cụt văn bản. |
| **File ZIP tải về** | Mở file `.zip`, bên trong chứa đầy đủ các file `.svg` được đặt tên chuẩn xác theo mã định danh của từng bản ghi. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền đọc và xuất dữ liệu (`RECORD_READ`, `RECORD_EXPORT`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Trích xuất dữ liệu để chuẩn bị in mã QR sản phẩm** | `listRecords` | *"Hãy truy vấn danh sách 50 sản phẩm mới nhất trong bảng 'Sản Phẩm', lấy mã sản phẩm, tên sản phẩm và đơn giá để xuất danh sách in tem nhãn."* |
| **Lấy đường link trực tiếp của các bản ghi để mã hóa** | `listRecords` | *"Hãy lấy danh sách các đơn hàng có trạng thái 'Đang giao' trong bảng 'Đơn Hàng', tạo danh sách liên kết trực tiếp tới từng bản ghi phục vụ in mã QR dán lên kiện hàng."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Xem trước danh sách tem in trên giao diện | Gọi `listRecords` thấy các trường thông tin trên từng con tem khớp hoàn toàn với dữ liệu trả về từ tool. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent truy vấn danh sách bản ghi | Mở tiện ích In tem nhãn trên Grid View, các con tem hiển thị đúng danh sách dòng dữ liệu tương ứng. |
