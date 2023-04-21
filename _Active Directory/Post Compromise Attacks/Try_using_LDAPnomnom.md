- - -
### LDAP Nom Nom : 
**Anonymously bruteforce Active Directory usernames from Domain Controllers by abusing LDAP Ping requests** (cLDAP)
Looks for enabled normal user accounts. No Windows audit logs generated. High speed ~ up to 10K/sec - go beyond 25K/sec with multiple servers!


### Installation : 

```go
go install github.com/lkarlslund/ldapnomnom@latest
```

### Usage : 

```sh
ldapnomnom --input 10m_usernames.txt --output results.txt --server 192.168.0.11 --parallel 4
```

```sh
# This is Fastest fucking Boy!!
ldapnomnom --input 10m_usernames.txt --output multiservers.txt --dnsdomain contoso.local --maxservers 32 --parallel 16
```

Explore it by yourself!! 😉😉😉

- - -

