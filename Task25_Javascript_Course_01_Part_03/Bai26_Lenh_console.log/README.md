## Bài 26: LỆNH `console.log` KẾT HỢP VỚI FIREBUG TRONG JAVASCRIPT

> Tài liệu: Lệnh console.log kết hợp với Firebug trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 06/03/2017

## Mục lục:

[1. Lệnh console.log() trong javascript](#1)

[Tài liệu tham khảo](#2)

***

Trong Javascript có 1 hàm thường sử dụng debug là hàm `console()` có nhiệm vụ hiển thị giá trị của tất cả các loại dữ liệu như: `number`, `integer`, `object` để biết biến đó có giá trị gì thì sử dụng hàm `console.log()`

<a name="1"></a>
### 1. Lệnh console.log() trong javascript: 

Lệnh console.log() có cú pháp `console.log(value)` trong đó value là biến hoặc giá trị muốn in ra. 

**Ví dụ 1**: console.log() một biến bình thường

```
var website = 'letutrinh';
console.log(website);
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai26_Lenh_console.log/image/1.png"/></p>

**Ví dụ 2**: console.log() một mảng

```
var website = ["Tú Trinh", "Trinh Tú", "Lê Tú", "Trinh Lê"];
console.log(website);
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai26_Lenh_console.log/image/2.png"/></p>

**Ví dụ 3**: console.log() một giá trị

```
console.log("Chào mừng đến với trang web của Trinh");
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai26_Lenh_console.log/image/3.png"/></p>

**Ví dụ 4**: console.log() một object

```
var info = {
	website: "letutrinh.com",
	email: "letutrinh.ktmm@gmail.com",
	address: "Quang Ngai"
};
console.log(info);
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai26_Lenh_console.log/image/4.png"/></p>

Việc sử dụng hàm `console.log()` giúp in ra tất cả giá trị của 1 biến để dễ dàng cho việc debug.

<a name="2"></a>
### Tài liệu tham khảo:

> Lệnh console kết hợp lệnh firebug trong javascript. http://freetuts.net/lenh-consolelog-ket-hop-voi-firebug-trong-javascript-381.html

