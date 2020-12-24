## 1.基础语法
### 1.声明变量 常量
变量：
```swift 
var age = 10
```
常量：
```swift
let age = 10
```

### 2. 数据类型：
|类型||
|-|-|
|值类型|Int Float Double Bool Character String Array Dictionary Tuple Optional Set|
|引用类型|class|
    
### 3.小数默认为Double型，需要自行设置为Float 
```swift
let d1 = 12.5 // double     
let d2: float = 12.5 // float
```

### 4. let只能赋值一次，不要求在编译期间确定值，但是在使用之前必须赋值
```swift
// 正确
let a: Int
a = 10
printf(a)

// 正确
let a = 10
printf(a)

// 错误
let a: Int
printf(a) // 常量Constant 'a' used before being initialized
```