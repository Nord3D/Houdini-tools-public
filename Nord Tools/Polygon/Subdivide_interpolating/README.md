# Subdivide Interpolating
![](https://github.com/Nord3D/Houdini-tools-public/blob/main/Nord%20Tools/Polygon/Subdivide_interpolating/2024-11-22_17-09-13.png)

Subdivide дополненный простейшим итеративным солвером, компенсирующим сдвиг сглаженной поверхности относительно контрольных вершин базовой поверхности

Обычная subdivide поверхность, подобно NURBS, в общем случае не проходит через вершины контрольной сетки, что создаёт эффект "замыливания". 
Интерполирующая поверхность проходит через все контрольные вершины, плотно прилегая к базовой сетке, сохраняет объём, не "замыливает" детали
