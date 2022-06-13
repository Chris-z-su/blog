---
title: Java基础(完整)
date: 2022-05-05 20:57:23
update: 2022-05-05 20:57:23
categories: Java
tags:
  - 编程语言
  - 基础
  - 技术
---

# java基础

> https://app.yinxiang.com/shard/s10/nl/41034272/d2bd137e-ae35-42f0-b79d-a58f3f7f7ef4?title=java

。作业领悟：

1.成员变量不需要初始化，局部变量必须初始化

2.对集合的遍历和删减不可同时进行，因为删减过后集合的长度会发生变化

3.一个迭代器只能用一次

4.从pdf文件中复制中文，可能会出现个别中文乱码的现象

java配置环境变量

JAVA_HOME java安装位置

PATH %JAVA_HOME%\bin

Java学习记录

[https://learn.kaikeba.com](https://learn.kaikeba.com/)

idea使用快捷键

ctrl+Y 删除光标所在行

ctrl+D 复制光标所在行，并插入到光标所在位置下面spring

ctrl+alt+L 格式化代码

ctrl+/ 单行注释

ctrl+shift+/ 多行注释

alt+shift+上下键 选中代码可以上下移动

ctrl +r (replace)  出来替换操作

sout

psvm

soutv 

int i = 1200;

按soutv自动生成   System.out.println("i = " + i);

fori

nfori

nforr

数组名.fori

  for (int i = 0; i < array2.length; i++) {

​      

  }

类中的快捷键

alt + insert 

code-》generate-》constructor 自动生成构造方法

code-》generate-》get set  自动生成get set 方法

需要修改 代码提示 alt /

补充代码末尾； ctrl shift enter

alt enter 导包

ctrl + i 父类方法的覆写 和 重写接口中的抽象和默认方法

ctrl + o 调出父类中可以重写的方法

敲完右边代码自动生成左边的变量 ctrl alt v alt insert

alt insert 导包

ctrl h 查看类的上下继承关系

数组名和集合名.for  生成增强for循环

for (String s : collection) {

​      

​    }

shift shift 出现搜索框，搜索类的源码

ctrl 鼠标左键单击 出现语法提示语句

ctrl z 回退一步操作

shift enter 另起一行

ctrl shift enter 另起一行

ctrl a  然后按空格 全部打勾

在resource层新建多层文件夹com/kkb/dao

在java层新建多层文件夹com.kka.dao

java语言严格区分大小写

在下载好新版本的jdk后要删除旧的jdk

package 声明包的关键字

public 公共的（修饰符）

static 静态的（修饰符）

void 无返回值类型

main 方法名（函数名）

args 数组名

system 系统

out 输出

print 打印

jdk:开发工具包，包含运行环境，核心类库，源码，Jvm标准实现

jre:java运行环境，一些核心类库，jvm

一个java文件中可以有多个类，但只能有一个public修饰的类。

jvm:虚拟机，用于解释执行字节码文件，使java程序可以在不同操作系统上运行

字节 byte或B

1B=8 bit

1kB=1024B

MB GB

// 单行注释

/*   */ 多行注释

/**   */ java特有的多行注释

特殊的注释 /**  */ 放在类和方法定义处，可以用于自动创建文档

包名（文件夹）：全部小写，格式xxx.yyy.zzz

命名法：

类和接口：每个单词首字母都大写  HelloWorld

方法和变量：只有一个单词时，小写 name

​          有多个单词时，第一个单词小写，其余单词首字母大写 nameNext

常量：只有一个单词时大写 MONEY

​     有多个单词时，第一个单词小写其余都大写 heightWEIGHT

​     或者用下划线隔开 HEIGHT_WEIGHT

关键字：publib class static void int package import

保留字：goto const

把路径写进路径变量中，在dos命令中就可以不用考虑路径运行。

Java源文件名要与类名相同

关键字：被java语言赋予特殊含义的单词，全部为小写。

标识符：由字母、数字、下划线、美元符号组成，不能以数字开头，区分大小写

java程序中自己命名的名称都是标识符

public class HelloWord{

​      public static void main(String[] args){

​            System.out.println("Hello Word");

​      }

}

print 打印

println 打印并换行

数据类型

基本数据类型：整数，小数，字符（输出时用'',''里只能有一个字符，一个字符包括一个字母，一个汉字），布尔（输出的只有俩种值，true和false）

引用数据类型：字符串（输出时用""）

常量

整数: byte  1

​     short 2

​     int   4

​     long  8

小数（浮点型）：float 4

​             double 8

字符：char  2

布尔：boolean 1

字符串：String

在声明float类型的时候结尾一定要加f或F ,否则默认为double类型

float a=33.3f

布尔类型只能赋俩个值true或flase

浮点型还可以这样赋值

char c=65;

在定义变量时，字符要加''，字符串要加""；在输出变量时只需要写变量名即可。

例：         char d='1';

​            System.out.println(d);

​             String f="abc";

​            System.out.println(f);

运算符

算术运算符：+（在字符串中起连接作用）、-、*、/、%、++、--

赋值运算符：=，+=（加后赋值），-=，*=，/=，%=

例：a=2,a+=2相当于a=a+2

比较运算符：结果为布尔类型。==，！=，<,>,<=,>=。

逻辑运算符：用于布尔值进行运算的，结果是true或false。

&（与），俩者都为真，值才为真。

|（或），俩者有一个为真即为真。

！（非），取反。

&&（短路与），比&返回更快捷，节省时间。

||（短路或），比|返回值更快。

转义字符

\t 加一个制表符（tab）

第一天

定义long 类型时在结尾加L，否则默认是int类型

long a = 100L

16进制表示的整型以0x开头

int a = 0xff00000

10进制表示的整型以0b开头

int a = 0b900000

使用常量便于理解程序意图

移位运算

<< 左移

\>>  不带符号右移（最高位位符号位）

\>>> 带符号右移

位运算

&运算：都是1结果才是1（保留某些位，将其余位全部置为0）

|运算：只要有一个是1就是（保留某些位，将其余位全部置为1

^异或运算：俩个操作数不相同时为1，相同时为0

~非运算：单目运算符 将0和1互换

不同整型类型进行运算时，结果为较大类型的整型

short s = 10

int i = 20

long L = 30

a =s+i 结果为int类型

b = i+L 结果为long类型

浮点数运算：

浮点数可能无法精确表示

浮点数运算结果可能会有误差

浮点数与整型运算，结果是浮点型

布尔运算

三元运算符

b?x:y 根据条件B计算X或y的值

X，Y只计算一个

且X，Y的类型要相同

字符和字符串

引用类型的理解

变量是指向某个字符串，而不是持有某个字符串

null是个空值

String s = null  指的是S不指向任何字符串

空字符串  ""

方法：把具有独立功能的代码块看做一个整体，避免了编写重复的代码

语法格式：

1.无参定义

修饰符 返回值类型 方法名（）{

​           代码

​          return 结果；（没有返回值不用写）          

}

2.有一个参数的定义

修饰符 返回值类型 方法名（参数）{

​           代码

​          return 结果；（没有返回值不用写）          

}

3.有多个参数的定义

修饰符 返回值类型 方法名（参数1，参数2，参数3）{

​           代码

​          return 结果；（没有返回值不用写）          

}

4.有返回值时

修饰符 返回值类型 方法名（参数）{

​           代码

​          return 包含返回值的变量；          

}

方法的调用：

1.无返回值时

方法名（）

2S

关系运算符

结果皆为布尔类型

逻辑运算符

^异或运算：俩边表达式真假相同时为false，不相同时为true

! 取相反值

&& 左边表达式为假，右边的表达式就不参与运算

||   左边表达式为真，右边的表达式就不参与运算

​    int x = 1;

​    int y = 1;

​    System.out.println((x++>3&&(y++>5)));

​    System.out.println(x);  2

​    System.out.println(y);  1

​    

​     int x = 1;

​    int y = 1;

​    System.out.println((x++>0)||(y++>4));

​    System.out.println(x);  2

​    System.out.println(y);  1

​       

三元运算符

数据类型 变量名 = 布尔表达式？结果1：结果2

真 把结果1赋给变量

假 把结果2赋给变量

结果类型与变量类型要一样

俩个值比大小

String s = 5==9? "相等":"不相等";

三个值中找出最大值

​    int a = 5;

​    int b = 7;

​    int c= 2;

​    int d = a>b? a:b;

​    int e = c>d? c:d;

​    System.out.println("abc中的最大值是:"+e);

​    

方法

1.遇到return,程序就会结束，不会再继续往下执行

第五天

格式化输出

不自动换行

System.out.printf()   //format 格式化

\r 回车 将光标置于本行开头 如果继续输出就会覆盖\r前面的内容

System.out.println("ssss\raaa");  输出结果：aaa

%x(hex) 十六进制数 

%d 整数

%f 浮点数  %.2f 保留俩位小数   %7.2f 前面有三个空格   %e 使用科学计数法打印浮点数  %+.2f 打印出符号位

%s 字符串  %1$s 表示第一参数

%% %

if 判断语句

if （.....）{

   。。。。。。。

   }

else{

   。。。。。。。

   }

if （....）{

   。。。。。。。

   }

else if（.....）{

   。。。。。。。

   }

else if（ .....）{

   。。。。。。。

   }

else{

   。。。。。。。

   }

判断浮点数是否相等

浮点数用==判断是不准确的

double d = 1-0.9;

​    if (d == 0.1){

​      System.out.println("计算结果精确");

​    }

​    else{

​      System.out.println("计算结果不准确");

​      System.out.println(d);

​      }

输出结果：计算结果不准确  0.09999999      

Math.abs()  用于返回一个数的绝对值

判断浮点数与一个数是否相等：利用Math.abs() 方法计算浮点数与该数的差值的绝对值，与小数0.00001（误差范围）做比较，小于这个小数就认为俩数相等

double d = 1-0.9;

​    if (Math.abs(d-0.1)<0.000001){

​      System.out.println("计算结果精确");

​    }

​    else{

​      System.out.println("计算结果不准确");

​      System.out.println(d);

​    }

引用类型的判断

== ： 判断是否指向同一个对象

equals() 判断内容是否相等

变量1.equals(变量2)  

如果变量1为null,那么调用equals()会报错

解决办法

1.短路&&

if （变量1 != null && 变量1.equals(变量2) ）

2.把不是null的变量置于变量1的位置

switch 多重选择 （尽量少用，基本可以用其他代替）

switch(表达式){     //表达式只能是整型，字符串，枚举类型  具有穿透性

​    case 1：         //表达式为整型的情况

​         执行语句

​         break;      //在每个case后必须加break语句，否则会一直执行下去，直到遇到break

​    case 2: 

​        执行语句

​        break；

​    default：

​        执行语句   //case 条件都不满足的时候执行default语句   

​                 

}

while 循环

while （表达式）{   //满足表达式就循环，不满足就不进入循环

​      语句执行

}

for循环

1.通过计数器进行循环

2.计数器变量最好放在循环体内

语句结构

for(计数器变量初始化赋值；布尔表达式；布进表达式){  //最好就按照这种结构写，不容易出现错误  布进表达式是用来更新计数器的值 

​      循环体                              //循环体中尽量不修改计数器的值

}

数组长度 利用length关键字

for each 循环

1.可以更简单的遍历数组，和迭代（同一条代码一直重复执行，一直到满足条件为止）数据类型

2.无法指定遍历的顺序，只能从左到右

3.无法获得数组索引

for (int n : 数组名){

​     System.out.println(n);  //n代表数组中的元素

}

break 和continue

第七天

数组

数组

创建数组

默认数据类型  整型：0  浮点型：0.0 字符型：'\u0000'  引用类型：null

数组在创建好后，可以存储的数据量是固定的,后期是无法修改的

1.数组中存放数据的数据类型[] 数组名 = new 数据类型[ 数组长度 ]

int[] num = new int[]; 只定义数组长度

// int[] array = new int[]{数据1，数据2}   int[] 不能写长度

2.数组中存放数据的数据类型[] 数组名 = {数据1，数据2}；

或者 数据类型 数组名[] = {元素1，元素2} ；

length 关键词   计算出数组的长度

数组名.length 

访问数组中的元素

数组名[索引]

为数组中的元素赋值

数组名[索引] = 值

java 中的程序是在jvm中执行的

   java编译器            jvm

.java  ->  .class  ->jvm类加载器 ->执行引擎    在程序执行过程中，数据存储在 运行数据区 中

运行数据区包括：堆内存（用于存放对象和数组） 方法区(存放运行时的类，方法)

数组名变量存放的是数组元素在堆内存中的地址，是16进制地址

String[] array = new String[3];

System.out.println(array);   结果：[Ljava.lang.String;@4554617c

int array1[] = new int[2];

System.out.println(array1);  结果：[I@1b6d3586

arr1把数组在堆内存的地址给了arr2，arr2 数组与arr1指向堆内存中的同一个数组，arr2就可以访问arr1所指向的这个数组

int array2[] = {1,2};

System.out.println(array1);      结果：[I@1b6d3586

int[] array2 = array1;

System.out.println(array2);      结果：[I@1b6d3586

System.out.println(array6[1]);    结果：2

遍历数组

1.for循环 带索引

int[] array = {1,2,3,4};

​    System.out.println(array); //结果是数组在JVM中的引用地址

​    for (int i = 0; i < array.length; i++){

​      System.out.println(array[i]);

​    }

2.for each 不带索引

int[] array = {1,2,3,4};

​    for (int n : array){   //变量n用来接收数组中的元素

​      System.out.println(n);

​    }

快速打印数组元素

Arrays.toString()  需要先导入Arrays类

import java.util.Arrays;

int[] array = {1,2,3,4};

​    System.out.println(Arrays.toString(array));

对数组元素进行排序

1.冒泡排序 对小数组排序

依次比较俩个元素的大小，然后交换

有升序和降序俩种排序方法

2.利用Arrays.sort 对大数组进行快速排序

多维数组

二维数组

int[] [] array = {

{         }，

{        }，

{        }，

}

1.数组中的元素是数组，数组的长度是其所包含的数组个数

2.用Arrays.deepToString() 打印出数组中的全部内容

3.访问二维数组中的元素：数组名[][]

命令行参数

1.是String[] 数组

return 结束return所在方法的所有执行语句欧阳娜娜

参数传递

\1. 方法中创建的基本数据类型变量只在本方法中有效 ，存在于方法栈

2.把引用数据数组传入方法，相当于把数组在堆内存中的地址传入方法

第八天

面向对象

创建的类就相当于对象的一个模型，要使用类中的功能先得创建一个对象实例

new创建的数据都放在堆内存中

对象创建的理解

把一个类的实例赋值给了类 这种数据类型的变量，这个变量就是对象名

新建一个类，类中存放成员变量和方法标记（通过方法标记找到方法栈中的方法），把类在堆内存中的地址赋值给对象（对象的类型是类）

成员变量有默认值，局部变量没有默认值，必须先定义并赋值

创建类

实际上是定义了一种新的数据类型

类：对一类事物的抽象描述

对象：相当于一类事物的一个实例

类中创建方法一般不加static

public class Student类名{

   //成员变量（类的特征，特点）字段  默认修饰词是public

   用private封装成员变量后，外部访问需要通过专门的方法

   String name;

   int age;

   String sex;

   //成员方法 (类的功能)

   public void study(){

   }  

   

创建对象 在主方法中

  Student(类名) s(对象名) = new Student()

  // 通过对象对成员变量赋值

  s.age =

  s.name =

  s.sex =

  System.out.println("s="+s);

  //打印出来时对象的地址值

  

访问变量，通过创建的对象访问

  System.out.println(s.name);

  System.out.println(s.age);   

   public void play(){

}

   

}

方法调用：s.study()

​        s.age()

成员变量的默认值：

整型：0  浮点型：0.0 字符型：'\u0000' 布尔型：false 引用类型：Null

null 空常量

封装：

设置为私有成员变量 用到private关键字

  private String brand;

  private String colour;

获取成员变量要定义一个专门的方法

  public String getBrand(){

​    return brand;

}

设置成员变量的值，也需要定义一个专门的方法

  //定义主方法时，创建变量需要变量类型[] args

  //定义其他方法时，则不需要加[]

  public void setBrand(String brand){

​    this.brand = brand; //为了区别接收变量和成员变量需要用到this关键字

​                    //this.变量名是指对象的变量，是用户成员变量

​                    //而后面这个变量是接收变量

​                     

  }

  

构造方法

在对象创建的同时，构造方法会被默认调用

构造方法的名称必须与类名相同

 //构造方法没有返回值，也不写void

 用于在创建对象的时候初始化成员变量

 构造方法可以定义多个，编译器会根据参数的差异来选择构造方法  

\1. //如果没有创建构造方法，系统会默认创建一个构造方法，没有参数，也没有执行语句

  public 类名（）{

  

  } 

2.//定义无参数的构造方法

  public 类名（）{

   执行语句    

  }

  /**无参数的构造方法创建对象的语法：类名 对象名 = new 类名（n）n表示这个对象数组中有几个对象

  */

  

3.//定义有参数的构造方法

  //语法：public 类名（参数类型 参数名，参数类型 参数名）{}

  //有参数的构造方法创建对象的语法：；；类名 对象名 = new 类名（"华为",1999）

  //可以直接对用户变量进行初始化

  public Phone(String brand,int price){

​    this.brand = brand;

​    this.price = price;

  }

\4. //用private也可以创建私有方法，私有方法需要通过其他方法间接调用

   private void 方法名（）{

   

   }

   

\5. 构造方法中也可以调用其他构造方法，用到的语法是 this() ，this语句在构造方法中必须是第一个语句

6.方法重载 overload

1.在同一个类中，有一个以上方法名相同的方法存在，且它们的参数类型、数量，位置不同

2..方法的是否是重载与方法的修饰词、返回值类型、参数名称无关 

3.重载方法应该完成相同的功能，返回值也应该相同（书写规范）   

Arraylist类

是一个集合，可以存放多个元素，类似于数组

创建ArrayList集合

import java.util.ArrayList;  使用ArrayList之前需要先输入ArrayList类

ArrayList<集合存放的元素类型> 集合名 = new Arraylist<元素类型>（）

//往集合中添加元素 集合名.add(元素)

​    list.add("张文斌");

​    list.add("贺博鑫");

/往集合指定位置添加元素 集合名.add(下标，元素)

​    list.add(0,"李静");

JavaBean 标准类

1.private 变量

2.构造方法

无参的，满参的

3.成员方法

4.get set 方法

API 

Application Program Interface 应用程序接口

需要先创建对象

然后通过对象调用类中的方法

通过对象，调用类的功能方法

类的功能方法需要了解

Scanner 类

在创建对象时，必须传入参数

System.in 键盘录入参数

猜数字练习

BigInteger

创建对象的时候必须传入整数字符串

让大整数做加减乘除，不限制整数的长度，构造方法中采用字符串类型表示整数

四大运算：

语法：

add()

subtract()

multiply()

divide()  

​    BigInteger bigNum1 = new BigInteger("22554896654");

​    System.out.println(bigNum1);    //传入的参数存储在对象名中

​     

​    BigInteger bigNum2 = new BigInteger("23659874123655412");

​    System.out.println(bigNum2);

​    

​    BigInteger add = bigNum1.add(bigNum2); //加法语法，bigNum1调用add方法，方法中传入bigNum2对象参数

​    System.out.println(add);

​    

​    BigInteger sbutract = bigNum2.subtract(bigNum1);   //最后运算结果也要用BigInteger类型的变量来存储

​    System.out.println(sbutract);

​    

​    BigInteger multiply = bigNum2.multiply(bigNum1);

​    System.out.println(multiply);

​    

​    BigInteger divide = bigNum2.divide(bigNum1);//自动取整数部分

​    System.out.println(divide);

BigDecimal 类

实现超大浮点数的准确运算

构造方法中以字符串形式存储浮点数

​    BigDecimal bigDec1 = new BigDecimal("5.3265244");  //对象中存储传入的参数

​    System.out.println(bigDec1);           //结果：5.3265244

​    BigDecimal bigDec2 = new BigDecimal("9.25331425257412");

​    System.out.println(bigDec2);

​    

​    BigDecimal add = bigDec2.add(bigDec1);

​    System.out.println(add);

​    

​    BigDecimal subtract = bigDec2.subtract(bigDec1);

​    System.out.println(subtract);

​    

​    BigDecimal multiply = bigDec2.multiply(bigDec1);

​    System.out.println(multiply);

​    除法语法：对象名.divide(除数对象名，保留几位小数，小数取舍方式)

​    小数取舍方式有三种：BigDecimal.ROUND_UP    BigDecimal.ROUND_DOWN     BigDecimal.ROUND_HALF_UP

​    

​    BigDecimal divide1 = bigDec2.divide(bigDec1,3,BigDecimal.ROUND_UP);//向上取整

​    System.out.println(divide1);

​    BigDecimal divide2 = bigDec2.divide(bigDec1,3,BigDecimal.ROUND_DOWN);//舍去小数

​    System.out.println(divide2);

​    BigDecimal divide3 = bigDec2.divide(bigDec1,3,BigDecimal.ROUND_HALF_UP);//四舍五入

​    System.out.println(divide3);

第九天

继承

代码复用的一种方式

类1包含类2已有的字段和方法，那么类1就可以通过extends关键字继承类2的这些字段和方法，这个类1就获得了类2的所有功能

类2 ：超类super 父类 基类

类1：子类subclass  扩展类

Object 所有类的根类

如果创建类的时候没有写类的父类，那么系统会默认添加Object父类

除了Object外，一个类只能有一个父类

Object中的几个重要方法：

toString() : 把instance(实例) 输出为String

public String toString() {

  执行语句

}

equals(): 判断俩个instance是否逻辑相等

hashCode: 计算一个instance的哈希值

父类中用private修饰的成员变量无法被子类访问

父类中用protected（被保护的）修饰的变量可以被子类访问

构造方法

父类中的构造方法要通过子类中的构造方法来调用

子类构造方法的第一行语句，默认调用super() 代表调用父类中的构造方法

子类默认的构造方法只能调用父类中默认的构造方法

1.调用空参的构造方法super（） 可以不写，默认会调用

2.调用有参数的构造方法：

调用的时候使用super(参数) 将参数传入父类

public Student(String name) {

​    super(name); //父类构造方法中有参数数，子类中调用父类构造方法要传入参数

  }            //一层一层的传递参数

  

组合

一个类中可以声明一个另一个类中的实例

private Book book;

方法覆写 Override

1.方法的返回值，参数，方法名一样，执行语句不一样

2.可以在子类的方法上一行加上 @Override ,可以让编译器帮我们检测是否进行了准确的覆写

子类覆写的方法中也可以调用父类被覆写的方法

语法：super.方法（） 

public void run() {

​    System.out.println("ren");

​    super.run();

  }

实际对象的调用的方法总是其实际类型的方法

People people1 = new Student();

​    People people2 = new People();

​    people1.run() ;  执行的是Student类的run()

​    people2.run();  执行的是People类型的ran()

​    

final关键字

1.用final修饰的方法不能被子类覆写，但可以使用

public final void eat() {

​    System.out.println("人都会吃");

  }

2.用final修饰的类不能被子类继承

public final class Book {

  private String name;

}

在final修饰的类中，用final修饰的此类的对象一旦被赋予实例后，无法被重新赋予实例

final Book book = new Book()

会报错：book = new Book()

3.用final修饰的变量在初始化后不能重写赋值

private final double weight;

抽象类

1.是用来实现多态的

2.无法实例化

3.用于被子类继承

4.子类覆写抽象方法，也可以没有执行语句

5.抽象方法相当于定义了规范

6.非抽象子类必须覆写抽象父类的所有抽象方法

7.可以有抽象方法。也可以有非抽象方法

8.抽象类中可以不包含抽象方法，但包含抽象方法的类，一定是抽象类

父类

9.可以定义成员变量

10.抽象类也可以有构造方法，用于子类创建对象时，初始化父类变量

11.

父类一般会定义为抽象类

public abstract class People {

  public abstract void printName(); //抽象方法不能有身体（大括号），以分号结尾

}

子类

public class Student extends People {

  private String name;

  public Student(String name) {

​    this.name = name;

  }

  public void printName() {

​    System.out.println("name = "+name);

  }

测试类

public class TestClass1 {

  public static void main(String[] args) {

​    People people = new Student("baiyulong"); //给父类对象赋值一个子类实例

​    people.printName();

  }

} 

抽象方法

1.用abstract修饰

2.没有任何执行语句

3.含抽象方法的类也必须声明为抽象类，也是用abstract修饰

面向抽象编程

1.上层代码值定义了规范

2.父类只负责调用子类

3.功能由子类实现

成员变量重名

子类父类变量重名，子类会使用自身的变量

super 和this关键字

this.变量  子类变量

super.变量  父类变量

方法使用方法相同

方法重名

重写后如果需要父类原方法的代码，直接在子类方法中用super调用即可

super() 调用父类中的构造方法

第十天

接口

接口可以定义的内容：

1.常量（一般不需要定义）

接口中的常量默认是由 public static final  修饰的，因此其值一旦定义不可改变

完整定义 ：public static final 变量类型 变量名 = 值

​         public static final 常量类型 常量名 = 值

2.方法(从jdk8开始才可以定义默认方法和静态方法)

静态方法和默认方法一般用于框架设计，平常写程序用不到，尽量不写

抽象方法 public abstract

默认方法  public default

静态方法  public static

类中如何使用接口中的内容：

1.常量和变量  会被其实现类所 继承  通过对象名可以引用

\2.  类中必须重写接口和接口父类中的所有抽象方法

   类要实现的俩个接口中有方法名一样的抽象方法，只需要重写一个

​     

   调用接口的默认方法 ：直接用对象名调用即可，可以继承也可以重写

   类要实现的俩个接口中有方法名一样的默认方法，则必须重写该默认方法

   

  调用接口中的静态方法 ：只能使用接口名调用，不能被重写

接口的定义：

1.接口定义的抽象方法默认修饰词是 public abstract,因此在接口中定义抽象方法时，public abstract 可以省略

2.语法 public interfance 接口名{

​    抽象方法语法： 返回值类型 方法名；

}

3.类实现接口，需要使用implements关键字

语法：

public class 类名 implements 接口1，接口n{

}

4.除了可以定义抽象方法外，还可以定义default方法，defaule方法有身体

语法：

default 返回值类型 方法名（）{

}

继承接口的类不用必须覆写defaule方法就可以实现接口

default方法可直接被继承类调用

5.一个接口也可以继承另一个接口

语法：public interface 接口名 extends 接口名{

}

静态字段和方法

静态字段：

1.用static修饰的字段

2.不同对象所使用的普通字段都有自己独自的存储空间，而静态字段只有一个共享空间，所以对象都共享这段空间

3.实例中并没静态字段，静态字段是用来描述类本身的，在调用静态字段时，推荐需要用 类名.静态字段名

4.静态变量称为类变量,全部对象共享一个静态变量

一般是多个对象具有相同的属性值，那么这个属性就可以设置为静态变量，让多个对象共享这个变量，只占用一个内存，节省内存空间

5.堆内存中存放的是静态变量的静态标记，而静态变量的值存放在方法区中与其所属类放在一起

6.既可以使用对象调用，也可以用类名调用，但一般用类名调用

静态方法：

1.用Static修饰的方法

2.调用静态方法可以通过对象，但最好用类名直接调用

类名.静态方法名（）

3.静态方法只能使用静态变量（用Static修饰的变量），不能使用实例变量（没有用static 修饰的变量）

4.静态方法中只能调用静态方法

5.静态方法常用于工具类,辅助方法

例如：Arrays.sort()

​      Math.random()

​      

静态代码块

类中，方法外，与变量一个级别

随着类的加载而执行且只执行一次，优先于构造方法执行，在类的第一次加载的时候执行一次

static{

   执行语句

}

​      

包

定义：package 包名

1.为了解决类名冲突

2.完整类名：包名.类名

只有包名不同，类就不同

3.class文件中显示的都是完整类名

包作用域：不用public,private,protected,修饰的字段和方法

import

导入类

语法 ：import 完整类名

import java.util.*  导入包下的所有类

引用其他类时有俩种方法

1.直接用完整类名

2.可以先用import导入

定义类名时：

不与java.long下的类重名 例如：String,System,runtime

也不与jdk常用类重名  例如：list,format,BigInteger

作用域

访问权限：在一个类的内部能否访问另一个类的字段和方法

有四种：public protected private package

public修饰的：可以被其他类访问,但得通过创建对象访问

private修饰的：只能在类内部使用

内部类：定义在一个类的内部，用private修饰

protected用于继承类：用protected修饰的字段和方法可以被子类使用

package修饰的

包作用域：指一个类可以访问同一个包下的不用public,private修饰的类，和不用public private protected 修饰的字段和方法

局部变量：方法内的定义的变量

1.方法中传入的变量：从方法传入开始到方法结束

2.方法开头定义的变量：从定义处开始到方法结束

3.循环和判断语句中定义的变量：从定义处开始到循环和判断结束

一个.java文件只能包含一个public class ,但可以包含多个非public class

clssspath 和jar

classpath是一个环境变量，提供搜索路径让jvm去搜索class，classpath设置的搜索路径与操作系统有关

windows上类路径的间隔用; 而mac上类路径之间的间隔用：

如果classpath中有空格，就必须用双引号括起

jar

是一种压缩文件，包含若干.class文件，也相当于一个目录

使用jar包是为了减少大量的目录

创建jar包

使用jdk提供的jar命令

使用构建工具Maven

jvm在运行时会自动加载jdk自带的class文件，因此有些文件不需要设置环境变量

编码

计算机只能表示数字，因此要表示字符，要把字符转换为数字

每个国家都有自己的编码方式，把国语编码为数字，因此各个国家之间会有冲突

Unicode全球统一编码 

一个Unicode字符占用俩个字节，而一个英文通常只需要一个字节，因此当程序中英文过多时会浪费空间

UTF-8 加长编码

英文编码与ASCII编码相同，占用一个字节，其他字符需要2-6个字节不等

字符串和数组进行转换时，优先使用UTF-8编码

StringBuilder类 不需要导入

append() insert() 按索引插入 toString() 返回一个String变量

高效拼接字符串

先创建一个对象

StringBuilder sb = new StringBuilder(1024)

链式操作

StringBuilder sb = new StringBuilder(1024);

​    String s = sb.append("bai")

​        .append("yu")

​        .insert(3,"name")

​        .toString();

​    System.out.println(sb);

​    System.out.println(s);

StringBuffer是StringBuilder的线程安全版本，很少使用    

第十一天

枚举类

定义常量

完整写法

public static final 常量类型 常量名 = 值

enum

通过enum关键字定义常量类型(枚举类),enum关键字其实定义的是class,继承自java.lang.Enum,

但是enum定义的类不能通过new创建实例,每一个常量都是一个实例，属于引用类型

public enum 常量类型 {

​     常量1，常量n;

}

常用工具类

Math类

abs() 求绝对值 / max() / min()

提供了俩个常量：PI = 3.14259.....  E = 2.71828

第十二天

类和接口的关系：类实现接口

类与类的关系：继承

接口与接口的关系：继承

接口也可以继承接口，还可以继承多个接口

如果继承的接口中有相同的默认方法，需要重写

多态

同一种行为，不同的表现形式

实现多态的前提：

1.继承或实现

2.方法重写（如果没有方法重写，多态没有任何意义）

3.父类对象指向了子类实例

子类对象既是子类类型也是父类类型

java实际方法的调用是基于运行时实际类型的动态调用 ，这种动态调用就叫多态

对象运行的方法取决于运行时实际类型的方法

好处：允许添加更多功能的子类来实现功能扩展

如果给父类类型的对象赋值一个子类类型的实例，那么父类类型的对象就可以执行子类中的方法

引用类型转换：

向上转型：父类类型指向子类实例，是安全的

向下转型：子类类型指向父类实例，是强制的，进行转化时，可以先进行判断是否是同一种类型

父类对象可以调用子类覆写父类的方法，如果要调用子类特有的方法，需要向下转型

向上转型

把一个子类型的实例安全的转化为更抽象的父类型的实例

People people3 = student2;  //把一个子类型的对象赋值给父类的对象

instanceof可以判断对象的类型，对象属于哪个类

对象名 instanceof 类名

子类中的对象既属于子类，也输入父类

System.out.println(student2 instanceof People);

System.out.println(student2 instanceof Student);

向下转型

需要强制转型 在要转型的对象前加要转的类名

直接可能会报错

Student student3 = (Student)people2;

可以先用instanceof判断对象的类型

if (people1 instanceof Student) {

​      Student student4 = (Student)people1;

​      

​    }

第十三天

修饰符的访问权限

public 同一类，同一包，不同包的子类，不同包的无关类

protected 同一类，同一包，不同包的子类

default 同一类，同一包

只有在接口中才能使用default修饰方法

在类中，不加修饰词的方法就是默认方法

private  同一类

**成员变量一般用private修饰

**构造方法和成员方法一般用public 修饰

内部类和匿名内部类在编译时都会生成.class文件

内部类（实际开发中几户不用）

类中类

class 外部类{

   class 内部类{

   

   }

   

}

内部类可以直接访问外部类的成员，包括私有成员

外部类要访问内部类的成员，必须通过内部类的对象访问

内部类对象的创建：

外部类名.内部类名 对象名= new 外部类().new 内部类()

外部类名.内部类名 对象名= 外部对象.new 内部类()

Waiclass.Neiclass nei = wai.new Neiclass();

Waiclass.Neiclass nei1 = new Waiclass().new Neiclass();

匿名内部类

接口中的抽象方法仅调用一次，可以用匿名内部类

不新建实现类可以直接实现接口中的抽象方法

内部类的简写

前提：

1.存在一个类或接口

匿名内部类调用方法：

1.相当于创建一个实现类的对象

父类名或接口名 对象名 = new 父类名或接口名（）{

​    方法重写

}；

对象名.方法名（）

2.

new 父类名或接口名（）{

​    方法重写

}.方法名（）；

lambda

jdk8中出现的新语法

对匿名内部类的简化

第十四天

API

Java API是一本程序员的 字典 ，是JDK中提供给我们使用的类的说明文档

API帮助文档：

**API学习步骤：

1.打开帮助文档

2.搜索框可以进行搜索需要的类和接口

3.java.lang下的类不需要导包

4.看类的解释和语法

5.学习构造方法

6.学习成员方法

java的输入

Scanner 键盘输入

1.将java中的库类输入到程序中：import 类所在路径

例：import java.util.Scanner;(放在首行)

2.创建键盘录入：Scanner scanner=new Scanner(System.in);  使用构造方法创建对象，使用的是有参数的构造方法需要传入参数System.in

3.接收键盘录入数据：double 变量名=scanner.nextDouble(); 浮点数接收

​                int 变量名=scanner.nextInt();   整数接收

​                String 变量名=scanner.nextLine()  字符串接收  String str = scanner.next()

​                boolean 变量名 = scanner.nextBoolean();

​             

Random 类

生成伪随机数

1.导入Random类

import java.util.Random;

2.创建Random实例 

Random r = new Random(seed种子);  可以给定一个种子，如果不给定种子系统会使用当前的时间戳作为种子

3.通过实例调用方法

​    random()              生成（0,1）之间的一个伪随机数

​    int i = 对象名.nextInt();   生成整数范围内的随机数

​    int ii = 对象名.nextInt(n))  生成一个[0,n)的随机整数

​    random.nextInt(n) + 1;   生成一个[1,n]的随机整数

​    double d = 对象名.nextDouble()); 

​    boolean b = 对象名.nextBoolean();

​    

​    

SecureRandom类

生成安全的随机数

1.导入类

import java.security.SecureRandom;

2.创建对象

SecureRandom sr = new SecureRandom();

3.使用方法

System.out.println(sr.nextInt(n));

String  

被final修饰的类

常用构造方法：

1.public String();

2.public String(char[] value);

3.public String(byte[] bytes);  将字节数组中的整数用ASKII表转换为字符写入字符串中

4.public String(byte[] bytes, int offset, int length) 将字节数组中从指定索引开始到指定长度的字节转换为字符串

String Str = "sss" 最常用

**俩种创建字符串对象的存储方式不同

1.String Str = "sss" 如果字符串的值相同，字符串是指向同一个地址值的

2.通过构造方法创建的对象，每一个对象对应一个地址值

常用方法

*****使用String方法后都会生成一个新的字符串

判断功能的方法：

1.equals()

2.equalsIgnoreCase() 忽略大小写

字符串的比较：==和equals的不同

1.==比较基本数据类型，比较的是具体的值

  ==比较引用数据类型，比较的是对象地址值

2.equals() 比较String类型，比较的是对象的内容是否相同  

  

获取功能的方法：在帮助文档中找一遍

1.length 返回字符串长度

2.concat（）连接俩字符串

3.charAt(索引) 返回索引处的char值

  char(s.length-1) 返回最后一个char值

4.indexOf(String) 返回字符串第一次出现的索引位置，如果没有返回-1

5.subString(int) 从指定位置开始到末尾返回一个子串

  subString(int m,int n) 返回从m开始到n-1结束的子串

转换功能的方法

1.toCharArray() 将字符串放到字符数组中

2.getBytes() 将字符串中的字符用AskIIS码转换为字节整数，放到字节数组中

3.replace()

replace(char,char) 将字符串中的一个字符转换为另一个字符

replace(String,String)  将字符串中的子串转换为另一个子串

分割功能的方法：

1.split() 将字符串按照给定的规则（字符中的）切割成字符串数组

String str4 = "h,e,l,l,o,w,o,r,l,d";

String[] strings = str4.split(",");

1.contains() 方法 查看一个字符串中是否包含另一个字符串

语法：字符串.contains(字符串)

\2. indexOf（）返回子串的索引位置 从前向后找

  lastIndexOf() 从后往前找

3.startsWith() 查看字符串是否由某个字符串开始

  endsWith()  查看字符串是否由某个字符串结束 

4.trim（） 移除首尾空白字符（空格 \t \n \r） 返回一个新字符串 trim 修整

5.substring() 提取一个子串

substring(n) 从下标为n开始提取

substring(n,m)  提取n 到m-1的串

6.toUpperCase() 将字符串全部转换为大写

 toLowerCase() 将字符串全部转换为小写

8.String join() 拼接字符串

语法：String.join("",可迭代对象或者多个单字符串)

第一个双引号中放的是字符串之间的间隔符

9.String.valueOf() 将任何类型转换为字符串

instanceof 关键字 判断变量类型是否是字符串类型

语法：要判断的变量 instanceof String

stem.out.println(String.valueOf(123) instanceof String);

10.Integer.parseInt(String)  将字符串转换为整型 parse 解析

字符串拼接：

对字符串进行拼接操作，每次拼接，都会构建一个新的String对象，既耗时，又浪费空

Object

java.lang.Object 类是Java语言中的根类，每个类都使用 Object 作为超类。所有对象（包括数组）都实现这个 类的方法。

如果一个类没有特别指定父类， 那么默认则继承自Object类

有native修饰的方法是本地方法，一般是由c++语言编写的

此方法中只有一个静态代码块，静态代码块中调用此方法

因此此方法一被调用静态代码块就会执行，调用此方法，这样就实现了java调用C的操作

private static native void registerNatives();

  static {

​    registerNatives();

  }

Object中的常用方法：

1.toString

直接打印对象名默认会调用Object类中的toString方法，得到的是完整类名和对象在内存中的16进制地址

Object类中的toString方法： public String toString() {

​                             return getClass().getName() + "@" + Integer.toHexString(hashCode());

}

People people = new People();

​    System.out.println(people);

相当于 System.out.println(people.toString());

重写toString方法：打印类的成员信息，返回一个字符串

public String toString() {

​    return "People{"+"name = "+name+','+"age = "+age+'}';

  }

重写toString方法后打印对象名会调用新的toString方法

2.equals()

内部是用==做比较的，比较是是俩个对象的地址

源码：public boolean equals(Object obj) {

​             return (this == obj);

​    }

如果要比较俩个对象的内容，需要重写equal()方法

public boolean equals(Object o) {

​    if (this == o) return true;

​    if (o == null || getClass() != o.getClass()) return false;

​    People people = (People) o;

​    return age == people.age &&

​        Objects.equals(name, people.name);

  }

Date

java.util.Date 类 表示特定的瞬间，精确到毫秒。1000毫秒等于1秒

构造方法

1.public Date()

Date date = new Date();

​    System.out.println("date = " + date); //对toString方法进行了重写

​    结果：date = Sun Jul 05 16:51:03 CST 2020

2.public Date(long date)

Date date1 = new Date(0);

​    System.out.println("date1 = " + date1); //打印的是计算机的起始时间

​    结果：date1 = Thu Jan 01 08:00:00 CST 1970

常用方法：

1.public long getTime() 把时间日期转换成对应的时间毫秒值。

long L = date.getTime();

​    System.out.println("L = " + L);

​    结果：L = 1593939881012

2.public void setTime(long time) 把方法参数给定的毫秒值转换成时间日期

date1.setTime(1593939697455L);

​    System.out.println("date1 = " + date1);

​    结果：date1 = Sun Jul 05 17:01:37 CST 2020

DateFormat 抽象类

对日期进行格式化，转化中国的日期表现形式

需要通过其子类SimpleDateFormat中的构造方法来创建实例  运用了多态

public class SimpleDateFormat extends DateFormat{}

构造方法：

public SimpleDateFormat(String pattern)  pattern:日期的格式

标识字母（区分大小写） 含义

y   年

M  月

d  日

H  时

m  分

s  秒

常用方法：

1.String format(Date date)  传 入日期对象，返回格式化后的字符串。

Date date = new Date();

​    DateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss"); //传入日期的显示格式

​    String s = dateFormat.format(date); //传入的是日期对象，返回的是字符串

​    System.out.println("s = " + s);  结果：s = 2020-07-05 18:06:11

2.Date parse(String str）   传入字符串，返回日期对象。

使用解析方法时，需要声明可能出现的解析错误

public static void main(String[] args) throws ParseException {  //声明可能出现的解析错误

​    DateFormat dateFormat1 = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss"); //此处个日期格式要与parse()方法中传入的格式相同，否则会出翔解析错误

​    Date date1 = dateFormat1.parse("2020-07-05 18:01:06");

​    System.out.println("date1 = " + date1);     结果：date1 = Sun Jul 05 18:01:06 CST 2020    

  }

Calendar日历类

作用： java.util.Calendar 是日历类，在Date后出现，替换掉了许多Date的方法。该类将所有可能用到的时间信息封装 为静态成员变量，方便获取。日历类就是方便获取各个时间属性的。

成员变量皆为静态成员变量，可以通过类名进行调用

通过调用getInstance()创建Calendar对象  //getInstance()方法中调用其创建对象

public static Calendar getInstance()；//getInstance()是静态方法

Calendar calendar = Calendar.getInstance();

常用的方法：

1.public int get(int field) ：返回给定日历字段的值

int year = calendar.get(Calendar.YEAR);

​    System.out.println("year = " + year);

​    int i = calendar.get(Calendar.MONTH ) + 1;//打印月份是从0开始的，需要进行加1打印真实月份

​    System.out.println("i = " + i);

​    int i1 = calendar.get(Calendar.DAY_OF_MONTH);

​    System.out.println("i1 = " + i1);

​    int i2 = calendar.get(Calendar.DAY_OF_WEEK ) - 1;//从周日开始，可以-1使用，打印出星期几

​    System.out.println("i2 = " + i2);

2.public void set(int field, int value) ：将给定的日历字段更改为特定的值。

calendar.set(Calendar.YEAR,2021);  //给一个字段设置值，无返回值

​    int i3 = calendar.get(Calendar.YEAR);

​    System.out.println("i3 = " + i3);

​    

   ***  calendar.set(2010,2,1); //0代表1月，1代表2月，以此类推  依次设置年月日

​    

3.public abstract void add(int field, int amount) ：根据日历的规则，为给定的日历字段添加或减去指定的时间量。

calendar.add(Calendar.MONTH,1);  //给月加1

​    int i4 = calendar.get(Calendar.MONTH);

​    System.out.println("i4 = " + i4);

​    calendar.add(Calendar.MONTH,-1); //给月减一

​    int i5 = calendar.get(Calendar.MONTH);

​    System.out.println("i5 = " + i5);

4.public Date getTime() ：返回一个表示此Calendar时间值（从历元到现在的毫秒偏移量）的Date对象

Date date = calendar.getTime();

​    System.out.println("date = " + date);

Calendar类中提供很多静态成员，直接类名调用，代表给定的日历字段：

字段值            含义

YEAR            年

MONTH          月（从0开始，可以+1使用）

DAY_OF_MONTH   月中的天（几号）

HOUR           时（12小时制）

HOUR_OF_DAY    时（24小时制）

MINUTE         分

SECOND         秒

DAY_OF_WEEK    周中的天（周几，周日为1，可以-1使用）

基本类型包装类

包装类中默认值都为Null

像对象一样操作基本类型

基本类型  对应的包装类（位于java.lang包中）

byte     Byte

short    Short

**int      Integer 

long     Long

foat     Float

double  Double

**char    Character

boolean  Boolean

Integer(int 包装类)

*****Integer对象在使用时与Int类型使用一样，其中包含了自动装箱和自动拆箱

包装一个对象中的原始类型 int 的值

构造方法：

前二个是根据构造方法创建对象，已过时

1.public Integer(int  value) 根据 int 值创建 Integer 对象(过时)

Integer integer = new Integer(100);

2.public Integer(String s) 根据 String 值创建 Integer 对象(过时)

Integer integer1 = new Integer("100");

3,4是调用类中的静态方法创建对象

3.public static Integer valueOf(int i) 返回表示指定的 int 值的 Integer  实例

Integer integer2 = Integer.valueOf(100);

4.public static Integer valueOf(String s) 返回一个保存指定值的 Integer 对象 String

Integer integer3 = Integer.valueOf("100");

*****5.直接给对象赋值，最常用

Integer integer4 = 100;

常用默认方法：

1.parseInt(String s)   将字符串参数解析为带符号的十进制整数。  

  parseUnsignedInt(String s)  将字符串参数解析为无符号十进制整数。

装箱与拆箱

装箱：从基本类型转换为对应的包装类对象。

​    Integer integer = Integer.valueOf(4); //将int类型装箱到Integer对象中

****    Integer integer1 = 5;         //将int类型自动装箱到Integer对象中

拆箱：从包装类对象转换为对应的基本类型。

int i = integer.intValue();  //integer是Integer对象

自动装箱与自动拆箱

Integer integer2 = 6;  自动装箱。相当于Integer i = Integer.valueOf(6);

******integer2 = integer2 + 1;  等号右边：将integer2对象转成基本数值(自动拆箱) i.intValue() + 5; //加法运算完成后，再次装箱，把基本数值转成对象。

StringBuilder

java.lang.StringBuilder

是个字符串的缓冲区，即它是一个容器，容器中可以装很多字符串。并且能够对其中的字符串进行各种操作。

它的内部拥有一个数组用来存放字符串内容，进行字符串拼接时，直接在数组中加入新内容

构造方法：

1.public StringBuilder() ：构造一个空的StringBuilder可变字符串容器

2.public StringBuilder(String str)

常用方法

1.public StringBuilder append(...) ：添加任意类型数据的字符串形式，将返回值赋给当前对象自身。

例： builder.append("ssss").append("aaaaaa");

2.public StringBuilder reverse() ：返回反转的字符序列

3.public String toString() ：将当前StringBuilder对象转换为String对象。

System

java.lang.System

System类包含几个有用的类字段和方法,它不能被实例化,直接用类名调用

常用方法：

1.public static void exit(int status)  终止当前运行的 Java 虚拟机，非零表示异常终止

2.public static long currentTimeMillis()  返回当前时间(以毫秒为单位)

3.public static void arrayCopy(Object src, int srcPos, Object dest, int destPos, int length)    从指定源数组中复制元素到另一个数组

​                       （源数组，源数组索引，目的数组，索引，复制的元素个数）

4.public static void gc()  JVM将从堆内存中清理对象，清理对象的同时会调用对象的finalize()方法

Arrays类

所有 方法均为静态方法

常用方法：

1.public static void sort(int[] a) 对指定的int数组进行升序排列

2.public static int binarySearch(int[] a,int key) 对数组进行二分查找法

如果数组中有此元素，则返回此元素的索引，找不到元素返回(-插入点)-1 

***在使用此方法前，必须对数组进行排序 

3.public static String toString(int[] a) 将数组以字符串形式输出，可以实现快速打印数组中的元素

Math类

所有 方法均为静态方法

1.public static int  abs(int a) 返回参数的绝对值

2.public static double ceil(double a) 向上取整，返回大于或等于参数的小double值，等于一个整数

3.public static double ?oor(double a) 向下取整，返回小于或等于参数的大double值，等于一个整数

4.public  static int round(?oat a) 按照四舍五入返回接近参数的int

第十五天

集合

对象数组：存储了引用数据类型的数组称为对象数组

数组的弊端

1.数组长度是固定的，一旦创建不可修改。

2.需要添加元素，只能创建新的数组，将原数组中的元素进行复制。

Collection接口（单列集合）

集合：集合是java中提供的一种容器，可以用来存储多个数据。

集合和数组的不同：

1.数组的长度是固定的。集合的长度是可变的。

2.数组中存储的是同一类型的元素，可以存储任意类型数据。

集合存储的都是引用数据类型，如果想存储基本类型数据需要存储对应的包装类型。

接口类的继承体系

Collection（结合类顶层接口）（单列集合）:

​                      list（接口）可以存储重复的数据:  ArrayList（实现类）

​                                                LinkedList（实现类）

​                      set（接口）不能存储重复的数据：HashSet:

​                                                      LinkedHashSet

​                                          

Map接口（双列集合）:  HashMap:

​             LinkedHashMap             

​         ConcurrentHashMap:

​         

Collection中的常用方法（子接口和子接口的继承类都可以的使用的方法）：

方法返回值要留意

public boolean add(E e)：把给定的对象添加到当前集合中

boolean boo = collection.add("aa");

public boolean addAll(Collection<? extends E>)将另一个集合元素添加到当前集合中

boolean b = collection1.addAll(collection); 把集合collection中的元素全部添加到集合collection1中

public void clear() :清空集合中所有的元素

collection.clear(); 无返回值

public boolean remove(E e): 把给定的对象在当前集合中删除

boolean aa = collection.remove("aa");

public boolean contains(Object obj): 判断当前集合中是否包含给定的对象

boolean boo1 = collection.contains("aaa");

public boolean isEmpty(): 判断当前集合是否为空

boolean boo2 = collection.isEmpty();

public int size(): 返回集合中元素的个数

int a = collection.size();

public Object[] toArray(): 把集合中的元素，存储到数组中

Object[] s = collection.toArray();

集合的遍历：

1.迭代器

Iterator接口 （collection接口的父类）

并发修改异常

在使用迭代器遍历集合中，不能改变集合的长度，一旦改变就会抛出异常

获取迭代器的方法：使用接口对象调用iterator()方法

public Iterator iterator(): 获取集合对应的迭代器，用来遍历集合中的元素的。

Collection<String> collection = new ArrayList<String>();

​    collection.add("add");

​    collection.add("aaa");

​    Iterator<String> iterator = collection.iterator();  

​    while (iterator.hasNext()) {                 //迭代器的hasNext()方法从o索引开始判断集合中是否有元素，按照索引依次判断

​      String next = iterator.next();              //next()按照索引依次输出集合中的元素

​      System.out.println(next);

​    }

2.for循环

*****3.增强for循环：用于数组的遍历和集合的遍历

底层是迭代器，因此也不能进行增删操作

数组遍历

for (元素类型 元素名（创建变量接收数组合集合中元素）：集合名和数组名) {

​    System.out.println(元素名)；     

}

for (String s: collection) {

​      System.out.println("s = " + s);  //底层运用了迭代器遍历

​    }

​    

数据结构：

1.栈：入口和出口都在栈顶，先进后出，从栈顶开始存储数据，依次往下压，最开始的在最下面，仅允许在标的一端进行插入和删除操作

压栈：就是存元素

弹栈：就是取元素

2.队列：入口-出口分别在俩端，先进先出，仅允许在表的一端进行插入，而在表的另一端进行删除

3.数组（Arraylist接口实现类运用的数据结构）：

增加元素和删除元素比较麻烦，查询元素比较快，可根据索引快速查询

​           

4.链表（LinkedList）：

把多个节点链接

节点：有数据域和指针域组成

有单向链表和双向链表

增加和删除元素比较方便

List集合

特点：

1.是有序的集合，存储和取出的顺序一致

2.允许存放重复的元素

3.每个元素都具有索引

特有方法

1.public void add(int index,E element)在列表的指定位置上插入元素

list.add(1,"ccc"); 无返回值

2.public E get(int index)返回列表中指定位置的元素。

String s = list.get(1); 返回获取到的元素

3.public E set(int index,E element)用指定元素替换列表中指定位置的元素，并返回替换前的元素。

*****String aaa = list.set(0, "dddd"); 返回更改前的元素

4.public E remove(int index)移除列表中指定位置的元素，并返回被移除之前的元素。

String remove = list.remove(1);  返回移除的元素

5.public E remove(E element) 删除某个指定元素

6toArray() 返回一个Object类型的数组，将集合装换为数组

 toArray()

LinkedList

特有的方法：

对第一个元素和最后一个元素进行操作

1.public void addFirst(E e):将指定元素插入此列表的开头。

2.public void addLast(E e):将指定元素添加到此列表的结尾。

3.public E getFirst():返回此列表的第一个元素。

3.public E getLast():返回此列表的最后一个元素。

4.public E removeFirst():移除并返回此列表的第一个元素。

5.public E removeLast():移除并返回此列表的最后一个元素

set接口下的集合：

不能存储重复元素

遍历：迭代器和增强for循环

***HashSet集合：

1.HashSet底层数据结构是单向哈希表

2.元素添加顺序和元素存储顺序不同（与底层存储结构有关）

****3.此集合不允许存储重复元素，因此需要重写存储对象类中的hashCode和equals方法

String类中重写了hashCode和equals方法，因此存入String类型时，可以不用重写hashCode和equals方法

存储自定义类型时，需要重写hashCode和equals方法，才能保证集合中不存储重复元素

判断俩个对象内容是否相等，比较的是成员变量的值

4.具有数组，链表，红黑树（特殊二叉树）三种结构特点

5.只能用加强for循环和迭代器遍历

哈希表（待理解）:

1.哈希值不同的存在数组中，哈希值相同比较成员变量的值，不同的话存储在链表中，每一个链表都存储在一个数组元素中

2.当链表长度超过8后，链表会转换成红黑树

3.哈希表的初始化容量，数组长度为16个，当数组容量不够时，扩容为原数组长度的2倍，指当数组的容量被使用到长度的75%时，进行扩容。

LinkedHashSet集合（HashSet的子集合）：

可以判断元素添加的前后顺序：双层链表数据结构

Map接口(双列集合)：

成对出现的数据

值可以有重复，键不能重复

常用方法：

1.public V put(K key, V value): 把指定的键与指定的值添加到Map集合中。

若指定的键(key)在集合中没有，则没有这个键对应的值，返回null，并把指定的键值添加到集合中；

若指定的键(key)在集合中存在，则返回值为集合中键对应的值（该值为替换前的值），并把指定键所对应的值，替换成指定的新值

在不改变键的情况下改变值，可以用这种添加方式

2.public V remove(Object key): 把指定的键所对应的键值对元素在Map集合中删除，返回被删除元素的值。

3.public V get(Object key)根据指定的键，在Map集合中获取对应的值。

4.public Set<K> keySet(): 获取Map集合中所有的键，存储到Set集合中。

5.public Set<Map.Entry<K,V>> entrySet(): 把Map集合中键值对封装成一个Entry对象，存储到Set集合

6.public boolean containKey(Object key):判断该集合中是否有此键

  public boolean containsValue(Objece value) :判断集合中是否由该值

7.public Collection<V> values()返回Map集合中的所有值到Collection集合

Entry接口

1.是Map中的内部接口

2.常用方法：

getKey()

getValue()

*Map集合的遍历

1.键找值

keySet()

增强for循环

get()

HashMap<Integer,String> hashMap = new HashMap<>();

Set<Integer> set = hashMap.keySet();

​    for (Integer integer : set) {

​      String s = hashMap.get(integer);

​      System.out.println(integer+"="+s);

​    }

2.通过键值对找键和值

entrySet()  把键值对封装成一个Entry对象放到set集合中

使用Map.Entry对象中的getKey()和getValue()

Set<Map.Entry<Integer,String>> set1 = hashMap.entrySet();

​    for (Map.Entry<Integer,String> mapentry:set1) {

​      Integer key = mapentry.getKey();

​      String value = mapentry.getValue();

​      System.out.println(key+"="+value);

​    }

HashMap集合：

键为自定义类型时，不重写俩方法时键相同时，，后面的值会替代前面的值

LinkedHashMap:

添加元素顺序和存储元素顺序相同

可变参数：

1.如果我们定义一个方法需要接受多个参数，并且多个参数类型一致,可以定义一个可变参数

2.可变参数的本质是数组，不传递参数，数组的长度是0,传递几个参数，数组的长度就是几

3.一个方法中只能有一个可变参数。如果方法中有多个参数，可变参数只能写在最后一位。

public class Test6 {

  public static void main(String[] args) {

​     getSum(1,2,3,4,6);

  }

  public static int getSum(int... arr) {

​    int sum = 0;

​    for (int i : arr) {

​      sum += i;

​    }

​    System.out.println(sum);

​    return sum;

  }

}

向collection接口下的集合批量添加元素

Collections类

public static <T> boolean addAll(Collection<T> c, T... elements)

addAll()方法 用的是可变参数

泛型

1.如果没有给集合中的传入的数据类型做指定即没有指定泛型时，那么传入的元素会默认提升为Object类型

2.泛型可以理解为一种新的数据类型，代表的是引用类型中的任意一种

3.***由于集合中可以存放各种类型的引用对象，但是一般集合中放同一种类型的对象，因此可以通过设置泛型来规定集合可以存储的引用对象的类型，保证集合中多存储的是同一种类型的对象

4.定义时候不具体，使用的时候确定泛型的具体类型

5.定义一种不确定的数据类型，使用这种数据类型可以进行其他数据类型进行的一系列操作，在使用变量的时候为泛型赋予真实的数据类型

根据传入的值确定值的数据类型

集合中的泛型

1.不加泛型默认存放的Object类型的元素

2.<> 设定集合中存储的数据类型，只能是引用数据

类泛型：

在创建对象的时候确定泛型的类型

public class Student<e> {}

Student<String> student = new Student<String>("bbbb",21);

泛型方法：

根据传入的参数确定泛型的类型

public class Dog {

  public <e> e run(e name) {

​    return name;

  }

}

​    Dog dog = new Dog();

​    String aaa = dog.run("aaa");

​    Integer run = dog.run(123);

​    Double run1 = dog.run(12.3);

泛型接口：

public abstract interface Interfance<e>{}

1.在创建实现类的时候确定泛型的类型

public class Implement<String> implements Interfance<String>

2.在创建对象的时候确定泛型的类型

Implement<String> implement = new Implement<String>();

泛型通配符：

1.<?>

2.泛型的上限

<? extends 类>

只能接收该类型和其子类的对象

3.泛型的下限

<? super 类>

只能接收该类型的和其父类的对象

第十六天

异常：

Throwable类中的方法：

1.public String getMessage() 打印出异常的描述信息

2.pulic void printStackTrace()  打印出异常的所有信息

Throwable（异常的根类）：Error Error是指发生了严重错误，与程序无关

​                     Exception(例外) Exception是指运行时发生了逻辑错误，可以进行处理

​                                 Exception下有俩种子类异常：编译异常（checked） 必须解决的

​                                 运行异常（runtime）只需要声明异常，可以不解决

1.异常是class,本身带有类型信息

2.异常可以任何地方抛出

3.产生异常就是创建一个异常对象并抛出异常对象

5.使用try {} catch() {} 捕获异常

try {

  可能出现异常的语句

  执行语句

} catch（错误类型 e）{    catch语句中也可以放多个异常类型，用或 | 逻辑运算隔开

  System.out.println(e)    异常1 | 异常2

  执行语句

  

} catch（错误类型 e）{

  System.out.println(e)

  e.printStackTrace()   //打印出方法的调用栈（即异常所处的包中的具体位置）

  执行语句

catch语句只会执行一个，因此子类异常要放在父类异常前面  

}  finally {

  执行语句

}

**finally 语句可有可无，不论有无异常出现总是最后执行

6.声明异常：可延后捕获，或不捕获

throws 异常类型 {

​    异常语句

}

7.抛出异常语法：throw new 异常名（参数）

***自定义异常：

1.创建编译异常 继承Exception  必须进行捕获

2.创建运行异常 继承RuntimeException 在方法中声明异常即可，可捕获可不捕获

重写父类中的空参构造方法和传入字符串的构造方法，并在此构造方法中调用父类构造方法

public class Practice2 extends RuntimeException {

  public Practice2() {

  }

  public Practice2(String message) {

​    super(message);

  }

}

看到第四节

第十七天

IO流(文件字节流 字节缓冲流)

File类

1.主要用于文件和目录的创建、查找和删除等操作

2.File类将文件，文件夹和路径封装成了对象，提供大量方法来操作这些对象

3.一个File对象代表硬盘中实际存在的一个文件或者目录

\4. 无论该路径下是否存在文件或者目录，都不影响File对象的创建

构造方法：

\\ 表示一个\

1.public File(String pathname)：传入文件路径名字符串

​    String pathName = "D:\\practice\\a1.txt";

​    File file = new File(pathName);

2.public File(String parent, String child)：传入父路径名字符串和子路径名字符串

3.public File(File parent, String child)：传入代表父抽象路径名的file对象和子路径名字符串

常用方法：

1.public String getAbsolutePath()：返回此File的绝对路径名字符串。

2.public String getPath()：将File对象转换为路径名字符串，是相对路径

3.public String getName()：返回由此File表示的文件或目录的名称。

4.public long length()：返回由此File表示的文件的长度。（以字节为单位）

5.public File getParentFile()返回父目录，若没有父目录，则返回Null

6.public boolean exists() 测试此抽象路径名表示的文件或目录是否存在。

***绝对路径和相对路径：

绝对路径：从盘符开始的路径，这是一个完整的路径，绝对路径具有唯一性。

相对路径：相对于项目目录的路径，这是一个便捷的路径，开发中经常使用

IO流

把这种数据的传输，按照流动的方向，以内存为基准，分为输入input和输出output，即流向内存是输入流，流出内存的输出流

IO的分类

1.根据数据的流向分为：输入流和输出流。（内存到硬盘，硬盘到内存）

输入流：把数据从其他设备上读取到内存中的流。输出流：把数据从内存中写出到其他设备上的流。

2.根据数据的类型分为：字节流和字符流。

字节流：以字节为单位，读写数据的流。字符流：以字符为单位，读写数据的流

***3.对非文本文档进行操作用字节流，对文本文档进行操作用字符流

文本文档：使用记事本打开不乱码的就是文本文档

4.任何文件本身都是以二进制存储的

IO流顶层父类

对文件本身操作

1.java.io.OutputStream字节输出流顶层父类，抽象类，定义了写出数据方法write

2.java.io.InputStream字节输入流顶层父类，抽象类，定义了读取数据方法read()

对文件内容进行操作

3.java.io.Writer字符输出流顶层父类，抽象类，定义了写出数据方法write()。

4.java.io.Reader字符输入流顶层父类，抽象类，定义了读取数据方法read()

字节Io流

1.字节流可以传输任意文件数据（以二进制形式保存的）

2.对文件本身操作

3.一切数据都是以二进制存储的

**OutputStream字节流输出抽象类

字节输出流的基本共性功能方法

1.public void close()：关闭此输出流并释放与此流相关联的任何系统资源。关闭文件

2.write(int b)方法，每次可以写出一个字节数据 ，传入字符对应的AsKll码值

3.public void write(byte[] b)：将字节数组写入此输出流

4.public void write(byte[] b, int off, int len） 从第off索引开始，写入len个字符

**写完数据后必须调用用close（）方法关闭输出流

FileOutputStream 文件字节输出流子类

构造方法

当你创建一个流对象时，必须传入一个文件路径。该路径下，如果没有这个文件，会创建该文件。如果有这个文件，会清空这个文件的数据

覆盖式写入构造方法：

创建一个覆盖式写出的字节输出流对象

1.public FileOutputStream(File file)：写入由指定的 File对象表示的文件。

2.public FileOutputStream(String name)：传入指定的文件名称

如果不指定文件父目录，默认是项目目录

数据追加续写：

创建一个追加式写出的字节输出流对象

1.public FileOutputStream(File file, boolean append)：传入一个布尔类型的变量true 表示追加式写入

2.public FileOutputStream(String name, boolean append)：传入一个布尔类型的变量true 表示追加式写入

InputStreamjava 字节输入流抽象类

方法：

1.public void close()：关闭此输入流并释放与此流相关联的任何系统资源。

2.public abstract int read()：读取数据的一个字节，从文件开始字节读取，一个字接一个字节读取

***返回字符对应的字符集中的值，字节读取完后，返回-1  

while循环输入

3.public int read(byte[] b)：每次读取数组长度个字节

while循环输入

new String（数组名，开始索引，长度）

改造方法：

main方法中变量不需要初始化

FileInputStream类 字节输入流子类

构造方法：

1.FileInputStream(File file)：通过打开与实际文件的连接来创建一个 FileInputStream ，该文件由文件系统中的 File对象 file命名。

2.FileInputStream(String name)：通过打开与实际文件的连接来创建一个 FileInputStream ，该文件由文件系统中的路径名 name命名。

****文件复制：

1.创建输出流对象（把文件从内存中写出）和输入流对象（把文件读入到内存）

2.使用while循环先把文件读入到内存，再把文件从内存中写出

3.关闭输出流和输入流

把D:\\byljavaprogram\\tupain.jpg这个文件复制到tupiaocopy.jpg文件（默认放在模块目录下）中

​    InputStream inputStream = new FileInputStream("D:\\byljavaprogram\\tupain.jpg");

​    OutputStream outputStream = new FileOutputStream("tupiaocopy.jpg");

​    byte[] bytes = new byte[1024]; // 每次写出1KB或1KB的整数倍

​    int len;

​    while ((len = inputStream.read(bytes)) != -1) {

​      outputStream.write(bytes);

​    }

​    outputStream.close();

​    inputStream.close();

字节缓冲流

1.针对基础流对象进行高效处理的流对象。或者为基础流增加功能。

2.在使用缓冲流时，必须传递基础流

3.缓冲流比普通流复制更快

4.在使用缓冲流时，必须传入普通流

字节缓冲输出流

BufferedOutputStream(继承OutputStream)

构造方法：

public BufferedOutputStream(OutputStream out) ： 创建一个新的缓冲输出流。

字节缓冲输入流

BufferedInputStream(继承InputStream)

构造方法：

public BufferedInputStream(InputStream in) ：创建一个 新的缓冲输入流。

使用缓冲流复制文件

​    Long start = System.currentTimeMillis();

​    BufferedInputStream bufferedInputStream = new BufferedInputStream(new FileInputStream("D:\\byljavaprogram\\book.pdf"));

​    BufferedOutputStream bufferedOutputStream = new BufferedOutputStream(new FileOutputStream("bookcopyy.pdf"));

​    

​    //用数组进行读取

​    byte[] bytes = new byte[1024];

​    while ((bufferedInputStream.read(bytes)) != -1) {

​      bufferedOutputStream.write(bytes);

​    }

​    //单个字节读取

​     byte[] bytes = new byte[1024];

​    while ((bufferedInputStream.read(bytes)) != -1) {

​      bufferedOutputStream.write(bytes);

​    }

​    

​    bufferedInputStream.close();

​    bufferedOutputStream.close();

​    Long end = System.currentTimeMillis();

​    long run = end - start;

​    System.out.println(run);

字符IO流

1.转换流 字符流 字符缓冲流 打印流

2.字符流本身作用是转换字节和字符，调用字节流进行输入和输出

3.编码表和解码表要相同

字符集

1.也叫编码表

2.常见字符集有ASCII字符集（ASCII编码）、GBK字符集（GBK编码）、Unicode字符集（UTF-8编码）等

3.设计到字符和字节之间的转换时需要用到编码表

OutputStreamWriter 转换流

原理：字符输出流将输出的字符通过编码表转换成字节，把字节给了字节输出流，字节输出流调用write（）将字节写入到文件中

1.java.io.OutputStreamwriter类，继承Writer类，他是字符输出流，用于操作文本文件

2.使用指定的字符集将字符编码为字节

构造方法

如果不传入编码表就使用系统默认的编码表

1.OutputStreamWriter(OutputStream  in): 需要传入一个字节输入流对象

2.OutputStreamWriter(OutputStream in,String  charsetName): 传入字节输入流对象和编码表

常用方法

1.void write(int c) 写出单个字符。

2.void write(char[] ch) 写出字符数组。

3.void write(char[] ch,int off,int  len) 写出字符数组一部分，开始索引和写出的个数，写出的数据从开始索引后一个字符开始

4.void write(String s) 写出字符串

**5.void flush() 刷新该流的缓冲，字符流写数据会先写在内存中，刷新后才会到达目的文件

每写出一次，就需要调用一次flush()刷新缓冲流

InputStreamReader 转换流

原理：字符输入流将输入的字符通过编码表转换成字节，把字节给了字节输入流，字节输入流调用read（）将字节从文件中读到内存

1.java.io.InputStreamReader类，继承Reader类，他是字符输入流，只能操作文本文件

2.字节流转成字符流，使用指定的字符集将字符编码为字节

构造方法

如果不传入编码表就使用系统默认的编码表

1.InputStreamReader(InputStream in): 创建一个使用默认字符集的字符流。

2.InputStreamReader(InputStream in,String charsetName): 创建一个指定字符集的字符流

方法

1.int read() 读取单个字符，读取到文件末尾时返回-1。

2.int read(char[] ch)  读取字符存储到数组中个，返回读取到的字符个数，读取到文件末尾时返回-1

***字符流便捷类

不能传入编码表只能使用开发工具默认的编码表

FileWriter  继承OutputStreamWriter，使用平台默认编码表写出数据

构造方法：

1.FileWriter(File file)：创建一个新的 FileWriter，给定要读取的File对象。

2.FileWriter(String fileName)：创建一个新的 FileWriter，给定要读取的文件的名称。

3.FileWriter(String fileName，boolean boo）追加写入

FileReader 继承InputStreamReader，使用平台默认编码表读取数据

构造方法

1.FileWriter(File  file)：创建一个新的 FileWriter，给定要读取的File对象。

2.FileWriter(String  fileName)：创建一个新的 FileWriter，给定要读取的文件的名称。

字符缓冲流

构造方法

1.public BufferedReader(Reader in)：创建一个新的缓冲输入流

2.public BufferedWriter(Writer  out)：创建一个新的缓冲输出流

特有方法：

1.BufferedReader： public String  readLine():  读一行，并将读到的内容返回给一个字符串变量

读完内容，返回null

2.BufferedWriter：  public void  newLine(): 写一行行分隔符，由系统属性定义符号

bufferedWriter.write(s1);

bufferedWriter.newLine(); 

bufferedWriter.flush(); 每写完一行都需要刷新一下

打印流  是专门负责数据输出打印的流对象

1.PrintStream 继承OutputStream，本质上是字节输出流。

2.PrintWriter 继承Writer，本质上是字符输出流

打印流的特点：

1.打印流只负责输出数据，不负责数据来源。

2.打印流永远不会抛出IOException。

3.使用PrintWriter打印流，可以开启自动刷新功能。调用println，printf，format三个方法中的一个才能自动刷新

PrintWriter类

构造方法：

1.public  PrintWriter(String  fileName)：使用指定的文件名创建一个新的打印流

可以传入布尔类型控制自动刷新缓冲区

2.public PrintWriter(OutputStream  out)：使用指定的字节输出流构造打印流

3.public PrintWriter(Writer writer)：使用指定的字符输出流构造打印流

方法：

println，printf，format

**打印流输出数据是原样输出，打印97，结果看到就是97，而不是a。

第十八天

java反射与泛型

Class类

1.class和interface的数据类型是Class

**2.jvm每加载一个.class文件就为其创建一个Class类型的实例，并关联起来

一个Class实例包括类的完整类名，包名，继承的父类，实现的接口，所有的字段和方法

3.是用final修饰的

4.一个类在jvm中只有一个Class实例

常用方法：

1.getName() 获取完整类名

2.getSimpleName() 获取简单类名

3.getPackage().getName 返回包名

4.isInterface() 判断是不是接口类

5.isArray() 判断是不是数组类

6.isPrimitive() 判读是不是基本类型的包装类

7.isEnum() 判断是不是枚举类

8.newInstance() 返回一个类对象

反射：通过Class实例获取class信息的方法

获取Class实例的方法：

1.类名.class

2.类对象.getClass

3.Class.forName(“完整类名”)

**Class实例作用：

1.判断类的类型

2.查看类的完整类名，包名

通过Class实例获取字段信息：

1.getField(String name) 获取某个public的字段（包括父类中字段）返回一个field 对象

2.getDeclaredField(String name) 获取该类中某个字段（不包括父类）返回一个field 对象

3.getFields() 打印出该类的所有公共字段（包括其父类） 返回一个field数组

4.getDeclaredFields() 打印出该类的所有字段（不包括父类）返回一个field数组

Field类

1.一个Filed对象一个field的所有信息（名称，类型，字段修饰符）

getname()

getType()

getModifiers()

get(类实例) 获取字段的值

set(类实例，新值) 为字段赋予新值

setAccessible(true) 将非Public字段设置为可以访问其值和更改其值

第十九天

网络编程多线程和TCP协议

进程：是系统运行程序的基本单位；系统运行一个程序即是一个进程从创建、运行到消亡的过程。

线程：

1.是进程中的一个执行单元，负责当前进程中程序的执行，一个进程中至少有一个线程。

一个进程中是可以有多个线程的，这个应用程序也可以称之为多线程程序

2.当一个进程中有多个线程时，哪个线程执行完全取决于CPU 的调度，程序员是干涉不了的。而这也就造成的多线程的随机性

3.每一个执行线程都有一片自己所属的栈内存空间。进行方法的压栈和弹栈

4.一个线程只能被启动一次

线程的创建-继承方式

Java使用java.lang.Thread类代表线程，所有的线程对象都必须是Thread类或其子类的实例。每个线程的作用是完成一定的任务，实际上就是执行一段程序流即一段顺序执行的代码

通过继承Thread类来创建并启动多线程的步骤如下:

\1. 定义Thread类的子类，并重写该类的run()方法，该run()方法的方法体就代表了线程需要完成的任务,因此把run()方法称为线程执行体。

\2. 创建Thread子类的实例，即创建了线程对象

\3. 调用线程对象的start()方法来启动该线程

Thread的构造方法

1.Thread(Runnable target)

Thread类的方法1.setName()

2.getName()

3.静态方法static Thread currentThread() 获取到当前正在执行的线程对象

线程的创建-实现接口方式

定义Runnable接口的实现类

步骤如下：1. 定义Runnable接口的实现类，并重写该接口的run()方法，该run()方法的方法体同样是该线程的线程执行体。

\2. 创建Runnable实现类的实例，然后在创建Thread实例的时候传入此实现类的实例

\3. 调用线程对象的start()方法来启动线程

实现Runnable接口比继承Thread类所具有的优势：

\1. 适合多个相同的程序代码的线程去共享同一个资源。

\2. 可以避免java中的单继承的局限性。

\3. 增加程序的健壮性，实现解耦操作，代码可以被多个线程共享，代码和线程独立。

线程的创建-匿名内部类方式

Runnable runnable = new Runnable(){

​      public void run() {

​        System.out.println("aaa");

​      }

};

​    new Thread(runnable).start();

网络编程入门

网络编程：在一定的协议下，实现两台计算机的通信的程序

网络编程三要素：

协议，

IP地址，

端口号：用两个字节表示的整数，它的取值范围是0~65535。其中，0~1023之间的端口号用于一些知名的网 络服务和应用，普通的应用程序需要使用1024以上的端口号。如果端口号被另外一个服务或应用所占用，会 导致当前程序启动失败

1.C/S结构：全称为Client/Server结构，是指客户端和服务器结构

2.B/S结构：全称为Browser/Server结构，是指浏览器和服务器结构。

网络通讯协议：

TCP/IP

传输的数据是字节类型，因此要把传输的数据转换成字节在进行传输

[java.net](http://java.net/)包中提供了两种常见的网络协议的支持：

1.TCP：传输控制协议 (Transmission Control Protocol)

客户端： [java.net.Socket](http://java.net.socket/) 类表示。创建 Socket 对象，向服务端发出连接请求，服务端响应请求，两者建 立连接开始通信。

服务端： [java.net.ServerSocket](http://java.net.serversocket/) 类表示。创建 ServerSocket 对象，相当于开启一个服务，并等待客户端 的连接。

Socket

构造方法：

public Socket(String host, int port)  传入服务器IP和端口号

成员方法

套接字指的是两台设备之间通讯的端点

1.public InputStream getInputStream() ： 返回此套接字的输入流。 如果此Scoket具有相关联的通道，则生成的InputStream 的所有操作也关联该通道。 关闭生成的InputStream也将关闭相关的Socket。

2.public OutputStream getOutputStream() ： 返回此套接字的输出流。 如果此Scoket具有相关联的通道，则生成的OutputStream 的所有操作也关联该通道。 关闭生成的OutputStream也将关闭相关的Socket。

3.public void close() ：关闭此套接字。 一旦一个socket被关闭，它不可再使用。 关闭此socket也将关闭相关的InputStream和OutputStream 。

4.public void shutdownOutput() ： 禁用此套接字的输出流。 任何先前写出的数据将被发送，随后终止输出流

ServerSocket

构造方法

public ServerSocket(int port) ：传入端口号

成员方法

public Socket accept() ：侦听并接受连接，返回一个连接服务器的Socket对象，用于和客户端实现通信。

UDP：用户数据报协议(User Datagram Protocol)

第二十天

类加载器

1.是将.class文件加载到内存

2.java.lang.ClassLoader是类加载器的父类、

出现六种情况中的一种，类的加载器就会将这个类的class文件加载到内存中，我们就可以使用这个类了

\1. 创建类的实例。

\2. 使用类的静态变量，或者为静态变量赋值。

\3. 使用类的静态方法。

\4. 使用反射方式来强制创建某个类或接口对应的java.lang.Class对象。

\5. 初始化某个类的子类。

\6. 直接使用java.exe命令来运行某个主类。。

类加载器的分类：

1.引导类加载器Bootstrap：是C++语言编写，负责加载JDK核心类库，核心类库位置\jdk\jre\lib\下的jar包。

2.扩展类加载器ExtClassLoader：Java语言编写的类加载器，负责加载JDK扩展类库，类库位置\jdk\lib\ext\下的jar包

3.应用类加载器AppClassLoader：Java语言编写的类加载器，负责加载我们定义的类和第三方jar包中的类

反射

1.反射的定义：通过Class对象调用类中的成员变量和方法和使用构造方法创建对象的方式

2.**Class对象：类加载器将.class文件加载到内存后，会将java代码的各个组成部分（成员变量，成员方法，构造方法）封装为一个Class对象

3.**反射是针对.class 文件进行操作

获取Class对象的方式：

1.Class.forName("全类名") 传入完整类名 返回Class对象

2.加载类类名.class 返回Class对象

3.对象名.getClass()   使用类对象调用类中的getClass方法 返回Class对象

反射获取构造方法

使用的是Class中与Constructor相关的方法

1.getConstructors() 返回一个Constructor数组，获取所有public修饰的构造方法

2.getConstructor(Class... parameterTypes) 

返回一个Constructor对象，

不传入参数获取的是空参的构造方法

3.newInstance(Object... initargs) 创建对象

4.newInstance(） 

通过反射获取空参构造方法并创建对象

1.Class class1 = Class.forName("com.reflex.Practice1");

2.Constructor constructor = class1.getConstructor(); //将获取到构造方法封装到Constructor

3.Object practice1 = constructor.newInstance();

System.out.println(practice1);

通过反射使用空参构造方法创建对象的简便方法

1.Class class1 = Class.forName("com.reflex.Practice1");

2.Object practice3 = class1.newInstance(）

System.out.println(practice3);

通过反射获取有参构造方法并创建对象

1.Class class1 = Class.forName("com.reflex.Practice1");

2.Constructor constructor1 = class1.getConstructor(String.class,int.class);   传入的是代表参数类型的Class对象

3.Object practice2 = constructor1.newInstance("白雨龙",12);       传入参数值

System.out.println(practice2);

通过反射调用成员方法

使用的是Class中与Method相关的方法

1.Method[] getMethods()   获取所有的public修饰的成员方法，包括父类中的方法，返回Method集合

2.Method getMethod("方法名", 方法的参数类型... 类型) 根据方法名和参数类型获得一个方法对象，只能是获取public修饰的

3.invoke(类对象) 调用方法

获取无参方法并调用

1.Class class1 = Class.forName("com.reflex.Practice1");

2.Constructor constructor = class1.getConstructor(); //将获取到构造方法封装到Constructor

3.Object practice1 = constructor.newInstance();

4.Method method = class1.getMethod("run"); 只需要传入方法名

5.method.invoke(practice1);  传入类对象

获取有参方法并调用

1.Class class1 = Class.forName("com.reflex.Practice1");

2.Constructor constructor = class1.getConstructor(); //将获取到构造方法封装到Constructor

3.Object practice1 = constructor.newInstance();

4.Method method1 = class1.getMethod("eat",String.class); 传入方法名和代表参数类型的Classd对象

5.method1.invoke(practice1,"白雨龙");  传入类对象和参数值

写一个"框架"，不能改变该类的任何代码的前提下，可以帮我们创建任意类的对象，并且执行其中任意方法

创建配置文件

1.在工程下创建一个目录，目录名设为resources,用来存放代码所用到的资源

2.将文件的作用改为resources Root 存放资源的文件 作用：编译时会将resources目录和src目录都放到classes目录下

3.在resources目录下创建一个后缀名为 .properties 的文件 后缀名必须是.properties

写程序

\1. 将需要创建的对象的全类名和需要执行的方法定义在配置文件中

\2. 在程序中加载读取配置文件

A使用ClassLoader中的静态方法getSystemResourceAsStream（要读取的配置文件） 返回一个输入流对象

B创建一个properties集合（特殊的Map集合，键和值不能更改）

C使用properties集合中的load方法，将流中的数据保存到集合

​    InputStream inputStream = ClassLoader.getSystemResourceAsStream("config.properties");

​    Properties properties = new Properties();

​    properties.load(inputStream);

\3. 使用反射技术来加载类文件进内存

\4. 创建对象

​    Class class1 = Class.forName(properties.getProperty("className"));

​    Object pratice2 = class1.newInstance();

\5. 执行方法

​    Method method = class1.getMethod(properties.getProperty("methodName"));

​    method.invoke(pratice2);

单元测试

1.黑盒测试：不需要写代码，给输入值，看程序是否能够输出期望的值。

2.白盒测试：需要写代码的，关注程序具体的执行流程

测试：脱离main,单独运行代码

Junit

1.是一个Java语言的单元测试框架，属于白盒测试，可以用于取代java的main方法。

2.Junit属于第三方工具，需要导入jar包后使用。

Junit的使用

@Test注释的方法要求：

修饰词是public 没有返回值（void），方法中不能传入参数，建议方法名以test开头

前提工作

1.在工程下键一个lib目录，将所需的Junit的jar包传入目录中

2.将此目录下的内容添加到可执行内库  右键目录 Add as Library  Ok 

\1. 编写测试类，简单理解Junit可以用于取代java的main方法

\2. 在测试类方法上添加注解 @Test

  @Test

  public void testRun() {

​    System.out.println("run方法运行");

  }

  

Junit测试框架中常用注解

@Test，用于修饰需要执行的测试方法。

@Before，前提是存在Test注释的方法，修饰的方法会在测试方法之前被自动执行。

@After，前提是存在Test注释的方法，修饰的方法会在测试方法执行之后自动被执行。

注解

1.注解可以写在代码的任意地方

2.用来对代码进行说明注释

3.注解本质上就是一个接口，该接口默认继承Annotation接口

常见注解

\1. @author：用来标识作者名

\2. @version：用于标识对象的版本号，适用范围：文件、类、方法。

\3. @Override：用来修饰方法声明，告诉编译器该方法是重写父类中的方法，如果父类不存在该方法，则编译失败。

注释的定义格式

元注解

public @interface 注解名称{

​    属性列表

}

注解中的属性

\1. 属性的作用：可以让用户在使用注解时传递参数，让注解的功能更加强大。

\2. 属性的格式格式：

A：数据类型 属性名();

B：数据类型 属性名() default 默认值;

\3. 属性适用的数据类型：

八种基本数据类型（int,float,boolean,byte,double,char,long,short)。String类型，Class类型，枚举类型，注解类型。以上所有类型的一维数组zhu

**特殊属性value 

1.当注解中只有一个属性且名称是value，在使用注解时给value属性赋值可以直接给属性值，无论value是单值元素还是数组类型。

\2. 如果注解中除了value属性还有其他属性，且至少有一个属性没有默认值，则在使用注解给属性赋值时，value属性名不能省略。

注解中的元注解

对注解的使用范围进行限制

1.@Target

作用：指明此注解用在哪个位置，如果不写默认是任何地方都可以使用

可选的参数值在枚举类ElemenetType中包括：

TYPE：用在类,接口上

FIELD：用在成员变量上

METHOD：用在方法上

PARAMETER：用在参数上

CONSTRUCTOR：用在构造方法上

LOCAL_VARIABLE：用在局部变量上

2.@Retention

作用：定义该注解存在的有效范围

SOURCE：注解只存在于Java源代码中，编译生成的字节码文件中就不存在了。

CLASS：注解存在于Java源代码、编译以后的字节码文件中，运行的时候内存中没有

RUNTIME：注解存在于Ja源代码av中、编译以后的字节码文件中、运行时内存中，程序可以通过反射获取该注解。

lombok

简化编写javabean

使用lombok注解的步骤

1.将lombok的jar包放到bin目录下

2.在bin目录下 设置 Mark Directory as 设置为Resources Root     作用是将bin目录下的文件添加到可执行内库

3.File | Settings | Plugins   在Setting plugins（插件） 搜索lombok插件进行下载

4.重启idea

5.File | Settings | Build,Execution, Deployment | Compiler（编译） | Annotation Processors（注解处理器）  enable Annotation Processors 打勾

常用的注解：

如果不写有参数的构造方法，系统默认添加无参构造方法

如果写了有参数的构造方法，系统就不会添加无参构造方法

@Setter

@Getter

@ToString

@EqualsAndHashCode

@NoArgsConstructor

@AllArgsConstructor

@Data   自动生成get/set，toString，hashCode，equals

第二十一天

数据库 MySQL

数据库：数据库就是存储数据的仓库，其本质是一个文件系统，数据按照特定的格式将数据存储起来。

用户可以对数据库中的数据进行增加，修改，删除及查询操作。

集合、文件、数据库，三者进行存储数据的对比：

\1. 集合：数据存储在内存中；问题是，一旦程序执行完毕了，数据消失了，数据不能永久性的储存

\2. 文件：数据储存在磁盘中，可以永久性储存；问题是，当文件储存数据量达到几个G时，文件的打开都成文件，数据的操作就更成问题了

\3. 数据库：数据储存的磁盘中，可以永久性储存；当数据量很大时，数据操作起来也很流畅；合适数据的频繁的增删改查的操作

数据库管理系统（DataBase Management System，DBMS）：指一种操作数据库、管理数据库的大型软件。

作用：用于数据库的建立、使用和维护数据库

功能：实现了对多个数据库进行统一管理和控制，以保证数据库的安全性和完整性

\1. 用户必须通过数据库管理系统才能访问到数据库中表的数据

\2. 数据库中的表，是存储数据的基本单位

表记录与java类的对应关系

Java                   数据库

类                     表

成员变量字段            表列

对象                   表行

一列是一个字段，一行是一个对象或记录

常见数据库

MYSQL：开源免费的数据库，小型的数据库.

Oracle：收费的大型数据库，Oracle公司的产品。

DB2：IBM公司的数据库产品,收费的。常应用在银行系统中.SQLServer

MicroSoft公司收费的中型的数据库。C#、.net等语言常使用。

SyBase：已经淡出历史舞台。提供了一个非常专业数据建模的工具PowerDesigner。

SQLite：嵌入式的小型数据库，应用在手机端。

MySql数据库

5.5 5.7

***重装MySql数据库的步骤：

1.卸载数据库

2.删除c:\ProgramData\MySQL目录下的目录

**SQL语句

1.用来操作数据库的语句，支持所有关系型数据库

2.所有数据类型的默认值都是null

3.非数字数据类型用单双引号括起，一般用单引号

4.以分号结尾

5./*

多?注释

*/

--空格  单行注释

\#空格  单行注释

6.comment 用在sql语句后面可以跟表中列的解释信息

SQL语句分类

SQL分类：

数据定义语言：来定义数据库对象：数据库，表， 列等。关键字：create（创建），alter（更改），drop（删除）

数据控制语言：来定义数据库的访问权限和安全级别，及创建用户

数据操作语言：来对数据库中表的记录进行更新。关键字：insert，delete，update等

数据查询语言：来查询数据库中表的记录。关键字： select，from，where等

SQL语言中数据的常用数据类型 ：

类型名称             说明

int                 整数类型

double              小数类型

decimal（m,d）       指定整数位与小数位长度的小数类型

date                日期类型，格式为yyyy-MM-dd，包含年月日，不包含时分秒

datetime            日期类型，格式为 YYYY-MM-DD HH:MM:SS，包含年月日时分秒

日期的范围不同  

timestamp           日期类型，时间戳

varchar（M）        文本类型， M为0~65535之间的整数

char(M)             文本类型, M为0~65535之间的整数

varchar 不会占用剩余空间

char   会占用全部空间

数据库操作: database

1.创建数据库

create database 数据库名称

create database mydb;

create database 数据库名称 character set 编码表

create database mydb1 character set utf8;

2.查询数据库

显示出所有存在的数据库 

show databases;

查看指定数据库的编码表 show creat database 数据库名

show create database mydb;

3..删除数据库

drop database 数据库名

drop database mydb1;

4.使用数据库

使用数据库 use 数据库名

use mydb;

查询当前正在使用的数据库

select database(); 

​                                                                                              

表操作：table

一.创建表

创建表 往当前使用的数据库中创建

create table 表名 (    

​    字段名 数据类型[?度] [约束],    

​    字段名 数据类型[?度] [约束],    

);

注:[]中的内容是可选项

create table mydbuser (

   name varchar(100), # varchar数据类型的长度必须写

   age int

);

二.查看表

查看表

show tables;

查看指定表的建表结构 show create table 表名

show create table mydbuser;

三.删除表

drop table 表名

drop table list;

四.修改表结构

对表中的列进行修改

\1. 添加新的列  格式: alter table 表名 add 新列名 数据类型(长度);

alter table mydbuser add sex varchar(100);

\2. 修改列的数据类型(长度), 格式: alter table 表名 modify 列名 修改后的数据类型(长度);

alter table mydbuser modify sex char(100);

\3. 修改列的名称, 格式: alter table 表名 change 列名 新列名 新列名的数据类型(长度);

alter table mydbuser change sex sss char(100);

\4. 删除指定列, 格式: alter table 表名 drop 列名;

alter table mydbuser drop sss;

对表进行修改

\1. 修改表的名称, 格式:  rename table 表名 to 新表名;

rename table mydbuser to list;

\2. 修改表的字符编码, 格式:  alter table 表名 character set 字符编码;

alter table list character set gbk;

表中记录操作

1.插入表记录

方式一为指定的列插入值   格式: insert into 表名(字段1, 字段2, ...) values (值1, 值2, ...);

insert into stu value(13,'炸','女');

方式二, 对所有字段插入值,  格式: insert into 表名 values(值1, 值2, ...);

insert into stu(age,sex) value(12,'男');

同时插入多个列

insert into stu value(14,'dd','ddd'),(15,'sss','sss');

2.更新表记录

格式: update 表名 set 字段1=值, 字段2=值... where 条件；

update stu set name='wang' where age=11;

update stu set sex='伞' where age>12;

3.删除表记录

delete from 表名 where 条件;

delete from stu where age>13;

在dos命令行操作中文时会报错

show variables like 'character';  查看所有MySQL的编码

解决办法：需要修改client、connection、results的编码一致（改为GBK编码）

***set names gbk; 只在本窗口有效为临时方案

数据库密码重置

1.停止MySQL服务

2.在cmd下,输入 mysqld  --console --skip-grant-tables 启动服务器

3.新打开cmd,输入mysql -uroot 不需要密码, 然后输入以下SQL语句, 完成密码的修改

use mysql;

update user set password=password('新密码')  WHERE user='root';

\4. 关闭两个cmd窗口

第二十二天

MySQL约束 和 查询(DQL)

数据库中的约束：就是指表中的数据内容不能胡乱填写, 必须按照要求填写. 好保证数据的完整性与安全性。

一、主键约束 primary key

针对单列主键

1.主键必须包含唯一的值, 不能重复。

2.主键列不能包含 NULL 值，在插入记录时必须为其传入值

3.每个表都应该有一个主键，并且每个表只能有一个主键

对于多列主键

4.联合主键可以包含多列

多个字段组合为一个主键

作为联合主键的各列的值不是都相等，就不算传入重复的值

作为联合主键的各列的值都不能为NUll

添加主键约束

方式一：创建表时，在字段描述处，声明指定字段为主键：

格式: 字段名 数据类型(⻓度) PRIMARY KEY

将某个字段设置为主键后，该字段在插入记录时值不能重复，并且值不能为空

  

方式二：创建表时，在constraint约束区域，声明指定字段为主键：CONSTRAINT 和 名称 可以省略

格式：constraint 名称  primary key (字段列表)

方式三：通过修改表结构，添加约束区域 CONSTRAINT 和 名称 可以省略

格式：alter table 表名 add CONSTRAINT 名称 PRIMARY KEY (字段列表)

删除主键约束PRIMARY KEY 约束 相当于更改表结构

格式: ALTER TABLE 表名 drop PRIMARY KEY

二、自动增⻓列

1.auto_increment（自动增⻓列）关键字

2.自动增⻓列类型必须是整形

3.自动增⻓列必须为键(通常是用于主键)

4.默认AUTO_INCREMENT 的开始值是 1

5.自动增长列不用传入值或传入null

格式: 字段名  整数类型() 约束 auto_increment

修改默认初始值：

alter table persons auto_increment=起始值

三、非空约束

列不接受 NULL 值

要求字段始终包含值

创建记录或更新记录时必须为非空列传入值

格式: 字段名 数据类型[⻓度]  NOT NULL

删除非空约束(修改数据类型) modify（修改）关键词 相当于更改列的数据类型

ALTER TABLE 表名 modify 字段名 数据类型 ⻓度

四、唯一约束 unique

指定列的值不能重复

如果添加唯一约束时，没有设置约束名称，默认是当前字段的字段名

1.UNIQUE 和 PRIMARY KEY 约束均为列提供了唯一性的保证。PRIMARY KEY 是自动定义的UNIQUE 约束。

\2. 每个表可以有多个 unique 约束，但是每个表只能有一个 PRIMARY KEY 约束。

\3. UNIQUE不限制 null 值出现的次数

方式一：创建表时，在字段描述处，声明唯一

格式: 字段名 数据类型[⻓度]  UNIQUE

式二：创建表时，在约束区域，声明唯一 constraint 名称可以省略

格式：constraint 名称  UNIQUE (单一字段)

​     constraint 名称  UNIQUE (字段1，字段2)

​     组合唯一约束：只有各个字段的值都相等才算重复的值

方式三：创建表后，修改表结构，声明字段唯一

格式: ALTER TABLE 表名 ADD CONSTRAINT 名称 UNIQUE (字段)

删除唯一约束

格式: ALTER TABLE 表名 DROP index 唯一约束名称

五、默认约束 default

用于指定字段默认值

当向表中插入记录时，如果没有明确的为字段赋值，则自动赋予默认值

添加默认约束

格式: 字段名 数据类型[⻓度] default 默认值

删除默认约束格式:

ALTER TABLE 表名 MODIFY 字段名 数 据类型[⻓度]

SQL语句(DQL)查询

语法：select distinct（是否去掉重复的值）  *（整个记录） 或列名,列名（要查询的列）  from 要查询的表  where 条件 

distinct:取出重复的值

针对单个表的查询

1.简单查询

-- 查询所有的商品.

select * from product;

-- 查询商品名和商品价格.

select pname,price from product;

-- 查询价格,去掉重复值.

select distinct price from product;

-- 查询结果是表达式（运算查询）：将所有商品的价格+10元进行显示.

select price+10 from product;

-- 别名查询.使用的关键字是as（as可以省略的）.列别名

select price*10 as price from product;

select price*10 ppp from product;

select pname,price/10 ppp from product;

select pname ppp, price pppp from product;

-- 别名查询.使用的关键字是as（as可以省略的）.表别名

select pname from product as p;

select pname from product p;

2.条件查询

***Mysql 特有的不等于 ！=

比较运算符  <  <=  >=  = <>  大于、小于、大于(小于)等于、不等于

BETWEEN...AND... 显示在某一区间的值(含头含尾)

IN(set)   显示在in列表中的值

like     语句中，% 代表零个或多个任意字符， _ 代表一个字符

and    多个条件同时成立

or     多个条件任一成立

not    不成立

\# 条件查询

\#查询商品名称为“花花公子”的商品所有信息：

select * from product where pname='花花公子';

\#查询价格为800商品

select * from product where price=800;

\#查询价格不是800的所有商品

select * from product where price<>800;

select * from product where price!=800;

\#查询商品价格大于60元的所有商品信息

select * from product where price>60;

\#查询商品价格在200到1000之间所有商品

select * from product where price between 200 and 1000;

select * from product where price>=200 and price<=2000;

\#查询商品价格是200或800的所有商品

select * from product where price in(200,800);

select * from product where price=200 or price=800;

\#like模糊查询 查询商品名称含有'霸'字的所有商品 不能用于数值类的查询

select * from product where pname like '%霸%';

\#查询商品名称以'香'开头的所有商品

select * from product where pname like '香%'

\#查询商品名称第二个字为'想'的所有商品

select * from product where pname like '_想%'

\#商品没有分类id的商品

select * from product where category_id is null;

\#查询有分类id的商品

select * from product where category_id is not null;

3.排序查询

通过order by语句，可以将查询出的结果进行排序

SELECT * FROM 表名 ORDER BY 排序字段  ASC|DESC; 

asc:升序排列，默认是asc

desc:降序排列

\#把查询结果使用价格排序(降序)

select * from product order by price desc;

\#在价格排序(降序)的基础上，以分类排序(降序)

select * from product order by category_id desc;

select * from product order by price DESC,category_id desc;  相等的时候按照后面字段排序

\#显示商品的价格(去重复)，并排序(降序)

select distinct price from product order by price desc;

4.聚合查询

五个聚合函数：

count：统计指定列不为NULL的记录行数； 查看有多少条记录时，一般传入主键列

sum：计算指定列的数值和，如果指定列类型不是数值类型，那么计算结果为0；

max：计算指定列的最大值，如果指定列是字符串类型，那么使用字符串排序运算；

min：计算指定列的最小值，如果指定列是字符串类型，那么使用字符串排序运算；

avg：计算指定列的平均值，如果指定列类型不是数值类型，那么计算结果为0；

\#查询总记录数

select count(pid) from product;

\#查询价格大于200商品的总条数

select count(price) from product where price>200;

\#查询分类为'c001'的所有商品的价格总和

select sum(price) from product;

select sum(price) from product where category_id='c001';

\#查询分类为'c002'所有商品的平均价格

select avg(price) from product;

select avg(price) from product where category_id='c001';

\#查询商品的最大价格和最小价格

select max(price),min(price) from product;

5.分组查询  使用group by字句对查询信息进行分组，然后输出分组结果

格式：SELECT 字段1,字段2...  FROM 表名 GROUP BY  分组字段  HAVING分组条件;

操作中的having子语句，是用于在分组结果后对数据进行过滤的

having与where的区别:

having是在分组操作执行后, 对分组后的数据进行过滤.

where是在分组操作执行前, 对分组前的数据只能使用表原始列进行条件过滤

having后面可以使用聚合函数

where后面不可以使用聚合函数。

当一条SQL语句中, 既有where 又有 group by \ having时, 先执行 where, 再执行 group by,最后执行having

**分组后直接查询分组字段或聚合字段

\#统计各个分类商品的个数

select category_id,count(category_id) from product group by category_id;

select count(category_id) from product group by category_id;

\#统计各个分类商品的个数,且只显示个数大于1的信息

select category_id,count(category_id) from product group by category_id having count(category_id)>1;

\#统计价格>200元的各个分类商品的个数,且只显示个数大于1的信息

select category_id,count(category_id) from product where price>200 group by category_id having count(category_id)>1;

6.条数限制查询 限制查询的记录数

使用limit关键字，其作用是用于限制查询结果的条数

格式: select * from 表名 limit m,n

m是指记录开始的index，从0开始，表示第一条记录

n是指从开始记录查找n条记录

应用场合:分⻚

分⻚查询

格式: SELECT * FROM 表名 LIMIT startRow,pageSize;

elect * from products limit 0,5;  #第一⻚，每⻚显示5条。

select * from products limit 5,5;  #第二⻚，每⻚显示5条。

select * from products limit 10,5; #第三⻚，每⻚显示5条。

起始记录 = （当前页-1）* 页大小

startRow = (curPage - 1) * pageSize

总页数 = Math.ceil（记录总数*1.0）/ 页大小

totalPage = Math.ceil(totalSize * 1.0 / pageSize

第二十三天

mysql数据库3

mysql多表操作

外键约束

***外键特点：

1.**从表外键的值是对主表主键的引用： 从表外键中的值必须用主表中主键中存在的值

2.从表外键类型，必须与主表主键类型一致

外键名称一般以_fk结尾

创建外键约束语法：alter table从表 add [constraint] [外键名称] foreign key (从表外键字段名) references 主表 (主表的主键);

删除外键约束的语法：alter table从表 drop foreign key 外键名称

***外键约束的作用：通过外键将俩个表联系起来

外键约束的限制;

从表增加数据：从表外键的值必须使用主表主键中存在的值

主表删除数据：不能删除从表中已经引用的数据

外键约束的起名规范：从表表名_主表表名_fk

多对多

加中间表 变成一对多

中间表：

必须包含俩个字段，分别关联俩个表的主键

1.俩个字段分别设置为外键，分别关联俩个表的主键

2.把俩个字段设置为联合主键

create table user_role (

  user_id varchar(32),

  role_id varchar(32),

  constraint user_role_pk primary key (user_id,role_id);

  constraint user_role_user_fk foreign key (user_id) references user (uid);

  constraint user_role_role_fk foreign key (role_id) references role (rid);

);

***多表查询

1.交叉连接查询(开发中不使用-得到的是两个表的乘积)

select * from 表1，表2;

效果是：将表1中的每条记录与表2中的所有记录分别连接

在交叉连接的基础上加上限制条件

2.内连接查询(使用的关键字 inner join -- inner可以省略)

隐式内连接：select * from A,B where 条件;

显示内连接：select * from A inner join B on 条件;

3.外连接查询(使用的关键字 outer join -- outer可以省略)

左外连接：left outer join 查询结果包含左边表的所有数据

select * from A left outer join B on 条件;

右外连接：right outer join 查询结果包含右边表的所有数据

select * from A right outer join B on 条件;

***子查询（嵌套查询）

一条select语句结果作为另一条select语法一部分

第二十四天

数据库有三种模型：层次模型，网状模型，关系模型

关系数据库：采用关系模型的数据库

主流的关系数据库有：商业关系数据库：Oracle, SQL Server, DB2， Sybase

​                开源的关系数据库：MySQL, PostgreSQL

关系数据的基本结构是：表

主键的作用是：作为每条记录的唯一标识

外键的作用是：通过引用主表中主键的信息来实现俩个表的关联

关系模型有三种：一对一，一对多，多对多，都是通过外键引用主表的主键的信息来实现关联的

SQL语言：

1.是针对关系数据设计的

2.各种数据库基本一致

3.可以直接根据sql语句进行查询，不必关心数据库底层存储结构

JDBC接口

1.java程序访问数据库的标准接口，定义了访问数据库的标准规范

2.JDBC接口是由jdk定义的连接关系数据库的规范，而具体用来连接数据库的驱动软件(包含jdbc接口的实现类)是由数据库产商定义的

JDBC规范（掌握四个核心对象）：

DriverManager:用于注册驱动

Connection: 表示与数据库创建的连接

Statement: 操作数据库sql语句的对象

ResultSet: 结果集或一张虚拟表

java程序访问数据库的步骤：

一、不使用jdbc工具类的步骤

\1. 注册驱动

加载 Driver 类并在 DriverManager 类中注册后，它们即可用来与数据库建立连接

通过创建驱动的Class对象把驱动类加载到jvm中

Class.forname("com.mysql.jdbc.Driver")

新加载的Driver类会自动调用 DriverManager.registerDriver方法进行自我注册

\2. 获得连接.

使用驱动管理类DriverManeger中的getConnection方法，传入三个字符串，创建连接对象

Connection conn = DriverManager.getConnection(数据库地址，账号，密码);

数据库地址的写法标准：

mysql数据库: jdbc:mysql://数据库ip地址:3306（端口号）/要连接的数据库 或者  jdbc:mysql:///day04（默认本机连接）

如果安装mysql的时候没有指定编码表，在使用java程序插入中文数据时会出现乱码

解决办法：

在数据库地址后？，？后再加俩个键值对 ，键值对之间有与&运算符连接： ?useUincode=true&characterEncoding=utf-8

在5.版本后的驱动程序，还需要在数据库地址后加上时区

& serverTimezone=Asia/Shanghai

&useSSL=false

oracle数据库: jdbc:oracle:thin:@localhost:1521:sid

\3. 获得执行sql语句的对象

Statement stat = conn.createStatement();

\4. 执行sql语句，并返回结果

使用的是Statement类中的方法

常用方法：

int executeUpdate(String sql);--执行insert update delete语句.

int i = statement.executeUpdate(sql); 返回表中记录更改的条数

ResultSet executeQuery(String sql); --执行select语句.

ResultSet resultSet = statement.executeQuery(sql); 返回Resultset对象

\5. 处理结果 处理的是执行select查询语句的结果

Resultset类中的方法：

String getString(int index) / String getString(String name)获得字符串

int getInt(int index) / int getInt(String name)获得整形

double getDouble(int index) / double getDouble(String name)获得双精度浮点型

boolean next() 

如果Resultset对象中有记录就返回ture

第一次调用next()方法时，便指向第一行记录的位置, 第二次调用指向第二行记录，以此类推，若指向的位置没有记录了，则返回false

while (resultSet.next()) {        

​      String cid = resultSet.getString("cid");

​      String cname = resultSet.getString("cname");

​      System.out.println("cid="+cid+"cname="+cname);

​    }

\6. 释放资源

关闭的顺序是先得到的后关闭，后得到的先关闭

close();

把资源文件存储到Properties集合的步骤：

1.把资源文件以输入流形式返回

InputStream ins = Practice3.class.getClassLoader().getResourceAsStream("后缀为.properties文件");

2.创建一个Properties集合，使用集合中的load(),把流中的文件存储到集合中

Properties properties = new Properties();

properties.load(ins);

3.使用集合中的getProperties()方法，通过键找值，返回文件中的值

JDBC工具类 JDBCUtils

1.创建一个以.properties为后缀的资源文件

文件内容：jdbc.driver=com.mysql.jdbc.driver  驱动的完整类名

​        jdbc.url=jdbc:[mysql://localhost:3306/mydb](mysql://localhost:3306/mydb) 数据库的地址

​        jdbc.user=root

​        jdbc.password=root 

2.创建 JDBCUtils工具类

import java.io.IOException;

import java.io.InputStream;

import java.sql.*;

import java.util.Properties;

public class JDBCUtils {

  private static String driver;

  private static String user;

  private static String url;

  private static String password;

  static {

​    try {

​      InputStream ins = JDBCUtils.class.getClassLoader().getResourceAsStream("jdbc.properties");

​      Properties properties = new Properties();

​      properties.load(ins);

​      driver = properties.getProperty("jdbc.driver");

​      user = properties.getProperty("jdbc.user");

​      url = properties.getProperty("jdbc.url");

​      password = properties.getProperty("jdbc.password");

​      Class.forName(driver);

​    } catch (IOException | ClassNotFoundException e) {

​      e.getStackTrace();

​    }

  }

  public static Connection getConnection() throws SQLException {

​    Connection conn = DriverManager.getConnection(url,user, password);

​    return conn;

  }

  public static void close(Connection conn, Statement stat,ResultSet rs) throws SQLException {

​    if (rs != null) {

​      rs.close();

​    }

​    if (stat != null) {

​      stat.close();

​    }

​    if (conn != null) {

​      conn.close();

​    }

  }

}

二、使用jdbc工具类的的步骤

前提：1.写好了资源文件

​     2.定义好了JDBCUtils工具类

查询代码：

​    //直接使用工具类中方法获取连接对象

​    Connection conn = JDBCUtils.getConnection();

​    Statement statement = conn.createStatement();

​    String sql = "select * from category where cid='c003'";

​    ResultSet resultSet = statement.executeQuery(sql);

​    while (resultSet.next()) {

​      String cid = resultSet.getString("cid");

​      String cname = resultSet.getString("cname");

​      System.out.println("cid=" + cid + "cname=" + cname);

​    }

   //直接使用工具类中的方法关闭资源

​    JDBCUtils.close(conn, statement, resultSet);

PreparedStatement

预编译对象，是Statement对象的子类

引入PreparedStatement的原因：

SQL注入问题：

**Statement 执行sql语句有Bug：

**使用Statement 执行sql语句会把用户输入的内容与单引号''进行字符串拼接

例如：如果用户输入 122' or '1=1

​     Statement 执行的sql语句就变成：select * from user where user='' and password='122' or '1=1';

​     这样的话，无论用户是否输对密码都会登录成功

preparedStatement 

1.会把sql语句先编译

2.每条sql语句中所有的实际参数，都必须使用占位符?替换

PreparedStatement使用：

\1. 获取PreparedStatement预处理对象：

String sql = "select * from category where cid=? or cid=?";

传入参数用占位符代替的sql语句

PreparedStatement pstat = conn.prepareStatement(sql);

2.使用PreparedStatement类中set参数类型() 方法，为sql语句中的参数赋值

void setXxx(int index, Xxx xx) 将指定参数设置指定类型的值

参数1：index实际参数序列号，从1开始。

参数2：xxx 实际参数值，xxx表示具体的类型。

3.使用PreparedStatement类中的方法执行sql语句

int executeUpdate();   --执行insert update delete语句.

ResultSet executeQuery();   --执行select语句.

****三、使用JDBCUtils工具类和PreparedStatement的步骤

​    Connection conn = JDBCUtils.getConnection();

​    String sql = "select * from category where cid=? or cid=?";

​    PreparedStatement pstat = conn.prepareStatement(sql);

​    pstat.setString(1,"c001");

​    pstat.setString(2,"c002");

​    ResultSet resultSet = pstat.executeQuery();

​    while (resultSet.next()) {

​      String cid = resultSet.getString("cid");

​      String cname = resultSet.getString("cname");

​      System.out.println("cid="+cid+"cname"+cname);

​    }

​    JDBCUtils.close(conn,pstat,resultSet);

VSCode

第二十五天

连接池

Java为数据库连接池提供了公共的接口（定义了连接池的标准和规范）：java.sql.DataSource

创建连接池的目的：解决创建连接和销毁连接所消耗的资源，提高性能

***连接池的原理：将多个连接放到连接池中，用户要要连接数据库的时候，使用连接池的工具类中的方法从连接池中得到一个连接，在使用完后，再将连接返回给连接池

Druid 连接池

Druid的下载地址：https://github.com/alibaba/druidDRUID

连接池使用的jar包：druid-1.1.16.jar

Druid连接池工具类编写（需要手动编写）

前提：

\1. 导入DRUID jar 包

\2. 编写配置文件（后缀是.properties）

driverClassName=com.mysql.jdbc.Driver

url=jdbc:[mysql://localhost:3306/mydb](mysql://localhost:3306/mydb)

username=root

password=root

创建DruidUtils工具类

1.定义一个静态字段Datasource对象，初始值设为null

2.把配置文件加载到内存

3.为静态字段Datasource对象赋值

4.创建静态方法返回一个Datasource对象

5.创建静态方法返回一个Connection对象

import javax.sql.DataSource;

import java.io.InputStream;

import java.sql.Connection;

import java.sql.SQLException;

import java.util.Properties;

public class DruidUtils {

  public static DataSource ds = null;

  static {

​    try {

​      InputStream ins = DruidUtils.class.getClassLoader().getResourceAsStream("druiddatesource.properties");

​      Properties properties = new Properties();

​      properties.load(ins);

​      ds = DruidDataSourceFactory.createDataSource(properties);

​    } catch (Exception e) {

​      e.printStackTrace();

​    }

  }

  public static DataSource getDataSource() {

​    return ds;

  }

  public static Connection getConnection() throws SQLException {

​    Connection conn = ds.getConnection();

​    return conn;

  }

}

DBUtils

1.是java编程中的数据库操作实用工具，DBUtils封装了对JDBC的操作，简化了JDBC操作

2.项目需要导入commons-dbutils-1.6.jar才能够正常使用DBUtils工具   依赖于commons-logging-1.1.1.jar

Dbutils三个核心功能介绍

一、QueryRunner：执行Sql语句的类

构造方法：

QueryRunner(DataSource)   传入连接池对象

方法：

update(String sql , Object ... params)  执行增删改语句，

传入sql语句和sql语句中每个参数的值 或者 传入Object类型的数组（包含每个参数的值）

1：  int update = queryRunner.update(sql, 14, "钉钉", 1000, "c0006");

2：  Object[] objects = {15,"呜呜",1000,"c006"};

​        int update = queryRunner.update(sql,objects);

query(String sql , ResultSetHandler , Object ... params)  执行DQL语句

传入：sql语句 如何处理结果的ResultSetHandler接口的实现类对象，需要使用泛型 参数的值

二、ResultSetHandler：定义如何封装查询结果的接口

前提：javabean类必须与数据库中的查询的表相匹配

JavaBean

具有如下特性

\1. 需要实现接口：java.io.Serializable ，通常实现接口这步骤省略了，不会影响程序。

\2. 提供私有字段：private 类型字段名;

\3. 提供getter/setter方法：

\4. 提供无参构造

四个实现类

1.BeanHandler：将结果集中第一条记录封装到一个指定的javaBean对象中

返回一个javaBean对象

​    public void testDBUtils4() throws SQLException {

​    QueryRunner queryRunner = new QueryRunner(DruidUtils.getDataSource());

​    String sql = "select * from product where pid=?";

​    Product product = queryRunner.query(sql, new BeanHandler<Product>(Product.class),14);

​    System.out.println(product);

  }

2.BeanListHandler：将结果集中每一条记录封装到指定的javaBean中，将这些javaBean在封装到List集合中

返回一个List集合

​    QueryRunner queryRunner = new QueryRunner(DruidUtils.getDataSource());

​    String sql = "select * from product where pid<?";

​    List<Product> list = queryRunner.query(sql,new BeanListHandler<Product>(Product.class),5);

​    for (Product p : list) {

​      System.out.println(p);

​    }

3.ScalarHandler：一般用于处理聚合函数的结果，它是用于单数据。

***返回的类型是整型，泛型用Long类型

***返回的类型是浮点型，泛型用BigDecimal类型

​    QueryRunner queryRunner =new QueryRunner(DruidUtils.getDataSource());

​    String sql = "select avg(pid) from product";

​    BigDecimal bigDecimal = queryRunner.query(sql, new ScalarHandler<BigDecimal>());

​    System.out.println("bigDecimal = " + bigDecimal);

4.ColumnListHandler：将结果集中指定的列的字段值，封装到一个List集合中

***返回一个List集合 列的类型是什么 list集合中的泛型就写什么

​    QueryRunner queryRunner =new QueryRunner(DruidUtils.getDataSource());

​    String sql = "select * from product";

​    List<String> list = queryRunner.query(sql,new ColumnListHandler<String>("pname")); //****

​    for (String s : list) {

​      System.out.println("s = " + s);

​    }

三、DbUtils：

第二十六天

数据库JDBC（事务操作&ThreadLocal）

事务：表示一组操作要么全部成功，要么全部失败

俩种事务管理方式：

自动提交：即执行一条sql语句提交一次事务。

手动提交：先开启，再提交

mysql默认是自动提交

mysql事务操作

start transaction 开启事务

commit  提交事务，让事务结果生效

rollback  回滚事务，让事务结果失效

创建工程方式变化：

jdbc事务操作

模拟转账

使用Connection对象的方法名描述

conn.setAutoCommit(false)  把自动提交设置为false  开启事务

[conn.commit](http://conn.commit/)()   提交事务 让事务结果生效

conn.rollback()   回滚事务 让事务结果失效

需要手动关闭资源

前提：已导入DruidUtils工具类

代码：

//---------------------------------

import org.junit.Test;

import java.sql.Connection;

import java.sql.PreparedStatement;

import java.sql.SQLException;

public class TestTransaction {

  //  jdbc事务操作

  /*  1.获得连接

​     2.开始事务

​     \3. 具体的sql操作(加钱, 减钱)

​     \4. 提交事务

​     5.如果出现异常, 回滚事务

​     6.释放资源*/

  

  private Connection conn = null;

  private PreparedStatement pstat = null;

  @Test

  public void test1() {

​    try {

​      conn = DruidUtils.getConnection();

​      conn.setAutoCommit(false);

​      String sql1 = "update account set money=money-? where name=?";

​      String sql2 = "update account set money=money+? where name=?";

​      pstat = conn.prepareStatement(sql1);

​      pstat.setDouble(1,1000);

​      pstat.setString(2,"rose");

​      int update = pstat.executeUpdate();

//    double i = 1/0;

​      System.out.println("update = " + update);

​      pstat = conn.prepareStatement(sql2);

​      pstat.setDouble(1,1000);

​      pstat.setString(2,"tom");

​      int update1 = pstat.executeUpdate();

​      System.out.println("update1 = " + update1);

​      [conn.commit();](http://conn.commit()%3B/)

​      conn.close();

​      pstat.close();

​    } catch (Exception e) {

​      e.printStackTrace();

​      try {

​        conn.rollback();

​        conn.close();

​        pstat.close();

​      } catch (SQLException throwables) {

​        throwables.printStackTrace();

​      }

​    }

  }

}

//-------------------------------------

DBUtils事务操作

Connection对象的方法名描述

conn.setAutoCommit(false) 把自动提交设置为false，开启事务

new QueryRunner()  创建QueryRunner对象，但是不传入数据源

query(conn , sql , handler, params ) 或update(conn, sql , params) 在进行执行sql操作时，传入连接对象

***[DbUtils.commitAndCloseQuietly(conn](http://dbutils.commitandclosequietly(conn/)) 提交事务并关闭资源，需要传入连接对象

***DbUtils.rollbackAndCloseQuietly(conn）回滚事务并关闭资源，需要传入连接对象

//------------------------------------

import [org.apache.commons.dbutils.DbUtils;](http://org.apache.commons.dbutils.dbutils%3B/)

import [org.apache.commons.dbutils.QueryRunner;](http://org.apache.commons.dbutils.queryrunner%3B/)

import org.junit.Test;

import java.sql.Connection;

//DBUtils 的事务操作

public class TestDBUtilsTransaction {

   /*

   1.获得连接

   2.开始事务

   3.具体的sql操作(加钱, 减钱)

   4.提交事务 ,释放资源

   5.如果出现异常, 回滚事务释放资源

   */

  private Connection conn = null;

  @Test

  public void test1() {

​    try {

​      conn = DruidUtils.getConnection();

​      QueryRunner qr = new QueryRunner();

​      conn.setAutoCommit(false);

​      String sql1 = "update account set money=money-? where name=?";

​      String sql2 = "update account set money=money+? where name=?";

​      int rose = qr.update(conn, sql1, 1000, "rose");

​      System.out.println("rose = " + rose);

​      int tom = qr.update(conn, sql2, 1000, "tom");

​      System.out.println("tom = " + tom);

​      [DbUtils.commitAndCloseQuietly(conn);](http://dbutils.commitandclosequietly(conn)%3B/)

​    } catch (Exception e) {

​      e.printStackTrace();

​      DbUtils.rollbackAndCloseQuietly(conn);

​    }

  }

}

//--------------------------------------

JavaEE分层开发思想

使用分层开发思想, 完成转账

web端程序：

//------------------------------------------

import com.practice.server.AccountServer;

public class TestAccount {

  /** * 程序执行的入口 */

  public static void main(String[] args) {

​    /*  1. 模拟数据扣款人收款人金额

​       \2. 调用AccountService中转账方法

​       \3. 打印转账后的结果 ( 成功, 失败)

​    */

​    String outUser = "rose";

​    String inUser = "tom";

​    double money = 1000;

​    //调用AccountService中的转账方法

​    try {

​       AccountServer accountServer = new AccountServer();

​       accountServer.transferAccount(outUser,inUser,money);

​      System.out.println("转账成功");

​    } catch (Exception e) {

​      e.printStackTrace();

​      System.out.println("转账失败");

​    }

  }

}

//---------------------------------------

server端的程序

//------------------------------------------

import com.practice.dao.AccountDao;

import com.practice.utils.DruidUtils;

import [org.apache.commons.dbutils.DbUtils;](http://org.apache.commons.dbutils.dbutils%3B/)

import [org.apache.commons.dbutils.QueryRunner;](http://org.apache.commons.dbutils.queryrunner%3B/)

import java.sql.Connection;

import java.util.Queue;

//服务器端进行的操作

public class AccountServer {

  /*** 转账方法*

   \* 参数1 : 扣款人*

   \* 参数2 : 收款人*

   \* 参数3 : 金额*/

  Connection conn = null;

  public void transferAccount(String outUsrt, String inUser, double money) {

​    try {

​      //创建连接，开启事务

​      conn = DruidUtils.getConnection();

​      conn.setAutoCommit(false);

​      //调用AccountDao中的减钱和加钱方法对数据库进行操作

​      AccountDao accountDao = new AccountDao();

​      accountDao.out(conn,outUsrt,money);

​      accountDao.in(conn,inUser,money);

​      //提交连接并释放资源

​      [DbUtils.commitAndCloseQuietly(conn);](http://dbutils.commitandclosequietly(conn)%3B/)

​    } catch (Exception e) {

​      e.printStackTrace();

​      DbUtils.rollbackAndCloseQuietly(conn);

​    }

  }

}

//---------------------------------------

数据库中的代码

//-----------------------------------------

import [org.apache.commons.dbutils.QueryRunner;](http://org.apache.commons.dbutils.queryrunner%3B/)

import java.sql.Connection;

import java.sql.SQLException;

public class AccountDao {

  /*** 扣钱方法*

   \* @param outUser * 扣钱人

   \* @param * money 金额

   \* */

  QueryRunner queryRunner = null;

  public void out(Connection conn, String outUser, double money) throws SQLException {

​    queryRunner = new QueryRunner();

​    String sql1 = "update account set money=money-? where name=?";

​    queryRunner.update(conn, sql1, money,outUser);

  }

  /*** 加钱方法*

   \* @param inUser 收钱人

   \* @param money 金额

   \* */

  public void in(Connection conn,String inUser,double money) throws SQLException {

​    queryRunner = new QueryRunner();

​    String sql2 = "update account set money=money+? where name=?";

​    queryRunner.update(conn, sql2, money,inUser);

  }

}

//-----------------------------------------

ThreadLocal

java.lang.ThreadLocal：该类提供了线程局部 (thread-local) 变量，用于在当前线程中共享数据

ThreadLocal工具类底层就是相当于一个Map，key存放的当前线程，value存放需要共享的数据

ThreadLocal的使用步骤:

1.创建ThreadLocal对象，

2.使用ThreadLocal中的set()方法，给当前线程设置一个线程局部变量

3.在需要使用该线程局部变量的时候，使用ThreadLocal中的get()方法获取

***注意：ThreadLocal类定义的线程局部变量只能在本线程中使用

一般在线程中不变的变量可以使用ThreadLocal类设置成线程局部变量，方便在线程其他地方使用。

使用了ThreadLocla技术的DBUtils工具类

//-----------------------------------------

import com.alibaba.druid.pool.DruidDataSourceFactory;

import javax.sql.DataSource;

import java.io.InputStream;

import java.sql.Connection;

import java.sql.SQLException;

import java.util.Properties;

public class DruidUtils {

  public static DataSource ds = null;

  static {

​    try {

​      InputStream inputStream = DruidUtils.class.getClassLoader().getResourceAsStream("Druid.properties");

​      Properties properties = new Properties();

​      properties.load(inputStream);

​      ds = DruidDataSourceFactory.createDataSource(properties);

​    } catch (Exception e) {

​      System.out.println("e = " + e);

​    }

  }

  public static DataSource getDataSource() {

​    return ds;

  }

  public static Connection getConnection() throws SQLException {

​    ThreadLocal<Connection> threadLocal = new ThreadLocal<>();

​      Connection conn = threadLocal.get();

​      if (conn == null) {

​        conn = ds.getConnection();

​        threadLocal.set(conn);

​      }

​      return conn;

  }

}

//-----------------------------------------

web中的代码

//----------------------------------------------

import com.practice.server.AccountServer;

public class AccountWeb {

  /** * 程序执行的入口 */

  public static void main(String[] args) {

​    /*  1. 模拟数据扣款人收款人金额

​       \2. 调用AccountService中转账方法

​       \3. 打印转账后的结果 ( 成功, 失败)

​    */

​    String outUser = "rose";

​    String inUser = "tom";

​    double money = 1000;

​    //调用AccountService中的转账方法

​    try {

​      AccountServer accountServer = new AccountServer();

​      accountServer.transferAccount(outUser,inUser,money);

​      System.out.println("转账成功");

​    } catch (Exception e) {

​      e.printStackTrace();

​      System.out.println("转账失败");

​    }

  }

}

//-------------------------------------------------------

server中的代码

//--------------------------------------------------------

import com.practice.database.AccountDatabase;

import com.practice.utils.DruidUtils;

import [org.apache.commons.dbutils.DbUtils;](http://org.apache.commons.dbutils.dbutils%3B/)

import java.sql.Connection;

public class AccountServer {

  /*** 转账方法*

   \* 参数1 : 扣款人*

   \* 参数2 : 收款人*

   \* 参数3 : 金额*/

  Connection conn = null;

  public void transferAccount(String outUsrt, String inUser, double money) {

​    try {

​      conn = DruidUtils.getConnection();

​      conn.setAutoCommit(false);

​      //调用AccountDao中的减钱和加钱方法对数据库进行操作

​      AccountDatabase accountDatabase = new AccountDatabase();

​      accountDatabase.out(outUsrt,money);

​      accountDatabase.in(inUser,money);

​      [DbUtils.commitAndCloseQuietly(conn);](http://dbutils.commitandclosequietly(conn)%3B/)

​    } catch (Exception e) {

​      e.printStackTrace();

​      DbUtils.rollbackAndCloseQuietly(conn);

​    }

  }

}

//-----------------------------------------------------

数据库操作的代码

//---------------------------------------------------

public class AccountDatabase {

  /*** 扣钱方法*

   \* @param outUser * 扣钱人

   \* @param * money 金额

   \* */

  QueryRunner queryRunner = null;

  public void out(String outUser, double money) throws SQLException {

​    Connection conn = DruidUtils.getConnection();

​    queryRunner = new QueryRunner();

​    String sql1 = "update account set money=money-? where name=?";

​    queryRunner.update(conn, sql1, money,outUser);

  }

  /*** 加钱方法*

   \* @param inUser 收钱人

   \* @param money 金额

   \* */

  public void in(String inUser,double money) throws SQLException {

​    Connection conn = DruidUtils.getConnection();

​    queryRunner = new QueryRunner();

​    String sql2 = "update account set money=money+? where name=?";

​    queryRunner.update(conn, sql2, money,inUser);

  }

}

//--------------------------------------------------

第二十七天

Tomcat&Http&Servlet

web:万维网，一种基于超文本和HTTP的、全球性的、动态交互的、跨平台的分布式图形信息系统

java web:使用javas技术来解决web开发的的技术总和

Java Web开发中的资源

静态web资源:html,js,css

动态web资源:Servlet,jsp

URL:统一资源定位符，是互联网上资源的一种表示，互联网上的每个文件都有唯一的URL

完整格式：协议：//域名或ip:端口号/资源位置？请求参数=值

软件开发的结构分类

1.CS结构的软件

cs: client/server客户端/服务器，这种软件需要安装客户端才可以使用

优缺点：

优点是：可以减轻服务器端压力，将部分代码写到客户端，界面很美观

缺点是：一旦服务器更新了，客户端也需要更新，分布式开发比较弱

2.BS结构的软件

Bs：browser/server 浏览器/服务器 这种软件不需要安装，可以直接通过浏览器访问服务器

优缺点：

优点：服务器一旦更新，不需要更新客户端，因为客户端就是浏览器，比较强的分布式能力

缺点：服务器端压力会比较大。界面效果不如CS结构软件

WEB服务器

服务器

硬件：一台配置非常高的电脑

软件：在一台电脑上安装web服务器的软件

Tomcat 服务器软件

1.把tomcat软件安装到电脑上，这台电脑就可以作为服务器使用

2.默认端口号：8080

3.Tomcat运行需要依赖Java环境，需要配置JAVA_HOME环境变量

4.要在idea中使用tomcat,需要先将tomcat与idea进行关联

5.可以响应对html页面的访问请求

6.支持运行基于Servlet的java程序

Tomcat版本   Servlet版本   JavaEE版本

9.0.x           4.0         8.0

8.5.x           3.1         8.0

8.0.x           3.1         7.0

7.0.x          3.0         6.0

6.0.x          2.5         5.0

在JavaEE规范中，WEB项目存在一定的目录结构，具体结构如下：

项目名称（存放于：Tomcat软件安装目录中，webapps目录下的子文件夹）

|-----静态资源 HTML，CSS，JS

|-----WEB-INF  （不能直接通过浏览器进行访问）

​       |----web.xml 当前WEB项目的核心配置，Servlet2.5必须有，3.0以后可省略

​       |----lib当前WEB项目所需要的第三方的jar的存放位置。

​       |----classes Java源码编译后生成class文件存放的位置。

HTTP

HTTP协议:超文本传输协议，用来定义浏览器和web服务器之间交换数据的过程

1.默认端口号是80

Http请求：客户端向服务器端发起的

请求包括四个部分：请求行:请求方式 url 协议/版本

​               请求头：请求参数 以键值对形式存在

​               空行：

​              请求体：表单，用来存放Post请求中带的请求参数

Http响应：从服务端到客户端

响应也包括四个部分：响应行：协议/版本 状态码 状态码描述

​                响应头：参数 以键值对形式存在

​                空行：

​                响应体：返回给浏览器的内容

Servlet（server applet）：服务器端小程序

作用：java类，运行时生成动态html网页的java程序

Servlet的使用步骤：

\1. 编写一个Java类实现Servlet的接口

需要重写Servlet中的五个抽象方法

每次请求该Sevlet都会执行其中的service方法

\2. 在web.xml中，配置Servlet

<servlet>

<servlet-name>Servlet类名</servlet-name>

<servlet-class>Serblet的完整类名</servlet-class>

</servlet>

<servlet-mapping>

<servlet-name>Servlet类名</servlet-name>

<url-pattern>/Servlet的别名（用于浏览器中请求Servlet）</url-pattern>

</servlet-mapping>

\3. 访问servlet

HttpServlet 

Servlet接口

   GenericServlet类     通用的Servlet，是一个与协议无关的Servlet

​       HttpServlet类   Http协议专用的Servlet,专⻔用来处理HTTP协议的请求响应

​         有俩个方法：doGet方法doPost方法

​         继承了HttpServlet之后不需要重写service方法，只需要重写doGet和doPost方法即可

​         当浏览器的请求方式是get方式时，会执行doGet方法

​         当浏览器的请求方式时post方式时，会执行doPost方法

****案例用户登录

1.创建数据库表

CREATE TABLE `user`(  

username VARCHAR(50),  

`password` VARCHAR(50)

);

INSERT INTO `user` VALUES('tom','123'),('jerry','456');

2.创建WEB项目

  添加必要的jar，配置文件，工具类，JavaBean(User类)

  创建自己的包  

//User类

  public class User {

  private String username;

  private String password;

  public String getUsername() {

​    return username;

  }

  public void setUsername(String username) {

​    this.username = username;

  }

  public String getPassword() {

​    return password;

  }

  public void setPassword(String password) {

​    this.password = password;

  }

}

3.编写⻚面

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

  <title>用户登录</title>

</head>

<body>

<form action="/tomcat/login" method="post">

  用户名：<input type="text" name="username" value=""/> <br/>

  密 码：<input type="text" name="password" value=""/> <br/>

  <input type="submit"/>

</form>

</body>

</html>

4.编写服务器Servlet

import com.pojo.User;

import com.utils.DruidUtils;

import [org.apache.commons.dbutils.QueryRunner;](http://org.apache.commons.dbutils.queryrunner%3B/)

import [org.apache.commons.dbutils.handlers.BeanHandler;](http://org.apache.commons.dbutils.handlers.beanhandler%3B/)

import javax.servlet.ServletException;

import javax.servlet.http.HttpServlet;

import javax.servlet.http.HttpServletRequest;

import javax.servlet.http.HttpServletResponse;

import java.io.IOException;

import java.io.PrintWriter;

import java.sql.SQLException;

public class LoginServlet extends HttpServlet {

  @Override

  protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

​    //开发中，get和post请求的处理方式是一样的

​    doPost(req,resp);

  }

  @Override

  protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

​    String username = req.getParameter("username");

​    String password =req.getParameter("password");

​    QueryRunner queryRunner = new QueryRunner(DruidUtils.getDataSource());

​    String sql = "select * from user where username=? and password=?";

​    try {

​      User user = queryRunner.query(sql,new BeanHandler<User>(User.class),username,password);

​      if (user == null) {

​        System.out.println("登录失败");

​        PrintWriter writer = resp.getWriter();

​        writer.print("login fail");

​      } else {

​        System.out.println("登录成功");

​        PrintWriter writer = resp.getWriter();

​        writer.print("login success");

​      }

​    } catch (SQLException throwables) {

​      throwables.printStackTrace();

​    }

  }

}

5.将浏览器与Servlet关联

  <servlet>

​    <servlet-name>LoginServlet</servlet-name>

​    <servlet-class>com.servlet.LoginServlet</servlet-class>

  </servlet>

  <servlet-mapping>

​    <servlet-name>LoginServlet</servlet-name>

​    <url-pattern>/login</url-pattern>

  </servlet-mapping>

6.更新服务器中的内容

7.访问login.html页面

8.进行用户登录

第二十八天

ServletContext & Response 

这俩个对象是由tomcat创建的

ServletContext

1.使用ServletContext对象表示WEB应用程序(在Tomcat服务器中的web的项目)

2.ServletContext是接口, 此接口的实现类是tomcat引擎提供

3.在一个WEB应用程序中，只能存在一个ServletContext对象

4.在服务器启动的时候，为每个web应用程序创建一个单独的ServletContext对象

5.当web项目从服务器中移除，或者是关闭服务器的时候ServletContext对象会被销毁

如何获取ServletContext对象

使用ServletConfig中的getServletContext方法

创建一个Servlet,让其继承HttpServlet

HttpServlet的父类GenericServlet中实现了ServletConfig方法

ServletContext servletContext = super.getServletContext();

作用：

1.获取web项目的初始化参数

在web.xml配置文件中设置参数参数

  <context-param>

​    <param-name>bai</param-name>

​    <param-value>123</param-value>

  </context-param>

获取SetvletContext对象

ServletContext servletContext = super.getServletContext();

使用SetvletContext对象中的getInitParameter()方法

public String getInitParameter(String name);  传入键，返回值

2.获取web项目下任意资源编译后的绝对路径(out目录下的资源的绝对路径)

注意：只有web目录和src目录下的内容才会被编译进tomcat中

使用使用SetvletContext对象中的getRealPath()方法

public String getRealPath(String path); 传入相对路径，返回绝对路径

注意：web1_war_exploded相当于web目录，classes目录相当于src目录

out\artifacts\web1_war_exploded\WEB-INF\classes

相对路径：以out目录下的out\artifacts\web1_war_exploded为顶层目录

web1_war_exploded目录下的文件的相对路径：文件名.后缀

WEB-INF目录下的文件的相对路径：WEB-INF//文件名.后缀

classes目录下的文件的相对路径：WEB-INF//classes//文件名.后缀

3.作为域对象，存储全局数据

放在ServletContext中的数据，单前项目中的每个Servlet都可以访问

javaweb四大域对象

根据有作用范围由小到大：

page(jsp有效)------》page域指在当前⻚面中有效, 一旦⻚面超出该⻚面就不能访问了.

request(一次请求)---》request域指在本次请求与响应过程中, 都能够访问.

session(一次会话)---》session域指在本次打开浏览器访问服务器开始, 到本次浏览器关闭之间访问有效

application(当前web应用)---》application域指在当前web项目中均可访问. 由ServletContext代表application域

都内置了map集合，都有setAttribute和getAttribute  方法

向域对象中存储数据(存储的数据是键值对)

public void setAttribute(String name, Object object);

得到域对象中存储的数据

public Object getAttribute(String name);

移除域对象中存储的数据

public void removeAttribute(String name);

案例 统计用户访问服务器的的次数

//init()方法：在用户第一次访问该servlet的时候会先执行一次init()方法，然后再执行doget()方法

@Override

public void init() throws ServletException {

  ServletContext context = super.getServletContext();

  context.setAttribute("count",0);

}

protected void doGet(HttpServletRequest request, HttpServletResponseresponse) throws ServletException, IOException {

  //取出数据进行加1操作，再将数据进行更改

  ServletContext context = super.getServletContext();

  //getAttribute()方法返回的是一个Object对象，需要强转为Integer对象，才能进行自加操作

  Integer count = (Integer) context.getAttribute("count");

  count++;

  System.out.println("welcome " + count);

  context.setAttribute("count",count);

}

Servlet

Servlet 3.0版本时，新增的注解

作用：用于简化 Servlet、过滤器（Filter）和监听器（Listener）的声明

__________________________________________________________________________

注解开发取代web.xml

1.直接创建Servlet

2.更改注解中的键，改为urlPatterns，并在值的前面加/

 或者直接去掉注解中的键，在值前面加/ 原因：不写键，默认键是urlPatterns

方式一、

@WebServlet(urlPatterns = "/annotation2")

public class annotation2 extends HttpServlet {

  protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

  protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

}

方式二、

@WebServlet("/annotation2")

public class annotation2 extends HttpServlet {

  protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

  protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

}

**********

更改Servlet注解模板后，直接创建Servlet即可

创建Servlet时，name:Servlet在网页中的地址  class:Servlet的完整类名

注意：在web项目中修改或增加了内容后，一定要重新部署web项目，要不会报错

_____________________________________________________________________________

***Response对象

1.对浏览器的请求进行响应的对象

2.Response对象是由tomcat创建的

响应：服务器收到浏览器的请求后，对请求进行处理，并把处理结果返回给浏览器的过程

响应内容包括: 响应行,响应头,响应体

Response设置响应行

设置响应的状态码

200        正确

302        重定向

304        查找本地缓存 浏览器请求的数据跟上一次请求一样，状态码返回304，告诉浏览器去浏览器本地缓存中找

404        请求资源不存在

500        服务器内部错误

使用response对象中的setStatus方法

public void setStatus(int sc);

response.setStatus(404);

Response设置响应头

1.响应头的内容是键值对

2.响应头的内容包含指导信息，指导浏览器

设置响应头的一些方法：

addHeader(String key,String value) 无返回值  添加响应头，值为String类型

addIntHeader(String key,int value) 无返回值   添加响应头，值为int类型

addDateHeader(String key,long l)  无返回值   添加响应头，值为日期类型

setHeader(String key,String value) 无返回值   更改响应头，值为String类型

setIntHeader(String key,int value)  无返回值   更改响应头，值为int类型

setDateHeader(String key,long l)   无返回值   更改响应头，值为日期类型

Response设置响应体

1.响应体中内容是返回给浏览器页面的内容

字符流向浏览器写数据

1.使用response对象中getWriter()方法，返回一个PrintWriter对象

PrintWriter pw = response.getWriter();

2.使用PrintWriter对象中的print()方法和write()方法向浏览器写数据

print()方法：原样输出

write()方法：输入字符串时原样输出，输入整数时，返回整数在编码表中对应的字符

​    pw.print(100);    100

​    pw.print("ssss")   ssss

​    pw.write("ssdd");  ssdd

​    pw.write(97);     a

****字符流的中文乱码问题    

原因：response底层用的编码表不识别中文

方法一:setHeader("Content-Type","text/html;charset=UTF-8")

//在响应头加一个键值对 "content-type","text/html;charset=utf-8"

response.setHeader("content-type","text/html;charset=utf-8");

方法二:setContextType(String type)

//使用response对象中的setContentType方法，只需要传入"text/html;charset=utf-8"这个字符串即可

response.setContentType("text/html;charset=utf-8");

字节流向浏览器写数据

使用response对象中的getOutputStream()方法

服务器给浏览器传一张照片

​    ServletContext sc = getServletContext();

​    String realPath = sc.getRealPath("WEB-INF\\classes\\tupian.jpg");

​    FileInputStream fis = new FileInputStream(realPath);

​    System.out.println(realPath);

​    OutputStream os = response.getOutputStream();

​    byte[] bytes = new byte[1024];

​    int len;

​    while ((len =fis.read(bytes)) != -1) {

​      os.write(bytes,0,len);

​    }

​    fis.close();

重定向

重定向的资源位置可以跨项目

重定向的理解:浏览器请求服务器的某个servlet,该servlet中没有浏览器中需要的信息，而该servlet知道浏览器所要的信息的地址，

因此该servlet返回给浏览器一个302状态码和所需信息的位置

浏览器进行重新的定向:

方法一、

1.设置302状态码: setStatus(302)

2.设置重定向资源的地址: setHeader("location","资源")

response.setStatus(302);

response.setHeader("location","/annotation/annotation1");

方法二、

直接是response对象中的sendRedirect()方法

sendRedirect(String location) 传入资源位置

response.sendRedirect("/annotation/annotation1");

\-----------------------------------------------------------------------------------------------------

文件下载案例

html中的代码

​    <a href="/download/download2?filename=照片.jpg" name="">点击下载图片</a>>

  

servlet中的代码

@WebServlet("/download2")

public class Download2 extends HttpServlet {

  protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

  

  protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    //获取请求头中的参数filename所对应的文件路径

​    String filepath = request.getParameter("filename");

​    //根据浏览器传进来的此文件相对路径得到文件的绝对路径

​    String realPath = getServletContext().getRealPath("WEB-INF/" + filepath);

​    FileInputStream fis = new FileInputStream(realPath);

​    //解决文件名中带中文浏览器下载后文件名乱码问题

​    String agent = request.getHeader("User-Agent");

​    if (agent.contains("MSIE")) {

​      // IE浏览器

​      filepath = URLEncoder.encode(filepath, "utf-8");

​      filepath = filepath.replace("+", " ");

​    } else if (agent.contains("Firefox")) {

​      // 火狐浏览器

​      BASE64Encoder base64Encoder = new BASE64Encoder();

​      filepath = "=?utf-8?B?" + base64Encoder.encode(filepath.getBytes("utf-8")) + "?=";

​    } else {

​      // 其它浏览器

​      filepath = URLEncoder.encode(filepath, "utf-8");

​    }

​    //通知浏览器该文件进行下载,不要打开

​    response.setHeader("Content-Disposition","attachment;filename="+filepath);

​    //使用字节流把文件传给浏览器

​    OutputStream os = response.getOutputStream();

​    int len;

​    byte[] bytes = new byte[1024];

​    while ((len = fis.read(bytes)) != -1) {

​      os.write(bytes,0,len);

​    }

​    fis.close();

  }

}

\------------------------------------------------------------------------------------------------

案例验证码

从字符串中生成四个随机字符

​     String a = "abcdefghigklmnopqrstuvwxyz0123456789";

​    for (int i=0; i<4; i++) {

​      Random rd = new Random();

​      //生成字符串中的一个随机索引

​      int index = rd.nextInt(a.length());

​      //使用String中的charAt()方法得到索引处的字符

​      char b = a.charAt(index);

​      System.out.println("b = " + b);

​    }

第二十九天

request

1.⼦接⼝HttpServletRequest, 它继承⾃ServletRequest, 是与HTTP协议相关的

Request请求对象

2.可以实现客户端向服务器发出请求, 请求内容包括: 请求⾏,请求头,请求体

一、使用request获取请求行

1.获取请求方式

⽅法             返回值    描述

getMethod()      String   获取提交的⽅式 (GET,POST)

String method = request.getMethod();

System.out.println("method = " + method);

2.获取WEB项目的虚拟路径

getContextPath()  String    获取WEB项目的虚拟路径

String path = request.getContextPath();

System.out.println("path = " + path);

****二、使用request获取post请求中的请求参数

\1. 获得提交的参数（⼀个键对应一个值的参数）

⽅法                               返回值      描述    

getParameter(表单中的name）           String     获得提交的参数（⼀个name对应⼀个value）

String vlaue = request.getParameter("username");

System.out.println("vlaue = " + vlaue);

2.获得提交的参数（⼀个键对应多个值的参数）

getParameterValues(表单中的name值)   String[]    获得提交的参数（⼀个name对应多个value）

String[] values = request.getParameterValues("hobby");

System.out.println(Arrays.toString(values));

3.获得提交的参数，将提交的参数名称和对应值存⼊到⼀个Map集合中

getParameterMap() Map<String,String[]>   获得提交的参数，将提交的参数名称和对应值存⼊到⼀个Map集合中

Map<String,String[]> map = request.getParameterMap();

Set<String> set = map.keySet();

for (String key : set) {

​    String[] strings = map.get(key);

​    System.out.println(key+"="+Arrays.toString(strings));

}

***使用request对象接收post请求中的请求参数时会出现中文乱码

解决办法：修改request缓冲区的编码

request.setCharacterEncoding("utf-8");

Tomcat8.5版本之后, Tomcat⾃动处理了get请求的中⽂乱码问题

Request域对象(一次请求域)

⼀次请求范围：从客户端浏览器向服务器发送⼀次请求，服务器针对这次请求对浏览器作出响应。当服

务器作出响应之后，请求对象就销毁了，保存在其中的数据就⽆效了。

⽅法                             返回值                描述

setAttribute(String name, Object obj)    void         向Request域中保存数据

request.setAttribute("name","bai");

getAttribute(String name)             Object       从Request域中获取数据

Object name = request.getAttribute("name");

System.out.println("name = " + name);

removeAttribute(String name)          void        从Request域中移除数据

request.removeAttribute("name");

****请求转发

请求转发后浏览器访问的路径就是转发后的路径，但是可以使用第一个路径中的资源

1.⽅法                            返回值             描述

getRequestDispatcher(String path)    RequestDispatcher   获得RequestDispatcher对象

RequestDispatcher requestDispatcher = request.getRequestDispatcher("/practice2");

2.⽅法                                             返回值         描述

forward(ServletRequest request, ServletResponse response)   void       进⾏请求转发

requestDispatcher.forward(request,response);

****请求转发和重定向区别

重定向：浏览器进行俩次请求

​       浏览器地址栏改变

​       重定向后的路径可以是外网

​       重定向地址需要写虚拟路径

请求转发：浏览器进行一次请求

​        浏览器地址栏不变

​        不能转发到外网

​        不需要写虚拟路径

***案例_⽤户登录注册  

在web9工程中

实例类中基本数据类型都用包装类型

第三十天

lambda表达式：一种匿名函数，没有声明的方法，即没有修饰符，没有返回值声明和名字

作用：用于简化单抽象方法接口的实现

​     可以自动识别参数类型

语法:() ->{};     

函数式接口：单抽象方法接口

函数式编程：将函数本身作为参数传递给另一个函数的编程方式，并且返回一个函数

函数式接口主要有四个

1.Supplier<T> 无输入，返回一个T类型的值

get() 获取返回值

2.Consumer<T> 输入一个T类型的值，无返回值

accept() 传入参数

3.Funtion<T,R> 输入一个T类型的值，返回一个R类型的值

apply() 获取返回值

compose()

andThen()

​    Function<Integer,Integer> fuction1 = (Integer a) -> {return a+10;};

​    Function<Integer,Integer> fuction2 = (Integer a) -> {return a*10;};

​    System.out.println(fuction1.apply(10));

​    System.out.println([fuction1.compose(fuction2).apply(10));](http://fuction1.compose(fuction2).apply(10))%3B/)

​    System.out.println(fuction1.andThen(fuction2).apply(10));

4.Predicate<T> 输入一个T类型的值，返回Ture或False

test()

negate()

and()

or()

​    Predicate<Integer> predicate2 = a -> a>1;

​    Predicate<Integer> predicate1 = (Integer a) -> a<5;

​    System.out.println(predicate1.test(4));

​    System.out.println(predicate1.negate().test(4));

​    System.out.println(predicate1.and(predicate2).test(2));

​    System.out.println(predicate1.or(predicate2).test(6));

Stream流式编程

List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);

1.串行流 单线程处理

list.stream().filter((x) -> x%2 == 1).forEach((y) -> System.out.println(Thread.currentThread().getName()+y));

2.并行流 多线程处理

list.parallelStream().filter((x) -> x%2 == 1).forEach((y) -> System.out.println(Thread.currentThread().getName()+y));

方法引用的五种方式：

User user = new User("baiyulong");

1.类名::静态方法名

Supplier<String> stringSupplier = User::get;

System.out.println(stringSupplier.get());

2.对象名::方法名

3.类名::new 引用类中的构造方法

Function<String,User> function = User::new;

System.out.println(function.apply("ssss"));

Stream流式编程的应用场景：

1.集合遍历

遍历存放普通数据类型的集合

​    List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);

​    list.stream().forEach((x) -> System.out.println(x));

​    list.stream().forEach(System.out::println);

遍历存放引用数据类型的集合

​     list1.stream().forEach(System.out::println);  方法引用

​    list1.stream().forEach(x -> System.out.println(x.getName())); lambda表达式

​    

2.list转map                                           age作为键  其他字段作为值  如果键重复，取第一个键所对应的值

Map<Integer,User> map = list1.stream().collect(Collectors.toMap(User::getAge, x->x,(k1,k2)->k1));  

System.out.println(map);  结果：{1=User{name='a'}, 2=User{name='aa'}, 3=User{name='aaa'}}

3.list分组

Map<String,List<User>> map = list1.stream().collect(Collectors.groupingBy(User::getSex));

System.out.println(map); 结果：{女=[User{name='aa'}, User{name='aaaa'}], 男=[User{name='a'}, User{name='aaa'}]}

4.list过滤                     listg过滤                 stream转list

方式一：List<User> list2 = list1.stream().filter(x->x.getSex().equals("男")).collect(Collectors.toList());   

方式二：list1.stream().filter(x->x.getSex().equals("男")).forEach(x-> System.out.println(x));

5.对某个字段进行统计

性别为男的年龄和

int sum = list1.stream().filter(x -> x.getSex().equals("男")).mapToInt(User::getAge).sum();

6.替代Runnable接口创建线程

Runnable runnable = () -> {

​      for (int i=0;i<100;i++) {

​        String name = Thread.currentThread().getName();

​        System.out.println(name);

​      }

};

new Thread(runnable).start();

第三十一天

cookie和session

web会话技术

会话：打开一个浏览器，访问一个web项目，请求该web项目中的若干个资源，关闭浏览器，这整个过程

在Servlet技术中，提供了两个⽤于保存会话数据的对象，分别是Cookie和Session。

cookie对象：记录服务器传递给浏览器的一些数据，记录浏览器访问服务器的时间和结束访问的时间

session对象：记录同一用户访问服务器的一些数据，实现该⽤户在本次会话中, 可随时获取Session域中的数据, 满⾜多次请求响应之

间进⾏数据传递\访问使⽤.

session与cookie的区别

cookie:1.用于保存服务器想要存储在客户端的数据 2.cookie在浏览器中是以文本的形式保存的

作用:

1.记录用户的登录信息

2.记录着用户第一次访问服务器的时间

3.保存上次查看的页面

Cookie的基本使⽤：

在服务端操作

1.创建cookie对象

使用Cookie类中的构造⽅法:

Cookie(String key, String value) , ⽤于创建Cookie对象, 并指定Cookie中保存的键值对信息

Cookie cookie = new Cookie("baiyulong","123456789");

2.把cookie对象返回给浏览器

使用response对象的方法：

addCookie( Cookie c ), ⽤于将指定的Cookie对象 响应回 客户端浏览器

response.addCookie(cookie);

3.获取浏览器携带的Cookie

第一步：使用request对象中的getCookie()方法，返回一个cookie对象数组

Cookie[] getCookies()  获取多个Cookie,返回的是Cookie对象数组

Cookie[] cookies = request.getCookies();

第二步：遍历cookie对象数组，使用Cookie类中俩个方法分别获取cookie对象的键和值

String getName()  获取Cookie的键

String getValue()  获取Cookie中的值

for (Cookie cookie1 : cookies) {

​      String key = cookie1.getName();

​      String value = cookie1.getValue();

​      System.out.println(key+"="+value);

}

4.在Tomcat8版本之下，Cookie中使⽤中⽂会出现乱码

解决办法：

1.使用中文之前，要先将中文进行编码，在传入cookie对象中

使用URLEncode类中的静态方法：

String encode("需要编码的数据","采⽤的编码表") 采⽤指定编码表对数据进⾏编码,返回编码后的字符串

Cookie cookie = new Cookie("baiyulong", URLEncoder.encode("白雨龙", "utf-8"));

response.addCookie(cookie);

2.获取浏览器携带的中文cookie时，要进行解码

使用URLDecode类中的静态方法：

String decode("需要解码的数据","采⽤的编码表") 采⽤指定编码表对数据进⾏解码,返回解码后的字符串

Cookie[] cookies = request.getCookies();

​    for (Cookie cookie1 : cookies) {

​      if (cookie1.getName().equals("baiyulong")) {

​        String value = URLDecoder.decode(cookie1.getValue(), "utf-8");

​        System.out.println("baiyulong=" + value);

​      } else {

​        String key = cookie1.getName();

​        String value = cookie1.getValue();

​        System.out.println(key + "=" + value);

​      }

5.设置cookie的携带路径

cookie的默认携带路径是：/web项目的虚拟路径/Servlet父类目录

设置让指定的Cookie, 可以在WEB应⽤下的任意资源都携带

cookie对象中的⽅法:

setPath("cookie的携带路径")   ⽤于设置cookie携带路径, 若参数写成 request.getContextPath() 代表web应⽤下任意资源都携带本Cookie

cookie.setPath(request.getContextPath());

6.设置cookie的存在时间

cookie默认的存在时间是：一次会话之内

使用cookie对象中的方法

setMaxAge(int 秒)  更改Cookie的⽣存时间, 参数单位: 秒

Integer.MAX_VALUE：表示整型中的最大值

7.删除已存在的Cookie

创建一个新的cookie对象，保证键和携带路径与要删除的cookie相同，把cookie的存在数据设置为0即可

​      Cookie cookie = new Cookie("byl","dddd");

​      cookie.setPath(request.getContextPath());

​      cookie.setMaxAge(0);

​      response.addCookie(cookie);

session

1.服务器端的会话技术，把同⼀⽤户与服务器多次请求响应的⼀些数据记录在服务器Session域中

2.实现该⽤户在本次会话中, 可随时获取Session域中的数据, 满⾜多次请求响应之间 进⾏数据传递\访问使⽤

3.Session的使⽤要求⽤户浏览器必须⽀持Cookie

4.30分钟之内没有使用session对象，session对象就会销毁

JsessionId

1.jsessionid是session对象的标识符,服务器是通过浏览器传递过来的cookie中的JsessionId来找到该用户对应的session对象

2.浏览器不携带jsessionid访问服务器，就相当于第一次访问服务器

每个用户第一次访问服务器，服务器都会产生一个新的session对象

3.获取到session对象后，要把session对应的jsessionid，返回给浏览器的cookie，并设置cookie的存在时间，便于浏览器下次访问服务器可以找到自己对应的session对象

Session的基本使⽤

1.获取HttpSession对象 使用request对象中的getSession()

HttpSession session = request.getSession();

2.使用HttpSession对象中的setAttribute()和getAttribute()方法存数据和取数据

session.setAttribute("byl","白雨龙");

Object byl = session.getAttribute("byl");

持久化Session对象

1.使用HttpSession对象中的getId()方法得到jsesseionid

HttpSession session = request.getSession();

String id = session.getId();

2.创建cookie对象，把得到的jsesseionid传入cookie对象中，设置cookie对象的携带路径和存在时间，并把cookie对象返回给浏览器

Cookie cookie = new Cookie("JSESSIONID",id);

cookie.setPath(request.getContextPath());    

***cookie.setMaxAge(Integer.MAX_VALUE);

response.addCookie(cookie);

session的生命周期

session创建时机

　　1：这个浏览器在servlet中第⼀次使⽤session时候,通过getSession⽅法创建；

　　2：这个浏览器第⼀次访问jsp的时候，服务器也会为这个浏览器创建⼀个session对象；

session销毁时机

　　1：程序员调⽤invalidate⽅法；（⽴刻销毁）

　　2：设置的存活时间到了；（默认是30分钟）

　　3：服务器⾮正常关闭；（突然断电）

案例 验证码 在Session和cookie课件中

第三十二天

filter和listener

filter过滤器作用：如果把web项目下的某个资源的访问网址写到filter的url-pattern中，

那么在访问该资源时，会先执行过滤器中的程序，如果过滤器放行，浏览器才可以访问到该资源

Filter的⽣命周期：过滤器对象的创建是在Tomcat启动是创建的，在服务器关闭时销毁

filter过滤器的使用：

1.创建一个类继承javax.servlet.Filter接口,重写该接口中的三个方法（ctrl i）

2.在web.xml配置文件中配置要过滤的资源地址

   <filter>

​    <filter-name>filter1</filter-name>

​    <filter-class>com.parctice.filter.RequestFilter</filter-class>

  </filter>

  <filter-mapping>

​    <filter-name>filter1</filter-name>

​    <url-pattern>/request</url-pattern>

  </filter-mapping>

3.在doFilter方法中要放行

chain.doFilter(request,response);

Filter的url-pattern配置

有三种配置方式：

1.可以写单个jsp文件或者单个servlet的访问地址

2.可以写项目路径下的某个目录  /* 表示过滤该项目下的所有资源

3.也可以过滤所有的jsp文件  /*.jsp 只有在xml中可以这么用

注解配置Filter

1.直接创建filter

2.更改@WebFilter注解中的内容 urlPatterns = "要过滤的资源"

****利用过滤统一处理中文乱码问题

1.创建一个过滤器，让其过滤所有资源

2.在过滤器的doFilter方法中处理中文乱码问题

​    req.setCharacterEncoding("utf-8");

​    resp.setContentType("text/html;charset=utf-8");

案例: 物品安全检查 filter工程中

FilterChain 过滤器链 由Tomcat引擎创建对象

作用：

1.维护过滤器执⾏顺序

2.对过滤资源进行放行

3.传递request和response对象

多个过滤器的先后执⾏顺序

1.过滤器是由web.xml配置

执行顺序：按照web.xml配置文件中url-pattern标签的先后顺序执行的

2.过滤器是由注解开发

执行顺序：按照过滤器类名的首字母顺序执行（A，B，C）

监听器Listener

作用：监听request, session, servletcontext域对象的创建和销毁

和request, session, servletcontext域对象中存储的数据变化

每一个域对象对应一个监听器

域对象             监听器

request          ServletRequestListener

session          HttpSessionListener

servletcontext     ServletContextListener

*****Servlet抽取

1.传统⽅式的开发：一个请求对应一个servlet

2.改进后的开发：以模块为单位创建servlet

开发思想：所有关于商品的请求都去访问ProductServlet,根据传递过来的参数值判断要执行ProductServlet中哪个方法

关于商品的所有方法都定义在ProductServlet中

Sevlet中执行方法的俩种办法：

1.直接调用

String method = request.getParameter("method");

​    if (method.equals("findall")) {

​      findall(request,response);

​    } else if (method.equals("add")) {

​      add(request,response);

​    }

2.使用反射调用

***this表示当前方法中的类对象

String method = request.getParameter("method");

Class aClass  = this.getClass();

​    try {

​      Method method1 = aClass.getMethod(method, HttpServletRequest.class, HttpServletResponse.class);

​      method1.invoke(this,request,response);

​    } catch (Exception e) {

​      e.printStackTrace();

​    }

3.BaseServlet抽取共性代码的开发

开发思想：把多个servlet的共性代码放到BaseServlet中，让其他servlet继承BaseServlet即可

\------------------------------------------------------------------------------------------------

BaseServlet 中的代码

@WebServlet("/base")

public class BaseServlet extends HttpServlet {

  protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

  }

  protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    //共性代码

​    String method = request.getParameter("method");

​    Class aClass = this.getClass();

​    try {

​      Method method1 = aClass.getMethod(method, HttpServletRequest.class, HttpServletResponse.class);

​      method1.invoke(this,request,response);

​    } catch (Exception e) {

​      e.printStackTrace();

​    }

  }

}

ProductServlet 中的代码

@WebServlet("/product")

public class ProductServlet extends BaseServlet {

  public void findall(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    System.out.println("findall执行了");

  }

  public void add(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    System.out.println("add执行了");

  }

}

UserServlet中的代码

@WebServlet("/user")

public class UserServlet extends BaseServlet {

  public void findall(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    System.out.println("findall执行了");

  }

  public void add(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

​    System.out.println("add执行了");

  }

}

\-----------------------------------------------------------------------------------------------

第三十三天

maven

下载地址： http://maven.apache.org/

maven的作用：用来创建和管理java项目，统一管理项目中用到的第三方jar包

Maven仓库：jar包所在位置

本地仓库：本机电脑上配置的存放jar的位置

中央仓库（远程仓库）：国外一个存放jar包的网址 网址：http://repo1.maven.org/maven2/

远程仓库（私服）：国内存放jar包的网址

Maven的坐标：jar包或其他资源的唯一标识

坐标的定义元素如下：

groupId:项⽬组织唯⼀的标识符，实际对应JAVA的包的结构

(⼀般写公司的组织名称 例如:com.baidu, com.alibaba)

artifactId: 项目（jar包，插件）名称

version：定义项⽬的当前版本

在maven要引入一个jar包，只需要在在pom.xml配置⽂件中配置该jar包的坐标即可

使用maven的步骤：

1.下载maven压缩包解压到没有中文和空格的文件夹即可

2.配置本地仓库：在apache-maven-3.6.1\conf下的settings.xml配置文件中第55行，把本地仓库的地址写进去

3.在idea中关联maven

4.使用maven下载java工程

Maven的常⽤命令

在界面右侧maven - lifecycle 下 双击执行命令

1.clear 清除target目录（存放.class文件的目录）

2.compile 对src/main/java目录下的所有java代码进行编译

3.test  执⾏src/test/java/下所有junit的测试⽤例

\4. package   如果是JavaSe的项⽬,打包成jar包

​           如果是JavaWeb的项⽬,打包成war包

5.install 把打的包安装到本地仓库

执⾏顺序: clean --> compile --> test --> package --> install

在执行install命令之前会先执行前四个命令，执行package之前会先执行前三个命令，其他同理

jar包坐标的位置：

maven仓库网址http://mvnrepository.com/

百度搜索 maven仓库

*****jar包导入：

使用方式：在pom.xml中通过<dependencies>标签导入jar包的坐标

jar包使用范围：

<scope> </scope>

1.compile 编译, 测试 打包部署有效

2.provided 编译, 测试 有效, 不会打包进去的  

在servlet jar包中要加provided 保证打包是servlet jar包不会打包进去 防止与tomcat中的servlet jar包冲突

3.test 测试有效

junit jar包要加上test 使用范围

4.runtime 编译⽆效, 测试 打包部署有效

Maven插件

****插件导入方式：在pom.xml中通过plugin标签引⼊maven的功能插件

maven3.6.1版本中tomcat插件最高版本是7

1.jdk编译插件 maven帮我们配好了

2.Tomcat7服务端的插件

tomcat7插件的坐标

<plugin>

   <groupId>org.apache.tomcat.maven</groupId>

   <artifactId>tomcat7-maven-plugin</artifactId>

   <configuration>

​     <!-- 指定端⼝ -->

​     <port>8080</port>

​     <!-- 请求路径 -->

​    <path>/</path>

  </configuration>

</plugin>

maven中开启tomcat服务：

1.在maven导入tomcat插件

2.使用tomcat插件中的tomcat:run开启tomcat服务

霈哥，您的CSS录播有个小错误，您有一次写h3 {size:20px}没起作用，您解释说是因为h3已经固定了字体大小，其实不是的，是因为不应该用size，而是font-size。

第三十四天

git

git:java项目版本控制工具

git的作用

1.在git本地仓库可以完成代码备份

2.每次修改后都会保存为一个项目版本，可以切换到上一个版本，实现代码还原

3.可以实现协同修改，如果开发者推送代码到远程仓库，出现代码冲突，可以手动解决冲突

4.多版本项目管路，通过创建分支，可以在多个版本之间进行切换

5.可以记录提交代码的编写人和编写时间

git中的一些常用命令：

1.Clone：把远程仓库的完整代码下载到本地，只在第一次获取代码时使用

2.Push：把工作区提交到本地仓库的修改和增加的代码，提交到远程仓库

3.Pull(fetch merge)：

pull命令是fetch merge俩个命令的结合

fetch:把本地仓库相比版本库的更新内容下载到本地仓库

merge:自动解决代码冲突

4.commit：把工作区提交到暂存区的更改或新增代码提交到本地仓库

5.add：把工作区更改或新增代码提交到暂存区

6.checkout：把本地仓库的代码放到工作区中

git下载地址：国外官网地址： https://git-scm.com/download

​          国内地址：https://npm.taobao.org/mirrors/git-for-windows/

Git远程仓库

需要使用代码托管服务来创建git远程仓库

常⽤的托管服务:github,码云，gitlab

码云的注册地址：https://gitee.com/signup

Idea中使⽤Git

1.在idea中关联git  File | Settings | Version Control | Git  导入git的安装路径

init：初始化

feature:新特性

霈哥远程仓库位置：https://gitee.com/likepei/git-project_006.git

第三十五天

Mybatis框架

MyBatis官⽹地址：https://mybatis.org/mybatis-3/

Mybatis框架做了什么？

封装了jdbc底层代码，可以自动实现参数映射和结果映射

我们可以利用Mybatis框架干什么？

与数据库进行交互

Mybatis 架构

1俩个配置文件

SqlMapConfig.xml:核心配置文件，配置了数据库的运行环境，连接数据所需要的数据

Mapper.xml：存放sql语句的配置文件

2.SqlSessionFactory：会话⼯⼚，创建会话

3.sqlSession：会话，用来执行sql语句

4.Executor接⼝：有两个实现，⼀个是基本执⾏器BaseExecutor、⼀个是缓存执⾏器CachingExecutor。

\5. MappedStatement：底层封装对象，它包装了mybatis配置信息及sql映射信息等

自动实现参数映射和结果映射

Mybatis增删改查操作

****//在执行增删改时需要提交事务

1.增

配置文件中内容

<insert id="insert" parameterType="com.practice.pojo.User">

​    insert into user values(#{id},#{username},#{sex},#{address})

​    <selectKey keyProperty="id" resultType="Integer" order="AFTER">

​       select LAST_INSERT_ID()

​    </selectKey>

</insert>

注意：<selectKey keyProperty="id" resultType="Integer" order="AFTER">

​       select LAST_INSERT_ID()

​    </selectKey>

作用：打印用户对象中的id时，可以打印出插入记录的id值

测试类中的代码

@Test

  public void insert() throws IOException {

​    InputStream resourceAsStream = Resources.getResourceAsStream("SqlMapConfig.xml");

​    SqlSessionFactory build = new SqlSessionFactoryBuilder().build(resourceAsStream);

​    SqlSession sqlSession = build.openSession();

​    User user = new User();

​    user.setUsername("李七");

​    user.setSex("男");

​    user.setAddress("澳门");

​    sqlSession.insert("userMapper.insert",user);

​    //在执行增删改时需要提交事务

​    [sqlSession.commit();](http://sqlsession.commit()%3B/)

​    //获取插入记录的id

​    System.out.println(user.getId());

​    sqlSession.close();

  }

2.删

<delete id="deleteById" parameterType="Integer">

​    delete from user where id=#{id}

</delete>

@Test

  public void delete() throws IOException {

​    InputStream resourceAsStream = Resources.getResourceAsStream("SqlMapConfig.xml");

​    SqlSessionFactory build = new SqlSessionFactoryBuilder().build(resourceAsStream);

​    SqlSession sqlSession = build.openSession();

​    Integer integer = 8;

​    sqlSession.delete("userMapper.deleteById",integer);

​    [sqlSession.commit();](http://sqlsession.commit()%3B/)

​    sqlSession.close();

  }

3.改

<update id="update" parameterType="com.practice.pojo.User">

​    update user set username=#{username}, sex=#{sex}, address=#{address}

​    where id=#{id}

</update>

@Test

  public void updateById() throws IOException {

​    InputStream resourceAsStream = Resources.getResourceAsStream("SqlMapConfig.xml");

​    SqlSessionFactory build = new SqlSessionFactoryBuilder().build(resourceAsStream);

​    SqlSession sqlSession = build.openSession();

​    User user = new User();

​    user.setId(6);

​    user.setUsername("赵八");

​    user.setSex("女");

​    user.setAddress("石家庄");

​    sqlSession.update("userMapper.update",user);

​    [sqlSession.commit();](http://sqlsession.commit()%3B/)

​    sqlSession.close();

  }

4.查   查询时，关键字自动忽略大小写

<select id="selectById" parameterType="Integer" resultType="com.practice.pojo.User">

​    select * from user where id=#{id}

</select>

@Test

  public void selectById() throws IOException {

​    InputStream resourceAsStream = Resources.getResourceAsStream("SqlMapConfig.xml");

​    SqlSessionFactory build = new SqlSessionFactoryBuilder().build(resourceAsStream);

​    SqlSession sqlSession = build.openSession();

​    User user = sqlSession.selectOne("userMapper.selectById", 1);

​    System.out.println(user);

​    sqlSession.close();

  }

Mybatis映射配置⽂件

1). namespce 与SQL语句的ID组合起来成为SQL的唯⼀标识

2).  <insert> , <delete> , <update> <select> 标签分别⽤来表示增删改查的操作 。

3). resultType 属性表示结果集映射中的单条记录所需要映射的类型 。

4). parameterType 属性指SQL语句需要传⼊的参数类型，

Mybatis核⼼配置⽂件

configuration

   |- properties（属性） 标签属性：resource

   |- settings（全局配置参数）

   |- typeAliases（类型别名）

   |- typeHandlers（类型处理器）

   |- objectFactory（对象⼯⼚）

   |- plugins（插件）

   |- environments（环境集合属性对象）

   |- environment（环境⼦属性对象）

​     |- transactionManager（事务管理）

​     |- dataSource（数据源）

   |- mappers（映射器）

标签的顺序是固定，必须按照顺序来写

常用标签

1.properties  关联数据库配置信息

<properties resource="jdbc.properties"/>

2.typeAliases 设置别名

为单个文件设置别名

<typeAliases>

  <typeAlias type="com.kkb.pojo.User" alias="user"></typeAlias>

</typeAliases>

为某个目录下的所有文件设置别名

<typeAliases>

<package name="com.kkb.pojo"/>

</typeAliases>

3.mappers 加载映射文件

A. <mapper resource="" />

使⽤相对于类路径的资源

如：<mapper resource="UserMapper.xml" />

B. <mapper class=" " />

使⽤mapper接⼝类路径

如：<mapper class="com.kkb.mapper.UserMapper"/>

注意：此种⽅法要求mapper接⼝名称和mapper映射⽂件名称相同，且放在同⼀个⽬录中。

C. <package name=""/>

注册指定包下的所有mapper接⼝

如：<package name="com.kkb.mapper"/>

注意：此种⽅法要求mapper接⼝名称和mapper映射⽂件名称相同，且放在同⼀个⽬录中

Mybatis核⼼API

\1. Resources ⼯具类

InputStream inputStream = Resources.getResourceAsStream("SqlMapConfig.xml");

2.SqlSessionFactoryBuilder

SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);

3.SqlSessionFactory

会默认开启⼀个事务

openSession()

opSession(boolean autocommit) 可以设置自动提交

4.SqlSession

<T> T       selectOne(String statement, Object parameter) ；

<E> List<E>  selectList(String statement, Object parameter) ；

int         insert(String statement, Object parameter)

int         update(String statement, Object parameter)

int         delete(String statement, Object parameter)

void commit() ;

void rollback() ;

Mybatis 的Mapper代理⽅式开发

在java目录下：创建一个mapper接口

接口定义的规范：

1.接口的类名和包名应与映射文件的相同

2.映射文件中的namespce属性值应写接口的完整名

3.接口中定义的方法名应与映射文件中的对应sql语句的id值相同

4.接口方法中传入参数类型应与sql语句中parameterType属性值相同

注意：如果接口方法中传入参数类型是集合，那parameterType值应写集合泛型

5.接口方法返回值类型应与sql语句中resultType属性值相同

注意：如果接口方法返回值是集合，那么resultType属性应写集合泛型

SqlSession工具类

\------------------------------------------------------------------------------------------------------------

public class SqlSessionUtils {

  private static SqlSessionFactory sqlSessionFactory;

  static {

​    try {

​      InputStream resourceAsStream = Resources.getResourceAsStream("mybatis-config.xml");

​      sqlSessionFactory = new SqlSessionFactoryBuilder().build(resourceAsStream);

​    } catch (IOException e) {

​      e.printStackTrace();

​    }

  }

  private SqlSessionUtils(){

  }

  public static SqlSession openSession() {

​    return sqlSessionFactory.openSession(true);

  }

}

\--------------------------------------------------------------------------------------------------------------

使用步骤：

1.使用SqlSession工具类创建SqlSession对象

2.使用SqlSession对象中的getMapper(接口.class),创建接口对象

UserDao userdao = sqlSession.getMapper(UserDao.class);

3.使用接口对象中定义的方法即可实现增删改查

4.释放资源

sqlSession.close();

Mybatis 动态SQL

1.多条件查询(where标签和if标签)

<select id="selectByCondition" parameterType="user" resultType="user">

​    <include refid="samesql"></include>        //sql片段提取

​    <where>

​      <if test="username != null">

​        and username=#{username}

​      </if>

​      <if test="sex != null">

​        and sex=#{sex}

​      </if>

​      <if test="address != null">

​        and address=#{address}

​      </if>

​    </where>

</select>

2.根据ID批量查询⽤户信息(where标签和froeach标签)

<select id="selectByIds" parameterType="integer" resultType="user">

​    <include refid="samesql"></include>    

​    <where>

​      <foreach collection="collection" open="id in(" close=")" item="id" separator=",">

​        \#{id}

​      </foreach>

​    </where>

</select>

foreach标签中的属性介绍

属性             含义

collection        代表要遍历的集合元素，注意编写时不要写#{} ；

open           代表语句的开始部分

close           代表结束部分

item           接收遍历元素的变量名

separator       代表分隔符,每⼀次循环都需要拼接该分割符

注意：

如果传递的参数为List , collection中可写的值为 list, collection ;

如果传递的参数为Set , collection中可写的值为 collection ;

如果传递的参数为数组 , collection中可写的值为 array ;

SQL⽚段抽取：将重复的 sql 提取出来，使⽤时⽤ include 引⽤即可

提取重复sql语句用sql标签

<sql id="samesql">

​    select id,username,sex,address from user

</sql>

引用sql标签中的sql片段用include标签

<include refid="sql标签中的id值"></include>

Mybatis 分⻚助⼿ PageHelper

使用步骤：

1.导入依赖坐标

2.在核心配置文件中配置PageHelper插件

<plugins>

​    <plugin interceptor="com.github.pagehelper.PageInterceptor" />

</plugins>

3.分⻚代码实现

设置分页参数：

PageHelper.startPage(page,size);

参数: page 代表查询的⻚⾯ ; size 代表每⻚返回的记录数 ;

获得分⻚结果：

方式一：

PageInfo<User> pageInfo = new PageInfo<User>(userList);

System.out.println("总条数："+pageInfo.getTotal());

System.out.println("总⻚数："+pageInfo.getPages());

System.out.println("当前⻚："+pageInfo.getPageNum());

System.out.println("每⻚显示⻓度："+pageInfo.getPageSize());

System.out.println("是否第⼀⻚："+pageInfo.isIsFirstPage());

System.out.println("是否最后⼀⻚："+pageInfo.isIsLastPage())

方式二、

Page page = (Page) userList;

System.out.println("总条数：" + page.getTotal());

System.out.println("总⻚数：" + page.getPages());

//打印当前⻚结果数据

for (User user : result) {

List<User> result = page.getResult();

System.out.println("user = " + user);

}

Mybatis 多表关系

注意事项：

1.核心配置文件中不能写没有用到的东西，例如：如果没有导入日志文件的.properties文件，那就不能导入日志插件

2.核心配置文件中有关数据库的信息站位符用  ${}

3.在映射配置文件中占位符用 #{}

4.一对多查询和多对多查询中，如果俩个表有同名的列，需要为副表中的同名列设置别名

5.在插入操作中返回当前插入记录的自增长主键值 用到的sql语句：select last_insert_id()     last_insert_id是一个函数

1.⼀对⼀查询(一个表中的一条记录对应另一个表中的一条记录)

映射文件中的代码：

\---------------------------------------------------------------------

<resultMap id="ordersMap" type="orders">               //type:结果映射的pojo类型

​    <id column="id" property="id" />                   //主键列用id标签.，其他列用result标签

​    <result column="ordertime" property="ordertime"/>    //column:表中列的名称  property:对应的映射类的字段名

​    <result column="total" property="total" />

​    <result column="userid" property="userid" />

​    <association property="user" javaType="user">        //为映射类中单个实体类对象字段赋值，property;映射类中实体类字段名称  javaType:实体类字段类型

​      <id column="id" property="id" />

​      <result column="username" property="username"/>

​      <result column="sex" property="sex"/>

​      <result column="address" property="address"/>

​    </association>

</resultMap>

<select id="selectByOrdersWithUser" resultMap="ordersMap">

​    select * from orders o,user u where o.userid=u.id

</select>

\---------------------------------------------------------------------------

一对多查询(一个表中的一条记录对应另一个表中的多条记录)

\---------------------------------------------------------------------------------------------------------------------------------------

<resultMap id="userMap" type="user">

​    <id column="id" property="id"/>

​    <result column="username" property="username"/>

​    <result column="sex" property="sex"/>

​    <result column="address" property="address"/>

​    <collection property="list" ofType="orders">          //为映射类中的实体对象集合赋值，property:映射类中集合字段名 ofType:集合中存放的对象类型

​      <id column="oid" property="id"/>

​      <result column="ordertime" property="ordertime"/>

​      <result column="total" property="total"/>

​      <result column="userid" property="userid"/>

​    </collection>

</resultMap>

<select id="selectByUserWithOrders" resultMap="userMap">

​    select u.id,u.username,u.sex,u.address,o.id oid,o.ordertime,o.total,o.userid from user u left join orders o on u.id=o.userid

</select>

\---------------------------------------------------------------------------------------------------------------------------------------------

多对多查询(一个表中的一条记录对应另一个表中的多条记录，另一个表中的一条记录也同样对应表中的多条记录)

\----------------------------------------------------------------------------

<resultMap id="userMap" type="user">

​    <id column="id" property="id"/>

​    <result column="username" property="username"/>

​    <result column="sex" property="sex"/>

​    <result column="address" property="address"/>

​    <collection property="list" ofType="role">

​      <id column="rid" property="id"/>

​      <result column="rolename" property="rolename"/>

​    </collection>

</resultMap>

<select id="selectByUserWithRole" resultMap="userMap">

​    select u.id,u.username,u.sex,u.address,r.id rid,r.rolename

​    from user u left join user_role ur on u.id=ur.userid

​    left join role r on r.id=ur.roleid

</select>

\-----------------------------------------------------------------------------

****************************

resultMap 与 resultType区别：

1.resultMap:结果映射类中有集合字段或者实体类字段，用resultMap高级映射

2.resultType：结果映射类中只有普通字段，用resultType普通映射

association 与 collection的区别

1.association：为单个实体对象字段赋值 对象类型放在javaType属性中

2.collection：为实体对象集合字段赋值  集合中的对象类型放在ofType属性中

************************

Mybatis 注解开发

***注意：在mybatis核心配置文件中加载的是Mapper接口

MyBatis的常⽤注解

序号         注解              含义

1           @Insert       类似于<insert>标签,⽤于声明插⼊操作

2          @Update      类似于<update>标签,⽤于声明更新操作

3          @Delete       类似于<delete>标签,⽤于声明删除操作

4           @Select      类似于<select>标签,⽤于声明查询操作

5           @Param      如果你的dao接⼝⽅法的形参有多个，需要使用Param注解为参数命名，该名称需要与Sql语句中占位符中对应的名称相同

6          @SelectKey    返回自增长主键的值

7           @Result      实现结果集封装 类似于,id ,result 标签

8          @Results      可以与@Result ⼀起使⽤，封装多个结果集, 类似于替换 <resultMap>标签

9          @One        实现⼀对⼀结果集封装, 类似于association 标签

10          @Many      实现⼀对多结果集封装, 类似于collection标签

\------------------------------------------------------------------

基本增删改查

public interface UserDao {

   //插入操作，并返回主键值

  @Insert("insert into user values(#{id},#{username},#{sex},#{address})")

  @SelectKey(keyProperty = "id",resultType = Integer.class,statement = "select last_insert_id()",before = false)  注意：resultType属性值：返回值类型的class对象

  void Insert(User user);

  //更新

  @Update("update user set username=#{username} where id=#{id}")

  void Update(User user);

  //删除

  @Delete("delete from user where id=#{id}")

  void delete(Integer id);

  //多参数删除

  @Delete("delete from user where id=#{id} and username=#{username}")

  void delete1(@Param("id") Integer id , @Param("username") String username);

  //查询

  @Select("select u.id,u.username,u.sex,u.address from user u")

  List<User> select();

}

\--------------------------------------------------------------------

使用注解实现一对一查询

注意：简单字段可以自动进行映射(只需字段名和表中列名相同)

\------------------------------------

public interface OrdersDao {

  @Select("select * from orders") //第一步：先查询出主表中的所有字段

   

  @Results({

​       //为复杂字段进行映射

​      @Result(property = "user",javaType = User.class,column = "userid",  //Properties:映射类中的复杂字段名 javaType:复杂字段的class对象 

​                                                           //column：主表与副表关联的表中列名，传递给副表作为查询条件的关联列名

​      one=@One(                                            // 为单个对象进行映射，相当于association 标签                                

​          fetchType = FetchType.LAZY,                           //设置延迟加载

​          select = "com.practice.dao.UserDao.select"                //select:副表执行sql语句的方法，在副表定义的mapper接口中定义的查询方法

​      )

​      )

  })

  List<Orders> selectAll();

}

public interface UserDao {

  @Select("select u.id,u.username,u.sex,u.address from user u where id=#{id}")

  User select(Integer userid);

}

\----------------------------------

一对多查询-

\-------------------------------------------------------------------------

public interface UserDao {

  @Select("select * from user")

  @Results({

​      @Result(column = "id",property = "id"),     注意：//主表作为参数传入副表的列，不会自动赋值，需要手动赋值

​      @Result(property = "list",javaType = List.class,   注意：此处要写集合的class对象   properties:复杂字段的名 javaType：复杂字段的class对象

​          column = "id",

​          many = @Many(                   //many:为多个对象赋值

​              fetchType = FetchType.LAZY,

​              select = "com.practice.dao.OrdersDao.select"

​          )

​      )

  })

  List<User> selectAll();

}

public interface OrdersDao {

  @Select("select * from orders where userid=#{id}")

  Orders select(Integer id);

}

\-----------------------------------------------------------------------

多对多

\----------------------------------------------------------------------

public interface UserDao {

  @Select("select * from user")

  @Results({

​      @Result(column = "id",property = "id"),

​      @Result(

​          property = "list",javaType = List.class,column = "id",

​          many = @Many(

​              fetchType = FetchType.LAZY,

​              select = "com.practice.dao.RoleDao.select"

​          )

​      )

  })

  List<User> select();

}

public interface RoleDao {

  @Select("select * from role r,user_role ur where r.id=ur.roleid and ur.userid=#{id}")  //用内连接查询role和user_role 俩个表  基于主表传过来的id值

  Role select();

\-----------------------------------------------------------------------

第三十六天

Spring框架

Spring官⽹地址：https://spring.io/

Spring：以ioc(Inverse Of Contro)反转控制和aop(Aspect Oriented Programming)面向切面编程为核心，提供了展现层Spring mvc和持久层spring jdbc 以及业务层事务管理等众多企业应用技术，还可以整合众多著名的第三方框架。

控制反转IoC

ioc:是一种思想，把创建对象的从java代码中剥离出去，交给spring仓库工厂去创建

IoC的作⽤：降低代码间的依赖关系，减少程序中的耦合

Spring的IoC⼊⻔

Spring中IoC的配置，⽀持纯XML配置或者纯注解配置以及XML和注解混合配置这三种⽅式

Bean标签的对象获取：getBean⽅法

1.getBean("id值") 返回object类型的对象

2.getBean(接口.class) 返回的是接口实现类对象 注意：接口只有一个实现类时，才能用这种方式

AccountService bean = applicationContext.getBean(AccountService.class);

3.getBean("id值",接口.class) 返回接口实现类对象

AccountService accountService = applicationContext.getBean("accountService", AccountService.class)

Bean标签的作⽤和属性

作用：把需要创建对象的类完整类名写到bean标签中，让spring完成对象的创建

​     默认调用的是无参构造方法

​     

bean标签中的属性：

id： 对象在spring容器中的唯一标识

class： 指定类的全限定类名。⽤于反射创建对象。默认情况下调⽤⽆参构造函数。

init-method： 指定类中的初始化⽅法名称。 初始化方法：对象创建好后执行的方法

Spring的依赖注⼊(DI)：Dependency Injection

依赖注入：让spring框架为bean标签中的对象属性赋值， 它是spring 框架核⼼ ioc 的具体实现.

spring框架为对象属性赋值的方式：

方式一：使用有参构造进行赋值   前提是：必须有有参构造方法

使用的是constructor-arg标签

标签属性：name :参数名称

​        value:参数值，只能为基本数据类型和String赋值

​      ***ref:为其他引用类型赋值，而且该引用类型必须在bean标签中配置过

<bean id="date" class="java.util.Date"></bean>        

<bean id="accountService" class="com.practice.service.impl.AccountServiceImpl" init-method="init">

​       <constructor-arg name="name" value="白雨龙"></constructor-arg>

​       <constructor-arg name="age" value="11"></constructor-arg>

​       <constructor-arg name="date" ref="date"></constructor-arg>  //ref:Date类型在bean标签中的id值

</bean>

方式二：使用set方法进行赋值  前提是：属性必须有set方法和无参构造方法

用到的标签是property

标签属性：name :参数名称

​        value:参数值，只能为基本数据类型和String赋值

​      ***ref:为其他引用类型赋值，而且该引用类型必须在bean标签中配置过

​      

为类中集合和数组字段传值： 使用set⽅法

array , list , set 这三个标签通⽤

为整型数组赋值

<property name="integers">

​      <array>

​        <value>1</value>

​        <value>2</value>

​        <value>3</value>

​      </array>

为list集合赋值

</property>

​    <property name="list">

​      <list>

​        <value>bai</value>

​        <value>ba</value>

​        <value>ba</value>

​      </list>

</property>

为set集合赋值

<property name="set">

​      <set>

​        <value>1</value>

​        <value>1</value>

​        <value>3</value>

​      </set>

</property>

为map集合赋值

<property name="map">

​      <map>

​        <entry key="1" value="sdds"></entry>

​        <entry key="1" value="ddddd"></entry>  //map集合键相同时，值覆盖

​        <entry key="2" value="ddddd"></entry>

​      </map>

</property>

spring和mybatis联合开发

一、纯xml开发(crud)   具体代码在D:\byljavaprogram\spring\spring2 项目中

spring核心配置文件内容：

\----------------------------------------------------------------

<?xml version="1.0" encoding="UTF-8"?>

<beans xmlns="http://www.springframework.org/schema/beans"

​    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

​    xmlns:context="http://www.springframework.org/schema/context"

​    xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd http://www.springframework.org/schema/context https://www.springframework.org/schema/context/spring-context.xsd">

​    

  <!--加载jdbc属性⽂件-->

  <context:property-placeholder location="classpath:jdbc.properties" />

  <!--配置数据源-->

  <bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">

​    <!--驱动, url, ⽤户名,密码-->

​    <property name="driverClassName" value="${jdbc_driver}"/>

​    <property name="url" value="${jdbc_url}"/>

​    <property name="username" value="${jdbc_username}"/>

​    <property name="password" value="${jdbc_password}"/>

  </bean>

  

  <!--配置SqlSessionFactory-->

  <bean id="sqlSessionFactory"

​     class="org.mybatis.spring.SqlSessionFactoryBean">

​    <!--关联数据源-->

​    <property name="dataSource" ref="druidDataSource"/>   //ref的值是配置数据源中的id值

​    <!--设置pojo的别名-->

​    <property name="typeAliasesPackage" value="com.practice.pojo"/>  //别名设置未生效

  </bean>

  

  <!--配置Mapper映射扫描, 扫描所有的Mapper.xml⽂件与 ⽣成dao接⼝的实现类对象存到IOC容

  器中-->

  <bean id="scannerConfigurer"

​     class="org.mybatis.spring.mapper.MapperScannerConfigurer">

  <!--可省略-->

  <property name="sqlSessionFactoryBeanName" value="sqlSessionFactory"/>  //value属性值是SqlSessionFactory配置中的id值

  <!--dao映射扫描-->

  <property name="basePackage" value="com.practice.dao"/>

  </bean>

  

  <!--service-->

  <bean id="accountService" class="com.practice.service.impl.AccountServiceImpl">

​    <!--依赖注⼊dao-->

​    <property name="accountDao" ref="accountDao"/>

  </bean>

</beans>

\---------------------------------------------------------------

Spring中的注解

***注意：使用注解时，必须在核心配置文件中打开注解扫描

<context:component-scan base-package="扫描的路径"></context:component-scan>

1.代替bean标签的注解 @Component

注解属性value：bean标签的id属性

***不指定value属性，默认就是类名或接口名，⾸字⺟⼩写

如果接口有一个实现类，注解可以写在接口，也可以卸载实现类

如果接口有多个实现类，注解写在实现类

@Controller,@Service,@Repository，⽤法和@Componet⼀致，分别用在控制层，业务层，持久层

2.依赖注⼊注解 （写在字段上方）

为类中接口字段赋值时，

接口有一个实现类时，用@Autowired注解

接口有多个实现类时，用@Autowired加@Qualifier("id") 或者直接用@Resource(name="Id")

3.使用注解让测试类加载spring核心配置文件 这样就可以在测试类中使用注解实现依赖注入

@RunWith(SpringJUnit4ClassRunner.class)

@ContextConfiguration(locations = {"classpath:beans.xml"}) 加载xml文件

@ContextConfiguration(classes = SpringConfig.class)      加载配置类

二、半注解半xml开发

自定义的类用注解导入spring库

使用注解实现依赖注入

在测试类中使用注解加载核心配置文件

\---------------------------------------------------------------------------

spring核心配置文件中的内容

<?xml version="1.0" encoding="UTF-8"?>

<beans xmlns="http://www.springframework.org/schema/beans"

​    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

​    xmlns:context="http://www.springframework.org/schema/context"

​    xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd http://www.springframework.org/schema/context https://www.springframework.org/schema/context/spring-context.xsd">

  <!--加载属性⽂件-->

  <context:property-placeholder location="classpath:jdbc.properties" />

  <!--配置数据源-->

  <bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">

​    <!--驱动, url, ⽤户名,密码-->

​    <property name="driverClassName" value="${jdbc_driver}"/>

​    <property name="url" value="${jdbc_url}"/>

​    <property name="username" value="${jdbc_username}"/>

​    <property name="password" value="${jdbc_password}"/>

  </bean>

  <!--配置SqlSessionFactory-->

  <bean id="sqlSessionFactory"

​     class="org.mybatis.spring.SqlSessionFactoryBean">

​    <!--关联数据源-->

​    <property name="dataSource" ref="druidDataSource"/>

​    <!--设置pojo的别名-->

​    <property name="typeAliasesPackage" value="com.practice.pojo"/>

  </bean>

  <!--配置Mapper映射扫描, 扫描所有的Mapper.xml⽂件与 ⽣成dao接⼝的实现类对象存到IOC容

  器中-->

  <bean id="scannerConfigurer"

​     class="org.mybatis.spring.mapper.MapperScannerConfigurer">

  <!--可省略-->

  <property name="sqlSessionFactoryBeanName" value="sqlSessionFactory"/>

  <!--dao映射扫描-->

  <property name="basePackage" value="com.practice.dao"/>

  </bean>

  <!--service-->

  <context:component-scan base-package="com.practice.service"></context:component-scan>

</beans>

\------------------------------------------------------------------------------------------------------------

三、纯注解开发

@Configuration :标识当前类是Spring的⼀个配置类

@ComponentScan：替代xml中的 <context:component-scan/> 开启注解扫描标签

@Import:把副配置类引入到主配置类中,被引⼊的配置类可以不加@Configuration注解

@PropertySource：引⼊外部properties⽂件，注意文件名前面要加classpath:文件名

@Value：对配置类中成员变量赋值

@Bean("id)：将⼀个⽅法的返回值对象加⼊到Spring的容器当中管理   如果不加id，默认以方法返回值首字母小写为id值

@Qualifier：为方法的参数进行依赖注入

***注意：如果要从spring容器中取值，就可以使用依赖注入

\--------------------------------------------------------------

JdbcConfig 有关数据的配置类

@PropertySource("classpath:jdbc.properties")   //引入Properties配置文件

public class JdbcConfig {

  @Value("${jdbc_driver}")   //把配置文件的内容赋值给类字段

  private String jdbc_driver;

  @Value("${jdbc_url}")

  private String jdbc_url;

  @Value("${jdbc_username}")

  private String jdbc_username;

  @Value("${jdbc_password}")

  private String jdbc_password;

  @Bean("druidDataSource")       //把druidDataSource对象加入到spring容器中

  public DruidDataSource creatDruidDataSource() {

​    DruidDataSource druidDataSource = new DruidDataSource();

​    druidDataSource.setDriverClassName(jdbc_driver);

​    druidDataSource.setUrl(jdbc_url);

​    druidDataSource.setUsername(jdbc_username);

​    druidDataSource.setPassword(jdbc_password);

​    return druidDataSource;

  }

}

\--------------------------------------------------------------------------------

\---------------------------------------------------------------------------------------------------------------------

Mybatis的配置类

public class MybatisConfig {

  @Bean("sqlSessionFactoryBean")   //把sqlSessionFactoryBean对象加入到spring容器中

  public SqlSessionFactoryBean creatSqlSessionFactoryBean(@Qualifier("druidDataSource") DruidDataSource druidDataSource) {  //为方法参数进行依赖注入

​    SqlSessionFactoryBean sqlSessionFactoryBean = new SqlSessionFactoryBean();

​    sqlSessionFactoryBean.setDataSource(druidDataSource);           //为DataSource字段进行赋值，需要传入一个连接池对象

​    sqlSessionFactoryBean.setTypeAliasesPackage("com.practice.pojo");  //为com.practice.pojo包下的类起别名

​    return sqlSessionFactoryBean;

  }

  @Bean("mapperScannerConfigurer")  //把mapperScannerConfigurer对象加入到spring容器中

  public MapperScannerConfigurer creatMapperScannerConfigurer() {  

​    MapperScannerConfigurer mapperScannerConfigurer = new MapperScanner Configurer();  

​    mapperScannerConfigurer.setBasePackage("com.practice.dao");   //扫描com.practice.dao包下的所有文件

​    return mapperScannerConfigurer;

  }

}

\----------------------------------------------------------------------------------------------------------

第三十七天

Spring框架3

AOP的相关概念

AOP：一种编程思想，把重复性代码提取出来放到切面类中，在需要执行的时候，通过注解或者配置文件的方式执行切面类中的增强方法，实现对已有代码的增强

AOP优势：1.代码独立性强  2.减少了重复了代码，提高开发效率  3.代码易于维护

AOP应⽤场景：过滤器，记录访问⽇志，统计⽅法执⾏效率，判断⽤户的访问权限，事务操作

Aop中的术语：

连接点：可以加入增强代码的方法的前后位置

切入点：增强代码执行的位置

切面：增强代码可以加入的多个类形成的面

***类中每一个方法是一个连接点，多个连接点成线，每个类是一条线，线成面，叫切面

目标对象：加入增强代码的方法

代理：增强代码所在类

切⼊点表达式：指的是遵循特定语法结构的字符串，其作⽤是⽤于对符合语法格式的连接点进⾏增强

关键字 ：execution ⽤于匹配⽅法执⾏的连接点

语法结构：execution(方法修饰符 方法返回值 包名.类名.方法名(参数))

注意：1.方法修饰符可省略

​     2.返回值可以使⽤*，表示任意返回值

​     3.包名可以使⽤".."表示当前包及其⼦包

​     4.类名和⽅法名，都可以使⽤*，表示任意类，任意⽅法

​     5.参数列表，可以使⽤具体类型  

​       基本类型直接写类型名称 ： int

​       引⽤类型必须写全限定类名：java.lang.String

​     6.参数列表可以使⽤*，表示任意参数类型，但是必须有参数

​     7.参数列表可以使⽤..，表示有⽆参数均可。有参数可以是任意类型

​     

aop配置中的标签：

1.aop:config标签   开始aop配置的标签

2.aop:aspect标签   配置切面的标签

属性：id：切面的唯一标识

​     ref:切面多对应的代理类id

​     order:为切面设置优先级 值只能去整数，值越小优先级越高

3.aop:pointcut标签 ⽤于配置通⽤切⼊点表达式

属性：id：表达式唯一标识

​     expression：属性值写切面表达式     

注意： 出现在aop:config标签内部要求必须在所有aop:aspect标签之前。它可以供所有切⾯使⽤

​      出现在aop:aspect标签内部，它没有顺序要求，但只能供当前切⾯使⽤

\4. JoinPoin类：

方法：getArgs() 获取切入点方法的参数  在前置通知中可以用来获取参数

Throwable类：Exception类的父类  是一个异常类

方法：printStackTrace() 打印异常信息

ProceedingJoinPoint类：JoinPoin的子类

方法：proceed(Objece[ ] orgs)  用于执行业务方法

​      

5..五种通知标签

前置通知：aop:before标签

属性：method：⽤于指定前置通知的⽅法名称

​     pointcut：⽤于指定切⼊点表达式

​     pointcut-ref：⽤于指定切⼊点表达式的id值

<aop:before method="beforePrintLog" pointcut-ref="pc1"></aop:before>-->     

对应的代理类中的增强方法：

public void beforePrintLog(JoinPoint joinPoint) throws Throwable {

​    Object[] args = joinPoint.getArgs();

​    System.out.println("前置通知"+ Arrays.toString(args));

  }

  

后置通知：aop:after-returning标签

属性：

​     method:⽤于指定后置通知的⽅法名称

​     pointcut:⽤于指定切⼊点表达式

​     pointcut-ref:⽤于指定切⼊点表达式的id值

​     returning:指定一个Objece变量来接收返回值   可以设定一个变量来接收切入点方法返回值

<aop:after-returning method="returningPrintLog" returning="reValus" pointcut-ref="pc1"></aop:after-returning>

对应的代理类中的增强方法：  

public void returningPrintLog(JoinPoint joinPoint ,Object reValus) throws Throwable {   //传入一个Object类型的对象来表示返回值

​    System.out.println("后置通知"+reValus);

  }    

  

异常通知：aop:after-throwing

属性：

​     method:⽤于指定异常通知的⽅法名称

​     pointcut:⽤于指定切⼊点表达式

​     pointcut-ref:⽤于指定切⼊点表达式的id值

​     throwing:⽤于指定异常通知中异常的变量名称(变量类型是Throwable)

<aop:after-throwing method="throwingPrintLog" pointcut-ref="pc1" throwing="t"></aop:after-throwing>  //通过throwing属性来定义一个异常变量

对应的代理类中的增强方法：

public void throwingPrintLog(JoinPoint joinPoint,Throwable t) throws Throwable {  //传入一个Throwable对象来表示异常变量

​    t.printStackTrace();

​    System.out.println("异常通知");

  }

​      

最终通知：aop:after标签

属性：method:⽤于指定最终通知的⽅法名称

​     pointcut:⽤于指定切⼊点表达式

​     pointcut-ref:⽤于指定切⼊点表达式的id值

<aop:after method="afterPrintLog" pointcut-ref="pc1"></aop:after>

对应的代理类中的增强方法：

public void afterPrintLog(JoinPoint joinPoint) throws Throwable {

​    System.out.println("最终通知");

  }    

​     

环绕通知：aop:around    用代码来配置方法执行的先后顺序，把前四种通知进行整合 通过编码方式控制增强代码何时执行

属性；

​    method:⽤于指定环绕通知的⽅法名称

​    pointcut:⽤于指定切⼊点表达式

​    pointcut-ref:⽤于指定切⼊点表达式的引⽤

<aop:around method="aroundPrintLog" pointcut-ref="pc1"></aop:around> 

对应的代理类中的增强方法：其他四个方法也需要创建，在环绕方法中调用其他四个方法，来控制执行的先后顺序

ublic Object aroundPrintLog(ProceedingJoinPoint proceedingJoinPoint) throws Throwable {

​    Object result = null;

​    try {

​      //执行前置通知

​      this.beforePrintLog(proceedingJoinPoint);

​      //执行业务方法

​      Object[] args = proceedingJoinPoint.getArgs();

​      result = proceedingJoinPoint.proceed(args);

​      //执行后置通知

​      this.returningPrintLog(proceedingJoinPoint, result);

​    } catch (Throwable e) {

​      e.printStackTrace();

​      //执行异常通知

​      this.throwingPrintLog(proceedingJoinPoint, e);

​    } finally {

​      //执行最终通知

​      this.afterPrintLog(proceedingJoinPoint);

​    }

​    return result;

  }

}

注意：异常通知和后置通知只执行一个，切入点方法不报异常，执行后置通知，反之执行异常通知

​     最终通知是肯定会执行的

基于注解的AOP配置   

用到的注解：

1.@EnableAspectJAutoProxy: 开启spring对注解aop的⽀持

2.@Aspect:声明当前类是⼀个切⾯类。

3.@Pointcut :⽤于指定切⼊点表达式的

4.⽤于配置通知的注解

@Before：前置通知

@AfterReturning：后置通知

@AfterThrowing：异常通知

@After：最终通知

@Around：环绕通知

半注解半配置文件

\----------------------------------------------------------------------------------

切面类中的代码：

@Component   //添加到spring仓库

@Aspect      //设置为切面类

public class SaveLog {

  //配置切入点表达式

  @Pointcut("execution(* com.practice.service.*.*(..))")

  public void pointCut() {}

//  @Before("pointCut()")

  public void beforePrintLog(JoinPoint joinPoint) throws Throwable {

​    Object[] args = joinPoint.getArgs();

​    System.out.println("前置通知"+ Arrays.toString(args));

  }

//  @AfterReturning(value = "pointCut()",returning = "reValus")

  public void returningPrintLog(JoinPoint joinPoint ,Object reValus) throws Throwable {

​    System.out.println("后置通知"+reValus);

  }

//  @AfterThrowing(value = "pointCut()",throwing = "t")

  public void throwingPrintLog(JoinPoint joinPoint,Throwable t) throws Throwable {

​    t.printStackTrace();

​    System.out.println("异常通知");

  }

//  @After("pointCut()")

  public void afterPrintLog(JoinPoint joinPoint) throws Throwable {

​    System.out.println("最终通知");

  }

  @Around("pointCut()")

  public Object aroundPrintLog(ProceedingJoinPoint proceedingJoinPoint) throws Throwable {

​    Object result = null;

​    try {

​      //执行前置通知

​      this.beforePrintLog(proceedingJoinPoint);

​      //执行业务方法

​      Object[] args = proceedingJoinPoint.getArgs();

​      System.out.println(Arrays.toString(args));

​      result = proceedingJoinPoint.proceed(args);

​      System.out.println(result);

​      //执行后置通知

​      this.returningPrintLog(proceedingJoinPoint, result);

​    } catch (Throwable e) {

​      e.printStackTrace();

​      //执行异常通知

​      this.throwingPrintLog(proceedingJoinPoint, e);

​    } finally {

​      //执行最终通知

​      this.afterPrintLog(proceedingJoinPoint);

​    }

​    return result;

  }

}

\---------------------------------------------------------------------------

全注解

创建一个配置类

\---------------------------------------------------

@Configuration

@ComponentScan("com.practice")  

@EnableAspectJAutoProxy

public class SpringConfig {

}

\-----------------------------------

注意：如果使用配置文件开发，则使用前置通知，后置通知，异常通知，最终通知  

​     如果使用注解开发，则只使用环绕通知   原因是：使用注解开发时，最终通知会在后置通知之前执行，因此使用环绕通知来自己设定方法执行的顺序     

事务注解：@Transactional 类上或者方法上 用于service层

spring的默认事务回滚是，遇到运行时异常回滚，遇到受查异常提交

@Transactional(rollbackFor = Exception.class) 设置事务遇到哪种异常进行回滚

用在类上：为类中所有方法开启事务

生效的需要的配置：

1.把事务管理器加到spring仓库

<bean id="transactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">

​    <!--配置数据源-->

​    <property name="dataSource" ref="druidDataSource"></property>

</bean>

2.开启事务注解扫描

<tx:annotation-driven></tx:annotation-driven>  

<tx:annotation-driven>:需要使用 xmlns:tx="http://www.springframework.org/schema/tx"

Spring下的事务开发

事务：逻辑上的一组操作

作用：这组操作要么全部成功，要么全部失败

事务并发产生的问题

1.脏读：读到未提交事务中的数据

2.不可重复读：事务对同一条记录的俩次查询结果不同 原因：在这俩次查询结果之间，该记录进行了更新操作

3.幻读：事务根据某一条件进行查询，俩次查询结果不同 原因；在俩次查询结果之间，该条件记录进行了增加或删除操作

spring 事务隔离级别

1.极端模式：读未提交 Read_uncommited

2.读已提交 Read_commited 解决了脏读

3.可重复读 Repeatable_Read 解决了脏读和不可重复读

4.极端模式：串⾏化 事务串行执行，解决了脏读，不可重复读，幻读

5.默认：DEFAULT 不同的数据库有不同的默认隔离级别

mysql数据库默认隔离级别可重复读Repeatable_Read，oracle数据库默认级别读已提交Read_commited

spring中用到了哪些设计模式？

在ioc中用到了工厂模式 

spring中定义的bean默认为单例模式

aop中用到了代理模式

第三十八天

SpringMVC

经典三层：web表现层（view+controller）+service业务层+dao（数据接⼊访问层）

SpringMVC：是一个表现层框架，用来写Controller接收请求跳转⻚⾯的

SpringMVC是对Servlet的封装和增强，简化了servlet的操作

ModelAndView：

方法：

1.setViewName() :设置跳转页面的路径，页面路径从WEB-INF目录开始写

2.addObject("返回值的名字(值的键)",值) : 设置需要返回给页面的值  值会存储到一个map集合中

springmvc的入门案例

1.引入需要的jar包坐标  所有spring jar包都用相同版本的  jsp 修改不需要重启tomcat

2.在controller层创建一个类

\-----------------------------------------------------------------------------

@Controller  //把该类添加到spring仓库

public class TimeController {

  @RequestMapping(value = "return") //为该方法做网址映射

  public ModelAndView returnTime(ModelAndView modelAndView) {   //方法返回值和参数都是ModelAndView

​    //设置返回值

​    modelAndView.addObject("time",new Date());

​    //设置跳转页面的路径

​    modelAndView.setViewName("WEB-INF\\jsp\\result.jsp");

​    return modelAndView;

  }

}

\-----------------------------------------------------------------------------

3.spring配置文件中开启注解扫描和springmvc注解驱动

<context:component-scan base-package="com.practice.controller"/>

<mvc:annotation-driven></mvc:annotation-driven>          //作用：SpringMVC会⾃动注册最合适的处理器映射器、处理器适配器

4.在web.xml中配置一个servlet  把springmvc的前端控制器DispatcherServlet配置为servlet

\---------------------------------------------------------------------------------------------

<servlet>

  <servlet-name>dispatcherServlet</servlet-name>

  <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>

  

<!--  加载SpringMVC的核⼼配置-->

  <init-param>

   <param-name>contextConfigLocation</param-name>

   <param-value>classpath:springmvc.xml</param-value>

  </init-param>

  

<!--  设置随着tomcat启动加载此servlet，完成springmvc前端控制器的启动加载-->

  <load-on-startup>1</load-on-startup>

  

 </servlet>

 

 <servlet-mapping>

  <servlet-name>dispatcherServlet</servlet-name>

  <url-pattern>*.do</url-pattern>

 </servlet-mapping>

\-------------------------------------------------------------------------------------------

5.创建一个访问页面jsp文件

\-----------------------------------------------------------------------------------------------------------

<%@ page contentType="text/html;charset=UTF-8" language="java" isELIgnored="false" %>   //isELIgnored="false"  忽略el表达式

<html>

<head>

  <title>结果页面</title>

</head>

<body>

​    ${time}       //controller层下的返回值的键名 通过键名找到返回的值

</body>

</html>

\--------------------------------------------------------------------------------------------------------

6.启动tomcat

SpringMVC架构的各大组件

1.DispatcherServlet：前端控制器

本质上是一个Servlet,用于接收用户请求，并响应结果。DispatcherServlet是各大组件的核心，用来指挥各大组件进行工作。

2.HandlerMapping：处理器映射器

本质上是一个Map<url,Handler>,根据用户的请求url找到对应的Handler处理器

3.HandlAdapter：处理器适配器

通过HandlerAdapter对Handler处理器进⾏执⾏

4.Handler：处理器  需要自行定义

相当于Controller或者Controller当中的⽅法，Handler相对于前端控制器DispatcherServlet来说是后端控制器，用于执⾏具体业务处理的

5.ViewResolver：视图解析器  需要自行配置

把处理器传过来的jsp页面路径简写解析成具体的⻚⾯地址，再⽣成View视图对象

<bean id="viewResolver" class="org.springframework.web.servlet.view.InternalResourceViewResolver">

​       <property name="prefix" value="/WEB-INF/jsp/"></property>  设置页面路径前缀

​       <property name="suffix" value=".jsp"></property>           设置页面路径后缀

</bean>

6.View：视图

提供了很多的View视图类型的⽀持，包括：jsp、freemarkerView等

RequestMapping注解使⽤

有三个属性：value:映射网址  method：设置请求方法  params:设置请求参数

⽤法1: 作用在方法上，多个URL路径映射到同⼀个Handler（同⼀个⽅法）

@RequestMapping(value = {"return1","return2"})

⽤法2:作⽤在类上，实现对请求路径的分类管理，为类做网址映射，限定类中⽅法访问的前缀

⽤法3 method属性限定请求⽅法: 访问同一个url，根据请求方式的不同执行不同的方法

@RequestMapping(value = {"return1","return2"},method = RequestMethod.POST)  使用method属性设值请求方法

@RequestMapping(value = {"return1","return2"},method = RequestMethod.GET)

⽤法4 params属性限定请求参数 : 访问同一个url，根据请求参数的不同执行不同的方法

params = {"id"}  :  请求必须包含id请求参数

params = {"!id"} ： 请求中不包含id请求参数

params = {"id=1","name=bai"} :请求中必须包含id和name俩个请求参数，并且id值为1，name值为白

params = {"id!=1"} :请求中必须包含id这个请求参数，并且id的值不为1

请求参数自动封装到pojo类：

1.SpringMVC中默认执行sevlet中的api  HttpSession HttpServletRequest HttpServletResponse

可以在处理器方法中作为参数传入这些类进行使用

2.绑定简单数据类型 方法中传入参数名与请求参数键名相同，请求参数的键对应的值就会自动赋值给方法中参数

基本数据类型推荐使⽤包装类，包装类可以为null

说明：对于布尔类型的参数，请求的参数值为true或false。或者1或0

3.@RequestParam注解使⽤ 为方法形参和请求参数做手动映射

@RequestParam("id") Integer ids  把id请求参数赋值给形参ids

\4. 绑定pojo对象 传递过来的请求参数名与实体类中的字段名相同，就会实现自动赋值

5.绑定pojo对象中的实体字段 请求参数中应该这样写：实体字段名.字段名=   实现为实体类中的实体字段赋值  student.name=aa&student.age=18

6.为pojo对象中的list集合字段映射，集合中存放的是实体类  集合字段名[0].实体字段=

list[0].name=bai&list[0].age=18  & list[1].name=aaa&list[1].age=18

7.为pojo对象中的map集合字段映射，集合中存放的是实体类 Map<String,Student> map;  集合字段名[map集合的键].实体类字段名

map[a].name=bai&map[a].age=18

web.xml中标签配置有先后顺序

配置编码过滤器 解决post请求中的中文乱码问题

<filter>

  <filter-name>characterEncodingFilter</filter-name>

  <filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class>

  <init-param>

   <param-name>encoding</param-name>

   <param-value>utf-8</param-value>

  </init-param>

</filter>

<filter-mapping>

  <filter-name>characterEncodingFilter</filter-name>

  <url-pattern>/*</url-pattern>

</filter-mapping>

  

@RequestHeader注解  注解作⽤在⽅法参数上 获取请求头中的指定信息

public ModelAndView returnTime10(@RequestHeader("User-Agent") String userAgent, ModelAndView modelAndView) {}

@CookieValue注解 注解⽤于⽅法参数上 获取浏览器携带的Cookie某一个键值对

public ModelAndView returnTime11(@CookieValue("JSESSIONID") String userAgent, ModelAndView modelAndView) {}  

Controller⽅法（Handler）的返回值

1.返回值是ModelAndView 参数是ModelAndView       返回ModelAndView 对象

2.返回值是String         参数是Model             直接返回逻辑视图名

Model接⼝：⽅法 addAttribute(String key,Object value) 往reques域中添加键值对 

3.返回值String          参数是ModelMap         直接返回逻辑视图名

ModelMap(本质是一个map集合) 方法：addAttribute(String key,Object value) 往reques域中添加键值对

4.无返回值              参数是ModelMap HttpServletRequest HttpServletResponse

使用request完成请求转发    getRequestDispatcher("请求转发路径")

RequestDispatcher requestDispatcher = request.getRequestDispatcher("return1.do");

requestDispatcher.forward(request,response);

使用response完成重定向    sendRedirect("重定向网址")

response.sendRedirect("[http://localhost:8080/thread/return1.do");](http://localhost:8080/thread/return1.do)

使用response对象给页面返回信息

PrintWriter writer = response.getWriter();

writer.print("hello world");

5.SpringMVC框架实现重定向和请求转发的字符串写法

***注意：如果转发到当前方法所在类的方法时，不用加类路径，否则会报错

请求转发 关键字forward

public String frowordTest(ModelMap modelMap) {

​    System.out.println("froword执行了");

​    //设置转发的路径

​    return "forward:/thread/return1.do";  

}

重定向   关键字redirect

public String redirectTest(ModelMap modelMap) {

​    System.out.println("redirect执行了");

​    //设置跳转页面的路径

​    return "redirect:[http://www.baidu.com";](http://www.baidu.com/)

}

JSON:是一种特殊的字符串,易于机器解析和生成

SON的结构：{"键":”值“,"键":”值“}

Ajax：是一种独立于Web服务器软件的浏览器动态页面生成技术

AJAX最大的特点：使网页实现异步更新，无需重新加载整个网页的情况下，能够更新部分网页的技术

Json格式数据实现Ajax交互

用到的注解：

1.@RequestBody注解， 将JSON 字符串转换为POJO对象     作用在参数上

2.@ResponseBody注解  将Controller的⽅法返回的java对象转换为json字符串返回给客户端、

作用在方法上，把方法返回值转化为json字符串返回给客户端

作用在类上，把类中所有方法返回值转化为json字符串返回给客户端

3.@RestController  相当于Controller + ResponseBody

http请求⽅式：

get：主要是想做select

post：主要是想做insert

put：主要是想做update

delete：主要是想做delete

RESTful：⼀个资源定位及资源操作的⻛格 定义url的一种方式  url编写的一种方式

***具体编写方式：把传递给Controller层方法的参数作为其方法的网址映射，在方法的网址映射上完成了方法传参

用到的参数：

1.@PathVariable 把方法网址上传递过来的参数，赋值给方法参数

@RequestMapping(value = "{id}",method = RequestMethod.GET) //为该方法做网址映射

  public String select(@PathVariable("id") Integer ids) {

​    System.out.println(ids);

​    return "select";

}

HiddenHttpMethodFilter过滤器：

由于浏览器 form 表单只⽀持 GET 与 POST 请求，⽽DELETE、PUT 等 method 并不⽀持

Spring3.0之后添加了⼀个过滤器，可以将浏览器请求改为指定的请求⽅式，发送给我们的控制器⽅法，使得⽀持

GET、POST、PUT 与DELETE请求.

<filter>

​       <filter-name>hiddenHttpMethodFilter</filter-name>

​       <filter-class>org.springframework.web.filter.HiddenHttpMethodFilter</filter-class>

</filter>

<filter-mapping>

​       <filter-name>hiddenHttpMethodFilter</filter-name>

​       <url-pattern>/*</url-pattern>

</filter-mapping>

SpringMVC拦截器

拦截器：SpringMVC框架中特有的，可以对handle中的方法进行拦截

自定义拦截器步骤：

1.在interceptor目录下创建一个类，让其实现HandleInterceptor接口，并重写接口中的三个方法

重写⽅法：

​        preHandle：handler之前执⾏，返回true表示放⾏，返回false表示拦截

​        postHandle：在Handler⽅法执⾏完毕后 , 进⾏⻚⾯跳转渲染之前 执⾏

​        afterCompletion：在⻚⾯渲染完毕以后 执⾏

2.在spring配置文件中配置拦截器

<mvc:interceptors>

​     <mvc:interceptor>

​        <!--设置拦截路径-->

​        <mvc:mapping path="/**"/>

​        <!--把继承了HandlerIntercepto接口的类加载到spring仓库-->

​        <bean id="myInterceptor" class="com.practice.interceptor.MyInterceptor"></bean>

​    </mvc:interceptor>

</mvc:interceptors>

拦截器链

拦截器链都放行时：

​              preHandle顺序执⾏ ：所有拦截器中的preHandle方法都放行时，才会执行handle方法

​              postHandle倒序执⾏

​              afterCompletion倒序执⾏

拦截器链有中断时：postHandle都不会执行    

第三十九天

SpringBoot

1.内置了tomcat9.0

SpringBoot工程创建的俩种方式：

一.Spring Initializr 联网创建

二.maven 不选骨架

入门程序：

\1. 创建Maven⼯程

\2. pom.xml⽂件中配置起步依赖

配置一个父pom文件

<parent>

​    <groupId>org.springframework.boot</groupId>

​    <artifactId>spring-boot-starter-parent</artifactId>

​    <version>2.1.7.RELEASE</version>

</parent>

导入相关依赖

\3. 编写SpringBoot启动引导类

@SpringBootApplication

public class HelloWorldAppication {

  public static void main(String[] args) {

​    SpringApplication.run(HelloWorldAppication.class,args);

  }

}

\4. 编写Controller

@RestController

public class HelloController {

  @RequestMapping("/hello")

  public String HelloWorld() {

​    return "hello";

  }

}

5.编写静态页面index.html

在resource目录下新建一个目录static，在static目录下创建一个index.html页面

6.. 访问http://localhost:8080/hello测试

SpringBoot⼯程热部署：不需要重启tomcat就可以更新java代码，需要点击锤子按键（build projec）

需要导入一个jar包依赖

<dependency>

​      <groupId>org.springframework.boot</groupId>

​      <artifactId>spring-boot-devtools</artifactId>

</dependency>

starters的原理:对依赖坐标进行整理，把一系列的依赖坐标整合到一个starter中

starters的作用：让开发者⽆需关⼼依赖导⼊，依赖冲突，及依赖的版本

starter为什么不需要写版本：因为springboot工程的pom文件中继承了父pom文件，jar包的版本在父pom文件中进行了指定

继承了spring-boot-starter-parent 的好处和特点：

1.默认编译Java 1.8

2.默认编码UTF-8

3.通过spring-boot-denpendencies的pom管理所有公共Starter依赖的版本

4.spring-boot-denpendencies通过Maven的⼀个特性来实现版本管理

5.随⽤随取，不⽤继承⽗类所有的starter依赖。

6.如果想使⽤⽗pom⽂件中的任何插件，⽆需配置即可使⽤

SpringBoot中的打包插件：可以把springboot工程中涉及到的父目录中的插件也都打包进去

<build>

  <plugins>

​      <plugin>

​      <groupId>org.springframework.boot</groupId>

​      <artifactId>spring-boot-maven-plugin</artifactId>

  </plugin>

​      </plugins>

</build>

***SpringBoot默认从Resource⽬录加载⾃定义配置⽂件

***SpringBoot的配置文件名必须是application

SpringBoot的配置⽂件：有三种

1.xml

2.properties

3.yml/yaml:支持多种编程语言

配置⽂件语法：区分大小写

​            数据值前必须有空格，作为间隔符

​            使⽤缩进表示层级关系，缩进的空格数不重要，只要相同层级的元素左对⻬即可

​            缩进不允许使⽤tab，只允许空格

​            单行注释：#

值不可以用%开头

所有写法：person:

  name: peige

  age: 31

  addr: ${name}  引用name的值

  city:

   \- beijing     多个值前面加横杆，可以放在一个数组中

   \- shanghai

   \- guangzhou

  animals:

   \- name: ${name}  值是集合元素

   age: 2

   \- name: tomcat

   age: 3

   \- name: pig

   age: 5     

​         

SpringBoot的默认配置查看方式：

1.官网：https://docs.spring.io/spring-boot/docs/2.0.1.RELEASE/reference/htmlsingle/#common-application-properties

2.在autoconfigure jar包下的文件中

https://www.toyaml.com/index.html：yml文件和properties文件相互转换

修改SpringBoot的默认配置：在resourse目录下创建application.yml文件或者application.properties文件 文件必须是application

server:

 port: 9090

 address: 127.0.0.1

 servlet:

  context-path: /springboot

debug: true

logging:

 [level.com.example](http://level.com.example/): debug

SpringBoot中用到的注解：

1.@SpringBootApplication:标记类为SpringBoot引导类

2.@MapperScan("包名") ：把包下所有接口标记为mapper接口 作用在引导类上

3.@Transactional：开启事务

4.@Mapper：把接口标记为mapper接口 作用在mapper层接口上

注意：SpringBoot中的配置文名必须是application

5.@SpringBootTest 用在测试类中  整合junit的注解

SpringBoot中连接数据库的配置信息：

spring.datasource.url=jdbc:[mysql://127.0.0.1:3306/ssm?useUnicode=true&characterEncoding=UTF-8&serverTimezone=Asia/Shanghai](mysql://127.0.0.1:3306/ssm?useUnicode=true&characterEncoding=UTF-8&serverTimezone=Asia/Shanghai)

spring.datasource.password=root

spring.datasource.username=root

SpringBoot中整合Junit

1.导入依赖坐标

<!--spring boot测试依赖-->

<dependency>

<groupId>org.springframework.boot</groupId>

<artifactId>spring-boot-starter-test</artifactId>

<scope>test</scope>

</dependency>

2.测试类中加俩个注解

@RunWith(SpringRunner.class)

@SpringBootTest

739819578

springboot整合redis

1.导入springboot整合redis的依赖

<dependency>

<groupId>org.springframework.boot</groupId>

<artifactId>spring-boot-starter-data-redis</artifactId>

</dependency>

2.修改application.yml配置文件

spring:

 redis:

  host: 192.168.223.130

  post: 6379

 cache:

  type: *redis*

  cache-names: reids_service 自定义的缓存名称

3.涉及的实体类，要实现序列化接口

implements Serializable

4.如果要使用redis中的注解开发，需要在启动类在加@EnableCaching

redis的注解开发：作用在servies层

*// @Cacheable**：开启**redis**缓存，再进行查询操作时，先去**redis**缓存查，如果*

*// redis**缓存没有，再去数据查，然后再写入**redis**缓存中*

*// value**：是配置文件配置的**redis**缓存的名称，随意命名的，**key**用来指定插入缓存数据的**key*

@Cacheable(value = "reids_service", key = "'student_'+#age")

@CacheEvict(value = "reids_service",allEntries = true) ：执行 增删改操作后，会清空缓存中的数据

多环境配置⽂件

创建四个配置文件

application.properties 在这个配置文件中选择使用哪个环境 spring.profiles.active=dev

application-dev.properties 开发环境

application-test.properties 测试环境

application-pro.properties ⽣产环境

第四十天

Redis

1.是一种key-value形式的nosql数据库(非关系型数据库)

2.是C语言开发的，建议在linux上运行

3.内存数据库

4.提供了五种基本数据类型：

字符串:string,动态字符串，长度是可变的，当字符串长度增加时，会进行动态扩容

字典:数组加链表，key存放在数组中，value存放在链表中

列表:数据结构是链表，是有序的，常用来做异步队列使用，队列是先进先出的数据结构，常用于消息队列和异步逻辑处理，轮询列表中的数据可以保证元素的访问顺序

集合:无序的，不可重复的，可以存储不可重复的元素 value{key,value,value}

有序集合: value{score,value},每一个值对应一个分数，因此值是有序

redis缓存中的数据可以分为俩种：一种是准确性要求高的数据，与数据库中的数据要时刻保持绝对一致性

​                          一种是准确性要求不高的数据，与数据库中的数据相差不大就行，可以设置失效时间，隔一段时间更新一下

双重检测机制:可能会有线程安全问题

造成原因：

redis的分布式锁:

目的:解决并发问题，在同一时间有多个用户对数据进行操作

原理:使用setnx lock命令为元素上锁，然后使用del释放

为防止造成死锁，可以使用expire命令为锁设置一个过期时间

2.8版本后

为防止设置过期时间未执行，导致死锁，可以set和

expire命令一起使用

set lock:key value ex 5 nx

del lock:key

分布式锁的超时问题:加锁和释放锁之间的逻辑执行有时间限制，一但超过这个时间限制，锁就会自动释放，导致加锁逻辑未执行完就释放了锁，如果此时有另一个线程持有了这把锁，就会出现数据错乱.

redis的分布式锁不能解决超时问题，因此分布式锁不适用于长时间的任务

加锁没加成功时，有三种处理方法:

1.直接抛出异常，通知客户重试

2.sleep一会，再重试

3.把该请求放到队列中进行处理

异步消息队列:redis的列表可以作为异步消息队列使用，用lpush(左)和rpush右入队列，用rpop右和lpop左出队列，

为了防止队列空了空读现象，可以使用阻塞读brop和blpop代替rpop和lpop

使用阻塞读时，如果一直没有读，redis的连接就会断开，这时读队列会报异常，因此在编写消息消费者时，如果捕获到异常，还要进行重试

NoSQL数据库的产生：为了解决高并发，高缓冲，高可用性开发的

NoSQL数据库的作用：作为关系型数据库的良好补充，但是不能替代关系型数据库

NoSQL数据库的四大分类：

1.键值(Key-Value)存储数据库：Redis  主要用于处理大量数据的高访问负载

优势：快速查询

劣势：存储的数据结构缺少结构化

2.列存储数据库

3.文档型数据库

4.图形(Graph)数据库

redis的应用场景：

1.缓冲

2.好友列表

3.任务队列

在linux中安装Redis：

1.下载C语言编译器gcc

yum install gcc-c++ -y

2.下载Redis源码

wget http://download.redis.io/releases/redis-5.0.7.tar.gz

3.解压源码压缩包

tar zxf redis-5.0.7.tar.gz

4.进入到解压好的文件夹 编译源码

make

5.把编译好的源码下载到 /usr/local/redis

make install PREFIX=/usr/local/redis

6.使用守护进程模式启动Redis服务

复制redis.conf 到 /usr/local/redis/bin

cp /root/redis-5.0.7/redis.conf /usr/local/redis/bin

7.修改redis.conf 文件

注释 bind 127.0.0.1 这一行  允许所有ip访问

protected-mode no 不需要指定ip就可以访问

daemonize yes  把守护进程改为yes

8.启动服务

./redis-server redis.conf  使用配好的配置文件启动服务

9.关闭服务 

kill 进程id

查看进程id  ps -ef | grep redis

10.使用redis自带的命令行客户端

./redis-cli -h [IP地址]  -p [端口号]

Redis支持五种数据类型： 都是针对值定义的

1.String 值是Sring  key value

对应操作：

赋值：set key value

取值：get key

删值：del key

判断key是否存在：exists key 存在返回1，不存在返回0

取值时重新赋值：getset key vlaue

值为整数的数据，值默认加1： incr key

值为整数的数据，值加n : incrby key n

值为整数的数据，值默认减1： decr key

值为整数的数据，值减n : decrby key n

该键中没有值时才可以为其赋值：setnx key vlaue 返回0赋值失败，返回1赋值成功

为value尾部添加内容：append key 要添加的内容

查看值的长度：strlen key

同时为多个字符串赋值：mset key vlaue key vlaue

查看所有的key: keys *

2.hash  值是键值对形式 key field value

赋值：hset key field value field value

取值：hget key field

取多个值：hmget key field field

删值：hdel key field

判断值是否存在：hexists key field

取field列表：hkeys key

取value列表：hvals key

取field和value的列表：hgetall key

field中没有值才为其赋值：hsetnx key field value

3.list   值是双向链表结构 key value value value

添加元素：从左边添加 lpush key value value value

​        从右边添加 rpush key value value value

取元素:   从左边开始取 lpop key    元素取出后，list中就没有该元素了

​        从右边开始取 rpop key

查看列表中元素:lrange key 开始下标 结束下标

查看列表长度：llen key

4.set   值是set集合，不能有重复数据   key value value value

往集合中添加元素：sadd key value value value '

取集合中元素：smembers key

查看集合中元素个数：scard key

查看元素是否在集合中：sismember key value

删除集合指定元素：srem key value

随机删除集合中一个元素：spop key

做运算：

差集运算 查看key1中存在于key1但不存在于key2的元素 sdiff key1 key2

交集运算 sinter key1 key2

并集运算 sunion key1 key2

5.SortedSet  值是键值对形式，不能有重复数据  key score(double型数据) value

添加元素：zadd key number value number value

删除元素: zrem key value

查看元素数量：zcard key

查看元素：zrange key start end

带分数查询元素：zrange key start end withscores

倒序查询：zrevrange key start end

查询某个值的score: zscore key vlaue

服务器命令

1.查看所有key: key *

2.删除key：del key  

3.判断key是否存在：exists key

4.设置key的存活时间：expire key time(单位是秒)

5.查看key的存活时间：ttl key 返回-1，代表永久存在；返回-2代表已过期；返回其他数字，代表其存活剩余时间

6.Redis默认有16个库 db0-db15

默认打开的库时db0

切换库：select 库index

7.清空当前数据库中的数据：flushdb

  删除所有数据库中的数据：flushall

redis缓存涉及到的三种现象：缓存穿透、缓存击穿、缓存雪崩

缓存穿透：查询一个不存在的数据时，由于从数据库查不到数据，因此不会写去缓存，因此每次查询都回去数据库查找，会导致数据瘫痪

解决方案：数据查询的数据为空时也存入缓存，并设置一个短的过期时间

缓存击穿：数据库中有数据，而缓存中没数据  当一时间大量的请求访问同一个key时，key刚好失效，就会导致这些请求都去访问数据库

解决方案：定时更新热点数据的值，设置热点数据用不过时 

使用互斥锁：当查询的数据缓存中没有时，为该数据上锁

缓存雪崩，：有大量数据同时到期，而此时刚好查询量巨大时

解决方案：设置热点数据用不过期，过期时间设置成随机

Redis数据持久化

Redis中的数据是保存在内存中的，一旦Redis重启数据就会丢失，因此需要进行数据持久化

数据的持久化：把数据从内存同步到硬盘

1.RDB模式：默认模式，快照模式 ，当符合一定条件时Redis会自动将内存中的数据进行快照并持久化到硬盘

在Redis重写启动后，会把通过快照加载到硬盘中的数据读取过来

在Redis.conf配置文件中进行持久配置

save 900 1 在900秒内有一次更新操作就会进行一次快照

关闭RDB模式

\#  save "" 打开这一行

**缺点：如果Redis异常关闭，可能造成部分数据丢失

2.AOF模式:录像，每执行一条会更改Redis中的数据的命令，Redis就会将该命令写入硬盘中的AOF文件

开启AOF持久化模式：在Redis.conf配置文件中 appendonly yes

缺点：aof文件中数据过大，影响Redis的启动

3.混合持久化方式：先把当前的数据以RDB的形式写入文件的开头，再将后续的操作命令以 AOF 的格式存入文件

查看是否开启混合持久化方式：config get aof-use-rdb-preamble 在Redis客户端执行的命令

开启混合持久化：使用命令 config set aof-use-rdb-preamble yes 重启后失效

​             使用配置文件：aof-use-rdb-preamble yes 永久生效   Redis 5.0中默认开启

主从模式：

1.为主服务器添加从服务器，如果主服务器出现故障，从服务器可以代替主服务器进行工作，但是只能进行查询操作，如果要进行写操作，需要做主从切换

2.实现读写分离，从服务器上进行读操作，主服务器上进行写操作，并且从服务器只能进行读操作

3.哨兵可以帮我们自动进行主从切换

4.只需要在从服务器上进行数据持久化，减轻主服务器负担

主从复制：主服务器中的数据会实时更新到从服务器，当主服务器中有数据写入时，会通过主从主从复制机制把数据复制到从服务器上

主从模式的配置：

1.复制一个redis的编译文件bin目录即可作为主服务器，主服务器不需要配置

2.从服务器需要在配置文件中打开从服务器  从服务器只能进行读操作

在redis.conf配置文件中：打开这一行 replicaof <masterip> <masterport>

replicaof 主服务器ip 主服务器端口号

info replication :redis客户端上的命令，用于查看主从配置信息

哨兵模式

哨兵既不可写，也不可读

作用：

\1. 集群监控：负责监控redis 所有的主从服务器是否正常工作

\2. 消息通知：如果某个redis服务器出现故障，哨兵会给管理员发送报警通知

\3. 故障转移：如果主服务器挂掉了，会自动实现主从切换

\4. 配置中心：如果主从切换发生了，会告知client客户端新的master地址

哨兵模式中的特有名词：

1.sdown是主观宕机，就一个哨兵如果自己觉得一个master宕机了，那么就是主观宕机

2.odown是客观宕机，如果quorum数量的哨兵都觉得一个master宕机了，那么就是客观宕机

\3. quorum：确认odown的最少的哨兵数量

\4. majority：授权进行主从切换的最少的哨兵数量  值一般设为一半以上的哨兵数量

三哨兵模式为最经典模式

哨兵模式的配置文件：sentinel.conf

修改配置文件：

1.daemonize yes 以守护进程模式启动redis客户端

2.logfile "日志文件的存放位置，需要写绝对路径"

3.sentinel monitor 哨兵名称 主服务器的ip 主服务器的端口号 判定服务器客观下线的哨兵个数

4.sentinel down-after-milliseconds mymaster 30000 判定ping命令超时的时间，单位是毫秒

5.sentinel parallel-syncs mymaster 1  主从交换后一次把几个从服务器关联到新的主服务器上

6.sentinel failover-timeout mymaster 180000 多少毫秒后主从交换被视为失败

启动哨兵：redis-sentinel sentinel.conf

**一主多从三哨兵为经典模式

redis支持高并发 读11万次/S 写8.7万次/S  从机多少个 每秒每增加10万并发 就增加一台从机

cluster集群模式：

1.在cluster集群模式当中，从机默认既不可写，也不可读，仅仅是做备份机

2.如果超过半数的主节点挂点，则集群不可用 或者 任意一个主节点挂点且该主节点没有从节点，则集群不可用

3.只要连上集群中任一节点（服务器），就可以使用集群了

4.集群最低需要创建三个主节点，并且为每个主节点配一个从节点

5.使用redis-cli客户端方式创建集群

6.有多个主服务器，每个主服务器又有多个从服务器

集群创建步骤：

以三个主节点，三个从节点为例

1.创建6个redis服务器，端口号分别为8001-8006

2.更改配置文件

修改端口号

开启集群模式：打开这一行cluster-enabled yes

3.分别启动6个服务器

以文件形式启动

创建一个文件，在文件写上需要执行的命令

cd 8001

./redis-server redis.conf

cd ..

cd 8002

./redis-server redis.conf

cd ..

cd 8003

./redis-server redis.conf

cd ..

cd 8004

./redis-server redis.conf

cd ..

cd 8005

./redis-server redis.conf

cd ..

cd 8006

./redis-server redis.conf

cd ..

修改文件的权限：chmod +x 文件名

执行文件：./文件名

4.创建集群

随便进去一个节点服务器目录下

./redis-cli --cluster create 服务器ip:端口号 服务器ip:端口号 服务器ip:端口号 服务器ip:端口号 --cluster-replicas 1

--cluster-replicas 1 : 为每个主节点分配一个从节点

5.连接集群

随便进去一个服务器目录

./redis-cli -p 端口号 -c       -c:表示以集群模式连接

6.查看集群状态

cluster info :查看集群信息

cluster nodes:查看集群节点信息

redis的java客户端：推荐使用Jedis和Redisson

Jedis学习：

1.连接单一服务器 Jedis

Jedis jedis = new Jedis("192.168.200.128", 6379);  服务器ip和端口号

​    jedis.set("sex","男");

​    String sex = jedis.get("sex");

​    jedis.close();        //最后都要关闭连接

2.使用连接池连接单一服务器 JedisPool

JedisPool jedisPool = new JedisPool("192.168.200.128", 6379);

​    Jedis resource = jedisPool.getResource();

​    String name = resource.get("name");

​    System.out.println(name);

​    resource.close();

3.使用连接池连接哨兵集群 JedisSentinelPool

Set<String> sentinelSet = new HashSet<String>(); 创建一个set集合

​    sentinelSet.add("192.168.200.128:26379");  把哨兵的ip和端口号写入集合中

​    JedisSentinelPool mymaster = new JedisSentinelPool("mymaster", sentinelSet); 传入哨兵名和集合名

​    Jedis resource = mymaster.getResource();

​    resource.set("name","baiyulong");

​    String name = resource.get("name");

​    System.out.println("name = " + name);

​    resource.close();   //关闭连接

4.连接集群  JedisCluster

Set<HostAndPort> nodes = new HashSet<>();  创建一个存放HostAndPort对象的set集合

​    nodes.add(new HostAndPort("192.168.200.128",8001)); 把每个集群节点写入HostAndPort对象中，添加到集合中

​    nodes.add(new HostAndPort("192.168.200.128",8002));

​    nodes.add(new HostAndPort("192.168.200.128",8003));

​    nodes.add(new HostAndPort("192.168.200.128",8004));

​    nodes.add(new HostAndPort("192.168.200.128",8005));

​    nodes.add(new HostAndPort("192.168.200.128",8006));

​    JedisCluster jedisCluster = new JedisCluster(nodes);   传入集合名，获取JedisCluster连接对象

​    jedisCluster.set("name","baiyulong");

​    String name = jedisCluster.get("name");

​    System.out.println(name);

​    jedisCluster.close();

使用SpringBoot整合redis

用到的类：

1.StringRedisTemplate：用于操作redis数据库的类，继承自RedisTemplate

RedisTemplate中的方法

方法：redisTemplate.opsForValue();　　//操作字符串

​     redisTemplate.opsForHash();　　 //操作hash

​     redisTemplate.opsForList();　　  //操作list

​     redisTemplate.opsForSet();　　  //操作set

​     redisTemplate.opsForZSet();　 　//操作有序set

2.ObjectMapper：用于json字符串和java对象的相互转换

方法：readValue(String,User.class)  把json字符串转化为User对象

​     writeValueAsString(user):    把java对象转化为json字符串

配置文件：application.yml

spring:

 datasource:

  url: jdbc:[mysql://127.0.0.1:3306/mybatis?useUnicode=true&characterEncoding=UTF-8&serverTimezone=Asia/Shanghai](mysql://127.0.0.1:3306/mybatis?useUnicode=true&characterEncoding=UTF-8&serverTimezone=Asia/Shanghai)

  username: root

  password: root

 redis:

  host: 192.168.200.128  //配置redis服务器的ip和端口号

  port: 6379

debug: true

logging:

 level:

  com:

   example: debug

控制层：

****思想：服务器接收到查询请求后，先去redis服务器取数据，如果redis服务器有数据，则直接返回给客户端；

如果redis服务器中没有数据，则去mysql数据库取数据，把取出来的数据存储到redis服务器中，

并把取出的数据返回给客户端。

@RestController

@RequestMapping("/user")

public class UserController {

  @Autowired

  private UserServer userServer;

  @Autowired

  private StringRedisTemplate redisTemplate;  //StringRedisTemplate用于操作redis数据库的类，主要是存取数据

  @Autowired

  private ObjectMapper objectMapper;       //ObjectMapper:用于转换json字符串和java对象

  @RequestMapping("/{id}")

  public User findById(@PathVariable Integer id) throws JsonProcessingException {

​    String json = redisTemplate.opsForValue().get("user" + id);  //接收到客户端请求后先去redis服务器中取数据

​    if (json != null) {                                   //如果取出来的数据不为空，则直接返回

​      return objectMapper.readValue(json,User.class);

​    }

​    User user = userServer.findById(id);                    //redis数据库中没有数据，去mysql数据库中取数据

​    redisTemplate.opsForValue().set("user"+id,objectMapper.writeValueAsString(user)); // 把取出来的数据存储到redis数据库中

​    return user;              //返回数据

  }

}

​                      

第四十一天

Zookeeper

集中式系统：一个项目就是一个独立的应用，所有的资源都在这一个应用中，部署到一台服务器上

分布式系统：把一个大的项目分成多个模块，每个模块处理一个方向的请求，并且每个模块单独在一个tomcat服务器中运行，所有的模块整合起来就是一个大的项目

有多个服务器，服务器之间通过网络进行通信，服务器之间还可以进行交互，

ZooKeeper：用于分布式应用程序的高可用协调服务  

为项目中的服务进行统一命名管理

zookeeper的应用场景：

1.注册中心：注册节点  项目中所有服务都需要去注册中心注册节点，为服务器进行统一命名，即在zookeeper客户端创建一个节点，节点名就是服务器的名称

2.配置中心：配置文件管理 数据发布和订阅 注册了节点的服务器，可以把数据发布到自己节点上，其他服务器可以对该数据进行订阅，当数据有变时，会及时得到变化通知，达到动态获取数据的目的

3.分布式锁：多服务之间的事务控制  用于控制分布式系统之间同步访问共享资源的一种方式

4.分布式队列:用来实现跨进程，跨主机，跨网络的数据共享和数据传递

Zookeeper环境搭建

Zookeeper服务的默认端口是2181

1.必须安装jdk1.8以上,配置环境变量 PATH和JAVA_HOME

2.安装Zookeeper  解压即安装

下载路径：https://zookeeper.apache.org/releases.html  

下载好的压缩包是.tar.gz格式 是linux系统下的压缩包格式  需要使用7-zip打开该压缩包，进行解压缩

3、修改配置文件

在conf目录下复制一份zoo_sample.cfg文件，改名为zoo.cfg

打开zoo.cfg文件，修改其数据存放路径

dataDir=../data 这个目录zookerper会自动创建，也可以自己手动创建

4.启动Zookeeper服务器   服务启动后不可点击页面，点相当于暂停

打开bin目录，双击zkServer.cmd

5.启动Zookeeper客户端

打开bin目录，双击zkCli.cmd

Zookeeper数据存储模型：层次模型(树状模型)

树状中的点称为节点，节点可以保存数据

Zk节点分类：

1.持久性节点：存储在硬盘中

2.临时节点：存储在内存中  不能创建子节点

3.持久顺序型节点：排序号作为节点名后缀

4.临时顺序型节点

客户端命令操作Zookeeper

1.随便输入一个错误命令，可以查看其所有命令

2.ls 查看该节点下所有几点   ls 节点路径(要写绝对路径)

查询顺序节点的时候，要写节点名和其排序号

3.创建节点  节点名要写绝对路径

创建持久节点：create /节点名 '节点值'    值不加''也可以

创建持久顺序节点：create -s /节点名 '节点值'   

创建临时节点：create -e /节点名 '节点值'

创建临时顺序节点：create -e -s /节点名 '节点值'

4.查看节点的值 get

get 节点路径

5.查看节点状态 stat

stat 节点路径

\# -------------------------节点的状态信息，也称为stat结构体---------------------- -------------

cZxid = 0x17f # 该数据节点被创建时的事务id #其中zxid表示的是zookeeper的事务ID，由64位数字组成，分为高32位和低32位

ctime = Sat Dec 21 19:47:36 CST 2019 # 该数据节点创建时间

mZxid = 0x17f # 该数据节点被修改时最新的事物id

mtime = Sat Dec 21 19:47:36 CST 2019 # 该数据节点最后更新时间

pZxid = 0x183 # 当前节点的父级节点事务ID

cversion = 4 # znode子节点变化号，

znode子节点修改次数 dataVersion = 0 # znode数据变化号

aclVersion = 0 # 访问控制列表的变化号 access control list

ephemeralOwner = 0x0 # 如果临时节点，表示当前节点的拥有者的 sessionI。如果不是临时节点，则值为0

dataLength = 6 # 数据长度

numChildren = 4 # 子节点数据

6.修改节点的值 set

set 节点路径 节点值

7.删除节点 delete

delete 节点路径

deleteall 节点路径 递归删除

通过Java客户端操作Zookeeper

Apache Curator：目前最好的Zookeeper的Java客户端

用到的类：

1.ExponentialBackoffRetry：用来配置重试策略的类

构造方法：

ExponentialBackoffRetry(重试的间隔时间(单位是毫秒),重试次数)

2.CuratorFrameworkFactory：用来创建Zookeeper客户端的类

方法：CuratorFramework  newClient("服务ip和端口号"，重试对象)

1.新增节点 create()

创建客户端

ExponentialBackoffRetry exponentialBackoffRetry = new ExponentialBackoffRetry(3000, 3);

CuratorFramework client = CuratorFrameworkFactory.newClient("127.0.0.1:2181", exponentialBackoffRetry);

开启客户端

client.start();

zookeeper服务中没有设置编码和解码，因此只能传入字节数据

getBytes()：把字符串转化为字节

创建一个持久无值节点：client.create().forPath("/app1");

创建持久有值节点：client.create().forPath("/app2","baiyulong".getBytes());

创建多层节点：client.create().creatingParentsIfNeeded().forPath("/app3/app1","aaa".getBytes());

创建临时节点：client.create().withMode(CreateMode.EPHEMERAL).forPath("/app4","abbb".getBytes());

创建持久有序节点：client.create().withMode(CreateMode.PERSISTENT_SEQUENTIAL).forPath("/app5","bbbb".getBytes());

创建临时有序节点：client.create().withMode(CreateMode.EPHEMERAL_SEQUENTIAL).forPath("/app7");

关闭客户端：client.close();

2.删除节点 delete().

创建客户端

开启客户端

//方式1: 删除一个节点

client.delete().forPath("/app1");

//方式2: 递归删除多个节点

client.delete().deletingChildrenIfNeeded().forPath("/app3");

//方式3: 强制删除【避免一些因为网络传输导致的删除不成功】

client.delete().guaranteed().forPath("/app2");

关闭客户端

3.修改节点 setData()

client.setData().forPath("/app50000000014","aaaaaaa".getBytes());

4.查看节点的值 getData()

byte[] bytes = client.getData().forPath("/app50000000014");

System.out.println(new String(bytes));

测试类中before注解获取全局客户端

方法上加@before注解，在执行其他方法前会先执行此方法

zookeeper中订阅发布功能：在zookeeper中注册了节点的服务器，可以往节点中发布值，而客户端可以根据自己的需求订阅

需要的节点。

推：如果客户端订阅的节点发生了变化，那么zookeeper就会推给客户端该节点的节点名和节点变化的描述

拉：客户端会根据zookerper推过来的节点名和节点变化的描述去服务器端把更新内容拉回来

zookeeper的watcher机制原理

由客户端，客户端WatchManager，Zookeeper服务器三部分组成

监听的步骤：

\1. Zookeeper客户端向Zookeeper服务器注册watcher

\2. 注册的同时会将watcher对象存储在客户端的watchManager。

\3. Zookeeper服务器触发watcher事件后，会向客户端发送通知，客户端线程从watchManager中回调watcher执行相应的功能。

Curator客户端中使用缓存cache的概念进行监听：

有三种模式的缓冲：

模式1-监听某节点内容变化 : NodeCache

模式2-监听某节点的子节点变化，不关心节点本身和孙子节点 : PathChildrenCache

模式3-监听某节点本身和其子节点变化：TreeCache

设置监听模式的步骤：

1.创建重试策略 

ExponentialBackoffRetry backoffRetry = new ExponentialBackoffRetry(1000 * 3, 3);

2.创建客户端,使用重试策略

client = CuratorFrameworkFactory.newClient("127.0.0.1:2181",backoffRetry);

3.开启客户端

client.start();

4.创建节点的缓冲对象

5.开始缓存(true:可以直接获取监听的节点; false:不可以获取监听的节点) ，把监听的节点信息从服务器中拿过来

6.创建监听对象并把监听对象加入到监听管理器中，如果监听内容发生变化，会执行回调方法

监听模式1：监听某个节点的值的变化

创建节点的缓冲对象

NodeCache nodeCache = new NodeCache(client, "/app1");

​     开始缓存

​    nodeCache.start();

​    创建监听对象并把监听对象加入到监听管理器中，如果监听内容发生变化，会执行回调方法

​    nodeCache.getListenable().addListener(new NodeCacheListener() {

​      @Override

​      public void nodeChanged() throws Exception {

​        String path = nodeCache.getPath();

​        System.out.println(path);

​        byte[] data = nodeCache.getCurrentData().getData();

​        System.out.println(new String(data));

​      }

​    });

Thread.sleep(1000*1000);

client.close();

监听模式2：监听某节点的子节点变化

PathChildrenCache childrenCache = new PathChildrenCache(client, "/app2", true);

childrenCache.start(PathChildrenCache.StartMode.NORMAL);

childrenCache.getListenable().addListener(new PathChildrenCacheListener() {

​      @Override

​      public void childEvent(CuratorFramework client, PathChildrenCacheEvent event) throws Exception {

​        String path = event.getData().getPath();

​        System.out.println("path = " + path);

​        byte[] data = event.getData().getData();

​        System.out.println(new String(data));

​        Stat stat = event.getData().getStat();

​        System.out.println(stat);

​      }

});

Thread.sleep(1000*1000);

client.close();

监听模式3：监听本节点和其子节点的变化

public void watcherTest3() throws Exception {

TreeCache treeCache = new TreeCache(client, "/app2");

treeCache.start();

treeCache.getListenable().addListener(new TreeCacheListener() {

​      @Override

​      public void childEvent(CuratorFramework clent, TreeCacheEvent event) throws Exception {

​        String path = event.getData().getPath();

​        System.out.println(path);

​        byte[] data = event.getData().getData();

​        System.out.println(new String(data));

​      }

});

Thread.sleep(1000*1000);

client.close();

​        

Zookeeper集群搭建

1.为了保证集群选举的的成功，Zookeeper 集群的数量一般为奇数

2.集群会自动推选出主节点和从节点，主节点中一般处理一些重要的操作，比如事务操作

集群搭建步骤：

一.安装三个linux虚拟机

二、在每个虚拟机上安装jdk,因为Zookeeper是使用java编写的，需要在java环境下运行

1.卸载系统自带的jdk

使用rpm -qa | grep java  命令查询已经安装的jdk的包

使用rpm -e --nodeps   命令卸载这些默认安装的jdk版本

2.使用xftp把windows系统上的jdk的.tar.gz类型压缩包上传到linux系统上

3.解压缩 tar -zxvf jdk1.8.0_181

4.配置JAVA_HOME和PATH和CLASSPATH

vim /etc/profile 打开/etc/profile

在末尾加三行

export JAVA_HOME=/root/jdk1.8.0_181

export PATH=$PATH:$JAVA_HOME/bin

export CLASSPATH=.:$Java_HOME/lib.tools.jar

5.重新加载profile文件

source profile

6.测试

java -version

三、安装zookeeper服务器

1把zookeep压缩包上传到linux系统，进行解压缩，并且把解压缩后的目录剪切到/usr/local/zookeeper

tar -vxf apache-Zookeeper-3.5.5-bin.tar.gz

mv apache-zookeeper-3.6.2-bin /usr/local/zookeeper

2.在/usr/local/zookeeper目录下创建一个data目录  mkdir data

3.进去conf目录下，复制zoo_sample.cfg文件，到zoo.cfg文件

cp zoo_sample.cfg zoo.cfg

4.修改zoo.cfg配置文件

dataDir=/usr/local/zookeeper/data

在配置文件尾部，编辑集群中服务的列表

server.1=192.168.200.128:2182:3182  

server.2=192.168.200.129:2182:3182

server.3=192.168.200.130:2182:3182

server.* 后面的数据对应myid中的数字

ip地址对应每台虚拟机的ip地址

2182：这个服务器与集群中的 Leader 服务器交换信息的端口

3182：表示的是万一集群中的 Leader 服务器挂了，需要一个端口来重新进行选举，选出一个新的 Leader，而这个端口就是用来执行选举时服务器相互通信的端口

5.进去到bin目录下，开启服务

./zkServer.sh start

6.查看服务状态

./zkServer.sh status

集群的leader主节点选举机制

服务器1启动，给自己投票，然后发投票信息，由于其它机器还没有启动所以它收不到反馈信息，

服务器1的状态一直属于Looking(选举状态)。

服务器2启动，给自己投票，同时与之前启动的服务器1交换结果，由于服务器2的编号大所以服务

器2胜出，但此时投票数没有大于半数，所以两个服务器的状态依然是LOOKING。

服务器3启动，给自己投票，同时与之前启动的服务器1,2交换信息，由于服务器3的编号最大所以

服务器3胜出，此时投票数正好大于半数，所以服务器3成为领导者，服务器1,2成为小弟。

服务器4启动，给自己投票，同时与之前启动的服务器1,2,3交换信息，尽管服务器4的编号大，但

之前服务器3已经胜出，所以服务器4只能成为小弟。

服务器5启动，后面的逻辑同服务器4成为小弟

第四十二天

RPC：远程调用的技术，是分布式架构的核心

序列化：把java对象转化为字节序列的过程  目的：在网络传输中保证对象的完整性

反序列化：把字节序列恢复为java对象的过程

SOA:面向服务的架构模型，把应用程序的不同服务进行拆分，通过公共接口模块中定义的接口把这些服务连接起来。

Dubbo：一种高性能的java RPC框架

Dubbo有三大核心能力：

1.面向接口的远程方法调用

2.智能容错和负载均衡

3.以及服务自动注册和发现

Dubbo这种RPC框架的原理：

底层由四部分组成：

1、 客户端(Client)：消费者模块

2、 服务端(Server)：提供者模块

3、 客户端存根(Client Stub)：存放服务端地址信息，把客户端的接口调用进行序列化操作，然后传递给服务器存根

4、 服务端存根(Server Stub)：把客户端存根发送过来的序列化信息进行反序列化操作，然后传递给服务器

Dubbo框架远程调用步骤：

1.客户端调用业务层接口

\2. 客户端存根把接口调用进行序列化操作，然后传递给服务器存根

3.服务端存根把客户端存根发送过来的序列化信息进行反序列化操作，然后传递给服务器

4.服务器接收到信息，执行对应的方法，并把方法返回值返回给服务端存根

5.服务端存根把返回结果进行序列化操作，传递给客户端存根

6.客户端存根进行反序列化，把结果返回给客户端

Dubbo在提供者服务中的配置

<!-- dubbo应用的名称-->

<dubbo:application name="dubbo_provider"/>

<!-- 注册中心的地址-->

<dubbo:registry address="[zookeeper://127.0.0.1:2181"/](zookeeper://127.0.0.1:2181/)>

<!--指定注册到注册中心的服务接口及实例-->

<dubbo:service interface="com.parent.service.UserService" ref="userService"/>

<bean id="userService" class="com.parent.service.impl.UserServiceImpl"/>

Dubbo在消费者服务中的配置

  <!-- dubbo应用的名称-->

  <dubbo:application name="dubbo_consumer"/>

  <!-- 注册中心的的地址-->

  <dubbo:registry address="[zookeeper://127.0.0.1:2181"/](zookeeper://127.0.0.1:2181/)>

  <!--订阅远程服务对象-->

  <dubbo:reference id="userservice" interface="com.parent.service.UserService"/>

  <!--初始化控制器，并把远程service注入到controller -->

  <bean id="userController2" class="com.parent.controller.UserController">

​    <property name="userService" ref="userservice"></property>

  </bean>

  启动消费者服务，不检查提供者服务是否启动

  <dubbo:consumer check="false"/>

第四十三天

保存到我的笔记

本内容不代表印象笔记立场
