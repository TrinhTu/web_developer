## BÀI 41:  HÀM XỬ LÝ NUMBER TRONG JAVASCRIPT

> Tài liệu: Hàm xử lí Number trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 07/04/2017

### Mục lục: 

- [1. Hàm xử lí Number toàn cục](#1)

	+ [1.1 Number()](#1.1)

	+ [1.2 parseInt()](#1.2)

	+ [1.3 parseFloat()](#1.3)

- [2. Hàm xử lý number cục bộ](#2)

	+ [2.1 toString()](#2.1)

	+ [2.2 toFixed(n)](#2.2)

	+ [2.3 toPrecision(n)](#2.3)

	+ [2.4 valueOf()](#2.4)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Hàm xử lý Number toàn cục:

<a name="1.1"></a>
#### 1.1 Number():

- DÙng để chuyển đổi 1 biến hoặc 1 giá trị nào đó sang kiểu number, chuyển tất cả về dạng Boolean, Date, String, nếu giá trị cần chuyển không thể chuyển sang kiểu number được thì sẽ chuyển sang giá trị mặc định là `NaN`

**Ví dụ**:

```
var boolean_true = true;
Number(boolean_true);           // returns 1
 
var boolean_false = false;
Number(boolean_false);          // returns 0    
 
var string_str = 'abc';
Number(string_str);             // returns NaN
 
var string_num = '100';
Number(boolstring_numean_true); // returns 100
 
var date = new Date();
Number(boolean_true);           // returns 1
```
<a name="1.2"></a>
#### 1.2 parseInt():

- Hàm này có tác dụng giống với hàm Number(), có 1 số điểm khác biệt như sau:

	+ Nếu chuỗi có kí tự đầu tiên là các con số theo sau là chữ cái thì nó sẽ lấy các chữ số đàu tiên đó chuyển về dạng number, đối với trường hợp này nếu sử dụng hàm number() thì giá trị sẽ là `NaN`

	+ Nếu dữ liệu ở định dạng khác string thì chuyển thành `NaN`

**Ví dụ**:

```
var boolean_true = true;
parseInt(boolean_true); // returns NaN
 
var boolean_false = false;
parseInt(boolean_false);// returns NaN
 
var string_str = '10 abc';
parseInt(string_str);   // returns 10
 
var string_num = '100';
parseInt(string_num);   // returns 100
 
var date = new Date();
parseInt(boolean_true); // returns NaN
```

<a name="1.3"></a>
#### 1.3 parseFloat():

- Hàm này chuyển dữ liệu về dạng Float, cách sử dụng tương tự như hàm `parseInt()`

**Ví dụ:**

```
var boolean_true = true;
parseFloat(boolean_true);   // returns NaN
 
var boolean_false = false;
parseFloat(boolean_false);  // returns NaN
 
var string_str = '10.2 abc';
parseFloat(string_str);     // returns 10.2
 
var string_num = '100';
parseFloat(string_num);     // returns 100
 
var date = new Date();
parseFloat(boolean_true);   // returns NaN
```
<a name="2"></a>
### 2. Hàm xử lý Number cục bộ:

- Hàm này phải gắn liền với đối tượng Number cụ thể. Ví dụ như khởi tạo 1 biến `var x=12` thì x là tất cả các hàm cục bộ đó, ngoài ra có thể sử dụng `()` để bao quanh 1 biểu thức hoặc 1 giá trị thì vẫn sử dụng bình thường.

**Ví dụ**:

```
var x = 12;
x.toString();
(12).toString();
(12 + 12).toString();
```

<a name="2.1"></a>
#### 2.1 toString():

- Hàm này có tác dụng chuyển đổi Number sang String.

**Ví dụ:**

```
var x = 123;
 
typeof x;   // number
  
x = x.toString();
typeof x;   // string
 
typeof 12;  // number
 
typeof (12).toString(); // string
```

<a name="2.2"></a>
#### 2.2 toFixed(n):

- Hàm này có tác dụng chuyển 1 số sang 1 số có n số lẻ sau nó được làm tròn.

**Ví dụ**:

```
var x = 5.656;
x.toFixed(0); // returns 6
x.toFixed(2); // returns 5.66
x.toFixed(4); // returns 5.6560
x.toFixed(6); // returns 5.656000
```

<a name="2.3"></a>
#### 2.3 toPrecision(n)

- Hàm này có tác dụng chuyển 1 số thành 1 số có chiều dài n, hàm này khác với hàm `toFixed()` ở chỗ hàm `toFixed()` chuyển thành số có n số lẻ phía sau. Lưu ý tham số `n`  luôn luôn lớn hơn `0`, nếu không truyền tham số vào thì mặc định nó sẽ lấy luôn chiều dài ban đầu.

**Ví dụ**:

```
var x = 5.656;
x.toPrecision();  // returns 5.656
x.toPrecision(2); // returns 5.6
x.toPrecision(4); // returns 5.656
x.toPrecision(6); // returns 5.65600
```

<a name="2.4"></a>
#### 2.4 valueOf():

- Hàm này có tác dụng lấy giá trị của 1 biến hoặc 1 giá trị khác, hàm này không được sử dụng nhiều bởi thường lấy giá trị trực tiếp. Ngoài kiểu Number thì hàm còn có thể được sử dụng với  các kiểu dữ liệu khác.

**Ví dụ:**

```
var x = 123 + 12;
 
x.valueOf(); // returns 135
 
(2 + 3).valueOf(); // returns 5
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Hàm sử lý number trong Javascript. https://freetuts.net/ham-xu-ly-number-trong-javascript-399.html