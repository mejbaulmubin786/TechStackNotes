#### Writing Your First PHP Script

To begin, you need to have a basic understanding of how to write and execute a simple PHP script. Here's a step-by-step guide:

1. **Create a PHP File:**
   - Start by creating a new file with the `.php` extension, e.g., `first_script.php`.

2. **Write a Simple PHP Script:**
   - Open the file in a text editor (like VS Code, Sublime Text, or Notepad++) and write your first PHP script. For example:
     ```php
     <?php
     echo "Hello, World!";
     ?>
     ```
   - This script will output the text "Hello, World!" when executed.

3. **Save the File:**
   - Save the file after writing your script.

#### Embedding PHP in HTML

One of the most powerful features of PHP is its ability to be embedded directly within HTML code. This allows you to dynamically generate HTML content based on logic written in PHP.

Here's how you can embed PHP in an HTML file:

1. **Basic Embedding:**
   - You can embed PHP within an HTML document like this:
     ```php
     <!DOCTYPE html>
     <html>
     <head>
         <title>My First PHP Page</title>
     </head>
     <body>
         <h1><?php echo "Hello, Mejbaul Mubin!"; ?></h1>
         <p>This is a paragraph in HTML.</p>
     </body>
     </html>
     ```
   - In this example, the PHP code `<?php echo "Hello, Mejbaul Mubin!"; ?>` is embedded within the HTML. When this page is loaded in a browser, it will display the message inside the `<h1>` tags.

2. **Mixing HTML and PHP:**
   - You can switch between HTML and PHP as needed. For example:
     ```php
     <!DOCTYPE html>
     <html>
     <body>
         <h2>Welcome to My Website</h2>
         <?php
         $name = "Mejbaul";
         echo "<p>Hello, $name! Welcome to my PHP-embedded webpage.</p>";
         ?>
         <p>Have a great day!</p>
     </body>
     </html>
     ```
   - Here, PHP is used to create a personalized greeting based on the variable `$name`.

#### Running PHP Scripts in the Browser

To run PHP scripts in your browser, you need a server that supports PHP. Here’s how you can do it:

1. **Install a Local Server Environment:**
   - To run PHP locally, you'll need a server like Apache or Nginx and a PHP interpreter. The easiest way to set this up is by using a package like:
     - **XAMPP**: Contains Apache, MySQL, PHP, and Perl.
     - **WAMP**: Contains Apache, MySQL, and PHP for Windows.
     - **MAMP**: Contains Apache, MySQL, and PHP for macOS.
     - **LAMP**: Linux variant that includes Apache, MySQL, and PHP.

2. **Move Your PHP Files to the Server's Root Directory:**
   - Once your server environment is set up, move your PHP file (`first_script.php`) to the server’s root directory:
     - For XAMPP, this is usually `C:\xampp\htdocs\`.
     - For WAMP, it is `C:\wamp\www\`.
     - For MAMP, it is `Applications/MAMP/htdocs/`.
     - For LAMP, it is `/var/www/html/`.

3. **Run the Script in Your Browser:**
   - Open your web browser and navigate to `http://localhost/first_script.php`.
   - The browser will display the output of your PHP script, for example, "Hello, World!".

4. **Check for Errors:**
   - If something goes wrong, ensure your server is running, and your file is in the correct directory. Also, ensure there are no syntax errors in your PHP code.

### Summary

- **Your First PHP Script**: Learn how to create, write, and save a basic PHP script.
- **Embedding PHP in HTML**: Understand how to embed PHP within HTML to create dynamic web pages.
- **Running PHP Scripts in the Browser**: Learn how to run PHP scripts using a local server environment like XAMPP, WAMP, MAMP, or LAMP.

These concepts form the foundation of PHP web development, and mastering them will allow you to create dynamic, data-driven websites. If you need more detailed examples or explanations, feel free to ask!
