## Chọn loại bài

| Loại | Dùng khi | Cách tổ chức |
| --- | --- | --- |
| **Loại A — Hướng dẫn một quy trình** | Các bước phụ thuộc nhau và cùng dẫn đến một kết quả cuối | Chia theo từng giai đoạn thực hiện |
| **Loại B — Hướng dẫn nhiều tính năng** | Các thao tác tương đối độc lập trên cùng màn hình hoặc đối tượng | Chia theo từng tính năng |

- Chọn **Loại A** cho các bài như tạo lịch, cấu hình Agent hoặc kết nối dịch vụ.
- Chọn **Loại B** cho các bài như quản lý Media, File, URL hoặc danh sách tài nguyên.
- Nếu một tính năng trong bài Loại B có quy trình dài hoặc nhiều nhánh, tách thành một bài Loại A và liên kết từ bài tổng.

### Cách phân loại từ tài liệu nguồn

| Dấu hiệu trong tài liệu nguồn | Chọn loại | Cách chuẩn hóa |
| --- | --- | --- |
| Các bước phụ thuộc nhau để tạo, kết nối, cấu hình, phát hành hoặc chuyển đổi một đối tượng | **Loại A** | Giữ một kết quả cuối; chia theo giai đoạn hoặc phương án thực hiện |
| Cùng một mục tiêu nhưng có nhiều cách thực hiện, như thủ công, bằng AI hoặc qua Agent | **Loại A** | Đặt mỗi cách dưới một H3/H4; nêu điều kiện chọn cách trước các bước |
| Tìm kiếm, lọc, xem, sửa, nhân bản, liên kết, Import, Export và xóa trên cùng một nhóm đối tượng | **Loại B** | Nhóm theo tính năng và sắp xếp theo luồng sử dụng |
| Có thanh công cụ, thao tác trên thẻ và thao tác hàng loạt | **Loại B** | Giới thiệu giao diện một lần, sau đó hướng dẫn từng thao tác mà không lặp đường dẫn |
| Một tính năng trong bài quản lý phải đi qua module khác và có nhiều bước riêng | **Loại A riêng** hoặc mục tóm tắt có liên kết | Không chép toàn bộ quy trình liên module vào bài Loại B nếu làm loãng chủ đề |

Không phân loại chỉ dựa vào số lượng H2. Một bài có nhiều phương án vẫn là Loại A nếu các phương án cùng dẫn đến một kết quả; một bài có nhiều quy trình ngắn, độc lập vẫn là Loại B.

## Phần chung

```markdown
## Mở khu vực [tên khu vực]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Mở module hoặc màn hình]. |
| 2 | [Chọn tab/menu/đối tượng]. [Nêu dấu hiệu xác nhận nếu cần]. |

```

## Outline Loại A — Hướng dẫn một quy trình

```markdown
## Mở khu vực [tên khu vực]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Mở module hoặc màn hình]. |
| 2 | [Chọn tab/menu/đối tượng]. |

## Các bước thực hiện

### Chọn phương án thực hiện

| Phương án | Dùng khi | Điều kiện |
| --- | --- | --- |
| [Phương án 1] | [Tình huống phù hợp] | [Quyền, phạm vi hoặc tài nguyên cần có] |
| [Phương án 2] | [Tình huống phù hợp] | [Quyền, phạm vi hoặc tài nguyên cần có] |

> Chỉ giữ bảng này khi có từ hai phương án và người dùng cần tiêu chí để lựa chọn.

### [Giai đoạn 1 — động từ + kết quả trung gian]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Thao tác]. |
| 2 | [Thao tác]. [Nêu kết quả cần thấy nếu cần]. |

### [Giai đoạn 2 — động từ + kết quả trung gian]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Thao tác]. |

## Kiểm tra kết quả

[Nêu dấu hiệu ngắn giúp xác nhận đối tượng đã được tạo, kết nối, cập nhật hoặc phát hành đúng. Bỏ mục này nếu kết quả đã rõ ngay trong bước cuối.]

```

Chỉ chia thành nhiều H3 khi quy trình có các giai đoạn rõ ràng. Với quy trình ngắn, dùng một bảng bước duy nhất.

Khi một quy trình có nhiều cách thực hiện:

- Dùng H3 cho từng phương án độc lập như **Tạo thủ công**, **Tạo bằng AI** hoặc **Tạo qua Agent**.
- Dùng H4 cho biến thể trong cùng một phương án, như thực hiện trong ứng dụng hoặc qua kênh bên ngoài.
- Đặt điều kiện về quyền, Workspace/Base, kênh hoặc tài nguyên trước bảng bước liên quan.
- Không gộp nhiều phương án vào một bảng nếu các bước và điều kiện khác nhau đáng kể.

## Outline Loại B — Hướng dẫn nhiều tính năng

```markdown
## Mở khu vực quản lý

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Mở module hoặc màn hình]. |
| 2 | [Chọn tab/menu/đối tượng]. |

## Các tính năng

### Tìm, lọc và nhận biết đối tượng

| Khu vực hoặc chức năng | Cách sử dụng |
| --- | --- |
| [Tab/bộ lọc/thanh tìm kiếm] | [Cách dùng và phạm vi dữ liệu được hiển thị] |

> Chỉ giữ mục định hướng này khi giao diện có nhiều tab, loại đối tượng, thanh công cụ hoặc phạm vi dữ liệu dễ nhầm.

### [Động từ + đối tượng]

[Một câu nêu tính năng dùng để làm gì hoặc điểm khác biệt cần biết. Bỏ nếu tên mục đã đủ rõ.]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Thao tác]. |
| 2 | [Thao tác]. [Nêu kết quả cần thấy nếu cần]. |

> **Lưu ý:** [Điều kiện hoặc cách chọn dễ nhầm.]

### [Tính năng tiếp theo]

| Bước | Cách thực hiện |
| --- | --- |
| 1 | [Thao tác]. |

> **Cảnh báo:** [Rủi ro hoặc phạm vi ảnh hưởng, đặt trước bước xác nhận nguy hiểm.]

```

## Cách tổ chức bài

- Không viết H1 trong nội dung file; tên bài được quản lý bằng tên file hoặc hệ thống xuất bản.
- Bắt đầu nội dung trực tiếp bằng H2.
- Dùng H2 **Mở khu vực...** một lần, không lặp đường dẫn truy cập trong từng tính năng.
- Dùng H2 **Các tính năng** và H3 cho từng thao tác độc lập như tạo, thêm, xem, sửa, RAG lại, tải xuống hoặc xóa.
- Với Loại A, dùng H2 **Các bước thực hiện** và H3 cho từng giai đoạn.
- Với Loại B, dùng H2 **Các tính năng** và H3 cho từng thao tác độc lập.
- Dùng H4 cho biến thể cùng mục tiêu, chẳng hạn thêm thủ công hoặc import từ file.
- Sắp xếp nội dung theo luồng: mở khu vực → tạo/thêm → xem/tìm → sửa/xử lý → tải/chia sẻ → xóa.
- Nếu một tính năng dài hoặc có nhiều nhánh riêng, tách thành bài độc lập thay vì làm bài tổng quá dài.
- Với bài quản lý, có thể đặt một mục **Thanh công cụ và bộ lọc** hoặc **Định hướng giao diện** trước các tính năng; mục này chỉ giải thích nút và phạm vi, không thay thế các bước thao tác.
- Tách rõ ba hành vi: **xóa đối tượng**, **xóa phiên bản/bản chụp** và **gỡ liên kết tài nguyên**. Mỗi hành vi phải nêu đúng phạm vi ảnh hưởng.
- Với Snapshot, phiên bản hoặc gói dữ liệu, nêu rõ thao tác tạo mới, ghi đè hay giữ nguyên đối tượng nguồn.

## Chuẩn viết bước thao tác

- Dùng bảng hai cột **Bước** và **Cách thực hiện** khi có từ hai bước trở lên.
- Mỗi bước bắt đầu bằng động từ và dùng đúng tên nút, tab, trường hoặc menu trên giao diện; in đậm các nhãn này.
- Gộp các thao tác liên tiếp phục vụ cùng một kết quả vào một bước; không chia nhỏ theo từng cú nhấp chuột.
- Chỉ nêu trạng thái hoặc kết quả sau bước khi người dùng cần nó để xác nhận đã làm đúng.
- Thao tác một bước đơn giản nên viết thành câu, không cần tạo bảng.
- Khi nhiều tính năng cùng bắt đầu bằng một thao tác như mở menu ba chấm hoặc chọn nhiều mục, viết thao tác chung ở dòng đầu tiên của bảng. Các dòng tính năng phía sau chỉ bắt đầu từ lựa chọn riêng, không lặp lại bước chung.

### Mẫu bảng có thao tác chung

Dùng mẫu này khi nhiều chức năng nằm trong cùng một menu hoặc cùng xuất hiện sau một thao tác chọn:

```markdown
| Tính năng | Cách thực hiện |
| --- | --- |
| **Mở menu thao tác** | Tại đối tượng cần quản lý, chọn menu ba chấm trong cột **Thao tác**. Menu hiển thị các chức năng [liệt kê chức năng]. |
| **[Tính năng 1]** | Chọn **[tên chức năng]**, sau đó [thao tác riêng nếu có]. |
| **[Tính năng 2]** | Chọn **[tên chức năng]**, sau đó [thao tác riêng nếu có]. |
```

Với thao tác hàng loạt, dùng dòng đầu để hướng dẫn chọn các mục và nêu các chức năng xuất hiện trên thanh công cụ:

```markdown
| Tính năng | Cách thực hiện |
| --- | --- |
| **Chọn nhiều [đối tượng]** | Đánh dấu các mục cần xử lý. Thanh công cụ hiển thị [các chức năng hàng loạt]. |
| **[Thao tác hàng loạt 1]** | Chọn **[chức năng]**, sau đó [các bước riêng]. |
| **[Thao tác hàng loạt 2]** | Chọn **[chức năng]**, sau đó [các bước riêng]. |
```

## Lưu ý và cảnh báo

- Đặt **Lưu ý** ngay sau phần có điều kiện, giới hạn hoặc cách chọn dễ nhầm.
- Đặt **Cảnh báo** trước thao tác xóa, ghi đè, xử lý hàng loạt, công khai dữ liệu hoặc hành động khó hoàn tác.
- Không gom lưu ý ở cuối bài nếu chúng chỉ liên quan đến một tính năng cụ thể.
- Không lặp cùng một lưu ý ở nhiều mục.
- Khi một nút đổi chức năng theo trạng thái lựa chọn, mô tả cả hai trạng thái ngay tại phần giới thiệu giao diện và nhắc cảnh báo ở thao tác nguy hiểm.
- Khi xóa chỉ gỡ liên kết, phải nói rõ tài nguyên gốc vẫn còn; khi xóa không thể hoàn tác, đặt cảnh báo trước bảng bước.

## Chỉ thêm khi cần

- **Giới hạn/định dạng hỗ trợ**: khi ảnh hưởng đến việc hoàn thành thao tác.
- **Bước tiếp theo**: chỉ giữ 1–3 bài liên quan trực tiếp.
- Ảnh minh họa: đặt ngay sau nhóm bước cần đối chiếu và dùng mô tả ảnh rõ nghĩa.

## Những phần nên bỏ

- Mục tiêu học tập hoặc bảng “Bạn có thể làm gì” khi chỉ lặp lại nội dung chính.
- Tổng quan quy trình cho bài ngắn.
- Giải thích khái niệm, nội dung quảng bá hoặc ví dụ dài không giúp hoàn thành thao tác.
- Bảng phân loại tính năng, mức ảnh hưởng hoặc trường cấu hình nếu giao diện đã tự giải thích rõ.
- FAQ, lỗi giả định, giới hạn chưa xác minh và danh sách liên kết dài.
- Kết quả xác nhận lặp lại sau mọi bước.

---

## Hướng dẫn thao tác qua AI Agent

Phần này quy chuẩn cấu trúc outline và cách viết tài liệu hướng dẫn người dùng điều khiển các chức năng của RedAI thông qua AI Agent, giúp người dùng ra lệnh bằng ngôn ngữ tự nhiên thay cho thao tác bấm nút thủ công trên giao diện.

## Chọn loại bài cho Agent

| Loại | Dùng khi | Cách tổ chức |
| --- | --- | --- |
| **Loại A — Hướng dẫn một quy trình qua Agent** | Các tác vụ gồm nhiều bước nối tiếp nhau, Agent cần gọi tuần tự nhiều công cụ để đạt một kết quả cuối | Chia theo từng giai đoạn thực hiện, kèm bảng công cụ và câu lệnh mẫu (Prompt) tổng thể |
| **Loại B — Hướng dẫn các thao tác tính năng qua Agent** | Các yêu cầu tương đối độc lập như tra cứu, tạo nhanh, sửa, bật/tắt hoặc xóa đối tượng | Chia theo từng tính năng, mỗi tính năng có bảng công cụ tương ứng và câu lệnh mẫu riêng |

- Chọn **Loại A** cho các bài như: Tạo và kết nối kịch bản tự động hóa, Phân tích hội thoại và lưu ký ức khách hàng, hoặc So sánh cước và tạo vận đơn giao hàng.
- Chọn **Loại B** cho các bài như: Quản lý thư mục, Bật/tắt kịch bản, Tra cứu lịch sử thực thi, hoặc Khôi phục dữ liệu từ Thùng rác.
- Khi bài viết hướng dẫn cả hai cách thực hiện (giao diện và Agent), đặt mục **Thao tác qua Agent** thành một phương án thực hiện riêng dưới H3 hoặc đặt ở phần cuối bài.

## Outline Loại A — Hướng dẫn một quy trình qua Agent

```markdown
## Chuẩn bị kỹ năng (Skill) cho Agent

| Yêu cầu | Chi tiết cần chuẩn bị |
| --- | --- |
| **Kỹ năng cần kích hoạt (Skill)** | [Tên kỹ năng Agent cần được bật trong mục Cài đặt Agent, ví dụ: Kỹ năng Quản lý Quy trình / Kỹ năng CSKH & Ký ức]. |
| **Quyền tài khoản** | [Quyền cần có trong Không gian làm việc, ví dụ: Thành viên / Quản trị viên]. |
| **Dịch vụ liên kết (nếu có)** | [Tài khoản ngoài cần kết nối sẵn trong mục Tích hợp, ví dụ: Google Sheets, Zalo OA, GHN...]. |

## Liên kết thao tác giao diện và công cụ của Agent

| Thao tác trên giao diện | Công cụ Agent sử dụng | Nhiệm vụ của công cụ |
| --- | --- | --- |
| [Tên nút hoặc bước thao tác trên màn hình] | `[Tên công cụ của Agent]` | [Mô tả ngắn gọn Agent làm gì để thay thế thao tác này]. |
| [Thao tác tiếp theo trên màn hình] | `[Tên công cụ của Agent]` | [Mô tả ngắn gọn Agent làm gì]. |

## Câu lệnh mẫu (Prompt mẫu)

> Sao chép câu lệnh dưới đây, thay thế các thông tin trong ngoặc vuông `[...]` bằng dữ liệu thực tế của bạn và gửi cho Agent:

```text
[Nội dung câu lệnh mẫu hoàn chỉnh, gồm:
- Vai trò & Mục tiêu: "Bạn là trợ lý..., hãy giúp tôi [kết quả cần đạt]..."
- Dữ liệu cung cấp: [Liệt kê các thông tin đầu vào cần xử lý]
- Các bước thực hiện: [Yêu cầu Agent làm các bước cụ thể nào]
- Báo cáo kết quả: [Yêu cầu Agent thông báo lại những gì sau khi hoàn thành]]
```

## Kiểm tra kết quả

| Cách kiểm tra | Cách thực hiện | Dấu hiệu nhận biết thành công |
| --- | --- | --- |
| **Kiểm tra trên giao diện** | Mở [tên màn hình / khu vực]. | [Đối tượng mới hiển thị, trạng thái cập nhật...]. |
| **Hỏi trực tiếp Agent** | Nhắn cho Agent: "[Câu lệnh ngắn để Agent kiểm tra lại]". | Agent phản hồi xác nhận kèm [mã, đường dẫn, trạng thái...]. |
```

## Outline Loại B — Hướng dẫn nhiều tính năng qua Agent

```markdown
## Chuẩn bị kỹ năng (Skill) cho Agent

- **Kỹ năng cần kích hoạt**: [Tên kỹ năng chính dùng cho nhóm tính năng này].
- **Phạm vi hỗ trợ**: [Tóm tắt ngắn các thao tác Agent có thể thực hiện thay cho người dùng].

## Các tính năng thao tác qua Agent

### [Tên tính năng 1 — Động từ + Đối tượng]

[Một câu nêu tính năng này dùng để làm gì qua Agent.]

| Mục | Chi tiết |
| --- | --- |
| **Thao tác tương đương trên UI** | [Tên nút, menu hoặc khu vực trên giao diện]. |
| **Công cụ Agent sử dụng** | `[Tên công cụ tương ứng]`. |
| **Thông tin cần cung cấp** | [Các dữ liệu người dùng cần nêu trong câu lệnh, ví dụ: Tên, Thư mục, Nội dung...]. |

**Câu lệnh mẫu (Prompt):**

> "[Câu lệnh mẫu ngắn gọn, tự nhiên, có chứa các biến `[thông tin]` để người dùng điền vào]".

> **Lưu ý:** [Điều kiện hoặc lưu ý quan trọng khi dùng câu lệnh này, nếu có.]

### [Tên tính năng 2 — Động từ + Đối tượng]

| Mục | Chi tiết |
| --- | --- |
| **Thao tác tương đương trên UI** | [Tên nút hoặc menu trên giao diện]. |
| **Công cụ Agent sử dụng** | `[Tên công cụ tương ứng]`. |
| **Thông tin cần cung cấp** | [Thông tin bắt buộc]. |

**Câu lệnh mẫu (Prompt):**

> "[Câu lệnh mẫu]".

> **Cảnh báo:** [Nhắc nhở người dùng yêu cầu Agent xác nhận trước nếu thao tác gây xóa hoặc thay đổi dữ liệu lớn.]
```

## Cách tổ chức bài viết cho Agent

- **Đối tượng độc giả**: Người dùng cuối của RedAI (chuyên viên nghiệp vụ, quản lý, người vận hành), không phải lập trình viên.
- **Quy chuẩn thuật ngữ**:
  - Dùng **Kỹ năng (Skill)** để chỉ gói năng lực cần bật cho Agent.
  - Dùng **Công cụ (Tool)** để chỉ hành động cụ thể mà Agent gọi thay cho việc người dùng bấm nút.
  - Dùng **Thông tin cần cung cấp** thay cho các khái niệm kỹ thuật như "tham số", "payload" hay "schema".
  - Dùng **Câu lệnh mẫu (Prompt mẫu)** để chỉ nội dung người dùng sao chép và gửi vào khung chat với Agent.
- **Bắt buộc có bảng liên kết**: Mọi bài viết hoặc mục hướng dẫn Agent đều phải có bảng đối chiếu giữa **Thao tác trên giao diện** và **Công cụ Agent sử dụng** để người đọc hiểu được sự tương đương giữa hai cách làm.
- **Đặt vị trí điền thông tin rõ ràng**: Trong Prompt mẫu, các dữ liệu cần người dùng tự điền luôn đặt trong dấu ngoặc vuông in hoa hoặc in đậm rõ ràng, ví dụ: `[Tên quy trình]`, `[Mã đơn hàng]`, `[Số điện thoại]`.
- **Hướng dẫn đối chiếu kết quả hai chiều**: Luôn chỉ rõ vừa cách xem lại trên màn hình, vừa cách hỏi tiếp Agent trong khung chat để xác nhận công việc đã hoàn thành đúng.

## Chuẩn viết câu lệnh mẫu (Prompt mẫu)

Mỗi Prompt mẫu đưa vào tài liệu cần có bố cục 4 phần giúp Agent hiểu chính xác và làm đúng ngay từ lần đầu:

1. **Bối cảnh & Mục tiêu**: Nêu rõ bạn muốn Agent đóng vai gì và cần đạt kết quả gì.
2. **Dữ liệu đầu vào**: Cung cấp đầy đủ thông tin thực tế mà Agent cần dùng để xử lý.
3. **Các bước yêu cầu**: Chỉ rõ thứ tự ưu tiên hoặc các bước cụ thể Agent cần thực hiện.
4. **Yêu cầu phản hồi**: Nêu rõ thông tin Agent cần trả lời sau khi hoàn tất (mã số, liên kết xem lại, bản tóm tắt...).

### Mẫu khung câu lệnh quy trình (Loại A)

```text
Hãy sử dụng kỹ năng [Tên kỹ năng] để giúp tôi thực hiện quy trình sau:

1. [Bước 1]: [Mô tả yêu cầu và thông tin [dữ liệu 1]].
2. [Bước 2]: [Mô tả yêu cầu và thông tin [dữ liệu 2]].

Yêu cầu thực hiện:
- [Điều kiện quan trọng, ví dụ: kiểm tra trước khi tạo mới, báo lại nếu thiếu dữ liệu].
- Sau khi hoàn thành, hãy thông báo cho tôi: [danh sách thông tin cần xác nhận lại].
```

### Mẫu khung câu lệnh thao tác nhanh (Loại B)

```text
Hãy giúp tôi [hành động] [đối tượng] [tên hoặc mã nhận diện] [thông tin chi tiết hoặc điều kiện đi kèm nếu có].
```

## Bảng tra cứu Kỹ năng (Skill) theo khu vực chức năng

Để người viết tài liệu hướng dẫn đúng kỹ năng mà người dùng cần bật cho Agent:

| Khu vực chức năng trên RedAI | Kỹ năng cần kích hoạt cho Agent (Skill) | Nhóm công cụ tiêu biểu Agent sử dụng |
| --- | --- | --- |
| **Quy trình tự động hóa (AI Workflow)** | Kỹ năng Quản lý Quy trình (`RedAI - Module - AI Workflow`) | Tạo/sửa quy trình, thêm/nối node, bật/tắt lịch chạy, quản lý thư mục, kiểm tra lỗi |
| **Chăm sóc khách hàng & Hội thoại (OmniAI Chat)** | Kỹ năng Hội thoại & Ký ức (`RedAI - OmniAI Chat`) | Đọc hội thoại, tóm tắt tin nhắn, lưu ký ức khách hàng, gửi tin nhắn đa kênh |
| **Dữ liệu & Tri thức (Knowledge Base)** | Kỹ năng Cơ sở Tri thức (`RedAI - Knowledge & Graph RAG`) | Tải tài liệu, cào dữ liệu từ trang web, tìm kiếm tri thức doanh nghiệp |
| **Giao hàng & Vận chuyển (Shipping)** | Kỹ năng Vận chuyển & Giao hàng (`RedAI - Shipping & Logistics`) | Tra cước phí các hãng (GHN, GHTK, ViettelPost...), tạo đơn vận chuyển, tra cứu hành trình |
| **Bảng tính & Tài liệu (Google Workspace)** | Kỹ năng Tích hợp Văn phòng (`RedAI - Integration Hub`) | Đọc/ghi dữ liệu Google Sheets, tạo và cập nhật văn bản Google Docs |

## Lưu ý và cảnh báo khi dùng Agent

- **Kiểm tra Kỹ năng trước khi ra lệnh**: Đặt lưu ý nhắc người dùng kiểm tra xem Agent đã được bật Kỹ năng phù hợp trong phần Cài đặt Agent chưa trước khi thực hiện.
- **Cảnh báo trước thao tác nguy hiểm**: Đặt cảnh báo rõ ràng với các lệnh xóa vĩnh viễn, hủy phiên chạy hoặc gửi tin nhắn hàng loạt ra ngoài; hướng dẫn người dùng yêu cầu Agent tóm tắt danh sách và hỏi xin xác nhận `Có/Không` trước khi thực hiện.
- **Rõ ràng về thông tin cung cấp**: Nhắc người dùng cung cấp đủ tên, mã số hoặc thông tin định danh cụ thể để tránh việc Agent chọn nhầm đối tượng.

## Những phần nên bỏ khi viết cho Agent

- Các mã định danh hệ thống nội bộ (như UUID, mã cơ sở dữ liệu, token bảo mật).
- Chi tiết mã kỹ thuật (code API, JSON Schema thô, phương thức HTTP GET/POST).
- Hướng dẫn các thao tác thuần giao diện trong phần Agent (như tọa độ chuột, phím tắt màn hình, phóng to thu nhỏ canvas).
- Các câu lệnh mẫu quá chung chung thiếu biến điền cụ thể khiến người dùng không biết cách áp dụng vào thực tế.

