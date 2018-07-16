### **ClipperOffset.Constructor**

```
Del.» constructor Create(MiterLimit: Double = 2; RoundPrecision: Double = 0.25);

C++ » ClipperOffset( double miterLimit = 2.0, double roundPrecision = 0.25);

C#  » public ClipperOffset( double miterLimit = 2.0, double roundPrecision = 0.25);
```

构造函数包含了两个可选的参数：MiterLimit和ArcTolerance，这两个参数和其同名的属性的含义是相同的。MiterLimit只有在JoinType是jtMiter的时候才启用，ArcTolerance只有在JoinType是jtRound或者当EndType是开放式轮廓的时候才有效；
