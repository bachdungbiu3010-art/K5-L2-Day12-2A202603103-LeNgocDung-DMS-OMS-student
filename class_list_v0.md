# Danh sách lớp v0 — Lê Ngọc Dũng · G09

Danh sách lớp và thuộc tính dự kiến cho DMS/OMS, bám Guideline Cabin v1.0 của bài 12. Bộ ảnh thực hành không đại diện đầy đủ mọi tình huống vận hành. Các câu hỏi cuối bài là câu hỏi đề xuất để làm rõ guideline.

## DMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | face | Box khuôn mặt | Xác định vùng mặt để phân tích mắt và hướng nhìn | Có khi mặt đủ rõ; quay đi hoặc bị che có thể không gán được |
| 2 | eye_left, eye_right | open / closed / unknown | Mô tả riêng trạng thái từng mắt; chuỗi thời gian mới hỗ trợ đánh giá nhắm mắt kéo dài | Có điều kiện; che khuất và phản xạ có thể làm mất thông tin |
| 3 | glasses | none / clear / sun / unknown | Nhận biết kính đang đeo và tình huống hạn chế quan sát mắt | Không luôn xác định được; kính râm có thể trông trong trên NIR |
| 4 | gaze_zone | road / mirror_l / mirror_r / mirror_c / cluster / center / lap / other | Phân loại vùng tài xế đang nhìn để hỗ trợ phân tích chú ý | Có khi quan sát đủ mắt và đầu; không chắc dùng other, ghi lý do |
| 5 | face13 | 13 điểm mắt, mũi, miệng; occluded / outside | Định vị cấu trúc mặt làm đầu vào cho các bước phân tích tiếp theo | Có điều kiện; mặt rộng dưới 60 px chỉ gán box face |
| 6 | hand và on_wheel | whose; side; yes / no / unknown | Xác định tay của ai, bên nào và có chạm vô lăng không | Có khi thấy rõ; on_wheel=no không tự chứng minh hành vi sai trong Drive&Act |
| 7 | phone và state | held / mounted / lap | Nhận biết điện thoại và cách đặt/cầm để mô tả tình huống sử dụng | Có khi nhận ra cạnh, góc hoặc màn hình; không suy từ tư thế tay |
| 8 | person và seatbelt | seat=driver; worn_correct / worn_incorrect / not_worn / unknown | Xác định người lái và trạng thái dây an toàn quan sát được | Có điều kiện; không rõ dải dây thì unknown |

## OMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person | Box người lớn | Xác định người lớn hiện diện ở vị trí ghế | Có khi phần cơ thể đủ rõ; không suy từ vật giống người |
| 2 | seat | driver / front_passenger / rear_left / rear_middle / rear_right | Gắn người hoặc vật với vị trí ghế theo xe | Dựa vào hình học và vị trí trong xe; camera OMS nhìn về sau nên trái ảnh=rear_right |
| 3 | child_seat | Box ghế trẻ em | Phân biệt chiếc ghế trẻ em với người hoặc đồ vật khác | Có thể dựa hình dạng; không đồng nghĩa có trẻ em đang ngồi |
| 4 | child_seat.occupied | no / unknown | Mô tả thấy ghế trống hay không xác định rõ bên trong trong phạm vi bài | Có điều kiện; schema bài 12 không cho yes |
| 5 | infant_seat | Box nôi/ghế em bé dạng xách | Phân biệt loại ghế/nôi với child_seat | Có thể dựa hình dạng; trường hợp mơ hồ cần hỏi coach |
| 6 | infant_seat.facing | rear / front | Mô tả hướng chiếc nôi so với đầu/đuôi xe | Dựa vào cấu trúc và hướng của nôi; không theo hướng nhìn của camera |
| 7 | object và type | bag / box / cup / other | Nhận biết đồ vật mang theo và tránh nhầm với người/ghế trẻ em | Dựa hình dạng, vị trí, ngữ cảnh; không dựa vào màu trên IR |
| 8 | person.seatbelt | not_worn / unknown trên SVIRO | Mô tả trạng thái quan sát được, không tạo nhãn worn_* không có trong bộ này | Có điều kiện; không suy từ ảnh RGB/IR còn lại |

## Hai câu hỏi leo thang

1. **Câu hỏi:** Khi có vật hình em bé giống búp bê trong nôi, có gán riêng object với type=other hay bỏ qua? Tiêu chí phân biệt và box của vật bên trong là gì?
   - **Khung ví dụ:** G09 S01_rgb, S01_ir.
   - **Phương án trong bản export:** nôi có nhãn infant_seat. Câu hỏi nhằm làm rõ vật hình em bé bên trong có cần box riêng theo quy tắc vật nằm trong ghế hay không.

2. **Câu hỏi:** Với cấu trúc ghế có thể bị nhầm giữa child_seat và infant_seat, guideline cần bổ sung đặc điểm nhận dạng nào và xử lý thế nào khi phần tay xách/đế bị che?
   - **Khung ví dụ:** G09 S05_rgb, S05_ir, S06_rgb, S06_ir.
   - **Phương án trong bản export:** child_seat. Câu hỏi nhằm bổ sung tiêu chí hình dạng và cấu trúc để phân biệt nhất quán ghế trẻ em với nôi dạng xách theo Guideline Cabin v1.0.
