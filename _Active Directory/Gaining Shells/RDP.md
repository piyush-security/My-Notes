- - -
## Basic Command : 

```sh
xfreerdp /u:admin /pth:<NTLM-hash-of-user-admin-pass> /v:$IP /cert-ignore /dynamic-resolution
```

```sh
xfreerdp /u:admin /p:password /cert:ignore /v:10.10.147.80 /workarea
```

```sh
xfreerdp /u:administrator /g:grandbussiness /p:bla /v:192.168.1.34
```

```sh
xfreerdp /d:THM /u:Administrator /p:Password321 /v:10.10.158.14 /dynamic-resolution
```

```sh
rdesktop $IP
```


- - -
## Enable multiple RDP sessions : 
https://twitter.com/Alh4zr3d/status/1609954528425558016

```
reg add HKLM\System\CurrentControlSet\Control\TerminalServer /v fSingleSessionPerUser /d 0 /f
```

```
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fSingleSessionPerUser /t REG_DWORD /d 0 /f
```

- - -
