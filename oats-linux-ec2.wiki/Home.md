#Oracle Application Testing Suite on Linux

###Introduction
The May 2012 release of Oracle Application Testing Suite (OATS) now has a Linux version of the 
OATS server. In the past the server application was only available for Windows. 
In an effort to evaluate this new Linux option, this project will prove these install 
procedures while creating a persistent OATS server hosted in the Amazon EC2 environment.

Amazon EC2 can provide an on demand hosted server that is ideal for occasional tasks. 
For many OATS testing needs there is little reason to dedicate full time virtual or physical machine resources.
Pricing for non mission-critical needs, such as for OATS evaluation, are 4¢ per hour with EC2 spot instances.
For higher reliability needs the costs start at 16¢ per hour for an EC2 medium machine instance, 
though [EC2 pricing](http://aws.amazon.com/ec2/pricing/) varies depending on CPU and memory configuration. 
Bandwidth costs are not a consideration with the goal of only testing the web application which is already
included in the OATS install.

This tutorial is aimed at evaluating OATS on an 
[Amazon image](https://aws.amazon.com/amis/oracle-database-11g-release-2-11-2-0-1-standard-edition-one-64-bit) 
which has been pre-built by Oracle with Linux and 11g Database.
Linux and Database configuration is not necessary. 
My selection of versions for Linux and Oracle Database were somewhat arbitrary, 
since most are able to meet the minimal OATS requirements. 
 
The entire procedure can be completed in less than 30 minutes. 
In the end you will have a single machine provisioned with Oracle Enterprise Linux Release 5, 
Oracle Database 11g Standard Edition One, and
Oracle WebLogic 11g Application Server hosting the 12.1.0.1 version of Oracle Application Suite application.
 
### Security 
Secure access is achieved though SSH public/private rsa [key pairing as 
configured](http://docs.amazonwebservices.com/AWSSecurityCredentials/1.0/AboutAWSCredentials.html#EC2KeyPairs) in your EC2 account. 
All these install steps and OATS server evaluation will be secure through this mechanism. 
This allows for secure access to the OATS interface from your local web browser. 
Tunnelled VNC access to the Linux machine is included, though not necessary.
As with any Linux distribution, secure access can be strengthened (or weakened) to meet particular needs. 



