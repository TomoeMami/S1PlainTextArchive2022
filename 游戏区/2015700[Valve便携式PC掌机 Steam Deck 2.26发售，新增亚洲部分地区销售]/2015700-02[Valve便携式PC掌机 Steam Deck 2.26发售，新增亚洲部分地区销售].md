

*****

####  distrowatch  
##### 1501#       发表于 2022-8-5 19:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56943304&amp;ptid=2015700" target="_blank">bypass 发表于 2022-8-5 19:53</a>

话说 Deck 开机第一次连 Wi-Fi 可以设置网关和 DNS 吗？</blockquote>
我也想知道，换了路由暂时不能用路由挂

*****

####  半江瑟瑟半江红  
##### 1502#       发表于 2022-8-5 20:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56942856&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-5 19:25</a>
给你们提个醒，开机第一次会自动更新，而且必须翻墙，不然会没网卡住。

  -- 来自 能看大图的 Stage1官方  ...</blockquote>
连主机的加速路由行吗

*****

####  rinkzea  
##### 1503#       发表于 2022-8-5 20:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56942782&amp;ptid=2015700" target="_blank">伊莉伊莉雅 发表于 2022-8-5 19:19</a>

真好吖真好吖我的还在静置</blockquote>
你要不打个电话问问fedex？感觉静置好久了……

*****

####  indtability  
##### 1504#       发表于 2022-8-5 20:44

 本帖最后由 indtability 于 2022-8-7 14:02 编辑 

利用恢复镜像应该可以改dns和网关，应该是 systemd 管理的

最近看了下 deck 的更新系统，感觉应该有可能做到离线更新，不过没条件试，就不折腾了，而且现在 valve 用的还是全量更新，所以才慢，之后或许就改成增量更新了

更新：

想想可能有人用得上，就具体说说吧，但是因为没有实机，所以一半靠经验一半靠虚拟机测试，水平一般，轻喷

在steam deck 上加快更新速度也就这么几个可能，代理，或者提前下载镜像本地离线更新，或者我前文说的增量更新。代理方法太多太乱，没法适合每一个人，本地离线更新很麻烦，更别说第一次开机时没法进入（或者说不建议进入）桌面，这让事情变得更加麻烦，切换到增量更新就比较简单，而且理论上没有坏处，但还是风险自负。

其实 valve 已经写好增量更新的代码，但不知道为啥没有启用，只说是“增量更新”功能不太准确，本质是使用另一个工具并且启用增量更新功能，sd 更新时默认使用 casync，但可以配置使用 desync，这个工具旨在提供兼容 casync 并且更强大的功能，而且是用 go 写的，使用多线程下载在网络上表现更加出色，我昨晚试了一下，不挂代理更新花了三十分钟左右，比之前更新时快很多，应该是比不上代理的，但又不冲突，而且比代理门槛低一些。

步骤：

制作恢复镜像和启动至恢复镜像就不多说了，进入恢复镜像后在开始菜单搜索并打开 konsole，输入以下命令，手打可能会有误，建议联网后打开本贴复制，使用 ctrl + c 在浏览器里复制，使用 ctrl + shift + v 在 konsole 里粘贴
 sudo ~/tools/repair_device.sh chroot sudo mkdir -p /var/lib/overlays/etc/upper/rauc sudo cp /etc/rauc/system.conf /var/lib/overlays/etc/upper/rauc/system.conf sudo nano /var/lib/overlays/etc/upper/rauc/system.conf复制代码
使用 方向键移动光标，删除键删除，删掉 [casync] 下面两行配置的 # 号来启用这两条配置 原来是 # install-args ...... # use-desync=true 删除后变成 install-args ..... use-desync=true复制代码
按 ctrl + o，回车 保存，ctrl + x 退出

然后执行 exit复制代码
这样就启用了 desync 和增量更新，退出恢复镜像，正常重启，更新速度大概能快一些。

上述操作没有碰 steam deck 的只读主分区，没有使用解锁主分区的命令，甚至没有修改任何原有文件，只是开启了一个 valve 已经写好但没有启用的功能，我昨晚在虚拟机里测试了下，能正常启动，理论上说没什么风险，但免责起见还是得说，风险自负。

想关闭的话也很简单，进入恢复镜像 sudo ~/tools/repair_device.sh chroot sudo rm -r /var/lib/overlays/etc/upper/rauc exit复制代码

*****

####  qappip  
##### 1505#       发表于 2022-8-5 22:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56943496&amp;ptid=2015700" target="_blank">半江瑟瑟半江红 发表于 2022-08-05 20:04:35</a>
连主机的加速路由行吗</blockquote>你是说uu那种？没试过。 我是翻墙的才能更新，包括后面更新新版本也是得翻墙。
平常下载浏览什么的就不需要。

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  伊莉伊莉雅  
##### 1506#       发表于 2022-8-6 00:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56943882&amp;ptid=2015700" target="_blank">rinkzea 发表于 2022-8-5 20:27</a>
你要不打个电话问问fedex？感觉静置好久了……</blockquote>
看时间还没到10天，感觉明后天差不多到10天

*****

####  半江瑟瑟半江红  
##### 1507#       发表于 2022-8-6 09:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56945295&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-5 22:04</a>
你是说uu那种？没试过。 我是翻墙的才能更新，包括后面更新新版本也是得翻墙。
平常下载浏览什么的就不需要 ...</blockquote>
哇日 这么麻烦……本来刚托朋友定了港版有点犹豫了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 HUAWEI NOP-AN00, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  qappip  
##### 1508#       发表于 2022-8-6 10:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56948480&amp;ptid=2015700" target="_blank">半江瑟瑟半江红 发表于 2022-08-06 09:54:52</a>
哇日 这么麻烦……本来刚托朋友定了港版有点犹豫了 v2.5.4</blockquote><img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">还好啦，对我来说网络几乎一直翻的状态。uu加速器这个我是真不清楚。

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  半江瑟瑟半江红  
##### 1509#       发表于 2022-8-6 11:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56948621&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-6 10:11</a>
还好啦，对我来说网络几乎一直翻的状态。uu加速器这个我是真不清楚。

  -- 来自 能搜索的 Stage1官 ...</blockquote>
对了，请教下，deck用steam串流的流畅度咋样？它本身还能用蓝牙连接xbox手柄和ps5手柄吗？

—— 来自 HUAWEI NOP-AN00, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  83913536  
##### 1510#       发表于 2022-8-6 12:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56949651&amp;ptid=2015700" target="_blank">半江瑟瑟半江红 发表于 2022-8-6 11:57</a>

对了，请教下，deck用steam串流的流畅度咋样？它本身还能用蓝牙连接xbox手柄和ps5手柄吗？

—— 来自 HU ...</blockquote>
用moonlight串流比较好，steam串流画质不太行

*****

####  qappip  
##### 1511#       发表于 2022-8-6 12:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56949651&amp;ptid=2015700" target="_blank">半江瑟瑟半江红 发表于 2022-08-06 11:57:34</a>
对了，请教下，deck用steam串流的流畅度咋样？它本身还能用蓝牙连接xbox手柄和ps5手柄吗？

—— 来自 HU ...</blockquote>手柄没连接过，串流还不错。 steam dcek内置了串流功能。

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  半江瑟瑟半江红  
##### 1512#       发表于 2022-8-6 14:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56949952&amp;ptid=2015700" target="_blank">83913536 发表于 2022-8-6 12:31</a>
用moonlight串流比较好，steam串流画质不太行</blockquote>
Deck如何安装程序？

—— 来自 HUAWEI NOP-AN00, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  83913536  
##### 1513#       发表于 2022-8-6 15:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56950978&amp;ptid=2015700" target="_blank">半江瑟瑟半江红 发表于 2022-8-6 14:50</a>

Deck如何安装程序？

—— 来自 HUAWEI NOP-AN00, Android 12上的 S1Next-鹅版 v2.5.4</blockquote>
桌面模式在自带的应用商店就可以下载，然后在steam里添加非steam游戏

*****

####  菜菜菜菜  
##### 1514#       发表于 2022-8-7 09:07

<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

开机后连了 wifi 就显示正在安装了，过去十几分钟了是正常的么？

*****

####  rinkzea  
##### 1515#       发表于 2022-8-7 10:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56959174&amp;ptid=2015700" target="_blank">菜菜菜菜 发表于 2022-8-7 09:07</a>
开机后连了 wifi 就显示正在安装了，过去十几分钟了是正常的么？</blockquote>
卡在剩余时间卡在剩余时间1秒或者0秒不动了的话，果断重启吧

*****

####  菜菜菜菜  
##### 1516#       发表于 2022-8-7 10:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56959634&amp;ptid=2015700" target="_blank">rinkzea 发表于 2022-8-7 10:09</a>
卡在剩余时间卡在剩余时间1秒或者0秒不动了的话，果断重启吧</blockquote>
多谢，貌似解决了第一步<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">。

语言选英文就有进度，中文就没有。现在到了 Starting  steam Deck update download，又没进度了<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

—— 来自 deltainno DT2002C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  RaidenII  
##### 1517#       发表于 2022-8-7 11:54

steamos 3.3还是没修WPA2 Enterprise连不上的问题。为啥非要用iwd不用wpa_supplicant呢

*****

####  rinkzea  
##### 1518#       发表于 2022-8-7 13:10

 本帖最后由 rinkzea 于 2022-8-7 13:50 编辑 

有人知道为什么chrome在桌面模式下可以运行，在deck界面下就不能运行吗？

更新：把chrome关闭账号同步，恢复初始状态后可以打开了。估计是哪个扩展出问题了吧……

*****

####  菜菜菜菜  
##### 1519#       发表于 2022-8-7 17:35

终于玩上了，建议语言改成英文，翻q更新。

这个玩意能装汉化补丁吗？类似蝙蝠侠阿卡姆城这些。

*****

####  indtability  
##### 1520#       发表于 2022-8-7 19:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56963957&amp;ptid=2015700" target="_blank">菜菜菜菜 发表于 2022-8-7 17:35</a>
终于玩上了，建议语言改成英文，翻q更新。

这个玩意能装汉化补丁吗？类似蝙蝠侠阿卡姆城这些。 ...</blockquote>
[https://bbs.saraba1st.com/2b/thread-2083792-0-1.html](https://bbs.saraba1st.com/2b/thread-2083792-0-1.html)

这有个关于汉化的帖子，我在里面回了些如何运行汉化补丁的内容，不过没啥人感兴趣的样子，在 win 上汉化后再复制也是一个不算错的选择。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  菜菜菜菜  
##### 1521#       发表于 2022-8-7 21:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56964928&amp;ptid=2015700" target="_blank">indtability 发表于 2022-8-7 19:13</a>
https://bbs.saraba1st.com/2b/thread-2083792-0-1.html

这有个关于汉化的帖子，我在里面回了些如何运行 ...</blockquote>
多谢，我研究下，当务之急是找一台 Windows 电脑<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">

—— 来自 deltainno DT2002C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  恋妖壶  
##### 1522#       发表于 2022-8-7 21:33

<blockquote>indtability 发表于 2022-8-7 19:13
https://bbs.saraba1st.com/2b/thread-2083792-0-1.html

这有个关于汉化的帖子，我在里面回了些如何运行 ...</blockquote>
我的帖子，已经照您的方法成功玩上汉化428，非常感谢

*****

####  83913536  
##### 1523#       发表于 2022-8-7 21:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56963957&amp;ptid=2015700" target="_blank">菜菜菜菜 发表于 2022-8-7 17:35</a>

终于玩上了，建议语言改成英文，翻q更新。

这个玩意能装汉化补丁吗？类似蝙蝠侠阿卡姆城这些。 ...</blockquote>
确实英文比较好，很多功能一开始都是限定英文的，比如最近更新的guide功能，可以在游戏里查看社区的攻略，然而只有英文界面时才能显示出东西

*****

####  yoyodty  
##### 1524#       发表于 2022-8-9 04:04

求推荐一个靠谱的转运啊，最好速度快一点

*****

####  bypass  
##### 1525#       发表于 2022-8-9 08:19

<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer"> 老美这个周末不出仓是真烦人，好不容易周一了，等待库房发货 又不动了。效率真的是低下。

*****

####  亚瑟摩根  
##### 1526#       发表于 2022-8-9 08:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56985812&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-8-9 04:04</a>
求推荐一个靠谱的转运啊，最好速度快一点</blockquote>
其实没有选择，就转中。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  weare17k  
##### 1527#       发表于 2022-8-9 09:20

想问一下，同一个游戏，直接steam启动和硬盘版桌面模式启动，会有优化待遇上的差别吗？

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  weare17k  
##### 1528#       发表于 2022-8-9 09:21

 本帖最后由 weare17k 于 2022-8-9 09:22 编辑 

风怒
[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  lucomefire  
##### 1529#       发表于 2022-8-9 14:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56517797&amp;ptid=2015700" target="_blank">zris 发表于 2022-7-4 11:58</a>

老哥，私你了</blockquote>
老哥，能私我个店铺吗，打算提前充值进去等邮件

*****

####  an0nymous  
##### 1530#       发表于 2022-8-9 15:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56990682&amp;ptid=2015700" target="_blank">lucomefire 发表于 2022-8-9 14:46</a>

老哥，能私我个店铺吗，打算提前充值进去等邮件</blockquote>
不要提前， 最好邮件收到后再充值， 防止帐号被ban， 机器没拿到



*****

####  indtability  
##### 1531#       发表于 2022-8-9 15:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56986864&amp;ptid=2015700" target="_blank">weare17k 发表于 2022-8-9 09:20</a>
想问一下，同一个游戏，直接steam启动和硬盘版桌面模式启动，会有优化待遇上的差别吗？

  -- 来自 能搜索 ...</blockquote>
理论上来说是有的
首先是在游戏模式用的 compositor 是 valve 开发的 gamescope，游戏表现应该比桌面模式用的 xorg/kwin 好一些。
其次如果硬盘版指的是非 steam 游戏的话，是没法下载着色器缓存的，对于 sd 比较孱弱的 cpu 而言，编译着色器可能会带来一定的影响。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  zris  
##### 1532#       发表于 2022-8-9 16:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56990682&amp;ptid=2015700" target="_blank">lucomefire 发表于 2022-8-9 14:46</a>

老哥，能私我个店铺吗，打算提前充值进去等邮件</blockquote>
我私你了，但是你別提前充，因为保不齐淘宝出啥幺蛾子，还是补款邮件快到的时候再充

*****

####  weare17k  
##### 1533#       发表于 2022-8-9 16:56

那如果是把steam库里有的游戏的学习版添加到steam里运行呢？会有性能上的损失吗？

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  stmule  
##### 1534#       发表于 2022-8-9 18:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=56890007&amp;ptid=2015700" target="_blank">亚瑟摩根 发表于 2022-8-1 09:51</a>
不行，deck不是掌机那种逻辑，等于一台pc和另一台pc

要想传东西，无非几种，typec转usb的转接口 ...</blockquote>
哪个type c手机就不需要u盘了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

—— 来自 samsung SM-G9730, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  菜菜菜菜  
##### 1535#       发表于 2022-8-13 07:55

<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">
请问 select 按钮是哪个？双方块图示的，一直没找到<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

—— 来自 deltainno DT2002C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  亚瑟摩根  
##### 1536#       发表于 2022-8-13 11:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57043403&amp;ptid=2015700" target="_blank">菜菜菜菜 发表于 2022-8-13 07:55</a>

请问 select 按钮是哪个？双方块图示的，一直没找到</blockquote>
``````select 不就是左摇杆边上那个吗

*****

####  bypass  
##### 1537#       发表于 2022-8-13 20:45

 本帖最后由 bypass 于 2022-8-13 20:46 编辑 

<img src="https://img.saraba1st.com/forum/202208/13/204424p5yg50t8ztx644x6.png" referrerpolicy="no-referrer">

<strong>image.png</strong> (68.71 KB, 下载次数: 0)

下载附件

2022-8-13 20:44 上传

清关也太快了…话说到北京的国际包裹是不是还得静置十天呢？

*****

####  vertusd  
##### 1538#       发表于 2022-8-14 16:29

 本帖最后由 vertusd 于 2022-8-14 16:34 编辑 

STEAM DECK终于到了，走的转中+EMS （EMS真是慢，花了接近一个月到手），运费一共285rmb(估计没被税，标签上写的预估价值UP TO 200$，也许有点用)。

默认的系统更新是真的慢（约300-500K），后来挂了全局代理，速度才提升到5M。

有没有玩模拟器的老哥推荐下打包好的工具？准备下EMUDECK，镜像估计还得自己一个个去搜刮

*****

####  恋妖壶  
##### 1539#       发表于 2022-8-14 16:34

有个问题一直没解决，就是自从我在desktop界面插过一次USB鼠标以后，SteamOS界面右触控板就没法当鼠标了，只有同时按着steam键时鼠标才会出现

但是我理解是这时候右触控版只是模拟了右摇杆的作用，毕竟steam+右摇杆本身就可以当鼠标

但是我清楚的记得刚拿到机器时候只要摸到右触控板就会出现鼠标，按下就是点击的，这个问题有谁遇到过能解决吗？

*****

####  83913536  
##### 1540#       发表于 2022-8-14 18:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57061271&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-14 16:34</a>

有个问题一直没解决，就是自从我在desktop界面插过一次USB鼠标以后，SteamOS界面右触控板就没法当鼠标了， ...</blockquote>
打开steam到大屏幕模式设置下手柄桌面配置看看？

*****

####  恋妖壶  
##### 1541#       发表于 2022-8-14 18:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57062254&amp;ptid=2015700" target="_blank">83913536 发表于 2022-8-14 18:10</a>

打开steam到大屏幕模式设置下手柄桌面配置看看？</blockquote>
那个好像设置的是desktop mode而不是steam OS mode吧？

我奇怪就奇怪在desktop mode反而是好的，回到steamOS就不按着steam就没法用……

*****

####  revoer  
##### 1542#       发表于 2022-8-14 19:05

淘宝3488全款预定64G去年8.11订单，年轻人的第一次赌博<img src="https://static.saraba1st.com/image/smiley/face2017/220.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202208/14/190458hg95cgooro0ou5bt.png" referrerpolicy="no-referrer">

<strong>Snipaste_2022-08-14_19-01-02.png</strong> (71.98 KB, 下载次数: 0)

下载附件

2022-8-14 19:04 上传

*****

####  恋妖壶  
##### 1543#       发表于 2022-8-14 20:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57062924&amp;ptid=2015700" target="_blank">revoer 发表于 2022-8-14 19:05</a>

淘宝3488全款预定64G去年8.11订单，年轻人的第一次赌博</blockquote>
相当可以啊，就算对方是75折充值卡也没赚多少钱

*****

####  83913536  
##### 1544#       发表于 2022-8-14 21:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57062754&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-14 18:48</a>

那个好像设置的是desktop mode而不是steam OS mode吧？

我奇怪就奇怪在desktop mode反而是好的，回到ste ...</blockquote>
是在gaming mode里？我也是一样

*****

####  恋妖壶  
##### 1545#       发表于 2022-8-14 21:26

<blockquote>83913536 发表于 2022-8-14 21:23
是在gaming mode里？我也是一样</blockquote>
啊？所以是更新完改的？我清楚记得刚拿到手时候不是这样的啊

*****

####  八八八云紫  
##### 1546#       发表于 2022-8-15 10:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57064041&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-14 20:47</a>

相当可以啊，就算对方是75折充值卡也没赚多少钱</blockquote>
这不是怒赚1K多么<img src="https://static.saraba1st.com/image/smiley/face2017/094.png" referrerpolicy="no-referrer">

*****

####  bypass  
##### 1547#       发表于 2022-8-15 10:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57051166&amp;ptid=2015700" target="_blank">bypass 发表于 2022-8-13 20:45</a>

清关也太快了…话说到北京的国际包裹是不是还得静置十天呢？</blockquote>
没错 <img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202208/15/105456rpeezuhhsoqebbcx.png" referrerpolicy="no-referrer">

<strong>image.png</strong> (125.55 KB, 下载次数: 0)

下载附件

2022-8-15 10:54 上传

*****

####  kalavinka  
##### 1548#       发表于 2022-8-15 11:14

好像tb出了一堆3k的全款？之前不都6k了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">有点心动了来自: iPhone客户端

*****

####  医生狼多  
##### 1549#       发表于 2022-8-15 11:17

tb和pdd都有3k2+的全款，说是8月底发，有点心动了<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">

*****

####  u2deack  
##### 1550#       发表于 2022-8-15 11:20

3200的我也有点想买了再买个ssd好像也不是很贵

*****

####  真田丸  
##### 1551#       发表于 2022-8-15 11:26

64g的emmc你们不嫌小吗？还有读取速度也不行吧

*****

####  403page  
##### 1552#       发表于 2022-8-15 11:55

有吃螃蟹的勇士尝试过tb8月发货的吗

*****

####  bypass  
##### 1553#       发表于 2022-8-15 11:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57072198&amp;ptid=2015700" target="_blank">真田丸 发表于 2022-8-15 11:26</a>

64g的emmc你们不嫌小吗？还有读取速度也不行吧</blockquote>
买 64G 的基本都是为了自己加固态的。

*****

####  医生狼多  
##### 1554#       发表于 2022-8-15 13:30

 本帖最后由 医生狼多 于 2022-8-15 13:42 编辑 

草，已经变成3600了，客服说已经截止了
换了另一家3300下单了，祝自己好运(

*****

####  revoer  
##### 1555#       发表于 2022-8-15 13:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57074199&amp;ptid=2015700" target="_blank">医生狼多 发表于 2022-8-15 13:30</a>

草，已经变成3600了，客服说已经截止了

换了另一家3300下单了，祝自己好运(</blockquote>
全款预订，直接确认收货吗<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  医生狼多  
##### 1556#       发表于 2022-8-15 14:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57074434&amp;ptid=2015700" target="_blank">revoer 发表于 2022-8-15 13:47</a>
全款预订，直接确认收货吗</blockquote>
那当然不是，不过明天就发货待揽收了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  403page  
##### 1557#       发表于 2022-8-15 14:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57074618&amp;ptid=2015700" target="_blank">医生狼多 发表于 2022-8-15 14:01</a>
那当然不是，不过明天就发货待揽收了</blockquote>
勇士，等你消息

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  萩原组土狼p  
##### 1558#       发表于 2022-8-15 15:00

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57072198&amp;ptid=2015700" target="_blank">真田丸 发表于 2022-8-15 11:26</a>

64g的emmc你们不嫌小吗？还有读取速度也不行吧</blockquote>
能加固态的，有一个专门的槽可以加固态

*****

####  慕容断月  
##### 1559#       发表于 2022-8-15 15:16

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57075354&amp;ptid=2015700" target="_blank">萩原组土狼p 发表于 2022-8-15 15:00</a>

能加固态的，有一个专门的槽可以加固态</blockquote>
哪来的，必须拆了64/256/512才能换，但凡看过拆机视频都不会觉得可以另加吧……

*****

####  revoer  
##### 1560#       发表于 2022-8-15 15:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57074618&amp;ptid=2015700" target="_blank">医生狼多 发表于 2022-8-15 14:01</a>

那当然不是，不过明天就发货待揽收了</blockquote>
我直接确认了，卖家给了steam账号和绑定邮箱，当一把赌狗<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">



*****

####  医生狼多  
##### 1561#       发表于 2022-8-15 15:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57075607&amp;ptid=2015700" target="_blank">revoer 发表于 2022-8-15 15:17</a>
我直接确认了，卖家给了steam账号和绑定邮箱，当一把赌狗</blockquote>
你这也太赌了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">我是不敢的

*****

####  distrowatch  
##### 1562#       发表于 2022-8-16 09:50

我的应该下周就能下单了，现在是只有转中能用么？我看转中要邀请码只注册过转运四方

*****

####  xrxtzz  
##### 1563#       发表于 2022-8-16 10:02

顺便求问下换2230 ssd大概什么价格，看了一圈tb和狗东，tb 铠侠bg4 512g未通电一般六七百但基本没货，狗东直接一千出头了<img src="https://static.saraba1st.com/image/smiley/face2017/093.png" referrerpolicy="no-referrer">

*****

####  bypass  
##### 1564#       发表于 2022-8-16 10:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57084691&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-8-16 09:50</a>

我的应该下周就能下单了，现在是只有转中能用么？我看转中要邀请码只注册过转运四方 ...</blockquote>
转中的邀请码淘宝或者海鲜市场应该都能买到。

*****

####  distrowatch  
##### 1565#       发表于 2022-8-16 11:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57085426&amp;ptid=2015700" target="_blank">bypass 发表于 2022-8-16 10:38</a>

转中的邀请码淘宝或者海鲜市场应该都能买到。</blockquote>
买到了谢谢，还好能买我以为跟PT站一样

*****

####  广告位  
##### 1566#       发表于 2022-8-17 14:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57084863&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-8-16 10:02</a>

顺便求问下换2230 ssd大概什么价格，看了一圈tb和狗东，tb 铠侠bg4 512g未通电一般六七百但基本没货，狗东 ...</blockquote>
可以看看海力士的BC711，目前几款2230里最快的，512g大概600多。有些通电几小时的拆机件500也有。

*****

####  zris  
##### 1567#       发表于 2022-8-17 14:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57084691&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-8-16 09:50</a>

我的应该下周就能下单了，现在是只有转中能用么？我看转中要邀请码只注册过转运四方 ...</blockquote>
还有个中环转运，但是吧·······慢

转中fedex是最快的了

四方就算了，不寄有电池的

*****

####  zris  
##### 1568#       发表于 2022-8-17 14:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57084863&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-8-16 10:02</a>

顺便求问下换2230 ssd大概什么价格，看了一圈tb和狗东，tb 铠侠bg4 512g未通电一般六七百但基本没货，狗东 ...</blockquote>
2230 可以选三星有一款大概900-1000左右有1t的，极客湾测试时候换的就是这个

还有换ssd的时候，一定要把电池拔下来

*****

####  菜菜菜菜  
##### 1569#       发表于 2022-8-17 15:57

推荐个网站查是否适配 Steam Deck 的，[www.protondb.com](http://www.protondb.com)

还有人在评论区说如果不适配到底是啥问题。

*****

####  FLighT  
##### 1570#       发表于 2022-8-17 16:13

s1有steam deck群么<img src="https://static.saraba1st.com/image/smiley/face2017/125.png" referrerpolicy="no-referrer">

*****

####  失身招领处  
##### 1571#       发表于 2022-8-17 16:16

现在SD能方便的安装win系统吗？

steam出个X86设备，不给装WIN，感觉好蠢。

*****

####  慕容断月  
##### 1572#       发表于 2022-8-17 19:32

 本帖最后由 慕容断月 于 2022-8-17 19:34 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57105317&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-17 16:16</a>

现在SD能方便的安装win系统吗？

steam出个X86设备，不给装WIN，感觉好蠢。</blockquote>
valve给sd最大的优势就是steamos，装win约等于放弃包括系统级fsr集成在内的所有steamos的软件特性，而且现在所有装win的测试无一不表示没有steamos的那些软件特性

给装win是仁义，不给装也没毛病，linux也是系统

*****

####  半江瑟瑟半江红  
##### 1573#       发表于 2022-8-17 19:56

托朋友订的港版，刚开预定那天上午订的，大概能什么时候发货啊

*****

####  nozomitech  
##### 1574#       发表于 2022-8-17 21:34

<img src="https://img.saraba1st.com/forum/202208/17/143243t919j2577got7eeg.png" referrerpolicy="no-referrer">

<strong>9FAB6618-9434-4199-BBB8-8B96D2134C8E.png</strong> (412.63 KB, 下载次数: 0)

下载附件

2022-8-17 21:32 上传

这是怎么回事？<img src="https://static.saraba1st.com/image/smiley/face2017/105.png" referrerpolicy="no-referrer">，管理员搞错了还是V社真的打了鸡血？之前V社说什么现在所有订单都能年底前发货我一直当是放屁。

<img src="https://img.saraba1st.com/forum/202208/17/143251isdfc8cdjtz56fd8.png" referrerpolicy="no-referrer">

<strong>FE4FFC00-DF6B-4943-8FC8-061D88C471D7.png</strong> (389.27 KB, 下载次数: 0)

下载附件

2022-8-17 21:32 上传

就欧版64G一枝独秀。。。

*****

####  nozomitech  
##### 1575#       发表于 2022-8-17 21:34

 本帖最后由 nozomitech 于 2022-8-17 17:58 编辑 

编辑

*****

####  ultraseven  
##### 1576#       发表于 2022-8-17 21:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57109261&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-17 21:34</a>

这是怎么回事？，管理员搞错了还是V社真的打了鸡血？之前V社说什么现在所有订单都能年底前发货我一 ...</blockquote>
是真打了鸡血<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">订单主要集中在前期，越往后肯定时间窗口跳得越快

*****

####  xrxtzz  
##### 1577#       发表于 2022-8-17 22:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57109262&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-17 21:34</a>
顺便提醒一下，64G版本的PCIE总线规格和其他两个版本的不一样，也就是说你换SSD只能解决容量问题。 ...</blockquote>
不是说即使是SD卡加载速度都没有特别明显区别嘛 还是选择性价比之王了<img src="https://static.saraba1st.com/image/smiley/face2017/062.gif" referrerpolicy="no-referrer">

*****

####  慕容断月  
##### 1578#       发表于 2022-8-18 00:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57109262&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-17 21:34</a>

顺便提醒一下，64G版本的PCIE总线规格和其他两个版本的不一样，也就是说你换SSD只能解决容量问题。 ...</blockquote>
真的？但没必要这么做吧？除了屏幕和储存外所有内容完全一样的硬件，生产也方便，没理由专门做一批不一样的吧？

说的应该是硬盘的参数而不是主机硬件的，这块没人拿64G版和256/512版一起测试的话没法下结论

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| nozomitech| + 1|哦对，应该是硬盘参数，你说的有道理。.|

查看全部评分

*****

####  guotao323  
##### 1579#       发表于 2022-8-18 10:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57109261&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-17 21:34</a>

这是怎么回事？，管理员搞错了还是V社真的打了鸡血？之前V社说什么现在所有订单都能年底前发货我一 ...</blockquote>
欧洲好快啊，羡慕坏了

*****

####  硫黄  
##### 1580#       发表于 2022-8-18 10:41

网传的64换ssd会有散热和供电的问题，是fakenews吗

*****

####  亚瑟摩根  
##### 1581#       发表于 2022-8-18 11:00

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57114644&amp;ptid=2015700" target="_blank">硫黄 发表于 2022-8-18 10:41</a>

网传的64换ssd会有散热和供电的问题，是fakenews吗</blockquote>
```没有，之前是传闻有人换不符合规格的SSD出问题了

如果用同样规格的2230，基本没啥事

虽然G胖也让你不换来着就是了

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| 硫黄| + 1|好评加鹅|

查看全部评分

*****

####  zris  
##### 1582#       发表于 2022-8-18 11:01

群号：498166847

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">我建了一个steam dick群，想交流的哥们可以加群

知无不言<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  sunnyjee  
##### 1583#       发表于 2022-8-18 11:33

去年8月18的美版64g版付款了，兴奋的搓搓手

*****

####  失身招领处  
##### 1584#       发表于 2022-8-18 11:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57107080&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-8-17 19:32</a>
valve给sd最大的优势就是steamos，装win约等于放弃包括系统级fsr集成在内的所有steamos的软件特性，而且现 ...</blockquote>
找到了，有win驱动。等等国产掌机再决定

优化再好不能超过6800U也是寂寞<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

*****

####  慕容断月  
##### 1585#       发表于 2022-8-18 14:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57115950&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 11:59</a>

找到了，有win驱动。等等国产掌机再决定

优化再好不能超过6800U也是寂寞 ...</blockquote>
都是rdna2，图形上限就在那，电池技术也没有飞跃，valve家大业大，win掌机能力再大也没法从底层改windows吧，就臭打游戏来说steamos足矣

其余都是用户自己的追求，这就属于自己喜欢咋样就上咋样嘛，反正产品到手都是自己的

*****

####  失身招领处  
##### 1586#       发表于 2022-8-18 15:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57117843&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-8-18 14:18</a>

都是rdna2，图形上限就在那，电池技术也没有飞跃，valve家大业大，win掌机能力再大也没法从底层改windows ...</blockquote>
帧数差了30~50%<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">钱倒是没差多少，不过国产小厂风险太高。

我可以再等等的，明年的7800U提升更大。

*****

####  任天索尼子  
##### 1587#       发表于 2022-8-18 15:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119152&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 15:42</a>
帧数差了30~50%钱倒是没差多少，不过国产小厂风险太高。

我可以再等等的，明年的7800U提升 ...</blockquote>
国内大部分连6800u都只是刚有个消息 连内测啥都没定呢 想玩上7800u估计要后年。

—— 来自 realme RMX2072, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  sky453055730  
##### 1588#       发表于 2022-8-18 15:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119152&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 15:42</a>

帧数差了30~50%钱倒是没差多少，不过国产小厂风险太高。

我可以再等等的，明年的7800U提升 ...</blockquote>
价格差的就不止50%了

*****

####  83913536  
##### 1589#       发表于 2022-8-18 15:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119152&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 15:42</a>

帧数差了30~50%钱倒是没差多少，不过国产小厂风险太高。

我可以再等等的，明年的7800U提升 ...</blockquote>
Win掌机更准确地说是接电玩的掌上电脑，运行逻辑就不一样，你把整机功耗控制在20w内，Deck不比6800u弱

*****

####  失身招领处  
##### 1590#       发表于 2022-8-18 16:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119255&amp;ptid=2015700" target="_blank">sky453055730 发表于 2022-8-18 15:49</a>

价格差的就不止50%了</blockquote>
随便聊聊，两者我暂时都只是保持关注，没打算买。

现在6800U大多数国产都还在产线上，只能看厂商给的价格

512gb的SD，5488港元=4752.2211人民币，加个运费的话，4800~4900差不多了。要是国内淘宝店的话，估计至少还得加200~300吧。

国产6800U的话，有一家声称9月低发完所有预定（鬼知道做不做得到），价格是5500，首发预定还能减600~800，那就姑且算是4900~5500吧

两者都是理想状态的话，差100~600块。差价大概13%？<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">



*****

####  失身招领处  
##### 1591#       发表于 2022-8-18 17:03

 本帖最后由 失身招领处 于 2022-8-18 17:08 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119344&amp;ptid=2015700" target="_blank">83913536 发表于 2022-8-18 15:55</a>

Win掌机更准确地说是接电玩的掌上电脑，运行逻辑就不一样，你把整机功耗控制在20w内，Deck不比6800u弱 ...</blockquote>
我理解的和你差不多，

目前国产这批X86掌机，产品构造上是APU平台的笔记本，去掉了键盘，缩小了屏幕。

SD能玩的游戏，X86掌机（高配）也都能玩，没错吧？

X86掌机还能玩一些SD玩不了的游戏。

对了，正好问一下SD能用修改器这样的其他程序吗？

6800U出来之后，价格和性能上SD都没什么优势，特别是性能上差太多。而且SD还难买不太想买了。所以就等等看

*****

####  sky453055730  
##### 1592#       发表于 2022-8-18 17:09

 本帖最后由 sky453055730 于 2022-8-18 17:11 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57120383&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 16:54</a>

随便聊聊，两者我暂时都只是保持关注，没打算买。

现在6800U大多数国产都还在产线上，只能看厂商给的价 ...</blockquote>
为什么要买512G的，64g的只要3000，你自己换个1t ssd只要500左右成本，何况实测tf卡的运行速度并不输ssd，3000差距6800u无预定价格，差价2000，值得吗？顺便我预定的64g，已经付尾款了，预计到手能比6800u掌机更快，我预定了ayaneo2 geek，预计能4799到手，还预定了ayaneo air plus，1899版本的

*****

####  zris  
##### 1593#       发表于 2022-8-18 17:15

<img src="https://static.saraba1st.com/image/smiley/face2017/034.png" referrerpolicy="no-referrer">说实话，国产要是没有双触控板，没啥意思

有触控板才发现可以玩一些不需要鼠标太复杂微操的游戏

*****

####  慕容断月  
##### 1594#       发表于 2022-8-18 17:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57120540&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 17:03</a>

我理解的和你差不多，

目前国产这批X86掌机，产品构造上是APU平台的笔记本，去掉了键盘，缩小了屏幕。

SD ...</blockquote>
两边都有玩不了的，有些老游戏win10/11不行，一定得靠虚拟机（比如有些gal和老国产），反而linux+wine可以，能不能玩这点两边差不多，而且有些可以靠调教proton之类的解决，主要是单人游戏那两边确实没啥大区别

至于修改器和杯赛家的mod+管理器这些据reddit上的一些帖子说可以用，ce也可以靠wine在linux下正常运行

最后就是，steamdeck，也是笔记本电脑，也是x86掌机

*****

####  慕容断月  
##### 1595#       发表于 2022-8-18 17:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57120714&amp;ptid=2015700" target="_blank">zris 发表于 2022-8-18 17:15</a>

说实话，国产要是没有双触控板，没啥意思

有触控板才发现可以玩一些不需要鼠标太复杂微操的游戏 ...</blockquote>
这玩意儿真就是steam手柄托梦的遗产，那些不支持手柄的游戏靠这俩触摸板跟steam手柄那套留下来的自定义套装愣是把体验拉上去了<img src="https://static.saraba1st.com/image/smiley/face2017/245.png" referrerpolicy="no-referrer">

*****

####  02031f84  
##### 1596#       发表于 2022-8-18 17:55

sd和6800的帧数差距有那么大吗？我看了一些视频6800只能说是略强于sd。我sd可能下个月就到了有点犹豫要不要再订台奥克

*****

####  猫不萌  
##### 1597#       发表于 2022-8-18 18:02

sd的系统能用虚拟机或者装在笔记本上体验吗

*****

####  慕容断月  
##### 1598#       发表于 2022-8-18 18:05

说起来，好像steamdeck的离线模式的体验不咋好来着，有人试过长期离线吗

*****

####  83913536  
##### 1599#       发表于 2022-8-18 18:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57120540&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 17:03</a>

我理解的和你差不多，

目前国产这批X86掌机，产品构造上是APU平台的笔记本，去掉了键盘，缩小了屏幕。

SD ...</blockquote>
其实最大区别我觉得是在床上玩还是随身玩，另一点是玩的游戏支不支持手柄。

*****

####  403page  
##### 1600#       发表于 2022-8-18 18:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57119344&amp;ptid=2015700" target="_blank">83913536 发表于 2022-8-18 15:55</a>

Win掌机更准确地说是接电玩的掌上电脑，运行逻辑就不一样，你把整机功耗控制在20w内，Deck不比6800u弱 ...</blockquote>
B站上有视频评测了，9w以内steam deck优势巨大，11w~15w 6800u掌机优势巨大

15w以上steam deck没有数据，但是9~15w这个区间提升很小

15w以上6800还能提升

*****

####  u2deack  
##### 1601#       发表于 2022-8-18 18:21

是说sd的待机和随时唤醒比win掌机好用很多是吗，之前好像看到说国内那些机器待机唤醒会有很多问题
我觉得掌机最重要的就是这个功能了

*****

####  zdn  
##### 1602#       发表于 2022-8-18 18:22

有没有p社专用机？现在steam玩最多的就是4萌+csl

*****

####  83913536  
##### 1603#       发表于 2022-8-18 19:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57121636&amp;ptid=2015700" target="_blank">403page 发表于 2022-8-18 18:17</a>

B站上有视频评测了，9w以内steam deck优势巨大，11w~15w 6800u掌机优势巨大

15w以上steam deck没有数据， ...</blockquote>
整机功耗，15w CPU功耗的时候，整机功耗可能就25w了

*****

####  403page  
##### 1604#       发表于 2022-8-18 19:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57122492&amp;ptid=2015700" target="_blank">83913536 发表于 2022-8-18 19:22</a>
整机功耗，15w CPU功耗的时候，整机功耗可能就25w了</blockquote>
都调成800p的屏幕没那么耗电的

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  83913536  
##### 1605#       发表于 2022-8-18 19:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57122532&amp;ptid=2015700" target="_blank">403page 发表于 2022-8-18 19:25</a>

都调成800p的屏幕没那么耗电的

—— 来自 S1Fun</blockquote>
我有onexplayer 1s和mini，调成800P真不好看，始终不如原生800P。

15wCPU 25W整机我说的是Deck，Deck的周边功耗算比较高，可以当作抵掉了低分辨率屏幕的优势。

*****

####  古代人皮克  
##### 1606#       发表于 2022-8-18 20:00

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  nozomitech  
##### 1607#       发表于 2022-8-18 20:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57114532&amp;ptid=2015700" target="_blank">guotao323 发表于 2022-8-18 03:35</a>
欧洲好快啊，羡慕坏了</blockquote>
但是贵，64G官价415欧元，美元399刀，而且淘宝上貌似没有卖低价steam欧元的<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  Midnight.Coup  
##### 1608#       发表于 2022-8-18 20:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57121074&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-8-18 17:39</a>

这玩意儿真就是steam手柄托梦的遗产，那些不支持手柄的游戏靠这俩触摸板跟steam手柄那套留下来的自定义套 ...</blockquote>
甚至还能玩红警3<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  mashav  
##### 1609#       发表于 2022-8-19 08:32

21年9月淘宝上预定的，一大早店主发消息22年4月前的都可以补款了<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

*****

####  泰坦失足  
##### 1610#       发表于 2022-8-19 08:34

中午在ebay上看到个600刀的开箱二手，下午再去看时候已经被人买了。然后越想越觉得后悔，就想躺在哪里玩红警2和红警3<img src="https://static.saraba1st.com/image/smiley/face2017/135.png" referrerpolicy="no-referrer">

*****

####  indtability  
##### 1611#       发表于 2022-8-19 08:49

昨晚发货，进度最慢的美版512跑了25天，到了九月，最快的英版64，跑了100天，到了11月，进度最多的欧版64，跑了78天，到了今年2月。

本周一valve宣布又又又又提升出货量，说超级加倍就超级加倍，你g哥哥什么时候骗过你。

下一波高峰应该在2月底媒体解禁，没啥问题的话我甚至觉得10月就能有现货了…emmm…乐观估计。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  83913536  
##### 1612#       发表于 2022-8-19 15:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57122967&amp;ptid=2015700" target="_blank">古代人皮克 发表于 2022-8-18 20:00</a>

触控板打slg绝对是碾压体验了，g胖对这个操作方式押宝思路上是没错的</blockquote>
触摸板还可以当快捷键用，比如绑快速存档 大地图之类的快捷键

*****

####  zris  
##### 1613#       发表于 2022-8-19 16:05

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">STEAM DICK到了之后，一直在玩模拟器····感觉用错地方了

*****

####  i渐行渐远u  
##### 1614#       发表于 2022-8-19 18:33

好像跑了一波大的，我这种今年6月才预定的，感觉可以直接等淘宝平价现货了，看来挂的刀继续屯着吧。

*****

####  yoyodty  
##### 1615#       发表于 2022-8-19 21:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57127933&amp;ptid=2015700" target="_blank">mashav 发表于 2022-8-19 08:32</a>

21年9月淘宝上预定的，一大早店主发消息22年4月前的都可以补款了</blockquote>
有这么快么？我二月定的依旧提示第四季度

*****

####  yulewuchu  
##### 1616#       发表于 2022-8-19 22:00

最近感觉待机再开特别慢呢，按住开关键好几分钟没反应，大伙遇到过这种情况么

*****

####  cscnake  
##### 1617#       发表于 2022-8-19 22:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57134239&amp;ptid=2015700" target="_blank">zris 发表于 2022-8-19 16:05</a>

STEAM DICK到了之后，一直在玩模拟器····感觉用错地方了</blockquote>
我也是，emudeck太方便了！

*****

####  伊莉伊莉雅  
##### 1618#       发表于 2022-8-19 22:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57120383&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-18 16:54</a>
随便聊聊，两者我暂时都只是保持关注，没打算买。

现在6800U大多数国产都还在产线上，只能看厂商给的价 ...</blockquote>
美区用充值卡，512g到手4200

*****

####  nozomitech  
##### 1619#       发表于 2022-8-19 22:14

这价格太羡慕了。欧洲乞丐版都要2900。话说之前都对这玩意死心了，现在感觉按这个进度Q3末都有可能啊。虽然现在官网还是写着Q4发货。我今年4月订的，进度已经到今年2月了。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  zris  
##### 1620#       发表于 2022-8-21 00:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57139489&amp;ptid=2015700" target="_blank">yulewuchu 发表于 2022-8-19 22:00</a>
最近感觉待机再开特别慢呢，按住开关键好几分钟没反应，大伙遇到过这种情况么 ...</blockquote>
待机再开几分钟？这个真没遇到过 也就最多几十秒

—— 来自 [S1Fun](https://s1fun.koalcat.com)



*****

####  rvunholy  
##### 1621#       发表于 2022-8-21 10:56

一下从8%跳到28%了 感觉可以开始囤余额了，求靠谱淘宝店铺推荐

—— 来自 Xiaomi 22041211AC, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  guotao323  
##### 1622#       发表于 2022-8-21 22:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57156710&amp;ptid=2015700" target="_blank">rvunholy 发表于 2022-8-21 10:56</a>

一下从8%跳到28%了 感觉可以开始囤余额了，求靠谱淘宝店铺推荐

—— 来自 Xiaomi 22041211AC, Android 12 ...</blockquote>
淘宝找个存活时间长的老店，充值不改区的都可以吧

*****

####  Gundamslave  
##### 1623#       发表于 2022-8-21 22:36

现在现货啥价了，越看越心痒

*****

####  四级过了  
##### 1624#       发表于 2022-8-21 23:42

<blockquote>Gundamslave 发表于 2022-8-21 22:36
现在现货啥价了，越看越心痒</blockquote>
现货放弃吧，还是天价。可以考虑找淘宝代预定，年内到手有希望

*****

####  yoyodty  
##### 1625#       发表于 2022-8-22 04:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57139752&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-19 22:14</a>

这价格太羡慕了。欧洲乞丐版都要2900。话说之前都对这玩意死心了，现在感觉按这个进度Q3末都有可能啊。虽然 ...</blockquote>
这么快？我就是2月订的，也写的q4

*****

####  nozomitech  
##### 1626#       发表于 2022-8-22 05:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57166098&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-8-21 21:53</a>

这么快？我就是2月订的，也写的q4</blockquote>
我4月18日订的，那个统计网站说还有68天，那不是已经到两月了吗？我看了一下你的发言记录，国内转运的话你买的应该是美版吧？我订的是欧版64G，进度不一样的。

*****

####  zakas  
##### 1627#       发表于 2022-8-22 07:30

<blockquote>02031f84 发表于 2022-8-18 17:55
sd和6800的帧数差距有那么大吗？我看了一些视频6800只能说是略强于sd。我sd可能下个月就到了有点犹豫要不要 ...</blockquote>
最好别信

*****

####  yulewuchu  
##### 1628#       发表于 2022-8-22 08:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57154339&amp;ptid=2015700" target="_blank">zris 发表于 2022-8-21 00:28</a>

待机再开几分钟？这个真没遇到过 也就最多几十秒

—— 来自 S1Fun</blockquote>
那看来可能是我这机器开关键真出问题了，现在待机关机也得按好几下了

*****

####  zris  
##### 1629#       发表于 2022-8-22 09:15

<img src="https://static.saraba1st.com/image/smiley/face2017/026.png" referrerpolicy="no-referrer">今天看贴吧有几个哥们用信用卡和余额支付尾款直接红信，不知道是bill和ship地址对不上还是咋判定的。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  guotao323  
##### 1630#       发表于 2022-8-22 10:27

红信 

看描述是他用PayPal支付，信用卡（真名）信息和订单信息（真名+转运随机字符串）不一致造成的，看起来这样触发了红信规则

余额支付不会触发，前提是充值渠道正规

*****

####  distrowatch  
##### 1631#       发表于 2022-8-22 11:53

我也是怕红信当天才买充值卡，结果100刀涨到了510，有点亏

*****

####  戰國卍丸  
##### 1632#       发表于 2022-8-22 12:20

<img src="https://static.saraba1st.com/image/smiley/face2017/048.png" referrerpolicy="no-referrer">好在俺胆子大，付尾款前几天就搞好了，460 100刀

当然之前可能更便宜，据说有哥们2700 就搞了512g

*****

####  distrowatch  
##### 1633#       发表于 2022-8-22 12:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57169834&amp;ptid=2015700" target="_blank">戰國卍丸 发表于 2022-8-22 12:20</a>

好在俺胆子大，付尾款前几天就搞好了，460 100刀

当然之前可能更便宜，据说有哥们2700 就搞了512g ...</blockquote>
收到邮件忘了带绑令牌的手机，当时充值卡490下班回去就变510了，看着他涨价就感觉很亏

*****

####  戰國卍丸  
##### 1634#       发表于 2022-8-22 12:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57170189&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-8-22 12:49</a>

收到邮件忘了带绑令牌的手机，当时充值卡490下班回去就变510了，看着他涨价就感觉很亏 ...</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">别纠结这个事情了，这玩意大差不差

*****

####  yoyodty  
##### 1635#       发表于 2022-8-22 15:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57166106&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-8-22 05:03</a>

我4月18日订的，那个统计网站说还有68天，那不是已经到两月了吗？我看了一下你的发言记录，国内转运的话 ...</blockquote>
难怪 那我估计最快也要10月了

*****

####  xrxtzz  
##### 1636#       发表于 2022-8-23 10:26

tb预定的在美国发货了，正在发往转运公司，敲碗等，感觉转运回来到手还得两三周？现在国际快递是不是还是要静置。。。

*****

####  rinkzea  
##### 1637#       发表于 2022-8-23 10:43

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57180923&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-8-23 10:26</a>

tb预定的在美国发货了，正在发往转运公司，敲碗等，感觉转运回来到手还得两三周？现在国际快递是不是还是要 ...</blockquote>
看快递公司和收件地区政策，fedex寄上海不用静置，北京静置10天

*****

####  zris  
##### 1638#       发表于 2022-8-23 12:06

最近越来越多铁子估计都要收到了

欢迎S1 SD群交流<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  sunnyjee  
##### 1639#       发表于 2022-8-23 15:33

fedex寄出发往上海了，不知道要等多久清关

*****

####  kimihung  
##### 1640#       发表于 2022-8-25 14:10

stockX上没买过东西。这上面的都是现货嘛？买了直接等运到就可以么？

stockX上价格折算下来比steam亚洲买都要便宜，定了日本区亏大了

*****

####  亚瑟摩根  
##### 1641#       发表于 2022-8-25 14:43

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57212887&amp;ptid=2015700" target="_blank">kimihung 发表于 2022-8-25 14:10</a>

stockX上没买过东西。这上面的都是现货嘛？买了直接等运到就可以么？

stockX上价格折算下来比steam亚洲买 ...</blockquote>
`````是现货

*****

####  Arhjoy  
##### 1642#       发表于 2022-8-25 14:51

2月份订的，原来是q4今天看变成q3了

*****

####  onezer0618  
##### 1643#       发表于 2022-8-26 10:09

4月底订的，q4也变成q3了

<img src="https://img.saraba1st.com/forum/202208/26/100829r646j49jmwjcz90v.png" referrerpolicy="no-referrer">

<strong>image.png</strong> (167.03 KB, 下载次数: 0)

下载附件

2022-8-26 10:08 上传

 进度大跃进了，g胖说产能增加不骗人<img src="https://static.saraba1st.com/image/smiley/face2017/026.png" referrerpolicy="no-referrer">

*****

####  yoyodty  
##### 1644#       发表于 2022-8-26 10:46

已经跳到9月了，求私个充值的店，以前从没冲过

*****

####  snakeyou  
##### 1645#       发表于 2022-8-26 14:41

 本帖最后由 snakeyou 于 2022-8-26 14:42 编辑 

为什么没人是挂刀搞余额的？

*****

####  失身招领处  
##### 1646#       发表于 2022-8-26 15:15

看了视频15瓦，80℃。
这台机器的U最好能跑多少瓦？

*****

####  任天索尼子  
##### 1647#       发表于 2022-8-26 15:19

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57224831&amp;ptid=2015700" target="_blank">失身招领处 发表于 2022-8-26 15:15</a>
看了视频15瓦，80℃。
这台机器的U最好能跑多少瓦？</blockquote>
最多就是15了 上限。

—— 来自 realme RMX2072, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  onezer0618  
##### 1648#       发表于 2022-8-26 16:53

目前有办法打汉化补丁吗

—— 来自 vivo V2157A, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  qappip  
##### 1649#       发表于 2022-8-26 16:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57226033&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-8-26 16:53</a>

目前有办法打汉化补丁吗

—— 来自 vivo V2157A, Android 12上的 S1Next-鹅版 v2.5.2-play ...</blockquote>
可以，但是不是100%可以打，我个人测试大部分都可以。

*****

####  ky怪  
##### 1650#       发表于 2022-8-26 17:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57226091&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-26 16:58</a>
可以，但是不是100%可以打，我个人测试大部分都可以。</blockquote>
请问大概哪些游戏不能打呢，老伊苏轨迹什么的可以打么，之前贴吧好像看到有人说不行，但不知道是不是操作方式的问题



*****

####  nozomitech  
##### 1651#       发表于 2022-8-26 19:06

好耶，变成Q3了<img src="https://static.saraba1st.com/image/smiley/face2017/072.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202208/26/120624z4u1qe1htrk1qn8r.jpg" referrerpolicy="no-referrer">

<strong>BE2CC61C-273B-43E4-A3D5-24335DD8F248.jpg</strong> (529.19 KB, 下载次数: 0)

下载附件

2022-8-26 19:06 上传

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  nozomitech  
##### 1652#       发表于 2022-8-26 19:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57226091&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-26 09:58</a>
可以，但是不是100%可以打，我个人测试大部分都可以。</blockquote>
同问，顺便问一下怎么打的？我看网上说是在电脑上把布丁打好然后直接把游戏整个复制进机器里？

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  qappip  
##### 1653#       发表于 2022-8-26 20:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57226215&amp;ptid=2015700" target="_blank">ky怪 发表于 2022-08-26 17:06:23</a>
请问大概哪些游戏不能打呢，老伊苏轨迹什么的可以打么，之前贴吧好像看到有人说不行，但不知道是不是操作 ...</blockquote>这两游戏我没测试我没有pc版，我说下测试不行的，需要软件，名称你搜下b站教程有，唯一注意你游戏装tf卡，需要在桌面模式打一段代码激活，这样软件才能搜到游戏。 另外一种就是直接复制到根目录。
这两种都有遇到不行情况。

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| ky怪| + 1|好评加鹅|

查看全部评分

*****

####  qappip  
##### 1654#       发表于 2022-8-26 20:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57227196&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-08-26 19:07:44</a>
同问，顺便问一下怎么打的？我看网上说是在电脑上把布丁打好然后直接把游戏整个复制进机器里？

—— 来 ...</blockquote>这种我没试过，我是用软件安装的，另外一种就是直接把复制粘贴到根目录起作用那种。

[  -- 来自 能看大图的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  distrowatch  
##### 1655#       发表于 2022-8-27 09:39

fedex称是1.81kg到转中出库只有1.56kg了，我有点慌啊

*****

####  qappip  
##### 1656#       发表于 2022-8-27 10:28

补充一下 读取tf卡 需要的命令  $ flatpak override --user --filesystem=/run/media/mmcblk0p1 com.github.Matoking.protontricks 

主意需要在桌面模式左下角系统找终端输入 和平常linux系统一样。 

安装汉化补丁 软件名称 protontrlcks  在桌面模式左下角运用商店可搜到并安装。

*****

####  neversink  
##### 1657#       发表于 2022-8-27 11:05

我这边也入转中仓库了，请问商品信息要怎么填写合适

*****

####  frankCC  
##### 1658#       发表于 2022-8-27 11:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57232158&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-8-27 09:39</a>

fedex称是1.81kg到转中出库只有1.56kg了，我有点慌啊</blockquote>
我是1.58kg，应该没问题吧

*****

####  zris  
##### 1659#       发表于 2022-8-27 11:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57232158&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-8-27 09:39</a>

fedex称是1.81kg到转中出库只有1.56kg了，我有点慌啊</blockquote>
fedex 只是很笼统的4磅 大概1.8kg

其实实重基本都在3.5lb 也就是1.6左右kg左右

所以不用担心，我那个到手也是1.6kg

当然了，要是少于1.5kg ，比如一两磅那些，铁没了

红迪就有个哥们是这样
<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  山形石雄  
##### 1660#       发表于 2022-8-27 17:14

之前淘宝订的也通知补款了，说九月底到！

*****

####  时空之旅  
##### 1661#       发表于 2022-8-28 00:54

淘宝有没有可能原价预定到？多几百块钱代购费都可以

*****

####  时空之旅  
##### 1662#       发表于 2022-8-28 01:20

<blockquote>kimihung 发表于 2022-8-25 14:10
stockX上没买过东西。这上面的都是现货嘛？买了直接等运到就可以么？

stockX上价格折算下来比steam亚洲买 ...</blockquote>
哪便宜，看了哈64g都600多美金。。。。

*****

####  kimihung  
##### 1663#       发表于 2022-8-28 13:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57242141&amp;ptid=2015700" target="_blank">时空之旅 发表于 2022-8-28 01:20</a>

哪便宜，看了哈64g都600多美金。。。。</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">第二天我才发现我这里算错了,实际是日版原价订购便宜.

stockX上64GB溢价200刀+

512 GB 溢价180刀左右.最近stockX价格在跌.不知道会不会跌到750刀以下(512)

*****

####  硫黄  
##### 1664#       发表于 2022-8-28 13:22

给g胖交了5刀，希望今年能到

*****

####  萩原组土狼p  
##### 1665#       发表于 2022-8-30 08:56

让朋友帮我再日本定了steamdeck，有在日订的朋友知道大概今年啥时候能下单么

*****

####  Sayuki1025  
##### 1666#       发表于 2022-8-30 11:25

用余额的老哥们 100刀是多钱买的 

现在看淘宝都500多<img src="https://static.saraba1st.com/image/smiley/face2017/056.gif" referrerpolicy="no-referrer">

*****

####  yoyodty  
##### 1667#       发表于 2022-8-30 11:52

预测进度停在了99.92%

这是发到我这儿正好就停了对么<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  indtability  
##### 1668#       发表于 2022-8-30 12:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57271465&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-8-30 11:52</a>
预测进度停在了99.92%

这是发到我这儿正好就停了对么</blockquote>
如果你是us64，就不是刚好停到你，这个进度是按时间来算的，今年二月初的时候三个媒体预览，二月底媒体解禁，这段时间进度会涨得非常非常慢，接下来一周可能都涨不了百分之一，现在没收到邮件的us64显然都是在媒体解禁之后的预定，我记得我是卡在媒体解禁前预定的，已经收到邮件了。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  恋妖壶  
##### 1669#       发表于 2022-8-30 12:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57232517&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-27 10:28</a>

补充一下 读取tf卡 需要的命令  $ flatpak override --user --filesystem=/run/media/mmcblk0p1 com.github ...</blockquote>
麻烦问下protontrlcks怎么用，能不能大概说下，谢谢

*****

####  yoyodty  
##### 1670#       发表于 2022-8-30 13:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57271840&amp;ptid=2015700" target="_blank">indtability 发表于 2022-8-30 12:15</a>

如果你是us64，就不是刚好停到你，这个进度是按时间来算的，今年二月初的时候三个媒体预览，二月底媒体解 ...</blockquote>
256的，2月8号订的，64都发到11号之后了

*****

####  indtability  
##### 1671#       发表于 2022-8-30 13:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57272816&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-8-30 13:24</a>
256的，2月8号订的，64都发到11号之后了</blockquote>
emmm…虽然不是64，但应该还是这么个道理，2月8号应该是媒体预览之后，64是发到媒体解禁那一天，媒体曝光会带来大量订单，按时间确定的进度不能实际反应订单数量，当然队列在那放着肯定拖不了太久就是了。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  onezer0618  
##### 1672#       发表于 2022-8-30 19:32

<img src="https://img.saraba1st.com/forum/202208/30/193216tn6cwkqk8af78h98.png" referrerpolicy="no-referrer">

<strong>image.png</strong> (151.94 KB, 下载次数: 0)

下载附件

2022-8-30 19:32 上传

更新下进度，进度喜人

*****

####  硫黄  
##### 1673#       发表于 2022-8-31 05:48

这么一说，买deck的号需要绑手机令牌吗？

*****

####  qappip  
##### 1674#       发表于 2022-8-31 10:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57272200&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-30 12:36</a>

麻烦问下protontrlcks怎么用，能不能大概说下，谢谢</blockquote>
sd我吃灰好久了，我只能凭记忆大致说下，其实很简单的。  安装号软件后打开它，它会读取已安装的游戏列出一个目录出来，安装在tf卡的游戏必须要之前在终端输入命令才能读取出来。 选择你要打汉化补丁的游戏，会弹出一个框然后选择你放的汉化补丁（建议一般放游戏根目录）。

 选好后会有一段较为漫长等待时间，（根据游戏汉化补丁不等）然后会弹出熟悉安装补丁界面（比如3dm 天邈  游侠等 这个就不用教了吧和 win系统安装汉化补丁一样。 正常安装后就ok了。

*****

####  an0nymous  
##### 1675#       发表于 2022-8-31 11:09

终于到手了

*****

####  恋妖壶  
##### 1676#       发表于 2022-8-31 11:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57283512&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-31 10:22</a>

sd我吃灰好久了，我只能凭记忆大致说下，其实很简单的。  安装号软件后打开它，它会读取已安装的游戏列出 ...</blockquote>
感谢，这就去试试二之国！

*****

####  恋妖壶  
##### 1677#       发表于 2022-8-31 12:41

 本帖最后由 恋妖壶 于 2022-8-31 12:48 编辑 

风怒风怒

*****

####  恋妖壶  
##### 1678#       发表于 2022-8-31 12:42

 本帖最后由 恋妖壶 于 2022-8-31 12:49 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57283512&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-31 10:22</a>

sd我吃灰好久了，我只能凭记忆大致说下，其实很简单的。  安装号软件后打开它，它会读取已安装的游戏列出 ...</blockquote>
很奇怪，能认出我装的游戏（在本体），但是选任何一个游戏都弹窗报错

<img src="https://img.saraba1st.com/forum/202208/31/124916aq2k10k0wk0kfvkw.jpg" referrerpolicy="no-referrer">

<strong>ao3bS.jpg</strong> (431.71 KB, 下载次数: 0)

下载附件

2022-8-31 12:49 上传

*****

####  qappip  
##### 1679#       发表于 2022-8-31 14:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57285439&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-31 12:42</a>

很奇怪，能认出我装的游戏（在本体），但是选任何一个游戏都弹窗报错</blockquote>
你安装哪个游戏汉化补丁就得选哪个游戏，不是随便选的。 另外这方法不是100%成功看游戏。

*****

####  恋妖壶  
##### 1680#       发表于 2022-8-31 14:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57286359&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-31 14:09</a>

你安装哪个游戏汉化补丁就得选哪个游戏，不是随便选的。 另外这方法不是100%成功看游戏。 ...</blockquote>
不是，我现在是选完游戏后就报错，还没到选补丁的步骤，我装的10个游戏都报这个错



*****

####  qappip  
##### 1681#       发表于 2022-8-31 14:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57285439&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-31 12:42</a>

很奇怪，能认出我装的游戏（在本体），但是选任何一个游戏都弹窗报错</blockquote>
是不是要更新？ 提示是版本有问题

*****

####  恋妖壶  
##### 1682#       发表于 2022-8-31 14:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57286374&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-31 14:10</a>

是不是要更新？ 提示是版本有问题</blockquote>
对，所以我也不知道为啥……我刚才在软件中心下载安装的，update栏也没有更新提示

*****

####  qappip  
##### 1683#       发表于 2022-8-31 14:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57286571&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-31 14:29</a>

对，所以我也不知道为啥……我刚才在软件中心下载安装的，update栏也没有更新提示 ...</blockquote>
这个我也不懂，我之前都是这样安装的没出问题。

*****

####  恋妖壶  
##### 1684#       发表于 2022-8-31 15:08

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57286712&amp;ptid=2015700" target="_blank">qappip 发表于 2022-8-31 14:42</a>

这个我也不懂，我之前都是这样安装的没出问题。</blockquote>
重启也没用，放狗也没搜到同款问题，放弃了……

*****

####  亚瑟摩根  
##### 1685#       发表于 2022-9-2 12:18

 本帖最后由 亚瑟摩根 于 2022-9-2 12:34 编辑 

<img src="https://static.saraba1st.com/image/smiley/face2017/143.png" referrerpolicy="no-referrer">太惨了，现在有哥们用余额也红了

还特么有挂刀红············<img src="https://static.saraba1st.com/image/smiley/face2017/125.png" referrerpolicy="no-referrer">

*****

####  cc-2  
##### 1686#       发表于 2022-9-2 15:02

去年8月淘宝预定的512G

之前几个月问都是说还没，到年底了等等

上周忍不住，要求把我的剩余期限截图给我看，然后就说可以补款了

现在支付了尾款等待中，说是九月底能到手

抱着怀疑的态度等待ING

*****

####  yoyodty  
##### 1687#       发表于 2022-9-2 16:13

我的昨天终于补款了，老天保佑不要红，特意选了贵一点的充值

*****

####  亚瑟摩根  
##### 1688#       发表于 2022-9-2 16:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57315709&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-9-2 16:13</a>

我的昨天终于补款了，老天保佑不要红，特意选了贵一点的充值</blockquote>
红都是前后几个小时的事情，如果你没有频繁换区啥的，都没事

*****

####  亚瑟摩根  
##### 1689#       发表于 2022-9-2 16:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57314807&amp;ptid=2015700" target="_blank">cc-2 发表于 2022-9-2 15:02</a>

去年8月淘宝预定的512G

之前几个月问都是说还没，到年底了等等</blockquote>
·········你这被卖家坑了吧

现在512g都卖到2023年2月的订单了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  cc-2  
##### 1690#       发表于 2022-9-2 16:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57315750&amp;ptid=2015700" target="_blank">亚瑟摩根 发表于 2022-9-2 16:17</a>

·········你这被卖家坑了吧

现在512g都卖到2023年2月的订单了</blockquote>
我也是觉得，前面懒得问，估计原来属于我的那架早都高价卖了吧<img src="https://static.saraba1st.com/image/smiley/face2017/212.png" referrerpolicy="no-referrer">

不过能原价到手的话也就算了，实在到不了退款投诉，说实话兴趣也减退了很多，不如直接上6800的WIN掌机了

*****

####  亚瑟摩根  
##### 1691#       发表于 2022-9-2 16:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57315823&amp;ptid=2015700" target="_blank">cc-2 发表于 2022-9-2 16:22</a>

我也是觉得，前面懒得问，估计原来属于我的那架早都高价卖了吧

不过能原价到手的话也就算了，实 ...</blockquote>
说实话我玩了不到一个月，就吃灰了，始终都是个玩具，新鲜感没几天。

但是吧国产就不建议买了

*****

####  yoyodty  
##### 1692#       发表于 2022-9-2 18:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57315732&amp;ptid=2015700" target="_blank">亚瑟摩根 发表于 2022-9-2 16:15</a>

红都是前后几个小时的事情，如果你没有频繁换区啥的，都没事</blockquote>
为了买机器特意注册的号，没转过区的

*****

####  83913536  
##### 1693#       发表于 2022-9-2 18:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57315970&amp;ptid=2015700" target="_blank">亚瑟摩根 发表于 2022-9-2 16:33</a>

说实话我玩了不到一个月，就吃灰了，始终都是个玩具，新鲜感没几天。

但是吧国产就不建议买了 ...</blockquote>
还是看平常习惯，我的已经取代游戏本、台式机、VR还有Switch成为日常娱乐最常用的设备了

*****

####  indtability  
##### 1694#       发表于 2022-9-2 18:49

谁对这种交易比较熟啊，或者有类似情况的吗？我预定时因为听说paypal不用填账单地址就直接用paypal支付的定金，后知后觉才反应过来，应该不是不用填，而是paypal自动填了，现在充好余额，准备用余额付尾款，然而 steam 说要填账单地址，现在我担心这个账单地址会不会和下定金的 paypal 对账啊？因为我看到贴吧有用贝宝付尾款然而账单地址对不上导致被冻结的。不过他是同一个交易的账单地址和支付的信息对不上，我担心的是尾款的账单地址会不会和定金的冲突。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  superkin185  
##### 1695#       发表于 2022-9-3 09:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57317803&amp;ptid=2015700" target="_blank">indtability 发表于 2022-9-2 18:49</a>
谁对这种交易比较熟啊，或者有类似情况的吗？我预定时因为听说paypal不用填账单地址就直接用paypal支付的定 ...</blockquote>
我定金就是用的PayPal付的，尾款用的余额，账单地址填的转运地址，过了快一周了，目前一切正常

*****

####  indtability  
##### 1696#       发表于 2022-9-3 23:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57323019&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-9-3 09:40</a>
我定金就是用的PayPal付的，尾款用的余额，账单地址填的转运地址，过了快一周了，目前一切正常 ...</blockquote>
感谢，琢磨了一会觉得也没别的选择就填了转运地址，没事就好。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  onezer0618  
##### 1697#       发表于 2022-9-4 17:34

请问转中，买的512g版本，如果选货到即发，要预充值多少钱

—— 来自 vivo V2157A, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  zris  
##### 1698#       发表于 2022-9-5 14:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57337170&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-9-4 17:34</a>

请问转中，买的512g版本，如果选货到即发，要预充值多少钱

—— 来自 vivo V2157A, Android 12上的 S1Next ...</blockquote>
300左右

*****

####  zris  
##### 1699#       发表于 2022-9-5 14:36

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">最近转中有一批入库称重却缺斤少两了

各位用转中的要多留意一下

*****

####  kimihung  
##### 1700#       发表于 2022-9-5 14:40

一批是多少啊，好可怕

—— 来自 HUAWEI PCT-AL10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  zris  
##### 1701#       发表于 2022-9-5 14:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57349448&amp;ptid=2015700" target="_blank">kimihung 发表于 2022-9-5 14:40</a>

一批是多少啊，好可怕

—— 来自 HUAWEI PCT-AL10, Android 10上的 S1Next-鹅版 v2.5.4</blockquote>
贴吧第一页起码有两个帖子了

有个哥们说好几个都这样了，太惨了

*****

####  sunnyjee  
##### 1702#       发表于 2022-9-5 15:18

中环转运 28号出库 到今天还在排航班<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">

*****

####  yoyodty  
##### 1703#       发表于 2022-9-5 15:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57349992&amp;ptid=2015700" target="_blank">sunnyjee 发表于 2022-9-5 15:18</a>

中环转运 28号出库 到今天还在排航班</blockquote>
明天美国劳动节，估计上飞机有点难

*****

####  onezer0618  
##### 1704#       发表于 2022-9-5 15:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57349646&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-5 14:56</a>

贴吧第一页起码有两个帖子了

有个哥们说好几个都这样了，太惨了</blockquote>
看到了，吓人。

*****

####  zris  
##### 1705#       发表于 2022-9-5 15:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57350060&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-9-5 15:22</a>

看到了，吓人。</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/032.png" referrerpolicy="no-referrer">这还算好的了

去红迪看看，老美偷SD更是触目惊心

*****

####  硫黄  
##### 1706#       发表于 2022-9-5 15:46

0元购这么近那么远

*****

####  kimihung  
##### 1707#       发表于 2022-9-7 08:50

蓝鸟上 steam deck 新建了4个账号来做本地化的宣传和服务。

应该是亚洲区要开始发货了吧

*****

####  xrxtzz  
##### 1708#       发表于 2022-9-8 09:43

转中排了一个星期航班了<img src="https://static.saraba1st.com/image/smiley/face2017/217.gif" referrerpolicy="no-referrer">

*****

####  xrxtzz  
##### 1709#       发表于 2022-9-8 09:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57386666&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-9-8 09:43</a>
转中排了一个星期航班了</blockquote>
说错了 中环<img src="https://static.saraba1st.com/image/smiley/face2017/217.gif" referrerpolicy="no-referrer">

*****

####  kalavinka  
##### 1710#       发表于 2022-9-8 15:32

<img src="https://img.saraba1st.com/forum/202209/08/153155qdhyrer5hhar4oah.png" referrerpolicy="no-referrer">

<strong>WX20220908-153118@2x.png</strong> (133.73 KB, 下载次数: 0)

下载附件

2022-9-8 15:31 上传

这也太哈人了吧<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">



*****

####  精钢魔像  
##### 1711#       发表于 2022-9-8 15:57

离谱，快递丢件一点责任都没？

*****

####  qappip  
##### 1712#       发表于 2022-9-8 20:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57286571&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-8-31 14:29</a>
对，所以我也不知道为啥……我刚才在软件中心下载安装的，update栏也没有更新提示 ...</blockquote>
<img src="https://p.sda1.dev/7/b09a46694ca0bdf4f7dbe7b0f6e7492b/CMP_20220908201713000.jpg" referrerpolicy="no-referrer">
我刚刚拿出吃灰好久了sd用软件安装这个游戏汉化补丁一切正常，安装软件有更新。

—— 来自 HUAWEI ELS-AN00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  恋妖壶  
##### 1713#       发表于 2022-9-9 00:21

<blockquote>qappip 发表于 2022-9-8 20:18
我刚刚拿出吃灰好久了sd用软件安装这个游戏汉化补丁一切正常，安装软件有更新。

—— 来自 HUAWEI ELS- ...</blockquote>
我擦，我更新了一下虽然报了个错但是进去了……这个我要选application？

<img src="https://img.saraba1st.com/forum/202209/09/002131xoc0m8eb050054u1.png" referrerpolicy="no-referrer">

<strong>7A5B2CF2-370D-42FB-9D3D-451A4005C248.png</strong> (666.61 KB, 下载次数: 0)

下载附件

2022-9-9 00:21 上传

<img src="https://img.saraba1st.com/forum/202209/09/002131r2e6yi6754xdd22d.png" referrerpolicy="no-referrer">

<strong>3543A48C-955F-44F8-964F-26638D3E4B3E.png</strong> (482.76 KB, 下载次数: 0)

下载附件

2022-9-9 00:21 上传

*****

####  恋妖壶  
##### 1714#       发表于 2022-9-9 00:40

我深度怀疑咱俩用的软件是不是有啥不一样，我所有选项都看了一遍也没看见哪里可以让我选择汉化补丁的

*****

####  qappip  
##### 1715#       发表于 2022-9-9 10:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57402202&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-09-09 00:40:16</a>
我深度怀疑咱俩用的软件是不是有啥不一样，我所有选项都看了一遍也没看见哪里可以让我选择汉化补丁的 ...</blockquote>你有在汉化补丁右键么？菜单栏第一个应该是就是软件名称 接着应该就是游戏列表才对，选择游戏列表后会出现汉化补丁界面。

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  sunnyjee  
##### 1716#       发表于 2022-9-9 12:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57386666&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-9-8 09:43</a>
 转中排了一个星期航班了</blockquote>
我中环28号出库7号才送往机场然后又再等飞机了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  yoyodty  
##### 1717#       发表于 2022-9-9 13:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57408184&amp;ptid=2015700" target="_blank">sunnyjee 发表于 2022-9-9 12:06</a>

我中环28号出库7号才送往机场然后又再等飞机了</blockquote>
貌似现在航班非常紧张。希望走fedex线能快点

*****

####  yoyodty  
##### 1718#       发表于 2022-9-9 13:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57408184&amp;ptid=2015700" target="_blank">sunnyjee 发表于 2022-9-9 12:06</a>

我中环28号出库7号才送往机场然后又再等飞机了</blockquote>
貌似现在航班非常紧张。希望走fedex线能快点

*****

####  Piano-Forest  
##### 1719#         楼主| 发表于 2022-9-10 10:30

Steam Deck 维修中心现已上线：
[https://store.steampowered.com/n ... 3398545888823804940](https://store.steampowered.com/news/app/1675200/view/3398545888823804940)

今天，我们很高兴为大家带来一个好消息：全新的 Steam Deck 维修中心现已开张。 如果您的 Steam Deck 遇到问题，需要发来进行维修或更换，该设备现在将送至我们的维修中心之一。 设备送达后，我们的团队将对设备进行诊断并维修（如有必要），然后将修好的设备发回给您。

若问题在保修范围内，可免费维修。 如果发来的 Steam Deck 不在保修范围内，我们的团队将联系您并提供付费维修（如果可以维修）。 这种保修范围外的维修完全由您自选，您也可以要求我们退回设备。

当然了，如果您更愿意亲自修理，[iFixit](https://steamcommunity.com/linkfilter/?url=https://www.ifixit.com/Device/Steam_Deck#) 上有修理套件、替换件和指南。

这些维修中心可解决以下几种情况：

如果您的设备出现间歇性的按键输入问题（极少见，但有时候还是会发生），请联系[客服](https://help.steampowered.com/zh-cn/wizard/HelpWithSteamDeck)，他们会帮忙将您的 Steam Deck 发送至我们的维修中心之一。 我们的团队将进行诊断、更换按键、测试并校准设备，然后将修好的设备发回给您，且一切免费——因为这在保修范围内。

如果您的爱犬把摇杆啃坏，这就不在保修范围内了。 以前，您只能自己动手维修，但现在您将能联系客服，在他们的指引下将 Steam Deck 发送至我们的维修中心之一。 我们的团队将进行检查，然后提供付费的摇杆更换和校准。 在您的保修过期后，也可使用此流程。

我们很高兴能提供这项服务——虽然多数人永远用不到，但对于有需要的各位，我们想要确保你们的需求得到满足。

*****

####  Piano-Forest  
##### 1720#         楼主| 发表于 2022-9-10 10:34

吉祥物：Pal

Introducing a special version of our Steam Pal mascot, created for our launch in Japan, South Korea, **, and Hong Kong!

「Steam Deck（スチームデック）」のマスコットキャラクターに就任した「Pal（パル）」です！

「Pal」は、英语で【友达】や【仲间】という意味があります。#TGS2022 では、「Pal（パル）」を使用したノベルティーもご用意していますので、お楽しみに！
<img src="https://p.sda1.dev/7/1da2c399f78acb6938d6f81ca1f9f540/20220910_103432.jpg" referrerpolicy="no-referrer">

*****

####  霖岚_  
##### 1721#       发表于 2022-9-10 10:51

刚瞄了一眼自己年初淘宝预定的SD订单，现在才总算成功下单了，问了下客服估计是年底之前能到手

提前问下这个搞PS2往前的主机模拟器方便不？有无具体的教程可以参考的

*****

####  慕容断月  
##### 1722#       发表于 2022-9-10 12:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57422178&amp;ptid=2015700" target="_blank">霖岚_ 发表于 2022-9-10 10:51</a>
刚瞄了一眼自己年初淘宝预定的SD订单，现在才总算成功下单了，问了下客服估计是年底之前能到手

提前问下这 ...</blockquote>
模拟器爬楼就行，emudeck解君愁

*****

####  nozomitech  
##### 1723#       发表于 2022-9-12 21:09

借楼问一下，如果某游戏我已经用PC端下好游戏打好汉化补丁了，（都是正版的）可不可以直接把PC端的游戏文件直接复制进SD里然后识别成steam游戏？

主要有些游戏年代久远，忘记当初是怎么打汉化补丁的了。还有我游戏库里好多游戏显示🚫图标，可以强行玩吗？

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  windhawind2  
##### 1724#       发表于 2022-9-13 07:27

问一下万能的潭友们 想买一台steamdeck 主要可能是想玩玩以撒血污这种小型独立游戏以及一些avg 然后想折腾下模拟器之类 问题是：
1.现在sd的类型只有容量有区别吗？
2.淘宝上买靠谱不？大概会溢价多少？（如果不多就直接淘宝买了

[  -- 来自 能手机投票的 Stage1官方 iOS客户端](https://itunes.apple.com/fi/app/saraba1st/id1221237470?mt=8)

*****

####  Suzutsuki.Mk.II  
##### 1725#       发表于 2022-9-13 10:12

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57455920&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-9-12 21:09</a>

借楼问一下，如果某游戏我已经用PC端下好游戏打好汉化补丁了，（都是正版的）可不可以直接把PC端的游戏文件 ...</blockquote>
都可以直接带过去，但是考虑到linux的情况，最好是sd上装完了然后再复制过去

显示不支持的都可以碰运气，多人游戏和网游需要看看protondb上的情况

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| nozomitech| + 1|好评加鹅|

查看全部评分

*****

####  Suzutsuki.Mk.II  
##### 1726#       发表于 2022-9-13 10:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57459721&amp;ptid=2015700" target="_blank">windhawind2 发表于 2022-9-13 07:27</a>

问一下万能的潭友们 想买一台steamdeck 主要可能是想玩玩以撒血污这种小型独立游戏以及一些avg 然后想折腾 ...</blockquote>
除了512的基本只有容量区别

512是防眩光屏幕和更好的包，再加上一些独有的虚拟物品

淘宝溢价必然严重，这可是大热产品，咋可能不严重

*****

####  zris  
##### 1727#       发表于 2022-9-13 11:14

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57422178&amp;ptid=2015700" target="_blank">霖岚_ 发表于 2022-9-10 10:51</a>
刚瞄了一眼自己年初淘宝预定的SD订单，现在才总算成功下单了，问了下客服估计是年底之前能到手

提前问下这 ...</blockquote>
下载个emudeck 基本有模拟器的都给你整合了，然后自己捣鼓一个bios包，rom放专门的文件夹里即可，方便的一批<img src="https://static.saraba1st.com/image/smiley/face2017/035.png" referrerpolicy="no-referrer">

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  zdn  
##### 1728#       发表于 2022-9-13 12:01

国服wow跟ff14能玩吗？

*****

####  onezer0618  
##### 1729#       发表于 2022-9-13 12:21

完了，提示补款了，我余额还有300刀没充

*****

####  distrowatch  
##### 1730#       发表于 2022-9-13 17:23

转中默认线路今天国内发货了，运气不错没被税

*****

####  83913536  
##### 1731#       发表于 2022-9-13 20:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57461458&amp;ptid=2015700" target="_blank">Suzutsuki.Mk.II 发表于 2022-9-13 10:12</a>

都可以直接带过去，但是考虑到linux的情况，最好是sd上装完了然后再复制过去

显示不支持的都可以碰运气 ...</blockquote>
protondb有个插件可以显示适配性在游戏详情左上角

*****

####  hashire.owl  
##### 1732#       发表于 2022-9-14 12:21

就没人传个sd玩儿非steam gal的视频看看吗

*****

####  山形石雄  
##### 1733#       发表于 2022-9-14 13:25

被中环卡吐了，10天还没上飞机

*****

####  distrowatch  
##### 1734#       发表于 2022-9-14 21:48

大屏幕模式下可以用触摸板来移动么？我这边只能按下左触摸板才能动

*****

####  02031f84  
##### 1735#       发表于 2022-9-15 07:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57480092&amp;ptid=2015700" target="_blank">hashire.owl 发表于 2022-9-14 12:21</a>

就没人传个sd玩儿非steam gal的视频看看吗</blockquote>
我试了几个小黄油倒是都能玩

*****

####  xrxtzz  
##### 1736#       发表于 2022-9-16 14:13

无语，tb预定的还在中环排航班，自己官网预定的已经能下单了<img src="https://static.saraba1st.com/image/smiley/face2017/217.gif" referrerpolicy="no-referrer">问问哪个转运公司靠谱，转中好像有偷机器的？

*****

####  Suzutsuki.Mk.II  
##### 1737#       发表于 2022-9-16 15:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57487726&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-9-14 21:48</a>

大屏幕模式下可以用触摸板来移动么？我这边只能按下左触摸板才能动</blockquote>
设置里改，一般默认左边模拟十字键，所以要按下

*****

####  亚瑟摩根  
##### 1738#       发表于 2022-9-16 16:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57509921&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-9-16 14:13</a>

无语，tb预定的还在中环排航班，自己官网预定的已经能下单了问问哪个转运公司靠谱，转中好像有偷机 ...</blockquote>
就转中了，别的没得选

*****

####  mashav  
##### 1739#       发表于 2022-9-16 16:24

9.03 到现在还在排...

*****

####  sunnyjee  
##### 1740#       发表于 2022-9-16 16:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57509921&amp;ptid=2015700" target="_blank">xrxtzz 发表于 2022-9-16 14:13</a>

无语，tb预定的还在中环排航班，自己官网预定的已经能下单了问问哪个转运公司靠谱，转中好像有偷机 ...</blockquote>
转中fedex线最快，我的中环今天开始清关，还不知道要多久



*****

####  distrowatch  
##### 1741#       发表于 2022-9-16 21:02

 本帖最后由 distrowatch 于 2022-9-16 21:11 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57511098&amp;ptid=2015700" target="_blank">Suzutsuki.Mk.II 发表于 2022-9-16 15:50</a>

设置里改，一般默认左边模拟十字键，所以要按下</blockquote>
设置里好像没有看到有触摸板映射，beta channel的问题么？

游戏里可以设置不过主页没法设置，主页用摇杆太慢了触屏DECK又太宽不方便

*****

####  远野四季  
##### 1742#       发表于 2022-9-16 22:37

能玩DOTA吗

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  萩原组土狼p  
##### 1743#       发表于 2022-9-16 22:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57516477&amp;ptid=2015700" target="_blank">远野四季 发表于 2022-9-16 22:37</a>

能玩DOTA吗

—— 来自 S1Fun</blockquote>
能玩，但是操作很麻烦

*****

####  distrowatch  
##### 1744#       发表于 2022-9-17 23:59

我的512也翻了，开始出现气泡

*****

####  02031f84  
##### 1745#       发表于 2022-9-18 00:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57531475&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-9-17 23:59</a>

我的512也翻了，开始出现气泡</blockquote>
这么惨啊，这是只有512才会出现的吗？

*****

####  distrowatch  
##### 1746#       发表于 2022-9-18 00:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57531612&amp;ptid=2015700" target="_blank">02031f84 发表于 2022-9-18 00:05</a>

这么惨啊，这是只有512才会出现的吗？</blockquote>
对，512有个防眩光层

*****

####  时空之旅  
##### 1747#       发表于 2022-9-18 00:18

我比较好奇，我电脑有一个pc版樱花大战1-4的中文版合集，需要开虚拟机运行，那么sd能不能玩到？

*****

####  时空之旅  
##### 1748#       发表于 2022-9-18 00:21

还有个比较好奇和有这种需求的问题，能运行dosbox模拟器嘛？不知道方便不

*****

####  慕容断月  
##### 1749#       发表于 2022-9-18 05:08

 本帖最后由 慕容断月 于 2022-9-18 05:09 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57531862&amp;ptid=2015700" target="_blank">时空之旅 发表于 2022-9-18 00:18</a>
我比较好奇，我电脑有一个pc版樱花大战1-4的中文版合集，需要开虚拟机运行，那么sd能不能玩到？ ...</blockquote>
你不如查查deck怎么装虚拟机

另外dosbox这种开源跨平台的玩意，一定少不了Linux的份的，steam很多老游戏都自带dosbox的

*****

####  Suzutsuki.Mk.II  
##### 1750#       发表于 2022-9-19 11:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57514940&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-9-16 21:02</a>

设置里好像没有看到有触摸板映射，beta channel的问题么？

游戏里可以设置不过主页没法设置，主页用摇杆太 ...</blockquote>
可能steam那边改了新UI的模式，旧UI用steam手柄是可以改的

*****

####  冰原狼  
##### 1751#       发表于 2022-9-19 13:42

本地600刀收了个512的，问问有什么需要设置的吗？
我记得之前看过说最好锁40帧，还有风扇什么的，这些是在开发者模式里吗

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  bighand3714  
##### 1752#       发表于 2022-9-19 22:46

疯了，手边没有拓展坞，鼠标必须按着难摁的steam键才能动，虚拟键盘查了半天也不知道怎么调出来，连怎么改网关都找不到位置，太难受了<img src="https://static.saraba1st.com/image/smiley/face2017/139.png" referrerpolicy="no-referrer">今天早晨期待了一天了都

*****

####  02031f84  
##### 1753#       发表于 2022-9-19 23:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57558826&amp;ptid=2015700" target="_blank">bighand3714 发表于 2022-9-19 22:46</a>

疯了，手边没有拓展坞，鼠标必须按着难摁的steam键才能动，虚拟键盘查了半天也不知道怎么调出来，连怎么改 ...</blockquote>
虚拟键盘steam键+X，但要是你挂梯子的话可能会遇到steam要重新登陆但又没有虚拟键盘输入密码的囧况

*****

####  bighand3714  
##### 1754#       发表于 2022-9-20 07:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57559846&amp;ptid=2015700" target="_blank">02031f84 发表于 2022-9-19 23:45</a>
虚拟键盘steam键+X，但要是你挂梯子的话可能会遇到steam要重新登陆但又没有虚拟键盘输入密码的囧况 ...</blockquote>
我试过了，摁不出来<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  onezer0618  
##### 1755#       发表于 2022-9-20 10:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57531697&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-9-18 00:09</a>

对，512有个防眩光层</blockquote>
这个目前翻车的多吗<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">还有如果出现气泡，只能返厂解决吗

*****

####  distrowatch  
##### 1756#       发表于 2022-9-20 12:51

 本帖最后由 distrowatch 于 2022-9-20 12:54 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57563509&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-9-20 10:32</a>

这个目前翻车的多吗还有如果出现气泡，只能返厂解决吗</blockquote>

<img src="https://img.saraba1st.com/forum/202209/20/125442mfwea22saffvszez.png" referrerpolicy="no-referrer">

<strong>QQ截图20220920125418.png</strong> (98.51 KB, 下载次数: 0)

下载附件

2022-9-20 12:54 上传

可以擦掉也可能再复现

<img alt="" border="0" class="vm" src="https://static.saraba1st.com/image/filetype/unknown.gif" referrerpolicy="no-referrer">

b5wktvi94rj91.webp

2022-9-20 12:49 上传
点击文件名下载附件

28.57 KB, 下载次数: 1

*****

####  yweili99  
##### 1757#       发表于 2022-9-20 13:21

现在进度是不是加快了很多？我7月份的订单都排到了

*****

####  Motoko-9  
##### 1758#       发表于 2022-9-20 13:36

2022年我又沉迷半条命传送门了，deck把我拉回了高中毕业那个暑假<img src="https://static.saraba1st.com/image/smiley/face2017/026.png" referrerpolicy="no-referrer">

*****

####  qappip  
##### 1759#       发表于 2022-9-20 15:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57558826&amp;ptid=2015700" target="_blank">bighand3714 发表于 2022-9-19 22:46</a>

疯了，手边没有拓展坞，鼠标必须按着难摁的steam键才能动，虚拟键盘查了半天也不知道怎么调出来，连怎么改 ...</blockquote>
单纯就是steam没启动而已，桌面模式必须steam启动才能激活全部功能，不然就是坡脚的功能。

*****

####  zqr211  
##### 1760#       发表于 2022-9-20 15:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57565694&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-20 13:21</a>
现在进度是不是加快了很多？我7月份的订单都排到了</blockquote>
应该是把 6800u的win掌机已经在路上 在不大量放货是不行的

*****

####  yweili99  
##### 1761#       发表于 2022-9-20 15:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57567433&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-20 15:36</a>

应该是把 6800u的win掌机已经在路上 在不大量放货是不行的</blockquote>
这个会比steam deck强很多吗？

如果这样，考虑取消deck了

*****

####  nnnnick22  
##### 1762#       发表于 2022-9-20 16:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57567459&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-20 15:37</a>
这个会比steam deck强很多吗？

如果这样，考虑取消deck了</blockquote>
要比纸面数据那基本没悬念啊 

*****

####  02031f84  
##### 1763#       发表于 2022-9-20 16:15

<blockquote>yweili99 发表于 2022-9-20 15:37
这个会比steam deck强很多吗？

如果这样，考虑取消deck了</blockquote>
其实除了64g的性价比和steamos，我想象不出sd比6800u强的地方

*****

####  任天索尼子  
##### 1764#       发表于 2022-9-20 16:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57567459&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-20 15:37</a>
这个会比steam deck强很多吗？

如果这样，考虑取消deck了</blockquote>
15w左右sd大多数游戏更有优势 同等特效能高几帧  过了15w基本上sd就落后很多了 sd下限高 6800u上限高 

—— 来自 realme RMX2072, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  zqr211  
##### 1765#       发表于 2022-9-20 19:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57567459&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-20 15:37</a>
这个会比steam deck强很多吗？

如果这样，考虑取消deck了</blockquote>
不是一个级别的 吊打

 低功耗那几帧差距可比不过高功耗几十帧差距

不过首发价格也不会低 说穿了 无论ns和steam掌机 到最后核心竞争力就是优化和价格

*****

####  indtability  
##### 1766#       发表于 2022-9-20 20:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57567459&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-20 15:37</a>
这个会比steam deck强很多吗？

如果这样，考虑取消deck了</blockquote>
极限性能当然强，但功能和体验大概率不如 sd，如果以 极限性能为唯一追求的话当然选 6800u，有别的考量可以多看看测评再决定。

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  恋妖壶  
##### 1767#       发表于 2022-9-20 20:16

win掌机休眠都做不好不要想真当碎片时间的掌机玩了，就新鲜一下

*****

####  zqr211  
##### 1768#       发表于 2022-9-21 10:14

 本帖最后由 zqr211 于 2022-9-21 10:16 编辑 

说真的 虽然我觉得win掌机挺一般
但 steam deck这大小 真有人能在碎片时间随时掏出来玩？<img src="https://p.sda1.dev/7/57222e2b2ecf2a44f17a0fa816a5a547/CMP_20220921101350650.jpg" referrerpolicy="no-referrer">

*****

####  Paradox7  
##### 1769#       发表于 2022-9-21 10:30

我定的这两天出货但是感觉用不上了，有没有人要收的

*****

####  5353  
##### 1770#       发表于 2022-9-21 10:32

<blockquote>Paradox7 发表于 2022-9-21 10:30
我定的这两天出货但是感觉用不上了，有没有人要收的</blockquote>
我推荐你先买回来后试一下，在挂闲鱼上卖，队也不能白排。



*****

####  fancykid  
##### 1771#       发表于 2022-9-21 11:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57577005&amp;ptid=2015700" target="_blank">Paradox7 发表于 2022-9-21 10:30</a>

我定的这两天出货但是感觉用不上了，有没有人要收的</blockquote>
64g的吗

*****

####  bypass  
##### 1772#       发表于 2022-9-21 11:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57576771&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-21 10:14</a>

说真的 虽然我觉得win掌机挺一般

但 steam deck这大小 真有人能在碎片时间随时掏出来玩？ ...</blockquote>
能，我就放到我的书桌上，我工作用的 MBP，底下有台 PC，晚上加班，等编译结果的时候就会拿来玩一小会。

*****

####  Paradox7  
##### 1773#       发表于 2022-9-21 11:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57577485&amp;ptid=2015700" target="_blank">fancykid 发表于 2022-9-21 11:04</a>

64g的吗</blockquote>
64g的

*****

####  Paradox7  
##### 1774#       发表于 2022-9-21 11:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57577040&amp;ptid=2015700" target="_blank">5353 发表于 2022-9-21 10:32</a>

我推荐你先买回来后试一下，在挂闲鱼上卖，队也不能白排。</blockquote>
我也打算挂咸鱼算了

*****

####  fancykid  
##### 1775#       发表于 2022-9-21 11:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57577807&amp;ptid=2015700" target="_blank">Paradox7 发表于 2022-9-21 11:26</a>

64g的</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/135.png" referrerpolicy="no-referrer">好价吗，想要

*****

####  revoer  
##### 1776#       发表于 2022-9-21 15:25

中环清关7天了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  山形石雄  
##### 1777#       发表于 2022-9-21 15:26

中环光订舱就订了16天，现在还没上飞机<img src="https://static.saraba1st.com/image/smiley/face2017/013.png" referrerpolicy="no-referrer">

*****

####  guotao323  
##### 1778#       发表于 2022-9-21 15:38

1. 0902付了款。

2. 0921上午中环终于发往机场了。

3. SN530已经进入付款队列，SteamOS已下好，NS淘汰下来的吃灰TF卡（200G）已准备好。

4. 接下来又是一个月漫长的等待。

*****

####  nozomitech  
##### 1779#       发表于 2022-9-21 17:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57576771&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-21 03:14</a>
说真的 虽然我觉得win掌机挺一般
但 steam deck这大小 真有人能在碎片时间随时掏出来玩？ ...</blockquote>
看到这图我的第一反应是原来XSS居然这么小。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  恋妖壶  
##### 1780#       发表于 2022-9-21 17:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57576771&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-21 10:14</a>

说真的 虽然我觉得win掌机挺一般

但 steam deck这大小 真有人能在碎片时间随时掏出来玩？ ...</blockquote>
你可能没见过实物，我意思是XSS和SD实物都没见过

XSS本来就是出了名的小，你不要把XSS默认当主机普通大小了

SD是大但是没有那么大

*****

####  sunnyjee  
##### 1781#       发表于 2022-9-21 18:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57581229&amp;ptid=2015700" target="_blank">revoer 发表于 2022-9-21 15:25</a>
 中环清关7天了</blockquote>
我清了6天了<img src="https://static.saraba1st.com/image/smiley/face2017/020.png" referrerpolicy="no-referrer">只希望国庆放假前能出来

*****

####  onezer0618  
##### 1782#       发表于 2022-9-21 19:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57565396&amp;ptid=2015700" target="_blank">distrowatch 发表于 2022-9-20 12:51</a>

可以擦掉也可能再复现</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/254.png" referrerpolicy="no-referrer">

然后是不是说这个防眩光屏的通透度不如普通的屏幕？

*****

####  yoyodty  
##### 1783#       发表于 2022-9-21 19:41

今天中午收到了，有群么

*****

####  onezer0618  
##### 1784#       发表于 2022-9-21 19:41

自己换2230固态有什么要求吗，pcie3.0即可？还有读写有要求吗，查了下sn530现在1t就500多

*****

####  distrowatch  
##### 1785#       发表于 2022-9-21 20:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57585178&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-9-21 19:39</a>

我退了512g的换64g的预定了，回来自己换ssd

然后是不是说这个防眩光屏的通透度不如普通的 ...</blockquote>
那不清楚毕竟没看过普通的DECK，我个人感觉还可以

*****

####  yoyodty  
##### 1786#       发表于 2022-9-21 21:44

今天终于收到了 感觉还是没正儿八经的游戏机那么无脑 需要一些电脑知识

*****

####  泰坦失足  
##### 1787#       发表于 2022-9-22 03:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57585178&amp;ptid=2015700" target="_blank">onezer0618 发表于 2022-9-21 19:39</a>

我退了512g的换64g的预定了，回来自己换ssd

然后是不是说这个防眩光屏的通透度不如普通的 ...</blockquote>
我看的评测的确说了这个现象。我是预定了64g在想要不要换512g的。还看到reddit一个帖子说64g+sd卡会因为着色器缓存用光空间而卡。

*****

####  Gundamslave  
##### 1788#       发表于 2022-9-22 03:51

看楼里想出的不少啊，那等两个月应该有好价现货了

*****

####  笨笨塞  
##### 1789#       发表于 2022-9-22 07:34

现在淘宝的价格好夸张。

*****

####  yweili99  
##### 1790#       发表于 2022-9-22 08:47

目前性价比最高的是64G版+自己换ssd吧? 那个炫光屏没意义吧？

*****

####  yoyodty  
##### 1791#       发表于 2022-9-22 10:10

有的游戏切中文以后没办法显示中文，是缺了字库么

*****

####  泰坦失足  
##### 1792#       发表于 2022-9-22 12:56

 本帖最后由 泰坦失足 于 2022-9-22 12:59 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57591003&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-22 08:47</a>

目前性价比最高的是64G版+自己换ssd吧? 那个炫光屏没意义吧？</blockquote>
512比256贵250刀，就算用充值卡也要200刀。同款接口512g SSD要50刀左右，就看那个屏幕技术值不值150刀了。我是觉得这技术要是真特管用的话，苹果和安卓手机干嘛不用呢. 只有苹果Pro display加1000刀才能加配纳米玻璃，不知道Steam deck 512和这个有没有啥关系就是了。“如果你所处的环境光线复杂难控，可选择 Nano-texture 纳米纹理玻璃的创新亚光屏幕。普通亚光显示屏会在屏幕表面添加涂层来分散光线，但这些涂层会降低对比度，并产生多余的虚影和光点。而 Pro Display XDR 的 Nano-texture 纳米纹理，则是以纳米级技术蚀刻在玻璃之中。这样打造的屏幕既能呈现精美画质，保持出色对比度，同时又能分散光线，尽可能减少眩光。”

*****

####  yweili99  
##### 1793#       发表于 2022-9-22 13:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57595036&amp;ptid=2015700" target="_blank">泰坦失足 发表于 2022-9-22 12:56</a>

512比256贵250刀，就算用充值卡也要200刀。同款接口512g SSD要50刀左右，就看那个屏幕技术值不值150刀了。 ...</blockquote>
看起来无需为了屏膜多花钱。

我看网上有人换了1TB的SSD也能用，这个配置比原厂的还要高啊

*****

####  83913536  
##### 1794#       发表于 2022-9-22 13:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57591003&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-22 08:47</a>

目前性价比最高的是64G版+自己换ssd吧? 那个炫光屏没意义吧？</blockquote>
没意义，反正会贴膜

*****

####  83913536  
##### 1795#       发表于 2022-9-22 13:35

大部分游戏显示器都不是镜面屏吧，习惯了就好

*****

####  亚瑟摩根  
##### 1796#       发表于 2022-9-22 13:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57585207&amp;ptid=2015700" target="_blank">yoyodty 发表于 2022-9-21 19:41</a>

今天中午收到了，有群么</blockquote>
498166847 S1群

*****

####  恋妖壶  
##### 1797#       发表于 2022-9-22 14:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57591003&amp;ptid=2015700" target="_blank">yweili99 发表于 2022-9-22 08:47</a>

目前性价比最高的是64G版+自己换ssd吧? 那个炫光屏没意义吧？</blockquote>
眩光屏没意义，但是个人资料有意义啊，没个人资料我都不会买

朋友：“你这个个人资料页挺好看的，哪来的”

我：“买Deck给的”

朋友：“我**不会为了这盘醋包的饺子吧”

我：“你是不是没搞懂谁是醋谁是饺子？一个两年后变成电子垃圾扔了都占地方的东西也配和限定个人资料比啊”<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">

*****

####  Motoko-9  
##### 1798#       发表于 2022-9-22 14:47

玩了一个星期，堆料堆成这逼样结果做成了躺着玩半小时手腕子就会酸的""便携""设备
把你那俩触摸板抠了怕是手感都能好上一大截，索尼惦记这玩意到现在ps5手柄还是五小时续航，你也惦记干啥。。

不过原生游戏支持全自定义是真的舒服，没想到这么多年后我又沉迷半条命2了

*****

####  夜_乌鸦  
##### 1799#       发表于 2022-9-23 05:16

拿到手了，有啥推荐在steam deck上体验的游戏么

*****

####  慕容断月  
##### 1800#       发表于 2022-9-23 07:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57596251&amp;ptid=2015700" target="_blank">Motoko-9 发表于 2022-9-22 14:47</a>
玩了一个星期，堆料堆成这逼样结果做成了躺着玩半小时手腕子就会酸的""便携""设备
把你那俩触摸板抠了怕是 ...</blockquote>
没触摸板玩不了不支持手柄的游戏，你觉得它多余那是你没懂这个的存在意义，这玩意比索尼那样子货实用百倍



*****

####  nnnnick22  
##### 1801#       发表于 2022-9-23 09:05

妈的在日本定的512遥遥无期

*****

####  kimihung  
##### 1802#       发表于 2022-9-23 09:20

网站模拟了一下，就算今天定，下周也能发货了。

后面steam deck应该就要变成随卖随发的模式了吧

*****

####  Motoko-9  
##### 1803#       发表于 2022-9-23 13:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57605762&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-9-23 07:33</a>
没触摸板玩不了不支持手柄的游戏，你觉得它多余那是你没懂这个的存在意义，这玩意比索尼那样子货实用百倍 ...</blockquote>
那可能是我库里这种游戏极少吧...

*****

####  慕容断月  
##### 1804#       发表于 2022-9-23 17:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57610569&amp;ptid=2015700" target="_blank">Motoko-9 发表于 2022-9-23 13:17</a>
那可能是我库里这种游戏极少吧...</blockquote>
我举几个例子，这个触摸板能在游戏里第三方的方式实现一个最大九宫格的快捷菜单，或者一些类似的东西，而且这个触摸板打fps非常爽，这类在比如文明6这样的游戏能更好利用，毕竟pc版确实不支持手柄

*****

####  Motoko-9  
##### 1805#       发表于 2022-9-23 17:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57614127&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-9-23 17:13</a>
我举几个例子，这个触摸板能在游戏里第三方的方式实现一个最大九宫格的快捷菜单，或者一些类似的东西，而 ...</blockquote>
fps用触摸板吗？有点意思我适应一下看看

*****

####  Motoko-9  
##### 1806#       发表于 2022-9-23 17:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57614127&amp;ptid=2015700" target="_blank">慕容断月 发表于 2022-9-23 17:13</a>
我举几个例子，这个触摸板能在游戏里第三方的方式实现一个最大九宫格的快捷菜单，或者一些类似的东西，而 ...</blockquote>
fps用触摸板吗？有点意思我适应一下看看

*****

####  kalavinka  
##### 1807#       发表于 2022-9-23 18:11

8月4号预定的提醒付尾款了<img src="https://static.saraba1st.com/image/smiley/animal2017/008.png" referrerpolicy="no-referrer">

*****

####  久島鴎  
##### 1808#       发表于 2022-9-23 23:01

 本帖最后由 久島鴎 于 2022-9-23 23:06 编辑 

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">64g下单一个月就收到补款邮件了，看来现货不远了

*****

####  anjel  
##### 1809#       发表于 2022-9-24 00:51

付钱付了3天了
收到thank you for the purchase
信用卡账单显示pending
请问要不要紧啊
我好方<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  Motoko-9  
##### 1810#       发表于 2022-9-24 03:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57620778&amp;ptid=2015700" target="_blank">anjel 发表于 2022-9-24 00:51</a>
付钱付了3天了
收到thank you for the purchase
信用卡账单显示pending</blockquote>
才三天，我等了十天才发货。。。

*****

####  nyaneko  
##### 1811#       发表于 2022-9-24 03:26

SD到了，跟我的键盘差不多大<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  riin  
##### 1812#       发表于 2022-9-24 07:38

气人啊，我错过补款的通知，过期了。不过我是6月份订的9月份就有通知，我现在再订估计也就1-2个月就能定了

*****

####  yulewuchu  
##### 1813#       发表于 2022-9-24 07:44

又开不开机了，遇到好几次了，玩2077和如龙7，待机后再按电源键没反应，下次是不是得退游戏后再关机

*****

####  慕容断月  
##### 1814#       发表于 2022-9-24 09:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57614418&amp;ptid=2015700" target="_blank">Motoko-9 发表于 2022-9-23 17:33</a>
fps用触摸板吗？有点意思我适应一下看看</blockquote>
对，用触摸板准确度远高于摇杆，而且还有陀螺仪，体感配合触摸板微操，准确度一点都不比鼠标差

*****

####  plumlis  
##### 1815#       发表于 2022-9-24 09:30

Steam库里大部分标称“完全支持”的RPG或者Gal，以及某些 AVG，所谓的支持就是让你用摇杆控制鼠标……

这时候触摸板就很重要了。

*****

####  plumlis  
##### 1816#       发表于 2022-9-24 09:31

我就想知道现在亚洲那个 komodo 到底什么时候开始发货。

*****

####  nnnnick22  
##### 1817#       发表于 2022-9-24 09:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57622307&amp;ptid=2015700" target="_blank">plumlis 发表于 2022-9-24 09:31</a>
我就想知道现在亚洲那个 komodo 到底什么时候开始发货。</blockquote>
按原计划年末吧 目前产能虽然上来了 但看起来完全没有在亚洲好好批货的意思

*****

####  lasrotel  
##### 1818#       发表于 2022-9-24 09:40

按现在的出货速度，大概再过十天半个月就有现货了。到时候应该就会轮到亚洲代理商了吧

*****

####  zris  
##### 1819#       发表于 2022-9-24 11:48

现在据说加拿大那边出点事了

不过肯定是优先欧盟 北美，等那边能同步卖的话

估计亚洲这边就开始放货了

顺便欢迎谭友加dick群<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  夜_乌鸦  
##### 1820#       发表于 2022-9-24 12:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57623715&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-24 11:48</a>
现在据说加拿大那边出点事了

不过肯定是优先欧盟 北美，等那边能同步卖的话</blockquote>
群号求发一个<img src="https://static.saraba1st.com/image/smiley/face2017/075.png" referrerpolicy="no-referrer">

*****

####  zris  
##### 1821#       发表于 2022-9-24 12:02

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57623864&amp;ptid=2015700" target="_blank">夜_乌鸦 发表于 2022-9-24 12:01</a>

群号求发一个</blockquote>
498166847

其实我签名就写了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  夜_乌鸦  
##### 1822#       发表于 2022-9-24 12:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57623871&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-24 12:02</a>
498166847

其实我签名就写了</blockquote>
app上没有签名<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  李小狼  
##### 1823#       发表于 2022-9-24 12:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57623715&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-24 11:48</a>
现在据说加拿大那边出点事了

不过肯定是优先欧盟 北美，等那边能同步卖的话</blockquote>
刚托基友在加拿大订上。请问出啥事了？

—— 来自 Xiaomi MIX 2S, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  indtability  
##### 1824#       发表于 2022-9-24 12:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57621659&amp;ptid=2015700" target="_blank">riin 发表于 2022-9-24 07:38</a>
气人啊，我错过补款的通知，过期了。不过我是6月份订的9月份就有通知，我现在再订估计也就1-2个月就能定了 ...</blockquote>
找客服可以再给一次购买机会

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  zris  
##### 1825#       发表于 2022-9-24 12:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57623985&amp;ptid=2015700" target="_blank">李小狼 发表于 2022-9-24 12:11</a>

刚托基友在加拿大订上。请问出啥事了？

—— 来自 Xiaomi MIX 2S, Android 10上的 S1Next-鹅版 v2.5.4 ...</blockquote>
说是暂时发送订单

*****

####  ivly  
##### 1826#       发表于 2022-9-25 09:34

在想要不要买个可以付尾款的账号了，但是又怕被原主找回<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 HUAWEI ABR-AL60, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  泰坦失足  
##### 1827#       发表于 2022-9-26 14:05

看了下这周五估计就轮到我付款了，问下现在挂刀能做到多少汇率？不行就当下勇士直接淘宝买5.7左右余额算了

*****

####  赤魔法师  
##### 1828#       发表于 2022-9-26 21:37

 本帖最后由 赤魔法师 于 2022-9-26 21:42 编辑 

终于到手了

可是有点失望

这屏幕是不是太垃圾了

感觉比ns的还差…

有的分辨率还没有适配怪怪的

512G的是不是也这样

*****

####  5353  
##### 1829#       发表于 2022-9-26 21:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57662294&amp;ptid=2015700" target="_blank">赤魔法师 发表于 2022-9-26 21:37</a>

终于到手了

可是有点失望

可这屏幕是不是太垃圾了</blockquote>
屏幕这点不用感觉,除了分辨率,甚至不如初版的ns.

*****

####  yoyodty  
##### 1830#       发表于 2022-9-27 01:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57662294&amp;ptid=2015700" target="_blank">赤魔法师 发表于 2022-9-26 21:37</a>
终于到手了

可是有点失望

这屏幕是不是太垃圾了</blockquote>
有个调整饱和度的插件可以略微改善



*****

####  revoer  
##### 1831#       发表于 2022-9-27 10:00

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57662294&amp;ptid=2015700" target="_blank">赤魔法师 发表于 2022-9-26 21:37</a>

终于到手了

可是有点失望

这屏幕是不是太垃圾了</blockquote>
不用感觉，就是比ns差，基本是这个价位消费电子产品最差的屏幕<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">

*****

####  Pettabuz  
##### 1832#       发表于 2022-9-27 10:49

9.3下单的，今天凌晨收到了补款邮件。问一下64GB款换SSD的话买什么硬盘比较好？

*****

####  zris  
##### 1833#       发表于 2022-9-27 10:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57667623&amp;ptid=2015700" target="_blank">Pettabuz 发表于 2022-9-27 10:49</a>

9.3下单的，今天凌晨收到了补款邮件。问一下64GB款换SSD的话买什么硬盘比较好？ ...</blockquote>
性价比最高：SN530

其他的话可以考虑买铠侠

反正2230 ssd选择不多，看着来就行

*****

####  Re.Troy  
##### 1834#       发表于 2022-9-27 11:08

512GB八月定今天收到邮件，下单了<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

*****

####  kalavinka  
##### 1835#       发表于 2022-9-27 14:04

看了评测和数据就对这块屏幕放弃了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  yulewuchu  
##### 1836#       发表于 2022-9-27 19:41

兄弟们注意开机键，我之前开不开机是因为开机键塌了，接触不良，修好之后玩了两天今天按开机键感觉又有点松

*****

####  Hanzong  
##### 1837#       发表于 2022-9-27 20:37

话说大家从补款 到 发货 大概等了多久？

*****

####  zris  
##### 1838#       发表于 2022-9-27 21:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57675419&amp;ptid=2015700" target="_blank">Hanzong 发表于 2022-9-27 20:37</a>
话说大家从补款 到 发货 大概等了多久？</blockquote>
现在差不多一个月，估计接下来一两周，或者直接现货了

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  硫黄  
##### 1839#       发表于 2022-9-28 01:39

8.29预定的64G。昨天通知可以补款了

一看淘宝充值卡涨到570不想补了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  Hanzong  
##### 1840#       发表于 2022-9-28 02:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57676213&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-27 21:47</a>

现在差不多一个月，估计接下来一两周，或者直接现货了

—— 来自 S1Fun</blockquote>
我是说补款 到 发货啊， 不是预购到补款

*****

####  萩原组土狼p  
##### 1841#       发表于 2022-9-28 02:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57678198&amp;ptid=2015700" target="_blank">硫黄 发表于 2022-9-28 01:39</a>

8.29预定的64G。昨天通知可以补款了

一看淘宝充值卡涨到570不想补了</blockquote>
你定的是美版还是哪边的

我也差不多是29号让朋友帮我订的日版的

*****

####  硫黄  
##### 1842#       发表于 2022-9-28 02:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57678298&amp;ptid=2015700" target="_blank">萩原组土狼p 发表于 2022-9-28 02:10</a>

你定的是美版还是哪边的

我也差不多是29号让朋友帮我订的日版的</blockquote>
美版

*****

####  anjel  
##### 1843#       发表于 2022-9-28 03:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57678297&amp;ptid=2015700" target="_blank">Hanzong 发表于 2022-9-28 02:10</a>
我是说补款 到 发货啊， 不是预购到补款</blockquote>
我等了四天
付钱的时候信用卡显示pending
到发货时候才扣款
reddit说一般周末会发前一周的

*****

####  Hanzong  
##### 1844#       发表于 2022-9-28 06:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57678477&amp;ptid=2015700" target="_blank">anjel 发表于 2022-9-28 03:40</a>

我等了四天

付钱的时候信用卡显示pending

到发货时候才扣款</blockquote>
多谢多谢

*****

####  zris  
##### 1845#       发表于 2022-9-28 09:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57678297&amp;ptid=2015700" target="_blank">Hanzong 发表于 2022-9-28 02:10</a>
我是说补款 到 发货啊， 不是预购到补款</blockquote>
哦哦，我之前是两天左右，有的一天就发，这个不一定

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  Hanzong  
##### 1846#       发表于 2022-9-28 09:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57679723&amp;ptid=2015700" target="_blank">zris 发表于 2022-9-28 09:21</a>

哦哦，我之前是两天左右，有的一天就发，这个不一定

—— 来自 S1Fun</blockquote>
好的好的，刚等一天，焦急中

*****

####  笨笨塞  
##### 1847#       发表于 2022-9-28 10:09

哪里可以预定，并且比较快啊😔😔😔

*****

####  zris  
##### 1848#       发表于 2022-9-28 10:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57680312&amp;ptid=2015700" target="_blank">笨笨塞 发表于 2022-9-28 10:09</a>
哪里可以预定，并且比较快啊😔😔😔</blockquote>
美区steam

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  ivly  
##### 1849#       发表于 2022-9-28 12:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57680312&amp;ptid=2015700" target="_blank">笨笨塞 发表于 2022-9-28 10:09</a>
哪里可以预定，并且比较快啊😔😔😔</blockquote>
现在美区steam预订很快了
我9月24日预订，可能这一周或者下一周就能付尾款了

—— 来自 HUAWEI ABR-AL60, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  lonelycat  
##### 1850#       发表于 2022-9-28 12:53

终于快要有现货了，然鹅按摩店下一代CPU都出来了，啥也不说了，早买早享受，晚买有折扣。

*****

####  医生狼多  
##### 1851#       发表于 2022-9-28 13:04

等明年7800u和sd2<img src="https://static.saraba1st.com/image/smiley/face2017/032.png" referrerpolicy="no-referrer">

*****

####  笨笨塞  
##### 1852#       发表于 2022-9-28 14:48

这么快的嘛

*****

####  zqr211  
##### 1853#       发表于 2022-9-28 14:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57682678&amp;ptid=2015700" target="_blank">医生狼多 发表于 2022-9-28 13:04</a>
等明年7800u和sd2</blockquote>
2年就更新过分了吧 这是游戏机啊

好歹4年

*****

####  笨笨塞  
##### 1854#       发表于 2022-9-28 14:53

注册那个steam号一直卡认证。

*****

####  医生狼多  
##### 1855#       发表于 2022-9-28 15:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57683919&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-28 14:51</a>
2年就更新过分了吧 这是游戏机啊

好歹4年</blockquote>
当pc来看嘛
今年已经打不过6800u了，再过两年就太落伍了

*****

####  亚瑟摩根  
##### 1856#       发表于 2022-9-28 15:23

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">还四年？估计明年下半年就有dick2了

现在soc不都曝光了吗

*****

####  83913536  
##### 1857#       发表于 2022-9-28 20:50

Deck的标准是30帧-40帧

现在6800U都奔着60帧去了，下一步得是1080P 60帧

*****

####  时空之旅  
##### 1858#       发表于 2022-9-28 21:36

<blockquote>zqr211 发表于 2022-9-28 14:51
2年就更新过分了吧 这是游戏机啊

好歹4年</blockquote>
g胖说过更新会比较快，2年可以了

传统游戏机更新慢主要是硬件研发过于贵，更重要的是兼容始终不如pc方便

*****

####  时空之旅  
##### 1859#       发表于 2022-9-28 21:37

<blockquote>亚瑟摩根 发表于 2022-9-28 15:23
还四年？估计明年下半年就有dick2了

现在soc不都曝光了吗</blockquote>
soc是啥？

*****

####  frankCC  
##### 1860#       发表于 2022-9-28 21:50

 本帖最后由 frankCC 于 2022-9-28 21:59 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57688939&amp;ptid=2015700" target="_blank">时空之旅 发表于 2022-9-28 21:37</a>

soc是啥？</blockquote>

<img src="https://img.saraba1st.com/forum/202209/28/214818fce50yfvvvy12vcy.png" referrerpolicy="no-referrer">

<strong>84357347893478945.png</strong> (48.81 KB, 下载次数: 0)

下载附件

2022-9-28 21:48 上传

规格没变，架构和工艺提升，可能还是比不上6800u，主要研发方向如之前pdf说的省电和缩小体积。



*****

####  zqr211  
##### 1861#       发表于 2022-9-28 22:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57688925&amp;ptid=2015700" target="_blank">时空之旅 发表于 2022-9-28 21:36</a>

g胖说过更新会比较快，2年可以了

传统游戏机更新慢主要是硬件研发过于贵，更重要的是兼容始终不如pc方便

 ...</blockquote>
2年更新

那不买首发就不用买了....

*****

####  83913536  
##### 1862#       发表于 2022-9-29 00:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57689759&amp;ptid=2015700" target="_blank">zqr211 发表于 2022-9-28 22:50</a>

2年更新

那不买首发就不用买了....</blockquote>
国产都是每年更新呢…

*****

####  zqr211  
##### 1863#       发表于 2022-9-29 01:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57690787&amp;ptid=2015700" target="_blank">83913536 发表于 2022-9-29 00:40</a>
国产都是每年更新呢…</blockquote>
这个就是我想的问题

国产 怎么样发售后2个月一般就能原价买

这个steam掌机下一代要出了这一代原价都买不到。。。<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  亚瑟摩根  
##### 1864#       发表于 2022-9-29 10:36

不如看看aya 今年发布了多少新机<img src="https://static.saraba1st.com/image/smiley/face2017/053.png" referrerpolicy="no-referrer">



*****

####  xrxtzz  
##### 1865#       发表于 2022-9-30 08:48

终于收到了，换完硬盘感觉背后盖子没合紧，但真的懒得再拆一次重装了<img src="https://static.saraba1st.com/image/smiley/face2017/217.gif" referrerpolicy="no-referrer">



*****

####  revoer  
##### 1866#       发表于 2022-9-30 09:47

中环清关半个月了<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">



*****

####  Pettabuz  
##### 1867#       发表于 2022-10-1 13:10

话说货物已打包是什么意思，已经两天了为什么还不给我发



*****

####  zris  
##### 1868#       发表于 2022-10-1 13:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57719345&amp;ptid=2015700" target="_blank">Pettabuz 发表于 2022-10-1 13:10</a>
话说货物已打包是什么意思，已经两天了为什么还不给我发</blockquote>
集中发，现在量多了，大概一周发一次，是v社拉去fedex的网店。以前量少一周可以发两次。你这两天先别急。

—— 来自 [S1Fun](https://s1fun.koalcat.com)



*****

####  硫黄  
##### 1869#       发表于 2022-10-2 16:43

SD桌面模式装了heroic，开个游戏要等五分钟，太神秘了<img src="https://static.saraba1st.com/image/smiley/face2017/125.png" referrerpolicy="no-referrer">



*****

####  慕容断月  
##### 1870#       发表于 2022-10-2 21:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57731885&amp;ptid=2015700" target="_blank">硫黄 发表于 2022-10-2 16:43</a>
SD桌面模式装了heroic，开个游戏要等五分钟，太神秘了</blockquote>
用heroic装游戏，启动另外装个legendary+指令的方式，这样快一些



*****

####  硫黄  
##### 1871#       发表于 2022-10-3 07:53

steamdick这个os咖喱味实在太浓了

有些默认全屏的游戏，打开后黑屏但有声音，按键有反应

改兼容层没用，但切桌面模式就打开就变窗口化能跑了，比如数码兽赛博侦探

有的切桌面模式打开还是全屏黑屏。比如回溯依存

只要在电脑上在进游戏改成窗口模式，然后云存档

sd上同步存档以后就能玩了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  wfhtony  
##### 1872#       发表于 2022-10-7 02:57

 本帖最后由 wfhtony 于 2022-10-7 03:01 编辑 

[Steam Deck 和基座已有现货，可直接购买！](https://store.steampowered.com/news/app/1675200/view/3276955672625890259)
[https://youtu.be/bcwkMfoUATc](https://youtu.be/bcwkMfoUATc)

现在买Steam Deck不用排队了，基本是即买即下单（欧美）。
官方的Dock也有售价信息了...[不过要89刀](https://store.steampowered.com/steamdeckdock)...

另外：<blockquote>使用基座会提升 Deck 的效能吗？

不会，基座提供充电及连接功能，但无法提供额外效能益处。</blockquote>咱还是用hub算了。<img src="https://static.saraba1st.com/image/smiley/face2017/019.png" referrerpolicy="no-referrer">

*****

####  Hanzong  
##### 1873#       发表于 2022-10-7 04:59

终于到手了，握持感不错

然后就看着今天宣布现货了啊嗯

*****

####  roxassix  
##### 1874#       发表于 2022-10-7 05:21

 本帖最后由 roxassix 于 2022-10-7 05:28 编辑 

亚版代理两天前发公告说亚版还是年末发。。。<img src="https://static.saraba1st.com/image/smiley/face2017/028.png" referrerpolicy="no-referrer">

今天本社这边都说可以直接现货了，亚版也不说提前一点。。<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer"> 

[https://twitter.com/ondeckjp/sta ... XT_upxSCHaT2wy0RgxQ](https://twitter.com/ondeckjp/status/1577142687546736640?s=46&amp;t=kLKXT_upxSCHaT2wy0RgxQ)

【Regarding the shipping schedule in Asia】

The shipping will be started from the end of 2022. We will make announcement as soon as the product is ready for shipment. For more information, please check the FAQ at the bottom of the reservation site.



*****

####  Hanzong  
##### 1875#       发表于 2022-10-7 06:17

问两个问题，翻楼翻不动了：

1.想给428加汉化，应该怎么操作啊

2.现在最佳的玩模拟的方法是啥



*****

####  nozomitech  
##### 1876#       发表于 2022-10-7 06:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57789202&amp;ptid=2015700" target="_blank">Hanzong 发表于 2022-10-6 23:17</a>
问两个问题，翻楼翻不动了：

1.想给428加汉化，应该怎么操作啊

2.现在最佳的玩模拟的方法是啥3.好像看有老 ...</blockquote>
最简单的方法就是电脑端下好游戏打好补丁，SD这里同样下好游戏未打补丁，然后用U盘把电脑上整个游戏覆盖回去。

—— 来自 [S1Fun](https://s1fun.koalcat.com)



*****

####  Hanzong  
##### 1877#       发表于 2022-10-7 06:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57789236&amp;ptid=2015700" target="_blank">nozomitech 发表于 2022-10-7 06:46</a>

最简单的方法就是电脑端下好游戏打好补丁，SD这里同样下好游戏未打补丁，然后用U盘把电脑上整个游戏覆盖 ...</blockquote>
这么简单，多谢



*****

####  Piano-Forest  
##### 1878#         楼主| 发表于 2022-10-7 10:49

[https://store.steampowered.com/n ... 3276955672625890259](https://store.steampowered.com/news/app/1675200/view/3276955672625890259)

Steam Deck 现在无需预订即可购买！(美区）

我们很高兴能带来这条好消息：在发送今天这批订购邮件后，我们已经处理完了预订队列中的所有订单。 Steam Deck 现在处于有货状态，可以直接购买！

距离 Steam Deck 首次露面已经过去了一年多。 从第一天起，我们一直在应对层出不穷的供应链问题和部件短缺问题。 在团队努力解决这些问题并尽力满足需求的同时，我们启用了一个预订系统。 这个系统让客户能够排队占位，而无需费心刷新页面或大战抢购软件。

在过去的一年中，团队为解决部件短缺和物流问题付出了很大的努力。正是因为这些努力，我们现在正以空前的高速度生产和配送 Steam Deck。 尽管预订的增长速度越来越快，但我们已经能够超出发货预期，并终于在今天清空了预订队列。

尽管如此，我们的生产、处理和配送能力也还是有限的。 如果 Steam Deck 特定型号的订单量超出我们及时发货的能力，预计配送时间就会延长，而到了一定程度我们就会退回到预订模式，直至能赶上收到订单的速度。 与之前一样，顾客们将在队列中获得一个位置，可以下单时将收到电子邮件通知。 一旦我们赶上预订的增长速度，并处理完所有已收到的预订，我们就将再次允许直接下单。

能够达成这个重要的里程碑，我们感到非常兴奋，并将尽快把各位订购的 Deck 发送出来。

官方基座来了！
[https://store.steampowered.com/steamdeckdock](https://store.steampowered.com/steamdeckdock)

官方基座配有 3 个 USB-A 3.1 Gen1 端口、1 个 USB-C 充电端口、DisplayPort 端口、HDMI 端口以及 1 个千兆以太网端口，满足您的一切连接需求。 这款完美适配的基座能将您的 Steam Deck 连接至电源、最多两台外部显示器，以及任意数量的其他外设。

如果基座是否来自官方对您来说并不重要，您也完全可以使用任何其他 USB-C 基座或集线器。 我们在 SteamOS 上下了很多功夫，这不仅让 Steam Deck 与官方基座完美适配，也有助于提升与其他第三方集线器和基座的适配性。

官方基座现已开放购买！ 您可以在这里了解更多信息，或在这里下单购买。

与 Steam Deck 一样，官方基座的订单处理和配送能力也是有限的，如果订单量极大，我们将转为预订模式，直至赶上下单速度为止。 终于能将官方基座交到各位顾客的手中，我们感到很高兴，也非常感谢大家的耐心！

Steam Deck 软件更新 <blockquote>我们的团队在过去几个月中不断地更新和改进 Steam Deck 的软件，以下是已发布更新中的一些亮点：

用户界面和用户体验改进

我们在 Steam 界面中添加了直达成就和指南的快速链接，改进了游戏内的体验。 存放截图的媒体页面进行了重新设计，性能也大大改进。 夜间模式现在可以设置为在一天的不同时间自动开启和关闭。 离线模式进行了一系列改进，稳定性大大提升，用起来更为直观。

新的 Steam 输入功能

除多项错误修复和用户界面改进外，现在模式切换已得到支持，Steam 输入虚拟菜单也进行了彻底的改版和重新设计。 您现在可以命名虚拟菜单，将其在不同来源之间移动，对于图标和颜色也有了更好的控制。

更多键盘、体验改进

为准备好在新的地区推出 Steam Deck，我们为简体中文、繁体中文、日语和韩语添加了屏幕键盘支持。 此外，无论是在游戏模式中还是桌面模式中，使用触摸屏和触控板在屏幕键盘上打字时的体验和响应都有了大幅提升。

系统更新

SteamOS、驱动程序和固件都得到了更新，以提升整个 Steam Deck 的性能和稳定性。 此外，为了帮助大家追踪系统更新和测试版（如果您选择加入测试），我们添加了更简单的全新更新通道：稳定、测试和预览。

基座模式焕新

我们专注于多项用户界面、软件和操作系统的更新，以提升接入基座的体验——这不只是针对官方基座，也面向所有连接的基座、集线器和外设。 我们的团队为外部显示器添加了缩放、分辨率和刷新率设置，并为外部显示器、外设和音频输出场景提供了广泛的兼容性。</blockquote>

Steam Deck 面向日本、韩国、台湾和香港开放预订

我们扩大生产的另一项成果是扩展到其他地区的能力。 最近，我们通过在日本、韩国、台湾和香港的分销合作伙伴 Komodo，在上述地区开放了预订。 为了庆祝产品的发布并进行宣传，我们最近去了东京电玩展，并带去了一个巨大的 Steam Deck，非常酷。

如果您身在这些地区，并想要预订 Steam Deck 的话，可以在这个网站通过 Komodo 预订。 我们还在继续将 Steam Deck 推向全球更多地区，在有更多消息时将会让大家知道。

这就是今天的内容，我们下次见！



*****

####  windhawind2  
##### 1879#       发表于 2022-10-8 19:51

额啊本来想买了 一看现在淘宝上美区100刀充值卡已经600多了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">



*****

####  superkin185  
##### 1880#       发表于 2022-10-8 20:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57815912&amp;ptid=2015700" target="_blank">windhawind2 发表于 2022-10-8 19:51</a>
额啊本来想买了 一看现在淘宝上美区100刀充值卡已经600多了</blockquote>
没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。



*****

####  windhawind2  
##### 1881#       发表于 2022-10-9 08:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-08 20:48:06</a>
没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>莫非我搜错了..方便把店铺名私我一下吗谢谢

[  -- 来自 能手机投票的 Stage1官方 iOS客户端](https://itunes.apple.com/fi/app/saraba1st/id1221237470?mt=8)



*****

####  Re.Troy  
##### 1882#       发表于 2022-10-9 08:53

完了，收到货都一天了才想起自己没用充值卡直接信用卡买了<img src="https://static.saraba1st.com/image/smiley/face2017/143.png" referrerpolicy="no-referrer">



*****

####  慕容断月  
##### 1883#       发表于 2022-10-9 12:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57789242&amp;ptid=2015700" target="_blank">Hanzong 发表于 2022-10-7 06:50</a>

这么简单，多谢</blockquote>
如果没记错Linux版steam的游戏安装信息也是记录在库的common文件夹同级目录内的acf文件里，偷懒一点的办法是直接win上处理完了连带处理好的游戏和acf文件丢到sd的对应位置，再重启steam，这样可以少下一次游戏，但是有些游戏可能不能这样

*****

####  mp5  
##### 1884#       发表于 2022-10-9 12:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>

没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
求私信



*****

####  psvsd  
##### 1885#       发表于 2022-10-9 12:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
 没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
同求个私信

*****

####  psvsd  
##### 1886#       发表于 2022-10-9 12:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
 没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
同求个私信

*****

####  psvsd  
##### 1887#       发表于 2022-10-9 12:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
 没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
同求个私信



*****

####  superkin185  
##### 1888#       发表于 2022-10-9 13:19

这没啥好私信的，淘宝搜索steam充值卡，各个商家的价格都是在100美金510元人民币左右的水平，自己选择口碑好一点的就可以了呀，充值会比较慢，大概需要3到5天。

<img src="https://img.saraba1st.com/forum/202210/09/131842p900fdzd4yodyueq.png" referrerpolicy="no-referrer">

<strong>F8DFD665-94D3-4BE0-8971-62DDB375D8F0.png</strong> (663.61 KB, 下载次数: 0)

下载附件

2022-10-9 13:18 上传

泥潭还有个SD群，我之前都是在群里大佬的指导下买的

FE114DA0-59A0-4F27-92BA-B2C7D13C4492.jpeg
(236.31 KB, 下载次数: 0)

下载附件

2022-10-9 13:19 上传

<img src="https://img.saraba1st.com/forum/202210/09/131921yeez1vpe1ke3okke.jpeg" referrerpolicy="no-referrer">" src="https://static.saraba1st.com/image/common/none.gif" referrerpolicy="no-referrer">

*****

####  psvsd  
##### 1889#       发表于 2022-10-9 13:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
 没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
同求个私信



*****

####  虚拟小仓星  
##### 1890#       发表于 2022-10-9 13:35

占个楼更新一下自己的购买经历<img src="https://static.saraba1st.com/image/smiley/carton2017/313.png" referrerpolicy="no-referrer">应该算steamdeck现货后第一批购买客户

<img src="https://p.sda1.dev/7/9a48738c76a93c3da3b452c6ef40bc39/55ef8043b3409ef1.jpg" referrerpolicy="no-referrer">

*10月8号淘宝买充值卡花费2080 

*10月9号显示货物已打包



*****

####  superkin185  
##### 1891#       发表于 2022-10-9 13:57

 本帖最后由 superkin185 于 2022-10-9 13:59 编辑 

我用的中环转运，运了30天还没到手里<img src="https://static.saraba1st.com/image/smiley/face2017/044.png" referrerpolicy="no-referrer">

4FB3E6DE-6656-4D77-906D-9F58C95A0DCC.jpeg
(281.25 KB, 下载次数: 0)

下载附件

2022-10-9 13:59 上传

<img src="https://img.saraba1st.com/forum/202210/09/135926qzq4oa7r8mzm5htn.jpeg" referrerpolicy="no-referrer">" src="https://static.saraba1st.com/image/common/none.gif" referrerpolicy="no-referrer">

*****

####  EEEEhentai  
##### 1892#       发表于 2022-10-9 13:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57826268&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-9 13:57</a>

我用的中环转运，运了30天还没到手里</blockquote>
兄弟 太真实了，听说清关要8个工作日



*****

####  endn1991  
##### 1893#       发表于 2022-10-9 14:02

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
求私信

—— 来自 samsung SM-N9860, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play



*****

####  布里兰特  
##### 1894#       发表于 2022-10-9 15:47

<blockquote>superkin185 发表于 2022-10-8 20:48
没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
私信推荐下！



*****

####  时空之旅  
##### 1895#       发表于 2022-10-9 16:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>

没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
球私信



*****

####  windhawind2  
##### 1896#       发表于 2022-10-9 17:10

我看了下较便宜的美区充值不是充值卡 都是自己登陆steam账号密码或者和机器人交易啥的 这样的安全性没问题么…？

[  -- 来自 能搜索的 Stage1官方 iOS客户端](https://itunes.apple.com/fi/app/saraba1st/id1221237470?mt=8)



*****

####  亚瑟摩根  
##### 1897#       发表于 2022-10-9 22:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57830568&amp;ptid=2015700" target="_blank">windhawind2 发表于 2022-10-9 17:10</a>
我看了下较便宜的美区充值不是充值卡 都是自己登陆steam账号密码或者和机器人交易啥的 这样的安全性没问题 ...</blockquote>
买了两个了，一点事都没有，就是泥潭推荐那个马云店

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  Pettabuz  
##### 1898#       发表于 2022-10-20 12:36

今天到货了，虽然有些心理准备，但是打开箱子第一眼还是觉得，好大……



*****

####  zris  
##### 1899#       发表于 2022-10-20 12:43

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">DICK大点好



*****

####  笨笨塞  
##### 1900#       发表于 2022-10-20 13:15

不能翻墙就买不了是吧？

*****

####  笨笨塞  
##### 1901#       发表于 2022-10-20 13:15

不能翻墙就买不了是吧？

*****

####  山形石雄  
##### 1902#       发表于 2022-10-23 16:38

到了到了！历时49天。<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">



*****

####  solora  
##### 1903#       发表于 2022-10-23 19:49

QQ群加不进去啊，谁私信个淘宝店

*****

####  maninhole  
##### 1904#       发表于 2022-11-5 19:23

清关延误——国际货物放行，这是清完关了吗

到fedex服务站又说本地延误超出了我们的控制，这到底什么情况，是已经清完关了还是没清完



*****

####  这是闹球甚  
##### 1905#       发表于 2022-11-5 20:41

8月底开始发货昨天才到，中环转运真闹不住



*****

####  asd235614  
##### 1906#       发表于 2022-11-7 15:25

<img src="https://static.saraba1st.com/image/smiley/face2017/149.png" referrerpolicy="no-referrer">准备在京东自营店上入一个，之前没操作过更换硬件，想问一下换硬盘的话有啥注意事项么，还一个就是对于一些需要加速的游戏能在steamOS上使用加速器么



*****

####  精钢魔像  
##### 1907#       发表于 2022-11-7 16:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58319760&amp;ptid=2015700" target="_blank">asd235614 发表于 2022-11-7 15:25</a>

准备在京东自营店上入一个，之前没操作过更换硬件，想问一下换硬盘的话有啥注意事项么，还一个就是 ...</blockquote>
要注意拔电池线，不拔可能会砖。搜搜b站应该就有了

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| asd235614| + 1|了解，感谢|

查看全部评分



*****

####  zris  
##### 1908#       发表于 2022-11-7 18:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58319760&amp;ptid=2015700" target="_blank">asd235614 发表于 2022-11-7 15:25</a>

准备在京东自营店上入一个，之前没操作过更换硬件，想问一下换硬盘的话有啥注意事项么，还一个就是 ...</blockquote>
拔电池，但是现在电池有点恶心，难拔，注意别把电容给搞飞了就行

*****

####  zris  
##### 1909#       发表于 2022-11-7 18:39

顺便说一句，有不会的可以加群，群里多是大佬研究透了，不懂直接群里发问，马上解决<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">

steam dick 交友群：498166847



*****

####  Litccc  
##### 1910#       发表于 2022-11-7 18:47

京东自营那个纯杀猪价



*****

####  maninhole  
##### 1911#       发表于 2022-11-7 20:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58323252&amp;ptid=2015700" target="_blank">Litccc 发表于 2022-11-7 18:47</a>
京东自营那个纯杀猪价</blockquote>
闲鱼上一般也是三千六七……



*****

####  akane3000  
##### 1912#       发表于 2022-11-7 23:22

中环显示等待清关已经一周多了，这还要清多久



*****

####  sunnyjee  
##### 1913#       发表于 2022-11-8 02:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58326928&amp;ptid=2015700" target="_blank">akane3000 发表于 2022-11-7 23:22</a>
 中环显示等待清关已经一周多了，这还要清多久</blockquote>
一般要2周



*****

####  annoth  
##### 1914#       发表于 2022-11-8 09:21

<blockquote>asd235614 发表于 2022-11-7 15:25
准备在京东自营店上入一个，之前没操作过更换硬件，想问一下换硬盘的话有啥注意事项么，还一个就是 ...</blockquote>
我觉得要注意挑好的螺丝刀，这机器的螺丝质量不太行，我拆的时候就滑丝了，后来找旧手机的用电烙铁把那个孔烫了个洞弄下来的



*****

####  LMBS  
##### 1915#       发表于 2022-11-8 10:17

清关时间随机性好高，隔天到三周都能看到，这个也是跟选择的线路有关吗

*****

####  maninhole  
##### 1916#       发表于 2022-11-8 10:17

牛逼，好不容易动态更新到送货了

结果fedex公众号上的送货员号码是个停机的号<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

这nm联系个毛



*****

####  cqc1021  
##### 1917#       发表于 2022-11-8 10:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58324582&amp;ptid=2015700" target="_blank">maninhole 发表于 2022-11-7 20:21</a>
闲鱼上一般也是三千六七……</blockquote>
京东自营都4000了，而且换了硬盘后也不用指望京东能提供售后了，那还干嘛在京东买。



*****

####  kalavinka  
##### 1918#       发表于 2022-11-8 12:20

终于运到国内了 中环清关大概要多久



*****

####  zhjnppy  
##### 1919#       发表于 2022-11-8 14:23

准备入手 爬了最新的几页 现在最好的入手方式是闲鱼+低配自换硬盘？

*****

####  霖岚_  
##### 1920#       发表于 2022-11-8 14:27

我10月24日到的国内，到现在已经等清关等了11个工作日了



*****

####  sunnyjee  
##### 1921#       发表于 2022-11-8 16:49

中环我是8.26美国出库

9.16到达中国开始清关

9.28海关查验

10.13查验结束缴税

10.21显示放行但是上海圆通疫情挂了发不出货

10.27转京东物流发货 10.29到手

反正就是很慢且税。。。



*****

####  maninhole  
##### 1922#       发表于 2022-11-8 20:59

拿到了

360的税加350的运费加30人工费加2100的美区充值

<img src="https://p.sda1.dev/8/ab01b44846050c4811118a0ed2392c98/CMP_20221108205849441.jpg" referrerpolicy="no-referrer">



*****

####  世界的膀胱者  
##### 1923#       发表于 2022-11-9 17:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58334636&amp;ptid=2015700" target="_blank">zhjnppy 发表于 2022-11-8 14:23</a>
准备入手 爬了最新的几页 现在最好的入手方式是闲鱼+低配自换硬盘？</blockquote>
不在乎等两个礼拜的话淘宝礼品卡+FedEx直邮
3000左右能到手

—— 来自 samsung SM-G9910, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play



*****

####  脸宽  
##### 1924#       发表于 2022-11-10 09:17

想拼多多买了，看他整了个百亿补贴只要3450。就是不知道是不是现货，不然不如自己折腾



*****

####  魔法少女大头  
##### 1925#       发表于 2022-11-12 08:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57816730&amp;ptid=2015700" target="_blank">superkin185 发表于 2022-10-8 20:48</a>
没有啊，不仅没有涨，还降了。之前泥潭群里推荐店家现在100美金508元。</blockquote>
求私信下地址<img src="https://static.saraba1st.com/image/smiley/face2017/075.png" referrerpolicy="no-referrer">

—— 来自 HUAWEI HMA-AL00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4



*****

####  洪水熊猫大势去  
##### 1926#       发表于 2022-11-12 09:37

 本帖最后由 洪水熊猫大势去 于 2022-11-12 09:38 编辑 

问下用steamdeck的，可以用变速齿轮或者ce吗



*****

####  thorlay  
##### 1927#       发表于 2022-11-12 15:56

3150 整了个二手256steam deck，有点点划痕。不知道值不值。

*****

####  魔法少女大头  
##### 1928#       发表于 2022-11-12 15:59

所以现在最简单的购买方式是啥呢，电商平台的3500，3600直购的能买么。

—— 来自 HUAWEI HMA-AL00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4



*****

####  i渐行渐远u  
##### 1929#       发表于 2022-11-12 16:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58399865&amp;ptid=2015700" target="_blank">魔法少女大头 发表于 2022-11-12 15:59</a>

所以现在最简单的购买方式是啥呢，电商平台的3500，3600直购的能买么。

—— 来自 HUAWEI HMA-AL00, Andro ...</blockquote>
国内现货的话还可以。

搞个美区号冲钱+转运费+必税，3000左右，时间1个月起步。

看了下淘宝现在100刀要570，这尼玛也太贵了吧。。。



*****

####  akane3000  
##### 1930#       发表于 2022-11-14 10:28

中环10号显示放行，然后给了我一个顺丰单号，然而到现在都还没揽收，那么到底放行没放行？客服电话24小时无限打不通



*****

####  akane3000  
##### 1931#       发表于 2022-11-14 17:44

发邮件总算联系上了，说我的件退回海关重新查验了，还有这种事？家人们碰到过吗，这大概又要多久？

*****

####  cqc1021  
##### 1932#       发表于 2022-11-21 16:51

桌面模式用触控板好难受啊，感觉时灵时不灵的。



*****

####  403page  
##### 1933#       发表于 2022-11-21 18:12

我的终于上飞机了，预计一周后到中国，不知要清关多久



*****

####  psvsd  
##### 1934#       发表于 2022-11-21 18:24

不要用中环，会变得不幸



*****

####  晴岚  
##### 1935#       发表于 2022-11-24 16:29

问一下现在想买steam deck但不想在闲鱼或者淘宝上面买的话转运那些应该怎么操作？



*****

####  洪水熊猫大势去  
##### 1936#       发表于 2022-11-24 19:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58591902&amp;ptid=2015700" target="_blank">晴岚 发表于 2022-11-24 16:29</a>

问一下现在想买steam deck但不想在闲鱼或者淘宝上面买的话转运那些应该怎么操作？ ...</blockquote>
最近不用看了 产能跟不上又变成预定模式了

不急等明年过完年以后再看吧



*****

####  妄想中毒  
##### 1937#       发表于 2022-11-27 19:21

现在怎么给STEAM充值啊，淘宝全是代充连礼品卡都没了，用自己的国内信用卡好像也不能充



*****

####  kalavinka  
##### 1938#       发表于 2022-11-28 20:55

到了！<img src="https://static.saraba1st.com/image/smiley/face2017/062.gif" referrerpolicy="no-referrer">8月4号预定的一共4个月



*****

####  isa2456  
##### 1939#       发表于 2022-11-28 23:04

想问下tf卡怎么才能在windows上拷文件<img src="https://static.saraba1st.com/image/smiley/face2017/096.png" referrerpolicy="no-referrer">ext4格式主pc的win不能读，exfat的话steam又用不了，不可能准备两张卡吧？



*****

####  guotao323  
##### 1940#       发表于 2022-11-29 16:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58668696&amp;ptid=2015700" target="_blank">isa2456 发表于 2022-11-28 23:04</a>

想问下tf卡怎么才能在windows上拷文件ext4格式主pc的win不能读，exfat的话steam又用不了，不可能准 ...</blockquote>
exFAT格式可以在SteamOS桌面模式读取，右下角快捷区域，选择扩展卡后点击“mount and open”



*****

####  zris  
##### 1941#       发表于 2022-11-29 16:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58591902&amp;ptid=2015700" target="_blank">晴岚 发表于 2022-11-24 16:29</a>

问一下现在想买steam deck但不想在闲鱼或者淘宝上面买的话转运那些应该怎么操作？ ...</blockquote>
美区号，充值美刀，找转运，收货

基本就是这个流程



*****

####  isa2456  
##### 1942#       发表于 2022-11-29 17:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58678260&amp;ptid=2015700" target="_blank">guotao323 发表于 2022-11-29 16:04</a>
exFAT格式可以在SteamOS桌面模式读取，右下角快捷区域，选择扩展卡后点击“mount and open” ...</blockquote>
但是exfat不给创建steam库
最后美团外卖了一条转接线从外接硬盘拷过去了<img src="https://static.saraba1st.com/image/smiley/face2017/152.png" referrerpolicy="no-referrer">



*****

####  kalavinka  
##### 1943#       发表于 2022-11-29 22:58

仁王2有稳40帧的设置吗<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">感觉优化好屎



*****

####  isa2456  
##### 1944#       发表于 2022-11-30 00:00

说好的模拟神器呢，yuzu开咒术泡泡那种游戏都闪退<img src="https://static.saraba1st.com/image/smiley/face2017/152.png" referrerpolicy="no-referrer">



*****

####  泰坦失足  
##### 1945#       发表于 2022-11-30 07:08

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58668696&amp;ptid=2015700" target="_blank">isa2456 发表于 2022-11-28 23:04</a>

想问下tf卡怎么才能在windows上拷文件ext4格式主pc的win不能读，exfat的话steam又用不了，不可能准 ...</blockquote>
Linux桌面模式商城有个Usermode FTP, 我都是FTP传的



*****

####  Piano-Forest  
##### 1946#         楼主| 发表于 2022-11-30 10:46

1217日开始面向日本、韩国、台湾和香港发售



*****

####  yxydd88  
##### 1947#       发表于 2022-12-1 21:37

<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">收到补款邮件了，已下单



*****

####  妄想中毒  
##### 1948#       发表于 2022-12-1 22:50

用的转运中国G胖今天发货了，然后我转运中国填入库发现几种转运方式都不支持我所在的地址只能香港自提，这什么坑爹玩意<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">



*****

####  maninhole  
##### 1949#       发表于 2022-12-1 23:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58713555&amp;ptid=2015700" target="_blank">妄想中毒 发表于 2022-12-1 22:50</a>
用的转运中国G胖今天发货了，然后我转运中国填入库发现几种转运方式都不支持我所在的地址只能香港自提，这 ...</blockquote>
先问问客服，不行……就只能再转运一次了

—— 来自 realme RMX3370, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4



*****

####  nnnnick22  
##### 1950#       发表于 2022-12-2 16:00

日本的邮件总算到了 付款了坐等



*****

####  kalavinka  
##### 1951#       发表于 2022-12-2 16:24

这个触控板怎么还有惯性的<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">能关吗

*****

####  斯库鲁多  
##### 1952#       发表于 2022-12-2 16:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58725364&amp;ptid=2015700" target="_blank">kalavinka 发表于 2022-12-2 16:24</a>

这个触控板怎么还有惯性的能关吗</blockquote>
触控板行为最右的齿轮里，把轨迹球模式关了



*****

####  kalavinka  
##### 1953#       发表于 2022-12-2 19:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58725420&amp;ptid=2015700" target="_blank">斯库鲁多 发表于 2022-12-2 16:27</a>

触控板行为最右的齿轮里，把轨迹球模式关了</blockquote>
感谢



*****

####  慕容断月  
##### 1954#       发表于 2022-12-2 20:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58668696&amp;ptid=2015700" target="_blank">isa2456 发表于 2022-11-28 23:04</a>

想问下tf卡怎么才能在windows上拷文件ext4格式主pc的win不能读，exfat的话steam又用不了，不可能准 ...</blockquote>
win10和11的话可以装wsl，然后挂载，win10和11可以通过这个方式原生支持ext4的读写



*****

####  LMBS  
##### 1955#       发表于 2022-12-2 23:48

好奇怪，之前机战30还能玩的，突然就不能玩了

其实重装之前就试过一次也是这样



*****

####  isa2456  
##### 1956#       发表于 2022-12-3 00:30

终于全部折腾好了<img src="https://static.saraba1st.com/image/smiley/face2017/255.png" referrerpolicy="no-referrer">玩起来感觉还是很不错的，mangohud折腾老半天，最后完全关机重启了之后就能用了，就是不知道为什么模拟器只能用ryujinx不能用yuzu，可能是装的ea版不对？



*****

####  Fuero  
##### 1957#       发表于 2022-12-3 10:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58733060&amp;ptid=2015700" target="_blank">LMBS 发表于 2022-12-2 23:48</a>

好奇怪，之前机战30还能玩的，突然就不能玩了

其实重装之前就试过一次也是这样 ...</blockquote>
试了下我机战30能玩的，proton experimental的bleeding edge分支



*****

####  eistla  
##### 1958#       发表于 2022-12-3 12:03

deck现在是不是还不能用创意工坊，以及为什么风扇老是狂转，都还没开游戏诶，吵死了

*****

####  yoyodty  
##### 1959#       发表于 2022-12-3 12:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58739117&amp;ptid=2015700" target="_blank">eistla 发表于 2022-12-3 12:03</a>

deck现在是不是还不能用创意工坊，以及为什么风扇老是狂转，都还没开游戏诶，吵死了 ...</blockquote>
可以用创意工坊啊，我环世界的mod都是在游戏模式上创意工坊打的



*****

####  安广多惠子  
##### 1960#       发表于 2022-12-3 13:34

hk终于补款了，当做给自己的圣诞礼物了，虽然25号前不一定能拿到233

—— 来自 [S1Fun](https://s1fun.koalcat.com)



*****

####  拉沃契金  
##### 1961#       发表于 2022-12-3 16:16

收到补款邮件了，香港转中可以运吗？

*****

####  leo204672099  
##### 1962#       发表于 2022-12-3 16:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58739117&amp;ptid=2015700" target="_blank">eistla 发表于 2022-12-3 12:03</a>

deck现在是不是还不能用创意工坊，以及为什么风扇老是狂转，都还没开游戏诶，吵死了 ...</blockquote>
没遇到你的情况，我机器风扇狂转情况很少，看看是不是设置的问题



*****

####  LMBS  
##### 1963#       发表于 2022-12-3 16:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58737813&amp;ptid=2015700" target="_blank">Fuero 发表于 2022-12-3 10:31</a>

试了下我机战30能玩的，proton experimental的bleeding edge分支</blockquote>
之前也是能玩的，突然就玩不了

想起还有桌面模式，切到桌面模式竟然可以玩，回到掌机又不行，真的好奇怪

*****

####  妄想中毒  
##### 1964#       发表于 2022-12-7 17:47

看楼里不少用中环的，中环运费大概多少要交税吗，转中太坑了不送我这里货到库房了还得转到其他转运公司

*****

####  恋妖壶  
##### 1965#       发表于 2022-12-7 17:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58818239&amp;ptid=2015700" target="_blank">妄想中毒 发表于 2022-12-7 17:47</a>

看楼里不少用中环的，中环运费大概多少要交税吗，转中太坑了不送我这里货到库房了还得转到其他转运公司 ...</blockquote>
中环体验太差了，不推荐，群里全是中环受害者

转中怎么还能不到你那里的，他们也是到国内转快递而已啊



*****

####  妄想中毒  
##### 1966#       发表于 2022-12-7 18:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58818292&amp;ptid=2015700" target="_blank">恋妖壶 发表于 2022-12-7 17:50</a>

中环体验太差了，不推荐，群里全是中环受害者

转中怎么还能不到你那里的，他们也是到国内转快递而已啊 ...</blockquote>
游戏机只有香港自提UPS和联邦快递3条线，我所在地址UPS和联邦都不支持打电话问了客服他们也解决不了<img src="https://static.saraba1st.com/image/smiley/face2017/163.png" referrerpolicy="no-referrer">

而且就算能发我看快递费也贵的离谱要369还没算保价，这要是过海关再交税就真的和淘宝上卖的便宜不了多少了<img src="https://static.saraba1st.com/image/smiley/face2017/163.png" referrerpolicy="no-referrer">



*****

####  世界的膀胱者  
##### 1967#       发表于 2022-12-8 00:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58819145&amp;ptid=2015700" target="_blank">妄想中毒 发表于 2022-12-7 18:38</a>
游戏机只有香港自提UPS和联邦快递3条线，我所在地址UPS和联邦都不支持打电话问了客服他们也解决不了[f:16 ...</blockquote>
FedEx基本上是必税的
实在寄不到的话寄到其他省市的朋友家然后让他转寄给你？

—— 来自 samsung SM-G9910, Android 13上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play



*****

####  ky怪  
##### 1968#       发表于 2022-12-8 01:12

现在hk和日本买的到手价和时效大概都多少？



*****

####  nozomitech  
##### 1969#       发表于 2022-12-8 05:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58739117&amp;ptid=2015700" target="_blank">eistla 发表于 2022-12-3 05:03</a>
deck现在是不是还不能用创意工坊，以及为什么风扇老是狂转，都还没开游戏诶，吵死了 ...</blockquote>
你是不是用的老风扇调度？老的感觉比较激进，APU五十几度就开始狂转，然后吹出来的是凉风。。。

—— 来自 [S1Fun](https://s1fun.koalcat.com)



*****

####  妄想中毒  
##### 1970#       发表于 2022-12-8 08:08

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58824578&amp;ptid=2015700" target="_blank">世界的膀胱者 发表于 2022-12-8 00:36</a>
FedEx基本上是必税的
实在寄不到的话寄到其他省市的朋友家然后让他转寄给你？</blockquote>
邮费加税快1000了，我这海淘本来就是图个便宜这么一搞反而更贵了，还不如换一家慢点就慢点吧

*****

####  roxassix  
##### 1971#       发表于 2022-12-16 19:24

日版开始发货了，发货顺序好像是根据付款时间来的，最快的明天能送到<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">



*****

####  nnnnick22  
##### 1972#       发表于 2022-12-16 20:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58969188&amp;ptid=2015700" target="_blank">roxassix 发表于 2022-12-16 19:24</a>
日版开始发货了，发货顺序好像是根据付款时间来的，最快的明天能送到 ...</blockquote>
发邮件了吗 我这边还是处理中12月2号付的尾款 看来还要等



*****

####  roxassix  
##### 1973#       发表于 2022-12-16 20:49

 本帖最后由 roxassix 于 2022-12-16 20:50 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58970021&amp;ptid=2015700" target="_blank">nnnnick22 发表于 2022-12-16 20:23</a>

发邮件了吗 我这边还是处理中12月2号付的尾款 看来还要等</blockquote>

Komodo没发，系统上也是显示处理中，是佐川的 smartclub先发了配送预定邮件<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

顺便我也是2号付的尾款，订单编号104xx



*****

####  nnnnick22  
##### 1974#       发表于 2022-12-17 05:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58970412&amp;ptid=2015700" target="_blank">roxassix 发表于 2022-12-16 20:49</a>
Komodo没发，系统上也是显示处理中，是佐川的 smartclub先发了配送预定邮件

顺便我也是2号付的尾 ...</blockquote>
感谢 昨晚收到邮件了 也是佐川预定今天配达 希望一切顺利



*****

####  kalavinka  
##### 1975#       发表于 2022-12-17 14:36

昨天更新系统后用指令的装的火狐不见了，重新运行指令安装也不行，有谭友知道解决方法吗<img src="https://static.saraba1st.com/image/smiley/face2017/125.png" referrerpolicy="no-referrer">



*****

####  h122h  
##### 1976#       发表于 2022-12-17 17:25

今天亚洲地区都开始发货了，是不是等一等网上价格就会下来点？



*****

####  雨中曲  
##### 1977#       发表于 2022-12-17 19:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58980751&amp;ptid=2015700" target="_blank">h122h 发表于 2022-12-17 17:25</a>
今天亚洲地区都开始发货了，是不是等一等网上价格就会下来点？</blockquote>
steam掌机价格跟哪里发售没大关系，跟steam充值卡比例强关系。得看秋促前那批卡是否真得被用去美区扫货(红锁新高峰)，又有多少货能安全到岸

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4



*****

####  医生狼多  
##### 1978#       发表于 2022-12-17 19:52

sd2出来sd估计就彻底降价了

*****

####  Litccc  
##### 1979#       发表于 2022-12-17 19:54

valve的硬件有出过二代么<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">



*****

####  bulechaos  
##### 1980#       发表于 2022-12-17 20:10

算了下自己美金卡自订+国际运费+关税也要3100+了，图方便直接淘宝或者PDD买3288的预定或者3488的现货好像也不是很亏？

有坛友推荐靠谱的店家吗，在B站看到某家叫小纯电玩爆出要你临时加钱的瓜<img src="https://static.saraba1st.com/image/smiley/face2017/125.png" referrerpolicy="no-referrer">



*****

####  nnnnick22  
##### 1981#       发表于 2022-12-18 08:47

日区总算到了 直接买了吸血鬼生还者在玩 老婆看到接近花十万日元的东西竟然拿来玩貌似二十年前的游戏直接崩溃



*****

####  时空之旅  
##### 1982#       发表于 2022-12-18 10:16

<blockquote>Litccc 发表于 2022-12-17 19:54
valve的硬件有出过二代么</blockquote>
g胖一般不会数3，所以2代板上钉钉妥妥的



*****

####  菜菜菜菜  
##### 1983#       发表于 2022-12-18 10:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58987821&amp;ptid=2015700" target="_blank">nnnnick22 发表于 2022-12-18 08:47</a>

日区总算到了 直接买了吸血鬼生还者在玩 老婆看到接近花十万日元的东西竟然拿来玩貌似二十年前的游戏直接崩 ...</blockquote>
话说我当时买也是为了这个，可以跑老头环给你老婆看看。



*****

####  李小狼  
##### 1984#       发表于 2022-12-18 11:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=58987821&amp;ptid=2015700" target="_blank">nnnnick22 发表于 2022-12-18 08:47</a>
日区总算到了 直接买了吸血鬼生还者在玩 老婆看到接近花十万日元的东西竟然拿来玩貌似二十年前的游戏直接崩 ...</blockquote>
一样，刷了掌机快一百小时了，我老婆问我这种小游戏为啥不用手机玩

—— 来自 Xiaomi MIX 2S, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4



*****

####  Fuero  
##### 1985#       发表于 2022-12-18 16:40

吸血鬼幸存者如果终局帧数会到个位数，记得在游戏设置里把性能模式打开，这样可以把终局帧数提到30-40



*****

####  Ryuji1145  
##### 1986#       发表于 2022-12-18 17:18

<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">推上看到有鬼子买SD来玩DOAXVV，好眼馋



*****

####  Sue  
##### 1987#       发表于 2022-12-18 19:27

笑死，刚刚想起来昨天发售，看了一下邮件啥通知都没

然后去看了一下推，在炎上了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer"> 

<img src="https://img.saraba1st.com/forum/202212/18/192625r758xax8z6xvbvh5.jpg" referrerpolicy="no-referrer">

<strong>IMG_20221218_192552.jpg</strong> (731.63 KB, 下载次数: 0)

下载附件

2022-12-18 19:26 上传

<img src="https://img.saraba1st.com/forum/202212/18/192625zn2xxnvq28xrtn32.jpg" referrerpolicy="no-referrer">

<strong>IMG_20221218_192608.jpg</strong> (577.58 KB, 下载次数: 0)

下载附件

2022-12-18 19:26 上传

然后看了一下日本那边，也是一片欢声笑语<img src="https://static.saraba1st.com/image/smiley/face2017/053.png" referrerpolicy="no-referrer"> 

<img src="https://img.saraba1st.com/forum/202212/18/192654z77llbn7r5jebtze.jpg" referrerpolicy="no-referrer">

<strong>IMG_20221218_191910.jpg</strong> (770.61 KB, 下载次数: 0)

下载附件

2022-12-18 19:26 上传

安心了，继续慢慢等



*****

####  褪色的雪花  
##### 1988#       发表于 2022-12-20 22:22

底座买哪个好

—— 来自 Xiaomi Mi9 Pro 5G, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play



*****

####  聚散浮云  
##### 1989#       发表于 2022-12-21 08:37

底座这玩意没啥技术含量随便买个第三方就行吧



*****

####  setree  
##### 1990#       发表于 2022-12-21 12:05

碰到个奇怪的bug问问坛友有没有解决方案
我这边在家下载完成+实际玩过的游戏，第二天重启机器后要整个游戏重新下载
还有一部分游戏卡在正在分配空间下载不下来
<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">



*****

####  安广多惠子  
##### 1991#       发表于 2022-12-22 17:39

今天终于收到了，在公司第一时间下了个杀戮尖塔试试，好爽<img src="https://static.saraba1st.com/image/smiley/face2017/045.png" referrerpolicy="no-referrer">

—— 来自 [S1Fun](https://s1fun.koalcat.com)

