


# Contributing code
Code contributions are very welcome! Browse the [Issue tracker](https://github.com/LibreHealthIO/LibreEHR/issues) for issues that need code and/or come up with your own ideas & code. Please open a [Pull Request](https://github.com/LibreHealthIO/LibreEHR/pulls) to contribute your own code.

## Local Development

## Windows :: 

Firstly make sure that you have [WAMP](https://sourceforge.net/projects/wampserver/) or [XAMPP](https://www.apachefriends.org/index.html) server installed and the time zone is set correctly.

Make the following changes in `php.ini` file. You can find the `php.ini` file by looking at the following destination :
* In case of WAMP :
`C:/WAMP/BIN/PHP/php.ini` OR (left click )  wampmanager icon -> PHP -> php.ini
* In  case of XAMPP:
`C:/WAMP/BIN/PHP/php.ini`.


Make the following changes in your php.ini file :
(Search for the following and make necessary changes)

* `short_open_tag` = On
* `max_execution_time` = 600
* `max_input_time` = 600
* `max_input_vars` = 5000
* `memory_limit` = 1024M
* `error_reporting` = E_ALL & ~E_DEPRECATED & ~E_STRICT & ~E_NOTICE
* `register_argc_argv` = On
* `post_max_size` = 32M
* `upload_max_filesize` = 16M
* `session.gc_maxlifetime` = 14400

Make sure you have disabled strict mode in Mysql . 

## How to disable Mysql strict mode?

Make the following changes in the `my.ini/my.cnf`:
Find it here `C:\WAMP\BIN\MYSQL\MySQL Server 5.6\my.ini` OR `C:\xampp\mysql\bin\my.ini` 
OR (left click ) wampmanager icon -> MYSQL -> my.ini

    1.  Look for the following line:
        sql-mode = STRICT_TRANS_TABLES,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION
        or sometimes it maybe  sql_mode

    2.  Change it to:
        sql-mode="" (Blank)

    3. Restart the MySQL service.
    

Restart WAMPP/XAMPP Server.

You can fork & clone the repository for local development. To get started you need to:
 - Clone the repository
 - Run index.php file which then redirects to setup page! Follow the instructions and you are done!!
 
Sometimes , installation may take more time than usual on some systems. In that case, you would need to increase `max_execution_time` in your php.ini file and then restart your server.
