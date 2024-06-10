[[msfvenom]]

#### Modules

The Modules detailed above are split into separate categories in this folder. We will go into detail about these in the next sections. They are contained in the following folders:

Introduction to Metasploit

```shell-session
NivaLada@htb[/htb]$ ls /usr/share/metasploit-framework/modules

auxiliary  encoders  evasion  exploits  nops  payloads  post
```

#### Plugins

Plugins offer the pentester more flexibility when using the `msfconsole` since they can easily be manually or automatically loaded as needed to provide extra functionality and automation during our assessment.

Introduction to Metasploit

```shell-session
NivaLada@htb[/htb]$ ls /usr/share/metasploit-framework/plugins/

aggregator.rb      ips_filter.rb  openvas.rb           sounds.rb
alias.rb           komand.rb      pcap_log.rb          sqlmap.rb
auto_add_route.rb  lab.rb         request.rb           thread.rb
beholder.rb        libnotify.rb   rssfeed.rb           token_adduser.rb
db_credcollect.rb  msfd.rb        sample.rb            token_hunter.rb
db_tracker.rb      msgrpc.rb      session_notifier.rb  wiki.rb
event_tester.rb    nessus.rb      session_tagger.rb    wmap.rb
ffautoregen.rb     nexpose.rb     socket_logger.rb
```

#### Scripts

Meterpreter functionality and other useful scripts.

Introduction to Metasploit

```shell-session
NivaLada@htb[/htb]$ ls /usr/share/metasploit-framework/scripts/

meterpreter  ps  resource  shell
```

#### Tools

Command-line utilities that can be called directly from the `msfconsole` menu.

Introduction to Metasploit

```shell-session
NivaLada@htb[/htb]$ ls /usr/share/metasploit-framework/tools/

context  docs     hardware  modules   payloads
dev      exploit  memdump   password  recon
```


![[Pasted image 20240606022920.png]]