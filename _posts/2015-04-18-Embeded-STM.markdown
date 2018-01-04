---
layout: post
title:  "[STM]STM32F103x RESET 관련"
date:   2018-01-04 16:43:59
author: Shuu
categories: Embeded
---

# STM32F103x Reset 

- STM 칩 내부에 슈미트 트리거가 있어서 판단이 힘든 전압을 판단하여 
HIGH, LOW를 판단해 Reset을 걸어준다.
- NRST(RESET핀) 어떤 Reset을 걸던지 NRST핀에 걸리게 되어있다. 내부에 풀업저항이 달려있다.  
그래서 평상 시에 HIGH상태를 유지하다가 내부 스위치에 의해 GND로 떨어지면 
LOW 상태로 변하면서 Reset이 걸린다.
- 외부에서 NRST Pin을 제어할 경우 push-pull 특성으로 구성하지 말아야한다. push-pull로 구성하게 되면 내부에 스위치가 GND에 물려있기 때문에 쇼트가 날 수 있다.  
(그내부 스위치를 통해서 WWDG reset, IWDG reset, Power reset, Software reset, Low-power management reset)등의 기능이 사용된다.
- 

