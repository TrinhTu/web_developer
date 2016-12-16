## VIẾT CHỨC NĂNG PHÓNG TO THUMBNAIL KHI HOVER VỚI CSS3

> Tài liệu: Viết chức năng phóng to thumbnail khi hover với CSS3
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[Xây dựng chức năng](#1)

- [Viết HTML](2)

- [Viết CSS](#3)

<a name="1"></a>
### Xây dựng chức năng:

- Chức năng phóng to thumbnail khi hover chuột vào rất phổ biến và được sử dụng rộng rãi, nó tạo hiệu ứng chuyển động rất đpẹ, bắt mắt và thu hút người dùng.

<a name="2"></a>
#### Viết HTML:

- Tạo 1 file `index.html` với nội dung sau:

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Thumbnail</title>
    <style>
         
    </style>
</head>
<body>
    <div class="thumbnail">
        <img src="http://1.bp.blogspot.com/-3oZ7k46VeG4/Vk0d1nmNODI/AAAAAAAAC20/3B1E5A8BDC4/s1600/hinh-anh-dep-ve-dong-vat..jpg" alt="">
    </div>
</body>
</html>
```
- Trong đó:

    - `thumbnail` là khung chứa thumbnail

    - Cặp thẻ `style` là nơi sẽ code CSS.
<a name="3"></a>
#### Viết CSS:

- Viết CSS cho khung chứa thumbnail trước

```
.thumbnail {
    width: 300px;
    height: 200px; 
    overflow: hidden; 
    border: 1px solid #e5e5e5; 
}
```

- Trong đó:

    - `overflow: hidden;` là để thumbnail không bị tràn ra ngoài khung chứa khi phóng to lên.

    - `width` và `height` là chỉnh tùy ý sao cho phù hợp với kích thước của thumbnail.

- Viết CSS cho phần thumbnail:

```
.thumbnail img {
    width: 100%; 
    height: 100%;  
    transition-duration: 0.5s;
        /* Safari */
        -webkit-transition-duration: 0.5s; 
        /* Mozilla Firefox */
        -moz-transition-duration: 0.5s; 
        /* Opera */
        -o-transition-duration: 0.5s;
        /* IE 9 */
        -ms-transition-duration: 0.5s;
}
```

- Trong đó:

    - `width` và `height` của thumbnail là 100% để nó kéo dãn hết khung chứa thumbnail

    - `transtion-duration` chứa các giá trị về thời gian (đơn vị giây), thiết lập quá trình phóng to thumbnail mất bao nhiêu thời gian.

- Viết sự kiện hover chuột vào thumbnail thì sẽ phóng to ảnh lên.

```
.thumbnail img:hover {
    transform: scale(1.2);
        -webkit-transform: scale(1.2); 
        -moz-transform: scale(1.2); 
        -o-transform: scale(1.2);
        -ms-transform: scale(1.2);
    cursor: pointer; 
}
```

- Xem kết quả [tại đây](http://tutrinh01.chuyengiaseoweb.net/hi.html)