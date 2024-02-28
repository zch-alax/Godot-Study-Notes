# Node节点  
Node节点，是基类节点，所有节点都会继承Node节点，所以其它类型都包含Node节点的功能，相当于java的Object类。  
节点的三种状态：  
1. Inherit（继承）：处理与否取决于父、祖父等等节点中第一个非 Inherit 状态的节点。  
2. Stop（停止）：无条件停止节点（以及 Inherit 模式的子节点）。暂停时该节点不会进行处理。  
3. Process（处理）：无条件处理节点（以及 Inherit 模式的子节点）。无论暂停与否，该节点都会进行处理。比如 父节点状态为Stop，子节点状态为Process，则父节点停止运行，而子节点依旧运行。  
# CanvasItem节点  
Canvas是画布的意思，所以CanvasItem代表了就是可以被绘制节点，可以设置可视化界面和材质的颜色。  
所有2D节点与GUI节点都继承于CanvasItem节点。  
主要属性如下：  
1. Texture 贴图，附加到物体表面的贴图
2. Material 材质，物体的质地，指色彩，纹理，光滑度，透明度，反射率，折射率，发光度。实际就是Shader  
3. Shader 着色器，使用代码来渲染图形的技术，可以控制GPU运算图像效果的一段代码  
# Node2D节点  
继承关系：Node2D -> CanvasItem -> Node，主要属性如下：  
1. Position 位置
2. Rotation 旋转
3. Scale 缩放  
