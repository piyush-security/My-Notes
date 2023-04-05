- - -
## Wordpress Version Detection : 

```sh
curl -s -X GET http://blog.inlanefreight.com | grep -oP '(?<=WordPress\s)[0-9]+\.[0-9]+\.[0-9]+' file.txt

curl -s -X GET http://blog.inlanefreight.com | grep '<meta name="generator"'
```

![Imgur](https://i.imgur.com/D9XUwGv.png)


## Plugins Enumeration : 

```sh
curl -s -X GET http://blog.inlanefreight.com | sed 's/href=/\n/g' | sed 's/src=/\n/g' | grep 'wp-content/plugins/*' | cut -d"'" -f2
```

```sh
curl -I -X GET http://blog.inlanefreight.com/wp-content/plugins/<|PLUGIN-NAME|>
```
- If exists, then **200-OK**, **302** .. . And If not -> **404 Not Found**.
- We can automate this process by using our own Tool : 
[WordPress-Plugin-Enum](https://github.com/piyush-security/WordPress-Plugin-Enum)


## Themes Enumeration : 

```sh
curl -s -X GET http://blog.inlanefreight.com | sed 's/href=/\n/g' | sed 's/src=/\n/g' | grep 'themes' | cut -d"'" -f2
```


- - -
