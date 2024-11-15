## Chapter: Searching Functions in PHP

PHP offers a variety of functions to efficiently search and retrieve data from arrays. These searching functions allow you to locate specific values or keys, check for their existence, and retrieve collections of keys or values based on certain criteria. By mastering these functions, you’ll be able to quickly search and manipulate array data within your PHP applications.

---

### 1. `in_array()`: Checks if a Value Exists in an Array

The `in_array()` function searches for a specific value within an array and returns `true` if it finds the value, or `false` if it doesn’t. This function is particularly useful when you need to check if an array contains a particular value before performing further operations.

**Syntax:**

```php
in_array(mixed $needle, array $haystack, bool $strict = false): bool
```

- **$needle**: The value you’re searching for.
- **$haystack**: The array to search within.
- **$strict**: Optional. If set to `true`, `in_array()` will also check the type of the value.

**Example:**

```php
$colors = ["red", "green", "blue"];
if (in_array("green", $colors)) {
    echo "Green is in the array.";
} else {
    echo "Green is not in the array.";
}
// Output: Green is in the array.
```

With the `strict` parameter set to `true`, `in_array()` will only return `true` if both the value and type match.

**Example with `strict` parameter:**

```php
$numbers = [1, 2, "3"];
var_dump(in_array(3, $numbers, true));  // Output: bool(false)
var_dump(in_array(3, $numbers, false)); // Output: bool(true)
```

Use `in_array()` when you need to confirm the presence of a specific value in an array.

---

### 2. `array_search()`: Finds the First Key of a Specified Value

The `array_search()` function searches for a value within an array and returns the first key that holds that value. If the value is not found, `array_search()` will return `false`. You can optionally use the `strict` parameter to ensure that the search matches both value and type.

**Syntax:**

```php
array_search(mixed $needle, array $haystack, bool $strict = false): int|string|false
```

- **$needle**: The value to search for.
- **$haystack**: The array to search in.
- **$strict**: Optional. If set to `true`, `array_search()` will only return the key if both value and type match.

**Example:**

```php
$fruits = ["a" => "apple", "b" => "banana", "c" => "cherry"];
$key = array_search("banana", $fruits);
echo $key;
// Output: b
```

`array_search()` is particularly useful when you need to locate the key of a specific value in an associative array. If `strict` is enabled, it will only return the key if there’s a strict match.

**Example with `strict` parameter:**

```php
$values = ["1", 2, 3];
$key = array_search(1, $values, true);  // Output: false (no strict match for integer 1)
```

---

### 3. `array_key_exists()`: Checks if a Specified Key Exists in an Array

`array_key_exists()` checks whether a specific key or index exists within an array. It returns `true` if the key exists and `false` if it doesn’t. This function works with both indexed and associative arrays and is often used to verify the presence of a key before attempting to access its value.

**Syntax:**

```php
array_key_exists(mixed $key, array $array): bool
```

- **$key**: The key to search for.
- **$array**: The array to search in.

**Example:**

```php
$person = ["name" => "John", "age" => 30];
if (array_key_exists("age", $person)) {
    echo "Age is a key in the array.";
} else {
    echo "Age is not a key in the array.";
}
// Output: Age is a key in the array.
```

Use `array_key_exists()` when you want to check for the presence of a specific key in an array, especially if you’re dealing with associative arrays.

---

### 4. `array_keys()`: Returns All Keys of an Array

The `array_keys()` function retrieves all keys from an array and returns them as a new array. This function is particularly useful when you need to obtain a list of all keys, for example, to iterate over or inspect them.

**Syntax:**

```php
array_keys(array $array, mixed $search_value = null, bool $strict = false): array
```

- **$array**: The array from which to retrieve the keys.
- **$search_value**: Optional. If specified, only keys associated with this value are returned.
- **$strict**: Optional. If `true`, `array_keys()` will perform a strict comparison (type and value).

**Example:**

```php
$animal_ages = ["cat" => 3, "dog" => 7, "bird" => 2];
$keys = array_keys($animal_ages);
print_r($keys);
// Output: Array ( [0] => cat [1] => dog [2] => bird )
```

Using the `search_value` and `strict` parameters, you can also retrieve keys associated with a specific value.

**Example with `search_value`:**

```php
$grades = ["Alice" => "A", "Bob" => "B", "Charlie" => "A"];
$keys = array_keys($grades, "A");
print_r($keys);
// Output: Array ( [0] => Alice [1] => Charlie )
```

---

### 5. `array_values()`: Returns All Values of an Array

The `array_values()` function returns all values from an array as a new indexed array. Unlike `array_keys()`, which provides only the keys, `array_values()` retrieves only the values, ignoring the keys.

**Syntax:**

```php
array_values(array $array): array
```

- **$array**: The array from which to retrieve the values.

**Example:**

```php
$fruit_colors = ["apple" => "red", "banana" => "yellow", "cherry" => "red"];
$values = array_values($fruit_colors);
print_r($values);
// Output: Array ( [0] => red [1] => yellow [2] => red )
```

`array_values()` is helpful when you only need the values, regardless of their associated keys. It’s commonly used to reset the array indices for associative arrays, as it returns the values in a new indexed array.

---

### Summary

These PHP searching functions offer powerful tools for identifying and retrieving specific data within arrays. From checking the presence of values with `in_array()` to retrieving only keys with `array_keys()`, each function serves a unique purpose, making it easier to navigate, verify, and access data in arrays. Understanding how to leverage these functions will enhance your ability to manipulate arrays effectively in PHP applications.
