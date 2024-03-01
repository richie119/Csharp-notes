B站 丑萌气质狗
======

## 1 入门简介
C++ 编译器 ->机器指令 ->bin-Debug-exe文件

C# 编译器 ->IL中间语言 ->  .NET里的CLR动态转换为机器指令

提升开发效率，但性能不如C++极致

.NET

.NET Framework 1.0,2.0,3.0,4.8

but 只能windows 不能mac unix/linux

爱好者自己搞**MONO**->微软亡羊补牢 **.NEt CORE ** 5.0 兼容

    e.g. Unity MONO使游戏运营其他平台 -> 现在也支持.NET Core

## 2. 代码编译

## 3. 开发工具 VS2022

## 4. 注释

## 5. 代码结构

## 6. 变量

## 7. 运算

## 8. 输入输出

## 9. if判断

## 10. for循环
```
using System;
using System.Collections.Generic;
using System.Globalization;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HelloWorldCS
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Hero hero = new Hero();
            bool flag = true;

            for(;flag ; )
            {
                Console.WriteLine("please input your age:");
                string str = Console.ReadLine();
                try
                {
                    hero.age = int.Parse(str) + 20;  //int.parse()
                    flag= false;
          
                }
                catch
                {
                    Console.WriteLine("请输入正确数字");
                }

            }
            Console.WriteLine("20年后你的年龄是" + hero.age.ToString());

            Console.WriteLine("please input your name:");
            string str2 = Console.ReadLine();
            hero.name = str2 + 250.ToString(); // toString()
            Console.WriteLine("你的名字是：" + hero.name);

            Console.ReadKey(); // 读取下一个键，其实算暂停

        }


        
    }


    class Hero
    {
        public int id;
        public string name;
        public int age;
    }
}

```
## 11. 方法

## 12. 调试
**F5 F10 F11**

## 13. 错误处理
try{

}
catch{

}

## 14. 面向对象

## 15. Static

## 16. 代码抽离
**新建类库**->可以给.NET core framework用->build会生成.dll文件(右键属性可以改BUILD生成类型)

class必须是public

想要引用的话 add reference， 然后using...就行了
```
.dll 文件指的是动态链接库（Dynamic Link Library）文件。
这些文件包含可被程序在运行时调用的代码和数据。 它们是Windows操作系统中重要的组成部分，允许程序共享资源，提高效率并降低重复编码的需要。
.dll 文件允许程序模块化，以便多个应用程序可以共享它们，这样便于维护和更新
```
注意：引用.dll之后，单独exe就不能直接打开用了；必须配上dll

**.dll的集合平台--NuGet**


## 17. 文件操作
```
using System;
using System.IO;

namespace changeFiles
{
    internal class Program
    {
        static void Main(string[] args)
        {

            String path = @"D:\SENECA\semester 5 winter24\APD545 NAA Mahboob Ali马布·阿里\APD Workshops";

            //第一种方法
            var files = Directory.GetFiles(path, "*.txt"); //返回一个数组

            foreach (var file in files)
                Console.WriteLine(file);

            //第二种方法
            DirectoryInfo folder = new DirectoryInfo(path);

            foreach (FileInfo file in folder.GetFiles("*.txt"))
            {
                Console.WriteLine(file.FullName);
            }

            Console.ReadKey();
        }
    }
}

```

## 18. 总结
多看微软技术文档

创建窗体应用 https://learn.microsoft.com/zh-cn/visualstudio/ide/create-csharp-winform-visual-studio?view=vs-2022

数据注释最初作为System. ComponentModel. DataAnnotations命名空间的一部分而引入到.NET 3.5中。此后，它已成为.NET中一种广泛使用的功能。你可以充分利用数据注释在单单一处定义数据验证规则，因而没必要一再重写同样的验证代码
