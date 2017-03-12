## Bài 40: ĐỐI TƯỢNG NUMBER TRONG JAVASCRIPT

> Tài liệu: Đối tượng number trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/03/2017

## Mục lục:

- [1. Đối tượng Number trong Javascript](#1)

- [2. Xử lý Number trong Javascript](#2)

	- [2.1 Chuyển Number sang string](#2.1)

	- [2.2 Số Infinity](#2.2)

	- [2.3 NaN - Not a Number](#2.3)

	- [2.4 Numbers - Objects](#2.4)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Đối tượng Number trong Javascript:

- Trong Javascript có 2 giá trị lưu trữ trong `Number` đó là dấu chấm động và không có dấu chấm động.

**Ví dụ:**

```javascript
var x = 12; // không có dấu chấm động
var y = 12.5; //có dấu chấm động
```

- Nếu như 1 số lớn thì có thể dùng số mũ để biểu diễn.

**Ví dụ:**

```javascript
var x = 123e5; //giá trị của nó là 12300000
var y = 123e-5; // giá trị của nó là 0.00123
```

- Trong Javascript các số luôn có 64 bit và kiểu float vậy nên không thể định nghĩa các kiểu dữ liệu như `integer`, `short`, `long`,... khi làm việc với các chữ số chỉ có khái niệm `Number`. Ngoài ra còn có thể biểu diễn giá trị của `Number` ở dạng nhị phân, thập phân, thập lục phân,...

**Ví dụ:**

`var x = 0xFF;  // x có giá trị bằng 255`

- Trong Javascript tất cả các dữ liệu liên quan đến những con số đều có kiểu dữ liệu là `Number`, sử dụng hàm `typeof` thì nso sẽ trả về là `number`.

**Ví dụ:**

```javascript
var x = 123;
var y = 1.23;
typeof 12;	//number
typeof x;	//number
typeof y;	//number
```

<a name="2"></a>
### 2. Xử lý Number trong Javascript:

<a name="2.1"></a>
#### 2.1 Chuyển Number sang String:

- Để chuyển 1 biến đang ở kiểu 	`Number` sang kiểu `string` thì sử dụng phương thức `number.toString(type)`. Hàm này có 1 số tham số truyền vào là `type` - đây là kiểu dữ liệu muốn chuyển về, mặc định là hệ thập phân (10)

- Danh sách các cơ số thông dụng:

	+ Hệ nhị phân (2)

	+ Hệ bát phân (8)

	+ Hệ thập phân (10)

	+ Hệ thập lục phân (8)

**Ví dụ:**

```javascript
var myNumber = 128;
myNumber.toString(16);	//returns 80
myNumber.toString(8);	//returns 200
myNumber.toString(2);	//returns 10000000
```

<a name="2.2"></a>
#### 2.2 Số Infinity:

- Đây cũng là 1 kiểu dữ liệu `Number`, khi 1 biến có giá trị là `Infinity` thì nó đã vượt mức lưu trữ cho phép, nên mặc định nó sẽ chuyển về dạng này

**Ví dụ:** Sử dụng vòng lặp While để lặp cho tới khi biến `myNumber` có giá trị `Infinity`:

```javascript
 var myNumber = 2;
    while (myNumber != Infinity) {
        myNumber = myNumber * myNumber;
    }
    document.write("Giá trị của myNumber là: " + myNumber);
```

<a name="2.3"></a>
#### 2.3 NaN - Not a Number:

Nếu thực hiện 1 phép toán nào liên quan đến Number mà vi phạm quy tắc tính toán thì kết quả trả về 1 giá trị gọi là `NaN` (not a number)

**Ví dụ:**

```javascript
var x = 2/"abc"; 	//NaN
var x = 100/"10"; 	//Kết quả = 10
```

- Để kiểm tra 1 biến nào đó có phải là `NaN` hay không thì sử dụng hàm `isNaN()`

**Ví dụ:**

```javascript
  var x = 2/"s";
    if (isNaN(x)){
        document.write("NaN");
    }
```

<a name="2.4"></a>
#### 2.4 Numbers - Objects:

Ngoài cách tạo biến `Number` thông thường là gán trực tiếp thì có 1 cách khác là sử dụng đối tượng `Number`, 2 cách này sẽ có kiểu dữ liệu khác nhau.

**Ví dụ:**

```javascript
var x = 123; 	//number
var y = new Number(123); 	//object
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Đối tượng Number trong Javascript. http://freetuts.net/doi-tuong-number-trong-javascript-397.html
