I Ran into trouble while setting up PFSense, and was unable to ping google.com from the PFSense Shell. I was able to resolve this by going into WKS01 and finishing my firewall configuration via the web panel.

WAN Upstraem is 10.0.17.2

Had difficulty joining my domain: Username - administrator, password - Admin802!


Figured out the issue, where I was trying to use the username - riley

riley.bashaw-admin account - password - RB802802!

riley.bashaw uses Admin802!

Struggled to connect wks01-riley to the Domain, realized that my DNS on wks01-riley was still set to 10.0.5.2 so I changed it to 10.0.5.5.


Topics I am interested in:

1.) I am very interested in learning more about PowerShell and its uses. I have experience with it, however I'd like to learn more about it's informational commands. For instance, the Get-Command has a lot of uses, and when researching how to get Deliverable 5 I found so many different options to achieve what I needed to.

2.) I'd also like to learn more about Domain Users. I understand that they have a purpose of providing a user that can be used within the Domain, but how much can they be used for within a larger network? Given what I've researched, they can be given access to specific computers and servers within a Domain, and potentially extended to specific network drives and so forth. Do they have additional purposes that the user can take advantage of?

3.) I'd still like to learn more about Reverse Lookup Zones. I can understand that it is used to map an IP with a domain, so I can understand why it's important, however, I'm curious about the additional applications of this. What it's meant for is enough reason to keep it secure, but I'm curious about what kind of threats can use this to their advantage in the Cybersecurity world.







