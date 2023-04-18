- - -
#### Drop Your Wireless Password in Clear-text : 

```
netsh wlan export profile key=clear
type .\*.xml | findstr Key
```

#### Get Your Wireless Report : 

```
netsh wlan show wlanreport
```

#### Show all your Interfaces : 

```
netsh interface show interface
```

#### Show your All IP addr : 

```
netsh interface ip show address | findstr "IP Address"
```

#### Show all DNS Servers Saved : 

```
netsh interface ip show dnsservers
```

#### Show nearer Wireless Network's BSSID : 

```
netsh wlan show network mode=bssid
```

- - -
