### **Clipper.PreserveCollinear**

```
Del.» property PreserveCollinear: boolean; override;

C++ » void PreserveCollinear(bool value);

C#  » public bool PreserveCollinear { get {} set {} };
```

默认的，当输入的被裁剪和裁剪多边形的内容中三个或者更多的点是共线的，Clipper对象会在进行布尔运算之前对多余的共线点进行删除；当设定PreserveCollinear属性防止了这种行为，来允许共线的点的情况出现在结果当中；