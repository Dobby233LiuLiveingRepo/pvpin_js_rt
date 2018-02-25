# [![封面](https://dn-coding-net-production-static.qbox.me/3113aa7b-291d-402e-819e-bebbf07e5ef3.png)](http://pvpin.com/) <br />__用拼积木的方式开发Minecraft插件__

 


 Develop Minecraft plugins by building blocks ~~in Blockly~~ like play.
 
 
 
 
### <big>介绍</big> <small>introduce</small>
 ### Pay attention 
 The English's in this Readme are not so well, because this is translated by AIs. So, if you have any issue at that, I hope you can forgive me, and if you can, please help me to improvement translate so I’d like to thank you. Please [mail me at i@timewk.cn](i@timewk.cn) about that.
 <br />
 
#### <big>这是什么？</big> <small>What's this?</small>
<big>这是<i>[PVPIN](http://pvpin.com/)</i>，一个基于JavaScript实现编写JAVA语言用于“我的世界”/“Minecraft”中的插件的一个网站，中的运行环境时，也就是前端的源代码。</big> 

<br />This is *"PVPIN"*,one Bukkit plugin wroter based on JavaScript implementation of JAVA 
This is that RunTime's front-end source.
<br />

~~forgive me please but narshon and scriptcraft are the real frontend~~
<br/>

#### <big>为什么可以使用JavaScript开发Java版的Minecraft插件？</big> 
#### <small>Why we can use JavaScript to develop java version of the Minecraft plugins</small>

因为java运行环境中有一个JavaScript引擎工程，可以运行JavaScript代码。更重要的是，可以直接在javascript中调用java代码。这样，我们就可以用javascript来写“Java”程序。

<br>Because the Java had a Javascript engine project, so you can run the JavaScript code. More importantly, you can directly call the Java code in JavaScript. In this way, we can use JavaScript to write "Java" program.

<br>![结构](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_0.jpeg)

<br>这样做有以下几个好处：
<br>* 更简单，JavaScript是一门比Java更简单的语言。学习更快，编写相同的功能，花费的时间也更短；
<br>* javascript本身是一门性价比高的语言，值得一学。性＝用途广泛性（跨前后端与各种平台），价 ＝学习的代价（耗费时间与难易程度）
<br>

<br>This has the following benefits:
<br>* JavaScript is a more simple language than JAVA. Learn faster, write the same function, and take less time;
<br>* dynamic, as a dynamic language, JavaScript can be modified and deployed in the server running code.
<br>* JavaScript itself is a cost-effective language, it is worth learning. cost = use wide (across the front end and various platforms), price = the cost of learning (time and difficulty)

#### <big>如何使用它?</big> <small>How to use it?</small>
##### Pay attention 
The next part will not provide English text as the PVPIN has only for Chinese's. If you I'd like to use it, consult the webmaster:

* QQ: 4740281 (Gang Ma)
* Mail: gangma@foxmail.com (Gang Ma)

在此之前，你需要拥有一个PVPIN账号来编写插件，详细的规则请查看PVPIN内的相关帮助。+

一、获取服务端包。
		这里有一个简单的整合包：[https://pan.baidu.com/s/1dENjTyL](https://pan.baidu.com/s/1dENjTyL)  。
		
下载后解压：
 ![解压](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_1.png)

我们简要的解释一下压缩包里的这几个目录

* plugins 目录：这里就是放插件的地方。这里已经放了一个NPC插件 citizens-2.0.21-SNAPSHOT，*PVPIN*的NPC功能直接调用了这个插件。
* server.properties ：这是服务器的配置文件。你可以根据自己的需要修改，然后重启就可以生效。简要的说一下其中的几个配置：      
    * pvp=true：玩家之间是否可以对战。
    * difficulty=1：游戏难度，0是平和模式，1是容易，2是正常，3是困难。
    * gamemode=0：游戏模式，0生存，1创造，2冒险。
    * motd=A Minecraft Server：motd是每日消息（Message Of The Day）的英文缩写，就是玩家在服务器列表上看到的消息。
* start.bat  ：这是启动服务的脚本。

双击启动脚本start.bat(前提是你已经安装好了java8)，就可以看到启动消息了。
 ![消息](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_2.png)

同时会发现目录下又多了几个文件，其中最重要的就是 world目录。

* world 目录：这样的目录有好几个，都是用world开头的，例如world，world_nether，world_the_end。这里就是存放游戏地图的目录。在游戏运行的时候，最好不要修改里面的文件，有可能会带来严重的错误。

#### 连入服务器
* 打开minecraft客户端，选择“多人模式”。
* 选择添加服务器
* 填入本地ip地址 127.0.0.1
* 然后就可以连入了
![连接1](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_2_1.png)
![连接2](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_2_2.png)

关于开服更详细的介绍请看czfy和aria的教程。 [http://bbs.pvpin.com/topic/217](http://bbs.pvpin.com/topic/217)

#### 如何下载和运行在*PVPIN*上开发的插件？
进入“我的作品”，在每一个作品下，有一个下载jar按钮。

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_3.png)

如果点击后看到了这样的界面：

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_4.png)

说明你的程序里用到了“我”这块积木，或者使用了没有指定出生位置的“建筑精灵”。到导出的代码请不要包含这两块积木，因为在服务器里不知道谁是“我”，而没有指定出生位置的“建筑精灵”，实际上也是取了“我”的位置，所以一样不能使用。

在正常情况下，你会看到这样的界面

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_5.png)

这时你有两个选择，下载jar包或者只下载js文件。如果你是第一下载请下载jar包。因为这里包含了pvpin的js运行环境。
将你下载好的插件放进plugins目录下。

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_6.png)

然后关闭服务器窗口，重新启动。看到PVPIN OK. 说明插件加载成功。

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_7.png)

这时候再看服务器目录，会发现多了一个PVPIN目录，这里包括了pvpin的js运行环境和你自己写的插件

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_8.png)

我们进入这个PVPIN目录，在 plugins/player 下里面就是你开发的js插件。

![](https://raw.githubusercontent.com/PVPIN/pvpin_js_rt/master/images/jar_9.png)

#### 如果你要安装第二个插件，只需要下载插件的js文件，然后把js放进这个目录，然后重启服务器即可。不需要重新下载jar包，否则可能会覆盖。
##至此，本文已经结束，尽情使用吧！
##  提示：PVPIN的js运行环境会不时更新，请关注网站的更新通知。 
GPL v2 开源协议
<br>
<Br>This project uses GPL V2 open source protocol for production, please follow this agreement in the relevant operations!
<br> if it is for commercial use, please declare copyright at the relevant location!
<br>Copy right 2017 PVPIN.com
<br> thanks again for your reading!

		
