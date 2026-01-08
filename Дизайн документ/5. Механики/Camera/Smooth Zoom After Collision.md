---
tags:
  - camera
  - systems
---
# Описание
___
Механика обеспечивает **плавное восстановление расстояния камеры до персонажа** после того, как камера сократила дистанцию из-за столкновения с объектами сцены.  
Позволяет избежать резких скачков и дёрганий камеры, создавая комфортное и предсказуемое движение камеры в играх от третьего лица.

Параметры описаны [[Smooth Zoom After Collision (params)|тут]].

Демо:
<iframe width="560" height="315" src="https://www.youtube.com/embed/_hbVDKHGG8s?si=7bM-ikpW4LafuR5V&amp;clip=UgkxSTkWh541ooQeaJVljwjnudKM5WQ1wsbr&amp;controls=0&amp;autoplay=1&amp;mute=1&amp;clipt=EOVXGOGmAQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen loop=1 Volume = 0></iframe>
## Принцип работы
---

- При движении камеры сцена проверяется на столкновения с объектами.

- Если камера сталкивается с мешами или коллайдерами, дистанция до персонажа временно уменьшается, чтобы избежать прохождения сквозь геометрию.

- После того как препятствие исчезает, система плавно возвращает камеру к исходной дистанции с использованием интерполяции и демпинга.

- Восстановление расстояния может быть адаптивным: быстрее при малых сокращениях и мягче при больших.

## Использование
---

- Включается для всех third-person камер, где возможны столкновения с объектами окружения.

- Настраивается отдельно для разных типов коллизий (стены, деревья, декор).

- Может работать вместе с другими системами камеры (Camera Lag, World Space Masking) без конфликтов.
# См. Также
---
- [[Smooth Zoom After Collision (params)]]