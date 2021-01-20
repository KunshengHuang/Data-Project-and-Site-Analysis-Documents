基本原理描述：
- 选择所有的"等高线"（Curve）
- 根据Curve Length和所希望“分段的距离”，确定一根线段所需要分割的段数，使用“Integer”将数字规范化为整数
- 使用Divide Curve来分割这些等高线
- 之后使用电池“Cull Duplicates”，去除掉公差范围内重合的“Points（点）”
- 然后使用“Delaunay Mesh”来生成Mesh地形
