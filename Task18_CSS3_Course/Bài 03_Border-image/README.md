## Bài 3: HỌC CSS3 - BORDER - IMAGE - TẠO ĐƯỜNG VIỀN BẰNG HÌNH

> Tài liệu: Học CSS3 - border - image - tạo đường viền bằng hình
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/12/2016

### Mục lục:

[1. Border-image trong CSS3](#1)

- [SOURCE](#2)

- [OFFSET](#3)

- [REPEAT](#4)

[Tài liệu tham khảo](#2)

### Nội dung:

<a name="1"></a>
### 1. Border-image trong CSS3:

Thuộc tính **border-image** trong CSS3 dùng để thiết lập hình ảnh làm đường viền cho thẻ HTML. Thuộc tính này hỗ trợ các trình duyệt:

- IE > 11.0

- Chrome > 16.0

- Firefox > 15.5

- Safary > 6.0

- Opera > 15.0

> Chiều cao của đường viền phụ thuộc vào thuộc tính `border` vậy nên ta phải thiết lập `border` thì mới có thể sử dụng được `border-image`

Cú pháp: `border-image: url(border-image.png) 25 repeat;`

**Trong đó**

- `url(border-image.png)` (SOURCE) là đường dẫn đến file hình ảnh

- `25` (OFFSET) là kiểu ghi tắt của thuộc tính offset( đầy đủ sẽ gồm 4 tham số tương ứng với lề trên, lề phải, lề dưới và lề trái)

- `repeat` (REPEAT): cách sử dụng các hình ảnh đã cắt.

**Code Hack CSS cho các trình duyệt:**

- `-webkit-border-image`: Chrome and Safaty

- `-moz-border-image`: đối với Firefox

- `-o-border-image`: đối với Opera


<a name="2"></a>
#### SOURCE:

- Đây là đường dẫn đến file hình ảnh dùng là border.

<a name="3"></a>
#### OFFSET:

Offset là khoảng cách tính từ ngoài bên đi vào trong hình ảnh sẽ được lấy làm border

Thuộc tính offset gồm 4 cạnh, và giá trị của OFFSET tuân theo quy tăc rút gọn như sau:

- Nếu có 4 giá trị `25 25 25 25` sẽ tương ứng với các cạnh như sau: trên, phải, dưới, trái.

- Nếu có 3 giá trị `25 25 25` sẽ tương ứng với các cạnh như sau: trên, trái+phải, dưới.

- Nếu có 2 giá trị `25 25` sẽ tương ứng với các cạnh như sau: trên+dưới, trái+phải

- Nếu có 1 giá trị `25` sẽ tương ứng với các cạnh như sau: trên + dưới + trái + phải.

![7](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/7.png)

Phần 1,3,7,9 là phần **border cho 4 góc** và nó là cố định, còn phần 5 sẽ là vị trí trung tâm. Những phần còn lại sẽ bị ảnh hưởng bởi thuộc tính REPEAT.

<a name="4"></a>
#### REPEAT:

Chúng ta có các giá trị thường sử dụng như sau:

- stretch

- repeat

- round

> Các giá trị này chỉ tác dụng với các phần 2,6,8,4.

**Stretch**: kéo giãn hình ảnh tương ứng với chiều dài các cạnh.

Ví dụ:

```javascript
	div{
            width: 300px;
            height: 200px;
            border-style: solid;
            border-width: 60px;
            border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 stretch;
            -webkit-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 stretch;
            -moz-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 stretch;
            -o-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 stretch;
        }
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/9.png"/></p>

**Repeat**: lặp lại hình ảnh cho các cạnh. ( lặp từ giữa đi ra 2 phía)

```javascript
 	div{
            width: 300px;
            height: 200px;
            border-style: solid;
            border-width: 60px;
            border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 repeat;
            -webkit-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 repeat;
            -moz-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 repeat;
            -o-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 repeat;
        }
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/8.png"/></p>

**Round**: lặp lại hình ảnh cho các cạnh nhưng nó sẽ fix theo tỉ lệ phần trăm, co giãn sao cho lặp lại vừa khít.

```javascript
	div{
            width: 300px;
            height: 200px;
            border-style: solid;
            border-width: 60px;
            border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 round;
            -webkit-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 round;
            -moz-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 round;
            -o-border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 round;
        }
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/10.png"/></p>

**Lưu ý**: Giá trị của repeat có thể chia làm 2 phần đó là Vertical (round) và Horizontal (repeat).

`border-image: url(http://hinh-nen.org/images/131021khung-anh-la-mua-thu.jpg) 60 round repeat;`

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Freetuts Blog. CSS3 căn bản.
>
> Online: http://freetuts.net/hoc-css3-border-image-tao-duong-vien-bang-hinh-477.html

