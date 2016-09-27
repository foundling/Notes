# Digital Ocean Domain Setup

+ Get a domain from a domain reseller like NameCheap, GoDaddy, etc.
+ Get a VPS through Digital Ocean, Linode, etc.

## Let's assume the following:

+ You use Digital Ocean for your VPS.
+ You've bought a domain name (mywebsite.com) through NameCheap.
+ You want to use digital ocean's nameservers and not those of your domain reseller. 
+ Your ip address is 132.180.381.110. (run 'ifconfig | grep addr' in a terminal on your VPS to find the ip address).

## Now do the following: 

+ Login to your Digital Ocean account and find the list of nameservers (ns1.digitalocean.com, ns2.digitalocean.com, etc).
+ Login to NameCheap and configure your DNS settings to use an external DNS service. Add the list digital ocean name servers there.
+ Back in your Digital Ocean account, go to the Networking configuration panel and add a domain.
+ In the domain configuration, for 'www.mywebsite.com', put '@' as the name in the A record field. Put the IP address of your VPS in the address field.
+ If the nameservers aren't automatically filled out for you, use the list of digital ocean name servers you found previously.
