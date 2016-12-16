## Bài 9: HỌC CSS3 - SỬ DỤNG @FONT-FACE

> Tài liệu: Sử dụng @font-face
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/12/2016

### Mục lục:

[1. Một số định dạng file font](#1)

[2. Sử dụng @font-face](#2)

<a name="1"></a>
### 1. Một số định dạng file font:

- **TrueType Fonts (TTF)**: TrueType là một định dạng được phát triển vào cuối những năm 1980 bởi Apple và Microsoft, đây là định dạng font phổ biến cho các hệ điều hành Mac OS và Windows.

- **OpenType Fonts (OTF)**: OpenType là một định dạng được phát triển dựa trên nền tảng của TrueType và nó đã được đăng ký thương hiệu bởi Microsoft. Font chữ OpenType được sử dụng phổ biến hiện nay trên các nền tảng máy tính lớn.

- **The Web Open Font Format (WOFF)**: WOFF là một định dạng sử dụng trong các trang web, nó được phát triển vào năm 2009. WOFF bản chất là một OpenType hoặc TrueType được bổ sung một số siêu dữ liệu giúp việc truyền tải qua mạng nhẹ nhàng hơn. W3C khuyến khích sử dụng định dạng này.

- **The Web Open Font Format (WOFF 2.0)**: TrueType/OpenType là một bản nén tuyệt vời hơn WOFF 1.0.

- **SVG Fonts/Shapes**: SVG Fonts giúp hiển thị văn bản giống như một hình ảnh Graphic.

- **Embedded OpenType Fonts (EOT)**: EOT là một hình thức nén của OpenType, được phát triển bởi Microsoft và dùng để nhúng vào website.

- Danh sách các trình duyệt hỗ trợ kiểu font:

![43](https://github.com/TrinhTu/web_developer/blob/master/Task18_CSS3_Course/image/43.png)

<a name="2"></a>
### 2. Sử dụng @font-face:

- `@font-face` giống như 1 funciton gom nhiều thuộc tính CSS lại kết hợp với định dạng font giúp tạo ra những font theo ý muốn.

**Ví dụ**

```
@font-face{
    font-family: MyFont;
    src: url(sansation_light.woff);
    font-weight: 100;
}
h2{
    font-family: MyFont;
}
```

Có thể tham khảo thêm [tại đây](http://www.w3schools.com/css/css3_fonts.asp)