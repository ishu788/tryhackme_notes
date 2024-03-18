## Queries
- whois
- dig
- nslookup


Reconnaissance (recon) can be defined as a preliminary survey to gather information about a target. It is the first step in The Unified Kill Chain to gain an initial foothold on a system. We divide reconnaissance into:

In passive reconnaissance, you rely on publicly available knowledge. It is the knowledge that you can access from publicly available resources without directly engaging with the target. Think of it like you are looking at target territory from afar without stepping foot on that territory.


Active reconnaissance, on the other hand, cannot be achieved so discreetly. It requires direct engagement with the target. Think of it like you check the locks on the doors and windows, among other potential entry points.


https://dnsdumpster.com/

https://www.shodan.io/


telnet ip port
GET / HTTP/1.1
host: telnet



52 - DNS
22 - SSH


## Advanced Nmap

3 types of scan
 - null scan   nmap -sN target
 - fin scan    nmap -sF target
 - xmas scan   nmap -sX target
 - maimon scan nmap -sM target
 - ack scan    namp -sA target
 - windows scan     -sW
 - zombie scan      -sI
 - version scan     -sV

 ## different script categories.
 - auth,brute, dos, exploit, vuln

## To attack ftp 

 hydra -l eddie -P /usr/share/wordlists/rockyou.txt ftp://10.10.9.160:10021

 hydra -l username -P passwordlist ftp://ip:port


 # always use -sN null scan to avoid detection /firewalls
 
 


