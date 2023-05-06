# Using PHPkoru for PHP 7.4 with CloudLinux PHP Selector in cPanel

## Installation of PHPkoru Loader for PHP version 7.4 with CloudLinux PHP Selector in cPanel

Download the PHPkoru Loader into the CloudLinux PHP Selector PHP 7.4 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.4.so -O /opt/alt/php74/usr/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/alt/php74/etc/php.d.all/phpkoru.ini"
```

Restart cPanel PHP FPMs
```shell
/scripts/restartsrv_apache_php_fpm
```

## Removing PHPkoru Loader for PHP Version 7.4 from CloudLinux PHP Selector in cPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/alt/php74/etc/php.d.all/phpkoru.ini && rm -f /opt/alt/php74/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```