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

### Check after installation
* Restart Plesk PHP 7.4 FPM service from `Plesk > Tools & Settings > Server Management > Services Management`
* If using dedicated FPM applications in Plesk, you will need to restart the Dedicated FPM application from the `PHP settings for website`

## Removing PHPkoru Loader for PHP Version 7.4 from Plesk

You can use the following code to uninstall PHPkoru Loader.
```shell
rm -f /opt/plesk/php/7.4/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/7.4/lib/php/modules/phpkoru_loader.so
```

### Check after removal
* Restart Plesk PHP 7.4 FPM service from `Plesk > Tools & Settings > Server Management > Services Management`
* If using dedicated FPM applications in Plesk, you will need to restart the Dedicated FPM application from the `PHP settings for website`