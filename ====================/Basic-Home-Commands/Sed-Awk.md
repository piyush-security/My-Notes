## awk 

```sh
#Print specific column
awk '{print $1, $3}' file.txt


```

```sh
#Extract usernames from /etc/passwd
awk -F: '{print $1}' /etc/passwd

#Extract only IPs from a dump
awk '{for(i=1;i<=NF;i++) if($i ~ /^[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+$/) print $i}' dump.txt




## Sed

```sh
#Delete Empty Lines
sed '/^$/d' file.txt



```
