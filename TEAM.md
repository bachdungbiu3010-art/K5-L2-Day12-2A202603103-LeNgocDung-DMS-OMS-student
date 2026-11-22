# TEAM — Ngày 12

**Mã bộ ảnh:** G09 · **Hình thức:** cá nhân.

| Họ tên | MSSV | Đã gán đủ 22 ảnh? | Review chéo với | Số dòng đối chiếu đã chốt |
|---|---|---|---|---|
| Lê Ngọc Dũng | 2A202603103 | Có | Nguyễn Bảo Khánh — 2A202603191 | 30 dòng: 24 mine, 6 peer |

## Cá nhân

### LeNgocDung-2A202603103

- **Phần tôi làm:** gán DMS và OMS, lưu export, sửa frame_meta và đối chiếu nhãn với bản của bạn review.
- **Nguồn đối chiếu:** Khanh_review cheo.zip của Nguyễn Bảo Khánh; có 22 khung chung và 30 dòng khác biệt.
- **Điều tôi học được:** ghế theo xe, trái/phải theo người; trạng thái mắt phải nhất quán với cờ điểm bị che; tách tính hợp lệ của giá trị với kết luận đúng/sai theo ảnh.

## Quyết định sau review

Ngày **22/11/2026**, **Lê Ngọc Dũng xác nhận sửa sáu giá trị tại D04.png theo phương án của Khánh**, đồng thời giữ bản cá nhân cho 24 dòng còn lại:

1. face.eye_left: open → unknown.
2. left_eye_outer.occluded: 0 → 1.
3. left_eye_inner.occluded: 0 → 1.
4. left_eye_upper.occluded: 0 → 1.
5. left_eye_lower.occluded: 0 → 1.
6. mouth_right.outside: 0 → 1.

Sáu thay đổi được áp dụng vào export_final_v2.zip. Giữ nguyên tọa độ các box/điểm và nội dung 21 khung còn lại. Bản export_final.zip được giữ làm bằng chứng trước sửa.

Đây là lựa chọn cụ thể do Lê Ngọc Dũng xác nhận dựa trên bản đối chiếu; không được ghi thành chữ ký của Khánh hoặc kết luận của coach đối với toàn bộ nhãn.

## Bản nộp và kết quả kiểm

- **Sau review:** export_final_v2.zip, kiểm bởi check_final_v2.txt.
- **Trước sửa:** export_final.zip, kiểm bởi check_final.txt.
- Cả hai bản có 22 khung, 22 frame_meta và được công cụ kiểm báo 0 lỗi, 0 cảnh báo.

Chi tiết quyết định nằm trong disagreement_log.csv; các công cụ sử dụng được khai báo trong prompts.md.
