TFTP

Trivial File Transfer Protocol (TFTP) is simpler than FTP and performs file transfers between client and server processes. However, it does not provide user authentication and other valuable features supported by FTP. In addition, while FTP uses TCP, TFTP uses UDP, making it an unreliable protocol and causing it to use UDP-assisted application layer recovery.

This is reflected, for example, in the fact that TFTP, unlike FTP, does not require the user's authentication. It does not support protected login via passwords and sets limits on access based solely on the read and write permissions of a file in the operating system. Practically, this leads to TFTP operating exclusively in directories and with files that have been shared with all users and can be read and written globally. Because of the lack of security, TFTP, unlike FTP, may only be used in local and protected networks.

Let us take a look at a few commands of TFTP:
Commands 	Description
- connect 	   Sets the remote host, and optionally the port, for file transfers.
- get             Transfers a file or set of files from the remote host to the local host.
- put 	           Transfers a file or set of files from the local host onto the remote host.
- quit 	   Exits tftp.
- status 	   Shows the current status of tftp, including the current transfer mode (ascii or                     binary), connection status, time-out value, and so on.
- verbose 	    Turns verbose mode, which displays additional information during file transfer, on or off.

Unlike the FTP client, TFTP does not have directory listing functionality.


  - Connect to an FTP server:
    ftp ftp.example.com

  - Connect to an FTP server specifying its IP address and port:
    ftp ip_address port

  - Switch to binary transfer mode (graphics, compressed files, etc):
    binary

  - Transfer multiple files without prompting for confirmation on every file:
    prompt off

  - Download multiple files (glob expression):
    mget *.png

  - Upload multiple files (glob expression):
    mput *.zip

  - Delete multiple files on the remote server:
    mdelete *.txt

  - Rename a file on the remote server:
    rename original_filename new_filename