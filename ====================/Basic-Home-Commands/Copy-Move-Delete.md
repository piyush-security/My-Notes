# Copy Command

### Copy the entire directory with everything inside to /opt/MYNEWFolder

```sh
#Fast and safe :
rsync -av /path/to/folder/ /opt/MYNEWFolder/

cp -r /path/to/folder /opt/MYNEWFolder
```


# Delete 

### Delete the entire directory with everything inside

```sh
rm -rf /path/to/folder

#Safer - Send to Trash Instead permanent Deletion
trash-put /path/to/folder

```
```sh
#Clear Linux cache (safe)
sync; echo 3 > /proc/sys/vm/drop_caches

```


# Folder Size

```
#Show folder size (human-readable).
du -sh /path/to/folder

#Show sizes of all subfolders, largest last
du -ah /path/to/folder | sort -h

#List files sorted by size (largest first)
find . -type f -exec du -h {} + | sort -rh | head -20

#Count files & directories
find . -type f | wc -l   # Files only
find . -type d | wc -l   # Directories only

#Show last 10 modified files
ls -lt | head -10


```

