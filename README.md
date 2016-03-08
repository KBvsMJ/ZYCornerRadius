# ZYCornerRadius
A Category to make cornerRadius for UIImageView have no Offscreen-Rendered, be more efficiency  

![](https://img.shields.io/badge/pod-v0.3.1-blue.svg)
![](https://img.shields.io/badge/build-passing-brightgreen.svg)
![](https://img.shields.io/badge/license-MIT-brightgreen.svg)  




<br>
##CocoaPods:  
```
pod 'ZYCornerRadius', '~> 0.3.1'
``` 

<br>
##Usage:  
>ZYCornerRadius提供两种使用方式  

**Category方式：**  
导入头文件  
```objc
#import "UIImageView+CornerRadius.h"
```
创建圆角半径为6的UIImageView(三种方式)：  
```objc
//1
UIImageView *imageView = [UIImageView zy_cornerRadiusAdvance:6.0f rectCornerType:UIRectCornerAllCorners];
imageView.image = [UIImage imageNamed:@"mac_dog"];

//2
UIImageView *imageView = [[UIImageView alloc] initWithCornerRadiusAdvance:6.0f rectCornerType:UIRectCornerAllCorners];
imageView.image = [UIImage imageNamed:@"mac_dog"];

//3
UIImageView *imageView = [[UIImageView alloc] init];
[imageView zy_cornerRadiusAdvance:6.0f rectCornerType:UIRectCornerAllCorners];
imageView.image = [UIImage imageNamed:@"mac_dog"];
```
创建圆形的UIImageView(三种方式)：  
```objc
//1
UIImageView *imageView = [UIImageView zy_roundingRectImageView];
imageView.image = [UIImage imageNamed:@"mac_dog"];

//2
UIImageView *imageView = [[UIImageView alloc] initWithRoundingRectImageView];
imageView.image = [UIImage imageNamed:@"mac_dog"];

//3
UIImageView *imageView = [[UIImageView alloc] init];
[imageView zy_cornerRadiusRoundingRect];
imageView.image = [UIImage imageNamed:@"mac_dog"];
```  
**子类ZYImageView方式同理：**  
导入头文件  
```objc
#import "ZYImageView.h"
```
使用方式同理  



<br>
##以下列出ZYCornerRadius所开放的主要的func:  
配置一个圆角UIImageView，传入圆角半径和圆角类型  
```objc
+ (UIImageView *)zy_cornerRadiusAdvance:(CGFloat)cornerRadius rectCornerType:(UIRectCorner)rectCornerType;
- (instancetype)initWithCornerRadiusAdvance:(CGFloat)cornerRadius rectCornerType:(UIRectCorner)rectCornerType;
```  
配置一个圆形的UIImageView  
```objc
+ (UIImageView *)zy_roundingRectImageView;
- (instancetype)initWithRoundingRectImageView;
```  
直接为UIImageView设置圆角图片，传入UIImage，圆角半径和圆角类型，当次有效  
```objc
- (void)zy_cornerRadiusWithImage:(UIImage *)image cornerRadius:(CGFloat)cornerRadius rectCornerType:(UIRectCorner)rectCornerType;
```  



<br>
##Relation:  
[@liuzhiyi1992](https://github.com/liuzhiyi1992) on Github  

<br>
##License:  
ZYCornerRadius is released under the MIT license. See LICENSE for details.
