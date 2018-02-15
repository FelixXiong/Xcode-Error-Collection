# his class is not key value coding-compliant for the key '

参考链接

[http://blog.csdn.net/menxu\_work/article/details/8825664](http://blog.csdn.net/menxu_work/article/details/8825664)

> 一般此问题 都是由interface build与代码中IBOutlet的连接所引起的。
>
> 可能是在代码中对iboutlet的名称进行了修改，导致interface build中的连接失效。
>
> 如果在该viewcontroller连接的xib文件中没发现错误，
>
> 那就很可能是mainWindow.xib文件中存在问题，
>
> 本人遇到的问题是在mainWindow.xib的tabbarcontroller的某个tab的viewcontroller设置了loadfrom"\*\*.xib"，
>
> 但忘了将其class设为对应的viewcontroller类了。
>
> 仔细检查自己的nib文件，清理、修正不正确的连接关系即可。

## 可能报错的情况

**1.在修改从Storyboard拖拽的控件到swift文件中的控件（类名）时之前的IBOutlet和IBAction链接未去除**

报错位置：控制台

解决方法：去除修改类名之前的IBOutlet和IBAction链接

