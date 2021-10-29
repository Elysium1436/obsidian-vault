### Class

```php
class foo
{
	var $foo;
	var $bar;
	
	function __construct()
	{
		$this->foo = 'Foo';
		$this->bar = array('Bar1', 'Bar2', 'Bar3');
	}
}

$foo = new foo();
$name = 'Myname';

echo <<<EOT
My name is "$name". I am printing some $foo->foo.
Now, I am printing some {$foo->bar[1]}.
This should print a capital 'A': \x41
EOT;
```