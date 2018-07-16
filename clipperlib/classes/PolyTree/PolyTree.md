### **PolyTree**

继承自：**PolyNode**

PolyTree被设计成一个**只读**数据结构只能够用来接收裁剪或者偏置的结果。一般在结果中经常会选择是否使用Paths或者PolyTree来获取最终的结果；PolyTree数据结构优于Paths的两个点为1）能够正确反映返回类型的**父子关系** 2）能够对开放路径和闭合轮廓进行区别。但是，也正因为PolyTree有着比Paths更复杂的结构，导致算法效率下降大约5%以上。PolyTree目前只能用于需要寻找父子关系或开放路径需要考虑的场合；
在Clipper.Execute与ClipperOffset.Execute两个函数中，可以使用一个空的PolyTree对象来作为solution参数接收结果。一旦裁剪工作或者偏置工作完成后，函数就会将结果以PolyTree的形式返回出来；
一个PolyTree对象可以包含任何数目的PolyNode子对象，其中每一个PolyNode代表了多边形的一个轮廓（内轮廓或者外轮廓）。==PolyTree本身就是一个特殊的PolyNode对象，它的子对象即代表结果中了最高级别的外轮廓，而它自身的Contour数据始终为空==。被包含的最高级别的PolyNode还可能包含它自己的子对象（内孔），甚至自己的内孔还可以包括被嵌套的外轮廓等。但是外轮廓的子对象永远是孔，孔的子对象永远是外轮廓。
PolyTree可以包含开放路径。开放路径永远会在最高级别的子轮廓中存储。提供了两个函数可以快速的分离提取PolyTree开放路径和封闭轮廓——OpenPathsFromPolyTree和ClosedPathsFromPolyTree。
![](polytree.png)
```
polytree: 
    Contour = ()
    ChildCount = 1
    Childs[0]: 
        Contour = ((10,10),(100,10),(100,100),(10,100))
        IsHole = False
        ChildCount = 1
        Childs[0]: 
            Contour = ((20,20),(20,90),(90,90),(90,20))
            IsHole = True
            ChildCount = 2
            Childs[0]: 
                Contour = ((30,30),(50,30),(50,50),(30,50))
                IsHole = False
                ChildCount = 0
            Childs[1]: 
                Contour = ((60,60),(80,60),(80,80),(60,80))
                IsHole = False
                ChildCount = 0

```