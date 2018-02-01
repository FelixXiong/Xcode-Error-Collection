## libc++abi.dylib: 

## terminating with uncaught exception of type NSException

### 模拟器出现白屏

检查是否有黄色的叹号的Outlets，进行删除。

[libc++abi.dylib: terminating with uncaught exception of type NSException \(lldb\)](https://stackoverflow.com/questions/26442414/libcabi-dylib-terminating-with-uncaught-exception-of-type-nsexception-lldb)

> CMYR - "his could also happen if you've wired up a button to an IBAction that doesn't exist anymore \(or has been renamed\)"
>
> If you're running into this problem make sure that you go to Main.storyboard, RIGHT click on the yellow box icon \(view controller\) at the top of the phone outline and DELETE the outlet\(s\) with yellow flags.
>
> What happens in instances like this is you probably named an action, then renamed it. You need to delete the old name and if that was the only issue will start right up in sim!



#### 点按某个控件出现崩溃（crash）



