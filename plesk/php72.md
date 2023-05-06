# Using PHPkoru for PHP 7.2 with Plesk

## Installation of PHPkoru Loader for PHP version 7.2 with Plesk

Download the PHPkoru Loader into the Plesk PHP 7.2 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.2.so -O /opt/plesk/php/7.2/lib/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/7.2/etc/php.d/00-phpkoru.ini"
```

Restart Plesk PHP 7.2 FPM
```shell
service plesk-php72-fpm restart
```

Re-read Plesk PHP Handler
```shell
plesk bin php_handler --reread
```

## Removing PHPkoru Loader for PHP Version 7.2 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/7.2/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/7.2/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php72-fpm restart
```