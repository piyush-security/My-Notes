- - -
## Theory 🔖
- Sometimes our Target network is not busy. means less traffic is created.
- But for Successful crack we needed lots of traffic and Data ( IVs ) on out target network.

In this case; 
- We have to inject packets into the traffic to force the router to create new packets with new **IVs**.

- - -
## But But But 🚏⏹️⛔
Before we can start injectiong Packets into the traffic, **we have to authenticate** our WiFi-card with the **AP**.  (Otherwise, The **AP** will ignore our request. )

We can do this using **airplay-ng** liske so : 

```sh
aireplay-ng  --fakeauth 0 -a <Target-MAC> -h <Our-MAC> mon0
```

> [!Check]
> - If the authentication was succesful, the value under the "**AUTH**" column in **airodump-ng** will change to "**OPN**".

![Imgur](https://i.imgur.com/lwJruPy.png)

- - -

















