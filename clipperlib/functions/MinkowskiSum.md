### **MinkowskiSum**

```
Del.» function MinkowskiSum(const Pattern: TPath; const Path: TPath; PathIsClosed: Boolean): TPaths; overload;

Del.» function MinkowskiSum(const Pattern: TPath; const Paths: TPaths; PathFillType: TPolyFillType; PathIsClosed: Boolean): TPaths; overload;

C++ » void MinkowskiSum(const Path& pattern, const Path& path, Paths& solution, bool pathIsClosed);

C++ » void MinkowskiSum(const Path& pattern, const Paths& paths, Paths& solution, PolyFillType pathFillType, bool pathIsClosed);

C#  » public static Paths MinkowskiSum(Path pattern, Path path, bool pathIsClosed);

C#  » public static Paths MinkowskiSum(Path pattern, Paths paths, PolyFillType pathFillType, bool pathIsClosed);
```

（待编写）闵可夫斯基和。