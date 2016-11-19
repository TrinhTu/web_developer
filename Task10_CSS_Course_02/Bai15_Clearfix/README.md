## Bài 15: Kĩ thuật ClearFix trong CSS:

>Tài liệu: Kĩ thuật ClearFix trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 19/11/2016

###Mục lục:

[1. Kĩ thuật ClearFix là gì?](#1)

[2. Kĩ thuật ClearFix trong CSS](#2)

###Nội dung:

<a name="1"></a>
####1. Kĩ thuật ClearFix là gì?

Sử dụng thuộc tính ClearFix để chỉnh vùng không gian của thẻ cha so với thẻ con có sử dụng float, khi sử dụng float thì chiều cao của thẻ cha sẽ được tính là 0px so với thẻ con float. Chiều cao của thẻ cha sẽ được tăng lên khi nội dung bên trong của nó không sử dụng float.
Kĩ thuật này sử dụng chủ yếu để tạo layout bố cục.

```
<style>
     .group1{
         border: solid 1px red;
         }
     .left{
         border: solid 1px blue;
         width: 200px;
         height: 200px;
         float: left;
        }
      .right{
         border: solid 1px blue;
         width: 200px;
         height: 200px;
         float: right;
        }
 
</style>
 </head>
    <body>
        <div class="group1">
            <div class="left">
                float:left, không ảnh hưởng tới chiều cao thẻ cha
            </div>
            <div class="right">
                float:right, không ảnh hưởng tới chiều cao thẻ cha
            </div>
            <div>
                Nội dung không có float. Chiều cao của thẻ cha phụ thuộc thẻ div này thôi.
            </div>
        </div>
```
Hiển thị nội dung sẽ như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai15_Clearfix/image/(1).png)

Kĩ thuật Clearfix là kĩ thuật chỉnh chiều cao của thẻ cha tương đương với chiều cao của mọi thẻ con để nội dung hiển thị không bị đè lên.


<a name="2"></a>
####2. Kĩ thuật ClearFix trong CSS:

Ví dụ ta có:

```
 <style>
 
    .group1{
         border: solid 1px yellow;
         padding: 2px;
        }
 
    .left{
        border: solid 1px blue;
        width: 200px;
        height: 200px;
        float: left;
        background: aqua;
        }
    .right{
         border: solid 1px blue;
         width: 200px;
         height: 200px;
         float: right;
         background: green;
        }
    .group2{
        background: red;
        height: 150px;
         }
 </style>
    </head>
    <body>
        <div class="group1">
            <div class="left">Nội dung hiển thị bên trái</div>
            <div class="right">Nội dung hiển thị bên phải</div>
        </div>
        <div class="group2">
            Nội dung hiển thị bên dưới
        </div>
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai15_Clearfix/image/(2).png)

 Nhìn vào ví dụ ta có thể thấy rằng nội dung của cột chính giữa đã bị 2 cột 2 bên đè lên, vì 2 cột đó sử dụng float nên phần border màu đen không ảnh hưởng chiều cao, vì vậy phâng nội dung chính giữa màu đỏ sẽ nằm bên dưới. Và phần tiếp giao giữa 2 phần là vùng After của phần border màu đen. Ta thêm vào nội dung như sau để xóa vùng cho 2 bên:

 ```
 .ground1:after{
    display: block;
    content: ".";
```

Nhưng vì mặc định của `after` là hiển thị dạng `display: inline-block` nên ta cần đổi nó sang dạng `display: block`

```
.group1: after{
    clear: both;
    content:".";
    display: block;
}
```

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai15_Clearfix/image/(3).png)

Ta thấy phần nội dung nằm trong ô chính giữa đã được đẩy xuống

Thiết lập them chiều dài và chiều rộng cho phần after để xóa đi vùng dấu chấm không cần thiết:

```
group1:after{
    clear: both;
    content:".";
    display: block;
    width: 0px;
    height: 0px;
}
```

![4](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai15_Clearfix/image/(4).png)
