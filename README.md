sundries
=========================================
Android
-----------------------------------------
+ [Google System Release Notes](https://support.google.com/product-documentation/answer/14343500)
+ [Tags / Build IDs per AOSP](https://source.android.com/docs/setup/reference/build-numbers)
+ [mAvailableDoHProviders, or bootstrapping DoH Providers](https://android.googlesource.com/platform/packages/modules/DnsResolver/+/refs/tags/android-14.0.0_r21/PrivateDnsConfiguration.h#250)
  + DNS over TLS is supported since Android 9.0, while only servers listed in mAvailableDoHProviders are able to serve DNS over HTTPS when Private DNS specifies any mAvailableDoHProviders\[ind\]\[2\]. This is the case for Android 13.

IP and IPv6 setup
-----------------------------------------
+ setup
  + pppoe_nxwgh7m4zf_routeros.txt
    + PPPoE on CPE and common WAN services such as NTP
  + dhcp_x5anyx7p3f_routeros.txt
  + icslap_ifdown_routeros.txt
    + UPnP IGD
  + ipv6_osefz7dhky_routeros.txt
    + radvd and DHCPv6
  + tunnelbroker_ifup_routeros.txt
    + DDNS and RFC 1933
+ firewall
  + iptables_fxckiwrzan_routeros.txt
  + ip6tables_xjz6bh4spr_routeros.txt

password_tca_\*.txt and clock_tca_\*.txt
-----------------------------------------
while password_tca_\*.txt, emulating Hash_DRBG, is originally intended for
[an Android app](https://github.com/chrisgch/tca),
it should run on UNIX systems featuring "/dev/urandom".
characters of class \[ 028IVlv\] are excluded
from the password generator, in particular upper case i and lower case L.

before running these scripts,
put a personalization string, say 'abc' with quotes,
instead of a78ju3y1xh;
settle on a POSIX TZ string, say '\\047\<CET\>-1\<CEST\>-2,M3.5.0,M10.5.0\\047'
without quotes, instead of fdpen962jq;
settle on another POSIX TZ string, say '\<CET\>-1\<CEST\>-2,M3.5.0,M10.5.0'
alongside quotes, instead of q1mt7beqhi;
settle on a site, say 'https://site/id/name' without quotes,
to get the Date header via HTTPS, instead of j2fpqdcx7t; and
settle on a randomness beacon, say 'https://site/id/name' without quotes,
instead of t4w5jeyckg. settle on a nonce, and pass it to base64, which begets,
say "abc"; then put this value, alongside quotes, instead of buqoxj1ey5.

_kofpjw1ma3.txt takes a personalization string, while _md46o7eyt5.txt tosses a
timestamp to the mix. _utkafywcim.txt draws from a randomness beacon to boot.
however, due to a dearth of commands/utilities on Android, entropy sources are
mixed through an unkeyed MAC function, or just a simple hash function.
where available, try HMAC/UMAC/PBKDF2/yescrypt and friends instead.
