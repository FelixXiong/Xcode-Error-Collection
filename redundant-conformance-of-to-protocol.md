# Redundant conformance of '' to protocol ''

**参考链接**

Stackoverflow

[Swift : Redundant conformance of Viewcontroller to protocol UIGestureRecognizerDelegate](https://stackoverflow.com/questions/32540452/swift-redundant-conformance-of-viewcontroller-to-protocol-uigesturerecognizerd)

可能报错的情况

**1.各种ViewController不正确**

报错位置：\#import下方class 类名处

```swift
class ListTableViewController: UITableViewController,UITableViewDataSource,UITableViewDelegate{
```

解决方法：应为ViewController（以下简称VC），实际则输入为TableViewViewController，VC文件开头class处修改对则正常。

```swift
class ListViewController: UIViewController,UITableViewDataSource,UITableViewDelegate{
```



