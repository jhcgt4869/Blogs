## 数据查询
### SELECT查询的基本结构



```sql
SELECT [ALL|DISTINCT] <目标列> FROM <列表名> [WHERE <条件>] [GROUP BY <列名>] [HAVING <条件>] [ORDER BY <列名>] [ASC|DESC];
```
`ALL`：默认值，表示全部

`DISTINCT`:表示不重复的目标列

`where`断句：条件短语  

`GROUP by`： 分组短语

`ORDER by`：排序短语

`ASC`：升序

`DESC`：降序



## 条件语句

### 1、常见的比较符

`<`,`>`,`=`,`!>`,`!<`,`!=`,`<>`,`not`,`not>`,`not=`,`not<`等

### 2、范围确定

`BETWEEN……BY` ：在……之间

`NOT BETWEEN …… BY`：不在……之间

### 3、确定集合

`IN`

`NOT IN`

### 4、字符匹配

`LINK`

`NOT LINK`

`%` 通配符

### 5、空值

`IS NULL`

`IS NOT NULL`

主码不能够为空

注意参照完整性规则

### 6、连接符

`AND`：与

`OR`：或

### 7、函数

```sql
count(*)           --统计元组个数
count(<列名>)       --统计列值个数
SUM(<列名>)         --统计列的和值
AVG(<列名>)         --统计平均值
MAX(<列名>)         --统计最大值
MIN(<列名>)         --统计最小值
```

## 嵌套查询

### SELECT-FROM-WHERE

查询语句块

```sql
SELECT-FROM-WHERE
```

如果一个查询快在另一个查询块的`where`中就是嵌套查询。

其中：

上层查询为父查询（外查询）

下层查询为子查询（内查询）

查询顺序：由内向外

内层查询不能够有`ORDER BY` 子句排序只对最终结果有效。（`ORDER BY` 为排序语句）

1、可以带有`IN`的子查询

2、带有比较符的子查询

3、带有ANY或ALL的查询

`> NAY`:大于子查询结果的某个值

`> ALL`:大于子查询结果的所有值

4、带有大量量词的查询（`EXISTS`）

①、带有`EXISTS`的查询不返回值，只返回真或假

②、使用`EXISTS`语句引出的子查询只能够用`*`进行

