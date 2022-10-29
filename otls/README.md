
### Edge Group to Curve
  Давно хотел сделать замену "неспешному" лабсовскому Edge Group To Curve.
1. В моей версии убран лишний, как мне кажется, функционал (странный трансфер атрибутов, который можно сделать обычным ray sop'ом).
2. Добавлена галка "Make Isolated Loops Closed".
3. Производительность (на данной тестовой сцене) примерно в 5.5 раз выше.

#### Совместимость:
  Проверено в Houdini 18.0 - 19.0, теоретически начиная с 16.0.
  
#### Зависимости:
  PolyPath
  
#### Файлы:
  - nord__edgegroup_to_curve__0_05_004.hda      - ассет
  - nord__edgegroup_to_curve__0_05_002_TEST_.hip - пример (Houdini 19.0, в иных версиях возможны варнинги)

#### Update to 0.05.002
1. Removed unnecessary primitives creation, thanks to Pedohorse (ХАРКОННЕН)
2. Added "Join Connected Segments Together" toggle, so you can leave the segments unjoined

#### Update to 0.05.004
1. Added toggle "Sort Points by Vertex Order", because it's usually mess in point numbers
2. Added Descriptive Parm for Group string, truncated if it is too long

### Curve to Edge Group
HDA для обратной задачи, получения эдж группы на основе кривой. При этом, кривая может не содержать никаких групп, она интерпретируется как одна эдж-группа. Имя группы задаётся произвольно, либо выбирается из меню со списком групп, существующих на меше. Возможно, в дальнейшем, добавлю группы на самой кривой.
- Особенно может понадобиться после сабдива, который, как известно, херит эдж группы

#### Файлы:
- nord__curve_to_edgegroup__1_01_001_TEST_.hda - ассет
- nord__curve_to_edgegroup__1_01_001_TEST_.hip - пример
- nord__curve_to_edgegroup__1_01_001_TEST_.png - картинка

### Remove Degenerate Poly
Определяет и удаляет вырожденные полигоны на основе отношения площади к квадрату четверть-периметра.
- The "quality" of a polygon here refers to the ratio of its area to the square of a quarter-perimeter. For example, the "quality" of a circle > 1, a square is 1, a rectangle < 1. The thinner the polygon, the lower its "quality". A fully degenerate polygon has a "quality" of zero

#### Файлы:
- nord__removedegenerate__1_01_001.hda - ассет
- nord__removedegenerate__1_01_001.hip - пример (Houdini 19.0.657, в иных версиях возможны варнинги)

### Size/Step Grid
Like an original Grid, but with explicitly specified Grid size and Step size parameters

#### Файлы:
- nord__sizestepgrid__1_01_001.hda - ассет

### Omni Extrude
Two-way PolyExtrude, such it's extrudes in positive and negative direction simultaneously

#### Файлы:
- nord__omniextrude__1_02_002.hda - ассет

