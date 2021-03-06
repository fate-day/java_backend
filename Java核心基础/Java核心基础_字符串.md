# Java核心基础



[TOC]

## 1.基础知识

### 1.5 字符串

Java字符串就是Unicode字符序列，Java没有内置的字符串类型，而是在标准Java类库中提供了一个预定义类叫做String，每个用双引号括起来的字符串都是String类的一个实例。

#### 1.5.1 子串

String类的substring方法可以从一个较大的字符串提取一个子串。

#### 1.5.2 拼接

Java允许使用+号连接（拼接）两个字符串。

如果需要将多个字符串放在一起，用一个定界符分隔，可以使用静态join方法。

**Notes：**

-   当讲一个字符串与一个非字符串的值进行拼接时，后者被转换成字符串。

#### 1.5.3 不可变字符串

String类没有提供用于修改字符串的方法，所以Java文档中将String类对象称为不可变字符串。

#### 1.5.4 检测字符串是否相等

使用equals方法检测两个字符串是否相等，要检测两个字符串是否相等而不区分大小写使用eaualdIgnoreCase方法。一定不要使用运算符==检测两个字符串是否相等。

#### 1.5.5 空串与Null串

空串是长度为0的字符串，String变量还可以存放一个特殊的值null。

#### 1.5.6 构建字符串

有些时候需要由较短的字符串构建字符串，采用字符串连接的方式达到此目的效率较低，每次连接字符串都会构建一个新的String对象，既耗时又浪费空间，使用StringBuilder类就可以避免这个问题的发生。

### 1.6 输入输出

#### 1.6.1 读取输入

想要通过控制台进行输入，首先需要构造一个Scanner对象，并与标准输入流“System.in”关联。

```
Scanner in = new Scanner(System.in)；
```

现在，就可以使用Scanner类的各种方法实现输入操作了。

**Notes：**

-   应为输入是可见的，所以Scanner类不适用于从控制台读取密码。Java SE 6特别引入了Console类实现这个目的。要读取一个密码，可以采用下列代码：



```
Console cons = System.console();
String uername = cons.readLine("User name:");
char[] passwd = cons.readPassword("Paddword");
```

#### 1.6.2 格式化输出

Java格式化数值沿用了C语言库函数中printf方法。

用于printf的转换符：

| 转换符 | 类型                  | 举例                              |
| :------: | :-------------------: | :------------------------------: |
| d      | 十进制整数            | 159                               |
| x      | 十六进制整数          | 9f                                |
| o      | 八进制整数            | 237                               |
| f      | 定点浮点数            | 15.9                              |
| e      | 指数浮点数            | 1.59e+01                          |
| g      | 通用浮点数            | -                                 |
| a      | 十六进制浮点数        | 0x1.fccdp3                        |
| s      | 字符串                | hello                             |
| c      | 字符                  | H                                 |
| b      | 布尔                  | True                              |
| h      | 散列码                | 42628b2                           |
| tx或Tx | 日期时间（T强制大写） | 已经过时，应当改为使用java.time类 |
| %      | 百分号                | %                                 |
| n      | 与平台无关的行分隔符  | -                                 |

**格式化字符串：**











