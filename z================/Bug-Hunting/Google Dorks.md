- - -
#### Find sensitive data : 

```
site:http://target.com ext:doc | ext:docx | ext:odt | ext:rtf | ext:sxw | ext:psw | ext:ppt | ext:pptx | ext:pps | ext:csv
```

#### Directory listing bug : 

```
site:http://target.com intitle:index.of
```

#### Configuration files : 

```
site:http://target.com ext:xml | ext:conf | ext:cnf | ext:reg | ext:inf | ext:rdp | ext:cfg | ext:txt | ext:ora | ext:ini | ext:env
```

#### Find PHPinfo() : 

```
site:http://target.com ext:php intitle:phpinfo "published by the PHP Group"
```

#### Find Signup-page : 

```
signup page :- site:http://target.com inurl:signup | inurl:register | intitle:Signup
```

#### Find Subdomain : 

```
site:*.target.com
```

#### Find Sud-Subdoamins : 

```
site:*.*.target.com
```

#### Try to find ip address : 

```
(https://medium.com) (site:*.*.29.* |site:*.*.28.* |site:*.*.27.* |site:*.*.26.* |site:*.*.25.* |site:*.*.24.* |site:*.*.23.* |site:*.*.22.* |site:*.*.21.* |site:*.*.20.* |site:*.*.19.* |site:*.*.18.* |site:*.*.17.* |site:*.*.16.* |site:*.*.15.* )
```

#### Search on github and gitlab.com : 

```
site:http://github.com | site:http://gitlab.com "http://target.com"
```

#### search http://stakoverflow.com : 

```
site:http://stackoverflow.com "http://target.com"
```

#### login page of admin pannel : 

```
site:http://target.com inurl:login | inurl:signin | intitle:Login | intitle:"sign in" | inurl:auth
```

####  php errors/warning : 

```
site:http://target.com "PHP Parse error" | "PHP Warning" | "PHP Error"
```

#### database file exposed : 

```
site:http://target.com ext:sql | ext:dbf | ext:mdb
```

#### Log files exposed : 

```
site:http://target.com ext:log
```

#### Backup and old files : 

```
site:http://target.com ext:bkf | ext:bkp | ext:bak | ext:old | ext:backup
```

#### sql error : 

```
site:site.com1 intext:"sql syntax near" | intext:"syntax error has occurred" | intext:"incorrect syntax near" | intext:"unexpected end of SQL command" | intext:"Warning: mysql_connect()" | intext:"Warning: mysql_query()" | intext:"Warning: pg_connect()"
```

- - -

