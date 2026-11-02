## Mở khu vực Trung Tâm Tiện Ích và Bộ công cụ xử lý dữ liệu nâng cao

**Trung Tâm Tiện Ích (Utilities Center)** là phân hệ công cụ mở rộng của **RedAI Database**, cung cấp các tính năng tự động hóa chuyên sâu hỗ trợ vận hành dữ liệu: từ in ấn mã QR hàng loạt, thiết kế mẫu báo cáo tài liệu PDF, kiểm tra chất lượng dữ liệu, cho đến làm sạch và phát hiện bản ghi trùng lặp.

| Bước | Thao tác thực hiện trên giao diện | Chi tiết hiển thị |
| :--- | :--- | :--- |
| **1. Mở Dạng xem bảng tính** | Tại danh sách bảng, nhấp vào Dạng xem bảng tính (ví dụ: `Trang chủ > Database > View Details`). | Màn hình hiển thị bảng tính dữ liệu với thanh công cụ phía trên. |
| **2. Mở Trung Tâm Tiện Ích** | Trên thanh công cụ của View Details, nhấp vào biểu tượng ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> → Chọn <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Trung Tâm Tiện Ích**. | Ngăn kéo **Trung Tâm Tiện Ích** xuất hiện từ cạnh phải màn hình, gồm ô tìm kiếm `Q Tìm kiếm tiện ích theo tên hoặc mô tả...` và bộ lọc danh mục `Tất cả danh mục`. |

---

### Danh mục 10 công cụ trong Trung Tâm Tiện Ích

| Tên công cụ tiện ích | Biểu tượng | Phạm vi xử lý & Nghiệp vụ giải quyết |
| :--- | :--- | :--- |
| **1. Chuẩn hóa & Làm sạch dữ liệu** | <img src="https://api.iconify.design/lucide:wand-2.svg?color=%23ff3333" width="16" alt="" /> | Chuẩn hóa định dạng số điện thoại chuẩn quốc tế (+84/09x), định dạng chuẩn email, tự động viết hoa họ tên và loại bỏ khoảng trắng thừa. |
| **2. Quét & Xử lý Trùng lặp tự động** | <img src="https://api.iconify.design/lucide:git-merge.svg?color=%23ff3333" width="16" alt="" /> | Tự động quét và phát hiện các cụm bản ghi bị trùng lặp theo số điện thoại, email hoặc họ tên; hỗ trợ gộp bản ghi chỉ bằng 1 cú nhấp chuột. |
| **3. Báo Cáo Sức khỏe & Chất lượng dữ liệu** | <img src="https://api.iconify.design/lucide:alert-circle.svg?color=%23ff3333" width="16" alt="" /> | Đánh giá tỷ lệ hoàn thiện cơ sở dữ liệu (% số ô có dữ liệu), phát hiện các ô thiếu thông tin hoặc sai lệch định dạng. |
| **4. In Tem Nhãn & Tạo Mã QR Hàng Loạt** | <img src="https://api.iconify.design/lucide:printer.svg?color=%23ff3333" width="16" alt="" /> | Tự động sinh mã QR cho từng bản ghi, thiết kế nhãn dán định dạng giấy A4 hoặc Decal cuộn và xuất in hàng loạt. |
| **5. Xuất Markdown Long Text** | <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> | Đóng gói và xuất toàn bộ nội dung từ các trường văn bản dài (Long text / Rich text) ra tệp định dạng Markdown `.md`. |
| **6. Xuất báo cáo Tài liệu mẫu** | <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> | Mở trình thiết kế mẫu PDF trực quan, kéo thả các biến dữ liệu từ bảng vào tài liệu mẫu theo tọa độ chính xác. |
| **7. Sinh Dữ Liệu Mẫu (Mock Data)** | <img src="https://api.iconify.design/lucide:database.svg?color=%23ff3333" width="16" alt="" /> | Tạo ngẫu nhiên từ 5 đến 50 dòng bản ghi giả lập thử nghiệm với họ tên tiếng Việt, số điện thoại, địa chỉ và email hợp lệ. |
| **8. Danh sách lịch sử chạy ngầm** | <img src="https://api.iconify.design/lucide:clock.svg?color=%23ff3333" width="16" alt="" /> | Theo dõi tiến trình, trạng thái hoàn thành và nhật ký lỗi của các tác vụ hệ thống chạy ngầm (SysJobs). |
| **9. Thu thập thông tin Group Zalo từ link** | <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> | Đọc các liên kết nhóm Zalo lưu trong bảng để tự động cào thông tin thành viên và trạng thái nhóm. |
| **10. Chiến dịch SMS** | <img src="https://api.iconify.design/lucide:message-square.svg?color=%23ff3333" width="16" alt="" /> | Khởi tạo chiến dịch gửi tin nhắn SMS Marketing & Chăm sóc khách hàng tự động theo danh sách số điện thoại có trong bảng. |

---

## Hướng dẫn chi tiết các tác vụ trọng tâm

### Tác vụ 1 — In Tem Nhãn & Tạo Mã QR Hàng Loạt

Quy trình tạo mã QR định danh và in ấn tem nhãn dán sản phẩm, hồ sơ hoặc thẻ khách hàng:

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Mở tiện ích In tem nhãn** | Trong Trung Tâm Tiện Ích, nhấp vào mục <img src="https://api.iconify.design/lucide:printer.svg?color=%23ff3333" width="16" alt="" /> **In Tem Nhãn & Tạo Mã QR Hàng Loạt**. | Ngăn kéo cấu hình in ấn xuất hiện bên phải màn hình. |
| **2. Cấu hình nguồn dữ liệu mã hóa QR** | Tại menu **Dữ liệu mã hóa QR**, chọn cột thông tin dùng để sinh mã QR (ví dụ: `Link trực tiếp`, `Mã bản ghi ID`, `Mã đơn hàng`). | Dữ liệu từ cột này sẽ được chuyển thành mã hình học QR Code hai chiều. |
| **3. Cấu hình văn bản hiển thị trên tem** | • **Tiêu đề trên tem**: Chọn trường hiển thị ở dòng chữ phía trên mã QR (ví dụ: `Tên cơ sở`, `Tên sản phẩm`).<br>• **Thông tin phụ dưới tem**: Chọn trường hiển thị ở chân tem (ví dụ: `Ngày tạo`, `Hotline`, `Giá tiền`). | Tạo nhãn dán hoàn chỉnh vừa có mã quét vừa có thông tin chữ để người dùng đối soát bằng mắt. |
| **4. Chọn bố cục khổ giấy in** | Tại menu **Bố cục tem**, chọn định dạng dàn trang phù hợp:<br>• `Lưới A4 (3 cột)`: Định dạng chuẩn 3 tem trên một hàng giấy A4.<br>• `Lưới A4 (4 cột)`: Tem kích thước nhỏ gọn hơn.<br>• `Decal đơn / Tem cuộn`: Dành cho máy in mã vạch nhiệt chuyên dụng. | Căn chỉnh kích thước và khoảng cách lề tem tự động. |
| **5. Xem trước trực tiếp (Live Preview)** | Quan sát khung **Xem trước tem in ({N} tem)** ở giữa màn hình. | Khung hiển thị trực tiếp hình ảnh các con tem thực tế với mã QR rõ nét và các dòng thông tin mẫu. |
| **6. Thực hiện in ấn** | Kiểm tra tổng số tem tại thanh trạng thái chân trang (`Hiển thị {N} tem nhãn`) → Bấm nút **In tem nhãn**. | Trình duyệt mở hộp thoại in của hệ điều hành để gửi lệnh in tới máy in vật lý hoặc xuất file PDF. |

---

### Tác vụ 2 — Thiết Kế Mẫu Báo Cáo Tài Liệu (PDF Template Designer)

Tính năng kết xuất dữ liệu tự động từ bảng vào biểu mẫu hợp đồng, biên bản bàn giao hoặc báo cáo tài liệu PDF:

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Mở trình thiết kế mẫu** | Trong Trung Tâm Tiện Ích, nhấp vào mục <img src="https://api.iconify.design/lucide:file-spreadsheet.svg?color=%23ff3333" width="16" alt="" /> **Xuất báo cáo Tài liệu mẫu**. | Hệ thống mở toàn màn hình giao diện **Thiết Kế Mẫu Báo Cáo Tài Liệu**. |
| **2. Thiết lập thông tin chung của mẫu** | Tại thanh công cụ phía trên:<br>• **Bảng dữ liệu**: Xác nhận bảng nguồn (ví dụ: `01_CoSo`).<br>• **Tên mẫu**: Đặt tên định danh (ví dụ: `Mẫu Hợp Đồng Dịch Vụ Mới`).<br>• **Phân loại**: Chọn nhóm tài liệu (ví dụ: `Hợp đồng pháp lý`, `Biên bản nghiệm thu`). | Định danh mẫu tài liệu để tái sử dụng lâu dài cho toàn bộ các bản ghi sau này. |
| **3. Tải lên tệp PDF biểu mẫu** | Bấm biểu tượng <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **(Tải lên)** trên thanh công cụ để chọn tệp tài liệu PDF mẫu có sẵn của doanh nghiệp. | Tệp PDF hiển thị ngay tại trang giấy trung tâm màn hình làm việc. |
| **4. Kéo thả các biến dữ liệu vào biểu mẫu** | Tại cột bên trái (**Trường dữ liệu & Biến**):<br>• **BIẾN TỪ BẢNG DỮ LIỆU**: Danh sách toàn bộ các cột trong bảng (ví dụ: `Tên cơ sở`, `Địa chỉ`, `Hotline`, `Quản lý`...). Nhấp giữ chuột vào biến và kéo thả vào vị trí dòng tương ứng trên trang PDF.<br>• **BIẾN TỰ DO (TỰ ĐẶT)**: Bấm `+ Thêm biến` để định nghĩa thêm các trường thông tin ngoài bảng (ví dụ: `Số Hợp Đồng`, `Ngày Lập Tài Liệu`, `Đại Diện Bên B`). | Khớp nối chính xác tọa độ các ô dữ liệu trên văn bản PDF. |
| **5. Xem trước và Lưu mẫu** | Bấm nút **Chế độ xem trước** để kiểm tra việc điền dữ liệu thực tế → Bấm nút **Lưu mẫu** (màu đỏ) ở góc dưới bên phải. | Mẫu được lưu vào danh sách mẫu khả dụng, sẵn sàng để xuất báo cáo PDF hàng loạt cho bất kỳ dòng bản ghi nào. |

---

### Tác vụ 3 — Quy trình Ánh xạ Nhập dữ liệu (Import Data Mapping)

Khi thêm dữ liệu từ các file ngoại bộ vào một Dạng xem hiện có (thông qua menu View → **Nhập dữ liệu**):

| Bước | Thao tác thực hiện | Mô tả chi tiết |
| :--- | :--- | :--- |
| **1. Tải lên tệp nguồn** | Kéo thả tệp bảng tính (`.xlsx`, `.xls`, `.csv`) dung lượng tối đa 10MB vào khung tải lên. | Hệ thống trích xuất cấu trúc và chuyển sang màn hình **Nhập dữ liệu**. |
| **2. Kiểm tra thông số tệp** | Quan sát thông báo ở đầu trang (ví dụ: `redai_catalog.xlsx - 1 sheets available • 5 cột dữ liệu trong tệp`). | Xác nhận hệ thống đã đọc đúng số trang tính và số lượng cột của file. |
| **3. Thiết lập bảng ánh xạ 3 cột** | Đối soát từng dòng trong bảng ánh xạ:<br>• **TRƯỜNG HỆ THỐNG TƯƠNG ỨNG**: Cột đích trong bảng RedAI.<br>• **NGUỒN DỮ LIỆU**: Nhấp vào menu thả xuống để chọn tiêu đề cột tương ứng trong file Excel (hoặc chọn `— Bỏ qua (Không import) —`).<br>• **CẤU HÌNH GIÁ TRỊ / ÁNH XẠ**: Thiết lập chuyển đổi định dạng nếu cần. | Đảm bảo dữ liệu từ file ngoại bộ đổ vào đúng trường mục tiêu mà không bị lệch dữ liệu. |
| **4. Thực thi nhập bản ghi** | Bấm nút xác nhận nhập dữ liệu ở chân trang. | Hệ thống chạy ngầm tiến trình import và tự động cập nhật số lượng dòng mới vào bảng tính. |

---

## Kiểm tra kết quả

Sau khi thực hiện các tác vụ trong Trung Tâm Tiện Ích, người dùng kiểm tra lại:

| Hạng mục kiểm tra | Tiêu chí đạt chuẩn |
| :--- | :--- |
| **1. Mã QR & Tem nhãn** | Mã QR quét thử bằng điện thoại mở ra đúng đường dẫn hoặc hiển thị chính xác mã bản ghi; bố cục tem in vừa khít khổ giấy và không bị tràn lề. |
| **2. Báo cáo PDF mẫu** | Tải thử một tệp PDF kết xuất từ bản ghi; toàn bộ dữ liệu họ tên, số tiền, ngày tháng điền đúng vào tọa độ đã định vị trên mẫu. |
| **3. Dữ liệu Import** | Sau khi import tệp Excel, bảng tính hiển thị đầy đủ các dòng mới với các cột được điền đúng dữ liệu theo ánh xạ. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động khai thác các công cụ trong Trung Tâm Tiện Ích: trích xuất dữ liệu để in mã QR hoặc xuất báo cáo tài liệu PDF, thực hiện chuẩn hóa và làm sạch dữ liệu ô tính, quét và gộp các bản ghi trùng lặp, sinh dữ liệu mẫu (Mock data) thử nghiệm và truy vấn phân tích số liệu theo lô thông qua bộ công cụ quản trị Database.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Database` (ID: `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6`)
- **Bộ công cụ (Tool Suite) đi kèm**: `RedAI - Module - Database` (ID: `eb8a7504-5844-4e6e-ba7f-7645f104c0af`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền thao tác dữ liệu trong Workspace (Member, Editor, Admin hoặc Owner).

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Mở tiện ích **In Tem Nhãn & Tạo Mã QR Hàng Loạt** | `listRecords` | Truy vấn danh sách các bản ghi, lấy mã định danh và đường dẫn để tạo mã QR và thông tin in ấn. |
| Mở tiện ích **Xuất báo cáo Tài liệu mẫu (PDF)** | `listRecords`, `getRecord` | Đọc toàn bộ các giá trị trường của bản ghi để điền tự động vào các biến tọa độ trên biểu mẫu PDF. |
| Mở tiện ích **Xuất Markdown Long Text** | `listRecords` | Kết xuất toàn bộ nội dung từ các cột văn bản dài của bảng ra định dạng văn bản Markdown chuẩn. |
| Sử dụng công cụ **Chuẩn hóa & Làm sạch dữ liệu** | `updateRecords` | Tự động rà soát, chuẩn hóa định dạng số điện thoại (+84/09x), viết hoa họ tên và cập nhật lại ô tính. |
| Sử dụng công cụ **Quét & Xử lý Trùng lặp tự động** | `mergeRecords`, `listRecords` | Phát hiện các bản ghi có số điện thoại hoặc email trùng nhau và thực thi gộp dữ liệu thành một bản ghi chuẩn. |
| Tiện ích **Báo Cáo Sức khỏe & Chất lượng dữ liệu** | `countRecords`, `listRecords` | Thống kê số lượng bản ghi, tỷ lệ các ô có dữ liệu và phát hiện các dòng bản ghi còn thiếu trường thông tin. |
| Tiện ích **Sinh Dữ Liệu Mẫu (Mock Data)** | `createRecords` | Tự động khởi tạo ngẫu nhiên từ 5 đến 50 dòng bản ghi giả lập với họ tên, số điện thoại, địa chỉ tiếng Việt hợp lệ. |
| Thực hiện **Nhập dữ liệu (Import Data Mapping)** | `createRecords`, `bulkColumns` | Nhập dữ liệu hàng loạt từ danh sách ánh xạ vào các cột tương ứng trong bảng dữ liệu. |
| Phân tích và tổng hợp số liệu dữ liệu theo lô | `bulkGroupBy`, `bulkAggregateRecords`, `queryByName` | Thực hiện gom nhóm dữ liệu và tính toán tổng hợp chuyên sâu phục vụ báo cáo quản trị. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi kiểm tra chất lượng dữ liệu, xử lý trùng lặp và sinh dữ liệu mẫu thử nghiệm trên RedAI Database theo quy trình chuẩn:

1. Bối cảnh và Mục tiêu:
- Tôi cần rà soát lại bảng "Khách Hàng Doanh Nghiệp", kiểm tra tỷ lệ hoàn thiện dữ liệu, quét các bản ghi trùng số điện thoại để gộp lại, sau đó sinh thêm 10 dòng bản ghi dữ liệu mẫu tiếng Việt để kiểm thử dạng xem Kanban.

2. Dữ liệu cung cấp:
- Tên bảng dữ liệu: "Khách Hàng Doanh Nghiệp"
- Tiêu chí quét trùng lặp: Trùng số điện thoại tại cột "Hotline"
- Số lượng bản ghi mẫu cần sinh: 10 bản ghi gồm đầy đủ Tên công ty, Hotline, Địa chỉ và Người liên hệ đại diện.

3. Các bước yêu cầu thực hiện:
- Bước 1: Gọi tool countRecords và listRecords trên bảng "Khách Hàng Doanh Nghiệp" để thống kê tổng số bản ghi và kiểm tra các ô còn thiếu dữ liệu.
- Bước 2: Rà soát danh sách bản ghi, nếu phát hiện các bản ghi trùng số điện thoại, gọi tool mergeRecords để gộp dữ liệu và giữ lại bản ghi đầy đủ thông tin nhất.
- Bước 3: Gọi tool createRecords để sinh 10 dòng bản ghi mẫu thử nghiệm với thông tin doanh nghiệp tiếng Việt hợp lệ.
- Bước 4: Gọi lại tool countRecords để xác nhận tổng số lượng bản ghi sau khi xử lý.

4. Yêu cầu phản hồi:
- Báo cáo số lượng bản ghi ban đầu, số cụm trùng lặp đã gộp thành công, số bản ghi mẫu vừa sinh và tổng số bản ghi hiện tại của bảng.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở bảng **Khách Hàng Doanh Nghiệp** trên Grid View; kiểm tra các bản ghi trùng lặp trước đó đã được gộp gọn gàng, và 10 dòng bản ghi mẫu mới xuất hiện với đầy đủ thông tin hợp lệ. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `countRecords` và `listRecords` với limit 10 của bảng 'Khách Hàng Doanh Nghiệp' để xác nhận dữ liệu đã được làm sạch và bổ sung hoàn chỉnh."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm In tem nhãn hoặc kết xuất PDF trên giao diện | Gọi `listRecords` thấy dữ liệu các dòng được kết xuất đồng bộ chính xác với nội dung trên tem in. |
| Bấm Gộp bản ghi trong tiện ích Quét trùng lặp | Gọi `listRecords` thấy các bản ghi trùng đã được hợp nhất thành một dòng duy nhất. |
| Thực hiện Import file Excel qua bảng ánh xạ 3 cột | Gọi `countRecords` thấy tổng số bản ghi tăng lên tương ứng với số dòng trong file đã import. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createRecords` sinh dữ liệu mẫu | Mở Grid View của bảng, 10 dòng bản ghi mẫu mới lập tức hiển thị trên bảng tính. |
| Agent gọi `mergeRecords` gộp bản ghi trùng | Tải lại View Details, các dòng trùng lặp biến mất và gom lại thành một bản ghi hoàn chỉnh. |
| Agent gọi `updateRecords` chuẩn hóa số điện thoại | Các ô số điện thoại hiển thị đúng định dạng chuẩn quốc tế (+84...) trên bảng tính. |
