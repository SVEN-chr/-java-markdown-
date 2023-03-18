# -java-markdown-
# JavaSE学习笔记

## JavaSE简介

### Java语言特点

- Java是面向对象的语言
- Java具有平台无关性，即一次编写可在多个平台运行
- Java具有自动内存管理机制（垃圾回收）
- Java具有强类型检查机制
- Java具有丰富的类库支持

### JavaSE体系结构

![JavaSE体系结构](https://images2018.cnblogs.com/blog/363476/201808/363476-20180814220420015-193800058.png)

- Java语言
- Java虚拟机（JVM）
- Java标准库

### JavaSE环境搭建

- 下载JDK并安装
- 配置环境变量

## Java基础语法

### 基本数据类型

Java的基本数据类型包括整型（byte、short、int、long）、浮点型（float、double）、字符型（char）和布尔型（boolean）。

### 变量

在Java中定义变量需要指定变量类型，并使用操作符“=”来为其赋值。变量名遵循标识符命名规范。

```java
// 定义并初始化变量
int a = 10;
double b = 3.14;
char c = 'A';
boolean d = true;

// 定义变量并赋初值
int e;
e = 20;
```

### 运算符

Java中支持的运算符包括算术运算符、比较运算符、逻辑运算符、位运算符等。

```java
// 算术运算符
int a = 10, b = 3;
int c = a + b;
int d = a - b;
int e = a * b;
int f = a / b;
int g = a % b;

// 比较运算符
boolean bool1 = a > b;
boolean bool2 = a >= b;
boolean bool3 = a < b;
boolean bool4 = a <= b;
boolean bool5 = a == b;
boolean bool6 = a != b;

// 逻辑运算符
boolean bool7 = true && false;
boolean bool8 = true || false;
boolean bool9 = !true;

// 位运算符
int h = a & b;
int i = a | b;
int j = a ^ b;
int k = ~a;
int l = a << 1;
int m = a >> 1;
```

### 分支结构

Java中的分支结构包括if语句和switch语句。

```java
// if语句
int a = 10, b = 20;
if (a > b) {
    System.out.println("a > b");
} else if (a < b) {
    System.out.println("a < b");
} else {
    System.out.println("a == b");
}

// switch语句
int num = 2;
switch (num) {
    case 1:
        System.out.println("num == 1");
        break;
    case 2:
        System.out.println("num == 2");
        break;
    default:
        System.out.println("num != 1 && num != 2");
        break;
}
```

### 循环结构

Java中的循环结构包括for循环、while循环和do-while循环。

```java
// for循环
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}

// while循环
int j = 0;
while (j < 10) {
    System.out.println(j);
    j++;
}

// do-while循环
int k = 0;
do {
    System.out.println(k);
    k++;
} while (k < 10);
```

### 数组

Java中的数组是一种存储多个相同类型数据的容器，数组长度不可变且不可超出范围。

```java
// 定义并初始化数组
int[] array1 = {1, 2, 3};
String[] array2 = {"hello", "world", "!"};

// 定义数组并赋初值
int[] array3 = new int[3];
array3[0] = 1;
array3[1] = 2;
array3[2] = 3;

// 遍历数组
for (int i = 0; i < array1.length; i++) {
    System.out.println(array1[i]);
}
```

### 类和对象

Java是一种面向对象的语言，所有的操作都是通过对象来完成的。Java中的类是对对象的描述，包括类名、属性和方法等成员变量。每个对象都是类的一个实例，可以调用类的方法来完成各种操作。

```java
// 定义类
public class Person {
    String name;
    int age;

    public void eat() {
        System.out.println("eating...");
    }
}

// 创建对象
Person person = new Person();
person.name = "Tom";
person.age = 18;
person.eat();
```

### 异常处理

在Java中，异常是一种不正常的程序状态，可以通过try-catch语句来捕捉并处理异常。

```java
try {
    // 可能抛出异常的代码
} catch(Exception e) {
    // 捕捉到异常后的处理代码
} finally {
    // 无论是否抛出异常都会执行的代码
}
```

## Java常用类库

### String类

Java中的字符串是一种不可变对象，String类提供了一系列方法来操作字符串。

```java
// 定义字符串
String str = "hello world!";

// 获取字符串长度
int length = str.length();

// 字符串拼接
String str1 = "hello";
String str2 = "world";
String str3 = str1 + " " + str2;

// 字符串比较
boolean bool = str1.equals(str2);

// 字符串查找
int index = str.indexOf("world");

// 字符串替换
String str4 = str.replace("world", "java");
```

### Math类

Java中的Math类提供了一系列数学运算的方法。

```java
// 求绝对值
int abs = Math.abs(-10);

// 求平方根
double sqrt = Math.sqrt(16);

// 求最大值、最小值
int max = Math.max(10, 20);
int min = Math.min(10, 20);

// 求随机数
double random = Math.random(); // 0.0 <= random < 1.0
int randomInt = (int)(Math.random() * 10); // 0 <= randomInt < 10
```

### Date类

Java中的Date类提供了一系列有关日期和时间的方法。

```java
// 获取当前时间
Date date = new Date();

// 格式化日期
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
String now = sdf.format(date);

// 计算时间差
long time1 = System.currentTimeMillis();
doSomething();
long time2 = System.currentTimeMillis();
long diff = time2 - time1;
```

### File类

Java中的File类提供了一系列关于文件的方法。

```java
// 创建文件
File file = new File("test.txt");
file.createNewFile();

// 删除文件
file.delete();

// 判断文件是否存在
boolean bool = file.exists();

// 获取文件属性
long length = file.length();
String path = file.getAbsolutePath();
```

### ArrayList类

Java中的ArrayList是一种动态数组，可以动态地添加和删除元素。

```java
// 创建ArrayList
ArrayList<String> list = new ArrayList<>();

// 添加元素
list.add("hello");
list.add("world");

// 获取元素
String str = list.get(0);

// 删除元素
list.remove(0);

// 遍历ArrayList
for (int i = 0; i < list.size(); i++) {
    System.out.println(list.get(i));
}
```

### HashMap类

Java中的HashMap是一种键值对存储结构，可以根据键来快速访问对应的值。

```java
// 创建HashMap
HashMap<String, String> map = new HashMap<>();

// 添加元素
map.put("key1", "value1");
map.put("key2", "value2");

// 获取元素
String str = map.get("key1");

// 删除元素
map.remove("key1");

// 遍历HashMap
for (String key : map.keySet()) {
    String value = map.get(key);
    System.out.println(key + " : " + value);
}
```

### Collections类

Java中的Collections类提供了一系列方法来操作集合。

```java
// 排序集合
ArrayList<Integer> list = new ArrayList<>();
Collections.sort(list); // 按照升序排序

// 查找元素
int index = Collections.binarySearch(list, 10); // 返回元素所在索引

// 反转集合
Collections.reverse(list);

// 洗牌集合
Collections.shuffle(list);
```

## Java高级特性

### 继承

Java中的继承是一种类与类之间的关系，通过继承可以获得父类的属性和方法。

```java
// 定义父类
public class Animal {
    String name;
    int age;

    public void eat() {
        System.out.println("eating...");
    }
}

// 定义子类
public class Cat extends Animal {
    public void mew() {
        System.out.println("mew...");
    }
}

// 创建对象，并使用继承来调用父类的方法
Cat cat = new Cat();
cat.name = "Tom";
cat.age = 3;
cat.eat();
cat.mew();
```

### 多态

Java中的多态是指同一操作作用于不同的对象，产生不同的结果。

```java
// 定义接口
public interface Animal {
    public void eat();
}

// 定义实现类
public class Cat implements Animal {
    public void eat() {
        System.out.println("eating fish...");
    }
}

public class Dog implements Animal {
    public void eat() {
        System.out.println("eating bone...");
    }
}

// 创建对象，并使用多态调用相同接口的不同实现
Animal animal1 = new Cat();
Animal animal2 = new Dog();
animal1.eat();
animal2.eat();
```

### 接口

Java中的接口是一种特殊的抽象类，它只包含方法的声明，没有方法的实现。

```java
// 定义接口
public interface Animal {
    public void eat();
}

// 实现接口
public class Cat implements Animal {
    public void eat() {
        System.out.println("eating fish...");
    }
}

public class Dog implements Animal {
    public void eat() {
        System.out.println("eating bone...");
    }
}

// 创建对象，并使用接口调用实现类的方法
Animal animal1 = new Cat();
Animal animal2 = new Dog();
animal1.eat();
animal2.eat();
```

### 泛型

Java中的泛型是一种将类型参数化的机制，可以在编译时检查类型的正确性，增加程序的可读性和安全性。

```java
// 定义泛型类
public class Box<T> {
    private T data;
    public void setData(T data) {
        this.data = data;
    }
    public T getData() {
        return data;
    }
}

// 创建对象，并使用泛型来传递参数
Box<String> box1 = new Box<>();
Box<Integer> box2 = new Box<>();
box1.setData("hello");
box2.setData(2021);
String str = box1.getData();
int num = box2.getData();
```

### 注解

Java中的注解是一种提供元数据的机制，可以通过注解来描述代码的结构和行为。

```java
// 定义注解
@Target(ElementType.METHOD) // 表示注解用于方法
@Retention(RetentionPolicy.RUNTIME) // 表示注解在运行时也可以访问
public @interface MyAnnotation {
    String value(); // 定义注解属性
}

// 使用注解
public class MyClass {
    @MyAnnotation("hello")
    public void myMethod() {
        System.out.println("myMethod...");
    }
}

// 获取注解信息
Class<MyClass> clazz = MyClass.class; // 获取Class对象
Method method = clazz.getMethod("myMethod"); // 获取Method对象
MyAnnotation annotation = method.getAnnotation(MyAnnotation.class); // 获取注解对象
String value = annotation.value(); // 获取注解属性
System.out.println(value);
```
