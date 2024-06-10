## What is a Web Shell?

A `web shell` is a browser-based shell session we can use to interact with the underlying operating system of a web server. Again, to gain remote code execution via web shell, we must first find a website or web application vulnerability that can give us file upload capabilities. Most web shells are gained by uploading a payload written in a web language on the target server. The payload(s) we upload should give us remote code execution capability within the browser. The proceeding sections and challenges will primarily be focused on executing commands through our web shells in the browser. Still, it is essential to know that relying on the web shell alone to interact with the system can be unstable and unreliable because some web applications are configured to delete file uploads after a certain period of time. To achieve persistence on a system, in many cases, this is the initial way of gaining remote code execution via a web application, which we can then use to later upgrade to a more interactive reverse shell.

In the following few sections, we will learn and experiment with various web shells that allow us to interact with a web server's underlying OS through the web browser.

Webshells: 
[[Laudanum]]
[[Antak]]
[[PHP Shells]]
