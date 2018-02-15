# Terminating app due to uncaught exception ''

# reason: '-\[项目名称.项目（自定义）类名:\]: unrecognized selector sent to instance ：

报错位置：控制台

## 1.‘NSInvalidArgumentException'

## 2.'NSUnknownKeyException'

### 2.1.this class is not key value coding-compliant for the key'

**出现此问题的情况说明：**

**1:模拟器出现白屏**

**2:运行之后点击控件发生崩溃**

解决步骤：

1:检查是否有黄色的叹号的Outlets，进行删除。

2:去除更改过控件值之后的IBOutlet或者IBAction

Stackoverflow

[libc++abi.dylib: terminating with uncaught exception of type NSException \(lldb\)](https://stackoverflow.com/questions/26442414/libcabi-dylib-terminating-with-uncaught-exception-of-type-nsexception-lldb)

> CMYR - "his could also happen if you've wired up a button to an IBAction that doesn't exist anymore \(or has been renamed\)"
>
> If you're running into this problem make sure that you go to Main.storyboard, RIGHT click on the yellow box icon \(view controller\) at the top of the phone outline and DELETE the outlet\(s\) with yellow flags.
>
> What happens in instances like this is you probably named an action, then renamed it. You need to delete the old name and if that was the only issue will start right up in sim!

## \*.可能报错的情况

**情况说明：controller，在调用的时候声明成了局部变量，系统无法找到正确的 controller.**

解决方法：不要把controller 写成局部变量。（不用xib，无所谓）

参考链接

CSDN

[http://blog.csdn.net/hong1595/article/details/39189923](https://www.gitbook.com/book/felixxiong/xcode/edit#)

> 我的controller，在调用的时候声明成了局部变量，系统无法找到正确的 controller.

## 



