### **一、安装Cygwin终端**

 1. 在[cygwin官网](http://www.cygwin.com/)下载对应的cygwin软件

 2. 安装cygwin的时候，在选择安装软件的时候选择安装**lynx**，**wget**和**git**工具

 3. 安装目录即为模拟的linux系统的**根目录**， 即**'/'**目录

 4. 将apt-cyg拷贝到安装目录的**home/Administrator**下（Administrator为Windows用户名）

 5. 运行cygwin，由于cygwin默认没有apt-get的安装工具，所以要安装一个shell脚本作为软件安装工具：**apt-cyg**

    ```
    chmod +x apt-cyg
    cp apt-cyg /bin/
    ```

 6. 换源：

    ```
    apt-cyg update --mirror http://mirrors.163.com/cygwin
    apt-cyg update
    ```

    然后就可以像apt-get一样使用了，如：apt-cyg install wget

### **二、下载AOSP源码**

1. 由于被墙的原因，不能从google下载AOSP源码，所以使用国内edu的源：[清华下载aosp的guideline](https://lug.ustc.edu.cn/wiki/mirrors/help/aosp)
2. 根据清华镜像的help文档，下载AOSP源码，时间看网速

**注：下载过程中会报错，报错原因自行百度解决。**

### **三、使用sublime text看源码（可忽略，直接在cygwin上安装vim查看源码）**

1. 下载安装sublime软件
2. 安装Package Controller
3. 使用Package Controller安装Ctags插件
4. 在Preject -> Add folder to project中打开下载好的AOSP目录
5. 在左侧打开的AOSP文件夹右键->Ctags:Rebuild tags， 该操作会生成大概1.5g的.tags，请不要关闭电脑，可以关闭sublime
6. 然后打开sublime就可以愉快的查看AOSP源码了。

