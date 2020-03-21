# cPanel PHP 7.2 için PHPkoru Kullanımı

## cPanel'de PHP 7.2 sürümü için PHPkoru Loader'ın Kurulumu

PHPkoru Loader'i cPanel PHP 7.2 modülleri dizinine indir.

```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.2.so -O /opt/cpanel/ea-php72/root/usr/lib64/php/modules/phpkoru_loader.so
```

PHPkoru Loader'i ekle
```shell
echo -e "; Enable phpkoru_loader extension module\nextension=phpkoru_loader.so" > "/opt/cpanel/ea-php72/root/etc/php.d/00-phpkoru.ini"
```

cPanel PHP Fpm'leri yeniden başlat
```shell
/scripts/restartsrv_apache_php_fpm
```

## cPanel'de PHP 7.2 sürümü için PHPkoru Loader'ın Kaldırması

PHPkoru Loader'ı kaldırmak için aşağıdaki kodu kullanabilirsiniz.
```shell
rm -f /opt/cpanel/ea-php72/root/etc/php.d/00-phpkoru.ini && rm -f /opt/cpanel/ea-php72/root/usr/lib64/php/modules/phpkoru_loader.so && /scripts/restartsrv_apache_php_fpm
```