# How to make .deb package from your source code #
## Continue behind the auto-tools ##
当你自己有一个源代码，可以利用auto-tools来进行方便的发布和管理。但是我相信，这些都是对于对linux的安装结构有一定了解的人才会知道这样的发布方式该如何安装在自己的电脑上面。对于跟加一般的用户，可能想要的是更加简单的安装方式，比如 **双击** 。
比如在ubuntu下面，就是需要制作deb包来进行发布。我至今用得最多的有两种方法，都是非常的方便的。
  1. 第一种就是已经延续了很久的方法，而且该方法会让你的程序显得更加的可控。具体的可以参见[如何制作deb包](http://www.webupd8.org/2010/01/how-to-create-deb-package-ubuntu-debian.html)。这个里面有非常详细的描述，而且对于依赖问题描述的非常的详细。我在我用这个方法制作的过程中，遇到了一些问题，但是都一一解决了。现在还有一个比较搞不懂的问题是，你写的一个软件需要一个比如叫做libtest.so的动态链接库，但是这个库是你自己编译的，这样用这个网页里面提到的方法是检查不到依赖关系的，最后他就会提示你，你的程序用到了一个库，但是这个库的依赖关系找不到。
  1. 另一个非常 **便民** 的方法就是今天我才发现的，用checkinstall这个工具，具体参见[Linux 的源码安装工具 Checkinstall](http://www.ibm.com/developerworks/cn/linux/l-cn-checkinstall/)。里面的举例是rpm包的，制作deb包更加的方便，参见[使用Checkinstall生成deb安装包](http://www.cnblogs.com/tigertnt/archive/2008/12/21/1359242.html)。但是一个问题是，我感觉这个方法生成的并不是很安全，第一没有第一种方法中需要的签名，第二并没有涉及到依赖关系的问题。

## 总而言之 ##
总的来说，在开发的初期，用第二种方法快速的发布是比较方便的。