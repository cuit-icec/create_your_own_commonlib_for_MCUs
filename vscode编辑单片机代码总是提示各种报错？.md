## 此篇文章默认你的vscode已经安装了c++插件

vscode编辑代码总是提示各种报错？

根本的问题就是两个

**includepath &**

**预定义宏**



以示例中我新建的通用库为例，

右键项目文件夹，以vscode打开

打开vscode的命令面板

![image-20210131224115411](http://tuchuang.hanbaoaaa.xyz/20210131224115.png)

输入c/c++

选择配置json

![image-20210131224204178](http://tuchuang.hanbaoaaa.xyz/20210131224204.png)

会看到新增了.vscode 目录。里面有一个c_cpp_properties.json

然后下面需要修改的就是这里面的includePath

![image-20210131225715384](http://tuchuang.hanbaoaaa.xyz/20210131225715.png)

我们去cubeide里看看有哪些include path

![image-20210131230003199](http://tuchuang.hanbaoaaa.xyz/20210131230003.png)

打开项目配置

![image-20210131230133674](http://tuchuang.hanbaoaaa.xyz/20210131230133.png)

这边这些就是我们要添加到vscode里的include path

复制到vscode中并修改成一致的格式

![image-20210131230433722](http://tuchuang.hanbaoaaa.xyz/20210131230433.png)

这个时候已经不报错了![image-20210131230547807](http://tuchuang.hanbaoaaa.xyz/20210131230547.png)

再去看看一些底层的文件，在下图中这个文件里uint32_t报错了。这个报错很常见

![image-20210131230744573](http://tuchuang.hanbaoaaa.xyz/20210131230744.png)

罪魁祸首就是这个

![image-20210131231134064](http://tuchuang.hanbaoaaa.xyz/20210131231134.png)

我们往配置中加入

![image-20210131231346096](http://tuchuang.hanbaoaaa.xyz/20210131231346.png)

报错只剩一点点了

![image-20210131231422207](http://tuchuang.hanbaoaaa.xyz/20210131231422.png)

回到我们的ide中，寻找一些和预定义相关的

我这边找到在这里

![image-20210131231534535](http://tuchuang.hanbaoaaa.xyz/20210131231534.png)

加入配置中

![image-20210131231625801](http://tuchuang.hanbaoaaa.xyz/20210131231625.png)

完成！可以顺畅的写代码了