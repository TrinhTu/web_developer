##Bài 14: Reset CSS là gì và vì sao nên reset CSS

> Tài liệu: Reset CSS là gì và vì sao nên reset CSS
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 30/10/2016

###Mục lục:

[1. Reset CSS như thế nào](#1)

[2. Một số bộ reset CSS thông dụng](#2)

###Nội dung:

Khi sử dụng HTML thì trình duyệt đã tự mặc định hiển thị 1 số thẻ HTML thanhf1 đoạn văn bản đã được định dạng đầy đủ, nhưng khi sử dụng CSS chúng ta muốn chúng có thể hiển thị như theo ý mình tức là xóa các định dạng đã có sẵn trong HTML đi và sử dụng CSS để đảm bảo nó hiển thị tốt ở mọi trình duyệt, việc này là Reset CSS.

<a name="1"></a>
####1. Reset CSS như thế nào:

Cách đơn giản nhất là viết 1 tập tin CSS như sau và đưa toàn bộ giá trị trong đó về 0:

```
* {
	padding: 0;
	margin:0;
	border:none;
}
```

<a name="2"></a>
####2. Một số bộ reset CSS thông dụng

Thay vì tự reset như vậy theo cách không được tối ưu cho lắm thì chúng ta có các bộ reset CSS thông dụng như sau:

[normalize.css](https://github.com/necolas/normalize.css/blob/master/normalize.css)

Đây là bộ reset thông dụng nhất phù hợp với HTML5 và CSS3, nó sẽ điều chỉnh các phần tử trong website phù hợp với tất cả các trình duyệt thông dụng, xóa bỏ toàn bộ margin padding có sẵn style cho các thẻ `<sub>`, `<sup>` `<code>` 

[Reset CSS 2.0 by Eric Meyer](http://meyerweb.com/eric/tools/css/reset/)

Bộ reset này giúp đưa toàn bộ website về ban đầu không có bất cứ định dạng nào, khi sử dụng bộ reset này mình sẽ phải tự viết lại CSS cho toàn bộ các thành phần trong website.

Đầu tiên chúng ta tạo 1 tập tin HTML thông thường.

![10](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_14/image/10.png)

Sau đó tạo thêm tập tin CSS lưu với thư mục cùng tên với đường dẫn HTML tìm đến **.css**. Copy và paste lại bộ reset mà ta muốn sử dụng rồi lưu lại.

![11](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_14/image/11.png)

Và đây là 1 văn bản HTML đã được reset:

![12](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_14/image/12.png)

