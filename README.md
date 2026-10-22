# First Date Quest

Thiệp mời hẹn hò phong cách pixel game. Bạn nữ bấm **CÓ** (nút KHÔNG sẽ bỏ chạy) rồi xem bản đồ lộ trình buổi hẹn đã lên sẵn.

## Sửa lộ trình

Mở `index.html`, tìm khối `const PLAN = { ... }` ở đầu thẻ `<script>`:

- `date`, `pickup`, `dressCode`: thông tin trên vé.
- `stages`: từng chặng gồm `time`, `sprite` (hình pixel), `place`, `desc`, `map` (chữ để tìm trên Google Maps, để `""` nếu không cần link).
- `notes`, `ending`: ghi chú và câu kết.

Danh sách sprite có sẵn được ghi ngay trên khối `PLAN`.

## Deploy

Push lên nhánh `main` là GitHub Actions tự deploy lên GitHub Pages:
https://nguyenha1004.github.io/Date-Plan/

Lần đầu, nếu workflow báo lỗi Pages chưa bật: vào **Settings → Pages → Source**, chọn **GitHub Actions**, rồi chạy lại workflow.
