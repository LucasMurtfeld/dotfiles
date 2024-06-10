Search for S File:
`find / -user root -perm -4000 -exec ls -ldb {} \; 2>/dev/null`

Look for Creds in as ww-data:
`grep -arin 'DB_USER\|DB_PASSWORD' |awk -F':' '{print $1}' | sort | uniq -c`y