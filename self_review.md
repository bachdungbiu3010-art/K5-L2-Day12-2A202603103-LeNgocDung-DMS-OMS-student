# Tự đánh giá — Lê Ngọc Dũng · G09

## 1. Rà soát bốn khung

Bảng tổng hợp dựa trên các lỗi đã ghi nhận, bản export và kết quả đối chiếu hai file export. Nhận xét từ dữ liệu nhãn được phân biệt với kết luận đúng/sai theo nội dung ảnh.

| Ảnh | Đối tượng | Loại ghi nhận | Ghi chú | Cách xử lý |
|---|---|---|---|---|
| S01_ir | frame_meta | Nhầm modality | Trong quá trình làm đã có modality=rgb trên ảnh _ir; bản mới có modality=ir | Đã sửa trên CVAT và lưu trong export |
| S07_rgb | frame_meta | missing | Bản ghép trước thiếu tag; bản mới có đúng tag, modality=rgb, light=unknown | Đã bổ sung; check_final báo 0 lỗi |
| D01 | face, face13 | Bất đồng thuộc tính/cờ | Bản tôi có gaze_zone=cluster, right_eye_outer.occluded=1; bản đối chiếu dùng road và cờ 0 | Chọn bản tôi: giữ gaze_zone=cluster và right_eye_outer.occluded=1; không thay theo bản đối chiếu |
| D04 | face, face13 | flag và trạng thái mắt | Chấp nhận eye_left=unknown, bốn cờ mắt trái occluded=1 và mouth_right.outside=1 từ bản Khánh | Đã cập nhật sáu giá trị trong export_final_v2.zip, giữ nguyên tọa độ |

## 2. Nhóm sai sót đã ghi nhận và cách tránh

- **Nhóm lỗi nổi bật trong bằng chứng kiểm tra:** frame_meta, với hai biểu hiện là nhầm loại ảnh và bỏ sót tag.
- **Nguy cơ dẫn đến lỗi:** chuyển ảnh mà không kiểm lại thông tin chung; ảnh RGB/IR cùng cảnh dễ bị nhầm khi sao chép hình.
- **Cách tránh:** trước khi chuyển ảnh, đọc tên file; kiểm đúng một frame_meta; đối chiếu modality; giữ light=unknown trên SVIRO; lưu Ctrl+S. Chạy công cụ theo đúng phạm vi checkpoint và lưu log ngay tại mốc thực hiện.

## 3. Bài học từ review chéo

Hai dòng S02 cho thấy bản đối chiếu có occupied=yes ngoài schema, còn unknown của tôi là giá trị hợp lệ. Điều đó giúp phân biệt lỗi quy tắc với bất đồng cần xem nội dung ảnh. Sáu khác biệt thuộc tính face ở OMS cũng cần xét đúng phạm vi yêu cầu, thay vì đổi giá trị chỉ để hai bản giống nhau.

Ở D04, tôi chấp nhận sáu giá trị Khánh đề xuất về mắt trái và cờ điểm mặt. Trường hợp này giúp tôi chú ý mối liên hệ giữa eye_left=unknown và các điểm mắt trái có occluded=1, đồng thời phân biệt occluded với outside. Tôi cập nhật đúng các giá trị được chọn, giữ nguyên tọa độ và ghi lại kết quả sau sửa. Kết quả đối chiếu không được dùng để tự khẳng định toàn bộ nhãn đều đúng theo ảnh.

## 4. Phương án đã thống nhất

Ngày 22/11/2026, tôi chọn 24 dòng theo bản cá nhân và sửa 6 dòng D04 theo Khánh. Bản sau sửa là export_final_v2.zip; check_final_v2.txt báo 22 khung, 22 frame_meta, 0 lỗi, 0 cảnh báo. Bản trước sửa được giữ lại để đối chiếu.
