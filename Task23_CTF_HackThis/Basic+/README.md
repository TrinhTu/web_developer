## HackThis: BASIC

> **Category:** BASIC
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/Basic+

## Write-up

### Level 1: 

- **URL:**https://www.hackthis.co.uk/levels/basic+/1

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/1.png"/></p>


- **Solution:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/11.png"/></p>

Định dạng của tập tin có thể sai, nó không phải là dạng văn bản, chuyển sang định dạng khác `bmp` --> kết quả

### Level 2:

- **URL:**https://www.hackthis.co.uk/levels/basic+/2

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/2.png"/></p>

- **Solution:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/12.png"/></p>

Ở đây user agent hiện tại không được chấp nhận chỉ cho phép secure_user_agent vậy nên cần đổi tên của user agent hiện tại

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/12-1.png"/></p>

Tại trình duyệt Chrome ta cài đặt user agent và tạo thêm sercure_user_agent.

### Level 3: 

- **URL:**https://www.hackthis.co.uk/levels/basic+/3

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/3.png"/></p>

- **Solution:**

Dùng tamper để thay đổi giá trị 

[3.1]

### Level 4:

- **URL:**https://www.hackthis.co.uk/levels/basic+/4

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/4.png"/></p>

- **Solution:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/14.png"/></p>

Tải hình ảnh về và xem thông tin của nó ta có:

	+ author: james

	+ comment: I like chocolate

Không còn thông tin gì thêm nên try hard username: `james` và password: `ilikechocolate` nhưng không thành công vậy thử lại 1 lần nữa với password là `chocolate` --> level complete.

### Level 5: 

- **URL:**https://www.hackthis.co.uk/levels/basic+/5

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/5.png"/></p>

- **Solution:**

	+ Cũng như ở level 5 ta tải về và xem thông tin hình không có gì vậy nên thử mở hình ảnh bằng 1 công cụ khác chẳng hạn như notepad.

		+ username: **admin**

		+ password: **safe**

### Level 6: // to-do

- **URL:**https://www.hackthis.co.uk/levels/basic+/6

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/6.png"/></p>

- **Solution:**

### Level 7: // to-do

- **URL:**https://www.hackthis.co.uk/levels/basic+/7

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Basic%2B/image/7.png"/></p>


- **Solution:**
