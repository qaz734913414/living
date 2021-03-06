# 小朋友学C++
[参考](https://blog.csdn.net/haishu_zheng/article/details/80605431)

[c语言基础 啊哈C语言 书籍](https://github.com/zxysilent/books/blob/master/%E5%95%8A%E5%93%88C%E8%AF%AD%E8%A8%80%E4%B9%A6.pdf)

[算法图解-python.pdf](https://github.com/zxysilent/books/blob/master/%E7%AE%97%E6%B3%95%E5%9B%BE%E8%A7%A3-python.pdf)

[c语言教程](https://github.com/Ewenwan/ShiYanLou/tree/master/learn_c)

[在线C++/C/python编译器](https://c.runoob.com/compile/12)

# C语言基础==========================

[C语言实验指导与习题解答](https://github.com/Baisha-Geek/Curriculum-Design/tree/master/c-programing-homework/%E3%80%8AC%E8%AF%AD%E8%A8%80%E5%AE%9E%E9%AA%8C%E6%8C%87%E5%AF%BC%E4%B8%8E%E4%B9%A0%E9%A2%98%E8%A7%A3%E7%AD%94%E3%80%8B%E7%9A%84%E7%A8%8B%E5%BA%8F)

[小项目学习 扫雷小游戏 贪吃蛇小游戏 学生成绩管理系统 图书管理系统 小说分析软件](https://github.com/Ewenwan/Curriculum-Design)

# 第一章，与 计算机小朋友开始沟通
    欧拉同学---素数----2147483647---17221----数学英雄---
              素数-----只能被1和其本身整除的数
    八皇后问题---8x8国际象棋---八个皇后---92种解
    数独---9x9大宫格----
    哥德巴赫猜想----
    以上计算机都可以在很短时间内完成计算。
    
    我们需要与计算机进行沟通，来让计算机小朋友为我们做事情
    人与人之间的沟通，可以用肢体语言、汉语、英语、法语和德语等等。
    我们学习的C语言就是与计算机沟通的一种语言，其他还有C++, python等。
    
    小宝宝刚刚来到世上，开口说的第一句话是什么?爸爸？妈妈？哇哇哇大哭？
    
    计算机要把它想说的话告诉人类，可以有两种方法，
       一种是 显示在显示器屏幕上(就像人类写信一样，写在纸上)，
       另外一种是 通过 喇叭(音箱) 发出声音(就像人类说话一样，用嘴巴说)。
    显示在屏幕上比较简单。
    
```c

printf("wa wa wa wa");
// printf 打印 和说一样，后面的()是不是想一个嘴巴
// 只要把想说的内容，放在这个嘴巴里，用双引号包围起来。

// 让计算机说你好
printf("ni hao");

// 仅仅写一句 printf("ni hao"); 计算机是识别不了的，需要加一个框架

#include <stdio.h>  // 是一个头文件。代表stantard input & output。 标准输入输出
#include <stdlib.h> // 代表stantard library 标准库
int main() // main是函数名称，int代表整形，该函数范围 int类型
{ // 大括号之间，是函数体。
    /* 我的第一个 C 程序 */
    printf("ni hao"); // 其他的都是 框架 
    // printf()函数的声明在stdio.h中，printf()函数的定义在stdio.c中。
    // printf("ni\nhao"); // 中间换一行打印
    sleep(5000);// 暂停5秒,5000毫秒
    return 0;
    // return 0;是main()函数的返回值，main()函数是特殊的函数，只调用别人，不会被别人调用。
    // 所以返回多少无关紧要，比如还可以return 1; 或return 100;
}

// 要运行以上程序，还需要将上述源程序 编译成 可执行文件
// 总结： 
// 第一次接触程序，上面有些东西，估计不会一下子全明白过来。但是不要紧，只要能明白一半就行。
// 本节课主要是看一下程序长什么模样，运行结果长什么模样。有不明白的地方，以后会陆陆续.



// 打印 小星星
*
**
***
// 2
 *
* *
* *
 *


// 带点颜色====
    system("color 5"); // 颜色 5，代表紫色，黑底，紫色字体
    // system("color f5"); // 两位数，第一位代表背景颜色 f代表被色 第二位 字体颜色，5代表黑色
    // 颜色范围 0、1、2、3,...,f 共16种
    printf("ni hao");  // 其他的都是 框架
    sleep(5000);// 暂停5秒,5000毫秒

// 十进制    逢十进一    0~9 
// 十六进制  逢十六进一  0~9,A,B,C,D,E,F ,古代大多使用16进制的，
//          如半斤八两，还有算盘，上面两颗珠子，每颗代表5，下面5颗珠子，每颗代表1，超过15，算盘上就要进位了
// 二进制   逢二进一    计算机用二进制（数字用0和1来表示）来存储数据。二进制 的进位规则是“逢二进一”。 
// 现代日常生活中也不都是十进制，例如 时间进制，60秒为1分钟，60分钟为1小时，用的是60进制

//    而 24小时为1天，用的是 24进制，
//    28天/30天/31天 为一个月
//    12个月为1年

/*
十进制整数转换为二进制整数采用”除2取余，逆序排列”法。 
具体做法是：用2整除十进制整数，可以得到一个商和余数；
再用2去除商，又会得到一个商和余数，如此进行，直到商为0时为止，
然后把先得到的余数作为二进制数的低位有效位，
后得到的余数作为二进制数的高位有效位，依次排列起来。
https://blog.csdn.net/haishu_zheng/article/details/78334207

*/

// 打印 小飞机======
        *
        **
*       ***
**      ****
******************
**      ****
*       ***
        **
        *
        
        
// 打印小队旗=========
A
I*
I**
I***
I****
I*****
I
I
I




// 计算机也会做 算术题=====
int a,b,c; // 申请 3个小房子，变量，来存储数据的
           // 有不同类型的小房子，平方、瓦房、别墅
           // int   存储 整数   %d
           // float 存储 小数   %f   浮点数
           // char  存储 字符   %c   字符编码--- ASCII编码---
           // double 双精度浮点数，存储更大，精度更高的数
a=1;// 房子里面 存储 1
b=2;
c=a+b;
// c = my_add(a,b); // 函数求和====
printf("a+b=%d",c);
// printf("%d + %d = %d",a,b,c); // 格式化输出==


// 定义 模块 函数 积木 魔法 法术 特技 哆啦A梦的口袋====
int my_add(int x, int y) // 类型 函数名称（类型 形式参数，……） 
{// 函数体 
    int z = x + y; // 两个数求和
    return z;
}

// + - * / 四则运算======



// 输入数据===========scanf()===========
int a;
scanf("%d", &a);
// printf("%d",a);// printf变身为scanf, 小房子前面多了个 &符号，取地址符号，查户口；
// 上课(到教室里)，需要知道教室地址
// 下课(离开教室)，不需要知道教师地址

// 获取2个数
int c,d,e;
// 可以在前后加一些 人性化的提示性语言
scanf("%d %d", &c,&d);        // 耳朵听进来
e=c+d;// 算数计算
printf("%d + %d = %d",c,d,e); // 嘴巴说出去



// 交换两个 变量的值 =======
int a,b,t;
a=10;
b=3;
//方法一,使用另外一个小房子
t=a;
a=b;
b=t;
// 方法二，使用3次运算
a = a+b; // 如果数很大的话，采用（三）中的方法，a = a + b这一步，有可能发出内存溢出现象
b = a-b;
a = a-b;
     // 这个叫做内存溢出（可联想为：米缸装满了，再也装不进去，继续装的话，米就会溢出来了）。 
     // 内存溢出是一种程序漏洞，有可能被黑客所利用并攻击（可联想为：米被老鼠吃了）。 
     // 所以，建议不要使用此方法来交换两个数。
// 方法三，使用位 异或云算符
a ^= b;
b ^= a;
a ^= b;

// 代码规范化=====
// 注释
// 缩进
// 简介
// 高效
// 艺术家

```


# 计算机不傻=====

> 判断
```c
操作数1 == 操作数2; // 判断是否相等，单个 = 号是赋值 
                   // 建议写成 常量 == 变量，比如if(10 == x) ,防止少写一个=，而将变量的值改变了。
操作数1 != 操作数2; // 不相等判断
操作数1 >= 操作数2; // 大于等于
操作数1 <= 操作数2; // 小于等于
操作数1 > 操作数2;  // 大于
操作数1 < 操作数2;  // 小于

//-----------------------------------------
// 判断是否大于零==============
int a;          // 小房子
scanf("%d",&a); // 告诉计算机这个数是多少
if(a>0)
    printf("yes");
// if(a<= 0)
else  // 简化代码
    printf("no");
sleep(5000);

// 加减乘除 + - * /  取余数%==

//-----------------------------------------
// 判断偶数，除以2的余数为0==========
int a;          // 小房子
scanf("%d",&a); // 告诉计算机这个数是多少
if(a%2 == 0)
    printf("yes");
// if(a%2 != 0)=====
else // 简化代码
    printf("no");
sleep(5000);


//-----------------------------------------
//计算两个数的和===================
int a,b,c;
scanf("%d %d",&a,&b);
c=a+b;
printf("%d + %d = %d",a,b,c)


//-----------------------------------------
//判断两个小朋友谁大===================
int a,b,c;
scanf("%d %d",&a,&b);
if(a>b)
{
    printf("%d is bigger",a);
    c=a;
}
else if(a == b)
{
    printf("equal");
    c=a;
}
else
{
    printf("%d is bigger",b);
    c=b;
}


//-----------------------------------------
//判断三个小朋友谁大===================
int a,b,c,d;
scanf("%d %d",&a,&b,&c);
if(a>b)
    d=a;
else 
    d=b;
// 和第三个数比较==
if(d<c)
    d=c;   
printf("%d is bigger",d);

//--------------------
// && 逻辑与，并且，两者都   ；    || 逻辑或    !逻辑非=====
/*
 && 相当于生活中说的“并且”，就是两个条件都同时成立的情况下 && 的运算结果才为“真”。
只要有一个条件不成立，则结果为“假”。 
1 && 1 = 1 
1 && 0 = 0 
0 && 1 = 0 
0 && 0 = 0

 || 相当于生活中说的“或者”，只要有一个条件成立， || 的运算结果就为“真”。
 两个条件都不成立结果才为“假”。 
1 || 1 = 1 
1 || 0 = 1 
0 || 1 = 1 
0 || 0 = 0

逻辑非!，如果条件为真，加上“!”后判断为假；
如果条件为假，加上”!”后判断为真。 
!0 = 1 
!1 = 0 
注意，计算机 非0 即为真，比如x = 1或x = 3或x = 50或x=-27，这些情况下if(x)判断都为真。
*/

// 或者使用 连续 逻辑判断-------------
if(a >= b && a >= c)
    printf("%d is bigger",a);
    
if(b >= a && b >= c)
    printf("%d is bigger",b);   
    
if(c >= a && c >= b)
    printf("%d is bigger",c);   


//------------------------------
// 三个小朋友 身高排序
int a,b,c,t;
scanf("%d %d",&a,&b,&c);
if(a<b)
   { // 交换 a,b
    t=b;
    b=a;
    a=t;
    }
    // a>=b ===
if(a<c)
   { // 交换 a,c
    t=a;
    a=c;
    c=t;
   }
   // c>a>=b
else if(b<c)
   { // 交换 b,c
    t=c;
    c=b;
    b=t;
   }
printf("%d >= %b >= %d",a,b,c);


// if() ...; else if() ...; else ...;


// switch case语句=====
https://blog.csdn.net/haishu_zheng/article/details/78334232


// 二进制位 运算符 “与（&）”、“或（|）”、“异或（^）”

https://blog.csdn.net/haishu_zheng/article/details/78334210
switch case语句与if elseif语句类似，都是从多个选择条件里选取一个来执行。

switch case的结构为:

switch(表达式或变量或常量)
{
    case 条件1:
        {
            执行语句;
            break; // “break;”表示中断，若忘了写，程序会继续执行下面的条件。
        }
    case 条件2:
        {
            执行语句;
            break;
        }
    ……
    default:
        {
            执行语句;
            break;
        }
}


```


# 重复不停的哭 我最在行  循环 重复不停的做 
```c
while(1)
{
    printf("wa");
}

// 指定 循环次数
int a;
a = 1;
int sum=0;
while(a <= 100)
{
    printf("wa");
    // printf("%d",a); // 打印 1,...,100
    // if(a%2 == 0) printf("%d",a); // 打印偶数
    // if(a%3 == 0) printf("%d",a); // 打印 3的倍数 数
 
    // 求和===
    // sum = sum + a;
    
    
    a =  a+1;
    // a += 1;
    // a++;     // ++符号表示“自加”，就是变量在原来的基础上加1。 --表示自减
                // a++ 表达式的值 为 a之前的值，a的值变为 a+1
                // ++a 表达式的值 为 a+1的值，a的值也变为 a+1
}

/*
while是先判断条件，再执行循环里的语句。
而do while是先执行循环里的语句，再判断循环条件。 

do while至少会执行一次循环；
而while若第一次判断条件不成立时，一次循环都不会执行。

*/

// 倒计时
system("cls");// 清屏
printf("3");
system(1000);//停止1秒
printf("2");
system(1000);//停止1秒
printf("1");
system(1000);//停止1秒

system("cls");// 清屏
printf("0");

system(5000);//停止1秒


// 可以用 循环来实现 60秒 倒计时===


// 循环打印 图形----------------------
*****
*****
*****
// 方法1，直接打印---
printf("*****");
printf("*****");
printf("*****");
// 方法2，循环实现----
int a = 1;
while(a <= 15)// 总共15个 * 号
{
    printf("*");// 打印1个*
    if(a%5 == 0)
        printf("\n");// 换行
    a++;
}

// =======
*
**
***
****
*****
inta=1;
while(a <= 5)// 总共5行
{
    int i=1;
    while(i<=a)// 打印 a 个 * 号
       {
           printf("*");// 打印1个*
           i++;
       }
        
    printf("\n");// 换行
    a++;
}

// =======
*
***
*****
*******
*********
inta=1;
while(a <= 5)// 总共5行
{
    int i=1;
    while(i <= 2*a-1 )// 打印 2*a-1 个 * 号=====
       {
           printf("*");// 打印1个*
           i++;
       }
        
    printf("\n");// 换行
    a++;
}

//===============
1
2 2
3 3 3
4 4 4 4
5 5 5 5 5


//  奔跑的小明同学====================
//   让字母 M 每格1秒 向右移动一格

int a,b;
a=1;
while(a<=5)// 移动5次
{
    system("cls");// 清屏
    b=1;
    while(b <= a) // 打印 a个 空格=====
    {
        printf(" ");//打印 1个 空格
        b++;
    }
    
    printf("M");// 打印 小明明
    sleep(1000);// 停1秒钟
    a++;
}

// 打印 小人====
printf(" O\n");   //头
printf("<H>\n");  //身体
printf("I I\n");  //腿
system("pause");  //暂停

// 让小人跑起来=====
int a,b;
a=1;
while(a<=5)// 移动5次
{
    system("cls");// 清屏
    
    b=1;
    while(b <= a) // 打印 a个 空格
    {
        printf(" ");//打印 1个 空格
        b++;
    }
    printf(" O\n");   //头======
    
    b=1;
    while(b <= a) // 打印 a个 空格
    {
        printf(" ");//打印 1个 空格
        b++;
    }
    printf("<H>\n");  //身体====
    
    b=1;
    while(b <= a) // 打印 a个 空格
    {
        printf(" ");//打印 1个 空格
        b++;
    }
    printf("I I\n");  //腿=====
    
    
    sleep(1000);// 停1秒钟
    a++;
}



// for 循环=======计算1+2+...+100的和
// for循环的语句结构为： 
// for(表达式1; 表达式2; 表达式3) 
// { 
    语句; 
// }
/*
其执行顺序为： 
（1）执行表达式1 
（2）执行表达式2。表达式2是一个判断语句；若为真，则执行{}中的语句。若为假，则结束for循环 
（3）若表达2为真，执行{}中的语句后，执行表达式3 
（4）执行表达式2 
（5）不断重复步骤（3）和步骤（4），直到表达式2为假，结束循环。
*/

int a,sum;
for(a=1; a<= 10; a++) // 1+2+...+100的和
// for(a=2; a<= 10; a=a+2) // 2+4+,...,+100 偶数和
// 奇数和...
{
    sum = sum + a; // sum += a; // 都是让sum和a相加后，把新的值赋给sum。 
}
printf("1+2+,...,+100 = %d",sum);


//=========打印复杂形状
  *
 ***
*****
 ***
  *

// 打印九九乘法表======

````

# 编程 计算 思考题
```c
题目
有两堆一样多的苹果，老师将第一堆苹果分给男生，每人4个，最后剩下6个。 
老师又将第二堆苹果分给女生，每个5个，最后剩下5个。 
已知男生比女生多1人。 
求：女生有多少人？男生有多少人？苹果有多少个？
使用方程求解
设苹果总数为y，女生人数为x，则有 
y = 5 * x + 5         (1) 
y = 4 * (x + 1) + 6       (2) 
(2) 式- (1)式得， 
0 = 4 * (x + 1) + 6 - (5 * x + 5) 
解得x = 5, y = 30 
所以，女生5人，男生6人，苹果30个。

编程求解
在解法（二）的思想基础上，可以编写程序如下：

#include <stdio.h>

int main()
{
    int x;// 设 x为 女生人数， 则 x+1为男生人数
    for(x = 1; x < 100000000; x++)
    {
    // 两种分配情况下，两堆苹果熟了应该相等
        if( 4 * (x + 1) + 6 ==  5 * x + 5)
        {
            break;  // 找到合适的x，跳出for循环
        }
    }

    printf("女生的人数为%d\n", x);
    printf("男生的人数为%d\n", x + 1);
    printf("苹果共有%d个\n", 5 * x + 5);

    return 0;
}

>>>
女生的人数为5
男生的人数为6
苹果共有30个


求圆周率 
  圆周率（Pi）是圆的周长与直径的比值，一般用希腊字母π表示，是一个在数学及物理学中普遍存在的数学常数。
  π也等于圆形之面积与半径平方之比。是精确计算圆周长、圆面积、球体积等几何形状的关键值。 
  圆周率是一个无理数，即无限不循环小数。在日常生活中，通常都用3.14代表圆周率去进行近似计算。
  而用十位小数3.141592654便足以应付一般计算。
  即使是工程师或物理学家要进行较精密的计算，充其量也只需取值至小数点后几百个位。

  计算公式
    1965年，英国数学家约翰·沃利斯（John Wallis）出版了一本数学专著，
    其中他推导出一个公式，发现圆周率等于无穷个分数相乘的积。
    2015年，罗切斯特大学的科学家们在氢原子能级的量子力学计算中发现了圆周率相同的公式： 
     
     pi/4 = 1/1 - 1/3 + 1/5 - 1/7 + 1/9 - 1/11 + ……
     
     
#include <stdio.h>
#include <math.h>

int main()
{
    float pi = 0;
    int sign = 1;       // 正负符号 
    float deno = 1;     // 分母
    float item = 1;     // 项 
    // fabs是求绝对值的函数，在math.h中声明，在math.c中定义
    // 1e-6中的"-"左右两侧不能有空格；等价于0.000001。同理1e-3等价于0.001 
    while(fabs(item) >= 1e-6)
    {
        pi += item;
        sign = -sign;       // 根据公式，每计算一项，就得变动一次正负号 
        deno +=2;           // 分母每次都自加2 ，奇数
        item = sign / deno; // 第几项的值，用于下一轮计算 
    }

    pi = 4 * pi; // 还原 pi
    printf("pi = %f", pi);

    return 0;
}

   
   
// 鸡腿同笼问题=================
#include<stdio.h>
main()
{
	int h, f, x, y;
	printf("鸡兔的总数，鸡兔脚总数:");
	scanf_s("%d%d", &h, &f);
	if (h> 0 && f> 0)
	{
		x = (4 * h - f) / 2;
		y = (f - 2 * h) / 2;
		printf("鸡:%d   兔:%d", x, y);
	}
	else
		printf("输入错误!\n");
}
 

// 箱子形状======
#include<stdio.h>
int main()
{
	int l, w, h;
	printf("请输入箱子的长、宽、高：\n");
	scanf("%d%d%d", &l, &w, &h);
	if (l == w && w==h && l==h)
		printf("该箱子是正方形\n");
	else 
	    printf("该箱子是长方形\n");
	return 0;
}


// 年月日 计算=================
 #include<stdio.h>
int main()
{
	int year,month,days;
	printf("Please enter year and month:\n");
	scanf("%d%d",&year,&month);
	switch (month)
	{
		case 2:
			if((year%4==0 && year%100!=0) || year%400==0)
			   days=29;
			else
			   days=28;
		    break;
	    case 1:
	    	days=31;
	    	break;
	    case 3:
	    	days=31;
	    	break;
	    case 4:
	    	days=30;
	    	break;
	    case 5:
	    	days=31;
	    	break;
	    case 6:
	    	days=30;
	    	break;
	    case 7:
	    	days=31;
	    	break;
	    case 8:
	    	days=31;
	    	break;
	    case 9:
	    	days=30;
	    	break;
	    case 10:
	    	days=31;
	    	break;
		case 11:
	    	days=30;
	    	break;
		case 12:
	    	days=31;
	    	break;    
	}
	printf("%d年%d月%d日",year,month,days);
	return 0;
}


// 小卖铺====当小老板======================
#include<stdio.h>
int main()
{
	int x,n,y;
	float sume=0.0;
	printf("请选择：1.日用品      2.文具         3.食品\n");
	scanf("%d",&x);
	switch(x)
	{
		case 1:
			printf("请选择：1.牙刷（3.5元/支）  2.牙膏（6.2元/支）\n");
			printf("        3.肥皂（2元/块）    4.毛巾（8.6元/条）\n");
			scanf("%d",&y);
			printf("数量？"); 
			scanf("%d",&n);
			switch(y)
			{
				case 1: sume=n*3.5; break;
				case 2: sume=n*6.2; break;
				case 3: sume=n*2;   break;
				case 4: sume=n*8.6;	break;
			 } 
			 break;
		case 2:
			printf("请选择：1.笔（3元/支）         2.笔记本（1.2元/个）\n");
			printf("        3.文件夹（12元/个）    4.文具盒（8.6元/个）\n");
			scanf("%d",&y);
			printf("数量？");
			scanf("%d",&n);
			switch(y)
			{
				case 1: sume=n*3;   break;
				case 2: sume=n*1.2; break;
				case 3: sume=n*12;  break;
				case 4:	sume=n*8.6; break;
			 } 
			 break;
 	    case 3:
			printf("请选择：1.白糖（3.6元/包）  2.盐（1元/包）\n");
			printf("        3.饼（2元/个）      4.方便面（3.6元/条）\n");
			scanf("%d",&y);
			printf("数量？");
			scanf("%d",&n);
			switch(y)
			{
				case 1: sume=n*3.6; break;
				case 2: sume=n*1;   break;
				case 3: sume=n*2;   break;
				case 4: sume=n*3.6; break;
			 } 
			 break;
	} 
	printf("总计：%.2f 元\n",sume);
	return 0; 
 } 







```


## 递归 斐波那契数列
```c
/*
斐波那契数列指的是这样一个数列 
1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233，377，610，987，1597，2584，4181，6765，10946，17711，28657，46368…….. 
这个数列从第3项开始，每一项都等于前两项之和。
黄金分割树 0.618  
*/

#include <stdio.h>

int fibonacci(int n) 
{
    if(1 == n || 2 == n)
    {
        return 1;
    }

    int f1 = 1;
    int f2 = 1;
    int f3 = 0;

    for(int i = 3; i <= n; i++)
    {
        f3 = f1 + f2;
        f1 = f2; 
        f2 = f3;
    }

    return f3;
}

int main()
{   
    int m, result;

    printf("input  item number: ");
    scanf("%d", &m);

    result = fibonacci(m);

    printf("The result is %d", result);

    return 0;
}
 
// 斐波那契数列的递归实现------------
/*
什么是递归呢？先举个例子：

从前有座山，山里有座庙，庙里有个老和尚，正在给小和尚讲故事呢！故事是什么呢？
”从前有座山，山里有座庙，庙里有个老和尚，正在给小和尚讲故事呢！故事是什么呢？
’从前有座山，山里有座庙，庙里有个老和尚，正在给小和尚讲故事呢！故事是什么呢？……’ ”
这个例子里，故事内嵌套着故事，构成了递归。 
// 函数调用自身，就叫函数的递归调用。这个程序里，fibonacci()函数就调用了它本身。
*/
#include <stdio.h>

int fibonacci(int n) 
{
    // printf(“n = %d\n”, n); // 用断点查看程序的执行过程
    if(1 == n || 2 == n)
    {
        return 1;
    }
// 函数调用自身，就叫函数的递归调用。这个程序里，fibonacci()函数就调用了它本身。
    return fibonacci(n-2) + fibonacci(n - 1);
}

int main() 
{
    int m;
    printf("input m: ");
    scanf("%d", &m);

    int result = fibonacci(m);
    printf("fibonacci(%d) = %d\n", m, result);

    return 0;   
}


 
```

## 数组----火车??
    C 语言支持数组数据结构，它可以存储一个固定大小的相同类型元素的顺序集合。
    数组是用来存储一系列数据，但它往往被认为是一系列相同类型的变量。 
    数组的声明并不是声明一个个单独的变量，比如 number0、number1、…、number99，
    而是声明一个数组变量，比如 numbers，
    然后使用 numbers[0]、numbers[1]、…、numbers[99] 来代表一个个单独的变量。
    数组中的特定元素可以通过索引访问。 
    所有的数组都是由连续的内存位置组成。
    最低的地址对应第一个元素，最高的地址对应最后一个元素。
    
https://blog.csdn.net/haishu_zheng/article/details/78308753

    字符串----字符数组
    在 C 语言中，字符串实际上是使用 null 字符 ‘\0’ 终止的一维字符数组。
    
    由于在数组的末尾存储了空字符，所以字符数组的大小比单词 “Hello” 的字符数多一个。
    
    char str[] = {'H', 'e', 'l', 'l', 'o', '\0'};
    但是在算字符串的长度时，最后的空字符‘\0’不算在内。
    
https://blog.csdn.net/haishu_zheng/article/details/78334193


## 排序

    冒泡排序
      将相邻两个数比较，将大的调到后头。如果有n个数，则要进行n-1趟比较。
      在第1趟中要进行n-1次两两比较，在第j趟比较中要进行n-j次两两比较。
https://blog.csdn.net/haishu_zheng/article/details/78334217
    
    选择排序
      如果有n个数，需要比较n-1轮： 
      第1轮，将n个数中最小的数与a[0]对换，当然若a[0]就是最小的数则不用对换。 
      第2轮，将a[1]到a[n-1]中最小的数与a[1]对换，当然若a[1]就是最小的数则不用对换。 
      …… 
      第n-1轮，将最后的两个数，即a[n-2]与a[n-1]比较，若a[n-2] > a[n-1]，则对换。至此，排序完毕。
https://blog.csdn.net/haishu_zheng/article/details/78334221
    
## 指针，家庭住址，班级座位号，变量在计算机内部存储的 地址

     https://blog.csdn.net/haishu_zheng/article/details/78334227
    
    二级指针与多级指针 
     https://blog.csdn.net/haishu_zheng/article/details/82723314
    


# C++语言==========================

## Hello World
```cpp
#include <iostream> // 定义了一些头文件，这些头文件包含了程序中必需的或有用的信息
using namespace std;// 告诉编译器使用 std 命名空间, standard 标准库，类似不同的班级
                    // 可以防止不同的人 有相同的名字，避免命名发生冲突
                    // 5年级4班 的 李小明 同学
                    // 6年级3班 也有一个 李小明 同学
                    // 可以使用前面 所属 班级 来区别他们
 
int main() // 是主函数，程序从这里开始执行。
{
   cout << "Hello World\n"; // 会在屏幕上显示消息 “Hello World”。 \n 换行打印
   cout << "小明，你好";     // 显示中文
   return 0;                //  终止 main( )函数，并向调用进程返回值 0。
}

```


## 面向过程与面向对象
```cpp
// 编写一个加法程序
#include <iostream>
using namespace std;

// 编写一个 计算两个数 和 的 函数 
int add(int a, int b)
{
    return a + b;
}

int main()
{
    int x = 5, y = 10;
    int z = add(5, 10);
    cout << "x = " << x << endl;
    cout << "y = " << y << endl;
    cout << "x + y = " << z << endl;

    return 0;
}

// 运行结果：
x = 5
y = 10
x + y = 15

// 区别 与联系=====
C是面向过程的。 
C++既可以面向过程，也可以面向对象，并且以面向对象为主。 
C++是一些聪明的程序员在C的基础上创造、发展起来的，与C语言最大的区别就是面向对象。

C语言的重点在于算法和数据结构，
   C程序的设计首要考虑的是如何通过一个过程，对输入进行运算处理得到输出。 
   所以C语言是面向过程语言。

C++，首要考虑的是如何构造一个对象模型，让这个模型能够契合与之对应的问题域，
   这样就可以通过获取对象的状态信息得到输出或实现过程控制。 

以狗吃屎为例，来说明面向过程和面向过对象的区别。

C语言：吃(狗，屎) 
这里“吃”是函数名，“狗”和“屎”是参数。强调的是吃这一过程。

C++：狗.吃屎() 
这里狗是对象，吃屎是狗的一个函数。语法是一个完整的主谓宾结构。主语是“狗”，谓语是“吃”，宾语是“屎”。 
狗除了吃屎外，还有其他行为，比如汪汪叫，伸舌头等。语法为 
狗.汪汪叫() 
狗.伸舌头() 
这一系列行为里，强调的是“谁来做”，这里是狗来做，所以强调的是狗这一对象。

```


## 类与对象
```cpp
一）类与对象
  类是由我们根据客观事物抽象而成，形成一类事物，然后用类去定义对象，形成这类事物的具体个体。
  比如小狗是一个类，你家的“旺财”则是小狗一个具体的对象。
二）属性与方法
  一般把类的数据成员称为类的属性,把类的函数成员称为方法。 
  比如小狗这个类吧，它的属性有身高、体长、体重、名字、年龄、性别等，它的方法有吃，走，跑，呼吸，吠等。 
  从这里也可以看出，属性都是静态的，而方法都是动作。

#include <iostream>
using namespace std;

class Dog
{
public: // public表示公有的，在类的外部可以访问。main()函数就属于类的外部。
  // public: 可以被 类自己、外部、继承者(孩子)、朋友等其他所有 访问
  // protected: 保护类型，可以被自己、继承者(孩子)以及朋友访问，主要是实现继承
  // private: 私有类型，可以被自己、朋友(同辈)访问，实现封装
  // class 默认 为 private属性
  // struct 默认为 public属性
    // 属性===特性===特点===特征
    string name;    // 名字 
    int age;        // 年龄 
    int sex;        // 性别，可以定义为，1表示公，0表示母 
    float height;   // 身高 
    float length;   // 体长 
    float weight;   // 体重 
    // 吃=====
    void eat()
    {
        cout << "eating..." << endl;
    }
    // 走======
    void walk()
    {
        cout << "walking..." << endl;
    }
    // 跑=====
    void run()
    {
        cout << "running..." << endl; 
    }
    // 呼吸=====
    void breathe()
    {
        cout << "breathing..." << endl;
    }
    // 犬吠=====
    void bark()
    {
        cout << "wang! wang!" << endl;
    }
};  // 在类定义结尾处的}后面需要加分号，这是语法要求。否则编程出错。

int main()
{
    Dog dog; // 创建类实例 对象 声明一个类型为Dog的对象dog
    // Dog mydog;
    dog.name = "Wang Cai";// 起名字,给对象设置属性
    dog.age = 3;// 3岁
    dog.run();  // 遛狗，狗跑起来,调用对象的方法
    dog.bark(); // 见到其它狗，犬吠

    return 0;
}

运行结果：

running...
wang! wang!

```


## 类构造函数
```cpp
构造函数，作用是完成对象的初始化工作。 
可类比于：int a = 1;这里是给变量a赋初值。
构造函数是一种特殊的函数，首先构造函数名与类名是完全一致的，其次构造函数没有类型。
构造函数可以不带参数，也可以带参数。

#include <iostream>
using namespace std;

class Dog
{
public:
    // 类 属性 名字，类内参数，命名时，通常在前面+ m_
    string m_name;
    
// 构造函数是在生成对象时被调用的，并且不需要显示调用=====

    // 无参 构造函数 
    Dog()
    {
        cout << "Dog's constructor!" << endl;
    }

    // 有参 构造函数 
    Dog(string Name)// 实例化对象 时 直接传入 类的一些属性(这里为狗的名字)
    {
        m_name = Name;
        cout << "Dog's constructor with name!" << endl;
    }
    
    // 方法: 狗跑
    void run()
    {
        cout << m_name << " is running..." << endl;
    }
};

int main()
{
    Dog dog1;// 无参构造函数
    dog1.m_name = "Wang Cai";// 旺财
    dog1.run();

    Dog dog2("Xiao Bai");// 小白 黑豆 桂花
    dog2.run();

    return 0;
}

```

## this指针 我就是我 不一样的自我 酸酸甜甜就是我
```cpp
this指针是一个隐含于类中的特殊指针，指向对象本身。
   也就是说对象一旦被创建，this指针也就存在了。 
就好比你的名字叫做 小明，别人说你的时候用的是 小明，但是你说你自己的时候，用的是“我”。 
这个“我”，在C++和Java中，是用 this 来表示的。
而在Python和Objective-C（苹果的开发语言）中，则用 self 来表示。

#include <iostream>
using namespace std;

class Dog
{
private:
    string name;

public:
    // 有参构造函数
    Dog(string name)
    {
        this->name = name; // 为类属性赋值
        printf("%p\n", &this->name);// 类属性 变量  地址
        printf("%p\n", &name);// 构造函数 形参 地址
        cout << "Constructor method with name!" << endl;
        
        // 打印 本类对象 的地址
        printf("Memory address of this: %p\n", this);// this为 指针地址
    }

    void run()
    {
        cout << name << " is running!" << endl;
        printf("%p\n", &name); // 这里的 name为 类的属性变量 
    }

};

int main() 
{
    Dog dog("Wang Cai");
    dog.run();
    
    printf("Memory address of dog: %p\n", &dog); 
    
    return 0;   
}

运行结果：

000000000022fe20     // 类属性 name 的地址
000000000022fe30     // 构造函数形参 name的地址，中间变量，临时存在
Constructor method with name!
Memory address of this: 000000000022fe4f // 类 this 指针的值，就是类实例对象的地址
Wang Cai is running!
000000000022fe20     // 类属性 name 的地址
Memory address of dog: 000000000022fe4f  // 在类外部运行的对象的内存地址，与类内部运行的this的内存地址，完全一样。 

// 这也印证了上面说的，别人口中的小明 与 小明自己口中的“我”，就是同一个人。

```


## 封装 隐藏 绑定 藏起来
```cpp
所有的 C++ 程序都有以下两个基本要素： 
函数：这是程序中执行动作的部分，它们被称为函数或方法。 
数据：数据是程序的信息，会受到程序函数的影响，也叫属性。

封装是面向对象编程中的把数据和操作数据的函数绑定在一起的一个概念，这样能避免受到外界的干扰和误用，从而确保了安全。

我们已经知道，类包含私有成员（private）、保护成员（protected）和公有成员（public）成员。
默认情况下，所有的数据成员和函数成员都是私有的。 

为了使类中的成员变成公有的（即程序中的类外部的其他部分也能访问），必须在这些成员前使用 public 关键字进行声明。
所有定义在 public 标识符后边的属性或函数可以被程序中所有其他的函数访问。


#include <iostream>
using namespace std;

class Adder{// 累加器
   public:
      // 构造函数
      Adder(int i = 0)// 带默认参数值，构造函数的默认参数
      {
        total = i;
      }
      // 对外的接口
      void addNum(int number)
      {
          total += number;// 加上一个数
      }
      // 对外的接口
      int getTotal()
      {
          return total; // 返回累计的值
      };
   private:
      // 对外隐藏的数据，外部不可访问，不过朋友可以访问(有元函数、有元类)
      int total;
};

int main()
{
   Adder a;// total默认初始化为0

   a.addNum(10);
   a.addNum(20);
   a.addNum(30);

   cout << "Total is " << a.getTotal() << endl;
   return 0;
}
 
运行结果：

Total is 60

上面的类把数字相加，并返回总和。公有成员 addNum 和 getTotal 是对外的接口，用户需要知道它们以便使用类。
私有成员 total 是对外隐藏的（即被封装起来），用户不需要了解它，但它又是类能正常工作所必需的。

类的设计策略： 
通常而言，要把类的数据成员设计成私有（private），
类的函数成员则根据实际需要设计成publice, protected或private。

```



## protected继承 子承父业 改革创新 遗传 鼻子耳朵像爸爸 眼睛像妈妈 嘴巴有点变化
```cpp
父类(基类) 具有一些 拓展类(继承类)的共性，
可以定义一个父类，而一些具有不同特性的子类可以从父类继承过来。
这个 定义一个 动物父类，大都具有叫、跑等功能，小狗，小猫可以从父类继承过来，再根据自身特点，创新


#include <iostream>
using namespace std;

// 父类(基类) 动物类
class Animal
{
protected:// 保护类型，可以被子类继承，如果为 private，则该属性不可被继承
    float weight;// 体重
    
public:
    void setWeight(float w) 
    {// 设置体重
        weight = w;
    }

    float getWeight()
    {// 获取体重信息
        return weight;
    }
    
    // 呼吸
    void breathe()
    {
        cout << "breathing..." << endl; 
    }   
};


// 小狗 子类 继承父类 动物的一些属性和方法，并增添一些新方法
class Dog : public Animal
{
private:// 注意为 私有 该类 的 该属性 不可再被继承
    int legs;// 多 一个属性 腿的数量
    
public:
    void setLegs(int number)
    {// 也就相应多了 操作 腿属性的 函数方法
        legs = number;  // 设置腿的数量
    }

    int getLegs()
    {// 获取腿的数量
        return legs;    
    }
    
    // 犬吠，汪汪叫
    void bark()
    {
        cout << "wang! wang!" << endl;
    }   
};

int main(int argc, char** argv)
{
    Dog dog;
    dog.setWeight(12.5);// 设定体重属性，继承自 动物类
    dog.setLegs(4);     // 设定腿数量属性，子类 新增添的属性

    cout << "The dog's weight is " << dog.getWeight() << "kg" << endl;// 重量
    cout << "The dog has " << dog.getLegs() << " legs" << endl;       // 几条腿
    dog.breathe(); // 呼吸
    dog.bark();    // 犬吠

    return 0;
}
运行结果：

The dog’s weight is 12.5kg
The dog has 4 legs
breathing...
wang! wang!

程序分析： 
1）Animal为一个类，Dog为另一个类。 
   class Dog : public Animal 表示Dog类继承了 Animal类。
   此时，Animal就成了Dog的基类或父类。Dog就成了Animal的派生类或子类。

2）体重和呼吸是所有动物的共性，所以weight和breathe()定义在类Animal中。
   腿和吠不是所有动物的共性，所以legs和bark()定义在了类Dog中。

3）class Dog : public Animal , 这里的public表示继承方式 。 
继承方式有三种：public, protected和private。 
 a. 父类为private的属性和方法，不能被子类继承。 
 b. 父类为protected的成员，若被子类public继承的，仍为子类的protected成员；
    若被子类protected或private继承的，变为子类的private成员。 
 c. 父类为public的成员，若被子类public继承的，仍为子类的public成员；
    若被子类protected继承的，变为子类的protected成员；
    若被子类private继承的，变为子类的private成员。

注：这些不用强记，编多了自然就知道

4）根据 3）中 第a条 的结论，若程序改为class Dog : protected Animal，则程序无法通过编译。
   因为setWeight()和getWeight()被protected继承后，变为Dog的protected成员，
   而protected成员，无法在类外部（比如main函数中）访问。


```


## 构造函数的默认参数
```cpp
构造函数的参数可以预先赋一个初值，
其作用是：在构造函数被调用时，省略部分或全部参数，这时就会使用默认参数代替实参。

#include <iostream>
using namespace std;

// 长方形类====
class Rectangle
{
private:// 私有属性，不可继承
    int width;  // 宽
    int height; // 高
    
public:
    Rectangle(int w = 0, int h = 0)// 带默认参数的 有参构造函数
    {
        cout << "Constructor method is invoked!" << endl;
        width = w;
        height = h;
    }
    
    // 方法，计算并返回 长方形面积====
    int area()
    {
        return width * height; 
    }
};

int main(int argc, char** argv) 
{
    Rectangle rec1;//默认参数，实例化 长方形类对象         // 0*0=0
    cout << "Area of rec1 is : " << rec1.area() << endl;

    Rectangle rec2(5);// 1个传入参数，1个默认参数，实例化 长方形类对象 // 5*0=0
                      // 传入实参5，相当于传入（5，0）
    cout << "Area of rec2 is : " << rec2.area() << endl;

    Rectangle rec3(5, 10);// 2个传入参数，实例化 长方形类对象   // 5*10 =50
    cout << "Area of rec3 is : " << rec3.area() << endl;

    return 0;   
}

运行结果：

Constructor method is invoked!
Area of rec1 is : 0
Constructor method is invoked!
Area of rec2 is : 0
Constructor method is invoked!
Area of rec3 is : 50



```



## 子类构造函数调用父类构造函数
```cpp
从哲学层面来看，子类会继承父类除private以外的所有成员。 
因为构造函数是公有的，所以理所当然地会被子类继承。

#include <iostream>
using namespace std;

class Shape // 形状基类
{
public:
    Shape() 
    {
        cout << "Shape's constructor method is invoked!\n";
    }
};

// 长方形 公开 继承 自 形状类
class Rectangle : public Shape
{
public:
    // 长方形类 构造函数 显示 调用 基类 的 构造函数
      // 这是先调用父类的构造函数，再执行它本身的语句
    Rectangle() : Shape()
    {
        cout << "Rectangle's constructor method is invoked!\n" << endl;
    }
};

int main(int argc, char** argv) 
{
    Rectangle rec;

    return 0;   
}

运行结果：

Shape's constructor method is invoked!
Rectangle's constructor method is invoked!

就算 子类 的 构造函数 不显示 调用 父类的 构造函数
在构造子类时，父类的 构造函数也会被执行，
并且调用顺序优先于子类本身的构造函数。
    Rectangle()
    {
        cout << "Rectangle's constructor method is invoked!\n" << endl;
    }
    
    
```



## 箭头解引用 调用对象的方法、属性等
```cpp
#include <iostream>
using namespace std;

class A
{
public:
    void play() // 玩
    {
        cout << "playing..." << endl;
    }
};

int main()
{
    A a; // 实例化A类的一个对象a
    a.play(); // 对象a .号直接调用 类方法

    A *p = &a; // 定义对象指针
    
    (*p).play();// *号解引用 后 得到对象 再使用 .号访问类方法
    p->play();  // 直接使用 -> 箭头 对 对象的指针 进行调用

    return 0;
}
运行结果：

playing...
playing...
playing...


结论： 
在C++中， 
若是普通对象，使用点号操作符； 
若是指针对象，有两种操作方式：

1.  (*指针).方法()        （1）
2.  指针-->方法()         （2）

但是 1 不常用，所以 2 中的箭头操作符用的比较多。

```




## 多态，父类指向不同的子类时，会有不同的表现，父亲让不同的孩子做事情，会产生不同的结果
```cpp
#include <iostream> 
using namespace std;

// 父类 形状
class Shape
{
   protected: // 保护类型，可被继承
      int width, height;

   public:
      Shape( int a = 0, int b = 0)// 带默认参数的 有参构造函数
      {
         width = a;
         height = b;
      }
      
      // 虚函数 面积，可以被 子类的同名函数覆盖
      virtual int area()
      {
         cout << "Parent class area :" <<endl;// 只打印，未计算真实面积
         return 0;
      }
};

// 子类1：长方形，公开继承自 形状类 Shape====
class Rectangle: public Shape
{
   public:
      Rectangle( int a = 0, int b = 0)  
      { // 构造函数 沿用 父类的 构造函数
      }

      int area ()
      { 
      // 该 面积函数 会覆盖 父类 的面积函数
         cout << "Rectangle class area :" <<endl;
         return (width * height); // 矩形面积 = 宽*高
      }
};


// 子类2：三角形，公开继承自 形状类 Shape====
class Triangle: public Shape
{
   public:
      // 三角形类 构造函数，显示调用 父类 的构造函数
      Triangle( int a=0, int b=0) : Shape(a, b) { }

      int area ()
      {  // 该 面积函数 会覆盖 父类 的面积函数
         cout << "Triangle class area :" <<endl;
         return (width * height / 2); // 三角形面积，宽*高/2
      }
};


int main( )
{
   Shape *shape;// 父类，基类 指针，空
   Rectangle rec(10,7);// 子类 长方形类 实例化对象
   Triangle  tri(10,5);// 三角形

   // 存储矩形的地址
   shape = &rec;// 指向 子类1 长方形类实例对象
   // 调用矩形 的求面积函数 area
   shape->area();

   // 存储三角形的地址
   shape = &tri;// 指向 子类2 长方形类实例对象
   // 调用三角形 的求面积函数 area
   shape->area();

   return 0;
}

运行结果：
Rectangle class area :
Triangle class area :

如果 父类的 面积函数不加 virtual
运行结果：
Parent class area :
Parent class area :

程序分析： 
1）虚函数 
   虚函数是在基类中使用关键字 virtual 声明的函数。
   在派生类中重新定义基类中定义的虚函数时，会告诉编译器不要静态链接到该函数。 
   我们想要的是在程序中任意点可以根据所调用的对象类型来选择调用的函数，这种操作被称为动态链接，或后期绑定。 
   虚函数是C++中用于实现多态(polymorphism)的机制。核心理念就是通过基类访问派生类定义的函数。 
2）此时，编译器看的是指针的内容，而不是它的类型。
   因此，由于 tri 和 rec 类的对象的地址存储在 *shape 中，所以会调用各自的 area() 函数。 
   正如您所看到的，每个子类都有一个函数 area() 的独立实现。这就是多态的一般使用方式。
   有了多态，您可以有多个不同的类，都带有同一个名称但具有不同实现的函数。


```




## 引用 & 
```cpp
一）C语言中的“&”
在C语言里，我们碰到过“&”这个符号。
“&”的使用场景有两种： 

1）位运算符
int a = 5;
int b = 10;
int c = a & b;

2）取地址符
int a;
scanf("%d", &a);

二）C++语言中的“&”
在C++里，“&”的使用场景有三种： 
1）位运算符，这在C, C++, Java等语言中，都是一样的

2）取地址符，这是因为C++兼容了C

#include <iostream>
using namespace std;

int main() 
{
    int a;
    printf("Input a = ");
    scanf("%d", &a);
    printf("a = %d", a);

    return 0;
}

3）作为引用 
这是C++中加入的新语言特性。 
所谓引用，就是变量的别名。 
比如有一个人叫做小明，他有一个外号叫做“明明”，那么“明明”就是小明的引用。
别人说“小明”或明明，说的都是同一个人。

引用的语法为：类型 &引用名 = 变量名 
比如

int a;
int &ra = a; 
操作引用，就是操作变量本身。 


#include <iostream>
using namespace std;

int main() 
{
    int a; 
    int &ra = a;
    ra = 1;

    printf("Memory address of ra: %d\n", &ra);
    printf("Memory address of a: %d\n", &a);
    printf("ra = %d\n", ra);
    printf("a = %d\n", a);

    return 0;
}

运行结果：

Memory address of ra: 2293316
Memory address of a: 2293316
ra = 1 
a = 1

可见，ra和a的内存地址是一样的，值自然也一样。ra和a实际上是同一回事。

```



##  使用引用 实现两数交换的函数
```cpp
之前学C语言的时候，咱们直接在main函数中使用“异或”位运算符，很容易实现了两数交换。 
本节课将在此基础上，把交换两个数的算法，封装到swap函数中。
这样不管是哪个地方想要交换两个数，调用swap函数就可以了。

#include <iostream>
using namespace std;

void swap(int &m, int &n) // 注意这里为 引用形参
                          // 也就是 直接使用 传递给函数的 参数，
{
    cout << "Memory address of m: " << &m << endl;
    cout << "Memory address of n: " << &n << endl;

    cout << "\nBefore Swap:" << endl;
    cout << "m = " << m << endl;
    cout << "n = " << n << endl;
    
    // 使用 3次 “异或”位运算符 完成两个数的交换
    m ^= n;
    n ^= m;
    m ^= n;

    cout << "\nAfter Swap:" << endl;
    cout << "m = " << m << endl;
    cout << "n = " << n << endl;    
}

int main(int argc, char** argv) 
{
    int a = 1;
    int b = 2;

    cout << "Memory address of a: " << &a << endl;
    cout << "Memory address of b: " << &b << endl;  

    swap(a, b);

    cout << "a = " << a << endl;
    cout << "b = " << b << endl;

    return 0;
}

运行结果：

Memory address of a: 0x7fffd009de98
Memory address of b: 0x7fffd009de9c
Memory address of m: 0x7fffd009de98
Memory address of n: 0x7fffd009de9c

Before Swap:
m = 1
n = 2

After Swap:
m = 2
n = 1
a = 2
b = 1

使用引用后，达到了交换a和b的目的。
这是因为形参m和n是实参a和b的引用，m和a是一回事，n和b是一回事。 
交换m和n的值，就是交换a和b的值。


如果：
swap函数不使用引用 void swap(int m, int n){}，不会达到想要的效果。
从结果可以看出，a和b调用swap之后，值并没对换过来。 
其原因在于，形参m和n的作用域只是在 swap 函数内。
在swap内，m = a = 1, n = b = 2，交换后m = 2, n = 1。
但是，m和n的值并不会传回给a和b，导致a和b的值没有被对换。


```



## 多继承 
```cpp
单继承：子类（派生类）只能有一个父类（基类）。支持单继承的语言有Java, Objective-C, PHP, C#等。

多继承：子类（派生类）可以有多个父类（基类）。支持多继承的语言有C++, Python等。

举现实中的一个例子：农民工，既是农民，又是工人。所以农民工继承自农民和工人。

#include <iostream>
using namespace std;

class Farmer  // 农民==
{
public:
    Farmer()
    {
        cout << "I am a farmer" << endl;    
    }   
};

class Worker // 工人
{
public:
    Worker()
    {
        cout << "I am a worker" << endl;
    }

};

// 农民工MigrantWorker 继承 自 工人 和 农民
class MigrantWorker : public Farmer, public Worker
// 实例化 子类对象时，会按照 继承父类的顺序 调用的父类的 构造函数
{
public:
    MigrantWorker()
    {
        cout << "I am a migrant worker" << endl;
    }
};

int main(int argc, char** argv) 
{
    MigrantWorker m;

    return 0;
}
 
运行结果：

I am a farmer    // 父类1 Farmer 类的 构造函数 会先被调用
I am a worker    // 父类2 Worker 类的 构造函数 第二被调用
I am a migrant worker // 子类 的构造函数最后 才被调用


```


## C++创建对象的3种方式
```cpp

#include <iostream>
using namespace std;

class A
{
private:
    int n;
public:
    A(int m)
    {
        n = m;
        cout << "Constructor method is invoked!" << endl;   
    }

    void printNum()
    {
        cout << "n = " << n << endl;
    }
};

int main()
{
    // 第一种 
    A a1(1);            // 直接构造，a1在栈中 
    a1.printNum();

    // 第二种 
    A a2 = A(2);        // 拷贝构造，a2在栈中 
    a2.printNum();

    // 第三种  动态分配
    A *a3 = new A(3);   // a3所指的对象在堆中，但是a3本身放在栈中 
    a3->printNum();
    
    delete a3; // new 动态分配的，需要手动使用 delete删除

    return 0;
}
 
运行结果：

Constructor method is invoked!
n = 1
Constructor method is invoked!
n = 2
Constructor method is invoked!
n = 3

分析： 
1）第一种方法和第二种方法写法略有差异，但本质上是一样的。

2）一个由C/C++编译的程序占用的内存分为以下四个部分： 
a.栈区（stack）–由编译器自动分配释放，存放函数的参数值，局部变量的值等。 
b.堆区（heap）–由程序员分配释放。若程序员不释放，程序结束时可能由OS回收。 
  堆区的大小要远远大于栈区。 
c.全局区（静态区）（static）–全局变量和静态变量的存储是放在一块的。 
  里面细分有一个常量区，字符串常量和其他常量也存放在此。 
  该区域是在程序结束后由操作系统释放。 
d.程序代码区–存放函数体的二进制代码。 也是由操作系统进行管理的。

3）a1和a2，都是局部变量，放在栈里。 
指针a3本身放在栈区，但是它指向的对象，即new A()，放在堆里。 
用 malloc 或 new 出来的对象，都是放在堆里。 
cout << a3，这样得到的地址是指针a3所指的对象的存储地址，在堆里。 
cout << &a3，这样得到的地址，是指针a3本身存储的地址，在栈里。 

4）new出来的对象，使用完之后，要用delete语句来释放内存。


```



## 析构函数 妥善处理 善后工作 遛狗---清扫狗屎
```cpp
析构函数(destructor) 与构造函数相反，当对象结束其生命周期时（例如对象所在的函数已调用完毕），系统自动执行析构函数。
析构函数往往用来做“清理善后” 的工作（例如在建立对象时用new开辟了一片内存空间，delete会自动调用析构函数后释放内存）。

析构函数名也应与类名相同，只是在函数名前面加一个位取反符~，例如~A( )。以区别于构造函数。 
与构造函数一样，析构函数不能有返回值。
不同的是，析构函数，也不能带参数，并且一个类只能有一个析构函数。

如果用户没有编写析构函数，编译系统会自动生成一个缺省的析构函数。 
许多简单的类中没有使用用显式的析构函数。


#include <iostream>
using namespace std;

class A
{
public:
    A()
    {
        cout << "Constructor method is invoked!" << endl;   
    }

    ~A() //析构函数名也应与类名相同，只是在函数名前面加一个位取反符~
    {
        cout << "Deconstructor method is invoked!" << endl;
    }

    void sayHi()
    {
        cout << "Hi!" << endl;
    }
};

int main()
{   
    A *a = new A(); //动态分配一个类实例对象
    a->sayHi();
    delete a; // 清空内存，会调用 A类的 析构函数

    return 0;
}

运行结果：

Constructor method is invoked!
Hi!
Deconstructor method is invoked!

```




## 标准库vector类  动态大小的数组
```cpp
vector(向量)是 C++中的一种数据结构，也是一个类。
它相当于一个动态的数组，当程序员无法知道自己需要的数组的规模多大时，
用其来解决问题可以达到最大节约空间的目的。

一、定义和初始化
  vector v1; // T为类型名，比如int, float, string等 
  vector v2(v1); // 将v1赋值给v2 
  vector v3(n,i); // v3中含n个值为i的元素

二、操作
  v.empty(); // 判断v是否为空 
  v.size(); // 返回v的长度 
  v.begin(); // 返回v的第一个元素 
  v.end(); // 返回v最后一个元素的下一个元素的值(指向一个不存在的值) 
  v.push_back(a); //在v的最后添加元素a(a必须与v的类型一致)

三、迭代器(iterator)
  迭代器相当于指针，用来储存vector中元素的位置，即下标。
  vector<T>::iteartor iter = v.begin();   //iter指向v第一个元素
  vector<T>::iteartor iter = v.end();     //iter指向v最后一个元素的下一个元素，这个元素不存在，通常用作循环结束的标志
  *iter                                   //*iter指向的元素的值,可对其进行赋值
  iter++                                  //iter指向v下一个元素
  
  常见用法，变量数组元素: 
  for(vector::iterator iter = v.begin(); iter != v.end(); ++iter) 
  { 
  }


#include <iostream>
#include <vector>
using namespace std;

int main(int argc, char** argv) 
{
    vector<int> v;
    v.push_back(1); // [1]
    v.push_back(2); // [1,2]
    v.push_back(3); // [1,2,3]

    cout << "Size of v is: " << v.size() << endl;
    // 遍历数组元素
    for(vector<int>::iterator iter = v.begin(); iter != v.end(); iter++)
    {
        cout << *iter << ' ';   
    }
    cout << endl << endl;

    vector<float> v2(5, 3.33); // 5个 3.33
    cout << "Size of v2 is: " << v2.size() << endl;
    for(vector<float>::iterator iter = v2.begin(); iter != v2.end(); iter++)
    {
        cout << *iter << ' ';   
    }

    return 0;
}


运行结果：

Size of v is 3
1 2 3

Size of v2 is 5
3.33 3.33 3.33 3.33 3.33



```




## 函数模板
```cpp
https://blog.csdn.net/haishu_zheng/article/details/80664515
```




## 内联函数
```cpp
https://blog.csdn.net/haishu_zheng/article/details/80664522
```


## 命名空间
```cpp
https://blog.csdn.net/haishu_zheng/article/details/80679470
```




## cin与scanf，cout与printf的效率比较
```cpp
https://blog.csdn.net/haishu_zheng/article/details/80679481

结论：
1）scanf/printf需要格式化符号%d, %f, %c之类的，这是不如cin/cout方便的地方 
2）cout在控制小数位输出时，很不方便。需要如此操作

#include<iomanip>
cout << fixed << setprecision(5) << endl;   // 输出5位小数

3）对于某些优化过cin和cout的编译器（比如G++）而言，cin/cout的运行效率比scanf/printf高。 
   但是对于没做过优化的编译器，则是scanf/printf的效率大大高于cin/cout。
   互联网上能搜到的文章，几乎都是这种情况。
   这与本篇的实验结果恰好相反。 

4）对于非算法比赛而言，用 cin/cout 或 scanf/printf 无所谓。 
5）但是对于算法比赛而言，因为数据量大，经常会导致超时(TLE–Time limit exceeded)。
   此时可统一使用scanf/printf，
   或者使用加了ios::sync_with_stdio(false); cin.tie(0)的cin/cout。


```


## 实现简易计算器
```cpp
https://blog.csdn.net/haishu_zheng/article/details/84838509
```

## 运算符重载
```cpp
https://blog.csdn.net/haishu_zheng/article/details/86188467
```




## 
```cpp

```




## 
```cpp

```




## 
```cpp

```




## 
```cpp

```




## 
```cpp

```




## 
```cpp

```


