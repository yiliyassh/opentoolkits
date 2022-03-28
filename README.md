# 我常用的开源工具箱——my open source toolkits
- 自由分享是知识的本质 :+1::+1::+1:
***
## 开源办公套件
- openoffice https://zh-cn.libreoffice.org/
```
强大的开源办公软件，word,excle,ppt,visio,pdf制作等
```
- SumatraPDF https://www.sumatrapdfreader.org/free-pdf-reader
```
windows系统文档阅读器，支持：PDF, ePub, MOBI, CHM, XPS, DjVu, CBZ, CBR等格式。
```

## 开源音视频制作
- shotcut https://www.shotcut.org
```
简单易用，兼顾专业。
```
- openshot https://www.openshot.org/
```
切割分离方便。
```
- kdenlive https://kdenlive.org/en/
```
专业级别的好工具。
```
## 必备的实用工具
- Everything https://www.voidtools.com/zh-cn/
```
飞一样的搜索速度，高效率好帮手！
```
- FreeFilesSync https://freefilesync.org/
```
数据安全备份，镜像，增量同步。强烈推荐！！！
```
- FileZilla https://filezilla-project.org/
```
服务端搭建server，客户端文件上传下载，支持断点续传，ftp和sftp。强烈推荐！！！
```
- XnView https://www.xnview.com/en/xnview/
```
支持超过500种图片格式。强烈推荐！！！
```
- 7-zip https://www.7-zip.org/
```
必备：压缩解压利器。
```
- VeraCrypt https://www.veracrypt.fr/en/Home.html
```
磁盘加密工具，保护数据安全，文件和目录均可。
```
- Ventoy https://www.ventoy.net/cn/index.html
```
制作可启动U盘的开源工具。
```
- huorong https://www.huorong.cn/
```
火绒安全-专注终端安全。
```
- wireshark https://www.wireshark.org/
```
网络安全神器：抓包、协议分析，无所不能。
```
- PuTTY连接登录神器 https://www.chiark.greenend.org.uk/~sgtatham/putty/
```
支持raw,telnet,rlogin,ssh,serial等协议和方式连接。
短小精悍，稳定实用，兼容各种linux发行版本，交换机，路由器等设备调试。
工程师的必备神器，强烈推荐！！！
```
***
***
# 我常去的开源网站——my open source websites
- 自由分享是知识的本质 :+1::+1::+1:
***
## Linux发行版大全
https://distrowatch.com/
- 几百种linux发行版的详细介绍和官网链接，镜像下载等。珍爱生命，拥抱开源~_~
## Linux 内核——The Linux Kernel Archives
https://www.kernel.org/
- 最新的内核信息 Latest Release [5.17.1](https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.17.1.tar.xz)
```
Protocol 	Location
HTTP 	https://www.kernel.org/pub/
GIT 	https://git.kernel.org/
RSYNC 	rsync://rsync.kernel.org/pub/
```
======

|版本|版本号|发布日期|
|:----|:----|:----|
|mainline:| 	5.17 |	    2022-03-20 		
|stable: |	5.17.1 	|    2022-03-28 
|stable: |	5.16.18 |	2022-03-28 
|longterm: 	|5.15.32 |	2022-03-28 
|longterm: |	5.10.109| 	2022-03-28 	
|longterm:| 	5.4.188 |	2022-03-28 
|longterm:| 	4.19.237|	2022-03-28 
|longterm:| 	4.14.274 |	2022-03-28
|longterm:| 	4.9.309 |	2022-03-28 
|linux-next:| next-20220328 |	2022-03-28 

- 快速下载最新版Linux内核
```
wget -c --no-check-certificate https://www.kernel.org/
cat index.html |grep ChangeLog|awk -F '"' '{print $2}'|uniq|xargs wget -c 
cat index.html |grep tar.xz|awk -F '"' '{print $2}'|uniq|xargs wget -c 
```
## 包管理备忘录Package Management Cheatsheet
https://distrowatch.com/dwres.php?resource=package-management
- A package management reference card for Linux distributions and FreeBSD

##  应用软件最新稳定版追踪 Packages Tracked by DistroWatch
[详细链接](./packages.md)
- [Last Update: Monday 28 March 2022 09:05 GMT](https://distrowatch.com/packages.php)  
- 快速下载
```
wget -c --no-check-certificate https://distrowatch.com/packages.php
cat packages.php|grep -E '<td><a href="'|awk -F '"' '{print $2}'|uniq|xargs wget -c --no-check-certificate --tries=5 
```
======常见的应用软件======

|应用软件|版本|说明|
|:----|:----|:----|
|bash| 	5.1.16 |	Bash: an sh-compatible command language interpreter
|sed 	|4.8| 	GNU sed: a stream-oriented non-interactive text editor
|grep 	|3.7| 	GNU Grep: a program to search for strings inside a file
|curl |	7.82.0 |	cURL: a command line tool for transferring files with URL syntax
|wget 	|2.0.0| 	wget: retrieves files from web and FTP sites
|rsync 	|3.2.3| 	rsync: an open source utility that provides fast, incremental file transfer
|VirtualBox 	|6.1.32| 	VirtualBox: a family of x86 virtualisation products for enterprise and home use
|cmake |	3.22.3 |	cmake: a cross-platform, open-source build system
|eclipse |	4.23| 	Eclipse: a universal tool platform and IDE
|git 	|2.35.1| 	Git: an open source version control system
|subversion 	|1.14.1| 	Subversion: a version control system
|perl 	|5.34.1| 	Perl: Larry Wall's Practical Extraction and Reporting Language
|php 	|8.1.4| 	PHP: a server-side HTML embedded scripting language
|Python 	|3.10.4| 	Python: an interpreted, interactive, object-oriented programming language
|ruby 	|3.1.1| 	Ruby: interpreted, dynamically typed, pure object-oriented scripting language
|mariadb 	|10.7.3| 	MariaDB: a robust SQL server, a fork of MySQL
|mysql 	|8.0.28| 	MySQL: an SQL database server
|postgresql 	|14.2| 	PostgreSQL: a relational database management system
|sqlite 	|3.38.2| 	SQLite: an embeddable SQL engine in a C library
|phpMyAdmin 	|5.1.3| 	phpMyAdmin: a tool written in PHP intended to handle the administration of MySQL over the web
|bind| 	9.18.1 |	ISC BIND: an implementation of the Domain Name System (DNS) protocols
|httpd 	|2.4.53| 	httpd: a high-performance HTTP server, Apache 2.x version series
|nginx 	|1.20.2| 	nginx: an HTTP and reverse proxy server
|openssh| 	8.9p1 |	OpenSSH: a client and server for encrypted remote logins and file transfers
|iptables 	|1.8.7| 	iptables: enables the creation of packet alteration and firewall rules
|nmap 	|7.92 |	Nmap: a utility for network exploration or security auditing
|NVIDIA |	510.60.02| 	NVIDIA: a proprietary display driver for Linux, FreeBSD and Solaris
|snort 	|3.1.25.0| 	Snort: a light-weight network intrusion detection program
|tcpdump 	|4.99.1| 	TCPDUMP: a command-line packet sniffer and network debugging tool
|wireshark 	|3.6.3| 	Wireshark: a network protocol analyzer
***
## 数据库排名——DB-Engines Ranking
- Complete ranking  [完整排名 388 systems in ranking, March 2022](https://db-engines.com/en/ranking)
- Relational DBMS [关系数据库](https://db-engines.com/en/ranking/relational+dbms)
-  Key-value stores [键值数据库](https://db-engines.com/en/ranking/key-value+store)
-  Document stores  [文档数据库](https://db-engines.com/en/ranking/document+store)
-  Time Series DBMS  [时间序列数据库](https://db-engines.com/en/ranking/time+series+dbms)
-  Graph DBMS  [图数据库](https://db-engines.com/en/ranking/graph+dbms)
-  Search engines  [搜索引擎](https://db-engines.com/en/ranking/search+engine)
-  Object oriented DBMS  [面向对象库](https://db-engines.com/en/ranking/object+oriented+dbms)
-  RDF stores  [RDF存储](https://db-engines.com/en/ranking/rdf+store)
-  Wide column stores  [宽列存储](https://db-engines.com/en/ranking/wide+column+store)  
-  Multivalue DBMS  [多值数据库](https://db-engines.com/en/ranking/multivalue+dbms)
-  Native XML DBMS  [原生XML](https://db-engines.com/en/ranking/native+xml+dbms)
-  Spatial DBMS  [空间数据库](https://db-engines.com/en/ranking/spatial+dbms)
-  Event Stores  [事件存储](https://db-engines.com/en/ranking/event+store)
-  Content stores  [内容存储库](https://db-engines.com/en/ranking/content+store)
-  Navigational DBMS  [导航数据库](https://db-engines.com/en/ranking/navigational+dbms)
    [详情](db.md)
***
## NoSQL数据库
- [LIST OF NOSQL DATABASE MANAGEMENT SYSTEMS](https://hostingdata.co.uk/nosql-database/) [currently >225]
- Wide Column Store / Column Families
```markdown
  Hadoop / HBase
  Cassandra
  Apache Flink
```  
- Document Store
```markdown
  MongoDB
  CouchDB
```
- Key Value / Tuple Store
- Graph Database Management Systems
- Multimodel Database Management Systems
- Object Database Management Systems »
- Grid & Cloud Database Management Solutions
- XML Database Management Systems
- Multidimensional Database Management Systems
- Multivalue Database Management Systems
- Event Sourcing  
- Time Series / Streaming Database Management Systems
- Other NoSQL related database management systems
- Scientific and Specialized Database Management Systems
- unresolved and uncategorized  
  [详情](nosql.md)
***
## TIOBE 语言排行榜
- [TIOBE Index for March 2022](https://www.tiobe.com/tiobe-index/)
[详情](tiobe.md)
```
编程语言名人堂 
Year	Winner
2021	Python
2020	Python
2019	C
2018	Python
2017	C
2016	Go
2015	Java
2014	JavaScript
2013	Transact-SQL
2012	Objective-C
2011	Objective-C
2010	Python
2009	Go
2008	C
2007	Python
2006	Ruby
2005	Java
2004	PHP
2003	C++
```
***  
## Apache开源项目
### [开源项目列表](https://projects.apache.org/)
- [name 名称排序列表](https://projects.apache.org/projects.html?name)
- [Committee 提交排序列表](https://projects.apache.org/projects.html?committee)  
- [Category 类别排序列表](https://projects.apache.org/projects.html?category)
- [Programming Language 语言排序列表](https://projects.apache.org/projects.html?language)
- [Number of Committers 提交次数排序列表](https://projects.apache.org/projects.html?number)  
### [releases 项目发布信息](https://projects.apache.org/projects.html?category)  
- [详情](apache.md)
***
## 开源镜像网站
[详情](mirrors.md)
### 国内企业开源镜像站点
- 阿里云：http://mirrors.aliyun.com/
- 华为云：https://mirrors.huaweicloud.com/home
- 网易：http://mirrors.163.com/
- 搜狐：http://mirrors.sohu.com/
### 国内教育开源镜像站点
- 清华大学：https://mirrors.tuna.tsinghua.edu.cn/
- 中国科技大学：https://mirrors.ustc.edu.cn/
- 上海交通大学：http://ftp.sjtu.edu.cn/，ftp://ftp.sjtu.edu.cn/
- 西安交通大学：http://mirrors.xjtu.edu.cn/
- 浙江大学：http://mirrors.zju.edu.cn/
- 南京大学：https://mirrors.nju.edu.cn/
***
## 网络服务器调查 Web Server Survey
[详情(1997~2022年)](web-server-survey.md)
- https://news.netcraft.com/archives/category/web-server-survey/
### 2022
- [February 2022 Web Server Survey](https://news.netcraft.com/archives/2022/02/28/february-2022-web-server-survey.html)
- [January 2022 Web Server Survey]( https://news.netcraft.com/archives/2022/01/17/january-2022-web-server-survey.html)

