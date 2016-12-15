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

Nếu thiết lập kích thước cố định cho background thì sẽ không chạy tốt trong thiết kế responsive vì responsive co giãn không định chiều cao và chiều rộng, ta sẽ sử dụng 2 giá trị chuẩn sau đây:

- **contain**: background có tác dụng nhủ thẻ `img` tức là nó sẽ co giãn theo chiều cao và chiều rộng đúng tỉ lệ của ảnh.

- **cover**: nếu chiều rộng và chiều cao của thẻ HTML lớn hơn hình ảnh thì nó sẽ giản ra cho vừa.

**Ví dụ cover**:

```javascript
		div{
            width: 500px;
            height: 400px;
            background:
                url(http://wapquahay.com/wp-content/uploads/2015/07/tin-nhan-chuc-buoi-sang-7-.jpg) no-repeat center center;
            background-size: cover;
        }
```

Trong ví dụ này thì hình background nhỏ hơn khung nên nó sẽ giản ra cho vừa với khung.

![13](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/13.png)


**Ví dụ contain**

```javascript
		div{
            width: 600px;
            height: 200px;
            background:
                url(http://wapquahay.com/wp-content/uploads/2015/07/tin-nhan-chuc-buoi-sang-7-.jpg) no-repeat center center;
            background-size: contain;
        }
```

Vì chiều rộng dài còn chiều cao thì ngắn nên nó sẽ fix theo chiều cao.

![17](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/17.png)

<a name="3"></a>
### 3. Thuộc tính background-origin trong CSS3:

Thuộc tính `background-origin` dùng để xác định nơi mà hình ảnh sẽ hiển thị. Gồm 3 giá trị sau đây:

- **border-box**: Biên của background tính luôn border ngoài cùng.

- **padding-box**: biên của background tính từ vị trí padding (sát lề border)

- **content-box**: biên của background tính từ vị trí có thể sử dụng.

**Ví dụ**:

```javascript
		div{
               width: 350px;
               height: 200px;
               margin: 20px auto;
               border: 20px solid red;
               padding: 50px;
               background: url(http://thegioihinhanh.com/uploads/images/nh%E1%BB%AFng%20h%C3%ACnh%20%E1%BA%A3nh%20%C4%91%E1%BA%A1i%20di%E1%BB%87n%20fb%20d%E1%BB%85%20th%C6%B0%C6%A1ng%203.jpg) no-repeat top left;
            }
            #div1{
                background-origin: border-box;
            }
            #div2{
                background-origin: padding-box;
            }
            #div3{
                background-origin: content-box;
            }
```

![14](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/14.png)

![16](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/16.png)

![15](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/15.png)


<a name="4"></a>
### 4. Thuộc tính background-clip trong CSS3:

Dùng để xác định nơi mà **background color** sẽ hiển thị. Nó cũng tương tự như `background-origin` nó sẽ có tác dụng với background image.

```javascript
 		div{
               width: 150px;
               height: 80px;
               margin: 20px auto;
               border: dotted; 10px;
               padding: 30px;
               background: aqua;
            }

            #div1{
                background-clip: border-box;
            }

            #div2{
                background-clip: padding-box;
            }

            #div3{
                background-clip: content-box;
            }
```

![18](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/18.png)

