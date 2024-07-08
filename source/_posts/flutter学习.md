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
# Dart

## Dart介绍

> Dart是谷歌开发的计算机编程语言，可以被用于web、服务器、移动应用 和 物联网等领域的开发
> 学Flutter必须先学Dart


## Dart环境搭建(Win10)

### Dart下载

> https://gekorm.com/dart-windows/ 下载Dart软件(无脑安装)
> 不推荐命令行下载

### 测试Dart SDK是否安装成功

> 打开cmd 输入
>> dart --version
>
>  显示 Dart SDK version: 3.4.4 (stable) (Wed Jun 12 15:54:31 2024 +0000) on "windows_x64" 安装成功


## VS Code 配置 Dart

> Dart的开发工具有：IntelliJ IDEA、WebStorm、Atom、VS Code等
> VS Code中配置Dart
>> 1、安装Dart插件
>> 2、安装Code Runner插件
>
> 新建Dart文件
>> .dart结尾，例：index.dart


## Dart 基础

### Dart 基础运行
> 
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

### Dart 入口方法 注释 变量 常量 命名规则
#### 入口方法定义
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
#### 注释方法
> 
>     /*
>       第一种注释方法
>     */
>
>     // 第二种注释方法
>
>     /// 第三种注释方法
>
#### 变量
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
#### dart命名规则
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
#### 常量
>
> **常量：final 和 const修饰符**
>
>> const 值不变，一开始就得赋值
>> final 可以开始不赋值，只能赋一次
>
> const 关键字定义常量
> 
>     const PI = 3.14159;
>     // PI = 123; // 常量不可以修改，会报错
>     print(PI);
>
> final 关键字定义常量
> 
>     final PI = 3.14159;
>     // PI = 123; // 常量不可以修改，会报错
>     print(PI);
>
> **final 和 const 的区别**
> 
>     final a = new DateTime.now();
>     print(a);
> 
>     const a = new DateTime.now(); // const 就不可以，会报错
>     print(a);
>
>> final不仅有const的编译时常量的特性，最重要的它是运行时常量
>> 并且final是惰性初始化，即在运行时第一次使用前才初始化
>> 如果是普通的常量，那么const和final都是可以的；但如果是调用方法赋值给常量，const是不可以的，要用final
>

## Dart 数据类型
>
> **常用数据类型**
>
>> **Numbers** (数值)：int double
>> **Strings** (字符串)：String
>> **Booleans** (布尔)：bool
>> **List** (数组)：在Dart中，数组是列表对象，所以大多数人只是称它们为列表
>> **Maps** (字典)：通常来说，Map是一个键值对相关的对象。键和值可以是任何类型的对象，每个键只出现一次，而一个值则可以出现多次。映射是动态集合。换句话说，Maps可以在运行时增长和缩小。dart:core库中的Map类提供了相同的支持。
>
> 项目中用不到的数据类型：
> 
>> **Runes**：Rune是UTF-32编码的字符串，它可以通过文字转换成符号表情或者代表特定的文字
>>
>>     main() {
>>      var clapping = '\u{1f44f}';
>>      print(clapping);
>>      print(clapping.codeUnits);
>>      print(clapping.runes.toList());
>>
>>      Runes input = new Runes(
>>        '\u2665 \u{1f605} \u{1f60e} \u{1f47b} \u{1f596} \u{1f44d}'
>>      );
>>      print(new String.fromCharCodes(input));
>>     }
>
>> **Symbols**：一个Symbol对象代表Dart程序中声明的操作符或者标识符。也许不会用到Symbol，但是该功能对于通过名字来引用标识符的情况是非常有价值的，特别是混淆后的代码，标识符的名字被混淆了，但是Symbol的名字不会改变。使用Symbol字面量来获取标识符的symbol对象，也就是在标识符前面添加一个 # 符号
>
### 字符串类型
>
> **字符串定义的几种方式**
>
>>     void main() {
>>    
>>      // 1、var定义
>>      var str1 = 'this is str(单引号)';
>>      var str2 = "this is str(双引号)";
>>    
>>      print(str1);
>>      print(str2);
>>    
>>      // 2、类型定义
>>      // 虽然dart中的var会判断定义的类型，但还是建议定义变量的时候指定类型
>>      String str3 = 'this is str(单引号)';
>>      String str4 = "this is str(双引号)";
>>    
>>      print(str3);
>>      print(str4);
>>    
>>      // 3、也可以通过三个成对的单引号或三个成对的双引号定义String类型
>>      // 在定义一行字符串的时候看不出区别，但是三引号可以定义多行，单引号或双引号不可以
>>      String str5 = '''
>>        this is str(三个单引号) 
>>        ddd
>>        多行
>>      ''';
>>      String str6 = """
>>        this is str(三个双引号) 
>>        ddd
>>        多行
>>      """;
>>    
>>      print(str5); // 打印出来的是三行字符串
>>      print(str6); // 打印出来的是三行字符串
>>    
>>     }
>
> **字符串的拼接**
>
>>     void main() {
>>
>>      String strA = 'Hello';
>>      String strB = 'Dart';
>>
>>      // 1、用 $ 拼接
>>      print("$strA $strB");
>>      // 2、用 + 拼接
>>      print(strA + ' ' + strB);
>> 
>>      // 都会打印出  Hello Dart
>> 
>>     }
>

### 数值类型
>
> **数值有两种类型**
>
>> int：整数类型（只能是整型）
>> double：浮点数类型（既可以是整型，也可以是浮点型）
>
> **定义数值**
> 
>>     void main() {
>>
>>       // 1、int
>>       int a = 123;
>>       // a = 23.3; // 会报错，整型不能被赋值为浮点型
>>
>>       print(a);
>>
>>       // 2、double
>>       double b = 22.33;
>>       b = 45; // 浮点型也可以被赋值为整型，不会报错 打印出：45.0
>>
>>       print(b);
>>
>>       // 3、运算符
>>       // +(加) -(减) *(乘) /(除) %(取余)
>>       var c = a + b;
>>
>>       print(c); // 打印出：168.0
>>
>>     }
>

### 布尔类型
>
>> 用 bool 声明
>> 值为 true 或 false
>
> **定义布尔值**
> 
>>     void main() {
>>
>>       // 1、bool
>>       // 赋值其他类型会报错
>>       bool flag1 = true;
>>       bool flag2 = false;
>>
>>       print(flag1);
>>       print(flag2);
>>
>>
>>       // 2、条件判断语句
>>       var flag = true;
>>
>>       if (flag) {
>>         print('真');
>>       } else { // 因为值为true，永远不会走else的判断，所以会被认为是无用代码划黄线警告。但不影响运行，问题不大
>>         print('假');
>>       }
>>
>>
>>       var a = 123;
>>       var b = 123;
>>
>>       if (a == b) { // 一个等号是赋值，两个等号是条件判断
>>         print('a=b'); // 会打印相等
>>       } else {
>>         print('a!=b');
>>       }
>> 
>>       var a1 = 123;
>>       var b2 = '123';
>> 
>>       if (a1 == b2) { // dart中的 == 不会进行类型转换，所以字符串和数值是不相等的
>>         print('a=b');
>>       } else {
>>         print('a!=b'); // 会打印不相等
>>       }
>> 
>>     }
>

### 数组类型
>
>> list 就是一系列数据的集合
>
> **定义集合/数组**
> 
>>     void main() {
>>    
>>      // 1、第一种定义List的方式
>>      var list1 = ['张三', 20, true];
>>    
>>      print(list1); // [张三, 20, true]
>>      print(list1.length); // 获取集合长度 长度为3
>>      print(list1[0]); // 获取集合第一个元素 '张三'
>>    
>>    
>>      // 2、第二种定义List的方式 指定类型
>>      var list2 = <String>["张三", "李四"]; // 只能保存字符串类型数据
>>      // var list2 = <String>[12, true]; // 保存其他类型的就会报错
>>    
>>      print(list2);
>>    
>>      // 也可以保存指定其他类型的数据，比如整型
>>      var list3 = <int>[123, 456];
>>    
>>      print(list3);
>>    
>>    
>>      // 3、第三种定义List的方式 增加数据
>>      // 通过 [] 创建的集合，它的容量是可变的
>>      var list4 = []; // 定义了一个空数组
>>    
>>      print(list4); // []
>>      print(list4.length); // 0
>>    
>>      // 给list4增加数据
>>      list4.add("张三");
>>      list4.add(12);
>>      list4.add(true);
>>    
>>      print(list4); // [张三, 12, true]
>>      print(list4.length); // 3
>>    
>>      var list5 = ['张三', 20, true];
>>      list5.add("李四");
>>      list5.add("王五");
>>    
>>      print(list5); // [张三, 20, true, 李四, 王五]
>>      print(list5.length); // 5
>>    
>>    
>>      // 4、第四种定义List的方式
>>      // var list6 = new List(); // 新版本Dart已弃用该方法，flutter2.x还可以继续用
>>      // 通过List.filled创建的集合长度是固定的
>>      // List.filled(length, fill) 两个参数：集合长度, 填充内容
>>      // 这个方式也有类型推导，list6 填充内容为空字符串就会被认为是字符串类型的集合，不能往里加其他类型
>>      var list6 = List.filled(2, ""); // 创建一个固定长度的集合，创建好后是没法往该集合里增加数据的
>>      // var list6 = List<String>.filled(2, ""); // 该写法指定类型的方式
>>    
>>      print(list6); // [, ] <—— 两个空元素
>>      print(list6.length); // 2
>>    
>>      // 修改集合内容
>>      list6[0] = "张三";
>>      list6[1] = "李四";
>>    
>>      print(list6); // [张三, 李四]
>>    
>>      // list6.add("王五"); // 会报错，因为该集合长度固定，不能往里添加数据
>>      // list6.length = 0; // 会报错，因为该集合长度固定，没办法修改集合长度
>>    
>>    
>>      var list7 = ["张三", "李四"];
>>    
>>      print(list7.length); // 2
>>    
>>      list7.length = 0; // 长度可改变
>>    
>>      print(list7); // []
>>      print(list7.length); // 0
>>    
>>     }
>

### 字典类型 (Maps)
>
> **定义字典类型**
> 
>>     void main() {
>>       // Dart中的key值必须加引号（单双都可以）
>>    
>>       // 第一种定义Maps的方式
>>       var person = {
>>        "name": "张三",
>>        "age": 20,
>>        "work": [
>>          "程序员",
>>          "外卖员"
>>        ]
>>       };
>>     
>>       print(person); // {name: 张三, age: 20, work: [程序员, 外卖员]}
>>       // Dart中访问对象中的元素不能用 person.name   要用 person["name"]
>>       print(person["name"]); // 张三
>>       print(person["work"]); // [程序员, 外卖员]
>>    
>>    
>>       // 第二种定义Maps的方式
>>       var p = new Map();
>>     
>>       p["name"] = "李四";
>>       p["age"] = 20;
>>       p["work"] = ["程序员", "外卖员"];
>>     
>>       print(p); // {name: 李四, age: 20, work: [程序员, 外卖员]}
>> 
>>     }
>

### 判断数据类型
>
>> is 关键词来判断数据类型
>
> **is关键词用法**
>
>>     void main() {
>>    
>>       var str = '1234';
>>     
>>       if (str is String) {
>>         print("是String类型"); // 是String类型
>>       } else if (str is int) {
>>         print("是int类型");
>>       } else {
>>         print("其他类型");
>>       }
>>     
>>     
>>       var str2 = 123;
>>     
>>       if (str2 is String) {
>>         print("是String类型");
>>       } else if (str2 is int) {
>>         print("是int类型"); // 是int类型
>>       } else {
>>         print("其他类型");
>>       }
>>    
>>     }
>

### 类型转换
>
>     void main() {
>     
>       // 1、Number与String类型之间的转换
>       // Number类型转换成String类型 toString()
>       // String类型转成Number类型 parse
>       
>       // 整型
>       String str = '123';
>       var myNum = int.parse(str);
>     
>       print(myNum is int); // true
>     
>       // 浮点型
>       String str1 = '123.1';
>       String str2 = '123';
>       var myNum1 = double.parse(str1);
>       var myNum2 = double.parse(str2);
>     
>       print(myNum1 is double); // true
>       print(myNum2 is double); // true  double转换整型也不会报错
>       print(myNum2); // 123.0
>     
>       // 处理转换类型报错
>       // try...catch... 抛出异常不会导致程序崩溃
>       String price = '';
>     
>       try {
>         var myNum3  = double.parse(price);
>     
>         print(myNum3);
>         print(myNum3 is double);
>       } catch(err) {
>         print(0); // 0
>       }
>     
>       var myNum4 = 12;
>       var str3 = myNum4.toString();
>     
>       print(str3 is String); // true
>     
>       print('---------------');
>     
>     
>       // 2、其他类型转换成Booleans类型
>       // isEmpty：判断字符串是否为空
>       var str4 = "";
>       
>       print(str4.isEmpty); // true
>     
>       var myNum5;
>     
>       if (myNum5 == 0) {
>         print('0');
>       } else {
>         print('非0'); // 非0  因为myNum5为null
>       }
>     
>       var myNum6 = 0 / 0;
>     
>       print(myNum6); // NaN  因为0不能作为被除数
>       print(myNum6.isNaN); // true
>     
>     }
> 

## Dart 运算符

### 算术运算符
>
>> \+(加) &nbsp;&nbsp; -(减) &nbsp;&nbsp; *(乘) &nbsp;&nbsp; /(除) &nbsp;&nbsp; %(取余) &nbsp;&nbsp; ~/(取整)
>
>     void main() {
>     
>       int a = 13;
>       int b = 5;
> 
>       print(a + b); // 18
>       print(a - b); // 8
>       print(a * b); // 65
>       print(a / b); // 2.6
>       print(a % b); // 3
>       print(a ~/ b); // 2
>
>       var c = a * b;
>       print(c); // 65
> 
>     }
> 

### 关系运算符
>
>> == &nbsp;&nbsp; != &nbsp;&nbsp; > &nbsp;&nbsp; < &nbsp;&nbsp; >= &nbsp;&nbsp; <=
>
>     void main() {
>     
>       int a = 13;
>       int b = 5;
> 
>       print(a == b); // false
>       print(a != b); // true
>       print(a > b); // true
>       print(a < b); // false
>       print(a >= b); // true
>       print(a <= b); // false
>
>       if (a > b) {
>         print('a大于b');  // a大于b
>       } else {
>         print('a小于b');
>       }
> 
>     }
>

### 逻辑运算符
>
>> !(取反) &nbsp;&nbsp; &&(并且) &nbsp;&nbsp; ||(或者)
>
>     void main() {
>     
>       //  ! 取反
>       bool flag = true;
>       print(!flag); // false
>       
>       //  && 并且：全部为true的话值为true 否则值为false
>       bool flag1 = true;
>       bool flag2 = false;
>       print(flag1 && flag2); // false
>       
>       //  || 或者：全部为false的话值为false 否则值为true
>       bool flag3 = true;
>       bool flag4 = false;
>       print(flag3 || flag4); // true
>     
>     
>       // 如果一个人的年龄是20 并且 性别是女则打印出来
>       int age = 20;
>       String sex = '女';
>     
>       if (age == 20 && sex == '女') {
>         print("$age --- $sex"); // 20 --- 女
>       } else {
>         print("不打印");
>       }
>     
>       // 如果一个人的年龄是20 或者 性别是女则打印出来
>       int age1 = 23;
>       String sex1 = '女';
>     
>       if (age1 == 20 || sex1 == '女') {
>         print("$age1 --- $sex1"); // 23 --- 女
>       } else {
>        print("不打印");
>       }
> 
>     }
>

### 赋值运算符

#### 基础赋值运算符
>
>> = &nbsp;&nbsp; ??=
>
>     void main() {
>     
>       // 基础赋值运算符：=  ??=
>       int a = 10;
>       print(a); // 10
> 
>       // b ??= 23;  表示如果b为空的话把 23 赋值给b
>     
>       // int b; // 这样会报错
>       // The non-nullable local variable 'b' must be assigned before it can be used.
>       // 因为使用int等指定类型来声明变量，b必须是int类型的数据，不能为null，否则会报错
>       // 解决办法：使用var来声明变量，即与js语法一致，可以只声明变量而不初始化
>       var b;
>       b ??= 23; 
>       print(b); // 23
>     
>       int c = 6;
>       c ??= 8;
>       print(c); // 6
>       // c不为空 所以不会被赋值为8
> 
>     }
>

#### 复合赋值运算符
>
>> += &nbsp;&nbsp; -= &nbsp;&nbsp; *= &nbsp;&nbsp; /= &nbsp;&nbsp; %= &nbsp;&nbsp; ~/=
>
>     void main() {
>     
>       // 复合赋值运算符：+=  -=  *=  /=  %=  ~/=
>       var a1 = 10;
>       a1 += 10; // 表示 a1 = a1 + 10;
>     
>       print(a1); // 20
>     
>       var a2 = 10;
>       a2 *= 10; // 表示 a2 = a2 * 10;
>     
>       print(a2); // 100
>     
>     }
> 

## Dart 条件表达式
>
>> if else
>> switch case
>> 三目运算符
>> ??运算符
>
>     void main() {
>     
>       // 1、if else    switch case
>       bool flag = true;
>     
>       if (flag) {
>         print('true');
>       } else {
>         print('false');
>       }
>     
>       // 判断一个人成绩，如果大于60显示及格；大于70显示良好；大于90显示优秀
>       var score = 80;
>     
>       if (score > 90) {
>         print('优秀');
>       } else if (score > 70) {
>         print('良好'); // 良好
>       } else if (score >= 60) {
>         print('及格');
>       } else {
>         print('不及格');
>       }
>     
>     
>       var sex = "女";
>     
>       switch (sex) {
>         case "男":
>           print("性别为男");
>           break;
>         case "女":
>           print("性别为女"); // 性别为女
>           break;
>         default:
>           print("传入参数错误");
>           break;
>       }
>     
>     
>       // 2、三目运算符
>       // var flag1 = true;
>       // var c;
>     
>       // if (flag1) {
>       //   c = "我是true";
>       // } else {
>       //   c = "我是false";
>       // }
>       // print(c);
>     
>       // 用三目方式写
>       bool flag1 = true;
>       String c = flag1 ? "我是true" : "我是false";
>     
>       print(c); // 我是true
>     
>     
>       // 3、??运算符
>       var a;
>       var b = a ?? 10;
>     
>       print(b); // 10
>     
>       var a1 = 22;
>       var b1 = a1 ?? 10;
>     
>       print(b1); // 22
>     
>     }
>

## Dart 循环语句

### 自增 自减运算符
>
>> \++ &nbsp;&nbsp;&nbsp; \--  
>
>     void main() {
>     
>       /* 
>         ++ --   表示自增 自减 1
>     
>         在赋值运算里，如果 ++ -- 写前面  这时候先运算后赋值；
>         如果 ++ -- 写后面  这时候先赋值后运算
>
>         赋值运算才有这个区别，否则没区别
>       */
>     
>       // ++ --
>       var a = 10;
>       a++; // 等同于 a = a + 1;
>     
>       print(a); // 11
>     
>       var b = 10;
>       b--; // 等同于 b = b - 1;
>     
>       print(b); // 9
>     
>       // 先赋值再运算
>       var a1 = 10;
>       var b1 = a1++;
>     
>       print(a1); // 11
>       print(b1); // 10
>     
>        // 先运算再赋值
>       var a2 = 10;
>       var b2 = ++a2;
>     
>       print(a2); // 11
>       print(b2); // 11
>
>       print('-------------');
>     
>       // 不赋值运算 单纯自增自减
>       var a3 = 10;
>       a3++;
>     
>       print(a3); // 11
>       
>       var a4 = 10;
>       ++a4;
>     
>       print(a4); // 11
>     
>     }
>

### for循环 循环遍历List
>
>     /*
>       for 基本语法
>       for (int i = 1; i <= 100; i++) {
>         print(i);
>       }
>     
>       第一步：声明变量 int i = 1;
>       第二步：判断 i <= 100;
>       第三步：print(i);
>       第四步：i++;
>       第五步：从第二步再来，直到判断为false
>      */
>     
>     void main() {
>     
>       // 基础语法
>       for (int i = 1; i <= 10; i++) {
>         print(i);
>       }
>     
>     
>       // 1、打印 0-50 所有的偶数
>       for (int i = 0; i <= 50; i++) {
>         if (i % 2 == 0) {
>           print(i);
>         }
>       }
>     
>       print('----------------');
>     
>     
>       // 2、求 1+2+3+4+……+100 的和
>       var sum = 0;
>       for (int i = 0; i <= 100; i++) {
>         sum += i;
>       }
>     
>       print(sum); // 5050
>     
>       print('----------------');
>     
>     
>       // 3、计算5的阶乘  (1*2*3*4*5  n的阶乘 1*2……*n)
>       var pro = 1;
>       for (int i = 1; i <= 5; i++) {
>         pro *= i;
>       }
>     
>       print(pro); // 120
>     
>       print('----------------');
>     
>     
>       // 4、打印List ['张三', '李四', '王五'] 里面的内容
>       List l1 = ['张三', '李四', '王五'];
>       for (int i = 0; i < l1.length; i++) {
>         print(l1[i]);
>       }
>     
>       print('----------------');
>     
>     
>       // 5、打印复杂list内容
>       List l2 = [
>         {
>           "title": "111",
>         },
>         {
>           "title": "222",
>         },
>         {
>           "title": "333",
>         },
>       ];
>       for (int i = 0; i < l2.length; i++) {
>         print(l2[i]['title']);
>       }
>     
>       print('----------------');
>     
>     
>       // 6、定义一个二维数组 打印里面内容
>       List l3 = [
>         {
>           "cate": "国内",
>           "news": [
>             {
>               "title": "111",
>             },
>             {
>               "title": "222",
>             },
>             {
>               "title": "333",
>             },
>           ]
>         },
>         {
>           "cate": "国际",
>           "news": [
>             {
>               "title": "444",
>             },
>             {
>               "title": "555",
>             },
>             {
>               "title": "666",
>             },
>           ]
>         },
>       ];
>       for (int i = 0; i < l3.length; i++) {
>         print(l3[i]['cate']);
>         for (int j = 0; j < l3[i]['news'].length; j++) {
>           print(l3[i]['news'][j]['title']);
>         }
>       }
>     
>     }
>

### while do...while循环
>
>     /*
>       语法格式：
>         while(表达式/循环条件) {
>         }
>     
>         do{
>           语句/循环体
>         } while(表达式/循环条件);
>       
>       注意：
>         1、最后的分号不要忘记
>         2、循环条件中使用的变量需要经过初始化
>         3、循环体中，应有结束循环的条件，否则会造成死循环
>     */
>     
>     void main() {
>     
>       // 1、打印 1-10
>       int i = 1;
>       while(i <= 10) {
>         print(i);
>         i++; // 不增加 i 会进入死循环
>       }
>     
>       print('-----------');
>     
>     
>       // 2、求 1+2+3+4+……+100 的和
>       var sum = 0;
>       int i1 = 1;
>       while(i1 <= 100) {
>         sum += i1;
>         i1++;
>       }
>       print(sum); // 5050
>     
>       sum = 0;
>       i1 = 1;
>       do {
>         sum += i1;
>         i1++;
>       } while(i1 <= 100);  // do...while 居然是 do 在上面？！好吧我也没怎么用过这个:)
>       print(sum); // 5050
>     
>       print('-----------');
>     
>     
>       // while 和 do...while 的区别  第一次循环条件不成立的情况下
>       int i2 = 10;
>       while(i2 < 2) {
>         print('执行代码'); // 不符合条件所以不会执行
>       }
>     
>       int j2 = 10;
>       do {
>         print('执行代码'); // 执行代码 (无论满不满足条件会先执行一次)
>       } while(j2 < 2);
>     
>     }
> 

### break 和 continue
>
>     /*
>       break 语句功能：
>         1、在 switch 语句中使流程跳出 switch 结构
>         2、在循环语句中使流程跳出当前循环，遇到 break 循环停止，后面代码也不会执行
>     
>       强调：
>         1、如果在循环中已经执行了 break 语句，就不会执行循环体中位于 break 后的语句
>         2、在多层循环中，一个 break 语句只能向外跳出一层
>     
>       break 可以用在 switch case 中，亦可以用在 for 循环和 while 循环中
>     
>     
>       continue 语句功能：
>         【注】只能在循环语句中使用，使本次循环结束，即跳过循环体中continue下面尚未执行的语句，接着进行下次是否执行循环的判断
>         continue 可以用在 for 循环以及 while 循环中，但是不建议用在 while 循环中，不小心容易死循环
>     */
>     
>     void main() {
>     
>       // 1、打印 1-10  如果值为4时跳过
>       for (int i = 1; i <= 10; i++) {
>         if (i == 4) {
>           continue; // 跳过当前循环体 然后循环还会继续执行
>         }
>         print(i);
>       }
>     
>       print('-----------');
>     
>     
>       // 2、打印 1-10  如果值为4时跳出循环
>       for (int i = 1; i <= 10; i++) {
>         if (i == 4) {
>           break; // 跳出循环体
>         }
>         print(i);
>       }
>     
>       print('-----------');
>       
>     
>       // 3、break语句只能向外跳出一层循环
>       for (int i = 1; i <= 10; i++) {
>         print('外层---$i');
>         for (int j = 1; j <= 10; j++) {
>           if (j == 2) {
>             break; // 跳出循环体
>           }
>           print('里层$j');
>         }
>       }
>     
>       print('-----------');
>     
>     
>       // 4、break语句只能向外跳出一层循环 (while 版)
>       int i = 1;
>       while (i <= 10) {
>         if (i == 4) {
>           break;
>         }
>         print(i);
>         i++;
>       }
>     
>       print('-----------');
>     
>     
>       // 5、break语句只能向外跳出一层循环 (swicth 版)
>       var sex = '男';
>       switch (sex) {
>         case '男':
>           print('男');
>           break;
>         case '女':
>           print('女');
>           break;
>         default:
>       }
>     
>       print('-----------');
>     
>     }
> 
