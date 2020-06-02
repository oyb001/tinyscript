# tinyscript

整个项目包括三个东西：
1. 创建了一个自己的语言
2. 编译器
3. 虚拟机
 
golang实现的一个编译器，用来编译一个自己创建的语言（用来玩的），最后写了一个自定义虚拟机用来运行自定义语言。


## 语言介绍

为了跨平台（其实是为了方便开发 ^ ^），所以这个语言没有静态编译成硬件指令集，最后的机器码是我自己的定义的，和MIPS类似的（其实就是一个mips子集）虚拟指令集。为了运行这些指令集，我写了一个虚拟机。


语言和golang和javascript类似，实现了函数，类型声明，函数调用等最基本的一些语言元素，没有实现类，结构体，接口等复杂数据结构。
下面是用这个语言编程的例子：
```
func fact(int n)  int {
    if(n == 0) {
        return 1
    }
    return fact(n-1) * n
}
func main() void {
    return fact(2)
}
```

每个函数都实现了相应的UnitTest，单元测试真香～

## 声明：
工程思路不是我自己想出来的，来自于慕课网《大学计算机必修课新讲--编译原理+操作系统+图形学》这个课程。
理论主要是看《龙书》的一部分，《自己动手写编译器，连接器》和bilibili上的中科大华保健老师的《编译原理》和哈尔滨工业大学的《编译原理》课程的一部分。

