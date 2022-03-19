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
- 最新的内核信息 Latest Release 5.16.15
```
Protocol 	Location
HTTP 	https://www.kernel.org/pub/
GIT 	https://git.kernel.org/
RSYNC 	rsync://rsync.kernel.org/pub/
======
mainline: 	5.17-rc8 	2022-03-13 		
stable: 	5.16.15 	2022-03-16 	
longterm: 	5.15.29 	2022-03-16 	
longterm: 	5.10.106 	2022-03-16 	
longterm: 	5.4.185 	2022-03-16 	
longterm: 	4.19.235 	2022-03-16 	
longterm: 	4.14.272 	2022-03-16 	
longterm: 	4.9.307 	2022-03-16 	
linux-next: 	next-20220318 	2022-03-18
```
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
https://distrowatch.com/packages.php
- Last Update: Saturday 19 March 2022 08:05 GMT
- 快速下载
```
wget -c --no-check-certificate https://distrowatch.com/packages.php
cat packages.php|grep -E '<td><a href="'|awk -F '"' '{print $2}'|uniq|xargs wget -c --no-check-certificate --tries=5 
```
***
## 数据库排名——DB-Engines Ranking
https://db-engines.com/en/ranking
- 388 systems in ranking, March 2022
  [详情](db.md)
***
## NoSQL数据库
https://hostingdata.co.uk/nosql-database/
- LIST OF NOSQL DATABASE MANAGEMENT SYSTEMS [currently >225]
  [详情](nosql.md)
***
## TIOBE 语言排行榜
https://www.tiobe.com/tiobe-index/
- TIOBE Index for March 2022
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
https://projects.apache.org/
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
- February 2022 Web Server Survey https://news.netcraft.com/archives/2022/02/28/february-2022-web-server-survey.html
- January 2022 Web Server Survey https://news.netcraft.com/archives/2022/01/17/january-2022-web-server-survey.html

