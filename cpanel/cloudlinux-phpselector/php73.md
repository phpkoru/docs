# cPanel CloudLinux PHP Selector PHP 7.3 için PHPkoru Kullanımı

## cPanel CloudLinux PHP Selector'de PHP 7.3 sürümü için PHPkoru Loader'ın Kurulumu

PHPkoru Loader'i cPanel CloudLinux PHP Selector PHP 7.3 modülleri dizinine indir.

```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.3.so -O /opt/alt/php73/usr/lib64/php/modules/phpkoru_loader.so
```

PHPkoru Loader'i ekle
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/alt/php73/etc/php.d.all/phpkoru.ini"
```

cPanel PHP Fpm'leri yeniden başlat
```shell
/scripts/restartsrv_apache_php_fpm
```

## cPanel CloudLinux PHP Selector'de PHP 7.3 sürümü için PHPkoru Loader'ın Kaldırması

PHPkoru Loader'ı kaldırmak için aşağıdaki kodu kullanabilirsiniz.
```shell
rm -f /opt/alt/php73/etc/php.d.all/phpkoru.ini && rm -f /opt/alt/php73/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```