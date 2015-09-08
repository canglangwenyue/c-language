#C 数据类型
在 C 语言中，数据类型指的是用于声明不同类型的变量或函数的一个广泛的系统。变量的类型决定了变量存储占用的空间，以及如何解释存储的位模式。
C 中的类型可分为以下几种：
![](http://ww1.sinaimg.cn/large/e0a202ffgw1evu9uv217xj21520bq0uo.jpg)

数组类型和结构类型统称为聚合类型。函数的类型指的是函数返回值的类型。在本章节接下来的部分我们将介绍基本类型，其他几种类型会在后边几个章节中进行讲解。

##整数类型
下表列出了关于标准整数类型的存储大小和值范围的细节：
![](http://ww4.sinaimg.cn/large/e0a202ffgw1evu9w7ak2tj214w0g4417.jpg)

为了得到某个类型或某个变量在特定平台上的准确大小，您可以使用 sizeof 运算符。表达式 sizeof(type) 得到对象或类型的存储字节大小。下面的实例演示了获取 int 类型的大小：
```
#include <stdio.h>
#include <limits.h>

int main()
{
   printf("Storage size for int : %d \n", sizeof(int));
   
   return 0;
} 
```

##浮点类型
下表列出了关于标准浮点类型的存储大小、值范围和精度的细节：
![](http://ww3.sinaimg.cn/large/e0a202ffgw1evua0g690tj215206kwfg.jpg)
头文件 float.h 定义了宏，在程序中可以使用这些值和其他有关实数二进制表示的细节。下面的实例将输出浮点类型占用的存储空间以及它的范围值：

```
#include <stdio.h>
#include <float.h>

int main()
{
   printf("Storage size for float : %d \n", sizeof(float));
   printf("Minimum float positive value: %E\n", FLT_MIN );
   printf("Maximum float positive value: %E\n", FLT_MAX );
   printf("Precision value: %d\n", FLT_DIG );
   
   return 0;
} 
```
##void 类型
void 类型指定没有可用的值。它通常用于以下三种情况下：
![](http://ww3.sinaimg.cn/large/e0a202ffgw1evua1wc2g9j21500au40y.jpg)