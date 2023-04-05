- - -
## Theory 📜📜📜📜
- The aircrack ng creates a PMK for each password from wordlist then use that PMK to match.
- But What if we already give it a list of PMKs. ( Ready to use ).
- It will crack the key much faster.

- - -
# Computing PMKs : 

#### Create a database and import Wordlist : 

```sh
airolib-ng <DB_Name> --import passwd Password.txt 
```

![Imgur](https://i.imgur.com/ug4hOLZ.png)

#### Import SEO Target : 

```sh
# Note the ESSID of the Target Network.
echo '<APs_ESSID>' > test-essid
airolib-ng <DB_Name> --import essid test-essid
```

![Imgur](https://i.imgur.com/zp7vIqA.png)

#### Compute PMK for the wordlist : 

```sh
airolib-ng <DB_Name> --batch 
```

![Imgur](https://i.imgur.com/5lKIZYk.png)

#### Crack The Key using the PMK DB : 

```sh
aircrack-ng -r <DB_Name> handshake-01.cap 
```

![Imgur](https://i.imgur.com/0jU6R0d.png)

- - -
