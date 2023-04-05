- - -
# Username Enumeration : 
There are two methods for performing manual username enumeration.

### First Method ☝🏻: 
Add the ?author=1   ( By default ID "**1**" is a  `admin` user )

```sh
curl -L -w 'Redirected to: %{redirect_url}\n' -I http://example.com 
curl -L -w 'Redirected to: %{redirect_url}\n' -I http://example.com | grep -i "author"
```

![Imgur](https://i.imgur.com/rUL2Zyj.png)


### Second Method ✌🏻 : 
The second method requires interaction with the **JSON** endpoint, which allows us to obtain a **list of users**. This was **changed** in WordPress core after **version 4.7.1**, **and later versions** only show whether a user is configured or not. **Before this release, all users <u>who had published a post</u> were shown by default**.

```sh
curl http://blog.inlanefreight.com/wp-json/wp/v2/users | jq 
```

![Imgur](https://i.imgur.com/XMrODYS.png)

- - -

