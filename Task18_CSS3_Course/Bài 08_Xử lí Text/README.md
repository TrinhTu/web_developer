## Bài 8: HỌC CSS3 - XỬ LÍ TEXT

> Tài liệu: Xử lí Text
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[1. Text Overflow trong CSS3](#1)

[2. Word Wrap trong CSS3](#2)

[3. Word Break trong CSS3](#3)

[4. Tài liệu tham khảo](#4)

<a name="1"></a>
### 1. Text Overflow trong CSS3:

- Thuộc tính `text-overflow` dùng để xử lý một đoạn text khi bị tràn ra ngoài thẻ HTML.

- Cú pháp: `text-overflow: clip|ellipsis|string|initial|inherit;`

- Trong đó:

    - **clip**: là giá trị mặc định, nó sẽ kẹp các văn bản.

    - **ellipsis** : thêm ba dấu chấm (...) nếu text bị tràn ra ngoài

    - **string** : tự định nghĩa đoạn text nào đó thêm vào khi bị tràn ra ngoài.

    - **initial** : thiết lập giá trị mặc định

    - **inherit** : kế thừa giá trị từ thẻ HTML cha.

- Cần phải bổ sung thêm thuộc tính `overflow: hidden` thì mới có tác dụng.

**Ví dụ**

```
    <style type="text/css">
        h2{
            white-space: nowrap;
            border: 5px solid blue;
            width: 400px;
            height: 100px;
            font-size: 50px;
            text-overflow: ellipsis;
            overflow: hidden;
        }
    </style>
    </head>
    <body>
        <h2>Chào mừng tất cả các bạn đến với trang web học CSS3 của tôi</h2>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/40.png"/></p>

<a name="2"></a>
### 2. Word Wrap trong CSS3:

- Thuộc tính `word-wrap` cho phép đoạn text xuống hàng cho dù chữ đó dài cỡ nào đi nữa.

- Cú pháp: `word-wrap: normal|break-word|initial|inherit;`

- Trong đó:

    - **normal**: trạng thái mặc định, tức là hiển thị theo mặc định của trình duyệt

    - **break-word** : sẽ nhảy xuống hàng nếu chữ quá dài

    - **initial** : trở về trang thái mặc định

    - **inherit** : kế thừa giá trị từ thẻ HTML cha

**Ví dụ**

```
<style>
       div{
            border: solid 1px red;
            width: 100px;
            color: blue;
            font-size: 20px;
        }
        .breakword{
            word-wrap: break-word;
        }
        </style>
    </head>
    <body>
        <h2>No break-word</h2>
        <div>ChaoMungTatCaCacBanDenVoiTrangWebCuaTrinh</div>
        <h2>Break-word</h2>
        <div class='breakword'>ChaoMungTatCaCacBanDenVoiTrangWebCuaTrinh</div>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/41.png"/></p>

<a name="3"></a>
### 3. Word Break trong CSS3:

- Thuộc tính `word-break` trong CSS3 có tác dụng xử lý xuống hàng, tức là bạn có thể cho một chuỗi hiển thị và xuống hàng tại bất kì vị trí nào miễn là nó đã hiển thị full width.

- Cú pháp: `word-break: normal|break-all|keep-all|initial|inherit;`

- Trong đó:

    - **normal**: trạng thái mặc định, tức là sẽ dừng xuống hàng theo mặc định

    - **break-all** : có thể xuống hàng bất kì lúc nào khi nó đã hiển thị full width

    - **keep-all** : xuống hàng nếu chữ hiển thị sẽ bị tràn (overflow)

    - **initial** : trở về trang thái mặc định

    - **inherit** : kế thừa giá trị từ thẻ HTML cha

**Ví dụ**

```
    <style>
        div{
            border: solid 1px red;
            width: 150px;
            color: blue;
            font-size:30px;
        }
        .break-all{
            word-break: break-all;
        }
        .keep-all{
            word-break: keep-all;
        }
    </style>
    </head>
    <body>
        <h2>Break All</h2>
        <div class="keep-all">Chào mừng các bạn đến với trang web của Trinh</div>
        <h2>Keep All</h2>
        <div class="break-all">Chào mừng các bạn đến với trang web của Trinh</div>
    </body>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/42.png"/></p>

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Freetuts Blog. CSS3 căn bản
>
> Online: http://freetuts.net/hoc-css3-xu-ly-text-482.html
