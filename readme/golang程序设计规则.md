Go语言程序设计中的简约规则：

1. Go编程的风格，可以以组为单位进行申明变量和常量，以及加载包。//按组处理

2. Go语言支持简单的函数，条件和循环风格，把括号都给省掉了。//省略写法

3. 大写字母开头的变量是可导出的（即其它包可以读取，是公用变量）；小写字母开头的就是不可导出的（是私有变量）。//public变量和private变量

4. 大写字母开头的函数也是一样，相当于class中的带public关键词的公有函数；小写字母开头的就是有private关键词的私有函数。//public函数和private函数

5. go语言是不需要以分号结尾的。

6. Go语言是支持函数返回多个值。

总结：go是以包为程序组织单位，以包作为空间作用域，且以大小写字母开头来标识public和private的访问属性！（相对于class简化了很多，而且具有极固定的规则）


具体操作：

var 声明变量。

const 创建常量。

iota 这个关键字用来声明enum的时候采用，它默认开始值是0，每调用一次加1。

map 也就是Python中字典的概念，它的格式为map[keyType]valueType map的读取和设置也类似slice一样，通过key来操作，只是slice的index只能是int类型，而map多了很多类型，可以是int，可以是string。

make 用于内建类型（map、 slice和channel）的内存分配。

new 用于各种类型的内存分配。

goto 跳转到必须在当前函数内定义的标签。

func 关键字func用来声明一个函数funcName。

defer 延迟执行代码，类似于析构函数。

panic 中断原有的控制流程。

recover 恢复中断的函数。

import 导入包文件。

Go里面有两个保留的函数：init函数（能够应用于所有的package）和main函数（只能应用于package main）。
这两个函数在定义时不能有任何的参数和返回值。
虽然一个package里面可以写任意多个init函数，但这无论是对于可读性还是以后的可维护性来说，都强烈建议用户在一个package中每个文件只写一个init函数。
Go程序会自动调用init()和main()，所以你不需要在任何地方调用这两个函数。每个package中的init函数都是可选的，但package main就必须包含一个main函数。
