## BÀI 42:  ĐỐI TƯỢNG DATE TRONG JAVASCRIPT

> Tài liệu: Đối tượng Date trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 07/04/2017

### Mục lục: 

- [1. Đối tượng Date trong Javascript](#1)

- [2. Định dạng (format) Date trong Javascript](#2)

	+ [2.1 Định dạng ISO](#2.1)

	+ [2.2 Định dạng Long](#2.2)

	+ [2.3 Định dạng Short](#2.3)

	+ [2.4 Định dạng đầy đủ](#2.4)

- [3. Tài liệu tham khảo](#3)

***

<a name= "1"></a>
### 1. Đối tượng Date trong Javascript:

- Để khởi tạo đối tượng thời gian sử dụng cú pháp sau: `var timeObj = new Date();`

- Khi dùng cú pháp này nó sẽ lấy thời gian hiện tại trên máy tính của client.

**Ví dụ:**

```javascript
var dateObj = new Date();
document.write(dateObj);
```

- 4 cách khởi tạo thời gian thông thường:

```javascript
// Thời gian hiện tại
new Date();
 
// Tham số truyền vào là mili giây
new Date(milliseconds);
 
// Tham số truyền vào là chuỗi ngày tháng
new Date(dateString);
 
// Tham số truyền vào gồm
//  - year:         năm
//  - month:        tháng
//  - day:          ngày
//  - hours:        giờ
//  - minutes:      phút
//  - seconds:      giây
//  - milliseconds: mini giây
new Date(year, month, day, hours, minutes, seconds, milliseconds);
```

- Khi truyền tham số vào thì đối tượng đó sẽ tự nhận diện về đúng định dạng ngày tháng. 

**Ví dụ**: Khởi tạo 1 đối tượng với giá trị là ngày 20/11/2013

`var dateObj = new Date(2013, 11, 20);`

<a name="2"></a>
### 2. Định dạng (format) Date trong Javascript:

- Có 3 định dạng chính:

	+ ISO

	+ Long

	+ Short

<a name="2.1"></a>
#### 2.1 Định dạng ISO:

- Định dạng chuẩn nhất của ISO 8601 là (YYYY-MM-DD) hoặc (YYYY-MM) hoặc (YYYY) nếu truyền tham số không đủ (ngày-tháng-năm-giờ-phút-giây) thì mặc định các tham số khác sẽ lấy thời gian nhỏ nhất.

**Ví dụ**:

```javascript
var ISO_1 = new Date("2014-11-20");
var ISO_2 = new Date("2014-11");
var ISO_3 = new Date("2014");
```

<a name="2.2"></a>
#### 2.2 Định dạng Long:

- Định dạng này truyền vào với tên của tháng là 3 chữ cái đầu tiên ghi bằng tiếng anh, có thể đặt vị trí của nó bất kì vì đối tượng Date có thể tự nhận diện và chuyển đổi.

**Ví dụ:**

```javascript
var LONG_1 = new Date("Mar 25 2015");
var LONG_2 = new Date("2015 Mar 25");
var LONG_3 = new Date("25 2015 Mar");
```

<a name="2.3"></a>
#### 2.3 Định dạng Short:

- Định dạng Short được lưu trữ dưới dạng MM/DD/YYYY hoặc YYYY/MM/DD hoặc YYYY-MM-DD

**Ví dụ:**

```javascript
var SHORT_1 = new Date("03-25-2015");
var SHORT_2 = new Date("03/25/2015");
var SHORT_3 = new Date("2015/03/25");
var SHORT_4 = new Date("2015-03-25");
```

<a name="2.4"></a>
#### 2.4 Định dạng đầy đủ:

- Trên những định dạng ghi tắt , nếu truyền đầy đủ phải truyền (ngày-tháng-năm-giờ-phút-giây-timezone)

**Ví dụ:**

`var d = new Date("Wed Mar 25 2015 09:56:24 GMT+0100 (W. Europe Standard Time)");`

<a name="3"></a>
### 3. Tài liệu tham khảo:

> [1] Đối tượng Date trong Javascript. https://freetuts.net/doi-tuong-date-trong-javascript-401.html

