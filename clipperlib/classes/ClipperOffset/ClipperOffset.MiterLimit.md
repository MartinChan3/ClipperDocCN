### **ClipperOffset.MiterLimit**

```
Del.» property MiterLimit: double; //read and write

C++ » double MiterLimit;

C#  » public double MiterLimit {get; set;}
```

该属性包含了一个比例系数（= 最大容忍距离/偏置距离），当大于最大容忍距离时，则会使用1*delta距离来进行阶段；
**默认的MiterLimit值大小是2**，这也是允许的最小MiterLimit大小。如果没有规定合理的MiterLimit，在部分尖锐的拐角处就会形成长的突起；例子如下图所示
![](miterlimit.png)