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