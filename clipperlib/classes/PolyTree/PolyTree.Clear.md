### **PolyTree.Clear**

```
Del.» procedure Clear;

C++ » void Clear();

C#  » public void Clear();
```

该方法将删除PolyTree对象中的所有子对象。

Clear方法一般不需要显式的调用。每次执行Clipper.Execute方法每次接受一个PolyTree参数，并在生成新的结果之前会自动清除其中的内容。同样的，PolyTree的析构函数会自动清理其内部的包含的PolyNode。