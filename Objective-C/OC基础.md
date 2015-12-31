# Objective-C学习

这篇文章是自己学习Objective-C的笔记，希望这篇文章能够帮助一些没有Objective-C经验的童鞋更快的学习。

目录：




<h2 id="1">1.OC简介</h2>
### 1.OC和C对比

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


### 2.第一个OC程序
##### 1.如何创建Objective-C项目
* 创建工程
![创建工程1.png](http://upload-images.jianshu.io/upload_images/328309-19783f412de47ef2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程2.png](http://upload-images.jianshu.io/upload_images/328309-26067fdfc6d9955e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程3.png](http://upload-images.jianshu.io/upload_images/328309-654ae5603146c91f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![创建工程4.png](http://upload-images.jianshu.io/upload_images/328309-3a152b8f5f433692.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

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

### 3.面向对象思维
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
	
### 4.类与对象
##### 1.类与对象的关系
* 面向对象的核心就是对象,那怎么创建对象?
    * OC中创建对象比较复杂, 首先要理解一个概念叫做类.
    * 现实生活中是根据一份描述,一份模板创建对象,编程语言也一样,也必须先有一份描述,在这个描述中说清楚将来创建出来的对象有哪些属性和行为
* OC中的类相当于图纸，用来描述一类事物。也就是说，要想创建对象必须先有类
* OC利用类来创建对象，对象是类的具体存在, 因此面向对象解决问题应该是先考虑需要设计哪些类，再利用类创建多少个对象


### 5.类的设计
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


### 6.第一个OC类
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

### 7.对象方法的声明和实现
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

### 8.类方法的声明和实现
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


### 9.对象的存储细节
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

### 10.函数与方法对比
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
    
### 11.常见错误
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



	