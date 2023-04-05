- - -
### Online Hosted : 

My favorite 😍.
- Best Hirarchy OSINT Framework is https://osintframework.com/
- 

#### BBOT : 
https://github.com/blacklanternsecurity/bbot

Installation : 
```python
pip install bbot
```

Usage : 
```sh
# subdomains
bbot -t evilcorp.com -f subdomain-enum

# subdomains (passive only)
bbot -t evilcorp.com -f subdomain-enum -rf passive

# subdomains + port scan + web screenshots
bbot -t evilcorp.com -f subdomain-enum -m naabu gowitness -n my_scan -o .

# subdomains + basic web scan (wappalyzer, robots.txt, iis shortnames, etc.)
bbot -t evilcorp.com -f subdomain-enum web-basic

# subdomains + web spider (search for emails, etc.)
bbot -t evilcorp.com -f subdomain-enum -c web_spider_distance=2 web_spider_depth=2

# everything at once because yes
# subdomains + emails + cloud + port scan + non-intrusive web + web screenshots + nuclei
bbot -t evilcorp.com -f subdomain-enum email-enum cloud-enum web-basic -m naabu gowitness nuclei --allow-deadly

# list modules
bbot -l
```

- - -
