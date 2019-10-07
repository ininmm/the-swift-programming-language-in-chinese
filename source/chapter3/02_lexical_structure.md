# 词法结构（Lexical Structure）

Swift 的_“词法结构（lexical structure）”_ 描述了能构成该语言中有效符号（token）的字符序列。这些合法符号组成了语言中最底层的构建基块，并在之后的章节中用于描述语言的其他部分。一个合法符号由一个标识符（identifier）、关键字（keyword）、标点符号（punctuation）、字面量（literal）或运算符（operator）组成。

通常情况下，通过考虑输入文本当中可能的最长子串，并且在随后将介绍的语法约束之下，根据随后将介绍的语法约束生成的，根据 Swift 源文件当中的字符来生成相应的“符号”。这种方法称为_“最长匹配（longest match）”_，或者_“最大适合（maximal munch）”_。

## 空白与注释 <a id="whitespace_and_comments"></a>

空白（whitespace）有两个用途：分隔源文件中的符号以及帮助区分运算符属于前缀还是后缀（参见 [运算符](02_lexical_structure.md#operators)），在其他情况下空白则会被忽略。以下的字符会被当作空白：空格（U+0020）、换行符（U+000A）、回车符（U+000D）、水平制表符（U+0009）、垂直制表符（U+000B）、换页符（U+000C）以及空字符（U+0000）。

注释被编译器当作空白处理。单行注释由 `//` 开始直至遇到换行符（U+000A）或者回车符（U+000D）。多行注释由 `/*` 开始，以 `*/` 结束。注释允许嵌套，但注释标记必须匹配。

> 空白语法

> _空白_ → [_空白项_](02_lexical_structure.md#whitespace-item) [_空白_](02_lexical_structure.md#whitespace)可选 _空白项_ → [_断行符_](02_lexical_structure.md#line-break) _空白项_ → [_注释_](02_lexical_structure.md#comment) _空白项_ → [_多行注释_](02_lexical_structure.md#multiline-comment) _空白项_ → U+0000，U+0009，U+000B，U+000C 或者 U+0020

> _断行符_ → U+000A _断行符_ → U+000D _断行符_ → U+000D 接着是 U+000A

> _注释_ → // [_注释内容 断行_](02_lexical_structure.md#comment-text%20line-break) _多行注释_ → `/*` [_多行注释内容_](02_lexical_structure.md#multiline-commnet-text) `*/` _注释内容_ → [_注释内容项_](02_lexical_structure.md#comment-text-item) [_注释内容_](02_lexical_structure.md#comment-text)可选 _注释内容项_ → 任何 Unicode 标量值， 除了 U+000A 或者 U+000D _多行注释内容_ → [_多行注释内容项_](02_lexical_structure.md#multiline-comment-text-item) [_多行注释内容_](02_lexical_structure.md#multiline-comment-text)可选 _多行注释内容项_ → [_多行注释_](02_lexical_structure.md#multiline-comment). _多行注释内容项_ → [_注释内容项_](02_lexical_structure.md#comment-text-item) _多行注释内容项_ → 任何 Unicode 标量值， 除了 `/*` 或者 `*/`

注释可以包含额外的格式和标记，正如 [_Markup Formatting Reference_](https://developer.apple.com/library/prerelease/ios/documentation/Xcode/Reference/xcode_markup_formatting_ref/index.html#//apple_ref/doc/uid/TP40016497) 所述。

## 标识符 <a id="identifiers"></a>

_标识符（identifier）_ 可以由以下的字符开始：大写或小写的字母 `A` 到 `Z`、下划线（`_`）、基本多文种平面（Basic Multilingual Plane）中非字符数字组合的 Unicode 字符以及基本多文种平面以外的非个人专用区字符。在首字符之后，允许使用数字和组合 Unicode 字符。

使用保留字作为标识符，需要在其前后增加反引号（````` ）。例如，`class` 不是合法的标识符，但可以使用 ```class``` 。反引号不属于标识符的一部分，```x```  和 `x` 表示同一标识符。

闭包中如果没有明确指定参数名称，参数将被隐式命名为 `$0`、`$1`、`$2` 等等。这些命名在闭包作用域范围内是合法的标识符。

> 标识符语法

> _标识符_ → [_头部标识符_](02_lexical_structure.md#identifier-head) [_标识符字符组_](02_lexical_structure.md#identifier-characters)可选 _标识符_ → \`[_头部标识符_](02_lexical_structure.md#identifier-head) [_标识符字符组_](02_lexical_structure.md#identifier-characters)可选\` _标识符_ → [_隐式参数名_](02_lexical_structure.md#implicit-parameter-name)

> _标识符列表_ → [_标识符_](02_lexical_structure.md#identifier) \| [_标识符_](02_lexical_structure.md#identifier) **,** [_标识符列表_](02_lexical_structure.md#identifier-list)

> _头部标识符_ → 大写或小写字母 A - Z _头部标识符_ → \_ _头部标识符_ → U+00A8，U+00AA，U+00AD，U+00AF，U+00B2–U+00B5，或者 U+00B7–U+00BA _头部标识符_ → U+00BC–U+00BE，U+00C0–U+00D6，U+00D8–U+00F6，或者 U+00F8–U+00FF _头部标识符_ → U+0100–U+02FF，U+0370–U+167F，U+1681–U+180D，或者 U+180F–U+1DBF _头部标识符_ → U+1E00–U+1FFF _头部标识符_ → U+200B–U+200D，U+202A–U+202E，U+203F–U+2040，U+2054，或者 U+2060–U+206F _头部标识符_ → U+2070–U+20CF，U+2100–U+218F，U+2460–U+24FF，或者 U+2776–U+2793 _头部标识符_ → U+2C00–U+2DFF 或者 U+2E80–U+2FFF _头部标识符_ → U+3004–U+3007，U+3021–U+302F，U+3031–U+303F，或者 U+3040–U+D7FF _头部标识符_ → U+F900–U+FD3D，U+FD40–U+FDCF，U+FDF0–U+FE1F，或者 U+FE30–U+FE44 _头部标识符_ → U+FE47–U+FFFD _头部标识符_ → U+10000–U+1FFFD，U+20000–U+2FFFD，U+30000–U+3FFFD，或者 U+40000–U+4FFFD _头部标识符_ → U+50000–U+5FFFD，U+60000–U+6FFFD，U+70000–U+7FFFD，或者 U+80000–U+8FFFD _头部标识符_ → U+90000–U+9FFFD，U+A0000–U+AFFFD，U+B0000–U+BFFFD，或者 U+C0000–U+CFFFD _头部标识符_ → U+D0000–U+DFFFD 或者 U+E0000–U+EFFFD

> _标识符字符_ → 数值 0 - 9 _标识符字符_ → U+0300–U+036F，U+1DC0–U+1DFF，U+20D0–U+20FF，或者 U+FE20–U+FE2F _标识符字符_ → [_头部标识符_](02_lexical_structure.md#identifier-head)  _标识符字符组_ → [_标识符字符_](02_lexical_structure.md#identifier-character) [_标识符字符组_](02_lexical_structure.md#identifier-characters)可选

> _隐式参数名_ → **$** [_十进制数字列表_](02_lexical_structure.md#decimal-digits)

## 关键字和标点符号 <a id="keywords"></a>

下面这些被保留的关键字不允许用作标识符，除非使用反引号转义，具体描述请参考 [标识符](02_lexical_structure.md#identifiers)。除了 `inout`、`var` 以及 `let` 之外的关键字可以用作某个函数声明或者函数调用当中的外部参数名，不用添加反引号转义。

* 用在声明中的关键字： `associatedtype`、`class`、`deinit`、`enum`、`extension`、`func`、`import`、`init`、`inout`、`internal`、`let`、`operator`、`private`、`protocol`、`public`、`static`、`struct`、`subscript`、`typealias` 以及 `var`。
* 用在语句中的关键字：`break`、`case`、`continue`、`default`、`defer`、`do`、`else`、`fallthrough`、`for`、`guard`、`if`、`in`、`repeat`、`return`、`switch`、`where` 以及 `while`。
* 用在表达式和类型中的关键字：`as`、`catch`、`dynamicType`、`false`、`is`、`nil`、`rethrows`、`super`、`self`、`Self`、`throw`、`throws`、`true`、`try`、`#column`、`#file`、`#function` 以及 `#line`。
* 用在模式中的关键字：`_`。
* 以井字号（`#`）开头的关键字：`#available`、`#column`、`#else#elseif`、`#endif`、`#file`、`#function`、`#if`、`#line` 以及 `#selector`。
* 特定上下文中被保留的关键字： `associativity`、`convenience`、`dynamic`、`didSet`、`final`、`get`、`infix`、`indirect`、`lazy`、`left`、`mutating`、`none`、`nonmutating`、`optional`、`override`、`postfix`、`precedence`、`prefix`、`Protocol`、`required`、`right`、`set`、`Type`、`unowned`、`weak` 以及 `willSet`。这些关键字在特定上下文之外可以被用做标识符。

以下符号被当作保留符号，不能用于自定义运算符： `(`、`)`、`{`、`}`、`[`、`]`、`.`、`,`、`:`、`;`、`=`、`@`、`#`、`&`（作为前缀运算符）、`->`、````` 、`?`、`!`（作为后缀运算符）。

## 字面量 <a id="literals"></a>

_字面量（literal）_ 用来表示源码中某种特定类型的值，比如一个数字或字符串。

下面是字面量的一些示例：

```swift
42              // 整数字面量
3.14159         // 浮点数字面量
"Hello, world!" // 字符串字面量
true            // 布尔值字面量
```

字面量本身并不包含类型信息。事实上，一个字面量会被解析为拥有无限的精度，然后 Swift 的类型推导会尝试去推导出这个字面量的类型。比如，在 `let x: Int8 = 42` 这个声明中，Swift 使用了显式类型标注（`: Int8`）来推导出 `42` 这个整数字面量的类型是 `Int8`。如果没有可用的类型信息， Swift 则会从标准库中定义的字面量类型中推导出一个默认的类型。整数字面量的默认类型是 `Int`，浮点数字面量的默认类型是 `Double`，字符串字面量的默认类型是 `String`，布尔值字面量的默认类型是 `Bool`。比如，在 `let str = "Hello, world"` 这个声明中，字符串 `"Hello, world"` 的默认推导类型就是 `String`。

当为一个字面量值指定了类型标注的时候，这个标注的类型必须能通过这个字面量值实例化。也就是说，这个类型必须符合这些 Swift 标准库协议中的一个：整数字面量的 `IntegerLiteralConvertible` 协议、浮点数字面量的 `FloatingPointLiteralConvertible` 协议、字符串字面量的 `StringLiteralConvertible` 协议以及布尔值字面量的 `BooleanLiteralConvertible` 协议。比如，`Int8` 符合 `IntegerLiteralConvertible` 协议，因此它能在 `let x: Int8 = 42` 这个声明中作为整数字面量 `42` 的类型标注。

> 字面量语法
>
> _字面量_ → [_数值字面量_](02_lexical_structure.md#numeric-literal) \| [_字符串字面量_](02_lexical_structure.md#string-literal) \| [_布尔值字面量_](02_lexical_structure.md#boolean-literal) \| [_nil 字面量_](02_lexical_structure.md#nil-literal)

> _数值字面量_ → **-**可选 [_整数字面量_](02_lexical_structure.md#integer-literal) \| **-**可选 [_浮点数字面量_](02_lexical_structure.md#floating-point-literal)  _布尔值字面量_ → **true** \| **false**  _nil 字面量_ → **nil**

### 整数字面量 <a id="integer_literals"></a>

_整数字面量（Integer Literals）_ 表示未指定精度整数的值。整数字面量默认用十进制表示，可以加前缀来指定其他的进制。二进制字面量加 `0b`，八进制字面量加 `0o`，十六进制字面量加 `0x`。

十进制字面量包含数字 `0` 至 `9`。二进制字面量只包含 `0` 或 `1`，八进制字面量包含数字 `0` 至 `7`，十六进制字面量包含数字 `0` 至 `9` 以及字母 `A` 至 `F`（大小写均可）。

负整数的字面量在整数字面量前加负号 `-`，比如 `-42`。

整型字面面可以使用下划线（`_`）来增加数字的可读性，下划线会被系统忽略，因此不会影响字面量的值。同样地，也可以在数字前加 `0`，这同样也会被系统所忽略，并不会影响字面量的值。

除非特别指定，整数字面量的默认推导类型为 Swift 标准库类型中的 `Int`。Swift 标准库还定义了其他不同长度以及是否带符号的整数类型，请参考 [整数](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/01_The_Basics.html#integers)。

> 整数字面量语法
>
>  _整数字面量_ → [_二进制字面量_](02_lexical_structure.md#binary-literal) _整数字面量_ → [_八进制字面量_](02_lexical_structure.md#octal-literal) _整数字面量_ → [_十进制字面量_](02_lexical_structure.md#decimal-literal) _整数字面量_ → [_十六进制字面量_](02_lexical_structure.md#hexadecimal-literal)

> _二进制字面量_ → **0b** [_二进制数字_](02_lexical_structure.md#binary-digit) [_二进制字面量字符组_](02_lexical_structure.md#binary-literal-characters)可选  _二进制数字_ → 数值 0 到 1  _二进制字面量字符_ → [_二进制数字_](02_lexical_structure.md#binary-digit) \| \_  _二进制字面量字符组_ → [_二进制字面量字符_](02_lexical_structure.md#binary-literal-character) [_二进制字面量字符组_](02_lexical_structure.md#binary-literal-characters)可选

> _八进制字面量_ → **0o** [_八进字数字_](02_lexical_structure.md#octal-digit) [_八进制字符组_](02_lexical_structure.md#octal-literal-characters)可选  _八进字数字_ → 数值 0 到 7  _八进制字符_ → [_八进字数字_](02_lexical_structure.md#octal-digit) \| \_  _八进制字符组_ → [_八进制字符_](02_lexical_structure.md#octal-literal-character) [_八进制字符组_](02_lexical_structure.md#octal-literal-characters)可选

> _十进制字面量_ → [_十进制数字_](02_lexical_structure.md#decimal-digit) [_十进制字符组_](02_lexical_structure.md#decimal-literal-characters)可选  _十进制数字_ → 数值 0 到 9  _十进制数字组_ → [_十进制数字_](02_lexical_structure.md#decimal-digit) [_十进制数字组_](02_lexical_structure.md#decimal-digits)可选  _十进制字符_ → [_十进制数字_](02_lexical_structure.md#decimal-digit) \| \_  _十进制字符组_ → [_十进制字符_](02_lexical_structure.md#decimal-literal-character) [_十进制字符组_](02_lexical_structure.md#decimal-literal-characters)可选

> _十六进制字面量_ → **0x** [_十六进制数字_](02_lexical_structure.md#hexadecimal-digit) [_十六进制字面量字符组_](02_lexical_structure.md#hexadecimal-literal-characters)可选  _十六进制数字_ → 数值 0 到 9, 字母 a 到 f, 或 A 到 F  _十六进制字符_ → [_十六进制数字_](02_lexical_structure.md#hexadecimal-digit) \| \_  _十六进制字面量字符组_ → [_十六进制字符_](02_lexical_structure.md#hexadecimal-literal-character) [_十六进制字面量字符组_](02_lexical_structure.md#hexadecimal-literal-characters)可选

### 浮点数字面量 <a id="floating_point_literals"></a>

_浮点数字面量（Floating-point literals）_ 表示未指定精度浮点数的值。

浮点数字面量默认用十进制表示（无前缀），也可以用十六进制表示（加前缀 `0x`）。

十进制浮点数字面量由十进制数字串后跟小数部分或指数部分（或两者皆有）组成。十进制小数部分由小数点（`.`）后跟十进制数字串组成。指数部分由大写或小写字母 `e` 为前缀后跟十进制数字串组成，这串数字表示 `e` 之前的数量乘以 10 的几次方。例如：`1.25e2` 表示 1.25 x 10²，也就是 `125.0`；同样，`1.25e－2` 表示 1.25 x 10¯²，也就是 `0.0125`。

十六进制浮点数字面量由前缀 `0x` 后跟可选的十六进制小数部分以及十六进制指数部分组成。十六进制小数部分由小数点后跟十六进制数字串组成。指数部分由大写或小写字母 `p` 为前缀后跟十进制数字串组成，这串数字表示 `p` 之前的数量乘以 2 的几次方。例如：`0xFp2` 表示 15 x 2²，也就是 `60`；同样，`0xFp-2` 表示 15 x 2¯²，也就是 `3.75`。

负数的浮点数字面量由负号（`-`）和浮点数字面量组成，例如 `-42.5`。

浮点数字面量允许使用下划线（`_`）来增强数字的可读性，下划线会被系统忽略，因此不会影响字面量的值。同样地，也可以在数字前加 `0`，并不会影响字面量的值。

除非特别指定，浮点数字面量的默认推导类型为 Swift 标准库类型中的 `Double`，表示 64 位浮点数。Swift 标准库也定义了 `Float` 类型，表示 32 位浮点数。

> 浮点数字面量语法
>
>  _浮点数字面量_ → [_十进制字面量_](02_lexical_structure.md#decimal-literal) [_十进制分数_](02_lexical_structure.md#decimal-fraction)可选 [_十进制指数_](02_lexical_structure.md#decimal-exponent)可选 _浮点数字面量_ → [_十六进制字面量_](02_lexical_structure.md#hexadecimal-literal) [_十六进制分数_](02_lexical_structure.md#hexadecimal-fraction)可选 [_十六进制指数_](02_lexical_structure.md#hexadecimal-exponent)

> _十进制分数_ → **.** [_十进制字面量_](02_lexical_structure.md#decimal-literal)  _十进制指数_ → [_十进制指数 e_](02_lexical_structure.md#floating-point-e) [_正负号_](02_lexical_structure.md#sign)可选 [_十进制字面量_](02_lexical_structure.md#decimal-literal)

> _十六进制分数_ → **.** [_十六进制数字_](02_lexical_structure.md#hexadecimal-digit) [_十六进制字面量字符组_](02_lexical_structure.md#hexadecimal-literal-characters)可选  _十六进制指数_ → [_十六进制指数 p_](02_lexical_structure.md#floating-point-p) [_正负号_](02_lexical_structure.md#sign)可选 [_十进制字面量_](02_lexical_structure.md#decimal-literal)

> _十进制指数 e_ → **e** \| **E**  _十六进制指数 p_ → **p** \| **P**  _正负号_ → **+** \| **-**

### 字符串字面量 <a id="string_literals"></a>

字符串字面量是被引号包括的一串字符组成。 单行字符串字面量被包在双引号中的一串字符组成，形式如下：

> "`字符`"

字符串字面量中不能包含未转义的双引号（`"`）、未转义的反斜线（`\`）、回车符、换行符。

多行字符串字面量被包在三个双引号中的一串字符组成，形式如下：

> """ `字符` """

与单行字符串字面量不同的是，多行字符串字面量可以包含不转义的双引号（"），回车以及换行。它不能包含三个非转义的连续双引号。

""" 之后的回车或者换行开始多行字符串字面量，不是字符串的一部分。 """ 之前回车或者换行结束字面量，也不是字符串的一部分。要让多行字符串字面量的开始或结束带有换行，就在第一行或者最后一行写一个空行。

多行字符串字面量可以使用任何空格或制表符组合进行缩进；这些缩进不会包含在字符串中。 """ 的结束符号决定了缩进：字面量中的任何一个非空行必须起始于多行字符串字面量结束符号的前面；空格和制表符不会被转换。你可以包在缩进后含额外的空格和制表符；这些空格和制表符会在字符串中出现。

多行字符串字面量中的一行结束使用规范化的换行符号。尽管你的源代码混用了回车和换行符，字符串中所有的行结束都必须一样.

在多行字符串字面量里， 在行末用反斜线（`\`）可以省略字符串行间中断。 反斜线之间的空白和行间中断也可以省略。 你可以在你的代码里用这种语法硬包裹多行字符串字面量，不需要改变产生的字符串的值。

可以在字符串字面量中使用的转义特殊符号如下：

* 空字符 `\0`
* 反斜线 `\\`
* 水平制表符 `\t`
* 换行符 `\n`
* 回车符 `\r`
* 双引号 `\"`
* 单引号 `\'`
* Unicode 标量 `\u{`n`}`，n 为一到八位的十六进制数字

字符串字面量允许在反斜杠（`\`）后的括号 `()` 中插入表达式的值。插入表达式可以包含字符串字面量，但不能包含未转义的反斜线（`\`）、回车符以及换行符。

例如，以下所有字符串字面量的值都是相同的：

```swift
"1 2 3"
"1 2 \("3")"
"1 2 \(3)"
"1 2 \(1 + 2)"
let x = 3; "1 2 \(x)"
```

字符串字面量的默认推导类型为 `String`。更多有关 `String` 类型的信息请参考 [字符串和字符](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/03_Strings_and_Characters.html) 以及 [_字符串结构参考_](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Reference/Swift_String_Structure/index.html#//apple_ref/doc/uid/TP40015181)。

用 `＋` 操作符连接的字符型字面量是在编译时进行连接的。比如下面的 `textA` 和 `textB` 是完全一样的，`textA` 没有任何运行时的连接操作。

```swift
let textA = "Hello " + "world"
let textB = "Hello world"
```

> 字符串字面量语法
>
>  _字符串字面量_ → [_静态字符串字面量_](02_lexical_structure.md#static-string-literal) \| [_插值字符串字面量_](02_lexical_structure.md#interpolated-string-literal)

> _静态字符串字面量_ → **"**[_引用文本_](02_lexical_structure.md#quoted-text)可选**"**  _引用文本_ → [_引用文本项_](02_lexical_structure.md#quoted-text-item) [_引用文本_](02_lexical_structure.md#quoted-text)可选  _引用文本项_ → [_转义字符_](02_lexical_structure.md#escaped-character) _引用文本项_ → 除了 **"**、**\**、U+000A、U+000D 以外的所有 Unicode 字符

> _插值字符串字面量_ → **"**[_插值文本_](02_lexical_structure.md#interpolated-text)可选**"**  _插值文本_ → [_插值文本项_](02_lexical_structure.md#interpolated-text-item) [_插值文本_](02_lexical_structure.md#interpolated-text)可选  _插值文本项_ → **\\*\***\([_**表达式**_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/04_Expressions.html)\)_\* \| \[_引用文本项\*\]\(\#quoted-text-item\)

> _转义字符_ → **\\*\***0 **\|** \**\*\*\** \| **\t** \| **\n** \| **\r** \| **\"** \| **\'** _转义字符_ → **\u {** [_unicode 标量数字_](02_lexical_structure.md#unicode-scalar-digits) **}**  _unicode 标量数字_ → 一到八位的十六进制数字

## 运算符 <a id="operators"></a>

Swift 标准库定义了许多可供使用的运算符，其中大部分在 [基础运算符](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/02_Basic_Operators.html) 和 [高级运算符](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/25_Advanced_Operators.html) 中进行了阐述。这一小节将描述哪些字符能用于自定义运算符。

自定义运算符可以由以下其中之一的 ASCII 字符 `/`、`=`、`-`、`+`、`!`、`*`、`%`、`<`、`>`、`&`、`|`、`^`、`?` 以及 `~`，或者后面语法中规定的任一个 Unicode 字符（其中包含了_数学运算符_、_零散符号（Miscellaneous Symbols）_ 以及印刷符号（Dingbats）之类的 Unicode 块）开始。在第一个字符之后，允许使用组合型 Unicode 字符。

您也可以以点号（`.`）开头来定义自定义运算符。这些运算符可以包含额外的点，例如 `.+.`。如果某个运算符不是以点号开头的，那么它就无法再包含另外的点号了。例如，`+.+` 就会被看作为一个 `+` 运算符后面跟着一个 `.+` 运算符。

虽然您可以用问号 `?` 来自定义运算符，但是这个运算符不能只包含单独的一个问号。此外，虽然运算符可以包含一个惊叹号 `!`，但是前缀运算符不能够以问号或者惊叹号开头。

> 注意
>
> 以下这些标记 `=`、`->`、`//`、`/*`、`*/`、`.`、`<`（前缀运算符）、`&`、`?`、`?`（中缀运算符）、`>`（后缀运算符）、`!` 、`?` 是被系统保留的。这些符号不能被重载，也不能用于自定义运算符。

运算符两侧的空白被用来区分该运算符是否为前缀运算符、后缀运算符或二元运算符。规则总结如下：

* 如果运算符两侧都有空白或两侧都无空白，将被看作二元运算符。例如：`a+++b` 和 `a +++ b` 当中的 `+++` 运算符会被看作二元运算符。
* 如果运算符只有左侧空白，将被看作一元前缀运算符。例如 `a +++b` 中的 `+++` 运算符会被看做是一元前缀运算符。
* 如果运算符只有右侧空白，将被看作一元后缀运算符。例如 `a+++ b` 中的 `+++` 运算符会被看作是一元后缀运算符。
* 如果运算符左侧没有空白并紧跟 `.`，将被看作一元后缀运算符。例如 `a+++.b` 中的 `+++` 运算符会被视为一元后缀运算符（即上式被视为 `a+++ .b` 而不是 `a +++ .b`）。

鉴于这些规则，运算符前的字符 `(`、`[` 和 `{`，运算符后的字符 `)`、`]` 和 `}`，以及字符 `,`、`;` 和 `:` 都被视为空白。

以上规则需注意一点，如果预定义运算符 `!` 或 `?` 左侧没有空白，则不管右侧是否有空白都将被看作后缀运算符。如果将 `?` 用作可选链式调用运算符，左侧必须无空白。如果用于条件运算符 `? :`，必须两侧都有空白。

在某些特定的设计中 ，以 `<` 或 `>` 开头的运算符会被分离成两个或多个符号，剩余部分可能会以同样的方式被再次分离。因此，在 `Dictionary<String, Array<Int>>` 中没有必要添加空白来消除闭合字符 `>` 的歧义。在这个例子中， 闭合字符 `>` 不会被视为单独的符号，因而不会被错误解析为 `>>` 运算符。

要学习如何自定义运算符，请参考 [自定义运算符](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/25_Advanced_Operators.html#custom_operators) 和 [运算符声明](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter3/05_Declarations.html#operator_declaration)。要学习如何重载运算符，请参考 [运算符函数](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source/chapter2/25_Advanced_Operators.html#operator_functions)。

> 运算符语法
>
>  _运算符_ → [_头部运算符_](02_lexical_structure.md#operator-head) [_运算符字符组_](02_lexical_structure.md#operator-characters)可选 _运算符_ → [_头部点运算符_](02_lexical_structure.md#dot-operator-head) [_点运算符字符组_](02_lexical_structure.md#dot-operator-characters)可选

> _头部运算符_ → **/** \| **=** \| **-** \| **+** \| **!** \| **\*** \| **%** \| **&lt;** \| **&gt;** \| **&** \| **\|** \| **^** \| **~** \| **?** _头部运算符_ → U+00A1–U+00A7 _头部运算符_ → U+00A9 或 U+00AB _头部运算符_ → U+00AC 或 U+00AE _头部运算符_ → U+00B0–U+00B1，U+00B6，U+00BB，U+00BF，U+00D7，或 U+00F7 _头部运算符_ → U+2016–U+2017 或 U+2020–U+2027 _头部运算符_ → U+2030–U+203E _头部运算符_ → U+2041–U+2053 _头部运算符_ → U+2055–U+205E _头部运算符_ → U+2190–U+23FF _头部运算符_ → U+2500–U+2775 _头部运算符_ → U+2794–U+2BFF _头部运算符_ → U+2E00–U+2E7F _头部运算符_ → U+3001–U+3003 _头部运算符_ → U+3008–U+3030

> _运算符字符_ → [_头部运算符_](02_lexical_structure.md#operator-head) _运算符字符_ → U+0300–U+036F _运算符字符_ → U+1DC0–U+1DFF _运算符字符_ → U+20D0–U+20FF _运算符字符_ → U+FE00–U+FE0F _运算符字符_ → U+FE20–U+FE2F _运算符字符_ → U+E0100–U+E01EF  _运算符字符组_ → [_运算符字符_](02_lexical_structure.md#operator-character) [_运算符字符组_](02_lexical_structure.md#operator-characters)可选

> _头部点运算符_ → **..**  _点运算符字符_ → **.** \| [_运算符字符_](02_lexical_structure.md#operator-character)  _点运算符字符组_ → [_点运算符字符_](02_lexical_structure.md#dot-operator-character) [_点运算符字符组_](02_lexical_structure.md#dot-operator-characters)可选

> _二元运算符_ → [_运算符_](02_lexical_structure.md#operator)  _前缀运算符_ → [_运算符_](02_lexical_structure.md#operator)  _后缀运算符_ → [_运算符_](02_lexical_structure.md#operator)

