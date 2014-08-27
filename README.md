#Simple JS validation

Needs jQuery library

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
<input type="text" data-validates="presence|max:10" name="name" /> presence|max:10
<input type="text" data-validates="min:18|max:100" name="age" /> min:18|max:100
<input type="text" data-validates="presence|min:3" name="name" /> presence|min:10
<input type="text" data-validates="minlength:3|maxlength:20" name="surname" /> minlength:3|maxlength:20
<input type="text" data-validates="int" name="sum" /> int
<input type="text" data-validates="float" name="money" /> float
<input type="text" data-validates="alpha" name="bla" /> alpha
<input type="text" data-validates="regexp:^([0-9]+)$" name="bla" /> regexp
<input type="text" data-validates="email" name="email" /> email
<input type="text" data-validates="ip" name="ip" /> ip
<textarea name="content" data-validates="presence"></textarea>presence
```

And use this script:
```javascript
$('#form').validates({
    error: function(err_field) {
        $(err_field).addClass('error');
    },
    ok: function (ok_field) {
        $(ok_field).removeClass('error');   
    }
});
```

