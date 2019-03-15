# iconfontTest
>Created By **JishuBao** on **2019-03-06 12:38:22**  
>Recently revised in **2019-03-08 12:38:22**

&nbsp;

　　**欢迎大家来到技术宝的掘金世界,您的star是我写文章最大的动力！[GitHub地址](https://github.com/WJB3/iconfontTest.git)**
　　
&nbsp;

　　**开篇点题:**
　　<br />
　　这是一篇教您如何使用阿里iconfont矢量图标的教程，看完此文，包你拿下iconfont不必苦恼。
　　<br />
　  　感觉不错的小伙伴，点赞star走一波;
　  <br />
　  　感觉文章有误的小伙伴，评论区、[QQ群](http://qm.qq.com/cgi-bin/qm/qr?k=BhM60jsO8NjCWBAVkUKJmAcjTy6iJLyY)走一波；
　  <br />
　  　虚心求教，不胜感激~
　  　
　  　&nbsp;

文章简介：

1、什么是iconfont？

2、为什么要使用iconfont？

3、如何进入iconfont官网选图标？

4、在web端(html,vue,react)中使用在线iconfont？

5、在web端(html,vue,react)中使用本地iconfont？

# 一、什么是iconfont？
&emsp; 顾名思义iconfont就是把图标用字体的方式呈现。

# 二、为什么要使用iconfont？
其优点在于以下几个方面:

1.可以通过css的样式改变其颜色(最霸气的理由）

2.相对于图片来说,具有更高的分辨率

3.更小的存储

**缺点:浏览器兼容性不够普及,所幸目前大部分主流浏览器都支持**

# 三、如何进入iconfont官网选图标?
&emsp;进入[阿里iconfont官网](https://www.iconfont.cn/),注册并登陆,登陆好以后在首页点击**我的项目**,。
![](https://user-gold-cdn.xitu.io/2019/3/15/1697f2d4ac8818ff?w=1227&h=928&f=png&s=200346)

&emsp;点击**添加项目按钮**。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f2e024bbc746?w=1227&h=928&f=png&s=186158)
&emsp;这里我们点击添加项目，填写好项目相关信息以后点击新建新建测试iconfont的项目。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f2f69f99deb4?w=1227&h=928&f=png&s=163279)
&emsp;在这里点击搜索框即可获取海量图标。
![](https://user-gold-cdn.xitu.io/2019/3/15/1697f305016c79e1?w=1227&h=928&f=png&s=186066)
&emsp;比如我们点击搜索公司。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f315519248ef?w=1227&h=928&f=png&s=173897)
&emsp;就会出现很多图标。鼠标悬浮在上面会出现三个图标。点击第一个。
![](https://user-gold-cdn.xitu.io/2019/3/15/1697f32d2c779fdb?w=1227&h=928&f=png&s=175878)
&emsp;点击第一个就会出现这种情况。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f33a59743990?w=1227&h=928&f=png&s=177604)
&emsp;点击右上角。点击添加至项目将项目添加到刚刚新建的项目里面。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f344d2ee10a6?w=1227&h=928&f=png&s=141787)
&emsp;点击确定即可。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f3533c7c988f?w=1227&h=928&f=png&s=145674)
&emsp;点击在线链接出现链接。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f3754c039286?w=1227&h=928&f=png&s=184327)

**我们可以看到图标上有三个按钮！**

**接下来我们的示例demo都会使用选择的这三个图标(2个有色图标,一个无色图标)！**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f7a0726991b5?w=351&h=154&f=png&s=8655)


一.**unicode**是**字体在网页端最原始的应用方式**，特点是：

1.兼容性最好，支持ie6+，及所有现代浏览器。

2.支持按字体的方式去动态调整图标大小，颜色等等。

3.但是因为是字体，所以不支持多色。只能使用平台里单色的图标，就算项目里有多色图标也会自动去色。
&emsp;

二.**font-class**是**unicode使用方式的一种变种**，主要是**解决unicode书写不直观，语意不明确**的问题。

与unicode使用方式相比，具有如下特点：

1.兼容性良好，支持ie8+，及所有现代浏览器。

2.相比于unicode语意明确，书写更直观。可以很容易分辨这个icon是什么。

3.因为使用class来定义图标，所以当要替换图标时，只需要修改class里面的unicode引用。

不过因为本质上还是使用的字体，所以多色图标还是不支持的。

三.**symbol**这是一种全新的使用方式，**应该说这才是未来的主流，也是平台目前推荐的用法**。相关介绍可以参考这篇文章

这种用法其实是做了一个svg的集合，与上面两种相比具有如下特点：

1.支持多色图标了，不再受单色限制。

2.通过一些技巧，支持像字体那样，通过font-size,color来调整样式。

3.兼容性较差，支持 ie9+,及现代浏览器。

浏览器渲染svg的性能一般，还不如png。

# 四、在web端(html,vue,react)中使用在线iconfont？
**使用在线iconfont的前提是先在head标签里面引入样式文件，在Iconfont里面找到在线链接：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f489a92c1245?w=840&h=302&f=png&s=27147)

## 一、html中使用

**1.unicode使用方法：**


![](https://user-gold-cdn.xitu.io/2019/3/15/1697f7bf1aa04142?w=823&h=571&f=png&s=51294)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f7cae405cd13?w=417&h=387&f=png&s=8586)

**2.font-class使用方法：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f80fea940d4c?w=817&h=574&f=png&s=51135)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f81a5546426b?w=276&h=181&f=png&s=5301)

**3.symbol使用方法：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fb8b6af4bcd5?w=968&h=799&f=png&s=77336)
**效果:前面2个是有色图标后面一个是无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fb95247eaebf?w=333&h=94&f=png&s=10470)

## 二、vue中使用
**1.unicode使用方法:**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdef83d3d150?w=821&h=733&f=png&s=60421)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**2.font-class使用方法:**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fe1080945417?w=821&h=736&f=png&s=60942)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**3.symbol使用方法：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fe3b9d909435?w=974&h=873&f=png&s=78605)

**效果:前面2个是有色图标后面一个是无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fe44344362a4?w=364&h=95&f=png&s=11884)

## 三、react中使用
**1.unicode使用方法:**
![](https://user-gold-cdn.xitu.io/2019/3/15/1697fed88cc0bad9?w=926&h=720&f=png&s=67454)

**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**2.font-class使用方法:**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fef21a6b31c3?w=923&h=712&f=png&s=66957)

**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**3.symbol使用方法：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697ff40df929ef6?w=934&h=874&f=png&s=85697)
**效果:前面2个是有色图标后面一个是无色图标**


![](https://user-gold-cdn.xitu.io/2019/3/15/1697ff46623ad767?w=355&h=117&f=png&s=15573)

**在线使用iconfont虽然很省事,不需要下载很多文件配置啥的,但是有一个缺点,当iconfont挂了,诸如此类发生...图片加载很慢,导致用户浏览页面不友好等等,所以我们还是尽量少用在线，接下来教大家使用下载下来的图标文件使用**

# 五、在web端(html,vue,react)中使用本地iconfont？
&emsp;既然是使用本地的iconfont，本地肯定需要相应的iconfont文件,点击下载至本地，将文件下载解压到我们的文件夹下。

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fffc06ddead7?w=892&h=380&f=png&s=32289)
如下图。

![](https://user-gold-cdn.xitu.io/2019/3/15/1698000240803e2b?w=611&h=271&f=png&s=35528)

**下载下来的iconfont.css文件**

![](https://user-gold-cdn.xitu.io/2019/3/15/1698004bcbc71517?w=1381&h=644&f=png&s=79030)
## 一、html中使用
**1.unicode使用方法：**


![](https://user-gold-cdn.xitu.io/2019/3/15/16980074eb4d9312?w=799&h=573&f=png&s=49297)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f7cae405cd13?w=417&h=387&f=png&s=8586)

**2.font-class使用方法：**


![](https://user-gold-cdn.xitu.io/2019/3/15/1698008b6d11bc72?w=718&h=579&f=png&s=48137)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697f81a5546426b?w=276&h=181&f=png&s=5301)

**3.symbol使用方法：**


![](https://user-gold-cdn.xitu.io/2019/3/15/1698009a284a6139?w=734&h=799&f=png&s=67647)
**效果:前面2个是有色图标后面一个是无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fb95247eaebf?w=333&h=94&f=png&s=10470)

## 二、vue中使用
**1.unicode使用方法:**


![](https://user-gold-cdn.xitu.io/2019/3/15/169800bbfe88c337?w=716&h=738&f=png&s=57222)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**2.font-class使用方法:**


![](https://user-gold-cdn.xitu.io/2019/3/15/169800c50cad070a?w=710&h=732&f=png&s=57463)
**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**3.symbol使用方法：**


![](https://user-gold-cdn.xitu.io/2019/3/15/169800cfa4306492?w=726&h=876&f=png&s=71566)

**效果:前面2个是有色图标后面一个是无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fe44344362a4?w=364&h=95&f=png&s=11884)

## 三、react中使用
**1.unicode使用方法:**

![](https://user-gold-cdn.xitu.io/2019/3/15/169800e7b437a899?w=933&h=707&f=png&s=65639)

**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**2.font-class使用方法:**


![](https://user-gold-cdn.xitu.io/2019/3/15/169800fc91b1b2db?w=940&h=710&f=png&s=65636)

**效果:全部变成无色图标**

![](https://user-gold-cdn.xitu.io/2019/3/15/1697fdf944998ed8?w=315&h=68&f=png&s=5496)

**3.symbol使用方法：**

![](https://user-gold-cdn.xitu.io/2019/3/15/1698010a41d51a7f?w=921&h=894&f=png&s=85063)x
**效果:前面2个是有色图标后面一个是无色图标**


![](https://user-gold-cdn.xitu.io/2019/3/15/1697ff46623ad767?w=355&h=117&f=png&s=15573)

**是不是很简单呢,小伙伴们！**
**如果你觉得我的文章还不错的话，可以给个star哦~，[GitHub地址](https://github.com/WJB3/iconfontTest.git)**
