### Find a file named exactly "My file" : 

```sh
find /path/to/folder -type f -name "My file"

#case-insensitive
find /path/to/folder -type f -iname "My file"
```

### Find a <u>file<u/> containing text "MySecretGame" : 

```sh
grep -ril "MySecretGame" /path/to/folder

grep -rin "MySecretGame" /path/to/folder

#search "MySecretGame" only inside ".md" files
find /path/to/folder -type f -name "*.md" | xargs grep -i "MySecretGame"


```
### Find any particular file type `(e.g., .md)`

```sh
find /path/to/folder -type f -name "*.md"

```

#### Find files > 100MB 
```sh
find . -type f -size +100M
```

#### Find and delete all .tmp files
```sh
find . -type f -name "*.tmp" -delete

```


## Grep : 

```sh
#Extract all emails from file
grep -E -o "[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-z]{2,}" dump.txt

#Extract all URLs
grep -E -o "https?://[^ ]+" dump.txt

Extract lines containing "password" 
grep -i "password" dump.txt


#You’ve got `/var/www` after shell — extract all possible creds in one go:
grep -RniE 'pass(word)?\s*[:=]\s*["\']?[A-Za-z0-9!@#$%^&*_.-]+' /var/www 2>/dev/null | \
sed 's/^[^:]*://g' | sort -u
```

