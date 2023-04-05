- - -
## Theory : 
It supports just about every image file, and is able to extract all types of data from it. It is an incredibly useful tool.

- - -
## Usage : 

#### Installation : 

```python
pip3 install stegoveritas
/home/<User>/.local/bin/stegoveritas_install_deps
```

#### Simple Use : 

```sh
stegoveritas file # by default run all checks.
stegoveritas -exif -meta -xmp -carve -imageTransform -BruteLSB -extractLSB -trailing massacre.png
```

#### Check For metadata : 

```sh
stegoveritas file -meta 
```

#### Perform various image transformations
Perform various image transformations on the input image and save them to the output directory.

```sh
stegoveritas file -imageTransform
stegoveritas -imageTransform -extractLSB Lost.png
```

#### Check for StegHide hidden info : 

```sh
stegoveritas -steghide file 
```

