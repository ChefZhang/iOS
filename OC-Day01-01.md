# 1.OC和C对比

## 本节知识点
1. 源文件对比
2. 关键字对比
3. 数据类型对比
4. 流程控制语句对比
5. 函数（方法）定义和声明对比
6. 面向对象新增特性
7. 面向对象新增语法
8. 新增异常处理
***

### 1.源文件对比
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

### 2.关键字对比
* C语言的关键字逗可以在OC源程序中使用
* OC新增的关键字在使用时，主意部分关键字以"@"开头
  
  例如
```objc
    @interface @implementation @end
    @public @protected @private @selector
    @protocol @optional @required 等
```
       
***        
### 3.数据类型对比
* C语言数据类型

![](file:/Users/John/Desktop/图片笔记/c数据类型.png)

* OC数据类型

![](file:/Users/John/Desktop/图片笔记/oc数据类型2.png )

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
### 4.流程控制语句对比
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
*OC增强for循环

```objc
for (NSString *name in NSArray){
	NSLog(@"%@", name);
}
```
***

### 5.方法（函数）定义和声明对比
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

***
### 6.面向对象特性
* 封装性
* 继承性
* 多态性

![](file:/Users/John/Desktop/图片笔记/mxdx.png)

***
### 7.面向对象新增语法
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
	
#### 8.新增异常处理
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




