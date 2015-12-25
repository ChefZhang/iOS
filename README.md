# My Awesome Book

This file serves as your book's preface, a great place to describe your book's content and ideas.

```objc
NSString *str = @"江哥";
BOOL flag = [str writeToFile:@"/Users/LNJ/Desktop/lnj.txt" atomically:YES encoding:NSUTF8StringEncoding error:nil];
if (flag == 1)
{
    NSLog(@"写入成功");
}
```

```objc
	NSString : 字符串
	NSArray : 数组
	NSDictionary : 字典
	NSDate : 日期
	NSData : 数据
	NSNumber : 数字
```



Here's a quiz about Gitbook

|                  | Good | Bad |
| ---------------- | ---- | --- |
| What is Gitbook? | (x)  | ( ) |

> Gitbook is good

What does Gitbook support?
- [x] Table-based questions with radio buttons
- [x] Table-based questions with checkboxes
- [ ] Telepathy
- [x] List-based questions with checkboxes
- [x] List-based questions with radio buttons
- [ ] Moon-on-a-stick

> Gitbook supports table and list based quiz questions using either radio buttons or checkboxes.
>
> Gitbook is not telepathic and does not give you the moon on a stick.

---


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