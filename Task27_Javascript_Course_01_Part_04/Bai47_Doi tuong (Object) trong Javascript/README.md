## BÀI 48: THAO TÁC VỚI ĐỐI TƯỢNG (OBJECT) TRONG JAVASCRIPT

> Tài liệu: Thao tác với đối tượng (Object) trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/04/2017

### Mục lục: 

- [1. Thao tác với đối tượng (Object) trong Javascript](#1)

	+ [1.1 Hàm xem đối tượng sinh viên](#1.1)

	+ [1.2 Hàm thêm đối tượng sinh viên](#1.2)

	+ [1.3 Hàm xóa đối tượng sinh viên](#1.3)

	+ [1.4 Hàm sửa đối tượng sinh viên](#1.4)

	+ [1.5 Sử dụng đối tượng sinh viên](#1.5)

- [Tài liệu tham khảo](#2)

***

<a name="1"></a>
### 1. Thao tác với đối tượng (Object) trong Javascript:

**Đề bài**: Viết chương trình quản lý sinh viên gồm các thao tác chính như sau:

    + Xem danh sách sinh viên
    
    + Thêm sinh viên
    
    + Xóa sinh viên khỏi danh sách
    
    + Sửa thông tin sinh viên

- Với mỗi sinh viên cần lưu trữ các thông tin sau:

    + Mã sinh viên
    
    + Tên sinh viên
    
    + Emai

- Xác định các thuộc tính của đối tượng - thông tin lưu trữ của sinh viên --> cấu trúc của đối tượng như sau:

```javascript
var Student = {
    data : [],
    viewStudent : function(){
        // Xem danh sách sinh viên
    },
    addStudent : function(id, name, email){
        // Thêm sinh viên mới
    },
    removeStudent : function(id){
        // Xóa sinh viên
    },
    editStudent : function(id, name, email){
        // Sửa sinh viên
    }
};
```

<a name="1.1"></a>
#### 1.1 Hàm xem đối tượng sinh viên:

- Hàm này dùng để lặp qua đối tượng và dùng hàm `document.write` để hiển thị thông tin.

```javascript
viewStudent : function(){
    // Lấy danh sách sinh viên
    var listStudent = this.data;
 
    // Lặp và hiển thị sinh viên
    for(var i = 0; i < listStudent; i++){
        document.write("<div>" + listStudent[i].id + "|" + listStudent[i].name + "|" + listStudent[i].email + "</div>");
    }
}
```

<a name="1.2"></a>
#### 1.2 Hàm thêm đối tượng sinh viên:

- Để thêm đối tượng cần truyền vào 3 tham số như yêu cầu:

```javascript
addStudent : function(id, name, email){
    // Tạo thông tin sinh viên
    var item = {
        id : id,
        name : name,
        email : email
    };
 
    //Thêm sinh viên
    this.data.push(item);
}
```

<a name="1.3"></a>
#### 1.3 Hàm xóa đối tượng sinh viên:

- Để xóa sinh viên cần biết `id` của sinh viên đó, sử dụng hàm `splice` để xóa các phần tử của mảng.

```javascript
removeStudent : function(id){
    // Lặp qua sinh viên để tìm kiếm và xóa
    for(var i = 0; i < this.data.length; i++){
        if (this.data[i].id === id) { // nếu là sinh viên cần xóa
            this.data.splice(i, 1); // thì xóa
        }
    }
},
```

<a name="1.4"></a>
#### 1.4 Hàm sửa đối tượng sinh viên:

- Dựa vào `id` truyền vào để tìm sinh viên cần sửa.

```javascript
editStudent : function(id, name, email){
    // Tìm sinh viên cần edit
    for(var i = 0; i < this.data.length; i++){
        // nếu là sinh viên cần edit thì thực hiện edit
        if (this.data[i].id === id) { 
            this.data[i].name = name;
            this.data[i].email = email;
        }
    }
}
```

<a name="1.5"></a>
#### 1.5 Sử dụng đối tượng sinh viên:

```javascript
document.write('<h4>Danh sách sinh viên ban đầu</h4>');
Student.viewStudent();
 
document.write('<h4>Danh sách sinh viên sau khi thêm hai sinh viên</h4>');
Student.addStudent("sv001", 'Nguyễn Văn Cường', "thehalfheart@gmail.com");
Student.addStudent("sv002", 'Vũ Thị Thu Tình', "freetuts.net@gmail.com");
Student.viewStudent();
 
document.write('<h4>Danh sách sinh viên sau khi xóa một sinh viên</h4>');
Student.removeStudent('sv001');
Student.viewStudent();
 
document.write('<h4>Danh sách sinh viên sau khi sửa thông tin</h4>');
Student.editStudent('sv002', "Tên Sinh Viên Mới", "mrcuong.winter@gmail.com");
Student.viewStudent();
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Thao tác với đối tượng (Object) trong Javascript. https://freetuts.net/thao-tac-voi-doi-tuong-object-trong-javascript-409.html
