## BÀI 43: HÀM XỬ LÝ NGÀY THÁNG (DATE) TRONG JAVASCRIP

> Tài liệu: Hàm xử lý ngày tháng (Date) trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 07/04/2017

### Mục lục: 

- [1. Các hàm nhóm Date Get trong Javascript](#1)

- [2. Các hàm nhóm Date Set trong Javascript](#2)

- [3. Tạo đồng hồ online bằng Javascript](#3)

	+ [3.1 Hàm checkTime()](#3.1)

	+ [3.2 Hàm startTime()](#3.2)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Các hàm nhóm Date Get trong Javascript:

- Trong Javascript có 10 hàm thiết lập thời gian thông dụng:

	+ getDate(): lấy ngày (1-31)

	+ getDay(): lấy ngày trong tuần (0-6)

	+ getFullYear(): lấy năm đầy đủ (YYYY)

	+ getYear(): lấy năm 2 số cuối (YY)

	+ getHours(): lấy số giờ (0 - 23)

	+ getMiliSeconds(): lấy số mili giây (0 - 999)

	+ getMinutes(): lấy số phút (0 - 59)

	+ getMonth(): lấy tháng (0 - 11)

	+ getSeconds(): lấy số giây (0 - 59)

	+ getTime(): thời gian đã được convert sang dạng miliseconds.

- Khi muốn sử dụng hàm nào chỉ việc gọi hàm đó ra sử dụng.

**Ví dụ:**

```javascript
// Đối tượng thời gian hiện tại
var d = new Date();
 
d.getDate();
d.getDay();
d.getFullYear();
d.getYear();
d.getHours();
d.getMilliseconds();
d.getMinutes();
d.getMonth();
d.getSeconds();
d.getTime();
```

- Riêng đối với hàm getDay() để có kết quả chính xác phải cộng lên 1 vì nó tính từ 0.

<a name="2"></a>
### 2. Các hàm nhóm Date Set trong Javascript:

- Tương ứng với mỗi hàm **Date Get** thì sẽ có 1 hàm **Date Set** (trừ hàm `getDay()`)

	
    + setDate() thiết lập ngày (1 - 31)

    + setFullYear() thiết lập năm đầy đủ (YYYY)

    + setYear() thiết lậpnăm 2 số cuối (YY)

    + setHours() thiết lập số giờ (0 - 23)

    + setMiliSeconds() thiết lập số mili giây (0 - 999)

    + setMinutes() thiết lập số phút (0 - 59)

    + setMonth() thiết lập tháng (0 - 11)

    + setSeconds() thiết lập số giây (0 - 59)

    + setTime() thiết lập thời gian đã được convert sang dạng miliseconds.

- Vì đây là hàm **set** nên phải truyền tham số vào, các hàm có ảnh hưởng lẫn nhau vậy nên nếu thiết lập ngày giờ không đúng thì nó sẽ lấy ngày giờ mặc định

- Nếu dùng hàm `setTime()` để thiết lập thì nó ảnh hưởng tới tất cả các giá trị còn lại bởi `setTime()` là hàm thiết lập thời gian đầy đủ đã chuyển sang dạng miniseconds.

**Ví dụ:**

```javascript
// Đối tượng thời gian hiện tại
var d = new Date();
 
d.setDate(20);
d.setFullYear(2011);
d.setHours(2);
d.setMilliseconds(2);
d.setMinutes(3);
d.setMonth(4);
d.setSeconds(5);
```

<a name="2.1"><
### 3. Tạo đồng hồ online bằng Javascript:

- Trước hết cần tạo file `index.html` với nội dung như sau:

```javascript
<!DOCTYPE html>
<html>
    <head>
        <script>
          // Hàm khởi tạo đồng hồ
          function startTime()
          {
               
          }
           
          // Hàm này có tác dụng chuyển những số bé hơn 10 thành dạng 01, 02, 03, ...
          function checkTime(i)
          {
               
          }
        </script>
    </head>
    <body onload="startTime()">
 
        <div id="timer"></div>
 
    </body>
</html>
```

- Trong đó: 

	+ `div#result`: dùng để hiển thị đồng hồ

	+ Thẻ `body` có sự kiện `onload="startTime()"` dùng để chạy đồng hồ khi website được load lên.

	+ Hàm `startTime()` để tạo đồng hồ và hàm `checkTime()` để chuyển đổi định dạng những con số sang dạng 01, 02, 03...

<a name="3.1"></a>
#### 3.1 Hàm checkTime():

- Hàm này có tác dụng chuyển những con số bé hơn 10 thành dạng 01,02,03...

```javascript
function checkTime(i) 
{
    if (i < 10) {
        i = "0" + i;
    }
    return i;
}
```

<a name="3.2"></a>
#### 3.2 Hàm startTime():

- Hàm này có tác dụng khởi tạo đồng hồ

```javascript
function startTime() 
{
    // Lấy Object ngày hiện tại
    var today = new Date();
 
    // Giờ, phút, giây hiện tại
    var h = today.getHours();
    var m = today.getMinutes();
    var s = today.getSeconds();
 
    // Chuyển đổi sang dạng 01, 02, 03
    m = checkTime(m);
    s = checkTime(s);
 
    // Ghi ra trình duyệt
    document.getElementById('timer').innerHTML = h + ":" + m + ":" + s;
 
    // Dùng hàm setTimeout để thiết lập gọi lại 0.5 giây / lần
    var t = setTimeout(function() {
        startTime();
    }, 500);
}
```

- Đối với cách này chỉ lấy được thời gian trên máy client chứ không thể lấy được thời gian từ hệ thống server phải thông qua PHP đồng thời dùng hàm `setTime()` để tăng giờ phút giây... chứ không phải lấy trực tiếp.

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Hàm xử lý ngày tháng trong javascript. https://freetuts.net/ham-xu-ly-ngay-thang-date-trong-javascript-400.html