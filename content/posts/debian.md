---
title: "Debian"
date: 2020-10-26T22:42:09+01:00
draft: false
---



[main](https://main.com).[features](https://features.com).[VPNsupport](https://VPNsupport.com).[Hacking](https://Hacking.com).[Translations](https://Translations.com).[Suppoort](https://Support.com)

### Distro specific NetworkManager notes: Debian

These instructions assume you are running Debian Unstable. At the time of writing, some of the packages necessary to compile are only available in experimental.  
Add:  

> **deb http://ftp.debian.org/debian experimental main contrib non-free**  

>to **/etc/apt/sources.list,**
and run 

>aptitude update  

1. Install build-essential, gnome-common, automake1.9, libglib2.0-dev, libgtk2.0-dev, libglade2-dev, libgconf2-dev, libgnome-keyring-dev, libgnomeui-dev, libiw-dev, libnl-dev, and git-core from Unstable:  

>aptitude install build-essential gnome-common automake1.9 libglib2.0-dev libgtk2.0-dev libglade2-dev libgconf2-dev libgnome-keyring-dev libgnomeui-dev libiw-dev libnl-dev git-core ppp-dev  

2. Install libdbus-glib-1-dev from Experimental  

>aptitude -t experimental install libdbus-glib-1-dev

3. Check out a copy of the source code  

>git clone git://git.freedesktop.org/git/NetworkManager/NetworkManager.git  

4. In the new source directory, generate the configure scripts  

>cd NetworkManager
>
>./autogen.sh  

5. Build!  

>make
>
>make install  





