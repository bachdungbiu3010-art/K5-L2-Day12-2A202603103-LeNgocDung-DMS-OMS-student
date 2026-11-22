# Khai báo dùng AI — Lê Ngọc Dũng

**Người học:** Lê Ngọc Dũng — 2A202603103 · **Bộ ảnh:** G09 · **Công cụ:** Codex/ChatGPT.

| # | Nội dung đã hỏi hoặc yêu cầu | Kết quả sử dụng | Cách kiểm lại và giới hạn |
|---|---|---|---|
| 1 | Đọc đề và yêu cầu nộp | Xác định E1–E5, tên file, phạm vi 22 khung và các mốc kiểm | Đối chiếu README, GUIDE, RULES, CHECKPOINTS, SUBMISSION, RUBRIC |
| 2 | Hướng dẫn CVAT: project, task, label, tag, box | Người học tự thao tác trên CVAT local | Kiểm tên file, danh sách đối tượng và thuộc tính; lưu export thực tế |
| 3 | Giải thích seat, facing, occupied, type và face | Áp dụng quy tắc theo xe/theo người, phân biệt OMS/DMS và unknown | Guideline Cabin v1.0; không coi suy đoán là nhãn quan sát |
| 4 | Ghép phần DMS/OMS và kiểm tra export | Giữ bản gốc, ghép khung theo tên, sửa thiếu frame_meta trên CVAT rồi xuất lại | Đối chiếu nguồn từng khung; cabin_check báo 0 lỗi, 0 cảnh báo cho 22 khung |
| 5 | Đối chiếu với Khanh_review cheo.zip | Sinh 30 dòng khác biệt, giải thích quy tắc và phương án giữ nhãn nguồn | Dùng hai export thực tế; người học chốt 24 mine và sửa 6 trường D04 theo peer ngày 22/11/2026; không ký nhận thay Khánh hoặc khẳng định toàn bộ nhãn đúng chỉ từ XML |
| 6 | Phân tích IR | Tính số đo cục bộ và soạn 4 dòng ir_log, tách IR_sim/real_IR | Phương pháp và số đo được lưu riêng; không quy số đo toàn ảnh thành kết luận đúng/sai từng nhãn |
| 7 | Soạn danh sách lớp, tự đánh giá và TEAM | Dùng thông tin trong guideline, file xuất và trao đổi để viết báo cáo | Không tự dựng một ca Khánh đúng/tôi sai hoặc xác nhận coach đã trả lời |
| 8 | Giải thích và rà soát exit ticket | Người học gửi phép tính 75/30 = 2,50 giây và giải thích mục đích NIR; sau phản hồi kiến thức đã chốt câu 3 là A, B, C ngày 22/11/2026 | Đáp án cuối trong exit_ticket.md được người học xác nhận sau trao đổi; không ghi là đã làm độc lập không dùng tài liệu |
| 9 | Cập nhật bản v2 theo giá trị người học chốt | Sửa sáu giá trị tại D04 trong XML export: eye_left=unknown, bốn occluded=1, mouth_right.outside=1 | Tạo export_final_v2.zip từ bản gốc; xác nhận chỉ đổi sáu giá trị, giữ tọa độ và 21 khung khác; cabin_check báo 0 lỗi, 0 cảnh báo. Đây là cập nhật file xuất, không ghi là đã thao tác sửa trên giao diện CVAT |
| 10 | Kiểm file ExportV2.zip vừa xuất từ CVAT | Phát hiện eye_left=open và bốn điểm mắt trái bị đánh outside thay vì occluded; cờ mouth_right.outside còn 0 | Giữ file người học xuất làm bản gốc, chỉnh các thuộc tính/cờ D04 đúng giá trị người học đã chốt. Bản nhãn sau chỉnh khớp phương án v2 đã duyệt, giữ nguyên tọa độ và 21 khung khác; cabin_check báo 0 lỗi, 0 cảnh báo. Cập nhật được thực hiện trên file xuất, không ghi là đã sửa trạng thái trong giao diện CVAT |

## Dữ liệu đã trao đổi

Trong buổi đã gửi một số ảnh chụp màn hình CVAT có ảnh cabin. RULES của bài yêu cầu không đưa ảnh cabin cho chatbot AI; nội dung này được khai báo đúng thực tế. Các phép đo bổ sung được chạy cục bộ trên máy, không đưa ảnh vào bộ nộp GitHub.

## Sự thống nhất của người học

Ngày **21/11/2026**, Lê Ngọc Dũng thống nhất định hướng ưu tiên chất lượng dữ liệu và hiệu quả. Ngày **22/11/2026**, người học chốt 24 dòng theo bản cá nhân và xác nhận sửa sáu giá trị D04 theo Khánh; bảng đối chiếu có 24 mine, 6 peer. Các công cụ hỗ trợ và dữ liệu đã dùng được khai báo ở trên; quyết định này không thay thế xác nhận từng dòng của người review hoặc đáp án của coach.
