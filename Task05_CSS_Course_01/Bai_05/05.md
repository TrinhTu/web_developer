##Bài 5: Các thuộc tính trang trí văn bản

> Tài liệu: Các thuộc tính trang trí văn bản
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 26/10/2016

### Mục lục

[1. Text-align](#1)

[2. Text decoration](#2)

[3. Text-indent](#3)

[4. Text-shadow](#4)

[5. Text-transform](#5)

###Nội dung:

Hiện nay Text Styles trong CSS có khoảng 13 thuộc tính trang trí văn bản, căn lề văn bản.... trong đó có các thuộc tính nổi bậc và thường được sử dụng như là:

- Text-align: căn lề văn bản

- Text-decoration: trang trí văn bản

- Text-indent: thêm khoảng trống theo chiều ngang từ trái sang phải

- Text-shadow: thêm bóng cho văn bản

- Text-transform: tùy chỉnh việc in hoa

Ngoài ra còn có thể tìm hiểu thêm 1 số thuộc tính trang trí khác cho văn bản tại đây https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

<a name="1"></a>
####1. Text-align:

Thuộc tính này giúp hỗ trợ căn lề văn bản bên trong Website, có các giá trị sau:

```
Text-align : left \\ căn lề bên trái
Text-align : right \\ căn lề bên phải
Text-align : center \\ căn lề chính giữa
Text-align : justify \\ căn đều 2 bên
```

Ví dụ:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_05/image/11.png)

<a name="2"></a>
####2. Text-decoration:

Thuộc tính này giúp trang trí lại văn bản hiển thị trên tài liệu theo 1 cách nhất định.

`text-decoration: overline | underline | line-through| none`

Trong đó:

- `overline`: gạch trên chữ

- `underline`: gạch dưới chữ

- `line-through`: gạch ngang chữ

- `none`: không có gì

**Ví dụ**

![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_05/image/12.png)

Ngoài ra còn có thêm các thuộc tính của nó như là: text-decoration-color, text-decoration-line, text-decoration-style nhưng chưa được hỗ trợ trên các trình duyệt thông dụng.

<a name="3"><a>
####3. Text-indent:

Thuộc tính này sẽ tạo ra khoảng trắng bên trái hay bên phải văn bản ( với các ngôn ngữ hiển thị từ trái sang phải), giá trị kèm theo của thuộc tính này là các đơn vị đo lường.

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_05/image/13.png)
<a name="4"></a>
####4. Text-shadow:

 Thuộc tính này giúp thêm bóng cho văn bản

Cú pháp như sau: ` text-shadow: [màu sắc] [tọa độ x y] [độ mờ]; `

Trong đó: **x** và **y** là giá trị đo lường, độ mờ nếu không khai báo thì sẽ có giá trị là không, và  giá trị của độ mờ luôn khai báo sau giá trị tọa độ.

Ví dụ như sau: 

```
#title {
	text-shadow: pink 2px 3px 4px;
}
```
Đoạn trên có nghĩa là : Văn bản mang id **#title** sẽ đổ bóng màu xanh, có tọa độ **x** là **2px** tọa độ **y** là **3px** và **độ mờ** là **4px**.

Ngoài ra còn có thể tạo ra nhiều bóng đổ cho 1 đoạn văn bảng bằng cách viết nhiều cú pháp tương tự như trên và mỗi cú pháp cách nhau bởi dấu phẩy. Nếu sử dụng các tên màu thông thường thì sẽ có ít sự lựa chọn nên có thể vào [đây](http://www.colorpicker.com/9414de) lấy mã màu.

**Ví dụ**:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_05/image/14.png)

<a name="5"></a>
####5. Text-transform:

Dùng để tùy chỉnh chữ in hoa hay chữ thường khi viết mà không dùng cách thủ công

Thuộc tính này có 3 giá trị là `capitalize` (in hoa chữ cái đầu tiên của mỗi từ, `uppercase` ( in hoa cả đoạn văn bản) , `lowercase` ( viết thường cả đoạn văn bản).

**Ví dụ**

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_05/image/15.png)





