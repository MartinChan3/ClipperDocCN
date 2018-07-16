### **Clipper.StrictlySimple**

```
Del.» property StrictlySimple: boolean; override;

C++ » void StrictlySimple(bool value);

C#  » public bool StrictlySimple { get {} set {} };
```

术语：
- 一个简单多边形是指没有自交现象的多边形；
- 一个弱简单多边形是指一个简单多边形包含重合点以及重合的线段；
- 一个强简单多边形是指一个简单多边形不包含重合点以及重合的线段；

对于点“重合”的定义是指如果多边形内的两个以上的点具有相同的坐标（并且在序列上来说不是相邻点，即相邻点除外）。一个边接触到另一条边的定义是指这条边的一个端点与接触到另一条边（相邻边除外）相接触，或者他们是共线或覆盖关系（包括相邻边）。

由Clipper库的裁剪操作返回的多边形都是简单多边形。当StrictlySimply属性被启用，返回的多边形将会是强简单多边形，否则会返回弱简单多边形。算法因为计算强简单多边形太大，导致该选项是默认关闭的；

注意：目前无法保证输出多边形是严格简单的因为“简单化”工作还在进行当中；
![](simplify2.png)
![](simplify3.png)
在上述图片中，两个例子显示出两个弱简单多边形被打断为两个强简单多边形（外围轮廓的方向是为了避免视觉上点集顺序的错误）

参考维基百科上的[简单多边形](https://en.wikipedia.org/wiki/Simple_polygon)词条；