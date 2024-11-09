### Chapter: Operators

Operators are fundamental components of programming languages that perform specific actions on variables or values. In PHP, operators are used to perform various types of operations such as arithmetic, comparison, logical, assignment, increment/decrement, and conditional operations. These operators play a vital role in controlling conditions and manipulating values in PHP.

---

### 1. Arithmetic Operators

Arithmetic operators are used to perform mathematical operations on numbers or values.

- **`+` (Addition)**: Adds two numbers.

  ```php
  $a = 10;
  $b = 5;
  $result = $a + $b; // $result will be 15
  ```

- **`-` (Subtraction)**: Subtracts the second number from the first.

  ```php
  $result = $a - $b; // $result will be 5
  ```

- **`*` (Multiplication)**: Multiplies two numbers.

  ```php
  $result = $a * $b; // $result will be 50
  ```

- **`/` (Division)**: Divides the first number by the second.

  ```php
  $result = $a / $b; // $result will be 2
  ```

- **`%` (Modulus)**: Returns the remainder of dividing the first number by the second.
  ```php
  $result = $a % $b; // $result will be 0, as 10 divided by 5 has no remainder
  ```

---

### 2. Comparison Operators

Comparison operators are used to compare values or variables, returning a Boolean value (true or false).

- **`==` (Equal)**: Checks if two values are equal.

  ```php
  $a = 5;
  $b = "5";
  var_dump($a == $b); // true, as values are equal
  ```

- **`===` (Identical)**: Checks if both the value and type are the same.

  ```php
  var_dump($a === $b); // false, as types differ (integer and string)
  ```

- **`!=` (Not equal)**: Checks if two values are not equal.

  ```php
  var_dump($a != $b); // false, as values are the same
  ```

- **`!==` (Not identical)**: Checks if the value or type is not identical.

  ```php
  var_dump($a !== $b); // true, as types differ
  ```

- **`>` (Greater than)**: Checks if the first value is greater than the second.

  ```php
  var_dump(7 > 5); // true
  ```

- **`<` (Less than)**: Checks if the first value is less than the second.

  ```php
  var_dump(3 < 5); // true
  ```

- **`>=` (Greater than or equal to)**: Checks if the first value is greater than or equal to the second.

  ```php
  var_dump(5 >= 5); // true
  ```

- **`<=` (Less than or equal to)**: Checks if the first value is less than or equal to the second.
  ```php
  var_dump(3 <= 5); // true
  ```

---

### 3. Logical Operators

Logical operators combine multiple conditions or statements to provide a logical result.

- **`&&` (And)**: Returns true if both conditions are true.

  ```php
  $x = 5;
  $y = 10;
  var_dump($x < $y && $y > 7); // true
  ```

- **`||` (Or)**: Returns true if at least one condition is true.

  ```php
  var_dump($x > 5 || $y > 5); // true
  ```

- **`!` (Not)**: Inverts the result of a condition.
  ```php
  var_dump(!($x > $y)); // true, because $x > $y is false
  ```

---

### 4. Assignment Operators

Assignment operators assign values to variables.

- **`=` (Assignment)**: Assigns the value on the right to the variable on the left.

  ```php
  $a = 10;
  ```

- **`+=` (Addition Assignment)**: Adds a value to the current variable's value.

  ```php
  $a += 5; // $a becomes 15
  ```

- **`-=` (Subtraction Assignment)**: Subtracts a value from the current variable's value.

  ```php
  $a -= 3; // $a becomes 12
  ```

- **`*=` (Multiplication Assignment)**: Multiplies the variable's value by a specified number.

  ```php
  $a *= 2; // $a becomes 24
  ```

- **`/=` (Division Assignment)**: Divides the variable's value by a specified number.

  ```php
  $a /= 4; // $a becomes 6
  ```

- **`%=` (Modulus Assignment)**: Sets the variable to the remainder of division by a specified number.
  ```php
  $a %= 5; // $a becomes 1
  ```

---

### 5. Increment and Decrement Operators

These operators are used to increase or decrease a variable's value by one.

- **`++$a` (Pre-increment)**: Increments the variable's value by one and returns the result.

  ```php
  $a = 5;
  echo ++$a; // 6
  ```

- **`$a++` (Post-increment)**: Returns the current value, then increments the variable's value by one.

  ```php
  $a = 5;
  echo $a++; // 5, $a will become 6 afterward
  ```

- **`--$a` (Pre-decrement)**: Decrements the variable's value by one and returns the result.

  ```php
  $a = 5;
  echo --$a; // 4
  ```

- **`$a--` (Post-decrement)**: Returns the current value, then decrements the variable's value by one.
  ```php
  $a = 5;
  echo $a--; // 5, $a will become 4 afterward
  ```

---

### 6. Ternary Operator and Null Coalescing Operator

The ternary and null coalescing operators are shorthand conditional statements.

#### Ternary Operator

The ternary operator is a compact `if-else` statement. Its format is `condition ? value_if_true : value_if_false;`

```php
$age = 18;
$status = ($age >= 18) ? "Adult" : "Minor";
echo $status; // Adult
```

#### Null Coalescing Operator (`??`)

The null coalescing operator provides a default value if a variable is not set or is null.

```php
$username = $_GET['username'] ?? 'Guest';
echo $username; // 'Guest' if 'username' is not set
```

---

### Summary

In this chapter, we explored different types of operators in PHP and how they work. This includes arithmetic, comparison, logical, assignment, increment/decrement, and conditional operators, each with practical examples.
