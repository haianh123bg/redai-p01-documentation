## Tổng quan Tiện ích Quét & Xử lý Trùng lặp tự động

Tiện ích **Quét & Xử lý Trùng lặp tự động** là công cụ phân tích và khử trùng lặp dữ liệu nâng cao trên **RedAI Database**. Tiện ích cho phép người dùng quét dữ liệu theo một hoặc nhiều cột tiêu chí (đa cột), tự động phân nhóm các bản ghi trùng lặp thành từng cụm trực quan và cung cấp 3 cơ chế giải quyết hàng loạt: giữ bản ghi cũ nhất, giữ bản ghi mới nhất hoặc cơ chế **Gộp thông minh (Smart Merge)** giúp bảo toàn 100% dữ liệu quý giá.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Cột tiêu chí so trùng** | **Danh sách các cột có thể quét trùng** | Liệt kê toàn bộ các cột trong bảng (loại trừ các cột hệ thống như ID tự sinh, thứ tự dòng hoặc cột ảo). Cho phép tích chọn đồng thời nhiều cột làm tiêu chí kép (ví dụ: vừa trùng `Số điện thoại` vừa trùng `Họ và tên`, hoặc chỉ trùng `Email`). |
| **2. Thanh thống kê cụm trùng lặp** | **Chỉ số tổng hợp** | Hiển thị thông báo định lượng trực quan: *"Phát hiện {N} cụm trùng lặp với tổng số {M} bản ghi bị trùng"* ngay trên đầu danh sách. |
| **3. Cột danh sách cụm trùng lặp** | **Khung cụm bên trái** | Liệt kê từng cụm trùng lặp kèm giá trị khóa (ví dụ: Khóa `0987654321` hoặc `mai.tran@gmail.com`) và số lượng bản ghi nằm trong cụm đó (ví dụ: `3 bản ghi`). Nhấp vào cụm để xem chi tiết bên phải. |
| **4. Khung đối soát chi tiết cụm** | **Bảng so sánh chi tiết bên phải** | Hiển thị bảng đối soát đầy đủ các trường thông tin của tất cả bản ghi trong cụm được chọn. Bản ghi được tạo đầu tiên được hệ thống đánh dấu nhãn nổi bật: `Bản ghi gốc`. |
| **5. Ba cơ chế xử lý hàng loạt** | • <img src="https://api.iconify.design/lucide:clock.svg?color=%23ff3333" width="16" alt="" /> **Giữ bản ghi cũ nhất** | Giữ lại bản ghi được khởi tạo đầu tiên trong hệ thống, xóa bỏ toàn bộ các bản ghi tạo trùng lặp phát sinh về sau. |
| | • <img src="https://api.iconify.design/lucide:rotate-cw.svg?color=%23ff3333" width="16" alt="" /> **Giữ bản ghi mới nhất** | Giữ lại bản ghi vừa được tạo hoặc cập nhật gần đây nhất, xóa bỏ các bản ghi cũ. |
| | • <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Gộp thông minh (Smart Merge - Khuyên dùng)** | Thuật toán hợp nhất bảo toàn dữ liệu: Lấy bản ghi gốc làm khung sườn chính, tự động quét qua tất cả các bản ghi trùng khác trong cụm. Nếu bản ghi gốc bị khuyết trường nào (ví dụ: thiếu Email, Địa chỉ hoặc Ghi chú) mà các bản ghi trùng có dữ liệu, hệ thống sẽ tự động điền bổ sung vào bản ghi gốc, sau đó mới thực hiện xóa các dòng thừa. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Hộp thoại Quét & Xử lý Trùng lặp]
                  │
                  ▼
[Tích chọn 1 hoặc nhiều Cột tiêu chí so trùng]
                  │
                  ▼
[Hệ thống tự động gom nhóm thành các Cụm trùng lặp (Clusters)]
                  │
                  ▼
[Nhấp vào từng Cụm để đối soát chi tiết các bản ghi]
                  │
                  ▼
[Chọn 1 trong 3 cơ chế xử lý: Cũ nhất / Mới nhất / Gộp thông minh]
                  │
                  ▼
[Hộp thoại Xác nhận: Kiểm tra số lượng dòng xóa & dòng giữ lại]
                  │
                  ▼
[Bấm "Xác nhận xử lý" ➔ Hệ thống cập nhật bảng tính ngay lập tức]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:git-merge.svg?color=%23ff3333" width="16" alt="" /> **Quét & Xử lý Trùng lặp tự động**. |
| **2** | **Chọn cột tiêu chí** | Tích chọn các cột dùng để so trùng (ví dụ: chọn cột `Số điện thoại`). Hệ thống tự động truy vấn danh sách bản ghi và phân nhóm. |
| **3** | **Đối soát dữ liệu các cụm** | Nhấp chọn từng dòng cụm ở cột bên trái để kiểm tra mắt xem các bản ghi có thực sự là của cùng một khách hàng hay không. |
| **4** | **Chọn phương án xử lý** | Bấm vào nút **Gộp thông minh (Smart Merge)** (hoặc *Giữ bản ghi cũ nhất* / *Giữ bản ghi mới nhất*) ở góc trên bên phải. |
| **5** | **Xác nhận thực thi** | Hộp thoại cảnh báo hiển thị tóm tắt: *"Bạn có chắc chắn muốn xử lý {N} cụm trùng lặp? Dự kiến sẽ giữ lại {X} bản ghi và xóa bỏ {Y} bản ghi thừa"*. Nhấp nút **Xác nhận xử lý** màu đỏ để hoàn tất quy trình. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Tổng số dòng trong bảng** | Tổng số bản ghi ngoài Grid View giảm đi chính xác bằng số bản ghi trùng lặp bị xóa. |
| **Chất lượng dữ liệu sau gộp** | Khi mở bản ghi được giữ lại, các ô dữ liệu trước đây bị bỏ trống (ví dụ: Email hoặc Địa chỉ) đã được tự động điền đầy đủ từ bản ghi trùng. |
| **Kiểm tra quét lại** | Mở lại tiện ích Quét trùng lặp với cùng tiêu chí, màn hình thông báo: *"Không phát hiện bản ghi trùng lặp nào"*. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) có quyền xóa và cập nhật bản ghi (`RECORD_DELETE`, `RECORD_UPDATE`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Quét và gộp thông minh các bản ghi trùng SĐT** | `listRecords`, `mergeRecords` | *"Hãy quét bảng 'Khách Hàng' theo cột 'Số điện thoại', phát hiện các bản ghi trùng nhau và gọi lệnh mergeRecords để gộp thông minh các ô trống vào bản ghi gốc, sau đó xóa dòng thừa."* |
| **Quét trùng lặp tiêu chí kép SĐT và Họ tên** | `listRecords`, `mergeRecords` | *"Hãy tìm trong bảng 'Học Viên' những dòng có cùng Số điện thoại và Họ và tên, thực hiện gộp lại và giữ bản ghi cũ nhất."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm nút **Gộp thông minh** trên giao diện | Gọi `listRecords` thấy số lượng bản ghi giảm đi, các bản ghi còn lại chứa đầy đủ dữ liệu từ các dòng đã gộp. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `mergeRecords` gộp bản ghi | Tải lại trang Dạng xem bảng tính, các dòng trùng lặp biến mất và bản ghi gốc có đầy đủ thông tin. |
