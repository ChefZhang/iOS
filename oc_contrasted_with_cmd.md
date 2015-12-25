## 1.OC和C对比

### 本节知识点
1. 源文件对比
2. 关键字对比
3. 数据类型对比
4. 流程控制语句对比
5. 函数（方法）定义和声明对比
6. 面向对象新增特性
7. 面向对象新增语法
8. 新增异常处理
***
#### 1.源文件对比
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
***

#### 2.关键字对比
* C语言的关键字逗可以在OC源程序中使用
* OC新增的关键字在使用时，主意部分关键字以"@"开头
  
  例如
```objc
    @interface @implementation @end
       @public @protected @private @selector
       @protocol @optional @required 等
       ```
       
***        
#### 3.数据类型对比
* C语言数据类型

![](file:///Users/John/Desktop/markdown_picture/1.png =490x)

* OC数据类型

![](file:///Users/John/Desktop/markdown_picture/oc数据类型2.png =490x)

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

*** 	
#### 4.流程控制语句对比
* C语言中使用的流程控制语句OC中都可以应用

```
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

```
for (int i = 0; i < 10; i++){
	printf("%d", i);
}
```
*OC增强for循环

```
for (NSString *name in NSArray){
	NSLog(@"%@", name);
}
```
***

#### 5.方法（函数）定义和声明对比
* C语言中函数的声明和实现
	* 函数声明: int sum(int a, int b);
	* 函数实现: int sum(int a, int b){return a+b;}
* OC中的方法
	* 方法声明： -(int)sum:(int)a andB:(int)b;
	* 方法实现： -(int)sum:(int)a andB:(int)b{return a+b;}

* 注意：方法只能卸载类里面，而函数可以卸载任何地方
	* 对象方法，使用对象调用的方法
	* 类方法，使用类名调用的方法
	

	
```
对象方法
- (id)initWithString:(NSString *)name;
类方法
+ (MyClass *)createMyClassWithString:(NSString *)name;
```	 

***
#### 6.面向对象特性
* 封装性
* 继承性
* 多态性
![](file:/Users/John/Desktop/笔记图片/mxdx.png =490x)

***
#### 7.面向对象新增语法
* 属性生成器
	* @property
	* @synthesize
	
```
// 声明属性
@property (nonatomic, strong)NSString *name;

// 合成属性
@synthesize name = _name;
```

* 分类
	* 分类与继承
	* 使用分类扩展类，无需子类化
	
```
@interface NSString (MyNSString)
- (NSString *) encrypWithMD5;
@end
```	
* 协议
	* 使用协议声明方法
	* 协议类似于C#,java中的接口
```
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
	
#### 8.新增异常处理
* 用于处理错误信息
* 格式：
	* @try ... @catch ... @finally
* 示例

```
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
***
***



## 2.第一个OC程序
***
### 本节知识点
1. 如何创建Objective-C项目
2. \#import和#include区别
3. NSLog和printf区别
4. "@"的使用方法  
5. NS前缀

***
#### 1.如何创建Objective-C项目
* 创建工程
![](file:/Users/John/Desktop/笔记图片/Snip20150512_3.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20150512_4.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20151225_22.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20151225_23.png =490x)

***
#### 2.\#import和#include区别
* \#import和#include的类似，都是把其后面的文件拷贝到该指令所在的地方
* \#import可以自动防止重复导入
* \#import<>用于包含系统文件
* \#import""用于包含本项目中的文件
* \#import告诉编译器找到并处理名为Foundation.h的文件，这是一个系统文件，\#import表示将该文件的信息导入到程序中。
* 框架地址：/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneO S.sdk/System/Library/Frameworks/

***
#### 3.NSLog和printf区别
* NSLog是Foundation框架􏰀供的Objective-C日志输出函数,与标准C中的printf函数类似,并可以格式化输出。

	* NSLog传递进去的格式化字符是NSString的对象,而不是char *这种字符串指针
	* NSLog输出的内容中会自动包含一些系统信息
	* NSLog输出的内容会自动换行
* NSLog声明在NSObjCRuntime.h中
	* 声明：void NSLog(NSString *format, ...);
	
```
NSLog(@“this is a test”); //打印一个字符串
NSString *str = @"hello xiaomage!”;
NSLog(@"string is:%@",str);//使用占位符,%@表示打印一个对象,%@ OC特有的
NSLog(@"x=%d, y=%d",10,20);//使用多个占位符,%d表示整型数
```
***
#### 4."@"的使用方法
* 在OC中"@"有特殊的用法
	* "@"这个符号表示将一个C的字符串转化为OC中的字符串对象NSString
	* OC中大部分的关键字都是以@开头的，比如@interface, @implemention, @end等
***
#### 	5.NS前缀 
* NS来自于NeXTStep的一个软件 NeXT Software
* OC中不支持命名空间(namespace)
* NS是为了避免命名冲突而给的前缀
* 看到NS前缀就知道是Cocoa中的系统类的名称

***
***
## 3.面向对象思想
***
### 本节知识点
1. 面向对象基本概念
2. 面向对象和面向过程区别
3. 面向对象的特点
***
#### 1.面向对象基本概念
* 面向对象(Object Oriented,OO)是软件开发方法
* 面向对象是一种对现实世界理解和抽象的方法，是计算机编程技术发展到一定阶段后的产物。
* Object Oriented Programming-OOP ——面向对象编程

#### 2.面向对象和面向过程区别
* 面向对象是相对面想过程而言
* 面向对象和面向过程都是一种思想
* 面向过程
	* 强调的是功能行为
	* 关注的是解决问题需要哪些步骤
* 面向对象
	* 将功能进行封装，强调具备功能的对象
	* 关注的是解决问题需要哪些对象
	
#### 3.面向对象的特点
* 可以将复杂的事情简单化
* 将程序员从执行者转化为指挥者
* 完成需求时：
	* 先要去找具有所需的功能的对象来用
	* 如果该对象不存在，那么创建一个具有所需功能的对象
	* 这样简化开发并提高复用
	
***
## 类与对象	
