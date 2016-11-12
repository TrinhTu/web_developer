##Bài 10: Thao tác với mảng trong JS

>Tài liệu: Thao tác với mảng trong JS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 13/11/2016

###Mục lục:

[1.Khai báo mảng ](#1)

- [1.1 Khai báo với từ khóa new Array()](#1.1)

- [1.2 Khai báo với cặp dấu ngoặc vuông](#1.2)

[2. Truy xuất các phần tử trong mảng](#2)

[3. In mảng ra trình duyệt và console](#3)

[4. Sử dụng vòng lặp để lặp mảng](#4)

- [4.1 Lặp mảng với vòng lặp for](#4.1)

- [4.2 Lặp mảng với vòng lặp while](#4.2)

###Nội dung:

 Mảng là một tập hợp các phần tử lại và mỗi phần tử sẽ được đánh dấu một vị trí trong tập hợp đó. Trong javascript nếu mảng có 10 phần tử thì các phần tử sẽ được đánh dấu từ 0 -9.

<a name="1"></a>
####1. Khai báo mảng:

<a name="1.1"></a>
#####1.1 Khai báo mảng với từ khóa new Array:

Cú pháp:

```
var name_array = new Array();
// Hoặc
var name_array = new Array(1,2,3);
```

<a name="1.2"></a>
#####1.2 Khai báo mảng với cặp dấu ngoặc vuông:

Cú pháp:

```
var name_array = [];
// Hoặc
var name_array = [1,2,3];
```
<a name="2"></a>
####2. Truy xuất các phần tử trong mảng:

Ta sử dụng cú pháp `tenmang[vitri]. Ví dụ:

```
var t = new Array(1,2,3);
alert(t[0]); // kết quả là 1
alert(t[1]); // kết quả là 2
alert(t[2]); // kết quả là 3
```

 Phần tử đầu tiên sẽ có số chỉ mục là 0, phần tử thứ hai là 1, ... phần tử thứ n là n-1.

<a name="3"></a>
####3. In mảng ra trình duyệt và console:

Để hiển thị các phần tử ra ngoài trình duyệt ta sử dụng hàm `arry.join()` . Ví dụ:

```
var t = new Array(1,2,3);
document.write(t.join()); // kết quả 1,2,3
document.write(t.join('-')); // kết quả 1-2-3
```

Ngoài ra còn 1 hàm nữa là `console.log()` dùng để debug. Hãy cài đặt Firebug trên firefox hoặc dùng chế độ "kiểm tra phần tử" có sẵn trên trình duyệt, sau đó chuyển vào mục console. 

Nếu code bị lỗi cú pháp hay lỗi gì liên quan đến javascrip thì nó sẽ hiển thị bên dưới cho mình dễ dàng nhận biết và sửa lỗi.

Ví dụ khi viết đoạn code này vào trong tài liệu chạy trên trình duyệt không thấy nó hoạt động:

```
var t = new Arry(1,2,3);
console.log(t);
```

Chạy giao diện console như sau:

![anh](http://i.imgur.com/5NRTxxR.png)

<a name="4"></a>
####4. Sử dụng vòng lặp để lặp mảng:

Để đếm tổng số phần tử của một mảng chúng ta sẽ dùng thuộc tính length của nó. Ví dụ:

```
var t = new Array(1,2,3);
alert(t.length);<br>
```
<a name="4.1"></a>
#####4.1 Lặp mảng với vòng lặp for:

Để lặp mảng với vòng lặp for thì chúng ta phải dùng thuộc tính length như trên để đếm tổng số phần tử, sau đó ở mỗi vòng lặp chúng ta sử dụng cú pháp truy xuất đến phần tử của mảng ở phần 2 để xử lý. Ví dụ:

```
var name_array = [1,2,3];
for (var i = 0; i < name_array.length; i++){
    document.write(name_array[i]);
}
```

<a name="4.2"></a>
#####4.2 Lặp mảng với vòng lặp while:

Tương tự để lặp với vòng lặp while  chúng ta sẽ khai báo một biến index để lưu vị trí đang lặp. Ví dụ:

```
var name_array = [2,3,4];
var index = 0;
while (index < name_array.length){
    document.write(name_array[index]);
    index++;
}
```

Đối với vòng lặp do while thì không nên sử dụng để lặp mảng, vì nó vòng lặp do while luôn luôn lặp ít nhất một lần nên trong trường hợp mảng cần lặp rỗng thì sẽ bị báo lỗi.
