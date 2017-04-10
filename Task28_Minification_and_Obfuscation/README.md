## MINIFICATION (PROGRAMMING) AND OBFUSCATION (SOFTWARE)

> Tài liệu:  Minification (Programming) and Obfuscation (Software)
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 10/04/2017

### Mục lục: 

- [1. Minification (Programming)](#1)

    + [1.1 Khái niệm](#1.1)

    + [1.2 Nguyên lí](#1.2)

    + [1.3 Công cụ](#1.3)

- [2. Obfuscation (software)](#2)

    + [2.1 Khái niệm](#2.1)

    + [2.2 Nguyên lí](#2.2)

    + [2.3 Công cụ](#2.3)

- [Tài liệu tham khảo](#3)

<a name="1"></a>
### 1. Minification(Programming)

<a name="1.1"></a>
#### 1.1 Khái niệm:

- Minification trong tất cả các ngôn ngữ trong máy tính đặc biệt là trong Javascript là quá trình loại bỏ tất cả các kí tự không cần thiết từ source code mà không làm thay đổi chức năng của nó. Các kí tự không cần thiết bao gồm: kí tự khoảng trắng, kí tự dòng mới, nhận xét và 1 vài kí tự phân cách giúp cho văn bản trở nên dễ đọc nhưng không cần thiết.

<a name="1.2"></a>
#### 1.2 Nguyên lí:

- Minified source code đặc biệt hữu ích cho các ngôn ngữ giải thích được triển khai và chuyển giao trên Internet (ví dụ như Javascript), bởi nó giảm thiểu tối đa dữ liệu cần để để chuyển. Minified source code có thể được sử dụng như **obfuscation**, mặc dù obfuscation có được sử dụng phân biệt như 1 dạng mật mã trong khi 1 minified code có thể bị đảo ngược bằng cách sử dụng 1 pretty- printer. Trong lập trình, mục đích Minified source code là mục đích giảm thiểu mã nguồn cực nhỏ. 

- Minification có thể được phân biệt với khái niệm tổng quát về nén dữ liệu, trong Minified source có  thể giải thích lập tức mà không cần bước giải thích, cùng 1 thông dịch viên có thể làm việc với bản gốc cũng như với minified source.

- **Ví dụ:** Cho đoạn javascript:

```javascript
var a = [];
for (var i = 0; i< 20; i++){
    a[i] = i;
}
```

Đoạn code trên tương đương với đoạn code sau:

```javascript
for(var a =[i=0]; ++i<20;a[i]=i);
```

- **Source mapping**: cho phép các công cụ hiển thị mã không mã hóa từ mã minified với 1 bản đồ tối ưu hóa giữa chúng.

#### Giảm thiểu tài nguyên (HTML, CSS và Javascript):

Quy tắc này được áp dụng khi PageSpeed Insights phát hiện ra kích thước của nguồn của bạn có thể được giảm xuống thông qua Minificaion.

- Tổng quan: 

    + Minification đề cập đến quá trình loại bỏ dữ liệu không cần thiết hoặc dữ liệu dư thừa mà không làm ảnh hưởng đến quá trình xử lí tài nguyên của trình duyệt - bình luận code, định dạng loại bỏ code chưa sử dụng đến, sử dụng các tên biến và chức năng ngắn hơn.

<a name="1.3"></a>
#### 1.3 Công cụ:

- Javascript: [JSbeautifier](http://jsbeautifier.org/) đây là công cụ có tác dụng làm đẹp các đoạn code. [Closure Compiler](https://developers.google.com/closure/compiler/?hl=vi) - đây là công cụ để tải các đoạn Javascript chạy nhanh hơn, kiểm tra cú pháp, cảnh báo về các lỗi Javascript phổ biến, giảm thiểu kích thước tệp và giảm băng thông. [Uglify-js2](https://github.com/mishoo/UglifyJS2) là bộ công cụ phân tích cú pháp, bộ lọc, bộ nén và làm đẹp Javascript.

- HTML: [HTML Minifier](http://minifycode.com/html-minifier/) - đây là công cụ giúp giảm thiểu các đoạn code trong HTML

- CSS: [CSS Nano](https://github.com/ben-eb/cssnano), [csso](https://github.com/css/csso)

<a name="2"></a>
### 2. Obfuscation (software):

<a name="2.1"></a>
#### 2.1 Khái niệm:

- Trong phát triển phần mềm, làm rối code bằng tay là hành động có chủ ý làm rối loạn code gây khó khăn cho người đọc. Giống như obfuscation trong ngôn ngữ tự nhiên, nó sử dụng các biểu thức không cần thiết để thể hiện. Các lập trình viên có thể cố tình làm xáo trộn mã để che dấu mục đích mục đích hay tính logic của nó.

- Thêm vào đó, công cụ `obfuscators` còn cung cấp làm rối loạn tự động để biên dịch ứng dụng làm cho kĩ thuật dịch ngược trở nên khó khăn cho người và máy móc, nhưng bên cạnh đó nó không làm biến đổi trạng thái của ứng dụng bị xáo trộn.

- Kiến trúc và đặc điểm của 1 số ngôn ngữ khiến chúng dễ bị là rối hơn các ngôn ngữ khác: C, C++ và Perl là một số ngôn ngữ dễ bị làm rối.

<a name="2.2"></a>
#### 2.2 Nguyên lí:

- Kĩ thuật này làm thay đổi tên hàm tên lớp, tên biến... hoặc chia nhỏ mã nguồn thành những đoạn code khó đọc. Một số thứ không thể thay đổi: keyword, cấu trúc câu lệnh của ngôn ngữ lập trình, những thứ có thể thay đổi là những thứ tự viết ra và đặt tên riêng.

- **Một số lưu ý khi viết Obfuscation**:

    + Chỉ thay đổi những tên riêng, không thay đổi từ khóa, tên lệnh, hay các API của hệ thống, tránh xung đột tên

    + Nhất quán: khi thay đổi tên phải thay đổi toàn bộ file nguồn có chứa cùng đối tượng đó; đặt tên càng ngắn càng tốt để quá trình dịch mã nhanh hơn, loại bỏ dư thừa. 

- **Recreational Obfuscation:**

    - Các kiểu làm rối bao gồm thay đổi các từ khóa đơn giản, sử dụng và không sử dụng khoảng trắng để tạo ra các chương trình nghệ thuật và tự tạo

- **Ưu điểm của Obfuscation**: 

    - 1 số ưu điểm của làm rối code tự động là làm nó phổ biến và được sử dụng hữu ích và rộng rãi trên nhiều diễn đàn. Trên 1 vài diễn đàn (ví dụ như Java, Androi và NET) có công cụ miễn phí gọi là **decompiler** có thể dễ dàng đảo ngược mã nguồn. Ưu điểm chính của làm rối code tự động là giúp bảo vệ bí mật thương mại (sở hữu trí tuệ) chứa trong các phần mềm bằng cách dịch ngược chương trình, gây khó khăn và không khả thi. Một vài ưu điểm khác là giúp bảo vệ tránh truy cập trái phép và thu nhỏ kích thước của file.

- **Nhược điểm của Obfuscation**:

    - Trong khi làm rối code giúp đọc, viết và dịch ngược chương trình khó khăn và chi phối thời gian. Một vài phần mềm anti-virus chẳng hạn như AVG sẽ cảnh báo người dùng khi họ truy cập vào 1 trang web bị làm rối bằng tay, đây chính là 1 trong những mục đích của làm rối có thể che dấu các mã độc. Tuy nhiên, 1 vài nhà phát triển có thể làm rối code nhằm giảm kích thước file và tăng cường bảo mật. 

<a name="2.3"></a>
#### 2.3 Công cụ:

- Javascript: [Javascript Obfuscator](https://www.daftlogic.com/projects-online-javascript-obfuscator.htm) - Đây là công cụ làm rối loạn code che dấu được code và giảm kích thước tệp --> tiết kiệm được băng thông. 

<a nam="3"></a>
### Tài liệu tham khảo:

> [1] Minification_(programming). https://en.wikipedia.org/wiki/Minification_(programming)
> 
> [2] Obfuscation_(software). https://en.wikipedia.org/wiki/Obfuscation_(software)
> 
> [3] Minify Resources. https://developers.google.com/speed/docs/insights/MinifyResources?hl=vi
>
> [4] Projects online javascript obfuscator. https://developers.google.com/speed/docs/insights/MinifyResources?hl=vi
> 
> [5] Che dấu và làm gọn mã nguồn. http://blogthienbao.blogspot.com/2010/10/che-dau-va-lam-gon-ma-nguon.html
>
> [6] Tool to unminify decompress javascript. http://stackoverflow.com/questions/822119/tool-to-unminify-decompress-javascript


