First you enable SNMP Service on pfSense.
Go to 10.0.5.2 on wks01 and login to pfSense panel.
Services>SNMP

I enabled the "SNMP Daemon and its controls", set the system Contact as Riley Bashaw, Read Community String as "SYS265", and Bind Interface as LAN.

Restarted the SNMP Service by using the Red restart button at the top of the page within Service/SNMP.

Used nmtui to configure network and hostname for nmon01.

Added user Riley to nmon01 using adduser and passed.

Managed to add nmon01 to the AD Domain using command from source:
https://www.rootusers.com/how-to-join-centos-linux-to-an-active-directory-domain/  

yum install sssd realmd oddjob oddjob-mkhomedir adcli samba-common samba-common-tools krb5-workstation openldap-clients policycoreutils-python -y

Then after successful download:

[root@centos7 ~]# realm join --user=riley.bashaw-adm riley.local

This would get me added to the AD Domain Computers list.

_BE SURE TO USE PROPER CAPITALIZATION FOR SSH USERNAME!!!_

Use nslookup to check if 10.0.5.2 is added to the lookup, and add it if need be.

use _sudo yum install net-snmp-utils to install the snmp_ service.

Use _snmpwalk -Os -c SYS265 -v2c fw01-riley system_ to check the SNMP values from fw01-riley.

Edit the snmpd.conf file to say the following:
![image](https://github.com/RileyBashaw/SYS265/assets/112733012/d25838f5-82de-4297-b8f2-3be31884030b)


Add Firewall port 161/udp and restart services on web01.


Add SNMP to all computers, to both mgmt01 and ad01 via Server Manager on mgmt01.

Add SYS265 to Security as a community under SNMP Services under Computer Management on ad01-riley, and accept packets only from nmon01-riley. Restart to apply!

3 Topics/Articles:

I was unfamiliar with SNMP prior to this lab, so I did a lot of searching to find out what I was doing wrong and what I may have been missing. So I did "yum install net-snmp" before installing the additional tools within the lab, thanks to this reference.
https://superuser.com/questions/1222811/not-able-to-install-snmp-on-centos 

I was also a little bit unfamiliar with adding a CentOS linux machine to an Active Directory Domain due to not doing it enough. I found that researching it gave me the perfect solution.
https://www.rootusers.com/how-to-join-centos-linux-to-an-active-directory-domain/

I was also unfamiliar with Vi by comparison to Nano as a text editor, where I learned from a source I found that ":wq" is save and exit, and "i" is insert mode. I also learned that ":w" allows you to save and continue editing.
https://www.redhat.com/sysadmin/introduction-vi-editor






