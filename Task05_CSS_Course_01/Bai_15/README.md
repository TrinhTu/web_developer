## Bài 15: Tùy biến hiển thị danh sách (list)

> Tài liệu: Tùy biến hiển thị danh sách
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/10/2016

### Mục lục:

[1. Quy tắc viết thuộc tính list-style](#1)

[2.Sử dụng thuộc tính này cho phần tử nào](#2)

[3. Viết ngắn gọn vào `list-style`](#3)

### Nội dung:

<a name="1"></a>
#### 1. Quy tắc viết thuộc tính list-style:

Với thuộc tính `list-style` này bạn có thể thay đổi tùy chỉnh cách hiển thị danh sách theo ý muốn, tức là thay vì trong HTML thẻ `<ol>` là hiển thị danh sách đánh số thứ tự, `<ul>` danh sách không đánh số thứ tự thì ở đây việc sử dụng thuộc tính `list-style` này nhằm để tự thiết lập cách hiển thị theo ý muốn. Thuộc tính này có các giá trị như sau:

```
list-style: <list-style-type> <list-style-position> <list-style-image>;
```

 3 Giá trị type, position, image là thuộc tính con của `list-style` có thể sử dụng cùng 1 lúc. Trong đó:

- `list-style-type` : thay đổi hiển thị của danh sách

- `list-style-position` tùy chỉnh vị trí hiển thị đầu dòng của mục con nằm bên trong danh sách hoặc bên ngoài danh sách

- `list-style-image` sử dụng hình ảnh để làm các dấu đầu dòng trong danh sách.

<a name="2"></a>
#### 2. Sử dụng thuộc tính này cho phần tử nào:

Thuộc tính `list-style` này chỉ có thể sử dụng cho các phần tử `<li>` trong website, tuy nhiên vẫn có thể sử dụng cho các phần tử có thêm thuộc tính `display: list-style-type`

`list-stype-type` : với giá trị này cần thiết lập kiểu hiển thị cho mỗi dầu dòng bên trong thẻ `<li>`, nó có 1 số giá trị như sau:

- `disc`: kiểu nút tròn có nền bên trong

- `circle`: kiểu nút tròn có nền không có viền

- `squre`: kiểu ô vuông có nền

- `lower-roman`: kiểu số La mã in thường

- `upper-roman`: kiểu số La mã in hoa

- `none` : Xóa các dấu đầu dòng.

![a](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_15/image/a.png)

`list-style-position` : thuộc tính này chỉ có 2 giá trị là : inside và outside.

- `inside` : hiển thị dấu đầu dòng bên trong block

- `outside`: hiển thị dấu đầu dòng bên ngoài block

![b](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_15/image/b.png)

`list-style-image` : thay vì dấu gạch đầu dòng hay dấu chấm tròn bạn có thể sử dụng hình ảnh để hiển thị. Nên sử dụng con trỏ để hiển thị. Cú pháp:

```
		list-style-image: url('link anh');
```
![c](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_15/image/c.png)

<a name="3"></a>
#### 3. Viết ngắn gọn vào `list-style`:

Hoặc ta có thể viết ngắn gọn 3 thuộc tính trên vào 1 dòng mà không cần viết dài dòng như vậy, cú pháp như sau:

```
		list-style: type position image;
```
Mình cần phải thay cái thuộc tính tương ứng theo đúng thứ tự như trên. Lưu ý nếu như sử dụng image thì không cần khai báo type, còn khai báo type thì không cần khai báo image.
