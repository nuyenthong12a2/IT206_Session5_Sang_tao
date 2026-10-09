# Bài 5 – Quy trình đưa yêu cầu mới vào Sprint (AC – DoD – MoSCoW)

**Dự án:** Ứng dụng đặt xe RikkeiGo
**Người thực hiện:** Lan (Scrum Master) – **Người xem xét:** Đức (Product Owner)

## Phạm vi

Quy trình áp dụng cho **mọi story mới** từ Marketing, Chăm sóc khách hàng (CSKH) và Vận hành, từ lúc được đề xuất đến lúc được đội cam kết làm trong Sprint và được nghiệm thu. Không bàn về cách ước lượng chi tiết hay kỹ thuật code.

Ba "cổng" xuyên suốt quy trình:

- **AC (Given – When – Then):** 3–7 AC cho mỗi story, thống nhất *trước* khi vào Sprint.
- **MoSCoW:** gắn với *một lần phát hành*; Must ≤ khoảng 60% năng lực.
- **DoD:** một bản chung cho mọi story, chỉ nâng dần theo năng lực của đội.

---

## Phần 1 – Thiết kế quy trình (5 bước)

| # | Bước | Việc cần làm | Người chịu trách nhiệm | Điều kiện sang bước sau |
|---|------|--------------|------------------------|--------------------------|
| 1 | **Tiếp nhận** | Bộ phận đề xuất gửi story theo mẫu *"Là… tôi muốn… để…"* kèm lý do kinh doanh và release mong muốn. PO ghi vào Product Backlog, trạng thái "Mới". Không bộ phận nào làm việc trực tiếp với Developers để chèn việc. | Người đề xuất (viết); **PO** (tiếp nhận, sở hữu Backlog) | Story đủ 3 phần và có lý do kinh doanh rõ ràng |
| 2 | **Làm rõ & viết AC** | PO cùng người đề xuất viết 3–7 AC dạng Given–When–Then. Developers đặt câu hỏi, kiểm tra AC có kiểm thử được không, ước lượng sơ bộ và đề nghị tách nếu story quá lớn. | **PO** (nội dung AC); **Developers** (xác nhận hiểu, ước lượng); **SM** (điều phối buổi làm rõ) | Có 3–7 AC; Developers xác nhận kiểm thử được và ước lượng được; story vừa trong 1 Sprint → trạng thái **Ready** |
| 3 | **Xếp MoSCoW theo release** | Với release đang lên kế hoạch, PO gắn nhãn Must/Should/Could/Won't dựa trên tiêu chí chung (nếu thiếu thì release có chạy được/an toàn/hợp lệ không; giá trị so với chi phí; hạn cứng). Chỉ story **Ready** mới được xét Must. | **PO** (quyết định); **Developers** (cho số liệu chi phí/năng lực); **SM** (giữ tiêu chí, chặn "người nói to nhất") | Tổng Must ≈ 60% năng lực release; mỗi Must có lý do ghi lại; có thứ tự ưu tiên trong Backlog |
| 4 | **Chọn vào Sprint** | Tại Sprint Planning, PO trình bày các story đầu Backlog và Sprint Goal; Developers chọn lượng việc vừa sức và cam kết. Story mới phát sinh *sau* buổi này không tự động vào Sprint. | **Developers** (chọn và cam kết); **PO** (Sprint Goal, thứ tự); **SM** (bảo vệ quy tắc) | Story đã Ready; Developers đồng ý khối lượng; Sprint Goal không bị phá vỡ |
| 5 | **Làm & nghiệm thu bằng DoD** | Developers làm, kiểm tra từng AC và từng mục DoD. Tại Sprint Review, PO nghiệm thu. Retrospective xem có nên nâng DoD không. | **Developers** (làm, tự kiểm); **PO** (nghiệm thu); **SM** (hỗ trợ, đề xuất nâng DoD) | **Tất cả AC đạt và mọi mục DoD hoàn thành** → Done. Nếu chưa, quay lại Backlog (không tính Done một phần) |

**Quy tắc chung:** story chưa qua bước 2 thì không được gán Must ở bước 3 và không được vào Sprint ở bước 4. Đây là cơ chế chặn các story thiếu AC và việc gán Must theo cảm tính.

---

## Phần 2 – Xử lý tình huống

### Tình huống 1: Giữa Sprint, Marketing đòi đưa ngay story "Tặng mã giới thiệu bạn bè" (chưa có AC) vào Sprint đang chạy

**Cách quy trình xử lý:** Story này mới ở bước 1 nên chưa có AC, chưa Ready, và không thể sang bước 4. Lan ghi story vào Backlog qua PO, không để Marketing giao việc trực tiếp cho Developers, vì Sprint Goal và Sprint Backlog đã được đội cam kết. Story sẽ được làm rõ và viết AC ở bước 2 (trong Backlog Refinement), xếp MoSCoW ở bước 3 và được xét tại Sprint Planning kế tiếp. Nếu thực sự khẩn cấp, chỉ **PO** mới có quyền quyết định, và chỉ sau khi story đã có AC và Developers ước lượng xong: đội có thể *đổi* một story có kích thước tương đương ra khỏi Sprint với điều kiện Sprint Goal vẫn giữ nguyên (nếu Sprint Goal không còn giá trị thì PO mới được hủy Sprint).

**AC mẫu cho story "Tặng mã giới thiệu bạn bè"** (số liệu mang tính minh họa, PO sẽ chốt):

> **AC1 – Tặng thưởng khi bạn bè hoàn thành chuyến đầu**
> **Given** Người dùng A đã có tài khoản và có mã giới thiệu cá nhân, và bạn B chưa từng có tài khoản RikkeiGo
> **When** B đăng ký bằng mã của A và hoàn thành chuyến đi đầu tiên
> **Then** cả A và B nhận mỗi người 1 mã giảm giá 20.000đ trong ví khuyến mãi, hiển thị trong vòng 5 phút sau khi chuyến đi hoàn tất

*(Các AC còn lại của story, trong phạm vi 3–7, nên bao gồm: mã đã được dùng cho tài khoản cũ, mã hết hạn, và giới hạn số lần giới thiệu mỗi người.)*

### Tình huống 2: Cả 3 bộ phận đều cho rằng yêu cầu của mình là Must

**Cách quy trình xử lý:** Nhãn MoSCoW không do bộ phận đề xuất tự gán mà do PO gán ở bước 3, theo tiêu chí chung và gắn với *một release cụ thể*. Lan tổ chức buổi xếp hạng, yêu cầu mỗi bộ phận trả lời cùng một câu hỏi: "Nếu release này thiếu yêu cầu đó thì có chạy được, an toàn và hợp lệ không?" Vì Must chỉ chiếm khoảng 60% năng lực, các yêu cầu còn lại phải chuyển xuống Should/Could/Won't dù người đề xuất mạnh tiếng đến đâu.

**Cách gán nhãn mẫu** (release "Tháng khuyến mãi"; story minh họa):

| Bộ phận | Story | Nhãn | Lý do |
|---------|-------|------|-------|
| Vận hành | Đối soát tự động tiền khuyến mãi với tài xế | **Must** | Thiếu thì tính sai tiền khi có khuyến mãi, rủi ro tài chính, release không thể chạy an toàn |
| Marketing | Tặng mã giới thiệu bạn bè | **Should** | Tăng người dùng nhưng release vẫn chạy được; tạm dùng mã khuyến mãi chung |
| CSKH | Xem lịch sử mã khuyến mãi trên màn hình hỗ trợ | **Could** | Giúp CSKH nhanh hơn nhưng có cách làm thủ công; làm nếu còn năng lực |

Story nào không vừa năng lực của release này được ghi **Won't (lần này)**, không xóa mà giữ trong Backlog để xét lại ở release sau. Nhãn được ghi kèm lý do để bộ phận không đồng ý có thể xem lại, và chỉ đổi khi có thông tin mới (mục tiêu release, chi phí, rủi ro thay đổi).

---

## Kết luận

Quy trình 5 bước cho phép mọi story mới đi qua cùng một "đường ray": **Ready (có AC) → có nhãn MoSCoW theo release → được cam kết trong Sprint Planning → Done theo DoD**. PO giữ quyền quyết định ưu tiên, Developers giữ quyền cam kết khối lượng, SM bảo vệ quy trình và Sprint đang chạy.
