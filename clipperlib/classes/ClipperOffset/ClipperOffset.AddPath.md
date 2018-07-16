### **ClipperOffset.AddPath**

```
Del.» procedure AddPath(const Path: TPath; JoinType: TJoinType; EndType: TEndType);

C++ » void AddPath(const Path& path, JoinType jointype, EndType endtype);

C#  » public void AddPath(Path path, JoinType jointype, EndType endtype);
```

向ClipperOffset对象添加一个路径用来准备偏置；
其中开放式路径只能被偏移一个正值；

