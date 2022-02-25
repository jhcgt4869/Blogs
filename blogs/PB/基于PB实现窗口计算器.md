# 基于PB实现窗口计算器

## 新建一个环境
`File`->`New`

![image-20211104173314558](image/image-20211104173314558.png)

`Woekspace`->`Workspace`->`ok`

![image-20211104211318425](image/image-20211104211318425.png)	

输入文件名确认

![image-20211104211512782](image/image-20211104211512782.png)

查看即可得到我们的环境

![img](image/08e9d56a59274426a64fe0f0a5ac938c.png)

## 添加`Target`
`Target`->`Application`->`OK`

![img](image/9906a08d84f74c3eaa9829865e2d61a0.png)

添加名字即可，后面的是自动生成的。

![img](image/fa014b8183ff4830bc284dd24fa619b0.png)

查看内容

![img](image/4e4db77e611e43d48db64de09b994df1.png)

### 生成窗口
`PB Object` ->`Window`->`OK`

![image-20211104220808199](image/image-20211104220808199.png)

查看窗口

![image-20211104220848250](image/image-20211104220848250.png)

## 插入组件
`Insert`->`Control`->`CommandButton`

![img](image/9cc163a3360943a0834a85927f04f264.png)



![image-20211104222239037](image/image-20211104222239037.png)





![image-20211104223832174](image/image-20211104223832174.png)

* 添加`SingleLineEdit`组件

![image-20211104224923277](image/image-20211104224923277.png)



![image-20211104225042592](image/image-20211104225042592.png)	

* 添加`Static Text`组件

![image-20211104225424024](image/image-20211104225424024.png)

## 组件成果展示

![img](image/93de012ee4be45a5974525d785adc026.png)

### 添加代码
添加全局变量

![image-20211104225546749](image/image-20211104225546749.png)

### 声明变量
```sql
decimal data  //保存中间结果
char str    //保存按下的运算符
int flag    //flag=1表示按下的数字是前面数字的一部分，flag=0表示按下的数字是一个新的数字的开始
```
### 十个数字按钮和小数点按钮代码

```sql
if flag=0 then 
	sle_1.text=""
	flag=1
end if
sle_1.text=sle_1.text+this.text
```
### +、-、*、/运算按钮代码

```sql
choose case str
	case '*'
		sle_1.text=string(dec(sle_1.text)*data)
	case '/'
		sle_1.text=string(data/dec(sle_1.text))
	case '+'
		sle_1.text=string(dec(sle_1.text)+data)
	case '-'
		sle_1.text=string(data - dec(sle_1.text))
end choose
data=dec(sle_1.text)
str=this.text
flag=0
```
### “=”按钮代码

```sql
choose case str
	case '*'
		sle_1.text=string(dec(sle_1.text)*data)
	case '/'
		sle_1.text=string(data/dec(sle_1.text))
	case '+'
		sle_1.text=string(dec(sle_1.text)+data)
	case '-'
		sle_1.text=string(data - dec(sle_1.text))
end choose
flag=0
str=''
```
`ctrl+S`保存项目使用`W_`开头

![image-20211104225833957](image/image-20211104225833957.png)

```sql
open(w_calculator)
```