## Chapter: Superglobals in PHP

Superglobals are built-in variables in PHP that are always accessible, regardless of scope, making them exceptionally useful for handling user inputs, managing sessions, handling file uploads, and more. PHP provides several superglobal arrays, each with a specific role, such as gathering request data, storing session data, or managing file uploads. By understanding and using these superglobals effectively, developers can create dynamic, interactive, and secure PHP applications.

---

### Understanding Superglobals

Superglobals are predefined arrays in PHP that allow data to be shared across different parts of a PHP script. They are called “super” because they are globally accessible from any function, class, or file without the need to use `global` to access them. This convenience simplifies handling user inputs, session data, server information, and cookies.

PHP’s core superglobals include:

- `$_GET`
- `$_POST`
- `$_REQUEST`
- `$_SESSION`
- `$_COOKIE`
- `$_FILES`

Each of these arrays has a unique purpose and offers specific methods for securely managing and processing data.

---

### Using `$_GET` and `$_POST`

The `$_GET` and `$_POST` superglobals handle data sent through HTML forms, allowing information to be collected and used in PHP scripts.

#### `$_GET`

The `$_GET` superglobal retrieves data from the URL query string, making it suitable for handling data sent via the HTTP GET method. Since data is visible in the URL, `$_GET` is typically used for non-sensitive information, like search queries or navigation options.

**Example of a URL with query parameters:**

```html
<a href="search.php?query=php&sort=asc">Search</a>
```

**Example using `$_GET` in `search.php`:**

```php
$query = $_GET['query'] ?? 'default';
$sort = $_GET['sort'] ?? 'desc';
echo "Search Query: " . htmlspecialchars($query) . "<br>";
echo "Sort Order: " . htmlspecialchars($sort);
```

The `htmlspecialchars()` function is used to escape special characters, helping to prevent XSS attacks by ensuring that any special characters in the user input don’t interfere with HTML.

#### `$_POST`

The `$_POST` superglobal is used for form submissions that send data via the HTTP POST method. Unlike `$_GET`, `$_POST` data isn’t visible in the URL, making it better suited for sensitive information, such as passwords and form data.

**Example HTML form using `$_POST`:**

```html
<form method="POST" action="submit.php">
  <input type="text" name="username" />
  <input type="password" name="password" />
  <input type="submit" value="Submit" />
</form>
```

**Example of accessing `$_POST` data in `submit.php`:**

```php
$username = $_POST['username'] ?? 'Anonymous';
$password = $_POST['password'] ?? '';
echo "Username: " . htmlspecialchars($username);
```

---

### Handling File Uploads with `$_FILES`

`$_FILES` is a superglobal specifically designed to handle file uploads from HTML forms. It contains information about the uploaded file, including its name, type, size, temporary location, and any errors that occurred during the upload.

**HTML Form for File Upload:**

```html
<form method="POST" action="upload.php" enctype="multipart/form-data">
  <input type="file" name="uploadFile" />
  <input type="submit" value="Upload" />
</form>
```

The `enctype="multipart/form-data"` attribute is required for forms that upload files.

**Example of handling file uploads in `upload.php`:**

```php
if ($_FILES['uploadFile']['error'] == UPLOAD_ERR_OK) {
    $tmpName = $_FILES['uploadFile']['tmp_name'];
    $fileName = basename($_FILES['uploadFile']['name']);
    $destination = "uploads/" . $fileName;
    if (move_uploaded_file($tmpName, $destination)) {
        echo "File uploaded successfully!";
    } else {
        echo "File upload failed!";
    }
} else {
    echo "An error occurred during the upload.";
}
```

Here, the `move_uploaded_file()` function is used to transfer the file from the temporary location to a permanent location in the server directory. Checking for errors using `$_FILES['uploadFile']['error']` ensures that any issues during the upload process are properly handled.

---

### Sessions with `$_SESSION`

The `$_SESSION` superglobal allows data to be stored and accessed across multiple pages for a single user session. Sessions are particularly useful for tracking user activity, managing user logins, and retaining user preferences during their time on a website.

#### Starting a Session

To use `$_SESSION`, start a session at the beginning of your PHP script using `session_start()`. Once a session is started, you can store and retrieve session variables.

**Example of setting session variables:**

```php
session_start();
$_SESSION['username'] = "JohnDoe";
$_SESSION['loggedIn'] = true;
echo "Session variables are set.";
```

**Example of accessing session variables on a different page:**

```php
session_start();
if (isset($_SESSION['loggedIn']) && $_SESSION['loggedIn'] === true) {
    echo "Welcome, " . $_SESSION['username'] . "!";
} else {
    echo "Please log in.";
}
```

Using sessions, data remains available until the user closes the browser or the session times out.

---

### Cookies with `$_COOKIE`

`$_COOKIE` provides access to cookies that are set by the server and stored on the user’s browser. Cookies are used for various purposes, like tracking users over time, storing preferences, or identifying returning visitors.

#### Setting a Cookie

You can set a cookie using PHP’s `setcookie()` function, and once set, it will be accessible through `$_COOKIE`.

**Example of setting a cookie:**

```php
setcookie("username", "JohnDoe", time() + (86400 * 30), "/"); // Expires in 30 days
```

**Example of accessing a cookie:**

```php
if (isset($_COOKIE['username'])) {
    echo "Hello, " . htmlspecialchars($_COOKIE['username']) . "!";
} else {
    echo "Welcome, guest!";
}
```

Cookies persist even after the browser is closed, and they’re sent with every HTTP request, making them ideal for maintaining data over longer periods.

---

### Summary

PHP’s superglobals provide efficient ways to access and manage a wide range of data, from form inputs to sessions and cookies. Understanding when and how to use `$_GET`, `$_POST`, `$_REQUEST`, `$_SESSION`, `$_COOKIE`, and `$_FILES` is essential for building dynamic and secure PHP applications that can handle various types of user interactions and data processing.
