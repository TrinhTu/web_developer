## Viết tài liệu với Markdown

>Tài liệu: Viết tài liệu với Markdown

>Thực hiện: Lê Tú Trinh

>Cập nhập lần cuối: 24/09/2016


###Mục lục

 [1. Tìm hiểu về Markdown](#Markdown)

[2. Markdown dùng làm gì](#congdung)

[3. Các cú pháp thường gặp](#cuphap)

[4. Công cụ viết Markdown](#congcu)


##Nội dung


<a name="Markdown"></a>
### 1. Tìm hiểu về Markdown

 1. Markdown là gì: 
 
	 

	>Markdown là ngôn ngữ đánh dấu siêu văn bản được tạo ra bởi John Gruber sử dụng cú pháp khá đơn giản và dễ hiểu để đánh dấu văn bản và văn bản được viết bằng Markdown có thể chuyển đổi sang HTML và ngược lại.

 2. Tại sao cần dùng Markdown:
 
	 

> Cũng giống như Markdown, HTML cũng dùng để đánh dấu siêu văn bản nhưng cú pháp của nó thì khá phức tạp và khó nhớ, Markdown giúp ta giải quyết được vấn đề này, cú pháp của Markdown thì ngắn gọn dễ hiểu hơn nhưng nội dung thì vẫn không có gì thay đổi.


*ví dụ*: đoạn văn bản trog html gồm 1 tiêu đề và 3 đoạn văn thì cú pháp sẽ là:

`<h1>Tiêu Đề</h1>
<p>Đoạn văn thứ nhất</p>
<p>Đoạn văn thứ 2</p>
<p>Đoạn văn thứ 3</p>`


**Còn với Markdown thì cú pháp sẽ đơn giản hơn nhiều:**

`## Tiêu Đề
Đoạn văn thứ 1
Đoạn văn thứ 2
Đoạn văn thứ 3`

<a name="congdung"></a>
### 2. Markdown dùng để làm gì: 

>John Gruber đã tạo ra ngôn ngữ Markdown với mục tiêu tạo ra một định dạng văn bản thô "dễ viết, dễ đọc, dễ dàng chuyển thành XHTML (hoặc HTML). Nói tóm lại Markdown là ngôn ngữ dùng để viết tài liệu và đánh dấu siêu văn bản.

<a name="cuphap"></a>
### 3. Các cú pháp thường gặp:

	

 - Thẻ tiêu đề: Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu để, có thể dùng từ 1 đến 6 kí tự # liên tiếp mức độ giảm dần từ 1 đến 6

**ví dụ**:	

###tiêu đề 1

####tiêu đề 2

#####tiêu đề 3

 - Chèn link và chèn ảnh: chèn link và chèn ảnh trong Markdown khá đơn giản, không phức tạp như trong HTML. Cú pháp chèn hình ảnh như sau:

		![tên ảnh](htpp://.......)

**ví dụ**:	 		đây là con mèo


![doremon](http://khohinhnen.com/wp-content/uploads/2015/01/hinh-anh-doremon-17.jpg)

**Cú pháp để chèn link như sau: ** 

		[tên](http://.......)


*ví dụ* : có thể copy và past trực tiếp link vào :

(https://github.com/)

Cũng có thể làm cho nó ngắn gọn hơn:

[github](https://github.com/)

 - Để in đậm 1 câu hay 1 đoạn ngắn có cú pháp như sau:

`**từ cần in đậm**`  sẽ được kết quả như sau **từ cần in đậm**

 - Để in nghiêng thì như sau:

`*từ cần in nghiêng*`  sẽ thu được kết quả *từ cần in nghiêng*


 - Để bo 1 đoạn văn cú pháp như sau:

`'đoạn cần bo'`    sẽ được kết quả như sau    `đoạn cần bo`

 - Để tạo bảng thực hiện như sau

`| ten | dia chi | sd |   |   |
|-----|---------|----|---|---|
| 1   |         |    |   |   |
| 2   |         |    |   |   |
| 3   |         |    |   |   |`

| ten 	| dia chi 	| sd 	|   	|   	|
|-----	|---------	|----	|---	|---	|
| 1   	|         	|    	|   	|   	|
| 2   	|         	|    	|   	|   	|
| 3   	|         	|    	|   	|   	|

<a name="congcu"></a>
###4. Công cụ viết Markdown:

Có thể dùng `notepad` `notepad++` `vi` ` ngoài ra còn có rất nhiều phần mềm khác hỗ trợ viết Markdown như [stackedit](https://stackedit.io/editor) hay [markdownlivepreview](http://markdownlivepreview.com/)  ....

###Các lỗi xảy ra

###Kết luận:

 - Ưu điểm: nó cho phép bạn soạn thảo và trình bày nhanh hơn phương pháp truyền thống ngoài ra còn có thể kết hợp sử dụng HTML với Markdown trong bài viết nếu có nhu cầu sử dụng màu chữ, khi viết tài liệu bằng markdown thì khồn cần sử dụng quá nhiều công cụ phức tạp

 -Nhược điểm: mới xài nên chưa tìm ra


###tham khảo: có thể tham khảo thêm 1 số tài liệu ở đây:

[tai_lieu1](https://github.com/hocchudong/git-github-for-sysadmin)

[tai_lieu2](https://help.ghost.org/hc/en-us/articles/224410728-Markdown-Guide)

Ngoài ra còn có thể đọc thêm tài liệu ở 1 số trang như [hoc_lap_trinh](http://www.hoclaptrinh.org/bai-viet/Markdown-La-Gi) [markdown](https://vi.wikipedia.org/wiki/Markdown)....

##hết.
