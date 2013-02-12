#Simple JS validation
##Tests

- presence
- minlength
- maxlength
- min (numeric)
- max (numeric)
- float
- alpha
- ip (ip address)
- email
- regexp

##Examples
Insert into html-tag like text, textarea or file data-validates:

```html
        <input type="text" data-validates="presence|max:10" name="name" /> presence|max:10<br />
        <input type="text" data-validates="min:18|max:100" name="age" /> min:18|max:100<br />
        <input type="text" data-validates="minlength:3|maxlength:20" name="surname" /> minlength:3|maxlength:20<br />
        <input type="text" data-validates="int" name="sum" /> int<br />
        <input type="text" data-validates="float" name="money" /> float<br />
        <input type="text" data-validates="alpha" name="bla" /> alpha<br />
        <input type="text" data-validates="regexp:^([0-9]+)$" name="bla" /> regexp<br />
        <input type="text" data-validates="email" name="email" /> email<br />
        <input type="text" data-validates="ip" name="ip" /> ip<br />
        <textarea name="content" data-validates="presence"></textarea>presence<br />

```

And use this script:
```javascript
    $('#form').validates({
        error: function(err_field) {
            $(err_field).addClass('error'); // Can be customized
        },
        ok: function (ok_field) {
            $(ok_field).removeClass('error');   
        }
    });
```

##Needs jQuery library
