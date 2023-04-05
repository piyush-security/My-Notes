- - -
### Installation : 

```sh
curl -s https://raw.githubusercontent.com/killswitch-GUI/SimplyEmail/master/setup/oneline-setup.sh | bash
cd SimplyEmail ; ./SimplyEmail.py

# -----------------OR--------------------------#

git clone --branch dev https://github.com/killswitch-GUI/SimplyEmail.git
cd SimplyEmail ; ./setup/setup.sh
cd .. ; cd SimplyEmail ; ./SimplyEmail.py
```

### Usage : 

#### Finding Emails without APIs : 

Simple and verbose use.
```python
./SimplyEmail.py -all -e cybersyndicates.com
./SimplyEmail.py -all -v -e cybersyndicates.com
```

Find and Verify Emails Too.
```python
./SimplyEmail.py -all -v -verify -e cybersyndicates.com 
./SimplyEmail.py -all -v -verify -n -e cybersyndicates.com 
```



