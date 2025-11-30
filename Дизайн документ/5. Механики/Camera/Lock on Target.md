---
tags:
  - camera
  - mechanics
  - target
aliases:
  - таргет
---
# Описание
___
Механика фиксирует камеру и ориентацию персонажа на выбранной цели, чтобы обеспечить точный контроль и читаемую композицию в бою.  
Камера при этом удерживает **и персонажа, и цель** в кадре, динамически подстраиваясь под их движение и окружение.

- При удерживании [[Target (input)|кнопки таргета]] система ищет ближайшую цель вокруг персонажа в заданном **радиусе действия**.

- После захвата, камера ориентируется так, чтобы **персонаж игрока и цель** оставались видимыми:

- При активном таргете камера **ограничивает вертикальное вращение (Pitch)**, но **разрешает свободное вращение по горизонтали (Yaw)** вокруг точки между персонажем и целью.

- Игрок может переключаться между целями [[Switch Target (input)|клавишей переключения]], если в пределах радиуса есть другие враги.

- При отпускании кнопки таргета режим деактивируется, а камера возвращается в обычный режим —  
  **либо через заданное время**, если от игрока не поступают инпуты,  
  **либо сразу**, если игрок вводит любое действие.

Параметры описаны [[Lock on Target (params)|тут]].

Так выглядит Lock on Target: 
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=JhZBLYfoqOA&controls=0"
frameborder="0" allowfullscreen></iframe>
Так он работает в движении:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=o5fnY8zjg_0&controls=0"
frameborder="0" allowfullscreen></iframe>
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=DQ0Q6D2_kN8&controls=0"
frameborder="0" allowfullscreen></iframe>
Поведение камеры после снятия лока на цели, если игрок начал двигаться:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=P5FbH70Lxpo&controls=0"
frameborder="0" allowfullscreen></iframe>
Поведение камеры после снятия лока на цели, если игрок стоит без действия:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=-Rb6VATej0w&controls=0"
frameborder="0" allowfullscreen></iframe>
## Особенности поведения
---

- **Плавное выравнивание камеры:**  
  Камера не мгновенно переключается на новую цель, а делает интерполяцию, чтобы избежать рывков и сохранить плавность движения.

- **Слежение за позицией:**  
  Камера вычисляет точку обзора на основе средней позиции между персонажем и целью, с дополнительными оффсетами для сохранения читаемости кадра.

- **Ограничение углов:**  
  Вертикальное вращение (Pitch) ограничено, чтобы сохранять боевой ракурс. Горизонтальное вращение (Yaw) доступно для полного оборота вокруг оси между персонажем и целью.

- **Динамическая дистанция:**  
  При сближении игрока и цели камера увеличивает FOV и немного отдаляется; при удалении — приближает, удерживая их обоих в кадре.

- **Коллизии:**  
  При столкновении камеры с геометрией сцены дистанция временно сокращается, а после выхода из препятствия плавно восстанавливается.

## Lock без цели
___

Если игрок входит в режим Lock On, когда целей нет, или если предыдущая цель пропадает (например, погибает), и рядом нет других, камера переходит в состояние **Lock без цели**:

- камера фокусируется на персонаже,

- персонаж сохраняет своё направление взгляда, зафиксированное в момент перехода в режим Lock без цели.

Если во время активного режима Lock On в пределах радиуса обнаружения появляется новая цель, камера автоматически переключается на неё, устанавливая новый фокус слежения.

Так выглядит лок без цели:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=GahLjBslHvg&controls=0"
frameborder="0" allowfullscreen></iframe>
Поведение камеры если во время Lock on traget цель пропала:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=AB4XGn2a-gc&controls=0"
frameborder="0" allowfullscreen></iframe>
Поведение камеры если во время лока без цели появится новая цель:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=cAix4zD6Km8&controls=0"
frameborder="0" allowfullscreen></iframe>

# См. Также
---

- [[Lock On Target Parameters +]]