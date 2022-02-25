@[TOC](SQL基本语法（一）)

## SQL是什么？
SQL（Structured Query Language）结构化查询语言，是一种关系数据库基本语言，在各个软件中使用方式基本相同（存在有靴微的差异）

## 常用数据类型
* 字符串型（`character(n)`/`char(n)`）
* 数值型
    1、整型（`Integer`、`int`）
    2、浮点型(`REAL`/`Float`)
    3、双精度型(`double`）
* 	日期型（`Date` `YYYY-MM-DD`）
* 时间型(`Time` `HH:MM:SS`)


## 新建表
创建基本表
使用`Create Table`语句实现

```sql
CREATE TABLE <基本表名>（
	<列名 类型 >,
	…………
	<完整性约束>）
```
完整性约束：
1、主键（PRIMARY KEY）
2、外键(FOREIGN KEY)
3、句子检查(CHECK)

创建一个学生信息表(S)，内含学号(sno)字符型4个字符，学生姓名（sname），字符型8个字符，性别（sex）字符型2个字符，系别（sdept）字符串10个字符。主键是学号。

```sql
create table S( 
sno char(4), 
sname char(8),
sex char(2),
age char(2),
sdept char(10),
primary key(sno));
```

## 修改表
### 新增列

```sql
ALTER TABLE <表名> ADD <列名> <类型>;
```
举例：
新增一个年龄（sage）整型

```sql
alter table S add sage int;
```

### 删除列

```sql
ALTER TABLE <列表名> DROP <列名> [CASCADE|RESTRICT];
```
`CASCADE`:表示删除数据以后，所有引用改列的数据会一起删除
`RESTRICT`: 只有没有没有师徒或者约束条件才允许被删除，否则则不允许被删除

举例：
删除年龄列

```sql
alter table S drop sage CASCADE;
```
 
 ### 撤销表
 

```sql
DROP TABLE <基本表名> [CASCADE|RESTRICT];
```
示例：撤销表

```sql
DROP TABLE S CASCADE;
```
## 索引的创建
### 索引创建

```sql
CREATE [UNIQUE] INDEX <索引名> ON <基本表名>(<列名序号>);
```

`UNIQUE`：表示每个索引对应唯一的数据记录
索引：当表没有设立主键可以使用索引起到主键的作用

```sql
CREATE UNIQUE INDEX S_INDEX ON S;
```

### 撤销索引

```sql
DROP INDEX <索引名>
```

举例：撤销索引

```sql
DROP INDEX  S_INDEX;
```

## 数据更新
### 数据插入(元组数据、表数据)
* 单元组插入
```sql
insert into <数据表>[<列名序列>] values (<元组值>);
```
* 多元组插入

```sql
insert into <数据表>[<列名序列>] values (<元组值>),(<元组值>),……,(<元组值>);
```
* 查询结果的插入

```sql
在这里插入代码片
```
```sql
insert into <数据表>[<列名序列>] <SELECT 查询语句>;
```

* 表的插入

```sql
INSERT INTO <基本表名>[(<列表序名>)] TABLE <基本表名>;
```
### 数据删除

```sql
DELETE FROM <基本表名> [WHERE<条件表达式>]
```

举例：
给S表添加数据：
![在这里插入图片描述](https://img-blog.csdnimg.cn/d36684f1b7d244d7867d732c9bab4d98.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBA5LiJ5bKB5a2m57yW56iL,size_18,color_FFFFFF,t_70,g_se,x_16)

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
```
删除最后一个

```sql
DELETE FROM S WHERE Sno='9805';
```


### 下一章
数据查询、表的连接等
