# 1.基础语法
## 1.声明变量 常量
变量：`var age = 10`
常量：`let age = 10`

## 2. 基本数据类型：

Int Float Double Bool  Character String Array Dictionary Tuple(元组类型) Optional(可选类型)

Swift中的中包括有符号整型和无符号整型

字符串：@"abc\(x)"  x为一个整型数据或其他：在Swift中没有stringWithFormat的用法  用\()代替

1> 定义一个指定类型的变量/ 常量，如下格式：
let age: Int = 10

2> Swift中的小数默认为Double型，需要自行设置为Float 
3> Swift强调语法安全：不同类型的两个变量 不能相加
4> 浮点数可以用十进制和十六进制表示 
十进制表示浮点数：eN：10的N次方

// 没有指数时
let d1 = 12.5
// 有指数
let d2 = 0.125e2
十六进制表示浮点数：pN:2的N次方   d3 = (8/16 + 12) * 1 = 12.5

let d3 = 0xC.8p0
// d3 = 0xC.8 * 2的0次方 = 12.5
3. Swift运算符：
1> 赋值=:
Swift可进行多个赋值：

基本的逻辑运算都一些样 强调赋值运算符：

= OC中的赋值运算符有返回值if(x = y)为永真  

Swift中这种写法属于语法错误，Swift中=没有具体返回值

2> 取余运算%：
Swift可以对浮点型数据进行取余运算 

a % b 结果所得余数的正负和a的符号一致

3>比较运算符：
Swift中的if语句必须是Bool型   true为真 false为假  没有C语言中非0为真的说法

三目运算符中的条件也必须是Bool型的  比较运算符和逻辑运算符的返回值为true 和 false两种（不是1 0）

4> 范围运算符（Swift新增）
a...b:范围是：[a, b]

a..<b: 范围是:[a, b)

Swift中的for循环：

for i in 0...5 {
// 执行6次 ：0 1 2 3 4 5
}
5> 溢出运算符：
&+ &- &/ &* &%

上溢出：最大值+1结果为0  下溢出：最小值-1结果为最大值

4. Swift新增的特殊数据类型：
1> 元组类型Tuple：
定义：有N个任意类型的数据组成

let po = (x : 12.6, y : 18 ) -----> x y是元素

例：

var point = (x : 10.3, y : 5)
/**
   *获取元组类型中的元素：
    *point.x  point.y
    * point.0(获取x) point.1(获取y)
**/ 
用let定义一个元组之后，不可以改变其中元素的值

下面语句错误：指定元素类型之后 不能加上元素的名称：

var person:(Int ,String) = (age : 23, name : "ha")
元组中：下划线可以忽略某个元素的值，以便取出其他的元素值