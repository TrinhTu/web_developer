##Bài 11: CÁC HÀM XỬ LÝ MẢNG TRONG JAVASCRIPT

>Tài liệu: Các hàm xử lý mảng trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 03/12/2016

###Mục lục:

[1. Hàm array.valueOf()](#1)

[2. Hàm array.push()](#2)

[3. Hàm arry.pop()](33)

[4. Hàm arry.shift()](#4)

[5. Hàm array.unshift()](#5)

[6. Hàm arry.splice()](#6)

[7. Hàm arry.sort()](#7)

[8. Hàm arry.reverse()](#8)

[9. Hàm arry.concat()](#9)

[10. Hàm arry.slice()](#10)


###Nội dung:

<a name="1"></a>
####1. Hàm arry.valueOf():

Hàm này có tác dụng nối các phần tử với nhau vào 1 chuỗi cách nhau bởi dấu phẩy. Ví dụ:

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt", "đầu."];
document.write(mang.valueOf());
```
Xem kết quả:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/1.png)

<a name="2"></a>
####2. Hàm arry.push():

Thêm 1 phần tử vào cuối mảng:

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt", "đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.push("tại đây"); //Thêm phần tử vào cuối mảng
document.write(mang.valueOf()); //in kết quả ra màn hình
```
Xem kết quả:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/2.png)

<a name="3"></a>
####3. Hàm arry.pop():

Ngược với hàm `array.push()`, hàm này có tác dụng xóa đi phần tử cuối cùng trong mảng:

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.pop(); //xóa phần tử cuối của mảng
document.write(mang.valueOf()); //in kết quả ra màn hình
```

Xem kết quả:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/3.png)

<a name="4"></a>
####4. Hàm arry.shift():

Xóa đi phần tử đầu tiên của mảng, sau đó dồn các phần tử phía sau xuống 1 bậc.

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.shift();
document.write(mang.valueOf()); //in kết quả ra màn hình
```
Xem kết quả:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/4.png)

<a name="5"></a>
####5. Hàm arry.unshift():

Thêm 1 phần tử vào vị trí đầu tiên của mảng, đầy các phần tử phía sau lên 1 bậc:

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.unshift("Chào mừng") //
document.write(mang.valueOf()); //in kết quả ra màn hình
```

Xem kết quả:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/5.png)

<a name="6"></a>
####6. Hàm arry.splice():

Hàm `splice()` có 3 tham số truyền vào như sau: `splice(position_add, num_element_remove, value1, value2, ...)`

Trong đó: 

- **position_add** là vị trí sẽ thêm ( vị trí đầu tiên là 0)

- **num_element_remove** là số phần tử sẽ xóa ( bắt đầu từ `position_add`)

- **value1, value2,...** là danh sách phần tử sẽ được thêm vào sau khi tại vị trí `position_add` và sau khi remove `num_element_remove` phần tử.

Ví dụ:

```javascript
var mang = ["Học", "javascript", "căn", "bản"];
mang.splice(1, 3, 'lập trình', 'tại', 'đây');
document.write(mang.valueOf());
```

Xem kết quả:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/6.png)

<a name="7"></a>
####7. Hàm arry.sort():

Hàm này dùng để sắp xếp các phần tử trong mảng theo thứ tự chữ cái alpha.

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.sort();
document.write(mang.valueOf()); //in kết quả ra màn hình
```

Xem kết quả: 

![7](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/7.png)

<a name="8"></a>
####8. Hàm arry.reverse():

Hàm đảo ngược các phần tử lại.

```javascript
var mang = ["Học", "javascript", "cơ", "bản", "cho", "người", "mới", "bắt đầu"];
document.write(mang.valueOf());
document.write('<br/>') //Xuống dòng
mang.reverse(); //
document.write(mang.valueOf()); //in kết quả ra màn hình
```

Xem kết quả:

![8](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/8.png)

<a name="9"></a>
####9. Hàm arry.concat():

Để nối 2 mảng với nhau và trả về 1 mảng gồm tổng số phần tử của 2 mảng đó.

```javascript
var mang1= ["Học", "lập", "trình"];
var mang2= ["cơ bản", "cho", "người", "mới", "bắt đầu"];
//nối mảng
var mang_con = mang1.concat(mang2);
document.write(mang_con.valueOf());
```

Xem kết quả:

![9](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/9.png)

<a name="10"></a>
####10. Hàm arry.slice():

Hàm dùng để lấy 1 số phần tử con trong mảng. Có 2 tham số truyền như sau: slice(start, end).

Trong đó:

- **start**: là vị trí bắt đầu

- **end**: là vị trí kết thúc

```javascript
var mang= ["Học", "lập", "trình", "cơ", "bản"];
var mang_moi = mang.slice(0, 3);
document.write(mang_moi.valueOf());
```
Xem kết quả:

![10](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/10.png)

Còn nếu muốn lấy phần tử từ vị trí nào đó đến cuối mảng thì chỉ truyền 1 tham số end thôi:

```javascript
var mang= ["Học", "lập", "trình", "cơ", "bản"];
var mang_moi = mang.slice(1);
document.write(mang_moi.valueOf());
```

Xem kết quả:

![11](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_11_Cac%20ham%20xu%20li%20mang/image/11.png)


