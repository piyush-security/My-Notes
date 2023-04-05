- - -
### What is this ? 
- [DataSurgeon](https://github.com/Drew-Alleman/DataSurgeon) ( **ds** ) is a versatile tool designed for incident response, penetration testing, and CTF challenges.
- It allows for the extraction of various types of sensitive information including **emails**, **phone numbers**, **hashes**, **credit cards**, **URLs**, **IP addresses**, **MAC addresses**, **SRV DNS records and a lot more**!

- - -
### Installation  : 

- Install **[Rust](https://www.rust-lang.org/tools/install)** 
- Install **[Github](https://git-scm.com/downloads)**
Then ruhn the  following commands : 

```sh
wget -O - https://raw.githubusercontent.com/Drew-Alleman/DataSurgeon/main/install/install.sh | bash
```


## Usage : 🔥

#### Extracting Files From a Remote Webiste :  📂

```sh
wget -qO - https://www.stackoverflow.com | ds -F --clean | uniq
```

Their are many useful uses of this tool.
Please explore it and consume all the data of your target.
![Imgur](https://i.imgur.com/G2rEYEl.png)

- - -









