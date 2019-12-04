# StudyOfJAVA
JAVA的基础部分学习
#### 整型

所有的浮点数值计算都遵循IEEE 754规范。下面是用于表示溢出和出错情况的三种特殊的浮点数值：

		- 正无穷大
		- 负无穷大
		- NaN（不是一个数字）

例如：一个正整数除以0的结果为正无穷大。计算0/0或者附属的平方根结果为NaN

常量Double.POSITIVE_INFINITY、Double.NEFATIVE_INFINITY和Double.Nan分别表示这三个特色的值

> 如果需要在数值计算中不含有任何舍入误差，就应该使用BigDecimal类

#### 常量

> 在JAVA中，利用关键字final声明常量

final double CM_PER = 2.54;

关键字final表示这个变量只能被赋值一次。一旦被赋值之后，就不能够再更改了。习惯上，常量名使用大写。

类常量可以用关键字static final设置。

类常量的定义位于main方法的外部。因此，在同一个类的其他方法中也可以使用这个常量。而且，如果一个常量被声明为public，那么其他类的方法也可以使用这个常量。

#### 字符串

> String类的substring方法可以从一个较大的字符串提取出一个字串。
>
> 例如：
>
> String greeting = "Hello";
>
> String s = greeting.substring(0,3);
>
> 在substring中从0开始计数，直到3为之，但不包含3

---

检测字符串是否相等

可以使用equals方法检测两个字符串是否相等

```java
s.equals(t);
```

> Java的compareTo方法与strcmp完全类似
>
> ```java
> if(greeting.compareTo("Hello") == 0)
> ```

#### 文件输入与输出

要想对文件进行读取，就需要一个用File对象构造一个Scanner对象

```java
Scanner in = new Scanner(new File("myfile.txt"));
```

#### 控制流程

- 块作用域

- 条件语句

- 循环

- for循环

- 多重选择：switch

- 中断控制流程语句：break; 

  - 带标签的break语句

  - ```java
    read_data:
    while(...){
    	break read_data;
    }
    ```

  - continue;

#### 大数值

java.math包中的两个很有用的类：BigInteger 和 BigDecimal。前者实现了任意精度的整数运算，后者实现了任意精度的浮点数运算。

如果需要 + 或 * 处理大数值：需要使用大数值类中的add和multiply方法；

```java
BigInteger c = a.add(b);
BigInteger d = c.multiply(BigInteger.valueOf(2)));
// d = c * (b + 2);
```

#### for each循环语句

```java
for(double a : a)
	do something with value
```

