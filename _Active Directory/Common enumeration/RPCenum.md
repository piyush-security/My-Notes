- - -
### Tool Discription : 📃
- Allows the **domain information enumeration** **through** protocol **RPC** ( Remote Procedure Call ).
- It allowed enumeration using a _Null Session_ ( no authentication ) if the target machine allowed it.
- And If you have a **domain user** credential then, this will give better results.
- This utility us **will allow you to obtain the following information** of a domain :- 
	-   Domain users
	-   Users of the domain with information
	-   Domain administrators users
	-   Domain groups
	-   Domain groups and users who belong to them
	-   Users of the domain and groups to which they intend

- - -
### Installation : 

```sh
git clone https://github.com/RipFran/rpcenum.git ; cd rpcenum/ ; chmod 755 ./rpcenum
```

## Usage : 

Commands.
```sh
sudo ./rpcenum -h
sudo ./rpcenum -i 10.10.101.10 -u 'rocky' -p 'Password123' -e DUsers
sudo ./rpcenum -N  -i 10.10.10.10 -e DUsersinfo
sudo ./rpcenum -i 10.10.101.10 -u 'rocky' -p 'Password123' -e DAUsers
sudo ./rpcenum -i 10.10.101.10 -u 'rocky' -p 'Password123' -e DGroups
sudo ./rpcenum -i 10.10.101.10 -u 'rocky' -p 'Password123' -e DUsersbyGroups
sudo ./rpcenum -i 10.10.101.10 -u 'rocky' -p 'Password123' -e DGroupsbyUser
sudo ./rpcenum -N -i 10.10.10.169 -e All

# any many more..4
```

![Imgur](https://i.imgur.com/Ti4nTzI.png)

![Imgur](https://i.imgur.com/iMQ7bz7.png)

- - -


