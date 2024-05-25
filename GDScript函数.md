1. 函数的创建方式
```GDScript
func _ready():
	var result = add(1, 2)
	print(result)

func add(num1: int, num2: int) -> int:
	var result = num1 + num2
	return result
```

2. _ready()、_input()这些函数前面的_是什么意思？  
这是为了表明不是由我们调用的，而是引擎本身调用的。
3. randf()函数  
randf()函数会返回一个0-1之间的随机数。用于为游戏分配概率，比如战利品的稀有度等
```GDScript
func get_rand():
    randf() # 返回一个0-1之间的随机数
    var a = randi_range(10, 100) # 返回一个指定最小值-最大值之间的随机整数
    randf_range(11.1, 23.5) # 返回一个指定最小值-最大值的随机小数
```
