# TEAM — Ngày 12

**Mã bộ ảnh:** G09 · **Hình thức:** cá nhân.

| Họ tên | MSSV | Đã gán đủ 22 ảnh? | Review chéo với | Số dòng đối chiếu đã chốt |
|---|---|---|---|---|
| Lê Ngọc Dũng | 2A202603103 | Có | Nguyễn Bảo Khánh — 2A202603191 | 30 dòng: chọn bản của tôi (mine) |

## Cá nhân

### LeNgocDung-2A202603103

- **Phần tôi làm:** gán đủ DMS và OMS, lưu export, sửa thông tin frame_meta và kiểm tra kết quả.
- **Nguồn đối chiếu:** Khanh_review cheo.zip, được cung cấp là bản của Nguyễn Bảo Khánh. Công cụ so sánh có 22 khung chung và 30 dòng khác biệt.
- **Điều tôi học được:** ghế gọi theo xe; trái/phải mắt và tay theo người; không nhìn rõ thì unknown; tách IR-sim với NIR thật; phân biệt lỗi giá trị không hợp lệ với khác biệt giữa hai bản.

## Quyết định bản nộp

Ngày **22/11/2026**, **Lê Ngọc Dũng quyết định chọn toàn bộ phần gán nhãn của mình** và xác nhận dùng phương án này để nộp bài, theo định hướng ưu tiên chất lượng dữ liệu và hiệu quả.

- Cả 30 dòng trong disagreement_log.csv có verdict=mine, kèm mục guideline và cách xử lý cụ thể.
- Hai dòng occupied=yes của bản đối chiếu không thuộc bộ giá trị của bài; giữ occupied=unknown của bản tôi.
- Các khác biệt còn lại giữ nhãn, thuộc tính, box và điểm của bản cá nhân. Không lấy sự giống nhau với bản đối chiếu làm mục tiêu thay nhãn.
- Bản sử dụng là export_final.zip. Quyết định đối chiếu này giữ nguyên dữ liệu trong export, không tạo một lần sửa nhãn trên CVAT không có thật.

Đây là quyết định chọn bản nộp của **Lê Ngọc Dũng**; không thay cho xác nhận từng dòng của Nguyễn Bảo Khánh hoặc kết luận đúng/sai theo đáp án của coach. Hai câu hỏi leo thang được trình bày trong class_list_v0.md.

## Kết quả kiểm tra

Export có **22 khung**, mỗi khung có đúng một frame_meta. Công cụ kiểm cuối báo **0 lỗi, 0 cảnh báo**. Chi tiết công cụ sử dụng được khai báo trong prompts.md.
