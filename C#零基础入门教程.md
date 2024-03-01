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

## 13. 错误处理

## 14. 面向对象

## 15. Static

## 16. 代码抽离

## 17. 文件操作

## 18. 总结
