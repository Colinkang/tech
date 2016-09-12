**df 查看磁盘剩余空间的数量**
**free 显示空闲内存的数量**

**ln 创建硬链接和符号链接**
**mv 移动/重命名文件和目录**

*`ln -s team1 team2` 软链接*
*`ln team1 team2` 硬链接*

* 一个硬链接不能关联它所在文件系统之外的文件。
这是说一个链接不能关联与链接本身不在同一个磁盘分区上的文件。
* 一个硬链接不能关联一个目录。
* *type -说明怎样解释一个命令名*
* *which -显示一个可执行程序的位置*
* *apropos -显示一系列适合的命令*
* *whatis -显示非常简洁的命令说明*
* alias name='string'
* [bash参考手册](http://www.gnu.org/software/bash/manual/bashref.html)
* [Bash FAQ](http://mywiki.wooledge.org/BashFAQ)

* *cat 连接文件*
* *sort 排序文本行*
* *uniq 报告和省略重复行*
* *grep 打印匹配行*
* *wc 打印文件中换行符，字和字节个数*
* *head 输出文件第一部分*
* *tail 输出文件最后一部分*
* *当我们使用 “>” 重定向符来重定向输出结果时,目标文件总 是从开头被重写。*
* *使用 “>>” 操作符,将导致输出结果添加到文件内容之后*
* *| 管道线*
* *tee 程序从标准输入读入数据,并且同时复制数据到标准输出 (允许数据继续随着管道线流动)和一个或多个文件。* *example : `ls /usr/bin | tee ls.txt | grep zip`*
* *字符展开 example:`echo *`*

* *通配符* 
* *算术表达式展开使用这种格式:$((expression))*
* 算术表达式只支持整数(全部是数字,不带小数点)

* `echo Front-{A,B,C}-Back`
* `echo Number_{1..5}`
*   *双引号 如果你把文本放在双引号中,shell 使用的特 殊字符,除了 $,\ (反斜杠),和 ‘(倒引号)之外,则失去它们的特殊含义,被当作普通字符 来看待。*
*   *单引号 如果需要禁止所有的展开,我们使用单引号。*
*   `Ctrl-a` 移动光标到行首
*   `Ctrl-e` 移动光标到行尾
*   `Ctrl-f` 光标后移一个字符
*   `Ctrl-b` 光标前移一个字符
*    `tab`  自动补全
*    `id`-显示用户身份号
*    `chmod`-更改文件模式
*    `umask`-设置默认的文件权限
*    `sudo`-以另一个用户的身份来执行命令
*    `chown`-更改文件所有者
*    `chgrp`-更改文件组所有权
*    `passwd`-更改用户密码
*   用户帐户定义在`/etc/passwd`文件里面,用户组定义在`/etc/group`文件里面。当用户帐户和用 户组创建以后,这些文件随着文件`/etc/shadow`的变动而修改,文件`/etc/passwd`包含了关于用户密码的信息。
*   `ps` -报告当前进程快照
*   `top` -显示任务,动态的查看进程
*   `jobs`-列出活跃的任务
*   `bg`-把一个任务放到后台执行
*   `fg`-把一个任务放到前台执行
*   `kill`-给一个任务放到前台执行
*   `killall`-杀死指定进行的进程
*   `shutdown`-关机或重启系统
*   `printenv`-打印部分或者所有的环境变量
*   `set` 设置shell选项
*   `export` 导出环境变量，让随便执行的程序知道
*   登录shell会读取一个或多个启动文件
   *   `/etc/profile` 应用于所有用户的全局配置脚本
   *   `~/.bash_profile`用户私人启动文件。可以用来扩展或重写全局配置脚本中的设置
   *   `~/.bash_login` 如果文件`~/.bash_profile`没有找到，bash会尝试读取这个脚本
   *   `~/.profile` 如果文件`~/.bash_profile`或文件`~/.bash_login`都没有找到，bash会试图读取这个文件
   *   `source .bashrc` 激活修改 
*  `x` 删除当前字符
*  `dd` 删除当前行
*  `d$`从光标位置开始到当前的行尾
*  `dG`从当前行到文件的末尾
*  `u` 按键三次，来恢复删除部分
*  `p`剪切板中文本粘贴到光标位置之后
*  `yy` 复制当前行

* 软件包管理是指系统中一种安装和维护软件的方法。
* `mount` 挂载一个文件系统
* `umount` 卸载一个文件系统
* `fsck` 检查和修复一个文件系统
* `fdisk` 分区表控制器
* `mkfs` 创建文件系统
* `dd` 把面向块的数据直接写入设备
*  `dd if=/dev/sdb of=/dev/sdc` 
*  `ping` 发送ICMP ECHO_REQUEST软件包到网络主机
* `traceroute` 打印到一台网络主机的路由数据包
* `netstat` 打印网络连接，路由表，接口统计数据，伪装连接和多路广播成员
* `wget` 非交互式网络下载器
* `ssh` OpenSSH 客户端(远程登录程序)
* `scp remote-sys:document.txt`
*  `locate` 通过名字来查找文件
*  `find` 在目录层次结构中搜索文件
*  `xargs` 从标准输入生成和执行命令行
*  `stat` 显示文件或文件系统状态
*  `gzip` 压缩或者展开文件
*  `bzip2` 
*  `tar` 打包工具  
*  文本处理
*  `cat` 连接文件并且打印到标准输出
*  `sort` 给文件行排序
*  `diff` 逐行比较文件
*  `patch` 给原始文件打补丁
*  `sed` 用于筛选和转换文本的流编辑器  

* linux 下载 安装 软件安装 
* [linux基本命令](https://linux.cn/article-6160-1.html)
  * ls/pwd/cd/echo/file/printenv/`Tab`
  * mkdir/rm/mv/touch/less/
  * cut/join/sed/awk/sort/uniq/wc/tr
  * useradd/userdel/usermod/passwd/chsh/id/chown/chmod
  * alias/grep
  * date/cal/bc/man 
* linux 文件层次结构
  * /etc 配置文件
  * /dev 设备文件
  * /bin 二进制命令文件
  * /home 用户的家目录
  * /root 管理员家目录
  * /usr 软件安装目录
  * ~/.bash_profile 是交互式、login 方式进入bash 运行的；~/.bashrc 是交互式 non-login 方式进入bash 运行的；
* 存储设备
   * dd
   * mount 挂载 umount 卸载
* vim编辑器
* shell编程
* 包管理
  
* 文本处理
* 进程管理
  * 查看 关闭进程
  * 关闭 重启系统
* 网络管理
  * 向服务器发送请求
  * 经过的路由节点
  * wget下载
  * scp 复制文件
  * ssh远程登录
* 用户管理
  * 添加 修改 删除用户
  * 添加 修改 删除组
  * 用户的切换
  * 用户的权限设置
* [算法复杂度速查表](https://linux.cn/article-7480-1.html?utm_source=index&utm_medium=moremore)
* ssh登录过程
* 1）远程主机收到用户的登录请求，把自己的公钥发给用户。（2）用户使用这个公钥，将登录密码加密后，发送回来。（3）远程主机用自己的私钥，解密登录密码，如果密码正确，就同意用户登录。
                                                    

