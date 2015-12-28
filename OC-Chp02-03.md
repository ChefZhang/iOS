# 3.对象和方法之间的关系

## 本小节知识点:

* 【掌握】对象作为方法的参数
* 【掌握】对象作为方法的返回值

***

### 1.对象作为方法的参数

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

### 2.对象作为方法的返回值
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