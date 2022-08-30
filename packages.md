## Packages Tracked by DistroWatch （229个包）    |  [返回](README.md)
- [ Last Update: Tuesday 30 August 2022 10:08 GMT ](https://distrowatch.com/packages.php)  
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
|[abiword](https://www.abisource.com/)|[3.0.5](https://www.abisource.com/downloads/abiword/3.0.5/source/abiword-3.0.5.tar.gz)|AbiWord: a full-featured word processor
|[AfterStep](http://www.afterstep.org/)|[2.2.12](https://github.com/afterstep/afterstep/archive/refs/tags/2.2.12.tar.gz)|AfterStep: a window manager for X with a NeXT look and feel
|[alsa-lib](http://www.alsa-project.org/)|[1.2.7.2](https://www.alsa-project.org/files/pub/lib/alsa-lib-1.2.7.2.tar.bz2)|alsa-lib: an audio library for use with the ALSA kernel modules
|[amarok](https://amarok.kde.org/)|[2.9.0](http://download.kde.org/stable/amarok/2.9.0/src/amarok-2.9.0.tar.bz2)|Amarok: a music player for Linux and UNIX
|[amdgpu](http://support.amd.com/en-us/download)|[22.20.3](https://repo.radeon.com/amdgpu-install/22.20.3/)|AMDGPU: a device driver and utility software package for AMD's graphics cards and APUs
|[apache-tomcat](http://tomcat.apache.org/)|[10.0.23](http://www.apache.org/dist/tomcat/tomcat-10/v10.0.23/src/apache-tomcat-10.0.23-src.tar.gz)|apache-tomcat: a Java Servlet and JSP Container
|[apt](https://tracker.debian.org/pkg/apt)|[2.5.2](https://deb.debian.org/debian/pool/main/a/apt/apt_2.5.2.tar.xz)|APT: a front-end for the dpkg package manager
|[audacity](http://www.audacityteam.org/)|[3.1.3](http://www.fosshub.com/Audacity.html/audacity-minsrc-3.1.3.tar.xz)|Audacity: a free audio editor
|[autoconf](http://www.gnu.org/software/autoconf/autoconf.html)|[2.71](https://ftp.gnu.org/gnu/autoconf/autoconf-2.71.tar.xz)|Autoconf: a package of M4 macros to produce scripts to automatically configure source code
|[automake](http://www.gnu.org/software/automake/)|[1.16.5](https://ftp.gnu.org/gnu/automake/automake-1.16.5.tar.xz)|GNU Automake: a tool for automatically generating Makefiles
|[avidemux](http://fixounet.free.fr/avidemux/)|[2.8.0](http://downloads.sourceforge.net/avidemux/avidemux_2.8.0.tar.gz)|Avidemux: a free video editor designed for simple cutting, filtering and encoding tasks
|[awesome](http://awesome.naquadah.org/)|[4.3](https://github.com/awesomeWM/awesome/releases/download/v4.3/awesome-4.3.tar.xz)|awesome: a configurable window manager for X
|[bash](http://www.gnu.org/software/bash/bash.html)|[5.1.16](http://ftp.gnu.org/gnu/bash/bash-5.1.16.tar.gz)|Bash: an sh-compatible command language interpreter
|[bind](http://www.isc.org/downloads/bind/)|[9.18.6](https://ftp.isc.org/isc/bind9/9.18.6/bind-9.18.6.tar.xz)|ISC BIND: an implementation of the Domain Name System (DNS) protocols
|[binutils](http://www.gnu.org/software/binutils/binutils.html)|[2.39](https://ftp.gnu.org/gnu/binutils/binutils-2.39.tar.gz)|GNU Binutils: an essential collection of binary utilities
|[bison](http://www.gnu.org/software/bison/bison.html)|[3.8.2](https://ftp.gnu.org/gnu/bison/bison-3.8.2.tar.xz)|Bison: a replacement for the parser generator Yacc
|[bitcoin](https://bitcoin.org/)|[23.0](https://github.com/bitcoin/bitcoin/archive/v23.0.tar.gz)|Bitcoin: an innovative payment network and a new kind of money
|[blender](https://www.blender.org/)|[3.2.2](https://download.blender.org/source/blender-3.2.2.tar.xz)|Blender: a very fast and versatile 3D modeller and renderer
|[budgie-desktop](https://github.com/BuddiesOfBudgie/budgie-desktop)|[10.6.3](https://github.com/BuddiesOfBudgie/budgie-desktop/releases/download/v10.6.3/budgie-desktop-v10.6.3.tar.xz)|Budgie Desktop: a simple desktop environment featuring heavy integration with the GNOME stack
|[busybox](http://www.busybox.net/)|[1.35.0](http://www.busybox.net/downloads/busybox-1.35.0.tar.bz2)|BusyBox: a program that combines many common UNIX utilities into a single small executable
|[bzip2](https://sourceware.org/bzip2/)|[1.0.8](https://sourceware.org/pub/bzip2/bzip2-1.0.8.tar.gz)|bzip2: a free, patent-free, high-quality data compressor
|[cacti](https://www.cacti.net/)|[1.2.22](https://www.cacti.net/downloads/cacti-1.2.22.tar.gz)|Cacti: a complete network graphing solution
|[calibre](http://calibre-ebook.com/)|[6.3.0](https://download.calibre-ebook.com/6.3.0/calibre-6.3.0.tar.xz)|Calibre: an e-book library management application
|[calligra](http://www.calligra-suite.org/)|[3.2.1](http://download.kde.org/stable/calligra/3.2.1/calligra-3.2.1.tar.xz)|Calligra: an integrated office suite based on the KDE libraries
|[cdrkit](https://tracker.debian.org/pkg/cdrkit)|[1.1.11](https://deb.debian.org/debian/pool/main/c/cdrkit/cdrkit_1.1.11.orig.tar.gz)|cdrkit: a collection of applications related to creation of optical disk media
|[chromium](http://www.chromium.org/Home)|[104.0.5112.101](http://src.chromium.org/viewvc/chrome/)|Google Chromium: an open-source edition of Google Chrome, a graphical web browser
|[cinnamon](https://github.com/linuxmint/cinnamon/)|[5.4.11](https://github.com/linuxmint/Cinnamon/archive/5.4.11.tar.gz)|Cinnamon: a desktop environment developed by Linux Mint
|[clementine](http://www.clementine-player.org/)|[1.3.1](https://github.com/clementine-player/Clementine/archive/1.3.1.tar.gz)|Clementine: a multi-platform music player
|[cmake](https://cmake.org/)|[3.24.1](https://github.com/Kitware/CMake/releases/download/v3.24.1/cmake-3.24.1.tar.gz)|cmake: a cross-platform, open-source build system
|[compiz](http://compiz.org/)|[0.9.14.2](https://launchpad.net/compiz/0.9.14/0.9.14.2/+download/compiz-0.9.14.2.tar.xz)|Compiz: a compositing window manager that uses 3D graphics acceleration via OpenGL
|[coreutils](https://www.gnu.org/software/coreutils/)|[9.1](https://ftp.gnu.org/gnu/coreutils/coreutils-9.1.tar.xz)|GNU Coreutils: provides basic file, shell and text manipulation utilities
|[cups](https://openprinting.github.io/)|[2.4.2](https://github.com/OpenPrinting/cups/releases/download/v2.4.2/cups-2.4.2-source.tar.gz)|CUPS: a UNIX printing system based on the Internet Printing Protocol
|[curl](https://curl.se/)|[7.84.0](https://github.com/curl/curl/releases/download/curl-7_84_0/curl-7.84.0.tar.xz)|cURL: a command line tool for transferring files with URL syntax
|[cvs](http://cvs.nongnu.org/)|[1.11.23](http://ftp.gnu.org/non-gnu/cvs/source/stable/1.11.23/cvs-1.11.23.tar.bz2)|CVS: a version control system
|[db](http://www.oracle.com/technetwork/database/database-technologies/berkeleydb/downloads/index.html)|[18.1.40](http://www.oracle.com/technetwork/database/database-technologies/berkeleydb/downloads/index.html)|Berkeley DB: a family of open source developer databases from Oracle
|[deluge](http://deluge-torrent.org/)|[2.1.0](http://download.deluge-torrent.org/source/2.0/deluge-2.1.0.tar.xz)|Deluge: a lightweight, cross-platform BitTorrent client
|[devede](http://www.rastersoft.com/programas/devede.html)|[4.17.0](https://gitlab.com/rastersoft/devedeng/-/archive/4.17.0/devedeng-4.17.0.tar.bz2)|DeVeDe: a program to create video DVDs and CDs suitables for home players
|[dhcp](https://www.isc.org/downloads/dhcp/)|[4.4.3](https://downloads.isc.org/isc/dhcp/4.4.3/dhcp-4.4.3.tar.gz)|ISC DHCP: a server and client for automatic IP configuration
|[diffutils](http://www.gnu.org/software/diffutils/)|[3.8](https://ftp.gnu.org/gnu/diffutils/diffutils-3.8.tar.xz)|GNU Diffutils: a utility which finds differences between and among files
|[digikam](https://www.digikam.org/)|[7.7.0](https://download.kde.org/stable/digikam/7.7.0/digikam-7.7.0.tar.xz)|Digikam: an advanced digital photo management application
|[dillo](http://www.dillo.org/)|[3.0.5](http://www.dillo.org/download/dillo-3.0.5.tar.bz2)|Dillo: a lightweight, alternative browser for UNIX systems
|[dnf](https://github.com/rpm-software-management/dnf/)|[4.13.0](https://github.com/rpm-software-management/dnf/archive/4.13.0.tar.gz)|DNF: a new package management library and a fork of yum
|[docker](https://www.docker.com/community-edition)|[20.10.17](https://github.com/moby/moby/archive/refs/tags/v20.10.17.tar.gz)|Docker: a program that performs operating-system-level virtualisation, also known as "containerisation"
|[dosbox](http://dosbox.sourceforge.net/)|[0.74-3](http://downloads.sourceforge.net/dosbox/dosbox-0.74-3.tar.gz)|DOSBox: a DOS emulator
|[dovecot](http://www.dovecot.org/)|[2.3.19.1](http://www.dovecot.org/releases/2.3/dovecot-2.3.19.1.tar.gz)|Dovecot: an open source IMAP and POP3 server for Linux/UNIX-like systems
|[doxygen](http://www.doxygen.nl/)|[1.9.5](http://doxygen.nl/files/doxygen-1.9.5.src.tar.gz)|Doxygen: a documentation system for C++, Java, C and IDL
|[dracut](https://dracut.wiki.kernel.org/index.php/Main_Page)|[057](https://github.com/dracutdevs/dracut/releases/download/057/dracut-057.tar.xz)|dracut: the event driven initramfs infrastructure
|[e2fsprogs](http://e2fsprogs.sourceforge.net/)|[1.46.5](http://downloads.sourceforge.net/e2fsprogs/e2fsprogs-1.46.5.tar.gz)|e2fsprogs: contains the required utilities for the EXT2 file system
|[eclipse](http://eclipse.org/)|[4.24](http://download.eclipse.org/eclipse/downloads/)|Eclipse: a universal tool platform and IDE
|[efibootmgr](https://github.com/rhinstaller/efibootmgr)|[18](https://github.com/rhinstaller/efibootmgr/releases/download/18/efibootmgr-18.tar.bz2)|efibootmgr: a Linux user-space application to modify the Intel EFI boot manager
|[emacs](http://www.gnu.org/software/emacs/)|[28.1](https://ftp.gnu.org/gnu/emacs/emacs-28.1.tar.xz)|GNU Emacs: the extensible, self-documenting real-time display editor
|[enlightenment](http://enlightenment.org/)|[0.25.3](https://download.enlightenment.org/rel/apps/enlightenment/enlightenment-0.25.3.tar.xz)|Enlightenment: a window manager for X
|[evolution](https://wiki.gnome.org/Apps/Evolution)|[3.44.4](https://download.gnome.org/sources/evolution/3.42/evolution-3.44.4.tar.xz)|Evolution: information management software providing mail, address book and calendaring functionality
|[exim](https://www.exim.org/)|[4.96](https://ftp.exim.org/pub/exim/exim4/exim-4.96.tar.xz)|exim: a mail server
|[ffmpeg](http://ffmpeg.org/)|[5.1](http://ffmpeg.org/releases/ffmpeg-5.1.tar.xz)|FFmpeg: a complete, cross-platform solution to record, convert and stream audio and video
|[file](http://www.darwinsys.com/file/)|[5.42](http://ftp.astron.com/pub/file/file-5.42.tar.gz)|file: a program that attempts to classify files by their content
|[findutils](http://www.gnu.org/software/findutils/)|[4.9.0](http://ftp.gnu.org/gnu/findutils/findutils-4.7.0.tar.xz)|GNU Findutils: a set of tools to find files and to operate on groups of files
|[firebird](http://www.firebirdsql.org/)|[4.0.2](https://github.com/FirebirdSQL/firebird/archive/refs/tags/v4.0.2.tar.gz)|Firebird: a relational database offering many ANSI SQL standard features that runs on Linux, Windows and UNIX
|[firefox](http://www.mozilla.org/products/firefox/)|[104.0.1](https://ftp.mozilla.org/pub/firefox/releases/104.0.1/source/firefox-104.0.1.source.tar.xz)|Mozilla Firefox: a web browser for Windows, Linux, macOS, FreeBSD and Android
|[firejail](https://firejail.wordpress.com/)|[0.9.70](http://downloads.sourceforge.net/firejail/firejail-0.9.70.tar.xz)|Firejail: a Linux namespaces sandbox program
|[flatpak](http://flatpak.org)|[1.14.0](https://github.com/flatpak/flatpak/releases/download/1.14.0/flatpak-1.14.0.tar.xz)|Flatpak: a framework for Linux application sandboxing and distribution
|[flex](http://flex.sourceforge.net/)|[2.6.4](https://github.com/westes/flex/releases/download/v2.6.4/flex-2.6.4.tar.gz)|Flex: a fast lexical analyser generator
|[fluxbox](http://fluxbox.sourceforge.net/)|[1.3.7](http://downloads.sourceforge.net/fluxbox/fluxbox-1.3.7.tar.bz2)|Fluxbox: a fast, compact window manager based on Blackbox
|[freecad](https://www.freecadweb.org/)|[0.20.1](https://github.com/FreeCAD/FreeCAD/archive/0.20.1.tar.gz)|FreeCAD: a general purpose parametric 3D modeller for CAD
|[freetype](https://www.freetype.org/)|[2.12.1](http://downloads.sourceforge.net/freetype/freetype-2.12.1.tar.xz)|FreeType: a free, quality, portable font engine
|[gawk](http://www.gnu.org/software/gawk/gawk.html)|[5.1.1](https://ftp.gnu.org/gnu/gawk/gawk-5.1.1.tar.xz)|GNU Gawk: a free version of awk, a string manipulation language
|[gcc](http://gcc.gnu.org/)|[12.2.0](http://ftp.gnu.org/gnu/gcc/gcc-12.2.0/gcc-12.2.0.tar.xz)|GNU GCC: the GNU compiler collection
|[gettext](http://www.gnu.org/software/gettext/)|[0.21](https://ftp.gnu.org/gnu/gettext/gettext-0.21.tar.xz)|GNU gettext: the GNU internationalisation (i18n) library
|[ghostscript](http://www.ghostscript.com/)|[9.56.1](https://github.com/ArtifexSoftware/ghostpdl-downloads/releases/download/gs9540/ghostscript-9.56.1.tar.gz)|Ghostscript: an interpreter for the PostScript language and PDF
|[gimp](https://www.gimp.org/)|[2.10.32](https://download.gimp.org/mirror/pub/gimp/v2.10/gimp-2.10.32.tar.bz2)|GIMP: the GNU Image Manipulation Program
|[git](https://git-scm.com/)|[2.37.2](https://github.com/git/git/archive/v2.37.2.tar.gz)|Git: an open source version control system
|[glade](https://glade.gnome.org/)|[3.40.0](https://download.gnome.org/sources/glade/3.40/glade-3.40.0.tar.xz)|Glade: a GUI builder for GTK+ and GNOME
|[glibc](http://www.gnu.org/software/libc/libc.html)|[2.36](http://ftp.gnu.org/gnu/glibc/glibc-2.36.tar.xz)|glibc: a C library for use with GNU/Hurd and GNU/Linux
|[gnome-shell](https://wiki.gnome.org/Projects/GnomeShell)|[42.4](https://download.gnome.org/sources/gnome-shell/42/gnome-shell-42.4.tar.xz)|GNOME Shell: a core user interface of the GNOME 3 desktop
|[gnucash](http://www.gnucash.org/)|[4.11](http://downloads.sourceforge.net/gnucash/gnucash-4.11.tar.bz2)|GNUCash: an open source personal finance suite
|[gnumeric](http://www.gnumeric.org/)|[1.12.52](https://download.gnome.org/sources/gnumeric/1.12/gnumeric-1.12.52.tar.xz)|Gnumeric: a spreadsheet and a part of the GNOME Desktop
|[gnupg](https://www.gnupg.org/)|[2.3.7](https://gnupg.org/ftp/gcrypt/gnupg/gnupg-2.3.7.tar.bz2)|GnuPG: a tool for secure communication and data storage
|[gparted](http://gparted.sourceforge.net/)|[1.4.0](http://downloads.sourceforge.net/gparted/gparted-1.4.0.tar.gz)|GParted: a disk partition editor application for GNOME
|[grep](http://www.gnu.org/software/grep/grep.html)|[3.7](http://ftp.gnu.org/gnu/grep/grep-3.7.tar.xz)|GNU Grep: a program to search for strings inside a file
|[groff](http://www.gnu.org/software/groff/groff.html)|[1.22.4](https://ftp.gnu.org/gnu/groff/groff-1.22.4.tar.gz)|GNU Groff: a device-independent document processor/formatter
|[grub](http://www.gnu.org/software/grub/)|[2.06](https://ftp.gnu.org/gnu/grub/grub-2.06.tar.xz)|GRUB: the GRand Unified Bootloader
|[gstreamer](https://gstreamer.freedesktop.org/)|[1.20.3](https://gstreamer.freedesktop.org/src/gstreamer/gstreamer-1.20.3.tar.xz)|GStreamer: a multimedia framework with a plugin-based architecture for a variety of platforms
|[gtk](https://www.gtk.org/)|[4.6.7](https://download.gnome.org/sources/gtk/4.6/gtk-4.6.7.tar.xz)|GTK: a multi-platform toolkit for creating GUIs
|[gzip](http://www.gnu.org/software/gzip/gzip.html)|[1.12](https://ftp.gnu.org/gnu/gzip/gzip-1.12.tar.gz)|gzip: a compression utility designed to replace compress
|[hexchat](https://hexchat.github.io/)|[2.16.1](https://dl.hexchat.net/hexchat/hexchat-2.16.1.tar.xz)|HexChat: an IRC client
|[hplip](https://developers.hp.com/hp-linux-imaging-and-printing)|[3.22.6](http://downloads.sourceforge.net/hplip/hplip-3.22.6.tar.gz)|hplip: Hewlett-Packard's Linux imaging and printing software
|[httpd](http://httpd.apache.org/)|[2.4.54](https://archive.apache.org/dist/httpd/httpd-2.4.54.tar.bz2)|httpd: a high-performance HTTP server, Apache 2.x version series
|[ibus](https://github.com/ibus/ibus/wiki)|[1.5.27](https://github.com/ibus/ibus/archive/1.5.27.tar.gz)|IBus: an intelligent input bus for Linux and UNIX
|[icewm](https://ice-wm.org/)|[2.9.9](https://github.com/ice-wm/icewm/releases/download/2.9.9/icewm-2.9.9.tar.lz)|IceWM: an X Window manager that emulates the looks of Motif, OS/2 and Windows
|[ImageMagick](https://imagemagick.org/)|[7.1.0-47](https://github.com/ImageMagick/ImageMagick/archive/7.1.0-47.tar.gz)|ImageMagick: a software suite to create, edit and compose bitmap images
|[inkscape](https://www.inkscape.org/)|[1.2.1](https://inkscape.org/gallery/item/33449/inkscape-1.2_2022-05-15_dc2aedaf03.tar.xz)|Inkscape: a drawing tool that uses the W3C standard scalable vector graphics format (SVG)
|[iptables](http://www.netfilter.org/projects/iptables/)|[1.8.8](http://www.netfilter.org/projects/iptables/files/iptables-1.8.8.tar.bz2)|iptables: enables the creation of packet alteration and firewall rules
|[k3b](http://www.k3b.org/)|[22.08.0](https://github.com/KDE/k3b/archive/v22.08.0.tar.gz)|K3b: a KDE-GUI for cdrecord and cdrdao, similar to Nero
|[kdevelop](https://www.kdevelop.org/)|[22.08.0](https://github.com/KDE/kdevelop/archive/refs/tags/v22.08.0.tar.gz)|KDevelop: a C/C++ development environment
|[kmod](https://www.kernel.org/pub/linux/utils/kernel/kmod/)|[30](https://www.kernel.org/pub/linux/utils/kernel/kmod/kmod-30.tar.xz)|kmod: a set of programs for loading, inserting and removing kernel modules
|[kmymoney](https://kmymoney.org/)|[5.1.3](https://download.kde.org/stable/kmymoney/5.1.3/src/kmymoney-5.1.3.tar.xz)|KMyMoney: a personal finance manager for KDE
|[kodi](https://kodi.tv/)|[19.4](https://github.com/xbmc/xbmc/archive/19.4-Matrix.tar.gz)|Kodi: a media player and entertainment hub for digital media
|[krita](https://krita.org/)|[5.1.0](https://download.kde.org/stable/krita/5.1.0/krita-5.1.0.tar.xz)|Krita: a cross-platform application that offers an end-to-end solution for creating digital art files from scratch
|[krusader](http://krusader.sourceforge.net/)|[2.7.2](http://download.kde.org/stable/krusader/2.7.2/krusader-2.7.2.tar.xz)|Krusader: an advanced twin panel (commander style) file manager for KDE
|[ktorrent](https://www.kde.org/applications/internet/ktorrent/)|[22.08.0](https://github.com/KDE/ktorrent/archive/v22.08.0.tar.gz)|KTorrent: a BitTorrent program for KDE
|[less](http://www.greenwoodsoftware.com/less/)|[590](http://www.greenwoodsoftware.com/less/less-590.tar.gz)|Less: a paginator that allows backward and forward movement
|[lftp](http://lftp.yar.ru/)|[4.9.2](http://lftp.yar.ru/ftp/lftp-4.9.2.tar.xz)|LFTP: a sophisticated FTP/HTTP client, file transfer program
|[libdvdcss](https://www.videolan.org/developers/libdvdcss.html)|[1.4.3](https://download.videolan.org/pub/libdvdcss/1.4.3/libdvdcss-1.4.3.tar.bz2)|libdvdcss: a library designed for accessing DVDs like a block device
|[libreoffice](http://www.libreoffice.org/)|[7.4.0](https://download.documentfoundation.org/libreoffice/stable/7.4.0/)|LibreOffice: a free personal productivity suite
|[libressl](http://www.libressl.org/)|[3.5.3](http://ftp.openbsd.org/pub/OpenBSD/LibreSSL/libressl-3.5.3.tar.gz)|LibreSSL: an implementation of SSL and TLS protocols, forked from OpenSSL
|[libselinux](http://userspace.selinuxproject.org/)|[3.4](https://github.com/SELinuxProject/selinux/archive/libselinux-3.4.tar.gz)|libselinux: a library providing an interface for security-aware applications in SELinux
|[libtool](http://www.gnu.org/software/libtool/)|[2.4.7](https://ftp.gnu.org/gnu/libtool/libtool-2.4.7.tar.gz)|GNU Libtool: a generic library support script
|[libvirt](http://libvirt.org/)|[8.6.0](https://libvirt.org/sources/libvirt-8.6.0.tar.xz)|libvirt: a toolkit to interact with the virtualization capabilities of the Linux kernel
|[libvorbis](http://www.vorbis.com/)|[1.3.7](http://downloads.xiph.org/releases/vorbis/libvorbis-1.3.7.tar.gz)|libvorbis: a free high-quality lossy audio codec library
|[lighttpd](http://www.lighttpd.net/)|[1.4.66](http://download.lighttpd.net/lighttpd/releases-1.4.x/lighttpd-1.4.66.tar.xz)|lighttpd: a secure, fast, compliant and flexible web server optimized for high-performance environments
|[lilo](http://www.joonet.de/lilo/)|[24.2](http://www.joonet.de/lilo/ftp/sources/lilo-24.2.tar.gz)|LILO: a boot loader for x86 computers
|[links](http://links.twibright.com/)|[2.27](http://links.twibright.com/download/links-2.27.tar.bz2)|Links: a text and graphics mode web browser similar to Lynx
|[linux](https://www.kernel.org/)|[5.19.5](https://www.kernel.org/pub/linux/kernel/v5.x/linux-5.19.5.tar.xz)|Linux kernel: a UNIX clone written from scratch by Linus Torvalds
|[llvm](http://llvm.org/)|[14.0.6](https://github.com/llvm/llvm-project/releases/download/llvmorg-14.0.6/llvm-14.0.6.src.tar.xz)|LLVM: a collection of modular and reusable compiler and toolchain technologies
|[lua](https://www.lua.org/)|[5.4.4](https://www.lua.org/ftp/lua-5.4.4.tar.gz)|Lua: a powerful, efficient, lightweight, embeddable scripting language
|[lumina](https://lumina-desktop.org/)|[1.6.2](https://github.com/lumina-desktop/lumina/archive/v1.6.2.tar.gz)|Lumina: a lightweight desktop environment for use on any UNIX-like operating system
|[lvm](https://sourceware.org/lvm2/)|[2.03.16](https://sourceware.org/pub/lvm2/LVM2.2.03.16.tgz)|LVM: the logical volume manager
|[lxpanel](https://sourceforge.net/projects/lxde/)|[0.10.1](http://downloads.sourceforge.net/lxde/lxpanel-0.10.1.tar.xz)|LXDE: a lightweight, fast and energy-saving desktop environment
|[lxqt-panel](https://github.com/lxqt/lxqt-panel)|[1.1.0](https://github.com/lxde/lxqt-panel/releases/download/1.1.0/lxqt-panel-1.1.0.tar.xz)|LXQt: a Qt port of the LXDE desktop environment
|[lynx](http://lynx.browser.org/)|[2.8.9](https://invisible-mirror.net/archives/lynx/tarballs/lynx2.8.9rel.1.tar.bz2)|Lynx: a text browser for the web
|[lyx](http://www.lyx.org/)|[2.3.6.1](http://ftp.lyx.org/pub/lyx/stable/2.3.x/lyx-2.3.6.1.tar.xz)|LyX: an advanced open source document processor
|[lzip](http://www.nongnu.org/lzip/lzip.html)|[1.23](http://download.savannah.gnu.org/releases/lzip/lzip-1.23.tar.lz)|Lzip: a lossless data compressor
|[m4](http://www.gnu.org/software/m4/)|[1.4.19](https://ftp.gnu.org/gnu/m4/m4-1.4.19.tar.xz)|GNU M4: the GNU m4 macro processor
|[make](http://www.gnu.org/software/make/)|[4.3](https://ftp.gnu.org/gnu/make/make-4.3.tar.lz)|GNU make: a tool which controls the generation of executables from the program's source files
|[man-db](http://man-db.nongnu.org/)|[2.10.2](http://download.savannah.nongnu.org/releases/man-db/man-db-2.10.2.tar.xz)|man-db: an implementation of the standard UNIX documentation system
|[man-pages](https://www.kernel.org/doc/man-pages/)|[5.13](https://www.kernel.org/pub/linux/docs/man-pages/man-pages-5.13.tar.xz)|Man Pages: files containing the manual pages displayed by man
|[mariadb](https://mariadb.org/)|[10.9.2](https://ftp.osuosl.org/pub/mariadb/mariadb-10.9.2/source/mariadb-10.9.2.tar.gz)|MariaDB: a robust SQL server, a fork of MySQL
|[mate-desktop](http://mate-desktop.org/)|[1.26.0](http://pub.mate-desktop.org/releases/1.26/mate-desktop-1.26.0.tar.xz)|MATE: a traditional desktop environment forked from GNOME 2
|[mc](http://www.midnight-commander.org/)|[4.8.28](http://www.midnight-commander.org/downloads/mc-4.8.28.tar.bz2)|GNU Midnight Commander: a file manager
|[mesa](http://www.mesa3d.org/)|[22.1.7](https://mesa.freedesktop.org/archive/mesa-22.1.7.tar.xz)|Mesa: a 3D graphics library
|[midori](https://astian.org/en/midori-browser/)|[9.0](https://github.com/midori-browser/core/releases/download/v9.0/midori-v9.0.tar.gz)|Midori: a lightweight web browser
|[mod_perl](http://perl.apache.org/)|[2.0.12](http://archive.apache.org/dist/perl/mod_perl-2.0.12.tar.gz)|mod_perl: provides a Perl module for httpd
|[MPlayer](http://www.mplayerhq.hu/)|[1.5](https://mplayerhq.hu/MPlayer/releases/MPlayer-1.5.tar.xz)|MPlayer: a movie and animation player
|[mutt](http://www.mutt.org/)|[2.2.7](http://ftp.mutt.org/pub/mutt/mutt-2.2.7.tar.gz)|Mutt: a text-based MIME Email client
|[mypaint](http://mypaint.org/)|[2.0.1](https://github.com/mypaint/mypaint/releases/download/v2.0.1/mypaint-2.0.1.tar.xz)|MyPaint: a nimble, distraction-free and easy tool for digital painters
|[mysql](https://dev.mysql.com/downloads/mysql/)|[8.0.30](https://cdn.mysql.com/Downloads/MySQL-8.0/mysql-8.0.30.tar.gz)|MySQL: an SQL database server
|[mythtv](https://www.mythtv.org/)|[32.0](https://github.com/MythTV/mythtv/archive/v32.0.tar.gz)|MythTV: an open-source software digital video recorder (DVR) project
|[nano](https://www.nano-editor.org/)|[6.4](https://www.nano-editor.org/dist/latest/nano-6.4.tar.gz)|GNU nano: a curse-based text editor for UNIX
|[nautilus](https://wiki.gnome.org/Apps/Files)|[42.2](https://download.gnome.org/sources/nautilus/42/nautilus-42.2.tar.xz)|Nautilus: a file manager for the GNOME desktop
|[ncurses](https://invisible-island.net/ncurses/)|[6.3](https://invisible-mirror.net/archives/ncurses/ncurses-6.3.tar.gz)|GNU ncurses: a programming library allowing a programmer to write text user interfaces in a terminal-independent manner
|[netbeans](https://netbeans.apache.org/)|[14](https://www-eu.apache.org/dist/netbeans/netbeans/14/netbeans-14-source.zip)|NetBeans: a full-featured cross-platform IDE written in Java
|[NetworkManager](https://wiki.gnome.org/Projects/NetworkManager)|[1.40.0](https://download.gnome.org/sources/NetworkManager/1.40/NetworkManager-1.40.0.tar.xz)|NetworkManager: a utility aimed at simplifying the use of computer networks on Linux
|[nginx](http://nginx.org/)|[1.22.0](http://nginx.org/download/nginx-1.22.0.tar.gz)|nginx: an HTTP and reverse proxy server
|[nmap](http://www.insecure.org/nmap/)|[7.92](http://download.insecure.org/nmap/dist/nmap-7.92.tgz)|Nmap: a utility for network exploration or security auditing
|[ntfs-3g](https://www.tuxera.com/community/ntfs-3g-download/)|[2022.5.17](https://tuxera.com/opensource/ntfs-3g_ntfsprogs-2022.5.17.tgz)|NTFS-3G: a read/write NTFS driver
|[nuspell](https://nuspell.github.io/)|[5.1.0](https://github.com/nuspell/nuspell/archive/refs/tags/v5.1.0.tar.gz)|Nuspell: a spelling checker software program
|[NVIDIA](http://www.nvidia.com/object/unix.html)|[515.65.01](https://us.download.nvidia.com/XFree86/Linux-x86_64/515.65.01/NVIDIA-Linux-x86_64-515.65.01.run)|NVIDIA: a proprietary display driver for Linux, FreeBSD and Solaris
|[octave](http://www.gnu.org/software/octave/)|[7.2.0](http://ftp.gnu.org/gnu/octave/octave-7.2.0.tar.xz)|GNU Octave: a high-level interpreted language intended for numerical computations
|[openbox](http://openbox.org/)|[3.6.1](http://openbox.org/dist/openbox/openbox-3.6.1.tar.gz)|Openbox: a standards-compliant, lightweight, extensible window manager
|[openjdk](https://openjdk.java.net/)|[18.0.1](https://download.java.net/java/GA/jdk18.0.1/3f48cabb83014f9fab465e280ccf630b/10/GPL/openjdk-18.0.1_linux-x64_bin.tar.gz)|OpenJDK: a complete and free implementation of Java SE, the core Java platform
|[openldap](https://www.openldap.org/)|[2.6.3](https://openldap.org/software/download/OpenLDAP/openldap-release/openldap-2.6.3.tgz)|OpenLDAP: a full-featured open source LDAP software suite
|[openshot](https://www.openshot.org/)|[2.6.1](https://github.com/OpenShot/openshot-qt/archive/v2.6.1.tar.gz)|OpenShot: a video editor
|[openssh](http://www.openssh.com/portable.html)|[9.0p1](https://ftp3.usa.openbsd.org/pub/OpenBSD/OpenSSH/portable/openssh-9.0p1.tar.gz)|OpenSSH: a client and server for encrypted remote logins and file transfers
|[openssl](https://www.openssl.org/)|[3.0.5](https://ftp.openssl.org/source/openssl-3.0.5.tar.gz)|OpenSSL: a library for providing encrypted transport layers
|[opera](https://www.opera.com/)|[90.0.4480.54](https://ftp.opera.com/pub/opera/desktop/90.0.4480.54/linux/)|Opera: a light-weight graphical web browser
|[pacman](https://archlinux.org/pacman/)|[6.0.1](https://gitlab.archlinux.org/pacman/pacman/-/archive/v6.0.1/pacman-v6.0.1.tar.bz2)|pacman: a utility which manages software packages in Linux
|[parted](http://www.gnu.org/software/parted/parted.html)|[3.5](https://ftp.gnu.org/gnu/parted/parted-3.5.tar.xz)|GNU Parted: a program to create, destroy, resize and copy PC disk partitions
|[pcmanfm](http://pcmanfm.sourceforge.net/)|[1.3.2](http://downloads.sourceforge.net/pcmanfm/pcmanfm-1.3.2.tar.xz)|PCManFM: an extremely fast and lightweight file manager
|[perl](https://www.perl.org)|[5.36.0](http://www.cpan.org/src/5.0/perl-5.36.0.tar.gz)|Perl: Larry Wall's Practical Extraction and Reporting Language
|[php](http://www.php.net/)|[8.1.9](http://us3.php.net/distributions/php-8.1.9.tar.xz)|PHP: a server-side HTML embedded scripting language
|[phpMyAdmin](https://www.phpmyadmin.net/)|[5.2.0](https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.zip)|phpMyAdmin: a tool written in PHP intended to handle the administration of MySQL over the web
|[pidgin](http://pidgin.im/)|[2.14.10](http://downloads.sourceforge.net/pidgin/pidgin-2.14.10.tar.bz2)|Pidgin: an instant messenger client for several protocols (formerly GAIM)
|[pipewire](https://pipewire.org/)|[0.3.56](https://gitlab.freedesktop.org/pipewire/pipewire/-/archive/0.3.56/pipewire-0.3.56.tar.bz2)|PipeWire: a server for handling audio and video streams and hardware on Linux
|[pitivi](http://www.pitivi.org/)|[2022.06](https://download.gnome.org/sources/pitivi/2022.06/pitivi-2022.06.tar.xz)|PiTiVi: a free and open-source video editor for Linux
|[plasma-desktop](https://kde.org/plasma-desktop/)|[5.25.4](https://download.kde.org/stable/plasma/5.25.4/plasma-desktop-5.25.4.tar.xz)|Plasma Desktop: a desktop environment
|[postfix](http://www.postfix.org/)|[3.7.2](https://de.postfix.org/ftpmirror/official//postfix-3.7.2.tar.gz)|Postfix: a mail transport agent
|[postgresql](https://www.postgresql.org/)|[14.5](https://ftp.postgresql.org/pub/source/v14.5/postgresql-14.5.tar.bz2)|PostgreSQL: a relational database management system
|[ppp](http://www.samba.org/ppp/)|[2.4.9](https://github.com/paulusmack/ppp/archive/ppp-2.4.9.tar.gz)|PPP: provides a server/client for point to point protocol
|[privoxy](http://www.privoxy.org/)|[3.0.33](http://downloads.sourceforge.net/ijbswa/privoxy-3.0.33-stable-src.tar.gz)|Privoxy: a non-caching web proxy with advanced filtering capabilities for enhancing privacy
|[pulseaudio](http://www.pulseaudio.org/)|[16.1](http://freedesktop.org/software/pulseaudio/releases/pulseaudio-16.1.tar.xz)|PulseAudio: a sound server for POSIX and Win32 systems
|[Python](https://www.python.org/)|[3.10.6](https://www.python.org/ftp/python/3.10.6/Python-3.10.6.tgz)|Python: an interpreted, interactive, object-oriented programming language
|[qbittorrent](https://www.qbittorrent.org/)|[4.4.4](http://downloads.sourceforge.net/qbittorrent/qbittorrent-4.4.4.tar.xz)|qBittorrent: a P2P BitTorrent client
|[qemu](http://wiki.qemu.org/)|[7.0.0](http://wiki.qemu.org/download/qemu-7.0.0.tar.xz)|QEMU: an open source machine emulator and virtualiser
|[qt](https://www.qt.io/)|[6.3.1](https://download.qt-project.org/official_releases/qt/6.3/6.3.1/single/qt-everywhere-src-6.3.1.tar.xz)|Qt: a C++ application framework for writing graphical applications
|[qt-creator](https://wiki.qt.io/Qt_Creator)|[8.0.1](https://download.qt.io/official_releases/qtcreator/7.0/8.0.1/qt-creator-opensource-src-8.0.1.tar.gz)|Qt Creator: a cross-platform IDE tailored to the needs of Qt developers
|[reiserfsprogs](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/)|[3.6.27](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/v3.6.27/reiserfsprogs-3.6.27.tar.xz)|reiserfsprogs: contains tools for using Reiser file system
|[rpm](https://rpm.org/)|[4.17.1](https://github.com/rpm-software-management/rpm/archive/refs/tags/rpm-4.17.1.tar.gz)|RPM: a package management system originally developed by Red Hat
|[rp-pppoe](https://dianne.skoll.ca/projects/rp-pppoe/)|[3.15](https://dianne.skoll.ca/projects/rp-pppoe/download/rp-pppoe-3.15.tar.gz)|RP-PPPoE: a PPP over Ethernet client/server suite
|[rsync](http://rsync.samba.org/)|[3.2.5](http://rsync.samba.org/ftp/rsync/rsync-3.2.5.tar.gz)|rsync: an open source utility that provides fast, incremental file transfer
|[ruby](http://www.ruby-lang.org/)|[3.1.2](https://ftp.ruby-lang.org/pub/ruby/3.1/ruby-3.1.2.tar.xz)|Ruby: interpreted, dynamically typed, pure object-oriented scripting language
|[rust](https://www.rust-lang.org/)|[1.63.0](https://github.com/rust-lang/rust/archive/1.63.0.tar.gz)|Rust: a systems programming language that runs blazingly fast, prevents segfaults and guarantees thread safety
|[samba](https://www.samba.org/)|[4.16.4](https://us1.samba.org/samba/ftp/stable/samba-4.16.4.tar.gz)|Samba: a free software re-implementation of SMB/CIFS networking protocol
|[sane-backends](http://www.sane-project.org/)|[1.1.1](https://gitlab.com/sane-project/backends/-/archive/1.1.1/backends-1.1.1.tar.bz2)|SANE: a universal scanner interface
|[screen](http://www.gnu.org/software/screen/)|[4.9.0](http://ftp.gnu.org/gnu/screen/screen-4.9.0.tar.gz)|Screen: multiplexes a physical terminal
|[scribus](https://www.scribus.net/)|[1.4.8](http://downloads.sourceforge.net/scribus/scribus-1.4.8.tar.xz)|Scribus: A desktop publishing program for Linux using the Qt library
|[seamonkey](http://www.seamonkey-project.org/)|[2.53.13](https://ftp.mozilla.org/pub/seamonkey/releases/2.53.13/source/seamonkey-2.53.13.source.tar.xz)|Mozilla SeaMonkey: a web browser, e-mail and newsgroup client, IRC chat client and HTML editor
|[sed](http://www.gnu.org/software/sed/)|[4.8](https://ftp.gnu.org/gnu/sed/sed-4.8.tar.xz)|GNU sed: a stream-oriented non-interactive text editor
|[sendmail](http://www.sendmail.org/)|[8.17.1](https://ftp.sendmail.org/sendmail.8.17.1.tar.gz)|Sendmail: a powerful and flexible Mail Transport Agent
|[shim](https://github.com/rhboot/shim)|[15.6](https://github.com/rhboot/shim/archive/shim-15.6.tar.gz)|shim: a bootloader to chain-load signed bootloaders under Secure Boot
|[shotwell](https://wiki.gnome.org/Apps/Shotwell)|[0.30.16](https://download.gnome.org/sources/shotwell/0.30/shotwell-0.30.16.tar.xz)|Shotwell: an open-source digital photo organiser for GNOME
|[snapd](https://snapcraft.io/)|[2.57.1](https://github.com/snapcore/snapd/archive/2.57.1.tar.gz)|snapd: a tool to support and manage .snap applications that are portable across different Linux systems
|[snort](https://www.snort.org/)|[3.1.40.0](https://snort.org/downloads/snortplus/snort3-3.1.40.0.tar.gz)|Snort: a light-weight network intrusion detection program
|[SpamAssassin](http://spamassassin.apache.org/)|[3.4.6](http://www.apache.org/dist/spamassassin/source/Mail-SpamAssassin-3.4.6.tar.bz2)|SpamAssassin: a mail filter which attempts to identify spam using text analysis
|[sqlite](http://www.sqlite.org/)|[3.39.2](https://www.sqlite.org/2022/sqlite-amalgamation-3390200.zip)|SQLite: an embeddable SQL engine in a C library
|[squid](http://www.squid-cache.org/)|[5.6](http://www.squid-cache.org/Versions/v5/squid-5.6.tar.xz)|Squid: a full-featured web proxy cache
|[subversion](http://subversion.apache.org/)|[1.14.2](http://www.apache.org/dist/subversion/subversion-1.14.2.tar.bz2)|Subversion: a version control system
|[sylpheed](http://sylpheed.sraoss.jp/en/)|[3.7.0](http://sylpheed.sraoss.jp/sylpheed/v3.7/sylpheed-3.7.0.tar.xz)|Sylpheed: an e-mail client and news reader based on GTK+
|[synaptic](https://tracker.debian.org/pkg/synaptic)|[0.91.2](https://deb.debian.org/debian/pool/main/s/synaptic/synaptic_0.91.2.+nmu1.tar.xz)|Synaptic: a graphical front-end for APT
|[systemd](http://www.freedesktop.org/wiki/Software/systemd/)|[251.4](https://github.com/systemd/systemd-stable/archive/refs/tags/v251.4.tar.gz)|systemd: a system and service manager for Linux
|[sysvinit](https://github.com/slicer69/sysvinit)|[3.05](https://github.com/slicer69/sysvinit/releases/download/3.05/sysvinit-3.05.tar.xz)|SysVinit: the Linux System V Init
|[tar](http://www.gnu.org/software/tar/)|[1.34](https://ftp.gnu.org/gnu/tar/tar-1.34.tar.xz)|GNU Tar: a utility for creating tar archives
|[tcl](http://core.tcl.tk/tcl/)|[8.6.12](http://downloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz)|TCL: a powerful and dynamic programming language
|[tcpdump](http://www.tcpdump.org/)|[4.99.1](http://www.tcpdump.org/release/tcpdump-4.99.1.tar.gz)|TCPDUMP: a command-line packet sniffer and network debugging tool
|[texinfo](http://www.gnu.org/software/texinfo/)|[6.8](https://ftp.gnu.org/gnu/texinfo/texinfo-6.8.tar.xz)|GNU Texinfo: a collection of utilities that generate online help and printed manuals
|[texlive](https://www.tug.org/texlive/)|[2022](https://tug.org/texlive/Images/texlive2022.iso)|TeX Live: a collection of programs for typesetting, previewing and printing of TeX documents
|[thunderbird](http://www.mozilla.org/products/thunderbird/)|[102.2.0](https://ftp.mozilla.org/pub/thunderbird/releases/102.2.0/source/thunderbird-102.2.0.source.tar.xz)|Mozilla Thunderbird: a full-featured e-mail and newsgroup client
|[tigervnc](http://www.tigervnc.org/)|[1.12.0](https://github.com/TigerVNC/tigervnc/archive/v1.12.0.tar.gz)|TigerVNC: a high-performance, platform-neutral implementation of VNC (Virtual Network Computing)
|[tmux](http://tmux.github.io/)|[3.3a](https://github.com/tmux/tmux/releases/download/3.3a/tmux-3.3a.tar.gz)|tmux: a terminal multiplexer
|[tor](http://www.torproject.org/)|[0.4.7.10](http://www.torproject.org/dist/tor-0.4.7.10.tar.gz)|Tor: a network of virtual tunnels that allows people to improve privacy and security on the Internet
|[transmission](http://www.transmissionbt.com/)|[3.00](https://github.com/transmission/transmission-releases/raw/master/transmission-3.00.tar.xz)|Transmission: a BitTorrent client
|[util-linux](https://github.com/karelzak/util-linux)|[2.38.1](http://www.kernel.org/pub/linux/utils/util-linux/v2.38/util-linux-2.38.1.tar.xz)|util-linux: a collection of essential utilities for Linux systems
|[vim](https://www.vim.org/)|[9.0](http://ftp.vim.org/pub/vim/unix/vim-9.0.tar.bz2)|Vim: an improved version of the editor "vi", one of the standard text editors on UNIX
|[VirtualBox](https://www.virtualbox.org/)|[6.1.36](http://download.virtualbox.org/virtualbox/6.1.36/VirtualBox-6.1.36.tar.bz2)|VirtualBox: a family of x86 virtualisation products for enterprise and home use
|[vivaldi](https://vivaldi.com/)|[5.4.2753.40](https://source.vivaldi.com/vivaldi-source_5.2.2623.tar.xz)|Vivaldi: a free, cross-platform, proprietary web browser developed by Vivaldi Technologies
|[vlc](http://www.videolan.org/streaming/)|[3.0.17.4](http://download.videolan.org/pub/videolan/vlc/3.0.17.4/vlc-3.0.17.4.tar.xz)|VLC: a cross-platform media player and streaming server
|[wayland](https://wayland.freedesktop.org/)|[1.21.0](https://wayland.freedesktop.org/releases/wayland-1.21.0.tar.xz)|Wayland: a display server protocol
|[webmin](http://www.webmin.com/)|[2.000](http://downloads.sourceforge.net/webadmin/webmin-2.000.tar.gz)|Webmin: a web-based interface for Unix system administration
|[wget](https://www.gnu.org/software/wget/)|[2.0.1](https://ftp.gnu.org/gnu/wget/wget2-2.0.1.tar.gz)|wget: retrieves files from web and FTP sites
|[WindowMaker](http://www.windowmaker.org/)|[0.95.9](http://windowmaker.org/pub/source/release/WindowMaker-0.95.9.tar.gz)|Window Maker: an X11 window manager, similar to NeXTSTEP
|[wine](http://www.winehq.org/)|[7.0](http://dl.winehq.org/wine/source/7.0/wine-7.0.tar.xz)|Wine: an open source implementation of the Windows API on top of X, OpenGL and Unix
|[wireshark](https://www.wireshark.org/)|[3.6.7](https://www.wireshark.org/download/src/wireshark-3.6.7.tar.xz)|Wireshark: a network protocol analyzer
|[wordpress](https://wordpress.org/)|[6.0.1](https://wordpress.org/wordpress-6.0.1.tar.gz)|WordPress: publishing software for the world wide web
|[xfdesktop](http://www.xfce.org/)|[4.16.1](http://archive.xfce.org/src/xfce/xfdesktop/4.16/xfdesktop-4.16.1.tar.bz2)|Xfdesktop: a desktop manager for the Xfce desktop
|[xfsprogs](http://xfs.org/)|[5.19.0](https://www.kernel.org/pub/linux/utils/fs/xfs/xfsprogs/xfsprogs-5.19.0.tar.xz)|xfsprogs: a set of utilities for managing the XFS file system
|[xine-lib](http://www.xine-project.org/)|[1.2.12](http://downloads.sourceforge.net/xine/xine-lib-1.2.12.tar.xz)|xine-lib: contains the libraries for xine, a free video player
|[xorg-server](https://www.x.org/)|[21.1.4](https://www.x.org/archive/individual/xserver/xorg-server-21.1.4.tar.xz)|X.Org: the X.Org Foundation's public implementation of the X Window System
|[xz](https://tukaani.org/xz/)|[5.2.6](https://tukaani.org/xz/xz-5.2.6.tar.xz)|XZ Utils: data compression software with high compression ratio
|[zfs](https://openzfs.org/)|[2.1.5](https://github.com/openzfs/zfs/releases/download/zfs-2.1.5/zfs-2.1.5.tar.gz)|ZFS: an advanced file system and volume manager maintained by the Illumos community
|[zlib](http://www.zlib.net/)|[1.2.12](http://www.zlib.net/zlib-1.2.12.tar.xz)|zlib: a legally unencumbered lossless data compression library

