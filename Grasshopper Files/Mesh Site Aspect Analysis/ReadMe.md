**思路分析：**

- 在grasshopper里，mesh并不是由面组成的，而是由 “点、点与点之间的关系” 组成的，所以给Mesh上色时并不是在给面上色，而是在给点上色，这一点请特别注意
- 先选取要进行“朝向/坡向分析”的Mesh
- 通过电池”Deconstruct Mesh“来获得一系列”点Vertices“的法向量Normal
- 通过电池”Projection“，将这些法向量投影到XY Plane上
- 计算这些投影后的向量和Unit Y(可以理解为北向向量)的夹角α，这些夹角α的取值为0~360°
- 通过Sort List和List Item来获得这些夹角α的最大值和最小值
- 通过将最大值、最小值和这些夹角α输入到电池“Gradient”来获得一系列颜色，这些颜色代表了α的大小，也即朝向
- 将这一系列颜色和Mesh输入到电池”Mesh Colors“后，获得分析上色后的Mesh模型
- Bake出Mesh模型到Rhino中的对应图层

<div align=center><img src="https://github.com/KunshengHuang/Data-Project-and-Site-Analysis-Documents/blob/main/Grasshopper%20Files/Mesh%20Site%20Aspect%20Analysis/Aspect%20Map_04.jpg" width="700" height="500"/></div>

<div align=center><img src="https://github.com/KunshengHuang/Data-Project-and-Site-Analysis-Documents/blob/main/Grasshopper%20Files/Mesh%20Site%20Aspect%20Analysis/Aspect%20Analysis%20Screenshot.jpg" width="700" height="500"/></div>
