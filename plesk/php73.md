# Plesk PHP 7.3 için PHPkoru Kullanımı

## Plesk'te PHP 7.3 sürümü için PHPkoru Loader'ın Kurulumu

PHPkoru Loader'i Plesk PHP 7.3 modülleri dizinine indir.

```shell
wget https://cdn.phpkoru.com/loaders/phpkoru_loader_v1.0.2_lin_7.3.so -O /opt/plesk/php/7.3/lib/php/modules/phpkoru_loader.so
```

PHPkoru Loader'i ekle
```shell
echo "extension=phpkoru_loader.so" > "/opt/plesk/php/7.3/etc/php.d/00-phpkoru.ini"
```

Plesk PHP ayarlarını güncelle
```shell
plesk bin php_handler --reread
```

Plesk PHP 7.3'ü yeniden başlat
```shell
service plesk-php73-fpm restart
```

## Plesk'te PHP 7.3 sürümü için PHPkoru Loader'ın Kaldırması

PHPkoru Loader'ı kaldırmak için aşağıdaki kodu kullanabilirsiniz.
```shell
rm -f /opt/plesk/php/7.3/etc/php.d/00-phpkoru.ini && rm -f /opt/plesk/php/7.3/lib/php/modules/phpkoru_loader.so && plesk bin php_handler --reread && service plesk-php73-fpm restart
```