# lightdm-webkit-theme-rotating-rubix


## Overview

WebGL LightDM Webkit Greeter Theme based on official LightDM Webkit Greeter Theme of Antergos Linux

Original can be found [here](https://github.com/Antergos/lightdm-webkit-theme-antergos). All credit goes to the great people who 
created, run, and maintain [Antergos](http://antergos.com).

## Screenshots
<img src="Screenshot.png" alt="screenshot1" />

## Prerequisites

* lightdm
* [web-greeter](https://github.com/JezerM/web-greeter)/[nody-greeter](https://github.com/JezerM/nody-greeter)

Enable `nody-greeter`/`web-greeter` by editing `/etc/lightdm/lightdm.conf` and setting `greeter-session` property to `nody-greeter` or `web-greeter` :

```
[SeatDefaults]
#greeter-session=lightdm-gtk-greeter
greeter-session=nody-greeter
user-session=your-session (gnome,cinnamon,xfce...)

```

# Installation

Can be installed through the [AUR](https://aur.archlinux.org/packages/lightdm-webkit-theme-luminos/).

To select rotating-rubix as default theme just change the `theme: greeter_theme`  in `/etc/lightdm/web-greeter.yml`
to `theme: rotating-rubix`.

# Uninstallation

To uninstall, simply restore the `greeter-session` property of the `/etc/lightdm/lightdm.conf` file and restart your computer (or at least lightdm).

You may also want to :
* Remove the folder `rotating-rubix` which was created in `/usr/share/lightdm-webkit/themes/`
* Restore the `webkit-theme` property of the `/etc/lightdm/lightdm-webkit-greeter.conf` file

# User icons management

To change users icons, there are two options :

* Create a `.face` file in the user's home folder in which you put a `jpg` or `png` resource

Or 

* Create a resource named with the user's login in `/var/lib/AccountsService/icons/`
* Edit `/var/lib/AccountsService/users/<userLogin>` and add a property `Icon` targeting the icon resource you just created

Read more at the [ArchWiki LightDM][3] page.
