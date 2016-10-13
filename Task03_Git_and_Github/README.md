##Git & Github

> Tài liệu: Git & Github
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 13/10/2016

### Mục lục

[1. Tìm hiểu cách thức hoạt động của Github](#hoatdong)

[2. Hiểu được các khái niệm: Add, Remove, Commit, Push, Pull, Fetch, Clone, Fork, Star, Watch.](#khainiem)

  <ul>
  <li>[2.1 Add, Commit, Push](#commit)</li>
  <li>[2.2 Watch](#watch)</li>
  <li>[2.3 Full](#full)</li>
  <li>[2.4 Stagging area](#staggingarea)</li>
  <li>[2.5 Fork](#fork)</li>
  <li>[2.6 Clone](#clone)</li>
  <li>[2.7 Fetch](#fetch)</li>
  <li>[2.8 Start](#start)</li>
  <li>[2.9 Remote](#remote)</li>
  </ul>
  
[3. Tìm hiểu các bước để Setting up Git, Generate and add SSH key, Caching your GitHub password in Git.](#tienhanh)
 <ul>
 <li>[3.1 Cài đặt Git](#caidat)</li>
 <li>[3.2 Tạo và thêm khóa SSH](#ssh)</li>
 <li>[Cách Caching mật khẩu trong Git](#caching)</li>
 </ul>

<a name="hoatdong"></a>
###1. Tìm hiểu cách thức hoạt động của Github:

Git là phần mềm quản lí mã nguồn phân tán (DVCS) nghĩa là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của mã nguồn, đc nhân bản từ 1 kho chứa mã nguồn.

Còn github là nơi để lưu trữ mã nguồn đó. Github là 1 dịch vụ lưu trữ dựa trên web cho các dự án phát triển phần mềm sử dụng hệ thống kiểm soát phiên bản của git. Github chính là 1 dịch vụ máy chủ repository công cộng, mọi người có thể tạo tài khoản trên đó tạo ra kho để lưu trữ dữ liệu của mình.

Các kho dữ liệu được lưu trên github có thể ở chế độ công khai hoặc là cá nhân bạn, hay nhóm thành viên làm việc có thể xem đc,  Bằng cách tạo repository trong github ta có thể đẩy repo này về máy để lưu lại, hoặc đẩy kho trong máy lên github để lưu trữ đề phòng dữ liệu trong máy bị mất.

<a name="khainiem"></a>
###2. Hiểu được các khái niệm:
<a name="commit"></a>
#####2.1  Add, Commit, Push:

Add: Cập nhật tình trạng các file( thêm, xóa, sửa) trong project được quản lý bởi GIT

Để thực hiện hành động `add` ta sử dụng lệnh sau

> git add README.md

để `add` file README.md

hoặc `git add *` để add tất cả các file hiện có.

Commit: Là đồng bộ file code trên máy tính với github trên server

Câu lệnh commit file README.md như sau:

> git commit -m "chú thích"

![anh](http://imageshack.com/a/img921/1826/XDsm5K.png)
-m là để ghi lại chú thích cho hành động đó

Push : là đẩy những thay đổi từ local lên server

> git push origin master

![anh](http://imageshack.com/a/img923/8539/C9Mvzx.png)

<a name="watch"></a>
#####2.2 Watch:

Khi bạn xem một repo lưu trữ, bạn nhận được thông báo cho bất kỳ yêu cầu mới  và các vấn đề mà được tạo ra, bao gồm cả những người không nhắc đến bạn.

Trên GitHub, điều hướng đến các trang chính của các repo lưu trữ.

Chọn menu sát Ở góc trên bên phải, trong danh sách "Watch", chọn Watch.

![anh](http://i.imgur.com/HsfCZqO.png)

<a name="pull"></a>
#####2.3 Pull:

Là đồng bộ trạng thái từ server về máy

Câu lệnh:   `git pull <tên nhánh>`
<a name="staggingarea"></a>
#####2.4 Stagging area:

Stagging area: những thay đổi với file mã nguồn sẽ được lưu lại
<a name="fork"></a>
#####2.5 Fork:

Fork: là 1 kho lưu trữ cho phép tự do thử nghiệm với những thay đổi mà không làm ảnh hưởng đến dự án ban đầu

Tại một thời điểm, chúng ta muốn phân phối project của ai đó, hay chúng ta muốn sử dụng project của một ai đố để bắt đầu. Điều này được định nghĩa là forking. Trong phần này, chúng ta sẽ forking một repo tên là awesome.


<a name="clone"></a>
#####2.6 Clone:

Clone: tải về máy hay tải lên server

Để clone 1 kho có sẵn trên máy cục bộ ta sử dụng câu lệnh như sau:

>git clone /đường_dẫn/repository
 
 Nếu như repository đó nằm ở máy khác thì ta gõ câu lệnh như sau:

>git clone tenusername@diachimaychu:/đường_dẫn/repository
<a name="fetch"></a>
#####2.7 Fetch:

Fetch: là cập nhập những thay đổi từ  repo server về repo local

 `$ git fetch [remote-name]`

Lệnh này sẽ truy cập vào dự án từ xa đó và kéo xuống toàn bộ dữ liệu mà bạn chưa có trong đó cho bạn.  Khi thực hiện xong bước này, bạn đã có các tham chiếu đến toàn bộ các nhánh của dự án từ xa đó, nơi mà bạn có thể tích hợp hoặc kiểm tra bất kỳ thời điểm nào
<a name="start"></a>
#####2.8 Start:

Star một kho lưu trữ cho phép bạn theo dõi các dự án mà bạn thấy thú vị, thậm chí nếu bạn không liên quan đến dự án.

<a name="remote"></a>
#####2.9 Remote:

Để xem bạn đã cấu hình tới máy chủ từ xa nào, bạn có thể chạy lệnh git remote. Nó sẽ liệt kê tên ngắn gọn của mỗi máy chủ từ xa bạn đã chỉ định. Nếu bạn sao chép nó từ một kho chứa có sẵn, ít nhất bạn sẽ thấy bản gốc (origin) - tên mặc định mà Git đặt cho phiên bản trên máy chủ mà bạn đã sao chép từ đó.

![anh](http://i.imgur.com/vR3DLLz.png)

<a name="tienhanh"></a>
###3. Các bước cài đặt Git, tạo và thêm khóa SSH, Caching mật khẩu của bạn trong git:

<a name="caidat"></a>
####**3.1Các bước cài đặt Git:**

- Tải về: [tại đây]( https://windows.github.com/)

- Mở git shell

- Nhập tên, email 
<ul>
<li>![anh](http://i.imgur.com/qe6eNIP.png)</li>

- Chứng thực với Github từ Git qua kết nối SSH<ul>

<a name="ssh"></a>
####**3.2 Tạo và thêm khóa SSH**
<ul>
<li>Tạo 1 SSH key mới:</li>

![anh](http://i.imgur.com/yNKtIvt.png)

<li>Đảm bảo ssh-agent được kích hoạt:</li>

![anh](http://imageshack.com/a/img921/2353/pgRyOb.png)

![anh](http://imageshack.com/a/img922/5405/loFt4M.png)

<li>Vào file id_rsa.pub để sao chép nội dung file sau đó upload lên [đây](https://github.com/settings/keys) và lưu lại.</li>

![anh](http://imageshack.com/a/img921/4867/82M8oi.png)

<a name="caching"></a>
####**3.3 Caching mật khẩu của bạn trong Git**

Nếu bạn đang [nhân bản kho trong github sử dụng HTTPS](https://help.github.com/articles/which-remote-url-should-i-use/) bạn có thể sử dụng 1 helper nói với git nhớ tên đăng nhập và mật khẩu của bạn mỗi khi nói đến github

Nếu như bạn chép kho GitHub sử dụng SSH, sau đó bạn xác thực bằng các phím SSH thay vì một tên người dùng và mật khẩu. Để giúp thiết lập một kết nối SSH xem tại [đây](#ssh)

Bật helper ủy nhiệm để Nó sẽ lưu mật khẩu của bạn trong bộ nhớ cho một số thời gian. Theo mặc định, Git sẽ cache mật khẩu của bạn trong 15 phút

Mở terminal và nhập: 

>$ git config --global credential.helper cache

  `#đặt git để sử dụng cache ủy nhiệm`
###Tài liệu tham khảo:

[Tài liệu 1](https://github.com/hocchudong/git-github-for-sysadmin)

[Tài liệu 2]( https://help.github.com/articles/set-up-git/)

[Tài liệu 3](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

[Tài liệu 4](https://help.github.com/articles/caching-your-github-password-in-git/)

    
