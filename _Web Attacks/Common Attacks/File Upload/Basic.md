- - -
### Useful Guide/Tool : 

- [ ] Check Out [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Upload%20Insecure%20Files)
- [ ] Check Out This [Tool](https://github.com/almandin/fuxploider). 
- - -

### By Alh4zr3d : 

If you have file upload but **.php** files are disallowed.  Try this : 
![Imgur](https://i.imgur.com/WvlPKX8.png)

What you have to do, is create a file named "**.htaccess**" with the following contents : 

```
AddType application/x-httpd-php .cth
```

And then upload this "**.htaccess**" file first.

#### What this is doing ?? 
This simple .htaccess file is going to be uploded and saved on the target.
Then it will change some rules their. 👹 👹 👹 

Now, You can upload for example : **.cth** file here, after upload that **.cth** file will act and work as **.php** file. 

- - -




