- - -
## Theory : 
Stegseek is a lightning fast steghide cracker that can be used to extract hidden data from files.

#### Embed Text file  : 

```sh
stegseek --embed hello.txt image.jpeg
```

#### Cracking password : 

```sh
stegseek image.jpeg wordlist.txt
stegseek --crack image.jpeg wordlist.txt Output.txt
```

#### Try All method to extract data : 

```sh
stegseek --seed image.jpeg Output.txt
```

