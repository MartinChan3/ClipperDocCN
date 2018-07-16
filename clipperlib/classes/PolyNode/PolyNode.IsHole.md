### **PolyNode.IsHole**

```
Del.» IsHole: Boolean; //read only

C++ » bool IsHole; //field

C#  » public bool IsHole; //read only property
```

当该PolyNode为孔洞时，返回true;
外轮廓的子对象永远为孔洞，同时孔洞的子对象永远为（被嵌套）的外轮廓；
对于PolyTree来说没有定义IsHole属性，但是其最高层的子对象永远都是外轮廓；