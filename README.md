# iOSMixProject
马甲包混淆工程

# 原工程地址
首先感谢将此脚本初始脚本开源的大佬，但不太适合我们工程，于是我们在原有的轮子上加了几颗螺丝钉，仅供参考思路，奉上原仓库地址。
注意看这里！原始代码仓库地址：[https://github.com/klaus01/KLGenerateSpamCode](https://github.com/klaus01/KLGenerateSpamCode)

# 新增功能
除了已有的图片资源递增修改、修改工程名、类前缀修改(修改了遍历方案)外，还加了一些骚东西

1、混淆随机添加垃圾代码、参数

2、修改方法名前缀

3、修改方法名，使用plist文件创建原始方法名仓库，共有6^6个方法名可以配置，随机方法名配参数

4、删除垃圾代码。以脚本前缀为索引

5、混淆概率

#使用方法
和原来的轮子一样，先配置启动参数再运行，如图

![image_0](http://ok9lu0v73.bkt.clouddn.com/image.png)
参数解释：

1.工程代码的绝对路径

2.-modifyProjectName [原工程名]>[新工程名]

3.-modifyClassNamePrefix [xcodeproj文件的绝对路径，不是pod安装后的那个打开文件] [旧类前缀]>[新类前缀]

4.-spamCodeOut

5.-ignoreDirNames [需要忽略的文件夹],[需要忽略的文件夹]             注意，Pods文件夹不在混淆范围内，不需要写

6.-handleXcassets              (混淆图片文件)

7.-deleteComments             (删除多余的空格和注释)

8.-chageAPIPrefix [旧方法名前缀]>[新方法名前缀]              注意，前缀要有“_”才能被识别，如果之前工程中没有xx_下划线开头来命名方法的，此项不要勾选

***此工程可以选择混淆概率，修改工程中kPercent数值。***

# 详情
有关此工程的设计详情请看这篇文章[传送门](http://www.imyuyang.com/2018/02/15/iOS%E9%A9%AC%E7%94%B2%E5%8C%85%E6%B7%B7%E6%B7%86%E6%96%B9%E6%A1%88/)

# 实际测试

![image_1](http://ok9lu0v73.bkt.clouddn.com/i18%5Epimgpsh_fullsize_distr.png)

# 痛点
时间复杂度可以说是非常的高，跑起来运行时CPU占用率几乎达到百分百。好在这基本是一次性工具。。。

