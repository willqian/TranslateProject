保护密码的利器：Ubuntu 之 KeePassX
================================================================================
**随着安全性问题变得越来越重要，密码当然是越安全越理想（比如多步认证），这一点再强调也不为过。

![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/security-key.jpg)

既然这样想了，于是我最近就试用了几个安全密码管理器，试图找到一款比较可靠，易于使用并且跨平台的应用软件。

首先，我尝试了LastPass[1]。LastPass大概最为人们所熟知，基于网络管理密码，是所有软件中平台无关性最强的。但是我发现它的界面简陋，而且提供太多的工具和选项，比较繁琐。

接下来，我又试了试KeePass 2[2]。尽管是一款功能相当完善的应用软件，非常类似于下面我将要描述的，但是官方又不提供Linux上的安装包和公共接口，虽然可用，还算不上最好的。所以我又尝试了其他应用。

在所有的试用过的软件中，我最喜欢的是**KeePassX**. KeePassX起初是作为linux的一个分支，但是后来逐渐演变为属于自己的应用程序。凭借更漂亮、更为本地化的接口，KeePassX 打败了KeePass 2。
## 在ubuntu中使用KeePassX ##

方便的是，KeePassX已经提供在ubuntu上安装的软件包。

从命令行安装KeePassX或者**从软件管理中心安装**：
- [Install KeePassX from the Ubuntu Software Centre][3]

打开它，你会看到一个空白窗口。点击工具条上的按钮创建一个数据库。可以使用密钥文件或者密码保护刚刚创建的数据库。你很可能使用密码，因为只需要记住它并输入就行了 - 你可能会键入许多字符，但是另一方面，你不会让其他人进入你的数据库。

接下来，你得把它存到某个位置。我保存在我的Dropbox里面，这样就可以从多个地方获取。Dropbox使用双重认证，所以如果有人想进到我的Dropbox里面，他就得用到我的手机，这样的方式是还是相当安全的。

另外，你可以使用其他的服务，比如Google Drive和Skydrive，它们都使用标准认证器[4];再比如Box，使用SMS进行双重认证。

当然，如果**的的确确**担心自己的密码，你很可能不打算把密码存到其他的一些组织团体，因为理论上密码是可以被他们获取到的。
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-190130.png)

*Ubuntu中KeePassX的主界面*

使用该应用还是相当直接的。你可以添加分组，然后在分组里添加密码。KeePassX带有一个很方便的密码生成器，当你需要输入一个密码的时候可以使用该生成器，而不用自己构思一个。我倾向于使用所有基本的字符以及挑选的特殊的字符来生成密码，
20个字符的长度，当然这得看网站接不接受了。

需要注意一点，有些网站并不告诉你他们接受多长字符的密码，倾向于只在输入框限制输入长度。如果你粘贴进去的密码看起来没那么长，事实上可能不是那么一回事，也有可能是被截断了。这种情况我碰到过几次。
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-190025.png)

*KeePassX 密码生成器*

根据日常的使用经验，我积累了一些小的技巧，使得操作KeePassX更简单一些：

**疯狂地复制粘贴**

像这样复制粘贴密码，你可能会比较担心。可以肯定的是这比手动输入高效多了。默认情况下，KeePassX会在一分钟之内清空粘贴板，也可以设置更短的时间，所以不必担心有人会在你电脑上把密码粘贴下来查看。你也可以开启一个AutoType的特性，该特性会自动输入密码，不过出于某种原因，它会把密码紧跟着用户名输入到同一个地方，这样一来该特性似乎用处不大。

**数据库的困境**

如果你把数据库存放到云端，就不要为云端服务设置完全随机的密码。如果你不能进入到云，但是又把云密码存储到云里边，这是完全没有益处的。这看起来似乎很明显，但是刚开始我却没有意识到这一点。

**确保所有的密码都是安全的**

为了查看常用的账号，工作或者学习的时候要频繁地掏手机，这也是一件挺痛苦的事儿，所以设置密码的时候不妨想象一下这种情形，哈。

## 未来 ##

如果你以前也深入了解过KeePass 2和KeePassX，或许会注意到二者使用不同的数据库格式。

KeePass 2使用一种新的版本格式，比如允许自定义字段。尽管KeePassX目前还不支持新的.kdbx格式，正在开发中的新的版本会加上这一点。

可以预览一下新版本的KeePassX，界面大为改善。你也可以从GitHub上[6]下载后自己安装。
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-19_33_23.png)

*KeePassX 2.0 主界面*
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-19_34_14.png)

*密码项的一些细节*
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-19_34_44.png)

*密码项的附加属性*
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-19_35_18.png)

*历史登陆信息，比如从先前的版本替换掉"Backup"文件夹之类的*
![](http://www.omgubuntu.co.uk/wp-content/uploads/2013/10/Screenshot-from-2013-10-11-19_35_51.png)

*KeePassX 2.0 中的配置*

## 其他建议 ##

正如本文开头所说，**我在寻找能够跨平台的东西**。这正是.kdb格式的优点 - 很多应用都支持这种格式。KeePassX 在 Mac OS X上运行起来要比KeePass 2容易得多，在windows上也可以。

Android系统上，我使用KeePassDroid[6]，在我的手机和平板上运行都很稳定。
--------------------------------------------------------------------------------

via: http://www.omgubuntu.co.uk/2013/10/manage-passwords-securely-keepassx

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创翻译，[Linux中国](http://linux.cn/) 荣誉推出

译者：[l3b2w1](https://github.com/l3b2w1) 校对：[校对者ID](https://github.com/校对者ID)

[1]:https://lastpass.com/
[2]:http://keepass.info/index.html
[3]:http://apt.ubuntu.com/p/keepassx
[4]:https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en
[5]:https://github.com/keepassx/keepassx
[6]:https://play.google.com/store/apps/details?id=com.android.keepass&hl=en_GB
