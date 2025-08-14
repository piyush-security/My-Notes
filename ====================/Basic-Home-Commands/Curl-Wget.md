## Curl : 

```sh
#Basic download
curl -O https://example.com/file.zip

#Download multiple Files 
curl -O URL1 -O URL2 -O URL3

# Download and Save with custom name
curl -o myfile.zip https://example.com/file.zip

#Follow redirects
curl -LO https://short.url/file

#Send data to API (POST JSON)
curl -X POST -H "Content-Type: application/json" -d '{"user":"piyush"}' https://api.example.com/create

#Pretend to be a browser (scrape without block)
curl -A "Mozilla/5.0" https://example.com


```


## Wget 

```sh
#Basic download
wget https://example.com/file.zip

#Download entire site (offline mirror)
wget -r -np -k https://example.com

#Resume broken download
wget -c https://example.com/bigfile.zip

#Limit speed (avoid hogging network)
wget --limit-rate=200k https://example.com/file.zip


```



## Wget2 

```sh
#Parallel downloads
wget2 --max-threads=8 -i urls.txt

#HTTP/2 for speed
wget2 --http2 https://example.com

#Mirror site faster
wget2 -r -np -k --max-threads=16 https://example.com


```