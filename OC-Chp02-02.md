# 2.结构体成员变量

## 本节知识点:

* 【掌握】结构体成员变量

### 1.结构体成员变量

* 设计一个”学生“类 1> 属性
    * 姓名
    * 生日
    * 用结构体作为类的实例变量(生日)

```objc
#import <Foundation/Foundation.h> //定义生日的结构体
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