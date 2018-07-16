### **PolyTree.GetFirst**

```
Del.» function GetFirst: TPolyNode;

C++ » PolyNode* GetFirst();

C#  » public PolyNode GetFirst();
```

该方法返回第一个有效的polygon的PolyNode指针，否则返回空；

该方法等价于调用Child[0]除非一个PolyTree的对象为空（无任何子对象），这种情况下使用Child[0]会产生越界。
