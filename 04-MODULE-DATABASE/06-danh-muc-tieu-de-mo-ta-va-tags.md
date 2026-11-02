## Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Database

Tài liệu này đóng vai trò là danh mục điều hướng trung tâm (Catalog Index) của Phân hệ **04 — Module Database (Bảng dữ liệu động)** trên hệ thống **RedAI**. Bảng tổng hợp siêu dữ liệu dưới đây giúp người dùng, quản trị viên và trợ lý ảo AI Agent nhanh chóng xác định đúng tài liệu nghiệp vụ cần tham chiếu theo từng tình huống vận hành cụ thể.

---

## Thông tin Kỹ năng (Skill) & Bộ công cụ (Tool Suite) của Phân hệ

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Workspace Member, Editor, Admin hoặc Owner |

---

## Bảng tổng hợp siêu dữ liệu các tài liệu nghiệp vụ

| Thuộc tính | Chi tiết tài liệu 01 | Chi tiết tài liệu 02 |
| :--- | :--- | :--- |
| **Tên file** | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` |
| **Tiêu đề tài liệu** | Quy trình khởi tạo bảng dữ liệu và phân loại danh mục | Quy trình cấu hình trường dữ liệu và kiểu dữ liệu |
| **Mô tả nghiệp vụ** | Hướng dẫn khởi tạo bảng mới qua 4 phương án (tạo trực tiếp, tạo từ bảng có sẵn kèm lọc và sao chép dữ liệu, tạo bằng AI Blueprint, import Excel/CSV/JSON tối đa 10MB), quản lý cây thư mục danh mục, vận hành Thùng rác đếm ngược 10 ngày và menu thao tác từng bảng. | Hướng dẫn quản trị cột tại màn hình chuyên sâu Table Fields và menu tiêu đề cột Grid View, cấu hình các kiểu dữ liệu chuyên sâu (văn bản, số, tiền tệ, ngày giờ, select, relation, lookup, rollup, formula), thiết lập ràng buộc Not Null, Unique, giá trị mặc định và validation rules. |
| **Mục tiêu sử dụng** | Cần khởi tạo bảng dữ liệu mới, phân nhóm danh mục, di chuyển bảng giữa các danh mục, khôi phục bảng từ thùng rác hoặc mở các ngăn kéo chức năng của bảng. | Cần bổ sung cột mới vào bảng, thay đổi kiểu dữ liệu cột, viết công thức tính toán tự động (Formula), cấu hình quan hệ liên kết bảng (Relation) hoặc tổng hợp dữ liệu (Rollup). |
| **Không dùng khi** | Cần chỉnh sửa chi tiết các dạng xem (Grid, Kanban, Gallery, Calendar, Form) hoặc cấu hình chuyên sâu từng kiểu dữ liệu. | Cần tạo bảng mới, đổi tên bảng, xóa bảng hoặc thiết lập bộ lọc/sắp xếp trên dạng xem. |
| **Thực thể & Phạm vi** | `Trang chủ > Database`, Thư mục Danh mục, Hộp thoại Tạo bảng, Thùng rác lưu trữ 10 ngày. | `Trang chủ > Database > Table Fields`, Header cột Grid View, Panel cấu hình trường dữ liệu. |
| **Công cụ AI Agent trọng tâm** | `createTable`, `listTables`, `getTable`, `updateTable`, `duplicateTable`, `bulkCreateTables`, `bulkDeleteTables`, `createCollectionCategory`, `assignTableCollectionCategory` | `getColumn`, `createColumn`, `updateColumn`, `deleteColumn`, `setPrimaryColumn`, `createOrUpdateCurrencyColumn`, `createOrUpdateRelationColumn`, `createOrUpdateFormulaColumn` |
| **10 Tags chuẩn hóa** | `database`, `table-create`, `categories`, `import-excel`, `import-csv`, `ai-blueprint`, `duplicate-table`, `trash-recovery`, `workspace-base`, `table-actions` | `database-fields`, `table-fields`, `field-types`, `relation-field`, `lookup-rollup`, `formula`, `autonumber`, `currency`, `not-null`, `unique-validation` |

---

| Thuộc tính | Chi tiết tài liệu 03 | Chi tiết tài liệu 04 |
| :--- | :--- | :--- |
| **Tên file** | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` |
| **Tiêu đề tài liệu** | Quy trình thiết lập và tùy biến các dạng xem Views | Quản lý sơ đồ quan hệ, webhooks và ma trận phân quyền |
| **Mô tả nghiệp vụ** | Hướng dẫn khởi tạo và vận hành 5 dạng xem cốt lõi (Grid View, Kanban View, Form View, Calendar View, Gallery View) qua ngăn kéo Cấu hình View (phân quyền Cộng tác/Đã khóa/Cá nhân), áp dụng bộ công cụ lọc, sắp xếp, gom nhóm, chiều cao dòng và Hộp thoại Chi tiết dòng bản ghi kèm lịch sử thay đổi. | Hướng dẫn các tính năng quản trị cấp cao: sơ đồ quan hệ trực quan Relations ERD canvas (kéo thả điểm nối, chỉ hiện PK/FK), ma trận phân quyền bảng 9 phạm vi, phân quyền cột, bảo mật cấp bản ghi theo vai trò/người dùng và tự động hóa Webhook/Scheduled Hook sang Workflow. |
| **Mục tiêu sử dụng** | Cần chuyển đổi góc nhìn dữ liệu, tạo View mới, thiết lập bộ lọc (Filter), sắp xếp (Sort), gom nhóm (Group by), điều chỉnh chiều cao dòng, theo dõi thẻ Kanban, lịch biểu Calendar hoặc thiết kế biểu mẫu Form. | Cần quan sát tổng thể kiến trúc ERD giữa các bảng, kéo dây liên kết dữ liệu, cấu hình ma trận phân quyền bảng/cột, thiết lập bảo mật cấp bản ghi hoặc tạo webhook bắn dữ liệu tự động. |
| **Không dùng khi** | Cần can thiệp cấu trúc cột gốc của bảng hoặc cấu hình Webhook/phân quyền hệ thống. | Cần thao tác nhập liệu ô tính thông thường hoặc vận hành Trung Tâm Tiện Ích in ấn tem nhãn. |
| **Thực thể & Phạm vi** | `View Details`, `Kanban View`, `Form View`, `Calendar View`, Hộp thoại Chi tiết dòng bản ghi, Lịch sử thay đổi. | `Trang chủ > Database > Quan hệ`, Ngăn kéo Quyền bảng, Quyền trường, Bảo mật cấp bản ghi, Hộp thoại Webhooks. |
| **Công cụ AI Agent trọng tâm** | `listTableViews`, `createGridView`, `createKanbanView`, `createFormView`, `updateViewColumns`, `setFiltersView`, `setOrdersView`, `setGroupBy`, `listRecords`, `createRecords` | `listTables`, `createOrUpdateRelationColumn`, `listLinkedRecords`, `hookList`, `hookCreateOrUpdate`, `hookTest`, `hookTrigger`, `hookLogList`, `listSources` |
| **10 Tags chuẩn hóa** | `grid-view`, `kanban-view`, `calendar-view`, `form-view`, `gallery-view`, `view-config`, `row-detail`, `change-history`, `filter-sort`, `group-by` | `relations-erd`, `canvas-handles`, `pk-fk`, `table-permissions`, `field-permissions`, `row-level-security`, `webhooks`, `scheduled-hooks`, `workflow-trigger`, `access-control` |

---

| Thuộc tính | Chi tiết tài liệu 05 | Chi tiết tài liệu 06 |
| :--- | :--- | :--- |
| **Tên file** | `05-trung-tam-tien-ich-in-tem-nhan-qr-va-bao-cao-tai-lieu.md` | `06-danh-muc-tieu-de-mo-ta-va-tags.md` |
| **Tiêu đề tài liệu** | Trung tâm tiện ích, in tem nhãn QR và báo cáo tài liệu | Danh mục Tiêu đề, Mô tả và Tags chuẩn hóa — Module Database |
| **Mô tả nghiệp vụ** | Hướng dẫn vận hành 10 công cụ trong Trung Tâm Tiện Ích: in tem nhãn và tạo mã QR hàng loạt (A4 3-cột, Decal), thiết kế mẫu báo cáo PDF kéo thả biến bảng dữ liệu, quy trình ánh xạ nhập dữ liệu (Import mapping 3 cột), làm sạch định dạng và xử lý trùng lặp. | Bảng tổng hợp siêu dữ liệu, bản đồ từ khóa và quy tắc định tuyến nhanh theo tình huống thực tế cho toàn bộ Phân hệ 04 — Module Database. |
| **Mục tiêu sử dụng** | Cần in mã QR dán tem sản phẩm/hồ sơ, thiết kế biểu mẫu PDF tự động điền dữ liệu từ bảng, import file Excel khớp nối cột hệ thống, hoặc kiểm tra tỷ lệ hoàn thiện dữ liệu. | Cần định vị nhanh tài liệu phù hợp khi tiếp nhận yêu cầu liên quan đến cơ sở dữ liệu hoặc bảng dữ liệu động. |
| **Không dùng khi** | Cần tạo bảng mới ban đầu hoặc cấu hình phân quyền truy cập. | Đã xác định được chính xác nghiệp vụ cụ thể cần thực hiện trong 5 tài liệu chuyên sâu 01, 02, 03, 04, 05. |
| **Thực thể & Phạm vi** | Ngăn kéo Trung Tâm Tiện Ích, In Tem Nhãn & Tạo Mã QR Hàng Loạt, Thiết Kế Mẫu Báo Cáo Tài Liệu, Bảng ánh xạ Nhập dữ liệu. | Toàn bộ Phân hệ 04 — Module Database. |
| **Công cụ AI Agent trọng tâm** | `listRecords`, `getRecord`, `updateRecords`, `mergeRecords`, `countRecords`, `createRecords`, `bulkGroupBy`, `bulkAggregateRecords` | Toàn bộ 97 công cụ thuộc Project Schema `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **10 Tags chuẩn hóa** | `utilities-center`, `print-qr-labels`, `qr-barcode`, `pdf-template-designer`, `import-mapping`, `data-cleaning`, `duplicate-merge`, `mock-data`, `data-health`, `sms-campaign` | `database-catalog`, `metadata-index`, `table-guide`, `schema-guide`, `view-guide`, `relation-guide`, `utilities-guide`, `qr-label-guide`, `database-module`, `redai-documentation` |

---

## Bảng định tuyến nhanh theo tình huống thực tế

Dưới đây là bảng tra cứu phản xạ nhanh giúp người dùng và AI Agent chọn ngay tài liệu cần thiết:

| Tình huống thực tế phát sinh | Tài liệu cần mở ngay | Khu vực / Giao diện & Công cụ trọng tâm |
| :--- | :--- | :--- |
| Muốn tạo bảng dữ liệu mới từ file Excel hoặc từ một bảng mẫu có sẵn | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Hộp thoại `Tạo bảng` • Tool `createTable`, `duplicateTable` |
| Cần tạo nhóm thư mục để gom các bảng bán hàng lại gọn gàng | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Thanh bên trái `Danh mục` • Tool `createCollectionCategory` |
| Vô tình xóa nhầm một bảng và muốn lấy lại trong vòng 10 ngày | `01-quy-trinh-khoi-tao-bang-du-lieu-va-phan-loai-danh-muc.md` | Biểu tượng `Thùng rác` trên toolbar chính, nút `Khôi phục` |
| Muốn thêm cột Tiền tệ, Ngày tháng hoặc Số điện thoại vào bảng | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | `Trang chủ > Database > Table Fields` • Tool `createOrUpdateCurrencyColumn` |
| Cần đặt cột làm nhãn đại diện chính khi tìm kiếm hoặc liên kết | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Header cột Grid View • Tool `setPrimaryColumn` |
| Muốn thiết lập công thức tính tự động Thành tiền = Số lượng * Đơn giá | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Cột kiểu `Formula` • Tool `createOrUpdateFormulaColumn` |
| Cần kết nối bảng Đơn Hàng với bảng Khách Hàng (Relation 1-N) | `02-quy-trinh-cau-hinh-truong-du-lieu-va-kieu-du-lieu.md` | Cột kiểu `Relation` • Tool `createOrUpdateRelationColumn` |
| Muốn tạo dạng xem bảng thẻ Kanban để kéo thả đơn hàng theo trạng thái | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `+ Thêm view...` $\rightarrow$ Loại `Kanban` • Tool `createKanbanView` |
| Cần tạo biểu mẫu thu thập đăng ký gửi khách hàng điền trực tiếp | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | `+ Thêm view...` $\rightarrow$ Loại `Form` • Tool `createFormView` |
| Muốn xem lịch sử ai đã cập nhật thông tin trên một dòng bản ghi | `03-quy-trinh-thiet-lap-va-tuy-bien-cac-dang-xem-views.md` | Mở `Hộp thoại Chi tiết dòng #{N}` $\rightarrow$ Tab `Lịch sử thay đổi` |
| Cần quan sát tổng thể sơ đồ liên kết giữa tất cả các bảng trong hệ thống | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | Menu bảng $\rightarrow$ `Quan hệ` (`Trang chủ > Database > Quan hệ`) |
| Muốn cấu hình chỉ Trưởng phòng mới được quyền xóa bảng hoặc xem cột lương | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | Menu bảng $\rightarrow$ Ngăn kéo `Quyền bảng` và `Quyền trường` |
| Muốn nhân viên kinh doanh chỉ nhìn thấy khách hàng do chính mình phụ trách | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | Menu bảng $\rightarrow$ `Bảo mật cấp bản ghi` (Row-level security) |
| Muốn tự động kích hoạt Agentic Workflow mỗi khi có bản ghi mới | `04-quan-ly-do-thi-quan-he-nguon-du-lieu-webhooks-va-phan-quyen.md` | Menu bảng $\rightarrow$ `Webhooks` • Tool `hookCreateOrUpdate`, `hookTest` |
| Cần in tem nhãn có mã QR dán lên sản phẩm hoặc xuất file A4 3 cột | `05-trung-tam-tien-ich-in-tem-nhan-qr-va-bao-cao-tai-lieu.md` | View Details $\rightarrow$ `Trung Tâm Tiện Ích` $\rightarrow$ `In Tem Nhãn` • Tool `listRecords` |
| Muốn kéo thả biến bảng dữ liệu vào hợp đồng mẫu PDF để tự động điền | `05-trung-tam-tien-ich-in-tem-nhan-qr-va-bao-cao-tai-lieu.md` | `Trung Tâm Tiện Ích` $\rightarrow$ `Xuất báo cáo Tài liệu mẫu` • Tool `listRecords` |
| Cần import file Excel và khớp nối từng cột vào đúng trường dữ liệu | `05-trung-tam-tien-ich-in-tem-nhan-qr-va-bao-cao-tai-lieu.md` | Menu View $\rightarrow$ `Nhập dữ liệu` • Tool `createRecords` |

---

## Danh mục từ khóa tìm kiếm (Keyword Index)

- **Khởi tạo & Danh mục**: `tạo bảng`, `tạo trực tiếp`, `tạo từ bảng có sẵn`, `sao chép dữ liệu`, `bộ lọc kế thừa`, `tạo bằng ai`, `import excel 10mb`, `danh mục category`, `thùng rác 10 ngày`, `khôi phục xóa mềm`.
- **Trường & Cột dữ liệu**: `table fields`, `cấu hình trường`, `not null`, `unique`, `display field`, `single line text`, `currency`, `relation`, `lookup`, `rollup`, `formula`, `autonumber`, `validation regex`.
- **Dạng xem & Trực quan hóa**: `cấu hình view`, `quyền view cộng tác/đã khóa/cá nhân`, `grid view`, `kanban view stacks`, `form view banner`, `calendar view scope`, `chi tiết dòng`, `lịch sử thay đổi`, `bộ lọc filter`, `gom nhóm group by`, `chiều cao dòng`.
- **Quản trị cấp cao & Bảo mật**: `quan hệ relations erd`, `kéo thả handles`, `pk-fk`, `quyền bảng 9 phạm vi`, `quyền trường`, `bảo mật cấp bản ghi row-level`, `quy tắc theo người`, `webhooks workflow`, `lập lịch theo thời gian`.
- **Trung tâm tiện ích & In ấn**: `trung tâm tiện ích`, `in tem nhãn qr hàng loạt`, `bố cục lưới a4 3 cột`, `decal cuộn`, `thiết kế mẫu báo cáo tài liệu`, `pdf template designer`, `biến tự do`, `biến từ bảng`, `nhập dữ liệu import mapping`, `chuẩn hóa làm sạch`, `xử lý trùng lặp`, `mock data`.
