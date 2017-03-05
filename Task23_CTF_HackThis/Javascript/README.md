## HackThis: JAVASCRIPT

> **Category:** Javascript
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/javascript

## Write-up

### Level 1:

- **URL**: https://www.hackthis.co.uk/levels/javascript/1

- **Desciption**:

<p align="center"><img src=""/></p>

- **Solution:**

	+ View source:

	[a]

Ở đây sau khi chỉnh sửa lại thì đoạn code sẽ như sau:

```javascript
<script type='text/javascript'>
    $(function() {
        $('.level-form').submit(function(e) {
            e.preventDefault();
            if (document.getElementById('pass').value == correct) {
                document.location = '?pass=' + correct;
            } else {
                alert('Incorrect password')
            }
        })
    })
</script>
```

- **pass**=correct, tìm được giá trị của `correct`:

`<script type='text/javascript'> var correct = 'jrules' </script>`

- Vậy `pass`= `jrules`

### Level 2:

- **URL**: https://www.hackthis.co.uk/levels/javascript/2

- **Desciption**:

<p align="center"><img src=""/></p>

- **Solution:**

	+ View source:

```
<script type='text/javascript'>
    $(function() {
        $('.level-form').submit(function(e) {
            e.preventDefault();
            if ($('.level-form #pass')[0].value.length == length) {
                document.location = "2?x=" + length;
            } else {
                alert('Incorrect Password');
            }
        });
    });
</script>
```

- Vậy **pass** có độ dài bằng `length`. Dựa vào `Console` tìm được `length` có độ dài bằng 9, vậy chỉ cần nhập 9 kí tự bất kì làm có được password.

[bb]

### Level 3:

- **URL**: https://www.hackthis.co.uk/levels/javascript/2

- **Description**:

- **Solution:**

	+ View source:

```javascript
<script type='text/javascript'>
    var thecode = 'code123';
    $(function() {
        $('.level-form').submit(function(e) {
            e.preventDefault();
            if ($('.level-form #pass')[0].value == thecode) {
                document.location = "?pass=" + thecode;
            } else {
                alert('Incorrect Password');
            }
        });
    });
</script>
```

- `pass`= `thecode`

[cc]

Vậy `pass`= `getinthere`