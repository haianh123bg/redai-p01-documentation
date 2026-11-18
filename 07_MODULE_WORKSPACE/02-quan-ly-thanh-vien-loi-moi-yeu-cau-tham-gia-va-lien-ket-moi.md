## Tổng quan hệ thống quản lý thành viên, lời mời và kết nối cộng tác

Trong môi trường làm việc cộng tác đa người dùng của **RedAI**, **Trung tâm Quản trị Thành viên & Lời mời** là hạt nhân điều phối nhân sự của từng Workspace, giúp chủ doanh nghiệp và quản trị viên phân quyền chính xác, mở rộng đội ngũ và kiểm soát an toàn bảo mật. Hệ thống cung cấp giải pháp quản trị toàn diện:

- **Phân cấp vai trò rõ ràng**: Hỗ trợ các vai trò tiêu chuẩn cấp Workspace: **Chủ sở hữu (Owner)**, **Quản trị viên (Admin)** và **Thành viên (Member)**, kết hợp khả năng cấp quyền cục bộ vào từng cơ sở dữ liệu (**Base**) ngay từ lúc gửi lời mời.
- **Đa dạng phương thức kết nối thành viên**: Hỗ trợ mời đích danh qua địa chỉ thư điện tử (Email), tiếp nhận đơn xin tham gia tự nguyện (Join Requests), và phát hành Liên kết mời tham gia (Invite Links) tiện lợi.
- **Kiểm soát hạn mức và tự động hóa vòng đời lời mời**: Theo dõi số lượng chỗ ngồi (Member Slots), tự động cảnh báo khi chạm giới hạn gói cước, hỗ trợ gửi lại mã mời, thu hồi khẩn cấp hoặc dọn dẹp hàng loạt lời mời đã hết hạn.

---

## Các tính năng chi tiết trên giao diện

Các nghiệp vụ quản trị nhân sự trong Workspace được tổ chức trực quan theo các chức năng sau:

```
[Cài đặt Workspace] ──> [Thẻ Thành viên] ──> [Bấm "Thêm thành viên" qua Email]
           │                                 │
           ├──> [Danh sách lời mời] ─────────┴──> [Theo dõi trạng thái: Chờ / Hết hạn / Thu hồi]
           │
           ├──> [Yêu cầu tham gia] ──────────────> [Duyệt / Từ chối đơn gia nhập]
           │
           └──> [Liên kết mời] ──────────────────> [Bật/Tắt link, Tạo mã mới, Sao chép link]
```

| STT | Tính năng trên UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở Trung tâm Quản lý Thành viên** | • Từ Trình duyệt Không gian làm việc: Rê chuột lên Workspace $\rightarrow$ Bấm nút ba chấm <img src="https://api.iconify.design/lucide:ellipsis-vertical.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Thành viên**.<br>• Hoặc mở **Hộp thoại Cài đặt Workspace** (biểu tượng bánh răng <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" />) $\rightarrow$ Nhấp chọn thẻ <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Thành viên**.<br>• Bảng danh sách thành viên hiện ra với 4 cột thông tin: *Người dùng* (Họ tên, Email, Avatar), *Vai trò*, *Ngày tham gia* và *Không gian nhóm (Base)* đã tham gia. |
| **2** | **Mời thành viên mới qua Email** | • Ở góc trên bên phải của thẻ Thành viên, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm thành viên**.<br>• Hộp thoại mời thành viên mở ra:<br>  + **Email \***: Nhập chính xác địa chỉ hòm thư của nhân sự cần mời (ví dụ: `nhanvien@congty.com`).<br>  + **Vai trò \***: Chọn vai trò cấp Workspace từ danh sách thả xuống (*Quản trị viên workspace*, *Thành viên workspace*).<br>  + **Thêm vào base (tùy chọn)**: Bạn có thể chọn trước một cơ sở dữ liệu (Base) cụ thể và chọn luôn vai trò tại Base đó (*Chủ sở hữu*, *Biên tập viên*, *Người xem*) để thành viên có thể vào việc ngay sau khi đồng ý.<br>• Nhấn nút <img src="https://api.iconify.design/lucide:send.svg?color=%23ff3333" width="16" alt="" /> **Gửi lời mời**. Hệ thống tự động gửi email thông báo kèm liên kết xác nhận và hiển thị thông báo: *"Đã thêm thành viên thành công"*. |
| **3** | **Giám sát Giới hạn thành viên & Mua thêm slot** | • Ngay trên đầu danh sách thành viên, khối **Giới hạn thành viên workspace** hiển thị tình trạng chỗ ngồi:<br>  + Nếu không giới hạn: Hiển thị thông điệp *"Workspace này hiện không áp dụng giới hạn số lượng thành viên"*.<br>  + Nếu có hạn mức: Hiển thị dòng trạng thái *"Hỗ trợ tối đa X thành viên. Đang sử dụng Y, còn lại Z chỗ"*, kèm thanh tiến trình trực quan.<br>• Khi đã dùng hết slot: Nút đỏ <img src="https://api.iconify.design/lucide:shopping-cart.svg?color=%23ff3333" width="16" alt="" /> **Mua thêm slot** sẽ sáng lên. Bấm vào nút để mở bảng chọn gói tính năng Addon mở rộng quy mô nhân sự. |
| **4** | **Đổi vai trò và phân quyền thành viên** | • Tìm đến dòng thành viên cần phân công lại trong bảng danh sách $\rightarrow$ Bấm nút thao tác ở cuối dòng $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Đổi vai trò**.<br>• Chọn vai trò mới mong muốn trong menu thả xuống $\rightarrow$ Bấm **Lưu**.<br>• Nhãn vai trò của thành viên lập tức chuyển đổi và hệ thống đồng bộ lại quyền hạn truy cập của người dùng đó trong tích tắc. |
| **5** | **Xóa thành viên khỏi Workspace** | • Khi một nhân sự nghỉ việc hoặc chuyển dự án: Nhấp vào nút ba chấm ở cuối dòng thành viên $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa khỏi workspace**.<br>• Hộp thoại cảnh báo bảo mật xuất hiện: *"Bạn có chắc muốn xóa [Tên thành viên] khỏi không gian làm việc?"*.<br>• Nhấn nút màu đỏ **Xác nhận xóa**. Thành viên đó sẽ lập tức mất toàn bộ quyền truy cập vào Workspace và các Base bên trong. |
| **6** | **Quản lý Danh sách Lời mời đang chờ** | • Nhấp chuyển sang thẻ <img src="https://api.iconify.design/lucide:mail.svg?color=%23ff3333" width="16" alt="" /> **Lời mời đang chờ**.<br>• Bảng hiển thị toàn bộ các email đã gửi kèm cột *Trạng thái* (Đang chờ, Đã chấp nhận, Hết hạn, Đã thu hồi) và thời điểm hết hạn.<br>• **Gửi lại lời mời**: Đối với các lời mời đang chờ hoặc hết hạn, bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Gửi lại** để gửi email nhắc nhở mới.<br>• **Thu hồi lời mời**: Bấm nút <img src="https://api.iconify.design/lucide:x-circle.svg?color=%23ff3333" width="16" alt="" /> **Thu hồi** nếu gửi nhầm email để vô hiệu hóa liên kết ngay lập tức.<br>• **Xóa lời mời hàng loạt**: Tích chọn vào ô vuông ở đầu các dòng lời mời $\rightarrow$ Bấm nút đỏ <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa các lời mời đã chọn** $\rightarrow$ Xác nhận để làm sạch danh sách. |
| **7** | **Quản lý Yêu cầu tham gia (Join Requests)** | • Nhấp chuyển sang thẻ <img src="https://api.iconify.design/lucide:user-plus.svg?color=%23ff3333" width="16" alt="" /> **Yêu cầu tham gia**.<br>• Bảng hiển thị thông tin những người dùng đã nộp đơn xin gia nhập Workspace.<br>• **Duyệt gia nhập**: Bấm nút màu xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Duyệt** $\rightarrow$ Người dùng chính thức trở thành thành viên của Workspace.<br>• **Từ chối**: Bấm nút <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> **Từ chối** $\rightarrow$ Hộp thoại xác nhận hiện ra $\rightarrow$ Bấm xác nhận để hủy đơn đăng ký. |
| **8** | **Cấu hình Tham gia qua Liên kết mời** | • Nhấp chuyển sang thẻ <img src="https://api.iconify.design/lucide:link.svg?color=%23ff3333" width="16" alt="" /> **Liên kết mời**.<br>• Gạt công tắc **Cho phép tham gia qua liên kết** sang trạng thái Bật màu xanh.<br>• Ô **Liên kết mời** xuất hiện chứa đường dẫn gia nhập nhanh kèm mã token bảo mật.<br>• Bấm nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Sao chép liên kết mời** để gửi cho nhóm chat hoặc mạng xã hội nội bộ.<br>• Khi cần đổi liên kết chống rò rỉ: Bấm nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Tạo liên kết mới**, link cũ sẽ bị vô hiệu hóa lập tức. |
| **9** | **Tiếp nhận lời mời và Hộp thoại Lời mời của tôi** | • **Người nhận link**: Mở liên kết được mời $\rightarrow$ Trang **Tham gia workspace** hiển thị thông tin Workspace và Chủ sở hữu $\rightarrow$ Bấm nút xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Chấp nhận lời mời** để tham gia.<br>• **Hộp thoại Lời mời của tôi**: Truy cập danh sách các lời mời gửi đến tài khoản của bạn $\rightarrow$ Bấm **Chấp nhận** hoặc **Từ chối** bất kỳ lời mời nào. |

---

## Kiểm tra kết quả

Sau khi thực hiện các nghiệp vụ quản trị thành viên, bạn có thể kiểm chứng kết quả trên giao diện:

1. **Sau khi mời thành viên mới**: Một dòng mới xuất hiện trong thẻ *Lời mời đang chờ* với nhãn màu vàng `Đang chờ`.
2. **Sau khi thành viên chấp nhận**: Tên và ảnh đại diện của thành viên xuất hiện chính thức trong bảng thẻ *Thành viên*, số đếm thành viên tăng lên `+1`.
3. **Sau khi tạo liên kết mời mới**: Thử mở liên kết bằng trình duyệt ẩn danh, trang chào đón *Tham gia workspace* hiển thị đầy đủ tên Workspace và thông tin người mời.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Workbase & Workspace Management` |
| **Mã định danh Kỹ năng (Skill ID)** | `4fa87112-9b2c-46ea-8822-1d187e59b201` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Workbase` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71c42938-16e5-4d29-9e87-251f9a84b102` |
| **Quyền tài khoản yêu cầu** | Quản trị viên Workspace (Workspace Admin hoặc Owner) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tra cứu danh sách thành viên** | `getWorkspaceMembers` | `Hãy liệt kê toàn bộ danh sách thành viên đang hoạt động trong Workspace hiện tại kèm email và vai trò của họ.` |
| **Mời thành viên mới qua Email** | `inviteWorkspaceMember` | `Hãy gửi lời mời tham gia Workspace cho email "tranvanduc@gmail.com" với vai trò "workspace_member" và gán vào Base "Dự án Alpha".` |
| **Đổi vai trò của thành viên** | `updateWorkspaceMemberRole` | `Hãy nâng vai trò của thành viên có userId 104 lên thành "workspace_admin" trong Workspace này.` |
| **Xóa thành viên khỏi Workspace** | `removeWorkspaceMember` | `Hãy xóa thành viên có userId 182 ra khỏi Không gian làm việc do đã chuyển vị trí công tác.` |
| **Kiểm tra danh sách lời mời đang chờ** | `getWorkspaceInvites` | `Hãy kiểm tra xem hiện tại Workspace có những lời mời nào đang ở trạng thái chờ (PENDING) hoặc đã hết hạn (EXPIRED).` |
| **Gửi lại lời mời cho thành viên** | `resendWorkspaceInvite` | `Lời mời của email "nguyenthimai@gmail.com" chưa được phản hồi, hãy gửi lại mã mời giúp tôi.` |
| **Thu hồi lời mời khẩn cấp** | `revokeWorkspaceInvite` | `Tôi vừa gửi nhầm lời mời cho email lạ, hãy thu hồi ngay lời mời có inviteId "inv_8829104".` |
| **Duyệt đơn yêu cầu tham gia** | `approveJoinRequest` | `Người dùng "Lê Văn Hùng" vừa nộp yêu cầu tham gia Workspace, hãy duyệt yêu cầu có requestId "req_992182".` |
| **Lấy liên kết mời tham gia** | `getWorkspaceInviteLink` | `Hãy kiểm tra xem chế độ tham gia bằng link mời có đang bật không và gửi cho tôi đường dẫn liên kết mời mới nhất.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm gửi lời mời cho email mới trên giao diện | Gọi `getWorkspaceInvites` thấy xuất hiện 1 bản ghi với đúng email và trạng thái `PENDING`. |
| Đổi vai trò thành viên sang Quản trị viên | Gọi `getWorkspaceMembers` thấy trường `role` của thành viên đó chuyển thành `workspace_admin`. |
| Duyệt 1 yêu cầu tham gia trên bảng | Gọi `getWorkspaceMembers` thấy người dùng đó đã xuất hiện trong danh sách thành viên chính thức. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `inviteWorkspaceMember` thành công | Mở thẻ Lời mời đang chờ trên giao diện, dòng email mới xuất hiện kèm nhãn vàng `Đang chờ`. |
| Agent gọi `removeWorkspaceMember` | Tải lại thẻ Thành viên, dòng tài khoản của nhân sự bị xóa biến mất khỏi bảng danh sách. |
| Agent gọi `regenerateInviteLink` | Khung hiển thị Liên kết mời trên thẻ Liên kết mời đổi sang chuỗi URL và token mới. |
