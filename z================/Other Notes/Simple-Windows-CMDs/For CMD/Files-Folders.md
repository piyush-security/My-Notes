- - -
## Creating Files and Folders : 

#### Create Folder : 

```
mkdir Test
```

#### Create Empty File : 

```
type nul> My_Test_File.txt
type nul> My_Test_File.pptx
```


- - -
## Renaming Files / Folders : 

```
rename Test NewTest
ren Test NewTest
```


- - -
## Copy-Paste File / Folder : 

```
copy sendme.txt C:\Users\hacker\Desktop\
copy sendme.txt C:\Users\hacker\Desktop\test.txt
```


- - -
## Move File / Folder : 

```
move file C:\Users\Hacker\Desktop\
move Folder C:\Users\Hacker\Desktop\
```


- - -
## Delete File / Folder : 

#### Del File : 

```
del DeleteMe.txt 
del .\*                    # Delete every file fron $PWD
```

#### Del Folder : 

```
rmdir IamEmpty
rmdir /S IamFull
```


- - -
#### Encrypt-Decrypt a File / Folder : 

Encrypt-Decrypt A File OR Folder.
```
cipher /e "C:\Users\test.txt"
cipher /d "C:\Users\test.txt"
```

Encrypt-Decrypt All Files and Subfolders inside a Folder.
```
cipher /e /s:"C:\Users\test\BackUp-Data\"
cipher /d /s:"C:\Users\test\BackUp-Data\"
```


- - -

