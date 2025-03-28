## Packages Tracked by DistroWatch （229个包）    |  [返回](README.md)
- [ Last Update: Wednesday 26 March 2025 01:08 GMT ](https://distrowatch.com/packages.php)  
- 快速下载
- **bash**脚本
>wget -c --no-check-certificate https://distrowatch.com/packages.php  
cat packages.php|grep -E '<td><a href="'|awk -F '"' '{print $2}'|uniq|xargs wget -c --no-check-certificate --tries=5   
- **python**代码
```python
import re
from urllib import request
url = 'https://distrowatch.com/packages.php'
req = request.Request(url)
response=request.urlopen(req)
content=response.read().decode('utf-8')
# 获得更新时间
pattern = re.compile('<h1>(.*?)</h1>.*?<div class="MainPage">(.*?)</div>',re.S)
items = re.findall(pattern,content)
for item in items:
    ltime = item[1]
    print(ltime)
# 获得应用包版本信息
pattern = re.compile('<th><a .*?<a href="(.*?)">(.*?)</a></th>.*?<td><a href="(.*?)">(.*?)</a></td>.*?<td.*?>(.*?)</td>',re.S)
items = re.findall(pattern,content)
# 打印表头（markdown格式）
title = '\n|应用软件（详情）|版本（下载）|说明|\n'+'|:----|:----|:----|\n'
print(title)
for item in items:
    url=item[0]
    name=item[1]
    url2=item[2]
    version=item[3]
    note=item[4]
    strs='|['+name+']('+url+')|['+version+']('+url2+')|'+note+'\n'
    # 输出所有
    print(strs)
```
======常见的应用软件======

|应用软件（详情）|版本（下载）|说明|
|:----|:----|:----|
|[abiword](https://gitlab.gnome.org/World/AbiWord/)|[3.0.6](https://gitlab.gnome.org/World/AbiWord/-/archive/release-3.0.6/AbiWord-release-3.0.6.tar.gz)|AbiWord: a full-featured word processor
|[amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu)|[23.0.0](https://xorg.freedesktop.org/archive/individual/driver/xf86-video-amdgpu-23.0.0.tar.xz)|amdgpu: an X.Org driver for AMD RADEON-based video cards
|[apt](https://tracker.debian.org/pkg/apt)|[2.9.34](https://deb.debian.org/debian/pool/main/a/apt/apt_2.9.34.tar.xz)|APT: a front-end for the dpkg package manager
|[autoconf](https://www.gnu.org/software/autoconf/autoconf.html)|[2.72](https://ftp.gnu.org/gnu/autoconf/autoconf-2.72.tar.xz)|Autoconf: a package of M4 macros to produce scripts to automatically configure source code
|[avidemux](http://fixounet.free.fr/avidemux/)|[2.8.1](https://downloads.sourceforge.net/avidemux/avidemux_2.8.1.tar.gz)|Avidemux: a free video editor designed for simple cutting, filtering and encoding tasks
|[bash](https://www.gnu.org/software/bash/bash.html)|[5.2.37](https://ftp.gnu.org/gnu/bash/bash-5.2.37.tar.gz)|Bash: an sh-compatible command language interpreter
|[binutils](https://www.gnu.org/software/binutils/binutils.html)|[2.44](https://ftp.gnu.org/gnu/binutils/binutils-2.44.tar.gz)|GNU Binutils: an essential collection of binary utilities
|[bitcoin](https://bitcoin.org/)|[28.1](https://github.com/bitcoin/bitcoin/archive/v28.1.tar.gz)|Bitcoin: an innovative payment network and a new kind of money
|[budgie-desktop](https://github.com/BuddiesOfBudgie/budgie-desktop)|[10.9.2](https://github.com/BuddiesOfBudgie/budgie-desktop/releases/download/v10.9.2/budgie-desktop-v10.9.2.tar.xz)|Budgie Desktop: a simple desktop environment featuring heavy integration with the GNOME stack
|[bzip2](https://sourceware.org/bzip2/)|[1.0.8](https://sourceware.org/pub/bzip2/bzip2-1.0.8.tar.gz)|bzip2: a free, patent-free, high-quality data compressor
|[calligra](https://calligra.org/)|[24.12.3](https://github.com/KDE/calligra/archive/refs/tags/v24.12.3.tar.gz)|Calligra: an integrated office suite based on the KDE libraries
|[chromium](http://www.chromium.org/Home)|[134.0.6998.165](https://chromium.googlesource.com/chromium/src/+/refs/tags/134.0.6998.165)|Google Chromium: an open-source edition of Google Chrome, a graphical web browser
|[clamav](https://www.clamav.net/)|[1.4.2](https://github.com/Cisco-Talos/clamav/archive/refs/tags/clamav-1.4.2.tar.gz)|ClamAV: an open-source antivirus engine for detecting trojans, viruses, malware and other malicious threats
|[coreutils](https://www.gnu.org/software/coreutils/)|[9.6](https://ftp.gnu.org/gnu/coreutils/coreutils-9.6.tar.xz)|GNU Coreutils: provides basic file, shell and text manipulation utilities
|[cups](https://openprinting.github.io/)|[2.4.11](https://github.com/OpenPrinting/cups/releases/download/v2.4.11/cups-2.4.11-source.tar.gz)|CUPS: a UNIX printing system based on the Internet Printing Protocol
|[cvs](https://cvs.nongnu.org/)|[1.11.23](https://ftp.gnu.org/non-gnu/cvs/source/stable/1.11.23/cvs-1.11.23.tar.bz2)|CVS: a version control system
|[deluge](https://deluge-torrent.org/)|[2.1.1](https://download.deluge-torrent.org/source/2.1/deluge-2.1.1.tar.xz)|Deluge: a lightweight, cross-platform BitTorrent client
|[dhcp](https://www.isc.org/downloads/dhcp/)|[4.4.3-P1](https://downloads.isc.org/isc/dhcp/4.4.3-P1/dhcp-4.4.3-P1.tar.gz)|ISC DHCP: a server and client for automatic IP configuration
|[digikam](https://www.digikam.org/)|[8.6.0](https://download.kde.org/stable/digikam/8.6.0/digiKam-8.6.0.tar.xz)|Digikam: an advanced digital photo management application
|[dnf](https://github.com/rpm-software-management/dnf5/)|[5.2.12.0](https://github.com/rpm-software-management/dnf5/archive/5.2.12.0.tar.gz)|DNF: a new package management library and a fork of yum
|[dosbox](https://dosbox.sourceforge.net/)|[0.74-3](https://downloads.sourceforge.net/dosbox/dosbox-0.74-3.tar.gz)|DOSBox: a DOS emulator
|[doxygen](https://www.doxygen.nl/)|[1.13.2](https://doxygen.nl/files/doxygen-1.13.2.src.tar.gz)|Doxygen: a documentation system for C++, Java, C and IDL
|[e2fsprogs](https://e2fsprogs.sourceforge.net/)|[1.47.2](https://downloads.sourceforge.net/e2fsprogs/e2fsprogs-1.47.2.tar.gz)|e2fsprogs: contains the required utilities for the EXT2 file system
|[efibootmgr](https://github.com/rhinstaller/efibootmgr)|[18](https://github.com/rhinstaller/efibootmgr/releases/download/18/efibootmgr-18.tar.bz2)|efibootmgr: a Linux user-space application to modify the Intel EFI boot manager
|[enlightenment](https://enlightenment.org/)|[0.27.1](https://download.enlightenment.org/rel/apps/enlightenment/enlightenment-0.27.1.tar.xz)|Enlightenment: a window manager for X
|[exim](https://www.exim.org/)|[4.98.1](https://ftp.exim.org/pub/exim/exim4/exim-4.98.1.tar.xz)|exim: a mail server
|[file](https://www.darwinsys.com/file/)|[5.46](https://ftp.astron.com/pub/file/file-5.46.tar.gz)|file: a program that attempts to classify files by their content
|[firebird](https://www.firebirdsql.org/)|[5.0.2](https://github.com/FirebirdSQL/firebird/archive/refs/tags/v5.0.2.tar.gz)|Firebird: a relational database offering many ANSI SQL standard features that runs on Linux, Windows and UNIX
|[firejail](https://firejail.wordpress.com/)|[0.9.72](https://downloads.sourceforge.net/firejail/firejail-0.9.72.tar.xz)|Firejail: a Linux namespaces sandbox program
|[flex](https://github.com/westes/flex)|[2.6.4](https://github.com/westes/flex/releases/download/v2.6.4/flex-2.6.4.tar.gz)|Flex: a fast lexical analyser generator
|[freecad](https://www.freecadweb.org/)|[1.0.0](https://github.com/FreeCAD/FreeCAD/archive/1.0.0.tar.gz)|FreeCAD: a general purpose parametric 3D modeller for CAD
|[gawk](https://www.gnu.org/software/gawk/gawk.html)|[5.3.1](https://ftp.gnu.org/gnu/gawk/gawk-5.3.1.tar.xz)|GNU Gawk: a free version of awk, a string manipulation language
|[gettext](https://www.gnu.org/software/gettext/)|[0.24](https://ftp.gnu.org/gnu/gettext/gettext-0.24.tar.xz)|GNU gettext: the GNU internationalisation (i18n) library
|[gimp](https://www.gimp.org/)|[3.0.2](https://download.gimp.org/mirror/pub/gimp/v3.0/gimp-3.0.2.tar.xz)|GIMP: the GNU Image Manipulation Program
|[glade](https://wiki.gnome.org/Apps/Glade)|[3.40.0](https://download.gnome.org/sources/glade/3.40/glade-3.40.0.tar.xz)|Glade: a GUI builder for GTK+ and GNOME
|[gnome-shell](https://wiki.gnome.org/Projects/GnomeShell)|[48.0](https://download.gnome.org/sources/gnome-shell/48/gnome-shell-48.0.tar.xz)|GNOME Shell: a core user interface of the GNOME 3 desktop
|[gnumeric](http://www.gnumeric.org/)|[1.12.59](https://download.gnome.org/sources/gnumeric/1.12/gnumeric-1.12.59.tar.xz)|Gnumeric: a spreadsheet and a part of the GNOME Desktop
|[gparted](https://gparted.sourceforge.net/)|[1.7.0](https://downloads.sourceforge.net/gparted/gparted-1.7.0.tar.gz)|GParted: a disk partition editor application for GNOME
|[groff](https://www.gnu.org/software/groff/groff.html)|[1.23.0](https://ftp.gnu.org/gnu/groff/groff-1.23.0.tar.gz)|GNU Groff: a device-independent document processor/formatter
|[gstreamer](https://gstreamer.freedesktop.org/)|[1.26.0](https://gstreamer.freedesktop.org/src/gstreamer/gstreamer-1.26.0.tar.xz)|GStreamer: a multimedia framework with a plugin-based architecture for a variety of platforms
|[gzip](https://www.gnu.org/software/gzip/gzip.html)|[1.13](https://ftp.gnu.org/gnu/gzip/gzip-1.13.tar.gz)|gzip: a compression utility designed to replace compress
|[httpd](https://httpd.apache.org/)|[2.4.63](https://archive.apache.org/dist/httpd/httpd-2.4.63.tar.bz2)|httpd: a high-performance HTTP server, Apache 2.x version series
|[icewm](https://ice-wm.org/)|[3.7.2](https://github.com/ice-wm/icewm/releases/download/3.7.2/icewm-3.7.2.tar.lz)|IceWM: an X Window manager that emulates the looks of Motif, OS/2 and Windows
|[inkscape](https://www.inkscape.org/)|[1.4](https://inkscape.org/gallery/item/53679/inkscape-1.4.tar.xz)|Inkscape: a drawing tool that uses the W3C standard scalable vector graphics format (SVG)
|[k3b](https://apps.kde.org/en-gb/k3b/)|[24.12.3](https://github.com/KDE/k3b/archive/v24.12.3.tar.gz)|K3b: a KDE-GUI for cdrecord and cdrdao, similar to Nero
|[kmod](https://www.kernel.org/pub/linux/utils/kernel/kmod/)|[34.1](https://www.kernel.org/pub/linux/utils/kernel/kmod/kmod-34.1.tar.xz)|kmod: a set of programs for loading, inserting and removing kernel modules
|[krita](https://krita.org/)|[5.2.9](https://download.kde.org/stable/krita/5.2.9/krita-5.2.9.tar.xz)|Krita: a cross-platform application that offers an end-to-end solution for creating digital art files from scratch
|[ktorrent](https://www.kde.org/applications/internet/ktorrent/)|[24.12.3](https://github.com/KDE/ktorrent/archive/v24.12.3.tar.gz)|KTorrent: a BitTorrent program for KDE
|[lftp](https://lftp.yar.ru/)|[4.9.3](https://lftp.yar.ru/ftp/lftp-4.9.3.tar.xz)|LFTP: a sophisticated FTP/HTTP client, file transfer program
|[LibreOffice](https://www.libreoffice.org/)|[25.2.1](https://download.documentfoundation.org/libreoffice/stable/25.2.1/)|LibreOffice: a free personal productivity suite
|[libselinux](http://userspace.selinuxproject.org/)|[3.8.1](https://github.com/SELinuxProject/selinux/archive/libselinux-3.8.1.tar.gz)|libselinux: a library providing an interface for security-aware applications in SELinux
|[libvirt](https://libvirt.org/)|[11.1.0](https://libvirt.org/sources/libvirt-11.1.0.tar.xz)|libvirt: a toolkit to interact with the virtualization capabilities of the Linux kernel
|[lighttpd](https://www.lighttpd.net/)|[1.4.78](https://download.lighttpd.net/lighttpd/releases-1.4.x/lighttpd-1.4.78.tar.xz)|lighttpd: a secure, fast, compliant and flexible web server optimized for high-performance environments
|[links](http://links.twibright.com/)|[2.30](http://links.twibright.com/download/links-2.30.tar.bz2)|Links: a text and graphics mode web browser similar to Lynx
|[llvm](https://llvm.org/)|[20.1.1](https://github.com/llvm/llvm-project/releases/download/llvmorg-20.1.1/llvm-20.1.1.src.tar.xz)|LLVM: a collection of modular and reusable compiler and toolchain technologies
|[lumina](https://lumina-desktop.org/)|[1.6.2](https://github.com/lumina-desktop/lumina/archive/v1.6.2.tar.gz)|Lumina: a lightweight desktop environment for use on any UNIX-like operating system
|[lxpanel](https://sourceforge.net/projects/lxde/)|[0.10.1](https://downloads.sourceforge.net/lxde/lxpanel-0.10.1.tar.xz)|LXDE: a lightweight, fast and energy-saving desktop environment
|[lynx](https://lynx.browser.org/)|[2.9.2](https://invisible-mirror.net/archives/lynx/tarballs/lynx2.9.2.tar.bz2)|Lynx: a text browser for the web
|[lzip](https://www.nongnu.org/lzip/lzip.html)|[1.25](https://download.savannah.gnu.org/releases/lzip/lzip-1.25.tar.lz)|Lzip: a lossless data compressor
|[make](https://www.gnu.org/software/make/)|[4.4.1](https://ftp.gnu.org/gnu/make/make-4.4.1.tar.lz)|GNU make: a tool which controls the generation of executables from the program's source files
|[man-pages](https://www.kernel.org/doc/man-pages/)|[6.13](https://www.kernel.org/pub/linux/docs/man-pages/man-pages-6.13.tar.xz)|Man Pages: files containing the manual pages displayed by man
|[mate-desktop](https://mate-desktop.org/)|[1.28.2](https://pub.mate-desktop.org/releases/1.28/mate-desktop-1.28.2.tar.xz)|MATE: a traditional desktop environment forked from GNOME 2
|[mesa](https://www.mesa3d.org/)|[25.0.2](https://mesa.freedesktop.org/archive/mesa-25.0.2.tar.xz)|Mesa: a 3D graphics library
|[mod_perl](https://perl.apache.org/)|[2.0.13](https://archive.apache.org/dist/perl/mod_perl-2.0.13.tar.gz)|mod_perl: provides a Perl module for httpd
|[mutt](http://www.mutt.org/)|[2.2.14](http://ftp.mutt.org/pub/mutt/mutt-2.2.14.tar.gz)|Mutt: a text-based MIME Email client
|[mysql](https://dev.mysql.com/downloads/mysql/)|[9.2.0](https://cdn.mysql.com/Downloads/MySQL-9.0/mysql-9.2.0.tar.gz)|MySQL: an SQL database server
|[nano](https://www.nano-editor.org/)|[8.3](https://www.nano-editor.org/dist/latest/nano-8.3.tar.gz)|GNU nano: a curse-based text editor for UNIX
|[ncurses](https://invisible-island.net/ncurses/)|[6.5](https://invisible-mirror.net/archives/ncurses/ncurses-6.5.tar.gz)|GNU ncurses: a programming library allowing a programmer to write text user interfaces in a terminal-independent manner
|[NetworkManager](https://networkmanager.dev/)|[1.52.0](https://gitlab.freedesktop.org/NetworkManager/NetworkManager/-/archive/1.52.0/NetworkManager-1.52.0.tar.bz2)|NetworkManager: a utility aimed at simplifying the use of computer networks on Linux
|[nginx](https://nginx.org/)|[1.26.3](https://nginx.org/download/nginx-1.26.3.tar.gz)|nginx: an HTTP and reverse proxy server
|[ntfs-3g](https://www.tuxera.com/community/ntfs-3g-download/)|[2022.10.3](https://tuxera.com/opensource/ntfs-3g_ntfsprogs-2022.10.3.tgz)|NTFS-3G: a read/write NTFS driver
|[NVIDIA](https://www.nvidia.com/object/unix.html)|[570.133.07](https://us.download.nvidia.com/XFree86/Linux-x86_64/570.133.07/NVIDIA-Linux-x86_64-570.133.07.run)|NVIDIA: a proprietary display driver for Linux, FreeBSD and Solaris
|[openbox](http://openbox.org/)|[3.6.1](http://openbox.org/dist/openbox/openbox-3.6.1.tar.gz)|Openbox: a standards-compliant, lightweight, extensible window manager
|[openldap](https://www.openldap.org/)|[2.6.9](https://openldap.org/software/download/OpenLDAP/openldap-release/openldap-2.6.9.tgz)|OpenLDAP: a full-featured open source LDAP software suite
|[openssh](https://www.openssh.com/portable.html)|[9.9p2](https://ftp3.usa.openbsd.org/pub/OpenBSD/OpenSSH/portable/openssh-9.9p2.tar.gz)|OpenSSH: a client and server for encrypted remote logins and file transfers
|[openvpn](https://openvpn.net/community/)|[2.6.13](https://swupdate.openvpn.org/community/releases/openvpn-2.6.13.tar.gz)|OpenVPN: an open-source VPN daemon
|[pacman](https://archlinux.org/pacman/)|[7.0.0](https://gitlab.archlinux.org/pacman/pacman/-/archive/v7.0.0/pacman-v7.0.0.tar.bz2)|pacman: a utility which manages software packages in Linux
|[pcmanfm](https://github.com/lxde/pcmanfm)|[1.4.0](https://github.com/lxde/pcmanfm/archive/refs/tags/1.4.0.tar.gz)|PCManFM: an extremely fast and lightweight file manager
|[php](https://www.php.net/)|[8.4.5](https://www.php.net/distributions/php-8.4.5.tar.xz)|PHP: a server-side HTML embedded scripting language
|[pidgin](https://pidgin.im/)|[2.14.14](https://downloads.sourceforge.net/pidgin/pidgin-2.14.14.tar.bz2)|Pidgin: an instant messenger client for several protocols (formerly GAIM)
|[pitivi](https://www.pitivi.org/)|[2023.03](https://download.gnome.org/sources/pitivi/2023/pitivi-2023.03.tar.xz)|PiTiVi: a free and open-source video editor for Linux
|[postfix](https://www.postfix.org/)|[3.10.1](http://ftp.porcupine.org/mirrors/postfix-release/official/postfix-3.10.1.tar.gz)|Postfix: a mail transport agent
|[ppp](https://www.samba.org/ppp/)|[2.5.2](https://github.com/paulusmack/ppp/archive/ppp-2.5.2.tar.gz)|PPP: provides a server/client for point to point protocol
|[pulseaudio](https://www.freedesktop.org/wiki/Software/PulseAudio/)|[17.0](https://freedesktop.org/software/pulseaudio/releases/pulseaudio-17.0.tar.xz)|PulseAudio: a sound server for POSIX and Win32 systems
|[qbittorrent](https://www.qbittorrent.org/)|[5.0.4](https://downloads.sourceforge.net/qbittorrent/qbittorrent-5.0.4.tar.xz)|qBittorrent: a P2P BitTorrent client
|[qt](https://www.qt.io/)|[6.8.2](https://download.qt-project.org/official_releases/qt/6.7/6.8.2/single/qt-everywhere-src-6.8.2.tar.xz)|Qt: a C++ application framework for writing graphical applications
|[reiserfsprogs](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/)|[3.6.27](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/v3.6.27/reiserfsprogs-3.6.27.tar.xz)|reiserfsprogs: contains tools for using Reiser file system
|[rp-pppoe](https://dianne.skoll.ca/projects/rp-pppoe/)|[4.0](https://dianne.skoll.ca/projects/rp-pppoe/download/rp-pppoe-4.0.tar.gz)|RP-PPPoE: a PPP over Ethernet client/server suite
|[ruby](https://www.ruby-lang.org/)|[3.4.2](https://ftp.ruby-lang.org/pub/ruby/3.4/ruby-3.4.2.tar.xz)|Ruby: interpreted, dynamically typed, pure object-oriented scripting language
|[samba](https://www.samba.org/)|[4.22.0](https://us1.samba.org/samba/ftp/stable/samba-4.22.0.tar.gz)|Samba: a free software re-implementation of SMB/CIFS networking protocol
|[screen](https://www.gnu.org/software/screen/)|[5.0.0](https://ftp.gnu.org/gnu/screen/screen-5.0.0.tar.gz)|Screen: multiplexes a physical terminal
|[seamonkey](https://www.seamonkey-project.org/)|[2.53.20](https://archive.seamonkey-project.org/releases/2.53.20/source/seamonkey-2.53.20.source.tar.xz)|Mozilla SeaMonkey: a web browser, e-mail and newsgroup client, IRC chat client and HTML editor
|[sendmail](https://www.proofpoint.com/us/products/email-protection/open-source-email-solution)|[8.18.1](https://ftp.sendmail.org/sendmail.8.18.1.tar.gz)|Sendmail: a powerful and flexible Mail Transport Agent
|[shotwell](https://wiki.gnome.org/Apps/Shotwell)|[0.32.10](https://download.gnome.org/sources/shotwell/0.32/shotwell-0.32.10.tar.xz)|Shotwell: an open-source digital photo organiser for GNOME
|[snort](https://www.snort.org/)|[3.7.1.0](https://snort.org/downloads/snortplus/snort3-3.7.1.0.tar.gz)|Snort: a light-weight network intrusion detection program
|[sqlite](https://www.sqlite.org/)|[3.49.1](https://github.com/sqlite/sqlite/archive/refs/tags/version-3.49.1.tar.gz)|SQLite: an embeddable SQL engine in a C library
|[subversion](https://subversion.apache.org/)|[1.14.5](https://www.apache.org/dist/subversion/subversion-1.14.5.tar.bz2)|Subversion: a version control system
|[synaptic](https://tracker.debian.org/pkg/synaptic)|[0.91.6](https://github.com/mvo5/synaptic/archive/refs/tags/0.91.6.tar.gz)|Synaptic: a graphical front-end for APT
|[sysvinit](https://github.com/slicer69/sysvinit)|[3.14](https://github.com/slicer69/sysvinit/releases/download/3.14/sysvinit-3.14.tar.xz)|SysVinit: the Linux System V Init
|[tcl](https://core.tcl.tk/tcl/)|[9.0.1](https://downloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz)|TCL: a powerful and dynamic programming language
|[texinfo](https://www.gnu.org/software/texinfo/)|[7.2](https://ftp.gnu.org/gnu/texinfo/texinfo-7.2.tar.xz)|GNU Texinfo: a collection of utilities that generate online help and printed manuals
|[thunderbird](https://www.mozilla.org/products/thunderbird/)|[136.0.1](https://ftp.mozilla.org/pub/thunderbird/releases/136.0.1/source/thunderbird-136.0.1.source.tar.xz)|Mozilla Thunderbird: a full-featured e-mail and newsgroup client
|[tmux](https://tmux.github.io/)|[3.5a](https://github.com/tmux/tmux/releases/download/3.5a/tmux-3.5a.tar.gz)|tmux: a terminal multiplexer
|[transmission](https://www.transmissionbt.com/)|[4.0.6](https://github.com/transmission/transmission/releases/download/4.0.6/transmission-4.0.6.tar.xz)|Transmission: a BitTorrent client
|[vim](https://www.vim.org/)|[9.1](https://github.com/vim/vim/archive/refs/tags/v9.1.0113.tar.gz)|Vim: an improved version of the editor "vi", one of the standard text editors on UNIX
|[vivaldi](https://vivaldi.com/)|[7.2.3621.67](https://source.vivaldi.com/vivaldi-source_5.2.2623.tar.xz)|Vivaldi: a free, cross-platform, proprietary web browser developed by Vivaldi Technologies
|[wayland](https://wayland.freedesktop.org/)|[1.23.1](https://wayland.freedesktop.org/releases/wayland-1.23.1.tar.xz)|Wayland: a display server protocol
|[wget](https://www.gnu.org/software/wget/)|[2.2.0](https://ftp.gnu.org/gnu/wget/wget2-2.2.0.tar.gz)|wget: retrieves files from web and FTP sites
|[wine](https://www.winehq.org/)|[10.0](https://dl.winehq.org/wine/source/10.0/wine-10.0.tar.xz)|Wine: an open source implementation of the Windows API on top of X, OpenGL and Unix
|[wordpress](https://wordpress.org/)|[6.7.2](https://wordpress.org/wordpress-6.7.2.tar.gz)|WordPress: publishing software for the world wide web
|[xfsprogs](https://xfs.wiki.kernel.org/)|[6.13.0](https://www.kernel.org/pub/linux/utils/fs/xfs/xfsprogs/xfsprogs-6.13.0.tar.xz)|xfsprogs: a set of utilities for managing the XFS file system
|[xorg-server](https://www.x.org/)|[21.1.16](https://www.x.org/archive/individual/xserver/xorg-server-21.1.16.tar.xz)|X.Org: the X.Org Foundation's public implementation of the X Window System
|[zfs](https://openzfs.org/)|[2.3.1](https://github.com/openzfs/zfs/releases/download/zfs-2.3.1/zfs-2.3.1.tar.gz)|ZFS: an advanced file system and volume manager maintained by the Illumos community
