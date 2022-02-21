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
```
-rwxrw-r-- 1 root root 42304 Sep4 18:26 install.log
```
- 其中第一段表示文件权限信息
- 第二段数字表示链接数
- 第三四分别表示文件所有者和文件所属的用户组
- 之后便是文件大小、修改时间等信息
文件权限信息一共由10个符号表示
- 第一个符号表示文件类型
  - d表示文件夹（目录）
  - \-表示普通文件
- 后面3个符号一组，分别表示
  - 文件所有者权限
  - 文件所属用户组权限
  - 其他人权限
- (实际上对应了之前说的owner group others)

`rwx`表示：r-read，w-write，x-execute
### 改变文件属性与权限
- chgrp改变文件所属用户组
`chgrp [-R] groupname filename`
-r表示递归
groupname必须在/etc/group内，否则会报错
- chown改变文件所属用户
`chown [-R] owner filename`
```
用了cp指令后会连同文件的属性和权限一并拷贝，因此有时可能需要变更文件所属
```
- chmod改变文件权限
owner group others三个不同用户组，分别对应着一组权限
修改权限的方式有两种，可以通过字符也可以通过数字
rwx三个字符对应三个不同的值
  - r:4
  - w:2
  - x:1
e.g.`owner=rwx=4+2+1=7`


# Chapter 7 Linux文件与目录管理

# Chapter 7 Linux磁盘与文件系统管理

# Chapter 10 Vim程序编辑器

# Chapter 11 认识和学习Bash

# Chapter 12 正则表达式与文件格式化处理

# Chapter 13学习shell script

