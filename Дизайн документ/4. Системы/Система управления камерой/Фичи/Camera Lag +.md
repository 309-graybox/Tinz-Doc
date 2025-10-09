---
tags:
  - camera
  - systems
  - animation
---
# Описание
___
**Camera Lag** — это система, при которой камера следует за целью (игроком) не жестко, а с небольшим упругим отставанием, имитируя движение объекта с массой на виртуальной пружине. Это создает более плавное, динамичное и визуально приятное движение, улучшающее восприятие скорости и инерции.

# См. Также
___
Пример реализации фичи в Unreal Engine:
- [Spring Arm](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-spring-arm-components?application_version=4.27)
- [Spring Arm API](https://dev.epicgames.com/documentation/en-us/unreal-engine/API/Runtime/Engine/GameFramework/USpringArmComponent?application_version=4.27)
- [Spring Arm Component](https://github.com/EpicGames/UnrealEngine/blob/release/Engine/Source/Runtime/Engine/Private/GameFramework/SpringArmComponent.cpp)

>[!info] Есть Нюанс!
> В Unreal нет отдельной реализации Camera Lag но эта фича встроена в Spring Arm Component.