
DNS enumeration:
`ffuf -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-20000.txt -u http://board.htb -H "Host: FUZZ.board.htb" -ic -t 200` 
`-c -fs 15949`

[[Identify Target OS by ICMP TTL]]