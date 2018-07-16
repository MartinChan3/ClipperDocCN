### **Area**

```
Del.» function Area(const pts: TPath): double;

C++ » double Area(const Path &poly);

C#  » public static double Area(Path poly);
```

该函数返回多边形的面积（默认输入的多边形为封闭轮廓）。根据方向的不同，该值大小可能为正或者负。如果方向为正，则结果为正，相反的，如果方向为负，则方向为负；