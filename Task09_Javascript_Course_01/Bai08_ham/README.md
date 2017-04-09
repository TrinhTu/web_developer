## Bài 8: Hàm vào tạo hàm (function) trong javascript

> Tài liệu: Hàm và tạo hàm (function) 
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/11/2016

### Mục lục:

[1. Định nghĩa hàm (function)](#1)

[2. Hàm có return và hàm không có return](#2)

[3. Ví dụ tạo hàm trong javascript](#3)

### Nội dung:

Hàm là phương pháp lập trình truyền thống thường đc ứng dụng trong các phương pháp lập trình thủ tục lập trình hướng module...

<a name="1"></a>
#### 1. Định nghĩa hàm (function) trong javascript:

Là sẽ gom một số đoạn code vào một khối xử lý và khi cần thì gọi ra dùng. Cú pháp tạo hàm trong javascript là:

```
function name_of_function(var1, var2,...)
{
// some code
}
```
 
 Trong đó:

 - function: là từ khóa bắt buộc 

- name_of_function: là tên của function, thông thường chúng ta tạo những tên có ý nghĩa như find_max, find_min, ...

- var1, var2 var3, ... là các tham số truyền vào hàm. 

Ví dụ: Kiểm tra tính chẳn lẽ của 5 số:

```
function text_number(i)
{
	if(i%2==0){
		alert(i + 'là số chẳn');
	}
	else{
		alert(i + 'là số lẻ');
	}
}
text_number(1);
text_number(3);
text_number(6);
text_number(8);
text_number(5);
```

<a name="2"></a>
#### 2. Hàm có return và hàm không có return:

Hàm có return là hàm có sử dụng từ khóa return để đặt ở cuối hàm mục đích trả kết quả về để sử dụng tiếp ở những đoạn code bên ngoài.  Ví dụ ta cần viết một hàm tính tổng của hai số a và b thì hàm này phải trả về giá trị là tổng của hai số a, b.

```
// Khai báo hàm
function tinh_tong(a, b)
{
    // trả về kết quả là a + b
    return a + b;
}
 
// Sử dụng
var so1 = 1;
var so2 = 2;
 
// truyền so1 và so2 vào hàm
var ketqua = tinh_tong(so1, so2);
 
alert( 'Tổng của 2 số là:' + ketqua);
```

![a](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai08_ham/image/(a).png)

- Hàm không có return là hàm không sử dụng từ khóa return đặt trong hàm. Ví dụ: viết chương trình tính tổng 2 số a,b:

```
function tong(a,b)
{
	document.write('Tổng là' + (a+b));
}
var so_1= 5;
var so_2=10;
tong(so_1, so_2);
```
![b](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai08_ham/image/(b).png)

<a name="3"></a>
#### 3. Ví dụ tạo hàm trong javascript:

Viết chương trình kiểm tra năm đó có phải là năm nhuận không.

```
function kiem_tra_nam_nhuan(nam)
{
    if (nam % 100 == 0)
    {
        if (nam % 400 == 0){
            alert(nam + ' là năm nhuận');
        }
        else { 
            alert(nam + ' không phải năm nhuận');
        }
    }
    else if (nam % 4 == 0){ 
        alert(nam + ' là năm nhuận');
    }
    else { 
        alert(nam + 'không phải là năm nhuận');
    }
}
kiem_tra_nam_nhuan(2016);
```

![c](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai08_ham/image/(c).png)
