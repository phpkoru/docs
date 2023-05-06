# Using PHPkoru for PHP 8.0 with Plesk

## Installation of PHPkoru Loader for PHP version 8.0 with Plesk

Download the PHPkoru Loader into the Plesk PHP 8.0 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.0.so -O /opt/plesk/php/8.0/lib/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/8.0/etc/php.d/00-phpkoru.ini"
```

Restart Plesk PHP 8.0 FPM
```shell
service plesk-php80-fpm restart
```

Re-read Plesk PHP Handler
```shell
plesk bin php_handler --reread
```

## Removing PHPkoru Loader for PHP Version 8.0 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/8.0/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/8.0/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php80-fpm restart
```