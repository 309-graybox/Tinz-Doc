---
tags:
  - camera
  - animation
  - mechanics
---
# Описание
___
**Camera Lag** — это механика, при которой камера следует за целью (игроком) не жестко, а с небольшим упругим отставанием, имитируя движение объекта с массой на виртуальной пружине. Это создает более плавное, динамичное и визуально приятное движение, улучшающее восприятие скорости и инерции.

Параметры для механики описаны [[Camera Lag (params)|тут]].

Так выглядит Camera Lag в игре Elden Ring: Nightreign:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=jyrCtQ3-mro&controls=0"
frameborder="0" allowfullscreen></iframe>
А так выглядит Camera Lag в игре если включен [[Автоповорот Камеры]]:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=C2DjBjtWNcQ&controls=0"
frameborder="0" allowfullscreen></iframe>
А вот демонстрация Camera Rotation Lag в Unreal:
<iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&loop=1&playlist=ahPor5qXibE&controls=0"
frameborder="0" allowfullscreen></iframe>
# См. Также
___
Пример реализации механики в Unreal Engine:
- [Spring Arm](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-spring-arm-components?application_version=4.27)
- [Spring Arm API](https://dev.epicgames.com/documentation/en-us/unreal-engine/API/Runtime/Engine/GameFramework/USpringArmComponent?application_version=4.27)
- [Spring Arm Component](https://github.com/EpicGames/UnrealEngine/blob/release/Engine/Source/Runtime/Engine/Private/GameFramework/SpringArmComponent.cpp)

>[!info] Есть Нюанс!
> В Unreal нет отдельной реализации Camera Lag но эта механика встроена в Spring Arm Component.

Параметры:
- [[Camera Lag (params)]]