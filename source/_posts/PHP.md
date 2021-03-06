---
title: PHP
date: 2017-12-21 22:06:52
id: 1513865212
tags:
  - 学习笔记
categories:
  - 笔记
keywords: PHP
description: PHP学习笔记
---

# 学习路径:
1. PHP官网看下基础语法
2. 找个PHP框架学习下,如:轻量级的lumen/yaf,稍微重量级些的:yii/ThinkPHP

# 学习笔记
## 《PHP入门篇》
[PHP入门篇](https://www.imooc.com/learn/54)
### 笔记
1. 在PHP中变量名是区分大小写的
2. 变量占用的空间单元不一样
3. 用”echo”指令输出布尔类型时，如果是“true”则输出的是“1”，“false”则什么也不输出。
4. 当双引号中包含变量时，变量会与双引号中的内容连接在一起;当单引号中包含变量时，变量会被当做字符串输出。
5. <<< 定界符，+标识符(自定义，保持末尾行一致并另起一行)定义长字符串
6. NULL是空类型，对大小写不敏感，NULL类型只有一个取值，表示一个变量没有值，当被赋值为NULL，或者尚未被赋值，或者被unset()，这三种情况下变量被认为为NULL。
7. define定义常量，constant获取常量，defined判断常量是否定义
8. PHP运算符一般分为算术运算符（+ - * / %）、赋值运算符（= &引用赋值，意味着两个变量都指向同一个数据。）、比较运算符、三元运算符（?:）、逻辑运算符、字符串连接运算符（. .=）、错误控制运算符（@）。
  ![比较运算符](.\PHP\php比较运算符.jpg)
  ![逻辑运算符](.\PHP\php逻辑运算符.jpg)
9. 在PHP中foreach循环语句，常用于遍历数组，一般有两种使用方式:不取下标、取下标。
10. 


## 《7天学会PHP》
###那双引号和单引号有什么区别呢？
1. 双引号解析变量，但是单引号不解析变量。
2. 在双引号里面插入变量，变量后面如果有英文或中文字符，它会把这个字符和变量拼接起来，视为一整个变量。一定要在变量后面接上特殊字符，例如空格等分开。
3. 如果在双引号里面插变量的时候，后面不想有空格，可以拿大括号将变量包起来。
4. 双引号解析转义字符，单引号不解析转义字符。但，单引号能解析' 和\
5. 单引号效率高于双引号，尽可能使用单引号
6. 双号和单引号可以互插！！！双引号当中插入单引号，单引号当中插入变量，这个变量会被解析。
7. 神奇的字符串拼接胶水——（.）点，用来拼接字符串。
8. 我们将定界符声明字符串视为双引号一样的功能来看待。

###判断数据类型

gettype(传入一个变量) 能够获得变量的类型
var_dump(传入一个变量) 输出变类型和值
我们使用is_* 系列函数。 is_types这一系列的函数，来进行判断某个东西是不是某个类型。如果是这个类型返回真，不是这个类型返回假。

is_int	是否为整型
is_bool	是否为布尔
is_float	是否是浮点
is_string	是否是字符串
is_array	是否是数组
is_object	是否是对象
is_null	是否为空
is_resource	是否为资源
is_scalar	是否为标量
is_numeric	是否为数值类型
is_callable	是否为函

###  布尔值判断时的自动类型转换：

1. 整型的0为假，其他整型值全为真
2. 浮点的0.0，布尔值的假。小数点后只要有一个非零的数值即为真。
3. 空字符串为假，只要里面有一个空格都算真。
4. 字符串的0，也将其看作是假。其他的都为真
5. 空数组也将其视为假，只要里面有一个值，就为真。
6. 空也为假
7. 未声明成功的资源也为假

### 自动类型转换
 ![逻辑运算符](.\PHP\自动类型转换.png)

### 环境变量
环境变量我们主要用的有$_SERVER和$_ENV两个环境变量。
 ![逻辑运算符](.\PHP\PHP变量.png)

### 自定义函数
1. 函数以function开始
2. function后面接空格，空格后接函数名
3. 函数名与变量命名规则基本一样，但是不同的是：函数名不区分大小写
4. 所谓参数其实就是变量
5. 函数名后接括号，括号内跟参数，参数全都有[]（中括号）括起来了，代表参数可填可不填
6. 如果有参数的话，参数后可以接（＝）等号，等号接默认值。参数值也是用[]（中括号）括起来的，代表选填
7. 函数后的参数变量，主要功能是把函数体外的变量值，传入函数体内来使用，函数体的变量和函数体外的变量通常是两个不同的变量。
8. 函数中的具体功能（功能体）用大括号括起来，代表这是一个函数的功能区间
9. 函数可以有返回值也可以没有返回值，用[]（中括号）括起来的，代表选填。
10. return后接空格，空格后接返回值，若有return,return后的代码均不执行。
11. 函数的执行没有顺序关系，可以在定义处之前的位置调用
12. 函数不能被定义两次，即函数不能被重载

学习到5.2.1