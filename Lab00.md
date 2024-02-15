Ran into trouble while setting up PFSense, and was unable to ping google.com from the PFSense Shell. I was able to resolve this by going into WKS01 and finishing my firewall configuration via the web panel.

WAN Upstraem is 10.0.17.2

Had difficulty joining my domain: Username - administrator, password - Admin802!


Figured out the issue, where I was trying to use the username - riley

riley.bashaw-admin account - password - RB802802!

riley.bashaw uses Admin802!

Struggled to connect wks01-riley to the Domain, realized that my DNS on wks01-riley was still set to 10.0.5.2 so I changed it to 10.0.5.5.







