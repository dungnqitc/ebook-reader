# Thư mục sách (server library)

Đặt các file `.epub` vào thư mục này rồi khai báo trong `books.json`.

## Cách thêm sách

1. Copy file EPUB vào `ebook-reader/books/`, ví dụ `my-book.epub`.
2. Mở `books.json` và thêm một mục:

```json
{
  "books": [
    {
      "file": "my-book.epub",
      "title": "Tên hiển thị",
      "author": "Tác giả (tuỳ chọn)"
    }
  ]
}
```

- `file` (bắt buộc): tên file EPUB trong thư mục này. Hỗ trợ thư mục con, ví dụ `"truyen/book.epub"`.
- `title` (tuỳ chọn): tên hiển thị trong thư viện. Bỏ trống thì dùng tên file.
- `author` (tuỳ chọn): tên tác giả.

Dạng rút gọn chỉ tên file cũng được chấp nhận:

```json
{ "books": ["book1.epub", "book2.epub"] }
```

## Lưu ý

- Static host (GitHub Pages) không quét được thư mục, nên danh sách phải khai báo thủ công trong `books.json`.
- App fetch file qua HTTP nên cần chạy qua web server (không mở bằng `file://`).
- File mẫu `sample.epub` trong `books.json` chỉ là placeholder — xoá hoặc thay bằng sách thật của bạn.
