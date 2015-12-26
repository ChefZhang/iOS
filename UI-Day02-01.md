# UILabel

### 什么是UILabel

* UILabel极其常用，功能单一，用于显示文字

### UILabel的常见属性
```objc
    显示的文字
    @property(nullable, nonatomic,copy)   NSString           *text;
    字体大小
    @property(null_resettable, nonatomic,strong) UIFont      *font;     
    字体颜色
    @property(null_resettable, nonatomic,strong) UIColor     *textColor;    
    文字的对齐方式
    @property(nonatomic)        NSTextAlignment    textAlignment;
    文字行数
    @property(nonatomic) NSInteger numberOfLines;
    换行模式
    @property(nonatomic)        NSLineBreakMode    lineBreakMode;
```