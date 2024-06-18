---
title: flutter学习
date: 2024-06-15 16:32:30
tags:
- 博客
- 菜鸟学习
- flutter
- dart
categories: 又要学新技术😇
---
## Dart

### Dart介绍

> Dart是谷歌开发的计算机编程语言，可以被用于web、服务器、移动应用 和 物联网等领域的开发
> 学Flutter必须先学Dart


### Dart环境搭建(Win10)

#### Dart下载

> https://gekorm.com/dart-windows/ 下载Dart软件(无脑安装)
> 不推荐命令行下载

#### 测试Dart SDK是否安装成功

> 打开cmd 输入
>> dart --version
>
>  显示 Dart SDK version: 3.4.4 (stable) (Wed Jun 12 15:54:31 2024 +0000) on "windows_x64" 安装成功


### VS Code 配置 Dart

> Dart的开发工具有：IntelliJ IDEA、WebStorm、Atom、VS Code等
> VS Code中配置Dart
>> 1、安装Dart插件
>> 2、安装Code Runner插件
>
> 新建Dart文件
>> .dart结尾，例：index.dart


### Dart 语法

#### Dart 基础运行
> Dart要执行的东西都放在入口方法里
>
>     // 第一种定义方法
>     main() {
>       print('Hello Dart'); // 每句话后面要加分号，里面内容双引号单引号都可以
>     }
> 
> 保存文件，右键 Run Code 运行，输出：
> 
>     [Running] dart "d:\Dart_Demo\demo001\index.dart"
>     Hello Dart
>     Hello Dart1
>
>     [Done] exited with code=0 in 0.338 seconds
> 
> 输出以上内容代表SDK和VS Code配置搞定
> 如果输出乱码，重启电脑解决（重启大法好😎）

#### Dart 入口方法 注释 变量 常量 命名规则
> **入口方法定义**
> 
>     // 第一种定义方法
>     main() {
>       print('Hello Dart');
>     }
>
>     // 第二种定义方法
>     void main() {
>       // 表示main方法没有返回值
>       // void的意思就是没有返回值
>       print('Hello Dart');
>     }
>
>     // typescript里的方法定义
>     function setData():void {
>       // 让这个方法没有返回值
>     }
>
> **注释方法**
> 
>     /*
>       第一种注释方法
>     */
>
>     // 第二种注释方法
>
>     /// 第三种注释方法
>
> **变量**
>
> dart是一个强大的脚本类语言，可以不预先定义变量类型，自动会类型推导
> dart中定义变量可以通过var关键字，或者可以通过类型来申明变量，如：
> 
>     var str = 'this is var';
>     String str = 'this is var';
>     int str = 123;
>
> 注意：var和类型不要同时用，如果 var a int = 5; 会报错
>
> 两者区别就在于var会自己推断变量类型，如果赋的值与其推断类型不一致则会报错
>
>     var str = ''; // 会推断为字符串类型
>     str = 123; // 赋值数字类型
>     print(str); // 会报错，提示类型不一致
>
>     String str = 123; // 这样也不可以，赋值要与定义类型一致
>
> **dart命名规则**
>
>> 1、变量名称必须由数字、字母、下划线和美元符($)组成
>> 2、注意：标识符开头不能是数字
>> 3、标识符不能是保留字和关键字
>> 4、变量的名字是区分大小写的，如：age和Age是不同的变量，在实际的运用中也建议不要用一个
>> 5、标识符(变量名称)一定要见名思意：变量名称建议用名词，方法名称建议用动词
>
>> **关键字及保留字**
>> abstract：用于创建抽象类和抽象方法。
>> as：用于类型转换。
>> assert：用于在条件不满足时抛出异常。
>> async：用于标记异步操作。
>> await：用于暂停异步函数，直到等待的非阻塞操作完成。
>> break：用于退出循环。
>> case：用在switch语句中。
>> catch：用于捕获异常。
>> class：用于定义类。
>> const：用于创建常量。
>> continue：用于继续循环。
>> default：默认情况，通常在switch语句中使用。
>> deferred：用于延迟加载库。
>> do：用于do-while循环。
>> dynamic：用于声明动态类型。
>> else：用在条件语句中。
>> enum：用于创建枚举。
>> export：用于导出库。
>> extends：用于继承类。
>> false：布尔类型的值，表示假。
>> final：用于声明一个不可变变量。
>> finally：用于try-catch语句中，无论是否抛出异常都会执行的代码块。
>> for：用于for循环。
>> Function：用于声明函数类型。
>> get：用于获取类的实例变量。
>> hide：用于在导入库时隐藏某些标识符。
>> if：用于条件语句。
>> implements：用于实现接口。
>> import：用于导入库。
>> in：用于判断值是否在集合中。
>> inout：用于标记函数参数是否可以被修改。
>> interface：用于声明接口。
>> is：用于检查对象类型。
>> library：用于声明库。
>> mixin：用于混入。
>> native：用于调用原生代码。
>> new：用于创建对象。
>> null：表示空值。
>> on：用于指定类实现接口。
>> operator：用于重载操作符。
>> out：用于标记函数参数是否可以被修改。
>> part：用于声明部分库。
>> rethrow：用于再次抛出捕获的异常。
>> return：用于从函数返回值。
>> set：用于设置类的实例变量。
>> static：用于声明静态成员。
>> super：用于访问父类的成员。
>> switch：用于switch语句。
>> sync：用于标记同步操作。
>> this：用于表示当前实例。
>> throw：用于抛出异常。
>> true：布尔类型的值，表示真。
>> try：用于try-catch语句。
>> typedef：用于声明
>