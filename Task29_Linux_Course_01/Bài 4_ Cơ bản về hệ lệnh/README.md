## Bài 04: CƠ BẢN VỀ HỆ LỆNH

> Tài liệu: Cơ bản về hệ lệnh
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 17/03/2017

### Mục lục:

[1. Shell lệnh](#1)

[2. Cấu trúc lệnh và cú pháp](#2)

[3. Các trang trợ giúp Help và MAN](#3)

[4. Các lệnh làm việc với thư mục](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Shell lệnh:

- Shell lệnh cung cấp cho người dùng các lệnh có thể tương tác với Kernel

- Môi trường mà các lệnh được nhập vào và thực thi

- Ngôn ngữ lệnh cho phép lập trình tạo các trình tiện ích nhỏ

- Điều khiển môi trường làm việc

- Thay đổi các biến và tên file dùng trong hệ thống

- Định hướng xuất nhập vào ra

- Shell còn được gọi là Command Line Interface (CLI)

- Các loại Shell

	+ C Shell (CSH)

	+ Korn Shell (KSH)

	+ Bourne Shell

- Các loại shell khác nhau có 1 số tính năng chung và 1 số tính năng riêng

- **C Shell**

	+ Có cú pháp tương tự ngôn ngữ C

	+ Ví dụ:

```javascript
if ( ! -e mylife ) echo mytext > mylife
	if ( ! -e mylife ) then
		echo mytext > mylife
	endif
```

- **Korn Shell**

	+ Tương thích với Bourne Shell 

	+ Có nhiều thuộc tính tương tự như C Shell. Ví dụ: Command history

	+ Được sử dụng như 1 ngôn ngữ lập trình để tạo ra các tiện ích nhỏ

- **Bourne Again Shell (BASH)**

	+ Được sử dụng phổ biến nhất trong các bản phân phối

	+ Được phát triển từ Bourne shell

	+ Có nhiều tính năng mới

		+ Điều khiển các tiến trình

		+ Các lệnh history

		+ Tên file dài

		+...

- Dấu nhắc trong Shell thường là $ thì là user thông thường, còn # là user root.

- Một số câu lệnh:

	+ Kiểm tra đang làm việc với shell nào sử dụng câu lệnh: `echo $SHELL`

	+ Tất cả các shell được đặt trong thư mục `bin`: `ls /bin | more`

	+ Có thể chuyển từ shell này sang shell khác bằng cách thay đổi tên, về cấu trúc các lệnh cơ bản vẫn như cũ.

![4]()

<a name="2"></a>
### 2. Cấu trúc lệnh và cú pháp:

- Lệnh để thực hiện gọi 1 chương trình, ứng dụng, script hoặc các tiện ích

- Lệnh được nhập tại dấu nhắc shell

- Cú pháp cho 1 lệnh trong linux

	+ command [options][expression][filenames] Trong đó:

		+ `command`: tên của lệnh hoặc tiện ích sẽ được sử dụng

		+ `option`: các tùy chọn đi kèm với lệnh hoặc tiện ích, ảnh hưởng đến quá trình thực thi của lệnh

		+ `expresstion`: một số lệnh hoặc tiện ích đòi hỏi có các biểu thức điều kiện để thực thi


		+ `file`: 1 số lệnh hoặc tiện ích yêu cầu 1 hoặc nhiều đối tượng cần có để áp dụng tính năng được thực thi

- Chính tả và cú pháp là rất quan trọng

- Linux là hệ thống phân biệt các trường hợp (case sentive)

- Các lệnh có rất nhiều tùy chọn khác nhau được gọi là switch

- Các switch được phân cách với nhau trong các câu lệnh bởi dấu (-).

- Các switch có thể được xâu chuỗi lại. 

![1](https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%204_%20C%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20h%E1%BB%87%20l%E1%BB%87nh/image/1.png)

![2](https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%204_%20C%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20h%E1%BB%87%20l%E1%BB%87nh/image/2.png)

<a name="3"></a>
### 3. Các trang trợ giúp Help và MAN

<a name="4"></a>
### 4. Các lệnh làm việc với thư mục:

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Cơ bản về hệ lệnh (4.1).FLV 
>
> [2] Cơ bản về hệ lệnh (4.2).FLV
>
> [3] Cơ bản về hệ lệnh (4.3).FLV