Development environment
=======================

This page explains how to set up a development environment oriented toward
Python development.


Tools
-----

* bash or zsh
* tmux
* vim
* git


Windows
-------


Cygwin
~~~~~~

Standard Unix tools can be installed on Windows workstations through
`Cygwin <https://cygwin.com/>`_.

Installed packages:

.. code-block:: console

    $ cygcheck -c -d | awk '{ if (NR > 2) { packages = packages ? packages "," $1 : $1 } } END { print packages }'
    _autorebase,_update-info-dir,adwaita-icon-theme,adwaita-themes,alternatives,autobuild,autoconf,autoconf2.1,autoconf2.5,autogen,automake,automake1.10,automake1.11,automake1.12,automake1.13,automake1.14,automake1.15,automake1.4,automake1.5,automake1.6,automake1.7,automake1.8,automake1.9,base-cygwin,base-files,bash,bash-completion,binutils,bzip2,ca-certificates,cfv,coreutils,crypt,csih,curl,cygrunsrv,cygutils,cygwin,cygwin-devel,dash,dbus,dbus-x11,ddd,desktop-file-utils,diffutils,dos2unix,doxygen,dri-drivers,editrights,file,findutils,font-adobe-dpi100,font-adobe-dpi75,font-alias,font-bh-lucidatypewriter-dpi75,font-misc-misc,gamin,gawk,gdb,gdk-pixbuf2.0-svg,getent,git,git-completion,git-gui,git-review,gitk,gnome-menus,gnupg,googlecl,grep,groff,gsettings-desktop-schemas,gtk-update-icon-cache,gtk2.0-engines-pixmap,gvim,gzip,hicolor-icon-theme,hostname,indent,inetutils,inetutils-server,info,ipc-utils,ipcalc,irssi,less,lftp,libargp,libatk1.0_0,libattr1,libblkid1,libbz2_1,libcairo2,libcatgets1,libclang,libcom_err2,libcroco0.6_3,libcrypt0,libcurl4,libdatrie1,libdb5.3,libdbus1_3,libedit0,libEGL1,libevent2.0_5,libexpat1,libfam0,libffi6,libfontconfig1,libfontenc1,libfreetype6,libgcc1,libgdbm4,libgdk_pixbuf2.0_0,libGL1,libglapi0,libglib2.0_0,libgmp10,libgnome-menu3_0,libgnutls28,libgraphite2_3,libgssapi_krb5_2,libgtk2.0_0,libguile17,libharfbuzz0,libhogweed2,libICE6,libiconv,libiconv2,libidn11,libintl-devel,libintl8,libjasper1,libjbig2,libjpeg8,libk5crypto3,libkrb5_3,libkrb5support0,libllvm3.5,libltdl7,liblzma5,liblzo2_2,libmcpp0,libmetalink3,libmpfr4,libncursesw10,libnettle4,libopenldap2_4_2,libopenssl100,libopts-devel,libopts25,libp11-kit0,libpango1.0_0,libpcre1,libpipeline1,libpixman1_0,libpng16,libpopt0,libreadline7,librsvg2_2,libsasl2_3,libsigsegv2,libSM6,libsmartcols1,libsqlite3_0,libssh2_1,libssp0,libstdc++6,libtasn1_6,libthai0,libtiff6,libusb0,libuuid-devel,libuuid1,libwrap0,libX11-xcb1,libX11_6,libXau6,libXaw7,libxcb-glx0,libxcb-icccm4,libxcb-image0,libxcb-render0,libxcb-shm0,libxcb-util1,libxcb1,libXcomposite1,libXcursor1,libXdamage1,libXdmcp6,libXext6,libXfixes3,libXfont1,libXft2,libXi6,libXinerama1,libxkbfile1,libXm4,libxml2,libXmu6,libXmuu1,libXpm4,libXrandr2,libXrender1,libXss1,libXt6,links,login,lrzip,luit,lynx,lzip,m4,make,man-db,mcpp,mintty,nc,net-snmp,net-snmp-agent-libs,net-snmp-devel,net-snmp-gui,net-snmp-libs,net-snmp-python,net-snmp-utils,openssh,openssl,p11-kit,p11-kit-trust,patch,pax,perl,perl-Carp,perl-Encode-Locale,perl-Error,perl-File-Listing,perl-HTML-Parser,perl-HTML-Tagset,perl-HTTP-Cookies,perl-HTTP-Daemon,perl-HTTP-Date,perl-HTTP-Message,perl-HTTP-Negotiate,perl-IO-HTML,perl-libwww-perl,perl-LWP-MediaTypes,perl-Net-HTTP,perl-net-snmp,perl-Pod-Simple,perl-Socket,perl-Stow,perl-URI,perl-WWW-RobotRules,perl_autorebase,perl_base,ping,popt,procps,psmisc,pwgen,python,python-chardet,python-gdata,python-requests,python-setuptools,python-simplejson,python-six,python-urllib3,python3,python3-setuptools,rebase,rgb,rsync,run,screen,sed,setxkbmap,shared-mime-info,shutdown,socat,stow,stunnel,tar,tcl,tcl-tk,tcsh,terminfo,texinfo,tftp,tftp-server,time,tmux,tree,ttcp,tzcode,unace,unzip,util-linux,vim,vim-common,vim-minimal,wget,which,whois,xauth,xbitmaps,xcursor-themes,xdg-user-dirs,xf86-video-dummy,xf86-video-nested,xhost,xinit,xkbcomp,xkbutils,xkeyboard-config,xmodmap,xorg-scripts,xorg-server,xorg-server-common,xorg-x11-fonts-dpi100,xorg-x11-fonts-dpi75,xorg-x11-fonts-ethiopic,xorg-x11-fonts-misc,xorg-x11-fonts-Type1,xrdb,xset,xterm,xwin-xdg-menu,xxd,xz,zip,zlib0,zsh


Python
~~~~~~

setuptools
++++++++++

`setuptools <http://pythonhosted.org/setuptools/>`_ is the de-facto standard
library for Python projects packaging.

It is installed for both Python 2 and Python 3 using the cygwin packages.

It also provides the ``easy_install`` tool.


pip
+++

`pip <https://pip.pypa.io/>`_ is the de-facto standard package manager in the Python ecosystem.
We install it using setuptools' easy_install:

.. code-block:: console

    $ easy_install-2.7 pip
    $ easy_install-3.4 pip

.. note::

    Since we installed setuptools for both Python 2.x and Python 3.x in
    the environment,
    we install pip for both Python versions,
    using the corresponding easy_install installation.


Python
------

This section describes Python-related components who are platform agnostic.

virtualenv
~~~~~~~~~~

`virtualenv <https://virtualenv.pypa.io>`_ is a tool to create isolated Python
environments.

Installation:

.. code-block:: console

    $ pip install virtualenv


Sphinx
~~~~~~

`Sphinx <http://sphinx-doc.org/>`_ is a tool to build documentations written
in `reStructuredText <http://docutils.sourceforge.net/rst.html>`_.

Installation:

.. code-block:: console

    $ pip install sphinx rstcheck

.. note::

    rstcheck is a static checker for reStructuredText documents,
    used by vim's syntastic plugin.
