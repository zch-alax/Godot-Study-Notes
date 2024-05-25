# SET
示例:
```GDScript
signal health_changed(new_health)

var health := 100:
	set(value):
		health = clamp(value, 0, 100) # 设置最大最小值 小于0则赋值0 大于100则赋值100
		health_changed.emit(health)
		
func _ready():
	health_changed.connect(_on_health_changed)
	health = -150
	
func _on_health_changed(new_health):
	print(new_health)
```
