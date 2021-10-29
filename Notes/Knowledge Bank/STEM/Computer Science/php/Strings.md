### String
- Single quotes have no special characters. You can only escape the ' and backslash character with the backslash. No \\n or \\r
- Heredoc will print whatever is actually in the string
```php
echo <<<END
		a
	   b
	  c
\n
END;
echo <<<END
		a
	   b
	  c
	  END;
	  
//itll print relative to the END word
```
- Closing identifier cannot be further than any lines in the body
- You also cannot mix spaces and tabs.




#### Functions or Methods
- `strpos(string, substr, offset)`: Find position of the first occurance of a string. Returns false if nothing was found.
```php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
    echo 'You are using Internet Explorer.<br />';
}
```
