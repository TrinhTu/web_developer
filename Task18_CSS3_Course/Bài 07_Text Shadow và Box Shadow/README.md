## Bài 7: HỌC CSS3 - TEXT SHADOW - BOX SHADOW

> Tài liệu: Text Shadow - Box Shadow
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[1. Text-shadow trong CSS3](#1)

- [Sử dụng nhiều color shadow](#1.1)

[2. Box-shadow trong CSS3](#2)

- [Sử dụng nhiều shadow](#2.1)

<a name="1"></a>
### 1. Text-shadow trong CSS3:

- Thuộc tính CSS3 `text-shadow` bổ sung thêm hiệu ứng shadow vào 1 đoạn text giúp nó hiển thị giống chữ 3D chuyên nghiệp.

**Ví dụ**

```
   <style type="text/css">
        h1{
            color: blue;
            text-shadow: 2px 2px;
            text-align: center;
        }
    </style>
    <body>
        <h1>Xin chào các bạn</h1>
    </body>
```

![34](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/34.png)

**Cú pháp**

`text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;`

- Trong đó:

    - **h-shadow**: vị trí bóng ngang so với chữ, số âm sẽ đẩy lên trên và số dương sẽ đẩy xuống dưới.

    - **v-shadow** : vị trí bóng dọc so với chứ, số âm sẽ đẩy lui phía sau và số dương sẽ đẩy tới phía trước

    - **blur-radius** : độ nhòe của chữ bóng, tính bằng pixel

    - **color** : màu sắc của bóng.

**Ví dụ**

```
    h1{
            color: blue;
            margin: 20px;
            float: left;
        }
        #heading1{
            text-shadow: 0px 0px 30px red;
        }
        #heading2{
            text-shadow: 0px 20px 2px green;
        }
        #heading3{
            text-shadow: 5px -10px 2px black;
        }
        #heading4{
            text-shadow: 10px 10px 5px yellow;
        }
    </style>
    <body>
        <h1 id="heading1">Xin chào các bạn</h1>
        <h1 id="heading2">Xin chào các bạn</h1>
        <h1 id="heading3">Xin chào các bạn</h1>
        <h1 id="heading4">Xin chào các bạn</h1>
    </body>
```

![35](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/35.png)

<a name="1.1"></a>
#### Sử dụng nhiều color shadow:

- Nếu muốn shadow có nhiều màu sắc thì phải bổ sung thêm shadow cho nó và chúng cách nhau bởi dấu phẩy.

**Ví dụ**

```
        h1{
            color: blue;
            margin: auto;
            text-align: center;
            font-size: 50px;
            text-shadow:
            0px 0px 10px red,
            5px 5px 5px green,
            -5px -5px 5px yellow;
        }
```

![36](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/36.png)

<a name="2"></a>
### 2. Box-shadow trong CSS3:

- Hiệu ứng tương tự như `text-shadow` nhưng có tác dụng tuyệt đối với đường viền (lề) chứ không tác dụng với đoạn text.

**Ví dụ**

```
        h1{
            width: 300px;
            height: 200px;
            margin: 100px auto;
            text-align: center;
            box-shadow: 0px 0px 20px red;
           
        }
```

![37](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/37.png)

- Cú pháp của box-shadow như sau:

`box-shadow: h-shadow v-shadow blur spread color |inset|initial|inherit;`

- Trong đó:

    - h-shadow : vị trí bóng ngang so với chữ, số âm sẽ đẩy lên trên và số dương sẽ đẩy xuống dưới

    - v-shadow : vị trí bóng dọc so với chứ, số âm sẽ đẩy lui phía sau và số dương sẽ đẩy tới phía trước.

    - blur-radius : độ nhòe của chữ bóng, tính bằng pixel.

    - spread: kích thước của bóng tối.

    - color : màu sắc của bóng.

    - inset: thay đổi bóng từ bên ngoài vào trong thay vì từ trong ra ngoài.

    - initial: thiết lập giá trị mặc định.

    - inherit: kế thừa giá trị từ thẻ HTML cha.

**Ví dụ**

```
        #box1{
            box-shadow: 0px 0px 12px 10px blue;
            -moz-box-shadow: 0px 0px 10px 10px blue;
            -webkit-box-shadow: 0px 0px 10px 10px blue;
        }
        #box2{
            box-shadow: 0px 0px 12px 10px green inset;
            -moz-box-shadow: 0px 0px 12px 10px green inset;
            -webkit-box-shadow: 0px 0px 12px 10px green inset;
        }
        #box3{
            box-shadow: 5px 5px 12px 0px yellow;
            -moz-box-shadow: 5px 5px 12px 0px yellow;
            -webkit-box-shadow: 5px 5px 12px 0px yellow;
        }
        #box4{
            box-shadow: -5px -5px 0px 0px red;
            -moz-box-shadow: -5px -5px 0px 0px red;
            -webkit-box-shadow: -5px -5px 0px 0px red;
        }
```

![38](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/38.png)

<a name="2.1"></a>
#### Sử dụng nhiều shadow:

**Ví dụ**

```
        h2{
            height: 200px;
            width: 300px;
            margin: 50px auto;
            border: solid 2px black;
            box-shadow: 
                0px 0px 5px 5px red,
                0px 0px 5px 10px yellow,
                0px 0px 5px 15px aqua;
            -moz-box-shadow: 
                0px 0px 5px 5px red,
                0px 0px 5px 10px yellow,
                0px 0px 5px 15px aqua;
            -webkit-box-shadow: 
                0px 0px 5px 5px red,
                0px 0px 5px 10px yellow,
                0px 0px 5px 15px aqua;
        }
```

![39](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/39.png)
