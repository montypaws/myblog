 # git使用教程

 ## git的安装和配置
 （一） 安装

 git的安装比较简单，此处只做粗略介绍
 1. windows平台

  windows只需要安装对应的安装包即可，使用`cmder`软件的用户可以不用再安装git

 2. Ubuntu平台

 打开终端（`Ctrl+Alt+T`）,输入`sudo apt intall git`,输入用户密码即可完成安装。

（ 二）配置

配置不需区分平台，各平台使用的命令基本相同，配置过程如下：

（1）设定用户名和用户邮箱

- 设定用户名，命令如下：
`git config --global user.name "yourusername"`
- 设定联系邮箱，命令如下：
`git config --global user.email "youremailaddress"`

**说明：** 使用`git config`指令的`--global`参数表示机器上所有的git仓库都使用该用户名和用户邮箱，当不使用该参数是可以对不同的仓库指定不同的用户名和邮箱

（2）生成SSH密钥
  -  检查SSH密钥是否存在，打开终端，输入以下命令：
  `ls -al ~/.ssh`
  公钥文件是以`.pub`后缀结束，  如果提示文件不存在，则说明本机不存在SSH密钥，需要重新生成。

  - 生成SSH密钥，并添加SSH代理。
  打开终端，输入以下命令：`ssh-keygen -t rsa -b 4096 -C "youremailaddress"`根据提示，即可生成你的SSH密钥。
  - 在github账户上添加SSH密钥
  进入github网站，登录之后，点击右上角账户->`Setting`->`SSH and GPG keys`->`New SSH key`,将`~/.ssh/id_rsa.pub`中的内容添加到key中，Title随便填写即可。
  - 检测SSH链接，输入以下命令：`ssh -T git@gith输入ub.com`,然后输入 解锁密钥即可。

（三） 使用
1. 初始化仓库，输入以下命令：`git init`
2. 添加文件：输入以下命令：`git add <filename>`
3. 提交文件：输入以下命令：`git commit <filename> -m message`,`-m`后面跟的是相关的消息，相当于添加一个标签。
