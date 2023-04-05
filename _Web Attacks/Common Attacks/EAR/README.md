- - -
## Theory 📝📚
Execution After Redirect (EAR) is **an attack where an attacker ignores redirects and retrieves sensitive content intended for authenticated users**. A successful EAR exploit can lead to complete compromise of the application.

- - -
# Exploitation Steps : 

Here The website is https://example.com 

There is a page for Example : https://example.com/admin/index.php  which is onl;y readable by authenticated users.
If we try to visit https://example.com/admin/index.php , without authenticating then the webapp will redirect us to https://example.com/admin/login.php. 

- Open Burpsuite.
- Visit the URL restricted. here : https://example.com/admin/index.php
- Capture in burp.
- **Do intercept the responce**.
- Modify the Headers. ( **200 OK** and remove **location** parameter ).
- If there is any **JavaScript in Responce Code** like this : 

![Imgur](https://i.imgur.com/NQWEsBb.png)

- **Delete/Remove** this Javascript code.

- - -


