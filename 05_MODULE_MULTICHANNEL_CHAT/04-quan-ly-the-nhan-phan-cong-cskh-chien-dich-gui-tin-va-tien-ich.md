## Tổng quan các tính năng quản trị nâng cao và tiếp thị đa kênh

Bên cạnh các tác vụ nhắn tin và trao đổi trực tiếp, **OmniAI Chat (Multichannel Chat)** được trang bị một hệ sinh thái công cụ quản trị vận hành và tiếp thị tự động hóa mạnh mẽ. Các tính năng này giúp doanh nghiệp chuẩn hóa quy trình phân loại khách hàng, phân công nhiệm vụ cho đội ngũ chăm sóc khách hàng (CSKH), xây dựng kho mẫu tin nhắn tương tác và phát động các chiến dịch gửi tin nhắn đa kênh quy mô lớn dựa trên dữ liệu thực tế từ Bảng dữ liệu động (Dynamic Table).

Đặc biệt, hệ thống tích hợp **Trung tâm Tiện ích (Multichannel Utilities Modal)** với kiến trúc 2 cấp độ trực quan (Màn hình Danh mục & Màn hình Chi tiết) cùng cơ chế Ghim linh hoạt (Pin to Toolbar), quy tụ trọn bộ 5 công cụ hỗ trợ tiếp thị và đồng bộ dữ liệu chuyên sâu cho nền tảng đa kênh và Zalo Cá nhân.

Tài liệu này tổng hợp hướng dẫn chi tiết cho 8 tính năng quản trị, tiếp thị và tiện ích mở rộng cốt lõi:

1. **Quản trị thẻ nhãn (Tags) & Phân loại hội thoại**: Tạo danh mục nhãn màu sắc trực quan, gắn/gỡ nhãn theo từng cuộc trò chuyện hoặc thực thi hàng loạt.
2. **Phân công nhân sự CSKH, Bật/Tắt AI Chat & Trường dữ liệu tùy chỉnh**: Gán nhân viên phụ trách chính, thêm người hỗ trợ, kiểm soát tự động trả lời bằng AI và chỉnh sửa trực tiếp các trường dữ liệu tùy chỉnh của bảng hội thoại.
3. **Kiến trúc Trung tâm Tiện ích & Cơ chế Ghim tiện ích (Pin Utilities)**: Khám phá giao diện danh mục 5 tiện ích, điều hướng 2 cấp độ và cơ chế ghim tối đa 2 tiện ích lên thanh công cụ của Chat Sidebar.
4. **Tiện ích 1 — Mẫu Template Tin Nhắn (`TEMPLATES`)**: Thiết kế các khối nội dung mẫu (văn bản, hình ảnh, sticker, nút bấm CTA) kèm các biến động placeholder để tái sử dụng tức thì.
5. **Tiện ích 2 — Chiến Dịch Gửi Tin Nhắn Đa Kênh (`CAMPAIGNS`)**: Quy trình 4 bước tạo chiến dịch gửi tin tự động từ Bảng dữ liệu động, xoay tua mẫu tin, cài đặt giãn cách chống spam và theo dõi tiến độ gửi thời gian thực.
6. **Tiện ích 3 — Thu Thập Group Zalo Bằng Link (`CRAWL_GROUPS`)**: Quét link nhóm Zalo `https://zalo.me/g/...`, tự động tham gia nhóm, ánh xạ 15 trường dữ liệu thành viên và nhóm vào Bảng dữ liệu động và gắn tag tự động.
7. **Tiện ích 4 — Đồng bộ Nhãn Zalo cá nhân vào Tag (`SYNC_LABELS`)**: Quét toàn bộ nhãn phân loại từ tài khoản Zalo cá nhân, tự động chuyển đổi thành Tag hệ thống và gắn tương ứng cho các cuộc trò chuyện.
8. **Tiện ích 5 — Đồng bộ Tên hiển thị Zalo (`SYNC_DISPLAY_NAMES`)**: Quét tên gợi nhớ (biệt danh / alias) từ danh bạ Zalo cá nhân để tự động đồng bộ hóa vào tên hiển thị của khách hàng trên hệ thống.

---

## Hướng dẫn chi tiết từng tính năng

### Tính năng 1 — Quản trị thẻ nhãn (Tags) & Phân loại hội thoại

Thẻ nhãn (Tags) là công cụ phân loại nhanh giúp toàn bộ đội ngũ nhận diện ngay nhóm khách hàng (ví dụ: `Khách VIP`, `Cần Chăm Sóc Lại`, `Khiếu Nại Sản Phẩm`, `Đã Ký Hợp Đồng`).

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở ngăn quản lý nhãn của hội thoại** | Tại thanh thông tin bên phải (`ConversationInfoSidebar`), cuộn đến mục <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **Nhãn (Tags)**. |
| **2. Gán nhãn có sẵn** | Nhấp vào ô chọn nhãn: Danh sách các nhãn trong không gian làm việc sẽ hiển thị kèm màu sắc tương ứng. Nhấp chọn một hoặc nhiều nhãn để gắn ngay vào cuộc trò chuyện. |
| **3. Tạo nhãn mới trực tiếp** | Nếu chưa có nhãn phù hợp, nhập tên nhãn mới vào ô (ví dụ: `Khách Tham Quan Showroom`) $\rightarrow$ Bấm nút **+ Thêm nhãn mới** $\rightarrow$ Chọn một trong các mã màu nhận diện nổi bật trong bảng màu (Đỏ, Cam, Vàng, Xanh lá, Xanh dương, Tím...) $\rightarrow$ Bấm **Xác nhận**. Nhãn mới sẽ được tạo vào danh mục dùng chung và gắn ngay vào hội thoại. |
| **4. Gỡ nhãn khỏi hội thoại** | Nhấp vào biểu tượng dấu <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="14" alt="" /> trên từng thẻ nhãn để gỡ bỏ nhãn đó khỏi cuộc trò chuyện hiện tại. |
| **5. Gắn / Gỡ nhãn hàng loạt** | Tại danh sách hội thoại bên trái, sử dụng tính năng chọn nhiều cuộc trò chuyện $\rightarrow$ Thanh công cụ hành động hàng loạt xuất hiện ở cạnh dưới $\rightarrow$ Chọn **Gán nhãn hàng loạt** để cập nhật đồng bộ cho hàng chục khách hàng cùng lúc. |

---

### Tính năng 2 — Phân công nhân sự CSKH, Bật/Tắt AI Chat & Quản lý trường dữ liệu tùy chỉnh

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Bật/Tắt tự động trả lời bằng AI Chat** | Tại mục **AI Chat** trên thanh thông tin bên phải, bật/tắt công tắc <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Tự động trả lời cuộc trò chuyện này**:<br>• Khi **BẬT**: Trợ lý ảo AI Agent sẽ tự động đọc tin nhắn đến và phản hồi khách hàng theo kịch bản tri thức doanh nghiệp.<br>• Khi **TẮT**: Trợ lý AI ngừng can thiệp, nhường toàn quyền xử lý cho nhân viên trực ca. |
| **2. Phân công người phụ trách (Assignee & Collaborators)** | Tại mục <img src="https://api.iconify.design/lucide:user-check.svg?color=%23ff3333" width="16" alt="" /> **Người hỗ trợ**:<br>• Nhấp vào ô chọn nhân viên để xem danh sách thành viên trong Không gian làm việc.<br>• Chọn nhân viên chịu trách nhiệm chính (Assignee).<br>• Bổ sung thêm các nhân viên hỗ trợ (Collaborators) để cùng theo dõi và phối hợp xử lý sự vụ phức tạp. |
| **3. Xem danh sách người tham gia (Participants)** | Nhấp vào mục **Người tham gia** để kiểm tra toàn bộ danh sách đối tượng trong cuộc trò chuyện: Khách hàng, Chuyên viên tư vấn, Trợ lý ảo Bot và Quản trị viên kèm vai trò và trạng thái trực tuyến. |
| **4. Chỉnh sửa trường dữ liệu tùy chỉnh (Custom Fields)** | Mục **Trường thông tin (Custom Fields)** kết nối trực tiếp với bảng dữ liệu động hệ thống `multichannel_conversations`:<br>• Hiển thị toàn bộ các cột bổ sung như: *Nguồn khách hàng*, *Doanh số ước tính*, *Giai đoạn bán hàng*, *Ngày hẹn tư vấn*...<br>• Nhấp trực tiếp vào ô để sửa dữ liệu bằng trình soạn thảo ô bảng tính (**GridCellEditor**) mà không cần chuyển sang màn hình Database.<br>• Bấm nút **+ Thêm trường** để mở hộp thoại cấu hình cột (**ColumnEditorModal**) nếu muốn bổ sung thêm trường thông tin mới cho toàn bộ các cuộc trò chuyện. |

---

### Tính năng 3 — Kiến trúc Trung tâm Tiện ích & Cơ chế Ghim tiện ích (Pin Utilities)

Trung tâm Tiện ích (**MultichannelUtilitiesModal**) được thiết kế theo cấu trúc điều hướng 2 cấp độ trực quan, hỗ trợ tối ưu hóa thao tác hàng ngày thông qua cơ chế ghim nhanh:

```
[Màn hình Chat Sidebar] ──(Bấm nút Zap Tiện ích)──> [CẤP 1: Danh mục 5 Tiện ích]
                                                             │
                  ┌──────────────────────────────────────────┴──────────────────────────────────────────┐
                  │                                                                                     │
         [Bấm Đinh ghim (Pin)]                                                                 [Bấm vào Thẻ tiện ích]
                  │                                                                                     │
        [Ghim tối đa 2 tiện ích                                                               [CẤP 2: Màn hình Chi tiết]
        lên Toolbar Chat Sidebar]                                                             (Breadcrumb + Footer động)
```

| Thành phần trên Giao diện | Cách hiển thị và tương tác người dùng |
| :--- | :--- |
| **1. Mở Trung tâm Tiện ích** | Bấm vào nút biểu tượng tia chớp màu vàng <img src="https://api.iconify.design/lucide:zap.svg?color=%23ff3333" width="16" alt="" /> **(Tiện ích)** trên thanh công cụ phía trên của Chat Sidebar. Hộp thoại kích thước toàn màn hình mở ra với tiêu đề **Trung tâm Tiện ích**. |
| **2. Cấp 1 — Lưới thẻ danh mục tiện ích (Catalog View)** | Giao diện hiển thị danh mục 5 thẻ tiện ích (bố cục 2 cột trên Desktop, 1 cột trên Mobile). Mỗi thẻ gồm:<br>• **Icon nhận diện & Màu nền**: Màu xanh dương cho Template, tím cho Chiến dịch, xanh ngọc cho Cào nhóm, xanh lá đậm cho Đồng bộ nhãn, chàm cho Đồng bộ tên hiển thị.<br>• **Tiêu đề & Huy hiệu (Badge)**: Hiển thị số lượng mẫu tin (`{count} mẫu tin`), số lượng chiến dịch (`{count} chiến dịch`) hoặc nhãn `Zalo Personal`.<br>• **Mô tả tính năng**: Tóm tắt ngắn gọn phạm vi và mục đích của tiện ích.<br>• **Nút bấm Đinh ghim <img src="https://api.iconify.design/lucide:pin.svg?color=%23ff3333" width="16" alt="" />**: Nằm ở góc phải của từng thẻ. |
| **3. Cơ chế Ghim tiện ích (Pin / Unpin)** | • Người dùng có thể bấm vào biểu tượng đinh ghim trên thẻ để đưa tiện ích ra ngoài thanh công cụ Chat Sidebar.<br>• **Giới hạn số lượng**: Hệ thống cho phép ghim tối đa **2 tiện ích** cùng lúc (`MAX_PINNED_MULTICHANNEL_UTILITIES = 2`).<br>• **Cảnh báo vượt hạn mức**: Nếu đã ghim đủ 2 tiện ích mà người dùng bấm ghim thêm tiện ích thứ 3, hệ thống sẽ hiển thị thông báo nổi: *"Chỉ có thể ghim tối đa 2 tiện ích lên thanh công cụ"*.<br>• **Nhận diện trạng thái**: Tiện ích đã ghim sẽ có icon đinh ghim xoay nghiêng 45 độ và đổi màu chủ đạo (Primary color). Khi ra ngoài Chat Sidebar, 2 tiện ích này xuất hiện thành 2 nút bấm nhanh trực tiếp trên header, bấm vào là mở thẳng màn hình chi tiết của tiện ích đó mà không cần qua menu trung gian. |
| **4. Cấp 2 — Màn hình Chi tiết Tiện ích (Full View Panel)** | Khi nhấp chuột vào bất kỳ thẻ tiện ích nào, hệ thống chuyển sang màn hình làm việc chi tiết:<br>• **Thanh Header điều hướng**: Nút <img src="https://api.iconify.design/lucide:chevron-left.svg?color=%23ff3333" width="16" alt="" /> **Quay lại danh mục tiện ích** bên trái, kèm đường dẫn breadcrumb: `Tiện ích / <Tên tiện ích đang chọn>`.<br>• **Khung nội dung chính**: Hiển thị toàn bộ trình quản lý chuyên biệt của tiện ích được chọn.<br>• **Chân trang (Footer) động ngữ cảnh**: Với các tiện ích Zalo Cá nhân, thanh footer sẽ hiển thị nút **Xem lịch sử chạy ngầm** (<img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" />), nút **Đóng** (<img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" />) và nút **Thực thi chính** (<img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" />) kèm số lượng mục tiêu đã chọn và hiệu ứng quay vòng khi đang xử lý (loading spinner). |

---

### Tính năng 4 — Tiện ích 1: Quản lý mẫu tin nhắn chuẩn hóa (TEMPLATES)

Tiện ích **Mẫu Template Tin Nhắn (`TEMPLATES`)** giúp đội ngũ CSKH và tiếp thị xây dựng kho mẫu tin nhắn tương tác chất lượng cao, hỗ trợ đa dạng khối nội dung và biến động tự động điền:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở Trình quản lý Template** | Trong Trung tâm Tiện ích, bấm chọn thẻ <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Mẫu Template Tin Nhắn (TEMPLATES)**. Màn hình quản lý mở ra với thanh công cụ tìm kiếm, bộ lọc phiên bản (V1 / V2), bộ lọc nhãn (#tags) và danh sách các mẫu tin hiện có kèm huy hiệu số lượng. |
| **2. Bấm nút Tạo mẫu tin nhắn mới** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo mẫu tin nhắn** để mở hộp thoại soạn thảo (**OmnichannelTemplateFormModal**). |
| **3. Khai báo thông tin nhận diện** | • **Tên mẫu tin \***: Nhập tên gợi nhớ (ví dụ: `Xác Nhận Đặt Lịch Hẹn Tư Vấn Khách VIP`).<br>• **Nền tảng áp dụng**: Chọn kênh hỗ trợ (Tất cả, Zalo OA, Zalo Cá nhân, Facebook Messenger, SMS).<br>• **Mã code định danh**: Nhập mã định danh duy nhất (ví dụ: `XN_LICH_HEN_VIP`).<br>• **Mô tả**: Nhập ghi chú về thời điểm và ngữ cảnh áp dụng mẫu tin.<br>• **Thẻ nhãn (Tags)**: Nhập từ khóa phân loại và bấm Enter để gắn tag cho mẫu tin. |
| **4. Soạn thảo khối tin nhắn kéo thả (Draggable Messages)** | Hộp thoại hỗ trợ cấu trúc nhiều khối tin nhắn gửi liên hoàn, cho phép kéo thả tay cầm icon <img src="https://api.iconify.design/lucide:grip-vertical.svg?color=%23ff3333" width="14" alt="" /> để đổi thứ tự:<br>• **Khối Tin nhắn Văn bản**: Soạn thảo nội dung và chèn các biến placeholder dạng `{{customer_name}}`, `{{phone}}`, `{{appointment_time}}`, `{{order_code}}`. Khi gửi thực tế, các biến này sẽ tự động thay bằng dữ liệu khách hàng tương ứng.<br>• **Khối Hình ảnh & Tệp đính kèm**: Bấm nút mở **Thư viện đa kênh (MultichannelLibraryModal)** để chọn ảnh banner, catalogue PDF hoặc video tải lên từ máy tính.<br>• **Khối Sticker sinh động**: Bấm biểu tượng Sticker để mở bảng chọn **StickerPickerModal**, chọn sticker Zalo cảm xúc phù hợp.<br>• **Khối Nút bấm tương tác (CTA Buttons)**: Thêm các nút điều hướng bên dưới tin nhắn gồm: *Mở liên kết Web (Open URL)*, *Gọi điện trực tiếp (Call Phone)* hoặc *Gửi dữ liệu phản hồi nhanh (Payload Postback)*. |
| **5. Xem trước hiển thị trên Mobile** | Bấm nút <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Xem trước mẫu tin (OmnichannelTemplatePreviewModal)**: Hệ thống mô phỏng khung hình điện thoại chân thực cho từng nền tảng (Zalo / Messenger / SMS) để bạn kiểm tra trực quan khoảng ngắt dòng và vị trí nút bấm. Bấm **Lưu mẫu tin** để hoàn tất. |

---

### Tính năng 5 — Tiện ích 2: Phát động chiến dịch gửi tin nhắn đa kênh (CAMPAIGNS)

Tiện ích **Chiến Dịch Gửi Tin Nhắn (`CAMPAIGNS`)** cho phép doanh nghiệp phát động các chiến dịch tương tác, chăm sóc khách hàng hàng loạt từ Bảng dữ liệu động với kiểm soát giãn cách delay chống khóa tài khoản:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở Trình quản lý Chiến dịch** | Trong Trung tâm Tiện ích, chọn thẻ <img src="https://api.iconify.design/lucide:rocket.svg?color=%23ff3333" width="16" alt="" /> **Chiến Dịch Gửi Tin Nhắn (CAMPAIGNS)**. Giao diện hiển thị 4 thẻ KPI thống kê trên đỉnh (*Tổng số*, *Đang chạy*, *Hoàn thành*, *Thất bại / Tạm dừng*) và bảng danh sách chiến dịch kèm bộ lọc 7 trạng thái (*Tất cả, Nháp, Đã lên lịch, Đang chạy, Tạm dừng, Hoàn thành, Đã hủy, Lỗi*). |
| **2. Khởi tạo Wizard 4 bước** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch mới** để mở hộp thoại cấu hình (**OmnichannelCampaignCreateModal**). Thanh tiến trình trên cùng hiển thị 4 bước rõ ràng: *1. Thông tin chung $\rightarrow$ 2. Chọn Template $\rightarrow$ 3. Bộ lọc Đối tượng $\rightarrow$ 4. Cài đặt & Xác nhận*. |
| **3. Bước 1 — Thông tin chung** | • **Tên chiến dịch \***: Nhập tên gợi nhớ (ví dụ: `Chiến Dịch CSKH Tái Tương Tác Tháng 10`).<br>• **Mô tả mục tiêu**: Ghi chú mục đích của đợt gửi tin.<br>• **Chiến lược phân bổ Template (Rotation Strategy)**: Chọn *Chia đều lần lượt (Round Robin)* để phân bổ luân phiên các mẫu tin cho từng khách hàng hoặc chọn *Ngẫu nhiên (Random)* để tránh bị thuật toán nền tảng nghi vấn spam nội dung lặp lại.<br>• **Lên lịch phát động hẹn giờ**: Bật công tắc hẹn giờ và chọn ngày giờ cụ thể bằng bộ chọn **DateTimePicker** (hoặc để trống nếu muốn phát động ngay sau khi tạo). |
| **4. Bước 2 — Chọn Template & Ánh xạ biến** | • Tích chọn 1 hoặc nhiều mẫu tin nhắn áp dụng trong chiến dịch (có ô tìm kiếm và nút tạo nhanh template mới).<br>• **Cấu hình Ánh xạ biến (Variable Mapping)**: Nếu các template đã chọn có chứa các placeholder (`{{name}}`, `{{code}}`, `{{date}}`), hệ thống sẽ mở bảng cấu hình ánh xạ:<br>  + *Chế độ Giá trị tĩnh (Static)*: Nhập một giá trị cố định áp dụng chung cho mọi khách hàng.<br>  + *Chế độ Cột động (Dynamic)*: Chọn cột dữ liệu tương ứng trong bảng dữ liệu đích kèm **Giá trị mặc định thay thế (Fallback Value)** trong trường hợp ô dữ liệu của khách hàng bị trống. |
| **5. Bước 3 — Bộ lọc Đối tượng nhận tin** | Chọn 1 trong 3 phương thức xác định đối tượng nhận tin:<br>• **Phương thức 1: Chọn từ Bảng dữ liệu tùy chọn (`custom_table`)**: Chọn Bảng dữ liệu khách hàng mục tiêu $\rightarrow$ Chọn cột chứa `CONVERSATION_ID` $\rightarrow$ Chọn View hoặc thiết lập thêm bộ lọc điều kiện bằng công cụ **FilterBuilder**.<br>• **Phương thức 2: Theo View hệ thống (`view`)**: Sử dụng trực tiếp các View đã được lưu và khóa trên bảng Hội thoại hệ thống `multichannel_conversations`.<br>• **Phương thức 3: Tự lọc điều kiện / Chọn trực tiếp (`direct`)**: Tự do lọc theo Kênh gửi (Platform), Tài khoản kết nối, Nhân viên phụ trách, Loại hội thoại, Trạng thái (Open, Closed), Thẻ nhãn tag hoặc Trạng thái AI Agent. Có nút **Lưu thành View mới** để tái sử dụng cho các chiến dịch sau.<br>• Bấm nút <img src="https://api.iconify.design/lucide:calculator.svg?color=%23ff3333" width="16" alt="" /> **Ước tính số lượng mục tiêu**: Hệ thống quét nhanh và trả về số lượng cuộc hội thoại thỏa mãn (ví dụ: `Ước tính tìm thấy ~185 đối tượng phù hợp`). |
| **6. Bước 4 — Cài đặt tốc độ gửi & Hành động sau gửi** | • **Cài đặt giãn cách gửi (Chaining Delay)**: Thiết lập khoảng cách ngẫu nhiên giữa 2 tin nhắn gửi liên tiếp: *Độ trễ tối thiểu (Min Delay)* và *Độ trễ tối đa (Max Delay)* tính bằng giây (ví dụ: từ `8 giây` đến `25 giây`) nhằm bảo vệ an toàn cho tài khoản gửi.<br>• **Hành động sau khi gửi (Post Actions)**: Thiết lập các tác vụ tự động kích hoạt sau khi gửi tin thành công gồm:<br>  + *Thêm thẻ tag (`ADD_TAG`)*: Tự động gắn nhãn (ví dụ: `da_gui_cskh_t10`).<br>  + *Gỡ thẻ tag (`REMOVE_TAG`)*: Bỏ nhãn cũ.<br>  + *Cập nhật trạng thái hội thoại (`UPDATE_CONVERSATION_STATUS`)*: Đổi sang `CLOSED` hoặc `PENDING`.<br>  + *Bật/Tắt AI Agent (`TOGGLE_AI_AGENT`)*: Tự động kích hoạt bot trả lời tiếp.<br>  + *Cập nhật trường tùy chỉnh (`UPDATE_FIELD`)*: Điền ngày gửi hoặc trạng thái vào cột Database.<br>  + *Kích hoạt quy trình Workflow tự động (`TRIGGER_WORKFLOW`)*: Đẩy dữ liệu sang quy trình tự động hóa tiếp theo.<br>• Kiểm tra bảng Tổng kết chiến dịch và bấm nút <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" /> **Phát động chiến dịch**. |
| **7. Giám sát thời gian thực** | Bấm vào dòng chiến dịch trên bảng danh sách để mở hộp thoại chi tiết (**OmnichannelCampaignDetailModal**):<br>• **Đồng hồ KPI Realtime**: Tổng mục tiêu, Đã gửi, Thành công, Thất bại và Tỷ lệ thành công (%).<br>• **Thanh tiến độ (Progress Bar)**: Hiển thị tỷ lệ hoàn thành tăng dần đều theo thời gian thực.<br>• **Tab Danh sách người nhận**: Xem trạng thái chi tiết của từng cuộc trò chuyện (Chờ gửi, Đang gửi, Thành công, Thất bại kèm mã lỗi chi tiết).<br>• **Các nút can thiệp khẩn cấp**: Bấm **Tạm dừng**, **Tiếp tục** hoặc **Hủy bỏ chiến dịch** bất kỳ lúc nào. |

---

### Tính năng 6 — Tiện ích 3: Thu Thập Group Zalo Bằng Link (CRAWL_GROUPS)

Tiện ích **Thu Thập Group Zalo Bằng Link (`CRAWL_GROUPS`)** là công cụ tự động hóa mạnh mẽ giúp doanh nghiệp khai thác dữ liệu từ các nhóm cộng đồng Zalo qua liên kết mời tham gia:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở tiện ích Cào nhóm Zalo** | Trong Trung tâm Tiện ích, chọn thẻ <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Thu Thập Group Zalo Bằng Link (CRAWL_GROUPS)**. Giao diện chi tiết mở ra kèm thanh breadcrumb `Tiện ích / Lấy thông tin Group Zalo từ link`. |
| **2. Chọn tài khoản Zalo thực thi** | Tại ô chọn tài khoản, nhấp chọn một tài khoản **Zalo Personal** đang ở trạng thái Hoạt động (`CONNECTED` / `ACTIVE`). Ô chọn hiển thị rõ ảnh đại diện, tên Zalo và số điện thoại liên kết. |
| **3. Nhập danh sách liên kết nhóm Zalo** | Dán các đường link nhóm vào ô soạn thảo văn bản nhiều dòng (**Textarea**):<br>• Định dạng: Mỗi dòng một đường dẫn hợp lệ dạng `https://zalo.me/g/...`<br>• **Phân tích thời gian thực**: Bên dưới khung nhập, hệ thống tự động kiểm tra cú pháp và hiển thị thống kê: *Số liên kết hợp lệ* (màu xanh lá) và *Số liên kết không hợp lệ* (màu đỏ cảnh báo nếu có đường link sai cú pháp). |
| **4. Bật công tắc Tự động tham gia nhóm (Auto Join)** | Bật/tắt công tắc **Tự động tham gia nhóm nếu chưa vào nhóm (Auto Join)**:<br>• Khi **BẬT**: Nếu tài khoản Zalo của bạn chưa là thành viên, hệ thống sẽ gửi yêu cầu gia nhập nhóm tự động trước khi trích xuất dữ liệu.<br>• Khi **TẮT**: Hệ thống chỉ thu thập dữ liệu với các nhóm mà tài khoản của bạn đã tham gia từ trước. |
| **5. Cấu hình Lưu dữ liệu vào Bảng dữ liệu động (Target Dynamic Table)** | Bật công tắc **Lưu dữ liệu vào Database** $\rightarrow$ Chọn bảng dữ liệu đích từ danh sách Bảng dữ liệu động trong không gian làm việc. Hệ thống nạp toàn bộ cấu trúc cột của bảng đã chọn. |
| **6. Ánh xạ 15 trường dữ liệu nguồn (15 Field Mappings)** | Hệ thống hỗ trợ ánh xạ tối đa 15 trường dữ liệu chi tiết chia thành 2 nhóm thực thể:<br><br>**Nhóm 1 — Thông tin Thành viên Nhóm (Member Info)**:<br>1. *Tên thành viên (`member_name`)*: Tên hiển thị của thành viên.<br>2. *ID Zalo thành viên (`member_id` / `member_uid`)*: UID định danh Zalo của thành viên.<br>3. *Mã hội thoại (`conversation_id`)*: ID cuộc trò chuyện tương ứng với thành viên.<br>4. *Ảnh đại diện TV (`member_avatar`)*: Đường dẫn URL ảnh đại diện của thành viên.<br>5. *Vai trò trong nhóm (`role`)*: Trưởng nhóm, Phó nhóm hoặc Thành viên.<br><br>**Nhóm 2 — Thông tin Nhóm cha (Group Info)**:<br>6. *Tên nhóm Zalo (`title` / `group_title`)*: Tên hiển thị của nhóm.<br>7. *Link nhóm (`group_url`)*: URL tham gia nhóm Zalo.<br>8. *ID nhóm Zalo (`group_id`)*: Mã định danh nhóm từ máy chủ Zalo.<br>9. *Số lượng thành viên (`member_count`)*: Tổng số thành viên trong nhóm.<br>10. *Số TV đã đồng bộ (`synced_member_count`)*: Số lượng thành viên nhóm đã đồng bộ danh bạ.<br>11. *Ảnh đại diện nhóm (`avatar` / `group_avatar`)*: URL ảnh đại diện nhóm.<br>12. *Mô tả nhóm (`description`)*: Nội dung thông tin giới thiệu nhóm.<br>13. *ID người tạo (`creator_id`)*: UID của người lập nhóm Zalo.<br>14. *Trạng thái thu thập (`crawl_status`)*: Đã cào / Chờ cào / Thất bại.<br>15. *Thời gian thu thập (`crawled_at`)*: Thời điểm hoàn tất trích xuất.<br><br>• Bấm nút **Tự động ánh xạ (Auto Mapping)**: Hệ thống tự động so khớp tên cột tương đồng giữa bảng nguồn và bảng đích.<br>• Bấm nút **+ Thêm trường** để cấu hình thủ công từng trường mong muốn. |
| **7. Cấu hình Gắn Tag tự động** | • **Gắn Tag hội thoại nhóm**: Tìm kiếm hoặc tạo mới thẻ nhãn để gắn vào cuộc trò chuyện của nhóm trên OmniAI Chat (ví dụ: `group_zalo_cong_dong`).<br>• **Gắn Tag thành viên nhóm**: Tìm kiếm hoặc tạo mới thẻ nhãn để gắn tự động cho toàn bộ thành viên được cào về (ví dụ: `lead_tu_nhom_bds`). |
| **8. Thực thi và Theo dõi Lịch sử chạy ngầm** | • Nhìn xuống thanh chân trang (Footer), nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Bắt đầu thu thập ({count} nhóm)** sáng màu xanh. Bấm vào để kích hoạt tác vụ chạy ngầm.<br>• Bấm vào biểu tượng đồng hồ <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **Xem lịch sử chạy ngầm** ở góc trái chân trang để mở hộp thoại **AllSysJobsHistoryModal**: Theo dõi tiến độ từng job cào nhóm, số dòng thành viên đã ghi vào Database và lý do lỗi nếu có nhóm bị chặn link. |

---

### Tính năng 7 — Tiện ích 4: Đồng bộ Nhãn Zalo cá nhân vào Tag (SYNC_LABELS)

Tiện ích **Đồng bộ Nhãn Zalo cá nhân vào Tag (`SYNC_LABELS`)** giúp chuyển đổi toàn bộ cấu trúc nhãn phân loại khách hàng trên ứng dụng Zalo cá nhân của bạn thành thẻ Tag chính thức trên RedAI:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở tiện ích Đồng bộ Nhãn** | Trong Trung tâm Tiện ích, chọn thẻ <img src="https://api.iconify.design/lucide:tag.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ Nhãn Zalo cá nhân vào Tag (SYNC_LABELS)**. |
| **2. Xem danh sách tài khoản Zalo cá nhân** | Màn hình tải danh sách toàn bộ các tài khoản Zalo Personal đang kết nối trong Không gian làm việc. Mỗi dòng tài khoản hiển thị: Ô checkbox lựa chọn, Ảnh đại diện, Tên tài khoản Zalo, Số điện thoại và trạng thái Hoạt động. |
| **3. Thao tác chọn tài khoản** | • Sử dụng 2 nút thao tác nhanh trên đầu danh sách: Bấm **Chọn tất cả** để tích chọn toàn bộ tài khoản, hoặc bấm **Bỏ chọn tất cả** để xóa trắng lựa chọn.<br>• Hoặc tích chọn thủ công vào ô checkbox của từng tài khoản mong muốn. |
| **4. Xem thống kê nhãn hiện có** | Khung thống kê bên phải hiển thị số lượng thẻ Tag hội thoại hiện có trên hệ thống RedAI để bạn nắm được quy mô danh mục trước khi đồng bộ. |
| **5. Kích hoạt đồng bộ hàng loạt** | Nhìn xuống thanh chân trang (Footer), nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ nhãn ({count} tài khoản)** sẽ hiển thị chính xác số tài khoản bạn đã chọn:<br>• Bấm nút để khởi tạo tác vụ đồng bộ nền qua hệ thống hàng đợi **Rai Job Queue**.<br>• Hệ thống hiển thị thanh thông báo tiến trình nổi (**Notification Marquee**) cập nhật trạng thái quét nhãn.<br>• Khi hoàn tất, các nhãn màu trên Zalo sẽ tự động xuất hiện trong danh mục Tag hệ thống và gắn tương ứng vào từng khách hàng. |
| **6. Xem lại lịch sử tác vụ** | Bấm nút biểu tượng <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **Xem lịch sử chạy ngầm** ở chân trang để mở hộp thoại lịch sử tác vụ hệ thống (**AllSysJobsHistoryModal**). |

---

### Tính năng 8 — Tiện ích 5: Đồng bộ Tên hiển thị Zalo (SYNC_DISPLAY_NAMES)

Tiện ích **Đồng bộ Tên hiển thị Zalo (`SYNC_DISPLAY_NAMES`)** giúp chuẩn hóa danh bạ khách hàng bằng cách lấy tên gợi nhớ (biệt danh / alias) mà nhân viên bán hàng đã lưu trên điện thoại Zalo cá nhân đưa vào hệ thống:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở tiện ích Đồng bộ Tên hiển thị** | Trong Trung tâm Tiện ích, chọn thẻ <img src="https://api.iconify.design/lucide:contact-round.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ Tên hiển thị Zalo (SYNC_DISPLAY_NAMES)**. |
| **2. Chọn tài khoản Zalo cá nhân** | Danh sách tài khoản Zalo Personal kết nối trong workspace sẽ hiển thị. Tương tự như tiện ích nhãn, bạn có thể bấm **Chọn tất cả**, **Bỏ chọn tất cả** hoặc tích chọn từng tài khoản cụ thể. |
| **3. Khởi tạo tác vụ đồng bộ** | Nhìn xuống thanh chân trang (Footer), nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Bắt đầu đồng bộ ({count} tài khoản)** sáng màu chàm nổi bật:<br>• Bấm nút để hệ thống kích hoạt tiến trình quét danh bạ ngầm qua **Rai Job Queue**.<br>• Hệ thống sẽ duyệt qua danh bạ của tài khoản Zalo cá nhân, tìm các liên hệ có đặt tên gợi nhớ (ví dụ: `Anh Nam - Đất Nền Củ Chi`, `Chị Lan - Giám Đốc Thẩm Mỹ`) và tự động cập nhật đè lên tiêu đề cuộc trò chuyện trên OmniAI Chat.<br>• Quá trình chạy hoàn toàn dưới nền, nhân viên vẫn có thể tiếp tục nhắn tin bình thường mà không bị gián đoạn. |
| **4. Kiểm tra lịch sử tác vụ** | Bấm nút <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **Xem lịch sử chạy ngầm** ở chân trang để kiểm tra trạng thái hoàn thành và số lượng liên hệ được cập nhật tên thành công. |

---

## Kiểm tra kết quả

Sau khi thực hiện các thiết lập quản trị, tiếp thị và tiện ích trên, bạn có thể kiểm chứng kết quả trực quan trên giao diện:

1. **Trên thẻ nhãn hội thoại**: Khi gán nhãn thành công, nhãn hiển thị ngay lập tức trên thanh thông tin bên phải và hiển thị biểu tượng màu tương ứng trên dòng hội thoại ở sidebar bên trái.
2. **Trên bảng phân công**: Avatar và tên nhân viên phụ trách xuất hiện chuẩn xác dưới dòng hội thoại của danh sách chat, công tắc AI Chat chuyển sang màu xanh nếu bật tự động trả lời.
3. **Trên thanh công cụ nhanh**: 2 tiện ích được ghim xuất hiện ngay trên header của Chat Sidebar và có thể bấm mở tức thì.
4. **Trên chiến dịch gửi tin**: Mở hộp thoại chi tiết chiến dịch, thanh tiến độ % tăng dần đều theo thời gian thực tương ứng với khoảng cách delay đã cài đặt, các tin nhắn gửi thành công hiển thị màu xanh `SUCCESS`.
5. **Trên bảng dữ liệu cào nhóm**: Mở màn hình Database của Bảng dữ liệu động đã ánh xạ, các dòng dữ liệu thành viên nhóm Zalo được điền đầy đủ thông tin: Tên, UID, Vai trò, Tên nhóm, Link nhóm và Avatar.
6. **Trên danh bạ hội thoại Zalo**: Tên khách hàng tự động chuyển từ tên mặc định sang tên gợi nhớ Zalo cá nhân, các nhãn màu Zalo xuất hiện đầy đủ trong bộ lọc Tag của thanh tìm kiếm.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động thực hiện các thao tác quản trị thẻ nhãn, phân công nhân viên, tạo mẫu tin, phát động chiến dịch và kích hoạt các tiện ích mở rộng Zalo, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - OmniAI Chat` |
| **Mã định danh Kỹ năng (Skill ID)** | `d274fc72-b5d7-4aff-bf25-7eb20fba0eea` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - OmniAI Chat` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71230a76-f1ab-4bdf-8e56-9fe1d8b6fd1a` |
| **Quyền tài khoản yêu cầu** | Workspace Member, Operator, Admin hoặc Workspace Owner |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

Dưới đây là bảng ánh xạ chi tiết các công cụ của AI Agent và câu lệnh thực thi cụ thể cho trọn bộ 8 tính năng quản trị, tiếp thị và tiện ích:

| Nhóm tính năng | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tính năng 1: Quản trị thẻ nhãn (Tags)** | `getTags`<br>`createConversationTag`<br>`addTagsToConversation`<br>`removeTagsFromConversation`<br>`bulkMutateConversationTags` | `Hãy kiểm tra danh sách nhãn hiện có, tạo một nhãn mới tên "Khách Hàng Thân Thiết" màu xanh lá (#10B981) và gắn nhãn này vào cuộc trò chuyện "conv_zalo_102".` |
| **Tính năng 2: Phân công nhân sự & Tự động trả lời** | `getBaseAssignableUsers`<br>`getConversationWorkspaceUsers`<br>`addConversationWorkspaceUsers`<br>`removeConversationWorkspaceUsers`<br>`updateAutoReply` | `Hãy phân công nhân viên có ID "usr_cskh_09" phụ trách cuộc trò chuyện "conv_fb_8821" và bật chế độ tự động trả lời bằng AI Chat (autoReply: true) cho hội thoại này.` |
| **Tính năng 3: Ghim tiện ích lên thanh công cụ** | `pinMultichannelUtility`<br>`unpinMultichannelUtility`<br>`getPinnedMultichannelUtilities` | `Hãy kiểm tra danh sách các tiện ích đang được ghim lên thanh công cụ và ghim 2 tiện ích "TEMPLATES" và "CAMPAIGNS" ra thanh công cụ Chat Sidebar giúp tôi.` |
| **Tính năng 4: Tiện ích Mẫu tin nhắn (Templates)** | `getOmnichannelTemplates`<br>`createOmnichannelTemplate`<br>`getOmnichannelTemplateDetail`<br>`updateOmnichannelTemplate`<br>`previewOmnichannelTemplate` | `Hãy tạo một mẫu tin nhắn mới có tên "Thông Báo Lịch Hẹn" với nội dung: "Xin chào {{customer_name}}, lịch hẹn tư vấn của bạn được xếp vào lúc {{appointment_time}} nhé!" và kiểm tra xem trước hiển thị.` |
| **Tính năng 5: Tiện ích Chiến dịch gửi tin (Campaigns)** | `estimateOmnichannelCampaign`<br>`createOmnichannelCampaign`<br>`getOmnichannelCampaigns`<br>`getOmnichannelCampaignDetail`<br>`updateOmnichannelCampaignStatus` | `Hãy ước tính số lượng đối tượng có nhãn "vip_customer" trên kênh Zalo OA, sau đó phát động một chiến dịch gửi tin nhắn áp dụng mẫu tin "KM_THANG_10" với khoảng cách giãn cách delay từ 8 đến 20 giây.` |
| **Tính năng 6: Tiện ích Thu thập Group Zalo (Crawl Groups)** | `crawlZaloGroupsByLink`<br>`getZaloCrawlGroupJobs`<br>`getZaloCrawlGroupJobDetail` | `Hãy dùng tài khoản Zalo cá nhân "acc_zalo_lead" cào thông tin và thành viên từ link nhóm "https://zalo.me/g/abc123xyz", bật tự động tham gia nhóm (shouldJoinGroup: true), lưu dữ liệu thành viên vào bảng "Danh Sách Khách Hàng BĐS" và gắn tag "lead_zalo_group".` |
| **Tính năng 7: Tiện ích Đồng bộ Nhãn Zalo (Sync Labels)** | `syncZaloPersonalLabelsToTags`<br>`getSyncZaloLabelsJobs` | `Hãy kích hoạt tác vụ đồng bộ nhãn từ tài khoản Zalo cá nhân "acc_zalo_lead" thành danh mục thẻ tag trên hệ thống và báo cáo số lượng nhãn đã quét thành công.` |
| **Tính năng 8: Tiện ích Đồng bộ Tên hiển thị (Sync Display Names)** | `syncZaloPersonalDisplayNames`<br>`getSyncDisplayNamesJobs` | `Hãy kích hoạt tác vụ quét và đồng bộ tên gợi nhớ từ danh bạ tài khoản Zalo cá nhân "acc_zalo_sales_01" vào tên khách hàng trên toàn bộ các cuộc trò chuyện của tài khoản này.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Gắn thẻ nhãn mới vào cuộc trò chuyện trên giao diện | Gọi `getCompactConversations` thấy mảng `tags` của hội thoại chứa nhãn vừa gắn. |
| Phân công nhân viên phụ trách tại thanh thông tin bên phải | Gọi `getConversationWorkspaceUsers` thấy danh sách nhân sự trả về đúng ID nhân viên. |
| Bấm Phát động chiến dịch gửi tin nhắn từ giao diện | Gọi `getOmnichannelCampaigns` thấy chiến dịch mới ở trạng thái `RUNNING` kèm tiến độ gửi. |
| Bấm Tạm dừng chiến dịch trên giao diện | Gọi `getOmnichannelCampaignDetail` thấy thuộc tính `status: PAUSED`. |
| Bấm Bắt đầu thu thập nhóm Zalo trên giao diện | Gọi `getZaloCrawlGroupJobs` thấy job cào nhóm mới với trạng thái `PENDING` hoặc `PROCESSING`. |
| Bấm Đồng bộ nhãn Zalo cá nhân trên giao diện | Gọi `getTags` thấy danh sách tag hệ thống xuất hiện các thẻ nhãn mới được trích xuất từ Zalo. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `addTagsToConversation` | Thẻ nhãn mới lập tức xuất hiện trên bong bóng nhãn của hội thoại trên giao diện chat. |
| Agent gọi `updateAutoReply` thành true | Công tắc AI Chat trên thanh thông tin bên phải tự động gạt sang trạng thái bật màu xanh. |
| Agent gọi `createOmnichannelCampaign` | Mở danh sách Chiến dịch trong Trung tâm Tiện ích, thấy thẻ chiến dịch mới xuất hiện và đang chạy tiến độ. |
| Agent gọi `crawlZaloGroupsByLink` | Mở Bảng dữ liệu động mục tiêu, các dòng dữ liệu thành viên mới cào từ nhóm Zalo xuất hiện kèm avatar và vai trò. |
| Agent gọi `syncZaloPersonalDisplayNames` | Danh sách chat bên trái tự động hiển thị tên khách hàng theo đúng tên gợi nhớ trong danh bạ Zalo cá nhân. |
