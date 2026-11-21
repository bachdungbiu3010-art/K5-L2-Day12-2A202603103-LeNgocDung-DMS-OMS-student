# TEAM — Ngày 12

**Mã bộ ảnh:** G09 · **Hình thức:** cá nhân.

| Họ tên | MSSV | Đã gán đủ 22 ảnh? | Review chéo với | Số dòng đối chiếu đã phân loại |
|---|---|---|---|---|
| Lê Ngọc Dũng | 2A202603103 | Có | Nguyễn Bảo Khánh — 2A202603191 | 30: 2 mine, 28 ambiguous |

## Cá nhân

### LeNgocDung-2A202603103

- **Phần tôi làm:** gán DMS và OMS, lưu các bản export, bổ sung frame_meta và kiểm tra kết quả. Phần DMS và OMS đều do tôi thực hiện theo xác nhận trong quá trình làm bài.
- **Nguồn đối chiếu:** file Khanh_review cheo.zip được người học cung cấp là bản của Nguyễn Bảo Khánh. So sánh thực tế có 22 khung chung và 30 dòng khác biệt.
- **Điều tôi học được:** ghế gọi theo xe; trái/phải mắt và tay theo người; không nhìn rõ thì unknown; ảnh SVIRO IR-sim khác NIR thật; hai bản giống nhau không tự chứng minh đúng.

## Phương án tôi đã thống nhất

Ngày **21/11/2026**, **Lê Ngọc Dũng đã thống nhất** định hướng ưu tiên **chất lượng dữ liệu và hiệu quả**, đồng thời sử dụng phương án xử lý có AI hỗ trợ:

1. Áp dụng quy tắc và bằng chứng kiểm chứng được. Hai dòng occupied=yes của bản đối chiếu không thuộc bộ giá trị của bài; giữ giá trị unknown hợp lệ trong bản của tôi.
2. Sáu khác biệt thuộc tính face trong OMS được ghi ambiguous và giữ bản tôi, vì OMS chỉ bắt buộc box mặt.
3. Hai mươi hai dòng còn lại được ghi ambiguous và giữ nguyên nhãn nguồn, thay vì chọn một bên chỉ vì có bất đồng. Cách xử lý này bảo toàn dữ liệu và thể hiện đúng mức chắc chắn của bằng chứng.

Việc ghi **đã thống nhất** ở đây là sự xác nhận của **Lê Ngọc Dũng đối với phương án xử lý**. Đây không phải xác nhận tất cả nhãn đều đúng hoặc chữ ký/thông báo quyết định từng dòng của Nguyễn Bảo Khánh.

## Ca guideline cần phân xử

Các ca có verdict=ambiguous trong disagreement_log.csv được bảo lưu theo quy tắc của bài. Hai câu hỏi leo thang có ví dụ cụ thể nằm trong class_list_v0.md.

## Hỗ trợ AI

Codex hỗ trợ giải thích, đối chiếu file và soạn báo cáo. Người học quyết định sử dụng phương án trên. Khai báo chi tiết nằm trong prompts.md.
