2025-07-23 18:50
Tags: 

PHP is mainly focused on server-side scripting, so it can do anything any other CGI program can do, such as collect form data, generate dynamic page content, or send and receive cookies. But PHP can do much more.

## Installation

-  Install [[MariaDB]], [[MySQL]] or any other database.  
- Install [[Apache]] and the PHP Apache module, refer to: https://wiki.archlinux.org/title/Apache_HTTP_Server#PHP.
- install [[PHPMyAdmin]] tool as a user-friendly front end for managing the database.

- Alternatively you can just install [[XAMPP]].

## Syntax

- We got `var_dump` function that gives info about given variables, could come in handy for debugging when used with `die`, if you know what i mean.
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
- [variadic functions](https://www.phptutorial.net/php-tutorial/php-variadic-functions/)! you can use `func_get_args()` and `func_num_args()` if you are a masochist, 
- There is an amazing operator called "spaceship operator", looks like this `<=>`, it 

-  Learn PHP Syntax.
-  Learn PHP File Handling.
-  Learn PHP HTTP\Request Handling.
-  Learn PHP State Management.
-  Learn PHP OOP.


# References

- Roadmap: https://roadmap.sh/php