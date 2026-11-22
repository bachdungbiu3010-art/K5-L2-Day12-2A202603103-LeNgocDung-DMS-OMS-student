# Tự đánh giá — Lê Ngọc Dũng · G09

## 1. Rà soát bốn khung

Bảng tổng hợp dựa trên các lỗi đã ghi nhận, bản export và kết quả đối chiếu hai file export. Nhận xét từ dữ liệu nhãn được phân biệt với kết luận đúng/sai theo nội dung ảnh.

| Ảnh | Đối tượng | Loại ghi nhận | Ghi chú | Cách xử lý |
|---|---|---|---|---|
| S01_ir | frame_meta | Nhầm modality | Trong quá trình làm đã có modality=rgb trên ảnh _ir; bản mới có modality=ir | Đã sửa trên CVAT và lưu trong export |
| S07_rgb | frame_meta | missing | Bản ghép trước thiếu tag; bản mới có đúng tag, modality=rgb, light=unknown | Đã bổ sung; check_final báo 0 lỗi |
| D01 | face, face13 | Bất đồng thuộc tính/cờ | Bản tôi có gaze_zone=cluster, right_eye_outer.occluded=1; bản đối chiếu dùng road và cờ 0 | Chọn bản tôi: giữ gaze_zone=cluster và right_eye_outer.occluded=1; không thay theo bản đối chiếu |
| D04 | face, face13 | Bất đồng trạng thái mắt/cờ | Hai bản khác eye_left và bốn cờ mắt trái; các nhãn có thể tự nhất quán trong mỗi bản | Chọn bản tôi: giữ trạng thái mắt và cờ điểm của export cá nhân |

## 2. Nhóm sai sót đã ghi nhận và cách tránh

- **Nhóm lỗi nổi bật trong bằng chứng kiểm tra:** frame_meta, với hai biểu hiện là nhầm loại ảnh và bỏ sót tag.
- **Nguy cơ dẫn đến lỗi:** chuyển ảnh mà không kiểm lại thông tin chung; ảnh RGB/IR cùng cảnh dễ bị nhầm khi sao chép hình.
- **Cách tránh:** trước khi chuyển ảnh, đọc tên file; kiểm đúng một frame_meta; đối chiếu modality; giữ light=unknown trên SVIRO; lưu Ctrl+S. Chạy công cụ theo đúng phạm vi checkpoint và lưu log ngay tại mốc thực hiện.

## 3. Bài học từ review chéo

Hai dòng S02 cho thấy bản đối chiếu có occupied=yes ngoài schema, còn unknown của tôi là giá trị hợp lệ. Điều đó giúp phân biệt lỗi quy tắc với bất đồng cần xem nội dung ảnh. Sáu khác biệt thuộc tính face ở OMS cũng cần xét đúng phạm vi yêu cầu, thay vì đổi giá trị chỉ để hai bản giống nhau.

Bài học là phân biệt kết quả kiểm cấu trúc, sự khác nhau giữa hai bản và quyết định chọn bản nộp. Không dùng số dòng thống nhất hoặc mức chồng box để tự khẳng định một người đúng theo ảnh. Sau đối chiếu, tôi quyết định giữ phần gán nhãn cá nhân và ghi rõ quyết định trong từng dòng.

## 4. Phương án đã thống nhất

Ngày 22/11/2026, tôi quyết định dùng bản gán nhãn của mình cho toàn bộ 30 dòng đối chiếu. Export được giữ nguyên; kết quả kiểm kỹ thuật là 22 khung, 22 frame_meta, 0 lỗi, 0 cảnh báo. Quyết định chọn bản không được ghi thành kết luận mọi nhãn đã được coach xác nhận.
