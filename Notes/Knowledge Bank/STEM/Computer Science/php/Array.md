### Array
Arrays are actually a mixed of arrays, maps, list, hash table, dictionary, collection, stack, queue, etc.

- Dictionary 
```php
$dicionary = array(
	"foo" => "bar",
	"bar" => "foo"
);
// Using the short array syntax
$array = [
    "foo" => "bar",
    "bar" => "foo",
];
```
- Array
```php
$array = ["one", "two", "three"];
echo "{$array[0]}";
```
- Nested array elements
```php
$array = array(
    "foo" => "bar",
    42    => 24,
    "multi" => array(
         "dimensional" => array(
             "array" => "foo"
         )
    )
);
```





#### Quirks
```php
$array = array(
    1    => 'a',
    '1'  => 'b', // the value "a" will be overwritten by "b"
    1.5  => 'c', // the value "b" will be overwritten by "c"
    -1 => 'd',
    '01'  => 'e', // as this is not an integer string it will NOT override the key for 1
    '1.5' => 'f', // as this is not an integer string it will NOT override the key for 1
    true => 'g', // the value "c" will be overwritten by "g"
    false => 'h',
    '' => 'i',
    null => 'j', // the value "i" will be overwritten by "j"
    'k', // value "k" is assigned the key 2. This is because the largest integer key before that was 1
    2 => 'l', // the value "k" will be overwritten by "l"
);

var_dump($array);
```