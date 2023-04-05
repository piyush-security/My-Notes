- - -
## AWK Command Usage : 

#### Print the lines which match the given word. 

```sh
awk '/grepme/ {print}' employee.txt 
```

####  Splitting a Line Into Fields : 

```sh
awk '{print $1}' employee.txt

awk '{print $1,$2}' employee.txt

awk '{print $1,$4}' employee.txt
```

#### Display Line From 'x' to 'y' : 
Here **3** to **6** 

```sh
awk 'NR==3, NR==6 {print NR,$0}' employee.txt 
```

#### find the length of the longest line present in the file : 

```sh
awk '{ if (length($0) > max) max = length($0) } END { print max }' geeksforgeeks.txt
```

#### To count the lines in a file : 

```sh
 awk 'END { print NR }' geeksforgeeks.txt 
```

####  Printing lines with more than 10 characters : 
Useful for finding interesting strings from a file.

```sh
 awk 'length($0) > 10' geeksforgeeks.txt
```

- - -

