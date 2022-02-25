# PB控件操作函数

## 数据窗口控件函数

此处假设窗口为DW_1

### 数据窗口插入行

```sql 
DW_1.InsertRow(n)
```

	### 数据窗口删除行

```sql
DW_1.DeleteRow(n)
```

### 检索

```sql
DW_1.Retrieve()
```

### 光标互动到指定行

```sql
DW_1.ScrollToRow(n)
```

### 光标移动到下一行

```sql
DW_1.ScollPriorRow()
```

### 光标移动到下一行

```sql
DW_1.ScrollNextRow()
```

### 获取数据窗口总行数

```sql
DW_1.ROWCount()
```

### 设计程序标准

```sql
DW_1.SetSort("format")
```

* format :A为升序，D为降序

### 对数据窗口进行过滤

```sql
DW_1.SetFileter("format")
```

* format为条件

* 举例：

  ```sql
  DW_1.SetFileter("age>10 and age<25")
  ```

  取消：

  ```sql
  DW_1.SetFileter("")
  ```

### 清除数据控件窗口所有数据

```sql
DW_1.Reset()
```

### 相对滚动

```sql
DW_1.Scroll(n)
```

* n为正值向下滚动n个
* n为负值向上滚动n个

### 获取当前光标所在行号

```sql
DW_1.GetRow()  // 行号
DW_1.GetColumn()  // 列号
```

### 获取数据窗口总行数

```sql
DW_1.GetCount()
```

### 设置数据窗口当前行列

```sql
DW_1.SetRow()  // 行号
DW_1.SetColumn()  // 列号
```

### 获取指定行列的值

```sql
DW_1.GetItemString(<行>, <列>)  // 字符串
DW_1.GetItemNumber(<行>, <列>)  // 数值
DW_1.GetItemDate(<行>, <列>)  // 时间
DW_1.GetItemDatetime(<行>, <列>)  // 日期时间
DW_1.GetItemDecimal(<行>, <列>)  // 浮点型
```



