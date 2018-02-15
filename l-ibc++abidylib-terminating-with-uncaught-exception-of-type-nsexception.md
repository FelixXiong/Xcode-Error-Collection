# libc++abi.dylib:

# terminating with uncaught exception of type NSException

报错位置：控制台

## 1.this class is not key value coding-compliant for the key'

**情况说明：模拟器出现白屏**

解决步骤：检查是否有黄色的叹号的Outlets，进行删除。

Stackoverflow

[libc++abi.dylib: terminating with uncaught exception of type NSException \(lldb\)](https://stackoverflow.com/questions/26442414/libcabi-dylib-terminating-with-uncaught-exception-of-type-nsexception-lldb)

> CMYR - "his could also happen if you've wired up a button to an IBAction that doesn't exist anymore \(or has been renamed\)"
>
> If you're running into this problem make sure that you go to Main.storyboard, RIGHT click on the yellow box icon \(view controller\) at the top of the phone outline and DELETE the outlet\(s\) with yellow flags.
>
> What happens in instances like this is you probably named an action, then renamed it. You need to delete the old name and if that was the only issue will start right up in sim!

## 2.unrecognized selector sent to instance '

**情况说明：点按某个控件出现崩溃（crash）**

解决步骤：定位断点进行查看

Cnblogs

[http://www.cnblogs.com/liuguanlei/p/4482327.html](http://www.cnblogs.com/liuguanlei/p/4482327.html)

> 在Xcode的菜单栏中选择Debug-&gt;Breakpoints-&gt;Create Symbolic Breakpoint点击后，会添加一个断点调试，弹出编辑框
>
> 在编辑框的Symbol中填写`-[NSObject(NSObject)doesNotRecognizeSelector:]`此方法签名，对于边看本博文边试验的同学来说，在复制方法签名后想粘贴的时候，发现Xcode中的编辑框不见了，此时右击刚才添加的那个断点，选择Edit Breakpoint即可。
>
> 运行代码，断点就会停留在导致崩溃的地方。



