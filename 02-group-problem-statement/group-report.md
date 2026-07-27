# Group Report — Day 02


## Thành viên nhóm


| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|--------------------|
| 1   |   Lăng Thị Phương Huế        |   2A202601915         |                    |
| 2   |   Nguyễn Hải Quân     |     2A202601863        |                    |
| 3   |   Đặng Đức Hòa        |      2A202601351        |                    |
| 4   |    Nguyễn Đức Dũng       |   2A202601823          |                    |
---


# 02 — Group Problem Statement


## Group convergence


Nhóm gồm 3-4 người, mỗi người chia sẻ top 3 vấn đề cá nhân. Tổng cộng thu thập được khoảng 9-12 candidates và tiến hành phân cụm như sau:


| Cluster | Candidate examples | Pattern chung | Ghi chú |
|---|---|---|---|
| **Báo cáo/tổng hợp thông tin** | Weekly/Daily meeting / Báo cáo tiến độ môn học / Tổng hợp slide bài giảng | Cần xem lại record hoặc ghi chép ngay tại thời điểm cuộc họp diễn ra. | Đây là vấn đề lặp đi lặp lại có tần suất cao nhất của BA. |
| **Nghiên cứu, thu thập tài liệu** | Research thị trường, giải pháp, viết user story, AC | Thông tin bị rời rạc từ nhiều nguồn khác nhau. | Tốn nhiều chất xám và thời gian phân tích chuyên sâu. |
| **Giao thông công cộng** | Dự đoán giờ xe buýt đến / Tình trạng còn trống | Thiếu thông tin real-time. | Khó giải quyết trong phạm vi buổi lab do hạn chế tiếp cận nguồn dữ liệu thực tế. |


---


## Shortlist và Score


Nhóm đưa 3 vấn đề nổi bật nhất vào ma trận chấm điểm để lựa chọn bài toán tối ưu nhất:


| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Báo cáo tổng hợp thông tin** | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35** |
| **Nghiên cứu, thu thập tài liệu** | 5 | 4 | 4 | 4 | 4 | 4 | 4 | **29** |
| **Giao thông công cộng** | 5 | 4 | 3 | 4 | 4 | 4 | 4 | **28** |


### Quyết định chọn của nhóm: **Báo cáo tổng hợp thông tin**


*   **Vì sao chọn:**
   *   Có workflow rõ nhất.
   *   Có baseline thời gian cụ thể để so sánh.
   *   Có thể validate nhanh với các PM khác.
   *   Có thể research các tool/pattern có sẵn trên thị trường.
   *   Có thể vẽ before/after workflow rất rõ ràng.
*   **Vì sao không chọn các bài khác:**
   *   *Nghiên cứu, thu thập tài liệu (đặc biệt là Slack Search/PRD review):* Impact rộng nhưng khả năng kết nối dữ liệu (data access) phức tạp, dễ trượt sang thiết kế hệ thống tìm kiếm/agent quá lớn vượt quá giới hạn thời gian làm lab. Quality metric của việc review PRD cũng khó thống nhất nhanh.
   *   *Giao thông công cộng:* Khó kiểm chứng và thiếu dữ liệu đầu vào thời gian thực để chạy thử nghiệm.


---


## Research giải pháp trên thị trường


Nhóm tiến hành phân tích điểm yếu cốt lõi và tác động thực tế của các giải pháp hiện tại:


| Sản phẩm | Domain yếu chính | Điểm yếu cụ thể | Tác động thực tế |
|---|---|---|---|
| **Otter.ai** | Tiếng Việt & tùy biến doanh nghiệp | Mạnh nhất với tiếng Anh; template, workflow CRM và quản trị enterprise không sâu bằng các công cụ chuyên sales. | Có thể sai tên riêng, thuật ngữ tiếng Việt; biên bản cần chỉnh sửa thủ công nhiều. |
| **Fireflies.ai** | Độ phức tạp & trải nghiệm sử dụng | Rất nhiều tính năng nên setup, phân quyền và quản lý bot có thể phức tạp. | Team nhỏ có thể chỉ dùng một phần tính năng nhưng vẫn phải trả tiền và cấu hình nhiều. |
| **Fathom** | Họp offline & workflow nghiệp vụ | Tập trung mạnh vào cuộc họp online, sales và customer success; workflow phê duyệt biên bản hoặc quản trị hành chính không phải thế mạnh. | Không phù hợp nếu cần biên bản họp hội đồng, họp nội bộ có quy trình ký duyệt nhiều bước. |
| **Avoma** | Họp hành chính & chi phí | Thiết kế thiên về sales/revenue intelligence, CRM và coaching; có thể dư thừa với nhu cầu chỉ ghi biên bản. | Doanh nghiệp không dùng CRM sẽ khó tận dụng hết giá trị, chi phí trên mỗi user có thể không hiệu quả. |
| **tl;dv** | Quản trị enterprise & kiểm soát dữ liệu | Mạnh về recording, transcript, summary và multi-meeting insights nhưng yếu hơn ở governance, workflow phê duyệt và quản trị chuyên sâu. | Khó đáp ứng các tổ chức cần audit log, phân quyền dữ liệu phức tạp hoặc quy trình compliance chặt. |
| **Google Meet + Gemini** | Hệ sinh thái & tính linh hoạt | Phụ thuộc Google Workspace; tùy biến template, CRM và phân tích ngoài Google không sâu bằng công cụ chuyên dụng. | Tốt nếu công ty dùng Google, nhưng kém phù hợp khi doanh nghiệp dùng Teams, Slack, Salesforce hoặc nhiều hệ thống khác. |
| **Microsoft Teams + Copilot** | Chi phí license & hệ sinh thái Microsoft | Các tính năng AI cần license phù hợp; giá trị cao nhất khi công ty đã dùng đầy đủ Microsoft 365. | Nếu chỉ dùng Teams cho họp nhưng không dùng SharePoint/Outlook/Planner, chi phí có thể cao so với nhu cầu. |
| **Zoom AI Companion** | Đa nền tảng & quản trị ngoài Zoom | Mạnh nhất trong Zoom; khả năng quản lý tri thức xuyên nhiều nền tảng không sâu bằng Fireflies hoặc Avoma. | Bất tiện nếu cuộc họp thường xuyên diễn ra trên Google Meet, Teams hoặc offline. |
| **Notta** | Workflow đội nhóm & CRM | Tốt ở transcription và ghi âm nhưng yếu hơn về quản lý action items, CRM sync, coaching và phân tích cuộc họp. | Phù hợp ghi chú cá nhân hơn là vận hành quy trình follow-up của sales hoặc project team. |
| **Sembly AI** | Tiếng Việt & cuộc họp phức tạp | Có thể giảm độ chính xác khi nhiều người nói cùng lúc, âm thanh kém, thuật ngữ chuyên ngành hoặc tiếng Việt không chuẩn. | Các cuộc họp đông người cần review kỹ speaker, decision và task owner. |


---


## Workflow trước và sau khi tối ưu


### 1. Mô tả chi tiết Before/After Impact


| Metric | Trước (Current) | Sau kỳ vọng (Future) | Ghi chú |
|---|---|---|---|
| **Tổng thời gian** | 40 phút/cuộc họp | 5 phút/cuộc họp | Giảm thời gian xử lý sau mỗi cuộc họp. |
| **Số bước** | 4 bước | 4 bước | Quy trình vẫn giữ nguyên, AI giúp transcript và lọc các nội dung chính của cuộc họp. |
| **Bước thủ công** | 4/4 bước | 2/4 bước | AI tự xử lý transcript và tạo biên bản, BA chỉ check review và gửi đi. |
| **Bottleneck chính** | Nghe lại ghi âm + tổng hợp biên bản (30 phút) | BA review nội dung (2 phút) | Mấu chốt của vấn đề chuyển sang việc kiểm chứng xem AI có tổng hợp đúng và chính xác không. |
| **Rủi ro mới** | Bỏ sót thông tin khi ghi chép hoặc nghe lại thủ công | AI có thể tóm tắt sai hoặc thiếu Action Items quan trọng | Khắc phục bằng cách BA bắt buộc phải kiểm tra và xác nhận trước khi gửi (Human-in-the-loop). |


---


## Problem Statement v0


| Field | Nội dung |
|---|---|
| **Actor** | Business Analyst (BA) kiêm nhiệm vai trò thư ký cuộc họp. |
| **Workflow** | 1. Tham gia họp và ghi chép nhanh.<br>2. Nghe lại ghi âm cuộc họp ở các phần thảo luận chưa rõ.<br>3. Tổng hợp và soạn thảo biên bản họp (quyết định, action items) vào tài liệu.<br>4. Gửi biên bản họp cho cả nhóm qua email/Slack. |
| **Bottleneck** | Bước 2 & 3 current state (Nghe lại ghi âm và tổng hợp thông tin có cấu trúc): Nội dung cuộc họp thường diễn ra lộn xộn, không theo trình tự; BA phải mất công bóc tách các điểm cốt lõi và định dạng lại. |
| **Impact** | Mất 30-45 phút/cuộc họp. Với trung bình 4 cuộc họp lấy yêu cầu lớn nhỏ mỗi tuần, BA mất khoảng 120-180 phút/tuần. Báo cáo biên bản muộn làm chậm tiến độ thực hiện các công việc tiếp theo của team. |
| **Success Metric** | - Giảm thời gian tổng hợp xuống dưới 5 phút.<br>- Gửi biên bản họp cho team trong vòng tối đa 30 phút ngay sau khi cuộc họp kết thúc. |
| **Boundary** | Không tự gửi report; không tự bịa insight; không thay PM quyết định nội dung cuối; chỉ dùng dữ liệu được cung cấp của cuộc họp đó. |


---


## Lựa chọn Rule / Workflow / Agent


| Mức | Phương án | Khi nào chọn | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Template ghi chú cố định (agenda, decision, action item) điền tay theo mẫu. | Đủ nếu số lượng meeting ít, nội dung đơn giản, không cần tra cứu lại nhiều. | Vẫn tốn thời gian điền, dễ bỏ sót ý quan trọng khi ghi tay theo thời gian thực. | Không chọn làm toàn bộ, nhưng dùng làm khung cấu trúc đầu ra. |
| **Workflow** | **Ghi âm/transcript cuộc họp $\rightarrow$ AI tóm tắt theo template (decision, action, follow-up) $\rightarrow$ người review/edit trước khi lưu.** | Hợp vì input rõ ràng (transcript thô), output có cấu trúc cố định, ranh giới người-máy dễ xác định. | Tóm tắt sai ý, bỏ sót ngữ cảnh quan trọng nếu transcript bị nhiễu âm thanh. | **CHỌN** |
| **Agent** | Agent tự nghe meeting, tự phân loại action item theo người phụ trách, tự nhắc deadline, tự gửi follow-up. | Chỉ cần nếu có nhiều cuộc họp song song, cần theo dõi action item xuyên suốt nhiều tuần liên tục. | Quá rộng, cần quyền truy cập lịch/task của nhiều người, rủi ro tự động gửi sai thông tin ảnh hưởng đến team. | Chưa chọn |


---


## Problem Statement v1 (Bản hoàn chỉnh sau phản biện)


| Field | Nội dung |
|---|---|
| **Actor** | Business Analyst (BA) kiêm nhiệm vai trò thư ký cuộc họp. |
| **Workflow** | 1. Lấy transcript tự động từ Zoom/Teams sau họp.<br>2. Chạy AI để cấu trúc hóa nội dung thô thành biên bản họp.<br>3. BA tiến hành soát lỗi, xác minh tên người và quyết định cốt lõi.<br>4. Gửi biên bản đã duyệt cho team. |
| **Bottleneck** | Bước 2 & 3 current state (Nghe lại ghi âm và tổng hợp thông tin có cấu trúc): Nội dung cuộc họp thường diễn ra lộn xộn, không theo trình tự; BA phải mất công bóc tách các điểm cốt lõi và định dạng lại. |
| **Impact** | Mất 30-45 phút/cuộc họp. Với trung bình 4 cuộc họp lấy yêu cầu lớn nhỏ mỗi tuần, BA mất khoảng 120-180 phút/tuần. Báo cáo biên bản muộn làm chậm tiến độ thực hiện các công việc tiếp theo của team. |
| **Success Metric** | - Giảm thời gian tổng hợp xuống dưới 5 phút.<br>- Gửi biên bản họp cho team trong vòng tối đa 30 phút ngay sau khi cuộc họp kết thúc.<br>- Đạt tỷ lệ chính xác thông tin được chốt là 100% sau bước review của BA. |
| **Boundary** | AI không tự động gửi biên bản đi; không tự ý tạo ra các quyết định mới không xuất hiện trong transcript; dữ liệu cuộc họp phải được bảo mật nội bộ và không dùng để train các mô hình công cộng. |
| **AI intervention point** | Nằm ở bước **xử lý file transcript thô** để phân loại và cấu trúc hóa thông tin theo template trước khi đưa cho BA duyệt. |
| **Mức chọn** | **Workflow** (Phối hợp tuyến tính giữa công cụ lấy transcript, API AI tóm tắt và BA review). |
| **Rủi ro & Người thật kiểm tra** | **Rủi ro:** AI tóm tắt thiếu hoặc sai các action items quan trọng hoặc gán nhầm người chịu trách nhiệm do transcript bị nhận diện nhầm từ đồng âm.<br>**Người thật kiểm tra:** BA bắt buộc phải đóng vai trò chốt chặn review, đọc soát kỹ bảng quyết định và gán việc trước khi nhấn nút phát hành biên bản. |




