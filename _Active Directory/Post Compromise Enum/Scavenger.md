- - -
## Theory 📕
**Scavenger** : is a multi-threaded post-exploitation scanning tool for scavenging systems, finding most frequently used files and folders as well as "interesting" files containing sensitive information.

- https://github.com/SpiderLabs/scavenger
- - -
# Usage : 

#### Basic Use : 
```python
python3 ./scavenger.py smb -t 10.0.0.10 -u administrator -p Password123 -d test.local
python3 ./scavenger.py smb --target iplist --username administrator --password Password123 --domain test.local --overwrite
```

#### Find Interesting Shares : 
https://twitter.com/Alh4zr3d/status/1614402579282427905

![Imgur](https://i.imgur.com/QqfGaOa.png)

```python
python3 http://scavenger.py smb -t <tgt_ip> -u <username> -p <passwd> -d test.local
```


- - -
