PHP is mainly focused on server-side scripting, so it can do anything any other CGI program can do, such as collect form data, generate dynamic page content, or send and receive cookies. But PHP can do much more.
# Installation

- Install [[MariaDB]], [[MySQL]] or any other database.  
- Install [[Apache]] and the PHP Apache module, refer to: https://wiki.archlinux.org/title/Apache_HTTP_Server#PHP.
- install [[PHPMyAdmin]] tool as a user-friendly front end for managing the database.

- Alternatively you can just install [[XAMPP]].

# Basics

## Variables

- Variables are defined and used using `$`, for example: `$cat_name = "kitty"`.
- When assigning variables to variables, they are passed by value, to pass by reference use `&` before the referenced variable.
- **Variable Variables**! Happens when you take the value of a variable as a name for a new variable, like this: `$$cat_name = "ahmed";` which is same as `$kitty = "ahmed";`, crazy!

## Constants

- Constants are defined **at run-time** using `define(name, value, casesensitive [deprecated])` function, they are used without the `$`.
- To check if a constant has been defined, use `defined(name)` which returns boolean.
- Constants are defined **at compile-time** using `const` function, they are used without the `$`, example: `const MESSAGE = 'hello'`.

- Differences between defining constant in run-time or compile-time:
	- constants defined in run-time can't be defined inside control blocks, like `if` for example.
	- run-time constant can be named dynamically, since their names are string values that could come from variables, same goes for the constant value.
	- 

## Printing

- There are some functions for printing variables, info about them and more.
- echo function is used like this `echo $cat_name;`, it's not an expression, so can't use it in other expressions.
- print function is used like echo, but it is an expression, and it returns 1.
- We got `var_dump` function that gives info about given variables
- `print_r` function for printing variables in a formatted way, could come in handy for debugging when used with `die`.
## Commenting

- Single line using `#` or `//`, multiline using `/* ... */`.


## Types

- To check the type, use `gettype(variable)` function.
- Typecasting in [[PHP]] is just prepend `(type_name)` to a variable to cast it, we go these casting operators:

| Cast Operator               | Conversion                                                       |
| --------------------------- | ---------------------------------------------------------------- |
| (array)                     | [Array](https://www.phptutorial.net/php-tutorial/php-array/)     |
| (bool) or (boolean)         | [Boolean](https://www.phptutorial.net/php-tutorial/php-boolean/) |
| (int) or (integer)          | [Integer](https://www.phptutorial.net/php-tutorial/php-int/)     |
| (object)                    | [Object](https://www.phptutorial.net/php-oop/php-objects/)       |
| (real), (double) or (float) | [Float](https://www.phptutorial.net/php-tutorial/php-float/)     |
| (string)                    | [String](https://www.phptutorial.net/php-tutorial/php-string/)   |
- [[PHP]] is dynamically-typed, so it permits ***type juggling***, where [[PHP]] tries to coerce variables types, it shoots type-errors if it can't.
- Fortunately for me there is ***type hinting*** which enforces types to function parameters and return types.
- ***type hinting*** allows implicit conversion tho, so there is also ***strict mode***, which will throw errors if types doesn't match, lovely <3 

## Scalar Types
-  [[Boolean]] (`bool`)
- [[Integer]] (`int`)
- [[Float]] (`float`)
- [[String]] (`string`)
### Compound Types
- [[MindMap/Software Engineering/Languages/PHP/Arrays|Arrays]]
- [[Objects]]
- [[Callable]]
- [[Iterators]]

## Special Types
- [[Resource]]
- [[null]]


## Functions
- functions has *local scopes*, can't access outsider variables.
- parameters are passed by value by default, to pass by reference, prefix an `&`.

### Function Types

#### `Callable`
- Anything that can be called as a function, this includes:

	- **Named Functions**: Any string variable holding name of a function as a string.	
	- **Static Class Methods**: Any string holding method name like `ClassName::Method` or array containing class name as a first element, and method name in that class as the second element.
	- **Object Methods**: Same as static class methods but with object name instead of class name.
	- **Anonymous Functions (Closure objects)**: Functions that can be assigned to variables.
	- **Invokable Objects**: Objects that has `__invoke()` method.

- To check if something is callable, pass it to `is_callable()`.

#### `Closure`
- 
	- 
- ***variadic functions***! you can use `func_get_args()` and `func_num_args()` if you are a masochist, but `function f(...args)` is easier to use IMO.
- [[PHP]] has anonymous functions!


### ***anonymous functions***
- functions that doesn't have an name.
- its body block needs to end with a *semicolon*; since it's an expression.
- can be assigned to variables.
- can access outsider variables, by adding those variables to ***`use`*** expression, works exactly like passing parameters to the function.
# Date
- date in PHP is 