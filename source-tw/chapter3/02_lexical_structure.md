# 02\_Lexical\_Structure

> 翻譯：[superkam](https://github.com/superkam)  
> 校對：[numbbbbb](https://github.com/numbbbbb)

## 詞法結構

本頁包含內容：

* [空白與註釋（_Whitespace and Comments_）](02_lexical_structure.md#whitespace_and_comments)
* [標識符（_Identifiers_）](02_lexical_structure.md#identifiers)
* [關鍵字（_Keywords_）](02_lexical_structure.md#keywords)
* [字面量（_Literals_）](02_lexical_structure.md#literals)
* [運算符（_Operators_）](02_lexical_structure.md#operators)

Swift 的「詞法結構（_lexical structure_）」描述了如何在該語言中用字符序列構建合法標記，組成該語言中最底層的代碼塊，並在之後的章節中用於描述語言的其他部分。

通常，標記在隨後介紹的語法約束下，由 Swift 源文件的輸入文本中提取可能的最長子串生成。這種方法稱為「最長匹配項（_longest match_）」，或者「最大適合」（_maximal munch_）。

### 空白與註釋

空白（_whitespace_）有兩個用途：分隔源文件中的標記和區分運算符屬於前綴還是後綴，（參見 [運算符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_871)）在其他情況下則會被忽略。以下的字符會被當作空白：空格（_space_）（U+0020）、換行符（_line feed_）（U+000A）、回車符（_carriage return_）（U+000D）、水平 tab（_horizontal tab_）（U+0009）、垂直 tab（_vertical tab_）（U+000B）、換頁符（_form feed_）（U+000C）以及空（_null_）（U+0000）。

註釋（_comments_）被編譯器當作空白處理。單行註釋由 `//` 開始直到該行結束。多行註釋由 `/*` 開始，以 `*/` 結束。可以嵌套註釋，但注意註釋標記必須匹配。

### 標識符

標識符（_identifiers_）可以由以下的字符開始：大寫或小寫的字母 `A` 到 `Z`、下劃線 `_`、基本多語言面（_Basic Multilingual Plane_）中的 Unicode 非組合字符以及基本多語言面以外的非專用區（_Private Use Area_）字符。首字符之後，標識符允許使用數字和 Unicode 字符組合。

使用保留字（_reserved word_）作為標識符，需要在其前後增加反引號 `````。例如，`class` 不是合法的標識符，但可以使用 ```class```。反引號不屬於標識符的一部分，```x``` 和 `x` 表示同一標識符。

閉包（_closure_）中如果沒有明確指定參數名稱，參數將被隱式命名為 `$0`、`$1`、`$2`... 這些命名在閉包作用域內是合法的標識符。

> 標識符語法  
> _標識符_ → [_標識符頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_head) [_標識符字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_characters) _可選_  
> _標識符_ → **\`** [_標識符頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_head) [_標識符字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_characters) _可選_ **\`**  
> _標識符_ → [_隱式參數名_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#implicit_parameter_name)  
> _標識符列表_ → [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) \| [_標識符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier) **,** [_標識符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_list)  
> _標識符頭\(Head\)_ → Upper- or lowercase letter A through Z  
> _標識符頭\(Head\)_ → U+00A8, U+00AA, U+00AD, U+00AF, U+00B2–U+00B5, or U+00B7–U+00BA  
> _標識符頭\(Head\)_ → U+00BC–U+00BE, U+00C0–U+00D6, U+00D8–U+00F6, or U+00F8–U+00FF  
> _標識符頭\(Head\)_ → U+0100–U+02FF, U+0370–U+167F, U+1681–U+180D, or U+180F–U+1DBF  
> _標識符頭\(Head\)_ → U+1E00–U+1FFF  
> _標識符頭\(Head\)_ → U+200B–U+200D, U+202A–U+202E, U+203F–U+2040, U+2054, or U+2060–U+206F  
> _標識符頭\(Head\)_ → U+2070–U+20CF, U+2100–U+218F, U+2460–U+24FF, or U+2776–U+2793  
> _標識符頭\(Head\)_ → U+2C00–U+2DFF or U+2E80–U+2FFF  
> _標識符頭\(Head\)_ → U+3004–U+3007, U+3021–U+302F, U+3031–U+303F, or U+3040–U+D7FF  
> _標識符頭\(Head\)_ → U+F900–U+FD3D, U+FD40–U+FDCF, U+FDF0–U+FE1F, or U+FE30–U+FE44  
> _標識符頭\(Head\)_ → U+FE47–U+FFFD  
> _標識符頭\(Head\)_ → U+10000–U+1FFFD, U+20000–U+2FFFD, U+30000–U+3FFFD, or U+40000–U+4FFFD  
> _標識符頭\(Head\)_ → U+50000–U+5FFFD, U+60000–U+6FFFD, U+70000–U+7FFFD, or U+80000–U+8FFFD  
> _標識符頭\(Head\)_ → U+90000–U+9FFFD, U+A0000–U+AFFFD, U+B0000–U+BFFFD, or U+C0000–U+CFFFD  
> _標識符頭\(Head\)_ → U+D0000–U+DFFFD or U+E0000–U+EFFFD  
> _標識符字符_ → 數值 0 到 9  
> _標識符字符_ → U+0300–U+036F, U+1DC0–U+1DFF, U+20D0–U+20FF, or U+FE20–U+FE2F  
> _標識符字符_ → [_標識符頭\(Head\)_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_head)  
> _標識符字符列表_ → [_標識符字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_character) [_標識符字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#identifier_characters) _可選_  
> _隱式參數名_ → **$** [_十進制數字列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_digits)

### 關鍵字

被保留的關鍵字（_keywords_）不允許用作標識符，除非被反引號轉義，參見 [標識符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/LexicalStructure.html#//apple_ref/doc/uid/TP40014097-CH30-XID_796)。

* **用作聲明的關鍵字：** _class_、_deinit_、_enum_、_extension_、_func_、_import_、_init_、_let_、_protocol_、_static_、_struct_、_subscript_、_typealias_、_var_
* **用作語句的關鍵字：** _break_、_case_、_continue_、_default_、_do_、_else_、_fallthrough_、_if_、_in_、_for_、_return_、_switch_、_where_、_while_
* **用作表達和類型的關鍵字：** _as_、_dynamicType_、_is_、_new_、_super_、_self_、_Self_、_Type_、_\_\_COLUMN\_\__、_\_\_FILE\_\__、_\_\_FUNCTION\_\__、_\_\_LINE\_\__
* **特定上下文中被保留的關鍵字：** _associativity_、_didSet_、_get_、_infix_、_inout_、_left_、_mutating_、_none_、_nonmutating_、_operator_、_override_、_postfix_、

  _precedence_、_prefix_、_right_、_set_、_unowned_、_unowned\(safe\)_、_unowned\(unsafe\)_、_weak_、_willSet_，這些關鍵字在特定上下文之外可以被用於標識符。

### 字面量

字面值表示整型、浮點型數字或文本類型的值，舉例如下：

```swift
42                 // 整型字面量
3.14159            // 浮點型字面量
"Hello, world!"    // 文本型字面量
```

> 字面量語法  
> _字面量_ → [_整型字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#integer_literal) \| [_浮點數字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#floating_point_literal) \| [_字符串字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#string_literal)

#### 整型字面量

整型字面量（_integer literals_）表示未指定精度整型數的值。整型字面量默認用十進製表示，可以加前綴來指定其他的進制，二進制字面量加 `0b`，八進制字面量加 `0o`，十六進制字面量加 `0x`。

十進制字面量包含數字 `0` 至 `9`。二進制字面量只包含 `0` 或 `1`，八進制字面量包含數字 `0` 至 `7`，十六進制字面量包含數字 `0` 至 `9` 以及字母 `A` 至 `F` （大小寫均可）。

負整數的字面量在數字前加減號 `-`，比如 `-42`。

允許使用下劃線 `_` 來增加數字的可讀性，下劃線不會影響字面量的值。整型字面量也可以在數字前加 `0`，同樣不會影響字面量的值。

```swift
1000_000     // 等於 1000000
005          // 等於 5
```

除非特殊指定，整型字面量的默認類型為 Swift 標準庫類型中的 `Int`。Swift 標準庫還定義了其他不同長度以及是否帶符號的整數類型，請參考 [整數類型](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-XID_411)。

> 整型字面量語法  
> _整型字面量_ → [_二進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_literal)  
> _整型字面量_ → [_八進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_literal)  
> _整型字面量_ → [_十進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal)  
> _整型字面量_ → [_十六進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal)  
> _二進制字面量_ → **0b** [_二進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_digit) [_二進制字面量字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_literal_characters) _可選_  
> _二進制數字_ → 數值 0 到 1  
> _二進制字面量字符_ → [_二進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_digit) \| **\_**  
> _二進制字面量字符列表_ → [_二進制字面量字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_literal_character) [_二進制字面量字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#binary_literal_characters) _可選_  
> _八進制字面量_ → **0o** [_八進字數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_digit) [_八進制字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_literal_characters) _可選_  
> _八進字數字_ → 數值 0 到 7  
> _八進制字符_ → [_八進字數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_digit) \| **\_**  
> _八進制字符列表_ → [_八進制字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_literal_character) [_八進制字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#octal_literal_characters) _可選_  
> _十進制字面量_ → [_十進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_digit) [_十進制字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal_characters) _可選_  
> _十進制數字_ → 數值 0 到 9  
> _十進制數字列表_ → [_十進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_digit) [_十進制數字列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_digits) _可選_  
> _十進制字符_ → [_十進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_digit) \| **\_**  
> _十進制字符列表_ → [_十進制字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal_character) [_十進制字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal_characters) _可選_  
> _十六進制字面量_ → **0x** [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制字面量字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal_characters) _可選_  
> _十六進制數字_ → 數值 0 到 9, a through f, or A through F  
> _十六進制字符_ → [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) \| **\_**  
> _十六進制字面量字符列表_ → [_十六進制字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal_character) [_十六進制字面量字符列表_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal_characters) _可選_

#### 浮點型字面量

浮點型字面量（_floating-point literals_）表示未指定精度浮點數的值。

浮點型字面量默認用十進製表示（無前綴），也可以用十六進製表示（加前綴 `0x`）。

十進制浮點型字面量（_decimal floating-point literals_）由十進制數字串後跟小數部分或指數部分（或兩者皆有）組成。十進制小數部分由小數點 `.` 後跟十進制數字串組成。指數部分由大寫或小寫字母 `e` 後跟十進制數字串組成，這串數字表示 `e` 之前的數量乘以 10 的幾次方。例如：`1.25e2` 表示 `1.25 □ 10^2`，也就是 `125.0`；同樣，`1.25e－2` 表示 `1.25 □ 10^－2`，也就是 `0.0125`。

十六進制浮點型字面量（_hexadecimal floating-point literals_）由前綴 `0x` 後跟可選的十六進制小數部分以及十六進制指數部分組成。十六進制小數部分由小數點後跟十六進制數字串組成。指數部分由大寫或小寫字母 `p` 後跟十進制數字串組成，這串數字表示 `p` 之前的數量乘以 2 的幾次方。例如：`0xFp2` 表示 `15 □ 2^2`，也就是 `60`；同樣，`0xFp-2` 表示 `15 □ 2^-2`，也就是 `3.75`。

與整型字面量不同，負的浮點型字面量由一元運算符減號 `-` 和浮點型字面量組成，例如 `-42.0`。這代表一個表達式，而不是一個浮點整型字面量。

允許使用下劃線 `_` 來增強可讀性，下劃線不會影響字面量的值。浮點型字面量也可以在數字前加 `0`，同樣不會影響字面量的值。

```swift
10_000.56     // 等於 10000.56
005000.76     // 等於 5000.76
```

除非特殊指定，浮點型字面量的默認類型為 Swift 標準庫類型中的 `Double`，表示64位浮點數。Swift 標準庫也定義 `Float` 類型，表示32位浮點數。

> 浮點型字面量語法  
> _浮點數字面量_ → [_十進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal) [_十進制分數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_fraction) _可選_ [_十進制指數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_exponent) _可選_  
> _浮點數字面量_ → [_十六進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal) [_十六進制分數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_fraction) _可選_ [_十六進制指數_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_exponent)  
> _十進制分數_ → **.** [_十進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal)  
> _十進制指數_ → [_浮點數e_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#floating_point_e) [_正負號_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#sign) _可選_ [_十進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#decimal_literal)  
> _十六進制分數_ → **.** [_十六進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal) _可選_  
> _十六進制指數_ → [_浮點數p_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#floating_point_p) [_正負號_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#sign) _可選_ [_十六進制字面量_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_literal)  
> _浮點數e_ → **e** \| **E**  
> _浮點數p_ → **p** \| **P**  
> _正負號_ → **+** \| **-**

#### 文本型字面量

文本型字面量（_string literal_）由雙引號中的字符串組成，形式如下：

```swift
"characters"
```

文本型字面量中不能包含未轉義的雙引號 `"`、未轉義的反斜線`\`、回車符（_carriage return_）或換行符（_line feed_）。

可以在文本型字面量中使用的轉義特殊符號如下：

* 空字符（Null Character）`\0`
* 反斜線（Backslash）`\\`
* 水平 Tab （Horizontal Tab）`\t`
* 換行符（Line Feed）`\n`
* 回車符（Carriage Return）`\r`
* 雙引號（Double Quote）`\"`
* 單引號（Single Quote）`\'`

字符也可以用以下方式表示：

* `\x` 後跟兩位十六進制數字
* `\u` 後跟四位十六進制數字
* `\U` 後跟八位十六進制數字

後跟的數字表示一個 Unicode 碼點。

文本型字面量允許在反斜線小括號 `\()` 中插入表達式的值。插入表達式（_interpolated expression_）不能包含未轉義的雙引號 `"`、反斜線 `\`、回車符或者換行符。表達式值的類型必須在 _String_ 類中有對應的初始化方法。

例如，以下所有文本型字面量的值相同：

```swift
"1 2 3"
"1 2 \(3)"
"1 2 \(1 + 2)"
var x = 3; "1 2 \(x)"
```

文本型字面量的默認類型為 `String`。組成字符串的字符類型為 `Character`。更多有關 `String` 和 `Character` 的信息請參照 [字符串和字符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/StringsAndCharacters.html#//apple_ref/doc/uid/TP40014097-CH7-XID_368)。

> 字符型字面量語法  
> _字符串字面量_ → **"** [_引用文本_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#quoted_text) **"**  
> _引用文本_ → [_引用文本條目_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#quoted_text_item) [_引用文本_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#quoted_text) _可選_  
> _引用文本條目_ → [_轉義字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#escaped_character)  
> _引用文本條目_ → **\(** [_表達式_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/04_Expressions.html#expression) **\)**  
> _引用文本條目_ → 除了"-, -, U+000A, or U+000D的所有Unicode的字符  
> _轉義字符_ → **\0** \| **\** \| **\t** \| **\n** \| **\r** \| **\"** \| **\'**  
> _轉義字符_ → **\x** [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit)  
> _轉義字符_ → **\u** [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit)  
> _轉義字符_ → **\U** [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit) [_十六進制數字_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#hexadecimal_digit)

### 運算符

Swift 標準庫定義了許多可供使用的運算符，其中大部分在 [基礎運算符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-XID_70) 和 [高級運算符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_28) 中進行了闡述。這裡將描述哪些字符能用作運算符。

運算符由一個或多個以下字符組成： `/`、`=`、`-`、`+`、`!`、`*`、`%`、`<`、`>`、`&`、`|`、`^`、`~`、`.`。也就是說，標記 `=`, `->`、`//`、`/*`、`*/`、`.` 以及一元前綴運算符 `&` 屬於保留字，這些標記不能被重寫或用於自定義運算符。

運算符兩側的空白被用來區分該運算符是否為前綴運算符（_prefix operator_）、後綴運算符（_postfix operator_）或二元運算符（_binary operator_）。規則總結如下：

* 如果運算符兩側都有空白或兩側都無空白，將被看作二元運算符。例如：`a+b` 和 `a + b` 中的運算符 `+` 被看作二元運算符。
* 如果運算符只有左側空白，將被看作前綴一元運算符。例如 `a ++b` 中的 `++` 被看作前綴一元運算符。
* 如果運算符只有右側空白，將被看作後綴一元運算符。例如 `a++ b` 中的 `++` 被看作後綴一元運算符。
* 如果運算符左側沒有空白並緊跟 `.`，將被看作後綴一元運算符。例如 `a++.b` 中的 `++` 被看作後綴一元運算符（同理， `a++ . b` 中的 `++` 是後綴一元運算符而 `a ++ .b` 中的 `++` 不是）.

鑒於這些規則，運算符前的字符 `(`、`[` 和 `{` ；運算符後的字符 `)`、`]` 和 `}` 以及字符 `,`、`;` 和 `:` 都將用於空白檢測。

以上規則需注意一點，如果運算符 `!` 或 `?` 左側沒有空白，則不管右側是否有空白都將被看作後綴運算符。如果將 `?` 用作可選類型（_optional type_）修飾，左側必須無空白。如果用於條件運算符 `? :`，必須兩側都有空白。

在特定構成中 ，以 `<` 或 `>` 開頭的運算符會被分離成兩個或多個標記，剩餘部分以同樣的方式會被再次分離。因此，在 `Dictionary<String, Array<Int>>` 中沒有必要添加空白來消除閉合字符 `>` 的歧義。在這個例子中， 閉合字符 `>` 被看作單字符標記，而不會被誤解為移位運算符 `>>`。

要學習如何自定義新的運算符，請參考 [自定義操作符](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_48) 和 [運算符聲明](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Declarations.html#//apple_ref/doc/uid/TP40014097-CH34-XID_644)。學習如何重寫現有運算符，請參考 [運算符方法](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/AdvancedOperators.html#//apple_ref/doc/uid/TP40014097-CH27-XID_43)。

> 運算符語法語法  
> _運算符_ → [_運算符字符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator_character) [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator) _可選_  
> _運算符字符_ → **/** \| **=** \| **-** \| **+** \| **!** \| **\*** \| **%** \| **&lt;** \| **&gt;** \| **&** \| **\|** \| **^** \| **~** \| **.**  
> _二元運算符_ → [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator)  
> _前置運算符_ → [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator)  
> _後置運算符_ → [_運算符_](https://github.com/ininmm/the-swift-programming-language-in-chinese/tree/8b9f8ba4cb97148e9d1b43c50f9e1c8e4175f753/source-tw/chapter3/LexicalStructure.html#operator)

