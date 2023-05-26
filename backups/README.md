


---

<details>
<summary>🆘各种教程</summary>
<br>
<br />
<br>

《[github actions编译教程](https://github.com/danshui-git/shuoming#%E7%BC%96%E8%AF%91%E6%95%99%E7%A8%8B)》

《[Amlogic、Rockchip系列固件打包设置教程](https://github.com/danshui-git/shuoming/blob/master/Amlogic.md)》

《[在线更新固件插件说明](https://github.com/danshui-git/shuoming/blob/master/%E5%AE%9A%E6%97%B6%E6%9B%B4%E6%96%B0%E6%8F%92%E4%BB%B6.md)》

<br />
</details>

---

<details>
<summary>🆙更新说明（2023年5月13号）</summary>

<br>

2023年5月13号
 
 1、重新整理了所有源码的插件包，因技术有限，gl-ax1800源码增加不了docker，还有个别源码不能编译ssrplus和passwall的NaiveProxy，个别源码的vssr和istore可以编译成功，但是不能用，还有没有其他插件也存在此问题，等你们测试了
 
 2、gl-ax1800源码的固件不能直接进行转换成Xwrt的固件，安装的时候会出错，然后卡死了，如果你用的是gl-ax1800源码编译的固件要注意，想用Xwrt的固件的固件，就先随便把gl-ax1800源码编译的固件安装成其他任意作者的固件再安装Xwrt的固件
 
 3、把所有源码的主题插件都整理了一遍，因为有些主题太老了，支持不了好多现在新的插件，那些新插件名称在主题错位的还没啥，反正还能看到，能设置，很多主题直接是不显示该插件的存在，或者好多主题名字不一样，其实都是大同小异的主题，所以我那些主题干掉了。（18.06LUCI的主题比较好用的有 luci-theme-argon，luci-theme-design，luci-theme-opentopd，luci-theme-kucat，19.07之后的主题基本没几个可以选了，感谢这些主题作者的辛苦付出）
 
 4、不管源码里面有没有luci-theme-argon,我都替换成jerrykuku大佬的luci-theme-argon主题了
 
 5、自定义设置里面的（export Enable_IPV6_function="0"）、（export Enable_IPV4_function="0"）和（export Create_Ipv6_Lan="0"）只能三选一的开启，如果你都同时开启的话，只会选择启用（export Enable_IPV6_function="1"）
 
 6、每次安装固件完毕，就是跑完码后，该运行的运行，该咋滴咋滴，全部搞定后就会进行重启，跑完码后，如果你使用页面后台进入固件是可以的，但是进入后因为相隔几十秒后(全部东西运行完毕大概是20-30秒,东西多的话时间要增加一点点)会进行重启，所以有些人进入后，修改了东西，没保存设置，因为才几十秒，很快就过去了，来不及按保存，然后造成你以为你设置了东西，但是过一会发现又没设置的情况，因为你没按保存，固件就重启了，应该要等重启后再来慢慢设置，如果请大家发现这个问题的时候莫慌

---

2023年4月22号

1、把autobuild仓库合拼到了这里了，以前拉autobuild仓库的应该都不可以用了，请重新拉取这个仓库吧，以前老的build-actions仓库也要重新拉取新的build-actions仓库使用（请不要继续拉取autobuild仓库使用，这个是我个人使用仓库）
 
2、编译教程全修改一遍了，看教程还不能启动编译的话，我只能说多看几次吧

3、增加了编译源码的选择，同作者源码的源码分支之间可以自由切换编译（每个作者源码的可支持选择什么分支，在settings.ini文件有写明）

4、晶晨系列固件不限制一个源码，理论上可以编译出rootfs.tar.gz包的，应该都可以打包使用，比较常用的有（天灵的openwrt-21.02分支、大雕的master分支、官方的master分支），固件编译跟打包分2次进行，这样免除了打包空间不足，或者编译+打包时间不足的问题，已经编译出了的rootfs.tar.gz可以使用手动启动打包程序，进行多次打包操作。（更新了amlogic和rockchip固件打包设置教程）
 
5、luci-app-oscam插件，云编译，编译不成功，云编译的时候切莫选择此插件，本地编译倒是可以编译成功。
 
6、大雕源码，有些机型编译增加mac80211驱动的时候会编译错误的，如果出现这个情况，自己带上日志找源码作者处理
 
7、我编译仓库里，增加大雕源码【gl-ax1800】分支选择，不是他 https://github.com/coolsnowwolf/lede 源码的分支，是他另外一个仓库 https://github.com/coolsnowwolf/openwrt-gl-ax1800 的源码，看他意思是专门给gl-ax1800路由器准备的，我看了下，也测试了一下，其实就是一个4.14内核的源码，有需要这个内核的朋友，也可以使用这个分支编译

</details>

---

<details>
<summary>✴️本地编译</summary>
<br>
<br />
<br>

《[本地Ubuntu一键编译OpenWrt固件](https://github.com/281677160/bendi)》

《[本地一键提取.config然后在云编译脚本使用](https://github.com/281677160/bendi)》

<br />
</details>

---

<details>
<summary>🏠Telegram群</summary>
<br>
<br />
 
《[Telegram聊天吹水群](https://t.me/heiheiheio)》

《[Telegram中文设置方法](https://github.com/danshui-git/shuoming/blob/master/tele.md)》

</details>

---

 ### 鸣谢！
 感谢以下各位大佬（排名无分先后）<br />
 
 [`coolsnowwolf`](https://github.com/coolsnowwolf/lede/tree/master)
 [`Lienol`](https://github.com/Lienol/openwrt/tree/21.02)
 [`immortalwrt`](https://github.com/immortalwrt/immortalwrt)
 [`openwrt`](https://github.com/openwrt/openwrt)
 [`x-wrt`](https://github.com/x-wrt/x-wrt)
 [`P3TERX`](https://github.com/P3TERX/Actions-OpenWrt)
 [`Hyy2001X`](https://github.com/Hyy2001X/AutoBuild-Actions)
 [`dhxh`](https://github.com/dhxh/Openwrt-Build)
 [`ophub`](https://github.com/ophub/amlogic-s9xxx-openwrt)
 [`nicholas-opensource`](https://github.com/nicholas-opensource/OpenWrt-Autobuild)
 [`hx210`](#/README.md)
 [`hyird`](#/README.md)
 [`World Peace`](#/README.md)
 [`klever1988`](https://github.com/klever1988/cachewrtbuild)
 [`actions`](https://github.com/actions/upload-artifact)
 [`svenstaro`](https://github.com/svenstaro/upload-release-action)
 [`jerrykuku`](https://github.com/jerrykuku/luci-theme-argon)