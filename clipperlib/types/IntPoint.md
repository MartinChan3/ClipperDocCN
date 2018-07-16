### **IntPoint**

```
Del.» TIntPoint = record X, Y: cInt; end;

C++ » struct IntPoint { cInt X; cInt Y; ... };

C#  » public class IntPoint { public cInt X; { get; set; } public cInt Y; { get; set; } ... };
```

整形点数据结构用来代表Clipper库中相关的所有点；Clipper库刻意选择了整形存储类型类保证数值稳定。（同上文）
一系列的IntPoint被保存在Path结构中，构成了一个轮廓。
在版本6.0以上，IntPoint现在可以拥有第三个成员“Z”。这可以通过在预编译器中定义“use_xyz”来实现。当Z轴数据也被加入时，它的值也会被考虑进裁剪的行为中去；但是，在那些没有对应的Z值的交点处，该值会被设定为0，除非用户提供了回调函数；
用户如果希望使用浮点数进行Clip，那么必须手动的进行正确的对浮点数进行缩放为IntPoint，再使用Clipper数进行处理；