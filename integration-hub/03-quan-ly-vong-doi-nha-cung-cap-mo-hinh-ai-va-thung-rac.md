## Mở khu vực Quản trị dịch vụ tự tạo

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh điều hướng chính ở cột bên trái của **nền tảng RedAI**, chọn mục <img src="https://api.iconify.design/lucide:blocks.svg?color=%23ff3333" width="16" alt="" /> **Tích hợp**. |
| **2** | Chọn tiếp tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **Nhà cung cấp tự tạo** (tại đường dẫn `/integrations/my-integrations?tab=custom-providers`) để mở bảng danh sách các ứng dụng do doanh nghiệp bạn tự xây dựng và quản trị. |

---

## Các tính năng

### Tìm, lọc và nhận biết nguồn gốc sở hữu ứng dụng

Màn hình quản lý cung cấp các công cụ lọc trực quan giúp bạn kiểm soát toàn bộ vòng đời của các phần mềm nội bộ:

| Khu vực hoặc chức năng | Cách sử dụng và phạm vi hiển thị |
| :--- | :--- |
| **Ô tìm kiếm nhanh** | Nhập từ khóa tên ứng dụng hoặc mã kỹ thuật vào ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm...** để lọc ngay trong danh sách. |
| **Lọc theo nguồn gốc sở hữu** | Thanh công cụ phân chia rõ các nhóm sở hữu:<br>- <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Tất cả:** Hiển thị toàn bộ các nhà cung cấp dịch vụ.<br>- <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Hệ thống (SYSTEM):** Các ứng dụng chuẩn mực do nền tảng cài đặt sẵn.<br>- <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Quản trị (ADMIN):** Các dịch vụ cốt lõi do Quản trị viên cấp cao phát hành.<br>- <img src="https://api.iconify.design/lucide:globe.svg?color=%23ff3333" width="16" alt="" /> **Cộng đồng (COMMUNITY):** Các tích hợp được mở chia sẻ cho mọi thành viên.<br>- <img src="https://api.iconify.design/lucide:user.svg?color=%23ff3333" width="16" alt="" /> **Người dùng (USER):** Các ứng dụng cá nhân hoặc phòng ban tự tạo riêng. |
| **Chế độ xem Thùng rác** | Bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xem Thùng rác)** để chuyển đổi giữa danh sách đang hoạt động và danh sách các ứng dụng đang tạm ẩn. |

---

### Quản lý danh sách mô hình trí tuệ nhân tạo (Text Models)

Áp dụng cho các nhà cung cấp mô hình ngôn ngữ lớn (LLM), giúp bạn bổ sung các phiên bản mô hình mới nhất (như GPT-4o, Claude 3.5, DeepSeek-V3, Qwen 2.5...) và kiểm soát chi phí:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại dòng nhà cung cấp dịch vụ AI, chọn menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Models)**. |
| **2** | Hộp thoại danh sách mô hình mở ra. Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm mô hình mới)**. |
| **3** | **Điền thông số mô hình:**<br>- **Tên hiển thị:** Tên gọi thân thiện (ví dụ: `DeepSeek V3 Chat`).<br>- **Mã kỹ thuật (Model ID):** Tên mã chính xác của nhà phát triển (ví dụ: `deepseek-chat`).<br>- **Độ dài ngữ cảnh tối đa (Context Window):** Số lượng token tối đa mà mô hình có thể đọc hiểu trong một lần (ví dụ: `64,000` hoặc `128,000`).<br>- **Đơn giá tính phí:** Mức giá theo triệu token đầu vào và đầu ra để hệ thống tự động đo lường chi phí sử dụng cho từng phòng ban. |
| **4** | Chọn <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu mô hình)**. Mô hình mới sẽ xuất hiện ngay trong danh sách lựa chọn của **trợ lý ảo AI Agent** và kịch bản tự động hóa. |

---

### Quản lý mô hình chuyển đổi ngôn ngữ thành vector (Embedding Models)

Mô hình chuyển đổi vector đóng vai trò như "bộ số hóa tri thức", giúp chuyển đổi văn bản, file tài liệu và bảng tính thành các chuỗi số để **trợ lý ảo AI Agent** tra cứu dữ liệu doanh nghiệp siêu tốc:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại dòng nhà cung cấp dịch vụ, chọn menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)** $\rightarrow$ chọn <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(Quản lý Embedding)**. |
| **2** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm mô hình Vector)**. |
| **3** | Nhập **Mã mô hình** (ví dụ: `text-embedding-3-small`, `bge-m3`) và **Số chiều không gian** (Dimensions: ví dụ `1536`, `1024` hoặc `768`). |
| **4** | Chọn <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận)** để đưa mô hình vào kho tri thức doanh nghiệp. |

---

### Thăng cấp hoặc hạ cấp phạm vi chia sẻ ứng dụng

Dành riêng cho Quản trị viên không gian làm việc muốn chia sẻ ứng dụng hữu ích cho toàn bộ thành viên trong công ty:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại dòng ứng dụng cần phân quyền, chọn menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)**. |
| **2** | **Lựa chọn mức độ thăng cấp:**<br>- Chọn <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Thăng cấp lên Hệ thống)**: Ứng dụng trở thành dịch vụ mặc định, xuất hiện cho mọi không gian làm việc.<br>- Chọn <img src="https://api.iconify.design/lucide:share-2.svg?color=%23ff3333" width="16" alt="" /> **(Chia sẻ cho Cộng đồng)**: Cho phép các phòng ban khác cùng tìm thấy và kết nối ứng dụng.<br>- Chọn <img src="https://api.iconify.design/lucide:arrow-down.svg?color=%23ff3333" width="16" alt="" /> **(Hạ cấp về nội bộ)**: Thu hồi quyền chia sẻ, đưa ứng dụng trở lại trạng thái riêng tư. |
| **3** | Xác nhận thay đổi trong hộp thoại thông báo. |

---

### Chuyển ứng dụng vào Thùng rác

Khi doanh nghiệp tạm ngừng dùng một ứng dụng hoặc muốn bảo trì, bạn nên chuyển ứng dụng vào Thùng rác thay vì xóa vĩnh viễn:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại dòng ứng dụng cần tạm ẩn, chọn menu ba chấm <img src="https://api.iconify.design/lucide:more-vertical.svg?color=%23ff3333" width="16" alt="" /> **(Thao tác)**. |
| **2** | Chọn lệnh <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **(Chuyển vào thùng rác)**. |
| **3** | Hộp thoại thông báo xuất hiện nhắc nhở ứng dụng sẽ tạm thời ẩn khỏi Kho tích hợp công cộng. Chọn <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Đồng ý chuyển vào thùng rác)**. |

> **Lưu ý an toàn:** Toàn bộ thông tin cấu hình, tài liệu hướng dẫn và lịch sử kết nối của ứng dụng vẫn được lưu giữ an toàn trong Thùng rác; bạn có thể khôi phục lại bất kỳ lúc nào mà không bị mất dữ liệu.

---

### Khôi phục ứng dụng từ Thùng rác

Khi cần kích hoạt lại ứng dụng đã tạm ẩn trước đó để tiếp tục công việc:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh công cụ phía trên bảng danh sách, chọn nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Xem Thùng rác)**. Danh sách các ứng dụng đã tạm ẩn sẽ hiển thị. |
| **2** | Tìm đến ứng dụng cần lấy lại, chọn nút <img src="https://api.iconify.design/lucide:rotate-ccw.svg?color=%23ff3333" width="16" alt="" /> **(Khôi phục)** ở cột Thao tác. |
| **3** | Chọn <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Xác nhận khôi phục)**. Ứng dụng lập tức trở lại danh sách hoạt động bình thường và xuất hiện lại trên Kho ứng dụng tích hợp. |

---

### Xóa vĩnh viễn ứng dụng khỏi nền tảng RedAI

Thao tác này chỉ dùng khi bạn chắc chắn 100% không bao giờ sử dụng lại ứng dụng này nữa và muốn dọn sạch hoàn toàn khỏi cơ sở dữ liệu:

> **Cảnh báo cực kỳ nguy hiểm:** Thao tác xóa vĩnh viễn không thể hoàn tác! Toàn bộ hồ sơ ứng dụng, cấu hình bảo mật, tài liệu hướng dẫn và các tài khoản kết nối liên quan sẽ bị xóa sạch hoàn toàn khỏi **nền tảng RedAI**.

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trong chế độ xem **Thùng rác**, tìm đến ứng dụng muốn xóa triệt để. |
| **2** | Chọn nút màu đỏ <img src="https://api.iconify.design/lucide:alert-triangle.svg?color=%23ff3333" width="16" alt="" /> **(Xóa vĩnh viễn)**. |
| **3** | Hộp thoại cảnh báo hiển thị mức độ nguy hiểm cao nhất. Bạn cần gõ đúng tên của ứng dụng hoặc tích chọn ô cam kết rủi ro, sau đó chọn nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Tôi hiểu và muốn xóa vĩnh viễn)**. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể quản lý vòng đời ứng dụng và dọn dẹp thùng rác an toàn thông qua việc trò chuyện trực tiếp với **trợ lý ảo AI Agent**.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng cần kích hoạt**: Kỹ năng Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `d5731aab-1a2b-48a6-a904-5dd84ec1d4bd`.
- **Bộ công cụ sử dụng**: Bộ công cụ Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `ae8afc9a-1180-48d6-b672-d30171ccf3a6`.
- **Phạm vi hỗ trợ**: Bổ sung mô hình AI mới, tạm ẩn ứng dụng vào thùng rác, khôi phục ứng dụng cũ và dọn dẹp thùng rác an toàn.

---

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Thêm mô hình AI mới vào nhà cung cấp dịch vụ

Nhờ **trợ lý ảo AI Agent** bổ sung phiên bản mô hình AI mới ra mắt vào danh mục mô hình của công ty.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Mở hộp thoại Quản lý Models và bấm thêm mô hình. |
| **Công cụ Agent sử dụng** | `integration_llm_custom_manage` |
| **Thông tin cần cung cấp** | Tên ứng dụng, tên mô hình AI, mã kỹ thuật và độ dài ngữ cảnh. |

**Câu lệnh mẫu (Prompt):**
> "Hãy giúp tôi bổ sung mô hình AI mới có tên [Tên mô hình, ví dụ: Qwen 2.5 72B] với mã nhận diện [qwen-2.5-72b-chat] vào nhà cung cấp dịch vụ [Tên nhà cung cấp AI của công ty]."

---

#### 2. Chuyển ứng dụng vào thùng rác hoặc khôi phục lại

Quản lý trạng thái hoạt động của ứng dụng qua câu lệnh ngắn gọn.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Chọn nút Chuyển vào thùng rác hoặc Khôi phục trên màn hình. |
| **Công cụ Agent sử dụng** | `integration_provider_delete` hoặc `integration_provider_restore` |
| **Thông tin cần cung cấp** | Tên ứng dụng và hành động muốn thực hiện (tạm ẩn hay khôi phục). |

**Câu lệnh mẫu (Prompt):**
> "Hãy giúp tôi chuyển ứng dụng [Tên ứng dụng] vào thùng rác để tạm bảo trì. Hãy báo lại cho tôi sau khi hoàn thành."

---

#### 3. Dọn dẹp thùng rác và xóa vĩnh viễn

Dành cho người quản trị muốn dọn sạch các ứng dụng thử nghiệm không còn nhu cầu sử dụng.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Mở Thùng rác và chọn Xóa vĩnh viễn. |
| **Công cụ Agent sử dụng** | `integration_provider_permanent_delete` hoặc `integration_provider_bulk_delete` |
| **Thông tin cần cung cấp** | Tên chính xác của ứng dụng trong thùng rác cần xóa bỏ. |

**Câu lệnh mẫu (Prompt):**
> "Hãy kiểm tra xem trong thùng rác có ứng dụng tên là [Tên ứng dụng] không. Nếu có, hãy hỏi lại xác nhận của tôi trước khi thực hiện xóa vĩnh viễn."

> **Cảnh báo khi dùng AI Agent:** Tuyệt đối không ra lệnh xóa chung chung như "hãy xóa hết các ứng dụng trong thùng rác". Luôn chỉ định đích danh tên ứng dụng và yêu cầu **trợ lý ảo AI Agent** xác nhận trước khi xóa vĩnh viễn.

---

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Cách thực hiện | Dấu hiệu nhận biết thành công |
| :--- | :--- | :--- |
| **Kiểm tra trong khung chat** | Đọc phản hồi của trợ lý ảo AI Agent. | Trợ lý ảo AI Agent thông báo kết quả cụ thể: số lượng mô hình AI đã thêm, hoặc xác nhận ứng dụng đã được chuyển trạng thái tương ứng. |
| **Kiểm tra trên màn hình quản trị** | Tải lại trang Nhà cung cấp tự tạo trên nền tảng RedAI. | Ứng dụng xuất hiện hoặc biến mất khỏi danh sách theo đúng yêu cầu bạn vừa đưa ra. |
