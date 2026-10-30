# Trang cá nhân học thuật (GitHub Pages)

Trang tĩnh một file, phong cách giống trang của Yake WEI (template Jon Barron). Không cần Jekyll hay build gì cả.

## Cấu trúc

```
index.html       ← nội dung trang (sửa ở đây)
stylesheet.css   ← giao diện
images/          ← ảnh đại diện, ảnh minh hoạ bài báo, favicon
files/           ← đặt CV.pdf ở đây
.nojekyll        ← báo GitHub phục vụ file tĩnh nguyên trạng
```

## Đưa lên GitHub Pages

1. Tạo repo mới tên **`<username>.github.io`** (thay `<username>` bằng tên GitHub của bạn), để Public.
2. Đẩy toàn bộ thư mục này lên nhánh `main`:
   ```bash
   cd site
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin https://github.com/<username>/<username>.github.io.git
   git push -u origin main
   ```
3. Vào **Settings → Pages**, chọn *Source: Deploy from a branch*, nhánh `main`, thư mục `/ (root)`, bấm Save.
4. Sau 1–2 phút trang sẽ có ở `https://<username>.github.io/`.

## Chỉnh nội dung

- Tìm và thay `Your Name`, `Your University`, `Advisor Name`, email, link Google Scholar / GitHub trong `index.html`.
- Ảnh đại diện: thay `images/profile.svg` bằng ảnh của bạn (ví dụ `images/profile.jpg`) và sửa đường dẫn trong `index.html`. Ảnh vuông sẽ đẹp nhất vì được cắt tròn.
- Mỗi bài báo là một khối `<div class="paper">…</div>`. Copy khối đó để thêm bài mới.
  - Thêm class `highlight` (`<div class="paper highlight">`) để tô nền vàng.
  - Nhãn trên ảnh: `<span class="badge hl">HIGHLIGHT</span>`, `<span class="badge venue">WWW</span>`, `<span class="badge oral">ORAL</span>`.
  - Ảnh minh hoạ nên có tỉ lệ khoảng 16:10, rộng ≥ 320px.
- Bỏ mục nào không cần (News, Talks, Honors…) thì xoá cả khối `<section>` tương ứng.
- Nhớ cập nhật dòng "Updated in …" ở cuối trang.

Lưu ý: bài đang nộp ở hội nghị double-blind thì chỉ nên đưa lên trang khi chính sách của hội nghị cho phép (thường là khi đã có bản arXiv).
