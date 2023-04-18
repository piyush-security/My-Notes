- - -
## Power Issues : 
#### Check and Battery / Power Issues : 

```
powercfg /energy
```

#### Get Your Battery Report : 

```
powercfg /batteryreport
```

## Disk Issues : 
#### Does it need a Repair : 
If yes, it will fix it.

```
chkdsk /f
```

#### Check For Physical Sector Issues : 

```
chkdsk /r
```

## Scan & Fix System Files : 

```
sfc /scannow
```

```
DISM /Online /Cleanup-Image /CheckHealth 
DISM /Online /Cleanup-Image /ScanHealth
DISM /Online /Cleanup-Image /RestoreHealth
```

again ; 
```
sfc /scannow
```

- - -
