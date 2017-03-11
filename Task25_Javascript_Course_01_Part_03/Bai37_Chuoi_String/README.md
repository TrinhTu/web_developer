## Bài 37: CHUỖI (STRING) TRONG JAVASCRIPT

> Tài liệu: Chuỗi (string) trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 11/03/2017

## Mục lục:

[1. Chuỗi (String) trong javascript](#1)

[2. Nối chuỗi trong Javascript](#2)

[3. Ép sang kiểu chuỗi String trong Javascript](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Chuỗi (String) trong javascript:

Chuỗi là 1 đoạn text có thể có 1 hoặc nhiều kí tự và thường được lưu trữ vào 1 biến, biến này có kiểu dữ liệu là String (chuỗi). Tất cả các chuỗi đều phải bao quanh bằng dấu nháy đơn hoặc nháy đôi. 

**Ví dụ:** 

```javascript
var website = "trello.com";
var email = 'tutrinh@gmail.com';
```

Trường hợp trong chuỗi cũng có xuất hiện dấu nháy đơn hoặc nháy đôi thì bắt buộc phải thêm kí tự `\` đằng trước dấu nháy để không bị lỗi cú pháp.

**Ví dụ:**

```javascript
var message = "Học lập trình \"thật\" thú vị";
var domain = 'chuoi \'string\'';
```

Ngoài ra còn nhiều kí hiệu kết hợp với dấu `\` như trong bảng dưới đây:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai37_Chuoi_String/4.png"/></p>

<a name="2"></a>
### 2. Nối chuỗi trong Javascript:

Để nối chuỗi sử dụng dấu `+` để ghép 2 chuỗi lại với nhau.

**Ví dụ:**

`var message = "Chào các bạn" + "Chúc các bạn học tốt";`

**Hoặc**

```javascript
var a1 = "Chào các bạn";
var a2 = "Chúc các bạn học tốt";
//nối 2 chuỗi
var a = a1 + a2;
```

**Lưu ý khi xuống hàng của chuỗi trong Javascript**

- Khi muốn enter xuống hàng 1 chuỗi trong Javascript bắt buộc phải sử dụng dấu `+` để nối chuỗi nếu không sẽ bị lỗi cú pháp. Ví dụ:

```javascript
// đúng
var message = "Xin chào"
			+ "Buổi sáng";
// Sai
var message = "Xin chào
			buổi sáng";
```

Có thể viết ngắn gọn hơn bằng cách sử dụng dấu `\` để thông báo cho trình duyệt biết là xuống hàng. Ví dụ:

```javascript
var message = "Xin chào \ 
			buối sáng";<br />
```

<a name="3"></a>
### Ép sang kiểu chuỗi String trong Javascript:

Muốn ép 1 giá trị nào đó sang kiểu chuỗi String sử dụng cú pháp `string.toString()`

**Ví dụ:**

```javascript
// Trước khi chuyển đổi
var number = 12;
alert(typeof number);
 
// Sau khi chuyển đổi
number = number.toString();
alert(typeof number);
```

Từ khóa `typeof vars` sẽ trả về kiểu dữ liệu của biến `vars` ngoài ra còn có thể sử dụng đối tượng String để tạo 1 chuỗi với từ khóa `new` phía trước. 

**Ví dụ:**

```javascript
var message = new String("Nếu cố gắng thành công sẽ đến với bạn");
```

Trong trường hợp này dù truyền tham số bất kì thì nó vẫn trả về kiểu String, tuy nhiên đối với cách này thì chương trình sẽ chạy chậm hơn.

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Chuỗi String trong Javascript. http://freetuts.net/chuoi-string-trong-javascript-392.html