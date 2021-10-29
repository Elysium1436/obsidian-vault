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


#### Iteration 
- Use the `foreach` syntax.
```php
foreach($array as $i => $value){
	//Do something... You can use the value of $i and $value
	//In each iteration.
}

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
- Assigning a value to the `[]` index will append listwise, incrementing the largest integer index
```php
$arr = array(5=>1, 12=>2);
$arr[] = "something" //Equivalent to $arr[13]="something"
```
- To delete an element, use the `unset`.
```php
unset($arr[5]) //deletes element with key 5
unset($arr) //deletes the whole thing
```
