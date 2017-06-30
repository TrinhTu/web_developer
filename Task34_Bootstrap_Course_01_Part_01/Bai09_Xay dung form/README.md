## BÀI 09: XÂY DỰNG FORM VỚI BOOTSTRAP 3

> Tài liệu: Xây dựng form với bootstrap 3
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 30/06/2017

### Mục lục:

[1. Định dạng Vertical form](#1)

[2. Horizontal form trong bootstrap 3](#2)

[3. Inline form trong bootstrap 3](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Định dạng Vertical form:

- Mọi thành phần trong form đều được bao quanh bởi cặp thẻ `form` và bên trong là class `form-group` và bên trong thành phần input được định nghĩa bằng class `form-control`, class có tác dụng stylesheet cho thẻ input.

```javascript
<div class="example">
<div class="container">
    <div class="row">
    <h2>Vertical Form</h2>
        <form>
        <div class="form-group">
            <label>Email</label>
            <input type="email" class="form-control" placeholder="Email">
        </div>
        <div class="form-group">
            <label>Mật Khẩu</label>
            <input type="password" class="form-control" placeholder="Password">
        </div>
        <div class="checkbox">
            <label><input type="checkbox"> Ghi Nhớ</label>
        </div>
        <button type="submit" class="btn btn-primary">Đăng Nhập</button>
    </form>
    </div>
</div>
     
</div>
```

<a name="2"></a>
### 2. Horizontal form trong bootstrap 3:

- Kiểu form này có thể kết hợp với Grid system để bố cục kích thước của form và tag `label` hợp lí, các class hỗ trợ:

	+ control-label (khai báo class này ở tag label để gán class col-xs-x)

	+ form-horizontal (định dạng kiểu form ngang)

	+ col-xs-offset-2 (canh lề trái)

```javascript
    		<div class="row">
                <h2>Horizontal Form</h2>
                <form class="form-horizontal">
                    <div class="form-group">
                        <label class="control-label col-xs-2">Email</label>
                        <div class="col-xs-10">
                            <input type="email" class="form-control" placeholder="Email">
                        </div>
                    </div>
                    <div class="form-group">
                        <label class="control-label col-xs-2">Mật Khẩu</label>
                        <div class="col-xs-10">
                            <input type="password" class="form-control" placeholder="Password">
                        </div>   
                    </div>
                    <div class="form-group">
                        <div class="col-xs-offset-2 col-xs-10">    
                            <button type="submit" class="btn btn-primary">Đăng Nhập</button>
                        </div>
                    </div>    
                </form>
            </div>
```

<a name="3"></a>
### 3. Inline form trong bootstrap 3:

```javascript
			 <div class="row">
                <h2>Inline Form</h2>
                <form class="form-inline">
                    <div class="form-group">
                            <input type="email" class="form-control" placeholder="Email">
                    </div>
                    <div class="form-group">
                            <input type="password" class="form-control" placeholder="Password">
                    </div>
                    <div class="form-group">
                            <button type="submit" class="btn btn-primary">Đăng Nhập</button>
                    </div>    
                </form>
            </div>
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Xây dựng form với bootstrap 3. https://freetuts.net/xay-dung-form-voi-bootstrap-3-176.html