# Plesk PHP 7.2 için PHPkoru Kullanımı #

## Plesk'te PHP 7.2 sürümü için PHPkoru Loader'ın Kurulumu ##

PHPkoru Loader'i Plesk PHP 7.2 modülleri dizinine indir.

```shell
wget https://raw.githubusercontent.com/aponkral/phpkoru/master/loaders/php7.2/phpkoru_loader_v1.0.2_lin_7.2.so -O /opt/plesk/php/7.2/lib/php/modules/phpkoru_loader.so
```

PHPkoru Loader'i ekle
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/7.2/etc/php.d/00-phpkoru.ini"
```

Plesk PHP ayarlarını güncelle
```shell
plesk bin php_handler --reread
```

Plesk PHP 7.2'ü yeniden başlat
```shell
service plesk-php72-fpm restart
```

## Plesk'te PHP 7.2 sürümü için PHPkoru Loader'ın Kaldırması ##

PHPkoru Loader'ı kaldırmak için aşağıdaki kodu kullanabilirsiniz.
```shell
rm -f /opt/plesk/php/7.2/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/7.2/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php72-fpm restart
```