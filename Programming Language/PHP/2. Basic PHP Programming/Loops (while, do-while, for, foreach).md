### Chapter: Loops in PHP

Loops are fundamental constructs in programming that allow repeated execution of a block of code as long as a specified condition is true. PHP offers various types of loops: `while`, `do-while`, `for`, and `foreach`. Each type of loop serves specific use cases depending on the situation, and knowing how to use them efficiently helps control code flow and manage repetitive tasks easily. Let's explore each type of loop in detail, with syntax, examples, and all possible variations.

---

### 1. `while` Loop

The `while` loop executes a block of code as long as a specified condition remains true. It checks the condition before each iteration, so if the condition is false initially, the loop will not execute at all.

#### Syntax:

```php
while (condition) {
    // Code to be executed
}
```

#### Example:

```php
$count = 1;
while ($count <= 5) {
    echo "Count: $count <br>";
    $count++;
}
// Output: Count from 1 to 5
```

#### Alternative Syntax:

PHP also allows an alternative syntax with `while:` and `endwhile;` for cleaner code, especially in templates or control structures within HTML.

```php
$count = 1;
while ($count <= 5):
    echo "Count: $count <br>";
    $count++;
endwhile;
```

---

### 2. `do-while` Loop

The `do-while` loop is similar to `while`, but it checks the condition after each iteration. Therefore, the block of code will execute at least once, even if the condition is false initially.

#### Syntax:

```php
do {
    // Code to be executed
} while (condition);
```

#### Example:

```php
$count = 6;
do {
    echo "Count: $count <br>";
    $count++;
} while ($count <= 5);
// Output: Count: 6 (executes once)
```

---

### 3. `for` Loop

The `for` loop is ideal when the number of iterations is known in advance. It contains three parts: initialization, condition, and increment/decrement.

#### Syntax:

```php
for (initialization; condition; increment/decrement) {
    // Code to be executed
}
```

#### Example:

```php
for ($i = 1; $i <= 5; $i++) {
    echo "Iteration: $i <br>";
}
// Output: Iteration from 1 to 5
```

#### Alternative Syntax:

For template-like structures, PHP provides an alternative syntax with `for:` and `endfor;`.

```php
for ($i = 1; $i <= 5; $i++):
    echo "Iteration: $i <br>";
endfor;
```

---

### 4. `foreach` Loop

The `foreach` loop is specifically designed for iterating over arrays, making it easier to access each element directly.

#### Syntax (Indexed Array):

```php
foreach ($array as $value) {
    // Code to be executed
}
```

#### Example (Indexed Array):

```php
$numbers = [1, 2, 3, 4, 5];
foreach ($numbers as $number) {
    echo "Number: $number <br>";
}
// Output: Number from 1 to 5
```

#### Syntax (Associative Array):

```php
foreach ($array as $key => $value) {
    // Code to be executed
}
```

#### Example (Associative Array):

```php
$person = ["name" => "Alice", "age" => 25];
foreach ($person as $key => $value) {
    echo "$key: $value <br>";
}
// Output: name: Alice and age: 25
```

#### Alternative Syntax:

For cleaner code with HTML templates, `foreach:` and `endforeach;` are alternative syntax options.

```php
foreach ($numbers as $number):
    echo "Number: $number <br>";
endforeach;
```

---

### 5. `break` and `continue` Statements

The `break` statement terminates a loop entirely, whereas `continue` skips the current iteration and moves to the next.

#### Using `break`:

```php
for ($i = 1; $i <= 5; $i++) {
    if ($i == 3) {
        break; // Exit the loop when $i is 3
    }
    echo "Iteration: $i <br>";
}
// Output: Iteration 1 and 2 only
```

#### Using `continue`:

```php
for ($i = 1; $i <= 5; $i++) {
    if ($i == 3) {
        continue; // Skip iteration when $i is 3
    }
    echo "Iteration: $i <br>";
}
// Output: Iteration 1, 2, 4, and 5
```

---

### Summary

This chapter covers all fundamental loops in PHP with syntax, examples, and alternative formats. Mastering these loops provides a strong foundation for writing efficient and clean PHP code. Use each loop based on your scenario to control code execution and achieve desired outcomes effectively.
