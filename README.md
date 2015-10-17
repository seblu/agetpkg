agetpkg
=======

Introduction
------------
**agetpkg** is a command line tool used to quickly list/get/install packages stored on the [Archlinux Archive](https://wiki.archlinux.org/index.php/Arch_Linux_Archive).

**agetpkg** means **A**rchive **G**et **P**ackage.

Usage
-----

###### Download a previous version of ferm package
```bash
agetpkg ferm
```

###### Download xterm version 296
```bash
agetpkg ^xterm 296
# or
agetpkg -g ^xterm 296
```

###### List all zsh versions
```bash
agetpkg -l zsh$
```

###### Install all gvfs packages in version 1.26.0 release 3
```bash
agetpkg -i gvfs 1.26.0 3
```

###### Download all pwgen packages
```bash
agetpkg -g -a pwgen
```

###### List only i686 packages of nftables
```bash
agetpkg -l -A i686 -- nftables
```

###### Force update of the index before listing packages matching i3
```bash
agetpkg -u -l i3-wm
```

###### Use another archive url
```bash
agetpkg --url http://archlinux.arkena.net/archive/packages/.all/ -l bash$
```
or
```bash
export ARCHIVE_URL=http://archlinux.arkena.net/archive/packages/.all/
agetpkg -l bash$
```

###### Run agetpkg in debug mode
```bash
agetpkg --debug -l coreutils
```

###### Display current version
```bash
agetpkg --version
```

Installation
------------

To install the current released version of **agetpkg**, run:
```bash
pacman -S agetpkg
```

To install the git development version, run:
```bash
makepkg -i
```

Dependencies
------------
- [Python 3.x](http://python.org/download/releases/)
- [PyXDG](http://freedesktop.org/wiki/Software/pyxdg)

Sources
-------
**agetpkg** sources are available on [github](https://github.com/seblu/agetpkg/).

License
-------
**agetpkg** is licensied under the term of [GPL v2](http://www.gnu.org/licenses/gpl-2.0.html).

AUTHOR
------
**agetpkg** was started by Sébastien Luttringer in September 2015.
