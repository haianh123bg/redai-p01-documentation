## Tổng quan quản lý không gian Base, di chuyển tài nguyên, lịch sử sử dụng và vùng nguy hiểm

Trong cấu trúc vận hành của **RedAI**, nếu Workspace đóng vai trò là "ngôi nhà lớn" của tổ chức thì **Base (Không gian dữ liệu nhóm)** chính là các "căn phòng chuyên biệt" chứa đựng các bảng dữ liệu, luồng tự động hóa, hồ sơ dự án và công cụ nghiệp vụ của từng phòng ban. Việc quản trị toàn diện vòng đời của Base kết hợp cùng các công cụ chuyên sâu như **Tùy biến Logo & Nhận diện thương hiệu**, **Di chuyển tài nguyên (Resource Transfer)**, **Trung tâm Lịch sử sử dụng (Usage History 5 phân hệ)**, **Biến môi trường toàn cục (Environment Variables)** và **Vùng nguy hiểm (Danger Zone)** mang lại nhiều năng lực vượt trội:

- **Linh hoạt nhân bản và phục hồi không gian**: Hỗ trợ nhân bản nguyên vẹn cấu trúc Base để triển khai dự án mới trong vài giây, đồng thời cung cấp khu vực lưu trữ an toàn (Archived Bases) giúp khôi phục hoặc dọn dẹp triệt để dữ liệu cũ.
- **Tùy biến nhận diện thương hiệu & Cấu hình múi giờ chuẩn xác**: Hỗ trợ tải lên Logo Workspace chuyên nghiệp với cơ chế nén ảnh tự động, cùng cấu hình Múi giờ thống nhất cho toàn bộ công thức, bộ lọc và luồng tích hợp Webhook.
- **Di chuyển tài nguyên thông minh có phân tích trước (Preview-First Transfer)**: Cho phép chuyển giao các tài sản số giá trị cao (Agent, Bảng dữ liệu, Workflow, Kỹ năng Skill, Mẫu Prompt) giữa các Base mà không làm đứt gãy quan hệ logic, luôn có bước phân tích cảnh báo trước khi thực hiện.
- **Minh bạch tài chính & Giám sát định mức tài nguyên 5 chiều**: Cung cấp trung tâm theo dõi toàn diện Lịch sử thanh toán gói dịch vụ, nạp điểm thưởng R-Point, nhật ký tiêu hao điểm theo từng Model AI, hạn mức các gói Addon (Cloud Storage GB, Thành viên) và danh mục Combo Model AI đã kích hoạt.
- **Bảo mật và an toàn dữ liệu tuyệt đối**: Cơ chế cấu hình biến môi trường dùng chung bảo vệ các chuỗi khóa API bí mật, kết hợp quy trình xác thực hai lớp nghiêm ngặt tại Vùng nguy hiểm khi cần đóng hoặc giải thể Workspace.

---

## Các tính năng chi tiết trên giao diện

Các nghiệp vụ quản lý không gian Base, cấu hình chung, lịch sử sử dụng và vùng nguy hiểm trong Hộp thoại Cài đặt Workspace được bố trí trực quan theo sơ đồ chức năng sau:

```
[Trình duyệt Không gian] ──> [Bấm "Thêm không gian"] ──> [Tạo Base mới: Tên, Biểu tượng, Màu sắc]
          │
          ├──> [Menu ba chấm Base] ──> [Sao chép ID / Nhân bản / Lưu trữ / Rời nhóm]
          │
[Cài đặt Workspace] ─────> [Không gian đã lưu trữ] ──> [Hoàn tác khôi phục hoặc Xóa vĩnh viễn]
          │
          ├──> [Cài đặt chung] ──────────────────────> [Tải Logo lên, Đổi tên, Mô tả, Múi giờ Timezone]
          │
          ├──> [Di chuyển dữ liệu] ──────────────────> [Preview phân tích ──> Thực hiện chuyển]
          │
          ├──> [Lịch sử sử dụng] ────────────────────> [Gói dịch vụ / R-Point / Trợ lý AI / Addons / AI Models]
          │
          └──> [Vùng nguy hiểm] ─────────────────────> [Gõ lại tên Workspace để Xóa vĩnh viễn]
```

| STT | Tính năng trên UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Khởi tạo Không gian làm việc mới (Base)** | • Tại Trình duyệt Không gian làm việc, tìm đến Workspace bạn muốn bổ sung không gian $\rightarrow$ Bấm nút menu ba chấm <img src="https://api.iconify.design/lucide:ellipsis-vertical.svg?color=%23ff3333" width="16" alt="" /> $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **Thêm không gian** (hoặc bấm biểu tượng dấu cộng cạnh tên nhóm).<br>• Hộp thoại **Tạo không gian làm việc** mở ra:<br>  + **Tên không gian làm việc \***: Nhập tên định danh của cơ sở dữ liệu (ví dụ: `Quản lý Khách hàng Doanh nghiệp CRM`).<br>  + **Biểu tượng & Màu sắc**: Chọn một icon nhận diện (hình cặp tài liệu, biểu đồ, cơ sở dữ liệu) và tông màu nền đặc trưng giúp nhận diện nhanh trên danh mục.<br>• Nhấn nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu**. Base mới lập tức được khởi tạo và hiển thị trong danh mục cây thư mục của Workspace. |
| **2** | **Thao tác nhanh trên Không gian Base** | Rê chuột lên một dòng Base trong Trình duyệt Không gian $\rightarrow$ Bấm nút ba chấm <img src="https://api.iconify.design/lucide:ellipsis-vertical.svg?color=%23ff3333" width="16" alt="" /> để mở menu lệnh:<br>• <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="14" alt="" /> **Sao chép base ID**: Sao chép mã định danh UUID của Base để phục vụ cấu hình API hoặc kết nối công cụ AI.<br>• <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="14" alt="" /> **Nhân bản không gian (Duplicate)**: Tự động sao chép toàn bộ cấu trúc bảng, view và quan hệ dữ liệu sang một Base mới.<br>• <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="14" alt="" /> **Lưu trữ không gian (Archive)**: Đưa Base vào trạng thái đóng băng tạm thời, chuyển vào kho lưu trữ của Workspace.<br>• <img src="https://api.iconify.design/lucide:log-out.svg?color=%23ff3333" width="14" alt="" /> **Rời khỏi không gian nhóm**: Đối với thành viên cộng tác, cho phép hủy quyền tham gia Base mà không ảnh hưởng đến tư cách thành viên của Workspace. |
| **3** | **Quản lý Không gian đã lưu trữ (Archived Bases)** | • Mở **Hộp thoại Cài đặt Workspace** $\rightarrow$ Nhấp chuyển sang thẻ <img src="https://api.iconify.design/lucide:archive.svg?color=%23ff3333" width="16" alt="" /> **Không gian đã lưu trữ**.<br>• Bảng hiển thị danh sách các Base đã được đóng băng kèm Logo (hoặc màu đại diện), Tên Base và Mô tả.<br>• Nút <img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23ff3333" width="16" alt="" /> **Tải lại**: Nạp mới danh sách kho lưu trữ.<br>• **Hoàn tác khôi phục**: Bấm nút màu xanh <img src="https://api.iconify.design/lucide:undo.svg?color=%23ff3333" width="16" alt="" /> **Khôi phục** $\rightarrow$ Base lập tức quay trở lại danh sách hoạt động bình thường.<br>• **Xóa vĩnh viễn**: Bấm nút đỏ <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **Xóa** $\rightarrow$ Hộp thoại xác nhận yêu cầu tích chọn cam kết: *"Tôi hiểu rằng base đã lưu trữ sẽ bị xóa vĩnh viễn và không thể khôi phục"* $\rightarrow$ Bấm **Xóa vĩnh viễn**. Toàn bộ dữ liệu của Base bị xóa sạch khỏi hệ thống. |
| **4** | **Cài đặt chung: Tải Logo & Cấu hình Múi giờ** | Trong Hộp thoại Cài đặt Workspace, chọn thẻ <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **Chung**:<br>• **Khối Logo Workspace**:<br>  + Khung xem trước logo hiện tại của Workspace.<br>  + Bấm nút <img src="https://api.iconify.design/lucide:upload.svg?color=%23ff3333" width="16" alt="" /> **Chọn logo** $\rightarrow$ Mở hộp thoại chọn tệp hình ảnh từ máy tính (chỉ nhận file ảnh hợp lệ `image/*`). Tên tệp vừa chọn hiển thị ngay bên dưới.<br>  + Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Tải logo lên** $\rightarrow$ Hệ thống tự động nén tối ưu dung lượng ảnh và tải lên kho lưu trữ đám mây an toàn, cập nhật logo mới cho toàn bộ giao diện.<br>• **Khối Thông tin Workspace**:<br>  + **Tên workspace \***: Chỉnh sửa tên hiển thị của Workspace khi có sự thay đổi về thương hiệu.<br>  + **Mô tả**: Cập nhật mô tả hoạt động nội bộ.<br>  + **Múi giờ \***: Nhấp chọn múi giờ chuẩn của tổ chức từ danh sách tìm kiếm (ví dụ: `Asia/Ho_Chi_Minh (GMT+7)`). Chú thích gợi ý: *"Dùng cho công thức ngày giờ, bộ lọc và payload webhook của workspace."*<br>  + Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **Lưu** để áp dụng thay đổi. |
| **5** | **Di chuyển tài nguyên giữa các Base (Resource Transfer)** | > [!IMPORTANT]<br>> Tính năng này chỉ dành riêng cho Chủ sở hữu Workspace để đảm bảo toàn vẹn dữ liệu.<br>• Trong Cài đặt Workspace, chọn thẻ <img src="https://api.iconify.design/lucide:repeat.svg?color=%23ff3333" width="16" alt="" /> **Di chuyển dữ liệu**:<br>  + **Loại dữ liệu \***: Chọn nhóm tài nguyên cần chuyển đổi (*Agent*, *Dự án Project*, *Bảng Table*, *Workflow*, *Skill*, hoặc *Prompt*).<br>  + **Base nguồn & Ô tìm kiếm**: Lọc dữ liệu theo từng Base hoặc xem tất cả, gõ từ khóa tìm kiếm tài nguyên.<br>  + **Base đích \***: Chọn cơ sở dữ liệu sẽ tiếp nhận tài nguyên.<br>  + **Danh sách dữ liệu**: Tích chọn đối tượng cụ thể cần chuyển.<br>• **Bước 1 — Phân tích trước khi chuyển (Preview)**: Bấm nút <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **Phân tích dữ liệu**. Hệ thống tự động quét đồ thị quan hệ, ước tính số lượng thực thể liên đới và liệt kê cảnh báo xung đột nếu có.<br>• **Bước 2 — Xác nhận chuyển dữ liệu**: Sau khi xem kết quả phân tích đạt yêu cầu, bấm nút <img src="https://api.iconify.design/lucide:arrow-right-circle.svg?color=%23ff3333" width="16" alt="" /> **Thực hiện chuyển** $\rightarrow$ Hộp thoại xác nhận yêu cầu tích chọn cam kết an toàn $\rightarrow$ Bấm **Xác nhận chuyển**. |
| **6** | **Khai thác Trung tâm Lịch sử sử dụng (Usage History)** | Trong Hộp thoại Cài đặt Workspace, chọn thẻ <img src="https://api.iconify.design/lucide:activity.svg?color=%23ff3333" width="16" alt="" /> **Lịch sử sử dụng**. Trung tâm tích hợp 5 thẻ con chuyên sâu:<br>• **Thẻ con 1 — Gói dịch vụ**: Xem bảng lịch sử thanh toán mua gói cước Workspace: Cột `ID` giao dịch (`#ID`), `Số tiền` (`amount` kèm loại tiền tệ), `Trạng thái` (gắn nhãn màu: Hoàn tất `COMPLETED`, Đang chờ `PENDING`, Thất bại `FAILED`, Đã hủy `CANCELLED`, Xác nhận `CONFIRMED`), `Phương thức thanh toán` (Chuyển khoản ngân hàng, Quà tặng thủ công, Mã giảm giá, Thẻ tín dụng, Ví điện tử, R-Point, Admin cấp...), `Ngày tạo`. Hỗ trợ ô tìm kiếm nhanh, lọc ẩn/hiện cột, nút tải lại và phân trang.<br>• **Thẻ con 2 — R-Point**: Nhật ký biến động nạp điểm thưởng R-Point. Bảng hiển thị: Mã `#ID`, `R-Point` (số điểm nạp cộng dồn `+X R-Point` màu xanh dương đậm), `Số tiền` nạp (VND), `Trạng thái` (Xác nhận, Đang chờ, Thất bại, Đã hoàn tiền), `Ngày tạo`. Có tìm kiếm và tải lại.<br>• **Thẻ con 3 — Trợ lý AI**: Minh bạch chi phí tiêu hao tài nguyên khi người dùng tương tác với AI: Cột `Trợ lý AI` (tên Agent thực thi), `Model` (mã mô hình trí tuệ nhân tạo như `claude-3-5-sonnet`, `gemini-1.5-pro`, `gpt-4o`...), `R-Point` (số điểm tiêu hao `-X điểm` màu đỏ đậm), `Ngày tạo`. Hỗ trợ tìm kiếm theo tên trợ lý.<br>• **Thẻ con 4 — Addons**: Quản trị định mức và tiến độ tiêu thụ các gói tài nguyên mở rộng. Bảng hiển thị: `Tiện ích` (tên Addon đa ngôn ngữ), `Mức sử dụng` (thanh tiến trình trực quan hiển thị %, chuyển màu đỏ khi vượt 90%; tự động quy đổi định lượng thông minh: Dung lượng lưu trữ Cloud Storage chuyển đổi từ Bytes sang `GB`, Hạn mức Thành viên theo người, theo Tháng, hoặc nhãn "Không giới hạn"), `Trạng thái` (`ACTIVE`, `EXPIRED`, `SUSPENDED`), `Kỳ sử dụng` (từ ngày đến ngày).<br>• **Thẻ con 5 — AI Models**: Danh mục các gói Combo Mô hình AI được cấp phát: Cột `Tên gói Model`, `Vai trò` (nhãn `NORMAL` hoặc vai trò đặc biệt), `Số lượng model` trong combo, `Định giá` (bảng giá niêm yết và giá bán ưu đãi), `Trạng thái` (Đang hoạt động hoặc Ngừng hoạt động). |
| **7** | **Quản trị Biến môi trường Không gian làm việc** | • Tại khu vực Cài đặt nâng cao hoặc thanh công cụ Workspace, nhấp mở **Hộp thoại Quản lý biến môi trường** (biểu tượng dấu ngoặc nhọn <img src="https://api.iconify.design/lucide:braces.svg?color=%23ff3333" width="16" alt="" />).<br>• Giao diện hiển thị danh sách các cặp khóa-giá trị (`Key` - `Value`) dùng chung cho toàn bộ các MiniApp, Trợ lý AI và Luồng Workflow trong Workspace.<br>• Bấm **Thêm biến mới** $\rightarrow$ Điền tên biến (ví dụ: `APP_API_BASE_URL`, `WEBHOOK_SECRET`) $\rightarrow$ Điền giá trị $\rightarrow$ Bấm **Lưu**. Biến môi trường được lưu trữ an toàn, hỗ trợ che giấu giá trị nhạy cảm. |
| **8** | **Vùng nguy hiểm — Xóa vĩnh viễn Không gian làm việc** | > [!CAUTION]<br>> **HÀNH ĐỘNG NÀY KHÔNG THỂ HOÀN TÁC!** Khi xóa Workspace, toàn bộ cơ sở dữ liệu Base, bảng, thành viên, trợ lý AI và lịch sử giao dịch sẽ bị xóa sạch hoàn toàn khỏi máy chủ.<br>• Chọn thẻ cuối cùng <img src="https://api.iconify.design/lucide:alert-triangle.svg?color=%23ff3333" width="16" alt="" /> **Vùng nguy hiểm** trong Cài đặt Workspace.<br>• Nhấp vào nút màu đỏ <img src="https://api.iconify.design/lucide:trash-2.svg?color=%23ff3333" width="16" alt="" /> **Xóa không gian làm việc**.<br>• Hộp thoại cảnh báo bảo mật cấp cao xuất hiện, hiển thị yêu cầu: *"Nhập chính xác tên workspace [Tên Workspace] để xác nhận xóa"*.<br>• Nhập đúng từng ký tự tên của Workspace vào ô xác nhận $\rightarrow$ Nút màu đỏ **Tôi hiểu, xóa ngay** sẽ sáng lên.<br>• Nhấp vào nút **Tôi hiểu, xóa ngay**. Hệ thống tiến hành thu hồi tài nguyên, đăng xuất người dùng khỏi Workspace và xóa bỏ vĩnh viễn không gian làm việc. |

---

## Kiểm tra kết quả

Sau khi thao tác với Không gian Base, di chuyển tài nguyên, lịch sử sử dụng và cấu hình hệ thống:

1. **Sau khi tạo Base mới**: Base mới xuất hiện ngay dưới cây phân cấp của Workspace trong Trình duyệt Không gian, nhấp vào sẽ mở giao diện thiết kế bảng dữ liệu của Base đó.
2. **Sau khi tải Logo mới**: Logo Workspace lập tức hiển thị trên thanh điều hướng chính, Trình duyệt Không gian và khung xem trước của Cài đặt chung.
3. **Sau khi di chuyển tài nguyên**: Mở Base đích, đối tượng (Agent, Workflow, Bảng) xuất hiện đầy đủ trong danh mục quản lý tương ứng, cấu hình phụ thuộc hoạt động trơn tru.
4. **Sau khi tra cứu Lịch sử sử dụng**: Nắm bắt chính xác số điểm R-Point đã tiêu thụ cho từng lượt gọi Trợ lý AI, dung lượng Cloud Storage còn lại và tình trạng gia hạn gói cước.
5. **Sau khi cập nhật Múi giờ**: Mở bảng dữ liệu có trường ngày giờ, giá trị giờ hiển thị theo đúng múi giờ đã đặt thay cho múi giờ UTC mặc định.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Workbase & Workspace Management` |
| **Mã định danh Kỹ năng (Skill ID)** | `4fa87112-9b2c-46ea-8822-1d187e59b201` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Workbase` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `71c42938-16e5-4d29-9e87-251f9a84b102` |
| **Quyền tài khoản yêu cầu** | Quản trị viên (Admin) hoặc Chủ sở hữu Workspace (Workspace Owner) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tạo mới một Base trong Workspace** | `createWorkspaceBase` | `Hãy tạo mới một cơ sở dữ liệu Base có tên là "Kho Dữ Liệu Marketing", icon "database", màu "#6366F1" trong Workspace hiện tại.` |
| **Nhân bản một Base hiện có** | `duplicateWorkspaceBase` | `Hãy nhân bản toàn bộ Base có ID "b1c2d3e4-f5a6-7b8c-9d0e-1f2a3b4c5d6e" thành một Base mới có tên là "Kho Dữ Liệu Marketing - Bản Sao".` |
| **Lưu trữ một Base** | `archiveWorkspaceBase` | `Dự án năm ngoái đã hoàn thành, hãy đưa Base có ID "c4d11ee6-7114-46b8-9216-dc1c6ea766da" vào trạng thái lưu trữ.` |
| **Khôi phục Base đã lưu trữ** | `restoreArchivedBase` | `Hãy khôi phục lại Base có ID "c4d11ee6-7114-46b8-9216-dc1c6ea766da" từ kho lưu trữ về trạng thái hoạt động bình thường.` |
| **Chạy phân tích di chuyển tài nguyên** | `previewResourceTransfer` | `Hãy phân tích việc di chuyển Workflow có ID "wf_998124" từ Base nguồn sang Base đích "b2c3d4e5-..." xem có những tài nguyên phụ thuộc nào.` |
| **Thực hiện di chuyển tài nguyên** | `executeResourceTransfer` | `Sau khi phân tích không có cảnh báo nghiêm trọng, hãy tiến hành di chuyển Workflow sang Base đích đã chọn.` |
| **Cập nhật Múi giờ Workspace** | `updateWorkspaceSettings` | `Hãy cập nhật múi giờ của Workspace thành "Asia/Ho_Chi_Minh" và bổ sung mô tả hoạt động mới.` |
| **Cập nhật Logo Workspace** | `uploadWorkspaceLogo` | `Hãy cập nhật logo mới cho Workspace hiện tại từ đường dẫn ảnh nhận diện thương hiệu đã cung cấp.` |
| **Tra cứu Lịch sử thanh toán gói dịch vụ** | `getWorkspaceSubscriptionHistory` | `Hãy kiểm tra lịch sử thanh toán các gói dịch vụ của Workspace trong 30 ngày gần nhất.` |
| **Tra cứu Nhật ký tiêu hao điểm Trợ lý AI** | `getWorkspaceAssistantSpending` | `Hãy trích xuất danh sách các lượt tiêu hao điểm R-Point khi gọi Trợ lý AI trong tuần qua kèm Model đã sử dụng.` |
| **Kiểm tra định mức Addons và Dung lượng** | `getWorkspaceAddonUsages` | `Hãy kiểm tra mức độ tiêu thụ dung lượng Cloud Storage và hạn mức thành viên hiện tại của Workspace.` |
| **Thiết lập biến môi trường Workspace** | `setWorkspaceEnvironmentVariable` | `Hãy cấu hình biến môi trường toàn cục "CRM_GATEWAY_URL" với giá trị "https://api.crm.internal/v2" cho Workspace này.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Bấm tạo Base mới trên giao diện | Gọi `getWorkspaceBases` thấy Base mới xuất hiện với đúng tên, icon và màu sắc. |
| Bấm Lưu trữ một Base trên giao diện | Gọi `getArchivedBases` thấy Base đó xuất hiện trong danh sách lưu trữ với trạng thái `ARCHIVED`. |
| Cập nhật múi giờ Workspace sang GMT+7 | Gọi `getWorkspaceDetail` thấy trường `timezone` trả về `"Asia/Ho_Chi_Minh"`. |
| Tải ảnh Logo Workspace mới trên giao diện | Gọi `getWorkspaceDetail` thấy trường `logo` trả về URL ảnh S3 mới cập nhật. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `createWorkspaceBase` thành công | Mở Trình duyệt Không gian, thấy dòng Base mới xuất hiện ngay dưới tên Workspace. |
| Agent gọi `executeResourceTransfer` | Mở Base đích trên giao diện, thấy tài nguyên được chuyển xuất hiện đầy đủ trong danh mục. |
| Agent gọi `restoreArchivedBase` | Tải lại trang, Base vừa được khôi phục biến mất khỏi thẻ Lưu trữ và quay lại danh sách hoạt động. |
| Agent gọi `uploadWorkspaceLogo` | Tải lại trang, biểu tượng logo Workspace mới lập tức hiển thị trên thanh tiêu đề và Cài đặt chung. |
