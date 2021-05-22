# Mikrotik-UA-BlackList

To redirect traffic to blocked adresses to VPN connection you should write it name to variable VPNgw.

     :local VPNgw "pptp-bypass";

Also, You should have:
 - NAT rule for this interface
 - Set DNS to use ONLY Google DNS servers. Do not use ISP DNS'es

If you want to restart VPN on ecript run, set VPNReconnect variable to 'true'.

    :local VPNReconnect true;
