## Tổng quan hệ thống phân quyền, vai trò và danh sách role đa miền

Hệ thống phân quyền trên nền tảng **RedAI** được xây dựng theo mô hình **Kiểm soát truy cập dựa trên khả năng đa miền (Domain-Driven Capability-Based Access Control — CBAC)**. Mô hình này vượt trội hơn các hệ thống phân quyền truyền thống nhờ tính linh hoạt tuyệt đối, cho phép doanh nghiệp phân tách ranh giới an toàn dữ liệu từ cấp độ vĩ mô (toàn bộ Workspace) xuống vi mô (từng bảng, từng trường dữ liệu, từng công cụ AI hoặc từng quy trình Workflow).

Kiến trúc phân quyền RedAI vận hành dựa trên 3 trụ cột cốt lõi:

1. **Phân cấp hai phạm vi kiểm soát (Two-Tier Scopes)**:
   - **Phạm vi Không gian làm việc (Workspace Scope)**: Quản lý các quyền vĩ mô như quản trị thành viên, mời nhân sự, thiết lập thanh toán, mua addon và cấu hình hệ sinh thái chung.
   - **Phạm vi Không gian nhóm (Base Scope)**: Quản lý các quyền cục bộ trên từng cơ sở dữ liệu cụ thể, bao gồm thiết kế bảng, phân quyền xem/sửa bản ghi và phân công bot trò chuyện.
2. **Ma trận 32 Miền nghiệp vụ (32 Business Domains)**: Phân quyền chuyên sâu theo từng phân hệ chức năng: `workspace`, `base`, `workspace_member`, `base_member`, `dynamic_table`, `table`, `view`, `field`, `record`, `source`, `acl`, `hook`, `api_token`, `comment`, `integration`, `agent`, `workflow`, `marketing`, `project`, `data`, `ask_ai`, `chat`, `calendar`, `tools`, `mcp_dynamic`, `models`, v.v.
3. **17 Nhóm hành động hạt nhân (17 Core Actions)**: Định nghĩa chính xác mức độ can thiệp: `read` (xem), `create` (tạo mới), `update` (cập nhật), `delete` (xóa), `manage` (quản lý toàn quyền), `share` (chia sẻ), `duplicate` (nhân bản), `invite` (mời), `assign` (gán), `import` (nhập), `export` (xuất), `sync` (đồng bộ), `execute` (thực thi), `connect` (kết nối), v.v.

---

## Các bước thực hiện chi tiết trên giao diện

Quy trình quản trị và thiết lập vai trò phân quyền được tiến hành theo các bước sau:

```
[Mở Cài đặt Workspace] ──> [Thẻ Thành viên] ──> [Bấm "Danh sách role quyền"]
            │
            ├──> [Xem chi tiết Role & Quyền mặc định]
            │
            ├──> [Bấm "Tạo mới role"] ──> [Điền Mã, Tên, Phạm vi, Chọn Capabilities]
            │
            └──> [Bấm "Sửa quyền" trên thành viên] ──> [Gán Role tùy chỉnh]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Tra cứu Quyền của tôi trên Workspace** | • Tại bất kỳ màn hình nào, nhấp vào menu ba chấm của dòng Workspace trong Trình duyệt Không gian $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Quyền của tôi**.<br>• **Hộp thoại Quyền của tôi** mở ra với tiêu đề: *"Quyền của tôi trên Workspace [Tên]"*.<br>• Giao diện phân loại danh mục quyền thành các nhóm trực quan (*Tất cả quyền*, *Quyền khác*), từng quyền được đánh dấu huy hiệu xanh lá: <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="14" alt="" /> **Được cấp cho tài khoản của bạn**, giúp bạn nắm rõ giới hạn thao tác của mình. |
| **2** | **Mở Trung tâm Quản lý Danh sách Role quyền** | • Mở **Hộp thoại Cài đặt Workspace** $\rightarrow$ Chuyển sang thẻ <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> **Thành viên**.<br>• Trên thanh công cụ phía trên bảng thành viên, nhấp vào nút <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **Danh sách role quyền**.<br>• Hộp thoại **Danh sách role quyền** hiển thị toàn bộ các vai trò sẵn có của hệ thống và các vai trò tùy chỉnh do bạn tự định nghĩa. |
| **3** | **Lọc và khảo sát danh mục vai trò hiện hữu** | • Hộp thoại cung cấp thanh công cụ lọc hai tầng:<br>  + **Bộ lọc Miền (Domain)**: Mặc định hiển thị *Miền: Tất cả*. Có thể nhấp chọn để lọc riêng các role liên quan đến `Workspace`, `Bảng động`, `Trợ lý AI` hoặc `Workflow`.<br>  + **Bộ lọc Hành động (Action)**: Mặc định hiển thị *Hành động: Tất cả*. Hỗ trợ lọc nhanh theo các quyền `Xem`, `Tạo mới`, `Xóa` hoặc `Quản lý`.<br>• Bảng hiển thị 7 cột thông số chi tiết: *Mã code*, *Tên vai trò*, *Phạm vi* (Workspace hay Base), *Trạng thái* (Đang hoạt động / Ngừng hoạt động), *Mô tả*, *Miền* và *Hành động*. |
| **4** | **Khởi tạo Role phân quyền mới** | • Ở góc trên bên phải hộp thoại, bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo mới role**.<br>• Biểu mẫu tạo vai trò mở ra:<br>  + **Tên role \***: Nhập tên gọi chức danh dễ hiểu (ví dụ: `Biên tập viên Nội dung Marketing`).<br>  + **Mã code \***: Nhập mã định danh nội bộ bằng chữ in hoa hoặc gạch dưới (ví dụ: `MARKETING_CONTENT_EDITOR`).<br>  + **Phạm vi \***: Chọn phạm vi áp dụng là *Workspace* (toàn bộ không gian) hoặc *Không gian làm việc (Base)*.<br>  + **Mô tả**: Nhập phạm vi trách nhiệm và đối tượng nhân sự được áp dụng vai trò này.<br>  + **Trạng thái**: Mặc định kích hoạt *Đang hoạt động*. |
| **5** | **Thiết lập danh mục Khả năng (Capabilities) cho Role** | • Trong phần **Quyền của vai trò (Capabilities)**, nhấp vào nút <img src="https://api.iconify.design/lucide:list-checks.svg?color=%23ff3333" width="16" alt="" /> **Chọn quyền**.<br>• Lưới ma trận năng lực mở ra, phân chia theo 32 Miền nghiệp vụ:<br>  + Tích chọn các quyền mong muốn (ví dụ: Miền *Bảng động* $\rightarrow$ Tích chọn `Xem`, `Tạo mới`, `Cập nhật`; Miền *Trợ lý AI* $\rightarrow$ Tích chọn `Xem`, `Thực thi`).<br>  + Số lượng quyền được chọn hiển thị thời gian thực: *"Đã chọn X quyền"*.<br>• Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Xác nhận** để ghi nhận danh sách năng lực vào cấu hình Role. |
| **6** | **Lưu vai trò mới vào hệ thống** | • Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu role**. Hệ thống lưu vai trò mới vào cơ sở dữ liệu và hiển thị thông báo nổi: *"Tạo role thành công"*, sẵn sàng để bạn phân bổ cho nhân sự. |
| **7** | **Gán Role tùy chỉnh cho thành viên cụ thể** | • Quay lại bảng danh sách thành viên ở thẻ Thành viên $\rightarrow$ Tìm nhân sự cần cấp quyền $\rightarrow$ Nhấp vào nút <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Sửa quyền** ở cuối dòng.<br>• Hộp thoại **Gán quyền thành viên** mở ra với dòng tiêu đề: *"Đang gán quyền cho: [Tên thành viên]"*.<br>• Chọn Role tùy chỉnh vừa tạo từ danh mục vai trò $\rightarrow$ Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Cập nhật quyền**.<br>• Thông báo nổi: *"Cập nhật quyền thành công"* hiển thị, nhân sự đó lập tức được cấp chính xác ma trận quyền hạn đã thiết kế. |

---

## Kiểm tra kết quả

Sau khi cấu hình và gán vai trò phân quyền, bạn có thể kiểm chứng kết quả trên giao diện:

1. **Trên Hộp thoại Danh sách Role**: Vai trò tùy chỉnh mới xuất hiện trong bảng với mã code và số lượng Capabilities tương ứng, trạng thái hiển thị nhãn xanh lá `Đang hoạt động`.
2. **Trên bảng Thành viên**: Dòng thành viên được gán hiển thị đúng tên vai trò mới, khi rê chuột vào có thể xem tóm tắt các quyền đã được cấp.
3. **Từ góc độ tài khoản của thành viên được gán**: Khi thành viên đăng nhập, các nút bấm hoặc phân hệ mà họ không được cấp quyền sẽ tự động ẩn đi hoặc hiển thị cảnh báo không có quyền truy cập, ngăn chặn hoàn toàn các hành vi thao tác trái phép.

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
| **Tra cứu danh sách Role trong Workspace** | `getScopeRoles` | `Hãy liệt kê toàn bộ danh sách vai trò (roles) hiện có trong Workspace này kèm mã code và trạng thái hoạt động.` |
| **Xem chi tiết quyền của một Role** | `getScopeRoleDetail` | `Hãy tra cứu chi tiết danh mục các Capabilities của vai trò có mã "MARKETING_CONTENT_EDITOR".` |
| **Tạo mới vai trò tùy chỉnh** | `createScopeRole` | `Hãy tạo mới một Role có tên "Biên tập viên Bảng dữ liệu", mã "DATA_TABLE_EDITOR", phạm vi "workspace", cho phép các hành động read, create, update trên miền "dynamic_table".` |
| **Cập nhật quyền cho Role** | `updateScopeRole` | `Hãy bổ sung thêm quyền "export" trên miền "dynamic_table" cho vai trò "DATA_TABLE_EDITOR".` |
| **Gán vai trò cho thành viên** | `assignScopeRoleToUser` | `Hãy gán vai trò "DATA_TABLE_EDITOR" cho thành viên có userId 104 trong Workspace này.` |
| **Kiểm tra quyền hạn của chính tôi** | `getMyScopeCapabilities` | `Hãy kiểm tra xem tài khoản của tôi hiện có quyền tạo mới Base và xuất dữ liệu trên Workspace này hay không.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Tạo role mới trên hộp thoại và bấm Lưu | Gọi `getScopeRoles` thấy xuất hiện thêm 1 bản ghi mới với đúng mã code và tên vai trò. |
| Gán role tùy chỉnh cho thành viên trên giao diện | Gọi `getWorkspaceMembers` thấy trường `roleCode` của thành viên đó khớp với role vừa gán. |
| Tắt quyền export trên vai trò của thành viên | Đăng nhập tài khoản thành viên đó và gọi `getMyScopeCapabilities` thấy quyền `dynamic_table:export` biến mất. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createScopeRole` thành công | Mở Hộp thoại Danh sách role quyền, thấy dòng vai trò mới xuất hiện ngay lập tức trong bảng. |
| Agent gọi `assignScopeRoleToUser` | Mở thẻ Thành viên trên UI, cột Vai trò của người dùng tương ứng tự động đổi sang tên vai trò mới. |
| Agent gọi `updateScopeRole` sửa năng lực | Bấm xem chi tiết quyền của vai trò trên giao diện, thấy số lượng quyền được chọn cập nhật chính xác. |
