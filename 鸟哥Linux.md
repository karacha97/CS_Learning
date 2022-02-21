# Chapter 6 Linux文件权限与配置
## 6.1 用户和用户组
Linux是一个多用户的系统，可以允许多用户访问使用（同时？），因此Linux也规定了不同用户组的权限，具体可以分为：
- owner：文件的所有者
- group：文件同组的人，也可以自由访问本组的文件
- other：其他人，如同定义，非本用户组的人
```
Linux还有一个root用户，权力无限大。
```
这些信息被存在如下三个文件夹内：
- /etc/passwd：一般身份用户和root的信息
- /etc/shadow: 个人密码
- /etc/group: 所有组名都存在这

## 6.2 文件权限
Linux文件和文件夹的权限分三个：read、write、execute
执行`ls-all`命令后

  -rwxrw-r-- 1 root root 42304 Sep4 18:26 install.log
 


# Chapter 7 Linux文件与目录管理

# Chapter 7 Linux磁盘与文件系统管理

# Chapter 10 Vim程序编辑器

# Chapter 11 认识和学习Bash

# Chapter 12 正则表达式与文件格式化处理

# Chapter 13学习shell script

