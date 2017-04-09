## Bài 10: Các thuộc tính tùy chỉnh kích thước

> Tài liệu: Các thuộc tính tùy chỉnh kích thước
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 29/10/2016

### Mục lục:

### Nội dung:

Khi làm việc với Box Model nói riêng và CSS layout nói chung thì ngoài việc chỉnh hiển thị cho các phần tử còn phải thiết lập kích thước cho các phần tử.  Hiện tại trong CSS có 6 thuộc tính để tùy biến chỉnh chiều rộng và chiều cao cụ thể như sau:


| Tên thuộc tính 	 	| Mô tả  		| 	Kiểu giá trị   	|
|---	|---	|---	|
| Height  	|  Thiết lập chiều cao của phần tử 	| auto , length, % 	|
| Max-height  	|Thiết lập chiều cao tối đa của 1 phần tử   	| none, length, %, inherit  	|
| Max-width  	| Thiết lập chiều rộng tối đa của 1 phần tử  	|  none, length, %, inherit 	|
|Min-height   	|  Thiết lập chiều rộng tối thiểu của 1 phần tử 	| length, %, inherit  	|
| Min-width  	|  Thiết lập chiều cao tối thiểu của 1 phần tử 	|   length, %, inherit	|
|  Width 	|  Thiết lập chiều rộng của phần tử 	| none, length, %, inherit  	|

- Ở cột giá trị `length` nghĩa là giá trị kèm theo đơn vị như là: `rem`, `em`, `px`, `pt`, giá trị `%`, `none` là bỏ thiết lập, `auto` là tự động thiết lập dựa theo chiều còn lại, `inherit` là thừa kế thuộc tính đã thiết lập trước đó cho thuộc tính này.

**Chúng ta chỉ được phép thiết lập kích thước với các phần tử Block, table, video hình ảnh... chứ không thể thiết lập cho các phần tử Inline**

- Đối với các thuộc tính `min-*` `max-*` nghĩa là nói sẽ căn độ dài của phần tử dựa vào nội dung bên trong nhưng sẽ có kích thước tối thiểu/ tối đa được sử dụng.  Ví dụ bạn có phần `#content`, bên trong `#content` bạn có phần `#post` và thiết lập chiều rộng cho `#post` là 500px. Thì nếu bạn đặt thuộc tính `max-width` cho `#content` là 400px thì `#post`  cũng chỉ giãn được tối đa là 400px chứ không thể hơn.
