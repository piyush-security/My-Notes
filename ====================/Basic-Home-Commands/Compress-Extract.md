# Compress-Extract

### Tar  

```sh
# Make a tar.gz backup
tar -czvf backup.tar.gz /path/to/folder


# Extract tar.gz
tar -xzvf backup.tar.gz

# Move all .jpg files from subdirs to current dir
find . -type f -name "*.jpg" -exec mv {} . \;
find . -type f -name "*.jpg" -exec bash -c 'for f; do mv "$f" "./$(basename "$(dirname "$f")")_$(basename "$f")"; done' _ {} +

```
```swift
/home/piyush/Pictures     ← main directory
/home/piyush/Pictures/Trips        ← subdirectory
/home/piyush/Pictures/Trips/Goa    ← sub-subdirectory
```



