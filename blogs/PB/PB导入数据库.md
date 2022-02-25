

# PB导入数据库

## 数据库导入
如何导入第三方数据库？
选择`Utilities`如何选择`Create ODBC Data Source`

![image-20211103234554051](./image/image-20211103234554051.png)

选择第二个即可如然后点击下一步。

![image-20211103234805517](image/image-20211103234805517.png)

下一步

![image-20211103234834831](image/image-20211103234834831.png)

​	完成

![image-20211103234904068](image/image-20211103234904068.png)

名字自定义！

![img](image/d76cbd6f82d548548a3edf2d076a69f6.png)

选中`Login`

![img](image/34046c13e3314e62a4ee6073d341dfe4.png)

输入账号：`dba`密码`sql`

![image-20211103235214476](image/image-20211103235214476.png)

选择`Database`选中`Browser……`

![image-20211103235259977](image/image-20211103235259977.png)

找到后缀为`.db`的文件

![image-20211104002256490](image/image-20211104002256490.png)

点击确认以后
到数据库中`ODB ODBC`右键选择`new Profule…`

![img](image/f39bf56174b3401db644114e17fcf7a8.png)

其中`Profile Name`可以自定义
`Data Source`就是你之前定义的`ODBC`名字

![image-20211104002411244](image/image-20211104002411244.png)

这里是账号密码

![img](image/4cdeafd90c304d4c96872381f6a5becb.png)

确认以后找到刚刚自定义的数据名字
右键点击`Connect`

![image-20211104002858392](image/image-20211104002858392.png)