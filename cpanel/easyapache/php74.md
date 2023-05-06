# Using PHPkoru for PHP 7.4 with EasyApache 4 in cPanel

## Installation of PHPkoru Loader for PHP version 7.4 with EasyApache 4 in cPanel

Download the PHPkoru Loader into the EasyApache 4 PHP 7.4 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.4.so -O /opt/cpanel/ea-php74/root/usr/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/cpanel/ea-php74/root/etc/php.d/00-phpkoru.ini"
```

Restart cPanel PHP FPMs
```shell
/scripts/restartsrv_apache_php_fpm
```

## Removing PHPkoru Loader for PHP Version 7.4 from EasyApache 4 in cPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/cpanel/ea-php74/root/etc/php.d/00-phpkoru.ini && rm -f /opt/cpanel/ea-php74/root/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```