##Bài 11: Tìm hiểu box-sizing

> Tài liệu: Tìm hiểu box-sizing
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 30/10/2016

###Mục lục:

[1. Lưu ý về cách viết](#1)

[2. Các giá trị của box-sizing](#2)

###Nội dung

Khi sử dụng Box Model thì có 2 thuộc tính là Padding và Border thì có đặc điểm là nó sẽ làm khung phần tử bị biến đổi kích thước, và nếu như thêm thuộc tính `width` và `height` để thiết lập kích thước cho nó.

Ví dụ như có box có width là 300px và height là 300px (300x300px) nhưng nếu đặt paading là 15px thì khung sẽ có kích thước là 330x330px bởi vì nếu cộng padding là 15px thì khung sẽ tự động cộng thêm là 30px ( cộng thêm 15px cho top và 15px cho bottom, với left right cũng tương tự), với `border` cũng tương tự padding. Ví dụ minh họa :

![7](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_11/image/7.png)

Tóm lại, nếu như muốn cho phần tử của mình giữ nguyên kích thước không bị thay đổi khi đặt thêm thuộc tính Padding hay Border như trên thì cần có thêm 1 thuộc tính nữa là box-sizing. Thuộc tính cày có tác dụng là khi mình thiết lập giá trị của width và height là đã bao gồm tính toán luôn cả thuộc tính padding và border, nên padding và border sẽ dựa vào đó mà tự tính toán sao cho phù hợp với thiết lập bên trong.


<a name="1"></a>
####1 . Lưu ý cách viết:

Khi viết phần tử trong HTML nên sử dụng toàn bộ là `border box`. Để chọn toàn bộ phần tử ta thực hiện như sau:

![9](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_11/image/9.png)

Trong đó dấu `*` nghĩa là chọn tất cả phần tử trong HTML.

`box-sizing` là 1 thuộc tính trong CSS3 nên khi viết phải viết thành 3 lần với các tiền tố khác nhau

```
box-sizing: border-box;
-moz-box-sizing: border-box;
-webkit-box-sizing: border-box;
```

`-mox-box-sizing`: là dành cho những trình duyệt phiên bản cũ có thể sử dụng được, còn `-wekit-box-sizing` là dành cho Google Chrome bản cũ.

Khi đã áp dụng `border-box` thì tỉ lệ bên trong khi đã thiết lập height và width đã tính toán sao cho phù hợp lại và bao gồm cả ``padding và border.

![10](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_11/image/10.png)

<a name="2"></a>
####2. Các giá trị của box-sizing:

Hiện tại box-sizing có hỗ trợ một số giá trị :

- `content-box`: Giá trị mặc định, là giá trị width và height chỉ áp dụng cho khu vực nội dung bên trong, không gồm padding, border và margin.

- `border-box`: Khi thiết lập giá trị này, thì width và height sẽ bao gồm cho cả phần nội dung, padding và border nhưng không bao gồm margin.

- `padding-box`: Với giá trị này thì width và height chỉ bao gồm cho phần nội dung và padding, không bao gồm border và margin.

**Chú ý**: `padding-box` chỉ có tác dụng với trình duyệt Firefox. Vậy nên chúng ta nên sử dụng `border-box` để thuận tiện cho việc tính toán trong website như ví dụ phía trên.

