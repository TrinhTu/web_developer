## Bài 33: BOM - COOKIE TRONG JAVASCRIPT

> Tài liệu: BOM - Cookie trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/03/2017

## Mục lục:

- [1. Cookie là gì?](#1)

- [2. Các thao tác với Cookie trong javascript](#2)

	- [2.1 Tạo Cookie](#2.1)

	- [2.2 Lấy giá trị Cookie](#2.2)

	- [2.3 Đổi giá trị cho Cookie](#2.3)

	- [2.4 Xóa Cookie](#2.4)

- [3. Viết hàm xử lí Cookie trong Javascript](#3)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Cookie là gì?

Cookie là dữ liệu được lưu trữ trong 1 file text nằm trong máy tính, thời gian lưu trữ cookie do bạn thiết lập. Ứng với mỗi domain thì có 1 dung lượng Cookie tối đa có thể lưu trữ được. Cookie được lưu trữ ở dạng `name=value`. Ví dụ:

`website=github.com`

Khi trình duyệt gởi thông tin lên server thì cookie sẽ được load và gởi kèm theo trong request, vì vậy trong ngôn ngữ server (PHP, JSP) cũng sẽ nhận được thông tin đó, ta hay sử dụng cookie để xây dựng chức năng Remember Me khi Login.

<a name="2"></a>
### 2. Các thao tác với Cookie trong Javascript:

Javascript có thể đọc, thêm và xóa Cookie thông qua đối tượng BOM `document.cookie`

<a name="2.1"></a>
#### 2.1 Tạo Cookie:

Để tạo Cookie sử dụng chuỗi dữ liệu `name=value`

**Ví dụ:**

`document.cookie = 'website=github.com';`

Nếu muốn lưu trữ nhiều Cookie chỉ việc tạo 2 lần:

```javascript
document.cookie = 'website=github.com';
document.cookie = 'email=letutrinh.ktmm@gmail.com';
```
Để thiết lập thời gian sống cho Cookie sử dụng từ khóa `expires`, cấu trúc của chuỗi này là thời gian ở dạng UTC.

**Ví dụ:**

```javascript
document.cookie="website=facebook.com; expires=Thu, 9 Mar 2017 20:00:00 UTC";
```

Theo mặc định thì khi đang ở trang nào thì cookie sẽ lưu với đường dẫn trang đó, muốn thay đổi đường dẫn thì sử dụng từ khóa `path`.

**Ví dụ:**

```javascript
document.cookie="website=facebook.com; expires= Thu, 9 Mar 2017 20:00:00 UTC; path=\";
```

<a name="2.2"></a>
#### 2.2 Lấy giá trị Cookie:

Để lấy danh sách các Cookie sử dụng cú pháp sau:

`var giatri = document.cookie;`

Kết quả trả về sẽ là 1 chuỗi Cookie có cấu trúc `name=value`, khi lưu nhiều cookie thì có dạng: `name1=value1; name2=value2`

<a name="2.3"></a>
#### 2.3 Đổi giá trị cho Cookie:

Để thay đổi giá trị cho cookie thì chỉ cần gán lại giá trị cho Cookie.

**Ví dụ:**

```javascript
//giá trị cũ
document.cookie = "domain=facebook.com";
//giá trị mới
document.cookie = "domain=github.com";
```

<a name="2.4"></a>
#### 2.4 Xóa Cookie:

Trong Javascript không có hàm xóa Cookie mà thay vào đó là sử dụng từ khóa `expires` để thiết lập thời gian sống cho cookie là khoảng thời gian đã qua.

<a name="3"></a>
### Viết hàm xử lí Cookie trong Javascript:

Vì Cookie được lưu trữ ở dạng chuỗi `key=value` và các chuỗi giá trị cách nhau bởi dấu chấm phẩy nên để lấy 1 giá trị nào đó thì phải xử lí chuỗi rất phức tạp, vậy nên ta thường viết hàm tạo và lấy Cookie để sử dụng được nhiều lần.

**Ví dụ:**

```javascript
// Hàm thiết lập Cookie
function setCookie(cname, cvalue, exdays) {
    var d = new Date();
    d.setTime(d.getTime() + (exdays*24*60*60*1000));
    var expires = "expires="+d.toUTCString();
    document.cookie = cname + "=" + cvalue + "; " + expires;
}
 
// Hàm lấy Cookie
function getCookie(cname) {
    var name = cname + "=";
    var ca = document.cookie.split(';');
    for(var i=0; i<ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0)==' ') c = c.substring(1);
        if (c.indexOf(name) == 0) return c.substring(name.length, c.length);
    }
    return "";
}
```
<a name="4"></a>
### Tài liệu tham khảo:

> [1] BOM - Cookie trong Javascript. http://freetuts.net/bom-cookie-trong-javascript-388.html