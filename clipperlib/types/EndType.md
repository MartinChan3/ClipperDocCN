### **EndType**

```
Del.» type TClipType = (ctIntersection, ctUnion, ctDifference, ctXor);

C++ » enum ClipType { ctIntersection, ctUnion, ctDifference, ctXor };

C#  » public enum ClipType { ctIntersection, ctUnion, ctDifference, ctXor };
```

关于EndType(结束类型)总共有五种值：
> - etClosedPolygon:末点是相交的，并且使用了JoinType来使路径视作一个多边形进行填充；
> - etClosedLine:末点是相交的，并且使用了JoinType来使路径视作一条线进行填充；
> - etOpenSqure:末点使用方形尾和扩展的delta角度；
> - etOpenRound:末点使用圆形尾和扩展的delta角度；
> - etOpenButt:末点使用了方向尾，并没有任何扩展；
> - ~~etOpenSingle~~:对一个开放式的多段线进行了偏置，等待未来更新；

注意：在etClosedPolygon和etClosedLine类型中，无论首末点是否重合，路径结束的情况将会相同。（主要针对部分图形格式，规定首末点相同，这里Clipper统一采用了非首末点相同的情况）；
![](endtypes1.png)
![](endtypes2.png)