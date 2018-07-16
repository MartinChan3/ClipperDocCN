### **ReversePath**

```
Del.» function SimplifyPolygon(const Poly: TPath; FillType: TPolyFillType = pftEvenOdd): TPaths;

C++ » void SimplifyPolygon(const Path &in_poly, Paths &out_polys, 
        PolyFillType fillType = pftEvenOdd);

C#  » public static Paths SimplifyPolygon(Path poly, 
        PolyFillType fillType = PolyFillType.pftEvenOdd);
```

将自交部分从自身的部分中剔除（通过指定一个FillType来实现一个布尔的求和操作）。

多个没有相邻重复点（或者说没有“接触”）的多边形将会被分割为两个多边形组；

![](simplify.png)
![](simplify2.png)
![](simplify3.png)