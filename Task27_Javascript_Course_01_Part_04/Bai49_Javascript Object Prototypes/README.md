## BÀI 49: JAVASCRIPT OBJECT PROTOTYPES

> Tài liệu: Javascript Object Prototypes
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/04/2017

### Mục lục: 

- [1. Prototypes trong Javascript](#1)

    + [1.1 Bổ sung dữ liệu vào đối tượng](#1.1)

- [2. Tạo mới Object và thao tác với Prototype](#2)

- [3. Thêm thuộc tính và phương thức vào Prototype](#3)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Prototypes trong javascript:

- Prototypes là các thành phần phương thức và thuộc tính của đối tượng, tất cả các đối tượng trong Javascript đều có 1 Prototype riêng để lưu trữ thành phần đó. Khi tạo mới 1 đối tượng thì đối tượng đó sẽ thừa kế tất cả các phương thức và thuộc tính chứa trong Prototype của đối tượng đó.

- Ví dụ khi tạo mới đối tượng Number thì nó sẽ bao gồm tất cả các hàm (phương thức) xử lý riêng của đối tượng Number.

```javascript
// Tạo mới đối tượng Number
var age = new Number(12);
 
// Lúc này sẽ sử dụng được các phương thức
age.toString();
age.toFixed();
age.toPrecision();
age.valueOf();
```

<a name="1.1"></a>
#### 1.1 Bổ sung dữ liệu vào đối tượng:

- Để thêm các thuộc tính và phương thức vào Prototype của 1 đối tượng bất kì sử dụng cú pháp:

```javascript
Object.prototype.thuoc_tinh = "giá trị mặc định";
Object.prototype.phuong_thuc = function(){
    // some thing
};
```

- Ví dụ thêm hàm `plus()` cộng dồn vào giá trị hiện tại của đối tượng Number, sử dụng hàm valueOf() để lấy giá trị hiện tại của đối tượng.

```javascript
// Tạo đối tượng
Number.prototype.plus = function(value){
return this.valueOf() + parseInt(value);
};
 
// Tạo mới đối tượng
var age = Number(12);
document.write(age.plus(12) + "<br/>");
 
// Tạo đối tượng khác
var year = 2014;
document.write(year.plus(12));
```

<a name="2"></a>
### 2. Tạo mới Object và thao tác với Prototype:

- Trong 2 cách tạo mới 1 Object với từ khóa `new Object` và `{}` thì khong thể sử dụng từ khóa `new` để khởi tạo 1 đối tượng được.

```javascript
var Person = {};
 
// Sai, không hoạt động
var p = new Person();
```

- **Ví dụ**: tạo đối tượng Person gồm các thuộc tính (name, email, address) và phương thức `showInfo()` để hiển thị thông tin

```javascript
function Person(){
     
    // Thuộc tính
    this.name = "";
    this.email = "";
    this.address = "";
     
    // Phương thức
    this.showInfo = function(){
        documenet.write("Tên là: " + this.name + "<br/>");
        documenet.write("Email là: " + this.email + "<br/>");
        documenet.write("Địa chỉ là: " + this.address + "<br/>");
    };
}
```

Muốn tạo mới đối tượng sử dụng các thuộc tính và phương thức thực hiện như sau:

```javascript
// Tạo mới
var cuong = new Person();
 
// Gán thuộc tính
cuong.name = "Nguyễn Văn Cường";
cuong.email = "thehalfheart@gmail.com";
cuong.address = "Buôn Ma Thuột ĐăkLăk";
 
// Gọi phương thức
cuong.showInfo();
```

<a name="3"></a>
### 3. Thêm thuộc tính và phương thức vào Prototype:

- Để bổ sung thuộc tính hoặc phương thức vào 1 đối tượng thông qua Prototype sử dụng cú pháp

```javascript
Object.prototype.thuoc_tinh = "giá trị mặc định";
Object.prototype.phuong_thuc = function(){
    // some thing
};
```

- **Ví dụ**: bổ sung thuộc tính `gender` và phương thức `showGender` vào đối tượng `Person`

```javascript
// Tạo đối tượng
function Person(){
     
    // Thuộc tính
    // ...
     
    // Phương thức
    // ...
}
 
// Bổ sung thông tin
Person.prototype.gender = "";
Person.prototype.showGender = function(){
  document.write(this.gender);  
};
 
 
// Sử dụng
var cuong = new Person();
cuong.gender = "Nam";
cuong.showGender();
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Javascript Object Prototypes. https://freetuts.net/javascript-object-prototypes-410.html
