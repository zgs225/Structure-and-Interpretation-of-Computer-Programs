构造过程抽象
===

**计算过程**是存在与计算机中的一类抽象事物，使用**程序**的特殊规则，去
操作称之为**数据**的抽象事物。设计良好的程序设计，具有**模块化**的设计，
其中的各个部分都可以独立地构造、替换、排除错误。

##程序设计的基本元素

+ 基本的表达形式
+ 组合的方法
+ 抽象的方法

以上，是基于对人类心智活动的总结。

### Namespace and Environment

`(define size 2)`

`define`是一种最简单的抽象方法，它使用一个简单的名字去引用一组计算。
环境是具有普遍性的概念，它为求职过程的提供了一种上下文，对于程序的执行
起到至关重要的作用。与一般性求职规则对应的是特殊形式。`define`是第一
种特殊形式。

### Procedure definition

The typical fomular is:

    (define (<name> <formal parameters>) <body>)

For example, `(define (square x) (* x x))`.

###应用序和正则序

完全展开而后约的求值模型成为**正则序求值**，先求值参数而后应用的形式，
称为**应用序求值**。

###条件表达式和谓词

条件表达式的一般形式为：

    (cond (<p1> <e1>)
          (<p2> <e2>)
          ...
          (<pn> <en>)
    )

举例说明：

    (define (abs x)
      (cond ((> x 0) x)
            ((= x 0) 0)
            ((< x 0) (- x))))

另外一种`if`形式：

    (if <predicate> <consequent> <alternative>)

举例说明：

    (define (abs x)
      (if (< x 0)
          (- x)
          x))

其他常用逻辑复合运算符：
+ `(and <e1>...<en>)`
+ `(or  <e1>...<en>)`
+ `(not <e>)`
