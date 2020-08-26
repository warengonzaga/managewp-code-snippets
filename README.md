# ManageWP Code Snippets [![Maintained by Waren Gonzaga](https://img.shields.io/badge/Maintained%20by-Waren%20Gonzaga-blue.svg?longCache=true&style=for-the-badge)](https://facebook.com/warengonzagaofficial)

ManageWP code snippets collection for WordPress.

## How To Use

Just copy and paste the available code snippets below and load it to your ManageWP code snippets editor.

## Code Snippets

Here's the collections of code snippets.

### Info & Debugging

* __List Plugins__ - This will list all of the available plugin in the WordPress plugin directory. Useful to check the installed plugins in your installation.

    ```php
    <?php

    // Directory to scan
    $files = scandir("wp-content/plugins");

    // Return the result of the scan
    foreach($files as $file) {
        echo $file."\n";
    }
    ```

* __Test Database Connection__ - This will return a database connection status. This is useful to when you want to make sure your database credentials are working correctly or not.

    ```php
    <?php

    // Test Database Connection
    $servername = "localhost";
    $username = "username-here";
    $password = "password-here";

    // Create connection
    $conn = new mysqli($servername, $username, $password);

    // Check connection
    if ($conn->connect_error) {
        die("Connection failed: " . $conn->connect_error);
    }
    echo "Connected successfully";
    ```

* __View File Contents__ - Able to view file contents in your installation. For example, you want to check the wp-config.php contents.

    ```php
    <?php

    // define specific file
    $file = "./wp-config.php";

    // do the magic
    $view = file_get_contents($file, true);

    // return the results
    echo $view;
    ```

## Contributing

Contributions are welcome, create a pull request to this repo and I will review your code. Please consider to submit your pull request to the ```dev``` branch. Thank you!

## Issues

If you're facing any problems with the code snippets please let me know by creating an issue to this repository. Thank you!

## To Do

* Add more code snippets

## Community

Wanna see other projects I made? Join today!

[![Community](https://discordapp.com/api/guilds/659684980137656340/widget.png?style=banner2)](https://bmc.xyz/l/wgofficialds)

## Donate or Support

If you love this collection please consider to donate or support the maintainer.

[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg?style=for-the-badge)](https://paypal.me/warengonzagaofficial) [![Support](https://img.shields.io/badge/Support-Buy%20Me%20A%20Coffee-orange.svg?style=for-the-badge)](https://buymeacoff.ee/warengonzaga)

## License

ManageWP Code Snippets is licensed under MIT - <https://opensource.org/licenses/MIT>

## Author

ManageWP Code Snippets is Maintained by **Waren Gonzaga**

* **Facebook:** <https://facebook.com/warengonzagaofficial>
* **Twitter:** <https://twitter.com/warengonzaga>
* **Website:** <https://warengonzaga.com>
* **Email:** dev(at)warengonzaga[.]com

---

:computer: with :heart: by **Waren Gonzaga** with **YHWH**
