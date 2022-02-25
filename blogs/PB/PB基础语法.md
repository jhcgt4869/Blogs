# PB基础语法

### 注释

1、单行注释：`//`

2、多行注释：`/*   */`

### 标识符

1、字母开头

2、不超过40个字符

3、不能够使用标点符号、运算符

4、大小写不敏感（不区分大小写）

### 连续符

`&`

### 特殊符号

`~n` ：换行

`~r`：回车

`~t`：制表符

（这里类似于把`\`换成了`~`）

### 信息框

`MessageBox(<标题栏显示信息>)`

### 常用数据类型

1、单个字符型：`cahr`(character)

2、字符串：`string`

3、整型：`int`(integer)

4、浮点型：`real`(精度6位)

5、长整型：`long`

6、浮点型：`decimal`（`dec`）（精度18位）	

7、双精度：`double`（可以为指数，精度15位）

8、时间型：`time`(NN:MM:SS)

9、日期型：`data`(YYYY:MM:DD)

## 变量声明及作用域

1、数据类型 

<变量名> [= <表达式>]

例如：

```sql
int x;
cahr a = 'i';
string b;
```

数组

```sql
int m[100];  // 这里的下标从1开始
```

### 变量类型

1、`loac` 本地变量

2、`instance`  实例变量

3、`Global` 全局变量

4、`shared` 共享变量



## 运算符

### 算数运算符

```sql
+|-|*|/|^|++|--|+=|-=|*=|/=|^=
```

### 关系运算符

```sql
<|>|=|>=|<=|<>
```

### 逻辑运算符

```sql
and|or|not
```

## 条件语句

#### 判断语句

* IF语句

  IF行语句：

  ```sql
  IF <条件> then <语句>
  ```

  IF块语句：

  ```sql
  IF <条件>
  THEN <语句块>
  END IF
  ```

* IF - ELSE 语句

  IF - ELSE 行语句：

  ```sql
  IF <条件> then <语句1> ELSE <语句2>
  ```

  IF - ELSE 块语句：

  ```sql
  IF <条件>
  THEN <语句块1>
  ELSE <语句块2>
  END IF
  ```

* 多迭语句

  CHOOSE 语句

  ```sql
  CHOOSE CASE <测试表达式>
  <语句块1>
  CASE <表达式2>
  <语句块2>
  ……
  END CHOOSE
  ```

#### 循环语句

* FOR循环

  ```sql
  FOR <循环变量> = <初始值> to <终值> [<步长值>]
      <循环体>
      NEXT
  ```

  

* DO  WHILE - LOOP语句

  ```sql
  DO WHEILE <条件>
      <循环体>
      LOOP
  ```

* DO - LOOP -WHILE语句

  ```sql
  DO
  <循环体>
  LOOP WHILE <条件>
  ```

* DO  UNTIL - LOOP语句

  ```sql
  DO UNTIL <条件>
      <循环体>
      LOOP
  ```

* DO - LOOP -UNTIL语句

  ```sql
  DO
  <循环体>
  LOOP UNTIL <条件>
  ```

