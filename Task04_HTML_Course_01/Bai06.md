### Bài 6: Tạo danh sách (List)

> Tài liệu: Tạo danh sách (List)
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **15/10/2016**

#### Mục lục

[1. Ordered List](#01)

[2. Unordered List](#02)

[3. Description List](#03)

[4. Xếp chồng danh sách](#04)

### Nội dung


Phần tử danh sách (list) được sử dụng rất thường xuyên trong tài liệu web bằng HTML, trong 1 trang web thường người ta sử dụng phần tử danh sách rất nhiều chẳng hạn như menu, danh sách những thông tin nào đó... đều được tạo ra bởi các thẻ tạo danh sách trong HTML. Trong HTML có 3 kiểu danh sách đó là: kiểu sắp xếp (ordered) , không sắp xếp (unordered) và kiểu danh sách mô tả (description) ,cụ thể như sau:

<a name="01"></a>
#### 1. Ordered List:

Để khai báo danh sách với kiểu được sắp xếp sẽ bắt đầu bằng cặp thẻ `<ol>` `</ol>` bên trong cặp thẻ này là danh sách những mục con, mỗi mục sẽ đặt trong cặp thẻ 	`<li>` `</li>` tương tự như trong Markdown. Thẻ `<ol>` này còn hỗ trợ thêm thuộc tính nữa là `type` để thiết lập kiểu sắp xếp mục con bên trong danh sách. Giá trị của `type` là : 1, i, I, a, A.

Cú pháp như sau:

```
<ol type="I">
<li>mục 1</li>
<li>mục 2</li>
<li>mục 3</li>
</ol>
```
![anh](http://imageshack.com/a/img924/1572/lyZdnZ.png)

<a name="02"></a>
#### 2. Unordered List:

Cũng giống như danh sách sắp xếp, danh sách không sắp xếp sẽ bắt đầu bằng cặp thẻ `<ul>` `</ul>` và bên trong mỗi mục con là cặp thẻ `<li>` `</li>`, chúng ta cũng có thể thêm các thuộc tính `type` vào thẻ `<ul>` với các thuộc tính của CSS như:   `list-style-type` và các giá trị `disc` `square`, `circle` và `none`

![anh](http://imageshack.com/a/img923/8591/FNx5zz.png)

Kết quả:

![anh](http://imageshack.com/a/img921/8352/ucF3FG.png)

<a name="03"></a>
#### 3. Description List:

Nó sẽ bắt đầu danh sách bằng cặp thẻ `<dl>` `</dl>` , mỗi mục con sẽ được khai báo bằng cặp thẻ `<dt>` `</dt>` , mô tả của mỗi mục con khai báo bằng cặp thẻ `<dd>` `</dd>` ,ví dụ như sau:

![anh](http://imageshack.com/a/img922/6038/wpTx3y.png)

Sau khi thực hiện xong thì trình duyệt sẽ đọc được như sau:

![anh](http://imageshack.com/a/img922/465/tAsd7M.png)

<a name="04"></a>
#### 4. Xếp chồng danh sách:

Trong HTML có thể xếp chồng danh sách bằng cách lồng thêm cặp thẻ `<li>` `</li>` vào mục con mà bạn muốn thêm tầng cho nó.

![anh](http://imageshack.com/a/img922/553/m8HANE.png)

![anh](http://imageshack.com/a/img923/7704/bAbjev.png)
