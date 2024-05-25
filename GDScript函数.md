_ready()、_input()这些函数前面的_是什么意思？
这是为了表明不是由我们调用的，而是引擎本身调用的。

```GDScript
func _ready():
	var result = add(1, 2)
	print(result)

func add(num1: int, num2: int) -> int:
	var result = num1 + num2
	return result
```
