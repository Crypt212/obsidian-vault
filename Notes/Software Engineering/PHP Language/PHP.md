2025-07-23 18:50
Tags: 

PHP is mainly focused on server-side scripting, so it can do anything any other CGI program can do, such as collect form data, generate dynamic page content, or send and receive cookies. But PHP can do much more.

## Installation

-  Install [[MariaDB]], [[MySQL]] or any other database.  
- Install [[Apache]] and the PHP Apache module, refer to: https://wiki.archlinux.org/title/Apache_HTTP_Server#PHP.
- install [[PHPMyAdmin]] tool as a user-friendly front end for managing the database.

- Alternatively you can just install [[XAMPP]].

## Basics

### Types and Functions

- We got `var_dump` function that gives info about given variables, and `print_r` function for printing variables in a formatted way, could come in handy for debugging when used with `die`, if you know what i mean.
- Typecasting in [[PHP]] is just prepend `(type_name)` to a variable to cast it, we go these casting operators:

| Cast Operator               | Conversion                                                       |
| --------------------------- | ---------------------------------------------------------------- |
| (array)                     | [Array](https://www.phptutorial.net/php-tutorial/php-array/)     |
| (bool) or (boolean)         | [Boolean](https://www.phptutorial.net/php-tutorial/php-boolean/) |
| (int) or (integer)          | [Integer](https://www.phptutorial.net/php-tutorial/php-int/)     |
| (object)                    | [Object](https://www.phptutorial.net/php-oop/php-objects/)       |
| (real), (double) or (float) | [Float](https://www.phptutorial.net/php-tutorial/php-float/)     |
| (string)                    | [String](https://www.phptutorial.net/php-tutorial/php-string/)   |
- [[PHP]] is dynamically-typed, so it permits [type juggling](https://www.phptutorial.net/php-tutorial/php-type-juggling/), where [[PHP]] tries to coerce variables types, it shoots type-errors if it can't.
- Fortunately for me there is [type hinting](https://www.phptutorial.net/php-tutorial/php-type-hints/) which enforces types to function parameters and return types.
- [type hinting](https://www.phptutorial.net/php-tutorial/php-type-hints/) allows implicit conversion tho, so there is also [strict mode](https://www.phptutorial.net/php-tutorial/php-strict_types/), which will throw errors if types doesn't match, lovely <3 
- [variadic functions](https://www.phptutorial.net/php-tutorial/php-variadic-functions/)! you can use `func_get_args()` and `func_num_args()` if you are a masochist, but `function f(...args)` is easier to use IMO.

### Arrays
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
#### Sorting

##### [`sort()`](https://www.php.net/manual/en/function.sort.php)

- **Behaviour**: Sorts an array by **values** in ascending order.
- **Key Association**: **Does not preserve keys** (re-indexes numeric keys).
- **Use Case**: Best for indexed arrays where key preservation is not needed.
- **Example**:
```php

$arr = ["banana", "apple", "cherry"];
sort($arr); // ["apple", "banana", "cherry"] (keys reset to 0,1,2)
```

##### [`asort()`](https://www.php.net/manual/en/function.asort.php)
- **Behaviour**: Sorts an array by **values** in ascending order.
- **Key Association**: **Preserves keys**.
- **Use Case**: Sorting associative arrays where you need to maintain keys.
- **Example**:
```php

$arr = ["3" => "banana", "2" => "apple", "1" => "cherry"];
asort($arr); // ["2" => "apple", "3" => "banana", "1" => "cherry"]
```

##### [`ksort()`](https://www.php.net/manual/en/function.ksort.php)
- **Behaviour**: Sorts an array by **keys** in ascending order. 
- **Key Association**: **Preserves keys**.
- **Use Case**: Sorting associative arrays where you need to maintain keys.
- **Example**:
```php

$arr = ["3" => "banana", "2" => "apple", "1" => "cherry"];
asort($arr); // ["2" => "apple", "3" => "banana", "1" => "cherry"]
```
- [`usort()`](https://www.php.net/manual/en/function.usort.php) – sort an array with a user-defined function.

##### Associative array sorting
- [`asort()`](https://www.php.net/manual/en/function.asort.php) – sort an associative array in ascending order, depends on **value**. reverse is `arsort()`.
- [`uasort()`](https://www.php.net/manual/en/function.uasort.php) – sort an associative array with a user-defined comparison function, depends on **value**.

- [`uksort()`](https://www.php.net/manual/en/function.uksort.php) – sort an associative array in using user-defined comparison function, depends on **key**.

- [`natsort()`](https://www.php.net/manual/en/function.natsort.php) - sort an array
- There is an amazing operator called "spaceship operator", looks like this `<=>`, it 

-  Learn PHP Syntax.
-  Learn PHP File Handling.
-  Learn PHP HTTP\Request Handling.
-  Learn PHP State Management.
-  Learn PHP OOP.


# References

- Roadmap: https://roadmap.sh/php