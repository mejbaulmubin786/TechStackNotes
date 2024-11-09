To get started with writing and running your first PHP script, I’ll guide you through two methods: using the XAMPP Control Panel and using Visual Studio Code (VS Code) with the Code Runner extension. We'll skip the installation steps and assume you already have PHP installed and configured on your system.

---

### Method 1: Running PHP Script Using XAMPP Control Panel

1. **Start the Apache Server in XAMPP:**

   - Open the XAMPP Control Panel.
   - Find the Apache module and click on **Start**. This starts the Apache server, which allows you to run PHP scripts on `localhost`.

2. **Write Your PHP Script:**

   - Open any text editor (e.g., Notepad or a code editor like VS Code).
   - Write the following PHP script and save it as `hello.php` in the `htdocs` folder inside the XAMPP directory (usually located in `C:\xampp\htdocs\`):
     ```php
     <?php
         echo "Hello, World!";
     ?>
     ```

3. **Run Your PHP Script:**

   - Open a web browser.
   - Type `http://localhost/hello.php` in the address bar and press **Enter**.
   - The browser should display:
     ```
     Hello, World!
     ```

   This confirms your PHP script is working correctly.

---

### Method 2: Running PHP Script Using VS Code with the Code Runner Extension

If you'd prefer to work directly in VS Code, you can run PHP scripts from the editor using the Code Runner extension.

1. **Set Up Code Runner in VS Code:**

   - Open VS Code.
   - Go to **Extensions** (click the square icon in the sidebar or press `Ctrl+Shift+X`).
   - Search for **Code Runner** and install it. Code Runner allows you to run code in various languages directly in the VS Code terminal.

2. **Write Your PHP Script:**

   - In VS Code, create a new file and name it `hello.php`.
   - Write the following code in the file:
     ```php
     <?php
         echo "Hello, World!";
     ?>
     ```

3. **Run the PHP Script with Code Runner:**

   - Right-click anywhere in the `hello.php` file and select **Run Code**.
   - Alternatively, you can press `Ctrl+Alt+N` to run the code using Code Runner.
   - The output will appear in the integrated terminal at the bottom of VS Code:
     ```
     Hello, World!
     ```

   This process runs the script directly in the terminal without needing a web server.

---

### Summary of Both Methods

- **Using XAMPP Control Panel:** Best for testing PHP scripts that interact with web browsers, as it mimics a real web server.
- **Using VS Code with Code Runner:** Quick and convenient for running PHP scripts directly in the editor, especially for testing basic PHP functionality without a web server.

Both methods are useful depending on your workflow, allowing you to test PHP scripts locally before deploying them to a live server.
