# 05\_Statements

## 语句（Statements）

在 Swift 中，有三种类型的语句：简单语句、编译器控制语句和控制流语句。简单语句是最常见的，用于构造表达式或者声明。编译器控制语句允许程序改变编译器的行为，包含编译配置语句和行控制语句。

控制流语句则用于控制程序执行的流程，Swift 中有多种类型的控制流语句：循环语句、分支语句和控制转移语句。循环语句用于重复执行代码块；分支语句用于执行满足特定条件的代码块；控制转移语句则用于改变代码的执行顺序。另外，Swift 提供了 `do` 语句，用于构建局部作用域，还用于错误的捕获和处理；还提供了 `defer` 语句，用于退出当前作用域之前执行清理操作。

是否将分号（`;`）添加到语句的末尾是可选的。但若要在同一行内写多条独立语句，则必须使用分号。

> 语句语法  _语句_ → [_表达式_](04_expressions.md#expression) **;**可选 _语句_ → [_声明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#declaration) **;**可选 _语句_ → [_循环语句_](05_statements.md#loop-statement) **;**可选 _语句_ → [_分支语句_](05_statements.md#branch-statement) **;**可选 _语句_ → [_带标签的语句_](05_statements.md#labeled-statement) **;**可选 _语句_ → [_控制转移语句_](05_statements.md#control-transfer-statement) **;**可选 _语句_ → [_defer 语句_](05_statements.md#defer-statement) **;**可选 _语句_ → [_do 语句_](05_statements.md#do-statement) **:**可选 _语句_ → [_编译器控制语句_](05_statements.md#compiler-control-statement)  _多条语句_ → [_语句_](05_statements.md#statement) [_多条语句_](05_statements.md#statements)可选

### 循环语句

循环语句会根据特定的循环条件来重复执行代码块。Swift 提供三种类型的循环语句：`for-in` 语句、`while` 语句和 `repeat-while` 语句。

通过 `break` 语句和 `continue` 语句可以改变循环语句的控制流。有关这两条语句，详情参见 [Break 语句](05_statements.md#break_statement) 和 [Continue 语句](05_statements.md#continue_statement)。

> 循环语句语法
>
>  _循环语句_ → [_for-in 语句_](05_statements.md#for-in-statement) _循环语句_ → [_while 语句_](05_statements.md#while-statement) _循环语句_ → [_repeat-while 语句_](05_statements.md#repeat-while-statement)

#### For-In 语句

`for-in` 语句会为集合（或实现了 `SequenceType` 协议的任意类型）中的每一项执行一次代码块。

`for-in` 语句的形式如下：

```swift
for item in collection {
    statements
}
```

`for-in` 语句在循环开始前会调用集合表达式的 `generate()` 方法来获取一个实现了 `GeneratorType` 协议的类型的值。接下来循环开始，反复调用该值的 `next()` 方法。如果其返回值不是 `None`，它将会被赋给“项”，然后执行循环体语句，执行完毕后回到循环开始处，继续重复这一过程；否则，既不会赋值也不会执行循环体语句，`for-in` 语句至此执行完毕。

> for-in 语句语法
>
>  _for-in 语句_ → **for** **case**可选 [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) **in** [_表达式_](04_expressions.md#expression) [_where 子句_](05_statements.md#where-clause)可选 [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#code-block)

#### While 语句

只要循环条件为真，`while` 语句就会重复执行代码块。

`while` 语句的形式如下：

```swift
while condition {
    statements
}
```

`while` 语句的执行流程如下：

1. 判断条件的值。如果为 `true`，转到第 2 步；如果为 `false`，`while` 语句至此执行完毕。
2. 执行循环体中的语句，然后重复第 1 步。

由于会在执行循环体中的语句前判断条件的值，因此循环体中的语句可能会被执行若干次，也可能一次也不会被执行。

条件的结果必须是 Bool 类型或者 Bool 的桥接类型。另外，条件语句也可以使用可选绑定，请参阅 [可选绑定](../chapter2/01_the_basics.md#optional_binding)。

> while 语句语法
>
>  _while 语句_ → **while** [_条件子句_](05_statements.md#condition-clause) [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#code-block)

> _条件子句_ → [_表达式_](04_expressions.md#expression) \| [_表达式_](04_expressions.md#expression) **,** [_条件列表_](05_statements.md#condition-list)  _条件_ → [_表达式_](04_expressions.md#expression) \|[_可用性条件_](05_statements.md#availability-condition) \| [_case 条件_](05_statements.md#case-condition) \| [_可选绑定条件_](05_statements.md#optional-binding-condition)
>
>  _case 条件_ → **case** [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) [_构造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#initializer)  _可选绑定条件_ → **let** [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) [_构造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#initializer) \| **var** [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) [_构造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#initializer)

#### Repeat-While 语句

`repeat-while` 语句至少执行一次代码块，之后只要循环条件为真，就会重复执行代码块。

`repeat-while` 语句的形式如下：

```swift
repeat {
    statements
} while condition
```

`repeat-while` 语句的执行流程如下：

1. 执行循环体中的语句，然后转到第 2 步。
2. 判断条件的值。如果为 `true`，重复第 1 步；如果为 `false`，`repeat-while` 语句至此执行完毕。

由于条件的值是在循环体中的语句执行后才进行判断，因此循环体中的语句至少会被执行一次。

条件的结果必须是 Bool 类型或者 Bool 的桥接类型。另外，条件语句也可以使用可选绑定，请参阅 [可选绑定](../chapter2/01_the_basics.md#optional_binding)。

> repeat-while 语句语法
>
>  _repeat-while 语句_ → **repeat** [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#code-block) **while** [_表达式_](04_expressions.md#expression)

### 分支语句

分支语句会根据一个或者多个条件来执行指定部分的代码。分支语句中的条件将会决定程序如何分支以及执行哪部分代码。Swift 提供两种类型的分支语句：`if` 语句和 `switch` 语句。

`if` 语句和 `switch` 语句中的控制流可以用 `break` 语句改变，请参阅 [Break 语句](05_statements.md#break_statement)。

> 分支语句语法
>
>  _分支语句_ → [_if 语句_](05_statements.md#if-statement) _分支语句_ → [_guard 语句_](05_statements.md#guard-statement) _分支语句_ → [_switch 语句_](05_statements.md#switch-statement)

#### If 语句

`if` 语句会根据一个或多个条件来决定执行哪一块代码。

`if` 语句有两种基本形式，无论哪种形式，都必须有花括号。

第一种形式是当且仅当条件为真时执行代码，像下面这样：

```swift
if condition {
    statements
}
```

第二种形式是在第一种形式的基础上添加 `else` 语句，当只有一个 `else` 语句时，像下面这样：

```swift
if ondition {
    statements to execute if condition is true
} else {
    statements to execute if condition is false
}
```

`else` 语句也可包含 `if` 语句，从而形成一条链来测试更多的条件，像下面这样：

```swift
if condition 1 {
    statements to execute if condition 1 is true
} else if condition 2 {
    statements to execute if condition 2 is true
} else {
    statements to execute if both conditions are false
}
```

`if` 语句中条件的结果必须是 Bool 类型或者 Bool 的桥接类型。另外，条件语句也可以使用可选绑定，请参阅 [可选绑定](../chapter2/01_the_basics.md#optional_binding)。

> if 语句语法
>
>  _if 语句_ → **if** [_条件子句_](05_statements.md#condition-clause) [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#code-block) [_else 子句_](05_statements.md#else-clause)可选  _else 子句_ → **else** [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#code-block) \| **else** [_if 语句_](05_statements.md#if-statement)

#### Guard 语句

如果一个或者多个条件不成立，可用 `guard` 语句用来退出当前作用域。

`guard` 语句的格式如下：

```swift
guard condition else {
    statements
}
```

`guard` 语句中条件的结果必须是 Bool 类型或者 Bool 的桥接类型。另外，条件也可以是一条可选绑定，请参阅 [可选绑定](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/01_The_Basics.html#optional_binding)。

在 `guard` 语句中进行可选绑定的常量或者变量，其可用范围从声明开始直到作用域结束。

`guard` 语句必须有 `else` 子句，而且必须在该子句中调用 `Never` 返回类型的函数，或者使用下面的语句退出当前作用域：

* `return`
* `break`
* `continue`
* `throw`

关于控制转移语句，请参阅 [控制转移语句](05_statements.md#control_transfer_statements)。关于 `Never` 返回类型的函数，请参阅 [永不返回的函数](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.md#rethrowing_functions_and_methods)。

> guard 语句语法
>
>  _guard 语句_ → **guard** [_条件子句_](05_statements.md#condition-clause) **else** \[_代码块_\] \(05\_Declarations.html\#code-block\)

#### Switch 语句

`switch` 语句会根据控制表达式的值来决定执行哪部分代码。

`switch` 语句的形式如下：

```swift
switch control expression {
case pattern 1:
    statements
case pattern 2 where condition:
    statements
case pattern 3 where condition,
     pattern 4 where condition:
    statements
default:
    statements
}
```

`switch` 语句会先计算_控制表达式_的值，然后与每一个 `case` 的模式进行匹配。如果匹配成功，程序将会执行对应的 `case` 中的语句。另外，每一个 `case` 都不能为空，也就是说在每一个 `case` 中必须至少有一条语句。如果你不想在匹配到的 `case` 中执行代码，只需在该 `case` 中写一条 `break` 语句即可。

可以用作控制表达式的值是十分灵活的。除了标量类型外，如 `Int`、`Character`，你可以使用任何类型的值，包括浮点数、字符串、元组、自定义类型的实例和可选类型。控制表达式的值还可以用来匹配枚举类型中的成员值或是检查该值是否包含在指定的 `Range` 中。关于如何在 `switch` 语句中使用这些类型，请参阅 [控制流](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html) 一章中的 [Switch](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#switch)。

每个 `case` 的模式后面可以有一个 `where` 子句。`where` 子句由 `where` 关键字紧跟一个提供额外条件的表达式组成。因此，当且仅当控制表达式匹配一个 `case` 的模式且 `where` 子句的表达式为真时，`case` 中的语句才会被执行。在下面的例子中，控制表达式只会匹配包含两个相等元素的元组，例如 `(1, 1)`：

```swift
case let (x, y) where x == y:
```

正如上面这个例子，也可以在模式中使用 `let`（或 `var`）语句来绑定常量（或变量）。这些常量（或变量）可以在对应的 `where` 子句以及 `case` 中的代码中使用。但是，如果一个 `case` 中含有多个模式，所有的模式必须包含相同的常量（或变量）绑定，并且每一个绑定的常量（或变量）必须在所有的条件模式中都有相同的类型。

`switch` 语句也可以包含默认分支，使用 `default` 关键字表示。只有所有 `case` 都无法匹配控制表达式时，默认分支中的代码才会被执行。一个 `switch` 语句只能有一个默认分支，而且必须在 `switch` 语句的最后面。

`switch` 语句中 `case` 的匹配顺序和源代码中的书写顺序保持一致。因此，当多个模式都能匹配控制表达式时，只有第一个匹配的 `case` 中的代码会被执行。

**Switch 语句不能有遗漏**

在 Swift 中，`switch` 语句中控制表达式的每一个可能的值都必须至少有一个 `case` 与之对应。在某些无法面面俱到的情况下（例如，表达式的类型是 `Int`），你可以使用 `default` 分支满足该要求。

**不存在隐式落入**

当匹配到的 `case` 中的代码执行完毕后，`switch` 语句会直接退出，而不会继续执行下一个 `case` 。这就意味着，如果你想执行下一个 `case`，需要显式地在当前 `case` 中使用 `fallthrough` 语句。关于 `fallthrough` 语句的更多信息，请参阅 [Fallthrough 语句](05_statements.md#fallthrough_statements)。

> switch 语句语法
>
>  _switch 语句_ → **switch** [_表达式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/04_Expressions.html#expression) **{** [_switch-case 列表_](05_statements.md#switch-cases)可选 **}**  _switch case 列表_ → [_switch-case_](05_statements.md#switch-case) [_switch-case 列表_](05_statements.md#switch-cases)可选  _switch case_ → [_case 标签_](05_statements.md#case-label) [_多条语句_](05_statements.md#statements) \| [_default 标签_](05_statements.md#default-label) [_多条语句_](05_statements.md#statements)

> _case 标签_ → **case** [_case 项列表_](05_statements.md#case-item-list) **:**  _case 项列表_ → [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) [_where 子句_](05_statements.md#where-clause)可选 \| [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.md#pattern) [_where 子句_](05_statements.md#where-clause)可选 **,** [_case 项列表_](05_statements.md#case-item-list)  _default 标签_ → **default** **:**
>
>  _where-clause_ → **where** [_where 表达式_](05_statements.md#where-expression)  _where-expression_ → [_表达式_](04_expressions.md#expression)

### 带标签的语句

你可以在循环语句或 `switch` 语句前面加上标签，它由标签名和紧随其后的冒号（`:`）组成。在 `break` 和 `continue` 后面跟上标签名可以显式地在循环语句或 `switch` 语句中改变相应的控制流。关于这两条语句用法，请参阅 [Break 语句](05_statements.md#break_statement) 和 [Continue 语句](05_statements.md#continue_statement)。

标签的作用域在该标签所标记的语句内。可以嵌套使用带标签的语句，但标签名必须唯一。

关于使用带标签的语句的例子，请参阅 [控制流](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html) 一章中的 [带标签的语句](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#labeled_statements)。

> 带标签的语句语法
>
>  _带标签的语句_ → [_语句标签_](05_statements.md#statement-label) [_循环语句_](05_statements.md#loop-statement) _带标签的语句_ → [_语句标签_](05_statements.md#statement-label) [_if 语句_](05_statements.md#if-statement) _带标签的语句_ → [_语句标签_](05_statements.md#statement-label) [_switch 语句_](05_statements.md#switch-statement)
>
> > _带标签的语句_ → [_语句标签_](05_statements.md#statement-label) [_do 语句_](05_statements.md#sdo-statement)  _语句标签_ → [_标签名称_](05_statements.md#label-name) **:**  _标签名称_ → [_标识符_](02_lexical_structure.md#identifier)

### 控制转移语句

控制转移语句能够无条件地把控制权从一片代码转移到另一片代码，从而改变代码执行的顺序。Swift 提供五种类型的控制转移语句：`break` 语句、`continue` 语句、`fallthrough` 语句、`return` 语句和 `throw` 语句。

> 控制转移语句语法
>
>  _控制转移语句_ → [_break 语句_](05_statements.md#break-statement) _控制转移语句_ → [_continue 语句_](05_statements.md#continue-statement) _控制转移语句_ → [_fallthrough 语句_](05_statements.md#fallthrough-statement) _控制转移语句_ → [_return 语句_](05_statements.md#return-statement) _控制转移语句_ → [_throw 语句_](05_statements.md#throw-statement)

#### Break 语句

`break` 语句用于终止循环语句、`if` 语句或 `switch` 语句的执行。使用 `break` 语句时，可以只写 `break` 这个关键词，也可以在 `break` 后面跟上标签名，像下面这样：

> break break `label name`

当 `break` 语句后面带标签名时，可用于终止由这个标签标记的循环语句、`if` 语句或 `switch` 语句的执行。

而只写 `break` 时，则会终止 `switch` 语句或 `break` 语句所属的最内层循环语句的执行。不能使用 `break` 语句来终止未使用标签的 `if` 语句。

无论哪种情况，控制权都会被转移给被终止的控制流语句后面的第一行语句。

关于使用 `break` 语句的例子，请参阅 [控制流](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html) 一章的 [Break](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#break) 和 [带标签的语句](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#labeled_statements)。

> break 语句语法
>
>  _break 语句_ → **break** [_标签名称_](05_statements.md#label-name)可选

#### Continue 语句

`continue` 语句用于终止循环中当前迭代的执行，但不会终止该循环的执行。使用 `continue` 语句时，可以只写 `continue` 这个关键词，也可以在 `continue` 后面跟上标签名，像下面这样：

> continue continue `label name`

当 `continue` 语句后面带标签名时，可用于终止由这个标签标记的循环中当前迭代的执行。

而当只写 `continue` 时，可用于终止 `continue` 语句所属的最内层循环中当前迭代的执行。

在这两种情况下，控制权都会被转移给循环语句的条件语句。

在 `for` 语句中，`continue` 语句执行后，增量表达式还是会被计算，这是因为每次循环体执行完毕后，增量表达式都会被计算。

关于使用 `continue` 语句的例子，请参阅 [控制流](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html) 一章的 [Continue](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#continue) 和 [带标签的语句](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#labeled_statements)。

> continue 语句语法
>
>  _continue 语句_ → **continue** [_标签名称_](05_statements.md#label-name)可选

#### Fallthrough 语句

`fallthrough` 语句用于在 `switch` 语句中转移控制权。`fallthrough` 语句会把控制权从 `switch` 语句中的一个 `case` 转移到下一个 `case`。这种控制权转移是无条件的，即使下一个 `case` 的模式与 `switch` 语句的控制表达式的值不匹配。

`fallthrough` 语句可出现在 `switch` 语句中的任意 `case` 中，但不能出现在最后一个 `case` 中。同时，`fallthrough` 语句也不能把控制权转移到使用了值绑定的 `case`。

关于在 `switch` 语句中使用 `fallthrough` 语句的例子，请参阅 [控制流](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html) 一章的 [控制转移语句](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/05_Control_Flow.html#control_transfer_statements)。

> fallthrough 语句语法
>
>  _fallthrough 语句_ → **fallthrough**

#### Return 语句

`return` 语句用于在函数或方法的实现中将控制权转移到调用函数或方法，接着程序将会从调用位置继续向下执行。

使用 `return` 语句时，可以只写 `return` 这个关键词，也可以在 `return` 后面跟上表达式，像下面这样：

> return return `expression`

当 `return` 语句后面带表达式时，表达式的值将会返回给调用函数或方法。如果表达式的值的类型与函数或者方法声明的返回类型不匹配，Swift 则会在返回表达式的值之前将表达式的值的类型转换为返回类型。

> 注意
>
> 正如 [可失败构造器](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.html#failable_initializers) 中所描述的，`return nil` 在可失败构造器中用于表明构造失败。

而只写 `return` 时，仅仅是从该函数或方法中返回，而不返回任何值（也就是说，函数或方法的返回类型为 `Void` 或者说 `()`）。

> return 语句语法
>
>  _return 语句_ → **return** [_表达式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/04_Expressions.html#expression)可选

#### Throw 语句

`throw` 语句出现在抛出函数或者抛出方法体内，或者类型被 `throws` 关键字标记的闭包表达式体内。

`throw` 语句使程序在当前作用域结束执行，并向外围作用域传播错误。抛出的错误会一直传递，直到被 `do` 语句的 `catch` 子句处理掉。

`throw` 语句由 `throw` 关键字紧跟一个表达式组成，如下所示：

> throw `expression`

表达式的结果必须符合 `ErrorType` 协议。

关于如何使用 `throw` 语句的例子，请参阅 [错误处理](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/18_Error_Handling.html) 一章的 [用 throwing 函数传递错误](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/18_Error_Handling.html#propagating_errors_using_throwing_functions)。

> throw 语句语法
>
>  _throw 语句_ → **throw** [_表达式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/04_Expressions.html#expression)

### Defer 语句

`defer` 语句用于在退出当前作用域之前执行代码。

`defer` 语句形式如下：

```swift
defer {
    statements
}
```

在 `defer` 语句中的语句无论程序控制如何转移都会被执行。在某些情况下，例如，手动管理资源时，比如关闭文件描述符，或者即使抛出了错误也需要执行一些操作时，就可以使用 `defer` 语句。

如果多个 `defer` 语句出现在同一作用域内，那么它们执行的顺序与出现的顺序相反。给定作用域中的第一个 `defer` 语句，会在最后执行，这意味着代码中最靠后的 `defer` 语句中引用的资源可以被其他 `defer` 语句清理掉。

```swift
func f() {
    defer { print("First") }
    defer { print("Second") }
    defer { print("Third") }
}
f()
// 打印“Third”
// 打印“Second”
// 打印“First”
```

`defer` 语句中的语句无法将控制权转移到 `defer` 语句外部。

> defer 语句语法
>
>  _延迟语句_ → **defer** [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.html#code-block)

### Do 语句

`do` 语句用于引入一个新的作用域，该作用域中可以含有一个或多个 `catch` 子句，`catch` 子句中定义了一些匹配错误条件的模式。`do` 语句作用域内定义的常量和变量只能在 `do` 语句作用域内使用。

Swift 中的 `do` 语句与 C 中限定代码块界限的大括号（`{}`）很相似，也并不会降低程序运行时的性能。

`do` 语句的形式如下：

```swift
do {
    try expression
    statements
} catch pattern 1 {
    statements
} catch pattern 2 where condition {
    statements
}
```

如同 `switch` 语句，编译器会判断 `catch` 子句是否有遗漏。如果 `catch` 子句没有遗漏，则认为错误已被处理。否则，错误会自动传递到外围作用域，被某个 `catch` 子句处理掉或者被用 `throws` 关键字声明的抛出函数继续向外抛出。

为了确保错误已经被处理，可以让 `catch` 子句使用匹配所有错误的模式，如通配符模式（`_`）。如果一个 `catch` 子句不指定一种具体模式，`catch` 子句会匹配任何错误，并绑定到名为 `error` 的局部常量。有关在 `catch` 子句中使用模式的更多信息，请参阅 [模式](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.html)。

关于如何在 `do` 语句中使用一系列 `catch` 子句的例子，请参阅 [错误处理](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/17_Error_Handling.html#handling_errors)。

> do 语句语法
>
>  _do 语句_ → **do** [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.html#code-block) [_多条 catch 子句_](05_statements.md#catch-clauses)可选  _多条 catch 子句_ → [_catch 子句_](05_statements.md#catch-clause) [_多条 catch 子句_](05_statements.md#catch-clauses)可选  _catch 子句_ → **catch** [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/07_Patterns.html#pattern)可选 [_where 子句_](05_statements.md#where-clause)可选 [_代码块_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.html#code-block)

### 编译器控制语句

编译器控制语句允许程序改变编译器的行为。Swift 有两种编译器控制语句：编译配置语句和线路控制语句。

> 编译器控制语句语法
>
>  _编译器控制语句_ → [_编译配置语句_](05_statements.md#build-config-statement) _编译器控制语句_ → [_线路控制语句_](05_statements.md#line-control-statement)

#### 条件性编译块

条件性编译块可以根据一个或多个配置来有条件地编译代码。

每一个条件性编译块都以 `#if` 开始，`#endif` 结束。如下是一个简单的条件性编译块：

```swift
#if compilation condition
statements
#endif
```

和 `if` 语句的条件不同，编译配置的条件是在编译时进行判断的。只有编译配置在编译时判断为 `true` 的情况下，相应的语句才会被编译和执行。

编译配置可以是 `true` 和 `false` 的字面量，也可以是使用 `-D` 命令行标志的标识符，或者是下列表格中的任意一个平台检测函数。

| 函数 | 可用参数 |
| :--- | :--- |
| `os()` | `OSX`, `iOS`, `watchOS`, `tvOS`, `Linux` |
| `arch()` | `i386`, `x86_64`, `arm`, `arm64` |
| `swift()` | `>=` 后跟版本号 |

`swift()`（语言版本检测函数）的版本号参数主要由主版本号和次版本号组成并且使用点号（`.`）分隔开，`>=` 和版本号之间不能有空格。

> 注意
>
> `arch(arm)` 平台检测函数在 ARM 64 位设备上不会返回 `true`。如果代码在 32 位的 iOS 模拟器上编译，`arch(i386)` 平台检测函数会返回 `true`。

你可以使用逻辑操作符 `&&`、`||` 和 `!` 来组合多个编译配置，还可以使用圆括号来进行分组。

就像 `if` 语句一样，你可以使用 `#elseif` 子句来添加任意多个条件分支来测试不同的编译配置。你也可以使用 `#else` 子句来添加最终的条件分支。包含多个分支的编译配置语句例子如下：

```swift
#if compilation condition 1
statements to compile if compilation condition 1 is true
#elseif compilation condition 2
statements to compile if compilation condition 2 is true
#else
statements to compile if both compilation conditions are false
#endif
```

> 注意
>
> 即使没有被编译，编译配置中的语句仍然会被解析。然而，唯一的例外是编译配置语句中包含语言版本检测函数：仅当 `Swift` 编译器版本和语言版本检测函数中指定的版本号匹配时，语句才会被解析。这种设定能确保旧的编译器不会尝试去解析新 Swift 版本的语法。

> 编译配置语句语法
>
>  _单个编译配置语句_ → **if** [_编译配置_](05_statements.md#build-configuration) [_语句_](05_statements.md#statements)可选 [_多个编译配置 elseif 子句_](05_statements.md#build-configuration-elseif-clauses)可选 **-** [_单个编译配置 else 子句_](05_statements.md#build-configuration-else-clause)可选 **\#endif**  _多个编译配置 elseif 子句_ → [_单个编译配置 elseif 子句_](05_statements.md#build-configuration-elseif-clause) [_多个编译配置 elseif 子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/build-configuration-elseif-clauses/README.md)可选  _单个编译配置 elseif 子句_ → **\#elseif** [_编译配置_](05_statements.md#build-configuration) [_语句_](05_statements.md#statements)可选  _单个编译配置 else 子句_ → **\#else** [_语句_](05_statements.md#statements)可选

> _编译配置_ → [_平台检测函数_](05_statements.md#platform-testing-function) _编译配置_ → [_语言版本检测函数_](05_statements.md#language-version-testing-function) _编译配置_ → [_标识符_](02_lexical_structure.md#identifier) _编译配置_ → [_布尔值字面量_](02_lexical_structure.md#boolean-literal) _编译配置_ → **\(** [_编译配置_](05_statements.md#build-configuration) **\)** _编译配置_ → **!** [_编译配置_](05_statements.md#build-configuration) _编译配置_ → [_编译配置_](05_statements.md#build-configuration) **&&** [_编译配置_](05_statements.md#build-configuration) _编译配置_ → [_编译配置_](05_statements.md#build-configuration) **\|\|** [_编译配置_](05_statements.md#build-configuration)

> _平台检测函数_ → **os** **\(** [_操作系统_](05_statements.md#operating-system) **\)** _平台检测函数_ → **arch** **\(** [_架构_](05_statements.md#architecture) **\)**  _语言版本检测函数_ → **swift** **\(** **&gt;=** [_swift 版本_](05_statements.md#swift-version) **\)**  _操作系统_ → **OSX** \| **iOS** \| **watchOS** \| **tvOS**  _架构_ → **i386** \| **x86\_64** \| **arm** \| **arm64**  _swift 版本_ → [_十进制数字_](02_lexical_structure.md#decimal-digit) ­**.** ­[_十进制数字_](02_lexical_structure.md#decimal-digit)

#### 行控制语句

行控制语句可以为被编译的源代码指定行号和文件名，从而改变源代码的定位信息，以便进行分析和调试。

行控制语句形式如下：

> \#sourceLocation\(file: `filename` , line:`line number`\)
>
> \#sourceLocation\(\)

第一种的行控制语句会改变该语句之后的代码中的字面量表达式 `#line` 和 `#file` 所表示的值。`行号` 是一个大于 0 的整形字面量，会改变 `#line` 表达式的值。`文件名` 是一个字符串字面量，会改变 `#file` 表达式的值。

第二种的行控制语句，`#sourceLocation()`，会将源代码的定位信息重置回默认的行号和文件名。

> 行控制语句语法
>
> _行控制语句_ → **\#sourceLocation\(file:**[_**文件名**_](05_statements.md#file-name)**,line:**[_**行号**_](05_statements.md#line-number)**\)** _行控制语句_ → **\#sourceLocation\(\)**  _行号_ → 大于 0 的十进制整数  _文件名_ → [_静态字符串字面量_](02_lexical_structure.md#static-string-literal)

#### 可用性条件

可用性条件可作为 `if`，`while`，`guard` 语句的条件，可以在运行时基于特定的平台参数来查询 API 的可用性。

可用性条件的形式如下：

```swift
if #available(platform name version, ..., *) {
    statements to execute if the APIs are available
} else {
    fallback statements to execute if the APIs are unavailable
}
```

使用可用性条件来执行一个代码块时，取决于使用的 API 在运行时是否可用，编译器会根据可用性条件提供的信息来决定是否执行相应的代码块。

可用性条件使用一系列逗号分隔的平台名称和版本。使用 `iOS`，`OSX`，以及 `watchOS` 等作为平台名称，并写上相应的版本号。`*` 参数是必须写的，用于处理未来的潜在平台。可用性条件确保了运行时的平台不低于条件中指定的平台版本时才执行代码块。

与布尔类型的条件不同，不能用逻辑运算符 `&&` 和 `||` 组合可用性条件。

> 可用性条件语法
>
>  _可用性条件_ → **\#available** **\(** [_可用性参数列表_](05_statements.md#availability-arguments) **\)**  _可用性参数列表_ → [_可用性参数_](05_statements.md#availability-argument) \| [_可用性参数_](05_statements.md#availability-argument) **,** [_可用性参数列表_](05_statements.md#availability-arguments)  _可用性参数_ → [平台名称](05_statements.md#platform-name) [平台版本](05_statements.md#platform-version) _可用性条件_ → **\***
>
>  _平台名称_ → **iOS** \| **iOSApplicationExtension** _平台名称_ → **OSX** \| **macOSApplicationExtension** _平台名称_ → **watchOS** _平台名称_ → **tvOS**  _平台版本_ → [十进制数字](02_lexical_structure.md#decimal-digits) _平台版本_ → [十进制数字](02_lexical_structure.md#decimal-digits) **.** [十进制数字](02_lexical_structure.md#decimal-digits) _平台版本_ → [十进制数字](02_lexical_structure.md#decimal-digits) **.** [十进制数字](02_lexical_structure.md#decimal-digits) **.** [十进制数字](02_lexical_structure.md#decimal-digits)

