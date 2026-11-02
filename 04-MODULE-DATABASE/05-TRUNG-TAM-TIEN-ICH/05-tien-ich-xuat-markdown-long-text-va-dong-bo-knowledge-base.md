## Tổng quan Tiện ích Xuất Markdown Long Text & Đồng bộ Knowledge Base

Tiện ích **Xuất Markdown Long Text & Đồng bộ Knowledge Base** là cầu nối trực tiếp giữa dữ liệu văn bản phong phú trên **RedAI Database** với hệ sinh thái Trí tuệ nhân tạo (AI RAG). Tiện ích tự động trích xuất các trường văn bản nhiều dòng (Long text / Rich text / HTML), chuyển đổi cấu trúc thẻ HTML sang định dạng chuẩn Markdown `.md`, hỗ trợ tải về máy tính dưới dạng tệp nén ZIP hoặc **đẩy thẳng vào Cơ sở Tri thức AI (Knowledge Base)** kèm gắn thẻ nhãn (Tags) để huấn luyện trợ lý ảo AI Agent tra cứu ngay lập tức.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Cột nội dung văn bản dài** | **Menu chọn cột nội dung** | Hệ thống tự động lọc danh sách chỉ hiển thị các cột kiểu `Văn bản dài (Long Text)` hoặc `HTML` có bật tính năng Rich Text. Đây là trường chứa toàn văn bài viết, điều khoản hợp đồng hoặc tài liệu quy trình. |
| **2. Cột đặt tên tệp** | **Menu chọn cột làm tên tệp** | Chọn trường dữ liệu đại diện đóng vai trò làm tên tệp (ví dụ: Cột `Tiêu đề bài viết`, `Mã hợp đồng`, `Tên chính sách`). Mỗi tệp Markdown sinh ra sẽ tự động được đặt tên theo quy tắc: `{Tên_Cột}.md` (các ký tự đặc biệt gây lỗi hệ điều hành sẽ được tự động làm sạch). |
| **3. Tùy chọn Tải về máy tính** | **Chế độ xuất mặc định** | Khi công tắc đồng bộ tri thức ở trạng thái tắt, hệ thống sẽ gom toàn bộ các tệp `.md` sinh ra từ các dòng bản ghi vào một tệp nén `.zip` để tải trực tiếp về thiết bị của người dùng. |
| **4. Công tắc Đồng bộ Cơ sở Tri thức AI** | • <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ vào Cơ sở Tri thức AI:** | Bật công tắc này để hệ thống không chỉ xuất Markdown mà còn tự động tải lên dịch vụ lưu trữ đám mây an toàn và đăng ký vào danh mục Tài nguyên Tri thức (Knowledge Files) của Không gian làm việc. |
| | • **Ô nhập Thẻ nhãn (Tags):** | Nhập danh sách các từ khóa phân loại ngăn cách bằng dấu phẩy (ví dụ: `chinh-sach-noi-bo, quy-trinh-ban-hang, bao-hanh-2026`). Thẻ nhãn này giúp AI Agent định tuyến chính xác tài liệu khi người dùng đặt câu hỏi. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Hộp thoại Xuất Markdown Long Text]
                  │
                  ▼
[Chọn Cột nội dung văn bản dài (Rich Text / HTML)]
                  │
                  ▼
[Chọn Cột định danh dùng làm Tên tệp .md]
                  │
                  ▼
[Lựa chọn Phương thức kết xuất]
       │                                  │
       ▼ (Tải về máy tính)                ▼ (Đồng bộ vào AI RAG)
[Tắt công tắc Tri thức]          [Bật công tắc "Đồng bộ Cơ sở Tri thức AI"]
       │                                  │
       │                                  ▼
       │                         [Nhập danh sách Thẻ nhãn Tags]
       │                                  │
       └──────────────────┬───────────────┘
                          ▼
            [Bấm nút "Bắt đầu xuất dữ liệu"]
                          ▼
    [Tải file .zip về máy HOẶC Nạp vào Knowledge Base]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Xuất Markdown Long Text**. |
| **2** | **Cấu hình cột** | Chọn cột chứa nội dung chi tiết tại menu *Cột nội dung cần xuất* và chọn cột tiêu đề đại diện tại menu *Cột dùng làm tên tệp*. |
| **3** | **Lựa chọn hướng đích** | Nếu cần tải về máy tính, để nguyên công tắc tắt $\rightarrow$ Bấm nút **Xuất tệp Markdown**. Nếu muốn huấn luyện AI, bật công tắc **Đồng bộ vào Cơ sở Tri thức AI** và nhập các nhãn thẻ tag. |
| **4** | **Thực thi** | Bấm nút xác nhận. Hệ thống tự động chuyển đổi định dạng, làm sạch thẻ HTML sang cú pháp chuẩn Markdown và hiển thị thông báo thành công khi hoàn tất. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Kiểm tra tệp tải về máy tính** | Mở tệp `.zip` tải về, bên trong chứa các tệp `.md` mở bằng trình soạn thảo văn bản thấy cấu trúc tiêu đề, danh sách, bảng biểu hiển thị chuẩn xác. |
| **Kiểm tra trong Cơ sở Tri thức AI** | Truy cập mục **Tri thức (Knowledge)** của Workspace, thấy danh sách các tệp tài liệu mới xuất hiện với đầy đủ tên tệp và thẻ nhãn tương ứng, sẵn sàng để AI Agent tra cứu. |

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
| **Trích xuất nội dung văn bản dài ra Markdown** | `listRecords` | *"Hãy lấy toàn bộ nội dung từ cột 'Quy trình vận hành' trong bảng 'Cẩm Nang Doanh Nghiệp' và định dạng kết xuất ra tài liệu chuẩn Markdown."* |
| **Xuất khẩu văn bản hợp đồng từ cơ sở dữ liệu** | `listRecords`, `getRecord` | *"Hãy truy vấn bản ghi hợp đồng có mã 'HD-2026-001', lấy nội dung từ trường 'Điều khoản chi tiết' và lưu thành văn bản Markdown."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm xuất Markdown trên giao diện | Gọi `listRecords` thấy dữ liệu trường văn bản dài khớp hoàn toàn với nội dung trong file `.md` đã xuất. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent đọc nội dung từ cột Long Text | Người dùng mở bảng tính ngoài Grid View, nội dung ô tính hiển thị đồng nhất với kết quả phản hồi của Agent. |
