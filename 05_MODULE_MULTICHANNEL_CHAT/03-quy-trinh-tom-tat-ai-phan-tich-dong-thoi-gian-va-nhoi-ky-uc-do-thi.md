## Mở các công cụ Trí tuệ Nhân tạo Phân tích Hội thoại và Ký ức Khách hàng

Trong hệ sinh thái **OmniAI Chat (Multichannel Chat)**, khả năng ứng dụng Trí tuệ Nhân tạo (AI) không chỉ dừng lại ở việc tự động phản hồi tin nhắn mà còn đóng vai trò là một trợ lý phân tích tâm lý, tóm lược nhu cầu và lưu trữ tri thức khách hàng chuyên sâu. Tính năng này giúp nhân viên tư vấn nắm bắt trọn vẹn bối cảnh cuộc trò chuyện chỉ trong 5 giây, hiểu rõ nguyên nhân khách hàng dừng tương tác và tự động nhồi ký ức vào Đồ thị Tri thức (Graph RAG).

Để kích hoạt các công cụ phân tích AI, bạn thao tác từ 2 vị trí trên màn hình trò chuyện:

1. **Thanh Menu Icon Tiện ích (MenuIconBar)**: Nằm ở góc trên cùng của thanh bên thông tin bên phải (`ConversationInfoSidebar`), bao gồm các nút chức năng:
   - <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Tóm tắt hội thoại AI**: Mở hộp thoại tóm lược ý định khách hàng, chủ đề quan tâm và sản phẩm.
   - <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **Ký ức khách hàng (Audience Memory)**: Mở hộp thoại trực quan hóa mạng lưới đồ thị tri thức của khách hàng.
   - <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> **Dòng thời gian & Hành vi tương tác**: Mở hộp thoại phân tích phiên trao đổi, tâm lý và cảnh báo khoảng lặng.
2. **Nút Lịch sử trên Chat Header**: Nhấp trực tiếp vào biểu tượng đồng hồ <img src="https://api.iconify.design/lucide:history.svg?color=%23ff3333" width="16" alt="" /> trên thanh tiêu đề cuộc trò chuyện để mở nhanh phân tích Dòng thời gian.

---

## Các bước thực hiện

### Giai đoạn 1 — Tóm tắt hội thoại bằng AI và Quản lý Lịch sử tóm tắt

Khi một cuộc hội thoại đã kéo dài hàng chục tin nhắn hoặc nhân viên mới tiếp nhận bàn giao ca, tính năng Tóm tắt AI giúp cô đọng toàn bộ thông tin quan trọng:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Kích hoạt Tóm tắt AI** | Nhấp vào biểu tượng <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Tạo tóm tắt AI)** trên thanh công cụ tiện ích. Hộp thoại **Tóm tắt hội thoại bởi AI (ConversationSummaryModal)** xuất hiện. |
| **2. Khai thác dữ liệu phân tích** | Bảng tóm tắt hiển thị trực quan các nhóm chỉ số cốt lõi:<br>• **Ý định khách hàng (Customer Intent)**: Xác định rõ mục tiêu chính của khách (ví dụ: `Hỏi giá dịch vụ`, `Cần tư vấn gói Enterprise`, `Khiếu nại giao chậm`).<br>• **Chủ đề quan tâm (Interest Topics)**: Các từ khóa nổi bật được trích xuất.<br>• **Sản phẩm quan tâm (Products)**: Danh sách mặt hàng hoặc gói dịch vụ khách hàng đang cân nhắc.<br>• **Độ tin cậy (Confidence)**: Tỷ lệ phần trăm đánh giá mức độ chính xác của phân tích AI.<br>• **Tổng quan cuộc hội thoại (Overview)**: Đoạn văn bản ngắn gọn tóm tắt diễn biến trao đổi.<br>• **Ghi chú nội bộ (Internal Summary)**: Ghi chú hữu ích dành riêng cho nhân viên chăm sóc tiếp theo.<br>• **Thống kê hội thoại**: Tổng số lượng tin nhắn đã phân tích, tỷ lệ tin nhắn đến từ khách (Inbound) so với phản hồi từ tư vấn viên (Outbound) và khung thời gian trao đổi. |
| **3. Xem Lịch sử các bản tóm tắt cũ** | Nhấp vào mục **Lịch sử tóm tắt (Summary History)** trong hộp thoại:<br>• Hệ thống lưu trữ toàn bộ các phiên bản tóm tắt qua từng thời kỳ.<br>• Nhãn màu xanh **Mới nhất** hiển thị bản cập nhật hiện tại.<br>• Nhấp vào các dòng **Bản cũ** để đối chiếu sự thay đổi trong nhu cầu của khách hàng qua từng mốc thời gian kèm cảnh báo màu vàng (*"Đang xem bản tóm tắt cũ ngày..."*).<br>• Bấm nút **Xem bản mới nhất** để quay lại dữ liệu hiện thời. |
| **4. Tạo tóm tắt lại (Regenerate)** | Khi có thêm các diễn biến mới trong cuộc trò chuyện, bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Tạo tóm tắt lại**. AI sẽ quét toàn bộ các tin nhắn mới phát sinh và cập nhật bản tóm tắt mới nhất. |

---

### Giai đoạn 2 — Nhồi Ký ức Khách hàng vào Đồ thị Tri thức (Graph RAG Memory)

Tính năng độc quyền giúp AI Agent và hệ thống ghi nhớ vĩnh viễn thói quen, sở thích và thông tin doanh nghiệp của khách hàng vào mạng lưới Đồ thị Tri thức:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở cửa sổ Ký ức Khách hàng** | Bấm biểu tượng não bộ <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> trên thanh tiện ích bên phải (hoặc bấm nút **Nhồi ký ức đồ thị** bên trong hộp thoại Tóm tắt AI). |
| **2. Bắt đầu tiến trình nhồi ký ức** | Bấm nút <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ vào Đồ thị Ký ức**. Hệ thống sẽ tự động chuyển đổi bản tóm tắt thành dạng cấu trúc YAML chuẩn hóa. |
| **3. Theo dõi tiến trình xử lý Graph Job** | Khung hiển thị tiến trình thời gian thực (**UnifiedGraphJobProgress**) xuất hiện:<br>• Bước 1: Trích xuất các thực thể (Entities: Tên khách hàng, Công ty, Chức vụ, Sở thích, Ngân sách...).<br>• Bước 2: Nhận diện các mối quan hệ (Relations: Làm việc tại, Quan tâm sản phẩm, Người ra quyết định...).<br>• Bước 3: Đưa vào mô hình nhúng Vector và đồng bộ vào cơ sở dữ liệu Đồ thị Tri thức (Graph RAG). |
| **4. Trực quan hóa mạng lưới tri thức** | Hộp thoại hiển thị sơ đồ mạng lưới đồ thị tương tác 2D: Các vòng tròn Node đại diện cho thông tin khách hàng liên kết với các Node sản phẩm và hành vi, cho phép AI Agent truy xuất siêu tốc trong các phiên chat tương lai. |

---

### Giai đoạn 3 — Phân tích Dòng thời gian, Tâm lý và Cảnh báo khoảng lặng

Hộp thoại **Dòng thời gian & Hành vi tương tác (ConversationTimelineModal)** là công cụ đắc lực hỗ trợ nhân viên giải quyết bài toán khách hàng "im lặng không trả lời":

| Khối chức năng | Cách thức vận hành trên Giao diện UI |
| :--- | :--- |
| **Hai chế độ phân tích linh hoạt** | Góc trên bên phải hộp thoại có công tắc gạt:<br>• **Chế độ Thuật toán (< 10ms, miễn phí)**: Gom cụm các phiên trao đổi thực tế (Sessionization) dựa trên độ ngắt quãng thời gian, tính toán chính xác tổng thời lượng trao đổi, số phiên tương tác và tỷ lệ tin nhắn.<br>• **Bật chế độ AI (Phân tích ngữ nghĩa & tâm lý)**: Bật công tắc gạt để AI đọc sâu nội dung từng phiên trao đổi, tự động gắn nhãn tâm lý cảm xúc và nhận diện các giai đoạn trò chuyện. |
| **Bảng đồng hồ chỉ số tương tác** | Hiển thị 5 thẻ số liệu tổng quan:<br>• **Vòng đời trao đổi**: Tổng số giờ từ tin nhắn đầu tiên đến nay.<br>• **Phiên tương tác**: Số lượng phiên trao đổi riêng biệt.<br>• **Tin nhắn đã phân tích**: Tổng số tin (phân tách rõ số lượng tin từ khách vs tư vấn viên).<br>• **Tâm lý khách hàng**: Nhãn tâm lý trực quan (Tích cực, Tiêu cực, Do dự/Cân nhắc, Khẩn cấp, Trung tính).<br>• **Khoảng lặng im lặng**: Đếm thời gian im lặng kể từ tin nhắn cuối cùng (ví dụ: `Im lặng 4 giờ 30 phút`). |
| **Cảnh báo khoảng lặng (Inactivity Alert)** | Khi cuộc hội thoại bị gián đoạn, khối cảnh báo màu vàng nổi bật phân tích:<br>• **Bên đang phải chờ phản hồi**: Nhận diện rõ ràng là **Chờ khách phản hồi** hay **Chờ CSKH trả lời**.<br>• **Ước lượng nguyên nhân dừng nhắn**: AI phán đoán lý do (ví dụ: `Khách hàng đang phân vân so sánh giá với đối thủ`, `Khách bận họp sau khi xem bảng báo giá`).<br>• **Gợi ý chăm sóc lại (Re-engagement Advice)**: Đề xuất một mẫu tin nhắn mở lời tinh tế, khéo léo để nhân viên gửi lại kéo khách về. Bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Sao chép** để dán ngay vào khung chat mà không cần nghĩ lời. |
| **Cây tiến trình phiên trao đổi** | Danh sách phân rã các mốc thời gian trao đổi theo 8 giai đoạn nghiệp vụ: *Chào hỏi ban đầu*, *Hỏi thăm thông tin*, *Tư vấn chi tiết*, *Thương lượng giá / Ưu đãi*, *Khiếu nại / Phản ánh*, *Chốt đơn / Thỏa thuận*, *Hỗ trợ kỹ thuật*, *Ngừng tương tác*. |
| **Đề xuất hành động tiếp theo từ AI** | Dưới chân trang hiển thị danh sách các đề xuất hành động được phân cấp rõ ràng theo 3 mức độ: **Ưu tiên cao** (màu đỏ), **Ưu tiên vừa** (màu vàng) và **Ưu tiên thấp** (màu xanh), chỉ rõ người xử lý và nút sao chép hành động. |

---

## Kiểm tra kết quả

Sau khi thực hiện phân tích hội thoại bằng AI, bạn kiểm tra lại:

1. **Bản tóm tắt hoàn chỉnh**: Các trường ý định, chủ đề, sản phẩm và tổng quan hiển thị đầy đủ, phản ánh chuẩn xác 100% nội dung khách hàng đã trao đổi trong tin nhắn.
2. **Ký ức đồ thị cập nhật**: Khi nhồi ký ức thành công, thanh tiến trình Graph Job đạt 100% màu xanh, sơ đồ mạng lưới xuất hiện thêm các Node thông tin mới của khách hàng.
3. **Cảnh báo khoảng lặng chính xác**: Nếu khách hàng chưa trả lời sau khi nhân viên gửi báo giá, thẻ cảnh báo nhận diện đúng trạng thái "Chờ khách phản hồi" kèm câu gợi mở chăm sóc lại phù hợp ngữ cảnh.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động tạo tóm tắt hội thoại, đọc bối cảnh khách hàng, nhồi ký ức đồ thị và kiểm tra lịch sử trao đổi, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - OmniAI Chat` |
| **Mã định danh Kỹ năng (Skill ID)** | `d274fc72-b5d7-4aff-bf25-7eb20fba0eea` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - OmniAI Chat` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71230a76-f1ab-4bdf-8e56-9fe1d8b6fd1a` |
| **Quyền tài khoản yêu cầu** | Workspace Member, Agent, Operator, Admin hoặc Owner |

---

### Bảng ánh xạ giao diện người dùng sang công cụ AI Agent

| Tác vụ trên Giao diện | Tên Tool tương ứng | Ý nghĩa & Tham số chính |
| :--- | :--- | :--- |
| Xem bản tóm tắt hội thoại mới nhất | `getLatestConversationSummary` | Đọc tóm tắt nhanh nhất để lấy bối cảnh trước khi trả lời tin nhắn (`conversationId`). |
| Lưu hoặc cập nhật nội dung tóm tắt hội thoại | `createOrUpdateConversationSummary` | Tạo hoặc ghi đè nội dung tóm tắt khách hàng (`conversationId`, `summaryData`). |
| Kích hoạt tác vụ tạo tóm tắt AI bất đồng bộ | `generateConversationSummaryAsync` | Đưa yêu cầu phân tích tóm tắt vào hàng đợi BullMQ (`conversationId`). |
| Kiểm tra trạng thái tiến trình tạo tóm tắt ngầm | `getConversationSummaryJobStatus` | Kiểm tra tiến độ hoàn thành của tác vụ tóm tắt ngầm qua mã (`sysJobId`). |
| Xem lịch sử các phiên bản tóm tắt cũ | `getConversationSummaryHistory` | Tra cứu danh sách các bản tóm tắt theo thời gian (`conversationId`). |
| Nhồi tóm tắt vào Đồ thị Ký ức (Graph RAG) | `consolidateConversationMemory` | Đẩy nội dung tóm tắt và insight vào Graph RAG Memory (`id`, `content`: tối thiểu 10 ký tự). |
| Tạo và cập nhật tóm tắt hàng loạt cho nhiều hội thoại | `generateBulkConversationSummaries`<br>`bulkUpsertConversationSummaries` | Tác vụ xử lý tóm tắt theo lô cho các chiến dịch CSKH lớn (`conversationIds`). |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động đọc hiểu bối cảnh cuộc trò chuyện, cập nhật tóm tắt và nhồi thông tin vào Đồ thị Ký ức:

```text
[MỤC TIÊU]
Đọc toàn bộ lịch sử trao đổi của cuộc hội thoại `conv_fb_4412`, tạo bản tóm tắt phân tích ý định khách hàng và đồng bộ tri thức này vào Đồ thị Ký ức (Graph RAG Memory).

[DỮ LIỆU ĐẦU VÀO]
- Mã cuộc trò chuyện: `conv_fb_4412`
- Yêu cầu trích xuất: Ý định chính, sản phẩm quan tâm, ngân sách dự kiến và ghi chú nội bộ.

[QUY TRÌNH THỰC THI]
1. Gọi tool `getCompactMessages` để đọc 30 tin nhắn gần nhất trong cuộc trò chuyện.
2. Phân tích nội dung và cấu trúc thành bản tóm tắt chuẩn gồm: `customerIntent`, `interestTopics`, `products`, `overview` và `internalSummary`.
3. Gọi tool `createOrUpdateConversationSummary` để lưu trữ bản tóm tắt chính thức vào cuộc trò chuyện.
4. Gọi tool `consolidateConversationMemory` với tham số `id: "conv_fb_4412"` và `content` là nội dung tóm tắt chi tiết để nhồi vào mạng lưới tri thức khách hàng.

[TIÊU CHÍ HOÀN THÀNH]
- Bản tóm tắt mới xuất hiện đầy đủ trong hộp thoại Tóm tắt AI trên giao diện.
- Tác vụ Graph RAG được khởi tạo thành công và trả về mã xác nhận tiến trình.
- Báo cáo tóm lược kết quả ngắn gọn cho người quản trị.
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm Tạo tóm tắt AI trên giao diện | Gọi `getLatestConversationSummary` thấy dữ liệu tóm tắt mới với đúng các trường intent và topics. |
| Bấm Nhồi ký ức vào Đồ thị Tri thức | Gọi `consolidateConversationMemory` thấy trạng thái hàng đợi đồ thị đã tiếp nhận ID hội thoại. |
| Bấm chuyển xem các phiên bản tóm tắt cũ | Gọi `getConversationSummaryHistory` thấy danh sách các bản ghi lịch sử trùng khớp với danh sách trên UI. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createOrUpdateConversationSummary` | Mở hộp thoại Tóm tắt AI trên giao diện, các ô ý định, sản phẩm và tổng quan lập tức hiển thị nội dung mới. |
| Agent gọi `consolidateConversationMemory` | Khung tiến trình Graph Job hiển thị thông báo đã đồng bộ thành công và sơ đồ đồ thị khách hàng được làm mới. |
