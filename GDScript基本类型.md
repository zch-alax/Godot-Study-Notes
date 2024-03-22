# 5种基本类型  
1. Boolean  `var a = true` `var a: bool`
2. Integer，相当于java的long  `var b = 1` `var b: int`
3. Float，相当于java的double  `var c = 0.5` `var c: float`
4. String  `var d = "Hello"` `var d: String`
5. Null  `var e = null`

# 导出变量export
export关键字可以让变量在编辑器中编辑`@export var a = 1`，代表将a这个变量导出到编辑器上，并赋予a变量一个初始值1。除了导出数字，还有以下用法：
1. 导出路径`@export var b:NodePath`
2. 导出文件路径 `@export_file var c: String` `@export_file("*.txt") var d: String`

# 函数
空函数需要使用pass关键字
```
func test(parm1, parm2):
  # 执行代码
  return x
```
