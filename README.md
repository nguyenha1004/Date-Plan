# First Date Quest

Thiệp mời hẹn hò phong cách pixel game, dạng slide. Slide 1 là lời mời: bạn nữ bấm **CÓ** (nút KHÔNG sẽ bỏ chạy) mới sang slide 2, một bản đồ game pixel tự vẽ (sông, cầu, khu phố, cây), bấm vào từng điểm để xem chi tiết. Slide 3 là lời kết và ghi chú.

## Sửa lộ trình

Mở `index.html`, tìm khối `const PLAN = { ... }` ở đầu thẻ `<script>` cuối trang:

- `date`, `pickup`, `dressCode`: thông tin trên vé.
- `stages`: từng điểm gồm `time`, `sprite` (hình pixel), `place`, `desc`. Các điểm tự xếp dọc con đường theo thứ tự, tối đa 6 điểm (tính cả điểm bí mật).
- `secretStops`: số điểm "??? sắp mở" hiện trong danh sách.
- `notes`, `ending`: ghi chú và câu kết.

Bản đồ được vẽ bằng canvas ngay trong trang (hàm `drawWorld`), không tải gì từ bên ngoài. Vị trí các điểm nằm trong mảng `SLOTS`.

## Deploy

Push lên nhánh `main` là GitHub Actions tự deploy lên GitHub Pages:
https://nguyenha1004.github.io/Date-Plan/
