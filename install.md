Laravel 安装指南
=====

### Composer 介绍
很多童鞋很奇怪，为什么要讲 Composer ？

恩，因为我们这里介绍的是 Laravel4，早在 Laravel3 的时候还是不用的 Composer 的。那么 Composer 是神马呢？简单的说 Composer 就是一个 PHP 的组件包的依赖管理器。早年间 PHP 其实是有自己的包管理器的，叫 PEAR。PEAR 就介绍到这里，你只要知道这是一个狗屎一般的管理器就行了。在 Node 的 npm 和 Ruby 的 bundler 都如火如荼的时候，连 Python 都有了好基友 easy_iinstall 和 pip，PHP也坐不住了，几个非官方的小伙伴一咬牙一跺脚，于是就有了 Composer。Composer 已经得到越来越多的 PHP 框架支持，基本就是你的 PHP 框架如果不支持 Composer，你都不好意思和同行打招呼。

Composer解决的问题是：

1. 你有一个依赖N多库的项目。
2. 这些库中一些又依赖于其他的库。
3. 你声明你所依赖的库。
4. Composer找出哪些包的哪个版本将会被安装，然后安装它们（也就是把它们下载到你的项目中）。

下面就是小白使用流程，更多关于 Composer 的内容，请到 [Composer官网] [3]

首先是安装，这里只介绍 Ubuntu 和 Windows 的安装，其他你们应该可以推理出来吧？

#### Ubuntu Composer 安装
1、切换到安装文件夹（建议安装在 /usr/local/bin 文件夹）
```terminal
cd /usr/local/bin
```

2、下载并执行 Installer，要注意的是，如果沒有在 php 前面加上 sudo 的话，有可能出现错误信息。
```terminal
sudo curl -s https://getcomposer.org/installer | sudo php
```

3、更改文件权限：上面的命令完成后，会下载好一个名为 composer.phar 的文件，而这个文件就是 Composer 的本体了，不过要更改一下它的权限。
```terminal
sudo chmod a+x composer.phar
```

4、更新：完成上面的步骤后，Composer 就装好了，过一段时间 Composer 自身升级版本，执行下面的命令就行（一般在你更新包的时候如果 Composer 有新版本，会提醒你需要升级）。
```terminal
sudo composer self-update
```

#### Windowns Composer 安装
1、下载 Windowns 下的 Composer 安装包：[官网下载页面] [4] 或者点击 [下载安装文件] [5]，进行安装。  
2、然后，就没然后了，你已经装好了。Composer 自身需要升级版本的时候你只需要在命令行（运行：cmd）输入
```terminal
composer self-update
```
Composer 装好后，我们就开始装 Laravel 吧！





[返回目录] [1]



[1]: https://github.com/maliang/LikeLaravel "返回目录"
[3]: http://getcomposer.org/ "Composer官网"
[4]: http://getcomposer.org/download/ "官网下载页面"
[5]: http://getcomposer.org/Composer-Setup.exe "下载安装文件"
