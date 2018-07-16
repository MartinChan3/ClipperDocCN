### **IntRect**

```
Del.»
TIntRect = record left, top, right, bottom: cInt; end;

C++ »
struct IntRect { cInt left; cInt top; cInt right; cInt bottom; ... };

C#  »
public class IntRect {
  public cInt left; { get; set; }
  public cInt top; { get; set; }
  public cInt right; { get; set; }
  public cInt bottom; { get; set; } ... };
```

用于接受Clipper库的GetBounds()函数的结果（包围盒）；