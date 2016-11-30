##Bài: Tim hiểu về Robots.txt và Sitemap.xml

>Tài liệu: Tìm hiểu về Robots.txt và Sitemap.xml
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 28/11/2016

##Mục lục:

[1. Cài đặt WordPress lên hosting](#1)

[2. Tìm hiểu về Robots.txt](#2)

[3. Tìm hiểu về Sitemap.xml](#3)

[4. Thực hành demo về robots.txt và sitemap.xml lên site WordPress vừa cài](#4)


##Nội dung:

<a name="1"></a>
####1. Cài đặt WordPress lên hosting:

Mục đích của việc sử dụng WordPress là cài website để sử dụng trực tiếp mà không cần sử dụng localhost để chuyển host lên như lần trước.

- Bước 1: Tạo database và database user. 

![a](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/a.png)

Vào **databases** và chọn MySQL Databases. 

- Bước 2: Nhập tên vào user và mật khẩu theo yêu cầu:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/1.png)

- Bước 3: Vào website và chọn **trình tự động cài đặt**

![b](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/b.png)

Sau đó điền tên ứng dụng cần tìm vào: WordPress -> Tiến hành điền các thông tin vào ô như bên dưới:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/2.png)

- Sau khi tạo xong bấm vào cài đặt và đợi trong vài phút và tải lại trang ta được như sau:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/3.png)

- Bước 4: Truy cập lại vào URL xác nhận lại thông tin đăng nhập:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/4.png)

- Bước 5: Đây là giao diện WordPress sau khi cài đặt thành công:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/5.png)

Và bây giờ truy cập lại vào địa chỉ letutrinh.com ta có giao diện như sau:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/6.png)


<a name="2"></a>
####2. Tìm hiểu về Robots.txt:

Robots là những con robot (bọ tìm kiếm), có tác dụng tìm kiếm thông tin trên Website, kiểm tra đánh giá chất lượng website theo các truy vấn tìm kiếm cụ thể. Còn file robots.txt được sử dụng để hướng dẫn công cụ tìm kiếm tự động đến những trang nào mà bạn muốn nó tìm kiếm và sau đó thì index trang đó. Hầu hết các trang web nào cũng có những thư mục và file không cần đến robot, tức là không muốn bị các công cụ tìm kiếm ghé thăm, vậy nên tạo file robots.txt rất cần thiết trong SEO.

File robots.txt được tạo bởi các công cụ đơn giản như Notepad, và file này được đặt trong thư mục gốc chứa mã nguồn website của mình.

4 lệnh cơ bản của robots.txt như sau:

- User-agent: User-agent của robot cần chặn, hoặc cấp quyền truy cập, sử dụng * cho tất cả robot.

- Disallow: không cho phép crawler truy cập 1 nội dung (file)

- Allow: cho phép crawler truy cập 1 nội dung

- Sitemap: Thông báo cho máy tìm kiếm biết XML của trang web

Ví dụ cụ thể:

- Không cho phép robot nào truy cập vào trang web của bạn:

```
	User-agent: *
	Disallow:/
```

Có ích trong việc ngăn chặn robot truy cập vào trang quản trị website của bạn


- Để cấp quyền cho phép robot truy cập vào tất cả nội dung trang web:

```
	User-agent: *
	Disallow: 
	( có thể tạo file robots.txt trắng hoặc xóa nó đi)
```

- Để ngăn chặn robot truy cập một vài nội dung trên trang web. Chúng ta sẽ chặn toàn bộ file/ thư mục con trong /cgi-bin/ và /private-directory/

```
	User-agent: *
	Disallow: /cgi-bin/
	Disallow: /private-directory/
```

- Để ngăn chặn đích danh một robot nào đó truy cập trang web. Chúng ta sẽ chặn BadBot

```
	User-agent: BadBot
	Disallow: /
```

- Để cho phép các robot truy cập một thư mục con của một thư mục bị cấm truy cập. Trong trường hợp này, chúng ta chặn toàn bộ file/ thư mục con của /private-parent/ ngoại trừ /public-child/.

```
	User-agent: *
	Disallow: /private-parent/
	Allow: /private-parent/public-child/
```

Trên WordPress nên tạo 1 file robots.txt như sau:

```
	User-agent: *
	Allow: /wp-content/uploads/
	Disallow: /readme.html
	Sitemap: http://tenmien.com/site.xml
```

Có nghĩa là chúng ta sẽ cho robot thu thập thư mục uploads, những thư mục chứa hình ảnh trong bài viết nhưng chặn chúng vào thư mục plugins trong `wp-content`, và chặn trang readme.html- đây là trang thông tin phiên bản WordPress ta đang sử dụng


<a name="3"></a>
####3. Tìm hiểu về sitemap.xml:

XML Sitemap là bản đồ thu nhỏ của website liệt kê tất cả các liên kết có bên trong website. Mục đích là lấy sitemap gởi lên Google Webmaster Tools, các bot tìm kiếm sẽ lần theo địa chỉ trong sitemap này đưa nó vào hệ thống dữ liệu của google.

XML Sitemap giúp cho bọ của các cỗ máy tìm kiếm như Google, Bing... dễ dàng thu thập dữ liệu trên trang Web của bạn bởi nó đã tạo ra 1 lộ trình sẵn (bản đồ) các bọ tìm kiếm chỉ việc đi theo lộ trình đó. Đối với các website mới thì sitemap giúp cho các công cụ tìm kiếm dò thấy trang mình nhanh hơn, giảm thời gian đáng kể để thiết lập chỉ mục.

Nhưng đối với những trang web có nội dung chất lượng kém thì mặc dù có trong sitemap nhưng vẫn có thể bị google loại bỏ không cho index.

<a name="4"></a>
####4. Thực hành demo về robots.txt và sitemap.xml lên site WordPress vừa cài:

- Tạo 1 file robots.txt trong thư mục gốc của website như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(1).png)


- Sau khi tạo xong:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(2).png)

- Vào SEO-> XML Sitemaps để cấu hình sitemap của plugin:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(3).png)

- Chúng ta có thể xem sơ đồ trang web tại đây: http://chuyengiaseoweb.net/sitemap_index.xml

![5](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(5).png)

- Gửi sitemap lên Google Webmasters Tool, làm theo hướng dẫn ta xã thực thành công quyền sở hữu với trang web:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(6).png)

- Sau khi thêm sơ đồ trang web thành công ta có:

![7](https://github.com/TrinhTu/web_developer/blob/master/Task14_Robots_and_Sitemap/image/(7).png)




