# Class Notes: Working with Strings
(Repository: _02-basics-03-strings_)

A preliminary introduction to __functions__ and working with strings, including string manipulation.

## Functions
In programming, a __function__ is a block of code that can be called to perform a specific task.

Functions simplify programming by:
1. Avoiding repetitive code in our programs, which could be a nightmare to maintain.
2. Allowing us to use a pre-written function, rather than write the code ourselves (which is a major time-saver).

### Parameters and Arguments
Functions are made useful when they can accept some data type(s), perform some operations on that data, and return a result of those operations. The data that a function can accept are known as its __parameters__ or __arguments__. Technically there is a difference between a _parameter_ and an _argument_, but it's too soon to get into that difference.

## String Functions
String functions can be used to modify a string or give us information about the string. 

### Length of a String
The `length` function gives us the number of characters in the string:
```cpp
string myName = "Andrew";
cout << myName.length() // outputs: 6
```
In this example, `length` was called by using the __dot notation__ (`.`)  on our variable `hthnc`.

#### CHALLENGE: An alternative
`length` is referred to as a __member__ function of a `string` __object__: `length` is a function that can use _dot notation_ (`.`) on a variable declared as a `string`. Beginning with _C++17_ (introduced in 2017), if you wanted to avoid using the `length` _member_ function, you could use a __non-member__ function called `size`:
```cpp
string myName = "Andrew";
cout << size(myName)
```
As you will see later, `size` works on many different types of _objects_ in the `std` __namespace__.

### Accessing Individual Characters
If we have a string:
```cpp
string abc = "ABCDEFGHIJK";
```
we can access a specific `char` in the string using __square bracket notation__, `[]`:
```
cout << abc[0] // outputs: A
cout << abc[1] // outputs: B
```
The square brackets, such as `abc[5]`,  allow us to select a character from the string using a number for its position in the string. Technically, this _position number_ is known as an __index__.

It is really important to note that when counting positions (_indices_), we always start with 0 as the first position (_index_).

### Finding Substrings
A __substring__ is simply a part or portion of a _string_. For example, "ndr" is a _substring_ of "Andrew".

The _position_ of a substring in a string is the position of the substring's first character in the string. The position of "ndr" in "Andrew" is 1 (it is not 2 because we always start counting with 0).

The `find` function can be used to find where specific substrings are located within a string. It has two parameters:
1. The _string_ to search
2. The string _index_ at which to begin the search

To find "ndr" in "Andrew" by searching from the beginning of the string, we could use:
```cpp
string myName = "Andrew";
cout << myName.find("ndr", 0); // outputs: 1
```

When there is more than one __instance__ of a substring that can be found by the `find` function, it only returns the index of the first _instance_. 

#### CHALLENGE: When "find()" can't find...
When `find()` cannot find a matching substring, it returns `std::string::npos`, which represents the largest possible value of `size_t` (typically `-1` when printed as an integer).

`size_t` is an __unsigned integer type__ in C++ that represents the size of objects (in bytes). Its key characteristics are:
- It is __unsigned__: It cannot represent negative values. This is useful when working with sizes since negative sizes don't make sense.
- It is __platform-dependent__: The actual size of `size_t` depends on the system:
  - On 32-bit systems, `size_t` is usually 4 bytes (can represent values from `0` to `4,294,967,295`).
  - On 64-bit systems, `size_t` is usually 8 bytes (can represent values up to `18,446,744,073,709,551,615`).

### Getting Substrings
When we have a string in our program and we only want a portion of it, we can obtain that portion (a __substring__)  by using the `substr()` function.

The `substr()` function takes two _parameters_:
1. The starting _index_.
2. The ending _index_.

Here is an example of its use:
```cpp
string abc = "ABCDEFGHIJK";
cout << abc.substr(3, 5); // outputs: DEF
```

