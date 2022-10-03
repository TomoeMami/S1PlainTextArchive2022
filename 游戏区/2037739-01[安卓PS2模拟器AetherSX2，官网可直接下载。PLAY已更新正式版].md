

*****

####  谷恒条野  
##### 1#       楼主       发表于 2021-11-16 10:51

 本帖最后由 谷恒条野 于 2022-7-5 11:58 编辑 

=============（一）安装包+BIOS==========

官网:
[https://www.aethersx2.com/archive/](https://www.aethersx2.com/archive/)

官网里面就直接可以下载安装包了。

百度盘含BIOS,公测版更新了正式版(上架play的版本，一般相对稳定,公测各版本更新信息汇总在4L)，封测版（做内部测试的版本，一般问题较多，谨慎更新），高通专用版（Turnip版需要在高级设置中选择Turnip驱动程序才能激活驱动），贴吧做的宿命传说专用的改版：

720和之前的版本对高通的机器比较友好。

从9开头的版本开始对mali设备（麒麟、发哥）优化，而且加强了特效的模拟还原，比以前的版本也许会有所发热和卡顿，但一些热门游戏有提速。

10版本例如1018开始对mali设备（麒麟、发哥）提速较明显，虽然似乎贴图错误等问题较多，但一些热门游戏也有提速。

按需取用
[https://pan.baidu.com/s/115E2qYKXnKsYBWmAXDd4rw](https://pan.baidu.com/s/115E2qYKXnKsYBWmAXDd4rw)

yh6f

注意1：720和后面的版本的即时存档不通用，新的一些版本之间的即时存档也不通用，用普通存档方式存档后再升级吧，而且看测试说996发热比较严重，想要换成旧版本记得备份记忆卡等文件。

注意2：卸载模拟器会把记忆卡那些文件都删掉的，注意备份。

记忆卡路径：

Android/data/xyz.aethersx2.android/files/memcards/

=============（二）兼容性===============

社区维护的以太兼容性列表
[https://aethersx2-community.fandom.com/wiki/Community_maintained_Compatibility_List](https://aethersx2-community.fandom.com/wiki/Community_maintained_Compatibility_List)

碰到玩不了的游戏也可以查查pcsx2的兼容性列表，看看里面有没有大佬的设置建议参考。
[https://pcsx2.net/compatibility-list.html](https://pcsx2.net/compatibility-list.html)

或者可以看看贴吧或者B站有没有人分享模拟器怎么设置的。
[aethersx2模拟器吧](https://tieba.baidu.com/f?kw=aethersx2模拟器)

实在运行不了的只能跟作者反馈等作者修复了。

261L有新鬼武者防卡死金手指

666L有北妹兼容性金手指

=============（三）金手指使用===========

应用设置》启用金手指

金手指文件名要改成游戏的CRC名加.pnach，放在以下目录。

Android/data/xyz.aethersx2.android/files/cheats

或者在游戏中调出设置》金手指代码》添加金手指。之后自己编辑保存。

金手指参考格式：

// 金钱最大

patch=1,EE,20199664,extended,3C033000

// pp9999

patch=1,EE,201F0FE0,extended,2412270F

//击坠数999

patch=1,EE,201F12E8,extended,241203E7

可以找到一些日版金手指的网站：
[http://daihouko.com/code/ps2/](http://daihouko.com/code/ps2/)

或者直接google日文游戏名+改造コード

美版金手指网站：
[https://gamehacking.org/system/ps2](https://gamehacking.org/system/ps2)

模拟器中长按游戏封面》游戏摘要，可以看到游戏编号，根据游戏编号或者游戏名等搜索

=============（四）手柄================

作者记得用的是PS4手柄和XBOX手柄，看潭友用这2种手柄应该现在都没有啥问题了。

截至720版本：

潭友和LZ使用过的一些其他手柄信息：

（1）LZ用过的：

         wee1代：按键正常（缺个R3），休眠重连正常。价格便宜但是对现在突出的摄像头和超长的手机屏幕（裸机）都比较难卡入，卡入后也因为摄像头突出只能插入部分，要看摄像头位置。

         小鸡X2蓝牙版：按键正常，休眠重连正常。右手拉伸部分有比较大的下沉空间给摄像头，K30S戴套都能卡入。564楼的潭友也是用的这个。

         ipega 9087s：对手机卡入的兼容性基本和wee1代一样，按键正常而且有L3R3，但是休眠重连会导致模拟器重置游戏（迷之问题,中兴5元的FUN手柄和610楼潭友并夕夕买的杂牌手柄也存在相同问题）。

         八位堂lite：按键正常，休眠重连正常，方向键感觉延迟有点大，而且没有L3R3。

（2）512楼：雷蛇骑士、北通H2，但是雷蛇骑士看566楼反馈好像只适合背后摄像头在左边的，K30Pro这种背后中间的摄像头会顶住塞不进去

（3）568楼：北通G3

（4）603楼：赛太克7007F

（5）659楼：ipega PG9055

*****

####  Deay店长  
##### 2#       发表于 2021-11-16 11:28

PS2模拟器速度不是问题 ，倒是各种奇怪游戏兼容性问题和图形错误问题比较大

*****

####  gamecalo  
##### 3#       发表于 2021-11-16 11:35

 本帖最后由 gamecalo 于 2021-11-16 11:36 编辑 

超级大sb 呆萌模拟器,    我不慎买了,  但后来发现它可以读PCSX2的ps2记忆卡, 但读过之后居然就把记忆卡给加密了,  然后在呆萌玩过的记忆卡没法转到PCSX2上面去.     

简直是tmd太阴暗了!!   呆萌大sb!! 

期待新项目退出, 然后让呆萌赶紧死掉. 

*****

####  谷恒条野  
##### 4#         楼主| 发表于 2021-11-16 11:48

 本帖最后由 谷恒条野 于 2022-2-17 09:36 编辑 

 版本更新信息：

=====================================

Play alpha-1276:

* Resync with upstream.

* Fix invalid texture binding in some games (e.g. GT4).

* Fix VU0-&gt;VU1 register access in MTVU mode (Primal, Castlevania: LOI).

* Fix possible texture corruption in Vulkan when readbacks are enabled (DMC status bar).

* Add ability to bind accelerometer/gyro to guest gamepads.

* Add affinity control modes.

* Fix unreliable vsync option.

=====================================

Play alpha-1106:

* Add experimental hash based texture cache (Texture Preloading -&gt; Full).

* Fix vibration with more than one motor (Android 12+).

* Support binding a single virtual controller.

* Default automatic binding to Z/RZ instead of RX/XY.

* Fix ESADD instruction corrupting pending P (MK: Shaolin Monks).

* Rewrite/fix VU ESUM instruction (Mega Man X7 shadows).

* Add vibration frequency throttle option.

* Fix deleting &gt;1 slot in save state manager.

* Auto-disable full hash cache when it exceeds 1GB usage.

=====================================

Play alpha-1087:

* Implement vibration.

* Support Vulkan rendering without D32S8. Plenty of games will be broken and/or slow.

* Fix texture barriers still being used in some cases when disabled.

* Fix combined atest+blending (NFS Underground on Mali+Vulkan).

* Fix VU divide clobbering regs/constants (Cold Winter, Tekken 4), recompile RSQRT.

* Fix sign extension in VU double branches (Harvest Moon: STH).

* Fix FPU MUL fix (Tales of Destiny).

=====================================

Pay-alpha-1059：

* Bug fixes for Mali GPUs in both Vulkan and OpenGL renderers (tested with Pixel 6).

* Texture preloading performance improvements.

* Add memory card creation/settings/per-game overrides.

* Disable texture barriers by default on Adreno (too many broken drivers).

* Prevent Vulkan being used on old drivers which are missing required formats.

* Minor optimization to VU dispatch (~10% improvement in Ratchet).

* Fix error reporting when loading incompatible save state.

* Add save state manager.
<img src="https://bbs.saraba1st.com/2b/forum.php?mod=image&amp;aid=914248&amp;size=300x300&amp;key=5a594db331d24a9a&amp;nocache=yes&amp;type=fixnone&amp;ramdom=sMZIu" id="aimg_p2ZNI" onclick="zoom(this, this.src, 0, 0, 0)" width="300"/)

======================================

Play alpha-1021:

* Minor optimization to EE/VU recompilers (+3-5% in GoW2).

* Improve texture preloading performance.

* Improve internal frame rate detection.

* Fix mipmapping in some games (e.g. Jak 2).

* Fix auto hide controller option when starting.

* Add per-game controller bindings (via "copy controller bindings").

* Fix CRC hack option not togglable while ingame.
<img src="https://bbs.saraba1st.com/2b/forum.php?mod=image&amp;aid=913590&amp;size=300x300&amp;key=8c14ce8282c707c2&amp;nocache=yes&amp;type=fixnone&amp;ramdom=FzcqO" id="aimg_xMPZS" onclick="zoom(this, this.src, 0, 0, 0)" width="300"/)

======================================

Play alpha-996：

* OLD SAVE STATES ARE NOT COMPATIBLE WITH THIS UPDATE!

* Add controller mapping and hotkeys. Chords are supported.

* Expose more GS options.

* Support trilinear filtering and software blending in Vulkan renderer. If you have rendering glitches, disable Texture barriers in Advanced Settings.

* Fix issues when combining texture preloading and GPU palette textures.

* Non-DSB path for Vulkan renderer.

* Add aspect ratio and software renderer FMV switch.

* Fix const prop bug in recompiler.

======================================

Play alpha-720：

- Fix constant colour/alpha blending on Mali devices (e.g. Silent Hill 2).

- OpenGL performance optimizations (e.g. Burnout 3 30fps -&gt; 45fps at 3x on 870).

- Fix depth copies/readbacks in OpenGL (e.g. SMT Nocturne).

- Minor rendering fix for Vulkan in some games (e.g. Xenosaga).

- Fix Traditional Chinese in language selector.

======================================

Play alpha-702:

- Prevent Vulkan renderer being used on Mali devices.

- Fix OpenGL rendering on Pixel 6 and other newer Mali drivers.

- Implement full FPU mode (needed for NFS Carbon and other games).

- Tiny optimization to VU flags calculation.

- Fix emitting invalid instructions (NFS Carbon, possibly others).

- Fix crash when activating some overdrives in FFX with the Vulkan renderer.

- Fix vibrate on touch for dpad.

- Switch back to AAudio from oboe.

- Stop audio output on pause (reduce idle battery usage).

======================================

Play alpha-678:

Disable bundle splitting for languages (allows any language selection post install).

Fix possible crash in Vulkan when texture preloading is on and large textures are used.

Correct rounding mode for float-&gt;int conversion (fixes water elevators in FFX).

Fix incorrect VU0 status flags in COP2 mode.

Add console-accurate FPU add/sub instructions (fixes location text in P4).

Add option for using brake/gas axes (needed for L2/R2 on some devices).

Add translations.

======================================

Play alpha-669:

Improve frame pacing in skip duplicate frames option.

Recompile BLTZAL/BLTZALL, swap delay slot in BGEZAL.

Fix a couple of VU bugs - Persona 4  PAL, Tony Hawk's Downhill Jam.

Fix possible crash when opening pause menu. 

Add internal frame rate detection and skip duplicate frames option.
<img src="https://bbs.saraba1st.com/2b/forum.php?mod=image&amp;aid=905352&amp;size=300x300&amp;key=2fac2c7b43a5eb8c&amp;nocache=yes&amp;type=fixnone&amp;ramdom=vBeub" id="aimg_OSQQO" onclick="zoom(this, this.src, 0, 0, 0)" width="300"/)
<img src="https://bbs.saraba1st.com/2b/forum.php?mod=image&amp;aid=905353&amp;size=300x300&amp;key=5661d27c0590f2ac&amp;nocache=yes&amp;type=fixnone&amp;ramdom=JhXh5" id="aimg_c7k24" onclick="zoom(this, this.src, 0, 0, 0)" width="300"/)

======================================

Play alpha-662:

Crash fix for Burnout 2/NBA 2k12, probably others.

Expose more GS settings.

Extract strings for translatability.

*****

####  whzfjk  
##### 5#       发表于 2021-11-16 11:50

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  whzfjk  
##### 6#       发表于 2021-11-16 11:52

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  彩虹肥宅  
##### 7#       发表于 2021-11-16 11:54

gkd！

*****

####  路西恩  
##### 8#       发表于 2021-11-16 13:10

开发呆萌的那一帮子估计全是司马呆笔

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  tclm  
##### 9#       发表于 2021-11-16 15:07

呆萌感觉还是太吃资源了，我用matepad11还是跑不溜

*****

####  walfeds  
##### 10#       发表于 2021-11-16 15:16

好，呆萌的末日到了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  JimmyZ  
##### 11#       发表于 2021-11-16 15:57

PS2上也没啥想补的游戏了

*****

####  gogoneogg  
##### 12#       发表于 2021-11-16 16:04

关键是用手机怎么操作那么多键位<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  梦窗  
##### 13#       发表于 2021-11-16 16:06

PC上的来个大神重做一下啊。

*****

####  JimmyZ  
##### 14#       发表于 2021-11-16 16:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53562848&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-11-16 11:48</a>

小道消息说duckstation作者还有ppsspp的2个开发者都在开发团队里，到时出了等兼容列表看看。这呆萌好像4年 ...</blockquote>
大道消息，我去duckstation discord里问了，扯jb蛋。

*****

####  中发白一副好牌  
##### 15#       发表于 2021-11-16 16:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53566296&amp;ptid=2037739" target="_blank">gogoneogg 发表于 2021-11-16 16:04</a>

关键是用手机怎么操作那么多键位</blockquote>
挂个拉伸手柄或者直接投屏用蓝牙手柄玩~

*****

####  shqingda_  
##### 16#       发表于 2021-11-16 16:55

好，干死呆萌

*****

####  JimmyZ  
##### 17#       发表于 2021-11-16 17:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53566380&amp;ptid=2037739" target="_blank">JimmyZ 发表于 2021-11-16 16:09</a>

大道消息，我去duckstation discord里问了，扯jb蛋。</blockquote>
说个笑话, 因为我去问这个事, Stenzek说我散布谣言, 把我ban了.

*****

####  Suzutsuki.Mk.II  
##### 18#       发表于 2021-11-16 17:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53567272&amp;ptid=2037739" target="_blank">JimmyZ 发表于 2021-11-16 17:06</a>

说个笑话, 因为我去问这个事, Stenzek说我散布谣言, 把我ban了.</blockquote>
可能因为之前被呆萌那群人骚扰恶心到了，不打算明面搞，你恰好成了牺牲品<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  ercai1  
##### 19#       发表于 2021-11-16 17:30

不管最后要花多久，只要能恶心到呆萌那个傻逼就是个大好事<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">

*****

####  谷恒条野  
##### 20#         楼主| 发表于 2021-11-16 17:32

 本帖最后由 谷恒条野 于 2021-11-16 17:59 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53567272&amp;ptid=2037739" target="_blank">JimmyZ 发表于 2021-11-16 17:06</a>

说个笑话, 因为我去问这个事, Stenzek说我散布谣言, 把我ban了.</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">

然后现在这个处于“无人认领”状态<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  samchen007  
##### 21#       发表于 2021-11-16 17:59

我问个可能会被人鄙视的问题，都说呆萌偷代码，那为什么PLAY STORE不下架呢？

*****

####  精钢魔像  
##### 22#       发表于 2021-11-16 18:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53568089&amp;ptid=2037739" target="_blank">samchen007 发表于 2021-11-16 17:59</a>

我问个可能会被人鄙视的问题，都说呆萌偷代码，那为什么PLAY STORE不下架呢？ ...</blockquote>
开源协议能商用就没事

*****

####  JimmyZ  
##### 23#       发表于 2021-11-16 18:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53568145&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-11-16 18:04</a>

开源协议能商用就没事</blockquote>
PCSX2是GPL的, 真正原因是人家闭源, 所以没有实锤.

*****

####  飞侠小黑  
##### 24#       发表于 2021-11-16 18:40

呆萌本来就是个骗钱玩意，好几年了兼容性流畅性几乎没有提升<img src="https://static.saraba1st.com/image/smiley/face2017/176.png" referrerpolicy="no-referrer">

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  lbzlxx  
##### 25#       发表于 2021-11-16 18:53

所以呆萌究竟是不是pcsx2改版？我没用过，我只知道当初制作组到处辟谣，也没实锤，现在用户到处喊升级只是升版本号<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">

*****

####  nozomitech  
##### 26#       发表于 2021-11-16 19:11

多半呆萌2

*****

####  JudgmentEye  
##### 27#       发表于 2021-11-16 19:55

<blockquote>引用第24楼lbzlxx于2021-11-16 18:53发表的  :

所以呆萌究竟是不是pcsx2改版？我没用过，我只知道当初制作组到处辟谣，也没实锤，现在用户到处喊升级......</blockquote>
旧版直接搜pcsx字符串16进制能搜出来一堆，新版加密了不知道

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  谷恒条野  
##### 28#         楼主| 发表于 2021-11-18 19:23

<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">更新了正式名称，而且据说已经给谷歌上架审核了，越来越期待了。

*****

####  暗之星尘  
##### 29#       发表于 2021-11-18 19:53

<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">米板5多了新用途了

*****

####  精钢魔像  
##### 30#       发表于 2021-11-18 20:00

双11 1550买的摩托罗拉 edge s 真值



*****

####  shellte  
##### 31#       发表于 2021-11-18 20:29

就为了能在手机上玩武神0，等这么久也值得了。

*****

####  双刀少女  
##### 32#       发表于 2021-11-18 20:32

希望870能有好的体验

*****

####  彩虹肥宅  
##### 33#       发表于 2021-11-18 22:29

[https://youtu.be/jakIupKQNlI](https://youtu.be/jakIupKQNlI)

性能测试

*****

####  walfeds  
##### 34#       发表于 2021-11-18 22:32

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">好，支持正义处刑

就是不知道855能不能带的动

*****

####  alexwu  
##### 35#       发表于 2021-11-18 23:35

喷了，战神用的汉化版iso

另外食蛇者和旺达是真的吃机能啊

*****

####  lbzlxx  
##### 36#       发表于 2021-11-18 23:48

看这FA，一上来就有vulkan了，那应该挺成熟了，如果到时能反向发展到PC平台就好了

*****

####  allenz3  
##### 37#       发表于 2021-11-19 00:18

看测试视频845尚可，870就挺好的，就是不知道870的安卓掌机猴年马月才有人搞了

*****

####  afer  
##### 38#       发表于 2021-11-19 00:30

日死呆萌

*****

####  轩辕无  
##### 39#       发表于 2021-11-19 02:04

这模拟器能解决机战系列黑线问题和图像放大不能问题哪就神了

*****

####  weiyun  
##### 40#       发表于 2021-11-19 05:41

<blockquote>梦窗 发表于 2021-11-16 16:06
PC上的来个大神重做一下啊。</blockquote>
这个应该也是基于pc的

*****

####  幽灵胖胖  
##### 41#       发表于 2021-11-19 06:02

看来能让我补完OGS和外传了，顺带阿花2和阿花3，期待

*****

####  桧山修之  
##### 42#       发表于 2021-11-19 07:20

我的865不知能不能玩

*****

####  tclm  
##### 43#       发表于 2021-11-19 08:11

希望865能玩

*****

####  RockingHorse  
##### 44#       发表于 2021-11-19 08:26

那到时候是不是可以用win11的安卓模拟器运行安卓的ps2模拟器

*****

####  路西恩  
##### 45#       发表于 2021-11-19 08:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53604842&amp;ptid=2037739" target="_blank">RockingHorse 发表于 2021-11-19 08:26</a>
那到时候是不是可以用win11的安卓模拟器运行安卓的ps2模拟器</blockquote>
套娃不可取啊<img src="https://static.saraba1st.com/image/smiley/face2017/034.png" referrerpolicy="no-referrer">

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  梦窗  
##### 46#       发表于 2021-11-19 08:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53604351&amp;ptid=2037739" target="_blank">weiyun 发表于 2021-11-19 05:41</a>
这个应该也是基于pc的</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/105.png" referrerpolicy="no-referrer">没见哪说有PC端啊。

*****

####  古畑任三郎2015  
##### 47#       发表于 2021-11-19 08:58

980不知道行不行

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  格林达姆  
##### 48#       发表于 2021-11-19 09:12

save more than one state
拯救不止一个州<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  UCXCU  
##### 49#       发表于 2021-11-19 10:06

说起来为什么感觉安卓平台开发的模拟器能效比win系统的平台上的好？比如这个ps2模拟器去年下了那个画风复古的模拟器，性能开销居然很大，而且图像错误也不少，同理的nds模拟器也是，安卓那个激烈模拟器和win平台的nds模拟器效能比完全不一样

*****

####  yan38324  
##### 50#       发表于 2021-11-19 10:41

虽然我也买了呆萌 但还是希望早死早超生<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer"> 说的话跟放屁一样 成天挖坑画大饼

*****

####  yan38324  
##### 51#       发表于 2021-11-19 10:43

希望888能玩 不要跑一会就热的掉帧了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  古畑任三郎2015  
##### 52#       发表于 2021-11-19 12:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53605973&amp;ptid=2037739" target="_blank">UCXCU 发表于 2021-11-19 10:06</a>
说起来为什么感觉安卓平台开发的模拟器能效比win系统的平台上的好？比如这个ps2模拟器去年下了那个画风复古 ...</blockquote>
应该只有drastic特别厉害吧，或者说是pc上的nds模拟器太拉了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  精钢魔像  
##### 53#       发表于 2021-11-19 13:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53605973&amp;ptid=2037739" target="_blank">UCXCU 发表于 2021-11-19 10:06</a>

说起来为什么感觉安卓平台开发的模拟器能效比win系统的平台上的好？比如这个ps2模拟器去年下了那个画风复古 ...</blockquote>
掌机都是arm，而且老任传统用的都是过时处理器

wiiu和ps3的模拟，安卓就不行了

*****

####  哼哈二将  
##### 54#       发表于 2021-11-19 14:30

买了个呆萌，玩了几分钟的CVS2感觉还可以的。几十块钱，无所谓的。

当然有竞争更好啦。看看新版对修改器的支持咋样，老游戏没有修改器真是玩不下去

*****

####  有点追求  
##### 55#       发表于 2021-11-19 14:31

求一个泪指环的改版，就熟练度别这么难升级就好

*****

####  卡普空  
##### 56#       发表于 2021-11-19 14:42

等一个麒麟<img src="https://static.saraba1st.com/image/smiley/face2017/074.png" referrerpolicy="no-referrer">9000的评测

*****

####  JimmyZ  
##### 57#       发表于 2021-11-19 15:11

这个也(会)是开源的, 还是LGPL, damon第二天就抄好了, 妥妥儿的

*****

####  UCXCU  
##### 58#       发表于 2021-11-19 18:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53607835&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-11-19 12:55</a>
应该只有drastic特别厉害吧，或者说是pc上的nds模拟器太拉了

—— 来自 S1Fun ...</blockquote>
主要是之前尝试了下pc上的nds模拟器，没想到模拟效率这么低，连用个滤镜都可以造成音频延迟爆炸

*****

####  alexwu  
##### 59#       发表于 2021-11-19 20:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53612426&amp;ptid=2037739" target="_blank">UCXCU 发表于 2021-11-19 18:21</a>

主要是之前尝试了下pc上的nds模拟器，没想到模拟效率这么低，连用个滤镜都可以造成音频延迟爆炸 ...</blockquote>
[https://ci.appveyor.com/project/zeromus/desmume/build/artifacts](https://ci.appveyor.com/project/zeromus/desmume/build/artifacts)

一直用desmume挺好的啊，如果你用的也是这个，能说一下怎么设滤镜的吗，我试试复现

*****

####  罐子  
##### 60#       发表于 2021-11-19 21:20

机战a3的头像问题能解决不？<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2



*****

####  RaidenII  
##### 61#       发表于 2021-11-19 21:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53612426&amp;ptid=2037739" target="_blank">UCXCU 发表于 2021-11-19 05:21</a>
主要是之前尝试了下pc上的nds模拟器，没想到模拟效率这么低，连用个滤镜都可以造成音频延迟爆炸 ...</blockquote>
melonds可以尝试一下

*****

####  轩辕无  
##### 62#       发表于 2021-11-19 22:45

melonds模拟虽然效率高但是不知道为啥PM之类会有图像错位

*****

####  jellyfis  
##### 63#       发表于 2021-11-19 23:06

司马的呆萌ppsspp贴吧嚯嚯了，现在整个贴吧成了他一个人自娱自乐的地方

*****

####  两个路人  
##### 64#       发表于 2021-11-19 23:11

<blockquote>精钢魔像 发表于 2021-11-18 20:00
双11 1550买的摩托罗拉 edge s 真值</blockquote>
亚美咯～ 地猫买家亏得慌 😩

*****

####  谷恒条野  
##### 65#         楼主| 发表于 2021-11-19 23:23

 本帖最后由 谷恒条野 于 2021-11-20 11:41 编辑 

更新了几个测试视频
古惑狼
Crash Twinsanity on OnePlus 6 (SD845)
[https://www.youtube.com/watch?v=n5ez-zl-jFU](https://www.youtube.com/watch?v=n5ez-zl-jFU)
[https://www.bilibili.com/video/BV17g411N7F8](https://www.bilibili.com/video/BV17g411N7F8)

铁拳
Tekken 5 with upscaling (Poco F3, SD870)
[https://www.youtube.com/watch?v=Xmgew02QTng](https://www.youtube.com/watch?v=Xmgew02QTng)
[https://www.bilibili.com/video/BV1Sq4y1679C](https://www.bilibili.com/video/BV1Sq4y1679C)

P3FES
Persona 3 FES (Xiaomi Mi A1, SD625 @ 3.1GHz)
[https://www.youtube.com/watch?v=-7HKHQm3RQY](https://www.youtube.com/watch?v=-7HKHQm3RQY)
[https://www.bilibili.com/video/BV1D34y1d7Z8](https://www.bilibili.com/video/BV1D34y1d7Z8)

—— 来自 Hisense HLTE730T, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  UCXCU  
##### 66#       发表于 2021-11-19 23:30

 本帖最后由 UCXCU 于 2021-11-20 00:10 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53614511&amp;ptid=2037739" target="_blank">alexwu 发表于 2021-11-19 20:28</a>
[https://ci.appveyor.com/project/zeromus/desmume/build/artifacts](https://ci.appveyor.com/project/zeromus/desmume/build/artifacts)

一直用desmume挺好的啊，如果你用的 ...</blockquote>
折腾了一下，把音频设置里默认的同步改成传统就正常了

屏幕截图 2021-11-19 234519.png
(59.27 KB, 下载次数: 0)

下载附件

2021-11-19 23:46 上传

<img src="https://img.saraba1st.com/forum/202111/19/234618ojkskmli1spo4zks.png" referrerpolicy="no-referrer">

*****

####  升职加薪  
##### 67#       发表于 2021-11-19 23:46

呆萌和他那模拟器一看就是个司马货色

怎么还会想去付费

*****

####  彩虹肥宅  
##### 68#       发表于 2021-11-19 23:47

我还没到的安卓掌机，真正的成为了模拟神器<img src="https://static.saraba1st.com/image/smiley/face2017/045.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  highsky  
##### 69#       发表于 2021-11-20 08:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53617087&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-11-19 23:47</a>

我还没到的安卓掌机，真正的成为了模拟神器

—— 来自 Xiaomi MI 6, Android 9上的 S1Next-鹅版 v2 ...</blockquote>
哪个？

沙雕2.5还是奥丁？<img src="https://static.saraba1st.com/image/smiley/face2017/048.png" referrerpolicy="no-referrer">

*****

####  彩虹肥宅  
##### 70#       发表于 2021-11-20 08:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53619097&amp;ptid=2037739" target="_blank">highsky 发表于 2021-11-20 08:15</a>
哪个？

沙雕2.5还是奥丁？</blockquote>
奥丁<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  highsky  
##### 71#       发表于 2021-11-20 10:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53619180&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-11-20 08:36</a>

奥丁

—— 来自 Xiaomi MI 6, Android 9上的 S1Next-鹅版 v2.5.2</blockquote>
同，我845和d900各订了一台

*****

####  彩虹肥宅  
##### 72#       发表于 2021-11-20 10:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53619732&amp;ptid=2037739" target="_blank">highsky 发表于 2021-11-20 10:09</a>

同，我845和d900各订了一台</blockquote>
可惜发货时间延迟到了12月15号。<img src="https://static.saraba1st.com/image/smiley/face2017/090.png" referrerpolicy="no-referrer">

*****

####  highsky  
##### 73#       发表于 2021-11-20 12:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53619774&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-11-20 10:15</a>

可惜发货时间延迟到了12月15号。</blockquote>
15号都悬，看他们进度，我感觉元旦前能发出来已经很不错了

*****

####  谷恒条野  
##### 74#         楼主| 发表于 2021-11-20 12:05

 本帖最后由 谷恒条野 于 2021-11-20 12:09 编辑 

给她爱
GTA: Vice City Stories (Xiaomi Mi A1, SD625 @ 3.1GHz)
[https://www.youtube.com/watch?v=cjd_M3LeTBs](https://www.youtube.com/watch?v=cjd_M3LeTBs)
[https://www.bilibili.com/video/BV1FF411a7HA/](https://www.bilibili.com/video/BV1FF411a7HA/)

MGS3(Xiaomi Mi A1, SD625 @ 3.1GHz)
[https://www.youtube.com/watch?v=CcduUiG1aQU](https://www.youtube.com/watch?v=CcduUiG1aQU)
[https://www.bilibili.com/video/BV1sq4y167iX](https://www.bilibili.com/video/BV1sq4y167iX)

*****

####  平井姨夫  
##### 75#       发表于 2021-11-20 12:15

845感觉比较悬，怎么也得865吧？

*****

####  mooerfoes  
##### 76#       发表于 2021-11-20 12:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53616505&amp;ptid=2037739" target="_blank">jellyfis 发表于 2021-11-19 23:06</a>

司马的呆萌ppsspp贴吧嚯嚯了，现在整个贴吧成了他一个人自娱自乐的地方</blockquote>
不懂就问，现在呆萌在贴吧是什么情况？很久没去了不知道咋样了

*****

####  ogloc  
##### 77#       发表于 2021-11-20 12:36

之前用呆萌玩OGS，老手机835，只有20几帧，卡的一逼，希望新的模拟器能全速玩机战

*****

####  保科智子  
##### 78#       发表于 2021-11-20 16:26

好！效果优秀的话就彻底抛弃ios手机家里平板都换安卓了。<img src="https://static.saraba1st.com/image/smiley/face2017/025.png" referrerpolicy="no-referrer">

*****

####  幽灵胖胖  
##### 79#       发表于 2021-11-25 09:29

跃跃欲试了，UP主又更新了很多游戏运行效果，这2021年我一刻都不想呆了

*****

####  梦窗  
##### 80#       发表于 2021-11-27 01:16

<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">擦，还是PCSX2。
[https://pcsx2.net/301-aethersx2-pcsx2-mobile.html](https://pcsx2.net/301-aethersx2-pcsx2-mobile.html)

*****

####  岬开斗  
##### 81#       发表于 2021-11-27 05:35

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  GOUKI1981  
##### 82#       发表于 2021-11-27 10:07

狗萌把这个模拟器的贴吧也注册了，估计也要像ppsspp一样搞的乌烟瘴气了

*****

####  彩虹肥宅  
##### 83#       发表于 2021-11-27 10:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53718721&amp;ptid=2037739" target="_blank">GOUKI1981 发表于 2021-11-27 10:07</a>

狗萌把这个模拟器的贴吧也注册了，估计也要像ppsspp一样搞的乌烟瘴气了</blockquote>
去aethersx2模拟器吧，这个吧可以随意骂呆萌

*****

####  有口皆悲  
##### 84#       发表于 2021-11-27 10:32

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  谷恒条野  
##### 85#         楼主| 发表于 2021-11-27 10:45

 本帖最后由 谷恒条野 于 2021-11-27 12:10 编辑 

测试和相关信息视频一般这个up都会搬
[https://space.bilibili.com/420760099](https://space.bilibili.com/420760099)

贴吧：aethersx2模拟器吧(aethersx2吧被狗萌的人占了)
[aethersx2模拟器吧](https://tieba.baidu.com/f?kw=aethersx2模拟器)

reddit社区
[https://www.reddit.com/r/AetherSX2/](https://www.reddit.com/r/AetherSX2/)

======================================
现在油管上出现一些为了骗点击的假测试视频，一般官方的都是不带水印的，而且有不知真假的视频被狗萌的人拿来对比狗萌模拟器说这里那里的贴图错误穿模跟狗萌一样(是假的话人是用pcsx2录的，真的话新模拟器也是pcsx2分支，狗萌能出一模一样的错误说明啥也不用多说了吧)。
然后github有人占了Aethersx2名发个假Aethersx2模拟器让人下，实际是狗萌皮角版，很难不让人联想。

*****

####  lbzlxx  
##### 86#       发表于 2021-11-27 11:14

貌似对天机的相性比较好，火龙的表现相对差一点

战神一直是模拟器难度的标杆，看这游戏的效率大概就知道这模拟器的需求，骁龙870 全程56-60帧，基本算是满速了，845应该足以应付绝大部分的游戏了

*****

####  mcfly  
##### 87#       发表于 2021-11-27 12:56

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  mcfly  
##### 88#       发表于 2021-11-27 12:56

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  谷恒条野  
##### 89#         楼主| 发表于 2021-11-28 17:35

预计12月4日公测，在reddit上放出了discord讨论组。
[https://www.reddit.com/r/AetherS ... ity_discord_server/](https://www.reddit.com/r/AetherSX2/comments/r3z6o3/aethersx2_community_discord_server/)

<img src="https://img.saraba1st.com/forum/202111/28/173453pgu14040co3gw13u.png" referrerpolicy="no-referrer">

<strong>OT.png</strong> (37.07 KB, 下载次数: 0)

下载附件

2021-11-28 17:34 上传

公测discord讨论组
[https://discord.com/invite/JZ7BkeEdrJ](https://discord.com/invite/JZ7BkeEdrJ)

*****

####  保科智子  
##### 90#       发表于 2021-11-28 22:44

翻出一个660的小米应该能跑大部分，但是屏幕排线可能坏了有黑线。<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

安卓掌机给力点啊！<img src="https://static.saraba1st.com/image/smiley/face2017/034.png" referrerpolicy="no-referrer">



*****

####  妖妖忍  
##### 91#       发表于 2021-11-28 22:51

好 枪毙呆萌

*****

####  谷恒条野  
##### 92#         楼主| 发表于 2021-12-2 20:43

 本帖最后由 谷恒条野 于 2021-12-2 21:19 编辑 

[https://www.bilibili.com/video/BV1LF41187rD](https://www.bilibili.com/video/BV1LF41187rD)
放出了第二次内测视频,是拿LG G8X 骁龙855测的
估计这边5号周日这样就能看到实际表现了，也没几天了。<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">

*****

####  zjoi  
##### 93#       发表于 2021-12-2 21:01

话说PS2模拟器不是连PC端都没完全搞定吗。。

还能出手机版了？

*****

####  bonnwang  
##### 94#       发表于 2021-12-2 22:34

990不知道行不行

*****

####  bighand3714  
##### 95#       发表于 2021-12-2 23:08

有种当年等Drastic的感觉了，期待啊期待

*****

####  谷恒条野  
##### 96#         楼主| 发表于 2021-12-3 10:13

 本帖最后由 谷恒条野 于 2021-12-3 12:07 编辑 

作者早上说已提交谷歌审核，等待通过，通过时间要看谷歌了。

<img src="https://img.saraba1st.com/forum/202112/03/110104r5gyzlvkjff0gllb.png" referrerpolicy="no-referrer">

<strong>51.png</strong> (21.79 KB, 下载次数: 0)

下载附件

2021-12-3 11:01 上传

<img src="https://img.saraba1st.com/forum/202112/03/101326rpb66p0isppbpipx.png" referrerpolicy="no-referrer">

<strong>1.png</strong> (10.42 KB, 下载次数: 0)

下载附件

2021-12-3 10:13 上传

<img src="https://img.saraba1st.com/forum/202112/03/102946h5m57h7t172bp5tb.png" referrerpolicy="no-referrer">

<strong>31.png</strong> (6.51 KB, 下载次数: 0)

下载附件

2021-12-3 10:29 上传

<img src="https://img.saraba1st.com/forum/202112/03/120718wopm5ov75lvp52pu.png" referrerpolicy="no-referrer">

<strong>61.png</strong> (11.86 KB, 下载次数: 0)

下载附件

2021-12-3 12:07 上传

测试者：

<img src="https://img.saraba1st.com/forum/202112/03/103013zeezotf7xszys9ny.png" referrerpolicy="no-referrer">

<strong>41.png</strong> (30.45 KB, 下载次数: 0)

下载附件

2021-12-3 10:30 上传

*****

####  tclm  
##### 97#       发表于 2021-12-3 10:16

没有谷歌就不能玩了吗……

*****

####  杉田悠一  
##### 98#       发表于 2021-12-3 10:17

我终于可以绕过那个死妈软件在手机上重温ogs了吗，好耶

*****

####  yan38324  
##### 99#       发表于 2021-12-3 10:32

md呆萌退钱<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  筒井彩芽  
##### 100#       发表于 2021-12-3 10:32

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">看着不错，该买个870了

*****

####  保科智子  
##### 101#       发表于 2021-12-3 10:41

还有16比9的手机可以收吗？现在拉伸手柄好像都避免覆盖手机上，弄的又长又不稳定。<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  Xenor  
##### 102#       发表于 2021-12-3 12:35

3ds/wii太占空间，在加上ps2要格式不能压缩的话64g也不够用了…还有电池也是，大概率平均不到1分钟掉电1%的速度<img src="https://static.saraba1st.com/image/smiley/face2017/100.png" referrerpolicy="no-referrer">虽然可能是想太多

*****

####  慕容断月  
##### 103#       发表于 2021-12-3 12:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53794227&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-3 12:35</a>
3ds/wii太占空间，在加上ps2要格式不能压缩的话64g也不够用了…还有电池也是，大概率平均不到1分钟掉电1%的 ...</blockquote>
如果是基于最新版pcsx2多半支持chd格式，一部分游戏可以压缩的很小

*****

####  矢量路比  
##### 104#       发表于 2021-12-3 12:39

14:9 的最后一代 Android 旗舰应该停留在 835 时代了吧

*****

####  Suljo  
##### 105#       发表于 2021-12-3 13:57

不知道新鬼还会不会花屏

*****

####  PYY  
##### 106#       发表于 2021-12-3 14:27

拷了个α2汉化版和北妹2汉化版到手机，
小米11u，就等模拟器了。

[  -- 来自 能看大图的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  棺材叔叔  
##### 107#       发表于 2021-12-3 14:56

<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

*****

####  lyt77777  
##### 108#       发表于 2021-12-3 15:08

限制安卓玩PS2的只有一个问题，空间。

这年头的安卓机器都不给插扩展卡了，你能放的ISO是非常少的…………

*****

####  医生狼多  
##### 109#       发表于 2021-12-3 15:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53795906&amp;ptid=2037739" target="_blank">棺材叔叔 发表于 2021-12-3 14:56</a>
何必等安卓版呢，买个靠谱田板，苏菲pro3级别就足够模拟大部分ps2游戏了，等等，你们不是想搓玻璃玩 ...</blockquote>
当然是外接手柄啊
pro3那重量能拿手里玩吗<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  Lilithy  
##### 110#       发表于 2021-12-3 15:33

今晚上能过审不<img src="https://static.saraba1st.com/image/smiley/face2017/056.gif" referrerpolicy="no-referrer">

----发送自 [HUAWEI PCT-AL10,Android 10](http://stage1.5j4m.com/?1.37)

*****

####  Jumbohard  
##### 111#       发表于 2021-12-3 16:43

 本帖最后由 Jumbohard 于 2021-12-3 16:51 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53795906&amp;ptid=2037739" target="_blank">棺材叔叔 发表于 2021-12-3 14:56</a>
何必等安卓版呢，买个靠谱田板，苏菲pro3级别就足够模拟大部分ps2游戏了，等等，你们不是想搓玻璃玩 ...</blockquote>
说起田板，我有个19款的matebook e用的是arm处理器，印象中好像pcsx2有原生ARM版来着？

—— 来自 OnePlus LE2100, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  Suzutsuki.Mk.II  
##### 112#       发表于 2021-12-3 17:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53795193&amp;ptid=2037739" target="_blank">Suljo 发表于 2021-12-3 13:57</a>

不知道新鬼还会不会花屏</blockquote>
必然会，不用想了

*****

####  Suzutsuki.Mk.II  
##### 113#       发表于 2021-12-3 17:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53797380&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-3 16:43</a>

说起田板，我有个19款的matebook e用的是arm处理器，印象中好像pcsx2有原生ARM版来着？

—— 来自 OnePl ...</blockquote>
没有，甚至主要维护都好像是win为主

*****

####  Jumbohard  
##### 114#       发表于 2021-12-3 18:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53798140&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2021-12-3 17:51</a>
没有，甚至主要维护都好像是win为主</blockquote>
行，谢谢，那我回去看看x86转译效果如何吧<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

—— 来自 OnePlus LE2100, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  希德尼娅  
##### 115#       发表于 2021-12-3 19:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53795906&amp;ptid=2037739" target="_blank">棺材叔叔 发表于 2021-12-3 14:56</a>

何必等安卓版呢，买个靠谱田板，苏菲pro3级别就足够模拟大部分ps2游戏了，等等，你们不是想搓玻璃玩 ...</blockquote>
手机上插个拉伸手柄多大事啊

*****

####  JimmyZ  
##### 116#       发表于 2021-12-3 20:20

[https://www.youtube.com/watch?v=UTrOGS8R6Xg](https://www.youtube.com/watch?v=UTrOGS8R6Xg)

看着不错, 就是想不起来PS2还有啥要玩.

*****

####  JimmyZ  
##### 117#       发表于 2021-12-3 20:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53798504&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-3 18:22</a>

行，谢谢，那我回去看看x86转译效果如何吧

—— 来自 OnePlus LE2100, Android 11上的 S1Next-鹅 ...</blockquote>
这应该好不了, 转译应该不可能用recompiler只能用interpreter, 性能完蛋.

*****

####  神道设教  
##### 118#       发表于 2021-12-3 20:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53796049&amp;ptid=2037739" target="_blank">lyt77777 发表于 2021-12-3 15:08</a>
限制安卓玩PS2的只有一个问题，空间。

这年头的安卓机器都不给插扩展卡了，你能放的ISO是非常少的………… ...</blockquote>
确实我目前手上能插卡的手机是红米9，g80根本带不起。至于手上其他的845 865的手机太“高端”了，根本插不了卡<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  彩虹肥宅  
##### 119#       发表于 2021-12-3 20:47

我小米6下了鬼泣5还有gt4来测试模拟器<img src="https://static.saraba1st.com/image/smiley/face2017/065.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  精钢魔像  
##### 120#       发表于 2021-12-3 20:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53799918&amp;ptid=2037739" target="_blank">神道设教 发表于 2021-12-3 20:46</a>

确实我目前手上能插卡的手机是红米9，g80根本带不起。至于手上其他的845 865的手机太“高端”了，根本插 ...</blockquote>
要不要来个摩托 edge s



*****

####  古畑任三郎2015  
##### 121#       发表于 2021-12-3 20:57

m6搭配512gtf卡，可以多放点rom试试

*****

####  Jumbohard  
##### 122#       发表于 2021-12-4 07:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53799624&amp;ptid=2037739" target="_blank">JimmyZ 发表于 2021-12-3 20:26</a>
这应该好不了, 转译应该不可能用recompiler只能用interpreter, 性能完蛋.</blockquote>
我表述有误<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">应该是说在Windows的x86模拟下性能咋样

—— 来自 OnePlus LE2100, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  back57992  
##### 123#       发表于 2021-12-4 09:34

好哦 可以补下前线任务2作了

*****

####  JimmyZ  
##### 124#       发表于 2021-12-4 09:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53802969&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-4 07:55</a>

我表述有误应该是说在Windows的x86模拟下性能咋样

—— 来自 OnePlus LE2100, Android 11上的 S1 ...</blockquote>
你是说在arm windows上模拟跑x86版的pcsx2吧，没错我说的就是这。

*****

####  谷恒条野  
##### 125#         楼主| 发表于 2021-12-4 11:24

审核通过，等上架

<img src="https://img.saraba1st.com/forum/202112/04/112442vr1mkmfk6o1kmruo.png" referrerpolicy="no-referrer">

<strong>unknown.png</strong> (18.19 KB, 下载次数: 0)

下载附件

2021-12-4 11:24 上传

*****

####  谷恒条野  
##### 126#         楼主| 发表于 2021-12-4 11:36

 本帖最后由 谷恒条野 于 2021-12-4 11:38 编辑 

上架了
[https://play.google.com/apps/testing/xyz.aethersx2.android/join](https://play.google.com/apps/testing/xyz.aethersx2.android/join)

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| kirito_wst| + 1|感谢|

查看全部评分

*****

####  彩虹肥宅  
##### 127#       发表于 2021-12-4 11:37

为什么我搜不到<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  lighttt  
##### 128#       发表于 2021-12-4 11:43

不知道华为效果咋样

*****

####  暗之星尘  
##### 129#       发表于 2021-12-4 11:49

<img src="https://static.saraba1st.com/image/smiley/animal2017/008.png" referrerpolicy="no-referrer">有用米板5试下效果吗

*****

####  fmchar  
##### 130#       发表于 2021-12-4 11:55

3d这么流畅，花3、bws这种2d的应该没什么问题吧？

*****

####  kirito_wst  
##### 131#       发表于 2021-12-4 11:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804591&amp;ptid=2037739" target="_blank">fmchar 发表于 2021-12-4 11:55</a>
3d这么流畅，花3、bws这种2d的应该没什么问题吧？</blockquote>
试了花2，爆杀呆萌5.0<img src="https://static.saraba1st.com/image/smiley/face2017/049.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  DaveZED  
##### 132#       发表于 2021-12-4 11:58

问一下上哪里能下到iso，感觉网上好多都是沾点广告的<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  fmchar  
##### 133#       发表于 2021-12-4 11:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804615&amp;ptid=2037739" target="_blank">kirito_wst 发表于 2021-12-4 11:57</a>

试了花2，爆杀呆萌5.0

—— 来自 Xiaomi M2012K11AC, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
谢了

*****

####  古畑任三郎2015  
##### 134#       发表于 2021-12-4 12:04

奥特曼格斗3全速

菊花980

*****

####  小天女  
##### 135#       发表于 2021-12-4 12:06

睡能提供一下apk…手机用谷歌商城下载就报错

*****

####  Kojimaru  
##### 136#       发表于 2021-12-4 12:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804415&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-12-4 11:37</a>
为什么我搜不到

—— 来自 Xiaomi MI 6, Android 9上的 S1Next-鹅版 v2.5.2</blockquote>
现在是测试吧，点楼主链接就能下了

*****

####  DaveZED  
##### 137#       发表于 2021-12-4 12:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804415&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-12-4 11:37</a>
为什么我搜不到

—— 来自 Xiaomi MI 6, Android 9上的 S1Next-鹅版 v2.5.2</blockquote>
搜aetherSX2，在搜索栏下面选“新”，应该就能看到了

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  彩虹肥宅  
##### 138#       发表于 2021-12-4 12:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804764&amp;ptid=2037739" target="_blank">Kojimaru 发表于 2021-12-4 12:15</a>
现在是测试吧，点楼主链接就能下了</blockquote>
下好了<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  彩虹肥宅  
##### 139#       发表于 2021-12-4 12:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804874&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 12:28</a>
搜aetherSX2，在搜索栏下面选“新”，应该就能看到了

—— 来自 samsung SM-N976N, Android 11上的 S1Ne ...</blockquote>
找到了<img src="https://static.saraba1st.com/image/smiley/face2017/032.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  kirito_wst  
##### 140#       发表于 2021-12-4 12:30

链接:https://pan.baidu.com/s/1YdgNKZ1KkasDE2aCasthcQ 
提取码:oe3e
做个度盘分流，apk用另一个手机安装测试过了

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| cuchulain2021| + 1|好评加鹅|

查看全部评分

*****

####  幽灵胖胖  
##### 141#       发表于 2021-12-4 12:30

我要打十遍花2，二十遍花3，三十遍ogs

*****

####  精钢魔像  
##### 142#       发表于 2021-12-4 12:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53804626&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 11:58</a>

问一下上哪里能下到iso，感觉网上好多都是沾点广告的

—— 来自 samsung SM-N976N, Android 11上的 ...</blockquote>
老男人

汉化rom和iso是不用注册的

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| DaveZED| + 1||

查看全部评分

*****

####  lyt77777  
##### 143#       发表于 2021-12-4 12:42

<img src="https://img.saraba1st.com/forum/202112/04/124205knrn5f4mf7757mnn.jpg" referrerpolicy="no-referrer">

<strong>QQ图片20211204124138.jpg</strong> (173.56 KB, 下载次数: 0)

下载附件

2021-12-4 12:42 上传

<img src="https://img.saraba1st.com/forum/202112/04/124205h25fgs2fdu875zb8.jpg" referrerpolicy="no-referrer">

<strong>QQ图片20211204124142.jpg</strong> (158.48 KB, 下载次数: 0)

下载附件

2021-12-4 12:42 上传

出家人不打诳语，小米8，战斗60，标题60，但是小地图移动的时候声音有拖慢，原因尚且不明。

*****

####  医生狼多  
##### 144#       发表于 2021-12-4 12:43

老男人的144个ps2游戏iso，原帖：[https://www.oldmanemu.net/%e5%ae ... %b8%b8%e6%88%8f/ps2](https://www.oldmanemu.net/%e5%ae%b6%e6%9c%ba%e6%b8%b8%e6%88%8f/ps2)

链接：[https://pan.baidu.com/s/1RxxgWkQTXVM7ZcUU5OBI-Q](https://pan.baidu.com/s/1RxxgWkQTXVM7ZcUU5OBI-Q) 

提取码：hw0y 

*****

####  小天女  
##### 145#       发表于 2021-12-4 12:46

搞定了，手机里面昨天弄了两个游戏，试了一下，全部流畅，『第二次机战阿华』贴图有点小问题，比如爆炸出来的是黑色色块。『重装机兵』基本完美。总体来说…呆萌模拟器可以进垃圾桶了

*****

####  cuchulain2021  
##### 146#       发表于 2021-12-4 12:52

配合拉伸手柄可以选自动隐藏屏幕按键，没什么问题

有人有什么游戏想要测试的么？

*****

####  JudgmentEye  
##### 147#       发表于 2021-12-4 12:57

865跑机战z完美

*****

####  erre_1  
##### 148#       发表于 2021-12-4 12:58

试试最难搞的北妹2怎么样

—— 来自 Sony J8170, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  cuchulain2021  
##### 149#       发表于 2021-12-4 13:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805137&amp;ptid=2037739" target="_blank">erre_1 发表于 2021-12-4 12:58</a>

试试最难搞的北妹2怎么样

—— 来自 Sony J8170, Android 11上的 S1Next-鹅版 v2.5.2-play ...</blockquote>
试了下黑屏打不开（

*****

####  highsky  
##### 150#       发表于 2021-12-4 13:11

试了下面的，都能ee正常满速

机战a3、ogs

鬼泣3se

gt4

前线5

这还只是公测版哦



*****

####  JudgmentEye  
##### 151#       发表于 2021-12-4 13:13

要求挺低的，765跑机战z都满速

*****

####  精钢魔像  
##### 152#       发表于 2021-12-4 13:21

再次觉得双11 1550的摩托edge s真值

*****

####  lyt77777  
##### 153#       发表于 2021-12-4 13:22

我突然意识到，泥潭做寨机生意的是不是都要砸手里了，其实海豚寨机就跑不好，这下PS2来了，谁还买寨机啊。<img src="https://static.saraba1st.com/image/smiley/face2017/048.png" referrerpolicy="no-referrer">

*****

####  冰比冰水冰  
##### 154#       发表于 2021-12-4 13:28

<blockquote>highsky 发表于 2021-12-4 13:11
试了下面的，都能ee正常满速

机战a3、ogs

鬼泣3se
</blockquote>
贝维克传说怎么样？

*****

####  highsky  
##### 155#       发表于 2021-12-4 13:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805399&amp;ptid=2037739" target="_blank">冰比冰水冰 发表于 2021-12-4 13:28</a>

贝维克传说怎么样？</blockquote>
完美

*****

####  DaveZED  
##### 156#       发表于 2021-12-4 13:30

大佬们这个问题怎么解决，从老男孩下的战神2iso<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  highsky  
##### 157#       发表于 2021-12-4 13:31

 本帖最后由 highsky 于 2021-12-4 13:32 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805339&amp;ptid=2037739" target="_blank">lyt77777 发表于 2021-12-4 13:22</a>

我突然意识到，泥潭做寨机生意的是不是都要砸手里了，其实海豚寨机就跑不好，这下PS2来了，谁还买寨机啊。[ ...</blockquote>
你搞反了吧，最近寨机界都沸腾了

不说用845的odin出来后通吃ps2了

就连soc用的很烂的rp2.5都能跑跑机战

年底起码有3、4台安卓寨机上市，明年寨机花样会更多

*****

####  navarra  
##### 158#       发表于 2021-12-4 13:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805410&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 13:30</a>
大佬们这个问题怎么解决，从老男孩下的战神2iso

—— 来自 samsung SM-N976N, Android 11上的 S1Ne ...</blockquote>
你需要ps2 bios……

—— 来自 samsung SM-G9880, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  ogloc  
##### 159#       发表于 2021-12-4 13:35

我用835玩花3，全速运行，体验太好了，晚点测试OGS， 以前用呆萌玩OGS都不到30帧，卡死

*****

####  Narrative  
##### 160#       发表于 2021-12-4 13:38

试了下，354 855可以60fps运行，呆萌这东西会拖慢

*****

####  谷恒条野  
##### 161#         楼主| 发表于 2021-12-4 13:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805226&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 13:07</a>
试了下黑屏打不开（</blockquote>
试试把system下面三个都打开

*****

####  JudgmentEye  
##### 162#       发表于 2021-12-4 13:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805399&amp;ptid=2037739" target="_blank">冰比冰水冰 发表于 2021-12-4 13:28</a>

贝维克传说怎么样？</blockquote>
2d基本都完美

*****

####  JudgmentEye  
##### 163#       发表于 2021-12-4 13:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805410&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 13:30</a>

大佬们这个问题怎么解决，从老男孩下的战神2iso

—— 来自 samsung SM-N976N, Android 11上的 S1Ne ...</blockquote>
需要ps2的bios

*****

####  猫不萌  
##### 164#       发表于 2021-12-4 13:44

<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">期待一台安卓16:9的855级别的寨机了，拿有打孔屏的手机玩真的很不爽

*****

####  JudgmentEye  
##### 165#       发表于 2021-12-4 13:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805546&amp;ptid=2037739" target="_blank">猫不萌 发表于 2021-12-4 13:44</a>

期待一台安卓16:9的855级别的寨机了，拿有打孔屏的手机玩真的很不爽</blockquote>
大法欢迎你

*****

####  猫不萌  
##### 166#       发表于 2021-12-4 13:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805564&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 13:46</a>

大法欢迎你</blockquote>
没实体按键的还是一边去

*****

####  cuchulain2021  
##### 167#       发表于 2021-12-4 13:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805546&amp;ptid=2037739" target="_blank">猫不萌 发表于 2021-12-4 13:44</a>

期待一台安卓16:9的855级别的寨机了，拿有打孔屏的手机玩真的很不爽</blockquote>
现在手机那么长的屏幕比例，打孔根本影响不到吧……

*****

####  cuchulain2021  
##### 168#       发表于 2021-12-4 13:50

 本帖最后由 cuchulain2021 于 2021-12-4 13:53 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805505&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-4 13:40</a>

试试把system下面三个都打开</blockquote>
能打开了，片头好像没什么问题。不过进游戏帧数很低，才3x（一加8t），似乎还是不太行

*****

####  医生狼多  
##### 169#       发表于 2021-12-4 13:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805410&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 13:30</a>

大佬们这个问题怎么解决，从老男孩下的战神2iso

—— 来自 samsung SM-N976N, Android 11上的 S1Ne ...</blockquote>
下载bios：链接：[https://pan.baidu.com/s/1ctkb7X0DXwQP7hDmpped9A](https://pan.baidu.com/s/1ctkb7X0DXwQP7hDmpped9A) 

提取码：gh3w 

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| DaveZED| + 1||

查看全部评分

*****

####  龘䶛䨻䎱㸞蚮䡶  
##### 170#       发表于 2021-12-4 13:54

这个可以开金手指吗

*****

####  猫不萌  
##### 171#       发表于 2021-12-4 13:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805600&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 13:50</a>
现在手机那么长的屏幕比例，打孔根本影响不到吧……</blockquote>
很不爽啊，虚拟按键也不能移动到打孔区域那一条。现在在看ayn odin怎么样

*****

####  LMBS  
##### 172#       发表于 2021-12-4 14:02

OGS的战斗背景黑线目前是不是无解，试过好多模拟器都一样

试玩了下OG2第一关，除了上面说的黑线，大招爆炸时有点掉帧，挺好的。870的手机

*****

####  古畑任三郎2015  
##### 173#       发表于 2021-12-4 14:03

 本帖最后由 古畑任三郎2015 于 2021-12-4 15:19 编辑 

菊花980
ff12,xs3这种3d游戏还是不太行，不过兼容性比狗萌强不少，凡人物语绝体绝命2表现都不错，体感有个四五十针
目前这个模拟器运行效率还是比不上pc版的
我记得和五六年前atom3740在win8.1上3d游戏的表现差不太多
-----------
编辑一下说法，微调了设置以后，ff12满速了<img src="https://static.saraba1st.com/image/smiley/face2017/174.png" referrerpolicy="no-referrer">
不过其他变化不大

*****

####  Xenor  
##### 174#       发表于 2021-12-4 14:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53794238&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-3 12:37</a>

如果是基于最新版pcsx2多半支持chd格式，一部分游戏可以压缩的很小</blockquote>
一时间想不起PS2上有啥想玩的游戏了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  cuchulain2021  
##### 175#       发表于 2021-12-4 14:10

合金装备3 生存 美版 草丛里有时候会掉帧

忍第一关满帧

龙背上的骑兵2教学关满帧

*****

####  杉田悠一  
##### 176#       发表于 2021-12-4 14:12

<img src="https://static.saraba1st.com/image/smiley/face2017/047.png" referrerpolicy="no-referrer">

*****

####  当光停止  
##### 177#       发表于 2021-12-4 14:35

<img src="https://static.saraba1st.com/image/smiley/face2017/062.gif" referrerpolicy="no-referrer">下个古堡迷踪玩玩。

*****

####  JudgmentEye  
##### 178#       发表于 2021-12-4 14:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805631&amp;ptid=2037739" target="_blank">龘䶛䨻䎱㸞蚮䡶 发表于 2021-12-4 13:54</a>

这个可以开金手指吗</blockquote>
暂无，先用pc改完，存档放猴上玩吧，或者root的机器用ce或八门神器之类内存修改工具

*****

####  JudgmentEye  
##### 179#       发表于 2021-12-4 14:40

 本帖最后由 JudgmentEye 于 2021-12-4 14:41 编辑 

765g，机战全家桶开2倍速都没问题，impact有拖慢，别的都ok

*****

####  被雨困住的城市  
##### 180#       发表于 2021-12-4 14:44

提示: 作者被禁止或删除 内容自动屏蔽



*****

####  lighttt  
##### 181#       发表于 2021-12-4 14:46

呆萌死了吧，这脑残玩意<img src="https://static.saraba1st.com/image/smiley/face2017/047.png" referrerpolicy="no-referrer">

*****

####  Suljo  
##### 182#       发表于 2021-12-4 14:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805098&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 12:52</a>
配合拉伸手柄可以选自动隐藏屏幕按键，没什么问题

有人有什么游戏想要测试的么？ ...</blockquote>
试试新鬼

*****

####  JudgmentEye  
##### 183#       发表于 2021-12-4 14:52

 本帖最后由 JudgmentEye 于 2021-12-4 14:53 编辑 

模拟器汉化版+bios
[https://pan.baidu.com/s/10oVZwJ3ranNWnVjNysX-YA](https://pan.baidu.com/s/10oVZwJ3ranNWnVjNysX-YA)

提取码9999

*****

####  谷恒条野  
##### 184#         楼主| 发表于 2021-12-4 14:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805631&amp;ptid=2037739" target="_blank">龘䶛䨻䎱㸞蚮䡶 发表于 2021-12-4 13:54</a>
这个可以开金手指吗</blockquote>
app settings&gt;enable patch codes
然后进游戏打开模拟器设置，有一项patch codes。

*****

####  cuchulain2021  
##### 185#       发表于 2021-12-4 14:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806034&amp;ptid=2037739" target="_blank">Suljo 发表于 2021-12-4 14:47</a>

试试新鬼</blockquote>
美版标题画面花屏，进了游戏之后倒是没啥问题，第一个场景60帧流畅

顺便说一下寂静岭2能打宽屏补丁，手动16：9显示正常，一开始在雾里跑60帧

*****

####  保科智子  
##### 186#       发表于 2021-12-4 15:09

660的小米跑新鬼都能正常进游戏，有点拖慢而已。p40帧数感觉不稳定，飙血就降到60%。麒麟核心兼容度不行？<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  JudgmentEye  
##### 187#       发表于 2021-12-4 15:10

 本帖最后由 JudgmentEye 于 2021-12-4 15:12 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806090&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-4 14:57</a>

app settings&gt;enable patch codes

然后进游戏打开模拟器设置，有一项patch codes。</blockquote>
那个是宽屏补丁，当然你解包apk，自己把金手指写入/assets/cheats_ws.zip里对应的pnach，重打包回apk也行，就是麻烦点

*****

####  谷恒条野  
##### 188#         楼主| 发表于 2021-12-4 15:14

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806167&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 15:10</a>
那个是宽屏补丁，当然你解包apk，自己把金手指写入/assets/cheats_ws.zip里对应的pnach，重打包回apk也行 ...</blockquote>
宽屏补丁在graphics&gt;enable widescreen patches吧

*****

####  JudgmentEye  
##### 189#       发表于 2021-12-4 15:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806204&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-4 15:14</a>

宽屏补丁在graphics&gt;enable widescreen patches吧</blockquote>
自定义金手指补丁放在哪？我放iso相同目录下，设成和iso文件名相同无效

*****

####  JudgmentEye  
##### 190#       发表于 2021-12-4 15:24

 本帖最后由 JudgmentEye 于 2021-12-4 16:56 编辑 

知道了，改成和游戏对应的crc名.pnach，放内部存储/android/data/xyz.sethersx2.android/files/cheats下，或者游戏中直接添加也行

资金

patch=1,EE,20558560,extended,05F5E0FF

BS

patch=1,EE,205585A8,extended,000F423F

SR

patch=1,EE,0055856F,extended,00000063

<img src="https://img.saraba1st.com/forum/202112/04/155107fqqjtzlmswqlwcim.png" referrerpolicy="no-referrer">

<strong>z.png</strong> (248.15 KB, 下载次数: 0)

下载附件

2021-12-4 15:51 上传

*****

####  fyzqwzh  
##### 191#       发表于 2021-12-4 15:40

厉害了，845打ogs完全不卡，问下怎么把存档转到这上面

*****

####  JudgmentEye  
##### 192#       发表于 2021-12-4 15:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806400&amp;ptid=2037739" target="_blank">fyzqwzh 发表于 2021-12-4 15:40</a>

厉害了，845打ogs完全不卡，问下怎么把存档转到这上面</blockquote>
和pcsx2的存档通用，用import memory cards导入，或者改名Mcd001.ps2直接放内部存储/android/data/xyz.sethersx2.android/files/memcards就行

*****

####  葫芦娃打爷爷  
##### 193#       发表于 2021-12-4 15:55

好耶可以补机战了<img src="https://static.saraba1st.com/image/smiley/face2017/045.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi M2007J3SC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  谷恒条野  
##### 194#         楼主| 发表于 2021-12-4 16:00

 本帖最后由 谷恒条野 于 2021-12-4 16:17 编辑 

出去了下好像作者更新了个版本。<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">
说是修复了扫描无效文件时崩溃和某些游戏的存档问题。
================================
发现游戏中把进入待机的手柄再连上会卡黑屏?
再试了一次好像又行了。

*****

####  lighttt  
##### 195#       发表于 2021-12-4 16:07

下的汉化版扫描不到游戏，是这个版的bug吗

*****

####  彩虹肥宅  
##### 196#       发表于 2021-12-4 16:09

gt赛车4，进游戏只会显示国行游戏的那个提示，之后黑屏无法操作，有办法解决吗。

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  okey3m  
##### 197#       发表于 2021-12-4 16:09

mate40，玩贝里克物语开opengl只有40%的速度，vulkan黑屏，看来麒麟和它无缘了……

*****

####  ogloc  
##### 198#       发表于 2021-12-4 16:10

835玩OGS还是有点卡，去闲鱼搞台855洋垃圾

*****

####  last_crusader  
##### 199#       发表于 2021-12-4 16:16

红魔5g，865,一直卡BIOS界面，不读碟(进不了游戏)求大佬设置教程<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  back57992  
##### 200#       发表于 2021-12-4 16:19

哇 牛逼，有没有自带手柄的手机呢？

*****

####  谷恒条野  
##### 201#         楼主| 发表于 2021-12-4 16:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806603&amp;ptid=2037739" target="_blank">lighttt 发表于 2021-12-4 16:07</a>
下的汉化版扫描不到游戏，是这个版的bug吗</blockquote>
文件名我是直接用拼音简写的，刷新没啥问题。

*****

####  谷恒条野  
##### 202#         楼主| 发表于 2021-12-4 16:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806688&amp;ptid=2037739" target="_blank">last_crusader 发表于 2021-12-4 16:16</a>
红魔5g，865,一直卡BIOS界面，不读碟(进不了游戏)求大佬设置教程

  -- 来自 能搜索的 Stage1官方 A ...</blockquote>
你选了文件夹在选bios,再选游戏iso镜像应该就能玩了啊。

*****

####  幽灵胖胖  
##### 203#       发表于 2021-12-4 16:25

游戏全部准备好，看来春节前上班有的鱼摸了<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  古畑任三郎2015  
##### 204#       发表于 2021-12-4 16:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806627&amp;ptid=2037739" target="_blank">okey3m 发表于 2021-12-4 16:09</a>
mate40，玩贝里克物语开opengl只有40%的速度，vulkan黑屏，看来麒麟和它无缘了…… ...</blockquote>
不会吧，我是980，贝里克物语opengl两倍分辨率满速啊，连微热都没有的那种

*****

####  黄金时代  
##### 205#       发表于 2021-12-4 16:35

750G联想板子全速跑A3人物图像都能正常显示，零红蝶有点拖慢正常能跑。呆萌去死阴沟里吧

----发送自 [Alldocube iPlay_30,Android 10](http://stage1.5j4m.com/?1.37)

*****

####  okey3m  
##### 206#       发表于 2021-12-4 16:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806838&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-12-4 16:33</a>
不会吧，我是980，贝里克物语opengl两倍分辨率满速啊，连微热都没有的那种 ...</blockquote>
你是什么版本？我是在老男人下载的中文版，莫非是这个原因？

*****

####  JudgmentEye  
##### 207#       发表于 2021-12-4 16:39

谁有条件？试试黄老板核弹shield的手柄能不能认

*****

####  古畑任三郎2015  
##### 208#       发表于 2021-12-4 16:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806860&amp;ptid=2037739" target="_blank">okey3m 发表于 2021-12-4 16:36</a>

你是什么版本？我是在老男人下载的中文版，莫非是这个原因？</blockquote>
同老男人啊。。和游戏版本应该没有关系吧

不过我稍微改过设置，但我觉得那些gpu加速选项对2d游戏应该没啥影响才是...

*****

####  JudgmentEye  
##### 209#       发表于 2021-12-4 16:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806619&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-12-4 16:09</a>

gt赛车4，进游戏只会显示国行游戏的那个提示，之后黑屏无法操作，有办法解决吗。

—— 来自 Xiaomi MI 6,  ...</blockquote>
换国行的bios试试

*****

####  幽灵胖胖  
##### 210#       发表于 2021-12-4 16:47

如何设置键位啊？我不知道设置了啥，虚拟键盘没了，本来想把摇杆换成十字键的<img src="https://static.saraba1st.com/image/smiley/face2017/143.png" referrerpolicy="no-referrer">



*****

####  桧山修之  
##### 211#       发表于 2021-12-4 16:48

回家马上试试，还好之前在网盘存了一大堆ps2的游戏，想重温的游戏挺多的，星海3，影之心2，凡人物语，宿命传说重制版，几部机战，数码恶魔传说，北欧女神2，荒野兵器f,4,5，幻水3，银河游侠，日式rpg迷的狂欢！

*****

####  magpte  
##### 212#       发表于 2021-12-4 16:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806886&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 16:39</a>

谁有条件？试试黄老板核弹shield的手柄能不能认</blockquote>
卧槽，这个的话会不会真的暴爽

*****

####  okey3m  
##### 213#       发表于 2021-12-4 16:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806894&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-12-4 16:40</a>
同老男人啊。。和游戏版本应该没有关系吧

不过我稍微改过设置，但我觉得那些gpu加速选项对2d游戏应该没啥 ...</blockquote>
刚才进设置乱勾了几个选项，再进游戏就全速了……

*****

####  JudgmentEye  
##### 214#       发表于 2021-12-4 16:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806937&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-4 16:47</a>

如何设置键位啊？我不知道设置了啥，虚拟键盘没了，本来想把摇杆换成十字键的 ...</blockquote>
我也碰上了，清空数据存储和缓存重设吧，记得先备份内部存储/android/data/xyz.sethersx2.android/files/memcards里的存档

*****

####  谷恒条野  
##### 215#         楼主| 发表于 2021-12-4 16:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806688&amp;ptid=2037739" target="_blank">last_crusader 发表于 2021-12-4 16:16</a>
红魔5g，865,一直卡BIOS界面，不读碟(进不了游戏)求大佬设置教程

  -- 来自 能搜索的 Stage1官方 A ...</blockquote>
看群里面有用红魔也载入不了游戏的，但是他可以点设置，start bios再点change disc来载入iso.<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  谷恒条野  
##### 216#         楼主| 发表于 2021-12-4 16:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806937&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-4 16:47</a>
如何设置键位啊？我不知道设置了啥，虚拟键盘没了，本来想把摇杆换成十字键的 ...</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">汉化版？有虚拟键盘消失的bug。

*****

####  JudgmentEye  
##### 217#       发表于 2021-12-4 16:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806688&amp;ptid=2037739" target="_blank">last_crusader 发表于 2021-12-4 16:16</a>

红魔5g，865,一直卡BIOS界面，不读碟(进不了游戏)求大佬设置教程

  -- 来自 能搜索的 Stage1官方 A ...</blockquote>
给模拟器访问存储设备的权限

*****

####  幽灵胖胖  
##### 218#       发表于 2021-12-4 16:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807026&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-4 16:57</a>

汉化版？有虚拟键盘消失的bug。</blockquote>
肏，那就装原版了，233

*****

####  精钢魔像  
##### 219#       发表于 2021-12-4 16:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806688&amp;ptid=2037739" target="_blank">last_crusader 发表于 2021-12-4 16:16</a>

红魔5g，865,一直卡BIOS界面，不读碟(进不了游戏)求大佬设置教程

  -- 来自 能搜索的 Stage1官方 A ...</blockquote>
试试把fast boot关掉，如果是关掉不行就打开

不过我觉得多半是iso格式不对，换cue+bin格式的镜像试试

*****

####  shamisen  
##### 220#       发表于 2021-12-4 17:01

宿命传说导演剪辑版进不去。。

*****

####  幽灵胖胖  
##### 221#       发表于 2021-12-4 17:07

确实是汉化版的BUG，换原版就好了，也能修改键位

*****

####  幽灵胖胖  
##### 222#       发表于 2021-12-4 17:07

风怒。。。。。。。

*****

####  古畑任三郎2015  
##### 223#       发表于 2021-12-4 17:09

公测版这么快就有更新了<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">

*****

####  lighttt  
##### 224#       发表于 2021-12-4 17:14

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806735&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-4 16:21</a>

文件名我是直接用拼音简写的，刷新没啥问题。</blockquote>
我是说游戏放进去了，设置了文件夹，好像读取不了文件夹，都要手动右下角选游戏<img src="https://static.saraba1st.com/image/smiley/face2017/022.png" referrerpolicy="no-referrer">

*****

####  愤怒的栗子  
##### 225#       发表于 2021-12-4 17:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806886&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 16:39</a>

谁有条件？试试黄老板核弹shield的手柄能不能认</blockquote>
Shield TV吗？模拟器界面测测就行还是要下个rom进游戏？

*****

####  Kojimaru  
##### 226#       发表于 2021-12-4 17:18

北妹2黑屏，什么情况<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  cuchulain2021  
##### 227#       发表于 2021-12-4 17:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807218&amp;ptid=2037739" target="_blank">Kojimaru 发表于 2021-12-4 17:18</a>

北妹2黑屏，什么情况</blockquote>
system下面最三个选项必须都要勾上，而且并不能流畅运行，没必要试了……

试了下王国之心fm，在小岛面对海会有些掉帧

*****

####  Kojimaru  
##### 228#       发表于 2021-12-4 17:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807293&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 17:26</a>

system下面最三个选项必须都要勾上，而且并不能流畅运行，没必要试了……

试了下王国之心fm，在小岛面对 ...</blockquote>
<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">打开了，港口那直接慢动作，确实还不太行

*****

####  Lilithy  
##### 229#       发表于 2021-12-4 18:07

女侧2港口慢动作，第一个图闪退，麒麟980

----发送自 [HUAWEI PCT-AL10,Android 10](http://stage1.5j4m.com/?1.37)

*****

####  JudgmentEye  
##### 230#       发表于 2021-12-4 18:07

黄老板核弹shield手柄好像没问题，我只有机器没手柄，但用遥控器可以直接控制方向，配合鼠标点电视上的触摸按键还真能玩

*****

####  JudgmentEye  
##### 231#       发表于 2021-12-4 18:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807205&amp;ptid=2037739" target="_blank">愤怒的栗子 发表于 2021-12-4 17:17</a>

Shield TV吗？模拟器界面测测就行还是要下个rom进游戏？</blockquote>
得进游戏吧，我测了，遥控器直接按方向好使，估计手柄99%没问题

*****

####  慕容断月  
##### 232#       发表于 2021-12-4 18:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805631&amp;ptid=2037739" target="_blank">龘䶛䨻䎱㸞蚮䡶 发表于 2021-12-4 13:54</a>

这个可以开金手指吗</blockquote>
可以啊，点开Enable Cheat就行了

*****

####  xbhuang  
##### 233#       发表于 2021-12-4 18:09

这个ps2模拟器能跑ps1游戏吗？

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  navarra  
##### 234#       发表于 2021-12-4 18:10

连扎2P选完觉醒后闪退.......

*****

####  navarra  
##### 235#       发表于 2021-12-4 18:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807624&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-4 18:09</a>

这个ps2模拟器能跑ps1游戏吗？

—— 来自 S1Fun</blockquote>
跑ps1游戏请用ps1模拟器，例如duckstation

*****

####  JudgmentEye  
##### 236#       发表于 2021-12-4 18:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807624&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-4 18:09</a>

这个ps2模拟器能跑ps1游戏吗？

—— 来自 S1Fun</blockquote>
pcsx2原版能跑他就能跑

*****

####  谷恒条野  
##### 237#         楼主| 发表于 2021-12-4 18:19

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807624&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-4 18:09</a>
这个ps2模拟器能跑ps1游戏吗？

—— 来自 S1Fun</blockquote>
作者说他也没试过，请用ps1模拟器<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  月夜凝雪  
##### 238#       发表于 2021-12-4 18:20

不知道紫光U的寨板能不能跑，现在能插卡的板子真没几个了

—— 来自 Xiaomi M2006J10C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  保科智子  
##### 239#       发表于 2021-12-4 18:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807624&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-4 18:09</a>

这个ps2模拟器能跑ps1游戏吗？

—— 来自 S1Fun</blockquote>
第一个试的就是手机里的PS1 iso，能进游戏。运行不正常。<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">

*****

####  51569  
##### 240#       发表于 2021-12-4 18:25

这界面和鸭子模拟器不能说十分相近，只能说一模一样了



*****

####  愤怒的栗子  
##### 241#       发表于 2021-12-4 18:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807621&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 18:09</a>

得进游戏吧，我测了，遥控器直接按方向好使，估计手柄99%没问题</blockquote>
那等我有闲工夫了试试吧

*****

####  navarra  
##### 242#       发表于 2021-12-4 18:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807712&amp;ptid=2037739" target="_blank">月夜凝雪 发表于 2021-12-4 18:20</a>

不知道紫光U的寨板能不能跑，现在能插卡的板子真没几个了

—— 来自 Xiaomi M2006J10C, Android 11上的 S1 ...</blockquote>
对自己好点，弄个欧美版三星tab s7......

*****

####  月夜凝雪  
##### 243#       发表于 2021-12-4 18:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807890&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-4 18:44</a>

对自己好点，弄个欧美版三星tab s7......</blockquote>
1100和4200这差距大太多了，给这数还不如笔记本了

*****

####  navarra  
##### 244#       发表于 2021-12-4 18:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807914&amp;ptid=2037739" target="_blank">月夜凝雪 发表于 2021-12-4 18:47</a>

1100和4200这差距大太多了，给这数还不如笔记本了</blockquote>
去咸鱼......

*****

####  飞侠小黑  
##### 245#       发表于 2021-12-4 18:52

 本帖最后由 飞侠小黑 于 2021-12-4 18:54 编辑 

零的帧数还是不行，是麒麟的问题？
晚上试试1+8t

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  红叶  
##### 246#       发表于 2021-12-4 18:58

870 ogs完美 内流满面
<img src="https://p.sda1.dev/3/48424e0e8bd13ee21a338fa08e33f43d/IMG_CMP_216696747.jpeg" referrerpolicy="no-referrer">

—— 来自 Xiaomi M2102J2SC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  月夜凝雪  
##### 247#       发表于 2021-12-4 18:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807935&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-4 18:49</a>
去咸鱼......</blockquote>
咸鱼也要3000左右

—— 来自 Xiaomi M2006J10C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  保科智子  
##### 248#       发表于 2021-12-4 19:04

麒麟990一到3D就完全不行。华为系绝望了吗？<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  古畑任三郎2015  
##### 249#       发表于 2021-12-4 19:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808031&amp;ptid=2037739" target="_blank">月夜凝雪 发表于 2021-12-4 18:59</a>

咸鱼也要3000左右

—— 来自 Xiaomi M2006J10C, Android 11上的 S1Next-鹅版 v2.5.2-play</blockquote>
二手菊板就可以，我看了下贴吧的表述结合自己的使用感觉，这模拟器对980/855及以上的u表现基本一视同仁

*****

####  彩虹肥宅  
##### 250#       发表于 2021-12-4 19:05

鬼泣3特别版闪退

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  月夜凝雪  
##### 251#       发表于 2021-12-4 19:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808075&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-12-4 19:04</a>

二手菊板就可以，我看了下贴吧的表述结合自己的使用感觉，这模拟器对980/855及以上的u表现基本一视同仁 ...</blockquote>
不能插卡啊，当初M6我卖掉的其中一个因素就是不能扩展

*****

####  navarra  
##### 252#       发表于 2021-12-4 19:08

 本帖最后由 navarra 于 2021-12-4 19:09 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808092&amp;ptid=2037739" target="_blank">月夜凝雪 发表于 2021-12-4 19:06</a>

不能插卡啊，当初M6我卖掉的其中一个因素就是不能扩展</blockquote>
？你在说什么......M6 8.4能插tf卡，还有4Glte版好吧？我以为你要插sim卡呢，联想今年那几台都可以插tf卡的

*****

####  susan28  
##### 253#       发表于 2021-12-4 19:12

有人跑战神2吗？能玩吗？

—— 来自 OPPO PCLM10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.0.4-play

*****

####  Jumbohard  
##### 254#       发表于 2021-12-4 19:13

 本帖最后由 Jumbohard 于 2021-12-4 20:51 编辑 

试了下深渊传说，麒麟990开3x原生分辨率FXAA能稳定60帧，感觉还留有一些拉分辨率、加滤镜之类的余地

但是选vulkan后端几乎所有游戏都会闪退，不知道是麒麟U的问题还是这个版本几乎都存在的问题。--看了眼faqs，原来现阶段mali GPU都不支持vulkan

说起来感觉完成度好高啊……本来看图标那么简陋还以为会是一个光架子，结果发现可能需要的东西都有了。搭配PS4手柄感觉平板又找到新乐子了。

进了大场景之后又遇到了那个鬼影问题……似乎游戏的柔化滤镜在拉了内部分辨率之后和画面错位了。PC上是后面升级了图形插件解决的，不知道这个模拟器多久能修这个问题。

*****

####  月夜凝雪  
##### 255#       发表于 2021-12-4 19:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808117&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-4 19:08</a>

？你在说什么......M6 8.4能插tf卡，还有4Glte版好吧？我以为你要插sim卡呢，联想今年那几台都可以插tf卡 ...</blockquote>
咦？那么记错了？虽然我卖掉的主因是华为系统更新后那个三大金刚强制隐藏不能不隐藏而且超容易触碰弹出

Sim卡当然也是能插最好，要联网时开热点还是有点麻烦，看看高能版现在什么价

*****

####  JudgmentEye  
##### 256#       发表于 2021-12-4 19:18

ps4手柄能用？什么平板

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  幽灵胖胖  
##### 257#       发表于 2021-12-4 19:19

搞了好久终于把尘封已久的飞智wee连上了，还得装飞智自家的游戏中心，玛德<img src="https://static.saraba1st.com/image/smiley/face2017/163.png" referrerpolicy="no-referrer">

*****

####  慕容断月  
##### 258#       发表于 2021-12-4 19:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806229&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 15:18</a>

自定义金手指补丁放在哪？我放iso相同目录下，设成和iso文件名相同无效</blockquote>
Android\data\xyz.aethersx2什么的

*****

####  navarra  
##### 259#       发表于 2021-12-4 19:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808164&amp;ptid=2037739" target="_blank">susan28 发表于 2021-12-4 19:12</a>

有人跑战神2吗？能玩吗？

—— 来自 OPPO PCLM10, Android 10上的 S1Next-鹅版 v2.0.4-play ...</blockquote>
贴吧有，小米9都能60帧

*****

####  cuchulain2021  
##### 260#       发表于 2021-12-4 19:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53807961&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-4 18:52</a>

零的帧数还是不行，是麒麟的问题？

晚上试试1+8t</blockquote>
一加8t

零zero大部分场景都是60，不过有时候会出现小掉帧，不知道为什么

女神异闻录3fes和4都没什么问题（不过这俩本来就不吃配置），其中4支持宽屏

*****

####  慕容断月  
##### 261#       发表于 2021-12-4 19:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806034&amp;ptid=2037739" target="_blank">Suljo 发表于 2021-12-4 14:47</a>

试试新鬼</blockquote>
用国外大佬做的绕过卡死+强制逐行金手指，菜单花屏有所减缓

帧数的话2X也能稳定60+，1X大概100帧左右

<img src="https://img.saraba1st.com/forum/202112/04/192623mb66u0vhv4u0s0vq.jpg" referrerpolicy="no-referrer">

<strong>1.jpg</strong> (127.23 KB, 下载次数: 0)

下载附件

2021-12-4 19:26 上传

<img src="https://img.saraba1st.com/forum/202112/04/192622fw6mibidsbe6o6cs.jpg" referrerpolicy="no-referrer">

<strong>2.jpg</strong> (142.43 KB, 下载次数: 0)

下载附件

2021-12-4 19:26 上传

代码：
  gametitle=Shin Onimusha - Dawn of Dreams (Japan) (Disc 1) (PlayStation 2 the Best) SLPM_742.32;1) comment=Test Ipu Hack (Kozarov) - Enhacement by felixthecat1970  //将 IPU_DATA IVF 设置为 Intra patch=0,EE,203C0468,extended,3C040020  //将 IPU_CMD 设置为 IDEC，并将 QSC 设置为 2 patch=0,EE,203C047C,extended,3C021002  //禁用打印控制台 patch=0,EE,2010FDC8,extended,34190180 patch=0,EE,2010FDCC,extended,1720FFFF patch=0,EE,2010FDD0,extended,2739FFFF patch=0,EE,2010FDD4,extended,03E00008 patch=0,EE,2010FDD8,extended,00000000  //解决方法修复崩溃（此游戏版本错过了“影子女士”解决方法补丁） patch=0,EE,20104190,extended,1440FFF9  //sceGSVsync f? bypass f. - 使用 nopi 代码转换错误 (测试游戏“计数器”性能) //patch=0,EE,20103480,extended,00000000 //patch=0,EE,2010343C,extended,00000000 //patch=0,EE,2010346C,extended,30420000 //test nopi //patch=0,EE,20103490,extended,30440000 //test nopi  //效果测试代码 (未知寄存器/值/效果瓶颈 GS 或 GPU) patch=1,EE,E0010E0A,extended,0084FB00 //unk - recomended enabled patch=1,EE,0084FB00,extended,00  patch=1,EE,E0010D03,extended,00850100 //df patch=1,EE,00850100,extended,00  patch=1,EE,E0010D05,extended,0084FF00 //ef patch=1,EE,0084FF00,extended,00  patch=1,EE,E0010D05,extended,00850300 //ef patch=1,EE,00850300,extended,00  //无隔行部分（菜单背景 -视频仍然抖动） patch=0,EE,20178454,extended,00001825  //宽屏 hack 16:9 by nemesis2000（宽屏存档） patch=0,EE,2012F960,extended,3C033F19 //3c033f4c patch=0,EE,2012F968,extended,34649999 //3464cccd patch=0,EE,2012F9C8,extended,3C023F19 //3c023f4c patch=0,EE,2012F9CC,extended,34439999 //3443cccd patch=0,EE,2012FB38,extended,3C033F19 //3c033f4c patch=0,EE,2012FB40,extended,34639999 //3463cccd patch=0,EE,2012FBB0,extended,3C02C3D6 //3c02c3a0 patch=0,EE,2012FAA0,extended,3C024527 //3c0244fa  ////https://forums.pcsx2.net/Thread-No-interlacing-codes?pid=619401#pid619401 //！！将 CRC Hack 级别更改为“无（调试）”！！ //！！推荐的 HW 2X+ 模式（软件太模糊/块状图像）也启用此选项 PCSX2&gt;Config&gt;Video (GS)&gt;plugin settings&gt;"Enable HW Hacks"&gt;Advanced Settings and Hacks&gt;Half-pixel Offset: "Special (Texture)"用于修复一些放大错位” //+添加部分“无后效”（最小化/禁用模糊，游戏中的自由度 -重要的过场动画）（图像更清晰） //*修复未对齐的放大 //+禁用寄存器/效果/功能瓶颈GS/GPU，给性能提升“v1测试代码” //*在集成 vega11 gpu 的 ryzen 3400g 中几乎以 60fps 的速度播放 HW 3x //+来自 kozarov 的 IPU hack 端口（美国版） //*游戏将显示“较少损坏的图像”和视频/控制台没有卡顿或崩溃 //+Partial No Interleacing 端口代码（视频和菜单/存储卡背景仍然抖动） //+添加解决崩溃代码（此游戏版本缺少PCSX2数据库中的“崩溃解决代码”） //-第二个磁盘检查但没有完全测试 //*此游戏版本有英文选项 //-模糊的过场动画（无事可做）//这是代码 v1 游戏具有密集的模糊.dof 后期效果，禁用所有后期效果会使游戏变得苍白/无灵感，所以我禁用了一些糟糕的放大部分模糊 -自由度效果并使游戏更清晰，1 级城镇的设计类似于“西部城镇”所以推荐污垢、风等效果，现在这个游戏几乎有随机的 ram 结果值写入每个场景（或多或少测试过激烈的游戏 1 小时一切看起来都不错）“也许”在长时间播放模糊或自由度重新出现看起来如果发生错位效果（如残像），（需要检查并添加更多代码）。如果游戏崩溃长时间播放禁用（效果测试代码块）并再次测试。复制代码

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| Suljo| + 1|好评加鹅|

查看全部评分

*****

####  Jumbohard  
##### 262#       发表于 2021-12-4 19:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808222&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 19:18</a>

ps4手柄能用？什么平板

----STAGE1 Mobile</blockquote>
基本上大部分安卓设备都能用，蓝牙菜单里面直接配对连接就是。有一个问题是不会自动休眠，每次都需要手动关蓝牙

*****

####  莫再提  
##### 263#       发表于 2021-12-4 19:29

问个弱智问题，怎么设置全屏？默认打开是竖屏的……

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  cuchulain2021  
##### 264#       发表于 2021-12-4 19:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808306&amp;ptid=2037739" target="_blank">莫再提 发表于 2021-12-4 19:29</a>

问个弱智问题，怎么设置全屏？默认打开是竖屏的……

  -- 来自 有消息提醒的 Stage1官方 Android客户端 ...</blockquote>
general里面的emulation screen orientation选landscape

*****

####  DaveZED  
##### 265#       发表于 2021-12-4 19:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808164&amp;ptid=2037739" target="_blank">susan28 发表于 2021-12-4 19:12</a>
有人跑战神2吗？能玩吗？

—— 来自 OPPO PCLM10, Android 10上的 S1Next-鹅版 v2.0.4-play ...</blockquote>
我三星note10+卡到批爆<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  Jumbohard  
##### 266#       发表于 2021-12-4 19:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808070&amp;ptid=2037739" target="_blank">保科智子 发表于 2021-12-4 19:04</a>

麒麟990一到3D就完全不行。华为系绝望了吗？</blockquote>
？我的感觉还好啊，你的是什么游戏？

*****

####  慕容断月  
##### 267#       发表于 2021-12-4 19:40

有人测了北妹2吗？丧失之森直接闪退，啥都不好使

*****

####  莫再提  
##### 268#       发表于 2021-12-4 19:43

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808325&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-04 19:31:07</a>
general里面的emulation screen orientation选landscape</blockquote>啊…谢谢，…但用的前面坛友发布的中文版……不晓得对应的是哪个？

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  cuchulain2021  
##### 269#       发表于 2021-12-4 19:43

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808425&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-4 19:40</a>

有人测了北妹2吗？丧失之森直接闪退，啥都不好使</blockquote>
测过了，卡，第一个游戏场景只有3x帧

*****

####  navarra  
##### 270#       发表于 2021-12-4 19:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808349&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 19:33</a>

我三星note10+卡到批爆

—— 来自 samsung SM-N976N, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
渲染换成vulkan试试



*****

####  莫再提  
##### 271#       发表于 2021-12-4 19:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808325&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-04 19:31:07</a>
general里面的emulation screen orientation选landscape</blockquote>原来是我把手机屏幕方向锁了，没问题了，谢谢啦

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  cuchulain2021  
##### 272#       发表于 2021-12-4 19:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808446&amp;ptid=2037739" target="_blank">莫再提 发表于 2021-12-4 19:43</a>

啊…谢谢，…但用的前面坛友发布的中文版……不晓得对应的是哪个？

  -- 来自 能搜索的 Stage1官方 Androi ...</blockquote>
设置第一页，倒数第三个选项，然后选倒数第二个

另外中文版有bug，推荐使用原版

*****

####  慕容断月  
##### 273#       发表于 2021-12-4 19:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53806006&amp;ptid=2037739" target="_blank">被雨困住的城市 发表于 2021-12-4 14:44</a>

352的模拟还是存在问题啊，865卡得不行T T</blockquote>

<img src="https://img.saraba1st.com/forum/202112/04/194716v8xemw8nhsuoewhm.jpg" referrerpolicy="no-referrer">

<strong>1.jpg</strong> (168.95 KB, 下载次数: 0)

下载附件

2021-12-4 19:47 上传

同865，红米k30pro，1x分辨率100+，开2X也是100+，人堆里也不掉

*****

####  慕容断月  
##### 274#       发表于 2021-12-4 19:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808447&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 19:43</a>

测过了，卡，第一个游戏场景只有3x帧</blockquote>
怎么过的？我点进丧失之森app就闪退了

*****

####  被雨困住的城市  
##### 275#       发表于 2021-12-4 19:51

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  cuchulain2021  
##### 276#       发表于 2021-12-4 19:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808508&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-4 19:48</a>

怎么过的？我点进丧失之森app就闪退了</blockquote>
港口就只有一半帧数了啊……也不需要测后面的了吧

*****

####  精钢魔像  
##### 277#       发表于 2021-12-4 19:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808546&amp;ptid=2037739" target="_blank">被雨困住的城市 发表于 2021-12-4 19:51</a>

请问您是怎么设置的T T</blockquote>
你没开vulkan吧

*****

####  慕容断月  
##### 278#       发表于 2021-12-4 19:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808546&amp;ptid=2037739" target="_blank">被雨困住的城市 发表于 2021-12-4 19:51</a>

请问您是怎么设置的T T</blockquote>
默认设置，啥都没动，opengl改成vulkan

*****

####  JudgmentEye  
##### 279#       发表于 2021-12-4 19:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808301&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-4 19:28</a>

基本上大部分安卓设备都能用，蓝牙菜单里面直接配对连接就是。有一个问题是不会自动休眠，每次都需要手动 ...</blockquote>
ds4连上了，但按一下半天才有反应，然后连键？

*****

####  慕容断月  
##### 280#       发表于 2021-12-4 19:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808557&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 19:52</a>

港口就只有一半帧数了啊……也不需要测后面的了吧</blockquote>
港口是一半，第二个场景直接90+

那当然要测下丧失之森吧，不会都只测了第一个场景吧。。。。。。。。。<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  慕容断月  
##### 281#       发表于 2021-12-4 19:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808559&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-4 19:52</a>

你没开vulkan吧</blockquote>
865就算不开也有60+，我刚测了352m，opengl有62+，最低58，这还是两倍分率下

*****

####  JudgmentEye  
##### 282#       发表于 2021-12-4 20:01

ds4用蓝牙连接到核弹shield上没问题，玩格斗完美无延迟

*****

####  彩虹肥宅  
##### 283#       发表于 2021-12-4 20:02

求个国行ps2的bios

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  cuchulain2021  
##### 284#       发表于 2021-12-4 20:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808584&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-4 19:54</a>

港口是一半，第二个场景直接90+

那当然要测下丧失之森吧，不会都只测了第一个场景吧。。。。。。。。。[f ...</blockquote>
那前面都卡了后面还有啥测的必要么……另外之前也有个说闪退的，应该是普遍问题了

高达无双2第一个场景倒是满帧，这么看无双类支持都还不错

*****

####  保科智子  
##### 285#       发表于 2021-12-4 20:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808408&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-4 19:39</a>
？我的感觉还好啊，你的是什么游戏？</blockquote>
你怎么设置的？
试了新鬼60%，山脊赛车比赛个位数，皇牌0菜单不正常，进场景个位数。基本上不如660的小米。<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  DaveZED  
##### 286#       发表于 2021-12-4 20:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808460&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-4 19:44</a>
渲染换成vulkan试试</blockquote>
渲染换vulkan画面就灰了，现在用着opengl开了ee超频，但还是有点慢动作<img src="https://static.saraba1st.com/image/smiley/face2017/010.png" referrerpolicy="no-referrer">
<img src="https://p.sda1.dev/3/a8687b6e06274bc304d55569f6a7cfc2/IMG_CMP_252077576.jpeg" referrerpolicy="no-referrer">

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  被雨困住的城市  
##### 287#       发表于 2021-12-4 20:21

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  JudgmentEye  
##### 288#       发表于 2021-12-4 20:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808683&amp;ptid=2037739" target="_blank">彩虹肥宅 发表于 2021-12-4 20:02</a>

求个国行ps2的bios

—— 来自 Xiaomi MI 6, Android 9上的 S1Next-鹅版 v2.5.2</blockquote>
往前翻，我发的汉化版下载地址里有

*****

####  DaveZED  
##### 289#       发表于 2021-12-4 20:28

换成vulkan怎么变这样了<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">
是不是这猎户座soc实在太拉了<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

—— 来自 samsung SM-N976N, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  navarra  
##### 290#       发表于 2021-12-4 20:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53809036&amp;ptid=2037739" target="_blank">DaveZED 发表于 2021-12-4 20:28</a>

换成vulkan怎么变这样了

是不是这猎户座soc实在太拉了</blockquote>
哦你是猎户座受害者啊......这模拟器对高通平台优化十分牛逼，其他平台就抱歉了- -

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| DaveZED| + 1|那就只能等换手机了|

查看全部评分

*****

####  Jumbohard  
##### 291#       发表于 2021-12-4 20:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808719&amp;ptid=2037739" target="_blank">保科智子 发表于 2021-12-4 20:05</a>

你怎么设置的？

试了新鬼60%，山脊赛车比赛个位数，皇牌0菜单不正常，进场景个位数。基本上不如660的小米 ...</blockquote>
我是用的深渊传说……基本默认设置，小场景能开5x分辨率，大场景能开3x分辨率，除了鬼影问题之外基本没有任何问题。大概是游戏个体差异？

*****

####  Jumbohard  
##### 292#       发表于 2021-12-4 20:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808582&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 19:54</a>

ds4连上了，但按一下半天才有反应，然后连键？</blockquote>
可能是干扰太大了吧？我在小米华为一加的设备上都试过连ps4手柄，感觉都没有遇到过这个问题

*****

####  彩虹肥宅  
##### 293#       发表于 2021-12-4 20:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808990&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-4 20:25</a>
往前翻，我发的汉化版下载地址里有</blockquote>
多谢

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  月夜凝雪  
##### 294#       发表于 2021-12-4 21:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53809052&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-4 20:29</a>

哦你是猎户座受害者啊......这模拟器对高通平台优化十分牛逼，其他平台就抱歉了- - ...</blockquote>
那么麒麟还好吧？

*****

####  古畑任三郎2015  
##### 295#       发表于 2021-12-4 21:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53809724&amp;ptid=2037739" target="_blank">月夜凝雪 发表于 2021-12-4 21:09</a>
那么麒麟还好吧？</blockquote>
vulkan不行,会闪退
不过opengl基本够用，大多数都能满速

*****

####  Meltina  
##### 296#       发表于 2021-12-4 21:56

试了试龙战士5，终于满速了，呆萌这么久都是拖慢，一直没解决的，今天毫不犹豫把呆萌删了，其实也没怎么用过

*****

####  杉田悠一  
##### 297#       发表于 2021-12-4 22:02

没错，我当时买256G的865手机就是为了后来会出现的这个PS2模拟器了，这个CPU和容量终于能用上了<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">

*****

####  未熟串烧  
##### 298#       发表于 2021-12-4 22:32

从老男人现下了一个ogs玩没问题<img src="https://static.saraba1st.com/image/smiley/face2017/056.gif" referrerpolicy="no-referrer">
说起来我是从gba的og系列直接跳到2og的，借此机会可以通一下<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  黄金时代  
##### 299#       发表于 2021-12-4 22:35

现在只有一个问题，怎么才能从天杀的呆萌里面导出存档数据

*****

####  saberserker  
##### 300#       发表于 2021-12-4 22:36

 本帖最后由 saberserker 于 2021-12-4 23:12 编辑 

试了一圈，唯独机战MX没法正常玩，OpenGL开头菜单和战斗动画帧数巨低，vulkan游戏菜单速度到正常，但是进地图就跳出，再就是机战Z用opengl战斗也掉帧，换vulkan速度正常但是有头像透明的老问题。

这预设的虚拟按键位置好别扭，是不是还不能自定义。

调了下设置，OpenGL下点了GPU Palette Conversion这个选项机战Z战斗动画速度正常了，同时点GPU Palette Conversion和Preload Textures这两个，机战MX的速度也正常了。

<img src="https://img.saraba1st.com/forum/202112/04/231221js2cs6b52gse4e22.jpg" referrerpolicy="no-referrer">

<strong>20211204231158.jpg</strong> (322.95 KB, 下载次数: 0)

下载附件

2021-12-4 23:12 上传



*****

####  拉姆扎  
##### 301#       发表于 2021-12-4 22:41

mark下，等机战og相关完整设置。

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  LuciferGX  
##### 302#       发表于 2021-12-4 22:44

865+机器
武神0试了下开头，几乎完美，开2X会拖慢
贝维克传说用vulkan菜单会花屏，opengl没问题
真女神转生3速度正常但是画面有bug，不知道怎么调
北妹2开1X港口帧数在70%，开2X直接卡到没法玩，没继续试

另外用16：9玩奥丁领域，左右超出4：3的部分显示有问题，吸收魔晶也会有点花，搞了半天没解决。
这个是不是玩PSP的加强版更好？ 

*****

####  saki0511  
##### 303#       发表于 2021-12-4 22:52

870在Vulcan模式下大部分3d游戏满速60帧，终于可以在手机上搓ps2版fate uc了。
<img src="http://p.sda1.dev/3/5a3c7528ec22a069939b2fea580d1e4b/IMG_CMP_226403063.jpeg" referrerpolicy="no-referrer"> 

—— 来自 vivo V2118A, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  JudgmentEye  
##### 304#       发表于 2021-12-4 22:53

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811359&amp;ptid=2037739" target="_blank">黄金时代 发表于 2021-12-4 22:35</a>

现在只有一个问题，怎么才能从天杀的呆萌里面导出存档数据</blockquote>
用root的机器搜索内存里的记录卡2进制数据？我没试过不知道是不是加密的

*****

####  小天女  
##### 305#       发表于 2021-12-4 22:54

更新：晚上试了一下另外一个游戏『多罗罗』，不行，帧数只有平均15帧。不知道是不是华为麒麟芯片的问题。

<img src="https://img.saraba1st.com/forum/202112/04/225353wyuhcjvycubvpv9z.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_20211204_223733_xyz.aethersx2.android_edit_405542968155304.jpg</strong> (163.42 KB, 下载次数: 0)

下载附件

2021-12-4 22:53 上传

*****

####  妖妖忍  
##### 306#       发表于 2021-12-4 22:58

<blockquote>小天女 发表于 2021-12-4 22:54
更新：晚上试了一下另外一个游戏『多罗罗』，不行，帧数只有平均15帧。不知道是不是华为麒麟芯片的问题。 ...</blockquote>
废话 当然是了 说了要用高通的大哥 咋不看帖呢

*****

####  月夜凝雪  
##### 307#       发表于 2021-12-4 23:01

 本帖最后由 月夜凝雪 于 2021-12-4 23:12 编辑 

田鸡1000+，默认设置战神2前面CG还是60帧的，开始操作就只有30了，开Vulkan就和前面猎户座的一样黑白了

零红蝶只有开始界面启动游戏后黑屏，看来只有高通的机子可以啊

<img src="https://img.saraba1st.com/forum/202112/04/230009llh2bgbvv4aea0vc.jpg" referrerpolicy="no-referrer">

<strong>QQ图片20211204225852.jpg</strong> (264.61 KB, 下载次数: 0)

下载附件

2021-12-4 23:00 上传

*****

####  谷恒条野  
##### 308#         楼主| 发表于 2021-12-4 23:06

测了几个手柄
wee1代∶按键，休眠，唤醒正常
八位堂lite:同上
ipega 9087s:按键正常，但是一休眠或者唤醒，模拟器会重置游戏。
真是奇怪的问题。<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  小天女  
##### 309#       发表于 2021-12-4 23:12

<blockquote>妖妖忍 发表于 2021-12-4 22:58
废话 当然是了 说了要用高通的大哥 咋不看帖呢</blockquote>
我手里只有一台华为手机和一个还是骁龙660的平板，只是图个热闹发个结果分享下而已。如果不喜我就不发了。所以我看帖了又有啥用…毕竟有几个游戏还是正常的，现在就去为了几个老游戏买台新骁龙手机也不现实。明年等新的骁龙gen出货看看情况再说了，不急。

*****

####  docklabor  
##### 310#       发表于 2021-12-4 23:34

ps2上还有哪些不错的jrpg是没出过官方手机版的？

*****

####  ogloc  
##### 311#       发表于 2021-12-4 23:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811378&amp;ptid=2037739" target="_blank">saberserker 发表于 2021-12-4 22:36</a>

试了一圈，唯独机战MX没法正常玩，OpenGL开头菜单和战斗动画帧数巨低，vulkan游戏菜单速度到正常，但是进地 ...</blockquote>
我按了你这个设置调，OGS战斗全速了，835的机子，之前战斗还卡现在不卡了。不过地图画面45帧数左右，花3倒是全程顺滑全速

*****

####  b091882  
##### 312#       发表于 2021-12-5 00:02

vulkan慎用，不少会中途跳出，影之心看这个直接卡死，当然也可能是855太挫了。

*****

####  rick343  
##### 313#       发表于 2021-12-5 00:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811524&amp;ptid=2037739" target="_blank">LuciferGX 发表于 2021-12-4 22:44</a>

865+机器

武神0试了下开头，几乎完美，开2X会拖慢

贝维克传说用vulkan菜单会花屏，opengl没问题</blockquote>
奥丁领域没有psp版吧

*****

####  杉田悠一  
##### 314#       发表于 2021-12-5 00:51

试了几个镜像，真不戳啊，可以在手机上过一遍4部花3部OG了，能玩到地球毁灭，

*****

####  月夜凝雪  
##### 315#       发表于 2021-12-5 01:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53812568&amp;ptid=2037739" target="_blank">ogloc 发表于 2021-12-4 23:56</a>

我按了你这个设置调，OGS战斗全速了，835的机子，之前战斗还卡现在不卡了。不过地图画面45帧数左右，花3 ...</blockquote>
感觉我的XZ1可以拿出来了

*****

####  LuciferGX  
##### 316#       发表于 2021-12-5 01:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53812658&amp;ptid=2037739" target="_blank">rick343 发表于 2021-12-5 00:05</a>

奥丁领域没有psp版吧</blockquote>
看了下是PSV的 <img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  Xenor  
##### 317#       发表于 2021-12-5 03:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811524&amp;ptid=2037739" target="_blank">LuciferGX 发表于 2021-12-4 22:44</a>

865+机器

武神0试了下开头，几乎完美，开2X会拖慢

贝维克传说用vulkan菜单会花屏，opengl没问题</blockquote>
推荐去玩PS3的加强版，非常不错，Rpcs3完美

*****

####  Rai.Z  
##### 318#       发表于 2021-12-5 09:51

找了半天没看到哪里调右摇杆，玩OGS不能拉视角不爽（

*****

####  希德尼娅  
##### 319#       发表于 2021-12-5 10:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53814534&amp;ptid=2037739" target="_blank">Rai.Z 发表于 2021-12-5 09:51</a>

找了半天没看到哪里调右摇杆，玩OGS不能拉视角不爽（</blockquote>
控制器设置里选dual analog

*****

####  neh3  
##### 320#       发表于 2021-12-5 10:46

加载bios闪退怎么办

—— 来自 vivo V1813A, Android 8.1.0上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  kerbad  
##### 321#       发表于 2021-12-5 10:47

想玩TOL来着，但是只有差不多30%的运行速度……<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

*****

####  tyauto  
##### 322#       发表于 2021-12-5 11:07

测试版就有这水平，期待正式版<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">

*****

####  被雨困住的城市  
##### 323#       发表于 2021-12-5 11:12

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  JudgmentEye  
##### 324#       发表于 2021-12-5 11:14

<blockquote>引用第319楼neh3于2021-12-05 10:46发表的  :

加载bios闪退怎么办—— 来自 vivo V1813A, Android 8.1.0上的 S1Ne......</blockquote>
确认是4m的bin，给模拟器存储访问权限

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  飞侠小黑  
##### 325#       发表于 2021-12-5 11:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808177&amp;ptid=2037739" target="_blank">Jumbohard 发表于 2021-12-4 19:13</a>
试了下深渊传说，麒麟990开3x原生分辨率FXAA能稳定60帧，感觉还留有一些拉分辨率、加滤镜之类的余地

但是选 ...</blockquote>
这模拟器目前感觉opengl下面帧数画质都要比vulk更高。而且麒麟不支持vulk，一开就黑屏了

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.2.2.1

*****

####  飞侠小黑  
##### 326#       发表于 2021-12-5 11:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53808282&amp;ptid=2037739" target="_blank">cuchulain2021 发表于 2021-12-4 19:25</a>
一加8t

零zero大部分场景都是60，不过有时候会出现小掉帧，不知道为什么</blockquote>
我重新测试了一下，原来是9000没开性能模式，开了性能模式就比8t强多了，8t的刺青之声开2x同样场景只能40帧，9000可以跑到50多

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.2.2.1

*****

####  被雨困住的城市  
##### 327#       发表于 2021-12-5 11:33

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  飞侠小黑  
##### 328#       发表于 2021-12-5 11:46

 本帖最后由 飞侠小黑 于 2021-12-5 11:51 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811688&amp;ptid=2037739" target="_blank">小天女 发表于 2021-12-4 22:54</a>
更新：晚上试了一下另外一个游戏『多罗罗』，不行，帧数只有平均15帧。不知道是不是华为麒麟芯片的问题。 ...</blockquote>
这游戏应该就是麒麟不行，我9000开了性能模式在开始那个场景只有30多帧，但是865跑这个场景可以在x2分辨率情况下跑到满<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">
<img src="https://p.sda1.dev/3/a96fededa173e61e0b8201d73661512a/IMG_CMP_176261972.jpeg" referrerpolicy="no-referrer">
—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  KOGmk2  
##### 329#       发表于 2021-12-5 11:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53812004&amp;ptid=2037739" target="_blank">小天女 发表于 2021-12-4 23:12</a>

我手里只有一台华为手机和一个还是骁龙660的平板，只是图个热闹发个结果分享下而已。如果不喜我就不发了 ...</blockquote>
Adreno尊享,Mali西奈......

*****

####  被雨困住的城市  
##### 330#       发表于 2021-12-5 12:15

提示: 作者被禁止或删除 内容自动屏蔽



*****

####  红叶  
##### 331#       发表于 2021-12-5 12:19

幻想传说2中文版偶尔会花屏 要怎么设置啊

—— 来自 Xiaomi M2102J2SC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  飞侠小黑  
##### 332#       发表于 2021-12-5 12:38

继续更新一下测试
星海3初始地图可以跑4x分辨率 60帧，麒麟9000和高通865都可以，并且没有开门闪退的bug。

呆萌请赶快去死<img src="https://p.sda1.dev/3/795eb347ecdffd7c9011c53a77961038/IMG_CMP_88814657.jpeg" referrerpolicy="no-referrer">

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  ΑΑ  
##### 333#       发表于 2021-12-5 12:44

试了试玩不了nfs

*****

####  希德尼娅  
##### 334#       发表于 2021-12-5 12:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53815538&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-5 11:46</a>
这游戏应该就是麒麟不行，我9000开了性能模式在开始那个场景只有30多帧，但是865跑这个场景可以在x2分辨 ...</blockquote>
gpu rendering用software，帧数比opengl还高

*****

####  飞侠小黑  
##### 335#       发表于 2021-12-5 13:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53816035&amp;ptid=2037739" target="_blank">希德尼娅 发表于 2021-12-5 12:48</a>
gpu rendering用software，帧数比opengl还高</blockquote>
9000开了software只有地图没有其他图像 <img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  oskneo  
##### 336#       发表于 2021-12-5 13:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53812622&amp;ptid=2037739" target="_blank">b091882 发表于 2021-12-5 00:02</a>
vulkan慎用，不少会中途跳出，影之心看这个直接卡死，当然也可能是855太挫了。 ...</blockquote>
顺便问一下pc玩影之心怎样设置，貌似问题很大

—— 来自 Sony XQ-AT52, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  保科智子  
##### 337#       发表于 2021-12-5 13:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53812004&amp;ptid=2037739" target="_blank">小天女 发表于 2021-12-4 23:12</a>

我手里只有一台华为手机和一个还是骁龙660的平板，只是图个热闹发个结果分享下而已。如果不喜我就不发了 ...</blockquote>
也没那么不堪，我也一个麒麟990一个660，设置超频跳帧开性能模式，新鬼勉强满帧。660稍微慢一点但跑2d基本完美兼容性更好。

*****

####  保科智子  
##### 338#       发表于 2021-12-5 13:39

国行50009的bios用不了，都是这样吗？

*****

####  JudgmentEye  
##### 339#       发表于 2021-12-5 14:07

<blockquote>引用第335楼oskneo于2021-12-05 13:28发表的  :

引用:b091882 发表于 2021-12-5 00:02vulkan慎用，不少会中途跳出，影之心......</blockquote>
1？用软渲染

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  jellyfis  
##### 340#       发表于 2021-12-5 14:13

刚才去呆萌贴吧感受了一下什么叫如丧考妣，断人财路如杀人父母啊

*****

####  lee0709  
##### 341#       发表于 2021-12-5 14:19

用xbox手柄蓝牙连接，发现左右扳机没法对应到L2 R2，你们有这问题么

*****

####  Rai.Z  
##### 342#       发表于 2021-12-5 14:26

<img src="https://static.saraba1st.com/image/smiley/face2017/029.png" referrerpolicy="no-referrer">OGS用2X分辨率战斗背景有黑线，3X显示不全，有解决办法吗？

*****

####  精钢魔像  
##### 343#       发表于 2021-12-5 14:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53816900&amp;ptid=2037739" target="_blank">Rai.Z 发表于 2021-12-5 14:26</a>

OGS用2X分辨率战斗背景有黑线，3X显示不全，有解决办法吗？</blockquote>
话说手机那么小的屏幕，1x还不够么

*****

####  卡普空  
##### 344#       发表于 2021-12-5 14:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53817092&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-5 14:49</a>

话说手机那么小的屏幕，1x还不够么</blockquote>
不够，屏幕是小，但是屏幕ppi可不小，ps2也就是480p水平

*****

####  彩虹肥宅  
##### 345#       发表于 2021-12-5 15:46

 本帖最后由 彩虹肥宅 于 2021-12-5 15:48 编辑 

啥时候能有480p 1x分辨率流畅通杀ps2的的寨机

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  samchen007  
##### 346#       发表于 2021-12-5 15:53

 第三次ALPHA终于能正常玩了，之前呆萌号称要修BUG然后就太监了，这回这个AETHERSX2打脸打的太爽了。

*****

####  古畑任三郎2015  
##### 347#       发表于 2021-12-5 16:20

话说这个模拟器怎么自动匹配游戏封面？

*****

####  lyt77777  
##### 348#       发表于 2021-12-5 17:16

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805422&amp;ptid=2037739" target="_blank">highsky 发表于 2021-12-04 13:31:15</a>
你搞反了吧，最近寨机界都沸腾了

不说用845的odin出来后通吃ps2了

就连soc用的很烂的rp2.5都能跑跑机 ...</blockquote>哈，就寨机这点存储，你指望能放几个iso啊？<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  highsky  
##### 349#       发表于 2021-12-5 17:54

 本帖最后由 highsky 于 2021-12-5 17:55 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53818356&amp;ptid=2037739" target="_blank">lyt77777 发表于 2021-12-5 17:16</a>

哈，就寨机这点存储，你指望能放几个iso啊？

  -- 来自 能搜索的 Stage1官方 Android客户端 ...</blockquote>
????

tf卡随意加的好不好目前所知的rp2.5和奥丁都能加tf卡

*****

####  三级怪兽  
##### 350#       发表于 2021-12-5 18:18

<blockquote>lyt77777 发表于 2021-12-5 17:16
哈，就寨机这点存储，你指望能放几个iso啊？

  -- 来自 能搜索的 Stage1官方 Android客户端 ...</blockquote>
而且chd压缩率还挺可观的，沙尘之锁直接chd到840m了

*****

####  罐子  
##### 351#       发表于 2021-12-5 18:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53805473&amp;ptid=2037739" target="_blank">ogloc 发表于 2021-12-4 13:35</a>
我用835玩花3，全速运行，体验太好了，晚点测试OGS， 以前用呆萌玩OGS都不到30帧，卡死 ...</blockquote>
有战斗菜单和头像问题吗

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  杉田悠一  
##### 352#       发表于 2021-12-5 18:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53818356&amp;ptid=2037739" target="_blank">lyt77777 发表于 2021-12-5 17:16</a>
哈，就寨机这点存储，你指望能放几个iso啊？

  -- 来自 能搜索的 Stage1官方 Android客户端 ...</blockquote>
安卓不知道，君正那些机器甚至系统存储都不是焊死的颗粒，都是可以插两张tf卡的，

*****

####  tbtbtbb  
##### 353#       发表于 2021-12-5 19:01

如何限速呀，三国无双2 VULKAN模式 2X分辨率 300帧完全快得没法玩

*****

####  xxrk  
##### 354#       发表于 2021-12-5 19:19

宿命传说导演剪辑版黑屏死机进不了游戏，异度传说3会卡

*****

####  黄金时代  
##### 355#       发表于 2021-12-5 19:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53819135&amp;ptid=2037739" target="_blank">罐子 发表于 2021-12-5 18:37</a>
有战斗菜单和头像问题吗

—— 来自 OnePlus KB2000, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
完全没有，画面完美，没有一丝抖动，已经打穿一轮了

*****

####  kiriko  
##### 356#       发表于 2021-12-5 19:47

<img src="https://static.saraba1st.com/image/smiley/face2017/180.png" referrerpolicy="no-referrer">果然移植的模拟器BUG也完全一致吗，推荐大家遇到问题也去看看。
[https://pcsx2.net/compatibility-list.html](https://pcsx2.net/compatibility-list.html)

*****

####  lyt77777  
##### 357#       发表于 2021-12-5 20:23

因为代码都是PCSX2的，所以我先提个醒，网球王子SH2和最强队伍集结都会五分钟强退，不可解。

非常可惜，这是网王最正经也是最好的两作了。

另外寒蝉需要调整内部声音参数，请参考PCSX2官网调整。

*****

####  古畑任三郎2015  
##### 358#       发表于 2021-12-5 21:13

话说你们谁试过凡人物语么，调了几次，人数多于3个的时候，就要掉到40帧以下

*****

####  好想毕业  
##### 359#       发表于 2021-12-5 21:20

玩2D游戏，用GPU渲染的话开菜单会卡一下，和 PCSX2 一样。但是软件渲染出错拖慢（毕竟移动U），PCSX2 倒是正确且保证性能。

*****

####  平井姨夫  
##### 360#       发表于 2021-12-5 21:20

现在玩PS2模拟器的手机有推荐的吗？应该要散热好还有非全面屏？



*****

####  Porsche  
##### 361#       发表于 2021-12-5 21:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53820862&amp;ptid=2037739" target="_blank">平井姨夫 发表于 2021-12-5 21:20</a>
现在玩PS2模拟器的手机有推荐的吗？应该要散热好还有非全面屏？</blockquote>
如果835没问题的话，你家的xz1c啊<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  wcorvo  
##### 362#       发表于 2021-12-5 23:24

机战z和@3能完美运行了嘛

*****

####  飞侠小黑  
##### 363#       发表于 2021-12-5 23:51

 本帖最后由 飞侠小黑 于 2021-12-6 00:03 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53820800&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-12-5 21:13</a>
话说你们谁试过凡人物语么，调了几次，人数多于3个的时候，就要掉到40帧以下 ...</blockquote>
估计是性能不行，9000跑战斗大概在150帧左右<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">  把渲染线程调成6个会快一些，默认是3个。
<img src="https://p.sda1.dev/3/57f4456e534d5e9482f88706eeeaba04/IMG_CMP_28936387.jpeg" referrerpolicy="no-referrer">

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  慕容断月  
##### 364#       发表于 2021-12-6 00:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53815216&amp;ptid=2037739" target="_blank">被雨困住的城市 发表于 2021-12-5 11:12</a>

想问您一个问题，您的352和352m的镜像是多大，可以分享一下吗，谢谢！</blockquote>
我是早年A9PS2区无题大佬和另一位大佬做的宽屏合盘版（忘了是不是宽屏，但一定是合盘版）

链接: [https://pan.baidu.com/s/1pfPWl-VGSBp2Me9Cljb0UA](https://pan.baidu.com/s/1pfPWl-VGSBp2Me9Cljb0UA) 提取码: 3egb

已经转成CHD格式了，1.7版PCSX2和AetherSX2可以直接用

要玩原版内容在Original按钮那里进去以后看提示按两次start就行了

中文版没有

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| jbowin| + 1|好评加鹅|

查看全部评分

*****

####  JudgmentEye  
##### 365#       发表于 2021-12-6 00:45

 本帖最后由 JudgmentEye 于 2021-12-6 00:47 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53820862&amp;ptid=2037739" target="_blank">平井姨夫 发表于 2021-12-5 21:20</a>

现在玩PS2模拟器的手机有推荐的吗？应该要散热好还有非全面屏？</blockquote>
可以外接手柄的865游戏手机，屏最大的是黑鲨3pro吧，不知道能不能认出实体肩键

*****

####  古畑任三郎2015  
##### 366#       发表于 2021-12-6 01:06

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53822434&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-5 23:51</a>
估计是性能不行，9000跑战斗大概在150帧左右  把渲染线程调成6个会快一些，默认是3个。</blockquote>
战斗以外场景呢？我是平常过剧情慢，980应该也还可以吧

*****

####  精钢魔像  
##### 367#       发表于 2021-12-6 01:12

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53820862&amp;ptid=2037739" target="_blank">平井姨夫 发表于 2021-12-5 21:20</a>

现在玩PS2模拟器的手机有推荐的吗？应该要散热好还有非全面屏？</blockquote>
双11价1550元 870 8+256的摩托edge s，应该没比这个能打的了

能插tf卡

能type-c投屏。不过投屏很耗电

*****

####  保科智子  
##### 368#       发表于 2021-12-6 01:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53823049&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-6 01:12</a>
双11价1550元 870 8+256的摩托edge s，应该没比这个能打的了

能插tf卡

能type-c投屏。不过投屏很耗电 ...</blockquote>
我觉得还得再加个立体声。
有横屏后双侧喇叭的手机吗？

*****

####  yujie  
##### 369#       发表于 2021-12-6 07:01

不知道玩机战MX回音问题解决没有，解决的话就可以重温了

*****

####  被雨困住的城市  
##### 370#       发表于 2021-12-6 07:13

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  Cray  
##### 371#       发表于 2021-12-6 07:26

<blockquote>引用第367楼保科智子于2021-12-06 01:40发表的  :

引用:精钢魔像 发表于 2021-12-6 01:12双11价1550元 870 8+256的摩托e......</blockquote>
索尼旗舰99%的机型都是正面双扬声器

----发送自 [Sony H8296,Android 9](http://stage1.5j4m.com/?1.37)

*****

####  飞侠小黑  
##### 372#       发表于 2021-12-6 07:37

 本帖最后由 飞侠小黑 于 2021-12-6 08:52 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53823005&amp;ptid=2037739" target="_blank">古畑任三郎2015 发表于 2021-12-6 01:06</a>
战斗以外场景呢？我是平常过剧情慢，980应该也还可以吧</blockquote>
看场景，大部分时候应该是七八十帧，低的时候也有四十多，高的时候一百几十。
980的gpu性能还是过于孱弱了一些，这模拟器本身对麒麟的优化就比高通差，我测试下来的游戏，9000比865性能强这么多的情况下，大部分游戏还是865跑的更流畅，更不要说比865性能低的980了，我觉得对980的定位应该是能玩就行。
ps：华为手机记得开性能模式

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  梦窗  
##### 373#       发表于 2021-12-6 09:37

<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">手头有一台不能插卡的夏普R3，好屏幕骁龙855，有人要吗？

*****

####  路西恩  
##### 374#       发表于 2021-12-6 10:28

天机1000+

小米

默认设置能跑FFX，可能还需要调教一下参数

*****

####  ogloc  
##### 375#       发表于 2021-12-6 11:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53819135&amp;ptid=2037739" target="_blank">罐子 发表于 2021-12-5 18:37</a>

有战斗菜单和头像问题吗

—— 来自 OnePlus KB2000, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
没有任何问题，花2花3 OGS都完美，我又试用主力机玩，870的U甚至都不用任何设置，开始引导直接选高性能模式，什么都不用调，机战全速完美无任何图形错误

*****

####  Meltina  
##### 376#       发表于 2021-12-6 11:33

我看到有加速帧数的选项，但是不知道怎么触发加速，是可以设置按键加速吗？另外就是再问一个在哪里设置看帧数

*****

####  游公子  
##### 377#       发表于 2021-12-6 11:35

等正式版了，不着急。

*****

####  路西恩  
##### 378#       发表于 2021-12-6 11:44

求救

不小心把触摸屏按钮弄没了

【控制器设置】——【触摸屏控制器试图】

手贱改了个设置，然后触摸屏上所有虚拟按钮都没了

【添加/移除按钮】的选项也灰了

怎么设置回来

*****

####  Dr.Web  
##### 379#       发表于 2021-12-6 11:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53826303&amp;ptid=2037739" target="_blank">路西恩 发表于 2021-12-6 11:44</a>

求救

不小心把触摸屏按钮弄没了</blockquote>
就touchscren 第一个选项, none就是没有,  选下面三个都可以(摇杆数量不同). 默认设置是单摇杆那个.

*****

####  JudgmentEye  
##### 380#       发表于 2021-12-6 12:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53826169&amp;ptid=2037739" target="_blank">Meltina 发表于 2021-12-6 11:33</a>

我看到有加速帧数的选项，但是不知道怎么触发加速，是可以设置按键加速吗？另外就是再问一个在哪里设置看帧 ...</blockquote>
点暂停然后toggle frame limiter

*****

####  慕容断月  
##### 381#       发表于 2021-12-6 12:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53823897&amp;ptid=2037739" target="_blank">被雨困住的城市 发表于 2021-12-6 07:13</a>
谢谢！还有个问题哈，我用我自己下载的两个镜像，联动不成功该怎么办呢 ...</blockquote>
放弃吧，直接用我这个，体积小还省事，进游戏直接两下start就联动成功

*****

####  保科智子  
##### 382#       发表于 2021-12-6 12:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53826169&amp;ptid=2037739" target="_blank">Meltina 发表于 2021-12-6 11:33</a>

我看到有加速帧数的选项，但是不知道怎么触发加速，是可以设置按键加速吗？另外就是再问一个在哪里设置看帧 ...</blockquote>
帧数在graphics-show vps

加速在按键设置勾上显示一个加速的虚拟按键，system设置可以调正常和加速的档位。

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| Meltina| + 1|欢乐多|

查看全部评分

*****

####  幽灵胖胖  
##### 383#       发表于 2021-12-6 13:11

用汉化版的会触发虚拟键位丢失的bug

*****

####  JudgmentEye  
##### 384#       发表于 2021-12-6 13:49

谁发个新版？我重新汉化一下

*****

####  杉田悠一  
##### 385#       发表于 2021-12-6 13:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53827399&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-6 13:11</a>

用汉化版的会触发虚拟键位丢失的bug</blockquote>
是的我就是搞没了怎么选也回不来，之后我就打开一直没用过的playstore下了个原版，

*****

####  JudgmentEye  
##### 386#       发表于 2021-12-6 14:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53827837&amp;ptid=2037739" target="_blank">杉田悠一 发表于 2021-12-6 13:54</a>

是的我就是搞没了怎么选也回不来，之后我就打开一直没用过的playstore下了个原版， ...</blockquote>
清空数据存储和缓存重设，设完尽量别改手柄设置

*****

####  sosgame67  
##### 387#       发表于 2021-12-6 14:37

一直提示bios过大无法载入，设置改权限的话貌似没有空间读取的选项..<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

*****

####  JudgmentEye  
##### 388#       发表于 2021-12-6 14:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53828318&amp;ptid=2037739" target="_blank">sosgame67 发表于 2021-12-6 14:37</a>

一直提示bios过大无法载入，设置改权限的话貌似没有空间读取的选项..</blockquote>
bios才4m啊，你机器权限控制问题？

*****

####  sosgame67  
##### 389#       发表于 2021-12-6 14:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53828332&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-6 14:38</a>

bios才4m啊，你机器权限控制问题？</blockquote>
忘记解压缩了，丢人了<img src="https://static.saraba1st.com/image/smiley/face2017/009.gif" referrerpolicy="no-referrer">

*****

####  sosgame67  
##### 390#       发表于 2021-12-6 14:56

顺带求个武神0的资源，网上找的盘载入一直提示插入disc<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">



*****

####  慕容断月  
##### 391#       发表于 2021-12-6 16:21

 本帖最后由 慕容断月 于 2021-12-6 16:23 编辑 

试了一下北妹2，关闭快速内存访问就不会在进丧失之森闪退了，估计后面也一样，总体来说能凑合玩吧，不错了

<img src="https://img.saraba1st.com/forum/202112/06/162329iyz8837yzupcp7lh.png" referrerpolicy="no-referrer">

<strong>Screenshot_20211206-161201.png</strong> (168.78 KB, 下载次数: 0)

下载附件

2021-12-6 16:23 上传

*****

####  谷恒条野  
##### 392#         楼主| 发表于 2021-12-6 17:19

alpha-662

Crash fix for Burnout 2/NBA 2k12, probably others.

Expose more GS settings.

Extract strings for translatability.

*****

####  菜头王子  
##### 393#       发表于 2021-12-6 18:05

干死呆萌那个奥特曼模拟器

*****

####  杉田悠一  
##### 394#       发表于 2021-12-6 18:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53830285&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-6 17:19</a>
alpha-662

Crash fix for Burnout 2/NBA 2k12, probably others.

Expose more GS settings.</blockquote>
656完了就直接662了呀，并且这更新速度真可以，上架两天吧，更新三次了，

*****

####  navarra  
##### 395#       发表于 2021-12-6 18:50

更新完后之前闪退的一些游戏（比如连扎2P）不闪退了......终于可以随时随地玩连扎2了

*****

####  nozomitech  
##### 396#       发表于 2021-12-6 19:40

855试玩了一下P3F，居然可以正常玩，不知后面是什么表现。

*****

####  NEIN  
##### 397#       发表于 2021-12-6 19:53

他都识别哪些手柄啊，连上用不了<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

—— 来自 realme RMX3370, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  精钢魔像  
##### 398#       发表于 2021-12-6 19:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53832120&amp;ptid=2037739" target="_blank">NEIN 发表于 2021-12-6 19:53</a>

他都识别哪些手柄啊，连上用不了

—— 来自 realme RMX3370, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
我用的xsx。蓝牙

*****

####  NEIN  
##### 399#       发表于 2021-12-6 20:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53832155&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-6 19:57</a>
我用的xsx。蓝牙</blockquote>
看来是识别不了杂牌了<img src="https://static.saraba1st.com/image/smiley/face2017/012.png" referrerpolicy="no-referrer">

—— 来自 realme RMX3370, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  桧山修之  
##### 400#       发表于 2021-12-6 20:36

 本帖最后由 桧山修之 于 2021-12-6 20:59 编辑 

有试过影之心2的朋友吗？我手上的索尼865能不能玩？

*****

####  幽灵胖胖  
##### 401#       发表于 2021-12-6 20:39

 本帖最后由 幽灵胖胖 于 2021-12-6 20:40 编辑 

我用飞智WEE一代，安装飞智游戏空间后开启按键映射，完美匹配，机战SL大法屡试不爽，模拟器的SL倒是用的不多<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  jellyfis  
##### 402#       发表于 2021-12-6 21:15

就等一个870的寨机，就完美了

*****

####  幽灵胖胖  
##### 403#       发表于 2021-12-6 22:04

宿命传说1导演剪辑版，打开iso黑屏没反应，有谁行吗

*****

####  拉姆扎  
##### 404#       发表于 2021-12-6 22:26

天玑1000的机器能跑ogs，全部默认没问题，已经打到第八关了，伸手党求个能用金手指全套和外传的<img src="https://static.saraba1st.com/image/smiley/bundam2017/001.png" referrerpolicy="no-referrer">

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  谷恒条野  
##### 405#         楼主| 发表于 2021-12-6 22:59

 本帖最后由 谷恒条野 于 2021-12-6 23:37 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53833705&amp;ptid=2037739" target="_blank">拉姆扎 发表于 2021-12-6 22:26</a>
天玑1000的机器能跑ogs，全部默认没问题，已经打到第八关了，伸手党求个能用金手指全套和外传的

—— 来自 ...</blockquote>
正好也在玩ogs，贴吧找的金手指，汉化版可用。
资金改造一次就变99999999，pp谁战斗谁变9999。
// 金钱最大
patch=1,EE,20199664,extended,3C033000
// pp9999
patch=1,EE,201F0FE0,extended,2412270F
//击坠数999
patch=1,EE,201F12E8,extended,241203E7

*****

####  谷恒条野  
##### 406#         楼主| 发表于 2021-12-6 23:02

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53833705&amp;ptid=2037739" target="_blank">拉姆扎 发表于 2021-12-6 22:26</a>
天玑1000的机器能跑ogs，全部默认没问题，已经打到第八关了，伸手党求个能用金手指全套和外传的

—— 来自 ...</blockquote>
这个是ogg，看贴吧说也有效。
gametitle=超级机器人大战OGG
//SLPS-25836
//PP9999
patch=1,EE,2026A3BC,extended,50C00006
//最大金钱
patch=1,EE,20172F34,extended,3C0205F6
//SP无消耗
patch=1,EE,202727D0,extended,0000102D
//强化部件99
patch=1,EE,20173BA0,extended,00A40821
patch=1,EE,20173BA4,extended,24020063
patch=1,EE,20173BA8,extended,03E00008
patch=1,EE,20173BAC,extended,A02210C8
//LV 1所有精神可使用
patch=1,EE,20272720 ,extended,24020001
//EN减らない
patch=1,EE,20229B90,extended,0000802D
//殘彈數不減
patch=1,EE,20229A84,extended,00000000
//击坠数999
patch=1,EE,20228970 ,extended,00000000

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| 拉姆扎| + 1|好评加鹅|

查看全部评分

*****

####  Porsche  
##### 407#       发表于 2021-12-6 23:12

855默认设置打GT4某些关还会卡，开vulkan会直接闪退
只能继续摸索各种设置选项了

*****

####  lighttt  
##### 408#       发表于 2021-12-7 00:28

用xbox手柄好像不能模拟L1L2R1R2，有人用xbox手柄的吗

*****

####  ZEEROKAMI  
##### 409#       发表于 2021-12-7 00:29

 本帖最后由 ZEEROKAMI 于 2021-12-7 10:22 编辑 

aethersx2 662汉化版

链接：/s/11A0Rq0VYcauRrjYjfSITaA

提取码：bj1y

*****

####  afer  
##### 410#       发表于 2021-12-7 00:31

<img src="https://static.saraba1st.com/image/smiley/face2017/049.png" referrerpolicy="no-referrer">草死呆萌！！！！！！！！！！

*****

####  scstriker  
##### 411#       发表于 2021-12-7 01:01

问个冷门的需求，pixelbook2017能用吗

—— 来自 Xiaomi MIX 2, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  蕾丝  
##### 412#       发表于 2021-12-7 01:11

那么哪里能用手机方便下载到ps2游戏呢

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v1.3.2.1-fix-play

*****

####  被雨困住的城市  
##### 413#       发表于 2021-12-7 01:28

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  qieyifonger  
##### 414#       发表于 2021-12-7 08:18

855，alpha-662，随便测了几个游戏，基本满速，太牛叉了，能在手机上面玩到原汁原味的FF12i汉化版，感动到哭～

—— 来自 Xiaomi Redmi K20 Pro Premium Edition, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  路西恩  
##### 415#       发表于 2021-12-7 08:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53835317&amp;ptid=2037739" target="_blank">afer 发表于 2021-12-7 00:31</a>
草死呆萌！！！！！！！！！！</blockquote>
草死呆萌

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  飞侠小黑  
##### 416#       发表于 2021-12-7 08:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53835304&amp;ptid=2037739" target="_blank">ZEEROKAMI 发表于 2021-12-7 00:29</a>
aethersx2 622汉化版

链接：/s/11A0Rq0VYcauRrjYjfSITaA</blockquote>
最新不是654了吗

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  cuchulain2021  
##### 417#       发表于 2021-12-7 08:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53836724&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-7 08:37</a>
最新不是654了吗

—— 来自 HUAWEI OCE-AN10, Android 10上的 S1Next-鹅版 v2.5.2</blockquote>
他写错了，应该是662

—— 来自 OnePlus KB2000, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  allenz3  
##### 418#       发表于 2021-12-7 10:17

 本帖最后由 allenz3 于 2021-12-15 15:12 编辑 

记录下设置，晓龙865

影之心：GPU Render:Software，Software Rendering Threads:Single Threaded，EE FPU Clamp Mode:Full

樱花大战灼热之血：战斗中Enable Affinity Control:ON，GPU Render:Software，Software Rendering Threads:4 Threads；战斗外GPU Render:Vulkan，Upscale Multiplier:2x Native

*****

####  ZEEROKAMI  
##### 419#       发表于 2021-12-7 10:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53836724&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-7 08:37</a>

最新不是654了吗

—— 来自 HUAWEI OCE-AN10, Android 10上的 S1Next-鹅版 v2.5.2</blockquote>
662，写错了

*****

####  慕容断月  
##### 420#       发表于 2021-12-7 10:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53832671&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-6 20:39</a>
我用飞智WEE一代，安装飞智游戏空间后开启按键映射，完美匹配，机战SL大法屡试不爽，模拟器的SL倒是用的不 ...</blockquote>
不用开映射，我2代的，用app切回传统模式就行了，进去自动识别成ps2键位位置



*****

####  慕容断月  
##### 421#       发表于 2021-12-7 10:36

vp2注意进游戏开快速内存访问，进游戏以后关掉，其余system的设置可以打开

*****

####  yan38324  
##### 422#       发表于 2021-12-7 10:57

求个sd高达neo的rom 一直想补的神作 好不容易找到个rom进去没有任何画面启动不了 估计是rom不对<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  爱死伊  
##### 423#       发表于 2021-12-7 11:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53835304&amp;ptid=2037739" target="_blank">ZEEROKAMI 发表于 2021-12-7 00:29</a>

aethersx2 662汉化版

链接：/s/11A0Rq0VYcauRrjYjfSITaA</blockquote>
显示安装未完成

*****

####  talesof213  
##### 424#       发表于 2021-12-7 11:48

 本帖最后由 talesof213 于 2021-12-7 12:27 编辑 

865，下载了帖子里大佬发的662，全默认，用OGG的观赏模式测试了一下战斗动画，在暴走幽灵这类最后的大爆炸时会有轻微掉帧爆音，不知还能怎么调一下？不过看着手机这小屏幕上跑ogs，莫名感动。

————————————

渲染换成vulcan就完美不掉帧了

*****

####  ZEEROKAMI  
##### 425#       发表于 2021-12-7 12:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53838644&amp;ptid=2037739" target="_blank">爱死伊 发表于 2021-12-7 11:22</a>

显示安装未完成</blockquote>
我MIUI能装好并玩上了，是不是你的系统问题？

*****

####  Dasboat  
##### 426#       发表于 2021-12-7 12:30

插个眼，等稳定版

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  谷恒条野  
##### 427#         楼主| 发表于 2021-12-7 13:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53838342&amp;ptid=2037739" target="_blank">yan38324 发表于 2021-12-7 10:57</a>

求个sd高达neo的rom 一直想补的神作 好不容易找到个rom进去没有任何画面启动不了 估计是rom不对 ...</blockquote>
[https://bbs.3dmgame.com/thread-5792267-1-7.html](https://bbs.3dmgame.com/thread-5792267-1-7.html)

3大妈的可以进

*****

####  JudgmentEye  
##### 428#       发表于 2021-12-7 13:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53839219&amp;ptid=2037739" target="_blank">ZEEROKAMI 发表于 2021-12-7 12:09</a>

我MIUI能装好并玩上了，是不是你的系统问题？</blockquote>
大法x1 mk2也这提示

*****

####  lyt77777  
##### 429#       发表于 2021-12-7 13:53

很严肃的再问一下，alpha2不管怎么调设置，大地图帧率总是会掉到80%左右，战斗画面和机体画面都毫无问题，到底是啥问题？

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  lbj5454  
##### 430#       发表于 2021-12-7 14:44

1月准备换手机，本来准备换水果13，现在开始纠结了

*****

####  Kazuhira  
##### 431#       发表于 2021-12-7 15:35

 本帖最后由 Kazuhira 于 2021-12-7 15:38 编辑 

应该是基于pcsx2的模拟器，里面不知道有没有图像hack什么的设置

如果遇到装甲核心Last Raven黑屏的问题，试着找一下Preload Frame Data的设置？

诶嘿，果然有这个设置，就像pcsx2嘛
<img src="https://p.sda1.dev/3/d8914c07f20475b6ff197534d55697c3/IMG_20211207_153743.jpg" referrerpolicy="no-referrer">

*****

####  yan38324  
##### 432#       发表于 2021-12-7 16:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53839821&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-7 13:03</a>

https://bbs.3dmgame.com/thread-5792267-1-7.html

3大妈的可以进</blockquote>
非常感谢！

*****

####  yan38324  
##### 433#       发表于 2021-12-7 16:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53839821&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-7 13:03</a>

https://bbs.3dmgame.com/thread-5792267-1-7.html

3大妈的可以进</blockquote>
非常感谢！

*****

####  yan38324  
##### 434#       发表于 2021-12-7 16:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53839821&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-7 13:03</a>

https://bbs.3dmgame.com/thread-5792267-1-7.html

3大妈的可以进</blockquote>
非常感谢！

*****

####  杉田悠一  
##### 435#       发表于 2021-12-7 16:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53840339&amp;ptid=2037739" target="_blank">lyt77777 发表于 2021-12-7 13:53</a>
很严肃的再问一下，alpha2不管怎么调设置，大地图帧率总是会掉到80%左右，战斗画面和机体画面都毫无问题， ...</blockquote>
什么cpu，865 3x换了几个滤镜也还是全程100%，

*****

####  掘墓人  
##### 436#       发表于 2021-12-7 17:25

 本帖最后由 掘墓人 于 2021-12-7 17:27 编辑 

老男人下的机战3a丢进去老是说iso容量太大，读不了，4个G

这个应该怎么设

*****

####  精钢魔像  
##### 437#       发表于 2021-12-7 17:32

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843316&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-7 17:25</a>

老男人下的机战3a丢进去老是说iso容量太大，读不了，4个G

这个应该怎么设 ...</blockquote>
没解压吧

*****

####  掘墓人  
##### 438#       发表于 2021-12-7 17:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843415&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-7 17:32</a>

没解压吧</blockquote>
已经解成ISO文件了，还需要进一步解开吗？

我看解开都是些零碎的文件和文件夹了

*****

####  lyt77777  
##### 439#       发表于 2021-12-7 17:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53842650&amp;ptid=2037739" target="_blank">杉田悠一 发表于 2021-12-7 16:41</a>

什么cpu，865 3x换了几个滤镜也还是全程100%，</blockquote>
小米8,845。

*****

####  Jumbohard  
##### 440#       发表于 2021-12-7 17:45

 本帖最后由 Jumbohard 于 2021-12-7 21:52 编辑 

问问深渊传说一拉渲染分辨率就这样有没有什么选项能修一下。我看了下，pcsx2好像本来也有这个问题但是后面GS插件更新了一次修好了。
<img src="https://s3.bmp.ovh/imgs/2021/12/dc3ca88296183f90.jpg" referrerpolicy="no-referrer">

解决了，参照贴吧设置
<img src="https://s3.bmp.ovh/imgs/2021/12/ad7bc177ce8c8fec.jpg" referrerpolicy="no-referrer">

—— 来自 OnePlus LE2100, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  精钢魔像  
##### 441#       发表于 2021-12-7 17:46

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843460&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-7 17:35</a>

已经解成ISO文件了，还需要进一步解开吗？

我看解开都是些零碎的文件和文件夹了 ...</blockquote>
我这里是正常的，是不是你那边有权限限制

用的是Dai-3-Ji Super Robot Taisen Alpha [CHS][OZ01][F07][Fix]

*****

####  古畑任三郎2015  
##### 442#       发表于 2021-12-7 17:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843316&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-7 17:25</a>
老男人下的机战3a丢进去老是说iso容量太大，读不了，4个G

这个应该怎么设 ...</blockquote>
你是tf卡限制么？
如果是的话，格式化成exfat

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  syz726  
##### 443#       发表于 2021-12-7 18:02

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843316&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-7 17:25</a>

老男人下的机战3a丢进去老是说iso容量太大，读不了，4个G

这个应该怎么设 ...</blockquote>
如果不是存储格式问题我建议你看看你选择的打开选项是打开BIOS还是打开ISO

这个模拟器需要先指定一个PS2的BIOS文件然后才能加载ISO（因为模拟器APP不会主动要写入读取存储权限，甚至某些系统下得先进BIOS然后用换盘功能打开游戏ISO再加载）

而BIOS文件最多4M，你塞个4G的ISO文件人当然要报错了。

而且打开ISO我记得是指定一个ISO所在的文件夹然后让模拟器自己扫描的……

*****

####  LuciferGX  
##### 444#       发表于 2021-12-7 18:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53828529&amp;ptid=2037739" target="_blank">sosgame67 发表于 2021-12-6 14:56</a>

顺带求个武神0的资源，网上找的盘载入一直提示插入disc</blockquote>
链接：[https://pan.baidu.com/s/1UAKs9CpTwJQ_fVRbKhMzLw](https://pan.baidu.com/s/1UAKs9CpTwJQ_fVRbKhMzLw) 

提取码：5xm1 

传了一个，我这里能玩

*****

####  sosgame67  
##### 445#       发表于 2021-12-7 18:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53844065&amp;ptid=2037739" target="_blank">LuciferGX 发表于 2021-12-7 18:26</a>

链接：https://pan.baidu.com/s/1UAKs9CpTwJQ_fVRbKhMzLw 

提取码：5xm1 </blockquote>
非常感谢<img src="https://static.saraba1st.com/image/smiley/face2017/031.png" referrerpolicy="no-referrer">

*****

####  桧山修之  
##### 446#       发表于 2021-12-7 18:52

玩了下og，完美模拟，太强了

*****

####  lighttt  
##### 447#       发表于 2021-12-7 18:55

麒麟990打og战斗动画掉帧，只能1x<img src="https://static.saraba1st.com/image/smiley/face2017/017.png" referrerpolicy="no-referrer">

—— 来自 HUAWEI MRX-W29, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  navarra  
##### 448#       发表于 2021-12-7 18:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843316&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-7 17:25</a>
老男人下的机战3a丢进去老是说iso容量太大，读不了，4个G

这个应该怎么设 ...</blockquote>
使用chdman把iso压缩成chd格式，可以节省大量空间，这模拟器也能读

—— 来自 samsung SM-G9880, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  lawsherman  
##### 449#       发表于 2021-12-7 19:15

用vulcan渲染，汉化花3的对白显示不出字，有人知道是怎么回事吗。我用的前面汉化的662

*****

####  JudgmentEye  
##### 450#       发表于 2021-12-7 19:22

<blockquote>引用第448楼lawsherman于2021-12-07 19:15发表的  :

用vulcan渲染，汉化花3的对白显示不出字，有人知道是怎么回事吗。我用的前面汉化的662</blockquote>
vulcan对非高通soc优化不好

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)



*****

####  飞侠小黑  
##### 451#       发表于 2021-12-7 19:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53844434&amp;ptid=2037739" target="_blank">lighttt 发表于 2021-12-7 18:55</a>
麒麟990打og战斗动画掉帧，只能1x

—— 来自 HUAWEI MRX-W29, Android 10上的 S1Next-鹅版 v2.5.2 ...</blockquote>
性能模式开了吗？

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  lighttt  
##### 452#       发表于 2021-12-7 19:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53845123&amp;ptid=2037739" target="_blank">飞侠小黑 发表于 2021-12-7 19:41</a>
性能模式开了吗？

—— 来自 HUAWEI OCE-AN10, Android 10上的 S1Next-鹅版 v2.5.2</blockquote>
等下再试试<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

*****

####  Xenor  
##### 453#       发表于 2021-12-7 21:05

本来在折腾PS模拟器的，结果太让人失望还是不那么完美，忍不住小试了几下这个PS2模拟器，没想到默认设置下就算个位帧也能玩，还支持PS模拟器至今都不支持的CHD格式，真是超乎想象的高效率<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">可以可以

<img src="https://img.saraba1st.com/forum/202112/07/210244ezz2d7g9esieqgj7.jpg" referrerpolicy="no-referrer">

<strong>set.jpg</strong> (120.41 KB, 下载次数: 0)

下载附件

2021-12-7 21:02 上传

<img src="https://img.saraba1st.com/forum/202112/07/210327uv6ffhqc9zffq8l2.jpg" referrerpolicy="no-referrer">

<strong>ai.jpg</strong> (367.52 KB, 下载次数: 0)

下载附件

2021-12-7 21:03 上传

<img src="https://img.saraba1st.com/forum/202112/07/205841yozk6lb4piubvcho.jpg" referrerpolicy="no-referrer">

<strong>1.JPG</strong> (210.33 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205842s1ynaz878qtq0u5w.jpg" referrerpolicy="no-referrer">

<strong>2.JPG</strong> (248.95 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205842iww8t0t2jiky00t0.jpg" referrerpolicy="no-referrer">

<strong>3.JPG</strong> (236.77 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205842amimkndbdsppizb1.jpg" referrerpolicy="no-referrer">

<strong>4.JPG</strong> (230 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205843ts5l00cqb5z628cw.jpg" referrerpolicy="no-referrer">

<strong>5.JPG</strong> (239.25 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205843ky607rp6rt9n7tff.jpg" referrerpolicy="no-referrer">

<strong>6.JPG</strong> (202.15 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205844sd2uzuvuevmom45u.jpg" referrerpolicy="no-referrer">

<strong>7.JPG</strong> (217.29 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

<img src="https://img.saraba1st.com/forum/202112/07/205844n1sslrmmwsg2r29l.jpg" referrerpolicy="no-referrer">

<strong>8.JPG</strong> (213.71 KB, 下载次数: 0)

下载附件

2021-12-7 20:58 上传

*****

####  慕容断月  
##### 454#       发表于 2021-12-7 21:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53846223&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-7 21:05</a>

本来在折腾PS模拟器的，结果太让人失望还是不那么完美，忍不住小试了几下这个PS2模拟器，没想到默认设置下 ...</blockquote>
唯一指定2021手机端PS模拟器duckstation，请

*****

####  精钢魔像  
##### 455#       发表于 2021-12-7 22:01

duckstation只要不是游戏太冷门，应该挺完美了

*****

####  NEIN  
##### 456#       发表于 2021-12-7 22:10

有啥能用的国行bios吗……50009根本启动不了<img src="https://static.saraba1st.com/image/smiley/face2017/012.png" referrerpolicy="no-referrer">

—— 来自 realme RMX3370, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  岬开斗  
##### 457#       发表于 2021-12-7 22:10

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  杉田悠一  
##### 458#       发表于 2021-12-7 22:15

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53847005&amp;ptid=2037739" target="_blank">岬开斗 发表于 2021-12-7 22:10</a>
NS的gpu相当于845，那岂不是NS也有戏了？
等一个最强掌机NS LITE</blockquote>
模拟器一直都是cpu更重要，，710水平的cpu我看比较够呛

*****

####  すぴぱら  
##### 459#       发表于 2021-12-7 22:23

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53847005&amp;ptid=2037739" target="_blank">岬开斗 发表于 2021-12-7 22:10</a>
NS的gpu相当于845，那岂不是NS也有戏了？
等一个最强掌机NS LITE</blockquote>
ns模拟psp都偶尔会卡一下<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">

*****

####  精钢魔像  
##### 460#       发表于 2021-12-7 22:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53847005&amp;ptid=2037739" target="_blank">岬开斗 发表于 2021-12-7 22:10</a>

NS的gpu相当于845，那岂不是NS也有戏了？

等一个最强掌机NS LITE</blockquote>
有戏，b站上有刷安卓的switch跑以太模拟器的

*****

####  qieyifonger  
##### 461#       发表于 2021-12-8 08:01

有人试过用小米平板5(或pro)跑过这个模拟器吗？效果如何？

—— 来自 Xiaomi Redmi K20 Pro Premium Edition, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  平井姨夫  
##### 462#       发表于 2021-12-8 09:29

坚果R1无法读取BIOS文件……服了……

*****

####  lbzlxx  
##### 463#       发表于 2021-12-8 09:59

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53847005&amp;ptid=2037739" target="_blank">岬开斗 发表于 2021-12-7 22:10</a>

NS的gpu相当于845，那岂不是NS也有戏了？

等一个最强掌机NS LITE</blockquote>
模拟器一直依赖的主要都是CPU，你ns那宇宙废物就不要搞模拟器了

*****

####  lbj5454  
##### 464#       发表于 2021-12-8 10:24

天玑1100CPU能玩这款模拟器吗？

*****

####  杉田悠一  
##### 465#       发表于 2021-12-8 11:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53849316&amp;ptid=2037739" target="_blank">qieyifonger 发表于 2021-12-8 08:01</a>

有人试过用小米平板5(或pro)跑过这个模拟器吗？效果如何？

—— 来自 Xiaomi Redmi K20 Pro Premium Editi ...</blockquote>
玩具窝发了个视频，是恰腾讯云游戏饭的，开头用米板5Pro跑了模拟器，一顿吹，说是最好的平台，

实际就看CPU就行，870肯定没问题

*****

####  GOUKI1981  
##### 466#       发表于 2021-12-8 11:23

鸭子界面和以太一样啊，鸭子好是好，几时能上个滤镜

*****

####  22174559  
##### 467#       发表于 2021-12-8 11:30

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  navarra  
##### 468#       发表于 2021-12-8 11:35

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53846223&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-7 21:05</a>
本来在折腾PS模拟器的，结果太让人失望还是不那么完美，忍不住小试了几下这个PS2模拟器，没想到默认设置下 ...</blockquote>
安卓ps模拟器请认准duckstation……

—— 来自 samsung SM-G9880, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  精钢魔像  
##### 469#       发表于 2021-12-8 12:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53851474&amp;ptid=2037739" target="_blank">GOUKI1981 发表于 2021-12-8 11:23</a>

鸭子界面和以太一样啊，鸭子好是好，几时能上个滤镜</blockquote>
你可以用ra用鸭站核心

手机那么小的屏幕，用不用滤镜都差不多

*****

####  JudgmentEye  
##### 470#       发表于 2021-12-8 12:35

 本帖最后由 JudgmentEye 于 2021-12-8 12:47 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53847005&amp;ptid=2037739" target="_blank">岬开斗 发表于 2021-12-7 22:10</a>

NS的gpu相当于845，那岂不是NS也有戏了？

等一个最强掌机NS LITE</blockquote>
反正黄老板shield用蓝牙连ds4完美，不会3秒真男人，玩机战我感觉比865都快

另外可以先用ns开机直接引导tf卡上的android再跑aethersx2，类似电脑直接运行u盘上的windows pe，但只有没修黄老板漏洞的旧版ns可以，lite没戏，lite只能焊芯片破解，芯片破解的权限低，没法直接引导tf卡上的boot文件

*****

####  JudgmentEye  
##### 471#       发表于 2021-12-8 12:53

有人试了，ogs挺流畅
[https://www.bilibili.com/video/BV1a34y1X7gA](https://www.bilibili.com/video/BV1a34y1X7gA)

*****

####  杉田悠一  
##### 472#       发表于 2021-12-8 13:00

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53852667&amp;ptid=2037739" target="_blank">JudgmentEye 发表于 2021-12-8 12:53</a>

有人试了，ogs挺流畅

https://www.bilibili.com/video/BV1a34y1X7gA</blockquote>
这第二话地图界面就卡到一半帧数了还能算流畅吗，，中后期机体多了那得多卡，

*****

####  JudgmentEye  
##### 473#       发表于 2021-12-8 13:08

shield不卡，他哪个参数没设好吧

*****

####  sdhgak1234  
##### 474#       发表于 2021-12-8 14:24

求个能用得662中文版，上车晚了，谢谢<img src="https://static.saraba1st.com/image/smiley/face2017/117.png" referrerpolicy="no-referrer">

*****

####  rare720  
##### 475#       发表于 2021-12-8 15:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53851638&amp;ptid=2037739" target="_blank">navarra 发表于 2021-12-8 11:35</a>

安卓ps模拟器请认准duckstation……

—— 来自 samsung SM-G9880, Android 11上的 S1Next-鹅版 v2.5.2 ...</blockquote>
xbox ps模拟器也是鸭子最强，ppsspp也好用。

xbox网页登录[https://gamr13.github.io/](https://gamr13.github.io/)商店下载安装。还有RetroArch。

甚至还有密特罗德2重制版，哈哈

*****

####  rare720  
##### 476#       发表于 2021-12-8 15:24

 本帖最后由 rare720 于 2021-12-8 15:30 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53846775&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-7 21:50</a>

唯一指定2021手机端PS模拟器duckstation，请</blockquote>
xbox平台也是鸭子最强。

[https://gamr13.github.io/](https://gamr13.github.io/)
所有游戏在xbox集结 ！！！

<img src="https://img.saraba1st.com/forum/202112/08/152953j77au00s5op8m5lu.jpg" referrerpolicy="no-referrer">

<strong>duck.jpg</strong> (19.79 KB, 下载次数: 0)

下载附件

2021-12-8 15:29 上传

<img src="https://img.saraba1st.com/forum/202112/08/153007cb88j81ex404pz6m.jpg" referrerpolicy="no-referrer">

<strong>98.jpg</strong> (68.47 KB, 下载次数: 0)

下载附件

2021-12-8 15:30 上传

*****

####  精钢魔像  
##### 477#       发表于 2021-12-8 15:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53854605&amp;ptid=2037739" target="_blank">rare720 发表于 2021-12-8 15:24</a>

xbox平台也是鸭子最强。

https://gamr13.github.io/</blockquote>
话说xbox的ra 怎么更新？

*****

####  精钢魔像  
##### 478#       发表于 2021-12-8 15:54

说到ra，还是steam的最好。一是steam控制器能支持稀奇古怪的设备，自己做个麻将机都可以

二是steam远程同乐用的是串流，直接把联机最难搞定的同步问题搞定了

*****

####  rare720  
##### 479#       发表于 2021-12-8 16:25

 本帖最后由 rare720 于 2021-12-8 16:26 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53854993&amp;ptid=2037739" target="_blank">精钢魔像 发表于 2021-12-8 15:51</a>

话说xbox的ra 怎么更新？</blockquote>
之前有下载过，Ra其实可以打开后更新吧。

最近微软商店又可以下载了，不需要白名单。

*****

####  谷恒条野  
##### 480#         楼主| 发表于 2021-12-8 17:20

 本帖最后由 谷恒条野 于 2021-12-8 17:23 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53853853&amp;ptid=2037739" target="_blank">sdhgak1234 发表于 2021-12-8 14:24</a>

求个能用得662中文版，上车晚了，谢谢</blockquote>
[https://www.lanzouw.com/iNrZFxd8pmb](https://www.lanzouw.com/iNrZFxd8pmb)

贴吧这个UP做的加了滤镜的汉化版
[https://www.bilibili.com/video/BV1vL41177xC](https://www.bilibili.com/video/BV1vL41177xC)

﹍﹍﹍

评分

 参与人数 1战斗力 +2

|昵称|战斗力|理由|
|----|---|---|
| sdhgak1234| + 2|谢谢|

查看全部评分



*****

####  终将不惑  
##### 481#       发表于 2021-12-8 17:29

最想玩的ico不支持<img src="https://static.saraba1st.com/image/smiley/face2017/012.png" referrerpolicy="no-referrer">

*****

####  无色老魔  
##### 482#       发表于 2021-12-8 18:31

 本帖最后由 无色老魔 于 2021-12-8 19:18 编辑 

xbox手柄识别不了lt，rt键怎么解决啊

—— 来自 OnePlus IN2020, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  掘墓人  
##### 483#       发表于 2021-12-8 23:47

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53843775&amp;ptid=2037739" target="_blank">syz726 发表于 2021-12-7 18:02</a>

如果不是存储格式问题我建议你看看你选择的打开选项是打开BIOS还是打开ISO

这个模拟器需要先指定一个PS2 ...</blockquote>
啊果然是这个，是我傻逼了眼花看混了ISO和BIOS。摸鱼时弄的没仔细看

谢谢

*****

####  syz726  
##### 484#       发表于 2021-12-9 00:25

 本帖最后由 syz726 于 2021-12-9 00:26 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53860728&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-8 23:47</a>

啊果然是这个，是我傻逼了眼花看混了ISO和BIOS。摸鱼时弄的没仔细看

谢谢 ...</blockquote>
不客气，因为在以太模拟器吧这种案例见的多了（在BIOS那里狂点ISO报错点不开然后求救）

毕竟我手头3α的ISO就是4G的，模拟器版本从英文原版到汉化版都没出过【文件太大】问题；且印象里ISO是自动搜寻的不是单个单个点开。

所以我就觉得是你在打开BIOS文件界面开ISO了

没事儿问题解决了就好，祝游戏愉快

*****

####  Xenor  
##### 485#       发表于 2021-12-9 06:05

 本帖最后由 Xenor 于 2021-12-9 12:38 编辑 

感谢推荐，duckstation之前了解过，但一直epsxe时间用得久很舍不得……<img src="https://static.saraba1st.com/image/smiley/face2017/093.png" referrerpolicy="no-referrer">现在看来是要到放弃的时候了，毕竟PS2模拟器都能跑了epsxe还这样

又去了解了下duckstation，发现作者名看着很眼熟，原来是dolphin调试版中最杰出的那位，之前一直都是下的这名字的版本<img src="https://static.saraba1st.com/image/smiley/face2017/075.png" referrerpolicy="no-referrer">稳定翻车少，信心大增试试去

手机cpu是老弱病残的高通火龙前三甲820，洋垃圾一个多月没关机可用内存只有600MB，闪存速度也退化得不行

但是试了2x默认设置跑深渊传说还能有40%~60%的速度，过场基本100%，越来越期待正式版了

<img src="https://img.saraba1st.com/forum/202112/09/055743yvl19ivxuyxzv8xx.jpg" referrerpolicy="no-referrer">

<strong>1.JPG</strong> (108.17 KB, 下载次数: 0)

下载附件

2021-12-9 05:57 上传

<img src="https://img.saraba1st.com/forum/202112/09/055744mkjmiboxbbuocbdi.jpg" referrerpolicy="no-referrer">

<strong>2.JPG</strong> (176.28 KB, 下载次数: 0)

下载附件

2021-12-9 05:57 上传

4X卡成20FPS也能跑

<img src="https://img.saraba1st.com/forum/202112/09/055744mm0yybyfl4feffu6.jpg" referrerpolicy="no-referrer">

<strong>3.JPG</strong> (181.38 KB, 下载次数: 0)

下载附件

2021-12-9 05:57 上传

<img src="https://img.saraba1st.com/forum/202112/09/055744xqcrrgr34chv8ssv.jpg" referrerpolicy="no-referrer">

<strong>4.JPG</strong> (180.19 KB, 下载次数: 0)

下载附件

2021-12-9 05:57 上传

8X也能撑

<img src="https://img.saraba1st.com/forum/202112/09/055745k36o9pc6pmiz3mn7.jpg" referrerpolicy="no-referrer">

<strong>5.JPG</strong> (178.03 KB, 下载次数: 0)

下载附件

2021-12-9 05:57 上传

_____________________

PS：

epsxe：支持pbp不支持chd

duckstation：支持chd不支持pbp

我：全pbp

两个只能活一个啊<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">太狠了

*****

####  天蓬元帅买买提  
##### 486#       发表于 2021-12-9 09:09

<img src="https://static.saraba1st.com/image/smiley/face2017/105.png" referrerpolicy="no-referrer">想问下坛友ps2的ISO都是在哪下的

*****

####  掘墓人  
##### 487#       发表于 2021-12-9 09:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53862814&amp;ptid=2037739" target="_blank">天蓬元帅买买提 发表于 2021-12-9 09:09</a>

想问下坛友ps2的ISO都是在哪下的</blockquote>
老男人
[https://www.oldmanemu.net](https://www.oldmanemu.net)

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| 天蓬元帅买买提| + 1|感恩|

查看全部评分

*****

####  22174559  
##### 488#       发表于 2021-12-9 12:06

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  JudgmentEye  
##### 489#       发表于 2021-12-9 12:29

<blockquote>引用第487楼22174559于2021-12-09 12:06发表的  :

我有个865的华为平板，请问买什么手柄最好，PS4吗？</blockquote>
当然，谁知道ps5手柄能不能用？

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  谷恒条野  
##### 490#         楼主| 发表于 2021-12-9 12:31

 本帖最后由 谷恒条野 于 2021-12-9 13:10 编辑 

alpha-669:

Improve frame pacing in skip duplicate frames option.
Recompile BLTZAL/BLTZALL, swap delay slot in BGEZAL.
Fix a couple of VU bugs - Persona 4  PAL, Tony Hawk's Downhill Jam.
Fix possible crash when opening pause menu. 
Add internal frame rate detection and skip duplicate frames option.

一下就从668到669了
看贴吧说从668开始加了这个选项，打开一些游戏提速明显。有兴趣可以测试试试。
<img src="https://p.sda1.dev/3/dc8bbd20d5dd5b9c38ab4351fcc7832d/IMG_CMP_147738242.jpeg" referrerpolicy="no-referrer">

*****

####  22174559  
##### 491#       发表于 2021-12-9 12:37

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  JudgmentEye  
##### 492#       发表于 2021-12-9 12:40

<blockquote>引用第490楼22174559于2021-12-09 12:37发表的  :

引用:JudgmentEye 发表于 2021-12-9 12:29当然，谁知道ps5手柄能不能用？......</blockquote>
马首富遍地假的，二手东买国行手柄不就行了

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  Xenor  
##### 493#       发表于 2021-12-9 12:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53865095&amp;ptid=2037739" target="_blank">22174559 发表于 2021-12-9 12:06</a>

我有个865的华为平板，请问买什么手柄最好，PS4吗？</blockquote>
[https://www.8bitdo.cn/sn30-pro-g-classic-or-sn30-pro-sn/](https://www.8bitdo.cn/sn30-pro-g-classic-or-sn30-pro-sn/)

小巧便携、功能全，续航做工质量也都还可以，就是按键响

*****

####  古畑任三郎2015  
##### 494#       发表于 2021-12-9 23:29

话说有人在quest2上成功玩上了吗？

试了半天，总是读不了文件目录，这程序居然默认是不要存储权限的？

*****

####  PYY  
##### 495#       发表于 2021-12-10 01:27

小米11u，高通888，668汉化版。

默认设置的话，北妹2城镇和菜单只有不到40。其他没问题。

改为：

gpu渲染器vulkin，禁用硬件回读，禁用深度模拟。

之后就60满帧了。

然后一直开到缩放倍数3倍都是满帧，4倍才又降到40多帧。

也就是说，之后只要更新几次，至少这游戏全速没问题。

<img src="https://img.saraba1st.com/forum/202112/10/012645me3eec552ck2c522.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2021-12-10-01-14-57-674_xyz.aethersx2.android.jpg</strong> (364.77 KB, 下载次数: 0)

下载附件

2021-12-10 01:26 上传

*****

####  yujie  
##### 496#       发表于 2021-12-10 05:14

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53811378&amp;ptid=2037739" target="_blank">saberserker 发表于 2021-12-4 22:36</a>
试了一圈，唯独机战MX没法正常玩，OpenGL开头菜单和战斗动画帧数巨低，vulkan游戏菜单速度到正常，但是进地 ...</blockquote>
845按这个设置ogs流畅
但是mx部分武器比如真实系主角机的机枪炮台就有明显的拖慢，不知道改哪个设置可以解决

*****

####  慕容断月  
##### 497#       发表于 2021-12-10 09:03

 本帖最后由 慕容断月 于 2021-12-10 09:15 编辑 

阔以，865，觉得可能有用的项目开了以后世嘉拉力2006直接半速变全速，vp2城镇里基本满帧，丧失之森的剧情还是卡，山脊赛车5算是能玩了虽然还有贴图错误，等更新<img src="https://p.sda1.dev/3/f4fdab21200652c10441cf79668ac8e5/IMG_CMP_205612669.jpeg" referrerpolicy="no-referrer">

<img src="https://p.sda1.dev/3/5c3ddcb68315af9cda0c4861414260ca/IMG_CMP_34201576.jpeg" referrerpolicy="no-referrer">

<img src="https://p.sda1.dev/3/16fc6037bc396941a11de2e72b8c6504/IMG_CMP_182274963.jpeg" referrerpolicy="no-referrer">

*****

####  kirito_wst  
##### 498#       发表于 2021-12-11 20:44

官方最新版添加界面中文语言，妈妈再也不用担心我看不懂菜单了<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi M2012K11AC, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  彩虹肥宅  
##### 499#       发表于 2021-12-11 21:14

835 跑真三国无双5 用 valken 会出现小地图标记丢失还有敌人血条显示不全，一般哪个设置可以影响这个<img src="https://static.saraba1st.com/image/smiley/face2017/162.png" referrerpolicy="no-referrer">

*****

####  谷恒条野  
##### 500#         楼主| 发表于 2021-12-12 01:23

alpha-678:
Disable bundle splitting for languages (allows any language selection post install).
Fix possible crash in Vulkan when texture preloading is on and large textures are used.
Correct rounding mode for float-&gt;int conversion (fixes water elevators in FFX).
Fix incorrect VU0 status flags in COP2 mode.
Add console-accurate FPU add/sub instructions (fixes location text in P4).
Add option for using brake/gas axes (needed for L2/R2 on some devices).
Add translations.

<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">新版本自带官方中文太棒了。

*****

####  blueelf  
##### 501#       发表于 2021-12-12 01:32

影之心1代要怎么设置？865的平板只有10几帧，群友用麒麟710都能满速，怪了

*****

####  Xenor  
##### 502#       发表于 2021-12-12 14:48

 本帖最后由 Xenor 于 2021-12-12 16:09 编辑 

<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">折腾了几天鸭站，对比epsxe，画面确实观感要好，细节错误的地方也更少

<img src="https://img.saraba1st.com/forum/202112/12/135234ju4tcaqtaw1qxtas.jpg" referrerpolicy="no-referrer">

<strong>1.jpg</strong> (196.86 KB, 下载次数: 0)

下载附件

2021-12-12 13:52 上传

<img src="https://img.saraba1st.com/forum/202112/12/135234z052l0f5f0can0s5.jpg" referrerpolicy="no-referrer">

<strong>2.jpg</strong> (227.58 KB, 下载次数: 0)

下载附件

2021-12-12 13:52 上传

<img src="https://img.saraba1st.com/forum/202112/12/135234wj8ctcmg743m1q1l.jpg" referrerpolicy="no-referrer">

<strong>3.jpg</strong> (181.41 KB, 下载次数: 0)

下载附件

2021-12-12 13:52 上传

<img src="https://img.saraba1st.com/forum/202112/12/135235xcxxt2l2bv2ldp3x.jpg" referrerpolicy="no-referrer">

<strong>4.jpg</strong> (198.6 KB, 下载次数: 0)

下载附件

2021-12-12 13:52 上传

最大的优势是3D防抖机制，打开后遇到3D场景就再也不会莫名抖动了，整体看上去更自然平稳在渲染3D的同时还能较好渲染2D画面，单独3D/2D也都是强项

不像epsxe只能偏向一种，效果还一般

epsxe

<img src="https://img.saraba1st.com/forum/202112/12/135646ouhgu1hp9po9hi2n.jpg" referrerpolicy="no-referrer">

<strong>epsxe.jpg</strong> (263.47 KB, 下载次数: 0)

下载附件

2021-12-12 13:56 上传

duckstation

<img src="https://img.saraba1st.com/forum/202112/12/135645aznnjokci3vnbowq.jpg" referrerpolicy="no-referrer">

<strong>duck.jpg</strong> (237.43 KB, 下载次数: 0)

下载附件

2021-12-12 13:56 上传

但是epsxe有一个xBRZ插件是duckstation没有的，效果看着不错，只可惜分辨率低还无法选择！导致人看不清脸…

<img src="https://img.saraba1st.com/forum/202112/12/143600rdkzdckaopj0aczo.jpg" referrerpolicy="no-referrer">

<strong>i.jpg</strong> (150.79 KB, 下载次数: 0)

下载附件

2021-12-12 14:36 上传

<img src="https://img.saraba1st.com/forum/202112/12/143601w3lpzbbiivnor9qp.jpg" referrerpolicy="no-referrer">

<strong>ii.jpg</strong> (86.27 KB, 下载次数: 0)

下载附件

2021-12-12 14:36 上传

<img src="https://img.saraba1st.com/forum/202112/12/143601xmrm7f1bmgkmqx54.jpg" referrerpolicy="no-referrer">

<strong>iii.jpg</strong> (217.34 KB, 下载次数: 0)

下载附件

2021-12-12 14:36 上传

<img src="https://img.saraba1st.com/forum/202112/12/143601okehgdj7wan0s6ak.jpg" referrerpolicy="no-referrer">

<strong>iv.jpg</strong> (175.48 KB, 下载次数: 0)

下载附件

2021-12-12 14:36 上传

真是遗憾极了

除此之外epsxe+隔行扫描看着效果应该是最好的吧，但手机看着累，而且还有一些图形BUG，比如菜单小花屏背景不透明，总是差那么一步<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/12/144012o1pnn91pv6sj1su4.jpg" referrerpolicy="no-referrer">

<strong>scan.jpg</strong> (485.8 KB, 下载次数: 0)

下载附件

2021-12-12 14:40 上传

不如epsxe的地方有：

1.duckstation不支持ppf外挂补丁，虽然有这个选项，但是打开后一样用不了

2.duckstation不支持动态振动

3.duckstation不支持隔行扫描

4.速度效率不如epsxe高，单核1G都能畅玩的PS游戏，用duck设置过了很容易卡成幻灯片

总的来说duckstation模拟效果不错几乎没啥错误，独创3D防抖，其他方面还在不断改进，比epsxe有前途，只是缺少了一些实用功能，要是加上了，同时epsxe继续原地后退的话，真就可以和epsxe say goodbye咯<img src="https://static.saraba1st.com/image/smiley/face2017/062.gif" referrerpolicy="no-referrer">

至于PS2模拟器，试了下FFX，2x晓龙820也能达到平均75%以上的速度<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">效率高到让人有模拟PS2就像模拟FC那样的感觉

<img src="https://img.saraba1st.com/forum/202112/12/155428r5zhwcm3pfisz1ph.png" referrerpolicy="no-referrer">

<strong>x.png</strong> (274.83 KB, 下载次数: 0)

下载附件

2021-12-12 15:54 上传

<img src="https://img.saraba1st.com/forum/202112/12/155428plqzxxizodqffjd5.png" referrerpolicy="no-referrer">

<strong>xx.png</strong> (257.35 KB, 下载次数: 0)

下载附件

2021-12-12 15:54 上传

和电脑版的pcsx2模拟效果相差不大

<img src="https://img.saraba1st.com/forum/202112/12/155655phxppl7pe6p7knpe.jpg" referrerpolicy="no-referrer">

<strong>yuna.jpg</strong> (270.51 KB, 下载次数: 0)

下载附件

2021-12-12 15:56 上传

<img src="https://img.saraba1st.com/forum/202112/12/155655lhnxl5bx9y3b9lz3.jpg" referrerpolicy="no-referrer">

<strong>feel.jpg</strong> (367.91 KB, 下载次数: 0)

下载附件

2021-12-12 15:56 上传

这样835以上肯定就能全速了，准备试看看在手机上开坑这个游戏，都过20年了还没碰过…
<img src="https://psxdatacenter.com/psx2/images2/hires/SLPS-25088/SLPS-25088-F-ALL.jpg" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/12/160632habpej4dbbkbtbjj.jpg" referrerpolicy="no-referrer">

<strong>jp.jpg</strong> (126.71 KB, 下载次数: 0)

下载附件

2021-12-12 16:06 上传

了解了一番后发现FFX国际版是最好的，但是被英文配音吓到了，还好有日语替换的补丁，可打完后发现开篇有个像花版一样的LOGO<img src="https://static.saraba1st.com/image/smiley/face2017/159.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/12/160112tizbiihqqhbkx0kc.jpg" referrerpolicy="no-referrer">

<strong>logo.jpg</strong> (136.82 KB, 下载次数: 0)

下载附件

2021-12-12 16:01 上传

每次打开都得看一遍……逼疯强迫症了，更何况上面写的这问题现在还会存在吗

不知有没有办法去掉这个呢<img src="https://static.saraba1st.com/image/smiley/face2017/097.png" referrerpolicy="no-referrer">还我纯白的Squaresoft Logo

*****

####  精钢魔像  
##### 503#       发表于 2021-12-12 15:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53906222&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-12 14:48</a>

折腾了几天鸭站，对比epsxe，画面确实观感要好，细节错误的地方也更少</blockquote>
鸭站的pc版是支持ppf的，安卓版不知为何不支持，安卓好像也不支持7zip

画面最好的是开retroarch滤镜，不过我觉得手机开不开滤镜无所谓，不开还能省电

鸭站强于其他模拟器的地方是几何修正，3d游戏画面会不抖，纹理也会对齐

观感变化最大的应该是《放浪冒险谭》

﹍﹍﹍

评分

 参与人数 1战斗力 +2

|昵称|战斗力|理由|
|----|---|---|
| Xenor| + 2|对的，我都抖习惯了Orz|

查看全部评分

*****

####  22174559  
##### 504#       发表于 2021-12-12 18:29

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  幽灵胖胖  
##### 505#       发表于 2021-12-12 18:47

冤大头，为了装新的自带中文版，卸载了第一版的，但是花2的十几关存档也没了，这存档到底保存在哪的啊，以后更新得备份了

*****

####  sodr  
##### 506#       发表于 2021-12-12 18:55

835补OGS中，一到战斗画面45~60之间，只能说能玩，这才一倍分辨率，希望有个835专用优化设置就好

*****

####  慕容断月  
##### 507#       发表于 2021-12-12 19:04

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53906222&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-12 14:48</a>

折腾了几天鸭站，对比epsxe，画面确实观感要好，细节错误的地方也更少</blockquote>
早年ez zone没倒前有人做了logo还原，现在估计找不到了，去玩hd版算了吧

*****

####  谷恒条野  
##### 508#         楼主| 发表于 2021-12-12 19:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908694&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-12 18:47</a>
冤大头，为了装新的自带中文版，卸载了第一版的，但是花2的十几关存档也没了，这存档到底保存在哪的啊，以 ...</blockquote>
Android/data/xyz.aethersx2.android/files/memcards/

*****

####  ΑΑ  
##### 509#       发表于 2021-12-12 19:13

问问有没有人玩过nfs，电脑版要改参数，手机版改完就闪退

*****

####  PYY  
##### 510#       发表于 2021-12-12 19:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908694&amp;ptid=2037739" target="_blank">幽灵胖胖 发表于 2021-12-12 18:47:03</a>
冤大头，为了装新的自带中文版，卸载了第一版的，但是花2的十几关存档也没了，这存档到底保存在哪的啊，以 ...</blockquote>直接装新的就行。
我就是668汉化版，再覆盖安装678。

[  -- 来自 能看大图的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)



*****

####  xbhuang  
##### 511#       发表于 2021-12-12 19:32

还在挑手柄，雷蛇的kishi手柄怎样，咸鱼要四百块，官方也要五百多，比nspro手柄还贵，值不值？
然后还看到仿joyvon的北通h2，分体手柄模拟器能用吗

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  爱死伊  
##### 512#       发表于 2021-12-12 19:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53909082&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-12 19:32</a>

还在挑手柄，雷蛇的kishi手柄怎样，咸鱼要四百块，官方也要五百多，比nspro手柄还贵，值不值？

然后还看到 ...</blockquote>
这俩我都买了

kishi手感巨好

这两天一直用这个刷basara2

h2的手感我完全不习惯

*****

####  xbhuang  
##### 513#       发表于 2021-12-12 20:12

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53909125&amp;ptid=2037739" target="_blank">爱死伊 发表于 2021-12-12 19:38</a>
这俩我都买了

kishi手感巨好

这两天一直用这个刷basara2</blockquote>
那还是买kishi吧，而且也便携点，h2看着配件一大堆，都不好带身上

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  allenz3  
##### 514#       发表于 2021-12-12 20:22

看你要玩什么，蓝牙手柄多少有延迟不适合快节奏的动作游戏或者音游，如果不在意延迟可以买赛太克7007F，PDD不到120

—— 来自 Sony XQ-AS72, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  路西恩  
##### 515#       发表于 2021-12-12 20:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53850643&amp;ptid=2037739" target="_blank">lbj5454 发表于 2021-12-8 10:24</a>
天玑1100CPU能玩这款模拟器吗？</blockquote>
一千加都可以，1100应该比1000加要好吧 不过分游戏，ff12会卡的很

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  谷恒条野  
##### 516#         楼主| 发表于 2021-12-12 20:40

收了个小鸡X2蓝牙版，用起来感觉还行，接上按键都正常，而且k30s带套也能夹住。

*****

####  orx  
##### 517#       发表于 2021-12-12 21:09

好几个十几年前就想玩的游戏终于有时间和空间去补完了<img src="https://static.saraba1st.com/image/smiley/face2017/057.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/12/210852ee4j5yvm50ugee1m.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2021-12-12-01-07-50-25_e2246895d6daacc7940d53fa6d65ea44.jpg</strong> (50.92 KB, 下载次数: 0)

下载附件

2021-12-12 21:08 上传

<img src="https://img.saraba1st.com/forum/202112/12/210901idivnnfkatibqikz.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2021-12-12-01-07-52-83_e2246895d6daacc7940d53fa6d65ea44.jpg</strong> (50.86 KB, 下载次数: 0)

下载附件

2021-12-12 21:09 上传

<img src="https://img.saraba1st.com/forum/202112/12/210906b8ptp00pbnpuws9l.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2021-12-12-01-07-55-30_e2246895d6daacc7940d53fa6d65ea44.jpg</strong> (47.91 KB, 下载次数: 0)

下载附件

2021-12-12 21:09 上传

<img src="https://img.saraba1st.com/forum/202112/12/210910v2yhbq55h5hu5rtn.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2021-12-12-01-14-35-72_e2246895d6daacc7940d53fa6d65ea44.jpg</strong> (48.23 KB, 下载次数: 0)

下载附件

2021-12-12 21:09 上传

*****

####  希德尼娅  
##### 518#       发表于 2021-12-12 22:35

求推个typec的拉伸手柄玩ps2，小鸡x2靠谱吗

*****

####  路西恩  
##### 519#       发表于 2021-12-13 00:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53909125&amp;ptid=2037739" target="_blank">爱死伊 发表于 2021-12-12 19:38</a>
这俩我都买了

kishi手感巨好

这两天一直用这个刷basara2</blockquote>
求问一个，这个kishi搓格斗手感如何

主要是十字键的感觉

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  费老师  
##### 520#       发表于 2021-12-13 06:48

888打女忍卡帧

*****

####  飞侠小黑  
##### 521#       发表于 2021-12-13 07:28

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908772&amp;ptid=2037739" target="_blank">sodr 发表于 2021-12-12 18:55</a>
835补OGS中，一到战斗画面45~60之间，只能说能玩，这才一倍分辨率，希望有个835专用优化设置就好 ...</blockquote>
835还是升级吧，低端的778都比835强太多了，没必要死守835了，865/870又那么便宜

—— 来自 HUAWEI OCE-AN10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  谢皮利男爵  
##### 522#       发表于 2021-12-13 09:41

<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">战国BASARA2能跑吗

*****

####  桧山修之  
##### 523#       发表于 2021-12-13 09:56

哪位朋友能分享一下最新的汉化版本啊，找了一下没找到

*****

####  yunalesca  
##### 524#       发表于 2021-12-13 11:19

买了个北通G3，明天到手，到时候试试手感

*****

####  highsky  
##### 525#       发表于 2021-12-13 11:23

<blockquote>谢皮利男爵 发表于 2021-12-13 09:41
战国BASARA2能跑吗</blockquote>
855跑完美，而且开了3x分辨率和宽屏补丁

*****

####  Kojimaru  
##### 526#       发表于 2021-12-13 11:25

<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">把存档扔到memcard那个文件夹，好像没啥用

*****

####  PYY  
##### 527#       发表于 2021-12-13 11:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53914317&amp;ptid=2037739" target="_blank">桧山修之 发表于 2021-12-13 09:56:11</a>
哪位朋友能分享一下最新的汉化版本啊，找了一下没找到</blockquote>另一个帖子，叫做更新官方678版的，就在后面一点。

我也问一下，游戏手柄怎么设置振动功能？
模拟器菜单中没找到开启振动的功能。
我是ps4手柄线连手机。

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  ogloc  
##### 528#       发表于 2021-12-13 12:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908772&amp;ptid=2037739" target="_blank">sodr 发表于 2021-12-12 18:55</a>

835补OGS中，一到战斗画面45~60之间，只能说能玩，这才一倍分辨率，希望有个835专用优化设置就好 ...</blockquote>
835打OGS看这帖300楼的设置，战斗全速，地图画面45-50左右

*****

####  JudgmentEye  
##### 529#       发表于 2021-12-13 12:49

<blockquote>引用第525楼Kojimaru于2021-12-13 11:25发表的  :

把存档扔到memcard那个文件夹，好像没啥用</blockquote>
要在设置里选存档文件导入

----[STAGE1 Mobile](http://bbs.saraba1st.com/?1.0)

*****

####  lbj5454  
##### 530#       发表于 2021-12-13 13:09

最后用晓龙888玩上了，实在太爽了，问一下金手指功能怎么用？

*****

####  桧山修之  
##### 531#       发表于 2021-12-13 13:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53915941&amp;ptid=2037739" target="_blank">PYY 发表于 2021-12-13 11:49</a>

另一个帖子，叫做更新官方678版的，就在后面一点。

我也问一下，游戏手柄怎么设置振动功能？</blockquote>
谢谢啦，找到了<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">

*****

####  reakiya  
##### 532#       发表于 2021-12-13 17:09

这几天在打352m发现曹操和甘宁的c6总是打不出来 甘宁要在普攻第四段连打蓄力才能出c6 是这代c技判定严格还是模拟器延迟加上蓝牙手柄延迟？

*****

####  xbhuang  
##### 533#       发表于 2021-12-13 17:13

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53915533&amp;ptid=2037739" target="_blank">yunalesca 发表于 2021-12-13 11:19</a>

买了个北通G3，明天到手，到时候试试手感</blockquote>
北通G3我看了，没有右摇杆啊，而且性价比不高，人家是针对王者荣耀的，连吃鸡都没考虑

*****

####  yunalesca  
##### 534#       发表于 2021-12-13 17:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53920680&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-13 17:13</a>

北通G3我看了，没有右摇杆啊，而且性价比不高，人家是针对王者荣耀的，连吃鸡都没考虑 ...</blockquote>
咸鱼270包邮收的，原价太过分，不可能原价买的。选北通的主要原因是不信任小鸡x2的按键手感，北通起码按键应该还可以，G3的右侧所谓手游键盘是可以锁的（不玩手游推指向性技能的话可以锁住当固定键位使用），可能……还好吧，的确，这玩意没有右摇杆是一个很大的问题，到手之后试试看四个手游按键能不能设置R3的四个方向，按理说是可以的。

*****

####  掘墓人  
##### 535#       发表于 2021-12-13 18:11

北通那个H2比起小鸡X2来说怎么样？看着也有右摇杆

其实就打打机战，是不是随便买个便宜的就行了？

—— 来自 Xiaomi Redmi K30 Pro Zoom Edition, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  Xenor  
##### 536#       发表于 2021-12-13 22:31

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908504&amp;ptid=2037739" target="_blank">22174559 发表于 2021-12-12 18:29</a>

835估计还是太弱了 如果要全部游戏满速</blockquote>
根据以前的经验估计的，dolphin在820上能达到65%的速度，835上就全速了，3ds也是一样，835要快近40%

我是手机里全塞满了，没空间弄PS2，只能拿个820试，猜<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

目前测下来835跑现在的主流模拟器都是足够玩了

<img src="https://img.saraba1st.com/forum/202112/13/220650dld27y9fpyd3kx3q.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_20211210-223155.jpg</strong> (192.1 KB, 下载次数: 0)

下载附件

2021-12-13 22:06 上传

<img src="https://img.saraba1st.com/forum/202112/13/220652joedkto0dqrl0riu.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_20211210-223209.jpg</strong> (201.56 KB, 下载次数: 0)

下载附件

2021-12-13 22:06 上传

*****

####  Xenor  
##### 537#       发表于 2021-12-13 22:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53908832&amp;ptid=2037739" target="_blank">慕容断月 发表于 2021-12-12 19:04</a>

早年ez zone没倒前有人做了logo还原，现在估计找不到了，去玩hd版算了吧</blockquote>
是啊，在国外下的UNDUB，发现也是这个版本，老外也用它<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">唯一的版本了，甚至还有统一标准的CRC32码

*****

####  oniwarud  
##### 538#       发表于 2021-12-13 23:13

老男人那边下的鬼泣3特别版一加载就闪退，有人知道原因吗，是模拟器不能运行还是游戏文件的问题

*****

####  LuciferGX  
##### 539#       发表于 2021-12-13 23:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53925047&amp;ptid=2037739" target="_blank">oniwarud 发表于 2021-12-13 23:13</a>

老男人那边下的鬼泣3特别版一加载就闪退，有人知道原因吗，是模拟器不能运行还是游戏文件的问题 ...</blockquote>
应该是镜像的问题，我在上面下的恶魔城暗黑诅咒也有这问题，换成其他地方找的另一个版本的镜像就正常了

*****

####  imosuke  
##### 540#       发表于 2021-12-14 03:39

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53862814&amp;ptid=2037739" target="_blank">天蓬元帅买买提 发表于 2021-12-9 09:09</a>

想问下坛友ps2的ISO都是在哪下的</blockquote>
琵琶行的一个帖子，国外网盘，只有英文游戏名，能找到一些比较偏门的游戏
[https://www.ppxclub.com/701818-1-1](https://www.ppxclub.com/701818-1-1)



*****

####  黄金时代  
##### 541#       发表于 2021-12-14 08:40

想找个异度传说1中文的下载，好多网盘都失效了

*****

####  桧山修之  
##### 542#       发表于 2021-12-14 08:52

865模拟凡人物语一进菜单就掉帧了，怎么设置都不行，是不是我的iso有问题？

*****

####  onemoment  
##### 543#       发表于 2021-12-14 09:06

 本帖最后由 onemoment 于 2021-12-14 10:44 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53927082&amp;ptid=2037739" target="_blank">黄金时代 发表于 2021-12-14 08:40</a>

想找个异度传说1中文的下载，好多网盘都失效了</blockquote>
异度传说1没汉化吧，异度传说3汉化了，以前倒是存过三部曲的日版资源看你需不需要吧
[https://pan.baidu.com/s/1W7f6BgvXjZKB-E083rhV0g](https://pan.baidu.com/s/1W7f6BgvXjZKB-E083rhV0g)   8a6h

3的盘2网盘下载有点问题<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">，重上传了盘2，试了下现在没问题了  

*****

####  fenrir  
##### 544#       发表于 2021-12-14 09:16

不知道865的能不能流畅玩机战alpha3

*****

####  tclm  
##### 545#       发表于 2021-12-14 09:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53927431&amp;ptid=2037739" target="_blank">fenrir 发表于 2021-12-14 09:16</a>
不知道865的能不能流畅玩机战alpha3</blockquote>
能

*****

####  yujie  
##### 546#       发表于 2021-12-14 10:16

845，机战试了一圈下来只有mx大地图拖慢以及战斗一部分攻击有拖慢
ogs都能基本满速，不知道是哪里设置不好

*****

####  lbj5454  
##### 547#       发表于 2021-12-14 11:19

888，特效全开，机战随便玩，就是玩异世纪传说(王牌机师)ACE3 的时候敌人一多会卡一下

*****

####  Suzutsuki.Mk.II  
##### 548#       发表于 2021-12-14 12:20

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53924585&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-13 22:31</a>

根据以前的经验估计的，dolphin在820上能达到65%的速度，835上就全速了，3ds也是一样，835要快近40%

我是 ...</blockquote>
这是3还是宴？咋设置的？我试了试都卡的要死

*****

####  lighttt  
##### 549#       发表于 2021-12-14 12:21

是华为的问题吗，读取不了文件夹里的游戏，要右下角进去才能打开

—— 来自 HUAWEI MRX-W29, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  保科智子  
##### 550#       发表于 2021-12-14 12:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53930364&amp;ptid=2037739" target="_blank">lighttt 发表于 2021-12-14 12:21</a>
是华为的问题吗，读取不了文件夹里的游戏，要右下角进去才能打开

—— 来自 HUAWEI MRX-W29, Android 10上 ...</blockquote>
好像权限问题，重新指定一下rom目录，一定要是本机路径。然后游戏列表就出来了。

*****

####  JudgmentEye  
##### 551#       发表于 2021-12-14 15:37

 本帖最后由 JudgmentEye 于 2021-12-14 15:42 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53917141&amp;ptid=2037739" target="_blank">lbj5454 发表于 2021-12-13 13:09</a>

最后用晓龙888玩上了，实在太爽了，问一下金手指功能怎么用？</blockquote>
游戏中右上暂停，选patch code ，再选第一项pnach，给金手指起个名，下面代码按以下格式输入

patch=1,EE,金手指码前半段地址,extended,金手指码后半段数值

例如机战z的金手指卡密码转换后就是

资金

patch=1,EE,20558560,extended,05F5E0FF

BS

patch=1,EE,205585A8,extended,000F423F

SR

patch=1,EE,0055856F,extended,00000063

*****

####  小泉花陽  
##### 552#       发表于 2021-12-14 16:04

下了OG、OG外传、Z还有SD高达neo，小时候玩机战啥都不懂也看不懂日文打通关就算牛逼，这次能把当年囫囵吞枣打通关又看不懂剧情的几部PS2机战放手机里随时怀旧重温了，这种能随便怀旧PS2游戏的幸福感比当初买PSV、NS等掌机真的是高太多了，搓玻璃技能也被最近一年平板玩原神、手机串流steam、PS5给锻炼出来了，现在搓玻璃玩家用机游戏真的是毫无压力<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  JAROD009  
##### 553#       发表于 2021-12-14 16:32

<img src="https://static.saraba1st.com/image/smiley/face2017/037.png" referrerpolicy="no-referrer">220收了个全新的小鸡X2蓝牙版，完美适配无延迟，不错

*****

####  Xenor  
##### 554#       发表于 2021-12-14 16:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53930345&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2021-12-14 12:20</a>

这是3还是宴？咋设置的？我试了试都卡的要死</blockquote>
是wii上的3，默认设置改2倍分辨率，很卡应该是模拟器版本对处理器负优化了，我用的是官方最新beta版本，试了2+外传，3、宴都是全速运行

*****

####  谷恒条野  
##### 555#         楼主| 发表于 2021-12-15 11:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53933758&amp;ptid=2037739" target="_blank">JAROD009 发表于 2021-12-14 16:32</a>

220收了个全新的小鸡X2蓝牙版，完美适配无延迟，不错</blockquote>
个人体感比wee1代延迟低，这个不知道是不是用的蓝牙5.0？wee1代好像是4.0来着？

*****

####  桧山修之  
##### 556#       发表于 2021-12-15 14:23

 本帖最后由 桧山修之 于 2021-12-15 14:25 编辑 

3a的游戏好像还不能完美模似，有点可惜

*****

####  sunnyjee  
##### 557#       发表于 2021-12-15 14:24

 本帖最后由 sunnyjee 于 2021-12-15 14:26 编辑 

试了下2017的神盾盒子

鬼武者2怎么设置都只能跑40帧 果然是cpu太弱了吗。。。说好的ns同款呐~~

*****

####  谷恒条野  
##### 558#         楼主| 发表于 2021-12-15 14:39

 本帖最后由 谷恒条野 于 2021-12-15 15:53 编辑 

alpha-702:

- Prevent Vulkan renderer being used on Mali devices.

- Fix OpenGL rendering on Pixel 6 and other newer Mali drivers.

- Implement full FPU mode (needed for NFS Carbon and other games).

- Tiny optimization to VU flags calculation.

- Fix emitting invalid instructions (NFS Carbon, possibly others).

- Fix crash when activating some overdrives in FFX with the Vulkan renderer.

- Fix vibrate on touch for dpad.

- Switch back to AAudio from oboe.

- Stop audio output on pause (reduce idle battery usage).

=======================================

用669版本时865玩ogs杂兵一多音乐就会拖慢，画面正常。不懂新版本怎么样。

看更新说明新版本是针对mali设备的，玛丽有救了？<img src="https://static.saraba1st.com/image/smiley/face2017/066.png" referrerpolicy="no-referrer">有玛丽机的可以试试。

鉴于贴吧置顶链接已被狗萌举报，转了一份Q群里面原版还有加了滤镜的mod版本方便没有play商店的人。

alpha-702：
[https://pan.baidu.com/s/115E2qYKXnKsYBWmAXDd4rw](https://pan.baidu.com/s/115E2qYKXnKsYBWmAXDd4rw)

yh6f

注意：卸载模拟器会把记忆卡那些文件都删掉的，注意备份。

记忆卡路径

Android/data/xyz.aethersx2.android/files/memcards/

*****

####  彩虹肥宅  
##### 559#       发表于 2021-12-15 14:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53945608&amp;ptid=2037739" target="_blank">sunnyjee 发表于 2021-12-15 14:24</a>
试了下2017的神盾盒子

鬼武者2怎么设置都只能跑40帧 果然是cpu太弱了吗。。。说好的ns同款呐~~

 ...</blockquote>
你觉得ns性能很强吗<img src="https://static.saraba1st.com/image/smiley/face2017/018.png" referrerpolicy="no-referrer">

—— 来自 Xiaomi MI 6, Android 9上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  艾尔特翔  
##### 560#       发表于 2021-12-15 15:50

问一个问题，这模拟器的记录卡在哪里能找到？

*****

####  谷恒条野  
##### 561#         楼主| 发表于 2021-12-15 15:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53946628&amp;ptid=2037739" target="_blank">艾尔特翔 发表于 2021-12-15 15:50</a>

问一个问题，这模拟器的记录卡在哪里能找到？</blockquote>
Android/data/xyz.aethersx2.android/files/memcards/

*****

####  艾尔特翔  
##### 562#       发表于 2021-12-15 15:52

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53946658&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-15 15:52</a>

Android/data/xyz.aethersx2.android/files/memcards/</blockquote>
太感谢了

*****

####  bk_201  
##### 563#       发表于 2021-12-15 15:56

所以有什么好用的拉伸手柄吗？

看了下kishi也太贵了，这个延迟咋样？

有没有便宜好用的

*****

####  JAROD009  
##### 564#       发表于 2021-12-15 16:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53946707&amp;ptid=2037739" target="_blank">bk_201 发表于 2021-12-15 15:56</a>

所以有什么好用的拉伸手柄吗？

看了下kishi也太贵了，这个延迟咋样？

有没有便宜好用的 ...</blockquote>
小鸡X2，OTG十字键版咸鱼全新290左右，蓝牙版220

OTG版可以边充边玩，蓝牙版可以给不同设备用，各有优点

我这边是平板和手机都用，所以买的蓝牙版，目前用起来除了摇杆感觉阻尼和回弹不习惯其它比较满意

*****

####  bk_201  
##### 565#       发表于 2021-12-15 17:17

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53947180&amp;ptid=2037739" target="_blank">JAROD009 发表于 2021-12-15 16:33</a>
小鸡X2，OTG十字键版咸鱼全新290左右，蓝牙版220

OTG版可以边充边玩，蓝牙版可以给不同设备用，各有优点

 ...</blockquote>
感谢推荐，虽然已经手快买了赛太克7007<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">

等到手试试，如果延迟太高就试试小鸡otg版

—— 来自 vivo V1981A, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  掘墓人  
##### 566#       发表于 2021-12-15 21:20

啊草买了kishi，结果红米K30Pro装不进去

Kishi好像只适合背后摄像头在左边的，K30Pro这种背后中间的摄像头会顶住塞不进去

好心塞，只能退货了。小鸡X2的蓝牙版能用在K30Pro上吗？

—— 来自 Xiaomi Redmi K30 Pro Zoom Edition, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  黄金时代  
##### 567#       发表于 2021-12-16 02:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53927319&amp;ptid=2037739" target="_blank">onemoment 发表于 2021-12-14 09:06</a>

异度传说1没汉化吧，异度传说3汉化了，以前倒是存过三部曲的日版资源看你需不需要吧

https://pan.baidu.co ...</blockquote>
感谢，日版从语音到习惯比美版好太多了。

*****

####  yunalesca  
##### 568#       发表于 2021-12-16 10:03

昨天手柄到了，跟大家分享一下。

<img src="https://img.saraba1st.com/forum/202112/16/093127owb57escip8bt12o.jpg" referrerpolicy="no-referrer">

<strong>960947574.jpg</strong> (580.71 KB, 下载次数: 0)

下载附件

2021-12-16 09:31 上传

首先是预料之中的部分：

按键手感确实还不错，能够接受，不管是右边的xyab键还是L12R12肩键，到底北通是有做手柄的经验的。

左边方向键提供了十字键改件，取代默认的手机圆盘方向键。这个可以自己更换（直接硬插拔）下方实际就是个十字键的底座。

直接连接蓝牙即可连接。

手柄键位方面默认设置直接进AetherSX2就可以直接键位对应，不需要额外设置（本身aetherSX2好像也不支持自定义键位）。

然后是预料之外的部分：

这个手柄……其实是有右摇杆的……那个XYAB键位所在的红色圆盘本身就是右摇杆（或者说右滑杆）……该设计应该是为了手游搓玻璃指向性技能用的……再强调一下，这玩意真的就是右摇杆，进模拟器后也可以证实这一点。

由于右摇杆和XYAB在一起，如果某个操作需要只操作右摇杆 ，而不按下XYAB的话……需要一定时间适应……

没有start和select键，从面板上直观就没看到这两个键，尤其在AetherSX2内不能自由设置按键，也没法把右方多出来的CDZ等键位设置为start和select，这俩键目前只能用模拟器的虚拟按键，

虽然说从操作习惯上还可以接受（在手柄正中心按start），但是从物理键位上不设计这两个键还是有点问题。

手机的连接设置也有点问题，虽然手柄本身在设置好初次连接之后，就很省心（手柄开机自动匹配，无需设置自动启动），但是首次与手机链接实在是有点麻烦，首先要下北通APP，还要进行高级链接激活，整个过程比较繁琐。

总结：你说这玩意玩模拟器行不行？如果用行或者不行来回答的话，肯定是“行”。

         优点：

         各键位设置基本能够满足模拟器使用的需求

         完成设置之后使用起来也比较简单

         按键手感不错

         重量适中

         对扣式设计带来很好的便携性

         缺点：

         右摇杆和xyab键设计在一起，完全不符合主机普通手柄的操作逻辑，真要使用的话需要适应。

         没有物理start和select键。

         左边十字键提供的十字键键帽不是标准的十字键键帽，当然这个是北通的老问题了。

         初次设置非常繁琐，还需要下专用app激活。

         官方价格贵的离谱，真要买还是走咸鱼吧，不到300可以拿到。

总结：这玩意设计出来其实是为了玩lol、王者荣耀等手游moba的，从那个右摇杆+键位的混合设计就可以看出来（毕竟这玩意是G2的升级版，G2甚至没有右边这半边）。

         只能说，G3还是考虑到了玩模拟器的需求的，毕竟从功能上它还是提供了所需的全部功能，它还设计了一个锁盘开关，可以把右摇杆锁住，只提供键位功能，但是这样又无法使用右摇杆了，有点……。

         推荐给：除了玩模拟器以外，平时有玩手机moba，适配G3的主要设计，此外，对键位手感有需求的玩家。 

         不推荐给：根本不玩手机moba，只想拿来玩模拟器，同时对键位手感没啥需求的玩家。         

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| xbhuang| + 1|好评加鹅|

查看全部评分

*****

####  cy1988813  
##### 569#       发表于 2021-12-16 10:22

为啥北欧女神2打不开啊

骁龙888应该能玩的啊

目前手头有的几个PS2游戏都试过了，就北欧女神2打不开，黑屏无反应，银河游侠帧数太低，只有不到二十帧，其他都能流畅玩

*****

####  wujae  
##### 570#       发表于 2021-12-16 10:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53955889&amp;ptid=2037739" target="_blank">yunalesca 发表于 2021-12-16 10:03</a>

昨天手柄到了，跟大家分享一下。</blockquote>
本来想买这个的，但是看到右摇杆设计成这样就知道玩模拟器肯定别扭，所以还是买了雷蛇kishi。不过看到评价kishi品控很糟糕，现在很迷茫<img src="https://static.saraba1st.com/image/smiley/face2017/069.png" referrerpolicy="no-referrer">



*****

####  JAROD009  
##### 571#       发表于 2021-12-16 10:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53951349&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-15 21:20</a>

啊草买了kishi，结果红米K30Pro装不进去

Kishi好像只适合背后摄像头在左边的，K30Pro这种背后中间的摄像头 ...</blockquote>
K30SU试了蓝牙版没问题，而且小鸡X2拉伸后右侧的下沉空间比较大，对于突出多的摄像头模组比较友好

*****

####  yunalesca  
##### 572#       发表于 2021-12-16 11:01

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53956504&amp;ptid=2037739" target="_blank">wujae 发表于 2021-12-16 10:41</a>

本来想买这个的，但是看到右摇杆设计成这样就知道玩模拟器肯定别扭，所以还是买了雷蛇kishi。不过看到评 ...</blockquote>
常规手柄布局的试试小鸡gamesir x2。

我一开始也是x2和g3二选一后选了G3。

本帖有不少人买了x2，不知道大家对于蓝牙延迟和按键手感的评价如何。

如果都不错的话，玩模拟器还是推荐x2。

*****

####  Suzutsuki.Mk.II  
##### 573#       发表于 2021-12-16 11:14

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53956213&amp;ptid=2037739" target="_blank">cy1988813 发表于 2021-12-16 10:22</a>

为啥北欧女神2打不开啊

骁龙888应该能玩的啊

目前手头有的几个PS2游戏都试过了，就北欧女神2打不开，黑屏无 ...</blockquote>
开快速内存访问进游戏，进去后关闭快速内存访问

*****

####  magpte  
##### 574#       发表于 2021-12-16 11:24

发哥1kplus，xs卡到不能自理，新版本vulkan还说驱动不支持dualsource blend

—— 来自 Xiaomi M2006J10C, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  cy1988813  
##### 575#       发表于 2021-12-16 11:56

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53957043&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2021-12-16 11:14</a>

开快速内存访问进游戏，进去后关闭快速内存访问</blockquote>
谢谢

那以后每次进游戏都要这么弄吗？

*****

####  黄金时代  
##### 576#       发表于 2021-12-16 12:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53956213&amp;ptid=2037739" target="_blank">cy1988813 发表于 2021-12-16 10:22</a>
为啥北欧女神2打不开啊

骁龙888应该能玩的啊

目前手头有的几个PS2游戏都试过了，就北欧女神2打不开，黑屏无 ...</blockquote>
同问，北妹2一样黑屏，之前看到有能运行的同学，求共享一下ISō

*****

####  yunalesca  
##### 577#       发表于 2021-12-16 13:45

就用573楼的办法，可以进vp2，而且目前似乎只需要首次进游戏需要，不需要每次进游戏都如此……

证据嘛……

<img src="https://img.saraba1st.com/forum/202112/16/134508jyh1emebb0syue13.jpg" referrerpolicy="no-referrer">

<strong>753898164.jpg</strong> (121.07 KB, 下载次数: 0)

下载附件

2021-12-16 13:45 上传

<img src="https://img.saraba1st.com/forum/202112/16/134519vgtn7qantnaqgnyi.jpg" referrerpolicy="no-referrer">

<strong>709355729.jpg</strong> (141.13 KB, 下载次数: 0)

下载附件

2021-12-16 13:45 上传

不过我这855，用702客户端部分场景真的挺卡的……

*****

####  PYY  
##### 578#       发表于 2021-12-16 17:03

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53956213&amp;ptid=2037739" target="_blank">cy1988813 发表于 2021-12-16 10:22:54</a>
为啥北欧女神2打不开啊

骁龙888应该能玩的啊

目前手头有的几个PS2游戏都试过了，就北欧女神2打不开，黑屏无 ...</blockquote>北妹2，应用设置-启用快速内存关了，下面两个开启。
我玩到后面了。
默认设置有速度问题，自己调整后又有图像问题，暂时还不能完美。
看之后版本更新了，现在只能说能玩。

[  -- 来自 能看大图的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  Suzutsuki.Mk.II  
##### 579#       发表于 2021-12-16 17:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53957688&amp;ptid=2037739" target="_blank">cy1988813 发表于 2021-12-16 11:56</a>

谢谢

那以后每次进游戏都要这么弄吗？</blockquote>
下面有人测了，但是游戏中必须关闭快速内存访问，不然有些地方会闪退

*****

####  gxy  
##### 580#       发表于 2021-12-16 17:21

真女神3 v模式在天台剧情后必闪退，OpenGL模式，很多墙壁透明，软件模式画面没问题，但是帧数有时很低，也不能调分辨率

*****

####  PYY  
##### 581#       发表于 2021-12-16 17:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53961989&amp;ptid=2037739" target="_blank">gxy 发表于 2021-12-16 17:21:12</a>
真女神3 v模式在天台剧情后必闪退，OpenGL模式，很多墙壁透明，软件模式画面没问题，但是帧数有时很低，也 ...</blockquote>分辨率就是那个
应用设置-图像设置-分辨率缩放
就是电脑版的那个内部分辨率的意思。

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  gxy  
##### 582#       发表于 2021-12-16 17:36

<blockquote>PYY 发表于 2021-12-16 17:29
分辨率就是那个

应用设置-图像设置-分辨率缩放

就是电脑版的那个内部分辨率的意思。</blockquote>
我的意思是，软件渲染模式下是固定一倍分辨率，而且已经做不到满速运行了，总之真3目前三个渲染模式都无法正常游玩，我是骁龙855

*****

####  JudgmentEye  
##### 583#       发表于 2021-12-16 18:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53961989&amp;ptid=2037739" target="_blank">gxy 发表于 2021-12-16 17:21</a>

真女神3 v模式在天台剧情后必闪退，OpenGL模式，很多墙壁透明，软件模式画面没问题，但是帧数有时很低，也 ...</blockquote>
汉化版cg的问题，先用日版过去存档再换回汉化版，不过有hd版了为啥还要玩ps2版

*****

####  xbhuang  
##### 584#       发表于 2021-12-16 19:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53955889&amp;ptid=2037739" target="_blank">yunalesca 发表于 2021-12-16 10:03</a>
昨天手柄到了，跟大家分享一下。</blockquote>
有没有试过其他模拟器？这四个额外的按键能不能映射？还有官方app设置后就能卸载吗，还是说一定要同时后台开着

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  xbhuang  
##### 585#       发表于 2021-12-16 22:11

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53951349&amp;ptid=2037739" target="_blank">掘墓人 发表于 2021-12-15 21:20</a>
啊草买了kishi，结果红米K30Pro装不进去

Kishi好像只适合背后摄像头在左边的，K30Pro这种背后中间的摄像头 ...</blockquote>
啊这，雷蛇这设计怪啊，还挑手机的吗？k30塞不进去，是不是K20也不行？

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  suoleisita  
##### 586#       发表于 2021-12-16 22:17

这玩意能不能把差不多亡了的拉伸手柄救回来，，

*****

####  烧刀  
##### 587#       发表于 2021-12-16 22:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53947180&amp;ptid=2037739" target="_blank">JAROD009 发表于 2021-12-15 16:33</a>

小鸡X2，OTG十字键版咸鱼全新290左右，蓝牙版220

OTG版可以边充边玩，蓝牙版可以给不同设备用，各有优点

 ...</blockquote>
220的哪家？没找到。。。方便发一下吗 

*****

####  L.L  
##### 588#       发表于 2021-12-16 23:31

<img src="https://static.saraba1st.com/image/smiley/face2017/075.png" referrerpolicy="no-referrer">怀念了一波青春。

*****

####  22174559  
##### 589#       发表于 2021-12-17 00:04

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  JAROD009  
##### 590#       发表于 2021-12-17 01:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53965666&amp;ptid=2037739" target="_blank">烧刀 发表于 2021-12-16 22:21</a>
220的哪家？没找到。。。方便发一下吗</blockquote>
随便找了个挂240的，问了下220能不能出一口成交<img src="https://static.saraba1st.com/image/smiley/face2017/034.png" referrerpolicy="no-referrer">

*****

####  bluesss  
##### 591#       发表于 2021-12-17 02:23

机战alpha3 画面抖动，应该怎么设置？

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  烧刀  
##### 592#       发表于 2021-12-17 07:43

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53967440&amp;ptid=2037739" target="_blank">JAROD009 发表于 2021-12-17 01:30</a>

随便找了个挂240的，问了下220能不能出一口成交</blockquote>
问了不行 我私信你下。。

*****

####  头文字D  
##### 593#       发表于 2021-12-17 07:55

tab s7三星865，开vulcan樱花大战5战斗基本满速，和wiiu版本差不多，终于不用忍受英文语音

*****

####  半江瑟瑟半江红  
##### 594#       发表于 2021-12-17 07:59

这个模拟器能运行ps1游戏吗

—— 来自 HUAWEI NOP-AN00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  yunalesca  
##### 595#       发表于 2021-12-17 08:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53963321&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-16 19:10</a>

有没有试过其他模拟器？这四个额外的按键能不能映射？还有官方app设置后就能卸载吗，还是说一定要同时后 ...</blockquote>
1.  用小鸡模拟器试了下GBA SFC PSP的模拟器，手柄也能自动匹配键位

2.  同样是小鸡模拟器，可以映射，我把c键d键设为select和start毫无问题

3.  不需要开启app，那个app一般是在玩手游moba的时候激活，平时玩模拟器不需要那个app

*****

####  yunalesca  
##### 596#       发表于 2021-12-17 08:41

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53966778&amp;ptid=2037739" target="_blank">22174559 发表于 2021-12-17 00:04</a>

越更新越卡？</blockquote>
不，更新前的658更卡……702明显是有改善的，但是还是个别场景有点卡

*****

####  Lilithy  
##### 597#       发表于 2021-12-17 09:31

702之后，麒麟980，女厕2的选地图画面能全速，进去地图还是30%以下

----发送自 [HUAWEI PCT-AL10,Android 10](http://stage1.5j4m.com/?1.37)

*****

####  月神侠  
##### 598#       发表于 2021-12-17 09:37

提示: 作者被禁止或删除 内容自动屏蔽

*****

####  掘墓人  
##### 599#       发表于 2021-12-17 10:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53965553&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-16 22:11</a>
啊这，雷蛇这设计怪啊，还挑手机的吗？k30塞不进去，是不是K20也不行？

—— 来自 S1Fun ...</blockquote>
K20的摄像头也在中间吧，虽然比K30Pro的大圆盘小一些

目测够呛

—— 来自 Xiaomi Redmi K30 Pro Zoom Edition, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  bk_201  
##### 600#       发表于 2021-12-17 10:24

买的赛太克7007F到了，但是怎么按键都对不上，而且没找到设置按键的地方<img src="https://static.saraba1st.com/image/smiley/face2017/091.png" referrerpolicy="no-referrer">



*****

####  谷恒条野  
##### 601#         楼主| 发表于 2021-12-17 12:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53969805&amp;ptid=2037739" target="_blank">bk_201 发表于 2021-12-17 10:24</a>
买的赛太克7007F到了，但是怎么按键都对不上，而且没找到设置按键的地方 ...</blockquote>
看看说明书是不是有多个配对模式的？我有个ipega 9087s有2个安卓模式，其中一个模式按键是不对的。另一个模式正常，但是手柄自动休眠或者唤醒重连时模拟器会重启游戏。<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

*****

####  xbhuang  
##### 602#       发表于 2021-12-17 14:07

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53968521&amp;ptid=2037739" target="_blank">yunalesca 发表于 2021-12-17 08:40</a>
1.  用小鸡模拟器试了下GBA SFC PSP的模拟器，手柄也能自动匹配键位

2.  同样是小鸡模拟器，可以映射，我 ...</blockquote>
最后还想问个问题，就是steamlink串流的时候，能单独显示一个右摇杆的触控按键出来吗？
感觉目前为止还是没有一个最适合手机用的手柄，kishi还存在厚度问题手机不匹配的

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  bk_201  
##### 603#       发表于 2021-12-17 15:10

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53972355&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-17 12:58</a>

看看说明书是不是有多个配对模式的？我有个ipega 9087s有2个安卓模式，其中一个模式按键是不对的。另一个 ...</blockquote>
去谷哥下载了他的专用app shootingplus V3，可以配置按键了

然后本质似乎是模拟点击屏幕上的虚拟按键而不是直接识别成手柄？

试了下神之手，只能说需要连打的动作游戏不是很合适，玩非动作游戏应该没什么问题

*****

####  半江瑟瑟半江红  
##### 604#       发表于 2021-12-17 19:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53969151&amp;ptid=2037739" target="_blank">月神侠 发表于 2021-12-17 09:37</a>
可以的，不过还是建议用PS模拟器</blockquote>
谢谢
就是打算玩机战阿花1
发现运行不了，需要怎么设置吗？

*****

####  Xenor  
##### 605#       发表于 2021-12-17 20:23

PS2版的深渊传说是不是不如3DS版画面好啊<img src="https://static.saraba1st.com/image/smiley/face2017/091.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/17/202313myv2ievyysvj2fgh.jpg" referrerpolicy="no-referrer">

<strong>toa1.JPG</strong> (220.93 KB, 下载次数: 0)

下载附件

2021-12-17 20:23 上传

<img src="https://img.saraba1st.com/forum/202112/17/202314lrury4wm10dc1d6q.jpg" referrerpolicy="no-referrer">

<strong>toa2.JPG</strong> (219.8 KB, 下载次数: 0)

下载附件

2021-12-17 20:23 上传

<img src="https://img.saraba1st.com/forum/202112/17/202314ds5vp036wq6qhs26.jpg" referrerpolicy="no-referrer">

<strong>toa3.jpg</strong> (133.68 KB, 下载次数: 0)

下载附件

2021-12-17 20:23 上传

<img src="https://img.saraba1st.com/forum/202112/17/202314p6xbwhwddzxrgjdi.jpg" referrerpolicy="no-referrer">

<strong>toa4.jpg</strong> (188.91 KB, 下载次数: 0)

下载附件

2021-12-17 20:23 上传

<img src="https://img.saraba1st.com/forum/202112/17/202315jdi6z6f6mimidm66.jpg" referrerpolicy="no-referrer">

<strong>toa5.JPG</strong> (178.05 KB, 下载次数: 0)

下载附件

2021-12-17 20:23 上传

*****

####  慕容断月  
##### 606#       发表于 2021-12-17 23:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53978860&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-17 20:23</a>

PS2版的深渊传说是不是不如3DS版画面好啊</blockquote>
是你的错觉，模型面数都是ps2版高，贴图分辨率也是

*****

####  allenz3  
##### 607#       发表于 2021-12-17 23:54

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53969805&amp;ptid=2037739" target="_blank">bk_201 发表于 2021-12-17 10:24</a>
买的赛太克7007F到了，但是怎么按键都对不上，而且没找到设置按键的地方 ...</blockquote>
按住home+x切换到hid模式（第三盏灯），然后蓝牙配对就行了，那个软件根本不用下<img src="https://static.saraba1st.com/image/smiley/face2017/034.png" referrerpolicy="no-referrer">

—— 来自 Sony XQ-AS72, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2-play

*****

####  highsky  
##### 608#       发表于 2021-12-17 23:54

<blockquote>bk_201 发表于 2021-12-17 15:10
去谷哥下载了他的专用app shootingplus V3，可以配置按键了

然后本质似乎是模拟点击屏幕上的虚拟按键而 ...</blockquote>
手柄打开后按住x和home键不放，开启xinput模式，然后再用手机蓝牙连，根本不用映射，ra和以太都直接支持的

*****

####  bk_201  
##### 609#       发表于 2021-12-18 00:02

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53981777&amp;ptid=2037739" target="_blank">allenz3 发表于 2021-12-17 23:54</a>

按住home+x切换到hid模式（第三盏灯），然后蓝牙配对就行了，那个软件根本不用下

—— 来自 Sony ...</blockquote>
草，原来是这样，我还连的第一个安卓模式<img src="https://static.saraba1st.com/image/smiley/face2017/021.png" referrerpolicy="no-referrer">

*****

####  津上翔一  
##### 610#       发表于 2021-12-18 18:32

每次在游戏时手柄开关都会重启游戏，是我个人问题还是通病啊？

*****

####  xbhuang  
##### 611#       发表于 2021-12-18 18:35

金手指哪里搜？想要改机战的钱

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  谷恒条野  
##### 612#         楼主| 发表于 2021-12-19 01:55

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53989681&amp;ptid=2037739" target="_blank">津上翔一 发表于 2021-12-18 18:32</a>
每次在游戏时手柄开关都会重启游戏，是我个人问题还是通病啊？</blockquote>
什么型号的手柄？我试过的手柄里ipega 9087s，还有个中兴FUN盒子带的手柄休眠或重连模拟器会重启，其他的不会，这个问题感觉很迷<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">。

*****

####  yunalesca  
##### 613#       发表于 2021-12-19 10:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53973476&amp;ptid=2037739" target="_blank">xbhuang 发表于 2021-12-17 14:07</a>

最后还想问个问题，就是steamlink串流的时候，能单独显示一个右摇杆的触控按键出来吗？

感觉目前为止还是 ...</blockquote>
steam link没试验，平时用手机串流steam的场景我这边几乎用不到……

*****

####  谷恒条野  
##### 614#         楼主| 发表于 2021-12-23 23:04

alpha-720：
- Fix constant colour/alpha blending on Mali devices (e.g. Silent Hill 2).
- OpenGL performance optimizations (e.g. Burnout 3 30fps -&gt; 45fps at 3x on 870).
- Fix depth copies/readbacks in OpenGL (e.g. SMT Nocturne).
- Minor rendering fix for Vulkan in some games (e.g. Xenosaga).
- Fix Traditional Chinese in language selector.

*****

####  PYY  
##### 615#       发表于 2021-12-24 10:53

高通888，每次出新版我都会用北妹2玩十分钟，
以前掉帧的地方（第一个城镇右边，森林剧情）提高了几帧，还是只能勉强玩的程度。

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  Xenor  
##### 616#       发表于 2021-12-25 22:48

好猛啊，产生高通晓龙820比英特尔酷睿i5-460m+hd5650强二倍的幻觉了<img src="https://static.saraba1st.com/image/smiley/face2017/159.png" referrerpolicy="no-referrer">

<img src="https://img.saraba1st.com/forum/202112/25/224348d3624406tk243b6h.jpg" referrerpolicy="no-referrer">

<strong>p1.jpg</strong> (95.58 KB, 下载次数: 0)

下载附件

2021-12-25 22:43 上传

<img src="https://img.saraba1st.com/forum/202112/25/224349de3ekkfg2ejkzrle.jpg" referrerpolicy="no-referrer">

<strong>p2.jpg</strong> (162.88 KB, 下载次数: 0)

下载附件

2021-12-25 22:43 上传

<img src="https://img.saraba1st.com/forum/202112/25/224349n2qbkmfm4l742rnz.jpg" referrerpolicy="no-referrer">

<strong>s1.jpg</strong> (145.62 KB, 下载次数: 0)

下载附件

2021-12-25 22:43 上传

<img src="https://img.saraba1st.com/forum/202112/25/224350gxri4ixzzxtboro2.jpg" referrerpolicy="no-referrer">

<strong>s2.jpg</strong> (160.7 KB, 下载次数: 0)

下载附件

2021-12-25 22:43 上传

迫不及待想在835上试试全速效果，然而空间不够<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  桜庭ななみ  
##### 617#       发表于 2021-12-26 09:59

ios用户羡慕的很

*****

####  lee0709  
##### 618#       发表于 2021-12-26 18:22

很好，x1手柄不认l2 r2已经修复了

----发送自 [Xiaomi M2007J3SC,Android 11](http://stage1.5j4m.com/?1.37)

*****

####  a2276382  
##### 619#       发表于 2021-12-26 21:23

这p3f模拟效果 太好了 还是天玑1000处理器 可惜没有中文<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  佐伯香織  
##### 620#       发表于 2021-12-26 21:26

有win10运行的方法吗，pcsx2几个动画渲染会内存溢出的游戏，这模拟器用vulkan完美解决

*****

####  a2276382  
##### 621#       发表于 2021-12-26 21:45

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54055011&amp;ptid=2037739" target="_blank">佐伯香織 发表于 2021-12-26 21:26</a>
有win10运行的方法吗，pcsx2几个动画渲染会内存溢出的游戏，这模拟器用vulkan完美解决 ...</blockquote>
win11 可以直接装安卓 win10试试安卓模拟器<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  reficul  
##### 622#       发表于 2021-12-26 22:04

什么套娃。。。win11通过安卓模拟器跑PS2模拟器

*****

####  Xenor  
##### 623#       发表于 2021-12-26 22:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54048281&amp;ptid=2037739" target="_blank">桜庭ななみ 发表于 2021-12-26 09:59</a>

ios用户羡慕的很</blockquote>
高贵的ios用户用零头钱就能买个845以上的安卓机了吧…

*****

####  tamatama  
##### 624#       发表于 2021-12-26 23:34

试了下魔塔大陆，进菜单还有战斗结算的时候会有卡顿、爆音。看兼容列表里的建议，关闭Enable INTC Spin Detection在app上也找不到，有啥好的解决办法么？

*****

####  桜庭ななみ  
##### 625#       发表于 2021-12-27 01:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54056010&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-26 22:42</a>
高贵的ios用户用零头钱就能买个845以上的安卓机了吧…</blockquote>
845洋垃圾的确也就300块左右，但问题是平时还要多带个手机多麻烦。

*****

####  津上翔一  
##### 626#       发表于 2021-12-27 15:18

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=53996234&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2021-12-19 01:55</a>

什么型号的手柄？我试过的手柄里ipega 9087s，还有个中兴FUN盒子带的手柄休眠或重连模拟器会重启，其他的 ...</blockquote>
pdd买的杂牌手柄<img src="https://static.saraba1st.com/image/smiley/face2017/002.png" referrerpolicy="no-referrer">居然还有不会的啊

*****

####  津上翔一  
##### 627#       发表于 2021-12-27 15:58

 本帖最后由 津上翔一 于 2021-12-27 16:08 编辑 

晕死，换成ps4手柄链接手柄后断电模拟器也不会重启，看来是手柄问题，求拉伸手柄推荐

*****

####  桧山修之  
##### 628#       发表于 2021-12-28 15:47

865玩了好几个游戏，除了机战阿尔法3和og算是完美之外，其他的都有不少问题，凡人物语的剧情动画掉帧问题，影之心2直接黑屏都不能解决，宿命传说r直接不能玩，都太可惜了

*****

####  谷恒条野  
##### 629#         楼主| 发表于 2021-12-28 17:44

 本帖最后由 谷恒条野 于 2021-12-28 17:45 编辑 
<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54063931&amp;ptid=2037739" target="_blank">津上翔一 发表于 2021-12-27 15:58</a>

晕死，换成ps4手柄链接手柄后断电模拟器也不会重启，看来是手柄问题，求拉伸手柄推荐 ...</blockquote>
在1楼整理了一些本楼里出现过的手柄信息，可以对照楼层找参考下。

*****

####  谷恒条野  
##### 630#         楼主| 发表于 2021-12-29 01:05

 本帖最后由 谷恒条野 于 2021-12-29 01:27 编辑 

官网上线:
[https://www.aethersx2.com/ ](https://www.aethersx2.com/ )
作者上次为了买测试设备和让无法使用谷歌的用户能正常下载搞了个众筹，想不到这么快就上线了。
里面还有封闭测试的版本，封测的已经到913了，看反馈封测的是没中文的，但是已经支持按键映射了，也多了些设置。
封测的好像bug也比较多，等公测版本更新了。<img src="https://static.saraba1st.com/image/smiley/face2017/033.png" referrerpolicy="no-referrer">



*****

####  津上翔一  
##### 631#       发表于 2021-12-30 22:35

听说9字系列对麒麟cpu有优化

*****

####  谷恒条野  
##### 632#         楼主| 发表于 2022-1-10 11:00

play alpha-996：

新功能

* OLD SAVE STATES ARE NOT COMPATIBLE WITH THIS UPDATE!

* Add controller mapping and hotkeys. Chords are supported.

* Expose more GS options.

* Support trilinear filtering and software blending in Vulkan renderer. If you have rendering glitches, disable Texture barriers in Advanced Settings.

* Fix issues when combining texture preloading and GPU palette textures.

* Non-DSB path for Vulkan renderer.

* Add aspect ratio and software renderer FMV switch.

* Fix const prop bug in recompiler.

看贴吧996好像发热严重点，而且问题有比较多，但是对麒麟有优化，对某些游戏兼容性会好点，谨慎更新吧。

*****

####  谷恒条野  
##### 633#         楼主| 发表于 2022-1-10 11:01

[https://tieba.baidu.com/p/7689715688](https://tieba.baidu.com/p/7689715688)

贴吧有人做了宿命传说的专用版本。

*****

####  Suzutsuki.Mk.II  
##### 634#       发表于 2022-1-10 12:50

 本帖最后由 Suzutsuki.Mk.II 于 2022-1-10 13:14 编辑 

看了下，TODR的问题说到底就是补丁效果对不上

*****

####  astkaasa  
##### 635#       发表于 2022-1-11 09:34

求北欧女神2配置分享

*****

####  shamisen  
##### 636#       发表于 2022-1-11 10:34

<blockquote>astkaasa 发表于 2022-1-11 09:34
求北欧女神2配置分享</blockquote>
865 996 默认配置外把图像设置最底下4个点上就基本满帧了

<img src="https://img.saraba1st.com/forum/202201/11/103427xyey6auolguo87yy.jpg" referrerpolicy="no-referrer">

<strong>Screenshot_2022-01-11-10-32-37-476_xyz.aethersx2.android.jpg</strong> (196.01 KB, 下载次数: 0)

下载附件

2022-1-11 10:34 上传

*****

####  shiko  
##### 637#       发表于 2022-1-11 10:35

鬼泣3的汉化版一律运行不了，日版倒是能跑，但是过剧情的时候声音会有拖慢和音画不同步。。。

*****

####  谷恒条野  
##### 638#         楼主| 发表于 2022-1-11 12:42

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54243842&amp;ptid=2037739" target="_blank">shiko 发表于 2022-1-11 10:35</a>

鬼泣3的汉化版一律运行不了，日版倒是能跑，但是过剧情的时候声音会有拖慢和音画不同步。。。 ...</blockquote>
[https://pan.baidu.com/s/1nCcN5uywnQErwSG0VZ5hhg](https://pan.baidu.com/s/1nCcN5uywnQErwSG0VZ5hhg)

gwyq

这个可以进去

*****

####  astkaasa  
##### 639#       发表于 2022-1-11 13:12

<blockquote>shamisen 发表于 2022-1-11 10:34
865 996 默认配置外把图像设置最底下4个点上就基本满帧了</blockquote>
多谢好像是可以了，870能开3x

*****

####  navarra  
##### 640#       发表于 2022-1-11 18:20

play商店已更新alpha-1021，带来大量更新

*****

####  谷恒条野  
##### 641#         楼主| 发表于 2022-1-11 19:48

play alpha-1021:

* Minor optimization to EE/VU recompilers (+3-5% in GoW2).

* Improve texture preloading performance.

* Improve internal frame rate detection.

* Fix mipmapping in some games (e.g. Jak 2).

* Fix auto hide controller option when starting.

* Add per-game controller bindings (via "copy controller bindings").

* Fix CRC hack option not togglable while ingame.

暂时观望

*****

####  PYY  
##### 642#       发表于 2022-1-11 20:11

一般官网比play晚多久更新？
官网还是996。

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  谷恒条野  
##### 643#         楼主| 发表于 2022-1-11 20:29

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54251214&amp;ptid=2037739" target="_blank">PYY 发表于 2022-1-11 20:11</a>

一般官网比play晚多久更新？

官网还是996。</blockquote>
我看了下版本信息，play版显示的和封测版11284-1021版一样的，应该是同一个。<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">

*****

####  精钢魔像  
##### 644#       发表于 2022-1-11 20:33

996好像是比720热一点

不过我的手机没到发热严重的程度

*****

####  幽灵胖胖  
##### 645#       发表于 2022-1-11 20:50

还是720中，观望等正式版，花2每天两关推进中

*****

####  虚无连斩  
##### 646#       发表于 2022-1-11 22:14

870试了试皇牌空战5……偶尔会卡一下，又不知道要怎么设置，好难受<img src="https://static.saraba1st.com/image/smiley/face2017/124.png" referrerpolicy="no-referrer">

*****

####  ChrisSnake  
##### 647#       发表于 2022-1-12 12:06

请教下能玩北妹2吗?

*****

####  谷恒条野  
##### 648#         楼主| 发表于 2022-1-12 12:49

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54257812&amp;ptid=2037739" target="_blank">ChrisSnake 发表于 2022-1-12 12:06</a>

请教下能玩北妹2吗?</blockquote>
可以啊，636L发的就是北妹2怎么设置的。

*****

####  lee0709  
##### 649#       发表于 2022-1-12 20:16

发现一个有趣的更新，1021版本里战国Basara2 英雄外传，每次进入战斗之前显示所有武将头像那个过场，可以加速到300%-400%的速度了，之前这一段动画加速只能到110%左右

*****

####  nilren  
##### 650#       发表于 2022-1-13 01:12

楼主好棒

关注本帖，等哪天想怀旧的时候来翻翻

*****

####  navarra  
##### 651#       发表于 2022-1-13 06:21

顺便一提，pc版pcsx2最新开发版终于加入了vulkan渲染的支持……

—— 来自 samsung SM-G9880, Android 11上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.2

*****

####  alexwu  
##### 652#       发表于 2022-1-13 07:28

<blockquote>navarra 发表于 2022-1-13 06:21
顺便一提，pc版pcsx2最新开发版终于加入了vulkan渲染的支持……

—— 来自 samsung SM-G9880, Android 11 ...</blockquote>
咦，他们不是一直嘴硬ps2架构太特殊不是现在主流的cpu-显卡架构所以vulkan没啥提升一直拒绝加入么，这是吹的什么风

*****

####  navarra  
##### 653#       发表于 2022-1-13 07:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54268870&amp;ptid=2037739" target="_blank">alexwu 发表于 2022-1-13 07:28</a>

咦，他们不是一直嘴硬ps2架构太特殊不是现在主流的cpu-显卡架构所以vulkan没啥提升一直拒绝加入么，这是 ...</blockquote>
是Duckstation的作者Stenzek塞进去的......实测cpu占用确实能降低

*****

####  路西恩  
##### 654#       发表于 2022-1-13 08:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54056010&amp;ptid=2037739" target="_blank">Xenor 发表于 2021-12-26 22:42</a>
高贵的ios用户用零头钱就能买个845以上的安卓机了吧…</blockquote>
天玑一千加都能模拟
这已经是过气手机了啊

—— 来自 [S1Fun](https://s1fun.koalcat.com)

*****

####  ChrisSnake  
##### 655#       发表于 2022-1-13 09:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54258417&amp;ptid=2037739" target="_blank">谷恒条野 发表于 2022-1-12 12:49</a>

可以啊，636L发的就是北妹2怎么设置的。</blockquote>
感谢

*****

####  PYY  
##### 656#       发表于 2022-1-13 11:17

就北妹2来说，
Vulkan比OpenGL快很多很多，
可是图像错误也成正比的多很多。。。

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  Suzutsuki.Mk.II  
##### 657#       发表于 2022-1-13 14:26

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54268870&amp;ptid=2037739" target="_blank">alexwu 发表于 2022-1-13 07:28</a>

咦，他们不是一直嘴硬ps2架构太特殊不是现在主流的cpu-显卡架构所以vulkan没啥提升一直拒绝加入么，这是 ...</blockquote>
他们有些开发者嘴巴死硬，还特别troll，不是开发组以外的人搞只会在那摆烂

现在除了vulkan拜鸭站作者所赐上了外，还有人要做基于qt的新UI

*****

####  Suzutsuki.Mk.II  
##### 658#       发表于 2022-1-13 14:27

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54268790&amp;ptid=2037739" target="_blank">navarra 发表于 2022-1-13 06:21</a>

顺便一提，pc版pcsx2最新开发版终于加入了vulkan渲染的支持……

—— 来自 samsung SM-G9880, Android 11 ...</blockquote>
不是最新，1月初（3号前）的推流版本就支持了

*****

####  stevenzero  
##### 659#       发表于 2022-1-13 14:49

ZOE2特别版，edge s，即时演算动画卡成狗，战斗敌机多一点也略卡，设定只改成vulkan其它没动。有什么配置可以优化的吗？

手柄用的PG9055，按键没问题。就是edge s太长卡不进去<img src="https://static.saraba1st.com/image/smiley/face2017/003.png" referrerpolicy="no-referrer">

*****

####  navarra  
##### 660#       发表于 2022-1-13 14:58

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54273279&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2022-1-13 14:26</a>

他们有些开发者嘴巴死硬，还特别troll，不是开发组以外的人搞只会在那摆烂

现在除了vulkan拜鸭站作者所赐 ...</blockquote>
五个字，早干啥去了......



*****

####  gaofar  
##### 661#       发表于 2022-1-13 14:59

搭车问一下   用安卓平板能运行这个模拟器吗？支不支持手柄操作？ 手机太小了  玩着费眼睛

*****

####  navarra  
##### 662#       发表于 2022-1-13 15:12

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54273647&amp;ptid=2037739" target="_blank">gaofar 发表于 2022-1-13 14:59</a>

搭车问一下   用安卓平板能运行这个模拟器吗？支不支持手柄操作？ 手机太小了  玩着费眼睛 ...</blockquote>
支持，我三星tab s7+和华为m6都能用

*****

####  stevenzero  
##### 663#       发表于 2022-1-13 16:00

看贴吧有人说870用720版本效果最好。好像是这么样，zoe2之前用720时战斗中没卡过，用1021同样场景就小卡。第一场boss战前打小兵。

*****

####  alexwu  
##### 664#       发表于 2022-1-13 21:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54268887&amp;ptid=2037739" target="_blank">navarra 发表于 2022-1-13 07:37</a>

是Duckstation的作者Stenzek塞进去的......实测cpu占用确实能降低</blockquote>
回来测试了几个稍微小众点的游戏，没解决的问题还是没解决外加vulkan的一堆画面错误，行吧，本来也没啥期待……不过支持了新的图形库终归是好事

*****

####  obelisk  
##### 665#       发表于 2022-1-14 10:54

<img src="https://static.saraba1st.com/image/smiley/face2017/074.png" referrerpolicy="no-referrer">买了个北通G3试了TODR 手感还不错 携带也挺方便 对了 机型是K30i

*****

####  astkaasa  
##### 666#       发表于 2022-1-16 23:01

 本帖最后由 astkaasa 于 2022-1-16 23:07 编辑 

看了下北妹2得用金手指, lost forest显示才不会错误

这个金手指好强, 速度都有大幅的提升, 开4x分辨率都可以了

<img alt="" border="0" class="vm" src="https://static.saraba1st.com/image/filetype/unknown.gif" referrerpolicy="no-referrer">

CC96CE93.pnach

2022-1-16 23:00 上传
点击文件名下载附件

6.33 KB, 下载次数: 17

*****

####  谷恒条野  
##### 667#         楼主| 发表于 2022-1-20 00:13

play-alpha-1059：
* Bug fixes for Mali GPUs in both Vulkan and OpenGL renderers (tested with Pixel 6).
* Texture preloading performance improvements.
* Add memory card creation/settings/per-game overrides.
* Disable texture barriers by default on Adreno (too many broken drivers).
* Prevent Vulkan being used on old drivers which are missing required formats.
* Minor optimization to VU dispatch (~10% improvement in Ratchet).
* Fix error reporting when loading incompatible save state.
* Add save state manager.

顺带一提，毒瘤狗萌账号被百度封了，棺材板可得压实点别又给放出来了。
好死。<img src="https://static.saraba1st.com/image/smiley/face2017/067.png" referrerpolicy="no-referrer">

*****

####  Xenor  
##### 668#       发表于 2022-1-20 01:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54269012&amp;ptid=2037739" target="_blank">路西恩 发表于 2022-1-13 08:09</a>

天玑一千加都能模拟

这已经是过气手机了啊</blockquote>
手持超过气手机一边清理空间，一边等正式版<img src="https://static.saraba1st.com/image/smiley/face2017/068.png" referrerpolicy="no-referrer">才清出2g出头太难了…

*****

####  yujie  
##### 669#       发表于 2022-1-20 03:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54268790&amp;ptid=2037739" target="_blank">navarra 发表于 2022-1-13 06:21</a>
顺便一提，pc版pcsx2最新开发版终于加入了vulkan渲染的支持……

—— 来自 samsung SM-G9880, Android 11 ...</blockquote>
借问下开发版有新的音频插件吗？

*****

####  PYY  
##### 670#       发表于 2022-1-20 15:23

1059好奇怪，搞不懂哪个设置变了，
北妹2，
Opengl速度大幅上升，
Vulkan速度大幅下降。
重置了最佳，快速两个设置都这样。
官网哪个地址是各个游戏推荐配置的？

[  -- 来自 能手机投票的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  谷恒条野  
##### 671#         楼主| 发表于 2022-1-23 20:03

Play alpha-1087:
* Implement vibration.
* Support Vulkan rendering without D32S8. Plenty of games will be broken and/or slow.
* Fix texture barriers still being used in some cases when disabled.
* Fix combined atest+blending (NFS Underground on Mali+Vulkan).
* Fix VU divide clobbering regs/constants (Cold Winter, Tekken 4), recompile RSQRT.
* Fix sign extension in VU double branches (Harvest Moon: STH).
* Fix FPU MUL fix (Tales of Destiny).

手柄支持震动了，修复了宿命传说的问题。

*****

####  neoaska  
##### 672#       发表于 2022-1-24 07:43

请问一下，ps4原装手柄蓝牙接红米手机，延迟得没法用，有解决方案吗？搜了搜就贴吧有人提过一个叫ds4 lag repair的软件，貌似也找不到

*****

####  PYY  
##### 673#       发表于 2022-1-24 08:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54407818&amp;ptid=2037739" target="_blank">neoaska 发表于 2022-01-24 07:43:28</a>
请问一下，ps4原装手柄蓝牙接红米手机，延迟得没法用，有解决方案吗？搜了搜就贴吧有人提过一个叫ds4 lag r ...</blockquote>不是红米手机的问题，
从PS4手柄第一天出来，就有这个问题了，
用索尼自己的手机连PS4手柄就完全没问题，
据说是用了和游戏一样的蓝牙协议，
其实手机只要没有用那个蓝牙协议的，就有很重的延迟，大概差不多有1到2秒左右。

[  -- 来自 能搜索的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  feizong  
##### 674#       发表于 2022-1-24 08:39

<blockquote>neoaska 发表于 2022-1-24 07:43
请问一下，ps4原装手柄蓝牙接红米手机，延迟得没法用，有解决方案吗？搜了搜就贴吧有人提过一个叫ds4 lag r ...</blockquote>
这个软件有用，我的米板装了就没延迟了

*****

####  cym887  
##### 675#       发表于 2022-1-24 08:43

<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">前几天更新新版后，ones手柄lt rt不识别就很操蛋 老版本无问题

最新版不知解决没

*****

####  谷恒条野  
##### 676#         楼主| 发表于 2022-1-24 11:48

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54407818&amp;ptid=2037739" target="_blank">neoaska 发表于 2022-1-24 07:43</a>

请问一下，ps4原装手柄蓝牙接红米手机，延迟得没法用，有解决方案吗？搜了搜就贴吧有人提过一个叫ds4 lag r ...</blockquote>
[https://pan.baidu.com/share/init?surl=pH0QuF6U7vuCENFXjBYkQw](https://pan.baidu.com/share/init?surl=pH0QuF6U7vuCENFXjBYkQw)

提取码：jstp

应该是这个吧。

*****

####  xman123601  
##### 677#       发表于 2022-1-24 13:15

顺便搭车问下 现在最好的pc上的ps2模拟器是那个

﹍﹍﹍

评分

 参与人数 1战斗力 +1

|昵称|战斗力|理由|
|----|---|---|
| PIN| + 1|PCSX2. 推荐下载最新的1.7开发版|

查看全部评分

*****

####  谷恒条野  
##### 678#         楼主| 发表于 2022-1-29 19:39

 本帖最后由 谷恒条野 于 2022-1-30 12:15 编辑 

Play alpha-1106:
* Add experimental hash based texture cache (Texture Preloading -&gt; Full).
* Fix vibration with more than one motor (Android 12+).
* Support binding a single virtual controller.
* Default automatic binding to Z/RZ instead of RX/XY.
* Fix ESADD instruction corrupting pending P (MK: Shaolin Monks).
* Rewrite/fix VU ESUM instruction (Mega Man X7 shadows).
* Add vibration frequency throttle option.
* Fix deleting &gt;1 slot in save state manager.
* Auto-disable full hash cache when it exceeds 1GB usage.

体感1106比1087卡和耗电

*****

####  慕容断月  
##### 679#       发表于 2022-1-30 03:21

借楼吐槽，1.7版pcsx2，取消插件之前火爆狂飙复仇还能在1066+6代i7上4K60帧稳定，结果现在最新版居然只剩下不到30帧，无法理解

*****

####  bonnwang  
##### 680#       发表于 2022-1-30 23:21

菊花10.8 990
试了一下皇牌空战50
0选机体只有30帧，进场卡成翔
5比0更卡<img src="https://static.saraba1st.com/image/smiley/face2017/065.png" referrerpolicy="no-referrer">

*****

####  83913536  
##### 681#       发表于 2022-2-19 23:41

奥丁掌机试了几款，战神1和2还是有点卡，45-55帧左右，2D的大多数挺完美的

*****

####  彩虹肥宅  
##### 682#       发表于 2022-2-19 23:57

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54758721&amp;ptid=2037739" target="_blank">83913536 发表于 2022-2-19 23:41</a>

奥丁掌机试了几款，战神1和2还是有点卡，45-55帧左右，2D的大多数挺完美的</blockquote>
1应该可以调到2x满帧，2我调试的时候开场都是不能满帧的。

*****

####  Xenor  
##### 683#       发表于 2022-5-6 22:56

 本帖最后由 Xenor 于 2022-5-15 04:44 编辑 

手机坏了，还二连了……<img src="https://static.saraba1st.com/image/smiley/face2017/097.png" referrerpolicy="no-referrer">
指定了文件夹，为什么主页不能识别出游戏文件。都是ISO格式的。</blockquote>
@保科智子 

常见ISO.RAR读不出，ROM文件后缀是ISO就行，要不指定了游戏文件夹但没确定以及没给权限……或者刷新一下以及退了再进试试

可以考虑压成CHD格式，体积大多能减半，速度也不影响

*****

####  Xenor  
##### 684#       发表于 2022-5-6 22:57

半年过去了，正式版还是没有出实在忍不住装了最新版1660，用845跑了下发现非常完美，前面820测试卡的都是满帧全速，这模拟器666的简直让人不敢相信

<img src="https://img.saraba1st.com/forum/202205/06/224108cz3938mu38ee5iwv.jpg" referrerpolicy="no-referrer">

<strong>1.jpg</strong> (265.18 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

<img src="https://img.saraba1st.com/forum/202205/06/224109qel3ldlnw24wln6z.jpg" referrerpolicy="no-referrer">

<strong>2.jpg</strong> (199.22 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

<img src="https://img.saraba1st.com/forum/202205/06/224112icqnjjvasjxx2tal.jpg" referrerpolicy="no-referrer">

<strong>3.jpg</strong> (205.27 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

对比3ds，ps2的对话字体更粗更清晰

<img src="https://img.saraba1st.com/forum/202205/06/224117bgk055zb03utugz0.jpg" referrerpolicy="no-referrer">

<strong>3i.jpg</strong> (132.64 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

<img src="https://img.saraba1st.com/forum/202205/06/224117s3lghlq3b1qqqtlg.jpg" referrerpolicy="no-referrer">

<strong>4.jpg</strong> (247.03 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

<img src="https://img.saraba1st.com/forum/202205/06/224129eppwonh66apr6mar.jpg" referrerpolicy="no-referrer">

<strong>5.jpg</strong> (221.19 KB, 下载次数: )

下载附件

2022-5-6 22:41 上传

<img src="https://img.saraba1st.com/forum/202205/06/224707s8eafefmm3s0itmn.jpg" referrerpolicy="no-referrer">

<strong>6.jpg</strong> (329.97 KB, 下载次数: )

下载附件

2022-5-6 22:47 上传

*****

####  susan28  
##### 685#       发表于 2022-5-7 01:28

现在在哪能买到原装的ds4手柄啊？

—— 来自 OPPO PCLM10, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.0.4-play

*****

####  zoe2  
##### 686#       发表于 2022-5-7 15:50

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=54408074&amp;ptid=2037739" target="_blank">PYY 发表于 2022-1-24 08:37</a>

不是红米手机的问题，

从PS4手柄第一天出来，就有这个问题了，

用索尼自己的手机连PS4手柄就完全没问题，</blockquote>
是啊，挺坑的，没有驱动ps3手柄在安卓10用线直连都没法用，太操蛋了

*****

####  PYY  
##### 687#       发表于 2022-5-7 17:33

没在手机上用过ps3手柄。

我真正开始用安卓手机是2013年中兴的N5大屏手机，之前用的都是充话费送的不算，一开始我就用蓝三角加ps2手柄玩模拟器；

后来换的也是中兴的天机一代，结果高通810大翻车，用着生不如死，后来买了ps4，第一件事当然就是用手柄线连手机，然后就发现系统状态栏会提示插入了游戏手柄，但实际根本无法操作。平时玩模拟器还是用的蓝三角加ps2手柄；

再下一个手机就是高通821的小米mix一代，这次线连ps4手柄能直接使用了，没有延迟。但是蓝牙连接就有非常大的延迟，大概有接近一秒，当时的说法就是索尼手机无线连没有延迟，其余的手机没这个协议所以延迟大，我是相信这个说法的，因为我在苹果平板上ios13更新后，ps4手柄在苹果平板上玩了好多手柄支持的游戏；

然后再下一个手机就是现在的小米11u，之前蓝牙连接我根本就没想去试了，一直用的线连。
后来手机上这个ps2模拟器出了，这才发现不知哪次更新居然蓝牙连接也没有延迟了，PSP模拟器的啪嗒砰一代我都能全程fever。
然后还是这个ps2模拟器，说能支持手柄振动了，但我的ps4手柄却实现不了这个功能，到处找答案，结果说原生安卓系统10之后都支持了，只是国内手机厂商阉割了手柄驱动导致没有振动。
几个月前的小米13大更新后，一天在玩ps2模拟器，突然发现振动选项那里居然亮了可以设置了，然后进能振动的游戏一看，果然可以振动了。
现在就是不知道ps4手柄的六轴旋转手机系统支持不，因为不知道哪个游戏支持没法测试。

[  -- 来自 有消息提醒的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  JudgmentEye  
##### 688#       发表于 2022-5-7 19:30

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=55721774&amp;ptid=2037739" target="_blank">susan28 发表于 2022-5-7 01:28</a>

现在在哪能买到原装的ds4手柄啊？

—— 来自 OPPO PCLM10, Android 10上的 S1Next-鹅版 v2.0.4-play ...</blockquote>
二手东国行

*****

####  保科智子  
##### 689#       发表于 2022-5-14 19:05

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=55720933&amp;ptid=2037739" target="_blank">Xenor 发表于 2022-5-6 22:57</a>

半年过去了，正式版还是没有出实在忍不住装了最新版1660，用845跑了下发现非常完美，前面820测试卡的都是满 ...</blockquote>
指定了文件夹，为什么主页不能识别出游戏文件。都是ISO格式的。<img src="https://static.saraba1st.com/image/smiley/face2017/001.png" referrerpolicy="no-referrer">

*****

####  唯美924  
##### 690#       发表于 2022-5-14 21:48

<img src="https://static.saraba1st.com/image/smiley/face2017/112.png" referrerpolicy="no-referrer">有没有人告诉我现在覆盖最广的下哪个版本，Google商店的版本就行吗



*****

####  okey3m  
##### 691#       发表于 2022-5-14 22:44

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=55842440&amp;ptid=2037739" target="_blank">唯美924 发表于 2022-5-14 21:48</a>
有没有人告诉我现在覆盖最广的下哪个版本，Google商店的版本就行吗</blockquote>
https://www.aethersx2.com/archive/
追求稳定就下最新beta版

*****

####  黑糖  
##### 692#       发表于 2022-5-15 08:21

试了下还不错

*****

####  007.5  
##### 693#       发表于 2022-5-19 09:38

最近借着影之心2汉化出了弄了个aethersx2来玩，官网下的1660版本，比我破电脑用模拟器爽多了
通了格兰蒂亚3弥补了当年记忆卡遗失导致烂尾的遗憾，现在想补另一个遗憾星之海洋3
但查到星海3有个地方吹笛子必须区分按键力度，求问aethersx2能通过设置处理么？网上查了一圈貌似都不行，自己有个不知道牌子的仿ps4手柄，倒是能通过蓝牙连接手机，玩aethersx2没问题，还有个ps4手柄但没试过

—— 来自 HUAWEI ELS-AN00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  桧山修之  
##### 694#       发表于 2022-5-19 11:37

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=55903802&amp;ptid=2037739" target="_blank">007.5 发表于 2022-5-19 09:38</a>

最近借着影之心2汉化出了弄了个aethersx2来玩，官网下的1660版本，比我破电脑用模拟器爽多了

通了格兰蒂亚3 ...</blockquote>
我也在玩星海3，龙角笛那只能在电脑那里过了再存回手机，存档是通用的，

*****

####  JudgmentEye  
##### 695#       发表于 2022-5-19 12:36

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=55903802&amp;ptid=2037739" target="_blank">007.5 发表于 2022-5-19 09:38</a>

最近借着影之心2汉化出了弄了个aethersx2来玩，官网下的1660版本，比我破电脑用模拟器爽多了

通了格兰蒂亚3 ...</blockquote>
存档通用，拿pc过这一段吧，pc版pcsx2用ds3可以支持按键压力感应，mgs2没问题，别的手柄我没试过

*****

####  PYY  
##### 696#       发表于 2022-5-19 15:44

ps2哪些游戏有用到按键压感的？
我熟悉的就想得出来，
皇牌空战的地图，这个只有几阶，
gt赛车的油门和刹车，这个阶数就好多好多了。

[  -- 来自 能看大图的 Stage1官方 Android客户端](https://www.coolapk.com/apk/140634)

*****

####  JudgmentEye  
##### 697#       发表于 2022-5-19 16:13

 本帖最后由 JudgmentEye 于 2022-5-19 16:16 编辑 

mgs系列，轻按是举起武器，使劲按是开火，慢慢放开是收起武器

zoe2，根据按键力度决定武器效果

gta3也有

*****

####  超赛锡纸烫  
##### 698#       发表于 2022-5-19 18:31

<blockquote>引用第695楼PYY于2022-05-19 15:44发表的  :

ps2哪些游戏有用到按键压感的？我熟悉的就想得出来，皇牌空战的地图，这个只有几阶，gt赛车的油门和刹......</blockquote>
保镖，星海传说3，某个音游，不过前两个都只有少少几阶，不过那个音游就有计量表了

----发送自 [STAGE1 App for Android.](http://stage1.5j4m.com/?1.37)

*****

####  007.5  
##### 699#       发表于 2022-5-20 20:06

星海传说3用硬件渲染开菜单就变得很卡，切换成软件渲染就正常，但软件渲染平时表现又很差

请问硬件渲染菜单卡顿这个有设置解决么？

—— 来自 HUAWEI ELS-AN00, Android 10上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  报应啊报应  
##### 700#       发表于 2022-8-23 01:38

最近发现更新到2632了，但是ea的游戏还是模拟不好orz极品飞车9还是有点卡

—— 来自 Xiaomi M2007J3SC, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  平井姨夫  
##### 701#       发表于 2022-9-4 14:49

奥丁掌机没法震动，到底怎么设置啊？

*****

####  samchen007  
##### 702#       发表于 2022-9-4 17:40

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57335896&amp;ptid=2037739" target="_blank">平井姨夫 发表于 2022-9-4 14:49</a>

奥丁掌机没法震动，到底怎么设置啊？</blockquote>
奥丁那个震动，还是关了吧，体验太差了。

*****

####  家里蹲废柴  
##### 703#       发表于 2022-9-26 15:09

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57335896&amp;ptid=2037739" target="_blank">平井姨夫 发表于 2022-9-4 14:49</a>

奥丁掌机没法震动，到底怎么设置啊？</blockquote>
同问

*****

####  家里蹲废柴  
##### 704#       发表于 2022-9-26 15:10

现在奥丁掌机下通用版还是高通专用版好

*****

####  bonnwang  
##### 705#       发表于 2022-9-27 13:24

用6g 64g麒麟990 mp10.8
玩bws会出现内存不足的问题
然后模拟器重启

也有可能是预留的空间不够了<img src="https://static.saraba1st.com/image/smiley/face2017/004.gif" referrerpolicy="no-referrer">

*****

####  Suzutsuki.Mk.II  
##### 706#       发表于 2022-9-27 13:38

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57178921&amp;ptid=2037739" target="_blank">报应啊报应 发表于 2022-8-23 01:38</a>

最近发现更新到2632了，但是ea的游戏还是模拟不好orz极品飞车9还是有点卡

—— 来自 Xiaomi M2007J3SC, An ...</blockquote>
极品飞车为啥要玩ps2版啊，不是有ngc版么？模拟效果比ps2版好

*****

####  报应啊报应  
##### 707#       发表于 2022-9-27 15:25

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57670105&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2022-9-27 13:38</a>
极品飞车为啥要玩ps2版啊，不是有ngc版么？模拟效果比ps2版好</blockquote>
在我865的手机上，ngc版也卡得不能玩

—— 来自 Xiaomi M2007J3SC, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  Suzutsuki.Mk.II  
##### 708#       发表于 2022-9-27 15:33

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57671535&amp;ptid=2037739" target="_blank">报应啊报应 发表于 2022-9-27 15:25</a>

在我865的手机上，ngc版也卡得不能玩

—— 来自 Xiaomi M2007J3SC, Android 12上的 S1Next-鹅版 v2.5.4 ...</blockquote>
我也是865，为啥我的还行？

*****

####  nukejoker  
##### 709#       发表于 2022-9-27 15:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57657100&amp;ptid=2037739" target="_blank">家里蹲废柴 发表于 2022-9-26 15:10</a>

现在奥丁掌机下通用版还是高通专用版好</blockquote>
同问。845还是太弱了。

开了性能模式，像零刺青这种还是只能跑80%。

*****

####  allenz3  
##### 710#       发表于 2022-9-27 15:39

高通版都多久不更新了，现在光是非整数分辨率这项就比老版本强

*****

####  violettor  
##### 711#       发表于 2022-9-28 16:21

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57671655&amp;ptid=2037739" target="_blank">nukejoker 发表于 2022-9-27 15:34</a>
 同问。845还是太弱了。 开了性能模式，像零刺青这种还是只能跑80%。</blockquote>
不会吧，我之前还看到一个用rp2+打通零的贴来着

*****

####  报应啊报应  
##### 712#       发表于 2022-9-28 16:22

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57671642&amp;ptid=2037739" target="_blank">Suzutsuki.Mk.II 发表于 2022-9-27 15:33</a>
我也是865，为啥我的还行？</blockquote>
我用海豚试过，明显是拖慢状态……

—— 来自 Xiaomi M2007J3SC, Android 12上的 [S1Next-鹅版](https://github.com/ykrank/S1-Next/releases) v2.5.4

*****

####  nukejoker  
##### 713#       发表于 2022-9-29 13:34

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57685104&amp;ptid=2037739" target="_blank">violettor 发表于 2022-9-28 16:21</a>

不会吧，我之前还看到一个用rp2+打通零的贴来着</blockquote>
RP2+  还是RP3？串流的吧？

RP2+不是连机战都会跑不满帧么？

*****

####  violettor  
##### 714#       发表于 2022-9-29 14:24

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57695801&amp;ptid=2037739" target="_blank">nukejoker 发表于 2022-9-29 13:34</a>

RP2+  还是RP3？串流的吧？

RP2+不是连机战都会跑不满帧么？</blockquote>
RP2+，0.75倍分辨率24帧。换算下来，感觉845应该是可以2倍分辨率的吧，你试试用vulkan？

*****

####  nukejoker  
##### 715#       发表于 2022-9-29 14:51

<blockquote><a href="httphttps://bbs.saraba1st.com/2b/forum.php?mod=redirect&amp;goto=findpost&amp;pid=57696355&amp;ptid=2037739" target="_blank">violettor 发表于 2022-9-29 14:24</a>

RP2+，0.75倍分辨率24帧。换算下来，感觉845应该是可以2倍分辨率的吧，你试试用vulkan？ ...</blockquote>
能折腾的都折腾过了。

而且刺青的问题是帧数浮动过大，这个场景能有24帧，换个视角说不定就15帧了。

可能是因为刺青的空间更大又或是优化问题吧。奥丁和手上的1加7pro用以太跑零刺青的体验很不行。Zero和红蝶倒还算稳定。目前所有手持设备里表现综合最好的居然是GPD Win2，因为win2的马达做的最好，win3和奥丁就只有傻震了。

但是win2风扇音起飞，win3能压得住风扇但是震感一塌糊涂，奥丁最轻手感最好但是帧数风扇都是败笔。

