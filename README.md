# News
All of this has been moved to contrib, this REPO will be archived and not be maintained anymore.

# crux-libreoffice

This should be fairly easy to build with CRUX 3.5 and there are no errors to be expected as of now.
Please report errors.

For information about libreoffice, visit [their Website](https://www.libreoffice.org/)
# How to use

1. enable the REPO on your CRUX system
  * put crux-libreoffice.httpup and crux-libreoffice.pub in /etc/ports
  * edit /etc/prt-get.conf to contain "prtdir /usr/ports/crux-libreoffice"
  * also allow scripts to be run or watch out for scripts you need to run (eg. when installing mysql)
2. what else to check?
  * *your first build?*
    * ~~Install python3 first and issue those commands afterwards (CRUX 3.5 as a basis):~~
    * ~~`ln -s /usr/include/python3.7m /usr/include/python3.7` `ln -s /usr/include/python3.7m /usr/include/python3` `ln -s /usr/lib/pkgconfig/python-3.7.pc /usr/lib/pkgconfig/python3.pc`~~
    * ~~the reason for that is that libixion and py3boost will fail to find python3 without them and the build will fail~~
    * this all should not be needed anymore
  * *not your first build?*
    * if you have harfbuzz installed (`prt-get isinst harfbuzz harfbuzz-icu`) already, you need to rebuild it with graphite2 support
    * `prt-get depinst ragel graphite2 && prt-get update -fr harfbuzz harfbuzz-icu`
3. `prt-get depinst libreoffice`
4. ???
5. Profit.

# Feedback

If anything is missing, needs fixing or lacks the feature you want, come find me on IRC (freenode) #crux, submit an issue here on github or write me an email.

# To Do:
With all that, it should be fairly easy to get an easy port for collabora-online.

# Screenshot

![screenshot](crux-libreoffice.png)
