## Bài 35: BOM - SCREEN TRONG JAVASCRIPT

> Tài liệu: BOM - Screen trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/03/2017

## Mục lục:

[1. Lấy width và height của Screen](#1)

[2. Lấy Color Depth của Screen](#2)

[3. Lấy số Pixel depth của Screen](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Lấy width và height của Screen:

Sử dụng thuộc tính `screen.height` để lấy chiều cao và `screen.width` để lấy chiều rộng của màn hình, kết quả sẽ định dạng Pixels.

**Ví dụ:**

```javascript
document.write("Width screen:" + screen.width + "<br/>");
document.write("Height screen:" + screen.height);
```

Ngoài ra để lấy chiều rộng và chiều cao mà không tính các tools tính năng khác thì sử dụng: `screen.availWidth` và `screen.availHeight`

**Ví dụ:**

```javascript
document.write("With Available screen: " + screen.availWidth + "<br/>");
document.write("Height Available screen: " + screen.availHeight);
```

<a name="2"></a>
### 2. Lấy Color Depth của Screen:

Để lấy Color depth của màn hình sử dụng thuộc tính `screen.colorDepth`

**Ví dụ:**

```javascript
document.write("Color Depth:" + screen.colorDepth);
```

<a name="3"></a>
### 3. Lấy Pixel depth của Screen:

Để lấy Pixels Depth của màn hình sử dụng thuộc tính `screen.pixelDepth`

**Ví dụ:**

```javascript
document.write("Pixels Depth:" + screenDepth);
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] BOM - Screen trong Javascript. http://freetuts.net/bom-screen-trong-javascript-390.html