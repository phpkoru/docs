# Using PHPkoru for PHP 8.3 with CloudLinux PHP Selector in cPanel

## Installation of PHPkoru Loader for PHP version 8.3 with CloudLinux PHP Selector in cPanel

Download the PHPkoru Loader into the CloudLinux PHP Selector PHP 8.3 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.3.so -O /opt/alt/php83/usr/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/alt/php83/etc/php.d.all/phpkoru.ini"
```

Restart cPanel PHP FPMs
```shell
/scripts/restartsrv_apache_php_fpm
```

## Removing PHPkoru Loader for PHP Version 8.3 from CloudLinux PHP Selector in cPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/alt/php83/etc/php.d.all/phpkoru.ini && rm -f /opt/alt/php83/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```