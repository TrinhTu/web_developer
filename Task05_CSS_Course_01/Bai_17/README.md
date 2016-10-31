##Bài 17: Thuộc tính `position` và Absolute – Relative

> Tài liệu: Thuộc tính `position` và Absolute - Relative
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/10/2016

###Mục lục

[1. Các giá trị của thuộc tính position](#1)

[2. Ví dụ về kiểu relative](#2)

[3. Ví dụ về kiểu absolute](#3)

[4. Ví dụ về kiểu fixed](#4)

###Nội dung:

<a name="1"></a>
####1. Các giá trị của thuộc tính position:

- relative: không thay đổi cấu trúc thẻ image, dùng để thiết lập một phần tử sử dụng các thuộc tính

- position (xem ở dưới) mà không làm ảnh hưởng đến việc hiển thị ban đầu.

- absolute: dùng để hiển thị phần tử trong dạng tuyệt đối. Tức là phần tử đó chỉ hiển thị trong khung của phần tử mẹ và không thể chạy ra ngoài được.

- fixed: Hiển thị cố định.

- static: Đưa phần tử về hiển thị theo kiểu mặc định.

Position có 4 thuộc tính để tùy chỉnh vị trí và giá trị của nó là:

- `top`: căn vị trí hiển thị hướng từ trên xuống, giá trị càng cao thì phần tử càng thụt xuống dưới.

- `bottom`: căn vị trí hiển thị từ dưới lên

- `left`: căn vị trí hiển thị từ trái sang phải

- `right`: căn vị trí hiển thị từ phải sang trái.

Lưu ý: là khi chúng ta sử dụng left thì không được sử dụng right, khi sử dụng top thì không sử dụng bottom và ngược lại.

<a name="2"></a>
####2. Ví dụ về kiểu relative:

![i](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_17/image/i.png)

<a name="3"></a>
####3. Ví dụ về kiểu absolute:

![ii](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_17/image/ii.png)
<a name="4"></a>
####4. Ví dụ về kiểu fixed:

![iii](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_17/image/iii.png)

Ngoài ra còn có thêm thuộc tính là `z-index` để tùy chỉnh lớp hiển thị, phần tử nào có thuộc tính `z-index` lớn hơn thì sẽ hiển thị lên trên(nổi lên), còn phần tử có `z-index` nhỏ hơn thì sẽ bị chìm xuống dưới.

![iiii](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_17/image/iiii.png)
