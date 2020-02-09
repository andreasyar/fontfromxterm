# Font from xterm guide

Guide how to use font from xterm at modern terminal emulator

## Getting Started

I very like to use good old Fixed SemiCondensed 6x13 font which you can see in xterm. In early days after googling sometimes, all I found is recommendations to use Terminus font. Terminus font is good but it looks not exactly like font in xterm. So I continued to search time for time and finally I found a solution what I will like to share with you.

### Prerequisites

Personally I use Fedora distro, MATE desktop and MATE Terminal as terminal emulator. But I think what this solution can be applied to many other distros and DE's

### Installing

Install X11 misc fonts package:

```
# dnf install xorg-x11-fonts-misc
```

Create file /etc/fonts/local.conf and past following code into it:

```
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
        <dir>/usr/share/X11/fonts/misc</dir>
</fontconfig>
```

Refresh fonts information cache:

```
# fc-cache -f -v
```

**You must close all instances of terminal emulator to changes take effect**

Go to terminal emulator font settings and choose font "Fixed SemiCondensed" size 10

## Tested in

* Fedora 23
* Fedora 28
* Fedora 29
* Fedora 30