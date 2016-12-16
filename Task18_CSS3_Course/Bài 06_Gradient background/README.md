## Bài 6: HỌC CSS3 - GRADIENT BACKGROUND

> Tài liệu: Gradient Background
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[1. Linear Gradient trong CSS3](#1)

- [Sử dụng Angles](#1.1)

- [Sử dụng nhiều màu](#1.2)

- [Sử dụng Transparency](#1.3)

- [Lặp-repeating-linear-gradient](#1.4)

[2. Radial Gradients trong CSS3](#2)

- [Phân chia khoảng cách màu đồng đều](#2.1)

- [Tùy chọn bảng màu](#2.2)

- [Tùy chọn size](#2.3)

- [Tùy chọn Position](#2.4)

- [Lặp-repeating-radial-gradient](#2.5)

<a name="1"></a>
### 1. Linear Gradients trong CSS3:

- **Cú pháp**:

    `background: linear-gradient(direction, color1, color2, color3,...)`

- Trong đó `direction` gồm các giá trị:

    - Giá trị đơn `to top` hoặc `to left` hoặc `to right` `to bottom` thì nó sẽ kéo sang cạnh đối diện.

    - Giá trị đôi (`to top left`) hoặc (`to top right`) chỉ rõ kéo từ cạnh nào sang cạnh nào.

Nếu ta không truyền `direction` thì sẽ mặc định có giá trị `top`

**Code hack CSS như sau:**

```
    background: -webkit-linear-gradient(direction, color1, color2, color3,...);
    background: -o-linear-gradient(direction, color1, color2, color3,...);
    background: -moz-linear-gradient(direction, color1, color2, color3,...);
```

Đối với code hack CSS thì `direction` không có `to`.

**Ví dụ**

```javascript
        div{
            width: 200px;
            height: 150px;
            float: left;
            margin: 30px;
        }
        #box1{
            background: linear-gradient(aqua, yellow);
        }
        #box2{
            background: linear-gradient(to left, aqua, yellow);
            background: -webkit-linear-gradient(left, aqua, yellow);
            background: -o-linear-gradient(left, aqua, yellow);
            background: -moz-linear-gradient(left, aqua, yellow);
        }
        #box3{
            background: linear-gradient(to right, aqua, yellow);
            background: -webkit-linear-gradient(right, aqua, yellow);
            background: -o-linear-gradient(right, aqua, yellow);
            background: -moz-linear-gradient(right, aqua, yellow);
        }
        #box4{
            background: linear-gradient(to bottom left, aqua, yellow);
            background: -webkit-linear-gradient(bottom left, aqua, yellow);
            background: -o-linear-gradient(bottom left, aqua, yellow);
            background: -moz-linear-gradient(bottom left, aqua, yellow);
        }
    </style>
    <body>
        <div id="box1"></div>
        <div id="box2"></div>
        <div id="box3"></div>
        <div id="box4"></div>
    </body>
```

![23](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/23.png)

<a name="1.1"></a>
#### Sử dụng Angles:

- Sử dụng góc thay vì xác định hướng (to left, to right,...) bằng cách sử dụng cú pháp sau:

        `background: linear-gradient(angle, color-stop1, color-stop2);`

- Trong đó Angle là góc xác định giữa đường ngang và đường Gradient ngược chiều kim đồng hồ. Túc là 0deg  sẽ tạo bottom to top Gradient, 90deg sẽ tạo left to right Gradient.

**Ví dụ**

```javascript
    <style type="text/css">
        div{
            width: 200px;
            height: 150px;
            float: left;
            margin: 30px;
        }
        #box1{
            background: linear-gradient(0deg, aqua, yellow);
            background: -webkit-linear-gradient(0deg, aqua, yellow);
            background: -o-linear-gradient(0deg, aqua, yellow);
            background: -moz-linear-gradient(0deg, aqua, yellow);
        }
        #box2{
            background: linear-gradient(90deg, aqua, yellow);
            background: -webkit-linear-gradient(90deg, aqua, yellow);
            background: -o-linear-gradient(90deg, aqua, yellow);
            background: -moz-linear-gradient(90deg, aqua, yellow);
        }
        #box3{
            background: linear-gradient(180deg, aqua, yellow);
            background: -webkit-linear-gradient(180deg, aqua, yellow);
            background: -o-linear-gradient(180deg, aqua, yellow);
            background: -moz-linear-gradient(180deg, aqua, yellow);
        }
        #box4{
            background: linear-gradient(360deg, aqua, yellow);
            background: -webkit-linear-gradient(360deg, aqua, yellow);
            background: -o-linear-gradient(360deg, aqua, yellow);
            background: -moz-linear-gradient(360deg, aqua, yellow);
        }
    </style>
    <body>
        <div id="box1"></div>
        <div id="box2"></div>
        <div id="box3"></div>
        <div id="box4"></div>
    </body>
```

![24](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/24.png)

<a name="1.2"></a>
#### Sử dụng nhiều màu:

- Nếu muốn trộn nhiều màu với nhau thì bổ sung màu vào thuộc tính Gradient, nhưng cần phải sắp xếp đúng thứ tự màu.

**Ví dụ**:

```javascript
    <style type="text/css">
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background: linear-gradient(to bottom, red, yellow, green, pink, tomato,aqua);
            background: linear-gradient(bottom, red, yellow, green, pink, tomato,aqua);
            background: linear-gradient(bottom, red, yellow, green, pink, tomato,aqua);
            background: linear-gradient(bottom, red, yellow, green, pink, tomato,aqua);
        }
    </style>
    <body>
        <div></div>
    </body>
```

![25](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/25.png)

<a name="1.3"></a>
#### Sử dụng Transparency:

- Kết hợp với HSLA color hoặc RGBA color để tạo độ trong suốt.

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background: linear-gradient(to bottom, rgba(255,0,0,0.2), red);
            background: -webkit-linear-gradient(to bottom, rgba(255,0,0,0.2), red);
            background: -o-linear-gradient(to bottom, rgba(255,0,0,0.2), red);
            background: -moz-linear-gradient(to bottom, rgba(255,0,0,0.2), red);
        }
```

![26](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/26.png)

<a name="1.4"></a>
#### Lặp-repeating-linear-gradient:

- Lặp lại trên 1 khoảng nào đó ta dùng thuộc tính: `repeating-linear-gradient`

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background : repeating-linear-gradient(to bottom, pink 10%, aqua 20%);
            background : -moz-repeating-linear-gradient(bottom, pink 10%, aqua 20%);
            background : -webkit-repeating-linear-gradient(bottom, pink 10%, aqua 20%);
            background : -o-repeating-linear-gradient(bottom, pink 10%, aqua 20%);
            }
```

![27](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/27.png)

<a name="2"></a>
### 2. Radial Gradients trong CSS3:

- Dùng để tạo hiệu ứng tại vị trí nào đó và lan tỏa ra từ các phía, và để có hiệu ứng chắc chắn thì phải sử dụng ít nhất hai màu khác nhau.

**Cú pháp**

`background: radial-gradient(shape size at position, start-color,..., last color);`

- Trong đó Shape mặc định là hình **Ellipse**, size là **farthest-cornet** và position là **center**.

<a name="2.1"></a>
#### Phân chia khoảng màu đồng đều:

- Mặc định các màu sẽ được chia 1 khoảng không gian bằng nhau.

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background: radial-gradient(red, yellow, aqua);
            background: -moz-radial-gradient(red, yellow, aqua);
            background: -webkit-radial-gradient(red, yellow, aqua);
            background: -o-radial-gradient(red, yellow, aqua);
            }   
```

![28](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/28.png)

<a name="2.2"></a>
#### Tùy chọn khoảng màu:

- Nếu muốn mỗi màu chiếm 1 khoảng bao nhiêu thì thêm số % đằng sau nó, tính từ vị trí trung tâm thì màu sau phải có số % lớn hơn màu trước.

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background: radial-gradient(red 20%, yellow 50%, pink 70%);
            background: -moz-radial-gradient(red 20%, yellow 50%, pink 70%);
            background: -webkit-radial-gradient(red 20%, yellow 50%, pink 70%);
            background: -o-radial-gradient(red 20%, yellow 50%, pink 70%);
            } 
```

![29](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/29.png)

<a name="2.3"></a>
#### Tùy chọn Shape:

- Mặc định là **ellipse** nhưng có thể thay bằng **circle**

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 200px;
            margin: auto;
            background: radial-gradient(circle, red 10%, yellow 90%);
            background: -moz-radial-gradient(circle, red 10%, yellow 90%);
            background: -webkit-radial-gradient(circle,red 10%, yellow 90%);
            background: -o-radial-gradient(circle, red 10%, yellow 90%);
            }   
```

![30](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/30.png)

<a name="2.4"></a>
#### Tùy chọn Size:

- Chúng ta có 4 giá trị sau:

    - closest-side

    - farthest-side

    - closest-corner

    - farthest-corner

- Mặc định nếu không chọn size thì nó sẽ là: **farthest-side**

**Ví dụ**

```javascript
        div{
            width: 200px;
            height: 150px;
            margin: 20px;
            float: left;
            } 
        #box1{
            background: radial-gradient(circle closest-side, tomato, aqua);
            background: -webkit-radial-gradient(circle closest-side, tomato, aqua);
            background: -o-radial-gradient(circle closest-side, tomato, aqua);
            background: -moz-radial-gradient(circle closest-side, tomato, aqua);
        }  
        #box2{
            background: radial-gradient(circle farthest-side, tomato, aqua);
            background: -webkit-radial-gradient(circle farthest-side, tomato, aqua);
            background: -o-radial-gradient(circle farthest-side, tomato, aqua);
            background: -moz-radial-gradient(circle farthest-side, tomato, aqua);
        }
        #box3{
            background: radial-gradient(circle closest-corner, tomato, aqua);
            background: -webkit-radial-gradient(circle closest-corner, tomato, aqua);
            background: -o-radial-gradient(circle closest-corner, tomato, aqua);
            background: -moz-radial-gradient(circle closest-corner, tomato, aqua);
        }
        #box4{
            background: radial-gradient(circle farthest-corner, tomato, aqua);
            background: -webkit-radial-gradient(circle farthest-corner, tomato, aqua);
            background: -o-radial-gradient(circle farthest-corner, tomato, aqua);
            background: -moz-radial-gradient(circle farthest-corner, tomato, aqua);
        }
```

![31](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/31.png)

<a name="2.5"></a>
#### Tùy chọn Position:

- Nếu muốn vị trí trung tâm không nằm giữa nữa thì có thể chọn 1 vị trí bất kì bằng cách nhập khoảng cách so với lề bên trái và lề trên, đơn vị của nó là `%` hoặc `px`

**Ví dụ**

```javascript
         div{
            width: 350px;
            height: 200px;
            margin: auto;
            background: radial-gradient(circle farthest-side at 100px 200px, tomato 30%, aqua 70%);
            background: -webkit-radial-gradient(circle, 100px 200px, farthest-side, tomato 30%, aqua 70%);
            background: -o-radial-gradient(circle, 100px 200px, farthest-side, tomato 30%, aqua 70%);
            background: -moz-radial-gradient(circle, 100px 200px, farthest-side, tomato 30%, aqua 70%);
            }
```

![32](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/32.png)

<a name="2.6"></a>
#### Lặp-repeating-radial-gradient:

- Tương tự như Linear Gradient ta có thể repeat Radial Gradient bằng cách sử dụng thuộc tính `repeating-radial-gradient`

**Ví dụ**

```javascript
        div{
            width: 300px;
            height: 300px;
            margin: auto;
            border: 5px solid red;
            background: repeating-radial-gradient(circle farthest-side, black 10%, white 20%);
            background: -webkit-repeating-radial-gradient(circle, farthest-side, black 10%, white 20%);
            background: -o-repeating-radial-gradient(circle, farthest-side, black 10%, white 20%);
            background: -moz-repeating-radial-gradient(circle, farthest-side, black 10%, white 20%);
            }
```

![33](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/33.png)