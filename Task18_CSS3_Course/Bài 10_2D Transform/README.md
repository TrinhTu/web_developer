## Bài 9: HỌC CSS3 - 2D TRANSFORMS

> Tài liệu: 2D Transforms
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[1. Transform translate() trong CSS3](#1)

[2. Transform rotate() trong CSS3](#2)

[3. Transform Scale() trong CSS3](#3)

[4. Transform skew()-skewX()-skewY() trong CSS3](#4)

[5. Transform matrix() trong CSS3](#5)

<a name="1"></a>
### 1. Transform translate() trong CSS3:

- `Translate()` có tác dụng di chuyển đối tượng HTML từ vị trí hiện tại của nó.

- Có 2 tham số truyền như sau: `translate(xpx, ypx)`.

- Trong đó:

    - `xpx` là di chuyển theo hướng trái (nếu só dương) và phải (nếu số âm)

    - `ypx` là di chuyên theo hướng xuống (nếu số dương) và lên (nếu số âm)

- Code hack CSS:

```
/* IE 9 */
-ms-transform: translate(50px,100px); 
/* Safari */
-webkit-transform: translate(50px,100px);
```

**Ví dụ**

```
    div{
            width: 300px;
            height: 200px;
            background: pink;
        }
        div:hover{
            transform: translate(20px, 20px);
            -ms-transform: translate(20px, 20px);
            -webkit-transform: translate(20px, 20px);
        }
```

- Xem kết quả chuyển động [tại đây](http://tutrinh01.chuyengiaseoweb.net/CSS3.10.html)

<a name="2"></a>
### 2. Transform rotate() trong CSS3:

- Rotate() dùng để xoay đối tượng HTML theo 1 góc độ nào đó.

- **Cú pháp**: Có 1 tham số truyền vào chính là độ ta muốn xoay, nếu giá trị âm thì xoay ngược chiều kim đồng hồ và ngược lại.

```
-ms-transform: rotate(xdeg); /* IE 9 */
-webkit-transform: rotate(xdeg); /* Safari */
transform: rotate(xdeg);
```
**Ví dụ**

```
        div:hover{
            transform: rotate(50deg);
            -ms-transform: rotate(50deg);
            -webkit-transform: rotate(50deg);
        }
```

- Xem kết quả chuyển động [tại đây](http://tutrinh01.chuyengiaseoweb.net/css.html)

<a name="3"></a>
### 3. Transform Scale() trong CSS3:

- Scale() dùng để kéo giãn đối tượng HTML.

- Cú pháp

```
-ms-transform: scale(x, y); /* IE 9 */
-webkit-transform: scale(x, y); /* Safari */
transform: scale(x, y);<br><br>
```

- Trong đó: 
    
    - `x` là số lần tăng theo chiều rộng

    - `y` số lần tăng theo chiều cao

- Tức là giá trị nhập vào tỉ lệ với độ dài hiện tại

**Ví dụ**

```
    div:hover{
            transform: scale(1.5, 1.5);
            -ms-transform: scale(1.5, 1.5);
            -webkit-transform: scale(1.5, 1.5);
        }
```

- Xem kết quả [tại đây](http://tutrinh01.chuyengiaseoweb.net/scale.html)

<a name="4"></a>
### 4. Transform skew()-skewX()-skewY() trong CSS3:

- Dùng để bẻ góc độ của chiều rộng và chiều cao của đối tượng HTML.

- Cú pháp

```
-ms-transform: skew(xdeg, ydeg); /* IE 9 */
-webkit-transform: skew(xdeg, ydeg); /* Safari */
transform: skew(xdeg, ydeg);
```
- Trong đó:

    - `xdeg` là góc độ 2 cạnh bên

    - `ydeg` là góc độ 2 cạnh dưới

**Ví dụ**

```
        div:hover{
            transform: skew(30deg, 40deg);
            -ms-transform: skew(30deg, 40deg);
            -webkit-transform: skew(30deg, 40deg);
        }
```

- Xem kết quả [tại đây](http://tutrinh01.chuyengiaseoweb.net/skew.html)

<a name="5"></a>
### 5. Transform matrix() trong CSS3:

- Matrix() là hàm tổng hợp tất cả các thuộc tính ở trên, nó có 6 tham số cho phép xoay, di chuyển, kéo giãn đối tượng HTML.

**Đây là một thuộc tính khá phức tạp vậy nên cần tham khảo và nghiên cứu thêm [tại đây](http://www.useragentman.com/blog/2011/01/07/css3-matrix-transform-for-the-mathematically-challenged/)**