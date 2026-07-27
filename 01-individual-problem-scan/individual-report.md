Nhân vật: Quan và nhóm học viên AI thực chiến tại VinUni. Hàng ngày Quan và các bạn phải đi đến trường bằng xe buýt, học và làm bài tập tại trường và ở nhà.
# Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật
| ----- | ----- | ----- | ----- |
| 1. Lặp lại | Chuẩn bị đồ trước khi ra khỏi nhà | Quan | Quan phải mất 5 phút để chuẩn bị đồ trước khi ra khỏi nhà |
| 2. Lặp lại | Chuẩn bị đồ trước khi ra khỏi nhà bằng trí nhớ | Quan | Quan thường xuyên quên đồ khi ra khỏi nhà và phải quay lại lấy|
| 3. Lặp lại | Kiểm tra task và lịch học vào mỗi buổi sáng| Quan | Quan thường xuyên phải mất 15 phút để kiểm tra task và lịch học vào mỗi buổi sáng|
| 4. Lặp lại | Tự nhắc giờ ra khỏi nhà để kịp giờ xe buýt không có hệ thống nhắc nhở | Quan | Quan thường đặt giờ cố định 7:45 dù giờ xe dao động|
| 5. Tốn thời gian | Chờ xe buýt tại trạm không biết giờ chính xác | Quan | Chờ dư 10 - 15 phút/ngày |
| 6. Tốn thời gian | Tổng hợp lại notes sau mỗi buổi học | Quan | 20-30 phút/buổi để chép lại |
| 7. AI có thể tốt hơn | Không có dự đoán giờ xe đến dựa trên pattern (thứ trong tuần, thời tiết) | Quan | Luôn phải đoán, không có cơ sở dữ liệu |
| 8. AI có thể tốt hơn | Không có gợi ý ưu tiên ôn tập dựa trên độ khó/tần suất xuất hiện của chủ đề | Quan | Ôn dàn trải, không rõ nên tập trung phần nào |
| 9. AI có thể tốt hơn | Tra cứu lại tài liệu bootcamp thủ công khi cần nhớ lại kiến thức cũ | Quan | Mất thời gian lục lại file/slide cũ |
| 10. Pain từ người khác | Bạn cùng tuyến xe buýt cũng gặp tình trạng chờ không rõ giờ, không có kênh báo tin real-time | Nhóm học viên cùng tuyến | Nhiều người cùng chờ dư, không ai chia sẻ tin |
| 11. Pain từ người khác | Nhóm bạn học hay hỏi lại nhau cách làm bài tập vì không có nơi lưu chung dễ tìm | Nhóm học viên cùng lớp | Hỏi lặp lại câu hỏi cũ trong group chat | 

## Top 3
| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
| ---- | ------- | --------- | ----------------- |
| 1 | Dự đoán giờ xe buýt đến | Pain có thật, lặp lại hằng ngày, đo được bằng phút chờ dư | Chất lượng dự đoán phụ thuộc lượng data log thu thập được |
| 2 | Kênh chia sẻ tình trạng xe (đông/vắng khách, dơ/sạch) trong nhóm bạn | Impact rộng hơn (nhiều người cùng đau), tận dụng data từ #1 | Cần đủ số người tham gia mới có giá trị (network effect) |
| 3 | Checklist chuẩn bị đồ trước khi ra cửa | Dễ làm, đo rõ (số lần quên đồ) | Impact nhỏ, thiên về habit-tracking hơn là bài toán cần AI |

Problem Card #1 — Dự đoán giờ xe buýt đến

Problem 1 câu:
Mỗi sáng Quan phải đến trạm xe buýt sớm và chờ một khoảng thời gian không cố định vì không có cơ sở để ước lượng chính xác giờ xe tới, gây lãng phí thời gian lặp lại mỗi ngày.

Actor:
Quan, học viên di chuyển đến trường bằng xe buýt mỗi sáng.

Thời điểm / bối cảnh:
Mỗi sáng ngày học, trước 8h, tại trạm xe buýt gần nhà.

Current workflow:

1. 7:45 rời nhà (giờ cố định, không dựa trên dữ liệu nào)
2. Khoảng 7:55 đến trạm
3. Chờ, không biết chính xác lúc nào xe tới
4. Thỉnh thoảng kiểm tra app/nhìn đường
5. Khoảng 7:50–8:15 xe đến (dao động), lên xe

Bottleneck:
Bước 3 — chờ mà không có dự đoán, nên phải "chờ dư" ra một khoảng an toàn thay vì canh giờ chính xác.

Impact:
Trung bình mất thêm khoảng 10–15 phút/ngày chờ dư × 5 ngày/tuần ≈ 50–75 phút/tuần lãng phí.

Success metric:
Giảm phút chờ dư trung bình từ ~12 phút/ngày xuống dưới 5 phút/ngày; độ lệch giữa giờ dự đoán và giờ thực tế dưới 3 phút.

Non-AI alternative:
Hỏi bạn cùng tuyến qua nhóm chat, hoặc dùng giờ biểu cố định của xe buýt công cộng, nhưng giờ thực tế hay lệch do kẹt xe/thời tiết nên độ chính xác thấp.

AI hypothesis:
Dùng log giờ xe đến thực tế (ghi theo thứ trong tuần, thời tiết) để dự đoán giờ đến hôm sau và gợi ý giờ nên rời nhà. Quan vẫn tự quyết định giờ đi.

Quick gut:
Workflow (thu thập log + mô hình dự đoán đơn giản, chưa cần agent).

Draft current workflow:
CURRENT STATE — ~12 phút chờ dư/ngày

[Rời nhà 7:45 cố định] → [Đến trạm 7:55] → [Chờ không rõ giờ] <-- bottleneck
→ [Xe đến 8:05–8:15] → [Lên xe]

Draft future workflow:
FUTURE STATE — dưới 5 phút chờ dư/ngày

[Ghi log giờ xe hằng ngày] → [Model dự đoán giờ đến] → [Gợi ý giờ rời nhà]
<-- human boundary: Quan tự quyết định giờ đi thực tế -->
→ [Rời nhà đúng giờ dự đoán] → [Đến trạm sát giờ xe] → [Lên xe]

Fallback: dự đoán sai lệch nhiều → Quan tự canh giờ như cũ.

Problem Cards #2 và #3 — tóm tắt
| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1|
| --- | --- | --- | --- | --- | --- |
| Kênh chia sẻ tình trạng xe | Nhóm bạn cùng tuyến | Không ai báo tin real-time khi xe trễ/sớm | Số bạn biết tin trễ trước khi ra trạm: 0 → phần lớn nhóm | Workflow / Rule đơn giản (broadcast tin nhắn) | Cần đủ người tham gia mới có giá trị, phụ thuộc hành vi cả nhóm |
| Checklist chuẩn bị đồ | Quan | Kiểm tra bằng trí nhớ, dễ quên | Số lần quên đồ/tuần | No AI / Rule (checklist tĩnh) | Impact nhỏ, không thật sự cần AI |