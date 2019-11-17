# CyberPanel'de PHP 7.2 sürümü için PHPkoru Loader'ın Kurulumu #

PHPkoru Loader'i CyberPanel PHP 7.2 modülleri dizinine indir.
```shell
wget https://raw.githubusercontent.com/aponkral/phpkoru/master/loaders/php7.2/phpkoru_loader_v1.0.2_lin_7.2.so -O /usr/local/lsws/lsphp72/lib64/php/modules/phpkoru_loader.so
```

PHPkoru Loader'i etkinleştir
```shell
echo "extension=phpkoru_loader.so" > "/usr/local/lsws/lsphp72/etc/php.d/00-phpkoru.ini"
```

## CyberPanel'de PHP 7.2 sürümü için PHPkoru Loader'ın Kaldırması ##

PHPkoru Loader'ı kaldırmak için aşağıdaki kodu kullanabilirsiniz.
```shell
rm -f /usr/local/lsws/lsphp72/etc/php.d/00-phpkoru.ini && rm -f /usr/local/lsws/lsphp72/lib64/php/modules/phpkoru_loader.so
```