## Open up the .htaccess file in a code editor and add the following
```
php_value upload_max_filesize 256M
php_value post_max_size 128M
php_value memory_limit 256M
php_value max_execution_time 300
php_value max_input_time 300
```