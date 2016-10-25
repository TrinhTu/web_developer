###Bài 3: TÌM HIỂU VỀ VÙNG CHỌN CƠ BẢN (SELECTOR)

> Tài liệu: Tìm hiểu về vùng chọn cơ bản (selector)
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **24/10/2016**

####Mục lục

[1. Vùng chọn là gì?](#1)

[2. Các loại vùng chọn cơ bản](#2)

- [Vùng chọn dựa vào tên thẻ](#7)

- [Vùng chọn dựa vào ID](#3)

- [Vùng chọn dựa vào Class](#4)

- [Vùng chọn theo thứ cấp](#5)

- [Vùng chọn theo thứ cấp liền nhau](#6)


###Nội dung

Vùng chọn trong CSS đóng vai trò rất quan trọng khi viết CSS vì nếu chọn sai vùng thì các quy tắc CSS đó sẽ không được áp dụng hoặc áp dụng không đúng chỗ

Vùng chọn trong CSS rất linh hoạt có thể chọn bất cứ gì từ thẻ `<body>` và đi vào sâu bên trong nó

<a name="1"></a>
####1. Vùng chọn là gì?

Vùng chọn là khu vực trong website được áp dụng chỉ đụng sử dụng CSS. Ví dụ như muốn viết CSS trong thẻ h1 thì vùng chọn của bạn sẽ là thẻ h1. Một đoạn CSS có thể sử dụng nhiều vùng chọn khác nhau.

Vùng chọn có thể là tên thẻ HTML hoặc thuộc tính của HTML.

<a name="2"></a> 
####2. Các loại vùng chọn cơ bản:

<a name="7"></a>
- Vùng chọn dựa vào tên thẻ:

Đây là kiểu đơn giản nhất, là chọn toàn bộ các phần tử trong HTML dựa vào tên thẻ có trong tài liệu rồi áp dụng CSS. Ví dụ muốn thay đổi style cho toàn bộ thẻ h1 trong website thì có đoạn CSS sau với vùng chọn h1. Đầu tiên ta tạo 1 tập tin HTML như sau và chèn CSS theo kiểu External styles, sau đó tạo thêm 1 tập tin **style.css** và thêm vào đó các thuộc tính muốn thêm vào:

[1](

[2](

[3](

Đối với kiểu vùng chọn này thì không thể áp dụng cho từng khu vực độc lập mà tất cả các vùng trong tài liệu HTML trong website được sử dụng CSS đều được áp dụng.

<a name="3"></a>
- Vùng chọn dựa vào ID:

Vùng chọn dựa vào ID ( tên định danh) nghĩa là có thể chọn 1 phần tử cụ thể để áp dụng CSS dựa vào giá trị của thuộc tính **id**, vùng chọn id được sử dụng để chọn 1 phần tử cụ thể vì trên trang tài liệu HTML mỗi phần tử phải mang 1 giá trị id riêng biệt không trùng nhau.

Id được thiết lập dựa vào thuộc tính **id** trong thẻ HTML và thẻ nào cũng đề có thể sử dụng thuộc tính id, khi viết tên id vào CSS phải có dấu thăng đặt trước (#tên_id) để tên id phân biệt với các vùng chọn khác.

[4](

[5](

[6](

<a name="4"></a> 
- Vùng chọn dựa vào Class:

Được sử dụng rất phổ biến điểm khác biệt của nó là có thể áp dụng cho nhiều phần tử trên 1 trang tài liệu HTML còn về id thì chỉ sử dụng cho 1 phần tử.

Class được khai báo trong phần tử HTML bởi thuộc tính class như sau `<h1 class="tên_class">` khai báo vùng chọn trong CSS thì tên class phải được đặt sau dấu chấm `(.tên_class)` 

[7](

[8](

[9](

<a name="5"></a>
- Vùng chọn theo thứ cấp:

Sử dụng rất thường xuyên khi tiến hành viết CSS cho website, với vùng chọn này có thể chọn 1 phần tử con trong phần tử mẹ. Ví dụ với 1 đoạn CSS như sau:
```
<ul id="menu">
 <li>Menu 1</li>
 <li>Menu 2</li>
 <li>Menu 3</li>
</ul>
 
<ul id="list">
 <li>list 1</li>
 <li>list 2</li>
 <li>list 3</li>
</ul>
```
Để chọn thẻ `<li>` bên trong thẻ `#menu`  mình sẽ viết vùng chọn là `#menu li` thay vì chỉ viết `li` trong CSS,  và khi đó CSS sẽ hiểu rằng mình muốn chọn tất tả các thẻ `<li>` nằm bên trong phân tử mang `#menu`

[10](

[11](

[12](

Cách viết `#menu ul li` như vậy thì CSS sẽ hiểu rằng sẽ chọn phần tử `li` nằm bên trong phần tử `ul` và phần tử `ul` nằm trong `menu`.

<a name="6"></a>
- Vùng chọn theo thứ cấp liền nhau:

 Đây là kiểu vùng chọn dựa theo thứ cấp.
 
```
<div id="menu">
<ul>
<li>Menu 1
<ul>
<li>Menu 1.a</li>
<li>Menu 1.b</li>
</ul>
</li>
<li>Menu 2</li>
<li>Menu 3</li>
</ul>
</div>
```

Muốn đặt CSS cho thẻ `<li>` của Menu 1.a Menu1.b sẽ đặt vùng chọn là `#menu ul ul > li`  tức là nó sẽ chọn thẻ `<li>` nằm trong thẻ `<u>` ở bậc thứ 2 và thẻ `<ul>` đó nằm trong id#menu

[13](

[14](

[15](