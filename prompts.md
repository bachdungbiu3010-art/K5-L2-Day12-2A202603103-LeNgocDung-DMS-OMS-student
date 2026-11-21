# Khai báo dùng AI — Lê Ngọc Dũng

**Người học:** Lê Ngọc Dũng — 2A202603103 · **Bộ ảnh:** G09 · **Công cụ:** Codex/ChatGPT.

| # | Nội dung đã hỏi hoặc yêu cầu | Kết quả sử dụng | Cách kiểm lại và giới hạn |
|---|---|---|---|
| 1 | Đọc đề và yêu cầu nộp | Xác định E1–E5, tên file, phạm vi 22 khung và các mốc kiểm | Đối chiếu README, GUIDE, RULES, CHECKPOINTS, SUBMISSION, RUBRIC |
| 2 | Hướng dẫn CVAT: project, task, label, tag, box | Người học tự thao tác trên CVAT local | Kiểm tên file, danh sách đối tượng và thuộc tính; lưu export thực tế |
| 3 | Giải thích seat, facing, occupied, type và face | Áp dụng quy tắc theo xe/theo người, phân biệt OMS/DMS và unknown | Guideline Cabin v1.0; không coi suy đoán là nhãn quan sát |
| 4 | Ghép phần DMS/OMS và kiểm tra export | Giữ bản gốc, ghép khung theo tên, sửa thiếu frame_meta trên CVAT rồi xuất lại | Đối chiếu nguồn từng khung; cabin_check báo 0 lỗi, 0 cảnh báo cho 22 khung |
| 5 | Đối chiếu với Khanh_review cheo.zip | Sinh 30 dòng khác biệt, giải thích quy tắc và phương án giữ nhãn nguồn | Dùng hai export thực tế; 2 mine và 28 ambiguous theo phương án người học thống nhất; không tự ký nhận thay Khánh |
| 6 | Phân tích IR | Tính số đo cục bộ và soạn 4 dòng ir_log, tách IR_sim/real_IR | Phương pháp và số đo được lưu riêng; không quy số đo toàn ảnh thành kết luận đúng/sai từng nhãn |
| 7 | Soạn danh sách lớp, tự đánh giá và TEAM | Dùng thông tin trong guideline, file xuất và trao đổi để viết báo cáo | Không tự dựng một ca Khánh đúng/tôi sai hoặc xác nhận coach đã trả lời |
| 8 | Giải thích exit ticket | Soạn lời giải có giải thích cho 3 câu | Khai báo trực tiếp trong exit_ticket.md là lời giải có AI hỗ trợ; không ghi đã làm độc lập |
| 9 | Đọc cách nộp và cập nhật GitHub | Đưa file bài làm vào thư mục gốc, kiểm tên và loại dữ liệu | Giữ ảnh cabin và bản export của người đối chiếu ở máy; chỉ đưa dữ liệu nhãn và báo cáo của bài làm lên repo |

## Dữ liệu đã trao đổi

Trong buổi đã gửi một số ảnh chụp màn hình CVAT có ảnh cabin. RULES của bài yêu cầu không đưa ảnh cabin cho chatbot AI; nội dung này được khai báo đúng thực tế. Các phép đo bổ sung được chạy cục bộ trên máy, không đưa ảnh vào bộ nộp GitHub.

## Sự thống nhất của người học

Ngày **21/11/2026**, **Lê Ngọc Dũng đã thống nhất** định hướng ưu tiên chất lượng dữ liệu và hiệu quả, sử dụng các báo cáo có AI hỗ trợ và phương án bảo toàn nhãn nguồn khi thiếu căn cứ phân xử. Sự thống nhất này là quyết định sử dụng phương án của người học; không thay thế xác nhận của người review hoặc đáp án của coach.
