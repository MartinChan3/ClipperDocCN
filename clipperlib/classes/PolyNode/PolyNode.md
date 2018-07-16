### **PolyNode**

PolyNodes是被封装在PolyTree的容器中，同时提供了一个数据结构来代表由Excute()方法返回的多边形轮廓中的父子关系；

一个PolyNode对象代表一个多边形；它的“IsHole”属性表明它是一个**外轮廓**还是一个**内孔**。PolyNodes可能包含任意数量的PolyNode子对象，一般为外轮廓的子对象是内轮廓，而内轮廓的子对象是（嵌套的）外轮廓；