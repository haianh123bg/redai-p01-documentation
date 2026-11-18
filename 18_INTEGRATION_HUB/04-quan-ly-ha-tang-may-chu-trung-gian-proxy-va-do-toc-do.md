## Mở khu vực Quản lý máy chủ trung gian

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh điều hướng chính ở cột bên trái của **nền tảng RedAI**, chọn mục <img src="https://api.iconify.design/lucide:blocks.svg?color=%23ff3333" width="16" alt="" /> **Tích hợp**. |
| **2** | Chọn tiếp tab <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Máy chủ trung gian (Proxy)** (tại đường dẫn `/integrations/my-integrations?tab=proxy` hoặc truy cập nhanh qua `/proxy`). |
| **3** | Thanh điều hướng phân đoạn (Segmented Header) hiển thị 4 thẻ phụ chuyên biệt, hỗ trợ liên kết URL sâu (`?subview=...`) giúp bạn bookmark hoặc mở trực tiếp phân khu cần quản trị:<br>- <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Danh sách proxy** (`?subview=list`): Quản lý từng máy chủ proxy đơn lẻ, giao thức mạng, đo tốc độ phản hồi Ping và kiểm tra tỷ lệ thành công.<br>- <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy (Pools)** (`?subview=pools`): Quản trị toàn diện vòng đời các nhóm máy chủ luân phiên, thuật toán điều phối tải và ngưỡng tự động xoay tua khi có sự cố.<br>- <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **Proxy tài khoản** (`?subview=base-binding`): Gán đường truyền máy chủ chuyên biệt cho từng tài khoản kết nối cụ thể (Base Integration) kèm giám sát tải kết nối đồng thời theo thời gian thực.<br>- <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Proxy Provider** (`?subview=provider-binding`): Gán máy chủ hoặc nhóm máy chủ cho toàn bộ nhà cung cấp dịch vụ bên ngoài (OpenAI, Anthropic, Gemini, Zalo...). |

---

## Các tính năng

### Tìm, lọc và nhận biết thông số máy chủ trung gian

Máy chủ trung gian (Proxy) đóng vai trò như một "trạm trung chuyển mạng", giúp bảo vệ địa chỉ IP thực tế của doanh nghiệp, tăng cường tính ẩn danh và vượt qua các rào cản kiểm duyệt hoặc giới hạn kết nối từ các dịch vụ quốc tế:

| Khu vực hoặc thông số | Ý nghĩa và cách nhận diện |
| :--- | :--- |
| **Ô tìm kiếm máy chủ** | Nhập địa chỉ IP, tên miền máy chủ hoặc tên gợi nhớ vào ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm...** để lọc nhanh các máy chủ đang quan tâm. |
| **Địa chỉ IP và Cổng (Host:Port)** | Cột định danh vị trí máy chủ trên mạng internet (ví dụ: `103.145.22.10:8080`). |
| **Giao thức mạng (Protocol)** | Chuẩn giao tiếp của máy chủ: `HTTP`, `HTTPS`, hoặc `SOCKS5` (khuyên dùng SOCKS5 cho các tác vụ cần tốc độ cao và bảo mật đường truyền đa năng). |
| **Huy hiệu trạng thái hoạt động** | Hiển thị tình trạng hiện tại:<br>- <span style="color:#16a34a">● **Đang hoạt động (active):**</span> Máy chủ sẵn sàng điều hướng các gói tin.<br>- <span style="color:#d97706">● **Tạm dừng (inactive):**</span> Máy chủ đang được bảo trì hoặc chủ động tắt.<br>- <span style="color:#dc2626">● **Hết hạn (expired):**</span> Gói cước thuê máy chủ với nhà cung cấp đã hết hạn dùng. |
| **Tỷ lệ thành công (Success Rate)** | Tỷ lệ phần trăm các gói tin chuyển tiếp thành công qua máy chủ trong 24 giờ qua. |

---

### Thêm mới máy chủ trung gian vào hệ thống

Khi doanh nghiệp thuê mới một địa chỉ máy chủ trung gian từ nhà cung cấp dịch vụ mạng:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại thẻ **Danh sách proxy**, chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Proxy)** ở góc trên bên phải. |
| **2** | **Chọn loại hình Proxy qua thẻ tương tác trực quan:**<br>- <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Proxy tĩnh (Static):** Duy trì một địa chỉ IP cố định duy nhất cho mọi kết nối ra ngoài, phù hợp khi cần whitelist IP tại các dịch vụ đối tác.<br>- <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Proxy xoay (Rotating):** Tự động đổi địa chỉ IP sau mỗi lượt yêu cầu hoặc theo phiên định kỳ từ nhà cung cấp để tránh bị chặn. |
| **3** | **Điền thông số kết nối kỹ thuật:**<br>- **Tên gợi nhớ:** Đặt tên nhận diện (ví dụ: `Proxy Mỹ 01 - Dành Cho OpenAI`, `Proxy Singapore Residential Tốc Độ Cao`).<br>- **Địa chỉ máy chủ (Host / IP):** Nhập dãy số IP (ví dụ: `192.168.1.1`) hoặc tên miền máy chủ (`proxy.example.com`).<br>- **Cổng kết nối (Port):** Nhập số cổng quy định (ví dụ: `8080`, `1080`, `3128`...).<br>- **Giao thức (Protocol):** Chọn `HTTP`, `HTTPS`, hoặc `SOCKS5` (khuyên dùng `SOCKS5` cho các tác vụ cần bảo mật và tốc độ cao nhất).<br>- **Tài khoản & Mật khẩu xác thực:** Điền Username/Password do nhà cung cấp máy chủ cấp phát (nếu có yêu cầu xác thực).<br>- **Thời gian hết hạn:** Chọn thời hạn kết thúc hợp đồng thuê proxy hoặc để trống nếu gói cước không giới hạn. |
| **4** | Chọn nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo proxy)** để lưu máy chủ vào hệ thống. |

---

### Đo độ trễ phản hồi mạng thực tế (Ping Test) qua thẻ IconCard

Toàn bộ các thao tác trên bảng máy chủ trung gian đã được chuẩn hóa bằng các nút thẻ biểu tượng (`IconCard`) trực tiếp, không sử dụng menu con rườm rà và tuân thủ nguyên tắc không hiệu ứng viền (No Border Effects Rule).

Tính năng này giúp bạn đo lường tốc độ truyền tín hiệu thực tế giữa **nền tảng RedAI** và máy chủ trung gian chỉ trong 1-2 giây:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trong bảng danh sách, tìm đến dòng máy chủ cần kiểm tra. |
| **2** | Chọn biểu tượng <img src="https://api.iconify.design/lucide:wifi.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Test Ping)** ở cột Hành động. |
| **3** | Hệ thống lập tức gửi gói tin thăm dò và cập nhật kết quả mili-giây (ms) trên bảng kèm phân cấp màu trực quan:<br>- <span style="color:#16a34a">● **Dưới 200ms (Màu xanh lá - Rất tốt):**</span> Đường truyền cực kỳ ổn định và mượt mà, tối ưu cho mọi tác vụ thời gian thực.<br>- <span style="color:#d97706">● **Từ 200ms - 500ms (Màu vàng cam - Bình thường):**</span> Tốc độ chấp nhận được đối với các máy chủ đặt tại Châu Âu hoặc Bắc Mỹ.<br>- <span style="color:#dc2626">● **Trên 1000ms hoặc báo lỗi (Màu đỏ - Kém / Mất kết nối):**</span> Máy chủ đang bị nghẽn mạng nặng hoặc đã ngừng hoạt động, cần đổi sang máy chủ khác. |

---

### Xem chi tiết hồ sơ kỹ thuật và lịch sử vận hành của máy chủ

Giúp người quản trị kỹ thuật rà soát toàn bộ cấu hình, tỷ lệ thành công và các chỉ số hoạt động chi tiết:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại dòng máy chủ cần tra cứu, chọn biểu tượng <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xem)** ở cột Hành động. |
| **2** | Hộp thoại thông tin hiển thị:<br>- **Địa chỉ mạng IP thực xuất hiện ra ngoài:** Giúp xác minh xem nhà cung cấp bên ngoài sẽ nhìn thấy địa chỉ IP nào.<br>- **Tổng số lượt gọi thành công, thất bại và tỷ lệ thành công (% Success Rate).**<br>- **Thời gian phản hồi trung bình qua các ngày.**<br>- **Thời hạn hợp đồng thuê máy chủ.** |

---

### Chỉnh sửa và xóa máy chủ trung gian

Khi cần cập nhật thông số kết nối hoặc máy chủ đã hết hạn sử dụng:

| Thao tác | Cách thực hiện |
| :--- | :--- |
| **Chỉnh sửa cấu hình** | Chọn biểu tượng <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Chỉnh sửa)** tại dòng tương ứng để mở biểu mẫu cập nhật. Để trống trường mật khẩu nếu không muốn thay đổi mật khẩu hiện tại. |
| **Xóa máy chủ an toàn** | Chọn biểu tượng <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xóa)**. Hộp thoại xác nhận an toàn hiện ra, chọn đồng ý xóa để dọn sạch máy chủ khỏi kho hạ tầng. |

---

### Quản lý toàn diện Nhóm máy chủ luân phiên (Proxy Pools CRUD)

Khi một tác vụ đòi hỏi vận hành liên tục 24/7 (như giám sát tin nhắn mạng xã hội hay cào dữ liệu lớn), bạn nên nhóm nhiều máy chủ lại thành một **Nhóm Proxy (Proxy Pool)**. Phân hệ Proxy cung cấp riêng thẻ phụ <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy (Pools)** (`?subview=pools`) để quản trị toàn diện:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh điều hướng phân đoạn, chọn thẻ <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy (Pools)**. |
| **2** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo nhóm Pool)** ở góc trên bên phải để mở biểu mẫu cấu hình. |
| **3** | **Thiết lập thông số cho Nhóm Proxy Pool:**<br>- **Tên nhóm & Mô tả:** Đặt tên rõ ràng (ví dụ: `Cụm Dự Phòng Khu Vực Châu Á`, `LLM Gateway High Performance Pool`).<br>- **Thuật toán phân bổ (Allocation Mode):** Chọn 1 trong 6 thuật toán điều phối thông minh:<br>&nbsp;&nbsp;+ *Tuần tự (Round-Robin):* Phân bổ đều lần lượt qua từng máy chủ.<br>&nbsp;&nbsp;+ *Ít kết nối nhất (Least Connections):* Ưu tiên máy chủ đang có ít người dùng nhất.<br>&nbsp;&nbsp;+ *Ưu tiên hiệu năng (Performance):* Ưu tiên máy chủ có độ trễ thấp và phản hồi nhanh nhất.<br>&nbsp;&nbsp;+ *Ngẫu nhiên (Random):* Chọn ngẫu nhiên máy chủ trong nhóm.<br>&nbsp;&nbsp;+ *Cố định phiên (Sticky Session):* Giữ nguyên một máy chủ IP cho cùng một phiên làm việc/tài khoản.<br>&nbsp;&nbsp;+ *Định tuyến theo vị trí (Geo-based):* Chọn máy chủ gần nhất với khu vực địa lý của yêu cầu.<br>- **Mục đích sử dụng (Purpose):** Khai báo mục đích: *Đa mục đích (General)*, *LLM Gateway (AI Providers)*, *Zalo Platform*, hoặc *Web Scraping / Crawling*.<br>- **Tải người dùng tối đa mặc định:** Khống chế số lượng phiên đồng thời trên mỗi máy chủ (mặc định 10 users).<br>- **Cơ chế tự động xoay tua khi lỗi (Auto-rotate on failure):** Bật công tắc để hệ thống tự động đổi máy chủ khác khi phát hiện gián đoạn sau số lần thất bại quy định (mặc định 3 lần liên tiếp).<br>- **Nhóm mặc định (Default Pool):** Bật cờ này nếu muốn các kết nối chưa gán nhóm riêng sẽ tự động đi qua nhóm này. |
| **4** | Chọn nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo nhóm Pool)** để lưu cấu hình. |
| **5** | **Quản trị trên bảng danh sách Nhóm Pool:**<br>- Bật/tắt trạng thái hoạt động tức thì qua công tắc <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="16" alt="" /> **Switch** inline ngay trên bảng.<br>- Dùng nút thẻ <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Chỉnh sửa)** để thay đổi thuật toán hoặc ngưỡng xoay tua.<br>- Dùng nút thẻ <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xóa)** để gỡ bỏ nhóm pool an toàn. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể ra lệnh cho **trợ lý ảo AI Agent** tự động kiểm tra sức khỏe của toàn bộ hạ tầng mạng và đo tốc độ phản hồi của các máy chủ trung gian trực tiếp từ khung chat.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng cần kích hoạt**: Kỹ năng Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `d5731aab-1a2b-48a6-a904-5dd84ec1d4bd`.
- **Bộ công cụ sử dụng**: Bộ công cụ Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `ae8afc9a-1180-48d6-b672-d30171ccf3a6`.
- **Phạm vi hỗ trợ**: Tra cứu danh sách máy chủ proxy, kiểm tra tốc độ phản hồi Ping ms, xem thông số chi tiết và quản lý cụm máy chủ luân phiên.

---

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Kiểm tra tốc độ phản hồi toàn bộ máy chủ trung gian

Nhờ **trợ lý ảo AI Agent** rà soát xem máy chủ nào đang hoạt động nhanh nhất và phát hiện những máy chủ bị nghẽn mạng để kịp thời xử lý.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm nút kiểm tra tốc độ Ping ms từng máy chủ trên bảng danh sách. |
| **Công cụ Agent sử dụng** | `proxy_list` kết hợp với `proxy_ping` |
| **Thông tin cần cung cấp** | Yêu cầu đo tốc độ mạng và lọc các máy chủ có tín hiệu tốt. |

**Câu lệnh mẫu (Prompt):**
> "Hãy kiểm tra giúp tôi toàn bộ các máy chủ trung gian Proxy trong hệ thống. Báo cáo lại máy chủ nào có độ trễ dưới 200ms và máy chủ nào đang bị gián đoạn mạng."

---

#### 2. Tra cứu chi tiết hồ sơ kỹ thuật một máy chủ

Xem nhanh thông số kỹ thuật của một máy chủ mà không cần tìm kiếm trên bảng.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Bấm icon Xem chi tiết tại dòng máy chủ. |
| **Công cụ Agent sử dụng** | `proxy_get` |
| **Thông tin cần cung cấp** | Tên gợi nhớ hoặc địa chỉ IP của máy chủ. |

**Câu lệnh mẫu (Prompt):**
> "Hãy tra cứu giúp tôi thông số kỹ thuật chi tiết của máy chủ Proxy có tên là [Tên máy chủ, ví dụ: Proxy Singapore Tốc Độ Cao]."

---

#### 3. Tra cứu danh sách các cụm máy chủ luân phiên (Proxy Pools)

Kiểm tra xem các cụm máy chủ dự phòng đang gồm những máy chủ thành viên nào.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Mở danh sách Cụm máy chủ luân phiên. |
| **Công cụ Agent sử dụng** | `proxy_pool_list` hoặc `proxy_pool_get` |
| **Thông tin cần cung cấp** | Yêu cầu liệt kê các cụm máy chủ đang kích hoạt. |

**Câu lệnh mẫu (Prompt):**
> "Hãy liệt kê cho tôi danh sách các cụm máy chủ luân phiên Proxy Pools hiện có trong hệ thống và cho biết mỗi cụm đang có bao nhiêu máy chủ thành viên."

---

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Cách thực hiện | Dấu hiệu nhận biết thành công |
| :--- | :--- | :--- |
| **Kiểm tra trong khung chat** | Đọc báo cáo do trợ lý ảo AI Agent gửi lại. | Trợ lý ảo AI Agent trình bày bảng đo tốc độ phản hồi chi tiết (số ms), xếp hạng máy chủ từ nhanh nhất đến chậm nhất và cảnh báo rõ ràng các máy chủ bị lỗi. |
| **Kiểm tra trên màn hình Proxy** | Tải lại trang Danh sách máy chủ trên nền tảng RedAI. | Các chỉ số đo tốc độ vừa kiểm tra được cập nhật màu sắc tươi mới trên cột thời gian phản hồi. |
