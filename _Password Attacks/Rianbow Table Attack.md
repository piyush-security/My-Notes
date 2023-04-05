- - -
## Theory ...📙🔖🌈
- For example in if we have a MD5 hash, which we want to crack.
- we will submit our MD5 Hash to this tool for cracking. 
- Then it will find that MD5 Hash in it's database.
- Its Database Table looks like this : 
![Imgur](https://i.imgur.com/klkCQpl.png)

> [!check]
> - If your PC have less memory but huge Storage, then this is for you.

- - -
## Download the Pakages  : ⬇️ 
From here : http://project-rainbowcrack.com/

Download and unzip it. Then ;
```sh
cd rainboecrack*
```

#### Creating Our Rainbow Table : ⚒️

```sh
# ./rtgen <hash_algorithm>  <charset> <len_min> <len_max> <table_index> <chain_len> <chain_sum> <part_index>
chmod 755 ./*
./rtgen md5 loweralpha 4 7 0 1000 1000 0 

#increase chain lenget like 1000 40000, to increase chances of success.
```

![Imgur](https://i.imgur.com/i0xq1Vy.png)

#### Sorting Our Rainbow Tables : 🦄

```sh
./rtsort /path/to/wordlist-Directory/ # dont include the wordlist name, only directory.
```

![Imgur](https://i.imgur.com/120DMlg.png)


#### Cracking The Hash : 💔 

```sh
./rcrack /path/to/wordlist-Directory/ -h <hash>
```

![Imgur](https://i.imgur.com/THboUlv.png)

- - -
