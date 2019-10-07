# 05\_Declarations

> 翻譯：[marsprince](https://github.com/marsprince)  
> 校對：[numbbbbb](https://github.com/numbbbbb), [stanzhai](https://github.com/stanzhai)

## 聲明

本頁包含內容：

* [模塊範圍](05_declarations.md#module_scope)
* [代碼塊](05_declarations.md#code_blocks)
* [引入聲明](05_declarations.md#import_declaration)
* [常量聲明](05_declarations.md#constant_declaration)
* [變量聲明](05_declarations.md#variable_declaration)
* [類型的別名聲明](05_declarations.md#type_alias_declaration)
* [函數聲明](05_declarations.md#function_declaration)
* [枚舉聲明](05_declarations.md#enumeration_declaration)
* [結構體聲明](05_declarations.md#structure_declaration)
* [類聲明](05_declarations.md#class_declaration)
* [協議聲明](05_declarations.md#protocol_declaration)
* [構造器聲明](05_declarations.md#initializer_declaration)
* [析構聲明](05_declarations.md#deinitializer_declaration)
* [擴展聲明](05_declarations.md#extension_declaration)
* [下標腳本聲明](05_declarations.md#subscript_declaration)
* [運算符聲明](05_declarations.md#operator_declaration)

一條聲明可以在你的程序裡引入新的名字和構造。舉例來說，你可以使用聲明來引入函數和方法，變量和常量，或者來定義 新的命名好的枚舉，結構，類和協議類型。你也可以使用一條聲明來延長一個已經存在的命名好的類型的行為。或者在你的 程序裡引入在其他地方聲明的符號。

在swift中，大多數聲明在某種意義上講也是執行或同事聲明它們的初始化定義。這意味著，因為協議和它們的成員不匹配， 大多數協議成員需要單獨的聲明。為了方便起見，也因為這些區別在swift裡不是很重要，聲明語句同時包含了聲明和定義。

> 聲明語法  
> _聲明_ → [_導入聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_declaration)  
> _聲明_ → [_常量聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#constant_declaration)  
> _聲明_ → [_變量聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration)  
> _聲明_ → [_類型別名聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_declaration)  
> _聲明_ → [_函數聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_declaration)  
> _聲明_ → [_枚舉聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#enum_declaration)  
> _聲明_ → [_結構體聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#struct_declaration)  
> _聲明_ → [_類聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#class_declaration)  
> _聲明_ → [_協議聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_declaration)  
> _聲明_ → [_構造器聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer_declaration)  
> _聲明_ → [_析構器聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#deinitializer_declaration)  
> _聲明_ → [_擴展聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#extension_declaration)  
> _聲明_ → [_附屬腳本聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_declaration)  
> _聲明_ → [_運算符聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#operator_declaration)  
> _聲明\(Declarations\)列表_ → [_聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration) [_聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declarations) _可選_  
> _聲明描述符\(Specifiers\)列表_ → [_聲明描述符\(Specifier\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration_specifier) [_聲明描述符\(Specifiers\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration_specifiers) _可選_  
> _聲明描述符\(Specifier\)_ → **class** \| **mutating** \| **nonmutating** \| **override** \| **static** \| **unowned** \| **unowned\(safe\)** \| **unowned\(unsafe\)** \| **weak**

### 模塊範圍

模塊範圍定義了對模塊中其他源文件可見的代碼。（註：待改進）在swift的源文件中，最高級別的代碼由零個或多個語句， 聲明和表達組成。變量，常量和其他的聲明語句在一個源文件的最頂級被聲明，使得它們對同一模塊中的每個源文件都是可見的。

> 頂級\(Top Level\) 聲明語法  
> _頂級聲明_ → [_多條語句\(Statements\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/10_Statements.html#statements) _可選_

### 代碼塊

代碼塊用來將一些聲明和控制結構的語句組織在一起。它有如下的形式：

> {  
> `statements`  
> }

代碼塊中的語句包括聲明，表達式和各種其他類型的語句，它們按照在源碼中的出現順序被依次執行。

> 代碼塊語法  
> _代碼塊_ → **{** [_多條語句\(Statements\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/10_Statements.html#statements) _可選_ **}**

### 引入聲明

引入聲明使你可以使用在其他文件中聲明的內容。引入語句的基本形式是引入整個代碼模塊；它由import關鍵字開始，後面 緊跟一個模塊名：

> import `module`

你可以提供更多的細節來限制引入的符號，如聲明一個特殊的子模塊或者在一個模塊或子模塊中做特殊的聲明。（待改進） 當你使用了這些細節後，在當前的程序匯總只有引入的符號是可用的（並不是聲明的整個模塊）。

> import `import kind` `module`.`symbol name`  
> import `module`.`submodule`

> 導入\(Import\)聲明語法  
> _導入聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **import** [_導入類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_kind) _可選_ [_導入路徑_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_path)  
> _導入類型_ → **typealias** \| **struct** \| **class** \| **enum** \| **protocol** \| **var** \| **func**  
> _導入路徑_ → [_導入路徑標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_path_identifier) \| [_導入路徑標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_path_identifier) **.** [_導入路徑_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#import_path)  
> _導入路徑標識符_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) \| [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator)

### 常量聲明

常量聲明可以在你的程序裡命名一個常量。常量以關鍵詞let來聲明，遵循如下的格式:

> let `constant name`: `type` = `expression`

當常量的值被給定後，常量就將常量名稱和表達式初始值不變的結合在了一起，而且不能更改。 這意味著如果常量以類的形式被初始化，類本身的內容是可以改變的，但是常量和類之間的結合關係是不能改變的。 當一個常量被聲明為全局變量，它必須被給定一個初始值。當一個常量在類或者結構體中被聲明時，它被認為是一個常量 屬性。常量並不是可計算的屬性，因此不包含getters和setters。（譯者註：getters和setters不知道怎麼翻譯，待改進）

如果常量名是一個元祖形式，元祖中的每一項初始化表達式中都要有對應的值

```swift
let (firstNumber, secondNumber) = (10, 42)
```

在上例中，firstNumber是一個值為10的常量，secnodeName是一個值為42的常量。所有常量都可以獨立的使用：

```swift
println("The first number is \(firstNumber).")
// prints "The first number is 10."
println("The second number is \(secondNumber).")
// prints "The second number is 42."
```

類型註釋（:type）在常量聲明中是一個可選項，它可以用來描述在類型推斷（type inference）中找到的類型。

聲明一個靜態常量要使用關鍵字static。靜態屬性在類型屬性（type propetries）中有介紹。

如果還想獲得更多關於常量的信息或者想在使用中獲得幫助，請查看常量和變量（constants and variables）, 存儲屬性（stored properties）等節。

> 常數聲明語法  
> _常量聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_聲明描述符\(Specifiers\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration_specifiers) _可選_ **let** [_模式構造器列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#pattern_initializer_list)  
> _模式構造器列表_ → [_模式構造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#pattern_initializer) \| [_模式構造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#pattern_initializer) **,** [_模式構造器列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#pattern_initializer_list)  
> _模式構造器_ → [_模式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/07_Patterns.html#pattern) [_構造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer) _可選_  
> _構造器_ → **=** [_表達式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/04_Expressions.html#expression)

### 變量聲明

變量聲明可以在你的程序裡聲明一個變量，它以關鍵字var來聲明。根據聲明變量類型和值的不同，如存儲和計算 變量和屬性，存儲變量和屬性監視，和靜態變量屬性，有著不同的聲明形式。（待改進） 所使用的聲明形式取決於變量所聲明的範圍和你打算聲明的變量類型。

> 注意：  
> 你也可以在協議聲明的上下文聲明屬性，詳情參見類型屬性聲明。

#### 存儲型變量和存儲型屬性

下面的形式聲明了一個存儲型變量或存儲型變量屬性

> var `variable name`: `type` = `expression`

你可以在全局，函數內，或者在類和結構體的聲明\(context\)中使用這種形式來聲明一個變量。當變量以這種形式 在全局或者一個函數內被聲明時，它代表一個存儲型變量。當它在類或者結構體中被聲明時，它代表一個存儲型變量屬性。

初始化的表達式不可以在協議（protocol）的定義中出現，在其他情況下，初始化表達式是可選的（optional），如果沒有初始化表達式，那麼變量定義時必須顯示的聲明變量類型（:type\)

對於常量的定義，如果名字是一個元祖（tuple），元祖每一項的`name`都要和初始化表達式`expression`中的相應值一致。

正如名字一樣，存儲型變量的值或存儲型變量屬性存儲在內存中。

#### 計算型變量和計算型屬性

如下形式聲明一個一個存儲型變量或存儲型屬性：

> var `variable name`: `type` {  
> get {  
> `statements`  
> }  
> set\(`setter name`\) {  
> `statements`  
> }  
> }

你可以在全局，函數體內或者類，結構體，枚舉，擴展聲明的上下文中使用這種形式的聲明。 當變量以這種形式在全局或者一個函數內被聲明時，它代表一個計算型變量。當它在類，結構體，枚舉，擴展聲明的上下文 中中被聲明時，它代表一個計算型變量屬性。

getter用來讀取變量值，setter用來寫入變量值。setter子句是可選擇的，只有getter是必需的，你可以將這些語句 都省略，只是簡單的直接返回請求值，正如在只讀計算屬性\(read-only computed properites\)中描述的那樣。 但是如果你提供了一個setter語句，你也必需提供一個getter語句。

setter的名字和圓括號內的語句是可選的。如果你寫了一個setter名，它就會作為setter的參數被使用。如果你不寫setter名， setter的初始名為newValue，正如在setter聲明速記\(shorthand setter declaration\)中提到的那樣。

不像存儲型變量和存儲型屬性那樣，計算型屬性和計算型變量的值不存儲在內存中。

獲得更多信息，查看更多關於計算型屬性的例子，請查看計算型屬性\(computed properties\)一節。

#### 存儲型變量監視器和屬性監視器

你可以用willset和didset監視器來聲明一個存儲型變量或屬性。一個包含監視器的存儲型變量或屬性按如下的形式聲明：

> var `variable name`: `type` = expression {  
> willSet\(setter name\) {  
> `statements`  
> }  
> didSet\(`setter name`\) {  
> `statements`  
> }  
> }

你可以在全局，函數體內或者類，結構體，枚舉，擴展聲明的上下文中使用這種形式的聲明。 當變量以這種形式在全局或者一個函數內被聲明時，監視器代表一個存儲型變量監視器； 當它在類，結構體，枚舉，擴展聲明的上下文中被聲明時，監視器代表屬性監視器。

你可以為適合的監視器添加任何存儲型屬性。你也可以通過重寫子類屬性的方式為適合的監視器添加任何繼承的屬性 \(無論是存儲型還是計算型的\)，參見重寫屬性監視器\(overriding properyt observers\)。

初始化表達式在類或者結構體的聲明中是可選的，但是在其他地方是必需的。無論在什麼地方聲明， 所有包含監視器的變量聲明都必須有類型註釋\(type annotation\)。

當變量或屬性的值被改變時，willset和didset監視器提供了一個監視方法（適當的回應）。 監視器不會在變量或屬性第一次初始化時運行，它們只有在值被外部初始化語句改變時才會被運行。

willset監視器只有在變量或屬性值被改變之前運行。新的值作為一個常量經過過willset監視器，因此不可以在 willset語句中改變它。didset監視器在變量或屬性值被改變後立即運行。和willset監視器相反，為了以防止你仍然 需要獲得舊的數據，舊變量值或者屬性會經過didset監視器。這意味著，如果你在變量或屬性自身的didiset監視器語句 中設置了一個值，你設置的新值會取代剛剛在willset監視器中經過的那個值。

在willset和didset語句中，setter名和圓括號的語句是可選的。如果你寫了一個setter名，它就會作為willset和didset的參數被使用。如果你不寫setter名， willset監視器初始名為newvalue，didset監視器初始名為oldvalue。

當你提供一個willset語句時，didset語句是可選的。同樣的，在你提供了一個didset語句時，willset語句是可選的。

獲得更多信息，查看如何使用屬性監視器的例子，請查看屬性監視器\(prpperty observers\)一節。

#### 類和靜態變量屬性

class關鍵字用來聲明類的計算型屬性。static關鍵字用來聲明類的靜態變量屬性。類和靜態變量在類型屬性\(type properties\)中有詳細討論。

> 變量聲明語法  
> _變量聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_模式構造器列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#pattern_initializer_list)  
> _變量聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_變量名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_name) [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _變量聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_變量名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_name) [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_getter-setter塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_block)  
> _變量聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_變量名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_name) [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_getter-setter關鍵字\(Keyword\)塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_keyword_block)  
> _變量聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_變量名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_name) [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_構造器_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer) _可選_ [_willSet-didSet代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#willSet_didSet_block)  
> _變量聲明頭\(Head\)_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_聲明描述符\(Specifiers\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration_specifiers) _可選_ **var**  
> _變量名稱_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _getter-setter塊_ → **{** [_getter子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_clause) [_setter子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_clause) _可選_ **}**  
> _getter-setter塊_ → **{** [_setter子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_clause) [_getter子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_clause) **}**  
> _getter子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **get** [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _setter子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **set** [_setter名稱_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_name) _可選_ [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _setter名稱_ → **\(** [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) **\)**  
> _getter-setter關鍵字\(Keyword\)塊_ → **{** [_getter關鍵字\(Keyword\)子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_keyword_clause) [_setter關鍵字\(Keyword\)子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_keyword_clause) _可選_ **}**  
> _getter-setter關鍵字\(Keyword\)塊_ → **{** [_setter關鍵字\(Keyword\)子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_keyword_clause) [_getter關鍵字\(Keyword\)子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_keyword_clause) **}**  
> _getter關鍵字\(Keyword\)子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **get**  
> _setter關鍵字\(Keyword\)子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **set**  
> _willSet-didSet代碼塊_ → **{** [_willSet子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#willSet_clause) [_didSet子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#didSet_clause) _可選_ **}**  
> _willSet-didSet代碼塊_ → **{** [_didSet子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#didSet_clause) [_willSet子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#willSet_clause) **}**  
> _willSet子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **willSet** [_setter名稱_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_name) _可選_ [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _didSet子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **didSet** [_setter名稱_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#setter_name) _可選_ [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)

### 類型的別名聲明

類型別名的聲明可以在你的程序裡為一個已存在的類型聲明一個別名。類型的別名聲明以關鍵字typealias開始，遵循如下的 形式：

> `typealias name` = `existing type`

當聲明一個類型的別名後，你可以在你程序的任何地方使用別名來代替已存在的類型。已存在的類型可以是已經被命名的 類型或者是混合類型。類型的別名不產生新的類型，它只是簡單的和已存在的類型做名稱替換。

查看更多Protocol Associated Type Declaration.

> 類型別名聲明語法  
> _類型別名聲明_ → [_類型別名頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_head) [_類型別名賦值_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_assignment)  
> _類型別名頭\(Head\)_ → **typealias** [_類型別名名稱_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_name)  
> _類型別名名稱_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _類型別名賦值_ → **=** [_類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type)

### 函數聲明

你可以使用函數聲明在你的程序裡引入新的函數。函數可以在類的上下文，結構體，枚舉，或者作為方法的協議中被聲明。 函數聲明使用關鍵字func，遵循如下的形式：

> func `function name`\(`parameters`\) -&gt; `return type` {  
> `statements`  
> }

如果函數不返回任何值，返回類型可以被忽略，如下所示：

> func `function name`\(`parameters`\) {  
> `statements`  
> }

每個參數的類型都要標明，它們不能被推斷出來。初始時函數的參數是常量。在這些參數前面添加var使它們成為變量， 作用域內任何對變量的改變只在函數體內有效，或者用inout使的這些改變可以在調用域內生效。 更多關於in-out參數的討論，參見in-out參數\(in-out parameters\)

函數可以使用元組類型作為返回值來返回多個變量。

函數定義可以出現在另一個函數聲明內。這種函數被稱作nested函數。更多關於nested函數的討論，參見nestde functions。

#### 參數名

函數的參數是一個以逗號分隔的列表 。函數調用是的變量順序必須和函數聲明時的參數順序一致。 最簡單的參數列表有著如下的形式：

> `parameter name`: `parameter type`

對於函數參數來講，參數名在函數體內被使用，而不是在函數調用時使用。對於方法參數，參數名在函數體內被使用， 同時也在方法被調用時作為標籤被使用。該方法的第一個參數名僅僅在函數體內被使用，就像函數的參數一樣，舉例來講：

```swift
func f(x: Int, y: String) -> String {
    return y + String(x)
}
f(7, "hello")  // x and y have no name
```

```swift
class C {
    func f(x: Int, y: String) -> String {
       return y + String(x)
    }
}
let c = C()
c.f(7, y: "hello")  // x沒有名稱，y有名稱
```

你可以按如下的形式，重寫參數名被使用的過程：

> `external parameter name` `local parameter name`: `parameter type`  
> \#`parameter name`: `parameter type`  
> \_ `local parameter name`: `parameter type`

在本地參數前命名的第二名稱\(second name\)使得參數有一個擴展名。且不同於本地的參數名。 擴展參數名在函數被調用時必須被使用。對應的參數在方法或函數被調用時必須有擴展名 。

在參數名前所寫的哈希符號\(\#\)代表著這個參數名可以同時作為外部或本體參數名來使用。等同於書寫兩次本地參數名。 在函數或方法調用時，與其對應的語句必須包含這個名字。

本地參數名前的強調字符\(\_\)使參數在函數被調用時沒有名稱。在函數或方法調用時，與其對應的語句必須沒有名字。

#### 特殊類型的參數

參數可以被忽略，值可以是變化的，並且提供一個初始值，這種方法有著如下的形式：

> \_ : &lt;\#parameter type\#.  
> `parameter name`: `parameter type`...  
> `parameter name`: `parameter type` = `default argument value`

以強調符\(\_\)命名的參數明確的在函數體內不能被訪問。

一個以基礎類型名的參數，如果緊跟著三個點\(...\)，被理解為是可變參數。一個函數至多可以擁有一個可變參數， 且必須是最後一個參數。可變參數被作為該基本類型名的數組來看待。舉例來講，可變參數int...被看做是int\[\]。 查看可變參數的使用例子，詳見可變參數\(variadic parameters\)一節。

在參數的類型後面有一個以等號\(=\)連接的表達式，這樣的參數被看做有著給定表達式的初始值。如果參數在函數 調用時被省略了，就會使用初始值。如果參數沒有省略，那麼它在函數調用是必須有自己的名字.舉例來講， f\(\)和f\(x:7\)都是只有一個變量x的函數的有效調用，但是f\(7\)是非法的，因為它提供了一個值而不是名稱。

#### 特殊方法

以self修飾的枚舉或結構體方法必須以mutating關鍵字作為函數聲明頭。

子類重寫的方法必須以override關鍵字作為函數聲明頭。不用override關鍵字重寫的方法，使用了override關鍵字 卻並沒有重寫父類方法都會報錯。

和類型相關而不是和類型實例相關的方法必須在static聲明的結構以或枚舉內，亦或是以class關鍵字定義的類內。

#### 柯裡化函數和方法\(Curried Functions and Methods\)

柯裡化函數或方法有著如下的形式：

> func `function name`\(`parameters`\)\(`parameters`\) -&gt; `return type` {  
> `statements`  
> }

以這種形式定義的函數的返回值是另一個函數。舉例來說，下面的兩個聲明是等價的:

```swift
func addTwoNumbers(a: Int)(b: Int) -> Int {
    return a + b
}
func addTwoNumbers(a: Int) -> (Int -> Int) {
    func addTheSecondNumber(b: Int) -> Int {
        return a + b
    }
    return addTheSecondNumber
}
```

```swift
addTwoNumbers(4)(5) // Returns 9
```

多級柯裡化應用如下

> 函數聲明語法  
> _函數聲明_ → [_函數頭_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_head) [_函數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_函數簽名\(Signature\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_signature) [_函數體_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_body)  
> _函數頭_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_聲明描述符\(Specifiers\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration_specifiers) _可選_ **func**  
> _函數名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) \| [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator)  
> _函數簽名\(Signature\)_ → [_parameter-clauses_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clauses) [_函數結果_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_result) _可選_  
> _函數結果_ → **-&gt;** [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type)  
> _函數體_ → [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _parameter-clauses_ → [_參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clause) [_parameter-clauses_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clauses) _可選_  
> _參數子句_ → **\(** **\)** \| **\(** [_參數列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_list) **...** _可選_ **\)**  
> _參數列表_ → [_參數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter) \| [_參數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter) **,** [_參數列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_list)  
> _參數_ → **inout** _可選_ **let** _可選_ **\#** _可選_ [_參數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_name) [_本地參數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#local_parameter_name) _可選_ [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_默認參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#default_argument_clause) _可選_  
> _參數_ → **inout** _可選_ **var** **\#** _可選_ [_參數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_name) [_本地參數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#local_parameter_name) _可選_ [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_默認參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#default_argument_clause) _可選_  
> _參數_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type)  
> _參數名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) \| **\_**  
> _本地參數名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) \| **\_**  
> _默認參數子句_ → **=** [_表達式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/04_Expressions.html#expression)

### 枚舉聲明

在你的程序裡使用枚舉聲明來引入一個枚舉類型。

枚舉聲明有兩種基本的形式，使用關鍵字enum來聲明。枚舉聲明體使用從零開始的變量——叫做枚舉事件，和任意數量的 聲明，包括計算型屬性，實例方法，靜態方法，構造器，類型別名，甚至其他枚舉，結構體，和類。枚舉聲明不能 包含析構器或者協議聲明。

不像類或者結構體。枚舉類型並不提供隱式的初始構造器，所有構造器必須顯式的聲明。構造器可以委託枚舉中的其他 構造器，但是構造過程僅當構造器將一個枚舉時間完成後才全部完成。

和結構體類似但是和類不同，枚舉是值類型：枚舉實例在賦予變量或常量時，或者被函數調用時被複製。 更多關於值類型的信息，參見結構體和枚舉都是值類型\(Structures and Enumerations Are Value Types\)一節。

你可以擴展枚舉類型，正如在擴展名聲明\(Extension Declaration\)中討論的一樣。

#### 任意事件類型的枚舉

如下的形式聲明了一個包含任意類型枚舉時間的枚舉變量

> enum `enumeration name` {  
> case `enumeration case 1`  
> case `enumeration case 2`\(`associated value types`\)  
> }

這種形式的枚舉聲明在其他語言中有時被叫做可識別聯合\(discrinminated\)。

這種形式中，每一個事件塊由關鍵字case開始，後面緊接著一個或多個以逗號分隔的枚舉事件。每一個事件名必須是 獨一無二的。每一個事件也可以指定它所存儲的指定類型的值，這些類型在關聯值類型的元祖裡被指定，立即書寫在事件 名後。獲得更多關於關聯值類型的信息和例子，請查看關聯值\(associated values\)一節。

#### 使用原始事件值的枚舉

以下的形式聲明了一個包含相同基礎類型的枚舉事件的枚舉：

> enum `enumeration name`: `raw value type` {  
> case `enumeration case 1` = `raw value 1`  
> case `enumeration case 2` = `raw value 2`  
> }

在這種形式中，每一個事件塊由case關鍵字開始，後面緊接著一個或多個以逗號分隔的枚舉事件。和第一種形式的枚舉 事件不同，這種形式的枚舉事件包含一個同類型的基礎值，叫做原始值\(raw value\)。這些值的類型在原始值類型\(raw value type\) 中被指定，必須是字面上的整數，浮點數，字符或者字符串。

每一個事件必須有唯一的名字，必須有一個唯一的初始值。如果初始值類型被指定為int，則不必為事件顯式的指定值， 它們會隱式的被標為值0,1,2等。每一個沒有被賦值的Int類型時間會隱式的賦予一個初始值，它們是自動遞增的。

```swift
num ExampleEnum: Int {
    case A, B, C = 5, D
}
```

在上面的例子中，ExampleEnum.A的值是0，ExampleEnum.B的值是。因為ExampleEnum.C的值被顯式的設定為5，因此 ExampleEnum.D的值會自動增長為6.

枚舉事件的初始值可以調用方法roRaw獲得，如ExampleEnum.B.toRaw\(\)。你也可以通過調用fromRaw方法來使用初始值找到 其對應的事件，並返回一個可選的事件。查看更多信息和獲取初始值類型事件的信息，參閱初始值\(raw values\)。

#### 獲得枚舉事件

使用點\(.\)來引用枚舉類型的事件，如 EnumerationType.EnumerationCase。當枚舉類型可以上下文推斷出時，你可以 省略它\(.仍然需要\)，參照枚舉語法\(Enumeration Syntax\)和顯式成員表達\(Implicit Member Expression\).

使用switch語句來檢驗枚舉事件的值，正如使用switch語句匹配枚舉值（Matching Enumeration Values with a Switch Statement\)一節描述的那樣。

枚舉類型是模式匹配\(pattern-matched\)的，和其相反的是switch語句case塊中枚舉事件匹配，在枚舉事件類型\(Enumeration Case Pattern\)中有描述。

> 枚舉聲明語法  
> _枚舉聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_聯合式枚舉_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum) \| [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_原始值式枚舉_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum)  
> _聯合式枚舉_ → [_枚舉名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#enum_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ **{** [_union-style-enum-members_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_members) _可選_ **}**  
> _union-style-enum-members_ → [_union-style-enum-member_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_member) [_union-style-enum-members_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_members) _可選_  
> _union-style-enum-member_ → [_聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration) \| [_聯合式\(Union Style\)的枚舉case子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_case_clause)  
> _聯合式\(Union Style\)的枚舉case子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **case** [_聯合式\(Union Style\)的枚舉case列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_case_list)  
> _聯合式\(Union Style\)的枚舉case列表_ → [_聯合式\(Union Style\)的case_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_case) \| [_聯合式\(Union Style\)的case_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_case) **,** [_聯合式\(Union Style\)的枚舉case列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#union_style_enum_case_list)  
> _聯合式\(Union Style\)的case_ → [_枚舉的case名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#enum_case_name) [_元組類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#tuple_type) _可選_  
> _枚舉名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _枚舉的case名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _原始值式枚舉_ → [_枚舉名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#enum_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ **:** [_類型標識_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_identifier) **{** [_原始值式枚舉成員列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_members) _可選_ **}**  
> _原始值式枚舉成員列表_ → [_原始值式枚舉成員_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_member) [_原始值式枚舉成員列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_members) _可選_  
> _原始值式枚舉成員_ → [_聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declaration) \| [_原始值式枚舉case子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_case_clause)  
> _原始值式枚舉case子句_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **case** [_原始值式枚舉case列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_case_list)  
> _原始值式枚舉case列表_ → [_原始值式枚舉case_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_case) \| [_原始值式枚舉case_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_case) **,** [_原始值式枚舉case列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_style_enum_case_list)  
> _原始值式枚舉case_ → [_枚舉的case名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#enum_case_name) [_原始值賦值_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#raw_value_assignment) _可選_  
> _原始值賦值_ → **=** [_字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#literal)

### 結構體聲明

使用結構體聲明可以在你的程序裡引入一個結構體類型。結構體聲明使用struct關鍵字，遵循如下的形式：

> struct `structure name`: `adopted protocols` {  
> `declarations`  
> }

結構體內包含零或多個聲明。這些聲明可以包括存儲型和計算型屬性，靜態屬性，實例方法，靜態方法，構造器， 類型別名，甚至其他結構體，類，和枚舉聲明。結構體聲明不能包含析構器或者協議聲明。詳細討論和包含多種結構體 聲明的實例，參見類和結構體一節。

結構體可以包含任意數量的協議，但是不能繼承自類，枚舉或者其他結構體。

有三種方法可以創建一個聲明過的結構體實例：

-調用結構體內聲明的構造器，參照構造器\(initializers\)一節。

—如果沒有聲明構造器，調用結構體的逐個構造器，詳情參見Memberwise Initializers for Structure Types.

—如果沒有聲明析構器，結構體的所有屬性都有初始值，調用結構體的默認構造器，詳情參見默認構造器\(Default Initializers\).

結構體的構造過程參見初始化\(initiaization\)一節。

結構體實例屬性可以用點\(.\)來獲得，詳情參見獲得屬性\(Accessing Properties\)一節。

結構體是值類型；結構體的實例在被賦予變量或常量，被函數調用時被複製。獲得關於值類型更多信息，參見 結構體和枚舉都是值類型\(Structures and Enumerations Are Value Types\)一節。

你可以使用擴展聲明來擴展結構體類型的行為，參見擴展聲明\(Extension Declaration\).

> 結構體聲明語法  
> _結構體聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **struct** [_結構體名稱_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#struct_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_類型繼承子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_inheritance_clause) _可選_ [_結構體主體_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#struct_body)  
> _結構體名稱_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _結構體主體_ → **{** [_聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declarations) _可選_ **}**

### 類聲明

你可以在你的程序中使用類聲明來引入一個類。類聲明使用關鍵字class，遵循如下的形式：

> class `class name`: `superclass`, `adopted protocols` {  
> `declarations`  
> }

一個類內包含零或多個聲明。這些聲明可以包括存儲型和計算型屬性，實例方法，類方法，構造器，單獨的析構器方法， 類型別名，甚至其他結構體，類，和枚舉聲明。類聲明不能包含協議聲明。詳細討論和包含多種類聲明的實例，參見類和 結構體一節。

一個類只能繼承一個父類，超類，但是可以包含任意數量的協議。這些超類第一次在type-inheritance-clause出現，遵循任意協議。

正如在初始化聲明\(Initializer Declaration\)談及的那樣，類可以有指定\(designated\)和方便\(convenience\)構造器。當你聲明任一種構造器時， 你可以使用required變量來標記構造器，要求任意子類來重寫它。指定類的構造器必須初始化類所有的已聲明的屬性， 它必須在子類構造器調用前被執行。

類可以重寫屬性，方法和它的超類的構造器。重寫的方法和屬性必須以override標注。

雖然超類的屬性和方法聲明可以被當前類繼承，但是超類聲明的指定構造器卻不能。這意味著，如果當前類重寫了超類 的所有指定構造器，它就繼承了超類的方便構造器。Swift的類並不是繼承自一個全局基礎類。

有兩種方法來創建已聲明的類的實例：

* 調用類的一個構造器，參見構造器\(initializers\)。
* 如果沒有聲明構造器，而且類的所有屬性都被賦予了初始值，調用類的默認構造器，參見默認構造器\(default initializers\).

類實例屬性可以用點\(.\)來獲得，詳情參見獲得屬性\(Accessing Properties\)一節。

類是引用類型；當被賦予常量或變量，函數調用時，類的實例是被引用，而不是複製。獲得更多關於引用類型的信息， 結構體和枚舉都是值類型\(Structures and Enumerations Are Value Types\)一節。

你可以使用擴展聲明來擴展類的行為，參見擴展聲明\(Extension Declaration\).

> 類聲明語法  
> _類聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **class** [_類名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#class_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_類型繼承子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_inheritance_clause) _可選_ [_類主體_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#class_body)  
> _類名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _類主體_ → **{** [_聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declarations) _可選_ **}**

### 協議聲明\(translated by 小一\)

一個協議聲明為你的程序引入一個命名了的協議類型。協議聲明使用 `protocol` 關鍵詞來進行聲明並有下面這樣的形式：

> protocol `protocol name`: `inherited protocols` {  
> `protocol member declarations`  
> }

協議的主體包含零或多個協議成員聲明，這些成員描述了任何採用該協議必須滿足的一致性要求。特別的，一個協議可以聲明必須實現某些屬性、方法、初始化程序及下標腳本的一致性類型。協議也可以聲明專用種類的類型別名，叫做關聯類型，它可以指定協議的不同聲明之間的關係。協議成員聲明會在下面的詳情裡進行討論。

協議類型可以從很多其它協議那繼承。當一個協議類型從其它協議那繼承的時候，來自其它協議的所有要求就集合了，而且從當前協議繼承的任何類型必須符合所有的這些要求。對於如何使用協議繼承的例子，查看[協議繼承](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#protocol_inheritance)

> 注意：  
> 你也可以使用協議合成類型集合多個協議的一致性要求，詳情參見[協議合成類型](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#protocol_composition_type)和[協議合成](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#protocol_composition)

你可以通過採用在類型的擴展聲明中的協議來為之前聲明的類型添加協議一致性。在擴展中你必須實現所有採用協議的要求。如果該類型已經實現了所有的要求，你可以讓這個擴展聲明的主題留空。

默認地，符合某一個協議的類型必須實現所有聲明在協議中的屬性、方法和下標腳本。也就是說，你可以用`optional`屬性標注這些協議成員聲明以指定它們的一致性類型實現是可選的。`optional`屬性僅僅可以用於使用`objc`屬性標記過的協議。這樣的結果就是僅僅類類型可以採用並符合包含可選成員要求的協議。更多關於如何使用`optional`屬性的信息及如何訪問可選協議成員的指導——比如當你不能肯定是否一致性的類型實現了它們——參見[可選協議要求](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#optional_protocol_requirements)

為了限制協議的採用僅僅針對類類型，需要使用`class_protocol`屬性標記整個協議聲明。任意繼承自標記有`class_protocol`屬性協議的協議都可以智能地僅能被類類型採用。

> 注意：  
> 如果協議已經用`object`屬性標記了，`class_protocol`屬性就隱性地應用於該協議；沒有必要再明確地使用`class_protocol`屬性來標記該協議了。

協議是命名的類型，因此它們可以以另一個命名類型出現在你代碼的所有地方，就像[協議類型](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#protocols_as_types)裡討論的那樣。然而你不能構造一個協議的實例，因為協議實際上不提供它們指定的要求的實現。

你可以使用協議來聲明一個類的代理的方法或者應該實現的結構，就像[委託\(代理\)模式](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#delegation)描述的那樣。

> 協議\(Protocol\)聲明語法  
> _協議聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **protocol** [_協議名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_name) [_類型繼承子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_inheritance_clause) _可選_ [_協議主體_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_body)  
> _協議名_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier)  
> _協議主體_ → **{** [_協議成員聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_member_declarations) _可選_ **}**  
> _協議成員聲明_ → [_協議屬性聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_property_declaration)  
> _協議成員聲明_ → [_協議方法聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_method_declaration)  
> _協議成員聲明_ → [_協議構造器聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_initializer_declaration)  
> _協議成員聲明_ → [_協議附屬腳本聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_subscript_declaration)  
> _協議成員聲明_ → [_協議關聯類型聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_associated_type_declaration)  
> _協議成員聲明\(Declarations\)列表_ → [_協議成員聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_member_declaration) [_協議成員聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#protocol_member_declarations) _可選_

#### 協議屬性聲明

協議聲明了一致性類型必須在協議聲明的主體裡通過引入一個協議屬性聲明來實現一個屬性。協議屬性聲明有一種特殊的類型聲明形式：

> var `property name`: `type` { get set }

同其它協議成員聲明一樣，這些屬性聲明僅僅針對符合該協議的類型聲明了`getter`和`setter`要求。結果就是你不需要在協議裡它被聲明的地方實現`getter`和`setter`。

`getter`和`setter`要求可以通過一致性類型以各種方式滿足。如果屬性聲明包含`get`和`set`關鍵詞，一致性類型就可以用可讀寫（實現了`getter`和`setter`）的存儲型變量屬性或計算型屬性，但是屬性不能以常量屬性或只讀計算型屬性實現。如果屬性聲明僅僅包含`get`關鍵詞的話，它可以作為任意類型的屬性被實現。比如說實現了協議的屬性要求的一致性類型，參見[屬性要求](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter2/21_Protocols.html#property_requirements)

更多參見[變量聲明](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration)

> 協議屬性聲明語法  
> _協議屬性聲明_ → [_變量聲明頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_declaration_head) [_變量名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#variable_name) [_類型註解_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_annotation) [_getter-setter關鍵字\(Keyword\)塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_keyword_block)

#### 協議方法聲明

協議聲明了一致性類型必須在協議聲明的主體裡通過引入一個協議方法聲明來實現一個方法. 協議方法聲明和函數方法聲明有著相同的形式，包含如下兩條規則：它們不包括函數體，你不能在類的聲明內為它們的 參數提供初始值.舉例來說，符合的類型執行協議必需的方法。參見必需方法一節。

使用關鍵字class可以在協議聲明中聲明一個類或必需的靜態方法。執行這些方法的類也用關鍵字class聲明。 相反的，執行這些方法的結構體必須以關鍵字static聲明。如果你想使用擴展方法，在擴展類時使用class關鍵字， 在擴展結構體時使用static關鍵字。

更多請參閱函數聲明。

> 協議方法聲明語法  
> _協議方法聲明_ → [_函數頭_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_head) [_函數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_name) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_函數簽名\(Signature\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#function_signature)

#### 協議構造器聲明

協議聲明了一致性類型必須在協議聲明的主體裡通過引入一個協議構造器聲明來實現一個構造器。協議構造器聲明 除了不包含構造器體外，和構造器聲明有著相同的形式，

更多請參閱構造器聲明。

> 協議構造器聲明語法  
> _協議構造器聲明_ → [_構造器頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer_head) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clause)

#### 協議下標腳本聲明

協議聲明了一致性類型必須在協議聲明的主體裡通過引入一個協議下標腳本聲明來實現一個下標腳本。協議屬性聲明 對下標腳本聲明有一個特殊的形式：

> subscript \(`parameters`\) -&gt; `return type` { get set }

下標腳本聲明只為和協議一致的類型聲明了必需的最小數量的的getter和setter。如果下標腳本申明包含get和set關鍵字， 一致的類型也必須有一個getter和setter語句。如果下標腳本聲明值包含get關鍵字，一致的類型必須至少包含一個 getter語句，可以選擇是否包含setter語句。

更多參閱下標腳本聲明。

> 協議附屬腳本聲明語法  
> _協議附屬腳本聲明_ → [_附屬腳本頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_head) [_附屬腳本結果\(Result\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_result) [_getter-setter關鍵字\(Keyword\)塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_keyword_block)

#### 協議相關類型聲明

協議聲明相關類型使用關鍵字typealias。相關類型為作為協議聲明的一部分的類型提供了一個別名。相關類型和參數 語句中的類型參數很相似，但是它們在聲明的協議中包含self關鍵字。在這些語句中，self指代和協議一致的可能的類型。 獲得更多信息和例子，查看相關類型或類型別名聲明。

> 協議關聯類型聲明語法  
> _協議關聯類型聲明_ → [_類型別名頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_head) [_類型繼承子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_inheritance_clause) _可選_ [_類型別名賦值_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#typealias_assignment) _可選_

### 構造器聲明

構造器聲明會為程序內的類，結構體或枚舉引入構造器。構造器使用關鍵字Init來聲明，遵循兩條基本形式。

結構體，枚舉，類可以有任意數量的構造器，但是類的構造器的規則和行為是不一樣的。不像結構體和枚舉那樣，類 有兩種結構體，designed initializers 和convenience initializers，參見構造器一節。

如下的形式聲明了結構體，枚舉和類的指定構造器：

> init\(`parameters`\) {  
> `statements`  
> }

類的指定構造器將類的所有屬性直接初始化。如果類有超類，它不能調用該類的其他構造器,它只能調用超類的一個 指定構造器。如果該類從它的超類處繼承了任何屬性，這些屬性在當前類內被賦值或修飾時，必須調用一個超類的 指定構造器。

指定構造器可以在類聲明的上下文中聲明，因此它不能用擴展聲明的方法加入一個類中。

結構體和枚舉的構造器可以調用其他的已聲明的構造器，委託其中一個或所有的構造器進行初始化過程。

以關鍵字convenience來聲明一個類的便利構造器：

> convenience init\(`parameters`\) {  
> `statements`  
> }

便利構造器可以將初始化過程委託給另一個便利構造器或類的一個指定構造器。這意味著，類的初始化過程必須 以一個將所有類屬性完全初始化的指定構造器的調用作為結束。便利構造器不能調用超類的構造器。

你可以使用required關鍵字，將便利構造器和指定構造器標記為每個子類的構造器都必須擁有的。因為指定構造器 不被子類繼承，它們必須被立即執行。當子類直接執行所有超類的指定構造器\(或使用便利構造器重寫指定構造器\)時， 必需的便利構造器可以被隱式的執行，亦可以被繼承。不像方法，下標腳本那樣，你不需要為這些重寫的構造器標注 overrride關鍵字。

查看更多關於不同聲明方法的構造器的例子，參閱構造過程一節。

> 構造器聲明語法  
> _構造器聲明_ → [_構造器頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer_head) [_泛型參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/GenericParametersAndArguments.html#generic_parameter_clause) _可選_ [_參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clause) [_構造器主體_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#initializer_body)  
> _構造器頭\(Head\)_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **convenience** _可選_ **init**  
> _構造器主體_ → [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)

### 析構聲明

析構聲明為類聲明了一個析構器。析構器沒有參數，遵循如下的格式：

> deinit {  
> `statements`  
> }

當類沒有任何語句時將要被釋放時，析構器會自動的被調用。析構器在類的聲明體內只能被聲明一次——但是不能在 類的擴展聲明內，每個類最多只能有一個。

子類繼承了它的超類的析構器，在子類將要被釋放時隱式的調用。子類在所有析構器被執行完畢前不會被釋放。

析構器不會被直接調用。

查看例子和如何在類的聲明中使用析構器，參見析構過程一節。

> 析構器聲明語法  
> _析構器聲明_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **deinit** [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)

### 擴展聲明

擴展聲明用於擴展一個現存的類，結構體，枚舉的行為。擴展聲明以關鍵字extension開始，遵循如下的規則：

> extension `type`: `adopted protocols` {  
> `declarations`  
> }

一個擴展聲明體包括零個或多個聲明。這些聲明可以包括計算型屬性，計算型靜態屬性，實例方法，靜態和類方法，構造器， 下標腳本聲明，甚至其他結構體，類，和枚舉聲明。擴展聲明不能包含析構器，協議聲明，存儲型屬性，屬性監測器或其他 的擴展屬性。詳細討論和查看包含多種擴展聲明的實例，參見擴展一節。

擴展聲明可以向現存的類，結構體，枚舉內添加一致的協議。擴展聲明不能向一個類中添加繼承的類，因此 type-inheritance-clause是一個只包含協議列表的擴展聲明。

屬性，方法，現存類型的構造器不能被它們類型的擴展所重寫。

擴展聲明可以包含構造器聲明，這意味著，如果你擴展的類型在其他模塊中定義，構造器聲明必須委託另一個在 那個模塊裡聲明的構造器來恰當的初始化。

> 擴展\(Extension\)聲明語法  
> _擴展聲明_ → **extension** [_類型標識_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_identifier) [_類型繼承子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type_inheritance_clause) _可選_ [_extension-body_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#extension_body)  
> _extension-body_ → **{** [_聲明\(Declarations\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#declarations) _可選_ **}**

### 下標腳本聲明\(translated by 林\)

附屬腳本用於向特定類型添加附屬腳本支持，通常為訪問集合，列表和序列的元素時提供語法便利。附屬腳本聲明使用關鍵字`subscript`，聲明形式如下：

> subscript \(`parameter`\) -&gt; \(return type\){  
> get{  
> `statements`  
> }  
> set\(`setter name`\){  
> `statements`  
> }  
> }

附屬腳本聲明只能在類，結構體，枚舉，擴展和協議聲明的上下文進行聲明。

_變量\(parameters\)_指定一個或多個用於在相關類型的下標腳本中訪問元素的索引（例如，表達式`object[i]`中的`i`）。儘管用於元素訪問的索引可以是任意類型的，但是每個變量必須包含一個用於指定每種索引類型的類型標注。_返回類型\(return type\)_指定被訪問的元素的類型。

和計算性屬性一樣，下標腳本聲明支持對訪問元素的讀寫操作。getter用於讀取值，setter用於寫入值。setter子句是可選的，當僅需要一個getter子句時，可以將二者都忽略且直接返回請求的值即可。也就是說，如果使用了setter子句，就必須使用getter子句。

setter的名字和封閉的括號是可選的。如果使用了setter名稱，它會被當做傳給setter的變量的名稱。如果不使用setter名稱，那麼傳給setter的變量的名稱默認是`value`。setter名稱的類型必須與_返回類型\(return type\)_的類型相同。

可以在下標腳本聲明的類型中，可以重載下標腳本，只要_變量\(parameters\)_或_返回類型\(return type\)_與先前的不同即可。此時，必須使用`override`關鍵字聲明那個被覆蓋的下標腳本。\(註：好亂啊！到底是重載還是覆蓋？！\)

同樣可以在協議聲明的上下文中聲明下標腳本，[Protocol Subscript Declaration](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-XID_619)中有所描述。

更多關於下標腳本和下標腳本聲明的例子，請參考[Subscripts](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Subscripts.html#//apple_ref/doc/uid/TP40014097-CH16-XID_393)。

> 附屬腳本聲明語法  
> _附屬腳本聲明_ → [_附屬腳本頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_head) [_附屬腳本結果\(Result\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_result) [_代碼塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#code_block)  
> _附屬腳本聲明_ → [_附屬腳本頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_head) [_附屬腳本結果\(Result\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_result) [_getter-setter塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_block)  
> _附屬腳本聲明_ → [_附屬腳本頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_head) [_附屬腳本結果\(Result\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#subscript_result) [_getter-setter關鍵字\(Keyword\)塊_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#getter_setter_keyword_block)  
> _附屬腳本頭\(Head\)_ → [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ **subscript** [_參數子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#parameter_clause)  
> _附屬腳本結果\(Result\)_ → **-&gt;** [_特性\(Attributes\)列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/06_Attributes.html#attributes) _可選_ [_類型_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/03_Types.html#type)

### 運算符聲明\(translated by 林\)

運算符聲明會向程序中引入中綴、前綴或後綴運算符，它使用上下文關鍵字`operator`聲明。 可以聲明三種不同的綴性：中綴、前綴和後綴。操作符的綴性描述了操作符與它的操作數的相對位置。 運算符聲明有三種基本形式，每種綴性各一種。運算符的綴性通過在`operator`和運算符之間添加上下文關鍵字`infix`，`prefix`或`postfix`來指定。每種形式中，運算符的名字只能包含[Operators](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_871)中定義的運算符字符。

下面的這種形式聲明了一個新的中綴運算符：

> operator infix `operator name`{  
> previewprecedence `precedence level`  
> associativity `associativity`  
> }

_中綴_運算符是二元運算符，它可以被置於兩個操作數之間，比如表達式`1 + 2` 中的加法運算符\(`+`\)。

中綴運算符可以可選地指定優先級，結合性，或兩者同時指定。

運算符的_優先級_可以指定在沒有括號包圍的情況下，運算符與它的操作數如何緊密綁定的。可以使用上下文關鍵字`precedence`並_優先級\(precedence level\)_一起來指定一個運算符的優先級。_優先級_可以是0到255之間的任何一個數字\(十進制整數\)；與十進制整數字面量不同的是，它不可以包含任何下劃線字符。儘管優先級是一個特定的數字，但它僅用作與另一個運算符比較\(大小\)。也就是說，一個操作數可以同時被兩個運算符使用時，例如`2 + 3 * 5`，優先級更高的運算符將優先與操作數綁定。

運算符的_結合性_可以指定在沒有括號包圍的情況下，優先級相同的運算符以何種順序被分組的。可以使用上下文關鍵字`associativity`並_結合性\(associativity\)_一起來指定一個運算符的結合性，其中_結合性_可以說是上下文關鍵字`left`，`right`或`none`中的任何一個。左結合運算符以從左到右的形式分組。例如，減法運算符\(`-`\)具有左結合性，因此`4 - 5 - 6`被以`(4 - 5) - 6`的形式分組，其結果為`-7`。 右結合運算符以從右到左的形式分組，對於設置為`none`的非結合運算符，它們不以任何形式分組。具有相同優先級的非結合運算符，不可以互相鄰接。例如，表達式`1 < 2 < 3`非法的。

聲明時不指定任何優先級或結合性的中綴運算符，它們的優先級會被初始化為100，結合性被初始化為`none`。

下面的這種形式聲明了一個新的前綴運算符：

> operator prefix `operator name`{}

緊跟在操作數前邊的_前綴運算符\(prefix operator\)_是一元運算符，例如表達式`++i`中的前綴遞增運算符\(`++`\)。

前綴運算符的聲明中不指定優先級。前綴運算符是非結合的。

下面的這種形式聲明了一個新的後綴運算符：

> operator postfix `operator name`{}

緊跟在操作數後邊的_後綴運算符\(postfix operator\)_是一元運算符，例如表達式`i++`中的前綴遞增運算符\(`++`\)。

和前綴運算符一樣，後綴運算符的聲明中不指定優先級。後綴運算符是非結合的。

聲明了一個新的運算符以後，需要聲明一個跟這個運算符同名的函數來實現這個運算符。如何實現一個新的運算符，請參考[Custom Operators](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_48)。

> 運算符聲明語法  
> _運算符聲明_ → [_前置運算符聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#prefix_operator_declaration) \| [_後置運算符聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#postfix_operator_declaration) \| [_中置運算符聲明_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#infix_operator_declaration)  
> _前置運算符聲明_ → **運算符** **prefix** [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator) **{** **}**  
> _後置運算符聲明_ → **運算符** **postfix** [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator) **{** **}**  
> _中置運算符聲明_ → **運算符** **infix** [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator) **{** [_中置運算符屬性_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#infix_operator_attributes) _可選_ **}**  
> _中置運算符屬性_ → [_優先級子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#precedence_clause) _可選_ [_結和性子句_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#associativity_clause) _可選_  
> _優先級子句_ → **precedence** [_優先級水平_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#precedence_level)  
> _優先級水平_ → 數值 0 到 255  
> _結和性子句_ → **associativity** [_結和性_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/05_Declarations.html#associativity)  
> _結和性_ → **left** \| **right** \| **none**

