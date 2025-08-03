 Arrays
- arrays in [[PHP]] are like maps, they have key-value pairs. When keys are just the indexes of the values in the array, they are called indexed arrays, else, they are called associative arrays.

- [array_unshift()](https://www.phptutorial.net/php-tutorial/php-array_unshift/) – add one or more elements to the beginning of an array.
- [array_push()](https://www.phptutorial.net/php-tutorial/php-array_push/) – add one or more elements to the end of an array.
- [array_pop()](https://www.phptutorial.net/php-tutorial/php-array_pop/) – remove an element from the end of an array and return it.
- [array_shift()](https://www.phptutorial.net/php-tutorial/php-array_shift/) – remove an element from the beginning of an array and return it.
- [array_keys()](https://www.phptutorial.net/php-tutorial/php-array_keys/) – get the keys of an array.
- [array_key_exists()](https://www.phptutorial.net/php-tutorial/php-array_key_exists/) – check if a key exists in an array.
- [in_array()](https://www.phptutorial.net/php-tutorial/php-in_array/) – check if a value exists in an array.
- [array_reverse()](https://www.phptutorial.net/php-tutorial/php-array_reverse/) – reverse the order of elements in an array.
- [array_merge()](https://www.phptutorial.net/php-tutorial/php-array_merge/) – merge multiple arrays into one.

- `...` is a [spread operator](https://www.phptutorial.net/php-tutorial/php-spread-operator/), which unzips array content inside other arrays.
- [Spread operator](https://www.phptutorial.net/php-tutorial/php-spread-operator/) performs better than the [array_merge()](https://www.phptutorial.net/php-tutorial/php-array_merge/) function because it is a language construct and a function call.
- [[PHP]] allows you to apply the [spread operator](https://www.phptutorial.net/php-tutorial/php-spread-operator/) not only to an array but also to any object that implements the `Traversable` interface. Example:
```php

class RGB implements IteratorAggregate
{
    private $colors = ['red', 'green', 'blue'];

    public function getIterator(): Traversable
    {
        return new ArrayIterator($this->colors);
    }
}

$rgb = new RGB();
$colors = [...$rgb];

print_r($colors);

```
- Generator functions are feasible by just putting `yield` statements in normal functions.
###### Sorting

##### Main Functions
###### [`sort()`](https://www.php.net/manual/en/function.sort.php)

- **Behaviour**: Sorts an array by **values** in ascending order.
- **Key Association**: **Does not preserve keys** (re-indexes numeric keys).
- **Use Case**: Best for indexed arrays where key preservation is not needed.
- **Example**:
```php

$arr = ["banana", "apple", "cherry"];
sort($arr); // ["apple", "banana", "cherry"] (keys reset to 0,1,2)
```

###### [`asort()`](https://www.php.net/manual/en/function.asort.php)

- **Behaviour**: Sorts an array by **values** in ascending order.
- **Key Association**: **Preserves keys**.
- **Use Case**: Sorting associative arrays where you need to maintain keys.
- **Example**:
```php

$arr = ["3" => "banana", "2" => "apple", "1" => "cherry"];
asort($arr); // ["2" => "apple", "3" => "banana", "1" => "cherry"]
```

###### [`ksort()`](https://www.php.net/manual/en/function.ksort.php)

- **Behaviour**: Sorts an array by **keys** in ascending order. 
- **Key Association**: **Maintained**.
- **Use Case**: Sorting associative arrays where you need to maintain keys.
- **Example**:
```php

$arr = ["3" => "banana", "2" => "apple", "1" => "cherry"];
asort($arr); // ["1" => "cherry", "2" => "apple", "3" => "banana"]
```

###### [`natsort()`](https://www.php.net/manual/en/function.natsort.php)
`**

- **Behaviour**: Sorts an array by values using **natural order** (human-friendly, e.g., `img2` before `img10`).
- **Key Association**: **Maintained**. (Indexed arrays indexes 
- Use Case: When sorting strings with numbers (e.g., filenames).
- **Example**:

```php 

$arr = ["img10", "img2", "img1"];
natsort($arr); // ["img1", "img2", "img10"] (keys preserved, [2, 1, 0]) 
```
###### Other Variants

- `rsort()`, `arsort()`, `krsort()`: Reverse-order versions.
- `usort()`, `uasort()`, `uksort()`: Takes user-defined compare function.
- `natcasesort()`: `natsort()` but case-***in***sensitive.