## Bài 39: HÀM TYPEOF TRONG JAVASCRIPT

> Tài liệu: Hàm typeof trong javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/03/2017

## Mục lục:

[1. Hàm typeof trong Javascript](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### 1. Hàm typeof trong Javascript:

- Hàm `typeof` trong Javascript được sử dụng để kiểm tra 1 biến nào đó (hoặc 1 giá trị) có kiểu dữ liệu gì. Cú pháp của nó như sau:

`var x = typeof value;`

- Trong đó `value` có thể là 1 biến hoặc 1 giá trị xác định. Có 1 số loại dữ liệu như sau:

	+ `number` - số

	+ `string` - chuỗi

	+ `object` - đối tượng

	+ `undefined` - không xác định

**Ví dụ:**

```javascript
 	var number = 12;
    var string = "12";
    var object = new Number();
    document.write("number: " + typeof number + "<br/>");
    document.write("string: " + typeof string + "<br/>");
    document.write("object: " + typeof object + "<br/>");
```

- Trong PHP để kiểm tra 1 biến có tồn tại hay không sử dụng hàm `isset()` còn trong javascript thì sử dụng hàm `typeof` kết hợp với kiểu dữ liệu `undefined`. Nếu 1 biến chứa kiểu dữ liệu `undefined` thì biến đó chưa được định nghĩa hoặc giá trị của biến đó không xác định.

**Ví dụ:**

```javascript
 if (typeof variable == 'undefined'){
        document.write("Biến variable không được định nghĩa");
 }
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Hàm typeof trong Javascript. http://freetuts.net/ham-typeof-trong-javascript-398.html