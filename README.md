swift代码规范
=====
#####Gavin 一木


ps:内容由作者整理公司代码、网络上的基础规范和在实际开发的经验总结。

### 命名规范
##### 文件命名：遵循大驼峰命名。
        例如：TestViewController
##### 变量常量函数命名：遵循小驼峰。
        例如：let nickName = "Gavin"
             func testTap(){}
##### 图片文件命名：小写单词+“_”命名。
        例如：tabbar_home@2x.png
##### 全局常量命名：有意义的标识+常量实际意义，要全部大写。
        例如：public let SCREENW = UIScreen.mainScreen().bounds.size.width 
             public let APP_COLOR_BACKGROUND = UIColor(rgb: 0xdddddd)
##### 命名选择使用功能和意思相近的英文单词或者组合，适当时候可以选测前缀区分变量的作用范围。
### 注释的规范
##### 代码中单行注释，一些属性使用“//”
        例如：var isLine = true //是否在线，true在线、false离线
              // 回传信息        
              var backBlockValue:((String) ->())?
##### 一个方法有多个参数或者有返回值是可以在方法前添加“/* …… */”
        例如：
        /**
        tableViewCell内容及样式
     
         - parameter tableView: 表试图
         - parameter indexPath: 单元个数
     
         - returns: 返回Cell内容及样式
         */
        func tableView(tableView: UITableView, cellForRowAtIndexPath indexPath: NSIndexPath) -> UITableViewCell 
        {
                let cell = UITableViewCell(style: UITableViewCellStyle.Value1, reuseIdentifier: "Cell")
                return cell
        }
##### 代码整体结构层次可使用“//MARK: ****”
        例如：在代码中写入可区分不同内容，提高程序阅读性
        //MARK: - UITableViewDataSource
        //MARK: - UITextFieldDelegate
        ![](https://github.com/huyanshi/swift-/blob/master/img/MARK.png)
##### 代码中没有完成还需要处理可使用“//TODO: ****”
        例如：
        //TODO: 闭包函数返回信息内容
        detailVC.backValue = {(value:String) in
        weakSelf!.sendRequest()
        tableView.reloadData()
        }
        ![](https://github.com/huyanshi/swift-/blob/master/img/TODO.png)
##### 后期调整或者修改代码可使用“//FIXME: ****”
        例如：
        func tableView(tableView: UITableView, cellForRowAtIndexPath indexPath: NSIndexPath) -> UITableViewCell {
        let cellIdentifier = "CellIdentifier"
        let cell: UITableViewCell! = tableView.dequeueReusableCellWithIdentifier(cellIdentifier,forIndexPath: indexPath) as? UITableViewCell
        //FIXME: 修改bug
        let row = indexPath.row
        let rowDict = self.listTeams[row] as [String:String]
        ...
        return cell
    }

