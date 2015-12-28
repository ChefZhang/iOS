# 6.第一个OC类

### 本节知识点
1. 如何声明一个类
2. 如何实现一个类
3. 如何创建一个对象
4. 对象的注意点

***
### 1.如何声明一个类
* 格式



插入图片

* 注意：
    * 1.必须以@interface开头，@end结尾
    * 2.成员变量的声明，必须写在@interface与@end之间的大括号中
    * 3.方法的声明必须在{}下面，不能写在{}中



### 2.如何实现一个类
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


### 3.如何创建一个对象
* 用类的方式告诉计算机，我们需要一个什么样的对象，之后我们要在程序中使用这个对象，就必须先创建一个对象
