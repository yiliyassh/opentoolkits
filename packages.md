## Packages Tracked by DistroWatch （229个包）    |  [返回](README.md)
- [ Last Update: Friday 4 August 2023 12:53 GMT ](https://distrowatch.com/packages.php)  
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
|[alsa-lib](https://www.alsa-project.org/)|[1.2.9](https://www.alsa-project.org/files/pub/lib/alsa-lib-1.2.9.tar.bz2)|alsa-lib: an audio library for use with the ALSA kernel modules
|[amdgpu](https://gitlab.freedesktop.org/xorg/driver/xf86-video-amdgpu)|[23.0.0](https://xorg.freedesktop.org/archive/individual/driver/xf86-video-amdgpu-23.0.0.tar.xz)|amdgpu: an X.Org driver for AMD RADEON-based video cards
|[apache-tomcat](https://tomcat.apache.org/)|[10.1.11](https://www.apache.org/dist/tomcat/tomcat-10/v10.1.11/src/apache-tomcat-10.1.11-src.tar.gz)|apache-tomcat: a Java Servlet and JSP Container
|[apt](https://tracker.debian.org/pkg/apt)|[2.7.3](https://deb.debian.org/debian/pool/main/a/apt/apt_2.7.3.tar.xz)|APT: a front-end for the dpkg package manager
|[audacity](https://www.audacityteam.org/)|[3.3.3](https://github.com/audacity/audacity/releases/download/Audacity-3.3.3/audacity-sources-3.3.3.tar.gz)|Audacity: a free audio editor
|[autoconf](https://www.gnu.org/software/autoconf/autoconf.html)|[2.71](https://ftp.gnu.org/gnu/autoconf/autoconf-2.71.tar.xz)|Autoconf: a package of M4 macros to produce scripts to automatically configure source code
|[automake](https://www.gnu.org/software/automake/)|[1.16.5](https://ftp.gnu.org/gnu/automake/automake-1.16.5.tar.xz)|GNU Automake: a tool for automatically generating Makefiles
|[avidemux](http://fixounet.free.fr/avidemux/)|[2.8.1](https://downloads.sourceforge.net/avidemux/avidemux_2.8.1.tar.gz)|Avidemux: a free video editor designed for simple cutting, filtering and encoding tasks
|[awesome](https://awesome.naquadah.org/)|[4.3](https://github.com/awesomeWM/awesome/releases/download/v4.3/awesome-4.3.tar.xz)|awesome: a configurable window manager for X
|[bash](https://www.gnu.org/software/bash/bash.html)|[5.2.15](https://ftp.gnu.org/gnu/bash/bash-5.2.15.tar.gz)|Bash: an sh-compatible command language interpreter
|[bind](https://www.isc.org/downloads/bind/)|[9.18.17](https://ftp.isc.org/isc/bind9/9.18.17/bind-9.18.17.tar.xz)|ISC BIND: an implementation of the Domain Name System (DNS) protocols
|[binutils](https://www.gnu.org/software/binutils/binutils.html)|[2.41](https://ftp.gnu.org/gnu/binutils/binutils-2.41.tar.gz)|GNU Binutils: an essential collection of binary utilities
|[bison](https://www.gnu.org/software/bison/bison.html)|[3.8.2](https://ftp.gnu.org/gnu/bison/bison-3.8.2.tar.xz)|Bison: a replacement for the parser generator Yacc
|[bitcoin](https://bitcoin.org/)|[25.0](https://github.com/bitcoin/bitcoin/archive/v25.0.tar.gz)|Bitcoin: an innovative payment network and a new kind of money
|[blender](https://www.blender.org/)|[3.6.1](https://download.blender.org/source/blender-3.6.1.tar.xz)|Blender: a very fast and versatile 3D modeller and renderer
|[budgie-desktop](https://github.com/BuddiesOfBudgie/budgie-desktop)|[10.7.2](https://github.com/BuddiesOfBudgie/budgie-desktop/releases/download/v10.7.2/budgie-desktop-v10.7.2.tar.xz)|Budgie Desktop: a simple desktop environment featuring heavy integration with the GNOME stack
|[busybox](https://www.busybox.net/)|[1.36.1](https://www.busybox.net/downloads/busybox-1.36.1.tar.bz2)|BusyBox: a program that combines many common UNIX utilities into a single small executable
|[bzip2](https://sourceware.org/bzip2/)|[1.0.8](https://sourceware.org/pub/bzip2/bzip2-1.0.8.tar.gz)|bzip2: a free, patent-free, high-quality data compressor
|[calibre](https://calibre-ebook.com/)|[6.24.0](https://download.calibre-ebook.com/6.24.0/calibre-6.24.0.tar.xz)|Calibre: an e-book library management application
|[calligra](https://calligra.org/)|[3.2.1](https://download.kde.org/stable/calligra/3.2.1/calligra-3.2.1.tar.xz)|Calligra: an integrated office suite based on the KDE libraries
|[cdrkit](https://tracker.debian.org/pkg/cdrkit)|[1.1.11](https://deb.debian.org/debian/pool/main/c/cdrkit/cdrkit_1.1.11.orig.tar.gz)|cdrkit: a collection of applications related to creation of optical disk media
|[chromium](http://www.chromium.org/Home)|[115.0.5790.170](http://src.chromium.org/viewvc/chrome/)|Google Chromium: an open-source edition of Google Chrome, a graphical web browser
|[cinnamon](https://github.com/linuxmint/cinnamon/)|[5.8.4](https://github.com/linuxmint/Cinnamon/archive/5.8.4.tar.gz)|Cinnamon: a desktop environment developed by Linux Mint
|[clamav](https://www.clamav.net/)|[1.1.0](https://github.com/Cisco-Talos/clamav/releases/download/clamav-1.1.0/clamav-1.1.0.tar.gz)|ClamAV: an open-source antivirus engine for detecting trojans, viruses, malware and other malicious threats
|[cmake](https://cmake.org/)|[3.27.1](https://github.com/Kitware/CMake/releases/download/v3.27.1/cmake-3.27.1.tar.gz)|cmake: a cross-platform, open-source build system
|[coreutils](https://www.gnu.org/software/coreutils/)|[9.3](https://ftp.gnu.org/gnu/coreutils/coreutils-9.3.tar.xz)|GNU Coreutils: provides basic file, shell and text manipulation utilities
|[cryptsetup](https://gitlab.com/cryptsetup/cryptsetup)|[2.6.1](https://www.kernel.org/pub/linux/utils/cryptsetup/v2.6/cryptsetup-2.6.1.tar.xz)|cryptsetup: a utility for setting up disk encryption based on the DMCrypt kernel module
|[cups](https://openprinting.github.io/)|[2.4.6](https://github.com/OpenPrinting/cups/releases/download/v2.4.6/cups-2.4.6-source.tar.gz)|CUPS: a UNIX printing system based on the Internet Printing Protocol
|[curl](https://curl.se/)|[8.2.1](https://github.com/curl/curl/releases/download/curl-8_1_1/curl-8.2.1.tar.xz)|cURL: a command line tool for transferring files with URL syntax
|[cvs](https://cvs.nongnu.org/)|[1.11.23](https://ftp.gnu.org/non-gnu/cvs/source/stable/1.11.23/cvs-1.11.23.tar.bz2)|CVS: a version control system
|[db](https://www.oracle.com/technetwork/database/database-technologies/berkeleydb/downloads/index.html)|[18.1.40](https://www.oracle.com/technetwork/database/database-technologies/berkeleydb/downloads/index.html)|Berkeley DB: a family of open source developer databases from Oracle
|[deluge](https://deluge-torrent.org/)|[2.1.1](https://download.deluge-torrent.org/source/2.1/deluge-2.1.1.tar.xz)|Deluge: a lightweight, cross-platform BitTorrent client
|[devede](https://www.rastersoft.com/programas/devede.html)|[4.17.0](https://gitlab.com/rastersoft/devedeng/-/archive/4.17.0/devedeng-4.17.0.tar.bz2)|DeVeDe: a program to create video DVDs and CDs suitables for home players
|[dhcp](https://www.isc.org/downloads/dhcp/)|[4.4.3-P1](https://downloads.isc.org/isc/dhcp/4.4.3-P1/dhcp-4.4.3-P1.tar.gz)|ISC DHCP: a server and client for automatic IP configuration
|[diffutils](https://www.gnu.org/software/diffutils/)|[3.10](https://ftp.gnu.org/gnu/diffutils/diffutils-3.10.tar.xz)|GNU Diffutils: a utility which finds differences between and among files
|[digikam](https://www.digikam.org/)|[8.1.0](https://download.kde.org/stable/digikam/8.1.0/digiKam-8.1.0.tar.xz)|Digikam: an advanced digital photo management application
|[dillo](https://www.dillo.org/)|[3.0.5](https://www.dillo.org/download/dillo-3.0.5.tar.bz2)|Dillo: a lightweight, alternative browser for UNIX systems
|[dnf](https://github.com/rpm-software-management/dnf/)|[4.16.2](https://github.com/rpm-software-management/dnf/archive/4.16.2.tar.gz)|DNF: a new package management library and a fork of yum
|[docker](https://www.docker.com/community-edition)|[24.0.5](https://github.com/moby/moby/archive/refs/tags/v24.0.5.tar.gz)|Docker: a program that performs operating-system-level virtualisation, also known as "containerisation"
|[dosbox](https://dosbox.sourceforge.net/)|[0.74-3](https://downloads.sourceforge.net/dosbox/dosbox-0.74-3.tar.gz)|DOSBox: a DOS emulator
|[dovecot](https://www.dovecot.org/)|[2.3.20](https://www.dovecot.org/releases/2.3/dovecot-2.3.20.tar.gz)|Dovecot: an open source IMAP and POP3 server for Linux/UNIX-like systems
|[doxygen](https://www.doxygen.nl/)|[1.9.7](https://doxygen.nl/files/doxygen-1.9.7.src.tar.gz)|Doxygen: a documentation system for C++, Java, C and IDL
|[dracut](https://dracut.wiki.kernel.org/index.php/Main_Page)|[059](https://github.com/dracutdevs/dracut/releases/download/059/dracut-059.tar.xz)|dracut: the event driven initramfs infrastructure
|[e2fsprogs](https://e2fsprogs.sourceforge.net/)|[1.47.0](https://downloads.sourceforge.net/e2fsprogs/e2fsprogs-1.47.0.tar.gz)|e2fsprogs: contains the required utilities for the EXT2 file system
|[eclipse](https://eclipse.org/)|[4.28](https://download.eclipse.org/eclipse/downloads/)|Eclipse: a universal tool platform and IDE
|[efibootmgr](https://github.com/rhinstaller/efibootmgr)|[18](https://github.com/rhinstaller/efibootmgr/releases/download/18/efibootmgr-18.tar.bz2)|efibootmgr: a Linux user-space application to modify the Intel EFI boot manager
|[emacs](https://www.gnu.org/software/emacs/)|[29.1](https://ftp.gnu.org/gnu/emacs/emacs-29.1.tar.xz)|GNU Emacs: the extensible, self-documenting real-time display editor
|[enlightenment](https://enlightenment.org/)|[0.25.4](https://download.enlightenment.org/rel/apps/enlightenment/enlightenment-0.25.4.tar.xz)|Enlightenment: a window manager for X
|[evolution](https://wiki.gnome.org/Apps/Evolution)|[3.48.4](https://download.gnome.org/sources/evolution/3.48/evolution-3.48.4.tar.xz)|Evolution: information management software providing mail, address book and calendaring functionality
|[exim](https://www.exim.org/)|[4.96](https://ftp.exim.org/pub/exim/exim4/exim-4.96.tar.xz)|exim: a mail server
|[ffmpeg](https://ffmpeg.org/)|[6.0](https://ffmpeg.org/releases/ffmpeg-6.0.tar.xz)|FFmpeg: a complete, cross-platform solution to record, convert and stream audio and video
|[file](https://www.darwinsys.com/file/)|[5.45](https://ftp.astron.com/pub/file/file-5.45.tar.gz)|file: a program that attempts to classify files by their content
|[findutils](https://www.gnu.org/software/findutils/)|[4.9.0](https://ftp.gnu.org/gnu/findutils/findutils-4.7.0.tar.xz)|GNU Findutils: a set of tools to find files and to operate on groups of files
|[firebird](https://www.firebirdsql.org/)|[4.0.3](https://github.com/FirebirdSQL/firebird/archive/refs/tags/v4.0.3.tar.gz)|Firebird: a relational database offering many ANSI SQL standard features that runs on Linux, Windows and UNIX
|[firefox](https://www.mozilla.org/products/firefox/)|[116.0.1](https://ftp.mozilla.org/pub/firefox/releases/116.0.1/source/firefox-116.0.1.source.tar.xz)|Mozilla Firefox: a web browser for Windows, Linux, macOS, FreeBSD and Android
|[firejail](https://firejail.wordpress.com/)|[0.9.72](https://downloads.sourceforge.net/firejail/firejail-0.9.72.tar.xz)|Firejail: a Linux namespaces sandbox program
|[flatpak](https://flatpak.org/)|[1.14.4](https://github.com/flatpak/flatpak/releases/download/1.14.4/flatpak-1.14.4.tar.xz)|Flatpak: a framework for Linux application sandboxing and distribution
|[flex](https://github.com/westes/flex)|[2.6.4](https://github.com/westes/flex/releases/download/v2.6.4/flex-2.6.4.tar.gz)|Flex: a fast lexical analyser generator
|[fluxbox](https://fluxbox.sourceforge.net/)|[1.3.7](https://downloads.sourceforge.net/fluxbox/fluxbox-1.3.7.tar.bz2)|Fluxbox: a fast, compact window manager based on Blackbox
|[freecad](https://www.freecadweb.org/)|[0.21](https://github.com/FreeCAD/FreeCAD/archive/0.21.tar.gz)|FreeCAD: a general purpose parametric 3D modeller for CAD
|[freetype](https://www.freetype.org/)|[2.13.1](https://downloads.sourceforge.net/freetype/freetype-2.13.1.tar.xz)|FreeType: a free, quality, portable font engine
|[gawk](https://www.gnu.org/software/gawk/gawk.html)|[5.2.2](https://ftp.gnu.org/gnu/gawk/gawk-5.2.2.tar.xz)|GNU Gawk: a free version of awk, a string manipulation language
|[gcc](https://gcc.gnu.org/)|[13.2.0](https://ftp.gnu.org/gnu/gcc/gcc-13.2.0/gcc-13.2.0.tar.xz)|GNU GCC: the GNU compiler collection
|[gettext](https://www.gnu.org/software/gettext/)|[0.22](https://ftp.gnu.org/gnu/gettext/gettext-0.22.tar.xz)|GNU gettext: the GNU internationalisation (i18n) library
|[ghostscript](https://www.ghostscript.com/)|[10.01.2](https://github.com/ArtifexSoftware/ghostpdl-downloads/releases/download/gs10012/ghostscript-10.01.2.tar.xzhttps://github.com/ArtifexSoftware/ghostpdl-downloads/releases/download/gs1001/ghostscript-10.01.1.tar.xz)|Ghostscript: an interpreter for the PostScript language and PDF
|[gimp](https://www.gimp.org/)|[2.10.34](https://download.gimp.org/mirror/pub/gimp/v2.10/gimp-2.10.34.tar.bz2)|GIMP: the GNU Image Manipulation Program
|[git](https://git-scm.com/)|[2.41.0](https://github.com/git/git/archive/v2.41.0.tar.gz)|Git: an open source version control system
|[glade](https://glade.gnome.org/)|[3.40.0](https://download.gnome.org/sources/glade/3.40/glade-3.40.0.tar.xz)|Glade: a GUI builder for GTK+ and GNOME
|[glibc](https://www.gnu.org/software/libc/libc.html)|[2.38](https://ftp.gnu.org/gnu/glibc/glibc-2.38.tar.xz)|glibc: a C library for use with GNU/Hurd and GNU/Linux
|[gnome-shell](https://wiki.gnome.org/Projects/GnomeShell)|[44.3](https://download.gnome.org/sources/gnome-shell/44/gnome-shell-44.3.tar.xz)|GNOME Shell: a core user interface of the GNOME 3 desktop
|[gnucash](https://www.gnucash.org/)|[5.3](https://downloads.sourceforge.net/gnucash/gnucash-5.3.tar.bz2)|GNUCash: an open source personal finance suite
|[gnumeric](http://www.gnumeric.org/)|[1.12.55](https://download.gnome.org/sources/gnumeric/1.12/gnumeric-1.12.55.tar.xz)|Gnumeric: a spreadsheet and a part of the GNOME Desktop
|[gnupg](https://www.gnupg.org/)|[2.4.3](https://gnupg.org/ftp/gcrypt/gnupg/gnupg-2.4.3.tar.bz2)|GnuPG: a tool for secure communication and data storage
|[gparted](https://gparted.sourceforge.net/)|[1.5.0](https://downloads.sourceforge.net/gparted/gparted-1.5.0.tar.gz)|GParted: a disk partition editor application for GNOME
|[grep](https://www.gnu.org/software/grep/grep.html)|[3.11](https://ftp.gnu.org/gnu/grep/grep-3.11.tar.xz)|GNU Grep: a program to search for strings inside a file
|[groff](https://www.gnu.org/software/groff/groff.html)|[1.23.0](https://ftp.gnu.org/gnu/groff/groff-1.23.0.tar.gz)|GNU Groff: a device-independent document processor/formatter
|[grub](https://www.gnu.org/software/grub/)|[2.06](https://ftp.gnu.org/gnu/grub/grub-2.06.tar.xz)|GRUB: the GRand Unified Bootloader
|[gstreamer](https://gstreamer.freedesktop.org/)|[1.22.5](https://gstreamer.freedesktop.org/src/gstreamer/gstreamer-1.22.5.tar.xz)|GStreamer: a multimedia framework with a plugin-based architecture for a variety of platforms
|[gtk](https://www.gtk.org/)|[4.10.4](https://download.gnome.org/sources/gtk/4.10/gtk-4.10.4.tar.xz)|GTK: a multi-platform toolkit for creating GUIs
|[gzip](https://www.gnu.org/software/gzip/gzip.html)|[1.12](https://ftp.gnu.org/gnu/gzip/gzip-1.12.tar.gz)|gzip: a compression utility designed to replace compress
|[hplip](https://developers.hp.com/hp-linux-imaging-and-printing)|[3.23.5](https://downloads.sourceforge.net/hplip/hplip-3.23.5.tar.gz)|hplip: Hewlett-Packard's Linux imaging and printing software
|[httpd](https://httpd.apache.org/)|[2.4.57](https://archive.apache.org/dist/httpd/httpd-2.4.57.tar.bz2)|httpd: a high-performance HTTP server, Apache 2.x version series
|[ibus](https://github.com/ibus/ibus/wiki)|[1.5.28](https://github.com/ibus/ibus/archive/1.5.28.tar.gz)|IBus: an intelligent input bus for Linux and UNIX
|[icewm](https://ice-wm.org/)|[3.4.1](https://github.com/ice-wm/icewm/releases/download/3.4.1/icewm-3.4.1.tar.lz)|IceWM: an X Window manager that emulates the looks of Motif, OS/2 and Windows
|[ImageMagick](https://imagemagick.org/)|[7.1.1-15](https://github.com/ImageMagick/ImageMagick/archive/7.1.1-15.tar.gz)|ImageMagick: a software suite to create, edit and compose bitmap images
|[inkscape](https://www.inkscape.org/)|[1.3](https://inkscape.org/gallery/item/42328/inkscape-1.3.tar.xz)|Inkscape: a drawing tool that uses the W3C standard scalable vector graphics format (SVG)
|[iptables](https://www.netfilter.org/projects/iptables/)|[1.8.9](https://www.netfilter.org/projects/iptables/files/iptables-1.8.9.tar.bz2)|iptables: enables the creation of packet alteration and firewall rules
|[k3b](https://apps.kde.org/en-gb/k3b/)|[23.04.3](https://github.com/KDE/k3b/archive/v23.04.3.tar.gz)|K3b: a KDE-GUI for cdrecord and cdrdao, similar to Nero
|[kdevelop](https://www.kdevelop.org/)|[23.04.3](https://github.com/KDE/kdevelop/archive/refs/tags/v23.04.3.tar.gz)|KDevelop: a C/C++ development environment
|[kmod](https://www.kernel.org/pub/linux/utils/kernel/kmod/)|[30](https://www.kernel.org/pub/linux/utils/kernel/kmod/kmod-30.tar.xz)|kmod: a set of programs for loading, inserting and removing kernel modules
|[kodi](https://kodi.tv/)|[20.2](https://github.com/xbmc/xbmc/archive/20.2-Nexus.tar.gz)|Kodi: a media player and entertainment hub for digital media
|[krita](https://krita.org/)|[5.1.5](https://download.kde.org/stable/krita/5.1.5/krita-5.1.5.tar.xz)|Krita: a cross-platform application that offers an end-to-end solution for creating digital art files from scratch
|[krusader](https://krusader.sourceforge.net/)|[2.8.0](https://download.kde.org/stable/krusader/2.8.0/krusader-2.8.0.tar.xz)|Krusader: an advanced twin panel (commander style) file manager for KDE
|[ktorrent](https://www.kde.org/applications/internet/ktorrent/)|[23.04.3](https://github.com/KDE/ktorrent/archive/v23.04.3.tar.gz)|KTorrent: a BitTorrent program for KDE
|[less](http://www.greenwoodsoftware.com/less/)|[633](http://www.greenwoodsoftware.com/less/less-633.tar.gz)|Less: a paginator that allows backward and forward movement
|[lftp](https://lftp.yar.ru/)|[4.9.2](https://lftp.yar.ru/ftp/lftp-4.9.2.tar.xz)|LFTP: a sophisticated FTP/HTTP client, file transfer program
|[libdvdcss](https://www.videolan.org/developers/libdvdcss.html)|[1.4.3](https://download.videolan.org/pub/libdvdcss/1.4.3/libdvdcss-1.4.3.tar.bz2)|libdvdcss: a library designed for accessing DVDs like a block device
|[libreoffice](https://www.libreoffice.org/)|[7.5.5](https://download.documentfoundation.org/libreoffice/stable/7.5.5/)|LibreOffice: a free personal productivity suite
|[libressl](https://www.libressl.org/)|[3.7.3](https://ftp.openbsd.org/pub/OpenBSD/LibreSSL/libressl-3.7.3.tar.gz)|LibreSSL: an implementation of SSL and TLS protocols, forked from OpenSSL
|[libselinux](http://userspace.selinuxproject.org/)|[3.5](https://github.com/SELinuxProject/selinux/archive/libselinux-3.5.tar.gz)|libselinux: a library providing an interface for security-aware applications in SELinux
|[libtool](https://www.gnu.org/software/libtool/)|[2.4.7](https://ftp.gnu.org/gnu/libtool/libtool-2.4.7.tar.gz)|GNU Libtool: a generic library support script
|[libvirt](https://libvirt.org/)|[9.6.0](https://libvirt.org/sources/libvirt-9.6.0.tar.xz)|libvirt: a toolkit to interact with the virtualization capabilities of the Linux kernel
|[libvorbis](https://xiph.org/vorbis/)|[1.3.7](https://downloads.xiph.org/releases/vorbis/libvorbis-1.3.7.tar.gz)|libvorbis: a free high-quality lossy audio codec library
|[lighttpd](https://www.lighttpd.net/)|[1.4.71](https://download.lighttpd.net/lighttpd/releases-1.4.x/lighttpd-1.4.71.tar.xz)|lighttpd: a secure, fast, compliant and flexible web server optimized for high-performance environments
|[lilo](https://www.joonet.de/lilo/)|[24.2](https://www.joonet.de/lilo/ftp/sources/lilo-24.2.tar.gz)|LILO: a boot loader for x86 computers
|[links](http://links.twibright.com/)|[2.29](http://links.twibright.com/download/links-2.29.tar.bz2)|Links: a text and graphics mode web browser similar to Lynx
|[linux](https://www.kernel.org/)|[6.4.8](https://www.kernel.org/pub/linux/kernel/v6.x/linux-6.4.8.tar.xz)|Linux kernel: a UNIX clone written from scratch by Linus Torvalds
|[llvm](https://llvm.org/)|[16.0.6](https://github.com/llvm/llvm-project/releases/download/llvmorg-16.0.6/llvm-16.0.6.src.tar.xz)|LLVM: a collection of modular and reusable compiler and toolchain technologies
|[lua](https://www.lua.org/)|[5.4.6](https://www.lua.org/ftp/lua-5.4.6.tar.gz)|Lua: a powerful, efficient, lightweight, embeddable scripting language
|[lumina](https://lumina-desktop.org/)|[1.6.2](https://github.com/lumina-desktop/lumina/archive/v1.6.2.tar.gz)|Lumina: a lightweight desktop environment for use on any UNIX-like operating system
|[lvm](https://sourceware.org/lvm2/)|[2.03.22](https://sourceware.org/pub/lvm2/LVM2.2.03.22.tgz)|LVM: the logical volume manager
|[lxpanel](https://sourceforge.net/projects/lxde/)|[0.10.1](https://downloads.sourceforge.net/lxde/lxpanel-0.10.1.tar.xz)|LXDE: a lightweight, fast and energy-saving desktop environment
|[lxqt-panel](https://github.com/lxqt/lxqt-panel)|[1.3.0](https://github.com/lxde/lxqt-panel/releases/download/1.3.0/lxqt-panel-1.3.0.tar.xz)|LXQt: a Qt port of the LXDE desktop environment
|[lynx](https://lynx.browser.org/)|[2.8.9](https://invisible-mirror.net/archives/lynx/tarballs/lynx2.8.9rel.1.tar.bz2)|Lynx: a text browser for the web
|[lyx](https://www.lyx.org/)|[2.3.7-1](http://ftp.lyx.org/pub/lyx/stable/2.3.x/lyx-2.3.7-1.tar.xz)|LyX: an advanced open source document processor
|[lzip](https://www.nongnu.org/lzip/lzip.html)|[1.23](https://download.savannah.gnu.org/releases/lzip/lzip-1.23.tar.lz)|Lzip: a lossless data compressor
|[m4](https://www.gnu.org/software/m4/)|[1.4.19](https://ftp.gnu.org/gnu/m4/m4-1.4.19.tar.xz)|GNU M4: the GNU m4 macro processor
|[make](https://www.gnu.org/software/make/)|[4.4.1](https://ftp.gnu.org/gnu/make/make-4.4.1.tar.lz)|GNU make: a tool which controls the generation of executables from the program's source files
|[man-db](https://man-db.nongnu.org/)|[2.11.2](https://download.savannah.nongnu.org/releases/man-db/man-db-2.11.2.tar.xz)|man-db: an implementation of the standard UNIX documentation system
|[man-pages](https://www.kernel.org/doc/man-pages/)|[6.05.01](https://www.kernel.org/pub/linux/docs/man-pages/man-pages-6.05.01.tar.xz)|Man Pages: files containing the manual pages displayed by man
|[mariadb](https://mariadb.org/)|[11.0.2](https://ftp.osuosl.org/pub/mariadb/mariadb-11.0.2/source/mariadb-11.0.2.tar.gz)|MariaDB: a robust SQL server, a fork of MySQL
|[mate-desktop](https://mate-desktop.org/)|[1.26.1](https://pub.mate-desktop.org/releases/1.26/mate-desktop-1.26.1.tar.xz)|MATE: a traditional desktop environment forked from GNOME 2
|[mc](https://www.midnight-commander.org/)|[4.8.29](https://www.midnight-commander.org/downloads/mc-4.8.29.tar.bz2)|GNU Midnight Commander: a file manager
|[mesa](https://www.mesa3d.org/)|[23.1.5](https://mesa.freedesktop.org/archive/mesa-23.1.5.tar.xz)|Mesa: a 3D graphics library
|[midori](https://astian.org/en/midori-browser/)|[9.0](https://github.com/midori-browser/core/releases/download/v9.0/midori-v9.0.tar.gz)|Midori: a lightweight web browser
|[mod_perl](https://perl.apache.org/)|[2.0.12](https://archive.apache.org/dist/perl/mod_perl-2.0.12.tar.gz)|mod_perl: provides a Perl module for httpd
|[MPlayer](https://www.mplayerhq.hu/)|[1.5](https://mplayerhq.hu/MPlayer/releases/MPlayer-1.5.tar.xz)|MPlayer: a movie and animation player
|[mutt](http://www.mutt.org/)|[2.2.10](http://ftp.mutt.org/pub/mutt/mutt-2.2.10.tar.gz)|Mutt: a text-based MIME Email client
|[mypaint](https://github.com/mypaint/mypaint)|[2.0.1](https://github.com/mypaint/mypaint/releases/download/v2.0.1/mypaint-2.0.1.tar.xz)|MyPaint: a nimble, distraction-free and easy tool for digital painters
|[mysql](https://dev.mysql.com/downloads/mysql/)|[8.1.0](https://cdn.mysql.com/Downloads/MySQL-8.1/mysql-8.1.0.tar.gz)|MySQL: an SQL database server
|[mythtv](https://www.mythtv.org/)|[33.1](https://github.com/MythTV/mythtv/archive/v33.1.tar.gz)|MythTV: an open-source software digital video recorder (DVR) project
|[nano](https://www.nano-editor.org/)|[7.2](https://www.nano-editor.org/dist/latest/nano-7.2.tar.gz)|GNU nano: a curse-based text editor for UNIX
|[nautilus](https://wiki.gnome.org/Apps/Files)|[44.2.1](https://download.gnome.org/sources/nautilus/44/nautilus-44.2.1.tar.xz)|Nautilus: a file manager for the GNOME desktop
|[ncurses](https://invisible-island.net/ncurses/)|[6.4](https://invisible-mirror.net/archives/ncurses/ncurses-6.4.tar.gz)|GNU ncurses: a programming library allowing a programmer to write text user interfaces in a terminal-independent manner
|[netbeans](https://netbeans.apache.org/)|[18](https://github.com/apache/netbeans/archive/refs/tags/18.tar.gz)|NetBeans: a full-featured cross-platform IDE written in Java
|[NetworkManager](https://wiki.gnome.org/Projects/NetworkManager)|[1.42.8](https://download.gnome.org/sources/NetworkManager/1.40/NetworkManager-1.42.8.tar.xz)|NetworkManager: a utility aimed at simplifying the use of computer networks on Linux
|[nftables](https://www.nftables.org/)|[1.0.8](https://www.nftables.org/projects/nftables/files/nftables-1.0.8.tar.xz)|nftables: a subsystem of the Linux kernel providing filtering and classification of network packets
|[nginx](https://nginx.org/)|[1.24.0](https://nginx.org/download/nginx-1.24.0.tar.gz)|nginx: an HTTP and reverse proxy server
|[nmap](https://www.insecure.org/nmap/)|[7.94](https://download.insecure.org/nmap/dist/nmap-7.94.tgz)|Nmap: a utility for network exploration or security auditing
|[ntfs-3g](https://www.tuxera.com/community/ntfs-3g-download/)|[2022.10.3](https://tuxera.com/opensource/ntfs-3g_ntfsprogs-2022.10.3.tgz)|NTFS-3G: a read/write NTFS driver
|[nuspell](https://nuspell.github.io/)|[5.1.2](https://github.com/nuspell/nuspell/archive/refs/tags/v5.1.2.tar.gz)|Nuspell: a spelling checker software program
|[NVIDIA](https://www.nvidia.com/object/unix.html)|[535.86.05](https://us.download.nvidia.com/XFree86/Linux-x86_64/535.86.05/NVIDIA-Linux-x86_64-535.86.05.run)|NVIDIA: a proprietary display driver for Linux, FreeBSD and Solaris
|[octave](https://www.gnu.org/software/octave/)|[8.2.0](https://ftp.gnu.org/gnu/octave/octave-8.2.0.tar.xz)|GNU Octave: a high-level interpreted language intended for numerical computations
|[openbox](http://openbox.org/)|[3.6.1](http://openbox.org/dist/openbox/openbox-3.6.1.tar.gz)|Openbox: a standards-compliant, lightweight, extensible window manager
|[openjdk](https://openjdk.java.net/)|[20.0.1](https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1_linux-x64_bin.tar.gz)|OpenJDK: a complete and free implementation of Java SE, the core Java platform
|[openldap](https://www.openldap.org/)|[2.6.6](https://openldap.org/software/download/OpenLDAP/openldap-release/openldap-2.6.6.tgz)|OpenLDAP: a full-featured open source LDAP software suite
|[openshot](https://www.openshot.org/)|[3.1.1](https://github.com/OpenShot/openshot-qt/archive/v3.1.1.tar.gz)|OpenShot: a video editor
|[openssh](https://www.openssh.com/portable.html)|[9.3p2](https://ftp3.usa.openbsd.org/pub/OpenBSD/OpenSSH/portable/openssh-9.3p2.tar.gz)|OpenSSH: a client and server for encrypted remote logins and file transfers
|[openssl](https://www.openssl.org/)|[3.1.2](https://ftp.openssl.org/source/openssl-3.1.2.tar.gz)|OpenSSL: a library for providing encrypted transport layers
|[openvpn](https://openvpn.net/community/)|[2.6.5](https://swupdate.openvpn.org/community/releases/openvpn-2.6.5.tar.gz)|OpenVPN: an open-source VPN daemon
|[opera](https://www.opera.com/)|[101.0.4843.33](https://ftp.opera.com/pub/opera/desktop/101.0.4843.33/linux/)|Opera: a light-weight graphical web browser
|[pacman](https://archlinux.org/pacman/)|[6.0.2](https://gitlab.archlinux.org/pacman/pacman/-/archive/v6.0.2/pacman-v6.0.2.tar.bz2)|pacman: a utility which manages software packages in Linux
|[parted](https://www.gnu.org/software/parted/parted.html)|[3.6](https://ftp.gnu.org/gnu/parted/parted-3.6.tar.xz)|GNU Parted: a program to create, destroy, resize and copy PC disk partitions
|[pcmanfm](https://sourceforge.net/projects/pcmanfm/)|[1.3.2](https://downloads.sourceforge.net/pcmanfm/pcmanfm-1.3.2.tar.xz)|PCManFM: an extremely fast and lightweight file manager
|[perl](https://www.perl.org)|[5.38.0](https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz)|Perl: Larry Wall's Practical Extraction and Reporting Language
|[php](https://www.php.net/)|[8.2.9](https://www.php.net/distributions/php-8.2.9.tar.xz)|PHP: a server-side HTML embedded scripting language
|[phpMyAdmin](https://www.phpmyadmin.net/)|[5.2.1](https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.zip)|phpMyAdmin: a tool written in PHP intended to handle the administration of MySQL over the web
|[pidgin](https://pidgin.im/)|[2.14.12](https://downloads.sourceforge.net/pidgin/pidgin-2.14.12.tar.bz2)|Pidgin: an instant messenger client for several protocols (formerly GAIM)
|[pipewire](https://pipewire.org/)|[0.3.77](https://gitlab.freedesktop.org/pipewire/pipewire/-/archive/0.3.77/pipewire-0.3.77.tar.bz2)|PipeWire: a server for handling audio and video streams and hardware on Linux
|[pitivi](https://www.pitivi.org/)|[2023.03](https://download.gnome.org/sources/pitivi/2023/pitivi-2023.03.tar.xz)|PiTiVi: a free and open-source video editor for Linux
|[plasma-desktop](https://kde.org/plasma-desktop/)|[5.27.7](https://download.kde.org/stable/plasma/5.27.7/plasma-desktop-5.27.7.tar.xz)|Plasma Desktop: a desktop environment
|[postfix](https://www.postfix.org/)|[3.8.1](https://de.postfix.org/ftpmirror/official//postfix-3.8.1.tar.gz)|Postfix: a mail transport agent
|[postgresql](https://www.postgresql.org/)|[15.3](https://ftp.postgresql.org/pub/source/v15.3/postgresql-15.3.tar.bz2)|PostgreSQL: a relational database management system
|[ppp](https://www.samba.org/ppp/)|[2.5.0](https://github.com/paulusmack/ppp/archive/ppp-2.5.0.tar.gz)|PPP: provides a server/client for point to point protocol
|[privoxy](https://www.privoxy.org/)|[3.0.34](https://downloads.sourceforge.net/ijbswa/privoxy-3.0.34-stable-src.tar.gz)|Privoxy: a non-caching web proxy with advanced filtering capabilities for enhancing privacy
|[pulseaudio](https://www.freedesktop.org/wiki/Software/PulseAudio/)|[16.1](https://freedesktop.org/software/pulseaudio/releases/pulseaudio-16.1.tar.xz)|PulseAudio: a sound server for POSIX and Win32 systems
|[Python](https://www.python.org/)|[3.11.4](https://www.python.org/ftp/python/3.11.4/Python-3.11.4.tgz)|Python: an interpreted, interactive, object-oriented programming language
|[qbittorrent](https://www.qbittorrent.org/)|[4.5.4](https://downloads.sourceforge.net/qbittorrent/qbittorrent-4.5.4.tar.xz)|qBittorrent: a P2P BitTorrent client
|[qemu](https://qemu.org/)|[8.0.3](https://wiki.qemu.org/download/qemu-8.0.3.tar.xz)|QEMU: an open source machine emulator and virtualiser
|[qt](https://www.qt.io/)|[6.5.2](https://download.qt-project.org/official_releases/qt/6.5/6.5.2/single/qt-everywhere-src-6.5.2.tar.xz)|Qt: a C++ application framework for writing graphical applications
|[qt-creator](https://wiki.qt.io/Qt_Creator)|[11.0.1](https://download.qt.io/official_releases/qtcreator/11.0/11.0.1/qt-creator-opensource-src-11.0.1.tar.gz)|Qt Creator: a cross-platform IDE tailored to the needs of Qt developers
|[reiserfsprogs](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/)|[3.6.27](https://www.kernel.org/pub/linux/kernel/people/jeffm/reiserfsprogs/v3.6.27/reiserfsprogs-3.6.27.tar.xz)|reiserfsprogs: contains tools for using Reiser file system
|[rpm](https://rpm.org/)|[4.18.1](https://github.com/rpm-software-management/rpm/archive/refs/tags/rpm-4.18.1-release.tar.gz)|RPM: a package management system originally developed by Red Hat
|[rp-pppoe](https://dianne.skoll.ca/projects/rp-pppoe/)|[4.0](https://dianne.skoll.ca/projects/rp-pppoe/download/rp-pppoe-4.0.tar.gz)|RP-PPPoE: a PPP over Ethernet client/server suite
|[rsync](https://rsync.samba.org/)|[3.2.7](https://rsync.samba.org/ftp/rsync/rsync-3.2.7.tar.gz)|rsync: an open source utility that provides fast, incremental file transfer
|[ruby](https://www.ruby-lang.org/)|[3.2.2](https://ftp.ruby-lang.org/pub/ruby/3.2/ruby-3.2.2.tar.xz)|Ruby: interpreted, dynamically typed, pure object-oriented scripting language
|[rust](https://www.rust-lang.org/)|[1.71.1](https://github.com/rust-lang/rust/archive/1.71.1.tar.gz)|Rust: a systems programming language that runs blazingly fast, prevents segfaults and guarantees thread safety
|[samba](https://www.samba.org/)|[4.18.5](https://us1.samba.org/samba/ftp/stable/samba-4.18.5.tar.gz)|Samba: a free software re-implementation of SMB/CIFS networking protocol
|[sane-backends](http://www.sane-project.org/)|[1.2.1](https://gitlab.com/sane-project/backends/-/archive/1.2.1/backends-1.2.1.tar.bz2)|SANE: a universal scanner interface
|[screen](https://www.gnu.org/software/screen/)|[4.9.0](https://ftp.gnu.org/gnu/screen/screen-4.9.0.tar.gz)|Screen: multiplexes a physical terminal
|[scribus](https://www.scribus.net/)|[1.4.8](https://downloads.sourceforge.net/scribus/scribus-1.4.8.tar.xz)|Scribus: A desktop publishing program for Linux using the Qt library
|[seamonkey](https://www.seamonkey-project.org/)|[2.53.17](https://ftp.mozilla.org/pub/seamonkey/releases/2.53.17/source/seamonkey-2.53.17.source.tar.xz)|Mozilla SeaMonkey: a web browser, e-mail and newsgroup client, IRC chat client and HTML editor
|[sed](https://www.gnu.org/software/sed/)|[4.9](https://ftp.gnu.org/gnu/sed/sed-4.9.tar.xz)|GNU sed: a stream-oriented non-interactive text editor
|[sendmail](https://www.proofpoint.com/us/products/email-protection/open-source-email-solution)|[8.17.2](https://ftp.sendmail.org/sendmail.8.17.2.tar.gz)|Sendmail: a powerful and flexible Mail Transport Agent
|[shim](https://github.com/rhboot/shim)|[15.7](https://github.com/rhboot/shim/archive/shim-15.7.tar.gz)|shim: a bootloader to chain-load signed bootloaders under Secure Boot
|[shotwell](https://wiki.gnome.org/Apps/Shotwell)|[0.32.2](https://download.gnome.org/sources/shotwell/0.32/shotwell-0.32.2.tar.xz)|Shotwell: an open-source digital photo organiser for GNOME
|[snapd](https://snapcraft.io/)|[2.60.2](https://github.com/snapcore/snapd/archive/2.60.2.tar.gz)|snapd: a tool to support and manage .snap applications that are portable across different Linux systems
|[snort](https://www.snort.org/)|[3.1.67.0](https://snort.org/downloads/snortplus/snort3-3.1.67.0.tar.gz)|Snort: a light-weight network intrusion detection program
|[SpamAssassin](https://spamassassin.apache.org/)|[4.0.0](https://www.apache.org/dist/spamassassin/source/Mail-SpamAssassin-4.0.0.tar.bz2)|SpamAssassin: a mail filter which attempts to identify spam using text analysis
|[sqlite](https://www.sqlite.org/)|[3.42.0](https://github.com/sqlite/sqlite/archive/refs/tags/version-3.42.0.tar.gz)|SQLite: an embeddable SQL engine in a C library
|[squid](http://www.squid-cache.org/)|[6.1](http://www.squid-cache.org/Versions/v6/squid-6.1.tar.gz)|Squid: a full-featured web proxy cache
|[subversion](https://subversion.apache.org/)|[1.14.2](https://www.apache.org/dist/subversion/subversion-1.14.2.tar.bz2)|Subversion: a version control system
|[sylpheed](https://sylpheed.sraoss.jp/en/)|[3.7.0](https://sylpheed.sraoss.jp/sylpheed/v3.7/sylpheed-3.7.0.tar.xz)|Sylpheed: an e-mail client and news reader based on GTK+
|[synaptic](https://tracker.debian.org/pkg/synaptic)|[0.91.3](https://deb.debian.org/debian/pool/main/s/synaptic/synaptic_0.91.3.+nmu1.tar.xz)|Synaptic: a graphical front-end for APT
|[systemd](https://www.freedesktop.org/wiki/Software/systemd/)|[254](https://github.com/systemd/systemd-stable/archive/refs/tags/v254.tar.gz)|systemd: a system and service manager for Linux
|[sysvinit](https://github.com/slicer69/sysvinit)|[3.07](https://github.com/slicer69/sysvinit/releases/download/3.07/sysvinit-3.07.tar.xz)|SysVinit: the Linux System V Init
|[tar](https://www.gnu.org/software/tar/)|[1.35](https://ftp.gnu.org/gnu/tar/tar-1.35.tar.xz)|GNU Tar: a utility for creating tar archives
|[tcl](https://core.tcl.tk/tcl/)|[8.6.13](https://downloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz)|TCL: a powerful and dynamic programming language
|[tcpdump](https://www.tcpdump.org/)|[4.99.4](https://www.tcpdump.org/release/tcpdump-4.99.4.tar.gz)|TCPDUMP: a command-line packet sniffer and network debugging tool
|[texinfo](https://www.gnu.org/software/texinfo/)|[7.0.3](https://ftp.gnu.org/gnu/texinfo/texinfo-7.0.3.tar.xz)|GNU Texinfo: a collection of utilities that generate online help and printed manuals
|[texlive](https://www.tug.org/texlive/)|[2023](https://tug.org/texlive/Images/texlive2023.iso)|TeX Live: a collection of programs for typesetting, previewing and printing of TeX documents
|[thunderbird](https://www.mozilla.org/products/thunderbird/)|[115.1.0](https://ftp.mozilla.org/pub/thunderbird/releases/115.1.0/source/thunderbird-115.1.0.source.tar.xz)|Mozilla Thunderbird: a full-featured e-mail and newsgroup client
|[tigervnc](https://www.tigervnc.org/)|[1.13.1](https://github.com/TigerVNC/tigervnc/archive/v1.13.1.tar.gz)|TigerVNC: a high-performance, platform-neutral implementation of VNC (Virtual Network Computing)
|[tmux](https://tmux.github.io/)|[3.3a](https://github.com/tmux/tmux/releases/download/3.3a/tmux-3.3a.tar.gz)|tmux: a terminal multiplexer
|[tor](https://www.torproject.org/)|[0.4.7.14](https://www.torproject.org/dist/tor-0.4.7.14.tar.gz)|Tor: a network of virtual tunnels that allows people to improve privacy and security on the Internet
|[transmission](https://www.transmissionbt.com/)|[4.0.3](https://github.com/transmission/transmission/releases/download/4.0.3/transmission-4.0.3.tar.xz)|Transmission: a BitTorrent client
|[util-linux](https://github.com/karelzak/util-linux)|[2.39.1](https://www.kernel.org/pub/linux/utils/util-linux/v2.39/util-linux-2.39.1.tar.xz)|util-linux: a collection of essential utilities for Linux systems
|[vim](https://www.vim.org/)|[9.0](http://ftp.vim.org/pub/vim/unix/vim-9.0.tar.bz2)|Vim: an improved version of the editor "vi", one of the standard text editors on UNIX
|[VirtualBox](https://www.virtualbox.org/)|[7.0.10](https://download.virtualbox.org/virtualbox/7.0.10/VirtualBox-7.0.10.tar.bz2)|VirtualBox: a family of x86 virtualisation products for enterprise and home use
|[vivaldi](https://vivaldi.com/)|[6.1.3035.257](https://source.vivaldi.com/vivaldi-source_5.2.2623.tar.xz)|Vivaldi: a free, cross-platform, proprietary web browser developed by Vivaldi Technologies
|[vlc](https://www.videolan.org/streaming/)|[3.0.18](https://download.videolan.org/pub/videolan/vlc/3.0.18/vlc-3.0.18.tar.xz)|VLC: a cross-platform media player and streaming server
|[wayland](https://wayland.freedesktop.org/)|[1.22.0](https://wayland.freedesktop.org/releases/wayland-1.22.0.tar.xz)|Wayland: a display server protocol
|[webmin](https://www.webmin.com/)|[2.100](https://downloads.sourceforge.net/webadmin/webmin-2.100.tar.gz)|Webmin: a web-based interface for Unix system administration
|[wget](https://www.gnu.org/software/wget/)|[2.0.1](https://ftp.gnu.org/gnu/wget/wget2-2.0.1.tar.gz)|wget: retrieves files from web and FTP sites
|[WindowMaker](https://www.windowmaker.org/)|[0.95.9](https://windowmaker.org/pub/source/release/WindowMaker-0.95.9.tar.gz)|Window Maker: an X11 window manager, similar to NeXTSTEP
|[wine](https://www.winehq.org/)|[8.0.2](https://dl.winehq.org/wine/source/8.0/wine-8.0.2.tar.xz)|Wine: an open source implementation of the Windows API on top of X, OpenGL and Unix
|[wireshark](https://www.wireshark.org/)|[4.0.7](https://www.wireshark.org/download/src/wireshark-4.0.7.tar.xz)|Wireshark: a network protocol analyzer
|[wordpress](https://wordpress.org/)|[6.2.2](https://wordpress.org/wordpress-6.2.2.tar.gz)|WordPress: publishing software for the world wide web
|[xfdesktop](https://www.xfce.org/)|[4.18.1](https://archive.xfce.org/src/xfce/xfdesktop/4.18/xfdesktop-4.18.1.tar.bz2)|Xfdesktop: a desktop manager for the Xfce desktop
|[xfsprogs](https://github.com/mtanski/xfsprogs)|[6.4.0](https://www.kernel.org/pub/linux/utils/fs/xfs/xfsprogs/xfsprogs-6.4.0.tar.xz)|xfsprogs: a set of utilities for managing the XFS file system
|[xine-lib](https://sourceforge.net/projects/xine/)|[1.2.13](https://downloads.sourceforge.net/xine/xine-lib-1.2.13.tar.xz)|xine-lib: contains the libraries for xine, a free video player
|[xorg-server](https://www.x.org/)|[21.1.8](https://www.x.org/archive/individual/xserver/xorg-server-21.1.8.tar.xz)|X.Org: the X.Org Foundation's public implementation of the X Window System
|[xz](https://tukaani.org/xz/)|[5.4.4](https://tukaani.org/xz/xz-5.4.4.tar.xz)|XZ Utils: data compression software with high compression ratio
|[zfs](https://openzfs.org/)|[2.1.12](https://github.com/openzfs/zfs/releases/download/zfs-2.1.12/zfs-2.1.12.tar.gz)|ZFS: an advanced file system and volume manager maintained by the Illumos community
|[zlib](https://www.zlib.net/)|[1.2.13](https://www.zlib.net/zlib-1.2.13.tar.xz)|zlib: a legally unencumbered lossless data compression library

