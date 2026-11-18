## Mở khu vực Trò chuyện Trực tiếp và Khung Soạn thảo Đa phương tiện

Trong **OmniAI Chat (Multichannel Chat)**, Khu vực Trò chuyện Trực tiếp (Chat Area) là không gian tương tác trung tâm nơi nhân viên tư vấn và khách hàng trao đổi tin nhắn thời gian thực. Hệ thống tích hợp đầy đủ các công cụ tương tác đa phương tiện hiện đại (văn bản, giọng nói, hình ảnh, video, tài liệu, nhãn dán sticker và trích dẫn) cùng cơ chế tự động kiểm soát chính sách gửi tin an toàn theo từng nền tảng kết nối.

Để bắt đầu tương tác, bạn nhấp vào bất kỳ cuộc trò chuyện nào trên danh sách hội thoại bên trái (`/multi-channel-chat/:conversationId`). Màn hình trung tâm sẽ mở ra với 3 thành phần chính:

1. **Thanh tiêu đề cuộc trò chuyện (Chat Header)**: Hiển thị tên định danh khách hàng, ảnh đại diện, trạng thái trực tuyến, kênh kết nối và các nút công cụ mở rộng.
2. **Khung hiển thị dòng tin nhắn (Message List)**: Danh sách tin nhắn trao đổi 2 chiều được bố trí trực quan kèm các hành động thả biểu cảm, trích dẫn trả lời, chuyển tiếp và thu hồi tin nhắn.
3. **Khung soạn thảo tin nhắn hiện đại (Modern Chat Input)**: Trình soạn thảo văn bản phong phú hỗ trợ định dạng, nhắc tên `@mention`, nhập liệu giọng nói và kho nội dung đa phương tiện.

---

## Các bước thực hiện

### Giai đoạn 1 — Quản lý nhận diện khách hàng và Kiểm tra năng lực nền tảng

| Thao tác | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **Đổi tên gợi nhớ cuộc trò chuyện** | **Nhấp đúp chuột (Double-click)** trực tiếp vào tên khách hàng trên thanh tiêu đề:<br>• Ô nhập văn bản sẽ kích hoạt tại chỗ.<br>• Nhập tên mới (ví dụ: `Anh Hoàng - Khách Mua Căn Hộ A12`).<br>• Nhấn phím `Enter` để lưu (hoặc nhấn `Escape` để hủy bỏ). Tên mới sẽ tự động đồng bộ trên toàn bộ hệ thống. |
| **Thay đổi ảnh đại diện khách hàng** | **Nhấp đúp chuột** vào vòng tròn ảnh đại diện (Avatar) của khách hàng:<br>• Cửa sổ chọn tệp của máy tính sẽ mở ra.<br>• Chọn tệp hình ảnh mong muốn (hỗ trợ JPG, PNG, WebP). Hệ thống sẽ tự động tối ưu hóa, nén ảnh chuẩn kích thước `800x800` và cập nhật ảnh đại diện mới ngay lập tức. |
| **Nhận diện thông tin kênh & Luồng email** | Quan sát nhãn thông tin dưới tên khách hàng:<br>• Đối với mạng xã hội (Zalo, Facebook): Hiển thị trạng thái hoạt động trực tuyến <img src="https://api.iconify.design/lucide:circle.svg?color=%23ff3333" width="16" alt="" /> **Trực tuyến** hoặc thời gian hoạt động gần nhất (ví dụ: `Hoạt động 5 phút trước`).<br>• Đối với kênh **Gmail**: Hiển thị thẻ màu đỏ nhận diện kênh Gmail, địa chỉ email người gửi, mã định danh luồng thư (ví dụ: `Thread #18a9...`) và tiêu đề thư (Subject). |
| **Tra cứu năng lực và ràng buộc kỹ thuật** | Bấm nút <img src="https://api.iconify.design/lucide:help-circle.svg?color=%23ff3333" width="16" alt="" /> **(Xem thông số kỹ thuật & năng lực nền tảng)** trên thanh tiêu đề:<br>• Hộp thoại **Thông số & Năng lực Nền tảng (PlatformCapabilityModal)** hiển thị chi tiết các tính năng được hỗ trợ của kênh đang mở: Hỗ trợ chat nhóm, trích dẫn trả lời, thả biểu cảm, chỉ báo đang gõ (Typing), độ dài ký tự tối đa của tin nhắn văn bản, giới hạn dung lượng tải lên và chính sách giãn cách chống spam (Rate limits). |
| **Bật/Tắt chế độ Toàn màn hình** | Bấm nút <img src="https://api.iconify.design/lucide:maximize.svg?color=%23ff3333" width="16" alt="" /> **(Toàn màn hình)** / <img src="https://api.iconify.design/lucide:minimize.svg?color=%23ff3333" width="16" alt="" /> **(Thoát toàn màn hình)** ở góc phải thanh tiêu đề để mở rộng tối đa không gian chat, ẩn bớt các thanh điều hướng xung quanh. |

---

### Giai đoạn 2 — Soạn thảo và gửi nội dung tin nhắn đa phương tiện

Khung soạn thảo phía dưới cùng cung cấp đầy đủ các tiện ích nhập liệu hiện đại:

| Tiện ích gửi tin | Cách sử dụng trên Giao diện UI |
| :--- | :--- |
| **Soạn văn bản & Nhắc tên (@Mention)** | Nhập nội dung vào khung soạn thảo. Trong các nhóm chat đông người, gõ ký tự `@` để mở danh sách thành viên và chọn người cần nhắc tên trực tiếp. |
| **Nhập bằng giọng nói (Voice Input)** | Bấm vào biểu tượng micro <img src="https://api.iconify.design/lucide:mic.svg?color=%23ff3333" width="16" alt="" /> **(Nhập bằng giọng nói)**:<br>• Trình duyệt sẽ lắng nghe giọng nói của bạn và chuyển hóa tức thì thành văn bản tiếng Việt chuẩn xác ngay trong khung soạn thảo.<br>• Bấm lại nút micro để kết thúc thu âm và chỉnh sửa lại văn bản trước khi gửi. |
| **Tải tệp đa phương tiện & Dán ảnh nhanh** | • Bấm biểu tượng kẹp ghim <img src="https://api.iconify.design/lucide:paperclip.svg?color=%23ff3333" width="16" alt="" /> để chọn tệp từ máy tính: Hình ảnh (JPG, PNG, GIF), Video (MP4), Ghi âm (Audio), Tài liệu (PDF, Word, Excel, PowerPoint, ZIP).<br>• **Dán ảnh siêu tốc từ Clipboard**: Chụp màn hình bằng công cụ Snipping Tool hoặc sao chép ảnh bất kỳ, sau đó nhấn tổ hợp phím `Ctrl + V` (hoặc `⌘ + V`) trực tiếp vào khung chat. Ảnh sẽ được tự động tải lên và hiển thị khung xem trước. |
| **Kho nhãn dán cảm xúc (Sticker Picker)** | Bấm biểu tượng mặt cười <img src="https://api.iconify.design/lucide:smile.svg?color=%23ff3333" width="16" alt="" /> **(Chọn sticker)**:<br>• Cửa sổ mở ra bộ sưu tập sticker phong phú được tối ưu riêng cho từng nền tảng (bộ sticker sinh động của Zalo, Telegram, Facebook...).<br>• Nhấp chọn sticker để gửi ngay lập tức. |
| **Trích xuất từ Thư viện Đa kênh (Multichannel Library)** | Bấm biểu tượng thư mục <img src="https://api.iconify.design/lucide:folder.svg?color=%23ff3333" width="16" alt="" /> **(Chọn từ thư viện)**:<br>• Hộp thoại hiển thị kho tài nguyên số dùng chung của doanh nghiệp: Catalogue sản phẩm, bảng giá PDF, ảnh quảng cáo, video hướng dẫn đã được duyệt sẵn.<br>• Tích chọn tài liệu cần gửi và bấm Xác nhận để đính kèm vào tin nhắn mà không mất công tìm kiếm lại trong máy. |
| **Mẫu email soạn sẵn (Khi chat qua Gmail)** | Khi đang trao đổi với khách hàng qua luồng Gmail, góc trên khung soạn thảo xuất hiện nút <img src="https://api.iconify.design/lucide:mail.svg?color=%23ff3333" width="16" alt="" /> **(Chọn mẫu email)** để chèn các mẫu thư chào hỏi, báo giá hoặc xác nhận thanh toán chuẩn hóa. |
| **Gửi tin nhắn** | Nhấn phím `Enter` trên bàn phím (hoặc bấm nút gửi <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" />). Để xuống dòng trong khi soạn thảo, nhấn tổ hợp phím `Shift + Enter`. |

---

### Giai đoạn 3 — Tương tác trực tiếp trên từng tin nhắn

Rê chuột vào bất kỳ bong bóng tin nhắn nào trên khung chat, thanh công cụ hành động sẽ xuất hiện:

| Hành động tương tác | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **Thả biểu cảm (Reactions)** | Rê chuột vào tin nhắn $\rightarrow$ Bấm biểu tượng cảm xúc <img src="https://api.iconify.design/lucide:smile.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn một trong các biểu tượng: Trái tim ❤️, Thích 👍, Cười 😂, Bất ngờ 😮, Buồn 😢, Tức giận 😡. Nhấp vào các biểu cảm đã thả dưới tin nhắn để mở hộp thoại xem danh sách ai đã thả cảm xúc. |
| **Trả lời trích dẫn (Reply)** | Rê chuột vào tin nhắn $\rightarrow$ Bấm biểu tượng mũi tên <img src="https://api.iconify.design/lucide:corner-up-left.svg?color=%23ff3333" width="16" alt="" /> **(Trả lời)**. Thanh xem trước nội dung trích dẫn sẽ gắn ngay phía trên khung soạn thảo. Nhập câu trả lời và bấm gửi, tin nhắn gửi đi sẽ đính kèm trích dẫn gốc rõ ràng. |
| **Chuyển tiếp tin nhắn (Forward)** | Bấm biểu tượng menu <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:share.svg?color=%23ff3333" width="16" alt="" /> **Chuyển tiếp tin nhắn**. Trong hộp thoại chuyển tiếp, tìm kiếm và tích chọn một hoặc nhiều cuộc trò chuyện đích (có thể lọc nhanh theo nhãn tag), sau đó bấm **Chuyển tiếp ngay**. |
| **Thu hồi / Xóa tin nhắn** | Bấm menu <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa / Thu hồi tin nhắn**. Xác nhận trên hộp thoại cảnh báo: Tin nhắn sẽ được thu hồi từ cả hai phía (nếu nền tảng cho phép trong khung thời gian quy định). |
| **Chọn nhiều tin nhắn hàng loạt** | Bấm menu <img src="https://api.iconify.design/lucide:more-horizontal.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn **Chọn nhiều tin nhắn**. Giao diện sẽ hiển thị ô checkbox cạnh mỗi tin nhắn cùng thanh công cụ hành động phía dưới để chuyển tiếp hoặc trích xuất hàng loạt. |

---

### Giai đoạn 4 — Kiểm soát chính sách và năng lực gửi tin an toàn (Messaging Capability Guard)

Để bảo vệ tài khoản doanh nghiệp không bị nền tảng khóa hoặc đánh dấu spam, RedAI tích hợp bộ kiểm soát chính sách gửi tin tự động:

1. **Chính sách 24 giờ của Facebook Messenger**:
   - Nếu khách hàng không tương tác trong vòng **24 giờ**, hệ thống sẽ cảnh báo không cho phép gửi tin tự do. Chỉ những tài khoản có quyền **Human Agent Tag** mới được phép phản hồi tiếp trong khung thời gian 7 ngày.
   - Sau 7 ngày hoàn toàn im lặng, nút gửi tin nhắn trên Facebook sẽ tự động khóa để bảo vệ Fanpage.
2. **Chính sách tương tác của Zalo Official Account (Zalo OA)**:
   - Zalo OA chỉ cho phép phản hồi miễn phí khi khách hàng có tương tác trong vòng **7 ngày** gần nhất. Ngoài khung 7 ngày, hệ thống sẽ nhắc nhở sử dụng hình thức gửi tin thông báo ZNS hoặc mời khách hàng tương tác lại.
3. **Bảo vệ tài khoản Zalo Cá nhân**:
   - Tự động nhận diện trường hợp khách hàng chặn số hoặc tài khoản cá nhân bị mất phiên đăng nhập. Khi phát hiện phiên đăng nhập hết hạn, hệ thống sẽ mở ngay hộp thoại **Quét mã QR đăng nhập lại (ReloginQRCodeModal)** để quản trị viên kết nối lại trong 10 giây mà không làm gián đoạn hội thoại.

---

## Kiểm tra kết quả

Sau khi gửi tin nhắn và thực hiện các tương tác, bạn kiểm tra lại:

1. **Trạng thái gửi tin (Message Status)**: Cạnh mỗi tin nhắn gửi đi có biểu tượng trạng thái rõ ràng: <img src="https://api.iconify.design/lucide:clock.svg?color=%23ff3333" width="14" alt="" /> *Đang gửi*, <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="14" alt="" /> *Đã gửi*, <img src="https://api.iconify.design/lucide:check-check.svg?color=%23ff3333" width="14" alt="" /> *Đã nhận* và đổi màu xanh khi đối phương *Đã đọc*.
2. **Hiển thị đa phương tiện**: Hình ảnh, video và tệp đính kèm hiển thị sắc nét, bấm vào để mở trình xem ảnh toàn màn hình hoặc tải tệp về máy tính mượt mà.
3. **Phản hồi chính sách**: Khi gửi tin vào cuộc trò chuyện quá hạn tương tác, giao diện hiển thị thông báo giải thích lý do cụ thể và hướng dẫn phương án khắc phục an toàn.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động đọc nội dung trao đổi, kiểm tra điều kiện gửi tin, phản hồi tin nhắn văn bản, gửi ảnh và thu hồi tin nhắn khi cần, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

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
| Kiểm tra điều kiện chính sách trước khi gửi tin | `getMessagingCapability` | Kiểm tra cuộc hội thoại có đủ điều kiện gửi tin không (`conversationId`). Trả về cờ `canSend` và lý do nếu bị chặn. |
| Soạn và gửi tin nhắn (Văn bản, Ảnh, File, Sticker) | `sendOutboundMessage` | Gửi tin nhắn phản hồi vào hội thoại (`conversationId`, `content`, `type`, `attachments`, `replyToMessageId`). |
| Đọc danh sách tin nhắn chi tiết của hội thoại | `getCompactMessages` | Đọc các tin nhắn gần nhất dạng compact tiết kiệm token (`conversationId`, `limit`). |
| Bấm Thu hồi / Xóa tin nhắn đã gửi | `recallMessage` | Thu hồi tin nhắn đã gửi nhầm (`conversationId`, `messageId`). |
| Nhấp đúp đổi tên hiển thị cuộc hội thoại | `updateConversationTitle` | Đổi tên khách hàng hoặc tiêu đề nhóm (`id`, `title`). |
| Tra cứu nhãn dán sticker đặc trưng theo kênh | `getPlatformStickers` | Lấy danh sách mã sticker khả dụng (`platform`). |
| Tra cứu tài nguyên số từ Thư viện Đa kênh | `getMultichannelLibrary` | Lấy đường dẫn ảnh, video, catalogue để đính kèm vào tin nhắn (`query`, `type`). |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động đọc tin nhắn của khách hàng, kiểm tra điều kiện an toàn và gửi phản hồi chào mừng kèm tài liệu hướng dẫn:

```text
[MỤC TIÊU]
Đọc tin nhắn mới nhất trong cuộc trò chuyện `conv_zalo_8892`, kiểm tra năng lực gửi tin của kênh, sau đó gửi tin nhắn phản hồi giải đáp thắc mắc và đính kèm đường dẫn tài liệu hướng dẫn sử dụng.

[DỮ LIỆU ĐẦU VÀO]
- Mã cuộc trò chuyện: `conv_zalo_8892`
- Nội dung phản hồi: "Chào bạn, cảm ơn bạn đã quan tâm đến giải pháp RedAI. Mình gửi bạn tài liệu hướng dẫn chi tiết đính kèm dưới đây nhé!"
- Tệp đính kèm: Đường dẫn file PDF tài liệu từ Thư viện Đa kênh.

[QUY TRÌNH THỰC THI]
1. Gọi tool `getCompactMessages` với `conversationId: "conv_zalo_8892"` để đọc nội dung câu hỏi gần nhất của khách hàng.
2. Gọi tool `getMessagingCapability` để xác minh kênh Zalo này có đang trong khung thời gian tương tác hợp lệ hay không.
3. Nếu `canSend: true`, gọi tool `sendOutboundMessage` với nội dung chào mừng và mảng `attachments` chứa liên kết tài liệu.
4. Lưu lại `messageId` trả về để đối soát xác nhận tin nhắn đã được gửi thành công.

[TIÊU CHÍ HOÀN THÀNH]
- Tin nhắn phản hồi xuất hiện tức thì trong dòng hội thoại của khách hàng.
- Trả về mã định danh `messageId` và trạng thái gửi thành công (SENT/DELIVERED).
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Gửi một tin nhắn văn bản hoặc tải ảnh lên khung chat | Gọi `getCompactMessages` thấy tin nhắn mới xuất hiện ở cuối danh sách với `direction: OUTBOUND`. |
| Bấm Thu hồi một tin nhắn trên giao diện | Gọi `getCompactMessages` thấy trạng thái tin nhắn chuyển thành `RECALLED` hoặc bị xóa bỏ. |
| Nhấp đúp đổi tên khách hàng trên thanh Chat Header | Gọi `getCompactConversations` thấy thuộc tính `title` cập nhật theo đúng tên mới. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `sendOutboundMessage` | Bong bóng tin nhắn mới lập tức xuất hiện trên màn hình chat với nhãn biểu tượng AI Agent. |
| Agent gọi `recallMessage` | Tin nhắn trên màn hình lập tức chuyển thành thông báo *"Tin nhắn đã được thu hồi"*. |
| Agent gọi `updateConversationTitle` | Tên khách hàng trên thanh Chat Header tự động cập nhật mà không cần tải lại trang. |
