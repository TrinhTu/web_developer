## BÀI 20: CÁC HÀM XỬ LÝ CHUỖI TRONG PHP

> Tài liệu: Các hàm xử lý chuỗi trong php
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/05/2017

### Mục lục:

[1. Quy tắc trong chuỗi](#1)

[2. Các hàm xử lí chuỗi thông dụng](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Quy tắc trong chuỗi:

- Nếu chuỗi được đặt trong dấu nháy kép `""` thì các kí tự nháy kép bên trong chuỗi phải thêm dấu gạch chéo phía trước.

`echo "He says\"I'm 20 years old\" ";`

- Nếu chuỗi được đặt trong dấu nháy kép thì trong chuỗi ta có thể truyền biến vào mà không càn dùng phép nối chuỗi

```
$str = "I'm 20 years old";
echo "He says\"$str\" ";
```

- Nếu chuỗi được đặt trong dấu nháy đơn thì các kí tự nháy đơn bên trong chuỗi phải thêm dấu gạch chéo đằng trước nó

<a name="2"></a>
### 2. Các hàm xử lý chuỗi thông dụng:

- **addcslashes($str,$char_list)**: thêm dấu gạch chéo (\) trước những kí tự trong chuỗi $str được liệt kê ở $char_list

- **addslashes($str)**: Hàm này thêm dấu gạch chéo trước những kí tự (',",\) trong chuỗi $str

- **stripslashes ($str)**: Hàm này ngược với hàm addslashes, nó xóa các ký tự \ trong chuỗi $str.

- **crc32 ( $str )**: chuyển chuỗi $str thành 1 dãy số nguyên (âm dương tùy theo hệ điều hành)

- **explode ( $delimiter , $string)**: chuyển một chuỗi $string thành một mảng các phần tử với ký tự tách mảng là $delimiter.

- **implode($delimiter, $piecesarray);**: Hàm này ngược với hàm explode, nó chuyển một mảng $piecesarray thành chuỗi và mỗi phần tử cách nhau bởi chuỗi $delimiter

- **ord ( $string )**: Hàm này trả về mã ASCII của ký tự đầu tiên trong chuỗi $string

- **strlen($string)**: đếm sô ký tự của chuỗi $string

- **str_word_count($str)**: trả về số từ trong chuỗi $str

- **str_repeat(  $str,  int $n  )**: Lặp chuỗi $str $n lần

- **str_replace( $chuoi_tim, $chuoi_thay_the, $chuoi_nguon )**: tìm kiếm và thay thế chuỗi

- **md5($str)**: Mã hóa chuỗi thành 1 dãy 32 ký tự

- **sha1($string)**: mã hóa chuỗi thành 1 dãy 40 ký tự (mã hóa sha1)

- **htmlentities($str)**: chuyển các thẻ html trong chuỗi $str sang dạng thực thể của chúng

- **html_entity_decode($string)**: Ngược lại với htmlentities, hàm này chuyển ngược các ký tự dạng thực thể HTML sang dạng ký tự của chúng

- **strip_tags( $string, $allow_tags )**: bỏ các thẻ html trong chuỗi $string được khai báo ở $allow_tags

- **substr( $string,  $start, $length )**: lấy chuỗi con nằm trong chuỗi $str bắt đầu từ kí tự $start và chiều dài là $lenght

- **nl2br($string)**: chuyển các kí tự xuống dòng "\n" thành thẻ

- **json_decode($json, $is_array)**: dùng để chuyển chuỗi dạng json sang các đối tượng mảng hoặc object. Nếu $is_array có giá trị false thì hàm sẽ chuyển một chuỗi $json thành một Class (object),  ngược lại nếu $is_array có giá trị true thì sẽ chuyển chuỗi $json thành một mảng.

- **json_encode($array_or_object)**: chuyển 1 mảng hoặc 1 đối tượng (class) sang chuỗi dạng JSON

- **Tham khảo thêm về các hàm xử lí chuỗi [tại đây](http://php.net/manual/en/ref.strings.php)**

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Các hàm xử lý chuỗi trong php. https://freetuts.net/cac-ham-xu-ly-chuoi-trong-php-20.html
