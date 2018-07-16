### **Orientation**

```
Del.» function Orientation(const poly: TPath): boolean;

C++ » bool Orientation(const Path &poly); // Function in the ClipperLib namespace.

C#  » public static bool Orientation(Path poly); // Static method of the Clipper class in the ClipperLib namespace.
```

方向只有在封闭的曲线里面是重要的，方向的定义就是在给定的封闭曲线中给出点集是按照顺时针还是逆时针进行排列；
方向同样是跟轴的方向有关联的：
- 在Y轴向上显示模式中，方向变量为true对应的是为逆时针轮廓；
- 在Y轴向下显示模式中，方向变量为true对应的是为顺时针轮廓；

![](orientation.png)

> **Note**:
> 自交多边形有着不确定的方向性，此时函数不会返回一个有意义的值；
> 大部分2D的图形显示库（例如GDI、GDI+）甚至SVG文件格式有其坐标原点（在左上角，y轴方向朝下）。但是，一部分显示库（OpenGL等）可以自定义坐标原点，或者自定义Y方向朝上；
> 对于None-Zero填充的多边形，内环（内孔）的方向必须和外环相反；
> 对于由CLipper库的Execute方法，他们的外孔结果永远为true,内孔结果永远为false;(除非ReverseSolution属性已经被启用)