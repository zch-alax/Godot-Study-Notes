# SET(常用于限制范围或者发送信号)
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
# GET(通常用于转换值)
```GDScript
var chance := 0.2
var chance_pct: int:
    get:
        return chance * 100
    set(value):
         chance = float(value) / 100
		

func _ready():
    print(chance_pct) # 20
    chance_pct = 40
    print(chance_pct) # 40
    chance = 0.6
    print(chance_pct) # 60
```
