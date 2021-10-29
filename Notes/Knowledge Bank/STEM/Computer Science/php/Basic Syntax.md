

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


