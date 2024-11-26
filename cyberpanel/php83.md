# Using PHPkoru for PHP 8.3 with CyberPanel

## Installation of PHPkoru Loader for PHP version 8.3 with CyberPanel

Download the PHPkoru Loader into the CyberPanel PHP 8.3 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.3.so -O /usr/local/lsws/lsphp83/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/usr/local/lsws/lsphp83/etc/php.d/00-phpkoru.ini"
```

## Removing PHPkoru Loader for PHP Version 8.3 from CyberPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /usr/local/lsws/lsphp83/etc/php.d/00-phpkoru.ini && rm -f /usr/local/lsws/lsphp83/lib64/php/modules/phpkoru_loader.so
```