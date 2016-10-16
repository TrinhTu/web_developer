###Bài 5: Các thẻ định dạng chữ viết và văn bản

> Tài liệu: Các thẻ định dạng chữ viết và văn bản
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **15/10/2016**

####Mục lục

[1. Tiêu đề và đoạn văn bản](#01)

[2. Các thẻ định dạng chữ viết](#02)

[3. Thẻ trích dẫn](#03)

[4. Thẻ định dạng sẵn](#04)

[5. Thuộc tính Style để định dạng chữ viết](#05)

###Nội dung

<a name="01"></a>
####1. Tiêu đề và đoạn văn bản:

Tiêu đề (headline) và đoạn văn bản (paragraph) là thành phần cần phải phân biệt. Trong HTML thẻ tiêu đề được định nghĩa bằng cặp thẻ `<hn>` trong đó n chạy từ 1->6, tương ứng với từng cấp độ số càng nhỏ thì cấp độ sẽ càng lớn

![anh](http://imageshack.com/a/img922/3073/Si1FcQ.png)

Còn đoạn văn bản thì nó sẽ được khai báo bằng cặp thẻ `<p>` `</p>` các văn bản nằm trong cặp thẻ này được hiểu là 1 đoạn văn bản, giữa mỗi đoạn văn bản sẽ xuống dòng và cách nhau với 1 tỷ lệ nhất định, ví dụ như sau:

![anh](http://imageshack.com/a/img922/2675/dcgHrh.png)

<a name="02"></a>
####2. Các thẻ định dạng chữ viết:

Cũng tương tự như Markdown, với HTML cũng có chức năng để định dạng văn bản như là **in đậm**, *in nghiêng*, ~~gạch ngang~~, ... Sau đây là các thẻ HTML để thực hiện các chức năng trên.

- in đậm chữ viết: `<strong>`

- in nghiêng chữ viết: `<i>`

- gạch chân chữ viết: `<u>`

- gạch ngang chữ viết: `<strike>`

- nhấn mạnh câu: `<em>`

- định dạng 1 đoạn mã nào đó: `<code>`

- thước kẻ ngang trên tài liệu: `<hr>`

- tô sáng chữ viết: `<mark>`

![anh](http://imageshack.com/a/img922/7306/UZkBKF.png)

<a name="03"></a>
####3. Thẻ trích dẫn:

Thẻ trích dẫn (Quote) là một thẻ dùng thường xuyên để viết báo hay phóng sự, mục đích của nó là trích dẫn lại câu nói như một câu dẫn hoặc có thể định dạng thêm tên người dẫn chuyên nghiệp hơn. Thẻ trích dẫn được quy định là `<quote>` thẻ trích dẫn tên tác giả là `<cite>`

![anh](http://imageshack.com/a/img924/3927/XXX1oE.png)

Và đây là kết quả sau khi mở bằng trình duyệt

![anh](http://i.imgur.com/8CJSKah.png)

Trên đây là những câu lệnh khá là đơn giản và dễ nhớ không hề phức tạp gì mấy nên có thể dễ dàng thực hiện được.

<a name="04"></a>
####4. Thẻ định dạng sẵn:

Trong HTML có 1 thẻ gọi là thẻ định dạng sẵn (preformatted) được viết là `<pre>`  `</pre>`  nó được gọi là thẻ định dạng bởi vì mặc định trình duyệt đã tự động định dạng cho các nội dung nằm bên trong thẻ đó như kích thước chữ, khoảng cách, màu chữ....

Thẻ này được dùng để đăng 1 câu đối thoại hay 1 đoạn mã để phân biệt với các văn bản thông thường, thẻ này có thể tự định dạng sẵn theo ý mình muốn mà không cần sự can thiệp của HTML. 

![anh](http://imageshack.com/a/img922/167/usO4Cw.png)

Save lại và mở bằng trình duyệt sẽ được kết quả như sau:

![anh](http://imageshack.com/a/img923/5382/h4Dlj8.png)
 
<a name="05"></a>
####5. Thuộc tính Style để định dạng chữ viết:

 Mặc dù việc đảm nhận màu sắc trong website do CSS đảm nhận nhưng đối với 1 văn bản HTML thông thường bạn vẫn có thể thêm màu sắc bằng thuộc tính `<style>` . Thuộc tính `<style>` có thể đặt trong bất cứ thẻ nào

Cấu trúc của thẻ:  `<tên thẻ style="tên thuộc tính:giá trị">`

Mỗi thuộc tính bên trong `<style>` cách nhau bằng dấu chấm phẩy, các thuộc tính thường sử dụng nằm bên trong thuộc tính `<style>` là:

- `<color>`: đây là thuộc tính màu sắc để làm cho văn bản có màu chữ theo ý muốn, có thể sử dụng tên màu bằng tiếng anh hoặc sử dụng bảng mã màu trong CSS. Nếu muốn có nhiều sự lựa chọn màu sắc thì có thể truy cập vào [đây](http://www.w3schools.com/colors/colors_picker.asp)

- `<background-color>` : đây là thuộc tính màu nền trong văn bản, cũng sử dụng như thuộc tính `<color>`

- `<font-size>` : thuộc tính kích thước chữ, đơn vị khai báo của nó là **px**

- `<font-family>`: là thuộc tính font chữ, font thì có 2 loại font là font có chân và font không chân, và thường sử dụng font có chân là `Time new roman`

- `<text-align>` : thuộc tính căn lề văn bản, trong này bao gồm các giá trị là left ( căn lề từ bên trái), center ( căn lề ở giữa) ,right ( căn lề từ bên phải) , justify ( căn đều 2 bên)

-  Ngoài ra còn có thể định dạng chữ hay câu trong 1 đoạn văn bản dài mà không cần phải thêm thẻ `<p>` để xuống hàng nhằm nhấn mạnh và nổi bậc câu chữ đó có thẻ dùng thẻ `<span>` và bên trong thẻ `<span>` cũng có các thuộc tính **color**, **font-size**....

![anh](http://imageshack.com/a/img924/1640/buVBnz.png)

Sau khi tải lên trình duyệt :

![anh](http://imageshack.com/a/img922/1556/GXMWQS.png)
