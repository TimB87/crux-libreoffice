# crux-libreoffice

Early stage, expect footprint missmatches (especially regarding python3).
Please report errors.

# How to use

1. enable the REPO on your CRUX system
  * put crux-libreoffice.httpup and crux-libreoffice.pub in /etc/ports
  * edit /etc/prt-get.conf to contain "prtdir crux-libreoffice" before contrib
  * also allow scripts to be run or watch out for scripts you need to run (eg. when installing mysql)
2. *your first build?*
  * install python3 first and issue those commands afterwards (CRUX 3.4 as a basis):
  * `ln -s /usr/include/python3.6m /usr/include/python3.6` `ln -s /usr/include/python3.6m /usr/include/python3` `ln -s /usr/lib/pkgconfig/python-3.6.pc /usr/lib/pkgconfig/python3.pc`
  * the reason for that is that libixion and py3boost will fail to find python3 without them and the build will fail
  * *not your first build?*
    * if you have harfbuzz installed already, you need to rebuild it with graphite2 support
    * if you have cups installed already, this REPO contains a version which builds with avahi installed
3. `prt-get depinst libreoffice`
4. ???
5. Profit.

# Feedback

If anything is missing, needs fixing or lacks the feature you want, come find me on IRC (freenode) #crux, submit an issue here on github or write me an email.

# Screenshot

![screenshot](crux-libreoffice.png)
