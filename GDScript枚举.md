```GDScript
#enum Alignment {ALLY, NEUTRAL, ENEMY} # 不赋值，默认为0，1，2
enum Alignment {ALLY = 1, NEUTRAL = 0, ENEMY = -1}
# var unit_alignment = Alignment.ALLY
# 导出到检视器上，可以在检视器上选择对应的元素
@export var unit_alignment: Alignment

func _ready():
    if unit_alignment == Alignment.ENEMY:
        print("You are not welcome here.")
    else:
        print("Welcome!")

    # 相当于swith	
    match unit_alignment:
        Alignment.ALLY:
            print("Hello!Friend!")
        Alignment.NEUTRAL:
            print("Hello!")
        Alignment.ENEMY:
            print("KILL YOU!")
        _:
            print("WHO ARE YOU?")
```
