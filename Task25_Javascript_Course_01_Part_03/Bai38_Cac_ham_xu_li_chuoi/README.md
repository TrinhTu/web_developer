## Bài 38: CÁC HÀM XỬ LÝ CHUỖI TRONG JAVASCRIPT

> Tài liệu: Các hàm xử lý chuỗi trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/03/2017

## Mục lục:

- [1. Các hàm xử lý chuỗi trong Javascript](#1)

	- [1.1 Tìm kiếm chuỗi con](#1.1)

	- [1.2 Cắt chuỗi con](#1.2)

	- [1.3 Tìm kiếm và lặp chuỗi](#1.3)

	- [1.4 Chuyển thành chữ hoa và chữ thường](#1.4)

	- [1.5 Nối thêm chuỗi](#1.5)

	- [1.6 Tìm kí tự hoặc mã ASCII của 1 kí tự](#1.6)

	- [1.7 Chuyển đổi chuỗi sang mảng](#1.7)

- [Tài liệu tham khảo](#2)

***

<a name="1"></a>
### 1. Các hàm xử lý chuỗi trong Javascript:

<a name="1.1"></a>
#### 1.1 Tìm kiếm chuỗi con:

- Có 3 hàm thường dùng để tìm chuỗi con trong Javascript như sau:

	+ indexOf()

	+ lastIndexOf()

	+ search()

- **Hàm indexOf()**

	+ Để tìm kiếm chuỗi con sử dụng hàm `String.indexOf(str)` trong đó `str` là chuỗi con và `string` là chuỗi cha. Hàm sẽ trả về kết quả là vị trí xuất hiện đầu tiên của chuỗi (bắt đầu là vị trí 0), nếu không tìm thấy chuỗi con thì nó sẽ trả về -1.

**Ví dụ:** 

```javascript
var string = "Ngày mới vui_vẻ";
document.write("Vị trí xuất hiện chuỗi vui vẻ là: " + string.indexOf("vui_vẻ"));
```

- **Hàm lastIndexOf()**

	+ Trường hợp nếu chuỗi con xuất hiện nhiều lần trong chuỗi cha thì kết quả cũng trả về vị trí xuất hiện của chuỗi con đầu tiên. Sử dụng hàm `String.lastIndexOf(str)` hàm này sẽ trả về vị trí xuất hiện của chuỗi con cuối cùng và trả về `-1` nếu không tìm thấy. 

**Ví dụ:**

```javascript
var string = "Học lập trình tại freetuts.net";
document.write("Vị trí xuất hiện chuỗi freetuts.net là: " + string.lastIndexOf("freetuts.net"));
```

- **Hàm search()**

	+ Ngoài 2 hàm trên có thể sử dụng hàm `string.search(str)` để tìm kiếm nó có tác dụng tương tự như hàm `string.indexOf(str)`

**Ví dụ:**

```javascript
 var string = "Thư giãn tại youtube.com";
 document.write("Vị trí xuất hiện chuỗi youtube.com là: " + string.search("youtube.com"));
```

<a name="1.2"></a>
#### 1.2 Cắt chuỗi con:

Nếu muốn cắt 1 chuỗi con từ chuỗi cha thì sử dụng 3 hàm sau: `slice(start,end)`, `substring(start,end)`, `substr(start,length)`.

**Lưu ý:** Tất cả vị trí của chuỗi đều bắt đầu từ 0

- **Hàm slice()**

	+ Hàm có 2 tham số truyền vào:

		+ `start`: vị trí bắt đầu

		+ `end`: vị trí kết thúc

**Ví dụ:**

```javascript
 var string = "Welcome to freetuts.net";
 document.write("Chuỗi cần lấy là: " + string.slice(11, 23));
```

Nếu như tham số truyền vào là số âm thì nó sẽ tính ngược lại từ cuối tính lên.

**Ví dụ:**

```javascript
var string = "Welcome to freetuts.net";
document.write("Chuỗi cần lấy là: " + string.slice(-12, 23));
```

Nếu như chỉ truyền 1 tham số thì mặc định nó sẽ hiểu `end` là vị trí cuối cùng.

- **Hàm substring()**

	+ Cách sử dụng hàm này tương tự với hàm `slice()` tuy nhiên tham số truyền vào luôn phải lớn hơn 0.

**Ví dụ:**

```javascript
 var string = "Welcome to freetuts.net";
 document.write("Chuỗi cần lấy là: " + string.substring(11, 23));
```

- **Hàm substr()**: 

	+ Hàm này có 2 tham số truyền vào là `start` và `length`, trong đó `start` là vị trí bắt đầu và `length` là kí tự muốn lấy bắt đầu từ vị trí `start`. Nếu truyền tham số `start` là số âm thì tính từ cuối trở lên còn tham sos `length` phải luôn luôn dương.

**Ví dụ:**

```javascript
 var string = "Welcome to freetuts.net";
 document.write("Chuỗi cần lấy là: " + string.substr(11, 12));
```

<a name="1.3"></a>
#### 1.3 Tìm kiếm và lặp chuỗi:

Để tìm kiếm và lặp 1 chuỗi con nào đó thì sử dụng hàm `replace(str_find, str_replace)` trong đó `str_find` là chuỗi cần tìm và `str_replace` là chuỗi được thay thế chuỗi `str_find`.

**Ví dụ:**

```javascript
var string = "Welcome to freetuts.net";
document.write(string.replace("freetuts.net", "code.freetuts.net"));
```

<a name="1.4"></a>
#### 1.4 Chuyển thành chữ hoa và chữ thường:

Để chuyển chuỗi thành chữ hoa ta sử dụng hàm `toUpperCase()` và chuyển thành chữ thường ta sử dụng hàm `toLowerCase()`.

**Ví dụ:**

```javascript
var string = "Try your best";
document.write(string.toUpperCase() + "<br/>");
document.write(string.toLowerCase());
```

<a name="1.5"></a>
#### 1.5 Nối thêm chuỗi:

Để nối thêm chuỗi thường sử dụng toán tử `+`, ngoài ra còn có thể dùng hàm `concat()` để thực hiện nối chuỗi.

**Ví dụ:**

```javascript
		var string = "Xin chào " + "các" + "bạn";
        document.write(string + "<br/>");
        // hoặc
        var string = "Xin chào ";
        string = string.concat("các ", "bạn");
        document.write(string + "<br/>");
```

<a name="1.6"></a>
#### 1.6 Tìm kí tự hoặc mã ASCII của 1 kí tự:

Để xem kí tự của 1 vị trí nào đó ta sử dụng hàm `charAt()` còn xem mã ASCII thì sử dụng hàm `charCodeAt()`, tham số truyền vào 2 hàm này là vị trí muốn xem.

**Ví dụ:**

```javascript
		var string = "Lê Tú Trinh";
        document.write(string.charAt(1) + "<br/>");
        document.write(string.charCodeAt(1) + "<br/>");
```

<a name="1.7"></a>
#### 1.7 Chuyển đổi chuỗi sang mảng:

Để chuyển đổi 1 chuỗi sang mảng sử dụng hàm `split()` với tham số truyền vào là kí tự ngăn cách giữa các phần tử.

**Ví dụ:**

```javascript
	string = "Lê Tú Trinh";
    // Tạo thành mảng với mỗi phần tử ngăn bởi khoảng trắng
    // kết quả là mảng gồm có 3 phần tử
    document.write(string.split(" ").length);
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Các hàm xử lý chuỗi trong Javascript. http://freetuts.net/cac-ham-xu-ly-chuoi-trong-javascript-393.html