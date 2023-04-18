- - -
## Sed Command : 

#### Replacing or substituting string : 

```sh
sed 's/unix/linux/' geekfile.txt
```

#### Parenthesize first character of each word : 

```sh
echo "Welcome To The Geek Stuff" | sed 's/\(\b[A-Z]\)/\(\1\)/g'

---> output
(W)elcome (T)o (T)he (G)eek (S)tuff
```

#### Replacing string on a specific line number : 
Here replacing only on line **3**.

```sh
sed '3 s/unix/linux/' geekfile.txt
```

#### Deleting lines from a particular file :

```sh
sed 'nd' filename.txt
sed '5d' filename.txt

## Delete the Last Line : 
sed '$d' filename.txt
```

- - -

