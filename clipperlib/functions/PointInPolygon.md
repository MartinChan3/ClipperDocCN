### **PointInPolygon**

```
Del.» function PointInPolygon(const Pt: TIntPoint; const poly: TPath): Integer;

C++ » int PointInPolygon(const IntPoint pt, const Path &poly); // Function in the ClipperLib namespace.

C#  » public static int PointInPolygon(IntPoint pt, Path poly); // Static method of the Clipper class.
```

判断点是否在多边形内，如果返回0则是不在，-1则为在多边形边缘上，1为在多边形内；