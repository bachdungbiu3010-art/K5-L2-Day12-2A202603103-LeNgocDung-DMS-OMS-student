# Khai báo dùng AI — Lê Ngọc Dũng

**Người học:** Lê Ngọc Dũng — 2A202603103 · **Bộ ảnh:** G09 · **Công cụ:** Codex/ChatGPT.

| # | Nội dung đã hỏi hoặc yêu cầu | Kết quả sử dụng | Cách kiểm lại và giới hạn |
|---|---|---|---|
| 1 | Đọc đề và yêu cầu nộp | Xác định E1–E5, tên file, phạm vi 22 khung và các mốc kiểm | Đối chiếu README, GUIDE, RULES, CHECKPOINTS, SUBMISSION, RUBRIC |
| 2 | Hướng dẫn CVAT: project, task, label, tag, box | Người học tự thao tác trên CVAT local | Kiểm tên file, danh sách đối tượng và thuộc tính; lưu export thực tế |
| 3 | Giải thích seat, facing, occupied, type và face | Áp dụng quy tắc theo xe/theo người, phân biệt OMS/DMS và unknown | Guideline Cabin v1.0; không coi suy đoán là nhãn quan sát |
| 4 | Ghép phần DMS/OMS và kiểm tra export | Giữ bản gốc, ghép khung theo tên, sửa thiếu frame_meta trên CVAT rồi xuất lại | Đối chiếu nguồn từng khung; cabin_check báo 0 lỗi, 0 cảnh báo cho 22 khung |
| 5 | Đối chiếu với Khanh_review cheo.zip | Sinh 30 dòng khác biệt, giải thích quy tắc và phương án giữ nhãn nguồn | Dùng hai export thực tế; ngày 22/11/2026 người học chốt giữ bản cá nhân ở cả 30 dòng (mine); không tự ký nhận thay Khánh hoặc khẳng định nhãn đúng theo ảnh chỉ từ XML |
| 6 | Phân tích IR | Tính số đo cục bộ và soạn 4 dòng ir_log, tách IR_sim/real_IR | Phương pháp và số đo được lưu riêng; không quy số đo toàn ảnh thành kết luận đúng/sai từng nhãn |
| 7 | Soạn danh sách lớp, tự đánh giá và TEAM | Dùng thông tin trong guideline, file xuất và trao đổi để viết báo cáo | Không tự dựng một ca Khánh đúng/tôi sai hoặc xác nhận coach đã trả lời |
| 8 | Giải thích và rà soát exit ticket | Người học gửi phép tính 75/30 = 2,50 giây và giải thích mục đích NIR; sau phản hồi kiến thức đã chốt câu 3 là A, B, C ngày 22/11/2026 | Đáp án cuối trong exit_ticket.md được người học xác nhận sau trao đổi; không ghi là đã làm độc lập không dùng tài liệu |

## Dữ liệu đã trao đổi

Trong buổi đã gửi một số ảnh chụp màn hình CVAT có ảnh cabin. RULES của bài yêu cầu không đưa ảnh cabin cho chatbot AI; nội dung này được khai báo đúng thực tế. Các phép đo bổ sung được chạy cục bộ trên máy, không đưa ảnh vào bộ nộp GitHub.

## Sự thống nhất của người học

Ngày **21/11/2026**, Lê Ngọc Dũng thống nhất định hướng ưu tiên chất lượng dữ liệu và hiệu quả. Ngày **22/11/2026**, người học chốt giữ toàn bộ bản gán nhãn cá nhân và cập nhật 30 dòng đối chiếu thành mine. Các công cụ hỗ trợ và dữ liệu đã dùng được khai báo ở trên; quyết định này không thay thế xác nhận từng dòng của người review hoặc đáp án của coach.
