## BÀI 52: HTML5 LocalStorage và sessionStorage

> Tài liệu:  HTML5 LocalStorage và sessionStorage
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/04/2017

### Mục lục: 

[1. HTML5 Local Storage](#1)

[2. localStorage Object](#2)

[3. sessionStorege Object](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. HTML5 Local Storage:

- Local Storage có công dụng tương tự như cookie, nó sẽ lưu trữ thông tin trên Browser mà người dùng đang truy cập. Điểm khác biệt giữa Cookie và Local Storage cho phép lưu trữ thông tin tương đối lớn lên đến 5MB, ngoài ra local storage không gởi thông tin lên server như cookie. Cả local storage và cookie đều không ảnh hưởng đến hiệu xuất trang web.

- Có 2 loại local storage là:

    + **window.localStorage**:  Lưu trữ dữ liệu vô thời hạn, dữ liệu sẽ được lưu trữ cho tới khi người dùng clear history

    + **window.sessionStorage**: Lưu trữ dữ liệu cho mọi phiên làm việc, nghĩa là dữ liệu sẽ bị mát khi tắt Browser.

<a name="2"></a>
### 2. localStorage Object:

- LocalStorage Object lưu trữ dữ liệu vô thời hạn, nghĩa là dữ liệu sẽ không bị mất cho tới khi bạn sử dụng chức năng clear history của trình duyệt, hoặc sử dụng localStorage API để xóa. Có 32 thao tác chính là gán dữ liệu và lấy dữ liệu. Trước khi sử dụng phương thức này chắc chắn trình duyệt hỗ trợ HTML5. Doạn code dưới đây kiểm tra trình duyệt có hộ trợ localStorage hay không

```javascript
if (typeof(Storage) !== "undefined") {
    // Có hỗ trợ local storage
} else {
    // Không hỗ trợ local storage
}
```

- **Ví dụ**: lưu trữ domain github.com vào trình duyệt người dùng.

Tạo 2 file `a.html` và `b.html` với nội dung sau:

**a.html**

```javascript
if (typeof(Storage) !== "undefined") {
    var domain = 'github.com';
    localStorage.setItem('domain', domain);
} else {
    document.write('Trình duyệt của bạn không hỗ trợ local storage');
}
```

**b.html**

```javascript
if (typeof(Storage) !== "undefined") {
    var domain = localStorage.getItem('domain');
    document.write(domain); // kết quả github.com
} else {
    document.write('Trình duyệt của bạn không hỗ trợ local storage');
}
```

- Chạy file `a.html` trước sau đó chạy file `b.html` thì lấy thông tin domain `github.com` đã được in lên website --> nghĩa là file `a.html` đã lưu trữ thông tin browserrooif nên file `b.html` mới có thể lấy được thông tin.

- Để lưu dữ liệu dùng phương thức `setltem(key,value)` va

<a name="3"></a>
### 3. sessionStorage Object:

- Công dụng của sessionStorage cũng tương tự như localStorage, chỉ có một điểm khác đó là dữ liệu của sessionStorage sẽ mất khi bạn đóng trình duyệt. sessionStorage không tồn tại hai phương thức getItem và setItem mà bạn sẽ bổ sung key và value cho nó.

- **Ví dụ:**

```javascript
if (typeof(Storage) !== "undefined") {
    // Gán dữ liệu
    sessionStorage.domain = 'github.com';
     
    // Lấy dữ liệu
    var domain = sessionStorage.domain; // github.com
} else {
    document.write('Trình duyệt của bạn không hỗ trợ local storage');
}
```

- **a.html**

```javascript
if (typeof(Storage) !== "undefined") {
    sessionStorage.domain = 'github.com';
} else {
    document.write('Trình duyệt của bạn không hỗ trợ local storage');
}
```

- **b.html**

```javascript
if (typeof(Storage) !== "undefined") {
    document.write(sessionStorage.domain); // kết quả github.com
} else {
    document.write('Trình duyệt của bạn không hỗ trợ local storage');
}
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] HTML5 localStorage và sessionStorage. https://freetuts.net/html5-localstorage-va-sessionstorage-760.html
