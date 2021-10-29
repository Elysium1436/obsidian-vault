### Logic
- If Statements:
	```
	if(bool){
		//code...
	}
	```

### String
- `strpos(string, substr, offset)`: Find position of the first occurance of a string. Returns false if nothing was found.
```php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
    echo 'You are using Internet Explorer.<br />';
}
```
