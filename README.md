# Mikrotik-UA-BlackList

Based on https://gist.github.com/uablacklist and https://uablacklist.net/ service.

Additions:
 - More informative logging, debugging and statistics.
 - Optimized for less disk operations and more memory operation (save our flash lifetime).
 - Intellectual rule processing. Do not touch unchangeable rules.
 - Interface workaround
 - different modes available: 
   - "route" create rules in routing table
   - "firewall" create rules in firewall address list table

To redirect traffic to blocked adresses to some interface you should write it name to variable blackholeGw.

     :local blackholeGw "ether4";

Also, You should have:
 - NAT rule for this interface
 - Set DNS to use ONLY Public DNS servers. Do not use your ISP DNS'es

If you want to restart interface on script run, set blackholeGwReconnect variable to 'true'.

    :local blackholeGwReconnect true;

Mode selection. "route" and "firewall"

    :local blackholeMode "firewall"
