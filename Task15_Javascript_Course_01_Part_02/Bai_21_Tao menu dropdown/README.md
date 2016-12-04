##Bài 21: BÀI TẬP JAVASCRIPT- XÂY DỰNG MENU DROPDOWN

>Tài liệu: Xây dựng menu dropdown
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Xây dựng HTML- CSS cho dropdown menu](#1)

[2. Code Javascript hiệu ứng Dropdown menu](#2)

##Nội dung:

<a name="1"></a>
####1. Xây dựng HTML-CSS cho dropdown menu:

Code đoạn mã `.html` như sau:

```javascript
<ul id="dropdown">
        <li><a href="#">Trang chủ</a></li>
        <li><a href="#">Giới thiệu</a>
                <ul>
                  <li><a href="#">Lịch sử hình thành</a></li>
                  <li><a href="#">Logo học viện</a></li>  
                </ul>
        </li>
        <li><a href="#">Đào tạo</a>
                <ul>
                    <li><a href="#">Mô hình đào tạo</a></li>
                    <li><a href="#">Chương trình học</a></li>
                    <li><a href="#">Chuẩn đầu ra</a></li>
                </ul>
        </li>
        <li><a href="#">Khoa học công nghệ</a>
                <ul>
                    <li><a href="#">Chiến lượt KH-CN</a></li>
                    <li><a href="#">Viện nghiên cứu</a></li>
                </ul>
        </li>
        <li><a href="#">Sinh viên</a>
                <ul>
                    <li><a href="#">Thông tin chung</a></li>
                    <li><a href="#">Học bổng</a></li>
                    <li><a href="#">Tuyển dụng</a></li>
                </ul>
        </li>
        <li><a href="#">Hợp tác quốc tế</a></li>
</ul>
```

Viết CSS cho menu này:

```javascript
		#dropdown{
            width: 200px;
        }
        #dropdown li{
            list-style: none;
            line-height: 30px;
            background: pink;
            margin: 2px;
        }
        #dropdown li a{
            margin-left: 20px;
            color: yellow;
            text-decoration: none;
        }
        #dropdown ul{
            display: none;
            padding: 0px;
            background: aqua;
        }
        #dropdown ul li{
            background: green;
        }
        
```

Giao diện khi xong bước 1:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_21_Tao%20menu%20dropdown/1.png)

<a name="2"></a>
####2. Code Javascript hiệu ứng dropdown menu:

```javascript
		var menu = document.querySelectorAll('#dropdown > li');
        for( var i=0; i < menu.length; i++)
        { // lặp để gán sự kiện
            menu[i].addEventListener("click", function()
            {
                var menuList = document.querySelectorAll('#dropdown > li > ul');
                for (var j = 0; j < menuList.length; j++)
                {
                    menuList[j].style.display="none";
                }
                this.children[1].style.display="block";
        	});
        }
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_21_Tao%20menu%20dropdown/2.png)

Xem kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript21.html#
