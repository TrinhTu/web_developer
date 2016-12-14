## Bài 2: HỌC CSS3-BORDER-RADIUS-BO GÓC

> Tài liệu: Học CSS3-border-radius-bo góc
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: /12/2016

### Mục lục:

[1. Border-radius trong CSS3](#1)

[2. Một số ví dụ border-redius trong CSS3](#2)

- [2.1 Tạo hình tròn](#2.1)

- [2.2 Tạo button được bo 4 cạnh](#2.2)

### Nội dung:

<a name="1"></a>
### 1. Border-radius trong CSS3:

Để tạo bo tròn đường viền bằng CSS3 ta sử dụng cú pháp sau:

```
	border-radius: 15px;
	border-radius: 15px 15px;
	border-radius: 15px 15px 15px;
	border-radius: 15px 15px 15px 15px;
```

Để chạy đầy đủ trên tất cả trình duyệt ta thêm 2 thuộc tính hack css nữa:

```javascript
	-moz-border-radius: 15px;
	-webkit-border-radius: 15px;
```

Giá trị tham số được tính theo đơn vị chiều dài
(px, pt) hoặc (%)

Định nghĩa 4 góc như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/1.png)

**1. Một tham số**: Trường hợp này áp dụng cho tất cả 4 góc:

**Ví dụ**: `border-radius: 15px`

![2](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/2.png)

**2. Hai tham số**: 

Trường hợp này: 

- Tham số đầu tiên là **GÓC 1** và **GÓC 3**

- Tham số thứ 2 là **GÓC 2** và **GÓC 4**

**Ví dụ**: `border-radius: 30px 10px`

![3](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/3.png)

**3. Ba tham số**:

- Tham số đầu tiên là **GÓC 1**

- Tham số thứ 2 là **GÓC 2** và **GÓC 4**

- Tham số thứ 3 là **GÓC 3**

**Ví dụ**: `border-radius: 10px 20px 50px`

**4. Bốn tham số**: Tương ứng với 4 góc

**Ví dụ**: `border-radius: 10px 20px 50px 50%`

![4](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/4.png)

<a name="2"></a>
### 2. Một số ví dụ border-redius trong CSS3:

<a name="2.1"></a>
#### 2.1 Tạo hình tròn:

Để tạo hình tròn thì ta chỉ việc thiết lập `width` và `height` của thẻ HTML bằng nhau và bo tròn 4 góc với giá trị là 50%.

```javascript
.css3{
	margin: 50px;
	width: 150px;
	height: 150px;
	border: 5px solid red;
	background: pink;
	border-radius: 50%;
	-moz-border-radius: 50%;
	-webkit-border-radius: 50%;
	}
```

![5](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/5.png)

<a name="2.2"></a>
#### 2.2 Tạo button được bo 4 cạnh:

```javascript
	<style>
        input{
            padding: 5px 20px;
            background: pink;
            color: blue;
            border-radius: 20px;
            -moz-border-radius: 20px;
            -webkit-border-radius: 20px;
            cursor: pointer;
        }
    </style>
    <input type="submit" value="SUBMIT"/>
```

![6](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/6.png)
