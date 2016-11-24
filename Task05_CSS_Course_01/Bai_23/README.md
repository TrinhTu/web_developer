##Bài 23: Tạo chuyển động với transition

>Tài liệu: Tạo chuyển động với transition
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 23/11/2016

###Mục lục:

[1. Tìm hiểu về phần mềm VertigoSrv](#1)

[2. Tải và cài đặt VertigoSrv trên máy](#2)

[3. Cấu hình cơ bản](#3)

###Nội dung:

<a name="1"></a>


Cấu trúc khai báo transition như sau:

```
transition: [thuộc tính chuyển động] [thời gian chuyển động ] [thời gian delay] [kiểu chuyển động];
```
 Vì transition là thuộc tính của CSS3 nên cần khai báo thêm 2 thuộc tính tương tự kèm theo tiền tố `-moz` và `-webkit` để nó hoạt động tốt hơn trong mọi trình duyệt:

 ```
 #a {
 	transition: margin-left 2s 0.5s ease-in-out;
 	-moz-transition: margin-left 2s 0.5s ease-in-out;
 	-webkit-transition: margin-left 2s 0.5s ease-in-out;
 }
 ```

 Trong đó:

 - `margin-left`: là thuộc tính cần chuyển động. Các thuộc tính có thể chuyển động: https://www.w3.org/TR/css3-transitions/#animatable-properties

 - `2s`: là thời gian chuyển động

 - `0.5s`: là thời gian delay(thời gian hoãn lại khi bắt đầu chuyển động)

 - `ease-in-out`: Kiểu chuyển động lúc đầu nhanh lúc sau chậm. Các kiểu chuyển động, xem [tại đây](https://developer.mozilla.org/en-US/docs/Web/CSS/single-transition-timing-function)

 Khi tạo hiệu ứng chuyển động  phải đặt thuộc tính 	transition` vào phần tử muốn làm chuyển động, và khai báo thuộc tính chuyển động, sau đó thiết lập sự kiện chuyển động thông qua các pseudo class.

 ![a](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_23/image/a.png)

 - Ngoài ra còn có thể thiết lập chuyển động cho nhiều thuộc tính khác nhau bằng cách thêm dấu phẩy.

 ```
 transition: margin-left 2s, background 1s, ease-in-out;
 -moz-transition: margin-left 2s, background 1s, ease-in-out;
 -webkit-transition: margin-left 2s, background 1s, ease-in-out;
 ```

 ![b](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_23/image/b.png)

 Ngoài ra có thể truy cập tại đây để xem sự chuyển động rõ hơn: http://192.168.1.102:81/sourse/box.html


