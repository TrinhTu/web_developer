## BÀI 45: TÌM HIỂU JAVASCRIPT HOISTING

> Tài liệu: Tìm hiểu Javascript Hoisting
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 07/04/2017

### Mục lục: 

[1. Hoisted trong Javascript](#1)

[2. Không phải hoisted trong Javascipt](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Hoisted trong Javascript:

- Trong Javascript có thể sử dụng 1 biến trước và định nghĩa sau.

**Ví dụ:**

```javascript
// Gán nhưng chưa khai báo biến
domain = 'https://github.com';
 
// In giá trị
document.write("Domain là: " + domain);
 
// Khai báo
var domain;
 
// In lại
document.write("<br/> Domain là: " + domain);
```

- Nếu trong lúc khởi tạo mà gán giá trị cho biến thì kết quả sẽ khác.

```javascript
// Gán nhưng chưa khai báo biến
domain = 'https://freetuts.net';
 
// In giá trị
document.write("Domain là: " + domain);
 
// Khai báo
var domain = 'http://course.freetuts.net';
 
// In lại
document.write("<br/> Domain là: " + domain);
```

- Nhưng nếu viết cách khai báo biến trước khi sử dụng thì ta vẫn có kết quả giống nhau.

```javascript
// Khai báo
var domain;
 
// Gán nhưng chưa khai báo biến
domain = 'https://freetuts.net';
 
// In giá trị
document.write("Domain là: " + domain);
 
// In lại
document.write("<br/> Domain là: " + domain);
```

- Đây là cách viết chuẩn nhất gọi là hoisting - khai báo biến nằm trên cùng của đoạn mã script.

<a name="2"></a>
### 2. Không phải hoisted trong javascript:

- Trong Javascript hoists chỉ tồn tại khi khai báo biến chứ không tồn tại khi gán giá trị ban đầu cho biến.

**Ví dụ:** 

```javascript
var domain = "github.com";
var email = "tutrinh@gmail.com";

document.write("domain là:" + domain);
document.write("<br/> Email là:" + email);
```

Trong ví dụ này khai báo và gán giá trị khởi tạo luôn.

**Ví dụ:**

```javascript
var domain = 'https://github.com';
 
document.write("Domain là: " + domain);
 
document.write("<br/> Email là: " + email);
 
var email = 'tutrinh@gmail.com';
```

Trong ví dụ này sử dụng rồi mới khai báo. Vậy nên giá trị của Email là `undefined`.

<a name="3"></a>
### 3. Tài liệu tham khảo:

> [1] Tìm hiểu javascript Hoisting. https://freetuts.net/tim-hieu-javascript-hoisting-403.html

