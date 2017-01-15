## HTML & CSS

### Lists

> Chương 3: Lists
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/01/2017

## Mục lục:

[1. Ordered Lists](#1)

[2. Unordered Lists](#2)

[3. Definition Lists](#3)

[4. Nested Lists](#4)

***

Có nhiều lúc ta cần phải sử dụng danh sách. HTML cung cấp cho ta 3 kiểu danh sách khác nhau

- Ordered lists (Danh sách có sắp xếp): Là danh sách mà mỗi mục trong danh sách đều được đánh số. Ví dụ: trong danh sách có thể là 1 tập hợp các công thức cần được sắp xếp theo thứ tự hoặc các mục điều khoản trong hợp đồng...

- Unordered lists (danh sách không có thứ tự): là danh sách bắt đầu với 1 kí tự điểm chứ không phải là kí tự cho biết thứ tự.

- Definition lists (danh sách định nghĩa): là danh sách được tạo thành từ 1 tập hợp các điều kiện cùng các định nghĩa.

<a name="1"></a>
### 1. Ordered lists (danh sách sắp xếp):

- Danh sách sắp xếp được tạo thành bắt đầu từ cặp thẻ `<ol>` 

- Mỗi mục trong danh sách thì nằm trong cặp thẻ `<li>` `</li>`. Mỗi mục đó sẽ được trình duyệt mặc định là thụt vào trong.

- Trong 1 số trường hợp ta thấy sử dụng các kiểu đánh số như là: số, chữ cái, số la mã... điều này hoàn toàn có thể thực hiện được khi áp dụng CSS stylelist.

<a name="2"></a>
### 2. Unordered lists (danh sách không sắp xếp):

- Danh sách không sắp xếp luôn được bắt đầu từ thẻ `<ul>`

- Tương tự như danh sách sắp xếp, mỗi mục trong danh sách không sắp xếp nằm trong cặp thẻ `<li>` `</li>`. Và các mục đó cũng được mặc định hiển thị thụt vào bên trong.

- Và 1 số trường hợp ta sẽ gặp các kiểu hiển thị đánh dấu chỉ mục với các biểu tượng như hình tròn, hình vuông, hình thoi,... điều này cũng được thể hiện rõ ràng hơn trong CSS.

<a name="3"></a>
### 3. Definition Lists (danh sách định nghĩa):

- Danh sách định nghĩa được tạo thành với thẻ `<dl>` thường bao gồm 1 loạt thuật ngữ và định nghĩa. Bên trong thẻ `<dl>` là cặp thẻ `<dt>` `<dd>`.
 
- Thẻ `<dt>` dùng để chứa nội dung của thuật ngữ được định nghĩa

- Thẻ `<dd>` sử dụng để chứa các định nghĩa

<a name="4"></a>
### 4. Nested Lists (danh sách lồng nhau):

- Chúng ta có thể đặt danh sách thứ 2 bên trong cặp thẻ `<li>` để tạo thành 1 danh sách con hoặc danh sách lồng nhau.

- Trình duyệt sẽ hiển thị danh sách được lồng vào thụt vô hơn so với danh sách cha

#### Tóm lại:

- Có 3 kiểu danh sách trong HTML: danh sách sắp xếp, danh sách không sắp xếp và danh sách định nghĩa.

- Danh sách sắp xếp thì sử dụng số

- Danh sách không sách xếp thì sử dụng kí tự chấm tròn (bullet)

- Danh sách định nghĩa được sử dụng để xác định thuật ngữ

- Danh sách có chức năng tạo các danh sách lồng vào bên trong nhau

