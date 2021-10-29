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

### PHP Quirks
- You can mix html and php logic with
```php 
<?php
if (strpos($SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE){
?>
<h3>strpos() returned a non false value</h3>
<p>Means you are using internet expolorer</p>
<?php
} else {
?>
<h3> not using IE </h3>
<?php
}
?>
```
- To Access Data form html forms
The html form:
```html
<form action="foo.php" method="post">
    Name:  <input type="text" name="username" /><br />
    Email: <input type="text" name="email" /><br />
    <input type="submit" name="submit" value="Submit me!" />
</form>

```
Accessing data
```php
<?php
echo $_POST['username'];
echo $_REQUEST['username'];
?>
```
- Conditional Rendering
```php
<?php if ($expression == true): ?>
	This will show if the expression is true.
<?php else: ?>
	Otherwise this will show.
<php endif; ?>
```
- Type Comparisions
	- https://www.php.net/manual/en/types.comparisons.php

