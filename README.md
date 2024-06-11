CSF

CSF (ConfigServer Security & Firewall) is a free, advanced firewall tool designed for most Linux-based VPS/Cloud environments. In addition to basic packet filtering, CSF offers enhanced security features, including login intrusion and flood detection.

Login Security: If there are 10 unsuccessful login attempts, the IP address attempting the logins will be blocked by CSF. This blocking is determined based on the IP address and its subnet mask, preventing incoming traffic from that source.

Traffic Control: CSF allows you to specify which ports can be used for outgoing traffic. For example, you can permit only essential ports like 80, 443, and 587, enhancing your server's security.

Command Features: With CSF commands, you can manage IP addresses on the server firewall. This includes allowing, denying, blocking, and unblocking specific IPs, providing granular control over your server's security.

Overall, CSF provides robust security measures to protect your Linux-based VPS/Cloud environment from various threats.

Can refer to the Cheatcode.txt to know more about CSF cmd manipulations.
The csf.conf file have the started block mehanisum, which also provides the best standard practices to the in-house cloud servers.

Installation file help you to install the CSF on your cloud server, Which enhanances the security a bit high. If using a cloud platform like AWS, Azure or GCP by default they only provide the port blockings. 
but installing this CSF will provide wide range of blockings to the application.

If we only wants our application to be worked on certain locations, We can only allow those region on the country list we can gets leverage to the application.

The country code is a standard option, Where we can use it on the configuration file.

All the port, country blocks can be done via csf.conf file. In that file, we can find 

Allow incoming TCP ports & Allow incoming IPv6 TCP ports
Allow outgoing TCP ports & Allow outgoing IPv6 TCP ports

CC_DENY = "Can mention the country code"

Other blocking mehanisums are Allowing the port based access to the country code under,
CC_ALLOW_PORTS = "IN"
what are the ports needs to allowed on this country for access can mention under,
CC_ALLOW_PORTS_TCP = "21,3000, or any other required ports on the application"
