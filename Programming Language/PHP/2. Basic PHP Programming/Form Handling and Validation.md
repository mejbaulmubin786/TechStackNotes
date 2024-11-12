## Chapter: Form Handling and Validation in PHP

Form handling and validation are essential for any web application that requires user interaction. Forms allow users to submit data to the server, and PHP provides robust tools for capturing, processing, validating, and sanitizing this data. Understanding how to create forms in HTML, process the data in PHP, and validate it securely will ensure that your application maintains high standards of usability and security.

---

### Creating Forms with HTML

HTML forms are the starting point for collecting user input on a webpage. Each form element, such as text inputs, radio buttons, checkboxes, and submit buttons, has a unique `name` attribute, allowing PHP to access and process the submitted data.

**Example of an HTML Form:**

```html
<form action="process_form.php" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />

  <label for="age">Age:</label>
  <input type="number" id="age" name="age" min="1" max="100" />

  <input type="submit" value="Submit" />
</form>
```

In this example:

- The `action` attribute specifies the PHP script (e.g., `process_form.php`) that will process the form data.
- The `method="POST"` attribute ensures that data is sent securely.
- `required`, `min`, and `max` attributes help enforce basic validation at the HTML level.

---

### Processing Form Data with PHP

After submitting a form, PHP can access the data via the `$_POST` or `$_GET` superglobal arrays, depending on the form’s method. It’s crucial to first check if the form has been submitted to avoid errors if the PHP script is accessed without a form submission.

**Example of Processing Form Data:**

```php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'] ?? '';
    $email = $_POST['email'] ?? '';
    $age = $_POST['age'] ?? '';

    echo "Name: " . htmlspecialchars($name) . "<br>";
    echo "Email: " . htmlspecialchars($email) . "<br>";
    echo "Age: " . htmlspecialchars($age);
}
```

Using `htmlspecialchars()` helps prevent cross-site scripting (XSS) by converting special characters to HTML entities, ensuring user input is safe for display.

---

### Validating User Input

Validation is critical for ensuring data integrity and security. Validating input means checking that the data meets certain criteria, such as being in the correct format or within an expected range. Proper validation prevents errors, improves user experience, and protects against malicious data.

#### 1. Required Fields

Ensuring required fields are filled is a fundamental validation step. PHP can check if a field has data by verifying its value.

**Example:**

```php
if (empty($name)) {
    echo "Name is required.";
}
```

#### 2. Data Formats

Validation against specific formats, like email or phone number formats, ensures the data is correctly structured. PHP’s `filter_var()` function offers built-in options for this.

**Example of Email Validation:**

```php
if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo "Invalid email format.";
}
```

#### 3. Length Constraints

Checking the length of input fields is essential for fields like usernames, passwords, or comments, ensuring they are neither too short nor excessively long.

**Example:**

```php
if (strlen($name) < 3) {
    echo "Name must be at least 3 characters long.";
}
```

---

### Sanitizing Input

Sanitization ensures that user input is safe to process and store. Sanitizing data is particularly important for data that will be stored in a database, displayed back to users, or used in queries.

#### 1. Filter Functions

PHP’s `filter_var()` function can be used for both validating and sanitizing input.

**Example of Sanitizing an Email Address:**

```php
$email = filter_var($email, FILTER_SANITIZE_EMAIL);
```

#### 2. `htmlspecialchars()`

`htmlspecialchars()` is effective for escaping HTML special characters, preventing them from being interpreted as code.

**Example:**

```php
$comment = htmlspecialchars($_POST['comment']);
```

This converts special characters (like `<`, `>`, and `&`) to HTML entities (`&lt;`, `&gt;`, `&amp;`), making it safe to display.

#### 3. `strip_tags()`

`strip_tags()` removes all HTML and PHP tags from a string, which is useful when you need to eliminate potentially dangerous tags.

**Example:**

```php
$bio = strip_tags($_POST['bio']);
```

---

### Example: Putting It All Together

Here’s a full example of creating, processing, validating, and sanitizing form data.

**HTML Form:**

```html
<form action="process_form.php" method="POST">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required />

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />

  <label for="age">Age:</label>
  <input type="number" id="age" name="age" />

  <input type="submit" value="Register" />
</form>
```

**PHP Script (`process_form.php`):**

```php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $username = filter_var(trim($_POST['username']), FILTER_SANITIZE_STRING);
    $email = filter_var($_POST['email'], FILTER_SANITIZE_EMAIL);
    $age = filter_var($_POST['age'], FILTER_SANITIZE_NUMBER_INT);

    $errors = [];

    // Validation
    if (empty($username) || strlen($username) < 3) {
        $errors[] = "Username must be at least 3 characters long.";
    }

    if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
        $errors[] = "Please enter a valid email address.";
    }

    if ($age && ($age < 1 || $age > 120)) {
        $errors[] = "Please enter a valid age between 1 and 120.";
    }

    if (empty($errors)) {
        echo "Registration successful!";
        echo "Username: " . htmlspecialchars($username) . "<br>";
        echo "Email: " . htmlspecialchars($email) . "<br>";
        echo "Age: " . htmlspecialchars($age);
    } else {
        foreach ($errors as $error) {
            echo $error . "<br>";
        }
    }
}
```

In this example:

- **Sanitization**: All inputs are sanitized to remove unwanted characters.
- **Validation**: Checks are in place for the required fields, format of email, and valid age range.
- **Output**: Uses `htmlspecialchars()` to safely display sanitized and validated data.

---

### Summary

PHP provides a powerful combination of tools for handling and validating form data. By structuring form handling with sanitization and validation checks, you can create secure and user-friendly applications that protect both the user and the server from potential issues. Through careful input processing and validation, you create a reliable and safe interaction layer between the user and your application.
