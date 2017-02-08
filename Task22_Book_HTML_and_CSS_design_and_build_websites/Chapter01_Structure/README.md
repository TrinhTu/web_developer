## HTML & CSS
### Text

> Chương 2: Text
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/1/2017

## Mục lục:

[1. Headings and paragraphs](#1)

[2. Bold, italic, emphasis](#2)

[3. Structural and semantic markup](#3)

[Tài liệu tham khảo](#4)

***

Khi tạo 1 trang Web, chúng ta thêm các thẻ, đánh dấu nội dung của từng trang. Các thẻ này cung cấp ý nghĩa cho phép trình duyệt hiển thị cho người dùng cấu trúc phù hợp của trang.

Trong chương này chú trọng tới việc đánh dấu văn bản và cách hiển thị của nó trong trang web của bạn. Chúng ta sẽ tìm hiểu về:

- Cấu trúc đánh dấu: Yếu tố sử dụng để mô tả cả tiêu đề và đoạn văn bản.

- Ý nghĩa của việc đánh dấu: Cung cấp thêm thông tin, cũng như nhấn mạnh vị trí dùng để sử dụng sao cho hợp lí, và ý nghĩa của các từ được viết tắt.

Trước tiên là phần tiêu đề: Phần tiêu đề sử dụng các thẻ từ h1 -> h6 theo cấp độ hiển thị giảm dần

- `<h1>`: Sử dụng như tiêu đề chính

- `<h2>`: Sử dụng như tiêu đề con

...

- `<h6>`: Hiển thị nhỏ nhất

Chúng ta có thể tùy chỉnh kích thước của đoạn text, chỉnh màu sắc, kích cỡ chữ...khi áp dụng CSS.

**Đoạn văn**: 

```javascript
<p>Đây là đoạn văn bản thứ nhất</p>
<p>Đây là đoạn văn bản thứ hai</p>
```

Các đoạn văn bản này được bao bọc bởi thẻ mở và thẻ đóng `<p>`, `</p>`. 

In đậm và in nghiêng:

- Bằng cách sử dụng cặp thẻ `<b>` `</b>` ta có thể làm cho nội dung đó được in đậm và nổi bậc hơn, thẻ `<b>` là yếu tố đại diện cho văn bản, trình bày 1 cách rõ ràng, có nhấn mạnh ý nghĩa nội dung của văn bản.

- Bằng các sử dụng cặp thẻ `<i>` </i>` thì cách hiển thị của nội dung bên trong sẽ được hiển thị nghiêng, thường được sử dụng cho tên, từ khóa riêng...

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.
