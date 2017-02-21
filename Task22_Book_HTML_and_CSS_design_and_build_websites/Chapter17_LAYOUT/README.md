## HTML & CSS

### HTML5 LAYOUT

> Chương 17: HTML5 LAYOUT
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 21/02/2017

## Mục lục:

[1. HTML5 layout elements](#1)

[2. Styling HTML5 layout elements with CSS](#2)

[Tài liệu tham khảo](#3)

***
<a name="1"></a>
### 1. HTML5 layout elements:

#### 1.1 TRADITIONAL HTML LAYOUTS:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter17_LAYOUT/1.png"/></p>

- Ở hình trên ta có thể thấy được bố cục thông thường được sử dụng cho website. Ở phần đầu của trang là tiêu đề dùng để chứa logo và đường dẫn sơ cấp. Phía dưới là 1 hay nhiều bài viết đôi khi là những liên kết tới bài viết cá nhân.

- Ở phía bên phải có 1 thanh dùng để tìm kiếm, liên kết đến các bài viết gần đây, các phần khác của trang web hoặc quảng cáo. Khi code 1 trang web thì các nhà phát triển thường đưa các nội dung chính của trang vào trong phần tử `<div>` và sử dụng thuộc tính class hay id để xác định mục đích của phần đó trong trang.

#### 1.2 NEW HTML5 LAYOUT ELEMNETS:

- HTML5 cung cấp 1 phần tử mới cho phép phân chia các phần của 1 trang, tên của phần tử đó chỉ ra các loại nội dung có thể tìm thấy trong đó. Trong ví dụ dưới đây cũng cung cấp cấu trúc chính xác của trang web tuy nhiền nhiều phần tử `<div>` trong đó đã được thay thế bằng bố trí phần tử HTML5 mới.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter17_LAYOUT/2.png"/></p>

- Ở ví dụ trên tiêu đề được đặt trong phần tử mới `<header>`, đường dẫn trong phần tử `<nav>` và bài viết cá nhân trong phần tử `<article>`. Điểm mới ở đây là có thể tạo ra các phần tử sử dụng cho mô tả cấu trúc của trang.

<a name="2"></a>
### 2. Styling HTML5 layout elements with CSS:

#### 2.1 HEADERS & FOOTERS:

`<header> <footer>`: 2 phần tử này được sử dụng cho:

- Tiêu đề chính và footer xuất hiện ở đầu cuối mỗi trang

- Header hoặc footer cho cá nhân `<article>` hay `<section>` trong trang.

```javascript
<header>
<h1>Yoko's Kitchen</h1>
<nav>
<ul>
<li><a href="" class="current">home</a></li>
<li><a href="">classes</a></li>
<li><a href="">catering</a></li>
<li><a href="">about</a></li>
<li><a href="">contact</a></li>
</ul>
</nav>
</header>
<footer>
&copy; 2011 Yoko's Kitchen
</footer>
```

- Trong ví dụ này phần tử `<header>` được sử dụng để chứa tên website và đường dẫn chính. Phần tử `<footer>` chứa thông tin bản quyền kèm với thông tin điều khoản bảo mật, chính sách và điều kiện. Mỗi cá nhân phần tử `<article>` và `<section>` cũng có thể chứa các `<header>` và `<footer>` của riêng chúng để chứa thông tin header và footer cho phần bên trong trang.

- Ví dụ: trên 1 trang với vài bài viết blog, mỗi bài viết cá nhân bao gồm các phần riêng biệt. Phần tử `<header>` được sử dụng để chứa các tiêu đề, ngày của mỗi bài viết cá nhân, và `<footer>` có thể chứa các liên kết để chia sẻ bài viết trên các trang mạng xã hội.

#### 2.2 NAVIGATION:

`<nav>`: phần tử `<nav>` được sử dụng để chứa đường dẫn chính tới website. Nếu muốn kết thúc 1 bài viết với các liên kết đến các blog có liên quan thì không được cho là đường dẫn chính và vì vậy nên không được đặt trong phần tử `<nav>`.

#### 2.3 ARTICLES:

`<article>`: Phần tử `<article>` đóng vai trò như 1 hộp chứa bất kì phần nào của trang và nó có thể đứng 1 mình có khả năng cung cấp thông tin. Nó có thể là 1 bài viết cá nhân hay blog, 1 bình luận, diễn đàn hay 1 nội dung độc lập. Nếu 1 trang có chứa 1 vài bài viết thì mỗi bài viết cá nhân sẽ được đặt trong phân tử `<article>`. Phần tử `<article>` có thể được lồng vào bên trong các phần tử khác.

#### 2.4 ASIDES:

`<aside>`: Phần tử `<aside>` gồm 2 mục đích tùy vào nó có được đặt vào trong phần tử `<article>` hay không. Khi phần tử `<aside>` được sử dụng bên trong 1 phần tử `<article>`, nó phải chứa thông tin liên quan đến các bài viết nhưng không cần làm rõ hết nghĩa. Khi phần tử `<aside>` được sử dụng bên ngoài phần tử `<article>` nó được coi như chứa nội dung liên quan đến toàn bộ trang. Ví dụ: có thể chứa các phần của trang web, danh sách các bài viết gần đây, hộp tìm kiếm... 

#### 2.5 SECTIONS:

`<section>`: phần tử `<section>` nhóm các nội dung liên quan với nhau và thường thì mỗi phần sẽ có heading riêng. Ví dụ trong 1 trang chủ có thể có 1 số phần tử `<section>` để chứa các phần khác nhau của 1 trang chẳng hạn như tin tức mới nhất, các sản phẩm hàng đầu, bản tin...

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter17_LAYOUT/3.png"/></p>

- Bởi vì phần tử `<section>` nhóm các mục có liên quan lại với nhau, nó có thể chứa 1 số phần tử `<article>` riêng biệt có chung 1 chủ đề hoặc 1 mục đích. Bên cạnh đó nếu có 1 trang với bài viết dài thì phần tử `<section>` có thể được sử đụng để chia bài viết ra thành các phần riêng biệt. Phần tử `<section>` không nên được sử dụng như bao bọc cho toàn bộ trang web (trừ khi trang chỉ chứa 1 nội dung riêng biệt). Nếu muốn có 1 phần tử chứa toàn bộ trang thì vẫn nên sử dụng phần tử `<div>`.

#### 2.6 HEADING GROUPS:

`<hgroup>`: Mục đích của phần tử `<hgroup>` là tạo nhóm các phần tử lại với nhau, thiết lập 1 hay nhiều phần tử từ `<h1>` đến `<h6>`, chúng được coi như 1 tiêu đề duy nhất. Ví dụ: phần tử `<hgroup>` chứa cả 2 tiêu đề bên trong phần tử `<h2>` và tiêu đề phụ với phần tử `<h3>`. 

#### 2.7 FIGURES:

`<figure> <figcaption>`: được sử dụng để chứa bất kì nội dung được tham chiếu từ flow chính của 1 bài viết (không chỉ từ hình ảnh)

```javascript
<figure>
<img src="images/bok-choi.jpg" alt="Bok Choi" />
<figcaption>Bok Choi</figcaption>
</figure>
```

- Quan trọng là các bài viết vẫn phải giữ ý nghĩa của nó nếu nội dung của phần tử `<figure>` bị thay đổi (khác 1 phần hoặc thậm chí là toàn bộ trang). Vì vậy chỉ nên sử dụng khi các nội dung đơn giản tham chiếu tới các phần tử. Bao gồm sử dụng cho: image, videos, graphs, diagrams, code sample, văn bản cung cấp body chính cho bài viết.

- Phần tử `<figure>` nên chứa 1 phần tử `<figcaption>` cung cấp 1 văn bản mô tả về nội dung của phần tử `<figure>`. 

#### 2.8 SECTIONING ELEMENTS:

`<div>`: Phần tử `<div>` vẫn rất quan trọng trong việc nhóm các phần tử có cùng quan hệ vào 1 nhóm, không nên sử dụng có phần tử mới bởi chúng không được cung cấp các quy định rõ ràng.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter17_LAYOUT/4.png"/></p>

#### 2.9LINKING AROUND BLOCK-LEVEL ELEMENTS:

HTML5 cho phép tác giả trang web đặt 1 phần tử xung quanh phần tử block level chứa phần tử con, việc này cho phép chuyển toàn bộ từ block thành link

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter17_LAYOUT/5.png"/></p>

<a name="3"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

