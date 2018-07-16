### **JoinType**

```
Del.» type TJoinType = (jtSquare, jtRound, jtMiter);

C++ » enum JoinType {jtSquare, jtRound, jtMiter};

C#  » public enum JoinType {jtSquare, jtRound, jtMiter};
```

当在ClipperOffset对象中通过AddPaths函数添加路径时，相交类型参数可从jtMiter,jtSquare和jtRound中选一个；
![](jointypes.png)
jtMiter:对于斜接式交点来说，有必要设定一个阈值，因为偏置的轮廓在极其窄的相交点处可能会造成过“尖角”。为了将这些潜在的尖角包含在内，ClipperOffset对象的MiterLimit属性用来制定一个偏置点所能容忍的最大值；对于所有给定的边缘交点处，一旦斜接式交点超过了该阈值，那么方形交角将会被应用；
jtRound:当扁平的路径始终无法完美的获取角度信息，他们等价于一系列的圆弧曲线（可以查阅ClipperObject的ArcTolerance属性）
jtSquare:相当于斜接式当中的delta值始终为1的情况；