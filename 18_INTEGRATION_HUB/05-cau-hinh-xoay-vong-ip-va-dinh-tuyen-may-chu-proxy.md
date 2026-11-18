## Mở khu vực Cấu hình xoay vòng mạng và Định tuyến máy chủ

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh điều hướng chính ở cột bên trái của **nền tảng RedAI**, chọn mục <img src="https://api.iconify.design/lucide:blocks.svg?color=%23ff3333" width="16" alt="" /> **Tích hợp**. |
| **2** | Chọn tiếp tab <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Máy chủ trung gian (Proxy)** (tại đường dẫn `/integrations/my-integrations?tab=proxy`). |
| **3** | Tùy theo nhu cầu quản trị và định tuyến đường truyền mạng, bạn chọn một trong bốn thẻ phụ chuyên biệt trên thanh điều hướng Segmented Header (hỗ trợ liên kết URL sâu `?subview=...`):<br>- <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Danh sách proxy** (`?subview=list`): Quản lý kho máy chủ trung gian đơn lẻ, giao thức kết nối, tài khoản xác thực, tỷ lệ thành công và đo độ trễ Ping.<br>- <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy (Pools)** (`?subview=pools`): Quản trị toàn diện vòng đời các nhóm máy chủ luân phiên, 6 thuật toán phân bổ tải, mục đích nghiệp vụ và ngưỡng tự động xoay tua khi có sự cố.<br>- <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **Proxy tài khoản** (`?subview=base-binding`): Gán đường truyền máy chủ chuyên biệt cho từng tài khoản kết nối cụ thể (Base Integration) kèm giám sát tải kết nối đồng thời theo thời gian thực.<br>- <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Proxy Provider** (`?subview=provider-binding`): Gán đường truyền máy chủ trung gian cho toàn bộ một Nhà cung cấp dịch vụ (ví dụ: Zalo, OpenAI, Anthropic, Gemini, Google). |

---

## Kiến trúc định tuyến đường truyền mạng đa tầng (Multi-tier Egress Routing)

Khi **nền tảng RedAI** hoặc **trợ lý ảo AI Agent** thực thi các cuộc gọi ra bên ngoài (gửi tin nhắn Zalo, gọi mô hình OpenAI, đồng bộ dữ liệu Google), hệ thống tự động giải quyết đường truyền qua cơ chế 5 tầng ưu tiên cao xuống thấp với bộ đệm siêu tốc Redis (TTL 60 giây):

```
[ Yêu cầu kết nối ra ngoài ]
         │
         ▼
┌────────────────────────────────────────────────────────┐
│ Tầng 1: Ràng buộc Tài khoản cụ thể (Base Integration)  │ ──► Tìm thấy? ──► Sử dụng Proxy chuyên biệt
└────────────────────────────────────────────────────────┘
         │ Không có
         ▼
┌────────────────────────────────────────────────────────┐
│ Tầng 2: Ràng buộc Nhà cung cấp (Provider Binding)       │ ──► Tìm thấy? ──► Sử dụng Proxy / Pool
└────────────────────────────────────────────────────────┘
         │ Không có
         ▼
┌────────────────────────────────────────────────────────┐
│ Tầng 3: Ràng buộc Mặc định Base (Workspace Default)     │ ──► Tìm thấy? ──► Sử dụng Proxy Base mặc định
└────────────────────────────────────────────────────────┘
         │ Không có
         ▼
┌────────────────────────────────────────────────────────┐
│ Tầng 4: Chính sách Mạng Doanh nghiệp (Policy Fallback) │ ──► Tìm thấy? ──► Phân bổ theo quy chuẩn
└────────────────────────────────────────────────────────┘
         │ Không có
         ▼
┌────────────────────────────────────────────────────────┐
│ Tầng 5: Kết nối trực tiếp (Direct Connection)          │ ──► Truy cập thẳng từ hạ tầng an toàn RedAI
└────────────────────────────────────────────────────────┘
```

---

## Các tính năng

### 1. Quản lý danh mục máy chủ Proxy đơn lẻ (Proxy List)

Kho lưu trữ, giám sát và vận hành các máy chủ trung gian đơn lẻ của doanh nghiệp:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Chuyển sang thẻ phụ <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Danh sách proxy** (`?subview=list`). |
| **2** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo Proxy)** ở góc trên bên phải. |
| **3** | **Lựa chọn loại hình Proxy qua thẻ tương tác trực quan:**<br>- <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Proxy tĩnh (Static):** Duy trì IP cố định cho mọi kết nối ra ngoài, phù hợp khi cần whitelist IP tại đối tác.<br>- <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Proxy xoay (Rotating):** Tự động đổi IP theo phiên định kỳ từ nhà cung cấp mạng. |
| **4** | **Điền thông số kết nối máy chủ:**<br>- **Tên Proxy:** Đặt tên nhận diện trực quan (ví dụ: `Proxy Mỹ 01 - OpenAI`, `Proxy Singapore Residential`).<br>- **Địa chỉ máy chủ (Host) & Cổng (Port):** Nhập IP hoặc tên miền cùng số cổng kết nối.<br>- **Giao thức (Protocol):** Hỗ trợ đầy đủ `HTTP`, `HTTPS`, `SOCKS5`.<br>- **Thông tin xác thực:** Tên đăng nhập và Mật khẩu (được mã hóa bảo mật tuyệt đối).<br>- **Ghi chú & Thời gian hết hạn:** Điền ghi chú quản trị và hạn kết thúc hợp đồng thuê proxy (nếu có). |
| **5** | Chọn nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo proxy)** để hoàn tất. Các thao tác đo tốc độ <img src="https://api.iconify.design/lucide:wifi.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Test Ping)**, xem chi tiết <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xem)**, chỉnh sửa <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Chỉnh sửa)** và xóa <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xóa)** đều được thực hiện trực tiếp trên từng dòng của bảng. |

---

### 2. Thiết lập cơ chế xoay vòng địa chỉ IP mạng (Proxy Allocation Mode)

Tại thẻ phụ <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy (Pools)** (`?subview=pools`), bạn có thể nhóm nhiều máy chủ trung gian thành một cụm dự phòng và lựa chọn cơ chế phân bổ đường truyền tối ưu:

| Cơ chế phân bổ IP | Ý nghĩa và trường hợp áp dụng |
| :--- | :--- |
| **Xoay vòng lần lượt (Round-Robin)** | Hệ thống luân phiên chuyển qua từng máy chủ trong nhóm: Yêu cầu 1 qua Máy chủ A, yêu cầu 2 qua Máy chủ B, yêu cầu 3 qua Máy chủ C rồi lặp lại. Phù hợp chia đều tải trọng mạng. |
| **Ít kết nối nhất (Least Connections)** | Tự động ưu tiên chọn máy chủ đang có số lượng kết nối đồng thời thấp nhất trong nhóm. Giúp triệt tiêu hiện tượng nghẽn mạng cục bộ. |
| **Ưu tiên hiệu năng (Performance)** | Tự động chọn máy chủ có độ trễ (latency) thấp nhất và tỷ lệ thành công cao nhất trong các phiên gần nhất. Tối ưu cho tác vụ gọi AI thời gian thực. |
| **Xoay vòng ngẫu nhiên (Random)** | Hệ thống bốc thăm ngẫu nhiên một máy chủ đang hoạt động. Giúp hành vi truy cập phân tán tự nhiên từ nhiều dải mạng khác nhau. |
| **Giữ kết nối ổn định (Sticky Session)** | Giữ nguyên một máy chủ trung gian cho toàn bộ phiên làm việc của một tài khoản. Bắt buộc cho các nền tảng chat đòi hỏi duy trì phiên đăng nhập liên tục. |
| **Định tuyến theo vị trí (Geo-based)** | Tự động chọn máy chủ proxy gần nhất với khu vực địa lý của yêu cầu gửi đến. |

Bên cạnh thuật toán phân bổ, bạn có thể thiết lập:
- **Mục đích sử dụng (Purpose):** Quy định nhóm phục vụ cho *Đa mục đích (GENERAL)*, *Cổng AI (LLM_GATEWAY)*, *Nền tảng Zalo (ZALO)*, hoặc *Thu thập dữ liệu (SCRAPING)*.
- **Tự động xoay tua khi lỗi (Auto-rotate on failure):** Bật công tắc để hệ thống tự động đổi máy chủ khác khi phát hiện gián đoạn liên tiếp (mặc định sau 3 lần lỗi).
- **Nhóm mặc định (Default Pool):** Đánh dấu cờ nhóm mặc định cho toàn bộ không gian làm việc.

---

### 3. Gán máy chủ trung gian cho Nhà cung cấp dịch vụ (Proxy Provider Binding)

Giúp bạn chỉ định riêng toàn bộ một Nhà cung cấp dịch vụ (như Zalo, OpenAI, Anthropic, Gemini, Google) bắt buộc phải đi qua máy chủ trung gian:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Chuyển sang thẻ phụ <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Proxy Provider** (`?subview=provider-binding`). |
| **2** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm liên kết Provider - Proxy)** ở góc trên bên phải. |
| **3** | **Lựa chọn thông số gán:**<br>- **Nhà cung cấp Tích hợp:** Chọn nhà cung cấp trong danh mục (ví dụ: `Zalo`, `OpenAI`, `Google Cloud`, `Anthropic`...).<br>- **Phương thức gán Proxy qua thẻ trực quan:**<br>&nbsp;&nbsp;+ <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Proxy đơn lẻ:** Gán 1 địa chỉ IP/Port cố định cho Nhà cung cấp.<br>&nbsp;&nbsp;+ <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Nhóm Proxy Pool:** Tự động cân bằng tải và luân phiên giữa các proxy trong cụm.<br>- **Chọn Proxy hoặc Nhóm Pool:** Nếu chọn Nhóm Pool, bạn có thể chọn nhanh từ danh sách khả dụng hoặc bấm nút thẻ <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Nhập UUID thủ công / Chọn danh sách)** để điền ID nhóm linh hoạt.<br>- **Độ ưu tiên (Priority):** Đặt chỉ số ưu tiên từ 1 đến 100 (chỉ số càng cao thì hệ thống càng ưu tiên dùng đường truyền đó trước).<br>- **Trạng thái kích hoạt:** Bật công tắc để đường truyền bắt đầu hoạt động ngay lập tức. |
| **4** | Chọn nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Tạo liên kết)**. Mọi cuộc gọi ra ngoài từ nhà cung cấp đó sẽ tự động chuyển tiếp an toàn qua máy chủ trung gian đã chỉ định. |
| **5** | **Quản trị trực tiếp trên bảng liên kết Provider:**<br>- Bật/tắt trạng thái hoạt động tức thì qua công tắc <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="16" alt="" /> **Switch** inline ngay trên bảng.<br>- Chỉnh sửa cấu hình liên kết qua nút thẻ <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Chỉnh sửa)**.<br>- Gỡ bỏ liên kết an toàn qua nút thẻ <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xóa)**. |

---

### 4. Gán máy chủ trung gian cho Tài khoản kết nối cụ thể (Proxy Base Binding)

Áp dụng khi bạn muốn gán máy chủ trung gian chuyên biệt cho một tài khoản kết nối cụ thể trong không gian làm việc hoặc thiết lập mặc định cho toàn bộ cơ sở dữ liệu Base:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Chuyển sang thẻ phụ <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> **Proxy tài khoản** (`?subview=base-binding`). |
| **2** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gán proxy cho Base)** ở góc trên bên phải. |
| **3** | **Điền thông số ràng buộc:**<br>- **Máy chủ trung gian:** Chọn máy chủ proxy trong danh sách khả dụng.<br>- **Tài khoản áp dụng:** Chọn một tài khoản cụ thể trong danh sách hoặc chọn *Tất cả tài khoản trong Base (Mặc định)*.<br>- **Mức ưu tiên:** Thiết lập chỉ số ưu tiên (1 - 100).<br>- **Giới hạn luồng truy cập đồng thời (Max Concurrency):** Đặt số luồng tối đa được phép gọi cùng một lúc (ví dụ: `5` hoặc `10` luồng) để tránh làm nghẽn đường truyền. |
| **4** | Chọn nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu ràng buộc)** để kích hoạt. |
| **5** | **Giám sát tải đồng thời và điều khiển trực tiếp trên bảng Base Binding:**<br>- **Giám sát tải thời gian thực (Live Concurrency Telemetry):** Bảng hiển thị tỷ lệ luồng đồng thời `currentConcurrency / maxConcurrencyForBase` kèm Chip trạng thái phân cấp màu sắc trực quan:<br>&nbsp;&nbsp;+ <span style="color:#d97706">● **Đầy tải (warning - màu vàng cam):**</span> Khi số luồng hiện tại đạt ngưỡng tối đa quy định.<br>&nbsp;&nbsp;+ <span style="color:#16a34a">● **Sẵn sàng (default - màu xanh lá):**</span> Khi còn dung lượng kết nối khả dụng.<br>- **Bật/tắt trạng thái tức thì:** Thao tác qua công tắc <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="16" alt="" /> **Switch** inline ngay trên cột trạng thái mà không cần mở modal.<br>- **Chỉnh sửa cấu hình:** Bấm nút thẻ <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Chỉnh sửa)** để cập nhật mức ưu tiên, giới hạn luồng hoặc kích hoạt lại.<br>- **Gỡ gán an toàn:** Bấm nút thẻ <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Gỡ gán)** để hủy liên kết. |

---

### 5. Gỡ bỏ liên kết định tuyến máy chủ trung gian

Khi bạn muốn đưa nhà cung cấp hoặc tài khoản trở về chế độ kết nối mạng trực tiếp mặc định của **nền tảng RedAI**:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trong bảng danh sách gán máy chủ (tại thẻ <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> `provider-binding` hoặc <img src="https://api.iconify.design/lucide:link-2.svg?color=%23ff3333" width="16" alt="" /> `base-binding`), tìm đến dòng cần gỡ bỏ. |
| **2** | Chọn nút thẻ <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> `IconCard` **(Xóa / Gỡ gán)** ở cột Hành động. |
| **3** | Hộp thoại xác nhận an toàn hiện lên. Chọn <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Đồng ý)**. Kết nối sẽ được gỡ bỏ an toàn mà không làm gián đoạn tài khoản hay dịch vụ. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể ra lệnh cho **trợ lý ảo AI Agent** tự động tra cứu cấu hình proxy, gán đường truyền tối ưu cho dịch vụ hoặc hủy gán nhanh chóng trực tiếp từ khung chat.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng cần kích hoạt**: Kỹ năng Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `d5731aab-1a2b-48a6-a904-5dd84ec1d4bd`.
- **Bộ công cụ sử dụng**: Bộ công cụ Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `ae8afc9a-1180-48d6-b672-d30171ccf3a6`.
- **Phạm vi hỗ trợ**: Tra cứu danh sách proxy, liên kết máy chủ trung gian cho nhà cung cấp hoặc tài khoản, thiết lập thứ tự ưu tiên và hủy gán an toàn.

---

### Các tính năng thao tác qua trợ lý ảo AI Agent

#### 1. Tra cứu danh sách máy chủ Proxy hiện có

Xem nhanh thông tin các máy chủ proxy, giao thức và trạng thái kết nối.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Xem bảng danh sách tại thẻ Danh sách máy chủ Proxy. |
| **Công cụ Agent sử dụng** | `proxy_list` |
| **Thông tin cần cung cấp** | Yêu cầu tra cứu danh sách máy chủ proxy hiện hành. |

**Câu lệnh mẫu (Prompt):**
> "Hãy tra cứu giúp tôi danh sách tất cả các máy chủ Proxy đang hoạt động trong hệ thống kèm giao thức kết nối và tình trạng sẵn sàng."

---

#### 2. Tự động gán máy chủ trung gian cho Nhà cung cấp

Ra lệnh cho **trợ lý ảo AI Agent** liên kết nhà cung cấp dịch vụ với một cụm máy chủ hoặc máy chủ an toàn.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Mở form Tạo liên kết Provider-Proxy và chọn Lưu thiết lập. |
| **Công cụ Agent sử dụng** | `proxy_provider_binding_create` |
| **Thông tin cần cung cấp** | Tên nhà cung cấp, tên máy chủ hoặc cụm máy chủ muốn gán, mức độ ưu tiên. |

**Câu lệnh mẫu (Prompt):**
> "Hãy gán nhà cung cấp OpenAI đi qua cụm máy chủ luân phiên [Tên cụm máy chủ, ví dụ: Cụm Proxy AI Châu Á] với mức ưu tiên cao nhất."

---

#### 3. Tra cứu danh sách định tuyến máy chủ hiện hành

Kiểm tra xem hiện tại công ty đang có những nhà cung cấp hoặc tài khoản nào đi qua máy chủ trung gian.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Xem bảng danh sách tại thẻ Proxy nhà cung cấp (`provider-binding`). |
| **Công cụ Agent sử dụng** | `proxy_provider_binding_list` |
| **Thông tin cần cung cấp** | Yêu cầu xem danh sách các liên kết định tuyến hiện hành. |

**Câu lệnh mẫu (Prompt):**
> "Hãy liệt kê cho tôi danh sách tất cả các nhà cung cấp hiện đang được định tuyến qua máy chủ trung gian Proxy kèm tên máy chủ và mức độ ưu tiên của từng liên kết."

---

#### 4. Gỡ bỏ liên kết định tuyến máy chủ

Hủy gán máy chủ trung gian để đưa nhà cung cấp về chế độ kết nối mạng trực tiếp.

| Mục | Chi tiết |
| :--- | :--- |
| **Thao tác tương đương trên UI** | Chọn nút Hủy gán tại dòng liên kết trên bảng liên kết. |
| **Công cụ Agent sử dụng** | `proxy_provider_binding_delete` |
| **Thông tin cần cung cấp** | Tên nhà cung cấp cần hủy gán đường truyền máy chủ trung gian. |

**Câu lệnh mẫu (Prompt):**
> "Hãy giúp tôi gỡ bỏ liên kết máy chủ trung gian Proxy của nhà cung cấp OpenAI để đưa nhà cung cấp này trở về chế độ kết nối mạng mặc định của nền tảng RedAI."

---

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Cách thực hiện | Dấu hiệu nhận biết thành công |
| :--- | :--- | :--- |
| **Kiểm tra trong khung chat** | Đọc báo cáo phản hồi của trợ lý ảo AI Agent. | Trợ lý ảo AI Agent thông báo xác nhận đã thiết lập liên kết thành công kèm bảng tóm tắt tên nhà cung cấp, máy chủ được chọn và mức độ ưu tiên. |
| **Kiểm tra trên màn hình Proxy** | Chuyển sang thẻ Proxy nhà cung cấp (`provider-binding`) trên nền tảng RedAI. | Dòng liên kết mới xuất hiện đầy đủ thông tin với công tắc hoạt động màu xanh sẵn sàng. |
