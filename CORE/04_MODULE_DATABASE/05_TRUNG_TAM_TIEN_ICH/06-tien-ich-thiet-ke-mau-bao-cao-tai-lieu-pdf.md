## Tổng quan Tiện ích Xuất báo cáo Tài liệu mẫu (PDF Template Designer)

Tiện ích **Xuất báo cáo Tài liệu mẫu (PDF Template Designer)** là công cụ xuất bản tài liệu tự động cao cấp trên **RedAI Database**. Cho phép doanh nghiệp tải lên các tệp PDF biểu mẫu có sẵn (hợp đồng pháp lý, biên bản giao nhận, hóa đơn, giấy chứng nhận), sử dụng trình thiết kế trực quan kéo thả các biến dữ liệu từ Bảng Động hoặc biến tự do vào đúng vị trí tọa độ trên trang giấy, tinh chỉnh font chữ tiếng Việt chuẩn xác và xuất tài liệu PDF hàng loạt cho từng dòng dữ liệu chỉ bằng 1 cú nhấp chuột.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Thanh công cụ định danh mẫu** | • **Bảng dữ liệu nguồn:** | Xác nhận bảng dữ liệu đang kết nối (hỗ trợ chuyển đổi sang bảng khác trong cùng Không gian làm việc). |
| | • **Tên mẫu báo cáo:** | Ô nhập tên định danh tài liệu (ví dụ: `Hợp Đồng Thuê Văn Phòng 2026`). |
| | • **Menu Phân loại:** | Phân nhóm tài liệu vào 6 danh mục: `Hợp đồng pháp lý`, `Phiếu giao nhận / Kho`, `Hóa đơn / Biên nhận`, `Báo cáo tổng hợp`, `Chứng chỉ / Chứng nhận`, `Mẫu chung`. |
| | • <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **Tải lên PDF biểu mẫu:** | Chọn tệp `.pdf` mẫu có sẵn từ máy tính hoặc kho tài nguyên số để làm nền tài liệu. |
| **2. Cột Danh sách Biến dữ liệu (Bên trái)** | • **BIẾN TỪ BẢNG DỮ LIỆU:** | Liệt kê toàn bộ các cột trong bảng (ví dụ: `Họ và tên`, `Số điện thoại`, `Địa chỉ`, `Số tiền`, `Mã số thuế`). Nhấp giữ chuột vào biến và kéo thả vào vị trí dòng trên trang PDF. |
| | • **BIẾN TỰ DO (TỰ ĐẶT):** | Bấm `+ Thêm biến tự do` để tạo các trường thông tin không có trong bảng (ví dụ: `Số hợp đồng`, `Ngày lập biên bản`, `Đại diện bên B`). Các biến này sẽ yêu cầu người dùng nhập giá trị khi bấm xuất PDF. |
| **3. Thanh tinh chỉnh thuộc tính biến** | • **Kiểu hiển thị (Field Type):** | Lựa chọn định dạng xuất:<br>• `Văn bản (Text)`: Chuỗi chữ thông thường.<br>• `Số (Number)`: Định dạng số học.<br>• `Tiền tệ (Currency)`: Tự động phân tách dấu chấm hàng nghìn và thêm hậu tố `VNĐ`.<br>• `Ngày tháng (Date)`: Định dạng ngày theo chuẩn `DD/MM/YYYY`.<br>• `Mã QR (QR Code)`: Tự động chuyển giá trị của biến thành mã hình học QR Code hai chiều in trực tiếp lên trang giấy.<br>• `Chữ ký điện tử (Signature)`: Khung chèn chữ ký số hoặc ảnh chữ ký scan. |
| | • **Phông chữ tiếng Việt:** | Hỗ trợ đầy đủ các bộ font vector hỗ trợ chuẩn tiếng Việt (Roboto, Arial, Times New Roman, Open Sans...). |
| | • **Cỡ chữ & Kiểu dáng:** | Tùy chỉnh kích thước từ `9 pt` đến `24 pt`, in đậm (`B`), in nghiêng (`I`), gạch chân (`U`). |
| | • **Bảng chọn màu sắc (ColorPicker):** | Chọn mã màu chữ hiển thị khớp với màu sắc nhận diện thương hiệu. |
| **4. Trang giấy trung tâm & Thao tác kéo thả** | **Khung vẽ trực quan (Canvas)** | Hiển thị các trang của tệp PDF mẫu. Người dùng có thể kéo di chuyển các ô biến đến đúng dòng kẻ trên văn bản, kéo giãn độ rộng tối đa (`Width %`) để tránh tràn dòng. |
| **5. Chế độ xem trước & Xuất tài liệu** | • <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Xem trước với dữ liệu bản ghi:** | Lấy thử dữ liệu từ một dòng bản ghi thực tế ngoài bảng tính để điền vào các vị trí biến trên trang PDF. |
| | • <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu mẫu báo cáo:** | Lưu cấu hình tọa độ mẫu vào thư viện để tái sử dụng lâu dài. |
| | • **Xuất tài liệu PDF:** | Cho phép xuất từng tệp PDF riêng lẻ hoặc gom toàn bộ danh sách bản ghi thành một tệp nén `.zip` tải về máy tính. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Xuất báo cáo Tài liệu mẫu]
                 │
                 ▼
[Bấm "Tải lên PDF biểu mẫu" chọn file nền .pdf]
                 │
                 ▼
[Đặt Tên mẫu báo cáo và Chọn Phân loại danh mục]
                 │
                 ▼
[Kéo thả các Biến từ Bảng dữ liệu vào đúng dòng trên PDF]
                 │
                 ▼
[Thiết lập Kiểu hiển thị (Text, Số, Tiền tệ, Ngày, QR) & Phông chữ]
                 │
                 ▼
[Bấm "Xem trước với dữ liệu bản ghi" để kiểm tra khớp nối]
                 │
                 ▼
[Bấm "Lưu mẫu báo cáo" ➔ Bấm "Xuất tài liệu PDF" hàng loạt]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> **Xuất báo cáo Tài liệu mẫu**. Giao diện trình thiết kế mở toàn màn hình. |
| **2** | **Tải lên PDF mẫu** | Bấm nút **Tải lên PDF biểu mẫu**, chọn tệp hợp đồng hoặc biểu mẫu của công ty. Trang PDF xuất hiện tại khu vực trung tâm. |
| **3** | **Kéo thả biến** | Nhìn sang cột bên trái, nhấp giữ chuột vào biến (ví dụ: `Họ và tên khách hàng`) và kéo thả vào vị trí dòng để trống trên trang PDF. |
| **4** | **Căn chỉnh định dạng** | Nhấp vào ô biến trên PDF: chọn kiểu hiển thị là `Văn bản`, chọn phông chữ `Roboto`, cỡ chữ `11 pt`, màu chữ đen. |
| **5** | **Xem trước & Lưu** | Bấm nút **Xem trước với dữ liệu bản ghi** để đảm bảo dữ liệu họ tên không bị lệch dòng hay tràn viền. Bấm nút màu đỏ **Lưu mẫu báo cáo** ở góc dưới bên phải. |
| **6** | **Xuất PDF hàng loạt** | Mở hộp thoại danh sách mẫu, chọn mẫu vừa lưu và bấm nút **Xuất tài liệu PDF** để in hoặc tải file nén về máy. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Độ chính xác của tọa độ** | Mở tệp PDF đã xuất, toàn bộ dữ liệu họ tên, số tiền, ngày tháng nằm chính xác trên các dòng kẻ của biểu mẫu gốc, không bị lệch hoặc đè lên chữ có sẵn. |
| **Định dạng phông chữ tiếng Việt** | Chữ tiếng Việt hiển thị sắc nét, dấu thanh rõ ràng, không xuất hiện lỗi ô vuông hay ký tự lạ (`font missing`). |
| **Mã QR trên tài liệu** | Quét thử mã QR in trên văn bản PDF, hiển thị đúng thông tin xác thực bản ghi hoặc hợp đồng điện tử. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền đọc và xuất bản ghi (`RECORD_READ`, `RECORD_EXPORT`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Trích xuất dữ liệu điền vào biểu mẫu hợp đồng PDF** | `listRecords`, `getRecord` | *"Hãy đọc thông tin bản ghi khách hàng có ID 'REC-1024' trong bảng 'Hợp Đồng', lấy đầy đủ Họ tên, Số CMND/CCCD, Địa chỉ và Giá trị thanh toán để phục vụ điền vào biểu mẫu hợp đồng PDF."* |
| **Lấy danh sách các bản ghi để xuất biên bản giao nhận hàng loạt** | `listRecords` | *"Hãy truy vấn danh sách 10 đơn hàng có trạng thái 'Đã xuất kho' trong ngày hôm nay để lấy dữ liệu kết xuất biên bản bàn giao PDF."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Xuất tệp hợp đồng PDF trên giao diện | Gọi `getRecord` thấy toàn bộ các giá trị trường trên văn bản PDF trùng khớp 100% với dữ liệu bản ghi. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent truy xuất và xác nhận thông tin bản ghi | Người dùng bấm xuất tài liệu trên UI, tệp PDF sinh ra đúng thông tin mà Agent đã kiểm toán. |
