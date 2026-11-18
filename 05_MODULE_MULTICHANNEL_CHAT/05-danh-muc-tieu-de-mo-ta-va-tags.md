## Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module OmniAI Chat

Tài liệu này đóng vai trò là danh mục điều hướng trung tâm (Catalog Index) của Phân hệ **05 — Module Multichannel Chat (OmniAI Chat)** trên hệ thống **RedAI**. Bảng tổng hợp siêu dữ liệu dưới đây giúp người dùng, chuyên viên tư vấn và đặc biệt là các trợ lý ảo AI Agent nhanh chóng xác định đúng tài liệu nghiệp vụ cần tham chiếu theo từng tình huống tiếp nhận, xử lý và tiếp thị hội thoại cụ thể.

---

## Bảng tổng hợp siêu dữ liệu các tài liệu nghiệp vụ

| Thuộc tính | Chi tiết tài liệu 01 | Chi tiết tài liệu 02 |
| :--- | :--- | :--- |
| **Tên file** | `01-quy-trinh-tiep-nhan-dieu-phoi-va-quan-ly-inbox-da-kenh.md` | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` |
| **Tiêu đề tài liệu** | Quy trình tiếp nhận, điều phối và quản lý inbox đa kênh | Quy trình soạn tin, tương tác đa phương tiện và kiểm soát năng lực gửi tin |
| **Mô tả nghiệp vụ** | Hướng dẫn mở không gian làm việc OmniAI Chat (`/multi-channel-chat`), lọc tài khoản đa kênh (Zalo OA, Zalo Cá nhân, Facebook, Website, Gmail), khai thác 3 tab trạng thái (Tất cả, Chưa đọc, Nhóm chat), tìm kiếm lọc hội thoại chuyên sâu, đồng bộ dữ liệu lịch sử và tạo cuộc trò chuyện chủ động. | Hướng dẫn đổi tên và ảnh đại diện khách hàng, xem năng lực nền tảng (`PlatformCapabilityModal`), soạn thảo tin nhắn đa phương tiện (văn bản, giọng nói voice, tệp đính kèm, sticker, thư viện đa kênh), tương tác tin nhắn (thả biểu cảm, trả lời trích dẫn, chuyển tiếp, thu hồi) và kiểm soát chính sách gửi tin 24h/7 ngày an toàn. |
| **Agent nên đọc khi** | Cần quét danh sách inbox, lọc hội thoại chưa đọc, kiểm tra số lượng tin chưa đọc, đánh dấu đã đọc hoặc chuyển trạng thái hội thoại (lưu trữ, tắt thông báo, chặn). | Cần đọc nội dung tin nhắn của khách, kiểm tra năng lực gửi tin (`getMessagingCapability`), soạn và gửi tin nhắn phản hồi, gửi ảnh/file, thu hồi tin nhắn hoặc đổi tên hội thoại. |
| **Không dùng khi** | Cần gửi tin nhắn phản hồi chi tiết hoặc cấu hình chiến dịch gửi tin tự động. | Cần tạo chiến dịch gửi tin hàng loạt hoặc phân tích tóm tắt tâm lý bằng AI. |
| **Thực thể & Quan hệ** | `Conversation`, `IntegrationAccount`, `ProviderEnum`, `Workspace`. Hội thoại thuộc về một Tài khoản tích hợp và Không gian làm việc. | `Message`, `Conversation`, `Attachment`, `Platform`, `MessagingCapability`. Mỗi tin nhắn thuộc về một Cuộc hội thoại xác định. |
| **10 Tags chuẩn hóa** | `omnichat-inbox`, `multichannel-chat`, `account-selector`, `unread-filter`, `group-chat`, `search-conversations`, `sync-messages`, `create-conversation`, `conversation-status`, `sidebar-resize` | `send-message`, `rich-text-input`, `voice-input`, `file-attachments`, `sticker-picker`, `multichannel-library`, `reply-message`, `forward-message`, `recall-message`, `messaging-capability` |

---

| Thuộc tính | Chi tiết tài liệu 03 | Chi tiết tài liệu 04 |
| :--- | :--- | :--- |
| **Tên file** | `03-quy-trinh-tom-tat-ai-phan-tich-dong-thoi-gian-va-nhoi-ky-uc-do-thi.md` | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` |
| **Tiêu đề tài liệu** | Quy trình tóm tắt AI, phân tích dòng thời gian và nhồi ký ức đồ thị | Quản lý thẻ nhãn, phân công CSKH, chiến dịch gửi tin và tiện ích |
| **Mô tả nghiệp vụ** | Hướng dẫn khai thác 3 công cụ trí tuệ nhân tạo chuyên sâu: Tóm tắt hội thoại AI (`ConversationSummaryModal` - ý định, chủ đề, sản phẩm, lịch sử tóm tắt), Nhồi ký ức khách hàng vào Đồ thị Tri thức (`AudienceMemoryModal` & Graph RAG), và Phân tích Dòng thời gian (`ConversationTimelineModal` - phiên trao đổi, tâm lý, cảnh báo khoảng lặng và gợi ý chăm sóc lại). | Hướng dẫn quản trị thẻ nhãn (Tags), phân công CSKH & AI Chat, chỉnh sửa trường dữ liệu động, khám phá Trung tâm Tiện ích 2 cấp độ, cơ chế ghim tối đa 2 tiện ích (Pin Utilities), và trọn bộ 5 tiện ích chuyên sâu: Mẫu tin nhắn (Templates), Chiến dịch gửi tin đa kênh (Campaigns - wizard 4 bước), Thu thập Group Zalo bằng link (Crawl Groups với 15 trường ánh xạ vào Database), Đồng bộ nhãn Zalo vào Tag (Sync Labels) và Đồng bộ tên hiển thị Zalo (Sync Display Names). |
| **Agent nên đọc khi** | Cần đọc bối cảnh nhanh qua tóm tắt AI, kiểm tra lịch sử các phiên tóm tắt cũ, tạo tóm tắt mới hoặc nhồi tri thức khách hàng vào mạng lưới Đồ thị Ký ức (Graph RAG). | Cần phân loại hội thoại qua thẻ tag, phân công nhân sự CSKH, bật/tắt AI Chat tự động trả lời, ghim tiện ích lên thanh công cụ, tạo mẫu tin, chạy chiến dịch gửi tin đa kênh, cào nhóm Zalo hoặc đồng bộ nhãn/tên hiển thị Zalo cá nhân. |
| **Không dùng khi** | Cần soạn gửi tin nhắn trực tiếp thông thường hoặc quản lý bộ lọc danh sách tài khoản kết nối. | Cần thao tác đọc tin nhắn đơn lẻ hoặc xem phân tích tâm lý dòng thời gian. |
| **Thực thể & Quan hệ** | `ConversationSummary`, `AudienceMemory`, `KnowledgeGraph`, `ConversationTimeline`. Tóm tắt và ký ức gắn chặt với Khách hàng và Hội thoại. | `ConversationTag`, `WorkspaceMember`, `OmnichannelTemplate`, `OmnichannelCampaign`, `CampaignRecipient`, `ZaloGroupCrawl`, `PinnedUtility`. Quản trị nguồn lực, tiện ích và chiến dịch gửi tin. |
| **10 Tags chuẩn hóa** | `ai-summary`, `customer-intent`, `summary-history`, `graph-rag`, `audience-memory`, `conversation-timeline`, `sentiment-analysis`, `inactivity-alert`, `re-engagement-advice`, `ai-recommendations` | `conversation-tags`, `cskh-assignment`, `multichannel-utilities`, `pin-utilities`, `omnichannel-templates`, `omnichannel-campaigns`, `zalo-crawl-groups`, `zalo-sync-labels`, `zalo-sync-names`, `campaign-delay` |

---

| Thuộc tính | Chi tiết tài liệu 05 |
| :--- | :--- |
| **Tên file** | `05-danh-muc-tieu-de-mo-ta-va-tags.md` |
| **Tiêu đề tài liệu** | Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module OmniAI Chat |
| **Mô tả nghiệp vụ** | Bảng tổng hợp siêu dữ liệu, bản đồ từ khóa và quy tắc định tuyến thông minh giữa người dùng, hệ thống tài liệu và trợ lý ảo AI Agent cho toàn bộ Phân hệ 05 — Module Multichannel Chat. |
| **Agent nên đọc khi** | Cần định vị nhanh tài liệu phù hợp khi tiếp nhận yêu cầu từ người dùng liên quan đến hội thoại đa kênh, nhắn tin, phân công CSKH hoặc chiến dịch gửi tin nhắn. |
| **Không dùng khi** | Đã xác định được chính xác nghiệp vụ cụ thể cần thực hiện trong 4 tài liệu chuyên sâu 01, 02, 03, 04. |
| **Thực thể & Quan hệ** | `DocumentationCatalog`, `ModuleMetadata`, `AIAgentRouting`. |
| **10 Tags chuẩn hóa** | `multichannel-catalog`, `metadata-index`, `agent-routing`, `inbox-guide`, `messaging-guide`, `ai-analysis-guide`, `campaign-guide`, `template-guide`, `multichannel-module`, `redai-documentation` |

---

## Bảng định tuyến nhanh theo tình huống thực tế

Dưới đây là bảng tra cứu phản xạ nhanh giúp người dùng và trợ lý ảo AI Agent chọn ngay tài liệu cần thiết:

| Tình huống thực tế phát sinh | Tài liệu cần mở ngay | Công cụ / Đường dẫn trọng tâm |
| :--- | :--- | :--- |
| Muốn xem toàn bộ tin nhắn chưa đọc của kênh Zalo OA và Page | `01-quy-trinh-tiep-nhan-dieu-phoi-va-quan-ly-inbox-da-kenh.md` | Tab `UNREAD`, `getCompactConversations` |
| Cần đồng bộ lại các tin nhắn cũ từ server của nền tảng về hệ thống | `01-quy-trinh-tiep-nhan-dieu-phoi-va-quan-ly-inbox-da-kenh.md` | Nút `Reload dữ liệu`, `SyncPlatformModal` |
| Muốn chủ động mở cuộc trò chuyện mới gửi tới một số điện thoại Zalo | `01-quy-trinh-tiep-nhan-dieu-phoi-va-quan-ly-inbox-da-kenh.md` | Nút `+ Thêm cuộc trò chuyện`, `CreateConversationModal` |
| Cần đổi tên gợi nhớ khách hàng hoặc đổi ảnh đại diện hội thoại | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` | Nhấp đúp tên trên `ChatHeader`, `updateConversationTitle` |
| Muốn kiểm tra xem Facebook có cho phép gửi tin nhắn lại hay đã quá 24h | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` | `PlatformCapabilityModal`, `getMessagingCapability` |
| Cần thu hồi gấp một tin nhắn báo giá đã gửi nhầm cho khách hàng | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` | Menu tin nhắn $\rightarrow$ `Thu hồi`, `recallMessage` |
| Muốn nhập tin nhắn nhanh bằng giọng nói tiếng Việt | `02-quy-trinh-soan-tin-tuong-tac-da-phuong-tien-va-kiem-soat-nang-luc-gui-tin.md` | Biểu tượng micro trên `ModernChatInput` |
| Cần nắm bắt nhanh khách hàng đang muốn mua gì trong cuộc chat 50 tin | `03-quy-trinh-tom-tat-ai-phan-tich-dong-thoi-gian-va-nhoi-ky-uc-do-thi.md` | `ConversationSummaryModal`, `getLatestConversationSummary` |
| Muốn biết lý do vì sao khách hàng im lặng sau khi nhận báo giá và câu mở lời kéo khách | `03-quy-trinh-tom-tat-ai-phan-tich-dong-thoi-gian-va-nhoi-ky-uc-do-thi.md` | `ConversationTimelineModal`, Khối Cảnh báo khoảng lặng |
| Cần lưu thông tin sở thích và chức vụ của khách vào Đồ thị Ký ức lâu dài | `03-quy-trinh-tom-tat-ai-phan-tich-dong-thoi-gian-va-nhoi-ky-uc-do-thi.md` | `AudienceMemoryModal`, `consolidateConversationMemory` |
| Cần tạo nhãn màu "Khách Tiềm Năng" và gắn vào cuộc hội thoại | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Mục Nhãn trên `ConversationInfoSidebar`, `addTagsToConversation` |
| Muốn giao cuộc trò chuyện cho nhân viên CSKH khác xử lý | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Mục Người hỗ trợ, `addConversationWorkspaceUsers` |
| Cần tắt AI Chat tự động trả lời để nhân viên tự chat tay với khách VIP | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Công tắc AI Chat trên sidebar phải, `updateAutoReply` |
| Muốn tạo mẫu tin nhắn xác nhận đơn hàng có chèn mã đơn và tên khách | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Tiện ích `TEMPLATES`, `createOmnichannelTemplate` |
| Muốn gửi tin nhắn hàng loạt cho 200 khách hàng trong Bảng dữ liệu | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Tiện ích `CAMPAIGNS`, `createOmnichannelCampaign` |
| Muốn đồng bộ toàn bộ nhãn từ app Zalo cá nhân vào hệ thống RedAI | `04-quan-ly-the-nhan-phan-cong-cskh-chien-dich-gui-tin-va-tien-ich.md` | Tiện ích `SYNC_LABELS` trong Trung tâm Tiện ích |

---

## Danh mục từ khóa tìm kiếm (Keyword Index)

- **Hộp thư & Điều phối**: `omnichannel inbox`, `hội thoại đa kênh`, `chọn tài khoản`, `tài khoản chính thức`, `tài khoản cá nhân`, `lọc chưa đọc`, `chat nhóm`, `tìm kiếm cuộc trò chuyện`, `reload dữ liệu`, `đồng bộ platform`, `chủ động tạo hội thoại`, `thu gọn sidebar`, `kéo dãn độ rộng`.
- **Soạn tin & Đa phương tiện**: `soạn tin nhắn`, `rich text tiptap`, `nhắc tên mention`, `nhập bằng giọng nói`, `voice input`, `đính kèm file`, `dán ảnh clipboard`, `sticker picker`, `thư viện đa kênh`, `mẫu email gmail`, `trả lời trích dẫn`, `thả biểu cảm reaction`, `chuyển tiếp tin nhắn`, `thu hồi tin nhắn`, `năng lực gửi tin`, `chính sách 24h facebook`, `cửa sổ 7 ngày zalo`.
- **Trí tuệ nhân tạo & Ký ức**: `tóm tắt hội thoại ai`, `ý định khách hàng`, `chủ đề quan tâm`, `sản phẩm quan tâm`, `độ tin cậy`, `lịch sử tóm tắt`, `nhồi ký ức đồ thị`, `graph rag memory`, `audience knowledge graph`, `unified graph job`, `dòng thời gian tương tác`, `timeline modal`, `phân tích tâm lý`, `khoảng lặng tương tác`, `inactivity alert`, `gợi ý chăm sóc lại`, `ai recommendations`.
- **Quản trị, Tiếp thị & Tiện ích**: `thẻ nhãn tag`, `quản lý nhãn`, `gán nhãn hàng loạt`, `phân công nhân sự`, `người hỗ trợ collaborators`, `bật tắt ai chat`, `tự động trả lời auto reply`, `trường tùy chỉnh custom fields`, `mẫu tin nhắn templates`, `biến động placeholder`, `chiến dịch gửi tin campaigns`, `chia đều template round robin`, `đối tượng từ dynamic table`, `giãn cách delay chống spam`, `thu thập group zalo`, `đồng bộ nhãn zalo`, `đồng bộ tên hiển thị`, `ghim tiện ích`.
