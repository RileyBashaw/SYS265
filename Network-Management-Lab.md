First you enable SNMP Service on pfSense.
Go to 10.0.5.2 on wks01 and login to pfSense panel.
Services>SNMP

I enabled the "SNMP Daemon and its controls", set the system Contact as Riley Bashaw, Read Community String as "SYS265", and Bind Interface as LAN.

Restarted the SNMP Service by using the Red restart button at the top of the page within Service/SNMP.

Used nmtui to configure network and hostname for nmon01.

Added user Riley to nmon01 using adduser and passed.


