# Terminating app due to uncaught exception ''

# reason: '-\[项目名称.项目（自定义）类名:\]: unrecognized selector sent to instance ：

报错位置：控制台

## 1.‘NSInvalidArgumentException'

## \*.可能报错的情况

**情况说明：controller，在调用的时候声明成了局部变量，系统无法找到正确的 controller.**

解决方法：不要把controller 写成局部变量。（不用xib，无所谓）

参考链接

CSDN

[http://blog.csdn.net/hong1595/article/details/39189923](https://www.gitbook.com/book/felixxiong/xcode/edit#)

> 我的controller，在调用的时候声明成了局部变量，系统无法找到正确的 controller.

## 



