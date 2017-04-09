## BÀI 50: RegExp - Regular Expression trong Javascript

> Tài liệu: RegExp - Regular Expression trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/04/2017

### Mục lục: 

[1. Regular Expression trong Javascript](#1)

[2. Các quy tắc Regular Expression căn bản](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Regular Expression trong Javascript:

- Trong Javascript thì Regular Expression là 1 chuỗi nhưng nó không được bao quanh bởi cặp dấu nháy `'` hoặc nháy `"` mà được bao quanh bởi cặp dấu `/`. 

**Cú pháp**:

`/pattern/modifiers`

**Trong đó**: 

- `pattern` là chuỗi Regular Expression

- `modifiers` là thông số cấu hình cho chuỗi pattern và nó có các giá trị 

    + `i`: so khớp không quan tâm đến chữ in hoa thường

    + `g`: so khớp toàn bộ chuỗi cần tìm

    + `m`: so khớp luôn cả các dữ liệu xuống dòng (multiline)

**Ví dụ:** Pattern kiểm tra chuỗi tồn tại chuỗi `hello` không, không phân biệt chữ hoa và chữ thường và tìm toàn bộ tài liệu.

`var pattern = /hello/igm;`

Trong ví dụ này thì:

- pattern là hello

- modifiers là igm

<a name="2"></a>
### 2. Các quy tắc Regular Expression căn bản:

- Một số quy tắc căn bản thường sử dụng trong Regular Expression

|  Expression |Decription   |
|---|---|
|[abc]|Tìm các chữ cái a,b hoặc c   |
|[0-9] hoăc [a-z]  |  Tìm các ký tự từ 0-9 hoặc từ a-z |
|(x\y)|Tìm kí tự x hoặc y  |
|\d |Tìm các chữ số   |
|\s |Tìm khoảng trắng   |
| n+  |Tìm 1 hoặc nhiều chữ n liên tiếp nhau   |
| n* |Tìm 0 hoặc nhiều chữ n liên tiếp nhau   |
|  n? |Tìm 0 hoặc 1 chữ n   |

- Một hàm trong `parttern` dùng để kiểm tra một chuỗi đó là hàm `test()`. **Cú pháp**: `pattern.test(string)`

- **Trong đó**: 

    + pattern: là chuỗi pattern

    + string là chuỗi cần kiểm tra

**Kết quả trả về**: TRUE là khớp và FALSE nếu không khớp.

- **Ví dụ**: kiểm tra chuỗi có xuất hiện chữ `xin chào` hay không?

```javascript
var patt = /xin chào/;
if (patt.test("xin chào các bạn")) {
    document.write('Trong chuỗi có chữ xin chào');
}
else {
    document.write('Trong chuỗi không có chữ xin chào');
}
```

Với ví dụ này có thể sử dụng trực tiếp hàm `test()` trong pattern

`/xin chào/.test("xin chào các bạn")`

- **Ví dụ**: kiểm tra chuỗi có ít nhất 1 chữ n

Trong ví dụ này ta sử dụng dấu `+` trong bảng RegEX căn bản, có tác dụng kiểm tra 1 chuỗi có ít nhất 1 kí tự cần tìm kiếm.

```javascript
if (/n+/.test("hello")) {
    document.write('Trong chuỗi có chữ n');
}
else {
    document.write('Trong chuỗi không có chữ n');
}
```

- **Ví dụ**: Kiểm tra trong chuỗi có xuất hiện số hay không?

Với ví dụ này cách thứ nhất sử dụng cặp dấu ngoặc `[0-9]` và cách thứ 2 là dùng kí hiệu `\d`

```javascript
if (/[0-9]/.test("hello123")) {
    document.write('Trong chuỗi có xuất hiện số');
}
else {
    document.write('Trong chuỗi không xuất hiện số');
}
```

- **Ví dụ**: Kiểm tra trong chuỗi không hoặc có xuất hiện số

Ở ví dụ này kết hợp cặp dấu ngoặc `[0-9]` và ksi hiệu `*` trong bảng trên

```javascript
if (/[0-9]*/.test("freetuts")) {
    document.write('Luôn luôn chạy');
}
else {
    document.write('Không bao giờ chạy');
}
```

- **Ví dụ:** Kiểm tra trong chuỗi có chữ H hay không?

```javascript
if (/H/i.test("hello")) {
    document.write('Có chữ H');
}
else {
    document.write('Không có chữ H');
}
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] RegExp - Regular Expression trong Javascript. https://freetuts.net/regexp-regular-expression-trong-javascript-405.html