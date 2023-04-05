- - -
#### Clear the CMD Screen : 

```
cls
```

- - -
### See Which File Type Associates with which programs : 

```
assoc 
```

##### Modify it : 

```
assoc .mp4=VLC.vlc
```


- - -
## ShutDown : 

#### Simple Shutdown : 

```
shutdown /s /t 20
```

#### Shutdown and Restart to BIOS Menu : 

```
shutdown /r /fw /f /t 0 
```

#### Reboot Computer : 

```
shutdown /r
```

- - -
### Hide-Unhide Folder : 

```
Attrib +h +s +r folder_name
Attrib -h -s -r folder_name
```

- - -
### CMD History : 

```
doskey /history

----Or--------
just press the "F7 key"
```

- - -
### Delete All Temp Files : 

```
del /q /f /s %temp%\*
del /q /f /s %temp%\* && del /s /q C:\Windows\temp\*
```

- - -
### Show Downloaded Programs : 

```
wmic product get name
```


