#  DomainsCompanys

List of domains related to technology companies for filtering

The objective of this repository is to provide the list of domains associated with each service provider or hardware manufacturer, with the purpose of being able to be managed by network filtering tools.

With this information, rules can be defined in a firewall, pihole, hosts file or any other tool that allows or block access from devices.

For a complete solution applied to all types of devices, I particularly apply a solution based on the implementation of rules in a physical firewall between the router that provides internet access and the local network to block DNS access by other devices that are not PiHole itself, since many of these their own name resolvers do not allow configuration bypass. An example can be seen in the following video:

https://www.youtube.com/shorts/wiDZuIql-mM

And to control the connections of the mobile terminals, I always use them connected through VPN to the network in which I have the PiHole, so that all the traffic is filtered.

Router <-> Firewall <-> [Local Network(PiHole+VPN)]

# Hosts file rules:
Modify with administration privileges the system hosts file located at:
Linux: /etc/hosts
Windows: \Windows\System32\drivers\etc\hosts
Mac: /private/etc/hosts

With the following content to block access, for example, to Facebook:
127.0.0.1 facebook.com
127.0.0.1 fb.com
127.0.0.1 fbcdn.net

# PiHole rules example:
![plot](https://github.com/baeksnip/DomainsCompanys/blob/main/images/01_create_group.jpg)
![plot](https://github.com/baeksnip/DomainsCompanys/blob/main/images/02_group.jpg)
![plot](https://github.com/baeksnip/DomainsCompanys/blob/main/images/03_rules.jpg)
