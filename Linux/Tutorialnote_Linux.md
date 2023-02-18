# 常用小知识
## 添加path有什么用
[Reference](https://blog.csdn.net/Forrit/article/details/108817578)
path环境变量是系统环境变量的一种，他用于保存一系列的路径，每个路径之间以分号分隔。

当在命令行窗口运行一个可执行文件（JDK中bin目录下的javac.exe,java.exe,jar.exe,javadoc.exe都是可执行程序）时，操作系统会先在当前目录下查找是否存在该文件，如果不存在会继续在path环境变量中定义的路径下寻找这个文件，如果仍未找到，系统会报错。

# 安装流程

## Ubuntu安装

- 磁盘分区：https://www.jianshu.com/p/fe4e3915495e
  - 这个分区稍微有点问题，直接划分好efi和swap之后，可以把剩下所有的空间全给根目录

- 更改国内镜像源，使用清华的。 
  - [CSDN](https://blog.csdn.net/nienelong3319/article/details/101570858)
  - [bilibili](https://www.bilibili.com/video/BV187411M79A?spm_id_from=333.337.search-card.all.click&vd_source=1d46d083dae85b6b2c01926780b0438b)
- 安装显卡驱动：[Ubuntu20.04、22.04安装nvidia显卡驱动](https://blog.csdn.net/xianrenli38/article/details/125254853?spm=1001.2101.3001.6650.18&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7Edefault-18-125254853-blog-122764717.pc_relevant_multi_platform_whitelistv2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7Edefault-18-125254853-blog-122764717.pc_relevant_multi_platform_whitelistv2&utm_relevant_index=24)
  - 这个显卡驱动安装教程虽然稍微复杂，但很稳定

- CUDA和Cudnn的安装：[bilibili](https://www.bilibili.com/video/BV16Y411M7SC?spm_id_from=333.880.my_history.page.click&vd_source=1d46d083dae85b6b2c01926780b0438b)，同时结合[教程](https://www.jb51.net/article/192158.htm)以及
  - cuda安装通常需要--override
  - cuDNN安装关于文件拷贝，参考：[bilibili](https://www.bilibili.com/video/BV1N54y1r71U?spm_id_from=333.880.my_history.page.click&vd_source=1d46d083dae85b6b2c01926780b0438b)

- 安装spark appstore
  - 安装快速apt fast
- 常见小问题
  - Ubuntu下添加chrome插件：[csdn](https://blog.csdn.net/EliminatedAcmer/article/details/102554228)
  - Ubuntu `Failed to fetch`：[baidu](https://www.baidu.com/s?wd=failed%20to%20fetch&rsv_spt=1&rsv_iqid=0xdd02be140002f205&issp=1&f=8&rsv_bp=1&rsv_idx=2&ie=utf-8&tn=baiduhome_pg&rsv_enter=1&rsv_dl=tb&rsv_sug3=16&rsv_sug1=12&rsv_sug7=100&rsv_sug2=0&rsv_btype=i&inputT=8979&rsv_sug4=9162)


## Anaconda的安装

- 在官网上下载Linux的anaconda
- 直接`sh xxx.sh`执行shell脚本进行安装

  - > do you wish installer to initialize Anaconda3 

    - 选择yes
- 取消anaconda默认使用base环境 [csdn](https://blog.csdn.net/Boys_Wu/article/details/122366971?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1-122366971-blog-111083564.pc_relevant_multi_platform_whitelistv2&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1-122366971-blog-111083564.pc_relevant_multi_platform_whitelistv2&utm_relevant_index=1) 

  - linux下激活或者退出anaconda：
```python
conda activate
conda deactivate

# 查看现有虚拟环境
conda env list

#删除现有虚拟环境
conda remove -n your_env_name --all
conda remove --name your_env_name --all

```
- 深度学习环境配置视频：[bilibili](https://www.bilibili.com/video/BV16a4y157ba?p=6&vd_source=1d46d083dae85b6b2c01926780b0438b)


## 深度学习环境的配置

- 首先更换清华镜像

  ```
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/conda-forge/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/peterjc123/
  conda config --set show_channel_urls yes
  conda config --show-sources
  ```

  然后文件会加在`/home/szwen/.condarc`下面

  其实也可直接通过`sudo gedit ~/.condarc`进行修改

- `conda install pytorch torchvision cudatoolkit=11.3` 

  - 安装与cuda相同版本或者低版本的torch

- `conda install pyg`

  - 安装pyg

- `pip install tensorboard`
	- 安装tensorboard


## 常用程序安装

- [paraview](https://blog.csdn.net/sinat_26809255/article/details/115917301?spm=1001.2101.3001.6650.5&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-5-115917301-blog-83275152.pc_relevant_multi_platform_whitelistv2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-5-115917301-blog-83275152.pc_relevant_multi_platform_whitelistv2&utm_relevant_index=5)
- 

# 基本概念：

- windows下有盘符
- Linux没有盘符的概念，只有一个根目录
- 根目录：`/`
  - `/bin`
  - `/etc`    放置一些配置文件
  - `/home`
  - `/lib`
  - `/usr`
- 不同的目录有不同的作用：
  - `/home/用户名`	存储一些用户相关的文档
  - `/usr` 安装的应用程序


- SSH相关知识
	-   [SSH原理](https://zhuanlan.zhihu.com/p/108161141)
	-   [SSH使用方法](https://zhuanlan.zhihu.com/p/21999778)
	-   [SSH配置](https://zhuanlan.zhihu.com/p/191627275)

- wheel 文件
> whl格式本质上是一个压缩包，里面包含了py文件，以及经过编译的pyd文件。使得可以在不具备编译环境的情况下，选择合适自己的python环境进行安装
通俗来说就是可以用pip install xxx.whl 安装的包。和用conda安装包刚好对立。对于很多包，即可用conda进行安装，也可以pip对其wheel文件进行安装。

# 常用命令

## 文件和目录操作

### 帮助命令

```markdown
ls --help
mkdir --help
cygcheck --help
```

有任何不懂需要查阅的命令都可以在命令后加上 --help

- `man rm`：打开用户手册，进入到一个新的页面

### 自动补全

- Tab进行自动补全
- 有重复的开头按两次tab键可以看到

### 切换各个文件夹

- `clear`：清屏

- `pwd`: 显示当前文件夹
  - 加粗表示文件夹，不见粗的表示文件，加‘ ’表示带有中文字符或者空格的

```c
cd /    切换到根目录（/称之为我们的根目录，在这个根目录下面有home路径。需要注意的是，绝对路径和home不是一个，home只是根目录下面的一个文件夹）
cd ..   切换到上一级目录
cd . 	打开当前目录
cd ./Desktop = cd Desktop
cd /home/tian  通过绝对路径来调控
cd ~	返回到home文件夹；也可用用 cd （什么都不加也可以直接回家）
cd -  	上一个目录和当前目录来回返回切换
```

一般用户是不允许操作root目录的，一般用户只允许在自己的home文件夹下进行操作。

### 列出当前目录下的子文件

- `ls` : 看一下该目录下有哪些文件

- `ls /`:看一下根目录下有哪些文件；`ls /home`: 看一下home文件夹有哪些文件

- `ls -l`: 以列的形式将文件显示出来，同时也会显示文件的所属人，权限等信息。

- `ls -a`: 显示隐藏文件（文件夹或文件，以.开头）
  - 创建隐藏文件只需要在创建的时候在前面加个点
  
- `ls -a -l`

- `ls -l -h`: 以kb来显示文件的大小

- `ls -lha`：一起使用

  

  **通配符**

- `*`：0个或者任意多个字符
  
  - `ls *.txt`
  - `ls 1*`
  - `ls 1*.txt`
  
- `？`：1个问好代表1个字符。直接来一个通配符是不显示的。要和其他字符结合。
  
  - `ls ???.txt`

- `[]`：表示一个字符
  - `ls [1234]23.odt` 中括号表示那个地方只有一个字符并且只能从1234里面取
  - `ls [1234][1234][1234].odt`
  - `ls [1-4].odt` 便是一段连续的字符段

### 文件和文件夹的操作

- `touch test.txt`: 创建一个文本文件
  - 只能创建文件，不能创建目录
  - `touch .test2.txt`: 创建一个隐藏文件
    - `ls -a`: 全部罗列出来
  
- `mkdir abc`: 创建文件夹
  - `mkdir cc/aa`: ==无法多级创建，但是应该可以在绝对路径下面建立文件夹`mkdir /home/abc/test`==
  
- `rm 123.odt`：文件的移除
  - `rm -d aa`: 文件夹的移除
  - `rm -r aa`:文件夹删除的另一种方式（两种方式都要加参数）
  
- `mv`: 移动
  - `mv test.txt aa` 相对于windows里面的剪切，也可以用绝对路径
  - `mv bb aa`: 也可以移动文件夹
  - `mv 125.odt .` 相当于把`125.odt`移动到当前目录下。没有任何变化。若使用`mv 125.odt ./123.odt`==这种相当于改了个名，同理，cp也可以进行这种操作==
  - 
  
- `cp`: 复制
  - `cp 125.txt aa`: 不删除原本的文件夹
  
  - `cp -r aa/bb .`: 使用cp不像mv，如果是文件夹一定要用-r进行指定。这里的意思是将aa/bb移动到当前文件夹下面。
  
    - ```
      cp em2.gro em3.gro
      ./   指的是当前文件夹 
      ../  指的是上一级问价夹
      cp em2.gro /home/tianwd/test/em4.gro
      ```
  
- `rm`:删除
  - `rm test.tet`:只能删除文件file
  - `rm -r test1`: 是将问价夹directory test1删除

- `tar`:压缩解压命令

  - `tar`压缩命令

  ```
  tar -cvf examples.tar files|dir
  #说明：
  -c, --create  create a new archive 创建一个归档文件
  -v, --verbose verbosely list files processed 显示创建归档文件的进程
  -f, --file=ARCHIVE use archive file or device ARCHIVE  后面要立刻接被处理的档案名,比如--file=examples.tar
  
  #举例：
  tar -cvf file.tar file1       #file1文件
  tar -cvf file.tar file1 file2 #file1，file2文件
  tar -cvf file.tar dir         #dir目录
  ```

  - `tar`解压命令

  ```
  tar -xvf examples.tar （解压至当前目录下）
  tar -xvf examples.tar  -C /path (/path 解压至其它路径)
  
  #说明：
  -x, --extract, extract files from an archive 从一个归档文件中提取文件
  
  #举例：
  tar -xvf file.tar
  tar -xvf file.tar -C /temp  #解压到temp目录下
  ```

  

### which查看命令所在位置

每个命令（ls touch mkdir mv cd)执行的时候，都会去执行一个程序，这个程序文件里面保存了当我们执行某个命令的时候需要做哪些事情，来完成这个命令，并输出结果。

which cd为空，cd是shell内置的命令



`/bin`		binary，二进制文件，普通命令

`/sbin` 	system binary,系统二进制文件，需要有系统权

`/usr/bin` 用户安装的应用程序

`/usr/sbin` 超管安装的应用程序

**带s和不带s的区别，带usr和不带usr的区别**

### 文件搜索

- **ls + 通配符：仅限于当前目录下的模糊查找）**

==linux里面是区分大小写的==

- `find 搜索范围 搜索条件`    [find的缺点是其搜索效率还是比较慢的]

  - `find / -name 125`

  - `^C` 可以终止掉命令的进行

  - `find /home -name 125.txt` 【精确搜索】

  - `find /home -name '12*'`   【模糊搜索】

  - `find /home -iname 'abc'` 忽略大小写来进行匹配

  - 按数据大小进行搜索

    - 文件大小理解
      - 1KB=1024B 【因为是按照二进制来进行的，所以是1024而不1000】
      - 1MB=1023KB
      - 1GB=1024MB
      - 1TB=1024GB
    - find /home -size [0.5k] 一个数据块是512字节(1KB=2个数据块)
    - find /home/siki/Desktop/ -size +1 查找大于512B的文件
    - find /home/siki/Desktop/ -size -1  查找小于512B的文件
    - find /home/siki/Desktop/ -size 7
    
  - 通过所属人来进行搜索
    
    - 每个文件都有个所属人
    
    - `ls -l` = `ll`
  
    - `find /home/Desktop -user siki` 文件夹也是有所属人的
    
      
      
  
  - 文件被修改的时间
  
    - 属性被修改的时间
  
    - 内容被修改的时间
  
    - 访问的时间
  
      `find /home/siki/Desktop/ -mmin -5` 在五分钟以内被修改文件内容的文件    
  
  - 按文件类型进行查找
  
    - 文件类型：文件类型；目录；软链接
    - `find /home/siki/Desktop/ -type f`
    -  `find /home/siki/Desktop/ -type d`
    - `find /home/siki/Desktop/ -type l`
  
    - 这些检索的参数可以进行组合【文件搜索的条件运算符】
      - `find /home/siki/Desktop/ -name 'a*' -a -type f`    and约束，说明两个条件都要满足
      - `find /home/siki/Desktop/ -name 'a*' -o -type f`  or约束，说明两个条件只要满足其一就可以了
  
  - 通过文件的id来进行检索
    - linux中，每个文件或则文件夹或者用户都是有个id的。但是一般通过`ls -l`不会显示id。可以用下面的方法`ls -i`来显示id。也可以用这个更常见的组合命令`ls -li`
  
- locate 命令【优点：其效率非常快】

  - `locate 文件/路径名` 参数项没有find那么复杂 `locate --help`
  - locate快的原因是因为它有一个自己的索引库，会很快。缺点是：索引库更新的不及时。
  - 强制更新索引库：`updatedb`，但必须以管理员的权限去运行。一般的用户搜索是不行的。
  - `sudo updatedb` 接着会让你输入密码

### 查看文本文件内容

- Ubuntu上面双击打开，有text editor

- `cat  126.txt`  直接把所有内容答应出来
  - `cat -b 126.txt` 不计算空格
  - `cat -n 126.txt` 计算空格
  
- `more 126.txt` 按分页形式展示。
  - 按空格是下一页
  - 按B是上一页
  - ^C是退出
  - 回车是换行
  
- `vi xxx.txt`

  - ```
    vi abd.txt
    先按i（此时左下角会出现“插入”），进入插入模式可以随便写内容了
    退出的时候分四种情况：保存退出、正常退出、不保存退出以及强制退出
    保存退出：先按“Esc”（左下角插入消失），然后按两遍shift+z
    不保存退出：先按"Esc"，再输入":"（左下脚可输入命令），之后在输入"q!"
    强制退出：先按"Esc"，再输入":"（左下脚可输入命令），之后在输入"!"
    正常退出：先按"Esc"，再输入":"（左下脚可输入命令），之后在输入"q"
    
    vi +2 abc.txt    这样进入的时候指针直接指到第二行
`gedit xxx.txt`
  - 此命令在Ubuntu这种拥有可视化界面的操作系统中非常好用

- `less`



### 文件内容的搜索

- Text editor可以直接^F
- `grep user 126.txt`
- `grep sdf 126.txt`
- `grep -n user 126.txt`  行号显示出来
- `grep -v '#' etc/services ` 反向搜索抓取不包含注释的行
- `grep ^'#' /etc/services`  ^以...开头
- `grep $s /etc/services` $以...结尾
- `grep -i abc 126.txt`       忽略大小写来进行搜索

### 文件内容的修改

- `echo` 回显
  - `echo hello > 126.txt` 会直接把原有内容覆盖掉
  - `echo hello world >> 126.txt`  >>表示的是追加
  - `ls > 126.txt` 把ls输出的结果输出到126.txt里面
  - `grep siki 126.txt >> res.txt`  后面的可以是已存在的文件，也可以是未存在的文件，未存在则会自动生成
- 在linux里面，后缀名没有那么重要了，很多配置文件都没有后缀。都默认为文本文件

### 管道

把一个命令的输出，通过管道的连接，作为另一个命令的输入

- `ls -lh | grep 125.txt` 把|前命令的输出作为|后命令的输入
- 通常某个命令的输出，不方便查看了，我们通过more命令来进行组合
  - `grep -v ^'#' /etc/services | more`
  - `grep -v ^'#' /etc/services | grep update`

### 软连接

相当于windows里面的快捷方式

一般不会在同一个目录里面创建

```
touch aa/abc
ln aa/abc abc_softlink #会创建在当前路径下面
cat abc_softlink
```

## 网络 | 软件

### 文件下载

- `wget`

  - `wget http://cn.wordpress.org/wordpress-4.9.4-zh_CN.tar.gz`  使用wget下载一个文件并保存在当前目录

  - `wget -o` 下载并以不同的文件名保存

    - ```
      wget -O wordpress.tar.gz  http://cn.wordpress.org/wordpress-4.9.4-zh_CN.tar.gz
      
      wordpress.tar.gz
      ```



## 用户和用户权限管理

Linux是个多用户的计算机系统

服务器是多个人管理（运维人员是多个）

安装Linux是有个初始用户 



存在一个特殊用户 **root用户** 【权限最牛逼的用户，拥有所有的权限】 



日常维护工作使用普通用户完成，除非遇到系统管理的工作，使用root来完成！

### 用户添加

**需要root权限**

- 添加用户名和密码

```
useradd user1   #无法执行，权限被拒绝。如果切换成root用户则可能执行
sudo useradd user1 #初始普通用户是可以执行sudo的。会让你输入密码，权限验证

cat /etc/passwd     #所有的用户都会在这个文件里面看到

sudo passwd user1
> Enter new UNIX password:
> Retype new UNIX password:
```

上述方式没有创建家目录

- 创建用户的同时创建家目录

```
sudo useradd -m user3
ls /home
cd /home/user3   #不是空的，有一些基本的桌面模块
```

- 创建用户的同时分配组

```
id
> 会显示gid （组id）
id user1
sudo useradd -g user3 user4
```

- 更改当前用户的密码

```
passwd

^D 和 ^C都有退出的含义。
```

### 如何启用root

- root用户的用户名不需要设定
- 密码需要设定

```
sudo passwd root
```



### 用户组

每个用户都有一个初始组，可以用零个或多个附加组。用户组的作用，是为了方便权限控制。（附加组就是为了给用户附加的权限）。

当创建用户的时候，系统会创建一个更用户名同名的组，每个组也有一个组id



### 用户切换

```
su root
$会变成#
# 当我们从siki切换到root的时候，siki还是处在登录状态。
exit   #退出该用户，或者使用^D。

su - user1  #切换用户并回到/home
```

### 用户的删除

```
userdel user1
userdel -r user2  #不仅把这个用户删除了，还可以删除这个用户的/home
userdel -f user2  #强制删除user2。即使user2处在登录的情况
```

### 用户组的管理

- 用户组的添加也必须是root权限才可

```
groupadd group1
cat /etc/group

groupmod -n group1new group1
cat /etc/group

groupdel group1new
cat /etc/group
```

### Linux文件中的id

Linux所有文件都有id。uid（用户id）gid（组id）

```
id   #查看当前用户id，组id，组

ls -i  #查看文件id

id siki  #查看用户siki的id
```



- 学习一下两个配置文件

```
cat etc/passwd
```

1. 用户名
2. 密码标志
3. UID
4. GID
5. 用户全名
6. 家目录
7. 使用的shell

什么是shell？（我们的命令cd ls...)

shell是用来解析命令的，它接收用户命令，然后调用相应的程序执行。

shell相当于一个翻译，翻译我们的命令，让机器听懂

第一种shell: /bin/bash 		翻译一号

第二种shell：/usr/sbin/nologin	翻译二号

第三种shell：/bin/sh					翻译三号（我们创建用户时候的shell）

​			缺点不支持上下方向键，还有一些其它的区别。如何更换shell？

​			查看所有shell  `cat  /etc/shells`

​			修改shell `chsh`，可以修改某些用户使用的shell



翻译二号通常是那种不可登录的用户所用的编译器



### 用户组的配置文件

`/etc/group`    配置当前系统有哪些用户组

1. 组名
2. 组密码标志
3. GID
4. 组中附加用户



### 影子文件

`/etc/shadow` : 用户的影子文件

`/etc/gshadow`：用户组的影子文件





### 内置命令和外置命令

1. 用户输入命令
2. 提交给shell
   1. 是内置命令
   2. 是外部命令或实用程序 > 在系统中查找该命令的文件并调入到内存中进行使用



如何判断是否是内置命令

```
which cd  #无返回，说明内置在shell里面

which ls
>/bin/ls    #返回了目录，所以ls是个外置命令
```

1. 为什么没有命令文件？
   - 因为`cd`这个命令是放在shell（bash里面的）
2. 什么是内置命令（`cd dirs ls`)
   - 内置命令是在系统启动时就调入内存，时常驻内存的，所以执行效率高。
   - 而外部命令是系统的软件功能，用户需要时才从硬盘中读入内存。
   - 大部分内置命令都是内置在shell中的，也有一些内置命令有自己单独的文件
   - 系统启动时，会把shell中的内置命令，其它不在shell中的内置命令加载到内存

Linux 内置命令和外置命令

https://www.cnblogs.com/pingzhe/p/7077685.html



### 查看和修改用户信息

- `id` 查看id信息

- `whoami`  查看当前用户

- `who`  查看当前登录的用户有哪些



**修改用户组信息：**

```
usermod -g siki user1  # 把user1的初始组修改到siki

usermod -G testu,user1 user1   # 修改附加组（不是追加，是修改）

usermod -s /bin/sh user1    #把user1的shell修改成/bin/sh
```



### 文件权限管理

- 用户组和用户对文件夹和文件的一个管理

**文件权限的表示方式**

1. 文件夹还是二进制

2. 所属人

3. 所属组

4. 其它用户



--- r w x

r：可读

w：可写

x：可执行【文本文件没有可执行】



文件夹的权限

r: 可以列出目录中的内容

w：可以在目录中创建、删除文件

x：可以进入目录（不能查看目录内容）



**文件权限的修改：**

文件所有者和超管都能修改权限

格式一：`chmod [ugoa][+-=][rwx]文件或者目录`

```
chmod u+x 126.txt   #可执行文件都是绿色显示
chmod u-rw,g-r 126.txt
chmod u=rwx 126.txt
```

格式二：`r--rw-rwx` = 467  用数字表示权限r=4 w=2 x=1

```
chmod 651 xxfile
chmod -R 777 xxfile 修改文件包括文件的所有子文件
```



**修改文件拥有者和所有组**

```
chown user1 126.txt
chgrp user1 126.txt
-R 递归修改所有子文件

通常权限不够，我们可以在前面加sudo
sudo chown user1 126.txt
sudo chgrp user1 126.txt
```





**可执行文件**

什么是可执行文件？

windows下的是exe（批处理命令或者批处理脚本），一般用来启动某个应用程序的linux下的shell脚本（或者类型的脚本），一般用来启动某个应用程序或者服务程序。



应用程序：给用户使用的，有操作界面的，有交互的

服务程序：不需要和用户交互的，但保存操作系统的稳定运行





## 服务器

### 查看硬盘

``` c
df -h
```

以G的形式显示硬盘有多大。

```c
du -sh pcpg-1   用来查问价夹的大小
du -sh *   该文件夹中所有文件的大小都给你显示出来
```

### 查看程序是否还在运行

```
top 命令提供了实时的对系统处理器的状态监视
kill 6185  （6185是进程的ID，用来终止指定的进程 terminate a process）
```

```
qme					#查看自己提交的任务，其中r代表run，qw代表排队
qdel 76232			#撤销自己提交的任务
pestat				#查看整个集群的状态
```

### 显示已安装软件包

``` markdown
cygcheck -h 查看该条命令的使用帮助
cygcheck -c -d 显示安装的的packages，但是并不对其进行verify
```



# 常见问题
1. Ubuntu下U盘突然权限只读，无法重命名和复制粘贴文件的问题修复： [CSDN](https://blog.csdn.net/qq_44459787/article/details/115366868?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-0-115366868-blog-125663048.pc_relevant_multi_platform_whitelistv4&spm=1001.2101.3001.4242.1&utm_relevant_index=3)

