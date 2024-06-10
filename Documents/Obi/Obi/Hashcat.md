hashcat -m 3200 -a 0 /home/niva/htb/labs/runner/hash --wordlist /usr/share/seclists/Passwords/rockyou.txt

We can use a very powerful tool called [Hashcat](https://hashcat.net/hashcat/) to combine lists of potential names and labels with specific mutation rules to create custom wordlists. To become more familiar with Hashcat and discover the full potential of this tool, we recommend the module [Cracking Passwords with Hashcat](https://academy.hackthebox.com/course/preview/cracking-passwords-with-hashcat). Hashcat uses a specific syntax for defining characters and words and how they can be modified. The complete list of this syntax can be found in the official [documentation](https://hashcat.net/wiki/doku.php?id=rule_based_attack) of Hashcat. However, the ones listed below are enough for us to understand how Hashcat mutates words.

|**Function**|**Description**|
|---|---|
|`:`|Do nothing.|
|`l`|Lowercase all letters.|
|`u`|Uppercase all letters.|
|`c`|Capitalize the first letter and lowercase others.|
|`sXY`|Replace all instances of X with Y.|
|`$!`|Add the exclamation character at the end.|

Each rule is written on a new line which determines how the word should be mutated. If we write the functions shown above into a file and consider the aspects mentioned, this file can then look like this:

#### Generating Rule-based Wordlist
[[CeWL]]

Password Mutations

```shell-session
NivaLada@htb[/htb]$ hashcat --force password.list -r custom.rule --stdout | sort -u > mut_password.list
NivaLada@htb[/htb]$ cat mut_password.list

password
Password
passw0rd
Passw0rd
p@ssword
P@ssword
P@ssw0rd
password!
Password!
passw0rd!
p@ssword!
Passw0rd!
P@ssword!
p@ssw0rd!
P@ssw0rd!
```

#### Hashcat Existing Rules

Password Mutations

```shell-session
NivaLada@htb[/htb]$ ls /usr/share/hashcat/rules/

best64.rule                  specific.rule
combinator.rule              T0XlC-insert_00-99_1950-2050_toprules_0_F.rule
d3ad0ne.rule                 T0XlC-insert_space_and_special_0_F.rule
dive.rule                    T0XlC-insert_top_100_passwords_1_G.rule
generated2.rule              T0XlC.rule
generated.rule               T0XlCv1.rule
hybrid                       toggles1.rule
Incisive-leetspeak.rule      toggles2.rule
InsidePro-HashManager.rule   toggles3.rule
InsidePro-PasswordsPro.rule  toggles4.rule
leetspeak.rule               toggles5.rule
oscommerce.rule              unix-ninja-leetspeak.rule
rockyou-30000.rule
```

