We can now use another tool called [CeWL](https://github.com/digininja/CeWL) to scan potential words from the company's website and save them in a separate list. We can then combine this list with the desired rules and create a customized password list that has a higher probability of guessing a correct password. We specify some parameters, like the depth to spider (`-d`), the minimum length of the word (`-m`), the storage of the found words in lowercase (`--lowercase`), as well as the file where we want to store the results (`-w`).

#### Generating Wordlists Using CeWL

Password Mutations

```shell-session
NivaLada@htb[/htb]$ cewl https://www.inlanefreight.com -d 4 -m 6 --lowercase -w inlane.wordlist
NivaLada@htb[/htb]$ wc -l inlane.wordlist

326
```

