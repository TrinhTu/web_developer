## Bài 34: BOM - WINDOW NAVIGATOR TRONG JAVASCRIPT

> Tài liệu: BOM - Window navigator trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/03/2017

## Mục lục:

[1. Kiểm tra Cookie có bật không](#1)

[2. Kiểm tra tên trình duyệt đang sử dụng](#2)

[3. Kiểm tra Engine của trình duyệt](#3)

[4. Kiểm tra version của trình duyệt](#4)

[5. Kiểm tra hệ điều hành của Client](#5)

[6. Kiểm tra ngôn ngữ của trình duyệt](#6)

[Tài liệu tham khảo](#7)

***

Window Navigator trong Javascript được sử dụng để kiểm tra thông tin về người dùng cũng như trình duyệt đang được sử dụng? hệ điều hành? có bật cookie không? tên version của trình duyệt...

<a name="1"></a>
### 1. Kiểm tra Cookie có bật không:

Để kiểm tra trình duyệt có bật Cookie hay không thì sử dụng thuộc tính `navigator.cookieEnable`

**Ví dụ:**

```javascript
          if (window.cookieEnabled){
          	alert("Có bật Cookie - freetuts.net");
          }
          else{
          	alert("Cookie đã bị tắt");
          }
```

<a name="2"></a>
### 2. Kiểm tra tên trình duyệt đang sử dụng:

Để kiểm tra tên trình duyệt sử dụng thuộc tính `navigator.appName` và thuộc tính `navigator.appCodeName` dùng để kiểm tra mã code của trình duyệt.

**Ví dụ:**

```javascript
        document.write("App Name: " + window.navigator.appName + "<br/>");
        document.write("Code Name: " + window.navigator.appCodeName);
```

<a name="3"></a>
### 3. Kiểm tra Engine của trình duyệt:

Để kiểm tra Engine của trình duyệt sử dụng thuộc tính `navigator.product`

**Ví dụ:**

```javascript
 document.write("Engine: " + navigator.product);
```

<a name="4"></a>
### 4. Kiểm tra Version của trình duyệt:

Để kiểm tra version của trình duyệt sử dụng thuộc tính `navigator.appVersion` hoặc `navigator.userAgent`

**Ví dụ:**

```javascript
	document.write("Cách 1: " + navigator.appVersion + "<br/>");
    document.write("Cách 1: " + navigator.userAgent);
```

Khi sử dụng Javascript để kiểm tra Version có thể trả về kết quả sai vậy cho nên không nên sử dụng nó để kiểm tra Version của trình duyệt.

<a name="5"></a>
### 5. Kiểm tra hệ điều hành của Client:

Để kiểm tra hệ điều hành của người dùng sử dụng thuộc tính `navigator.platform`

**Ví dụ:**

```javascript
document.write("Hệ điều hành:" + navigator.platform);
```

<a name="6"></a> 
### 6. Kiểm tra ngôn ngữ của trình duyệt:

Để kiểm tra ngôn ngữ của trình duyệt sử dụng thuộc tính `navigator.language`

**Ví dụ:**

```javascript
document.write("Ngôn ngữ của Browser:" + navigator.language);
```

<a name="7"></a>
### Tài liệu tham khảo:

> [1] BOM- Window navigator trong Javascript. http://freetuts.net/bom-window-navigator-trong-javascript-389.html