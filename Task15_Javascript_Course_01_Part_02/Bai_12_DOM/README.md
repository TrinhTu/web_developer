##Bài 12: DOM LÀ GÌ? CÁC LOẠI DOM TRONG JAVASCRIPT

>Tài liệu: DOM là gì? Các loại DOM trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 03/12/2016

###Mục lục:

[1. DOM là gì](#1)

[2. Các thể loại DOM trong javascript](#2)


###Nội dung:

<a name="1"></a>
####1. DOM là gì?

DOM là viết tắt của Document Object Model là mô hình các đối tượng trong tài liệu HTML. Trong mỗi thẻ HTML sẽ có thuộc tính Properties và có phân cấp cha-con, sự phân cấp của các thẻ HTML này được gọi là selector và trong DOM có nhiệm vụ xử lí các vấn đề như đổi thuộc tính của thẻ, đổi cấu trúc HTML của thẻ.

Ví dụ:

```javascript
<h1 id="main-content"></h1>
<script language="javascript">
	document.getElementById("main-content").innerHTML="Xin chào tất cả các bạn"
</script>
``` 

Xem kết quả:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_12_DOM/1.png)

<a name="2"></a>
####2. Các thể loại DOM trong javascript:

Danh sách chia nhóm DOM:

- DOM document: có nhiệm vụ lưu trữ toàn bộ các thành phần trong tài liệu website

- DOM element: có nhiệm vụ truy xuất tới thẻ HTML nào đó thông qua các thuộc tính như tên class, id, name của thẻ HTML

- DOM HTML: có nhiệm vụ thay đổi giá trị nội dung và giá trị thuộc tính của thẻ HTML

- DOM Event: có nhiệm vụ gán các sự kiện như `onclick()`, `onload()` vào các thẻ HTML

- DOM Listener: có nhiệm vụ lắng nghe các sự kiện tác động lên thẻ HTML đó.

- DOM Navigation: dung dể quản lí, thao tác với các thẻ HTML thể hiện mối quan hệ giữa các thẻ.

- DOM Node, Nodelist: co nhiệm vụ thao tác với HTML thông qua đối tượng Object.
