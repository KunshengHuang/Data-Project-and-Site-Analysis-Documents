**思路描述：**
- 在grasshopper里，mesh并不是由面组成的，而是由 “点，点与点之间的关系” 组成的，所以给Mesh上色时并不是在给面上色，而是在给点上色，这一点请特别注意
- 先选取要进行高度分析的Mesh
- 通过电池“Deconstruct Mesh”来获得Mesh的一系列点“Vertices”
- 在通过电池“Deconstruct”来获得一系列点的对应Z坐标
- 通过Sort List和List Item来获得这些Z坐标的最大值和最小值
- 通过将最大值、最小值和这些Z坐标输入到电池“Gradient”来获得一系列颜色
- 最后通过电池“Mesh Colors”来获得根据高度上色的Mesh模型

![image style="zoom:3%;" /](https://github.com/KunshengHuang/Data-Project-and-Site-Analysis-Documents/blob/main/Grasshopper%20Files/Mesh%20Site%20Altitude%20Analysis/Altitude%20Map_03.jpg)
![image](https://github.com/KunshengHuang/Data-Project-and-Site-Analysis-Documents/blob/main/Grasshopper%20Files/Mesh%20Site%20Altitude%20Analysis/Screenshot.png)
