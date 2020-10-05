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

* __Check Free Disk Space__ - This will return the total free disk space on your web server.

    ```php
    <?php

    // checking disk space
    $bytes = disk_free_space(".");

    // setting up arraw for prefix
    $si_prefix = array( 'B', 'KB', 'MB', 'GB', 'TB', 'EB', 'ZB', 'YB' );

    // do the magic with math!
    $base = 1024;
    $class = min((int)log($bytes , $base) , count($si_prefix) - 1);

    // return the result
    echo "Remaining disk space is " . sprintf('%1.2f' , $bytes / pow($base,$class)) . ' ' . $si_prefix[$class];
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

ManageWP Code Snippets is Maintained by **[Waren Gonzaga](https://github.com/warengonzaga)**

[![Facebook](https://img.shields.io/badge/facebook-%231877F2.svg?&style=for-the-badge&logo=facebook&logoColor=white)](https://facebook.com/warengonzagaofficial) [![Twitter](https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/warengonzaga) [![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/warengonzagaofficial) [![YouTube](https://img.shields.io/badge/youtube-%23FF0000.svg?&style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/warengonzaga)

---

:computer: Made with :heart: by Waren Gonzaga with **YHWH** :pray:
