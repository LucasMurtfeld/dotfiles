#### Move a Copy for Modification

Antak Webshell

```shell-session
NivaLada@htb[/htb]$ cp /usr/share/nishang/Antak-WebShell/antak.aspx /home/administrator/Upload.aspx
```

Make sure you set credentials for access to the web shell. Modify `line 14`, adding a user (green arrow) and password (orange arrow). This comes into play when you browse to your web shell, much like Laudanum. This can help make your operations more secure by ensuring random people can't just stumble into using the shell. It can be prudent to remove the ASCII art and comments from the file. These items in a payload are often signatured on and can alert the defenders/AV to what you are doing.

#### Modify the Shell for Use

![image](https://academy.hackthebox.com/storage/modules/115/antak-changes.png)