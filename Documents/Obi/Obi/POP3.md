

## Default Configuration

Both IMAP and POP3 have a large number of configuration options, making it difficult to deep dive into each component in more detail. If you wish to examine these protocol configurations deeper, we recommend creating a VM locally and install the two packages `dovecot-imapd`, and `dovecot-pop3d` using `apt` and play around with the configurations and experiment.

In the documentation of Dovecot, we can find the individual [core settings](https://doc.dovecot.org/settings/core/) and [service configuration](https://doc.dovecot.org/configuration_manual/service_configuration/) options that can be utilized for our experiments. However, let us look at the list of commands and see how we can directly interact and communicate with IMAP and POP3 using the command line.

#### POP3 Commands

|**Command**|**Description**|
|---|---|
|`USER username`|Identifies the user.|
|`PASS password`|Authentication of the user using its password.|
|`STAT`|Requests the number of saved emails from the server.|
|`LIST`|Requests from the server the number and size of all emails.|
|`RETR id`|Requests the server to deliver the requested email by ID.|
|`DELE id`|Requests the server to delete the requested email by ID.|
|`CAPA`|Requests the server to display the server capabilities.|
|`RSET`|Requests the server to reset the transmitted information.|
|`QUIT`|Closes the connection with the POP3 server.|