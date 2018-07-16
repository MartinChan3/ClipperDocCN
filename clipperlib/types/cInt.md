### **cInt**

```
Del.»
{$IFDEF use_int32}
 cInt = Int32;
{$ELSE}
  cInt = Int64;
{$ENDIF}

C++ »
#ifdef use_int32
  typedef int cInt;
#else
  typedef signed long long cInt;
#endif

C#  »
#if use_int32
  using cInt = Int32;
#else
  using cInt = Int64;
#endif
```

cInt是Clipper库用来表示点坐标数据使用的。目前Clipper库使用整形数据代替浮点数据来保证数据的鲁棒性。（在一开始的版本中曾经使用Clipper库中的浮点数据，但是和明显浮点数的不精确性引起了一些偶然性错误）；
默认的cInt代表了一个有符号64位整形数据并且整个多边形的坐标范围可以达到±9.2e+18的范围内。这容纳了整个浮点数坐标可以使其精度得到最完整的保留。但是，如果坐标范围可以被控制在 ± 3.0e+9之内，那么通过避免了大数的运算，可以得到大约百分之十的效率提升。如果预编译器定义了use_int32，则效率可以更高，详情见下方。