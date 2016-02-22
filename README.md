swift代码规范
=====
#####Gavin 一木


ps:内容由作者整理公司代码、网络上的基础规范和在实际开发的经验总结。

### 命名规范
##### 文件命名：遵循大驼峰命名。<br>
        例如：TestViewController
##### 变量常量函数命名：遵循小驼峰。<br>
        例如：let nickName = "Gavin"<br>
             func testTap(){}
##### 图片文件命名：小写单词+“_”命名。<br>
        例如：tabbar_home@2x.png
##### 全局常量命名：有意义的标识+常量实际意义，要全部大写。<br>
        例如：public let SCREENW = UIScreen.mainScreen().bounds.size.width <br>
             public let APP_COLOR_BACKGROUND = UIColor(rgb: 0xdddddd)
##### 命名选择使用功能和意思相近的英文单词或者组合，适当时候可以选测前缀区分变量的作用范围。
### 注释的规范

