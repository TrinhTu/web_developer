##Git & Github

> Tài liệu: Git & Github
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 30/09/2016

### Mục lục

[1. Tìm hiểu cách thức hoạt động của Github](#hoatdong)

[2. Hiểu được các khái niệm: Add, Remove, Commit, Push, Pull, Fetch, Clone, Fork, Star, Watch.](#khainiem)

[3. Tìm hiểu các bước để Setting up Git, Generate and add SSH key, Caching your GitHub password in Git.](#tienhanh)

<a name=hoatdong></a>
###1. Tìm hiểu cách thức hoạt động của Github:

Git là phần mềm quản lí mã nguồn phân tán (DVCS) nghĩa là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của mã nguồn, đc nhân bản từ 1 kho chứa mã nguồn.

Còn github là nơi để lưu trữ mã nguồn đó. Github là 1 dịch vụ lưu trữ dựa trên web cho các dự án phát triển phần mềm sử dụng hệ thống kiểm soát phiên bản của git. Github chính là 1 dịch vụ máy chủ repository công cộng, mọi người có thể tạo tài khoản trên đó tạo ra kho để lưu trữ dữ liệu của mình.

Các kho dữ liệu được lưu trên github có thể ở chế độ công khai hoặc là cá nhân bạn, hay nhóm thành viên làm việc có thể xem đc,  Bằng cách tạo repository trong github ta có thể đẩy repo này về máy để lưu lại, hoặc đẩy kho trong máy lên github để lưu trữ đề phòng dữ liệu trong máy bị mất.

<a name=khainiem></a>
###2. Hiểu được các khái niệm:
Commit: là đồng bộ file code trên máy tính với github trên server

Push: upload thay đổi lên server

Pull: là đồng bộ trạng thái từ server về máy

Stagging area: những thay đổi với file mã nguồn sẽ được lưu lại

Fork: là 1 kho lưu trữ cho phép tự do thử nghiệm với những thay đổi mà không làm ảnh hưởng đến dự án ban đầu

Clone: tải về máy hay tải lên server

<a name=tienhanh></a>
###3. Các bước cài đặt Git, tạo và thêm khóa SSH, Caching mật khẩu của bạn trong git:

**Các bước cài đặt Git:**

- Tải về: [tại đây]( https://windows.github.com/)

- Mở git shell

- Nhập tên, email <ul>

- Chứng thực với Github từ Git qua kết nối SSH<ul>
<li>Tạo 1 SSH key mới:</li>


<li>Đảm bảo ssh-agent được kích hoạt:</li>



<li>Vào file id_rsa.pub để sao chép nội dung file sau đó upload lên [đây](https://github.com/settings/keys) và lưu lại.


###Tài liệu tham khảo:

[Tài liệu 1](https://github.com/hocchudong/git-github-for-sysadmin)

[Tài liệu 2]( https://help.github.com/articles/set-up-git/)

[Tài liệu 3](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

[Tài liệu 4](https://help.github.com/articles/caching-your-github-password-in-git/)

    
