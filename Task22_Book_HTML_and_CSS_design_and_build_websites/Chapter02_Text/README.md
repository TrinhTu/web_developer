## HTML & CSS

### Text

> Chương 2: Text
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 13/1/2017

## Mục lục:

[1. Headings and paragraphs](#1)

[2. Bold, italic, emphasis](#2)

[3. Structural and semantic markup](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Headings and paragraphs:

Khi tạo 1 trang Web, chúng ta thêm các thẻ, đánh dấu nội dung của từng trang. Các thẻ này cung cấp ý nghĩa cho phép trình duyệt hiển thị cho người dùng cấu trúc phù hợp của trang.

Trong chương này chú trọng tới việc đánh dấu văn bản và cách hiển thị của nó trong trang web của bạn. Chúng ta sẽ tìm hiểu về:

- Cấu trúc đánh dấu: Yếu tố sử dụng để mô tả cả tiêu đề và đoạn văn bản.

- Ý nghĩa của việc đánh dấu: Cung cấp thêm thông tin, cũng như nhấn mạnh vị trí dùng để sử dụng sao cho hợp lí, và ý nghĩa của các từ được viết tắt.

Trước tiên là phần tiêu đề: Phần tiêu đề sử dụng các thẻ từ h1 -> h6 theo cấp độ hiển thị giảm dần

- `<h1>`: Sử dụng như tiêu đề chính

- `<h2>`: Sử dụng như tiêu đề con

...

- `<h6>`: Hiển thị nhỏ nhất

Chúng ta có thể tùy chỉnh kích thước của đoạn text, chỉnh màu sắc, kích cỡ chữ...khi áp dụng CSS.

**Đoạn văn**: 

```javascript
<p>Đây là đoạn văn bản thứ nhất</p>
<p>Đây là đoạn văn bản thứ hai</p>
```

Các đoạn văn bản này được bao bọc bởi thẻ mở và thẻ đóng `<p>`, `</p>`. 


<a name="2"></a>
### 2. Bold, italic, emphasis:

#### In đậm và in nghiêng:

- Bằng cách sử dụng cặp thẻ `<b>` `</b>` ta có thể làm cho nội dung đó được in đậm và nổi bậc hơn, thẻ `<b>` là yếu tố đại diện cho văn bản, trình bày 1 cách rõ ràng, có nhấn mạnh ý nghĩa nội dung của văn bản.

- Bằng các sử dụng cặp thẻ `<i>` </i>` thì cách hiển thị của nội dung bên trong sẽ được hiển thị nghiêng, thường được sử dụng cho tên, từ khóa riêng...

#### Superscript & Subscript:

- Sử dụng các thẻ `<sup>` như là để hiển thị ngày tháng hoặc các biểu thức toán học.

- Còn thẻ `<sub>` được sử dụng để chứa các kí tự mà nên được subscript. Được sử dụng phổ biến với các ghi chú gạch chân và cách ghi các công thức hóa học.

#### White space

Để làm cho đọc mã dễ đọc hơn thì người viết thường thêm các dấu cách (khoảng trắng) trên các dòng. Khi trình duyệt đọc qua 2 hoặc nhiều dấu cách xuất hiện liền kề nhau thì nó chỉ hiển thị 1 dấu cách. Tương tự như vậy, trong cùng 1 đoạn văn bản được bao bọc trong 1 cặp thẻ, thì việc sử dụng nhiều dấu cách không có tác dụng, và trình duyệt vẫn hiểu đó là cách 1 khoảng trắng.

#### Ngắt dòng và quy tắt ngang (Line Breaks & Horizontal Rules):

- Nếu muốn ngắt 1 dòng ở giữa đoạn văn có thể sử dụng cặp thẻ `<br>` `</br>`

-  Để tạo ra khoảng trống giữa chủ đề và nội dung ta có thể sử dụng thẻ `<hr/>`. Thẻ này không có thẻ mở và thẻ đóng được sử dụng duy nhất, nó có tác dụng tạo ra 1 đường kẻ ngăn cách nội dung và chủ đề.

#### Trình soạn thảo và xem mã nguồn  (Visual editors & their code views)

- Hệ thống quản lí và biên tập HTML như Dreamweaver thường có 2 cái nhìn khi tạo ra 1 trang web: Là 1 trình soạn thảo và xem mã nguồn

- Trình soạn thảo hoạt động giống như bộ vi xử lí. Mặc dù mỗi trình soạn thảo có 1 cách thức hoạt động khác nhau nhưng đều có đặc tính phổ biến là cho phép bạn kiểm soát việc trình bày 1 văn bản.

- Nếu sao chép và dán 1 đoạn văn bản vào trong chương trình, nó cho phép định dạng văn bản (như Word) vào 1 trình soạn thảo và thêm nội dung vào

- Xem mã nguồn (Code views): khi xem mã nguồn bởi trình soạn thảo, ta có thể tự thêm, chỉnh sửa nội dung, nó thường hoạt động sử dụng 1 cái hộp với các biểu tượng.

<a name="3"></a>
### 3. Đánh dấu ngữ nghĩa (Semantic Markup):

Có 1 số yếu tố văn bản không làm ảnh hưởng đến cấu trúc trang web của bạn nhưng khi nó có thêm chức năng thêm thông tin cho các trang - gọi là đánh dấu ngữ nghĩa.

Ở phần này chúng ta cần biết được ý nghĩa và cách sử dụng của các thẻ đánh dấu. Ví dụ như `<em>` cho biết hiển thị in nghiêng `<blockquote>` chỉ ra văn bản là 1 khối, hiển thị thụt vào, dùng để trích dẫn. Trình duyệt sẽ hiển thị nội dung của các yếu tố 1 cách khác nhau

#### Thẻ in đậm và in nghiêng (Strong & Emphasis):

- Sử dụng thẻ `<strong>` để chỉ ra rằng nội dung nằm bên trong thẻ đó rất quan trọng cần được nhấn mạnh lưu ý. Theo mặc định thì trình duyệt sẽ hiển thị nội dung bên trong thẻ này là in đậm.

- Thẻ `<em>` là yếu tố chỉ nhấn mạnh tinh tế không làm thay đổi ý nghĩa của câu. Theo mặc định thì trình duyệt sẽ hiển thị nội dung của thẻ `<em>` là chữ in nghiêng

#### Các từ viết tắt (Abbreviations & Acronyms): 

Ta có đoạn văn bản sau:

```javascript
<p><abbr title="Professor">Prof</abbr> Stephen Hawking is a theoretical physicist and cosmologist.</p>
<p><acronym title="National Aeronautics and Space Administration">NASA</acronym> do some crazy space stuff.</p>
```

Đoạn văn trên sử dụng 2 thẻ đó là `<abbr>` và `<acronym>` đều có mục đích là viết tắt 1 từ và mô tả ra đầy đủ hình thức viết tắt của từ đó khi được trỏ vào.

<p text-align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%202_Text/1.png"/></p>

#### Trích dẫn và định nghĩa (Citations & Definitions):

- Khi tham khảo sách hoặc báo cáo nghiên cứu thì thẻ `<cite>` được sử dụng để chỉ ra nơi trích dẫn là từ nào. Trình duyệt sẽ làm cho nội dung trong `<cite>` hiển thị in nghiêng.

- Tương tự như thẻ `<cite>` thì thẻ `<dfn>` cũng sử dụng để chỉ ra ví dụ của 1 số thuật ngữ mới. 1 số trình duyệt hiển thị nội dung của `<dfn>` dạng in nghiêng, còn 1 số như Chrome Safari thì không thay đổi sự xuất hiện của nó.

#### Chi tiết về tác giả (Author Details):

- `<address>`: đây là thẻ thường sử dụng để chứa thông tin nguồn gốn của trang, nó có thể là 1 địa chỉ vật lí, số điện thoại, địa chỉ email, và nội dung thường được hiển thị in nghiêng

#### Thay đổi nội dung (Changes to Content):

- Thẻ `<ins>` được sử dụng để hiển thị nội dung đã được chèn vào tài liệu được hiển thị dưới dạng gạch chân, còn `<del>` là phần tử có thể hiển thị văn bản đã bị xóa bởi nóthường được hiển thị bởi dấu gạch ngang qua nó.

- Thẻ `<s>` chỉ ra 1 vài điều chưa chính xác hoặc không liên quan nhưng không nên xóa, nội dung bên trong thường hiển thị với 1 đường thẳng gạch ngang.

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.
