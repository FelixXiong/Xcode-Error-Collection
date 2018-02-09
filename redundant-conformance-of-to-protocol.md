# Redundant conformance of '' to protocol ''

Stackoverflow

[https://stackoverflow.com/questions/32540452/swift-redundant-conformance-of-viewcontroller-to-protocol-uigesturerecognizerd](https://stackoverflow.com/questions/32540452/swift-redundant-conformance-of-viewcontroller-to-protocol-uigesturerecognizerd)

## 可能报错的情况

**各种ViewController不对**

报错位置：\#import下方class 类名处

```swift
class WillLearnListTableViewController: UITableViewController,UITableViewDataSource,UITableViewDelegate{
```

应为ViewController（以下简称VC），实际则输入为TableViewViewController，VC文件开头class处修改对则正常。

```swift
class WillLearnListViewController: UIViewController,UITableViewDataSource,UITableViewDelegate{
```



