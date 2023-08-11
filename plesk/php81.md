# Using PHPkoru for PHP 8.1 with Plesk

## Installation of PHPkoru Loader for PHP version 8.1 with Plesk

Download the PHPkoru Loader into the Plesk PHP 8.1 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.1.so -O /opt/plesk/php/8.1/lib/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/8.1/etc/php.d/00-phpkoru.ini"
```

Restart Plesk PHP 8.1 FPM
```shell
service plesk-php81-fpm restart
```

Re-read Plesk PHP Handler
```shell
plesk bin php_handler --reread
```

## Removing PHPkoru Loader for PHP Version 8.1 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/8.1/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/8.1/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php81-fpm restart
```