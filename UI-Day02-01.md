# UILabel

### 什么是UILabel

* UILabel极其常用，功能单一，用于显示文字

### UILabel的常见属性
```objc
    @property(nullable, nonatomic,copy)   NSString           *text;
    @property(null_resettable, nonatomic,strong) UIFont      *font;            
    @property(null_resettable, nonatomic,strong) UIColor     *textColor;            
    @property(nonatomic)        NSTextAlignment    textAlignment;
    @property(nonatomic) NSInteger numberOfLines;
    @property(nonatomic)        NSLineBreakMode    lineBreakMode;
```