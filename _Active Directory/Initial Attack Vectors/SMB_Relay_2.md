- - -
### Installation : 
Github Link : [Here](https://github.com/skorov/ridrelay)

```sh
pipenv install
pipenv shell

# Optional: Run if installing impacket
git submodule update --init --recursive
cd submodules/impacket
pip install .
cd ../..
```

### Usage : 

> [! attention] 
> - Find a target host to relay to.
> - The target must be a member of the domain and **MUST** have **SMB Signing off**.
> - [CrackMapExec](https://github.com/byt3bl33d3r/CrackMapExec) can get this info for you very quick!

```python
python ridrelay.py -t 10.0.0.50
python ridrelay.py -t 10.0.0.50 -o path_to_output.txt
```

> [! tip]
> - Start [Responder](https://github.com/SpiderLabs/Responder) to trick users to connecting to RidRelay


- - -
