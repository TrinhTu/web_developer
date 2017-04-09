##Bài 4: Các đơn vị đo lường cơ bản

> Tài liệu: Các đơn vị đo lường cơ bản
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 25/10/2016

### Mục lục

[1. Absolute Units( đơn vị tuyệt đối)](#1)

[2. Relative Units ( đơn vị tương đối)](#2)

###Nội dung

Các đơn vị dùng để đô chiều dài và chiều rộng trong CSS gọi chung là đơn vị đo lường

Có 2 loại đơn  vị đo lường chính đó là:

- Đơn vị tuyệt đối ( Absolute Units): là đơn vị đã được định nghĩa sẵn trong máy tính.

- Đơn vị tương đối (Relative Units) : Đơn vị sẽ bị biến đổi bởi thành phần khác hoặc thành phần mẹ.

<a name="1"></a>
#### 1. Absolute Units:

Là đơn vị vật lí đã được định nghĩa sẵn và đại diện cho các đơn vị đo lường vật lý, các đơn vị này không bị phụ thuộc và không hề bị thay đổi bởi các tác động nào. Ví dụ như là: mét, xen ti mét, px... là đơn vị tuyệt đối..

Các loại đơn vị tuyệt đối thường được sử dụng nhất:

- px: là đơn vị được sử dụng trong máy tính và trong màn hình hiển thị, 1 px sẽ tương ứng với 1 điểm ảnh trên màn hình hiển thị

- pt: đơn vị point, 1 ich= 72 pt.

Ví dụ về đại lượng **px**

![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_04/image/1.png)

Ví dụ về đại lượng **pt** cũng tương tự:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_04/image/2.png)
<a name="2"></a>
#### 2. Relative Units:

Là đơn vị đo lường được sử dụng trong CSS ở mức tương đối, nó có thể bị thay đổi bởi các thành phần khác, như kích thước màn hình.

Các đơn vị đo tương đối thường dùng: 

- % : nó sẽ biến đổi theo đơn vị của phần tử mẹ của nó. Ví dụ như tạo 1 cái khung có chiều rộng là 500px và tạo thêm 1 khung bên trong khung đó có kích thước bằng 50% thì nó sẽ tự biến đổi thành 250px, và khi ta thay đổi chiều rộng của khung mẹ tức là khung bên ngoài thì khung bên trong cũng sẽ thay đổi theo. Ví dụ:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_04/image/3.png)

- em : là đơn vị tham chiếu thuộc tính font-size của các phần tử mẹ. Ví du có 1 khung có font-size là 16px thì trong khung đó, 1 đơn vị **em** là 16px. Ví dụ:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_04/image/4.png)

- rem : là đơn vị tham chiếu với thuộc tính font-size của phần tử lớn nhất trong Website (HTML). Nếu như đặt font-size là 16px thì **1rem=16px** . Có thể nói là **rem** thì giống y hệt như **em** chỉ có đều là **rem** phụ thuộc vào font-size của phần tử HTML. Ví dụ:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_04/image/5.png)




