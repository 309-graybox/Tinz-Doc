---
tags:
  - camera
  - mechanics
  - new
---
# Описание
___
Цель игровой механики - обеспечить корректную работу камеры от третьего лица, предотвращая прохождение камеры сквозь геометрию уровня и объекты окружения, сохраняя при этом читаемость сцены, стабильность управления и визуальный комфорт игрока.

параметры Camera Collision описаны [[Camera Collision (params)|тут]]. 
## Принцип работы
___
Камера всегда стремится занять **целевую позицию** относительно персонажа (Offset), но при обнаружении препятствий между персонажем и камерой **моментально** корректирует своё положение, приближаясь к персонажу или смещаясь вдоль поверхности коллизии. 

Ограничением являются объекты которые не попадают в маску коллизии камеры. 
пример игнорирования коллизии:
<iframe width="560" height="315" src="https://www.youtube.com/embed/_hbVDKHGG8s?si=tiyOCCtg9lwJn83O&amp;autoplay=1&amp;mute=1&amp;clip=UgkxM6DaR2uH6YubAmu0wKmQ-70qgrpRk0U-&amp;clipt=EMWiChi-1Qo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay =1 ; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen loop=1 volume = 0></iframe>

В случае если коллизия с препятствием перестала влиять на камеру задействуется механика [[Smooth Zoom After Collision]] 

# См. Также
___
- [[Camera Collision (params)]]
 