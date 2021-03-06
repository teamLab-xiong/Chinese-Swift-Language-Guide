# 高级操作符

除了[基本操作符](Basic_Operators.md)中描述的操作符，Swift提供了几个高级操作符来执行复杂值操作。这些包括C和Objective-C中你熟悉的，所有按位和位移操作符。

不像C中的算术运算，Swift中的算术操作符默认不会溢出。溢出行为会作为错误包装并报告。如果选择处理溢出行为，用Swift中默认会溢出的第二套算术操作符，例如溢出加法操作符(`&+`)。所有的溢出操作符都以(`&`)符号开头。

当你定义自己的结构体、类和枚举时，为其提供Swift标准操作符的自身实现比较有用。Swift让给这些操作符定制实现，和决定你创建的每个类型的行为变得简单。

并不仅限于预定义操作符。Swift给你自定义具有优先性和关联性的中缀、前缀、后缀和复制操作符的自由。这些操作符可以像其他预定义操作符一样用在你的代码中，你甚至可以扩展现有类型以支持你自定义的操作符。

## 位操作符

*位操作符* 允许你操作一个数据结构中单独的原始数据的比特位。在底层编程中经常用到，如图形编程和设备驱动程序。当使用外部源数据时位操作符也比较有用，例如自定义协议间交流数据的编码和解码。

Swift支持C中所有的位操作符，如下面所述。

### 位取反操作符（NOT）

位取反操作符(`~`)翻转一个数中所有的位：

<p align="center">
<img src="https://docs.swift.org/swift-book/_images/bitwiseNOT_2x.png" alt="取反操作符（NOT）" width="300"/>
</p>

位取反操作符是一个前缀操作符，出现在要操作的数的正前面，不需要空格：
```swift
let initialBits: UInt8 = 0b00001111
let invertedBits = ~initialBits // equals 11110000
```

`UInt8`整数有8个比特位，可以存放从`0`到`255`任何数。这个例子用二进制值`00001111`初始化一个`UInt8`整数，前面四位设为`0`，后面四位设为`1`。这等同于十进制的`15`。














[< 访问控制](Access_Control.md) || [关于本指南 >](../Language_Reference/Advanced_Operators.md)
