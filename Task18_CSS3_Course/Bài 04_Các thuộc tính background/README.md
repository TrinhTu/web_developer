## Bài 4: HỌC CSS3 - CÁC THUỘC TÍNH BACKGROUNDS

> Tài liệu: Học CSS3 - Các thuộc tính Backgrounds
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/12/2016

### Mục lục:

[1. CSS3 Multiple backgrounds](#1)

[2. Cấu hình kích thước cho background (background-size)](#2)

[3. Thuộc tính background-origin trong CSS3](#3)

[4. Thuộc tính background-clip trong CSS3](#4)

### Nội dung:

<a name="1"></a>
### 1. CSS3 Multiple backgrounds:

CSS3 cho phép thêm nhiều background cho 1 thẻ HTML bằng cách sử dụng thuộc tính `background-image`.

**Cú pháp như sau**:

```javascript
	background : 
		url(link-to-file1.png),
		url(link0to-file2.png),
		...;
```

- Để thiết lập thuộc tính cho từng image ta sử dụng cấu trúc như sau:

```javascript
	background-position: top left, right bottom;
	background-repeat: no-repeat, no-repeat;
```

**Ví dụ**

```javascript
		div{
			width: 700px;
            height: 500px;
            background-image:
                url(https://s-media-cache-ak0.pinimg.com/736x/51/06/84/5106842edee15a9a47f699aa8fe9b671.jpg),
                url(http://tapchianhdep.com/wp-content/uploads/2015/05/dowload-hinh-nen-may-tinh-dep-mien-phi-7.jpg);
                background-position: center center, center center;
                background-repeat: no-repeat, no-repeat
        }
```

![11](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/11.png)

- Thay vì code dài dòng ta có thể thay như sau:

```javascript
		div{
			width: 700px;
            height: 500px;
            background:
                url(https://s-media-cache-ak0.pinimg.com/736x/51/06/84/5106842edee15a9a47f699aa8fe9b671.jpg) no-repeat center center,
                url(http://tapchianhdep.com/wp-content/uploads/2015/05/dowload-hinh-nen-may-tinh-dep-mien-phi-7.jpg), no-repeat center center;
        }
```

<a name="2"></a>
### 2. Cấu hình kích thước cho background (background-size):

Background-size dùng để thay đổi kích thước của background.

**Ví dụ:**

```javascript
		div{
			width: 700px;
            height: 500px;
            background:
                url(https://s-media-cache-ak0.pinimg.com/736x/51/06/84/5106842edee15a9a47f699aa8fe9b671.jpg) no-repeat center center,
                url(http://tapchianhdep.com/wp-content/uploads/2015/05/dowload-hinh-nen-may-tinh-dep-mien-phi-7.jpg), no-repeat center center;
                background-size: 200px 250px, 350px 400px;
        }
```

![12](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/12.png)



<a name="3"></a>
### 3. Thuộc tính background-origin trong CSS3:

<a name="4"></a>
### 4. Thuộc tính background-clip trong CSS3:



