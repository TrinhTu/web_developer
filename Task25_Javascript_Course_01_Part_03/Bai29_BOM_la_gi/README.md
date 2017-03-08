## Bài 29: BOM LÀ GÌ? BOM TRONG JAVASCRIPT

> Tài liệu: BOM là gì? BOM trong javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/03/2017

## Mục lục:

[1. BOM là gì](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### 1. BOM là gì?

BOM là viết tắt của Browser Object Model, còn được gọi là các đối tượng liên quan đến trình duyệt browser. Mỗi browser có những đối tượng khác nhau nên nó không có 1 chuẩn chung nào, để thống nhất giữa các trình duyệt thì quy ước các loại BOM sau:

+ window

+ screen

+ location

+ history

+ navigator

+ popup

+ timing

+ cookies

Các đối tượng trên có phân cấp lẫn nhau và window là cấp cao nhất đại diện cho browser. Ví dụ khi truy cập tới `document` thì viết là `window.document`, muốn truy cập tới cookie thì viết `window.document.cookie (viết tắt là `document.cookie`)

<a name="2"></a>
### Tài liệu tham khảo:

> [1] BOM trong javascript. http://freetuts.net/bom-la-gi-bom-trong-javascript-384.html