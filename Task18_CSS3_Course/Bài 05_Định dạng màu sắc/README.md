## Bài 5: HỌC CSS3 - ĐỊNH DẠNG MÀU SẮC

> Tài liệu: Định dạng màu sắc
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/12/2016

### Mục lục:

[1. RGBA Colors](#1)

[2. HSL Colors](#2)

[3. HSLA Colors](#3)

[4. Opacity](#4)

[5. HEX Colors](#5)

[6. Color Name](#6) 

[7. Tài liệu tham khảo](#7)

<a name="1"></a>
### 1. RGBA Colors:

- RGBA color là phần mở rộng của RGB color với phần bổ sung là chỉ số opacity. Cú pháp của loại màu này là `rgba(red, green, blue, alpha)` trong đó alpha có giá trị từ [0->1] càng gần về 0 thì màu sắc càng mờ và 1 là giá trị đậm nhất.

**Ví dụ**: 

```javascript
 	<style type="text/css">
            p{
                width: 250px;
                height: 30px;
                 margin-left: 500px;
            }
            #red{
                background-color: rgba(255,0,0,1);
            }
            #green{
                background-color: rgba(0,255,0,1);
            }
            #blue{
                background-color: rgba(0,0,255,1);
            }
            #gray{
                background-color: rgba(192,192,192,1);
            }
            #yellow{
                background-color: rgba(255,255,0,1);
            }
        </style>
    </head>
    <body>
        <p id='red'>red</p>
        <p id='green'>green</p>
        <p id='blue'>blue</p>
        <p id='gray'>gray</p>
        <p id='yellow'>yellow</p>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/19.png"/></p>


<a name="2"></a>
### 2. HSL Colors:

- Là viết tắt của Hue, Saturation và Lightness kí hiệu của nó là: `hsl(hue,saturation,lightness)`

+ Trong đó:

	- **Hue** có giá trị từ 0->360, giá trị 0 hoặc 360 là màu đỏ.

	- **Saturation** có giá trị phần trăm (%) và cao nhất là 100%.

	- **Lightness** cũng có giá trị phần trăm, 0% là màu đen và 100% là màu trắng.

**Ví dụ**:

```javascript
	<style type="text/css">
			p{
                width: 300px;
                height: 40px;
                margin-left: 500px;
            }
            #green {background-color:hsl(120,100%,50%);}
            #light-green {background-color:hsl(120,100%,75%);}
            #dark-green {background-color:hsl(120,100%,25%);}
            #pastel-green {background-color:hsl(120,60%,70%);}
            #violet {background-color:hsl(290,100%,50%);}
            #pastel-violet {background-color:hsl(290,60%,80%);}
    </style>
    <body>
        <p id='green'>Green</p>
        <p id='light-green'>Light Green</p>
        <p id='dark-green'>Dark Green</p>
        <p id='pastel-green'>Pastel Green</p>
        <p id='violet'>Violet</p>
        <p id='pastel-violet'>Pastel violet</p>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/20.png"/></p>


<a name="3"></a>
### 3. HSLA Colors:

- HSLA Color là phần mở rộng của HSL color với phần bổ sung là giá trị của alpha (opacity color). Cú pháp của loại màu này là: `hsla(hue, saturation, lightness, alpha).

	+ **Hue** có giá trị từ 0->360, giá trị 0 hoặc 360 là màu đỏ.

	+ **Saturation** có giá trị phần trăm (%) và cao nhất là 100%.

	+ **Lightness** cũng có giá trị phần trăm, 0% là màu đen và 100% là màu trắng.

	+ **Alpha** có giá trị từ [0->1], giá trị càng gần về 0 thì màu sắc càng mờ, giá trị 1 là màu đậm nhất.

**Ví dụ**:

```javascript
		<style type="text/css">
            #green {background-color:hsla(120,100%,50%, 0.3);}
            #light-green {background-color:hsla(120,100%,75%,0.3);}
            #dark-green {background-color:hsla(120,100%,25%,0.3);}
            #pastel-green {background-color:hsla(120,60%,70%,0.3);}
            #violet {background-color:hsla(290,100%,50%,0.3);}
            #pastel-violet {background-color:hsla(290,60%,70%,0.3);}
        </style>
        <head>
        <body>
        	<p id="green">Green</p>
        	<p id="light-green">Light Green</p>
        	<p id="dark-green">Dark Green</p>
        	<p id="pastel-green">Pastel Green</p>
        	<p id="violet">Violet</p>
        	<p id="pastel-violet">Pastel violet</p>
    	</body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/21.png"/></p>

<a name="4"></a>
### 4. Opacity:
 
- Dùng để bổ sung giá trị alpha cho mã màu HSL.

**Ví dụ**:

```javascript
	<style type="text/css">
            #green {background-color:hsl(120,100%,50%); opacity: 0.3}
            #light-green {background-color:hsl(120,100%,75%); opacity:0.3}
            #dark-green {background-color:hsl(120,100%,25%); opacity: 0.3}
            #pastel-green {background-color:hsl(120,60%,70%); opacity:0.3}
            #violet {background-color:hsl(290,100%,50%); opacity: 0.3}
            #pastel-violet {background-color:hsl(290,60%,70%); opacity: 0.3}
    </style>
    </head>
    <body>
        <p id="green">Green</p>
        <p id="light-green">Light Green</p>
        <p id="dark-green">Dark Green</p>
        <p id="pastel-green">Pastel Green</p>
        <p id="violet">Violet</p>
        <p id="pastel-violet">Pastel violet</p>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/22.png"/></p>


<a name="5"></a>
### 5. HEX Colors:

Đây là mã màu thông dụng nhất không chỉ ở CSS mà trong các công cụ thiết kế như Photoshop cũng sử dụng. Cấu trúc của nó như sau: `#xxxxxx`. Trong đó dấu `#` là khai báo loại mã màu HEX và `xxxxxx` là giá trị (chữ cái hoặc số)

- Xem thêm về bảng mã màu [tại đây](http://vforum.vn/diendan/showthread.php?61619-Bang-ma-mau-HEX-RGB-CMYK-day-du-cho-CSS-HTML)

<a name="6"></a>
### 6. Color Name:

Đây là cú pháp đơn giản nhất để xác định mã màu trong CSS nhưng nó không phải là bản chuẩn của color và cũng không chứa đầy đủ.

**Ví dụ**: 

- black: màu đen

- red: màu đỏ

- pink: màu hồng

...

<a name="7"></a>
### Tài liệu tham khảo:

> [1] Freetuts Blog. CSS3 căn bản.
>
> Online: http://freetuts.net/hoc-css3-dinh-dang-mau-sac-479.html



