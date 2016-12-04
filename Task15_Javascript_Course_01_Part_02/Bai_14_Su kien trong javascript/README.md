##Bài 14: SỰ KIỆN TRONG JAVASCRIPT

>Tài liệu: Sự kiện trong Javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 03/12/2016

###Mục lục:

[1. Sự kiện trong javascript là gì?](#1)

[2. Các sự kiện trong javascript](#2)

[3. Các ví dụ](#3)

###Nội dung:

<a name="1"></a>
####1. Sự kiện trong javascript là gì?

Sự kiện là 1 hành động nào đó tác động lên đối tượng HTML mà ta có thể bắt được sự kiện này và thực hiện hành động nào đó.

Mỗi sự kiện có thể thực hiện nhiều hành động. Bao nhiều hành động thì phụ thuộc vào từng chức năng cụ thể.

<a name="2"></a>
####2. Các sự kiện trong javascript:

- onclick: Xảy ra khi click vào thẻ HTML 

- ondbclick: Xảy ra khi double click vào thẻ HTML

- onchange: Xảy ra khi giá trị (value) của thẻ HTML đổi. Thường dùng trong các đối thẻ form input

- onmouseover: Xảy ra khi con trỏ chuột bắt đầu đi vào thẻ HTML

- onmouseout: Xảy ra khi con trỏ chuột bắt đầu rời khỏi thẻ HTML

- onmouseenter: Tương tự như onmouseover

- onmouseleave: Tương tự như onmouseout

- onmousemove: Xảy ra khi con chuột di chuyển bên trong thẻ HTML

- onkeydown: Xảy ra khi gõ một phím bất kì vào ô input

- onload: Sảy ra khi thẻ HTML bắt đầu chạy, nó giống như hàm khởi tạo trong lập trình hướng đối tượng vậy đó.

- onkeyup: Xảy ra khi bạn gõ phím nhưng lúc bạn nhã phím ra sẽ được kích hoạt

- onkeypress: Xảy ra khi bạn nhấn môt phím vào ô input

- onblur: Xảy ra khi con trỏ chuột rời khỏi ô input

- oncopy: Xảy ra khi bạn copy nội dung của thẻ

- oncut: Xảy ra khi bạn cắt nội dung của thẻ

- onpaste: Xảy ra khi bạn dán nội dung vào thẻ

<a name="3"></a>
####3. Các ví dụ:

Ví dụ 1: Viết chương trình gồm 1 ô input và 1 thẻ div dùng để hiển thị nội dung ( giá trị của ô input) khi người dùng gõ vào ô input.

```javascript
    <script language="javascript">
      // Hàm hiển thị kết quả
      function show_result()
      {
        // Lấy hai thẻ HTML
        var input = document.getElementById("message");
        var div = document.getElementById("result");
         
        // Gán nội dung ô input vào thẻ div
        div.innerHTML = input.value;
      }
    </script>
    <input type="text" id="message" value="" onkeyup="show_result()"/>
    <div id="result"></div>
```

Xem kết quả:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_14_Su%20kien%20trong%20javascript/1.png)
