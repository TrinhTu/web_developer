##Bài 16: Thuộc tính `display`

> Tài liệu: Thuộc tính `display`
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/10/2016

###Nội dung:

- Block: Các phần tử block nó sẽ được nằm một hàng riêng biệt khi hiển thị. Ví dụ như các thẻ `<div>`, `<li>`, `<ul>`, `<h1>`,..là các block.

- Inline: Các phần tử này sẽ hiển thị trên cùng một hàng trên nội dung khác. Ví dụ như các thẻ `<span>`, `<strong>`, `<a>`,..là các phần tử inline.

Thuộc tính display có một số giá trị cơ bản như:

- inline: Chuyển phần tử về hiển thị trên cùng một hàng.

- inline-block: Chuyển phần tử về hiển thị trên cùng một hàng nhưng nó vẫn thừa hưởng các đặc tính của block như có thể tùy chỉnh kích thước, thêm background,…

- block: Chuyển phần tử về hiển thị kiểu block, sở hữu một hàng riêng.

- list-item: Chuyển phần tử về hiển thị như một mục danh sách, để có thể sử dụng thuộc tính list-style.

- none: ẩn phần tử đó đi không cho hiển thị nữa, nó cũng sẽ ẩn luôn toàn bộ các khoảng trống mà nó sở hữu.

Ví dụ về chuyển từ dạng block sang inline:

![a1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_16/image/a1.png)

Ví dụ về chuyển từ dạng inline sang block:

![a2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_16/image/a2.png)

Trong bài 15 khi tạo danh sách bằng CSS thì chỉ áp dụng cho các thẻ `<li>` vậy còn nếu muốn tạo danh sách cho các thẻ không phải thẻ `<li>` thì ta thêm cho nó thuộc tính display cho nó có giá trị là **list-item**

```
			display: list-item;
```

![a3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_16/image/a3.png)

Ngoài ra chúng ta còn sử dụng thuộc tính display để chia cột cho wesite mà không cần sử dụng float hay clear float như sau:

![a4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_16/image/a4.png)
