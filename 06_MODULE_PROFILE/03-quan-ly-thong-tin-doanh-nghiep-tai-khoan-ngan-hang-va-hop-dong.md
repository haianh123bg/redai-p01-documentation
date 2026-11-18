## Tổng quan hồ sơ doanh nghiệp, tài khoản ngân hàng thụ hưởng và hợp đồng số

Đối với các tổ chức, công ty và đối tác kinh doanh vận hành trên **User Workspace** của nền tảng **RedAI**, việc quản lý thông tin pháp nhân doanh nghiệp, thiết lập tài khoản ngân hàng thụ hưởng và ký kết hợp đồng số là những nghiệp vụ pháp lý và thanh toán đặc biệt quan trọng. Hệ sinh thái này giúp doanh nghiệp:

1. **Chuẩn hóa thông tin pháp lý**: Nâng cấp tài khoản từ Cá nhân (`INDIVIDUAL`) lên Doanh nghiệp (`BUSINESS`), lưu trữ hồ sơ công ty, mã số thuế (MST), người đại diện pháp luật phục vụ xuất hóa đơn VAT và ký hợp đồng thương mại điện tử.
2. **Thiết lập tài khoản thanh toán và nhận hoa hồng**: Liên kết tài khoản ngân hàng thụ hưởng tại Việt Nam qua hệ thống mạng lưới liên ngân hàng NAPAS và VietQR, chuẩn hóa tên chủ tài khoản in hoa không dấu để đảm bảo dòng tiền đối soát minh bạch, chuẩn xác.
3. **Quản trị hợp đồng số (Digital Contracts)**: Tiếp cận trực tiếp và quản lý hai văn kiện pháp lý trọng tâm: *Hợp đồng nguyên tắc dịch vụ* và *Hợp đồng đối tác kinh doanh Affiliate*, hỗ trợ ký số điện tử và tải file hợp đồng đã ký về máy tính.

> [!NOTE]
> Nhóm tính năng Thông tin doanh nghiệp, Tài khoản ngân hàng và Hợp đồng số chỉ hiển thị tại **Không gian làm việc người dùng (User Workspace)** và tự động ẩn khi làm việc tại Không gian làm việc hệ thống (`System Workspace`).

---

## Các bước thực hiện chi tiết trên giao diện

Quy trình quản lý hồ sơ pháp nhân, ngân hàng và hợp đồng số được tiến hành theo các bước sau:

```
[Thẻ Thông tin doanh nghiệp] ──(Tài khoản Cá nhân)──> [Form Nâng cấp tài khoản Doanh nghiệp]
             │                                                          │
             │                                                          ▼
             └──(Đã là Doanh nghiệp)──> [Cập nhật MST, Địa chỉ, Người đại diện]
                                                        │
[Thẻ Thông tin ngân hàng] ────────────> [Chọn Ngân hàng NAPAS/VietQR + Số TK + Tên chủ TK]
                                                        │
[Thẻ Quản lý hợp đồng] ───────────────> [Mở Hợp đồng nguyên tắc & Hợp đồng Affiliate]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Nâng cấp tài khoản lên Doanh nghiệp** | • Nếu loại tài khoản của bạn hiện là *Cá nhân*, khi nhấp mở thẻ <img src="https://api.iconify.design/lucide:building.svg?color=%23ff3333" width="16" alt="" /> **Thông tin doanh nghiệp**, hệ thống sẽ hiển thị trực tiếp biểu mẫu **Nâng cấp tài khoản Doanh nghiệp**:<br>  + **Tên doanh nghiệp \***: Nhập tên công ty theo giấy phép kinh doanh (ví dụ: `Công ty TNHH Giải Pháp Công Nghệ RedAI`).<br>  + **Email doanh nghiệp \***: Nhập hòm thư công vụ của công ty.<br>  + **Số điện thoại doanh nghiệp \***: Nhập số hotline hoặc số liên hệ văn phòng.<br>  + **Mã số thuế \***: Nhập mã số doanh nghiệp hoặc mã số thuế do Cục thuế cấp.<br>  + **Tên người đại diện \***: Nhập họ tên người đại diện pháp luật ghi trên ĐKKD.<br>  + **Vị trí/Chức vụ người đại diện \***: Nhập chức danh (ví dụ: `Giám đốc`, `Tổng Giám Đốc`, `Chủ tịch HĐQT`).<br>  + **Địa chỉ doanh nghiệp \***: Nhập địa chỉ trụ sở chính đăng ký kinh doanh.<br>• Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu** $\rightarrow$ Hệ thống cập nhật loại tài khoản sang **Doanh nghiệp**, huy hiệu loại tài khoản trên Profile Header chuyển từ màu xám sang huy hiệu xanh dương `Tài khoản doanh nghiệp`. |
| **2** | **Chỉnh sửa thông tin Doanh nghiệp** | Khi tài khoản đã là Doanh nghiệp, thẻ Thông tin doanh nghiệp chuyển sang chế độ quản lý thông tin chính thức:<br>• Cho phép bạn cập nhật lại Tên công ty, Mã số thuế, Người đại diện, Chức vụ và Địa chỉ văn phòng khi có sự thay đổi về pháp nhân.<br>• Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu** để hệ thống ghi nhận thông tin pháp nhân mới. |
| **3** | **Cấu hình Tài khoản Ngân hàng thụ hưởng** | Nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:credit-card.svg?color=%23ff3333" width="16" alt="" /> **Thông tin ngân hàng**:<br>• **Chọn Ngân hàng \***: Sử dụng ô tìm kiếm ngân hàng thông minh:<br>  + Gõ tên ngân hàng bằng tiếng Việt có dấu hoặc không dấu (ví dụ: gõ `vcb`, `vietcombank`, `ngoai thuong`, `techcombank`, `acb`).<br>  + Hệ thống tự động chuẩn hóa từ ngữ, tự động nhận diện từ viết tắt (`TMCP`, `NHTMCP`, `NH` $\rightarrow$ `ngân hàng`) giúp bạn tìm ra ngay ngân hàng chuẩn xác trong danh mục ngân hàng Việt Nam.<br>• **Số tài khoản ngân hàng \***: Nhập chính xác dãy số tài khoản của bạn hoặc của công ty.<br>• **Tên chủ tài khoản \***: Nhập họ tên người thụ hưởng (hệ thống tự động chuẩn hóa sang dạng **chữ in hoa không dấu** theo đúng quy chuẩn liên ngân hàng, ví dụ: `NGUYEN VAN AN`).<br>• **Chi nhánh ngân hàng**: Nhập tên chi nhánh mở tài khoản (ví dụ: `Chi nhánh Đông Sài Gòn`). |
| **4** | **Lưu thông tin ngân hàng** | Ở chân thẻ Thông tin ngân hàng, bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu**. Hệ thống ghi nhận tài khoản ngân hàng thụ hưởng, sẵn sàng cho việc nhận tiền thanh toán hoa hồng Affiliate hoặc hoàn tiền tự động. |
| **5** | **Xem và quản lý Hợp đồng số** | Nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Quản lý hợp đồng**. Giao diện hiển thị 2 khối tài liệu pháp lý chuyên biệt dưới dạng thẻ điều hướng:<br>• **1. Hợp đồng nguyên tắc** (Icon khiên bảo vệ <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" />): Bấm vào thẻ để chuyển đến trang `/contract/principle`. Đây là hợp đồng dịch vụ cơ bản xác lập quyền và nghĩa vụ sử dụng nền tảng giữa bạn và RedAI.<br>• **2. Hợp đồng Affiliate** (Icon đối tác <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" />): Bấm vào thẻ để chuyển đến trang `/contract-affiliate`. Đây là văn kiện thỏa thuận hợp tác phân phối dịch vụ, cơ chế chiết khấu và chi trả hoa hồng kinh doanh. |
| **6** | **Ký hợp đồng và Tải file PDF** | Khi truy cập vào từng trang hợp đồng chi tiết:<br>• Hệ thống hiển thị toàn bộ nội dung văn bản điều khoản pháp lý.<br>• Kéo xuống phần chữ ký bên dưới: Bạn có thể thực hiện ký hợp đồng bằng cách vẽ chữ ký trực tiếp trên màn hình cảm ứng / chuột, hoặc tải lên ảnh chữ ký cá nhân.<br>• Sau khi hoàn tất ký số, bấm nút <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **Tải tệp hợp đồng (PDF)** để lưu trữ bản hợp đồng có đóng dấu chữ ký điện tử về máy tính. |

---

## Kiểm tra kết quả

Sau khi thiết lập doanh nghiệp, tài khoản ngân hàng và hợp đồng, bạn có thể kiểm chứng kết quả trên giao diện:

1. **Sau khi nâng cấp Doanh nghiệp**: Huy hiệu loại tài khoản trên Profile Header hiển thị `Tài khoản doanh nghiệp` màu xanh dương, mở thẻ Thông tin doanh nghiệp hiển thị đầy đủ tên công ty và mã số thuế đã lưu.
2. **Sau khi lưu thông tin ngân hàng**: Mở lại thẻ Thông tin ngân hàng, thông tin Tên ngân hàng, Số tài khoản, Tên chủ tài khoản in hoa và Chi nhánh được điền đầy đủ và giữ nguyên trạng thái.
3. **Trên trang Hợp đồng số**: Sau khi ký xong, dòng trạng thái hợp đồng hiển thị nhãn màu xanh lá `ĐÃ KÝ` kèm thời điểm ký chính xác, nút tải file PDF hoạt động bình thường.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tra cứu thông tin doanh nghiệp, đối soát tài khoản ngân hàng thụ hưởng hoặc hỗ trợ cập nhật hồ sơ pháp nhân, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - User Profile & Account` |
| **Mã định danh Kỹ năng (Skill ID)** | `c8319e04-7a1b-4f92-91ef-8d5421ac0721` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - User & Account` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `387d45d1-3e2a-4ec5-9572-218d70618d5c` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Tra cứu thông tin doanh nghiệp** | `getBusinessInfo` | `Hãy kiểm tra xem tài khoản của tôi đã đăng ký thông tin doanh nghiệp chưa, nếu có thì mã số thuế và người đại diện là ai.` |
| **Nâng cấp tài khoản doanh nghiệp** | `upgradeToBusinessAccount` | `Hãy hỗ trợ tôi gửi thông tin nâng cấp tài khoản doanh nghiệp với Tên công ty: "Công ty Cổ phần Công nghệ ABC", MST: "0316889988", Đại diện: "Trần Minh Đức".` |
| **Cập nhật địa chỉ doanh nghiệp** | `updateBusinessInfo` | `Hãy cập nhật địa chỉ trụ sở doanh nghiệp của tôi thành "Tầng 12, Tòa nhà Bitexco, Quận 1, TP.HCM".` |
| **Tra cứu danh sách ngân hàng Việt Nam** | `getBankList` | `Hãy tra cứu mã ngân hàng (bankCode) và tên đầy đủ của Ngân hàng TMCP Ngoại thương Việt Nam (Vietcombank) trong hệ thống.` |
| **Tra cứu thông tin ngân hàng đã lưu** | `getBankInfo` | `Hãy kiểm tra tài khoản ngân hàng thụ hưởng hiện tại của tôi xem đã cấu hình đúng số tài khoản và tên chủ tài khoản chưa.` |
| **Cập nhật tài khoản ngân hàng thụ hưởng** | `updateBankInfo` | `Hãy cập nhật thông tin ngân hàng thụ hưởng của tôi: Ngân hàng Quân Đội (MBBank - MB), Số tài khoản "0988776655", Tên chủ tài khoản "NGUYEN VAN AN", Chi nhánh "Sài Gòn".` |
| **Kiểm tra trạng thái hợp đồng số** | `getRuleContractStatus` | `Hãy kiểm tra xem tài khoản của tôi đã hoàn tất ký Hợp đồng nguyên tắc và Hợp đồng Affiliate chưa.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Điền form nâng cấp doanh nghiệp và bấm Lưu | Gọi `getBusinessInfo` thấy các trường `businessName`, `taxCode`, `representativeName` trả về đầy đủ. |
| Chọn ngân hàng, nhập số tài khoản và bấm Lưu | Gọi `getBankInfo` thấy `bankCode` và `accountNumber` khớp hoàn toàn với dữ liệu vừa nhập. |
| Ký hợp đồng số thành công trên trang hợp đồng | Gọi `getRuleContractStatus` thấy trạng thái hợp đồng chuyển sang `SIGNED` hoặc `ACTIVE`. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `upgradeToBusinessAccount` thành công | F5 trang Profile, thẻ Thông tin doanh nghiệp tự động chuyển sang giao diện quản trị doanh nghiệp chính thức. |
| Agent gọi `updateBankInfo` cập nhật tài khoản | Mở thẻ Thông tin ngân hàng trên giao diện, thấy thông tin ngân hàng và số tài khoản mới xuất hiện chuẩn xác. |
