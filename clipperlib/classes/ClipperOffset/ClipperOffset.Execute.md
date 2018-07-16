### **ClipperOffset.Execute**

```
Del.» procedure Execute(out solution: TPaths; Delta: Double); overload;

C++ » void Execute(Paths& solution, double delta);

C#  » public void Execute(ref Paths solution, double delta);


Del.» procedure Execute(out PolyTree: TPolyTree; Delta: Double); overload;

C++ » void Execute(PolyTree& polytree, double delta);

C#  » public void Execute(ref PolyTree polytree, double delta);
```

该方法有两个参数，第一个是接受结果的结构（可以是PolyTree或者Paths中的一种）。第二个参数是指偏移量的大小——**负值会缩水，正值会发生膨胀**；
该方法可以被调用多次，来实现对相同路径实现不同程度的偏置；
![](http://www.angusj.com/delphi/clipper/documentation/Images/offset1.png)
```
#include "clipper.hpp"  
...
using namespace ClipperLib;
 
int main()
{
  Path subj;
  Paths solution;
  subj << 
    IntPoint(348,257) << IntPoint(364,148) << IntPoint(362,148) << 
    IntPoint(326,241) << IntPoint(295,219) << IntPoint(258,88) << 
    IntPoint(440,129) << IntPoint(370,196) << IntPoint(372,275);
  ClipperOffset co;
  co.AddPath(subj, jtRound, etClosedPolygon);
  co.Execute(solution, -7.0);
   
  //draw solution ...
  DrawPolygons(solution, 0x4000FF00, 0xFF009900);
}
```

![](offset1.png)

