UnBlock - Website block/block using OpenWrt DNS blocking. This simple script uses OpenWrt uci to block and unblock websites.

Prerequisite: Access to router running OpenWrt.

Install:
Copy unblock to router at /www/cgi-bin/unblock

Create unblocklist file at /etc/config/unblocklist. These are sites you can see when unblocked.
```
youtube.com
```

Create blocklist file at /etc/config/blocklist.  These are sites you never want to see.
```
badsite.com
```

blocklist can also contain overrides for a sub-domain of a domain which is blocked elsewhere, that you actually need. We override with another known DNS server. Google relies on accounts.youtube.com for google authentication. That is the main example.
```
accounts.youtube.com/8.8.8.8
```

Unblock URL is at:

https://router/cgi-bin/unblock

Device MAC addresses allowed to unblock should be placed at /etc/config/unblock_allow.txt
```
YOURMACADDRESS
```
