### Namespaces

Namespaces are way to encapsulate namable stuff. The same way that two foo.txt files can exist in different directories, but no co-exist in the same. It is similar to modules in python.

For example:
```php
namespace Foo\Bar\subnamespace;

const FOO = 1;
function foo() {}
class foo
{
	static function staticmethod() {}
}

```
```php
namespace Foo\Bar;
include 'file1.php'

const FOO = 2;
```