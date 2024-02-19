The term kill chain is a military concept related to the structure of an attack. It consists of target identification, decision and order to attack the target, and finally the target destruction.


- Reconnaissance
- Weaponization
- Delivery
- Exploitation
- Installation
- Command & Control
- Actions on Objectives 



### Reconnaissance 
is discovering and collecting information on the system and the victim. The reconnaissance phase is the planning phase for the adversaries.
OSINT (Open-Source Intelligence) also falls under reconnaissance.

### Weaponization 
combines malware and exploit into a deliverable payload. 

### Delivery
- phishing email 
- malicious usb infection
- watering hole attack


### exploitation

- The victim triggers the exploit by opening the email attachment or clicking on a malicious link.
- Using a zero-day exploit.
- Exploit software, hardware, or even human vulnerabilities. 
- An attacker triggers the exploit for server-based vulnerabilities. 



### Installation 
- attacks tries to create  a backdoor for persistant access.
- Installing a web shell on the webserver. 
- attacker can use Meterpreter to install a backdoor on the victim's machine. 
- entry to the "run keys" for the malicious payload in the Registry or the Startup Folder.  everytime user logs on to computer
- Timestomping to change the timestamp of the file to trick the forensic investigator.


###  Comand and control
- beacon system consistent connection

### Exfileration
- Collect credentials
- privilege escalation
- lateral movement
- delete shadow files/backups
