# Using PHPkoru for PHP 8.0 with EasyApache 4 in cPanel

## Installation of PHPkoru Loader for PHP version 8.0 with EasyApache 4 in cPanel

Download the PHPkoru Loader into the EasyApache 4 PHP 8.0 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.0.so -O /opt/cpanel/ea-php80/root/usr/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/cpanel/ea-php80/root/etc/php.d/00-phpkoru.ini"
```

Restart cPanel PHP FPMs
```shell
/scripts/restartsrv_apache_php_fpm
```

## Removing PHPkoru Loader for PHP Version 8.0 from EasyApache 4 in cPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/cpanel/ea-php80/root/etc/php.d/00-phpkoru.ini && rm -f /opt/cpanel/ea-php80/root/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```