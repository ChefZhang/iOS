# Objective-C学习

这篇文章是自己学习Objective-C的笔记，希望这篇文章能够帮助一些没有Objective-C经验的童鞋更快的学习。

目录：

*  [1. OC简介](#1)
	*  [1.1 OC和C对比](#1.1)
	*  [1.2 第一个OC程序](#1.2)
	*  [1.3 面向对象思维](#1.3)
	*  [1.4 类与对象](#1.4)
	*  [1.5 类与设计](#1.5)
	*  [1.6 第一个OC类](#1.6)
	*  [1.7 对象方法的声明和实现](#1.7)
	*  [1.8 类方法的声明和实现](#1.8)
	*  [1.9 对象的存储细节](#1.9)
	*  [1.10 函数与方法对比](#1.10)
	*  [1.11 常见错误](#1.11)
*  [2. OC开发简介](#2)
	*  [2.1 NSString类介绍及用法](#2.1)
	*  [2.2 结构体成员变量](#2.2)
	*  [2.3 对象和方法之间的关系](#2.3)
	*  [2.4 pragma mark指令](#2.4)
	*  [2.5 对象作为方法的参数连续传递](#2.5)
	*  [2.6 OC多文件开发介绍](#2.6)
*  [3. 面向对象的三大特性](#3)
	*  [3.1 getter/setter方法](#3.1)
	*  [3.2 自定义代码段](#3.2)
	*  [3.3 点语法](#3.3)
	*  [3.4 self关键字](#3.4)
	*  [3.5 继承](#3.5)
	*  [3.6 继承相关特性](#3.6)
	*  [3.7 Super关键字](#3.7)
	*  [3.8 多态基本概念](#3.8)
	*  [3.9 多态的实现](#3.9)
*  [4. 实例变量修饰符、@property、构造方法和类工厂方法](#4)
	*  [4.1 实例变量修饰符](#4.1)
	*  [4.2 description方法](#4.2)
	*  [4.3 OC中的私有方法](#4.3)
	*  [4.4 @property基本概念](#4.4)
	*  [4.5 @synthesize基本概念](#4.5)
	*  [4.6 @property增强](#4.6)
	*  [4.7 @property修饰符](#4.7)
	*  [4.8 id类型](#4.8)
	*  [4.9 new方法实现原理](#4.9)
	*  [4.10 构造方法](#4.10)
	*  [4.11 自定义构造方法](#4.11)
	*  [4.12 继承中的自定义构造方法](#4.12)
	*  [4.13 自定义类工厂方法](#4.13)
	*  [4.14 类的本质](#4.14)
	*  [4.15 类的启动过程](#4.15)
	*  [4.16 SEL类型](#4.16)
*  [5. 内存管理](#5)
	*  [5.1 引用计数器](#5.1)
	*  [5.2 dealloc方法](#5.2)
	*  [5.3 野指针\空指针](#5.3)
	*  [5.4 Xcode设置](#5.4)
	*  [5.5 内存管理原则](#5.5)
	*  [5.6 @property参数](#5.6)
	*  [5.7 @class](#5.7)
	*  [5.8 循环retain](#5.8)
	*  [5.9 autorelease基本使用](#5.9)
	*  [5.10 autorelease注意事项](#5.10)
	*  [5.11 ARC基本概念](#5.11)
	*  [5.12 ARC快速入门](#5.12)
	*  [5.13 ARC下的内存管理](#5.13)
	*  [5.14 ARC和MRC兼容和转换](#5.14)
*  [6. Category、Extension、Block和Protocol](#6)
	*  [6.1 Category基本概念](#6.1)
	*  [6.2 Category注意事项](#6.2)
	*  [6.3 类扩展(Class Extension)](#6.3)
	*  [6.4 Block基本概念](#6.4)
	*  [6.5 typedef和Block](#6.5)
	*  [6.6 Block注意事项](#6.6)
	*  [6.7 Protocol基本概念](#6.7)
	*  [6.8 Protocol注意事项](#6.8)
	*  [6.9 Protocol类型限制](#6.9)
	*  [6.10 Protocol代理设计模式](#6.10)
*  [7. Foundation框架](#7)
	*  [7.1 Foundation框架介绍](#7.1)
	*  [7.2 NSString基本概念](#7.2)
	*  [7.3 NSString基本概念](#7.3)
	*  [7.4 NSString字符串比较](#7.4)
	*  [7.5 NSString字符串搜索](#7.5)
	*  [7.6 NSString字符串截取](#7.6)
	*  [7.7 NSString字符串替换](#7.7)
	*  [7.8 NSString字符串读写](#7.8)
	*  [7.9 NSString字符串与基本数据类型转换](#7.9)
	*  [7.10 NSMutableString基本概念](#7.10)
	*  [7.11 NSMutableString常用方法](#7.11)
	*  [7.12 NSMutableString练习](#7.12)
	*  [7.13 NSArray基本概念](#7.13)
	*  [7.14 NSArray遍历](#7.14)
	*  [7.15 NSArray排序](#7.15)
	*  [7.16 NSArray文件读写](#7.16)
	*  [7.17 NSArray与字符串](#7.17)
	*  [7.18 NSMutableArray基本概念](#7.18)
	*  [7.19 NSDictionary基本概念](#7.19)
	*  [7.20 NSMutableDictionary基本概念](#7.20)
	*  [7.21 常见的结构体](#7.21)
	*  [7.22 NSNumber](#7.22)
	*  [7.23 NSValue](#7.23)
	*  [7.24 NSDate](#7.24)
	*  [7.25 NSFileManager](#7.25)
	*  [7.26 集合对象的内存管理](#7.26)
	*  [7.27 Copy](#7.27)
	*  [7.28 copy与内存管理](#7.28)
	*  [7.29 @property中的copy关键字](#7.29)
	*  [7.30 自定义的类实现copy操作](#7.30)
	*  [7.31 单例设计模式](#7.31)
	
	
	
	
	
	
<h2 id="1">1. OC简介</h2>

<h3 id="1.1">1.1 OC和C对比</h3>

##### 1.源文件对比
* C语言中常见源文件.h头文件，.c文件：

文件扩展名 | 源类型
-------- | --------
.h       | 头文件，用于存放函数声明
.c       | C语言源文件，用于实现头文件声明的方法

* OC中的源文件.h头文件，.m与.mm的实现文件

文件扩展名 | 源类型
-------- |---------
.h       | 头文件，头文件包含类、方法、属性的声明
.m/.mm   | 类的实现文件，参与编译的文件，用来实现类中的声明方法


#####  2.关键字对比
* C语言的关键字逗可以在OC源程序中使用
* OC新增的关键字在使用时，主意部分关键字以"@"开头
  
  例如
```objc
    @interface @implementation @end
    @public @protected @private @selector
    @protocol @optional @required 等
```
       
      
#####  3.数据类型对比
* C语言数据类型

![c数据类型.png](http://upload-images.jianshu.io/upload_images/328309-8765658e6ea9d6c7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* OC数据类型

![oc数据类型2.png](http://upload-images.jianshu.io/upload_images/328309-c5174734a85d68de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

类型 | 描述
------------ | ------------
BOOL | 只有两个取值：真和假
NSObject * | OC中的对象类型
id | 动态对象类型，万能指针
SEL | 选择器数据类型
block | 代码快数据类型

* OC中的类
 	* Objective-C是一种面向对象的语言
 	* 那什么是类呢？类是用来描述对象的，它是一系列方法和属性的集合
 	* Objective-C的类声明和实现包括两个部分：接口部分和实现部分
 	* 想要定义方法（也就是C语言中的函数），那么就必须先有类的存在

	
##### 4.流程控制语句对比
* C语言中使用的流程控制语句OC中都可以应用

```objc
if 语句
switch 语句
while 语句
do while 语句
for 语句
break 关键字
continue 关键字
```
* 增强for循环，用于快速迭代数组或者集合
* C语言for循环

```objc
for (int i = 0; i < 10; i++){
	printf("%d", i);
}
```
* OC增强for循环

```objc
for (NSString *name in NSArray){
	NSLog(@"%@", name);
}
```


##### 5.方法（函数）定义和声明对比
* C语言中函数的声明和实现
	* 函数声明: int sum(int a, int b);
	* 函数实现: int sum(int a, int b){return a+b;}
* OC中的方法
	* 方法声明： -(int)sum:(int)a andB:(int)b;
	* 方法实现： -(int)sum:(int)a andB:(int)b{return a+b;}

* 注意：方法只能卸载类里面，而函数可以卸载任何地方
	* 对象方法，使用对象调用的方法
	* 类方法，使用类名调用的方法
	

	
```objc
对象方法
- (id)initWithString:(NSString *)name;
类方法
+ (MyClass *)createMyClassWithString:(NSString *)name;
```	 


##### 6.面向对象特性
* 封装性
* 继承性
* 多态性

![mxdx.png](http://upload-images.jianshu.io/upload_images/328309-37ebf984d1d47428.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##### 7.面向对象新增语法
* 属性生成器
	* @property
	* @synthesize
	
```objc
// 声明属性
@property (nonatomic, strong)NSString *name;

// 合成属性
@synthesize name = _name;
```

* 分类
	* 分类与继承
	* 使用分类扩展类，无需子类化
	
```objc
@interface NSString (MyNSString)
- (NSString *) encrypWithMD5;
@end
```	
* 协议
	* 使用协议声明方法
	* 协议类似于C#,java中的接口
```objc
@protocol MyProtocol
- (void)myProtocolMethod;
@end;
```	 
* Foundation框架
	* 创建和管理集合，如数组和字典
	* 访问存储在应用中的图像和其他资源
	* 创建和官吏字符串
	* 发布和观察通知
	* 创建日期和时间对象
	* 操控URL流
	* 异步执行代码
	
##### 8.新增异常处理
* 用于处理错误信息
* 格式：
	* @try ... @catch ... @finally
* 示例

```objc
// 创建对象car
Car *car = [][Car alloc] init];
@try{
// 调用一个没有实现的方法
	[car test];
}@catch (NSException *exception){
	NSLog(@"%@", exception.name);
}@finally{
	NSL(@"继续执行!");
}
```

<h3 id="1.2">1.2 第一个OC程序</h3>

##### 1.如何创建Objective-C项目
* 创建工程
![创建工程1.png](http://upload-images.jianshu.io/upload_images/328309-19783f412de47ef2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程2.png](http://upload-images.jianshu.io/upload_images/328309-26067fdfc6d9955e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程3.png](http://upload-images.jianshu.io/upload_images/328309-654ae5603146c91f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程4.png](http://upload-images.jianshu.io/upload_images/328309-3a152b8f5f433692.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 2.\#import和#include区别
* \#import和#include的类似，都是把其后面的文件拷贝到该指令所在的地方
* \#import可以自动防止重复导入
* \#import<>用于包含系统文件
* \#import""用于包含本项目中的文件
* \#import告诉编译器找到并处理名为Foundation.h的文件，这是一个系统文件，\#import表示将该文件的信息导入到程序中。
* 框架地址：/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneO S.sdk/System/Library/Frameworks/


##### 3.NSLog和printf区别
* NSLog是Foundation框架􏰀供的Objective-C日志输出函数,与标准C中的printf函数类似,并可以格式化输出。

	* NSLog传递进去的格式化字符是NSString的对象,而不是char *这种字符串指针
	* NSLog输出的内容中会自动包含一些系统信息
	* NSLog输出的内容会自动换行
* NSLog声明在NSObjCRuntime.h中
	* 声明：void NSLog(NSString *format, ...);
	
```objc
NSLog(@“this is a test”); //打印一个字符串
NSString *str = @"hello!”;
NSLog(@"string is:%@",str);//使用占位符,%@表示打印一个对象,%@ OC特有的
NSLog(@"x=%d, y=%d",10,20);//使用多个占位符,%d表示整型数
```
##### 4."@"的使用方法
* 在OC中"@"有特殊的用法
	* "@"这个符号表示将一个C的字符串转化为OC中的字符串对象NSString
	* OC中大部分的关键字都是以@开头的，比如@interface, @implemention, @end等


##### 5.NS前缀 
* NS来自于NeXTStep的一个软件 NeXT Software
* OC中不支持命名空间(namespace)
* NS是为了避免命名冲突而给的前缀
* 看到NS前缀就知道是Cocoa中的系统类的名称


<h3 id="1.3">1.3 面向对象思维</h3>

##### 1.面向对象基本概念
* 面向对象(Object Oriented,OO)是软件开发方法
* 面向对象是一种对现实世界理解和抽象的方法，是计算机编程技术发展到一定阶段后的产物。
* Object Oriented Programming-OOP ——面向对象编程

##### 2.面向对象和面向过程区别
* 面向对象是相对面想过程而言
* 面向对象和面向过程都是一种思想
* 面向过程
	* 强调的是功能行为
	* 关注的是解决问题需要哪些步骤
* 面向对象
	* 将功能进行封装，强调具备功能的对象
	* 关注的是解决问题需要哪些对象

	
##### 3.面向对象的特点
* 可以将复杂的事情简单化
* 将程序员从执行者转化为指挥者
* 完成需求时：
	* 先要去找具有所需的功能的对象来用
	* 如果该对象不存在，那么创建一个具有所需功能的对象
	* 这样简化开发并提高复用
	

<h3 id="1.4">1.4 类与对象</h3>

##### 1.类与对象的关系
* 面向对象的核心就是对象,那怎么创建对象?
    * OC中创建对象比较复杂, 首先要理解一个概念叫做类.
    * 现实生活中是根据一份描述,一份模板创建对象,编程语言也一样,也必须先有一份描述,在这个描述中说清楚将来创建出来的对象有哪些属性和行为
* OC中的类相当于图纸，用来描述一类事物。也就是说，要想创建对象必须先有类
* OC利用类来创建对象，对象是类的具体存在, 因此面向对象解决问题应该是先考虑需要设计哪些类，再利用类创建多少个对象



<h3 id="1.5">1.5 类的设计</h3>

##### 1.如何设计一个类
* 生活中描述事物无非就是描述事物的名称/属性和行为。
    * 如：人有身高，体重等属性，有说话，打架等行为。
    ```objc
    事物名称(类名):人(Person)
    属性:身高(height)、年龄(age)
    行为(功能):跑(run)、打架(fight)
    ```
* OC中用类来描述事物也是如此
    * 属性：对应类中的成员变量。
    * 行为：对应类中的成员方法。
* 定义类其实在定义类中的成员(成员变量和成员方法)

##### 2.如何分析一个类
* 一般名词都是类(名词提炼法)
    * 飞机发射两颗炮弹摧毁了8辆装甲车
    ```objc
    飞机
    炮弹
    装甲车
    ```
    * 隔壁老王在公车上牵着一条叼着热狗的草泥马
    ```objc
    老王
    公交车
    热狗
    草泥马
    ```
* 拥有相同(或者类似)属性（状态特征）和行为（能干什么事）的对象都可以抽像成为一个类



<h3 id="1.6">1.6 第一个OC类</h3>

#####  1.如何声明一个类
* 格式
![声明格式.png](http://upload-images.jianshu.io/upload_images/328309-10511b2c706af717.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


* 注意：
    * 1.必须以@interface开头，@end结尾
    * 2.成员变量的声明，必须写在@interface与@end之间的大括号中
    * 3.方法的声明必须在{}下面，不能写在{}中



##### 2.如何实现一个类
* 格式

```objc
@implementation MyClass

- (id)initWithString:(NSString *)aName
{
    //写代码处
}

+ (MyClass *)myClassWithString:(NSString *)aName
{
    //写代码处
}

@end
```
* 注意：
    * 1.必须以@implementation开头，@end结尾
    * 2.类名必须和声明的一致


##### 3.如何创建一个对象
* 用类的方式告诉计算机，我们需要一个什么样的对象，之后我们要在程序中使用这个对象，就必须先创建一个对象

![创建对象.png](http://upload-images.jianshu.io/upload_images/328309-30b973ce1bd2b02d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


* 注意[Car new];做了三件事
    * 1.在堆内存中开辟了一块新的存储空间
    * 2.初始化成员变量(写在类声明大括号中的属性就叫成员变量,也叫实例变量)
    * 3.返回指针地址
* 消息机制
    * 使用对象调用方法就是OC中的消息机制
    * OC中调用方法的格式：[类名或者对象名 方法名]; 

![调用方法.png](http://upload-images.jianshu.io/upload_images/328309-2a00f4750d56d0f7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 4.对象的注意点
* 可以通过 对象->对象成员(注意声明属性为:@public) 的方式访问对象中的成员,
* 每一个对象中都有一份属于自己的属性。
* 对其中一个对象的成员进行了修改。和另一个对象没有关系


<h3 id="1.7">1.7 对象方法的声明和实现</h3>

##### 1.对象方法声明
* 格式 
![对象方法声明.png](http://upload-images.jianshu.io/upload_images/328309-a763eb62276aad99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 特征
    * 对象方法以-开头如 -(void)xx;
    * 对象方法只能由对象来调用
    * 对象方法中可以访问当前对象的成员变量
    * 调用格式 [对象名 对象方法名];
* 示例

```objc
//声明没有返回值的对象方法
- (void)method;
//声明有返回值的对象方法
- (int)method;
//声明有返回值有参数的对象方法
- (int)method: (int)var;
//声明有返回值有多个参数的对象方法
- (int)method: (int)var1 andVar2: (int)var2;
```

##### 2.对象方法实现
+ 必须写在以@implementation开头，@end之间
+ 在声明的后面加上{}即表示实现
+ 将需要实现的代码写在{}中


<h3 id="1.8">1.8 对象方法的声明和实现</h3>

##### 1.类方法声明
* 格式
    * 将对象方法-号变为+号

* 特征
    * 类方法以+开头 如+(void)put;
    * 类方法只能由类来调用
    * 类方法中不能访问实例(成员)变量,因为类方法由类来调用,并没有创建存储空间来存储类中的成员变量。

* 类方法的好处:
    * 节省内存空间
    * 不依赖于对象,执行效率更高;
    * 能用类方法解决的问题,尽量使用类方法;

* 类方法的场合:
    * 当方法内部不需要使用到成员变量时,可以改为类方法
    * 类方法一般用于编写工具方法

* 示例

```objc
//声明没有返回值的类方法
+ (void)method;
//声明有返回值的类方法
+ (int)method;
//声明有返回值有参数的类方法
+ (int)method: (int)var;
//声明有返回值有多个参数的类方法
+ (int)method: (int)var1 andVar2: (int)var2;
```

##### 2.类方法实现
+ 必须写在以@implementation开头，@end之间
+ 在声明的后面加上{}即表示实现
+ 将需要实现的代码写在{}中

##### 3.对象方法和类方法区别
* 对象方法
    * 对象方法是属于对象的
    * 以减号-开头
    * 只能让对象调用，没有对象，这个方法根本不可能被执行
    * 对象方法能访问实例变量（成员变量）
    * 对象方法中可以调用当前对象的对象方法
    * 对象方法中可以调用其他对象的对象方法
    * 对象方法中不可以调用类方法


* 类方法
    * 类方法是属于类的
    * 以加号+开头
    * 只能用类名调用，对象不能调用
    * 类方法中不能直接访问实例变量（成员变量）
    * 类方法中不能直接调用对象方法，要想调用对象方法，必须创建或传入对象。


* 使用场合：
    * 当不需要访问成员变量的时候，尽量用类方法


* 类方法和对象方法可以同名



<h3 id="1.9">1.9 对象的存储细节</h3>

##### 1.对象的存储细节

* 类创建对象,每个对象在内存中都占据一定的存储空间,每个对象都有一份属于自己的单独的成员变量,所有的对象公用类的成员方法,方法在整个内存中只有一份,类本身在内存中占据一份存储空间,类的方法存储于此。

![对象的存储细节.png](http://upload-images.jianshu.io/upload_images/328309-441ac77d41bfca05.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
##### 2.isa指针

* 每一个对象都包含一个isa指针.这个指针指向当前对象所属的类。
* [p eat];表示给p所指向的对象发送一条eat消息,调用对象的eat方法,此时对象会顺着内部的isa指针找到存 储于类中的方法,执行。
* isa是对象中的隐藏指针,指向创建这个对象的类。
* 通过isa指针我们可以在运行的时候知道当前对象是属于那个Class（类）的 
![isa指针.png](http://upload-images.jianshu.io/upload_images/328309-652714ed3d52f7f9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 3.使用一个类创建多个对象
```objc
Car *car1 = [Car new];
Car *car2 = [Car new]
```


<h3 id="1.10">1.10 函数与方法对比</h3>

* 对象方法:
    * (1)对象方法的实现只能写在@implementation...@end中,对象方法的声明只能写在 @interface...@end中间
    * (2)对象方法都以-号开头,类方法都以+号开头
    * (3)对象方法只能由对象来调用,类方法只能由类来调用,不能当做函数一样调用
    * (4)函数属于整个文件,可以写在文件中的任何位置,包括@implementation...@end中,但写在 @interface...@end会无法识别,函数的声明可以在main函数内部也可以在main函数外部。
    * (5)对象方法归类\对象所有


* 函数:
    * (1)所有的函数都是平行的
    * (2)函数不存在隶属关系
    * (3)使用的时候可以直接调用
    * (4)不可以访问对象中的成员变量
    

<h3 id="1.11">1.11 常见错误</h3>

* 1)@interface @end和@implementation @end不能嵌套包含
* 2) OC是弱语法,可以只有@implementation,但实际开发中千万不要这样。
* 3）漏写@end
* 4）两个类的对象声明顺序(可以把顺序打乱)
* 5）成员变量没有写在{}里
* 6）方法的声明写在了{}里面
* 7）在声明时不能对类的成员变量进行初始化,请注意成员变量不能脱离对象而独立存在
* 8）方法无法像函数那样的调用
* 9）成员变量和方法不能用static等关键字修饰,不要和c语言混淆
* 10）类的实现可以写在mian函数后面,在使用之前只要有声明就可以




<h2 id="2">2. OC开发简介</h2>

<h3 id="2.1">2.1 NSString 类介绍及用法</h3>

##### 1.NSString常见方法

* NSString是Objective-C 中核心处理字符串的类之一

* 创建常量字符串,注意使用“@“符号。
```objc
NSString *astring = @"This is a String!";
```
* 创建空字符串,给予赋值。
```objc
NSString *string = [NSString new];
string = @"chefzhang";
```
* 创建格式化字符串:占位符(由一个%加一个字符组成)
```objc
[NSString stringWithFormat:@"chefzhang体重%i岁了", 130];
```

##### 2.NSString字符串长度计算

* 通过调用NSString类的对象方法 length 可以获得字符串的长度
* 字符串长度是指该字符串中一共有多个字符(无论是中文还是英文)

* 纯英文字符
```objc
    NSString *str = @"tom";
    NSLog(@"length = %i", [str length]);
    输出结果:3
```
    
* 中英文混合
```objc
    NSString *str = @"tom杨";
    NSLog(@"length = %i", [str length]);
    输出结果:4
```

* 纯中文
```objc
    NSString *str = @"杨春福";
    NSLog(@"length = %i", [str length]);
    输出结果:3
```

* NSUInteger 就是 unsigned long
```objc
源码：
typedef unsigned long NSUInteger;
```

<h3 id="2.2">2.2 结构体成员变量</h3>

##### 1.结构体成员变量

* 设计一个”学生“类 1> 属性
    * 姓名
    * 生日
    * 用结构体作为类的实例变量(生日)

```objc
\#import <Foundation/Foundation.h> //定义生日的结构体
typedef struct{
    int year;
    int month;
    int day;
}MyDate;

@interface Person : NSObject
{
    @public
    NSString *_name;//定义姓名 MyDate _birthday;//定义生日
}
@end

@implementation Person
@end


int main(int argc, const char * argv[]) {
    Person *p = [Person new];
    p->_name = @"sb";

    //因为结构体已经初始化为0了,在次初始化就报错了,但是可以逐个赋值。
    //p->_birthday = {1990,12,3};
    p->_birthday.year = 2014;
    p->_birthday.month = 05;
    p->_birthday.day = 12;
    NSLog(@"%@的生日是:%d年%d月%d 日",p->_name,p->_birthday.year,p->_birthday.month,p->_birthday.day);

    //也可以整体赋值
    MyDate de={1993,11,11};
    p->_birthday = de;
    NSLog(@"%@的生日是:%d年%d月%d 日",p->_name,p->_birthday.year,p->_birthday.month,p->_birthday.day);
    return 0;
}
```

<h3 id="2.3">2.3 对象和方法之间的关系</h3>

##### 1.对象作为方法的参数

* 对象作为方法参数传递是地址传递，因为对象是一个指针变量
* 在方法内部，可以通过对象形参，访问该对象的成员变量(如果该对象的该成员变量的访问权限是public的)
* 在方法内部，可以通过对象形参，调用该对象上的方法（给这个对象发送消息）

```objc
int main(int argc, const char * argv[])
{
    //    1.创建士兵对象
    Soldier *s1 = [Soldier new];
    s1->_name = @"jack";
    s1->_life = 10;
    s1->_level = kSoldierLevel1;

    //    2.创建枪对象
    Gun *gun = [Gun new];
    gun->_bulletCount = 100;

    //    3.射击
    [s1 fireByGun:gun];
}

@implementation Soldier

- (void)fireByGun:(Gun *)gun
{
    [gun shoot];
}

@end
```

##### 2.对象作为方法的返回值
* 对象可以作为方法的返回值；
* 对象返回值的实质是返回指向该对象的指针，该对象是存储在堆内存中的。
* 由于堆内存是由程序员管理的，所以它不会因为函数结束而被销毁

```objc
@implementation Shop

- (Gun *)buyGun
{
    Gun *gun = [Gun new];
    gun->_bulletCount = 100;
    return gun;
}

@end
```

<h3 id="2.4">2.4 pragma mark指令</h3>

##### 1.#pragma mark指令的使用

* 功能:简单来说就是对代码的分组,方便代码查找和导航用的 它们告诉Xcode编译器,要在编辑器窗格顶部的方法和函数弹出菜单中将代码分隔开。一些类(尤其是一些控制器类)可能很长,方法和函数弹出菜单可以便于代码导航。此时加入#pragma 指令(#pragma是一个编译指令)对代码进行逻辑组织很有效果。

* 一个类里我们总会有一些方法的功能与性质是相差不多的,你可能会有把方法们分组的想法。Xcode已经有了类似的支持,它就是 #pragma mark。
    * 分组: #pragma mark 分组(标识)名称 
    ![分组.png](http://upload-images.jianshu.io/upload_images/328309-418589b5856d32ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    * 分隔线: #pragma mark - 
    ![分割线.png](http://upload-images.jianshu.io/upload_images/328309-a696da406fe0ed15.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    * 分割线加分组: #pragma mark - 分组(标识)名称 
    ![分割线加分组.png](http://upload-images.jianshu.io/upload_images/328309-dae0208fb22d3609.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    
<h3 id="2.5">2.5 对象作为方法的参数连续传递</h3>

##### 1.对象作为方法的参数连续传递
```objc
实现功能:士兵开枪 枪射击子弹
枪类:
名称:Gun 属性:型号(_size),子弹个数(_bulletCount) 行为:射击
人类
名称:Soldier
属性:姓名(_name) life level(等级) 行为:跑蹲开枪 跳
```

```objc
#import <Foundation/Foundation.h>
/*
 士兵
 事物名称: 士兵(Soldier)
 属性:姓名(name), 身高(height), 体重(weight)
 行为:打枪(fire), 打电话(callPhone)
 
 枪
 事物名称:枪(Gun)
 属性:弹夹(clip) , 型号(model)
 行为:上弹夹(addClip)
 
 弹夹
 事物名称: 弹夹(Clip)
 属性:子弹(Bullet)
 行为:上子弹(addBullet)
 */

@interface Gun : NSObject
{
    @public
    int _bullet; // 子弹
}

// 射击
- (void)shoot;

@end

@implementation Gun
- (void)shoot
{
    // 判断是否有子弹
    if (_bullet > 0) {
        
        _bullet--;
        NSLog(@"打了一枪 %i", _bullet);
    }else
    {
        NSLog(@"没有子弹了, 请换弹夹");
    }
}
@end



@interface Soldier : NSObject
{
    @public
    NSString *_name;
    double _height;
    double _weight;
}
//- (void)fire;
- (void)fire:(Gun *)gun;

@end

@implementation Soldier

/*
- (void)fire
{
    NSLog(@"打了一枪");
}
 */

//  Gun * g = gp
- (void)fire:(Gun *)g
{
//    NSLog(@"打了一枪");
    [g shoot];
}

@end

int main(int argc, const char * argv[]) {
    
    // 1.创建士兵
    Soldier *sp =[Soldier new];
    sp->_name = @"屎太浓";
    sp->_height = 1.88;
    sp->_weight = 100.0;
    
    // 2.创建一把枪
    Gun *gp = [Gun new];
    gp->_bullet = 10;
    
    // 2.让士兵开枪
//    [sp fire];
    // 让对象作为方法的参数传递
    [sp fire:gp]; // 地址
    [sp fire:gp];
    [sp fire:gp];
    [sp fire:gp];
    [sp fire:gp];
    [sp fire:gp];
    
    return 0;
}
```

<h3 id="2.6">2.6 OC多文件开发介绍</h3>

##### 1.为什么要使用多文件

* 一个真正的iOS项目中可能会有成百上类，如果这些类都写在一个文件中，那么文件就会很大，想找到自己需要类都变的异常困难，开发效率低下

* 一个iOS项目可能会有多个人开发，如果多个人同时修改一个文件，那么就很可能会产生冲突，比如这个增加一个方法，那个人把这方法删掉了。另外就是当把多个人写功能合并起来的时候，也非常困难，写到一个文件中，无法顺畅的进行团队合作。

##### 2.@interface和@implementation的分工
* @interface就好像暴露在外面的时钟表面
* @implementation就好像隐藏在时钟内部的构造实现
![interface和implementation.png](http://upload-images.jianshu.io/upload_images/328309-aef80fcc216728a7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####3.在OC中如何进行多文件开发？

* 在工作中,通常把不同的类放到不同的文件中,每个类的声明和实现分开
    * 声明写在.h头文件中,
    * 实现写在相应的.m文件中去,
    * 类名是什么,文件名就是什么。
```objc
假设有两个类,分别是Person类和Dog类,则通常有下面五个文件:
(1)Person.h Person类的声明文件
(2)Person.m Person类的实现文件
(3)Dog.h Dog类的声明文件
(4)Dog.m Dog类的实现文件
(5)Main.m 主函数(程序入口) 在主函数以及类的实现文件中要使用#import包含相应的头文件。
```

##### 4.使用多文件开发好处

* 显著提高团队协作的效率
* 提高程序的开发速度
* 提高程序的可维护性
* 提高代码的可读性


<h2 id="3">3. 面向对象的三大特性</h2>

##### 1.面向对象三大特性
* 封装性
* 继承性
* 多态性

##### 2.什么是封装
* 封装性就是隐藏实现细节，仅对外公开接口。

##### 3.为什么要进行封装?
* 以下代码存在的问题?

```objc
// 1成员变量是public的,也就是公开的,我们不能控制外界如何赋值, 外界有可能赋值一些脏数据
@interface Gun : NSObject
{
    @public// 公开成员变量
    int _bulletCount;// 子弹数量
}
@end

// 可以利用封装来解决这个问题
// 封装:是指隐藏对象的属性和实现的细节,仅对外提供公共的访问方法
```


* 类是数据与功能的封装，数据就是成员变量，功能就类方法或对象方法
* 对数据的封装，也就是对成员变量的封装
* 不封装的缺点：当一个类把自己的成员变量暴露给外部的时候,那么该类就失去对该成员变量的管理权，别人可以任意的修改你的成员变量。
* 封装就是将数据隐藏起来,只能用此类的方法才可以读取或者设置数据,不可被外部任意修改是面向对象设计本质。这样降低了数据被误用的可能性 ，提高代码的灵活性!


##### 4.封装的好处
* 好处
	* 将变化隔离
	* 提高安全性

* 原则
	* 将不需要对外提供的内容都隐藏起来,把属性都隐藏,提供公共的方法对其访问
	

<h3 id="3.1">3.1 getter/setter方法</h3>

##### 1.setter方法
* 作用：用来设置成员变量，可以在方法里面过滤掉一些不合理的值
* 命名规范：
	* 必须是对象方法
	* 返回值类型为void
	* 方法名必须以set开头，而且后面跟上成员变量名去掉”_” 首字母必须大写
	* 必须提供一个参数，参数类型必须与所对应的成员变量的类型一致
	* 形参名称和成员变量去掉下划线相同
	
* 举例:
```objc
如：如果成员变量为int _age 那么与之对应seter方法为
-(void) setAge: (int) age;
```
* setter方法的好处
	* 不让数据暴露在外,保证了数据的安全性
	* 对设置的数据进行过滤 
	
##### 2.getter方法
* 作用：为调用者返回对象内部的成员变量的值
* 命名规范：
	* 必须是对象方法
	* 必须有返回值,返回值的类型和成员变量的类型一致
	* 方法名必须是成员变量去掉下划线
	* 一定是没有参数的	
	
* 举例

```objc
如：如果成员变量为int _age 那么与之对应geter方法为
- (int) age;
``` 
	
* getter方法的优点：
	* 可以让我们在使用getter方法获取数据之前,对数据进行加工；
	* 比如双十一活动，我们希望对全线商品的价格在原来的价格基础上打五折，那么我们只要去改成品类的价格的getter方法就可以了，让他返回的值为价格 * 0.5	
	
##### 3.getter/setter方法注意
* 在实际的开发中,不一定set和get方法都会提􏰀供,如果内部的成员变量,比如学生的学号或计算出来的数据。这样的数据只允许外界读取，但是不允许修改的情况,则通常只提供get方法而不􏰀提供set方法 。
* 成员变量名的命名以下划线开头,get方法名不需要带下划线
* 成员变量名使用下划线开头有两个好处
	* 与get方法的方法名区分开来
	* 可以和一些其他的局部变量区分开来,下划线开头的变量,通常都是类的成员变量。当我看到以下划线开头变量，那么他一定是成员变量
	
<h3 id="3.2">3.2 自定义代码段</h3>

##### 1.如何自定义代码片段
* 将代码拖拽到code区域 
![将代码拖拽到code区域.png](http://upload-images.jianshu.io/upload_images/328309-0baaba4e65b6b4e9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 配置快捷键等信息 
![配置快捷键等信息.png](http://upload-images.jianshu.io/upload_images/328309-9ea95f12e1132b8a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 使用快捷键 
![使用快捷键.png](http://upload-images.jianshu.io/upload_images/328309-793686e82ebf0ef5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![使用快捷键1.png](http://upload-images.jianshu.io/upload_images/328309-60757219b575ca75.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 2.如何导入代码片段
* 将下载好的代码片段拷贝到:/Users/LNJ/Library/Developer/Xcode/UserData/CodeSnippets下
	* 注意将LNJ换为自己的用户名
![如何导入代码片段.png](http://upload-images.jianshu.io/upload_images/328309-ffbacdb24ec0311e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<h3 id="3.3">3.3 点语法</h3>

##### 1.点语法的本质
* 其实点语法的本质还是方法调用
* 当使用点语法时，编译器会自动展开成相应的方法
![点语法本质.png](http://upload-images.jianshu.io/upload_images/328309-3ccf1cb9cf25129e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 当点语法使用在 “=“赋值符号左侧的时候，点语法会被展开为setter方法的调用，其他情况（等号右侧、直接使用）为点语法展开为getter方法的调用

##### 2.点语法注意
* 点语法的本质是方法的调用,而不是访问成员变量,当使用点语法时,编译器会自动展开成相应的方法调用。
* 切记点语法的本质是转换成相应的对setter和getter方法调用,如果没有set和get方法,则不能使用点语法。
* 不要在getter 与 setter方法中使用本属性的点语法

```objc
- (void) setAge:(int)age {
    // 下面的代码会引发死循环
    self.age = age;
        //编译器展开后 [self setAge:age]
}


- (int) age {
    // 下面的代码会引发死循环
    return self.age;
          // 编译器展开后 [self   age]
}
```
**总结：如果给属性提供了getter和setter方法，那么访问属性就又多了一种访问方式，点语法
点语法其实它的本质是调用了我们的setter和getter方法。没有setter和getter方法，就没有点语法！**

<h3 id="3.4">3.4 self关键字</h3>

##### 1.类方法中的self
* 在整个程序运行过程中，一个类有且仅有一个类对象。
* 通过类名调用方法就是给这个类对象发送消息。
* 类方法的self就是这个类对象
* 在类方法中可以通过self来调用其他的类方法
* 不能在类方法中去调用对象方法或成员变量，因为对象方法与成员变量都是属于具体的实例对象的。


```objc
main.m文件

Person *p = [Person personWithName:name];

Person.m文件
+ (instancetype)personWithName:(NSString *)name
{
	// 此处的self就是Person类
	return [[self alloc]initWith:name];
}
```

##### 2.对象方法中的self

* 在整个程序运行过程中，对象可以有0个或多个
* 通过对象调用方法就是给这个对象发送消息
* 对象方法中self就是调用这个方法的当前对象。
* 在对象方法中，可以通过self来调用本对象上的其他方法
* 在对象方法中，可以通过self来访问成员变量


```objc
main.m文件
Person *p = [[Person alloc] initWithName:name];

Person.m文件
- (instancetype)initWithName:(NSString *)name
{
	// 此处的self就是p对象
	Person *p = [[Person alloc] init];
	p.name = name;
	return p;
}
```

##### 3.全局变量成员变量局部变量
* 全局变量：只要是有声明它的地方都能使用
* 成员变量：只能在本类和其子类的对象方法中使用
* 局部变量：只能在本函数或方法中使用
* 从作用域的范围来看：全局变量 > 成员变量 > 局部变量
* 当不同的作用域中出现了同名的变量，内部作用域的变量覆盖外部作用域变量，所以同名变量的覆盖顺序为：局部变量覆盖成员变量，成员变量覆盖全局变量
* 如果在对象方法中出现与成员变量同名的局部变量，如果此时想使用该成员变量可以通过self->成员变量名的方式

##### 4.self总结
* 谁调用self所在的方法，那么self就是谁
* self在类方法中，就是这个类的类对象，全局只有一个，可通过self调用本类中的其他类方法，但是不能通过self来调用对象方法或访问成员变量
* self在对象方法中，就是调用这个方法的那个对象， 可以通过self调用本类中其他的对象方法，访问成员变量，但不能通过self调用本类的类方法。
* 通过self调用方法的格式：[self 方法名];
* 通过self访问成员变量格式：self->成员变量名

##### 5.self使用注意
* 同时有对象方法和类方法存在的时候,self不会调错
* self只能在方法中使用;不要使用self来调用函数，也不可以在函数内部使用self；
* 使用self调用本方法，导致死循环调用。

<h3 id="3.5">3.5 继承</h3>

##### 1.继承基本概念
* 现实生活中的继承 
![汽车继承.png](http://upload-images.jianshu.io/upload_images/328309-03e8f04089c2ab28.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 交通工具类是一个基类(也称做父类),通常情况下所有交通工具所共同具备的特性，如速度与额定载人的数量

* 按照生活常规,我们来继续给交通工具来细分类的时候,我们会分别想到有汽车类和飞机类等,汽车类和飞机类同样具备速度和额定载人数量这样的特性,而这些特性是所有交通工具所共有的,那么就可以让汽车或飞机类继承交通工具类，这样当建立汽车类和飞机类的时候我们无需再定义交通工具类（基类）中已经有的成员和方法,而只需要􏰁述汽车类和飞机类所特有的特性即可。

* 飞机类和汽车类的特性是由在交通工具类原有特性基础上增加而来的,那么飞机类和汽车类就是交通工具类的派生类(也称做子类)。以此类推,层层递增, 这种子类获得父类特性的概念就是继承

##### 2.OC中的继承关系
![OC中的继承关系.png](http://upload-images.jianshu.io/upload_images/328309-f1c065868d5e8087.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* B类继承A类，那么B类将拥有A类的所有属性和方法，此时我们说A类是B类的父类，B类是A类的子类
* C类继承B类，那么C类将拥有B类中的所有属性和方法，包括B类从A类中继承过来的属性和方法，此时我们说B类是C类的父类，C类是B类的子类
* 注意:
	* 基类的私有属性能被继承,不能在子类中访问。
	* OC中的继承是单继承:也就是说一个类只能一个父类,不能继承多个父类
	* 子类与父类的关系也称为isA（是一个）关系，我们说 子类isA父类，也就是子类是一个父类，比如狗类继承动物类，那么我们说狗isA动物，也就是狗是一个动物。在如汽车继承交通工具，那么们说汽车isA交工工具，也就是汽车是一个交通工具
	* 继承的合理性:引用《大话西游》里的一句话来描述继承的。“人是人他妈生的,妖是妖他妈生的!”
	
	
##### 3.OC中如何实现继承
* 在声明子类的时候，在子类名称后面通过：父类名称方式来实现继承	

```objc
@interface 子类名称 : 父类名称

@end
```


<h3 id="3.6">3.6 继承相关特性</h3>

##### 1.方法重写
* 在子类中实现与父类中同名的方法，称之为方法重写；
* 重写以后当给子类发送这个消息的时候，执行的是在子类中重写的那个方法，而不是父类中的方法。
* 如果想在子类中调用被子类重写的父类的方法，可以通过super关键字
* 使用场景：当从父类继承的某个方法不适合子类,可以在子类中重写父类的这个方法。

##### 2.继承中方法调用的顺序
* 1、在自己类中找
* 2、如果没有,去父类中找
* 3、如果父类中没有,就去父类的父类中
* 4、如果父类的父类也没有,就还往上找,直到找到基类(NSObject)
* 5、如果NSObject都没有就报错了
    * 如果找到了就执行这个方法，就不再往后查找了



##### 3.继承的注意事项
* 子类不能定义和父类同名的成员变量，私有成员变量也不可以；因为子类继承父类，子类将会拥有父类的所有成员变量，若在子类中定义父类同名成员变量 属于重复定义。

* OC类支持单一继承,不支持多继承；也就是说一个类只能有一个直接父类

* 子类继承父所有属性，但是不代表就有权限访问属性（父类中有定义@private的，子类就不能访问）

* OC类支持多层继承 ,如下图所示
![OC支持多层继承.png](http://upload-images.jianshu.io/upload_images/328309-eaae0f33bd506252.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


<h3 id="3.7">3.7 Super关键字</h3>

##### 1.super基本概念
* super是个编译器的指令符号,只是告诉编译器在执行的时候,去调谁的方法.
    * self是一个隐私参数;
```objc
self refers to the object receiving a message in objective-C programming.
```
    * super 并不是隐藏的参数，它只是一个“编译器指示符”，它和 self 指向的是相同的消息接收者
```objc
super is a flag that tells the compiler to search for the method implementation in a very different place. It begins in the superclass of the class that defines the method where super appears.
```

##### 2.super的作用
* 1.直接调用父类中的某个方法
* 2.super在对象方法中，那么就会调用父类的对象方法
     super在类方法中，那么就会调用父类的类方法

* 使用场景：
    * 子类重写父类的方法时想保留父类的一些行为
    

<h3 id="3.8">3.8 多态基本概念</h3>


##### 1.什么是多态?
* 什么是多态:多态就是某一类事物的多种形态
    * 猫: 猫-->动物
    * 狗: 狗-->动物
    * 男人 : 男人 -->人 -->高级动物
    * 女人 : 女人 -->人 -->高级动物

* 程序中的多态:父类指针指向子类对象



##### 2.多态的条件
* 有继承关系
* 子类重写父类方法
* 父类指针指向子类对象
```objc
狗 *g = [狗 new];
动物 *a = [狗 new];
猫 *c = [猫 new];
动物 *a = [猫 new];
```
* 表现：当父类指针指向不同的对象的时候，通过父类指针调用被重写的方法的时候，会执行该指针所指向的那个对象的方法


##### 3.多态的优点
* 多态的主要好处就是`简化了编程接口。`它允许`在类和类之间重用一些习惯性的命名,`而不用为每一个新的方法命名一个新名字。这样,编程接口就是一些抽象的行为的集合,从而和实现接口的类的区分开来。

* 多态也使得代码可以分散在不同的对象中而不用`试图在一个方法中考虑到所有可能的对象。` 这样使得您的代码扩展性和复用性更好一些。当一个新的情景出现时,您无须对现有的代码进行 改动,而只需要增加一个新的类和新的同名方法。

<h3 id="3.9">3.9 多态的实现</h3>

##### 1.如何实现多态
* Animal是父类,子类有Cat 和 Dog,子类分别重写了父类中的eat方法;实例化对象的时候可以用下面的方法:

```objc
Animal *animal = nil;

//实例化猫的对象
animal = [Cat new];
[animal eat];

//实例化狗的对象
animal = [Dog new];
[animal eat];
```



##### 2.多态的原理
- 动态绑定:
    + 动态类型能使程序直到执行时才确定对象的真实类型
    + 动态类型绑定能使程序直到执行时才确定要对那个对象调用的方法


- OC不同于传统程序设计语言,它可以在运行时加入新的数据类型和新的程序模块:动态类型识别,动态绑定,动态加载
- id类型:通用对象指针类型,弱类型,编译时不进行具体类型检查



##### 3.多态的注意点
- 1)如果存在多态,父类是可以访问子类特有的方法
```objc
假设 子类 Dog 有一个特有的方法bark
[dog bark];
Animal *an2 = [Dog new];
[(Dog*)an2 bark]; //把父类的指针,强制类型转换
```

- 2)如果不存在多态,父类是不可以访问子类特有的方法的

```objc
Animal *an3 = [Animal new];
[(Dog*)an3 bark]; //错误的,不能强制转换
```

<h2 id="4">4 实例变量修饰符、@property、构造方法和类工厂方法</h2>

<h3 id="4.1">4.1 实例变量修饰符</h3>

##### 1.实例变量的作用域

![实例变量的作用域.png](http://upload-images.jianshu.io/upload_images/328309-c6945c2934444eb7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 1)@public (公开的)在有对象的前,任何地方都可以直接访问。
- 2)@protected (受保护的)只能在当前类和子类的对象方法中访问
- 3)@private (私有的)只能在当前类的对象方法中才能直接访问
- 4)@package (框架级别的)作用域介于私有和公开之间,只要处于同一个框架中相当于@public,在框架外部相当于@private



##### 2.变量修饰符在子类中的访问
- 1)@private私有成员是能被继承,也不能被外部方法访问。
- 2)@public 公有成员能被继承,也能被外部方法访问。
- 3)@protected 保护成员能够被继承,不能够被外部方法访问。




##### 3.实例变量作用域使用注意事项
- (1)在@interface @end之间声明的成员变量如果不做特别的说明,那么其默认是protected 的。
- (2)一个类继承了另一个类,那么就拥有了父类的所有成员变量和方法,注意所有的成员变量它都拥有,只是有的它不能直接访问。例如@private的



<h3 id="4.2">4.2 description方法</h3>

##### 1.description基本概念

- NSLog(@"%@", objectA);这会自动调用objectA的description方法来输出ObjectA的描述信息.
- description方法默认返回对象的描述信息(默认实现是返回类名和对象的内存地址)
- description方法是基类NSObject 所带的方法,因为其默认实现是返回类名和对象的内存地址, 这样的话,使用NSLog输出OC对象,意义就不是很大,因为我们并不关心对象的内存地址,比较关心的是对象内部的一些成变量的值。因此,会经常重写description方法,覆盖description方法 的默认实现

##### 2.description重写的方法
- 对象方法
```objc
/**对象方法：当使用NSLog输出该类的实例对象的时候调用*/
-(NSString *) description
{
    return [NSString stringWithFormat:@"狗腿数:%d,狗眼数%d\n",_legNum,_eyeNum];
}
```
- 类方法
```objc
/**类方法：当使用NSLog输出该类的类对象的时候调用*/
+(NSString *) description
{
    return @"+开头的description方法";
}
```
##### 3.description陷阱
- 千万不要在description方法中同时使用%@和self,下面的写法是错误的
```objc
\- (NSString *)description {
    return [NSString stringWithFormat:@"%@", self];
}
```
- 同时使用了%@和self,代表要调用self的description方法,因此最终会导致程序陷入死循环,循环调用description方法

- 当[NSString stringWithFormat:@“%@”, self]; 使用它时，循环调用，导致系统会发生运行时错误。

- 当该方法使用NSLog(“%@”,self) 时候， 系统做了相关的优化，循坏调用3次后就会自动退出

<h3 id="4.3">4.3 OC中的私有方法</h3>

##### 1.OC中的私有变量
- 在类的实现,即.m文件中也可以声明成员变量,但是因为在其他文件中通常都只是包含头文件而不会包含实现文件,所以在.m文件中声明的成员变量是@private的。在.m中定义的成员变量不能和它的头文件.h中的成员变量同名,在这期间使用@public等关键字也是徒劳的。

```objc
@implementation Dog
{
    @public
    int _age;
}
@end
```


##### 2.OC中的私有方法
- 私有方法：只有实现没有声明的方法
- 原则上：私有方法只能在本类的方法中才能调用。

    + **注意: OC中没有真正的私有方法**

```objc

	@interface Dog : NSObject

	@end
	@implementation Dog

	\- (void)eat
	{
    	NSLog(@"啃骨头");
	}
	@end
	int main(int argc, const char * argv[]) 	{

    	Dog *d = [Dog new];
    	SEL s1 = @selector(eat);
    	[d performSelector:s1];

	    return 0;
	}
```

<h3 id="4.4">4.4 @property基本概念</h3>

##### 1.什么是@property
- @property是编译器的指令
- 什么是编译器的指令 ？
    + 编译器指令就是用来告诉编译器要做什么！

- @property会让编译器做什么呢？
    + @property 用在声明文件中告诉编译器声明成员变量的的访问器(getter/setter)方法
    + 这样的好处是:免去我们手工书写getter和setter方法繁琐的代码



##### 2.@property基本使用
- 在@inteface中,用来自动生成setter和getter的声明

```objc
用@property int age;就可以代替下面的两行
- (int)age;   // getter
- (void)setAge:(int)age;  // setter
```

- @property编写步骤

```objc
1.在@inteface和@end之间写上@property
2.在@property后面写上需要生成getter/setter方法声明的属性名称, 注意因为getter/setter方法名称中得属性不需要_, 所以@property后的属性也不需要_.并且@property和属性名称之间要用空格隔开
3.在@property和属性名字之间告诉需要生成的属性的数据类型, 注意两边都需要加上空格隔开
```


<h3 id="4.5">4.5 @synthesize基本概念</h3>

##### 1.什么是@synthesize
- @synthesize是编译器的指令
- 什么是编译器的指令 ？
    + 编译器指令就是用来告诉编译器要做什么！
- @synthesize会让编译器做什么呢？
    + @synthesize 用在实现文件中告诉编译器实现成员变量的的访问器(getter/setter)方法
    + 这样的好处是:免去我们手工书写getterr和setter方法繁琐的代码



##### 2.@synthesize基本使用
- 在@implementation中, 用来自动生成setter和getter的实现

```objc
用@synthesize age = _age;就可以代替
- (int)age{
	return _age;
}
- (void)setAge:(int)age{
	_age = age;
}
```

- @synthesize编写步骤

```objc
1.在@implementation和@end之间写上@synthesize
2.在@synthesize后面写上和@property中一样的属性名称, 这样@synthesize就会将@property生成的什么拷贝到@implementation中
3.由于getter/setter方法实现是要将传入的形参 给属性和获取属性的值,所以在@synthesize的属性后面写上要将传入的值赋值给谁和要返回哪个属性的值, 并用等号连接
```

- 以下写法会赋值给谁?

```objc
@interface Person : NSObject
{
    @public
    int _age;
    int _number;
}

@property int age;

@end

@implementation Person

@synthesize age = _number;

@end

int main(int argc, const char * argv[]) {

    Person *p = [Person new];
    [p setAge:30];
    NSLog(@"_number = %i, _age = %i", p->_number, p->_age);

    return 0;
}
```


##### 3.@synthesize注意点
- @synthesize age = _age;
    + setter和getter实现中会访问成员变量_age
    + 如果成员变量_age不存在，就会自动生成一个@private的成员变量_age

- @synthesize age;
    + setter和getter实现中会访问@synthesize后同名成员变量age
    + 如果成员变量age不存在，就会自动生成一个@private的成员变量age

- 多个属性可以通过一行@synthesize搞定,多个属性之间用逗号连接

```objc
@synthesize age = _age, number = _number, name  = _name;

```

<h3 id="4.6">4.6 @property增强</h3>

##### 1.@property增强
- 自从Xcode 4.x后，@property可以同时生成setter和getter的声明和实现

```objc
@interface Person : NSObject
{
    int _age;
}
@property int age;
@end
```


##### 2.@property增强注意点
- 默认情况下，setter和getter方法中的实现，会去访问下划线 _ 开头的成员变量。

```objc
@interface Person : NSObject
{
    @public
    int _age;
    int age;
}
@property int age;

@end

int main(int argc, const char * argv[]) {

    Person *p = [Person new];
    [p setAge:30];
    NSLog(@"age = %i, _age = %i", p->age, p->_age);

    return 0;
}
```

- 如果没有会自动生成一个_开头的成员变量,自动生成的成员变量是私有变量, 声明在.m中,在其它文件中无法查看,但当可以在本类中查看


- @property只会生成最简单的getter/setter方法,而不会进行数据判断

```objc
Person *p = [Person new];
[p setAge:-10];
NSLog(@"age = %i", [p age]);
```
- 如果需要对数据进行判断需要我们之间重写getter/setter方法
    + 若手动实现了setter方法，编译器就只会自动生成getter方法
    + 若手动实现了getter方法，编译器就只会自动生成setter方法
    + 若同时手动实现了setter和getter方法，编译器就不会自动生成不存在的成员变量

<h3 id="4.7">4.7 @property修饰符</h3>

##### 1.@property修饰符
- 修饰是否生成getter方法的
    + readonly    只生成setter方法，不生成getter方法
    + readwrite  既生成getter 又生成setter方法（默认）

```objc
@property (readonly) int age;
```

- 指定所生成的方法的方法名称
    + getter=你定制的getter方法名称
    + setter=你定义的setter方法名称(注意setter方法必须要有 :)

```objc
@property (getter=isMarried)  BOOL  married;
说明，通常BOOL类型的属性的getter方法要以is开头
```

<h3 id="4.8">4.8 id类型</h3>

##### 1.静态类型和动态类型
- 静态类型
    + 将一个指针变量定义为特定类的对象时,使用的是静态类型,在编译的时候就知道这个指针变量所属的类,这个变量总是存储特定类的对象。

```objc
Person *p = [Person new];
```

- 动态类型
    + 这一特性是程序直到执行时才确定对象所属的类

```objc
id obj = [Person new];
```


##### 2.为什么要有动态类型?
- 我们知道NSObject是OC中的基类
- 那么任何对象的NSObject类型的指针可以指向任意对象，都没有问题
- 但是NSObject是静态类型，如果通过它直接调用NSObject上面不存在的方法，编译器会报错。
- 你如果想通过NSObject的指针调用特定对象的方法，就必须把NSObject * 这种类型强转成特定类型。然后调用。如下

```objc
//定义NSObject * 类型
 NSObject* obj = [Cat new];
 Cat *c = (Cat*)obj;
 [c eat];
```

- id 是一种通用的对象类型,它可以指向属于任何类的对象,也可以理解为万能指针 ,相当于C语言的 void *
- 因为id是动态类型,所以可以通过id类型直接调用指向对象中的方法, 编译器不会报错

```objc
/// Represents an instance of a class.
struct objc_object {
    Class isa  OBJC_ISA_AVAILABILITY;
};

/// A pointer to an instance of a class.
typedef struct objc_object *id;
```

```objc
 id obj = [C at new];
 [obj eat]; // 不用强制类型转换

 [obj test]; //可以调用私有方法
```
- 注意：
    + 在id的定义中,已经包好了*号。id指针只能指向OC中的对象
    + 为了尽可能的减少编程中出错，Xcode做了一个检查，当使用id 类型的调用本项目中所有类中都没有的方法，编译器会报错
    + id类型不能使用.语法, 因为.语法是编译器特性, 而id是运行时特性

##### 3.id数据类型与静态类型
- 虽然说id数据类型可以存储任何类型的对象，但是不要养成滥用这种通用类型
    + 如没有使用到多态尽量使用静态类型
    + 静态类型可以更早的发现错误(在编译阶段而不是运行阶段)
    + 静态类型能够提高程序的可读性
    + 使用动态类型前最好判断其真实类型

- 动态类型判断类型
    + \- (BOOL)isKindOfClass:classObj 判断实例对象是否是这个类或者这个类的子类的实例

```objc
    Person *p = [Person new];
    Student *stu = [Student new];

    BOOL res = [p isKindOfClass:[Person class]];
    NSLog(@"res = %i", res); // YES
    res = [stu isKindOfClass:[Person class]];
    NSLog(@"res = %i", res); // YES
```
```objc
    - (BOOL) isMemberOfClass: classObj 判断是否是这个类的实例
```

```objc
    Person *p = [Person new];
    Student *stu = [Student new];

    BOOL res = [p isMemberOfClass:[Person class]];
    NSLog(@"res = %i", res); // YES
    res = [stu isMemberOfClass:[Person class]];
    NSLog(@"res = %i", res); // NO
```

```objc
    + (BOOL) isSubclassOfClass:classObj 判断类是否是指定类的子类
```

```objc
    BOOL res = [Person isSubclassOfClass:[Student class]];
    NSLog(@"res = %i", res); // NO

    res = [Student isSubclassOfClass:[Person class]];
    NSLog(@"res = %i", res); // YES
```

<h3 id="4.9">4.9 new方法实现原理</h3>

##### 1.new方法实现原理
- 完整的创建一个可用的对象:Person *p=[Person new];
- new方法的内部会分别调用两个方法来完成3件事情:
    + (1)使用alloc方法来分配存储空间(返回分配的对象);
    + (2)使用init方法来对对象进行初始化。
    + (3)返回对象的首地址

```objc
This method is a combination of alloc and init. Like alloc, it initializes the isa instance variable of the new object so it points to the class data structure. It then invokes the init method to complete the initialization process.
```

- 可以把new方法拆开如下:
    + (1)调用类方法+alloc分配存储空间,返回未经初始化的对象```Person *p1=[person alloc];```
    + (2)调用对象方法-init进行初始化,返回对象本身
```Person *p2=[p1 init];```
    + (3)以上两个过程整合为一句:```Person *p=[[Person alloc] init];```

- 说明：
    + alloc 与 init合起来称为构造方法，表示构造一个对象
    + alloc 方法为对象分配存储空间，并将所分配这一块区域全部清0.
```objc
The isa instance variable of the new instance is initialized to a data structure that describes the class; memory for all other instance variables is set to 0.
```
    + init方法是初始化方法（构造方法），用来对象成员变量进行初始化，默认实现是一个空方法。
```
An object isn’t ready to be used until it has been initialized. The init method defined in the NSObject class does no initialization; it simply returns self.
```

- 所以下面两句的作用是等价的
```objc
Person *p1 = [Person new];
Person *p = [[Person alloc] init];
```
- iOS 程序通常使用[[类名 alloc] init] 的方式创建对象，因为这个可以与其他initWithXX:...的初始化方法，统一来。代码更加统一

<h3 id="4.10">4.10 构造方法</h3>

##### 1.重写init方法
- 想在对象创建完毕后，成员变量马上就有一些默认的值就可以重写init方法
- 重写init方法格式:

```objc
- (id)init {
    self = [super init];
    if (self) {
        // Initialize self.
    }
    return self;
}
```


- [super init]的作用:
	+ 面向对象的体现,先利用父类的init方法为子类实例的父类部分属性初始化。
- self 为什么要赋值为[super init]:
	+ 简单来说是为了防止父类的初始化方法release掉了self指向的空间并重新alloc了一块空间。还有[super init]可能alloc失败,这时就不再执行if中的语句。

- 重写init方法其它格式

```objc
- (id)init {
    if (self = [super init]) {
        // Initialize self.
    }
    return self;
}
```


##### 2.练习
- 要求通过Person类创建出来的人初始化值都是10岁。

```objc
@implementation Person
- (instancetype)init
{
    if (self = [super init]) {
        _age = 10;
    }
    return self;
}
@end
```

- 让学生继承人类,要求学生对象初始化之后,年龄是10,学号是1,怎么办?

```objc
@implementation Person

- (instancetype)init
{
    if (self = [super init]) {
        _age = 10;
    }
    return self;
}
@end

@implementation Student

- (instancetype)init
{
    if (self = [super init]) {
        _no = 1;
    }
    return self;
}
@end
```



##### 3.构造方法使用注意
- 子类拥有的成员变量包括自己的成员变量以及从父类继承而来的成员变量,在重写构造方法的时候应该首先对从父类继承而来的成员变量先进行初始化。
    + 原则:先初始化父类的,再初始化子类的。
        * 先调用父类的构造方法[super init];
        * 再进行子类内部成员变量的初始化。
- 千万不要把**self = [super init]**写成self **==** [super init]

- 重写构造方法的目的:为了让对象方法一创建出来,成员变量就会有一些固定的值。



##### 4.instancetype的作用
- instancetype与id相似，不过instancetype只能作为方法返回值，它会进行类型检查，如果创建出来的对象，赋值了不相干的对象就会有一个警告信息，防止出错。

```objc
// init此时返回值是id
NSString *str = [[Person alloc] init];
// Person并没有length方法, 但是id是动态类型, 所以编译时不会报错
NSLog(@"length = %i", str.length);
```



```objc
// init此时返回值是instancetype
// 由于instancetype它会进行类型检查, 所以会报警告
NSString *str = [[Person alloc] init];
NSLog(@"length = %i", str.length);
```



```objc
instancetype *p = [[person alloc] init];
// 错误写法instancetype只能作为返回值
```

<h3 id="4.11">4.11 自定义构造方法</h3>

##### 1.自定义构造方法
- 有时候仅仅靠重写构造方法（初始化方法），不能满足需求。比如一个班级中不可能所有学生的年龄都一样，这时候我们需要在创建某个学生的时候能够传入这个学生的年龄。这时候就需要来自定义构造函数（初始化函数）

- 自定义构造方法的规范
    + (1)一定是对象方法,以减号开头
    + (2)返回值一般是instancetype类型
    + (3)方法名必须以initWith开头

- 示例

```objc
@interface Person : NSObject

@property int age;

@property NSString *name;

// 当想让对象一创建就拥有一些指定的值,就可以使用自定义构造方法
- (id)initWithAge:(int)age;

- (id)initWithName:(NSString *)name;

- (id)initWithAge:(int)age andName:(NSString *)name;

@end
```

<h3 id="4.12">4.12 继承中的自定义构造方法</h3>

##### 1.继承中的自定义构造方法

- 不能在子类访问父类私有变量

```objc
@interface Person : NSObject

@property int age;

- (id)initWithAge:(int)age;
@end



@interface Student : Person

@property NSString *name;

- (id)initWithAge:(int)age andName:(NSString *)name;
@end

@implementation Student

- (id)initWithAge:(int)age andName:(NSString *)name
{
    if (self = [super init]) {
//        这个_Age是父类中通过property自动在.m中生成的无法继承,不能直接访问
//        _age = age;
        [self setAge:age];
        _name = name;
    }
    return self;
}
@end
```

- 父类的属性交给父类的方法来处理

```objc
@interface Person : NSObject

@property int age;

- (id)initWithAge:(int)age;
@end



@interface Student : Person

@property NSString *name;

- (id)initWithAge:(int)age andName:(NSString *)name;
@end

@implementation Student

- (id)initWithAge:(int)age andName:(NSString *)name
{
    if (self = [super initWithAge:age]) {
        _name = name;
    }
    return self;
}
@end

```

![继承中的自定义构造方法.png](http://upload-images.jianshu.io/upload_images/328309-85896cbc05f2e910.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 2.自定义构造方法的使用注意
- (1)自己做自己的事情
- (2)父类的属性交给父类的方法来处理,子类的方法处理子类自己独有的属性

- 自定义构造方法必须以intiWith开头,并且’W’必须大写

<h3 id="4.13">4.13 自定义类工厂方法</h3>

##### 1.自定义工厂方法
- 什么是工厂方法(快速创建方法)
    + 类工厂方法是一种用于分配、初始化实例并返回一个它自己的实例的类方法。类工厂方法很方便，因为它们允许您只使用一个步骤（而不是两个步骤）就能创建对象. 例如new

- 自定义类工厂方法的规范
    + (1)一定是+号开头
    + (2)返回值一般是instancetype类型
    + (3)方法名称以类名开头,首字母小写

- 示例

```objc
+ (id)person;
+ (id)person
{
    return  [[Person alloc]init];
}

+ (id)personWithAge:(int)age;
+ (id)personWithAge:(int)age
{
    Person *p = [[self alloc] init];
    [p setAge:age];
    return p;
}
```

- apple中的类工厂方法

```objc
其实苹果在书写工厂方法时也是按照这样的规划书写
    [NSArray array];
    [NSArray arrayWithArray:<#(NSArray *)#>];
    [NSDictionary dictionary];
    [NSDictionary dictionaryWithObject:<#(id)#> forKey:<#(id<NSCopying>)#>];
    [NSSet set];
    [NSSet setWithObject:<#(id)#>];
```


##### 2.子父类中的类工厂方法
- 由于之类默认会继承父类所有的方法和属性, 所以类工厂方法也会被继承
- 由于父类的类工厂方法创建实例对象时是使用父类的类创建的, 所以如果子类调用父类的类工厂方法创建实例对象,创建出来的还是父类的实例对象
- 为了解决这个问题, 以后在自定义类工厂时候不要利用父类创建实例对象, 改为使用self创建, 因为self谁调用当前方法self就是谁

- 示例

```objc
@interface Person : NSObject
+ (id)person;
@end

@implementation Person
+ (id)person
{
    return  [[Person alloc]init];
}
@end

@interface Student : Person
@property NSString *name;
@end

@implementation Student

@end

int main(int argc, const char * argv[])
{
    Student *stu = [Student person];// [[Person alloc] init]
    [stu setName:@"lnj"]; // 报错, 因为Person中没有setName
}
```

- 正确写法

```objc
@interface Person : NSObject
+ (id)person;
@end

@implementation Person
+ (id)person
{
//   return  [[Person alloc]init];
//     谁调用这个方法,self就代表谁
//    注意:以后写类方法创建初始化对象,写self不要直接写类名
    return  [[self alloc]init];
}
@end

@interface Student : Person
@property NSString *name;
@end

@implementation Student
@end

int main(int argc, const char * argv[])
{
    Student *stu = [Student person];// [[Student alloc] init]
    [stu setName:@"lnj"];
}
```


<h3 id="4.14">4.14 类的本质</h3>

##### 1.类的本质
- 类的本质其实也是一个对象(类对象)
- 程序中第一次使用该类的时候被创建，在整个程序中只有一份。
- 此后每次使用都是这个类对象，它在程序运行时一直存在。
- 类对象是一种数据结构,存储类的基本信息:类大小,类名称,类的版本，继承层次，以及消息与函数的映射表等
- 类对象代表类,Class类型,对象方法属于类对象
- 如果消息的接收者是类名,则类名代表类对象
- 所有类的实例都由类对象生成,类对象会把实例的isa的值修改成自己的地址,每个实例的isa都指向该实例的类对象



##### 2.如何获取类对象
- 通过实例对象

```objc
格式：[实例对象   class ];
如：   [dog class];
```

- 通过类名获取(类名其实就是类对象)

```objc
格式：[类名 class];
如：[Dog class]
```



##### 3.类对象的用法
- 用来调用类方法

```objc
[Dog test];

Class c = [Dog class];
[c test];
```

- 用来创建实例对象

```objc
Dog *g = [Dog new];

Class c = [Dog class];
Dog *g1 = [c new];
```



##### 4.类对象的存储

![类和对象的存储.png](http://upload-images.jianshu.io/upload_images/328309-74433f5a94af33c3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 5.OC实例对象 类对象 元对象之间关系
- Objective-C是一门面向对象的编程语言。
    + 每一个对象 都是一个类的实例。
    + 每一个对象 都有一个名为isa的指针,指向该对象的类。
    + 每一个类􏰁述了一系列它的实例的特点,包括成员变量的列表,成员函数的列表等。
    + 每一个对象都可以接受消息,而对象能够接收的消息列表是保存在它所对应的类中。

- 在Xcode中按Shift + Command + O打开文件搜索框，然后输入NSObject.h和objc.h,可以打开 NSObject的定义头文件,通过头文件我们可以看到,NSObject就是一个包含isa指针的结构体,如下图所示:

```objc
NSObject.h
@interface NSObject <NSObject> {
    Class isa  OBJC_ISA_AVAILABILITY;
}
```

```objc
objc.h
/// An opaque type that represents an Objective-C class.
typedef struct objc_class *Class;

/// Represents an instance of a class.
struct objc_object {
    Class isa  OBJC_ISA_AVAILABILITY;
};
```

- 按照面向对象语言的设计原则,所有事物都应该是对象(严格来说 Objective-C并没有完全做到这一点,因为它有int,double这样的简单变量类型)
    + 在Objective-C语言中,每一个类实际上也是一个对象。每一个类也有一个名为isa的指针。每一个类都可以接受消息,例如[NSObject new],就是向NSObject这个类发送名为new的消息。
    + 在Xcode中按Shift + Command + O,然后输入runtime.h,可以打开Class的定义头文件,通过头文件我们可以看到,Class也是一个包含isa指针的结构体,如下图所示。(图中除了isa外还有其它成员变量,但那是为了兼容非2.0版的Objective-C的遗留逻辑,大家可以忽略它。)

```objc
runtime.h
struct objc_class {
    Class isa  OBJC_ISA_AVAILABILITY;

#if !__OBJC2__
    Class super_class                                        OBJC2_UNAVAILABLE;
    const char *name                                         OBJC2_UNAVAILABLE;
    long version                                             OBJC2_UNAVAILABLE;
    long info                                                OBJC2_UNAVAILABLE;
    long instance_size                                       OBJC2_UNAVAILABLE;
    struct objc_ivar_list *ivars                             OBJC2_UNAVAILABLE;
    struct objc_method_list **methodLists                    OBJC2_UNAVAILABLE;
    struct objc_cache *cache                                 OBJC2_UNAVAILABLE;
    struct objc_protocol_list *protocols                     OBJC2_UNAVAILABLE;
#endif

} OBJC2_UNAVAILABLE;
```

- 因为类也是一个对象,那它也必须是另一个类的实例,这个类就是元类 (metaclass)。
    + 元类保存了**类方法**的列表。当一个**类方法**被调用时,元类会首先查找它本身是否有该类方法的实现,如果没有则该元类会向它的父类查找该方法,直到一直找到继承链的头。
    + 元类(metaclass)也是一个对象,那么元类的isa指针又指向哪里呢?为了设计上的完整,所有的元类的isa指针都会指向一个根元类(root metaclass)。
    + 根元类(root metaclass)本身的isa指针指向自己,这样就行成了一个闭环。上面说􏰀到,一个对象能够接收的消息列表是保存在它所对应的类中的。在实际编程中,我们几乎不会遇到向元类发消息的情况,那它的isa 指针在实际上很少用到。不过这么设计保证了面向对象的干净,即所有事物都是对象,都有isa指针。
    + 由于**类方法**的定义是保存在元类(metaclass)中,而方法调用的规则是,如果该类没有一个方法的实现,则向它的父类继续查找。所以为了保证父类的类方法可以在子类中可以被调用,所以子类的元类会继承父类的元类,换而言之,类对象和元类对象有着同样的继承关系。

- 下面这张图或许能够 让大家对isa和继承的关系清楚一些

![实例对象类对象和元对象.png](http://upload-images.jianshu.io/upload_images/328309-6037b8bd3c19835b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 上图中,最让人困惑的莫过于Root Class了。在实现中,Root Class是指
NSObject,我们可以从图中看出:
- NSObject类对象包括它的对象实例方法。
- NSObject的元对象包括它的类方法,例如new方法。
- NSObject的元对象继承自NSObject类。
- 一个NSObject的类中的方法同时也会被NSObject的子类在查找方法时找到。

<h3 id="4.15">4.15 类的启动过程</h3>

##### 1.+load方法
- 在程序启动的时候会加载所有的类和分类，并调用所有类和分类的+load方法(只会调用一次)
- 先加载父类，再加载子类；也就是先调用父类的+load，再调用子类的+load
- 先加载元原始类，再加载分类
- 不管程序运行过程有没有用到这个类，都会调用+load加载

```objc
@implementation Person

+ (void)load
{
    NSLog(@"%s", __func__);
}
@end

@implementation Student : Person

+ (void)load
{
    NSLog(@"%s", __func__);
}
@end

输出结果:
+[Person load]
+[Student load]
```



##### 2.+initialize
- 在第一次使用某个类时（比如创建对象等），只会调用一次+initialize方法
- 一个类只会调用一次+initialize方法，先调用父类的，再调用子类的

```objc
@implementation Person
+ (void)initialize
{
    NSLog(@"%s", __func__);
}
@end

@implementation Student : Person
+ (void)initialize
{
    NSLog(@"%s", __func__);
}
@end
int main(int argc, const char * argv[]) {
    Student *stu = [Student new];
    return 0;
}
输出结果:
+[Person initialize]
+[Student initialize]
```

<h3 id="4.16">4.16 SEL类型</h3>

##### 1.什么是SEL类型
- SEL类型代表着方法的签名，在类对象的方法列表中存储着该签名与方法代码的对应关系

- 每个类的方法列表都存储在类对象中
- 每个方法都有一个与之对应的SEL类型的对象
- 根据一个SEL对象就可以找到方法的地址，进而调用方法
- SEL类型的定义
    + typedef struct objc_selector 	*SEL;

- 首先把test这个方法名包装成sel类型的数据
- 根据SEL数据到该类的类对象中，去找对应的方法的代码，如果找到了就执行该代码
- 如果没有找到根据类对象上的父类的类对象指针，去父类的类对象中查找，如果找到了，则执行父类的代码
- 如果没有找到，一直像上找，直到基类(NSObject)
- 如果都没有找到就报错。

- **注意**：
    + 在这个操作过程中有缓存,第一次找的时候是一个一个的找，非常耗性能，之后再用到的时候就直接使用。


```objc
Dog *dog=[[Dog alloc] init];
[dog eat];
```

![sel.png](http://upload-images.jianshu.io/upload_images/328309-16d8aecf8168d87c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##### 2.SEL使用
- 定义普通的变量
    + 如：SEL sel = @selector(show);

- 作为方法实参与NSObject配合使用
- 检验对象是否实现了某个方法
    + \- (BOOL) respondsToSelector: (SEL)selector 判断实例是否实现这样方法
    + \+ (BOOL)instancesRespondToSelector:(SEL)aSelector;

```objc
    BOOL flag;
    // [类 respondsToSelector]用于判断是否包含某个类方法
    flag = [Person respondsToSelector:@selector(objectFun)]; //NO
    flag = [Person respondsToSelector:@selector(classFun)]; //YES

    Person *obj = [[Person alloc] init];

    // [对象 respondsToSelector]用于判断是否包含某个对象方法
    flag = [obj respondsToSelector:@selector(objectFun)]; //YES
    flag = [obj respondsToSelector:@selector(classFun)]; //NO

    // [类名 instancesRespondToSelector]用于判断是否包含某个对象方法
    // instancesRespondToSelectorr只能写在类名后面, 等价于 [对象 respondsToSelector]
    flag = [Person instancesRespondToSelector:@selector(objectFun)]; //YES
    flag = [Person instancesRespondToSelector:@selector(classFun)]; //NO
```

- 让对象执行某个方法
    + \- (id)performSelector:(SEL)aSelector;
    + \- (id)performSelector:(SEL)aSelector withObject:(id)object;
    + \- (id)performSelector:(SEL)aSelector withObject:(id)object1 withObject:(id)object2;

```objc
    Person *p = [Person new];
    SEL s1 = @selector(objectFun);
    [p performSelector:s1];

    SEL s2 = @selector(objectFun:);
    [p performSelector:s2 withObject:@"lnj"];

    SEL s3 = @selector(objectFun:value2:);
    [p performSelector:s3 withObject:@"lnj" withObject:@"lmj"];

    SEL s4 = @selector(classFun);
    [Person performSelector:s4];

    SEL s5 = @selector(classFun:);
    [Person performSelector:s5 withObject:@"lnj"];

    SEL s6 = @selector(classFun:value2:);
    [Person performSelector:s6 withObject:@"lnj" withObject:@"lmj"];
```

- 作为方法形参

```objc
@implementation Person

- (void)makeObject:(id) obj performSelector:(SEL) selector
{
    [obj performSelector:selector];
}
@end

int main(int argc, const char * argv[]) {

    Person *p = [Person new];
    SEL s1 = @selector(eat);
    Dog *d = [Dog new];
    [p makeObject:d performSelector:s1];

    return 0;
}
```


##### 3.OC方法查找顺序

![OC方法查找顺序.png](http://upload-images.jianshu.io/upload_images/328309-ca740cb4275d7a97.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 1.给实例对象发送消息的过程(调用对象方法)
    + 根据对象的isA指针去该对象的类方法中查找，如果找到了就执行
    + 如果没有找到，就去该类的父类类对象中查找
    + 如果没有找到就一直往上找，直到跟类（NSObject）
    + 如果都没有找到就报错

- 2.给类对象发送消息(调用类方法)
    + 根据类对象的isA指针去元对象中查找，如果找到了就执行
    + 如果没有找到就去父元对象中查找
    + 如果如果没有找到就一直往上查找，直到根类（NSOject）
    + 如果都没有找到就报错


<h2 id="5">5. 内存管理</h2>

##### 1.内存管理的重要性
- 移动设备的内存极其有限，每个app所能占用的内存是有限制的

- 下列行为都会增加一个app的内存占用
    + 创建一个OC对象
    + 定义一个变量
    + 调用一个函数或者方法

- 当app所占用的内存较多时，系统会发出内存警告，这时得回收一些不需要再使用的内存空间。比如回收一些不需要使用的对象、变量等

- 如果app占用内存过大, 系统可能会强制关闭app, 造成闪退现象, 影响用户体验



##### 2.什么是内存管理
- 如何回收那些不需要再使用的对象?
    + 那就得学会OC的内存管理

- 所谓内存管理, 就是对内存进行管理, 涉及的操作有:
    + 分配内存 : 比如创建一个对象, 会增加内存占用
    + 清除内存 : 比如销毁一个对象, 能减小内存占用

- 内存管理的管理范围
    + 任何继承了NSObject的对象
    + 对其他非对象类型无效(int、char、float、double、struct、enum等 )

- 只有OC对象才需要进行内存管理的本质原因
    + OC对象存放于堆里面
    + 非OC对象一般放在栈里面(栈内存会被系统自动回收)



##### 3.堆和栈
- 栈（操作系统）：由操作系统自动分配释放，存放函数的参数值，局部变量的值等。其操作方式类似于数据结构中的栈(先进后出)；

- 堆（操作系统）：一般由程序员分配释放，若程序员不释放，程序结束时可能由OS回收，分配方式类似于链表。

- 示例:

```objc
int main(int argc, const char * argv[])
{
    @autoreleasepool {
        int a = 10; // 栈
        int b = 20; // 栈
        // p : 栈
        // Person对象(计数器==1) : 堆
        Person *p = [[Person alloc] init];
    }
    // 经过上一行代码后, 栈里面的变量a\b\c都会被回收
    // 但是堆里面的Person对象还会留在内存中,因为它是计数器依然是1
    return 0;
}
```

![堆和栈.png](http://upload-images.jianshu.io/upload_images/328309-a6ad48e12323ad35.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


[更多关于堆栈信息](http://baike.baidu.com/link?url=VJz-vKfY_ASVHCB17nWR_uQ4Adhuasl2WOrW4O7ZgFdgq5Tl_kBGfUYzbNSzkSBkHAbAH8qzfDpl5Wm4rxQ1Ka)


<h3 id="5.1">5.1 引用计数器</h3>

##### 1.什么是引用计数器
- 系统是如何判断什么时候需要回收一个对象所占用的内存?
    + 根据对象的引用计数器

- 什么是引用计数器
    + 每个OC对象都有自己的引用计数器
    + 它是一个整数
    + 从字面上, 可以理解为”对象被引用的次数”
    + 也可以理解为: 它表示有多少人正在用这个对象


![引用计数器.png](http://upload-images.jianshu.io/upload_images/328309-2ef3a3bf74a94555.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 2.引用计数器的作用
- 简单来说, 可以理解为:
    + 引用计数器表示有多少人正在使用这个对象

- 当没有任何人使用这个对象时, 系统才会回收这个对象, 也就是说
    + 当对象的引用计数器为0时,对象占用的内存就会被系统回收
    + 如果对象的计数器不为0，那么在整个程序运行过程，它占用的内存就不可能被回收(除非整个程序已经退出 )

- 任何一个对象, 刚生下来的时候, 引用计数器都为1
    + 当使用alloc、new或者copy创建一个对象时，对象的引用计数器默认就是1



##### 3.引用计数器的操作
- 要想管理对象占用的内存, 就得学会操作对象的引用计数器

- 引用计数器的常见操作
    + 给对象发送一条retain消息,可以使引用计数器值+1（retain方法返回对象本身）
    + 给对象发送一条release消息, 可以使引用计数器值-1
    + 给对象发送retainCount消息, 可以获得当前的引用计数器值

- 需要注意的是: release并不代表销毁\回收对象, 仅仅是计数器-1

<h3 id="5.2">5.2 dealloc方法</h3>

##### 1.dealloc方法基本概念
- 当一个对象的引用计数器值为0时,这个对象即将被销毁，其占用的内存被系统回收
- 对象即将被销毁时系统会自动给对象发送一条dealloc消息
(因此, 从dealloc方法有没有被调用,就可以判断出对象是否被销毁)

- dealloc方法的重写
    + 一般会重写dealloc方法,在这里释放相关资源,dealloc就是对象的遗言
    + **一旦重写了dealloc方法, 就必须调用[super dealloc],并且放在最后面调用（非ARC）**

- 使用注意
    + 不能直接调用dealloc方法
    + 一旦对象被回收了, 它占用的内存就不再可用,坚持使用会导致程序崩溃（野指针错误）


<h3 id="5.3">5.3 野指针\空指针</h3>

##### 1.僵尸对象
- 已经被销毁的对象(不能再使用的对象)

##### 2.野指针
- 指向僵尸对象(不可用内存)的指针
- 给野指针发消息会报EXC_BAD_ACCESS错误

##### 3.空指针
- 没有指向存储空间的指针(里面存的是nil, 也就是0)
- 给空指针发消息是没有任何反应的

- 为了避免野指针错误的常见办法
    + 在对象被销毁之后, 将指向对象的指针变为空指针


<h3 id="5.4">5.4 Xcode设置</h3>

##### 1.如何关闭ARC功能
- 要想手动调用retain、release等方法 , 就必须关闭ARC功能
![关闭arc.png](http://upload-images.jianshu.io/upload_images/328309-1121a56708b0377e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 2.如何开启僵尸对象监控
- 默认情况下，Xcode是不会管僵尸对象的，使用一块被释放的内存也不会报错。为了方便调试，应该开启僵尸对象监控
![僵尸对象.png](http://upload-images.jianshu.io/upload_images/328309-12ee4a17fafc753a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![僵尸对象1.png](http://upload-images.jianshu.io/upload_images/328309-8075807b3bb640b9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


<h3 id="5.5">5.5 内存管理原则</h3>

##### 1.内存管理原则
- 苹果官方规定的内存管理原则
    + 谁创建谁release :
        * 如果你通过alloc、new、copy或mutableCopy来创建一个对象，那么你必须调用release或autorelease

    + 谁retain谁release:
        * 只要你调用了retain，就必须调用一次release

- 总结一下就是
    + 有加就有减
    + 曾经让对象的计数器+1，就必须在最后让对象计数器-1



##### 2.多对象内存管理
- 单个对象的内存管理, 看起来非常简单

- 如果对多个对象进行内存管理, 并且对象之间是有联系的, 那么管理就会变得比较复杂

- 其实, 多个对象的管理思路 跟很多游戏的房间管理差不多
    + 比如斗地主 \ 劲舞团 \ QQ音速


- 总的来说, 有这么几点管理规律
    + 只要还有人在用某个对象，那么这个对象就不会被回收
    + 只要你想用这个对象，就让对象的计数器+1
    + 当你不再使用这个对象时，就让对象的计数器-1




##### 3.set方法内存管理
- (1)retain需要使用的对象
- (2)release之前的对象
- (3)只有传入的对象和之前的不同才需要release和retain

```objc
- (void)setRoom:(Room *)room
{
    // 避免过度释放
    if (room != _room)
    {
        // 对当前正在使用的房间（旧房间）做一次release
        [_room release];

        // 对新房间做一次retain操作
         _room = [room retain];
    }
}

```

##### 4.dealloc方法的内存管理

```objc
- (void)dealloc
{
    // 当人不在了，代表不用房间了
    // 对房间做一次release操作
    [_room release];
    [super dealloc];
}

```

<h3 id="5.6">5.6 @property参数</h3>

##### 1.控制set方法的内存管理
- retain ： release旧值，retain新值（用于OC对象）
- assign ： 直接赋值，不做任何内存管理(默认，用于非OC对象类型)
- copy   ： release旧值，copy新值（一般用于NSString *）

##### 2.控制需不需要生成set方法
- readwrite ：同时生成set方法和get方法（默认）
- readonly  ：只会生成get方法

##### 3.多线程管理
- atomic    ：性能低（默认）
- nonatomic ：性能高

##### 4.控制set方法和get方法的名称
- setter ： 设置set方法的名称，一定有个冒号:
- getter ： 设置get方法的名称


- 注意: 不同类型的参数可以组合在一起使用

<h3 id="5.7">5.7 @class</h3>

##### 1.@class基本概念
- 作用
    + 可以简单地引用一个类

- 简单使用
    + @class Dog;
    + 仅仅是告诉编译器:Dog是一个类;并不会包含Dog这个类的所有内容

- 具体使用
    + 在.h文件中使用@class引用一个类
    + 在.m文件中使用#import包含这个类的.h文件

---

##### #2.@class其它应用场景
- 对于循环依赖关系来说，比方A类引用B类，同时B类也引用A类
- 这种嵌套包含的代码编译会报错

```objc
#import "B.h"
@interface A : NSObject
{
    B *_b;
}
@end

#import “A.h"
@interface B : NSObject
{
    A *_a;
}
@end

```

- 当使用@class在两个类相互声明，就不会出现编译报错

```objc
@class B;
@interface A : NSObject
{
    B *_b;
}
@end

@class A;
@interface B : NSObject
{
    A *_a;
}
@end
```



##### 3.@class和#import
- 作用上的区别
    + \#import会包含引用类的所有信息(内容),包括引用类的变量和方法
    + @class仅仅是告诉编译器有这么一个类, 具体这个类里有什么信息, 完全不知

- 效率上的区别
    + 如果有上百个头文件都#import了同一个文件，或者这些文件依次被#import,那么一旦最开始的头文件稍有改动，后面引用到这个文件的所有类都需要重新编译一遍 , 编译效率非常低
    + 相对来讲，使用@class方式就不会出现这种问题了

<h3 id="5.8">5.8 循环retain</h3>

##### 1.循环retian基本概念

- 循环retain的场景
	+ 比如A对象retain了B对象，B对象retain了A对象
	
- 循环retain的弊端
	+ 这样会导致A对象和B对象永远无法释放

- 循环retain的解决方案
	+ 当两端互相引用时，应该一端用retain、一端用assign
	

<h3 id="5.9">5.9 autorelease基本使用</h3>

##### 1.autorelease基本概念
- autorelease是一种支持引用计数的内存管理方式,只要给对象发送一条autorelease消息,会将对象放到一个自动释放池中,当自动释放池被销毁时，会对池子里面的**所有对象做一次release操作**
    + *注意,这里只是发送release消息,如果当时的引用计数(reference-counted)依然不为0,则该对象依然不会被释放。*

- autorelease方法会返回对象本身

```objc
Person *p = [Person new];
p = [p autorelease];
```

- 调用完autorelease方法后，对象的计数器不变

```objc
Person *p = [Person new];
p = [p autorelease];
NSLog(@"count = %lu", [p retainCount]); // 1
```

- autorelease的好处
    + 不用再关心对象释放的时间
    + 不用再关心什么时候调用release

- autorelease的原理
    + autorelease实际上只是把对release的调用延迟了,对于每一个autorelease,系统只是把该 Object放入了当前的autorelease pool中,当该pool被释放时,该pool中的所有Object会被调用Release。



##### 2.自动释放池
- 创建自动释放池格式:
- iOS 5.0前

```objc
NSAutoreleasePool *pool = [[NSAutoreleasePool alloc] init]; // 创建自动释放池
[pool release]; // [pool drain]; 销毁自动释放池
```
- iOS 5.0 开始

```objc
@autoreleasepool
{ //开始代表创建自动释放池

} //结束代表销毁自动释放池
```
- 在iOS程序运行过程中，会创建无数个池子。这些池子都是以栈结构存在（先进后出）

- 当一个对象调用autorelease方法时，会将这个对象放到栈顶的释放池



##### 3.autorelease基本使用

```objc
NSAutoreleasePool *autoreleasePool = [[NSAutoreleasePool alloc] init];

Person *p = [[[Person alloc] init] autorelease];

[autoreleasePool drain];
```

```objc
@autoreleasepool
{ // 创建一个自动释放池
        Person *p = [[Person new] autorelease];
} // 销毁自动释放池(会给池子中所有对象发送一条release消息)
```

<h3 id="5.10">5.10 autorelease注意事项</h3>

##### 1.autorelease使用注意
- 并不是放到自动释放池代码中,都会自动加入到自动释放池

```objc
 @autoreleasepool {
    // 因为没有调用 autorelease 方法,所以对象没有加入到自动释放池
    Person *p = [[Person alloc] init];
    [p run];
}
```

- 在自动释放池的外部发送autorelease 不会被加入到自动释放池中
    + autorelease是一个方法,只有在自动释 放池中调用才有效。

```objc
 @autoreleasepool {
 }
 // 没有与之对应的自动释放池, 只有在自动释放池中调用autorelease才会放到释放池
 Person *p = [[[Person alloc] init] autorelease];
 [p run];

 // 正确写法
  @autoreleasepool {
    Person *p = [[[Person alloc] init] autorelease];
 }

 // 正确写法
 Person *p = [[Person alloc] init];
  @autoreleasepool {
    [p autorelease];
 }

```

- 自动释放池的嵌套使用
    + 自动释放池是以栈的形式存在
    + 由于栈只有一个入口, 所以调用autorelease会将对象放到栈顶的自动释放池
    + *栈顶就是离调用autorelease方法最近的自动释放池*
```objc
@autoreleasepool { // 栈底自动释放池
        @autoreleasepool {
            @autoreleasepool { // 栈顶自动释放池
                Person *p = [[[Person alloc] init] autorelease];
            }
            Person *p = [[[Person alloc] init] autorelease];
        }
    }
```

- 自动释放池中不适宜放占用内存比较大的对象
    + 尽量避免对大内存使用该方法,对于这种延迟释放机制,还是尽量少用
    + 不要把大量循环操作放到同一个 @autoreleasepool 之间,这样会造成内存峰值的上升

```objc
// 内存暴涨
    @autoreleasepool {
        for (int i = 0; i < 99999; ++i) {
            Person *p = [[[Person alloc] init] autorelease];
        }
    }
```

```objc
// 内存不会暴涨
 for (int i = 0; i < 99999; ++i) {
        @autoreleasepool {
            Person *p = [[[Person alloc] init] autorelease];
        }
    }
```


##### 2.autorelease错误用法
- 不要连续调用autorelease

```objc
 @autoreleasepool {
 // 错误写法, 过度释放
    Person *p = [[[[Person alloc] init] autorelease] autorelease];
 }
```
- 调用autorelease后又调用release

```objc
 @autoreleasepool {
    Person *p = [[[Person alloc] init] autorelease];
    [p release]; // 错误写法, 过度释放
 }
```

<h3 id="5.11">5.11 ARC基本概念</h3>

##### 1.什么是ARC
- Automatic Reference Counting,自动引用计数,即ARC,可以说是WWDC2011和iOS5所引入 的最大的变革和最激动人心的变化。ARC是新的LLVM 3.0编译器的一项特性,使用ARC,可以说一 举解决了广大iOS开发者所憎恨的手动内存管理的麻烦。
    + *手动管理内存, 可以简称MRC (Manual Reference Counting)*

- 在工程中使用ARC非常简单:只需要像往常那样编写代码,只不过永远不写**retain,release和autorelease**三个关键字就好~这是ARC的基本原则。

- 当ARC开启时,编译器将自动在代码合适的地方插入retain, release和autorelease,而作为程序猿,完全不需要担心编译器会做错(除非开发者自己错用ARC了)。



##### 2.ARC的注意点和优点
- ARC的注意点
    + ARC是编译器特性，而不是运行时特性
    + ARC不是其它语言中的垃圾回收, 有着本质区别

- ARC的优点
    + 完全消除了手动管理内存的烦琐, 让程序猿更加专注于app的业务
    + 基本上能够避免内存泄露
    + 有时还能更加快速，因为编译器还可以执行某些优化



##### 3.ARC的判断原则
- ARC的判断原则
    + 只要还有一个强指针变量指向对象，对象就会保持在内存中

- 强指针
    + 默认所有指针变量都是强指针
    + 被__strong修饰的指针

```objc
 Person *p1 = [[Person alloc] init];
 __strong  Person *p2 = [[Person alloc] init];
```

- 弱指针
    + 被__weak修饰的指针

```objc
__weak  Person *p = [[Person alloc] init];
```

- **注意:当使用ARC的时候,暂时忘记“引用计数器”,因为判断标准变了。**


<h3 id="5.12">5.12 ARC快速入门</h3>

##### 1.ARC机制判断
- OS5以后,创建项目默认的都是ARC

![ARC.png](http://upload-images.jianshu.io/upload_images/328309-4ab0d3c4c8e8352c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- ARC机制下有几个明显的标志:
    +  不允许调用对象的 release方法
    +  不允许调用 autorelease方法
    +   再重写父类的dealloc方法时,不能再调用 [super dealloc];



##### 2.ARC快速使用

```objc
int main(int argc, const char * argv[]) {
    // 不用写release, main函数执行完毕后p会被自动释放
    Person *p = [[Person alloc] init];
    return 0;
}
```

<h3 id="5.13">5.13 ARC下的内存管理</h3>

##### 1.ARC下单对象内存管理

- 局部变量释放对象随之被释放

```objc
int main(int argc, const char * argv[]) {
   @autoreleasepool {
        Person *p = [[Person alloc] init];
    } // 执行到这一行局部变量p释放
    // 由于没有强指针指向对象, 所以对象也释放
    return 0;
}
```
- 清空指针对象随之被释放

```objc
int main(int argc, const char * argv[]) {
   @autoreleasepool {
        Person *p = [[Person alloc] init];
        p = nil; // 执行到这一行, 由于没有强指针指向对象, 所以对象被释放
    }
    return 0;
}
```
- 默认清空所有指针都是强指针

```objc
int main(int argc, const char * argv[]) {
   @autoreleasepool {
        // p1和p2都是强指针
        Person *p1 = [[Person alloc] init];
        __strong Person *p2 = [[Person alloc] init];
    }
    return 0;
}
```
- 弱指针需要明确说明
    + 注意: 千万不要使用弱指针保存新创建的对象

```objc
int main(int argc, const char * argv[]) {
   @autoreleasepool {
        // p是弱指针, 对象会被立即释放
        __weak Person *p1 = [[Person alloc] init];
    }
    return 0;
}
```


##### 2.ARC下多对象内存管理
- ARC和MRC一样, 想拥有某个对象必须用强指针保存对象, 但是不需要在dealloc方法中release

```objc
@interface Person : NSObject

// MRC写法
//@property (nonatomic, retain) Dog *dog;

// ARC写法
@property (nonatomic, strong) Dog *dog;

@end

```


##### 3.ARC下循环引用问题
- ARC和MRC一样, 如果A拥有B, B也拥有A, 那么必须一方使用弱指针

```objc
@interface Person : NSObject

//@property (nonatomic, retain) Dog *dog;
@property (nonatomic, strong) Dog *dog;

@end

@interface Dog : NSObject

// 错误写法, 循环引用会导致内存泄露
//@property (nonatomic, strong) Person *owner;

// 正确写法, 当如果保存对象建议使用weak
//@property (nonatomic, assign) Person *owner;
@property (nonatomic, weak) Person *owner;
@end
```


##### 4.ARC下@property参数
- strong : 用于OC对象, 相当于MRC中的retain
- weak : 用于OC对象, 相当于MRC中的assign
- assign : 用于基本数据类型, 跟MRC中的assign一样

<h3 id="5.14">5.14 ARC和MRC兼容和转换</h3>

##### 1.ARC模式下如何兼容非ARC的类
- 转变为非ARC -fno-objc-arc
- 转变为ARC的, -f-objc-arc (不常用)

![ARC兼容非ARC.png](http://upload-images.jianshu.io/upload_images/328309-457e28b9d56c1d6d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 2.如何将MRC转换为ARC

![MRC转ARC.png](http://upload-images.jianshu.io/upload_images/328309-244839ea19432656.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<h2 id="6">6. Category、Extension、Block和Protocol</h2>

<h3 id="6.1">6.1 Category基本概念</h3>

##### 1.什么是Category
- Category有很多种翻译: 分类 \ 类别 \ 类目 (一般叫分类)

- Category是OC特有的语法, 其他语言没有的语法

- Category的作用
    + 可以在不修改原来类的基础上, 为这个类扩充一些方法
    + 一个庞大的类可以分模块开发
    + 一个庞大的类可以由多个人来编写,更有利于团队合作



##### 2.Category的格式
- 在.h文件中声明类别
    + 1)新添加的方法必须写在 @interface 与 @end之间
    + 2)ClassName 现有类的类名(要为哪个类扩展方法)            + 3)CategoryName 待声明的类别名称
    + 4)NewMethod 新添加的方法
```objc
@interface ClassName (CategoryName)
NewMethod; //在类别中添加方法
//不允许在类别中添加变量
@end
```
    + **注意: 1)不允许在声明类别的时候定义变量**

- 在.m文件中实现类别:
    + 1)新方法的实现必须写在@ implementation与@end之间
    + 2)ClassName 现有类的类名
    + 3)CategoryName 待声明的类别名称
    + 4)NewMethod 新添加的方法的实现

```objc
@implementation ClassName(CategoryName)

NewMethod
... ...
@end
```

- 使用Xcode创建分类

![创建分类.png](http://upload-images.jianshu.io/upload_images/328309-d641d39c2e6d06a2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![分类模板.png](http://upload-images.jianshu.io/upload_images/328309-17ec43c94d56ed26.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<h3 id="6.2">6.2 Category注意事项</h3>

##### 1.分类的使用注意事项
- **分类只能增加方法, 不能增加成员变量**

```objc
@interface Person (NJ)
{
//    错误写法
//    int _age;
}
- (void)eat;
@end
```

- 分类中写property只会生成方法声明

```objc
@interface Person (NJ)
// 只会生成getter/setter方法的声明, 不会生成实现和私有成员变量
@property (nonatomic, assign) int age;
@end
```

- 分类可以访问原来类中的成员变量

```objc
@interface Person : NSObject
{
    int _no;
}
@end

@implementation Person (NJ)
- (void)say
{
    NSLog(@"%s", __func__);
    // 可以访问原有类中得成员变量
    NSLog(@"no = %i", _no);
}
@end

```

- 如果分类和原来类出现同名的方法, 优先调用分类中的方法, 原来类中的方法会被忽略

```objc
@implementation Person

- (void)sleep
{
    NSLog(@"%s", __func__);
}
@end

@implementation Person (NJ)
- (void)sleep
{
    NSLog(@"%s", __func__);
}
@end

int main(int argc, const char * argv[]) {
    Person *p = [[Person alloc] init];
    [p sleep];
    return 0;
}

输出结果:
-[Person(NJ) sleep]

```


##### 2.分类的编译的顺序
- 多个分类中有同名方法,则执行最后编译的文件方法(注意开发中千万不要这么干)

```objc
@implementation Person

- (void)sleep
{
    NSLog(@"%s", __func__);
}
@end

@implementation Person (NJ)
- (void)sleep
{
    NSLog(@"%s", __func__);
}
@end

@implementation Person (MJ)
- (void)sleep
{
    NSLog(@"%s", __func__);
}
@end

int main(int argc, const char * argv[]) {
    Person *p = [[Person alloc] init];
    [p sleep];
    return 0;
}

输出结果:
-[Person(MJ) sleep]
```

![category注意事项.png](http://upload-images.jianshu.io/upload_images/328309-8a7e270e84621b21.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


- 方法调用的优先级(从高到低)
    + 分类(最后参与编译的分类优先)
    + 原来类
    + 父类

<h3 id="6.3">6.3 类扩展(Class Extension)</h3>

##### 1.什么是类扩展
- 延展类别又称为扩展(Extendsion),Extension是Category的一个特例

- 可以为某个类**扩充一些私有的成员变量和方法**
    + 写在.m文件中
    + 英文名是Class Extension



##### 2.类扩展书写格式

```objc
@interface 类名 ()
@end

```

- *对比分类, 就少了一个分类名称,因此也有人称它为”匿名分类”*

<h3 id="6.4">6.4 Block基本概念</h3>

##### 1.什么是Block
- Block是iOS中一种比较特殊的数据类型

- Block是苹果官方特别推荐使用的数据类型, 应用场景比较广泛
    + 动画
    + 多线程
    + 集合遍历
    + 网络请求回调

- Block的作用
    + 用来保存某一段代码, 可以在恰当的时间再取出来调用
    + 功能类似于函数和方法



##### 2.block的格式
- Block的定义格式

```objc
返回值类型 (^block变量名)(形参列表) = ^(形参列表) {

};
```

![block格式.png](http://upload-images.jianshu.io/upload_images/328309-3c32f78196878331.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- block最简单形式

```objc
void (^block名)() = ^{代码块;}

例如:
void (^myBlock)() = ^{ NSLog(@"李南江"); };
```
- block带有参数的block的定义和使用

```objc
void (^block名称)(参数列表)
= ^ (参数列表) { // 代码实现; }

例如:
void (^myBlock)(int) = ^(int num){ NSLog(@"num = %i", num); };
```
- 带有参数和返回值的block

```objc
返回类型 (^block名称)(参数列表)
= ^ (参数列表) { // 代码实现; }

例如:
int (^myBlock)(int, int) = ^(int num1, int num2){ return num1 + num2; };
```

- 调用Block保存的代码

```objc
block变量名(实参);
```

<h3 id="6.5">6.5 typedef和Block</h3>

##### 1.函数指针回顾
- 函数指针使用

```objc
int sum(int value1, int value2)
{
    return value1 + value2;
}

int minus(int value1, int value2)
{
    return value1 - value2;
}

int main(int argc, const char * argv[]) {
    int (*sumP) (int, int) = sum;
    int res = sumP(10, 20);
    NSLog(@"res = %i", res);

    int (*minusP) (int , int) = minus;
    res = minusP(10, 20);
    NSLog(@"res = %i", res);
    return 0;
}
```

- 函数指针别名

```objc
typedef int (*calculate) (int, int);
int main(int argc, const char * argv[]) {
    calculate sumP = sum;
    int res = sumP(10, 20);
    NSLog(@"res = %i", res);
    calculate minusP = minus;
    res = minusP(10, 20);
    NSLog(@"res = %i", res);
    return 0;
}
```


##### 2.block和typedef

- block使用
```objc
int main(int argc, const char * argv[]) {
    int (^sumBlock) (int, int) = ^(int value1, int value2){
        return value1 + value2;
    };
    int res = sumBlock(10 , 20);
    NSLog(@"res = %i", res);

    int (^minusBlock) (int, int) = ^(int value1, int value2){
        return value1 - value2;
    };
    res = minusBlock(10 , 20);
    NSLog(@"res = %i", res);
    return 0;
}
```

- block别名

```objc
int main(int argc, const char * argv[]) {
    calculateBlock sumBlock = ^(int value1, int value2){
        return value1 + value2;
    };
    int res = sumBlock(10, 20);
    NSLog(@"res = %i", res);
    calculateBlock minusBlock = ^(int value1, int value2){
        return value1 - value2;
    };
    res = minusBlock(10, 20);
    NSLog(@"res = %i", res);

    return 0;
}
```

<h3 id="6.6">6.6 Block注意事项</h3>

##### 1.Block注意事项
- 在block内部可以访问block外部的变量

```objc
int  a = 10;
void (^myBlock)() = ^{
    NSLog(@"a = %i", a);
    }
myBlock();
输出结果: 10
```

- block内部也可以定义和block外部的同名的变量(局部变量),此时局部变量会暂时屏蔽外部

```objc
int  a = 10;
void (^myBlock)() = ^{
    int a = 50;
    NSLog(@"a = %i", a);
    }
myBlock();
输出结果: 50
```

- 默认情况下, Block内部不能修改外面的局部变量

```objc
int b = 5;
void (^myBlock)() = ^{
    b = 20; // 报错
    NSLog(@"b = %i", b);
    };
myBlock();

```

- Block内部可以修改使用__block修饰的局部变量

```objc
 __block int b = 5;
void (^myBlock)() = ^{
    b = 20;
    NSLog(@"b = %i", b);
    };
myBlock();
输出结果: 20
```


<h3 id="6.7">6.7 Protocol基本概念</h3>

##### 1.protocol 基本概念
- Protocol翻译过来, 叫做”协议”
    + 在写java的时候都会有接口interface这个概念,接口就是一堆方法的声明没有实现,而在OC里面Interface是一个类的头文件的声明,并不是真正意义上的接口的意思,在OC中接口是由一个叫做协议的protocol来实现的
    + protocol它可以声明一些必须实现的方法和选择实现 的方法。这个和java是完全不同的

- Protocol的作用
    + 用来声明一些方法
    + 也就说, 一个Protocol是由一系列的方法声明组成的

---

##### 2.protocol 语法格式
- Protocol的定义

```objc
@protocol 协议名称
// 方法声明列表
@end
```

- 类遵守协议
    + 一个类可以遵守1个或多个协议
    + 任何类只要遵守了Protocol,就相当于拥有了Protocol的所有方法声明


```objc
@interface 类名 : 父类 <协议名称1, 协议名称2,…>
@end
```

- 示例

```objc
@protocol SportProtocol <NSObject>
- (void)playFootball;
- (void)playBasketball;
@end

#import "SportProtocol.h" // 导入协议
@interface Studnet : NSObject<SportProtocol> // 遵守协议
@end

@implementation Student
// 实现协议方法
- (void)playBasketball
{
    NSLog(@"%s", __func__);
}
// 实现协议方法
- (void)playFootball
{
    NSLog(@"%s", __func__);
}
@end
```


##### 3.protocol和继承区别
- 继承之后默认就有实现, 而protocol只有声明没有实现
- 相同类型的类可以使用继承, 但是不同类型的类只能使用protocol
- protocol可以用于存储方法的声明, 可以将多个类中共同的方法抽取出来, 以后让这些类遵守协议即可


<h3 id="6.8">6.8 Protocol注意事项</h3>

##### 1.protocol 的使用注意
- 1)Protocol:就一个用途,用来声明一大堆的方法(不能声明成员变量),不能写实现。

```objc
@protocol SportProtocol <NSObject>
{
    int _age; // 错误写法
}
- (void)playFootball;
- (void)playBasketball;
@end
```
- 2)只要父类遵守了某个协议,那么子类也遵守。

```objc
@protocol SportProtocol <NSObject>

- (void)playFootball;
- (void)playBasketball;
@end
```

```objc
#import "SportProtocol.h"
@interface Student : NSObject <SportProtocol>
@end

@interface GoodStudent : Student
@end

@implementation GoodStudent
- (void)playFootball
{
    NSLog(@"%s", __func__);
}
- (void)playBasketball
{
    NSLog(@"%s", __func__);
}
@end
```
- 3)OC不能继承多个类(单继承)但是能够遵守多个协议。继承(:),遵守协议(< >)

```objc
#import "SportProtocol.h"
#import "StudyProtocol.h"

@interface Student : NSObject <SportProtocol, StudyProtocol>

@end
```
- 4)协议可以遵守协议,一个协议遵守了另一个协议,就可以拥有另一份协议中的方法声明

```objc
@protocol A
-(void)methodA;
@end

@protocol B <A>
-(void)methodB;
@end
```

```objc

@interface Student : NSObject <B>
-(void)methodA; // 同时拥有A/B协议中的方法声明
-(void)methodB;

@end
```


##### 2.基协议
- NSObject是一个基类，最根本最基本的类，任何其他类最终都要继承它

- 还有名字也叫NSObject的协议，它是一个基协议，最根本最基本的协议

- NSObject协议中声明很多最基本的方法
    + description
    + retain
    + release

- 建议每个新的协议都要遵守NSObject协议

```objc
@protocol SportProtocol <NSObject> // 基协议

- (void)playFootball;
- (void)playBasketball;
@end
```



##### 3.@required和@optional关键字
- 协议中有2个关键字可以控制方法是否要实现(默认是@required，在大多数情况下，用途在于程序员之间的交流)
    + @required：这个方法必须要实现（若不实现，编译器会发出警告）
    + @optional：这个方法不一定要实现

```objc
@protocol SportProtocol <NSObject>

@required // 如果遵守协议的类不实现会报警告
- (void)playFootball;
@optional // 如果遵守协议的类不实现不会报警告
- (void)playBasketball;
@end
```

<h3 id="6.9">6.9 Protocol类型限制</h3>

##### 1.protocol类型限制
- 设定情景:
    + 某攻城狮A希望找一个会做饭、洗衣服的女生做女朋友,有国企工作的优先。
    + 满足条件的女生都可以向他发送消息

- 从题目中我们得到要求
    + 会做饭
    + 会洗衣服
    + 有份好工作

```objc
@protocol WifeCondition<NSObject>
- (void)cooking;
- (void)washing;
- (void)job;
@end
```

- 如何在代码中要求对象必须具备这些行为?
    + 数据类型<协议名称> 变量名

```objc
// 如果没有遵守协议则会报警告
id<WifeCondition> wife = [[Person alloc] init];
```

<h3 id="6.10">6.10 Protocol代理设计模式</h3>

##### 1.代理设计模式基本概念
- 什么是设计模式
    + 设计模式（Design pattern）是一套被反复使用、多数人知晓的、经过分类编目的、代码设计经验的总结。使用设计模式是为了可重用代码、让代码更容易被他人理解、保证代码可靠性。毫无疑问，设计模式于己于他人于系统都是多赢的；设计模式使代码编制真正工程化；设计模式是软件工程的基石脉络，如同大厦的结构一样。

- 什么是代理设计模式
    + 生活中大家一定遇到这样的情况了：比如说我要买一包纸，不妨就是心相印的吧，那一般人的话我应该不是去心相印的工厂里面直接去买吧，而是我们在心相印专卖店或者什么超市啊，这些地方购买，这些地方实际上就是洁丽雅毛巾的代理。这其实和我们OO中的代理模式是很相似的。

- 代理设计模式的场合:
    + 当对象A发生了一些行为,想告知对象B(让对象B成为对象A的代理对象)
    + 对象B想监听对象A的一些行为(让对象B成为对象A的代理对象)
    + 当对象A无法处理某些行为的时候,想让对象B帮忙处理(让对象B成为对象A的代理对象)



##### 2.代理设计模式示例
- 婴儿吃饭睡觉

```objc
// 协议
#import <Foundation/Foundation.h>
@class Baby;

@protocol BabyProtocol <NSObject>
- (void)feedWithBaby:(Baby *)baby;
- (void)hypnosisWithBaby:(Baby *)baby;
@end
```

```objc
#import "BabyProtocol.h"
@interface Baby : NSObject
// 食量
@property (nonatomic, assign) int food;
// 睡意
@property (nonatomic, assign) int drowsiness;
// 饿
- (void)hungry;
// 睡意
- (void)sleepy;
@property (nonatomic, strong) id<BabyProtocol> nanny;
@end

@implementation Baby

- (void)hungry
{
    self.food -= 5;
    NSLog(@"婴儿饿了");
    // 通知保姆
    if ([self.nanny respondsToSelector:@selector(feedWithBaby:)]) {
        [self.nanny feedWithBaby:self];
    }
}

- (void)sleepy
{
    self.drowsiness += 5;
    NSLog(@"婴儿困了");
    // 通知保姆
    if ([self.nanny respondsToSelector:@selector(hypnosisWithBaby:)]) {
        [self.nanny hypnosisWithBaby:self];
    }
}
@end

```

```objc
// 保姆
@interface Nanny : NSObject <BabyProtocol>
@end

@implementation Nanny

- (void)feedWithBaby:(Baby *)baby
{
    baby.food += 10;
    NSLog(@"给婴儿喂奶, 现在的食量是%i", baby.food);
}

- (void)hypnosisWithBaby:(Baby *)baby
{
    baby.drowsiness += 10;
    NSLog(@"哄婴儿睡觉, 现在的睡意是%i", baby.drowsiness);
}
@end
```

- 有一个婴儿,他本身不会自己吃饭和洗澡等等一些事情,于是婴儿就请了一个保姆,于是婴儿和保姆之间商定了一个协议,协议中写明了保姆需要做什么事情,而保姆就是这个代理人,即:婴儿和保姆之间有个协议,保姆遵守该协议,于是保姆就需要实现该协议中的条款成为代理人



##### 3.代理设计模式练习
- 学生通过中介找房子的过程,学生不知道怎么找所以让代理帮忙找

<h2 id="7">7. Foundation框架</h2>

<h3 id="7.1">7.1 Foundation框架介绍</h3>

##### 1.Foundation框架介绍
- 什么是框架?
    + 众多功能\API的集合
    + 框架是由许多类、方法、函数、文档按照一定的逻辑组织起来的集合,以便使研发程序变得更容易,在OS X下的Mac操作系统中大约有80个框架,为所有程序开发奠定基础的框架称为Foundation 框架

- Foundation框架的作用
    + Foundation框架是Mac\iOS中其他框架的基础
    + Foundation框架包含了很多开发中常用的数据类型:
        * 结构体
        * 枚举
        * 类

- 如何使用Foundation框架
    + Foundation框架中大约有125个可用的头文件,作为一个简单的形式,可以简单地使用以下语句导入#import<Foundation/Foundation.h>因为Foundation.h文件实际上导入其他所有Foundation框架中的头文件

- Foundation框架中的类
    + Foundation框架允许使用一些基本对象,如数字和字符串,以及一些对象集合,如数组,字典和集合,其他功能包括处理日期和时间、内存管理、处理文件系统、存储(或归档)对象、处理几何数据结构(如点和长方形)
    + Foundation框架提供了非常多好用的类, 比如
```objc
NSString : 字符串
NSArray : 数组
NSDictionary : 字典
NSDate : 日期
NSData : 数据
NSNumber : 数字
```

- Foundation框架中的类都是以NS为前缀(Next Step的缩写)
    + 乔布斯于1976年创立苹果公司
    + 乔布斯于1985年离开苹果公司, 创立NeXT公司, 开发了Next Step操作系统
    + 在开发Next Step操作系统过程中产生了Foundation框架
    + 1997年, 苹果公司收购NeXT公司,   乔布斯重返苹果公司(Mac系统就是基于Next Step系统)
    + 2007年, 苹果公司发布了iOS系统(iOS系统基于Mac系统)



##### 2.Foundation框架常见错误
- 有时候会在不经意之间修改了系统自带的头文件, 比如NSString.h, 这时会出现以下错误:

![foundationerror.png](http://upload-images.jianshu.io/upload_images/328309-d7376364e859c8cd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 解决方案很简单, 只需要删除Xcode的缓存即可
    + 缓存路径是/Users/用户名/Library/Developer/Xcode/DerivedData(默认情况下, 这是一个隐藏文件夹)

- 要想看到上述文件夹, 必须在终端敲指令显示隐藏文件夹, 指令如下
    + 显示隐藏文件 : defaults write com.apple.finder AppleShowAllFiles –bool true
    + 隐藏隐藏文件 : defaults write com.apple.finder AppleShowAllFiles –bool false
    + (输入指令后, 一定要重新启动Finder)


<h3 id="7.2">7.2 NSString基本概念</h3>

##### 1.NSString基本概念
- 什么是NSString?
    + 一个NSString对象就代表一个字符串(文字内容)
    + 一般称NSString为字符串类

##### 2.NSString创建方式

- 最直接的方式(常量字符串)
    + 常量区中的字符串只要内容一致, 不会重复创建
```objc
NSString *str1 = @"lnj";
NSString *str3 = @"lnj";
NSLog(@"str1 = %p, str3 = %p", str1, str3);
输出地址一致
```
- 格式化的方式
    + 堆区中得字符串哪怕内容一致, 也会重复创建
```objc
NSString *str2 = [NSString stringWithFormat:@"lnj"];
NSString *str4 = [NSString stringWithFormat:@"lnj"];
NSLog(@"str2 = %p, str4 = %p", str2, str4);
输出地址不一样
```

```objc
 NSString *str2 = [[NSString alloc] initWithFormat:@"height is %f". 1.75];
```

<h3 id="7.3">7.3 NSString字符串读写</h3>

##### 1.直接读写文件中的字符
- 从文件中读取

```objc
// 用来保存错误信息
NSError *error = nil;

// 读取文件内容
NSString *str = [NSString stringWithContentsOfFile:@"/Users/LNJ/Desktop/lnj.txt" encoding:NSUTF8StringEncoding error:&error];

// 如果有错误信息
if (error) {
    NSLog(@"读取失败, 错误原因是:%@", [error localizedDescription]);
} else { // 如果没有错误信息
    NSLog(@"读取成功, 文件内容是:\n%@", str);
}
```

- 写入文件中

```objc
NSString *str = @"江哥";
BOOL flag = [str writeToFile:@"/Users/LNJ/Desktop/lnj.txt" atomically:YES encoding:NSUTF8StringEncoding error:nil];
if (flag == 1)
{
    NSLog(@"写入成功");
}
```

- 重复写入同一文件会覆盖掉上一次的内容

```objc
NSString *str1 = @"江哥";
BOOL flag = [str1 writeToFile:@"/Users/LNJ/Desktop/lnj.txt" atomically:YES encoding:NSUTF8StringEncoding error:nil];

NSString *str2 = @"南哥";
[str2 writeToFile:@"/Users/LNJ/Desktop/lnj.txt" atomically:YES encoding:NSUTF8StringEncoding error:nil];

NSString *str = [NSString stringWithContentsOfFile:@"/Users/LNJ/Desktop/lnj.txt" encoding:NSUTF8StringEncoding error:&error];
NSLog(@"str = %@", str);

输出结果:南哥
```


##### 2.NSURL简介
- 什么是URL
    + URL的全称是Uniform Resource Locator(统一资源定位符)
    + URL是互联网上标准资源的地址
    + 互联网上的每个资源都有一个唯一的URL，它包含的信息指出资源的位置
    + 根据一个URL就能找到唯一的一个资源

- URL的格式
    + 基本URL包含协议、主机域名（服务器名称\IP地址）、路径
    + 举例: http://www.520it.com/ios/images/content_25.jpg
    + 可以简单认为: URL == 协议头://主机域名/路径

- 常见的URL协议头(URL类型)
    + http://\https:// :超文本传输协议资源, 网络资源
    + ftp:// :文件传输协议
    + file:// :本地电脑的文件

- URL的创建
    + 传入完整的字符串创建
```objc
NSURL *url = [NSURL URLWithString:@"file:///Users/LNJ/Desktop/str.txt"];
```
    + 通过文件路径创建(默认就是file协议的)
```objc
NSURL *url = [NSURL fileURLWithPath:@"/Users/LNJ/Desktop/str.txt"];
```


##### 3.使用NSURL读写字符串
- 从URL中读取

```objc
// 用来保存错误信息
NSError *error = nil;

// 创建URL路径
//    NSString *path = @"file://192.168.199.119/Users/LNJ/Desktop/lnj.txt";

//  本机可以省略主机域名
//    NSString *path = @"file:///Users/LNJ/Desktop/lnj.txt";
    NSURL *url = [NSURL URLWithString:path];

//  利用fileURLWithPath方法创建出来的URL默认协议头为file://
NSURL *url = [NSURL fileURLWithPath:@"/Users/LNJ/Desktop/lnj.txt"];

// 读取文件内容
NSString *str = [NSString stringWithContentsOfURL:url encoding:NSUTF8StringEncoding error:&error];

// 如果有错误信息
if (error) {
    NSLog(@"读取失败, 错误原因是:%@", [error localizedDescription]);
} else { // 如果没有错误信息
    NSLog(@"读取成功, 文件内容是:\n%@", str);
}
```

- 写入URL中

```objc
NSString *str = @"江哥";
[str writeToURL:[NSURL URLWithString:@"/Users/LNJ/Desktop/lnj.txt"] atomically:YES encoding:NSUTF8StringEncoding error:nil];

```

<h3 id="7.4">7.4 NSString字符串比较</h3>

##### 1.NSString大小写处理
- 全部字符转为大写字母
    + \- (NSString *)uppercaseString;

- 全部字符转为小写字母
    + \- (NSString *)lowercaseString

- 首字母变大写，其他字母都变小写
    + \- (NSString *)capitalizedString




##### 2.NSString比较
- \- (BOOL)isEqualToString:(NSString *)aString;
    + 两个字符串的内容相同就返回YES, 否则返回NO

```objc
    NSString *str1 = @"lnj";
    NSString *str2 = [NSString stringWithFormat:@"lnj"];
    if ([str1 isEqualToString:str2]) {
        NSLog(@"字符串内容一样");
    }

    if (str1 == str2) {
        NSLog(@"字符串地址一样");
    }
```

- \- (NSComparisonResult)compare:(NSString *)string;
    + 这个方法可以用来比较两个字符串内容的大小
    + 比较方法: 逐个字符地进行比较ASCII值，返回NSComparisonResult作为比较结果
    + NSComparisonResult是一个枚举，有3个值:
        * 如果左侧   > 右侧,返回NSOrderedDescending,
        * 如果左侧   < 右侧,返回NSOrderedAscending,
        * 如果左侧  == 右侧返回NSOrderedSame

```objc
    NSString *str1 = @"abc";
    NSString *str2 = @"abd";
    switch ([str1 compare:str2]) {
        case NSOrderedAscending:
            NSLog(@"后面一个字符串大于前面一个");
            break;
        case NSOrderedDescending:
            NSLog(@"后面一个字符串小于前面一个");
            break;
        case NSOrderedSame:
            NSLog(@"两个字符串一样");
            break;
    }
    输出结果: 后面一个字符串大于前面一个

```
- \- (NSComparisonResult) caseInsensitiveCompare:(NSString *)string;
    + 忽略大小写进行比较，返回值与compare:一致

```objc
    NSString *str1 = @"abc";
    NSString *str2 = @"ABC";
    switch ([str1 caseInsensitiveCompare:str2]) {
        case NSOrderedAscending:
            NSLog(@"后面一个字符串大于前面一个");
            break;
        case NSOrderedDescending:
            NSLog(@"后面一个字符串小于前面一个");
            break;
        case NSOrderedSame:
            NSLog(@"两个字符串一样");
            break;
    }
    输出结果:两个字符串一样
```


<h3 id="7.5">7.5 NSString字符串搜索</h3>

##### 1.字符串搜索
- \- (BOOL)hasPrefix:(NSString *)aString;
    + 是否以aString开头

- \- (BOOL)hasSuffix:(NSString *)aString;
    + 是否以aString结尾

- \- (NSRange)rangeOfString:(NSString *)aString;
    + 用来检查字符串内容中是否包含了aString
    + 如果包含, 就返回aString的范围
    + 如果不包含, NSRange的location为NSNotFound, length为0




##### 2.NSRange基本概念
- NSRange是Foundation框架中比较常用的结构体, 它的定义如下:

```objc
typedef struct _NSRange {
    NSUInteger location;
    NSUInteger length;
} NSRange;
// NSUInteger的定义
typedef unsigned int NSUInteger;
```

- NSRange用来表示事物的一个范围,通常是字符串里的字符范围或者数组里的元素范围

- NSRange有2个成员
    + NSUInteger location : 表示该范围的起始位置
    + NSUInteger length : 表示该范围内的长度

- 比如@“I love LNJ”中的@“LNJ”可以用location为7，length为3的范围来表示





##### 3.NSRange的创建
- 有3种方式创建一个NSRange变量
- 方式1

```objc
NSRange range;
range.location = 7;
range.length = 3;
```
- 方式2

```objc
NSRange range = {7, 3};
或者
NSRange range = {.location = 7,.length = 3};
```

- 方式3 : 使用NSMakeRange函数

```objc
NSRange range = NSMakeRange(7, 3);
```

<h3 id="7.6">7.6 NSString字符串截取</h3>

##### 1.字符串的截取
- \- (NSString *)substringFromIndex:(NSUInteger)from;
    + 从指定位置from开始(包括指定位置的字符)到尾部

```objc
    NSString *str = @"<head>小码哥</head>";
    str = [str substringFromIndex:7];
    NSLog(@"str = %@", str);

输出结果: 小码哥</head>
```
- \- (NSString *)substringToIndex:(NSUInteger)to;
    + 从字符串的开头一直截取到指定的位置to，但不包括该位置的字符

```objc
    NSString *str = @"<head>小码哥</head>";
    str = [str substringToIndex:10];
    NSLog(@"str = %@", str);

输出结果: <head>小码哥
```

- \- (NSString *)substringWithRange:(NSRange)range;
    + 按照所给出的NSRange从字符串中截取子串

```objc
    NSString *str = @"<head>小码哥</head>";
    NSRange range;
    /*
    range.location = 6;
    range.length = 3;
    */
    range.location = [str rangeOfString:@">"].location + 1;
    range.length = [str rangeOfString:@"</"].location - range.location;
    NSString *res = [str substringWithRange:range];
    NSLog(@"res = %@", res);
输出结果: 小码哥
```


<h3 id="7.7">7.7 NSString字符串替换</h3>

##### 1.字符串的替换函数
- \- (NSString *)stringByReplacingOccurrencesOfString:(NSString *)target withString:(NSString *)replacement;
    + 用replacement替换target

```objc
    NSString *str = @"http:**520it.com*img*ljn.gif";
    NSString *newStr = [str stringByReplacingOccurrencesOfString:@"*" withString:@"/"];
    NSLog(@"newStr = %@", newStr);

输出结果: http://www.520it.com/img/ljn.gif
```

- \- (NSString *)stringByTrimmingCharactersInSet:(NSCharacterSet *)set;
    + 去除首尾

```objc
    NSString *str =  @"   http://520it.com/img/ljn.gif   ";
    NSString *newStr = [str stringByTrimmingCharactersInSet:[NSCharacterSet whitespaceCharacterSet]];
    NSLog(@"str =|%@|", str);
    NSLog(@"newStr =|%@|", newStr);

输出结果:
str =|   http://520it.com/img/ljn.gif   |
newStr =|http://520it.com/img/ljn.gif|

```

```objc
    NSString *str =  @"***http://520it.com/img/ljn.gif***";
    NSString *newStr = [str stringByTrimmingCharactersInSet:[NSCharacterSet characterSetWithCharactersInString:@"*"]];

    NSLog(@"str =|%@|", str);
    NSLog(@"newStr =|%@|", newStr);

输出结果:
str =|***http://520it.com/img/ljn.gif***|
newStr =|http://520it.com/img/ljn.gif|
```

<h3 id="7.8">7.8 NSString字符串读写</h3>

##### 1.NSString与路径
- \- (BOOL)isAbsolutePath;
    + 是否为绝对路径

```objc
     // 其实就是判断是否以/开头
//    NSString *str = @"/Users/NJ-Lee/Desktop/lnj.txt";
    NSString *str = @"Users/NJ-Lee/Desktop/lnj.txt";
    if ([str isAbsolutePath]) {
        NSLog(@"是绝对路径");
    }else
    {
        NSLog(@"不是绝对路径");
    }
```
- \- (NSString *)lastPathComponent;
    + 获得最后一个目录

```objc
    // 截取最后一个/后面的内容
    NSString *str = @"/Users/NJ-Lee/Desktop/lnj.txt";
    NSString *component = [str lastPathComponent];
    NSLog(@"component = %@", component);
```
- \- (NSString *)stringByDeletingLastPathComponent;
    + 删除最后一个目录

```objc
    // 其实就是上次最后一个/和之后的内容
    NSString *str = @"/Users/NJ-Lee/Desktop/lnj.txt";
    NSString *newStr = [str stringByDeletingLastPathComponent];
    NSLog(@"newStr = %@", newStr);
```
- \- (NSString *)stringByAppendingPathComponent:(NSString *)str;
    + 在路径的后面拼接一个目录
(也可以使用stringByAppendingString:或者stringByAppendingFormat:拼接字符串内容)

```objc
// 其实就是在最后面加上/和要拼接得内容
    // 注意会判断后面有没有/有就不添加了, 没有就添加, 并且如果有多个会替换为1个
//    NSString *str = @"/Users/NJ-Lee/Desktop";
    NSString *str = @"/Users/NJ-Lee/Desktop/";
    NSString *newStr = [str stringByAppendingPathComponent:@"lnj"];
    NSLog(@"newStr = %@", newStr);
```
---

##### 2.NSString与文件拓展名
- \- (NSString *)pathExtension;
    + 获得拓展名

```objc
    // 其实就是从最后面开始截取.之后的内容
//    NSString *str = @"lnj.txt";
    NSString *str = @"abc.lnj.txt";
    NSString *extension = [str pathExtension];
    NSLog(@"extension = %@", extension);
```
- \- (NSString *)stringByDeletingPathExtension;
    + 删除尾部的拓展名

```objc
    // 其实就是上次从最后面开始.之后的内容
//    NSString *str = @"lnj.txt";
    NSString *str = @"abc.lnj.txt";
    NSString *newStr = [str stringByDeletingPathExtension];
    NSLog(@"newStr = %@", newStr);
```
- \- (NSString *)stringByAppendingPathExtension:(NSString *)str;
    + 在尾部添加一个拓展名

```objc
// 其实就是在最后面拼接上.和指定的内容
    NSString *str = @"lnj";
    NSString *newStr = [str stringByAppendingPathExtension:@"gif"];
    NSLog(@"newStr = %@", newStr);
```

<h3 id="7.9">7.9 NSString字符串与基本数据类型转换</h3>

##### 1.字符串索引
- \- (NSUInteger)length;
    + 返回字符串的长度(有多少个文字)

- \- (unichar)characterAtIndex:(NSUInteger)index;
    + 返回index位置对应的字符



##### 2.字符串和其他数据类型转换
- 转为基本数据类型
    + \- (double)doubleValue;
    + \- (float)floatValue;
    + \- (int)intValue;

```objc
    NSString *str1 = @"110";
    NSString *str2 = @"10";
    int res = str1.intValue + str2.intValue;
    NSLog(@"res = %i", res);
```

```objc
    NSString *str1 = @"110";
    NSString *str2 = @"10.1";
    double res = str1.doubleValue + str2.doubleValue;
    NSLog(@"res = %f", res);
```
- 转为C语言中的字符串
    + \- (char *)UTF8String;

```objc
    NSString *str = @"abc";
    const char *cStr = [str UTF8String];
    NSLog(@"cStr = %s", cStr);
```

```objc
    char *cStr = "abc";
    NSString *str = [NSString stringWithUTF8String:cStr];
    NSLog(@"str = %@", str);
```

<h3 id="7.10">7.10 NSMutableString基本概念</h3>

##### 1.NSMutableString 基本概念
- NSMutableString 类 继承NSString类,那么NSString 􏰀供的方法在NSMutableString中基本都可以使用,NSMutableString好比一个字符串链表,它可以任意的动态在字符串中添加字符 串 删除字符串 指定位置插入字符串,使用它来操作字符串会更加灵活。

- NSMutableString和NSString的区别
    + NSString是不可变的, 里面的文字内容是不能进行修改的
    + NSMutableString是可变的, 里面的文字内容可以随时更改
    + NSMutableString能使用NSString的所有方法



##### 2.字符串中的可变和不可变
- 不可变:指的是字符串在内存中占用的存储空间固定,并且存储的内容不能发生变化

```objc
    // 改变了指针的指向, 并没有修改字符串
    NSString *str = @"lnj";
    str = @"lmj";

    // 生成了一个新的字符串, 并没有修改字符串
    NSString *newStr = [str substringFromIndex:1];
    NSLog(@"str = %@", str);
    NSLog(@"newStr = %@", newStr);
```
- 可变:指的是字符串在内存中占用的存储空间可以不固定,并且存储的内容可以被修改

```objc
    NSMutableString *strM = [NSMutableString string];
    NSLog(@"strM = %@", strM);
     // 修改原有字符串, 没有生成新的字符串
    [strM appendString:@"lnj"];
    NSLog(@"strM = %@", strM);
    [strM appendString:@" v587"];
    NSLog(@"strM = %@", strM);
```

<h3 id="7.11">7.11 NSMutableString常用方法</h3>

##### 1.NSMutableString常用方法
- \- (void)appendString:(NSString *)aString;
    + 拼接aString到最后面

```objc
 NSMutableString *strM = [NSMutableString string];
    NSLog(@"strM = %@", strM);
    [strM appendString:@"lnj"];
    NSLog(@"strM = %@", strM);

```
- \- (void)appendFormat:(NSString *)format, ...;
    + 拼接一段格式化字符串到最后面

```objc
NSMutableString *strM = [NSMutableString string];
[strM appendFormat:@"/age is %i", 10];
```
- \- (void)deleteCharactersInRange:(NSRange)range;
    + 删除range范围内的字符串

```objc
    NSMutableString *strM = [NSMutableString stringWithString:@"http://www.520it.com"];
     // 一般情况下利用rangeOfString和deleteCharactersInRange配合删除指定内容
     NSRange range = [strM rangeOfString:@"http://"];
     [strM deleteCharactersInRange:range];
     NSLog(@"strM = %@", strM);
```
- \- (void)insertString:(NSString *)aString atIndex:(NSUInteger)loc;
    + 在loc这个位置中插入aString

```objc
    NSMutableString *strM = [NSMutableString stringWithString:@"www.520it.com"];
    [strM insertString:@"http://" atIndex:0];
    NSLog(@"strM = %@", strM);

```
- \- (void)replaceCharactersInRange:(NSRange)range withString:(NSString *)aString;
    + 使用aString替换range范围内的字符串

```objc
    NSMutableString *strM = [NSMutableString stringWithString:@"http://www.520it.com/lnj.png"];
    NSRange range = [strM rangeOfString:@"lnj"];
    [strM replaceOccurrencesOfString:@"lnj" withString:@"jjj" options:0 range:range];
    NSLog(@"strM = %@", strM);
```



##### 2.字符串使用注意事项
- @”lnj”这种方式创建的字符串始终是NSString,不是NSMutalbeString.所以下面的代码创建的还是NSString,此时使用可变字符串的函数,无法操作字符串。

```objc
NSMutalbeString *s1 = @”lnj”;
// 会报错
[strM insertString:@"my name is " atIndex:0];
```

<h3 id="7.12">7.12 NSMutableString练习</h3>

##### 1.NSMutableString练习
- 从要求讲3个520it拼接在一起

- 会生成很多新的字符串

```objc
    NSString *res = @"";
    NSString *subStr = @"520";
    // 1.拼接字符串

//    res = [res stringByAppendingString:subStr];
//    res = [res stringByAppendingString:@" "];
//
//    res = [res stringByAppendingString:subStr];
//    res = [res stringByAppendingString:@" "];
//
//    res = [res stringByAppendingString:subStr];
//    res = [res stringByAppendingString:@" "];

    for (int i = 0; i < 3; ++i) {
        res = [res stringByAppendingString:subStr];
        res = [res stringByAppendingString:@" "];
    }

    // 2.删除末尾的空格
//    res = [res stringByTrimmingCharactersInSet:[NSCharacterSet whitespaceCharacterSet]];
    res = [res substringToIndex:res.length - 1];

    NSLog(@"res = |%@|", res);
```

- 不会生成新的字符串

```objc
    NSString *subStr = @"520it";
    NSMutableString *res = [NSMutableString string];
    // 1.拼接字符串
    for (int i = 0; i < 3; ++i) {
        [res appendString:subStr];
        [res appendString:@" "];
    }
    // 2.删除空格
//    [res replaceCharactersInRange:NSMakeRange(res.length - 1, 1) withString:@""];
    [res deleteCharactersInRange:NSMakeRange(res.length - 1, 1)];
    NSLog(@"res = |%@|", res);
```

<h3 id="7.13">7.13 NSArray基本概念</h3>

##### 1.NSArray的基本概念
- 什么是NSArray?
    + NSArray是OC中的数组类,开发中建议尽量使用NSArray替代C语言中的数组
    + C语言中数组的弊端
        * int array[4] = {10, 89, 27, 76};
        * 只能存放一种类型的数据.(类型必须一致)
        * 不能很方便地动态添加数组元素、不能很方便地动态删除数组元素(长度固定)

- NSArray的使用注意
    + 只能存放任意OC对象, 并且是有顺序的
    + 不能存储非OC对象, 比如int\float\double\char\enum\struct等
    + 它是不可变的,一旦初始化完毕后,它里面的内容就永远是固定的, 不能删除里面的元素, 也不能再往里面添加元素



##### 2.NSArray的创建方式
- \+ (instancetype)array;
- \+ (instancetype)arrayWithObject:(id)anObject;
- \+ (instancetype)arrayWithObjects:(id)firstObj, ...;
- \+ (instancetype)arrayWithArray:(NSArray *)array;

- \+ (id)arrayWithContentsOfFile:(NSString *)path;
- \+ (id)arrayWithContentsOfURL:(NSURL *)url;



##### 3.NSArray 的使用注意事项
- NSArray直接使用NSLog()作为字符串输出时是小括号括起来的形式。

- NSArray中不能存储nil,因为NSArray认为nil是数组的结束(nil是数组元素结束的标记)。nil就是0。0也是基本数据类型,不能存放到NSArray中。

```objc
    NSArray *arr = [NSArray arrayWithObjects:@"lnj", nil ,@"lmj",@"jjj", nil];
    NSLog(@"%@", arr);
输出结果:
(
    lnj
)
```


##### 4.NSArray的常用方法
- \- (NSUInteger)count;
    + 获取集合元素个数

- \- (id)objectAtIndex:(NSUInteger)index;
    + 获得index位置的元素

- \- (BOOL)containsObject:(id)anObject;
    + 是否包含某一个元素

- \- (id)lastObject;
    + 返回最后一个元素

- \- (id)firstObject;
    + 返回最后一个元素

- \- (NSUInteger)indexOfObject:(id)anObject;
    + 查找anObject元素在数组中的位置(如果找不到，返回-1)

- \- (NSUInteger)indexOfObject:(id)anObject inRange:(NSRange)range;
    + 在range范围内查找anObject元素在数组中的位置



##### 5.NSArray的简写形式
- 自从2012年开始, Xcode的编译器多了很多自动生成代码的功能, 使得OC代码更加精简

- 数组的创建
    + 之前
```objc
[NSArray arrayWithObjects:@"Jack", @"Rose", @"Jim", nil];
```
    + 现在
```objc
@[@"Jack", @"Rose", @"Jim"];
```

- 数组元素的访问
    + 之前
```objc
[array objectAtIndex:0];
```
    + 现在
```objc
array[0];
```

<h3 id="7.14">7.14 NSArray遍历</h3>

##### 1.NSArray的下标遍历

```objc
    NSArray *arr = @[p1, p2, p3, p4, p5];
    for (int i = 0; i < arr.count; ++i) {
        Person *p = arr[i];
        [p say];
    }
```
---

##### 2.NSArray的快速遍历

```objc
    NSArray *arr = @[p1, p2, p3, p4, p5];
   for (Person *p in arr) {
        [p say];
    }
```
---


##### 3.NSArray 使用block进行遍历

```objc
    [arr enumerateObjectsUsingBlock:^(id obj, NSUInteger idx, BOOL *stop) {
        NSLog(@"obj = %@, idx = %lu", obj, idx);
        Person *p = obj;
        [p say];
    }];
```


##### 4.NSArray给所有元素发消息
- 让集合里面的所有元素都执行aSelector这个方法
    + \- (void)makeObjectsPerformSelector:(SEL)aSelector;
    + \- (void)makeObjectsPerformSelector:(SEL)aSelector withObject:(id)argument;

```objc
    // 让数组中所有对象执行这个方法
    // 注意: 如果数组中的对象没有这个方法会报错
//    [arr makeObjectsPerformSelector:@selector(say)];
    [arr makeObjectsPerformSelector:@selector(eat:) withObject:@"bread"];
```


<h3 id="7.15">7.15 NSArray排序</h3>

##### 1.NSArray排序
- Foundation自带类排序

```objc
NSArray *arr = @[@(1), @(9), @(5), @(2)];
NSArray *newArr = [arr sortedArrayUsingSelector:@selector(compare:)];
```
- 自定义类排序

```objc
    NSArray *arr = @[p1, p2, p3, p4, p5];
    //    默认按照升序排序
    NSArray *newArr = [arr sortedArrayWithOptions:NSSortConcurrent usingComparator:^NSComparisonResult(Person *obj1, Person *obj2) {
        return obj1.age > obj2.age;
    }];
    NSLog(@"%@", newArr);
```

<h3 id="7.16">7.16 NSArray文件读写</h3>

##### 1.NSArray数据写入到文件中

```objc
    NSArray *arr = @[@"lnj", @"lmj", @"jjj", @"xcq"];
    BOOL flag = [arr writeToFile:@"/Users/LNJ/Desktop/persons.plist" atomically:YES];
    NSLog(@"%i", flag);
```


##### 2.从文件中读取数据到NSArray中

```objc
    NSArray *newArr = [NSArray arrayWithContentsOfFile:@"/Users/LNJ/Desktop/persons.xml"];
    NSLog(@"%@", newArr);
```

<h3 id="7.17">7.17 NSArray与字符串</h3>

##### 1.把数组元素链接成字符串
- \- (NSString *)componentsJoinedByString:(NSString *)separator;
    + 这是NSArray的方法, 用separator作拼接符将数组元素拼接成一个字符串

```objc
    NSArray *arr = @[@"lnj", @"lmj", @"jjj", @"xcq"];
    NSString *res = [arr componentsJoinedByString:@"*"];
    NSLog(@"res = %@", res);
输出结果:
lnj*lmj*jjj*xcq
```


##### 2.字符串分割方法
- \- (NSArray *)componentsSeparatedByString:(NSString *)separator;
    + 这是NSString的方法,将字符串用separator作为分隔符切割成数组元素

```objc
    NSString *str = @"lnj-lmj-jjj-xcq";
    NSArray *arr = [str componentsSeparatedByString:@"-"];
    NSLog(@"%@", arr);

输出结果:
(
    lnj,
    lmj,
    jjj,
    xcq
)

```

<h3 id="7.18">7.18 NSMutableArray基本概念</h3>

##### 1.NSMutableArray介绍
- 什么是NSMutableArray
    + NSMutableArray是NSArray的子类
    + NSArray是不可变的,一旦初始化完毕后,它里面的内容就永远是固定的, 不能删除里面的元素, 也不能再往里面添加元素
    + NSMutableArray是可变的,随时可以往里面添加\更改\删除元素



##### 2.NSMutableArray基本用法
- 创建空数组

```objc
NSMutableArray *arr = [NSMutableArray array];
```
- 创建数组,并且指定长度为5,此时也是空数组

```objc
NSMutableArray *arr2 = [[NSMutableArray alloc] initWithCapacity:5];
```
- 创建一个数组,包含两个元素

```objc
NSMutableArray *arr3 = [NSMutableArray arrayWithObjects:@"1",@"2", nil];
```
- 调用对象方法创建数组

```objc
NSMutableArray *arr4 = [[NSMutableArray alloc] initWithObjects:@"1",@"2", nil];
```

- \- (void)addObject:(id)object;
    + 添加一个元素

- \- (void)addObjectsFromArray:(NSArray *)array;
    + 添加otherArray的全部元素到当前数组中

- \- (void)insertObject:(id)anObject atIndex:(NSUInteger)index;
    + 在index位置插入一个元素

- \- (void)removeLastObject;
    + 删除最后一个元素

- \- (void)removeAllObjects;
    + 删除所有的元素

- \- (void)removeObjectAtIndex:(NSUInteger)index;
    + 删除index位置的元素

- \- (void)removeObject:(id)object;
    + 删除特定的元素

- \- (void)removeObjectsInRange:(NSRange)range;
    + 删除range范围内的所有元素

- \- (void)replaceObjectAtIndex:(NSUInteger)index withObject:(id)anObject;
    + 用anObject替换index位置对应的元素

- \- (void)exchangeObjectAtIndex:(NSUInteger)idx1 withObjectAtIndex:(NSUInteger)idx2;
    + 交换idx1和idx2位置的元素




##### 3.NSMutableArray 错误用法
- 不可以使用@[]创建可变数组

```objc
NSMutableArray *array = @[@"lnj", @"lmj", @"jjj"];
// 报错, 本质还是不可变数组
[array addObject:@“Peter”];
```

<h3 id="7.19">7.19 NSDictionary基本概念</h3>

##### 1.NSDictionar基本概念
- 什么是NSDictionary
    + NSDictionary翻译过来叫做”字典”
    + 日常生活中,“字典”的作用:通过一个拼音或者汉字,就能找到对应的详细解释
    + NSDictionary的作用类似:通过一个key,就能找到对应的value
    + NSDictionary是不可变的, 一旦初始化完毕, 里面的内容就无法修改


##### 2.NSDictionary的创建
```
+ (instancetype)dictionary;
+ (instancetype)dictionaryWithObject:(id)object forKey:(id <NSCopying>)key;
+ (instancetype)dictionaryWithObjectsAndKeys:(id)firstObject, ...;
+ (id)dictionaryWithContentsOfFile:(NSString *)path;
+ (id)dictionaryWithContentsOfURL:(NSURL *)url;
```

- NSDictionary创建简写
    + 以前
```objc
NSDictionary *dict = [NSDictionary dictionaryWithObjectsAndKeys:@"lnj", @"name", @"12345678", @"phone", @"天朝", @"address", nil];
```
    + 现在
```objc
NSDictionary *dict = @{@"name":@"lnj", @"phone":@"12345678", @"address":@"天朝"};
```

- NSDictionary获取元素简写
    + 以前
```objc
[dict objectForKey:@"name”];
```
    + 现在
```objc
dict[@"name”];
```


- 键值对集合的特点
    + 字典存储的时候,必须是"键值对"的方式来存储(同时键不要重复)
    + 键值对中存储的数据是"无序的".
    + 键值对集合可以根据键, 快速获取数据.

##### 3.NSDictionary的遍历
- \- (NSUInteger)count;
    + 返回字典的键值对数目

- \- (id)objectForKey:(id)aKey;
    + 根据key取出value


- 快速遍历

```objc
    NSDictionary *dict = @{@"name":@"lnj", @"phone":@"12345678", @"address":@"天朝"};
    for (NSString *key in dict) {
        NSLog(@"key = %@, value = %@", key, dict[key]);
    }
```
- Block遍历

```objc
    [dict enumerateKeysAndObjectsUsingBlock:^(NSString *key, NSString *obj, BOOL *stop) {
        NSLog(@"key = %@, value = %@", key, obj);
    }];

```

##### 4.NSDictionary文件操作
- 将字典写入文件中
    + \- (BOOL)writeToFile:(NSString *)path atomically:(BOOL)useAuxiliaryFile;
    + \- (BOOL)writeToURL:(NSURL *)url atomically:(BOOL)atomically;
    + 存结果是xml文件格式,但苹果官方推荐为plist后缀。

- 示例

```objc
    NSDictionary *dict = @{@"name":@"lnj", @"phone":@"12345678", @"address":@"天朝"};
    BOOL flag = [dict writeToFile:@"/Users/LNJ/Desktop/dict.plist" atomically:YES];
    NSLog(@"flag = %i", flag);
```

- 从文件中读取字典

```objc
NSDictionary *newDict = [NSDictionary dictionaryWithContentsOfFile:@"/Users/LNJ/Desktop/dict.plist"];
    NSLog(@"newDict = %@", newDict);
```


<h3 id="7.20">7.20 NSMutableDictionary基本概念</h3>

##### 1.NSMutableDictionary 基本概念
- 什么是NSMutableDictionary
    + NSMutableDictionary是NSDictionary的子类
    + NSDictionary是不可变的,一旦初始化完毕后,它里面的内容就永远是固定的,不能删除里面的元素, 也不能再往里面添加元素
    + NSMutableDictionary是可变的,随时可以往里面添加\更改\删除元素




##### 2.NSMutableDictionary的常见操作
- \- (void)setObject:(id)anObject forKey:(id <NSCopying>)aKey;
    + 添加一个键值对(会把aKey之前对应的值给替换掉)

- \- (void)removeObjectForKey:(id)aKey;
    + 通过aKey删除对应的value

- \- (void)removeAllObjects;
    + 删除所有的键值对

##### 3.NSMutableDictionary的简写
- 设置键值对
    + 以前
```objc
[dict setObject:@"Jack" forKey:@"name”];
```
    + 现在
```objc
dict[@"name"] = @"Jack";
```


##### 4.NSDictionary和NSArray对比
- NSArray和NSDictionary的区别
    + NSArray是有序的,NSDictionary是无序的
    + NSArray是通过下标访问元素,NSDictionary是通过key访问元素

- NSArray的用法
    + 创建
```objc
@[@"Jack", @"Rose"] (返回是不可变数组)
```
    + 访问
```objc
id d = array[1];
```
    + 赋值
```objc
array[1] = @"jack";
```

- NSDictionary的用法
    +创建
```objc
@{ @"name" : @"Jack", @"phone" : @"10086" } (返回是不可变字典)
```
    + 访问
```objc
id d = dict[@"name"];
```
    + 赋值
```objc
dict[@"name"] = @"jack";
```

<h3 id="7.21">7.21 常见的结构体</h3>
##### 1.NSPoint和CGPoint
- CGPoint和NSPoint是同义的

```objc
typedef CGPoint NSPoint;

CGPoint的定义
struct CGPoint {
  CGFloat x;
  CGFloat y;
};
typedef struct CGPoint CGPoint;
typedef double CGFloat;
```
- CGPoint代表的是二维平面中的一个点
    + 可以使用CGPointMake和NSMakePoint函数创建CGPoint




##### 2.NSSize和CGSize
- CGSize和NSSize是同义的

```objc
typedef CGSize NSSize;

CGSize的定义
struct CGSize {
  CGFloat width;
  CGFloat height;
};
typedef struct CGSize CGSize;
```

- CGSize代表的是二维平面中的某个物体的尺寸(宽度和高度)
    + 可以使用CGSizeMake和NSMakeSize函数创建CGSize




##### 3.NSRect和CGRect
- CGRect和NSRect是同义的

```objc
typedef CGRect NSRect;

CGRect的定义
struct CGRect {
  CGPoint origin;
  CGSize size;
};
typedef struct CGRect CGRect;
```

- CGRect代表的是二维平面中的某个物体的位置和尺寸
    + 可以使用CGRectMake和NSMakeRect函数创建CGRect



##### 4.常见的结构体使用注意
-   苹果官方推荐使用CG开头的:
    + CGPoint
    + CGSize
    + CGRect

<h3 id="7.22">7.22 NSNumber</h3>
##### 1.NSNumber基本概念
- NSArray\NSDictionary中只能存放OC对象,不能存放int\float\double等基本数据类

- 如果真想把基本数据(比如int)放进数组或字典中,需要先将基本数据类型包装成OC对象

![nsnumber1.png](http://upload-images.jianshu.io/upload_images/328309-c70179ecab7c79f8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- NSNumber可以将基本数据类型包装成对象,这样就可以间接将基本数据类型存进NSArray\NSDictionary中

![nsnumber2.png](http://upload-images.jianshu.io/upload_images/328309-b2bba8d9c3ff9353.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



##### 2.NSNumber的创建
- 以前

```objc
+ (NSNumber *)numberWithInt:(int)value;
+ (NSNumber *)numberWithDouble:(double)value;
+ (NSNumber *)numberWithBool:(BOOL)value;
```

- 现在
```objc
@10;
@10.5;
@YES;
@(num);
```



##### 3.从NSNumber对象中的到基本类型数据
```objc
- (char)charValue;
- (int)intValue;
- (long)longValue;
- (double)doubleValue;
- (BOOL)boolValue;
- (NSString *)stringValue;
- (NSComparisonResult)compare:(NSNumber *)otherNumber;
- (BOOL)isEqualToNumber:(NSNumber *)number;
```


<h3 id="7.23">7.23 NSValue</h3>
##### 1.NSValue基本概念
- NSNumber是NSValue的子类, 但NSNumber只能包装数字类型

- NSValue可以包装任意值
    + 因此, 可以用NSValue将结构体包装后,加入NSArray\NSDictionary中



##### 2. 常见结构体的包装
- 为了方便 结构体 和NSValue的转换,Foundation提供了以下方法
- 将结构体包装成NSValue对象

```objc
+ (NSValue *)valueWithPoint:(NSPoint)point;
+ (NSValue *)valueWithSize:(NSSize)size;
+ (NSValue *)valueWithRect:(NSRect)rect;
```

- 从NSValue对象取出之前包装的结构体

```
- (NSPoint)pointValue;
- (NSSize)sizeValue;
- (NSRect)rectValue;
```


##### 3.任意数据的包装
- NSValue提供了下列方法来包装任意数据

```objc
+ (NSValue *)valueWithBytes:(const void *)value objCType:(const char *)type;
+ value参数 : 所包装数据的地址
+ type参数 : 用来描述这个数据类型的字符串, 用@encode指令来生成

- 从NSValue中取出所包装的数据
- (void)getValue:(void *)value;
```

<h3 id="7.24">7.24 NSDate</h3>
##### 1.NSDate基本概念
- NSDate可以用来表示时间, 可以进行一些常见的日期\时间处理

- 一个NSDate对象就代表一个时间

- [NSDate date]返回的就是当前时间

```objc
    NSDate *now = [NSDate date];
    NSLog(@"now = %@", now);
     // 设置转换后的目标日期时区
     NSTimeZone *zone = [NSTimeZone systemTimeZone];
     // 得到源日期与世界标准时间的偏移量
     NSInteger interval = [zone secondsFromGMTForDate: date];
     NSLog(@"interval = %lu", interval);
     // 在当前时间基础上追加时区差值
     now = [now dateByAddingTimeInterval:interval];
     NSLog(@"%@", date);
```
---

##### 2.格式化日期
- NSDate -> NSString

```objc
    // 1.创建时间
    NSDate *now = [NSDate date];
    // 2.创建时间格式化
    NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
    // 3.指定格式
    formatter.dateFormat = @"yyyy-MM-dd HH:mm:ss";
    // 4.格式化时间
    NSString *str = [formatter stringFromDate:now];
    NSLog(@"%@", str);
```

- NSString -> NSDate

```objc
    NSString *str = @"2015-06-28 19:53:24";
    NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
    formatter.dateFormat = @"yyyy-MM-dd HH:mm:ss";
    NSDate *date = [formatter dateFromString:str];
    NSLog(@"%@", date);
```
---


##### 3.日期时间对象
- 结合NSCalendar和NSDate能做更多的日期\时间处理

- 获得NSCalendar对象

```objc
NSCalendar *calendar = [NSCalendar currentCalendar];
```

- 获得年月日

```objc
- (NSDateComponents *)components:(NSCalendarUnit)unitFlags fromDate:(NSDate *)date;
```

```objc
    NSDate *date = [NSDate date];
    // 1.创建日历对象
    NSCalendar *calendar = [NSCalendar currentCalendar];
    // 2.利用日历对象获取年月日时分秒
    NSCalendarUnit type = NSCalendarUnitYear | NSCalendarUnitMonth | NSCalendarUnitDay | NSCalendarUnitHour | NSCalendarUnitMinute | NSCalendarUnitSecond;
    NSDateComponents *cmps =[calendar components:type fromDate:date];
    NSLog(@"year = %lu", cmps.year);
    NSLog(@"month = %lu", cmps.month);
    NSLog(@"day = %lu", cmps.day);
    NSLog(@"hour = %lu", cmps.hour);
    NSLog(@"minute = %lu", cmps.minute);
    NSLog(@"second = %lu", cmps.second);
    NSLog(@"date = %@", date);
```

- 比较两个日期的差距

```objc
- (NSDateComponents *)components:(NSCalendarUnit)unitFlags fromDate:(NSDate *)startingDate toDate:(NSDate *)resultDate options:(NSCalendarOptions)opts;

```

```objc
    // 1.确定时间
    NSString *time1 = @"2015-06-23 12:18:15";
    NSString *time2 = @"2015-06-28 10:10:10";
    // 2.将时间转换为date
    NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
    formatter.dateFormat = @"yyyy-MM-dd HH:mm:ss";
    NSDate *date1 = [formatter dateFromString:time1];
    NSDate *date2 = [formatter dateFromString:time2];
    // 3.创建日历
    NSCalendar *calendar = [NSCalendar currentCalendar];
    NSCalendarUnit type = NSCalendarUnitYear | NSCalendarUnitMonth | NSCalendarUnitDay | NSCalendarUnitHour | NSCalendarUnitMinute | NSCalendarUnitSecond;
    // 4.利用日历对象比较两个时间的差值
    NSDateComponents *cmps = [calendar components:type fromDate:date1 toDate:date2 options:0];
    // 5.输出结果
    NSLog(@"两个时间相差%ld年%ld月%ld日%ld小时%ld分钟%ld秒", cmps.year, cmps.month, cmps.day, cmps.hour, cmps.minute, cmps.second);
```    

<h3 id="7.25">7.25 NSFileManager</h3>
##### 1.NSFileManager介绍
- 什么是NSFileManager
    + 顾名思义, NSFileManager是用来管理文件系统的
    + 它可以用来进行常见的文件\文件夹操作

- NSFileManager使用了单例模式
    + 使用defaultManager方法可以获得那个单例对象
```objc
[NSFileManager defaultManager]
```



##### 2.NSFileManager用法
- \- (BOOL)fileExistsAtPath:(NSString *)path;
    + path这个文件\文件夹是否存在

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    // 可以判断文件
    BOOL flag = [manager fileExistsAtPath:@"/Users/LNJ/Desktop/lnj.txt"];
    NSLog(@"flag = %i", flag);
    // 可以判断文件夹
    flag = [manager fileExistsAtPath:@"/Users/LNJ/Desktop/未命名文件夹"];
    NSLog(@"flag = %i", flag);
```
- \- (BOOL)fileExistsAtPath:(NSString *)path isDirectory:(BOOL *)isDirectory;
    + path这个文件\文件夹是否存在, isDirectory代表是否为文件夹

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    BOOL directory = NO;
    BOOL flag = [manager fileExistsAtPath:@"/Users/LNJ/Desktop/未命名文件夹" isDirectory:&directory];
    NSLog(@"flag = %i, directory = %i", flag, directory);
```
- \- (BOOL)isReadableFileAtPath:(NSString *)path;
    + path这个文件\文件夹是否可读

- \- (BOOL)isWritableFileAtPath:(NSString *)path;
    + path这个文件\文件夹是否可写
    + 系统目录不允许写入

- \- (BOOL)isDeletableFileAtPath:(NSString *)path;
    + path这个文件\文件夹是否可删除
    + 系统目录不允许删除




##### 3.NSFileManager的文件访问
- \- (NSDictionary *)attributesOfItemAtPath:(NSString *)path error:(NSError **)error;
    + 获得path这个文件\文件夹的属性

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    NSDictionary *dict = [manager attributesOfItemAtPath:@"/Users/LNJ/Desktop/lnj.txt" error:nil];
    NSLog(@"dit = %@", dict);
```

- \- (NSArray *)contentsOfDirectoryAtPath:(NSString *)path error:(NSError **)error;
    + 获得path的当前子路径

- \- (NSData *)contentsAtPath:(NSString *)path;
    + 获得文件内容

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    NSArray *paths = [manager contentsOfDirectoryAtPath:@"/Users/LNJ/Desktop/" error:nil];
    NSLog(@"paths = %@", paths);
```

- \- (NSArray *)subpathsAtPath:(NSString *)path;
- \- (NSArray *)subpathsOfDirectoryAtPath:(NSString *)path error:(NSError **)error;
    + 获得path的所有子路径

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    NSArray *paths = [manager subpathsAtPath:@"/Users/LNJ/Desktop/"];
    NSLog(@"paths = %@", paths);
```



##### 4.NSFileManager的文件操作
- \- (BOOL)copyItemAtPath:(NSString *)srcPath toPath:(NSString *)dstPath error:(NSError **)error;
    + 拷贝

- \- (BOOL)moveItemAtPath:(NSString *)srcPath toPath:(NSString *)dstPath error:(NSError **)error;
    + 移动(剪切)

- \- (BOOL)removeItemAtPath:(NSString *)path error:(NSError **)error;
    + 删除

- \- (BOOL)createDirectoryAtPath:(NSString *)path withIntermediateDirectories:(BOOL)createIntermediates attributes:(NSDictionary *)attributes error:(NSError **)error;
    + 创建文件夹(createIntermediates为YES代表自动创建中间的文件夹)

```objc
    NSFileManager *manager = [NSFileManager defaultManager];
    BOOL flag = [manager createDirectoryAtPath:@"/Users/LNJ/Desktop/test" withIntermediateDirectories:YES attributes:nil error:nil];
    NSLog(@"flag = %i", flag);
```
- \- (BOOL)createFileAtPath:(NSString *)path contents:(NSData *)data attributes:(NSDictionary *)attr;
    + 创建文件(NSData是用来存储二进制字节数据的)

```objc
    NSString *str = @"lnj";
    NSData  *data = [str dataUsingEncoding:NSUTF8StringEncoding];
    NSFileManager *manager = [NSFileManager defaultManager];
    BOOL flag = [manager createFileAtPath:@"/Users/LNJ/Desktop/abc.txt" contents:data attributes:nil];
    NSLog(@"flag = %i", flag);
```


<h3 id="7.26">7.26 集合对象的内存管理</h3>
##### 1.集合对象的内存管理
- 当一个对象加入到集合中,那么该对象的引用计数会+1
- 当集合被销毁的时候,集合会向集合中的元素发送release消息

```objc
    NSMutableArray *arr = [[NSMutableArray alloc] init];

    Person *p = [[Person alloc] init];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [arr addObject:p];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [p release];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [arr release];
```

- 当一个对象加入到集合中,那么该对象的引用计数会+1
- 当把一个对象从集合中移除时,会向移除的元素发送release消息

```objc
    NSMutableArray *arr = [[NSMutableArray alloc] init];
    Person *p = [[Person alloc] init];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [arr addObject:p];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [arr removeObject:p];
    NSLog(@"retainCount = %lu", [p retainCount]);
    [p release];
    [arr release];
```


##### 2.集合对象内存管理总结
- 1.官方内存管理原则
    + 1> 当调用alloc、new、copy(mutableCopy)方法产生一个新对象的时候,就必须在最后调用一次release或者autorelease
    + 2> 当调用retain方法让对象的计数器+1,就必须在最后调用一次release或者autorelease

- 2.集合的内存管理细节
    + 1> 当把一个对象添加到集合中时,这个对象会做了一次retain操作,计数器会+1
    + 2> 当一个集合被销毁时,会对集合里面的所有对象做一次release操作,计数器会-1
    + 3> 当一个对象从集合中移除时,这个对象会一次release操作,计数器会-1

- 3.普遍规律
    + 1> 如果方法名是add\insert开头,那么被添加的对象,计数器会+1
    + 2> 如果方法名是remove\delete开头,那么被移除的对象,计数器-1

<h3 id="7.27">7.27 Copy</h3>
##### 1.copy基本概念
- 什么是copy
    + Copy的字面意思是“复制”、“拷贝”，是一个产生副本的过程

- 常见的复制有：文件复制
    + 作用：利用一个源文件产生一个副本文件
- 特点：
    + 修改源文件的内容，不会影响副本文件
    + 修改副本文件的内容，不会影响源文件

- OC中的copy
    + 作用：利用一个源对象产生一个副本对象
- 特点：
    + 修改源对象的属性和行为，不会影响副本对象
    + 修改副本对象的属性和行为，不会影响源对象




##### 2.Copy的使用
- 如何使用copy功能
    + 一个对象可以调用copy或mutableCopy方法来创建一个副本对象
    + copy : 创建的是不可变副本(如NSString、NSArray、NSDictionary)
    + mutableCopy :创建的是可变副本(如NSMutableString、NSMutableArray、NSMutableDictionary)

- 使用copy功能的前提
    + copy : 需要遵守NSCopying协议，实现copyWithZone:方法

```objc
@protocol NSCopying
- (id)copyWithZone:(NSZone *)zone;
@end
```

- 使用mutableCopy的前提
    + 需要遵守NSMutableCopying协议，实现mutableCopyWithZone:方法

```objc
@protocol NSMutableCopying
- (id)mutableCopyWithZone:(NSZone *)zone;
@end
```

##### 3.深复制和浅复制
- 浅复制（浅拷贝，指针拷贝，shallow copy）
    + 源对象和副本对象是同一个对象
    + 源对象（副本对象）引用计数器+1,相当于做一次retain操作
    + 本质是：没有产生新的对象

```objc
    NSString *srcStr = @"lnj";
    NSString *copyStr = [srcStr copy];
    NSLog(@"src = %p, copy = %p", srcStr, copyStr);
```

- 深复制（深拷贝，内容拷贝，deep copy）
    + 源对象和副本对象是不同的两个对象
    + 源对象引用计数器不变,副本对象计数器为1（因为是新产生的）
    + 本质是：产生了新的对象

```objc
    NSString *srcStr = @"lnj";
    NSMutableString *copyStr = [srcStr mutableCopy];
    NSLog(@"src = %p, copy = %p", srcStr, copyStr);
    NSLog(@"src = %@, copy = %@", srcStr, copyStr);
    [copyStr appendString:@" cool"];
    NSLog(@"src = %@, copy = %@", srcStr, copyStr);
```

```objc
    NSMutableString *srcStr = [NSMutableString stringWithFormat:@"lnj"];
    NSString *copyStr = [srcStr copy];
    [srcStr appendString:@" cool"];
    NSLog(@"src = %p, copy = %p", srcStr, copyStr);
    NSLog(@"src = %@, copy = %@", srcStr, copyStr);
```

```objc
    NSMutableString *srcStr = [NSMutableString stringWithFormat:@"lnj"];
    NSMutableString *copyStr = [srcStr mutableCopy];
    [srcStr appendString:@" cool"];
    [copyStr appendString:@" 520it"];
    NSLog(@"src = %p, copy = %p", srcStr, copyStr);
    NSLog(@"src = %@, copy = %@", srcStr, copyStr);
```

- 只有源对象和副本对象都不可变时，才是浅复制，其它都是深复制





<h3 id="7.28">7.28 copy与内存管理</h3>
##### 1.copy与内存管理

- 浅拷贝
    + 原对象引用计数器+1
    + 必须对原对象进行释放
```objc
    char *cstr = "this is a c string";
    NSString *str1 = [[NSString alloc] initWithUTF8String:cstr];
    NSLog(@"str = %lu", [str1 retainCount]);
    NSString *str2 = [str1 copy];
    NSLog(@"str = %lu", [str1 retainCount]);
    [str2 release];必须做一次release
```

- 深拷贝
    + 必须释放新对象
```objc
    char *cstr = "this is a c string";
    NSString *str1 = [[NSString alloc] initWithUTF8String:cstr];
    NSLog(@"str = %lu", [str1 retainCount]);
    NSMutableString *str2 = [str1 mutableCopy];
    NSLog(@"str = %lu", [str1 retainCount]);
    [str2 release]; // 必须做一次release
```

<h3 id="7.29">7.29 @property中的copy关键字</h3>
##### 1.@property中的copy的作用
- 防止外界修改内部的值

```objc
    @interface Person : NSObject
    @property (nonatomic, retain) NSString *name;
    @end
```

```objc
    NSMutableString *str = [NSMutableString stringWithFormat:@"lnj"];

    Person *p = [[Person alloc] init];
    p.name = str;
    // person中的属性会被修改
    [str appendString:@" cool"];
    NSLog(@"name = %@", p.name);
```

- 防止访问对象对象已经释放
    + 不用copy情况
```objc
    Person *p = [[Person alloc] init];
    p.name = @"lnj";
    Dog *d = [[Dog alloc] init];
    d.age = 10;
    NSLog(@"retainCount = %lu", [d retainCount]); // 1
    p.pBlock = ^{
        // 报错, 调用之前就销毁了
        NSLog(@"age = %d", d.age);
    };
    [d release]; // 0
    p.pBlock();
    [p release];
```
    + 用copy情况

```objc
    Person *p = [[Person alloc] init];
    p.name = @"lnj";
    Dog *d = [[Dog alloc] init];
    d.age = 10;
    NSLog(@"retainCount = %lu", [d retainCount]); // 1
    p.pBlock = ^{
        // 会对使用到的外界对象进行一次retain
        NSLog(@"age = %d", d.age);
        NSLog(@"retainCount = %lu", [d retainCount]); // 1
    };
    [d release]; // 1
    p.pBlock();
    [p release];
```


##### 2.@property内存管理策略选择
- 非ARC
    + 1> copy : 只用于NSString\block
    + 2> retain : 除NSString\block以外的OC对象
    + 3> assign :基本数据类型、枚举、结构体(非OC对象),当2个对象相互引用,一端用retain,一端用assign

- ARC
    + 1> copy : 只用于NSString\block
    + 2> strong : 除NSString\block以外的OC对象
    + 3> weak : 当2个对象相互引用,一端用strong,一端用weak
    + 4> assgin : 基本数据类型、枚举、结构体(非OC对象)

<h3 id="7.30">7.30 自定义的类实现copy操作</h3>
##### 1.自定义类实现copy操作
- 让类遵守NSCopying协议
- 实现 copyWithZone:方法,在该方法中返回一个对象的副本即可。
- 在copyWithZone方法中,创建一个新的对象,并设置该对象的数据与现有对象一致, 并返回该对象.
     >zone: 表示空间,分配对象是需要内存空间的,如果指定了zone,就可以指定 新建对象对应的内存空间。但是:zone是一个非常古老的技术,为了避免在堆中出现内存碎片而使用的。在今天的开发中,zone几乎可以忽略

- 无父类实现

```objc
-（id）copyWithZone(NSZone *)zone{

   CustomMode *custom = [[[self class]  copyWithZone:zone]  init];

   Custom ->_a = [_a copyWithZone:zone];

   Custom -> _c = _c;//不是对象的 直接赋值

   Return custom;

}
```
- 有父类实现
    + 不调用父类方法, 无法拷贝父类中继承的属性
    + 不重新父类copyWithZone, 无法拷贝本来中的特有属性
```objc
-（id）copyWithZone(NSZone *)zone{

    CustomModel *custom = [super copyWithZone:zone];
    ….
    Return custom;
}
```


<h3 id="7.31">7.31 单例设计模式</h3>


##### 1.单例模式概念
- 什么是单例模式:(Singleton)
    + 单例模式的意图是是的类的对象成为系统中唯一的实例,􏰀供一个访问点,供客户类 共享资源。

- 什么情况下使用单例?
    + 1、类只能有一个实例,而且必须从一个为人熟知的访问点对其进行访问,比如工厂方 法。
    + 2、这个唯一的实例只能通过子类化进行扩展,而且扩展的对象不会破坏客户端代码。

- 单例设计模式的要点:
    + 1) 某个类只能有一个实例。
    + 2)他必须自行创建这个对象
    + 3)必须自行向整个系统􏰀供这个实例;
    + 4)为了保证实例的唯一性,我们必须将
    + 5)这个方法必须是一个静态类



##### 2.简单的单例模式实现

```objc
#define interfaceSingleton(name)  +(instancetype)share##name


#if __has_feature(objc_arc)
// ARC
#define implementationSingleton(name)  \
+ (instancetype)share##name \
{ \
name *instance = [[self alloc] init]; \
return instance; \
} \
static name *_instance = nil; \
+ (instancetype)allocWithZone:(struct _NSZone *)zone \
{ \
static dispatch_once_t onceToken; \
dispatch_once(&onceToken, ^{ \
_instance = [[super allocWithZone:zone] init]; \
}); \
return _instance; \
} \
- (id)copyWithZone:(NSZone *)zone{ \
return _instance; \
} \
- (id)mutableCopyWithZone:(NSZone *)zone \
{ \
return _instance; \
}
#else
// MRC

#define implementationSingleton(name)  \
+ (instancetype)share##name \
{ \
name *instance = [[self alloc] init]; \
return instance; \
} \
static name *_instance = nil; \
+ (instancetype)allocWithZone:(struct _NSZone *)zone \
{ \
static dispatch_once_t onceToken; \
dispatch_once(&onceToken, ^{ \
_instance = [[super allocWithZone:zone] init]; \
}); \
return _instance; \
} \
- (id)copyWithZone:(NSZone *)zone{ \
return _instance; \
} \
- (id)mutableCopyWithZone:(NSZone *)zone \
{ \
return _instance; \
} \
- (oneway void)release \
{ \
} \
- (instancetype)retain \
{ \
return _instance; \
} \
- (NSUInteger)retainCount \
{ \
return  MAXFLOAT; \
}
#endif


```