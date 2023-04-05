- - -
Simple **python script** that helps you to **detect SQL injection** "**Error based**" by sending multiple requests with **14 payloads** and checking for **152 regex patterns** for different databases.

#### Installation : 

```
git clone  https://github.com/eslam3kl/SQLiDetector.git ; cd SQLiDetector/
pip3 install -r requirements.txt 
```

#### Usage : 
Before Using **Read the Official  Guide** : 
- https://github.com/eslam3kl/SQLiDetector

```
# cat urls.txt
http://testphp.vulnweb.com/artists.php?artist=1
```

```
python3 sqlidetector.py -h
python3 sqlidetector.py -f urls.txt -w 50 -o output.txt -t 10 
```


- - -



