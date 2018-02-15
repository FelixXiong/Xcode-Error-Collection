# libc++abi.dylib:

# terminating with uncaught exception of type NSException

报错位置：控制台

# 1.Terminating app due to uncaught exception ''

### **该情况的具体分支可以点击Terminating app due to uncaught exception ''页面查看。**

**情况说明：点按某个控件出现崩溃（crash）**

解决步骤：定位断点进行查看

参考链接：

cnblogs

[http://www.cnblogs.com/liuguanlei/p/4482327.html](http://www.cnblogs.com/liuguanlei/p/4482327.html)

> 在Xcode的菜单栏中选择Debug-&gt;Breakpoints-&gt;Create Symbolic Breakpoint点击后，会添加一个断点调试，弹出编辑框
>
> 在编辑框的Symbol中填写`-[NSObject(NSObject)doesNotRecognizeSelector:]`此方法签名，对于边看本博文边试验的同学来说，在复制方法签名后想粘贴的时候，发现Xcode中的编辑框不见了，此时右击刚才添加的那个断点，选择Edit Breakpoint即可。
>
> 运行代码，断点就会停留在导致崩溃的地方。



