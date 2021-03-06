# Java核心基础

[TOC]

## 1.基础知识点

### 1.4 运算符

Java运算符&优先级表

**Notes：**

-   整数被0除会产生一个异常，尔浮点数被0除将会得到无穷大或NaN结果
-   当参与/运算的两个操作数都是整数时，表示整数除法；否则表示浮点除法
-   对于使用strictfp关键字标记的方法必须使用严格的浮点计算来生成可再生的结果

#### 1.4.1 数学函数与常量

在math类中，包含了各种各样的数学函数。

#### 1.4.2 数值类型之间的转换

下图给出了数值类型之间的合法转换，实心箭头表示无信息丢失的转换，虚箭头表示可能有精度损失的转换。

![数值转换](/home/xiao_qi/Documents/Java后端/notes/img/深度截图_选择区域_20200209093952.png)

#### 1.4.3 强制类型转换

强制类型转换的语法格式是在圆括号中给出想要转换的目标类型，后面紧跟待转换的变量名。

#### 1.4.4 自增自减

前缀形式：先完成加1，后缀形式：使用变量的值。

#### 1.4.5 关系和Boolean运算符

Java使用&&表示”与“运算符，使用||表示”或“运算符，使用！表示”非“运算。

Java支持三元运算符?:，如果条件为true，下面的表达式

```java
condition ? expression1 : expression2
```

#### 1.4.6 位运算符

&（and）、|（or）、^（xor）、～（not）

#### 1.4.7 括号与运算符级别

| 运算符                                                       | 结合性   |
| :---------------------------------------------------------- | :------: |
| [] . ()                                                      | 从左向右 |
| ! ~ ++ -- +（一元运算符）-（一元运算符）()（强制类型转换） new | 从右向左 |
| * /  %                                                       | 从左向右 |
| + -                                                          | 从左向右 |
| << >> >>>                                                    | 从左向右 |
| < <= > >= instanceof                                         | 从左向右 |
| == !=                                                        | 从左向右 |
| &                                                            | 从左向右 |
| ^                                                            | 从左向右 |
| \|                                                           | 从左向右 |
| &&                                                           | 从左向右 |
| \|\|                                                         | 从左向右 |
| ？：                                                         | 从左向左 |
| = += -= *= /= %= &= \|= ^= <<= >>= >>>=                      | 从左向左 |

#### 1.4.8 枚举类型

