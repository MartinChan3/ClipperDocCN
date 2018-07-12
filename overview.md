# 简介

Clipper Library（以下简称为Clipper库或者ClipperLib或Clipper）提供了对线段和多边形的裁剪(clipping)以及偏置(offseting)功能。
和其他裁剪库相比，Clipper具有以下特征：
> - 它能够接受各类多边形输入，包含自交的多边形；
> - 它支持多种填充原则(奇偶填充、非零填充、正填充、负填充)；
> - 它相较于其他库来说效率极高；
> - 它数值稳定（鲁棒性强）；
> - 它支持多边形和线段的偏置；
> - 它对于商用以及免费软件来说都是免费使用的。

**当前版本:**6.2.0

**作者及版权:**Angus Johnson. Copyright © 2010-2014
License, terms and conditions: Boost Software License

**术语：**
- 裁剪(Clipping):通常是指在二维平面上把一个图形在指定的矩形框以外的部分去除掉。在更广义的角度，指定的裁剪范围不一定要是一个矩形，可以是各种各样的多边形，甚至是多个多边形；同样的，我们一般裁剪指的是形态学上的“求交”，但是在Clipper库中裁剪可以实现4种布尔运算（求交、求和、求异、求异或）；
- 路径(Path):是指一些列有序的点的集合，用来定义一个轮廓(contour)，这个轮廓既可以是代指一条线/开放路径(line/open path)，也可以代指一个多边形/闭合轮廓(polygon/closed path)。
- 线(Line):与Polyline同义，代指一个具有两个以上点的开放路径。
- 轮廓(Contour):与路径同义；
- 孔洞/内轮廓(Hole):代指一个多边形内部表示该部分不属于该多边形的闭合区域；一个“内轮廓(Hole Polygon)”就是一个代指孔的外围点集的封闭路径；
- 孔洞/内轮廓(Hole):代指一个多边形内部表示该部分不属于该多边形的闭合区域；一个“内轮廓(Hole Polygon)”就是一个代指孔的外围点集的封闭路径；
- 多边形填充规则(Polygon Filling Rule):即在一系列的闭合路径中，来定义哪些属于“内部”，哪些属于“外部”

**下载链接：**
[SourceForge](https://sourceforge.net/projects/polyclipping/)

**参考内容：**

