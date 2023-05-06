# Using PHPkoru for PHP 7.2 with CyberPanel

## Installation of PHPkoru Loader for PHP version 7.2 with CyberPanel

Download the PHPkoru Loader into the CyberPanel PHP 7.2 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.2.so -O /usr/local/lsws/lsphp72/lib64/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/usr/local/lsws/lsphp72/etc/php.d/00-phpkoru.ini"
```

## Removing PHPkoru Loader for PHP Version 7.2 from CyberPanel

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /usr/local/lsws/lsphp72/etc/php.d/00-phpkoru.ini && rm -f /usr/local/lsws/lsphp72/lib64/php/modules/phpkoru_loader.so
```