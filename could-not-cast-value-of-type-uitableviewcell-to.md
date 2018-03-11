# Could not cast value of type 'UITableViewCell' \(\) to '.' \(\)

**参考链接**

cnblogs

[swift类型转换之Could not cast value of type xxx to xxx错误的一种特殊情况记录](http://www.cnblogs.com/yajunLi/p/6488957.html)

> 这句话在swift中的使用，是做model类型强制转换（as！）时发生的。
>
> 分析了很多原因，都不能解决，后来偶然一次才发现了根本原因如下：
>
> 因为我之前的项目有两个Target，中间有共用model，然后，打包的时候，需要分开两个包，但其中的model我为了省事，就直接拷贝复用了，类名称都是一样的，然后，在使用的项目里，会引用这两个包，解析的时候，有时就会报如上的错误，猜测原因就是运行时把两个类弄混了，因为名称是一样的。
>
> 解决办法：只需要将另一个包里的模型类名称改一下就行了，让两者不要重复。这样就不会产生这个错误了。

Stackoverflow

[Swift, could not cast value of type](https://stackoverflow.com/questions/29831587/swift-could-not-cast-value-of-type)  


