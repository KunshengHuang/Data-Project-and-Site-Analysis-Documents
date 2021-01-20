**思路分析：**

- 径流分析可以使用Bison插件来进行，[Food4Rhino链接——https://www.food4rhino.com/app/bison](https://www.food4rhino.com/app/bison)
- 该插件使用非常简单，个人没有过研究它的代码，不过它的原理可以进行简单的推测：
  - 设想Mesh上方有一个划分好的网格（Grid设定每个网格的长与宽，Boundary设定网格的外轮廓）
  - 从网格的交叉点垂直下落“水”（Curves）
  - “水”（Curves）碰到Mesh后，根据地形朝向确定水之后”流动“的方向，每次“流动”的长度即为Length
  - 设定进行计算的步骤（即为Steps）
- 上面的原理推测已经基本解释了参数的含义，特别需要注意的是参数设定时应该与模型单位相符，事先应该确定好模型的单位是“毫米”还是“米”
