# Using PHPkoru for PHP 7.4 with Plesk

## Installation of PHPkoru Loader for PHP version 7.4 with Plesk

Download the PHPkoru Loader into the Plesk PHP 7.4 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.4.so -O /opt/plesk/php/7.4/lib/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/7.4/etc/php.d/00-phpkoru.ini"
```

Restart Plesk PHP 7.4 FPM
```shell
service plesk-php74-fpm restart
```

Re-read Plesk PHP Handler
```shell
plesk bin php_handler --reread
```

## Removing PHPkoru Loader for PHP Version 7.4 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/7.4/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/7.4/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php74-fpm restart
```