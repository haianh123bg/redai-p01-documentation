## Tổng quan quy trình khởi tạo, chuyển đổi ngữ cảnh và điều hướng Workspace

Trong kiến trúc nền tảng **RedAI**, **Workspace (Không gian làm việc)** là đơn vị tổ chức cao nhất cấp tổ chức/doanh nghiệp, đóng vai trò như một môi trường độc lập bao bọc toàn bộ cơ sở dữ liệu (**Base**), dự án AI, luồng tự động hóa (Workflow), thành viên và hạ tầng tài nguyên. Việc nắm vững quy trình khởi tạo và điều hướng Workspace mang lại nhiều giá trị thiết thực:

- **Phân tách dữ liệu an toàn và độc lập**: Mỗi Workspace vận hành một không gian lưu trữ riêng biệt, bảo vệ tuyệt đối dữ liệu nội bộ giữa các phòng ban, công ty con hoặc các khách hàng doanh nghiệp khác nhau.
- **Quản lý ngữ cảnh làm việc liền mạch**: Người dùng có thể nhanh chóng chuyển đổi ngữ cảnh làm việc từ Workspace cá nhân sang Workspace doanh nghiệp hoặc Workspace hệ thống trực tiếp từ thanh điều phối hoặc khung chat AI.
- **Hệ thống định danh chuẩn hóa**: Mỗi Workspace sở hữu một mã định danh duy nhất (Workspace ID) và đường dẫn thân thiện (Slug), hỗ trợ tích hợp API, webhook và chia sẻ liên kết cộng tác chuẩn xác.

---

## Các bước thực hiện chi tiết trên giao diện

Quy trình khởi tạo, chuyển đổi ngữ cảnh và điều hướng Workspace bao gồm các bước tuần tự sau:

```
[Mở Trình duyệt Không gian] ──> [Duyệt danh sách Workspace] ──> [Mở rộng xem các Base]
            │                                                              │
            ├──> [Bấm "Tạo Workspace mới"] ──> [Điền Tên, Slug, Mô tả]     ▼
            │                                                 [Chọn Base để chuyển ngữ cảnh]
            └──> [Menu ba chấm Workspace] ──> [Sao chép ID / Xem quyền / Rời Workspace]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở Trình duyệt Không gian làm việc** | • Tại góc dưới bên trái màn hình làm việc hoặc tại thanh tiêu đề của bảng điều khiển chat AI, nhấp chuột vào tên Workspace hiện tại (kèm biểu tượng mũi tên hoặc logo đại diện).<br>• Ngăn trượt **Trình duyệt Không gian làm việc** mở ra từ cạnh bên, hiển thị danh mục phân cấp toàn bộ các Workspace mà bạn sở hữu hoặc được mời tham gia. |
| **2** | **Duyệt danh sách Workspace và các Base trực thuộc** | • Giao diện liệt kê danh sách Workspace theo thứ tự ưu tiên: Workspace bạn làm chủ sở hữu và Workspace cộng tác.<br>• Mỗi dòng Workspace hiển thị tên, ảnh logo đại diện và số lượng không gian làm việc (Base) trực thuộc.<br>• Nhấp vào biểu tượng mũi tên mở rộng cạnh tên Workspace để hiển thị danh sách các Base (không gian dữ liệu nhóm) đang hoạt động bên trong.<br>• Workspace đang là ngữ cảnh kích hoạt hiện tại sẽ có dấu tích xanh nổi bật <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> và chấm màu chủ đạo. |
| **3** | **Chuyển đổi ngữ cảnh làm việc (Active Scope)** | • Để chuyển sang làm việc tại một Không gian khác: Nhấp chuột trực tiếp vào tên Base hoặc Workspace mong muốn trong danh sách.<br>• Hệ thống kích hoạt cơ chế dọn dẹp bộ nhớ đệm an toàn, reset phiên chat hiện tại để tránh nhầm lẫn dữ liệu giữa hai không gian, sau đó tự động chuyển hướng đường dẫn trình duyệt sang không gian mới.<br>• Biểu tượng tích xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> lập tức chuyển sang vị trí mới, toàn bộ dữ liệu bảng, workflow và trợ lý AI sẽ tự động đồng bộ theo đúng Workspace vừa chọn. |
| **4** | **Khởi tạo Workspace mới** | • Trên thanh công cụ của Trình duyệt Không gian làm việc, nhấp vào nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo Workspace mới** (hoặc truy cập trang `/workspaces/create`).<br>• Biểu mẫu khởi tạo mở ra với các trường thông tin:<br>  + **Tên Workspace \***: Nhập tên định danh hiển thị của tổ chức (ví dụ: `Chi nhánh Miền Nam - RedAI`).<br>  + **Đường dẫn rút gọn (Slug) \***: Hệ thống tự động tạo slug từ tên hoặc bạn có thể chỉnh sửa thủ công (ví dụ: `chi-nhanh-mien-nam`). Slug chỉ chứa chữ cái thường, chữ số và dấu gạch ngang, đảm bảo duy nhất trên toàn hệ thống.<br>  + **Mô tả**: Nhập thông tin tóm tắt về mục đích vận hành của không gian (không bắt buộc).<br>• Nhấn nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Tạo Workspace**. Hệ thống tạo mới thành công, cấp quyền Chủ sở hữu tuyệt đối và tự động chuyển ngữ cảnh vào Workspace mới. |
| **5** | **Sao chép Workspace ID** | • Rê chuột lên dòng Workspace mong muốn $\rightarrow$ Bấm nút menu ba chấm <img src="https://api.iconify.design/lucide:ellipsis-vertical.svg?color=%23ff3333" width="16" alt="" /> ở góc phải dòng.<br>• Chọn tùy chọn <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **Sao chép workspace ID**.<br>• Mã định danh UUID chuẩn của Workspace được lưu vào bộ nhớ tạm (clipboard) kèm thông báo nổi: *"Đã sao chép workspace ID vào clipboard"*, sẵn sàng để bạn dán vào API, kịch bản webhook hoặc cấu hình bot. |
| **6** | **Xem nhanh Quyền của tôi trên Workspace** | • Trong menu ba chấm của dòng Workspace, nhấp chọn <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Quyền của tôi**.<br>• Hộp thoại hiển thị vai trò hiện tại của bạn trong Workspace (Chủ sở hữu, Quản trị viên, Thành viên) cùng danh mục đầy đủ các quyền hạn (Capabilities) được cấp phép trên phạm vi Workspace này. |
| **7** | **Rời khỏi Workspace** | • Đối với Workspace mà bạn tham gia với tư cách thành viên (không phải Chủ sở hữu): Trong menu ba chấm, nhấp chọn <img src="https://api.iconify.design/lucide:log-out.svg?color=%23ff3333" width="16" alt="" /> **Rời khỏi workspace**.<br>• Hộp thoại cảnh báo xuất hiện: *"Bạn có chắc chắn muốn rời khỏi workspace này không?"*.<br>• Nhấn nút xác nhận **Rời khỏi workspace** màu đỏ. Bạn sẽ bị thu hồi quyền truy cập và danh sách Workspace tự động cập nhật lại. |

---

## Kiểm tra kết quả

Sau khi hoàn tất khởi tạo hoặc điều hướng Workspace, bạn có thể kiểm chứng kết quả trên giao diện:

1. **Trên thanh điều hướng chính**: Tên Workspace và logo mới được cập nhật trên thanh tiêu đề, menu ứng dụng nạp lại danh sách phân hệ được phép truy cập theo gói dịch vụ của Workspace đó.
2. **Trên Trình duyệt Không gian làm việc**: Dấu tích xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> xuất hiện cố định cạnh tên Workspace và Base đang hoạt động.
3. **Trên URL trình duyệt**: Đường dẫn hiển thị đúng cấu trúc định tuyến ngữ cảnh `/w/[slug-hoac-id]/...`, đảm bảo mọi thao tác lưu trữ dữ liệu đều thuộc quyền quản lý của đúng Workspace đích.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tra cứu thông tin Workspace, hỗ trợ tạo mới không gian làm việc hoặc chuyển đổi ngữ cảnh điều phối tự động, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Workbase & Workspace Management` |
| **Mã định danh Kỹ năng (Skill ID)** | `4fa87112-9b2c-46ea-8822-1d187e59b201` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Workbase` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71c42938-16e5-4d29-9e87-251f9a84b102` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tra cứu danh sách Workspace của tôi** | `getMyWorkspaces` | `Hãy liệt kê toàn bộ danh sách Workspace mà tài khoản của tôi đang tham gia kèm vai trò và trạng thái sở hữu.` |
| **Tạo Workspace mới** | `createWorkspace` | `Hãy tạo một Workspace mới có tên là "Phòng Kinh Doanh Số", slug "phong-kinh-doanh-so", mô tả "Không gian quản lý kinh doanh và chiến dịch khách hàng".` |
| **Xem chi tiết cấu hình Workspace** | `getWorkspaceDetail` | `Hãy tra cứu thông tin chi tiết của Workspace có ID "e79b6ce8-e8ac-4d22-827e-54c75e87946f" xem ai là chủ sở hữu và múi giờ đang đặt là gì.` |
| **Kiểm tra tính khả dụng của Slug** | `checkWorkspaceSlugAvailability` | `Hãy kiểm tra xem slug "redai-hcm" đã có tổ chức nào sử dụng chưa để tôi đặt cho Workspace mới.` |
| **Chuyển đổi ngữ cảnh làm việc** | `switchWorkspaceContext` | `Hãy chuyển ngữ cảnh hoạt động hiện tại sang Workspace "Phòng Kinh Doanh Số" để tôi bắt đầu làm việc với dữ liệu của bộ phận này.` |
| **Rời khỏi Workspace cộng tác** | `leaveWorkspace` | `Tôi không còn tham gia dự án này nữa, hãy hỗ trợ tôi thực hiện thao tác rời khỏi Workspace có ID "a1b2c3d4-e5f6-7a8b-9c0d-1e2f3a4b5c6d".` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm tạo mới Workspace và lưu thành công | Gọi `getMyWorkspaces` thấy xuất hiện thêm 1 bản ghi mới với đúng tên và vai trò là `OWNER`. |
| Nhấp chuyển sang Workspace khác trên Trình duyệt Không gian | Gọi `getCurrentWorkspaceContext` thấy `workspaceId` trả về đúng UUID của Workspace vừa chọn. |
| Bấm xác nhận Rời khỏi Workspace trên giao diện | Gọi `getMyWorkspaces` thấy Workspace tương ứng không còn nằm trong danh sách trả về. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createWorkspace` thành công | Mở Trình duyệt Không gian làm việc, thấy Workspace mới hiển thị ngay trên đầu danh sách. |
| Agent gọi `switchWorkspaceContext` | Giao diện tự động tải lại, logo và tên Workspace trên thanh điều hướng đổi sang Workspace mới được chỉ định. |
| Agent gọi `leaveWorkspace` | Danh sách Workspace trong trình duyệt tự động loại bỏ Workspace bị rời khỏi mà không cần tải lại toàn trang. |
