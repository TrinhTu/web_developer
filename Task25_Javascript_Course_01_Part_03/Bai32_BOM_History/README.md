## Bài 32: BOM - HISTORY TRONG JAVASCRIPT

> Tài liệu: BOM - History trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/03/2017

## Mục lục:

- [1. History trong Javascript](#1)

	- [1.1 Đếm tổng số trang đã lưu trong history](#1.1)

	- [1.2 Đi tới 1 trang nào đó trong history](#1.2)

- [Tài liệu tham khảo](#2)

***

<a name="1"></a>
### History trong Javascript:

Cũng như `location`, `history` cũng là 1 thành phần con của window nên thông qua đối tượng window để thao tác với `history`. `window.history`

<a name="1.1"></a>
#### 1.1 Đếm tổng số trang đã lưu trong trình duyệtL

Nếu muốn đếm tổng số trang đã lưu trong lịch sử lướt web thì sử dụng cú pháp sau:

```javascript
var totalPage = window.history.length;
```

**Ví dụ:**

```javascript
 <script>
        alert("Tổng số trang đã lưu trong history là: " + window.history.length);
 </script>
```

<a name="1.2"></a>
#### 1.2 Đi tới 1 trang nào đó trong history:

Có 3 phương thức thường dùng để đến 1 trang trong history:

- `history.back()`: trở lại trang trước

- `history.forward()`: đi tới trang kế tiếp

- `history.go(number)`: đi tới 1 trang

	+ `number` < 0: thì tính từ trang hiện tại trừ đi `number`

	+ `number` > 0: tính từ trang hiện tại cộng `number`

**Ví dụ:**

```javascript
// trở lại trang trước
window.history.back();
 
// đi tới trang kế tiếp sau khi sử dụng back()
window.history.forward()
 
// đi tới trang cách đây 5 lần lướt web
window.history.go(-5);
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] BOM - History trong Javascript. http://freetuts.net/bom-history-trong-javascript-387.html