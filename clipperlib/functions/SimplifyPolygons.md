### **SimplifyPolygons**

```
Del.» function SimplifyPolygons(const polys: TPaths; 
        FillType: TPolyFillType = pftEvenOdd): TPaths;

C++ » void SimplifyPolygons(const Paths &in_polys, Paths &out_polys, 
        PolyFillType fillType = pftEvenOdd);

C++ » void SimplifyPolygons(Paths &polys, PolyFillType fillType = pftEvenOdd);

C#  » public static Polygons SimplifyPolygons(Paths polys, 
        PolyFillType fillType = PolyFillType.pftEvenOdd);
```

将自交部分从自身的部分中剔除（通过指定一个FillType来实现一个布尔的求和操作）。

多个没有相邻重复点（或者说没有“接触”）的多边形将会被分割为两个多边形组；

![](simplify.png)
![](simplify2.png)
![](simplify3.png)