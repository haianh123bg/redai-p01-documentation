## Mở không gian làm việc OmniAI Chat và Điều phối Inbox Đa kênh

Để bắt đầu quản lý hội thoại tập trung từ nhiều kênh chăm sóc khách hàng, phân loại luồng tin nhắn và điều phối nhân sự trực tổng đài trên **OmniAI Chat (Multichannel Chat)**, bạn truy cập vào đường dẫn sau trên thanh điều hướng bên trái của hệ thống **RedAI**:

1. **Không gian làm việc OmniAI Chat (`/multi-channel-chat/:conversationId?`)**: Giao diện làm việc trực tuyến đa kênh hợp nhất toàn bộ tin nhắn từ các nền tảng: **Zalo OA**, **Zalo Cá nhân**, **Facebook Fanpage**, **Facebook Cá nhân**, **Website Widget** và **Gmail**.
2. **Bố cục màn hình làm việc OmniAI Chat**: Được phân chia thành 3 khu vực trực quan:
   - **Thanh bên trái (Chat Sidebar)**: Quản lý bộ lọc tài khoản kết nối, thanh tìm kiếm hội thoại nâng cao, danh sách các cuộc trò chuyện theo thẻ tab, cài đặt hiển thị và công cụ đồng bộ dữ liệu.
   - **Khu vực trung tâm (Chat Area)**: Không gian trò chuyện trực tiếp hiển thị tiêu đề khách hàng, lịch sử trao đổi đa phương tiện và khung soạn thảo tin nhắn hiện đại.
   - **Thanh bên phải (Conversation Info Sidebar)**: Bảng thông tin chi tiết khách hàng, gắn nhãn phân loại, phân công nhân sự, quản trị trường dữ liệu mở rộng và menu tiện ích AI.

---

## Các bước thực hiện

### Giai đoạn 1 — Lọc và chọn tài khoản kết nối đa kênh (Account Selector)

Hệ thống cho phép bạn lọc và hiển thị hội thoại của một hoặc nhiều tài khoản kết nối cùng lúc:

| Bước | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **1. Mở menu Chọn tài khoản** | Tại góc trên cùng bên trái của thanh bên Chat Sidebar, nhấp vào ô <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **Chọn tài khoản** (hiển thị trạng thái số lượng tài khoản đang chọn, ví dụ: `Đã chọn 2 tài khoản` hoặc tên tài khoản chính). |
| **2. Tìm kiếm và chọn kênh** | Trong danh sách thả xuống:<br>• Sử dụng ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm tài khoản...** để định vị nhanh theo tên kênh.<br>• Tích chọn hoặc bỏ chọn từng tài khoản theo nhu cầu (hệ thống phân loại rõ ràng: Tài khoản chính thức OA / Page và Tài khoản cá nhân).<br>• Bấm **Chọn tất cả** nếu muốn theo dõi toàn bộ luồng hội thoại của không gian làm việc. |
| **3. Lưu bộ nhớ lựa chọn** | Lựa chọn tài khoản của bạn được tự động ghi nhớ trên trình duyệt (Session Storage). Khi tải lại trang, hệ thống tự động giữ nguyên các tài khoản bạn đã kích hoạt mà không cần chọn lại từ đầu. |

---

### Giai đoạn 2 — Khai thác bộ lọc tab và thanh tìm kiếm hội thoại nâng cao

| Công cụ | Cách thức thiết lập trên Giao diện UI |
| :--- | :--- |
| **Chuyển đổi Tab trạng thái** | Sử dụng cụm tab chuyển đổi ngay dưới tiêu đề sidebar:<br>• <img src="https://api.iconify.design/lucide:message-square.svg?color=%23ff3333" width="16" alt="" /> **Tất cả (ALL)**: Hiển thị toàn bộ các cuộc trò chuyện từ các tài khoản đã chọn.<br>• <img src="https://api.iconify.design/lucide:mail.svg?color=%23ff3333" width="16" alt="" /> **Chưa đọc (UNREAD)**: Chỉ lọc ra các cuộc hội thoại có tin nhắn mới từ khách hàng chưa được nhân viên mở đọc.<br>• <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Nhóm chat (GROUP)**: Dành riêng cho các hội thoại nhóm Zalo, Telegram hoặc cộng đồng khách hàng. |
| **Tìm kiếm theo từ khóa** | Nhập tên khách hàng, số điện thoại hoặc nội dung tin nhắn vào ô <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Tìm kiếm cuộc trò chuyện** (phím tắt nhanh: `Ctrl + K` hoặc `⌘ + K`). |
| **Lọc chuyên sâu đa điều kiện (Filter Bar)** | Bấm vào nút mở rộng bộ lọc <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> để áp dụng các tiêu chí lọc nâng cao:<br>• **Lọc theo Nhãn (Tags)**: Chọn một hoặc nhiều nhãn danh mục (ví dụ: `Khách VIP`, `Cần Tư Vấn`, `Khiếu Nại`).<br>• **Lọc theo Người đảm nhiệm (Assignee)**: Chọn nhân viên CSKH cụ thể hoặc chọn `Chưa có người đảm nhiệm` để nhặt các cuộc gọi nhỡ/tin nhắn mới về ca trực.<br>• **Lọc theo Trạng thái hội thoại**: Chọn `Đang hoạt động (ACTIVE)`, `Đã lưu trữ (ARCHIVED)`, `Tắt thông báo (MUTED)` hoặc `Đã chặn (BLOCKED)`.<br>• **Lọc theo AI Chat**: Lọc các hội thoại `Đang bật AI Agent` tự động phản hồi hoặc `Tắt AI Agent`. |
| **Tùy biến hiển thị Sidebar** | Bấm biểu tượng <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Cài đặt** trên thanh tiêu đề sidebar:<br>• Bật/tắt công tắc **Hiển thị người đảm nhiệm**: Xem nhanh avatar và tên nhân viên đang phụ trách dưới mỗi dòng tin nhắn.<br>• Bật/tắt công tắc **Hiển thị tag**: Xem các nhãn màu phân loại ngay trên danh sách hội thoại. |

---

### Giai đoạn 3 — Tạo cuộc trò chuyện chủ động và Đồng bộ dữ liệu lịch sử

| Thao tác | Cách thực hiện trên Giao diện UI |
| :--- | :--- |
| **Chủ động tạo cuộc trò chuyện mới** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm cuộc trò chuyện)** trên thanh tiêu đề sidebar:<br>• Hộp thoại **Tạo cuộc trò chuyện mới (CreateConversationModal)** hiển thị.<br>• Chọn tài khoản gửi (kênh Zalo Cá nhân, Zalo OA hoặc Page hỗ trợ nhắn trước).<br>• Nhập số điện thoại, User ID hoặc liên kết trang cá nhân của khách hàng.<br>• Nhập tin nhắn mở đầu và bấm <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" /> **Gửi tin nhắn**. Cuộc hội thoại mới sẽ xuất hiện ngay trên danh sách. |
| **Đồng bộ dữ liệu nền tảng (Reload dữ liệu)** | Bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Reload dữ liệu** trên thanh tiêu đề sidebar:<br>• Hộp thoại **Đồng bộ dữ liệu nền tảng (SyncPlatformModal)** hiển thị.<br>• Chọn tài khoản cần đồng bộ và chọn số lượng cuộc trò chuyện muốn quét về (ví dụ: 50, 100 hoặc toàn bộ).<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Đồng bộ ngay**.<br>• Hệ thống sẽ kích hoạt tiến trình ngầm kiểm tra kết nối và cập nhật toàn bộ tin nhắn mới nhất từ máy chủ của nền tảng về hệ thống RedAI. |
| **Điều chỉnh độ rộng thanh bên (Sidebar Resizer)** | Rê chuột vào đường viền phân cách giữa Chat Sidebar và Chat Area (xuất hiện thanh kéo màu xám). Nhấp giữ chuột và kéo sang trái/phải để tùy chỉnh độ rộng sidebar từ **280px đến 420px** phù hợp với màn hình làm việc của bạn. Bấm nút mũi tên <img src="https://api.iconify.design/lucide:chevron-left.svg?color=%23ff3333" width="16" alt="" /> để thu gọn hoàn toàn sidebar khi cần không gian chat rộng rãi. |

---

### Giai đoạn 4 — Thao tác nhanh trên danh sách cuộc trò chuyện

Trên mỗi dòng hội thoại tại danh sách bên trái:
1. **Đổi trạng thái đã đọc**: Nhấp vào biểu tượng dấu chấm tròn hoặc nhấp chuột phải $\rightarrow$ Chọn **Đánh dấu là đã đọc** để xóa chỉ số thông báo chưa đọc.
2. **Ghim / Tắt thông báo**: Rê chuột vào hội thoại $\rightarrow$ Chọn biểu tượng chuông <img src="https://api.iconify.design/lucide:bell-off.svg?color=%23ff3333" width="16" alt="" /> **Tắt thông báo** cho các hội thoại spam.
3. **Lưu trữ cuộc trò chuyện**: Chọn **Lưu trữ** đối với các hội thoại đã xử lý hoàn tất để làm sạch hộp thư đến mà không bị mất dữ liệu.

---

## Kiểm tra kết quả

Sau khi hoàn tất tiếp nhận và điều phối inbox, bạn kiểm tra lại:

1. **Danh sách hội thoại theo thời gian thực**: Tin nhắn mới từ khách hàng lập tức đẩy cuộc trò chuyện lên đầu danh sách kèm âm báo và chỉ báo số tin nhắn chưa đọc màu đỏ.
2. **Bộ lọc chính xác**: Chuyển đổi giữa các tab `Tất cả`, `Chưa đọc` và `Nhóm chat`, danh sách cập nhật ngay lập tức theo đúng tiêu chí.
3. **Trực quan hóa nhân viên & nhãn**: Dưới mỗi dòng hội thoại hiển thị đúng nhãn màu phân loại và avatar của nhân viên phụ trách ca trực.
4. **Đồng bộ tin nhắn**: Khi bấm Reload dữ liệu, các tin nhắn khách hàng gửi trong lúc nhân viên vắng mặt đều được tải về đầy đủ.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tự động tiếp nhận tin nhắn, quét danh sách inbox, lọc hội thoại theo kênh và quản trị trạng thái cuộc trò chuyện, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - OmniAI Chat` |
| **Mã định danh Kỹ năng (Skill ID)** | `d274fc72-b5d7-4aff-bf25-7eb20fba0eea` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - OmniAI Chat` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71230a76-f1ab-4bdf-8e56-9fe1d8b6fd1a` |
| **Kỹ năng chuyên biệt cho 1 kênh duy nhất** | `RedAI - OmniAI Chat Only One Integration` (`32431888-e2d4-43e3-b21b-580bb82d0926`) |
| **Quyền tài khoản yêu cầu** | Workspace Member, Agent, Operator, Admin hoặc Owner |

---

### Bảng ánh xạ giao diện người dùng sang công cụ AI Agent

| Tác vụ trên Giao diện | Tên Tool tương ứng | Ý nghĩa & Tham số chính |
| :--- | :--- | :--- |
| Mở danh sách inbox `/multi-channel-chat` (chế độ tiết kiệm token) | `getCompactConversations` | Lấy danh sách hội thoại dạng tóm lược tiết kiệm token (`baseIntegrationId`, `page`, `limit`). |
| Lọc hội thoại nâng cao theo kênh, trạng thái, người đảm nhiệm | `getConversations` | Lấy danh sách hội thoại đầy đủ kèm bộ lọc sâu (`platform`, `status`, `tagIds`, `assigneeId`, `isUnread`). |
| Lọc riêng danh sách nhóm chat (Tab Group) | `getGroupConversations` | Lấy danh sách các nhóm trò chuyện đa kênh (`platform`, `baseIntegrationId`). |
| Xem số lượng tin nhắn chưa đọc của người dùng | `getUnreadCount` | Đọc tổng số hội thoại và tin nhắn chưa đọc trong toàn bộ không gian làm việc. |
| Đánh dấu cuộc trò chuyện đã đọc | `markConversationAsRead` | Cập nhật mốc đọc tin nhắn cho tài khoản hiện tại (`conversationId`). |
| Chuyển trạng thái hội thoại (Lưu trữ, Tắt thông báo, Chặn) | `updateConversationStatus` | Đổi trạng thái hội thoại (`id`, `status`: ACTIVE / ARCHIVED / MUTED / BLOCKED / DELETED). |
| Cập nhật trạng thái hàng loạt cho nhiều cuộc trò chuyện | `bulkUpdateConversationStatus` | Áp dụng trạng thái đồng loạt cho danh sách ID hội thoại (`conversationIds`, `status`). |
| Lấy danh sách tài khoản kênh kết nối | `getOmnichatAccounts` | Liệt kê toàn bộ tài khoản tích hợp (Zalo OA, Zalo Personal, Facebook...) đang hoạt động. |

---

### Khung lệnh (Prompt) mẫu chuẩn 4 phần cho AI Agent

Dưới đây là mẫu câu lệnh hoàn chỉnh để ra lệnh cho AI Agent tự động rà soát hộp thư đến đa kênh và báo cáo các hội thoại chưa được xử lý:

```text
[MỤC TIÊU]
Quét toàn bộ hộp thư đến OmniAI Chat của tài khoản Zalo OA CSKH, tìm ra tất cả các cuộc hội thoại chưa đọc và chưa có nhân viên đảm nhiệm, sau đó đánh dấu đã đọc và tóm tắt danh sách cần xử lý gấp.

[DỮ LIỆU ĐẦU VÀO]
- Nền tảng chỉ định: Zalo OA
- Trạng thái hội thoại: Đang hoạt động (ACTIVE)
- Tiêu chí lọc: Tin nhắn chưa đọc (unread: true) và chưa được phân công nhân sự (unassigned: true)
- Số lượng quét tối đa: 20 cuộc trò chuyện gần nhất

[QUY TRÌNH THỰC THI]
1. Gọi tool `getCompactConversations` để lấy danh sách các hội thoại mới nhất thỏa mãn tiêu chí lọc.
2. Với mỗi cuộc trò chuyện tìm thấy, ghi nhận: Tên khách hàng (`customerName`), ID cuộc trò chuyện (`conversationId`), thời gian tin nhắn cuối cùng và nội dung tin nhắn gần nhất.
3. Gọi tool `markConversationAsRead` đối với các hội thoại đã tiếp nhận để cập nhật trạng thái đọc.
4. Tổng hợp danh sách theo bảng báo cáo chi tiết.

[TIÊU CHÍ HOÀN THÀNH]
- Danh sách phản hồi đầy đủ họ tên khách hàng, mã hội thoại và thời điểm nhắn tin.
- Phân loại rõ các tin nhắn có tính chất khẩn cấp hoặc yêu cầu báo giá để nhân viên trực ca tiếp ứng ngay.
- Trả về đường dẫn truy cập trực tiếp đến từng cuộc trò chuyện trên giao diện chat.
```

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Chọn tab Chưa đọc và bấm Đánh dấu đã đọc trên hội thoại | Gọi `getUnreadCount` thấy số đếm giảm đi; gọi `getConversations` thấy cờ `unreadCount: 0`. |
| Bấm chuyển trạng thái hội thoại sang Đã lưu trữ (Archived) | Gọi `getConversations` với tham số `status: ARCHIVED` thấy hội thoại xuất hiện trong danh sách lưu trữ. |
| Bấm Reload dữ liệu đồng bộ lịch sử tin nhắn | Gọi `getCompactMessages` thấy danh sách tin nhắn mới nhất được cập nhật đồng bộ. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `markConversationAsRead` | Biểu tượng chấm đỏ thông báo chưa đọc trên dòng hội thoại lập tức biến mất trên thanh bên. |
| Agent gọi `updateConversationStatus` thành BLOCKED | Hội thoại biến mất khỏi tab Đang hoạt động và chuyển sang danh sách Đã chặn trong bộ lọc nâng cao. |
| Agent gọi `bulkUpdateConversationStatus` | Toàn bộ danh sách các hội thoại chỉ định được cập nhật trạng thái đồng loạt trên màn hình làm việc. |
