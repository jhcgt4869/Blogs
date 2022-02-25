# 	PB数据库搭建

### 版本说明

这里使用的是：`PowerBuilder 9.0`

## 新建数据库

1、进入PB点击数据库按钮

![image-20211103154204507](./image/image-20211103154204507.png)

2、选择`ODB ODBC`数据量

![image-20211103154908555](./image/image-20211103154908555.png)

3、选择`Utilities`然后选择里面的`Create ASA Database`

![image-20211103155343195](./image/image-20211103155343195.png)

4、对数据库进行保存

`Database Name`：保存的目标地址，点击地址选择按钮进行

`Use Transaction Log`：日志文件生成（是否需要更据自己实践情况决定）

![image-20211103155614221](./image/image-20211103155614221.png)

确认即可

![image-20211103164244842](./image/image-20211103164244842.png)

此时就出现了我们的数据库

![image-20211103164419817](./image/image-20211103164419817.png)

![image-20211103165835911](./image/image-20211103165835911.png)

### 创建数据表

* 方法一：表格法：

![image-20211103171015144](./image/image-20211103171015144.png)

![image-20211103171147707](./image/image-20211103171147707.png)

更据内容填写相对应的值即可

* 方法二：使用SQL代码完成编译

![image-20211103171326048](./image/image-20211103171326048.png)

代码如下：

```sql
create table S( sno char(4),sname char(8),sex char(2),age char(2),sdept char(10),primary key(sno));
```

输入代码以后一点击`Design`然后选择`Execute ISQL……`进行运行或者使用快捷键`Ctrl+L`

温馨提示：点击一遍就行（不要问为什么！）

![image-20211103172002038](./image/image-20211103172002038.png)

### 查看内容

`Tables`右键选择`Refresh`刷新即可

（如果没有响应，可以重启软件）

![image-20211103173126471](./image/image-20211103173126471.png)

![image-20211103173305190](./image/image-20211103173305190.png)

## 表的查看

* 使用窗口进行查看

  选中表以后右键`Edit Data`然后`Grid…`

  ![image-20211103213239141](./image/image-20211103213239141.png)

* 使用代码进行查看

  ```sql
  select * from S;
  ```

  

![image-20211103230512070](./image/image-20211103230512070.png)

### 添加数据表数据

```sql
insert into S values('9801','李铭','男','19','计算机软件');
insert into S values('9802','刘晓鸣','男','20','计算机应用');
insert into S values('9806','刘成刚','男','21','计算机软件');
insert into S values('9807','王铭','男','22','计算机应用');
insert into S values('9808','宣明尼','女','18','计算机应用');
insert into S values('9809','柳红利','女','19','计算机软件');
insert into S values('9803','李明','男','22','计算机应用');
insert into S values('9804','张鹰','女','21','计算机软件');
insert into S values('9805','刘竟静','女','22','计算机软件');
select * from S;
```

![image-20211103231757414](image/image-20211103231757414.png)

结果查看：

![image-20211103231821951](image/image-20211103231821951.png)
