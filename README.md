# First Date Quest

Thiệp mời hẹn hò phong cách pixel game, dạng slide. Slide 1 là lời mời: bạn nữ bấm **CÓ** (nút KHÔNG sẽ bỏ chạy) mới sang slide 2, một bản đồ lớn TPHCM vẽ lại kiểu pixel, bấm vào từng điểm để xem chi tiết. Slide 3 là lời kết và ghi chú.

## Sửa lộ trình

Mở `index.html`, tìm khối `const PLAN = { ... }` ở đầu thẻ `<script>` cuối trang:

- `date`, `pickup`, `dressCode`: thông tin trên vé.
- `stages`: từng điểm gồm `time`, `sprite` (hình pixel), `place`, `desc`, `lat`, `lng`.
  Lấy tọa độ: trên Google Maps nhấn giữ (hoặc chuột phải) vào điểm, bấm dòng số `10.xxx, 106.xxx` để sao chép.
- `secretStops`: số điểm "??? sắp mở" hiện trong danh sách.
- `notes`, `ending`: ghi chú và câu kết.

Bản đồ nền lấy từ OpenStreetMap qua CARTO, được thu nhỏ rồi phóng to không làm mượt và đổi sang bảng màu của game để ra kiểu pixel.

## Deploy

Push lên nhánh `main` là GitHub Actions tự deploy lên GitHub Pages:
https://nguyenha1004.github.io/Date-Plan/
