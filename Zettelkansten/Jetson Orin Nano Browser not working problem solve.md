---
tags: 
aliases: 
connected:
---
202507261518
# Jetson Orin Nano Browser not working problem solve
>The thing happened after update, upgrade.
>newest snap version not working properly with browsers like chromium, firefox..
>To solve it, downgrade snap.

```bash
~ » snap --version                                              thebeast@ubuntu
snap    2.70
snapd   2.70
series  16
ubuntu  22.04
kernel  5.15.148-tegra
--------------------------------------------------------------------------------
~ » snap download snapd --revision=24724                        thebeast@ubuntu
Fetching snap "snapd"
Fetching assertions for "snapd"
Install the snap with:
   snap ack snapd_24724.assert
   snap install snapd_24724.snap
--------------------------------------------------------------------------------
~ » sudo snap ack snapd_24724.assert                            thebeast@ubuntu
[sudo] password for thebeast: 
--------------------------------------------------------------------------------
~ » sudo snap install snapd_24724.snap                          thebeast@ubuntu
2025-07-26T15:17:04+09:00 INFO Waiting for automatic snapd restart...
snapd 2.68.5 from Canonical✓ installed
--------------------------------------------------------------------------------
~ » snap --version                                              thebeast@ubuntu
snap    2.68.5
snapd   2.68.5
series  16
ubuntu  22.04
kernel  5.15.148-tegra
-------------------------
```

after this, system work.


---
## References
[Jetsonhacks 3 Minute Fix for Chromium and other Snaps not launching](https://www.youtube.com/watch?v=x6bccF3xtRE)