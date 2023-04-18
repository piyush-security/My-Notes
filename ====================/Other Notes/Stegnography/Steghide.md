- - -
## Theory : 
Steghide is a steganography program that hides data in various kinds of **image** and **audio** files , only supports these file formats : `JPEG, BMP, WAV and AU`. but it’s also useful for extracting embedded and encrypted data from other files.

Very Useful : https://0xrick.github.io/lists/stego/

- - -
## Hide data : 

```sh
steghide embed -ef hideme.txt -cf index.jpeg
```

## Check for information inside image : 

```sh
steghide info file
```

![Imgur](https://i.imgur.com/kAyZtHs.png)

## Extract data from file : 

```sh
steghide extract -sf file
```

