# Mikrotik-UA-BlackList

To redirect traffic to blocked adresses to some interface you should write it name to variable blackholeGw.

     :local blackholeGw "ether4";

Also, You should have:
 - NAT rule for this interface
 - Set DNS to use ONLY Google DNS servers. Do not use ISP DNS'es

If you want to restart interface on script run, set blackholeGwReconnect variable to 'true'.

    :local blackholeGwReconnect true;
