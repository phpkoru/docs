# Using PHPkoru for PHP 8.2 with Plesk

## Installation of PHPkoru Loader for PHP version 8.2 with Plesk

Download the PHPkoru Loader into the Plesk PHP 8.2 modules directory.
```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_8.2.so -O /opt/plesk/php/8.2/lib/php/modules/phpkoru_loader.so
```

Enable PHPkoru Loader
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/8.2/etc/php.d/00-phpkoru.ini"
```

### Check after installation
* Restart Plesk PHP 8.2 FPM service from `Plesk > Tools & Settings > Server Management > Services Management`
* If using dedicated FPM applications in Plesk, you will need to restart the Dedicated FPM application from the `PHP settings for website`

## Removing PHPkoru Loader for PHP Version 8.2 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/8.2/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/8.2/lib/php/modules/phpkoru_loader.so
```

### Check after removal
* Restart Plesk PHP 8.2 FPM service from `Plesk > Tools & Settings > Server Management > Services Management`
* If using dedicated FPM applications in Plesk, you will need to restart the Dedicated FPM application from the `PHP settings for website`