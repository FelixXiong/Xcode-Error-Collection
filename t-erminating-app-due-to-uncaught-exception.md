# Terminating app due to uncaught exception ''

# reason: '-\[项目名称.项目（自定义）类名:\]:

报错位置：控制台

## 1.‘NSInvalidArgumentException'

### 1.2:unrecognized selector sent to instance ：

**出现此问题的情况说明：**

1:未设置代理

2.点按某个控件出现崩溃（crash）

**解决步骤：**

1:设置代理（Delegate）

2.定位断点进行查看

**参考链接：**

2:

cnblogs

[http://www.cnblogs.com/liuguanlei/p/4482327.html](http://www.cnblogs.com/liuguanlei/p/4482327.html)

> 在Xcode的菜单栏中选择Debug-&gt;Breakpoints-&gt;Create Symbolic Breakpoint点击后，会添加一个断点调试，弹出编辑框
>
> 在编辑框的Symbol中填写`-[NSObject(NSObject)doesNotRecognizeSelector:]`此方法签名，对于边看本博文边试验的同学来说，在复制方法签名后想粘贴的时候，发现Xcode中的编辑框不见了，此时右击刚才添加的那个断点，选择Edit Breakpoint即可。
>
> 运行代码，断点就会停留在导致崩溃的地方。

### 1.3.'Could not find a storyboard named 'Main' in bundle NSBundle &lt;/Users//Library/Developer/CoreSimulator/Devices//data/Containers/Bundle/Application//.app&gt; \(loaded\)'

**出现此问题的情况说明：**

删除Main.Storyboard之后再从文件夹复制上一个文件（没有选择添加文件）

**解决步骤：**

**参考链接：**

cnblogs

[http://www.cnblogs.com/ygm900/p/3836580.html](http://www.cnblogs.com/ygm900/p/3836580.html)

> 1、删掉工程中main.storyboard 后要删除plist文件中对应的键值，否则会报如下错误： Could not find a storyboard named 'Main' in bundle NSBundle
>
> ![](/assets/102112555517509.png)
>
> 2、删除main.storyboard后，需要在AppDelegate.m中初始化一个window进行使用，否则应用程序没有window可用。\`\`\`
>
> ```swift
> self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]]
> ```

### 1.4.'Could not load NIB in bundle: 'NSBundle &lt;/Users//Library/Developer/CoreSimulator/Devices//data/Containers/Bundle/Application//.app&gt; \(loaded\)' with name 'Main''

**出现此问题的情况说明：**

删除Main.Storyboard之后再从文件夹复制上一个文件\(上一个文件\)，重新添加上图中Info.plist键值

**解决步骤：**

**参考链接：**

Starkoverflow

[https://stackoverflow.com/questions/6827949/could-not-load-nib-in-bundle/6827988](https://stackoverflow.com/questions/6827949/could-not-load-nib-in-bundle/6827988)

> You have to take care of two things :
>
> 1. this call assumes you have a file named 'ViewLecturer.xib' and not 'file.xib'
> 2. make sure the file is included in the app bundle. Check that in the build phases &gt; copy ressources to bundle.

## 2.'NSUnknownKeyException'

### 2.1.this class is not key value coding-compliant for the key'

**出现此问题的情况说明：**

1:模拟器出现白屏

2:运行之后点击控件数次发生崩溃

**解决步骤：**

1:检查是否有黄色的叹号的Outlets，进行删除。

2:去除更改过控件值之后的IBOutlet或者IBAction

**参考链接：**

Stackoverflow

[libc++abi.dylib: terminating with uncaught exception of type NSException \(lldb\)](https://stackoverflow.com/questions/26442414/libcabi-dylib-terminating-with-uncaught-exception-of-type-nsexception-lldb)

> CMYR - "his could also happen if you've wired up a button to an IBAction that doesn't exist anymore \(or has been renamed\)"
>
> If you're running into this problem make sure that you go to Main.storyboard, RIGHT click on the yellow box icon \(view controller\) at the top of the phone outline and DELETE the outlet\(s\) with yellow flags.
>
> What happens in instances like this is you probably named an action, then renamed it. You need to delete the old name and if that was the only issue will start right up in sim!

## \*.可能报错的情况

**1.Controller在调用的时候声明成了局部变量，系统无法找到正确的 Controller.**

**解决方法：不要把controller 写成局部变量。（不用xib，无所谓）**

**参考链接**

CSDN

[http://blog.csdn.net/hong1595/article/details/39189923](https://www.gitbook.com/book/felixxiong/xcode/edit#)

> 我的controller，在调用的时候声明成了局部变量，系统无法找到正确的 controller.

## 



