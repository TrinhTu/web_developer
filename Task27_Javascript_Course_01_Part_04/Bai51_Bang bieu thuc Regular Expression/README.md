## BÀI 51: BẢNG BIỂU THỨC REGULAR EXPRESSION TRONG JAVASCRIPT

> Tài liệu: Bảng biểu thức Regular Expression trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/04/2017

### Mục lục: 

- [1. Bảng quy tắc Regular Expression](#1)

    + [1.1 Modifiers](#1.1)

    + [1.2 Brackets](#1.2)

    + [1.3 Metacharacters](#1.3)

    + [1.4 Quantifiers](#1.4)

- [2. Các ví dụ thực hành với biểu thức RegExp](#2)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Bảng quy tắc Regular Expression:

<a name="1.2"></a>
#### 1.1 Modifiers:

|  Modifier | Description   |
|---|---|
|i   | So sánh không phân biệt chữ hoa chữ thường (case-insensitive)  |
|g| So sánh toàn bộ chuỗi dù trong chuỗi có xuống hàng (global)  |
|m   | So sánh nhiều dòng (multiline)  |

<a name="1.2"></a>
#### 1.2 Brackets:

| Expression  |Description   |
|---|---|
|  [abc] |Tìm kí tự a, b hoặc c   |
|  [^abc] | Tìm các kí tự không phải a, b và c  |
|  [0-9] |Tìm các ký tự là chữ số từ 0-9   |
|  [^0-9] | Tìm các kí tự không phải chữ số từ 0-9  |
|  (x\y) |Tìm các kí tự x hoặc y   |

<a name="1.3"></a>
#### 1.3 Metacharacters:

|   Expression|Description   |
|---|---|
|  . | Tìm kí tự bất kì  |
| \w  | Tìm kí tự chữ cái  |
| \W  | Tìm các kí tự không phải là chữ cái  |
|  \d | Tìm kí tự là chữ số  |
|  \D | Tìm kí tự không phải là chữ số  |
| \s  | Tìm kí tự là khoảng trắng   |
|  \S | Tìm kí tự không phải là khoảng trắng  |
|  \b |  Tìm so khớp bắt đầu hoặc kết thúc chuỗi  |
|  \B | Tìm so khớp không phải bắt đầu hoặc kết thúc chuỗi  |
| \0  | Tìm kí tự NULL  |
|  \n | Tìm kí tự xuống hàng  |
| \t  | Tìm kí tự tab |

<a name="1.4"></a>
#### 1.4 Quantifiers:


|  Expression | Description  |
|---|---|
| +  |Kiểm tra kí tự xuất hiện 1 hoặc nhiều lần   |
|  * | Kiểm tra kí tự xuất hiện không hoặc nhiều lần  |
|  ? | Kiểm tra kí tự xuất hiện không hoặc 1 lần  |
|  {X} | Kiểm tra kí tự xuất hiện đúng X lần  |
|  {X,Y} |  Kiểm tra kí tự xuất hiện tối thiểu X lần và tối đa Y lần |
|  {X,} | Kiểm tra kí tự xuất hiện ít nhất X lần  |
| ^  |  Kiểm tra kí tự bắt đầu chuỗi  |
|  $ |  Kiểm tra kí tự kết thúc chuỗi |

<a name="2"></a>
### 2. Các ví dụ thực hành với biểu thức RegExp:

- **Ví dụ 1:** Kiểm tra chuỗi xuất hiện ít nhất 10 chữ N liên tiếp và không phân biệt chữ hoa chữ thường.

Sử dụng cú pháp {10,} để kiểm tra ít nhất 10 chữ N liên tiếp.

```javascript
var pattern = /n{10,}/i;
if (pattern.test("10 chu n la nnnnnnnnnn")) {
    document.write('Chuỗi có NHIỀU hơn 10 chữ n');
}
else {
    document.write('Chuỗi có ÍT hơn 10 chữ n');
}
```

- **Ví dụ 2:** Kiểm tra chuỗi có phải là "github.com" hay không

Để kiểm tra chính xác chuỗi là "github.com" thì bắt buộc phải thêm kí tự ^ và kết thúc $ để fix chuỗi lại. Kí tự `.` trong chuỗi "github.com" là kí tự đặc biệt nên phải thêm dấu `\` trước nó.

```javascript
var pattern = /^freetuts\.net$/i;
if (pattern.test("freetuts.net")) {
    document.write('Chuỗi freetuts.net');
}
else {
    document.write('Không phải chuỗi freetuts.net');
}
```

- **Ví dụ 3:** Kiểm tra chuỗi là các chữ số và dài 8 kí tự.

Để kiểm tra các chữ số ta dùng `[0-9]` và chiều dài 8 kí tự nên ta dùng {8}.

```javascript
var pattern = /^[0-9]{8}$/;
if (pattern.test("12345678")) {
    document.write('Các số dài 8 ký tự');
}
else {
    document.write('Không phải là số hoặc ngắn hơn 8 ký tự');
}
```

- **Ví dụ 4:** Kiểm tra chuỗi định dạng mã thẻ cào xxxx-xxxx-xxxx-xxxx và x chính là các chữ số.

Sử dụng [0-9] để kiểm tra chữ số, và các cặp xxxx có chiều dài là 4 nên sử dụng {4}.

```javascript
var pattern = /^[0-9]{4}-[0-9]{4}-[0-9]{4}-[0-9]{4}$/;
if (pattern.test("1234-1232-1321-2312")) {
    document.write('Mã thẻ hợp lệ');
}
else {
    document.write('Mã thẻ không hợp lệ');
}
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Bảng biểu thức Regular Expression trong Javascript. https://freetuts.net/bang-bieu-thuc-regular-expression-trong-javascript-418.html