### **PolyNode.Childs**

```
Del.» property Childs[index: Integer]: TPolyNode; //read only

C++ » std::vector < PolyNode* > Childs;//public field

C#  » public List < PolyNode > Childs; //read only property
```

会返回只读的PolyNode子对象内容。
外轮廓会包含内轮廓，而孔洞轮廓会包含被嵌套的外轮廓。