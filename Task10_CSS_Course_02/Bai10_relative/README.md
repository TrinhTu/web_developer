##Bài 10: Position relative - absolute trong CSS

>Tài liệu: Position relative - absolute trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 16/11/2016

###Mục lục:

[Position relative và absolute trong CSS](#1)

###Nội dung:
<a name="1"></a>
####Position relative và absolute trong CSS:

Position là thuộc tính dùng để xác định vị trí hiển thị cho thẻ HTML dùng để xây dựng CSS cho menu đa cấp, tooltip. Các giá trị của thuộc tính position:

- relative: không thay đổi cấu trúc thẻ image, dùng để thiết lập một phần tử sử dụng các thuộc tính

- position (xem ở dưới) mà không làm ảnh hưởng đến việc hiển thị ban đầu.

- absolute: dùng để hiển thị phần tử trong dạng tuyệt đối. Tức là phần tử đó chỉ hiển thị trong khung của phần tử mẹ và không thể chạy ra ngoài được.

- fixed: Hiển thị cố định.

- static: Đưa phần tử về hiển thị theo kiểu mặc định.

Position có 4 thuộc tính để tùy chỉnh vị trí và giá trị của nó là:

- top: căn vị trí hiển thị hướng từ trên xuống

- bottom: căn vị trí hiển thị từ dưới lên.

- left: căn vị trí hiển thị từ trái sang phải.

- right: căn vị trí hiển thị từ phải sang trái.

Ta có từng ví dụ cụ thể như sau:

- Relative:

Giả sử ta chèn hình ảnh vào tài liệu HTML:

```
<img src='http://topanhdep.net/wp-content/uploads/2015/08/hinh-dai-dien-cute.jpg'/>
```

Sau đó thêm CSS vào và sử dụng thêm thuộc tính `position: relative;`

```
img {
  position: relative;
  border: 2px inset green;
  top: 50px; 
  left: 200px; 
}
```

Ta có kết quả như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai10_relative/image/1.png)

- Ví dụ về kiểu absolute:

```
<div id="relative">
  <img src='http://topanhdep.net/wp-content/uploads/2015/08/hinh-dai-dien-cute.jpg'/>
</div>
```
 Ta cũng thêm CSS tương tự:

 ```
 #relative{
  width: 800px;
  height: 600px;
  background: #ff99cc;
  position: relative;
  margin: 0 auto;
}
img {
  position: absolute;
  border: 2px inset green;
  background: #ff6666;
  top: 50px; 
  left: 200px;
}
```

Ta có kết quả như sau:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai10_relative/image/2.png)

- Ví dụ về fixed: Thuộc tính này giúp cho hình ảnh được hiển thị cố định không bị dịch chuyển trong quá trình kéo.

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai10_relative/image/3.png)

