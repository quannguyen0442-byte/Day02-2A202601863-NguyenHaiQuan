03 — Individual Reflection
Đóng góp của Quan trong nhóm
Hoạt động | Quan đã làm gì? | Kết quả |
Scan cá nhân | Đưa ra các problems theo 4 lăng kính, trong đó có candidate "Dự đoán giờ xe buýt đến / Tình trạng còn trống" thuộc cluster Giao thông công cộng | Candidate được đưa vào shortlist chung của nhóm (9-12 candidates từ 3-4 người) |
Shortlist & Score | Cùng nhóm đánh giá candidate của mình theo 7 tiêu chí (Actor rõ, Workflow rõ, Pain có evidence, Impact đo được, Làm trong lab, So sánh R/W/A, Nhóm hiểu domain) | Giao thông công cộng đạt 28/35 điểm — thấp hơn Báo cáo tổng hợp thông tin (35) và Nghiên cứu/thu thập tài liệu (29), do "Pain có evidence" và "Impact đo được" chỉ đạt 3-4/5 |
Challenge | Tham gia thảo luận vì sao không chọn các bài khác, trong đó nhóm chỉ ra Giao thông công cộng thiếu thông tin real-time để làm bằng chứng pain rõ ràng | Nhóm quyết định chọn "Báo cáo tổng hợp thông tin" vì có baseline thời gian rõ và validate được nhanh với PM/BA khác |
Workflow | Cùng nhóm vẽ current/future workflow cho bài chọn (biên bản họp: BA nghe ghi âm → tổng hợp → review → gửi) | Xác định rõ bottleneck ở bước 2-3 (nghe lại ghi âm + tổng hợp, mất 30 phút) |
Research | Cùng nhóm research 10+ tool có sẵn trên thị trường (Otter.ai, Fireflies.ai, Fathom, Avoma, tl;dv, Google Meet + Gemini, Teams + Copilot, Zoom AI Companion, Notta, Sembly AI) | Thấy rõ pattern: các tool đều mạnh ở transcript/summary nhưng yếu ở tiếng Việt, governance, hoặc workflow phê duyệt nội bộ — nhóm không cần build lại transcript engine từ đầu |
Rule/Workflow/Agent | Cùng nhóm lập luận chọn Workflow, không chọn Agent, cho bài "Báo cáo tổng hợp thông tin" | Thống nhất: AI xử lý transcript + tạo draft biên bản, BA vẫn review và gửi (human-in-the-loop) |


Bảng dùng AI trong reflection
Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
Scan | Gợi ý thêm problems theo 4 lăng kính (lặp lại, tốn thời gian, AI tốt hơn, pain từ người khác) | Giúp mở rộng góc nhìn ngoài pain cá nhân (ví dụ pain từ nhóm bạn cùng tuyến xe) | Một số ý về "dự đoán giờ xe buýt" nghe hấp dẫn nhưng thiếu evidence cụ thể, chỉ dựa trên cảm nhận cá nhân | Khi nhóm score lại, tôi thừa nhận "Pain có evidence" của candidate mình chỉ đạt 3/5 vì chưa có số liệu thực tế đo lường |
Shortlist & Score | Không dùng AI để tự chấm điểm — nhóm tự thảo luận và cho điểm dựa trên thực tế | (Không áp dụng ở bước này) | (Không áp dụng) | Không sửa gì, giữ nguyên cách chấm điểm thủ công để đảm bảo tính khách quan giữa các thành viên |
Workflow | Nhờ AI hỗ trợ mô tả workflow current/future thành các bước rõ ràng | Nhanh hơn khi liệt kê bước và xác định bottleneck (bước 2-3: nghe ghi âm + tổng hợp) | AI ban đầu có xu hướng gộp bước "tổng hợp" và "review" thành một, làm mờ ranh giới human-in-the-loop | Tách lại rõ: AI tạo draft biên bản, BA là người review/edit/gửi cuối cùng |
Research | Nhờ AI tổng hợp danh sách tool tương tự trên thị trường (Otter.ai, Fireflies, Fathom, Avoma...) và điểm yếu của từng tool | Giúp nhóm thấy nhanh domain yếu chính và điểm yếu cụ thể của từng sản phẩm mà không cần đọc hết 10 trang review | Một vài nhận định về "tác động thực tế" khá chung, chưa có nguồn dẫn chứng cụ thể | Chỉ giữ lại các điểm so sánh có thể kiểm tra được (tính năng, domain phù hợp), bỏ các claim tác động không rõ nguồn |
Problem Statement | Nhờ AI phản biện field còn thiếu trong Problem Statement (ví dụ Boundary, AI intervention point ở v1 còn để trống) | Chỉ ra Success metric và Boundary cần cụ thể hơn ("giảm xuống dưới 5 phút" cần gắn với baseline 30-45 phút rõ ràng) | AI có xu hướng gợi ý thêm quyền hạn cho AI (tự gửi report) sớm hơn mức cần thiết | Nhóm giữ nguyên Boundary chặt: AI không tự gửi report, không tự bịa insight, không thay PM quyết định nội dung cuối |

Bài học của Quan
Ý tưởng nghe "đau" hoặc thú vị với cá nhân (như bài xe buýt của tôi) không đồng nghĩa là problem tốt nhất cho nhóm — thiếu evidence và impact đo được cụ thể là lý do chính khiến nó bị loại (28/35 so với 35/35 của bài được chọn).
Vẽ workflow trước/sau giúp nhóm thấy rõ Rule đã đủ ở đâu (template ghi chú cố định) và AI thực sự tạo giá trị ở đâu (bước tổng hợp transcript lộn xộn thành biên bản có cấu trúc).
Research tool có sẵn trên thị trường không phải để copy, mà để tránh build lại thứ đã tồn tại — nhóm thấy rõ pattern chung: các tool tốt đều để AI draft, con người review, đúng với hướng Workflow (không phải Agent) mà nhóm chọn.
Agent không phải đích đến mặc định: dù bài toán "dự đoán giờ xe buýt" của tôi có vẻ hợp với Agent (tự động theo dõi liên tục), nhóm cuối cùng chọn bài khác đơn giản hơn nhưng có ranh giới người-máy rõ ràng và dễ validate trong thời gian lab.

Nếu làm lại:
Tôi sẽ thu thập số liệu thực tế (log giờ xe đến trong 1-2 tuần) trước khi pitch candidate của mình, để "Pain có evidence" và "Impact đo được" đạt điểm cao hơn — thay vì chỉ dựa vào trải nghiệm cá nhân của tôi khi thuyết trình trước nhóm.