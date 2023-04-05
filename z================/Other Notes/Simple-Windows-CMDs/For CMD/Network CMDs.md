- - -
## Network Commands from CMD : 

#### Show IP Details : 

```
ipconfig
ipconfig /all
```

#### Show Basic DNS Details : 

```
ipconfig /all | findstr DNS
```

#### Assign a New IP to your Computer : 

```
ipconfig /release
ipconfig /renew
```

#### Show your MAC Addr : 

```
getmac /v
```

#### Check Connetion to IP / Domain : 

```
ping example.com
```

#### Show Route to your Website / IP : 

```
tracert example.com
tracert -d example.com
```

#### Show all DNS Details : 
All the website your Computer knows about.

```
ipconfig /displaydns 
```

#### Delete all DNS Data : 

```
ipconfig /flushdns
```

#### See All Listening Ports : 

```
netstat -af 
```

#### See All Connection Established Ports : 

```
netstat -o
```

- - -
## Troubleshoot DNS : 

#### Find The Connections.

```
nslookup  example.com
```

#### Try another DNS Server for the Connection : 
Here Using Google.

```
nslookup example.com 8.8.8.8
```

#### Check Different DNS Records : 

```
nslookup -type=mx example.com 
nslookup -type=txt example.com 
nslookup -type=all example.com
nslookup -type=ptr example.com
```

