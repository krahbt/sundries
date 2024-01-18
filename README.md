sundries
=========================================

IP and IPv6 setup
-----------------------------------------
+ setup
  + dhcp_x5anyx7p3f_routeros.txt
  + icslap_ifdown_routeros.txt
    + UPnP IGD
  + ipv6_osefz7dhky_routeros.txt
    + radvd and DHCPv6
  + tunnelbroker_ifup_routeros.txt
    + DDNS
+ firewall
  + iptables_fxckiwrzan_routeros.txt
  + ip6tables_xjz6bh4spr_routeros.txt

password_tca_\*.txt and clock_tca_\*.txt
-----------------------------------------
while password_tca_\*.txt emulates Hash_DRBG, originally intended for
[an Android app](https://github.com/chrisgch/tca),
it should run on UNIX systems featuring "/dev/urandom".
characters of class [ 028IVlv] are excluded
from the password generator. 

before running these scripts,
put a personalization string, say 'abc' with quotes,
instead of a78ju3y1xh;
settle on a POSIX TZ string, say '\047<CET>-1<CEST>-2,M3.5.0,M10.5.0\047'
without quotes, instead of fdpen962jq;
settle on another POSIX TZ string, say '<CET>-1<CEST>-2,M3.5.0,M10.5.0'
with quotes, instead of q1mt7beqhi;
settle on a site, say 'https://site/id/name' without quotes,
to get the Date header via HTTPS, instead of j2fpqdcx7t; and
settle on randomness beacon, say 'https://site/id/name' without quotes,
instead of t4w5jeyckg.
