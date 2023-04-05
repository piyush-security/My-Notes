- - -
#### Format A Drive : 

```
Diskpart
	list disk
	select disk 1
	clean
	create partition primary
	select partition 1
	format fs=ntfs quick  OR format fs=fat32 quick 

	active
	assign letter=X
	exit

label [Drive Letter]:
	Hacker

```

#### Format a Disk : 

```
diskpart
	list disk
	select disk [disk number]
	clean
	create partition primary
	format fs=ntfs quick
	exit
```

#### Format A CD : 

```
format [drive letter]: /fs:UDF /q
	Y
```

- - -
## Make a Mountable USB : 

- Format the Drive First.
- Be sure to download the ISO File. Then; 

```
xcopy kali.iso [USB drive letter]: /h /e /f
```

- Eject and Remove the USB Drive.
- Go Use It.

- - -
#### Hide-Unhide Drives : 

To Hide A Drive.
```
diskpart
	list volumes
	select volume 3
	remove letter Z
```

To Unhide A Drive.  
```
diskpart
	list volumes
	select volume 3
	assign letter Z
```


- - -
#### List all Installed "Drivers" : 

```
driverquery
```

- - -