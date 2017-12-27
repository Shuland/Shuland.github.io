---
layout: post
title:  "[TETRA]TETRA modulation (pi/4 DQPSK)"
date:   2017-12-19 08:43:59
author: Shuu
categories: RF
---
# TETRA MODULATION 

TETRA는 변조방식으로 pi/4-차등 4위상 편이 변조(pi/4 DQPSK)를 사용한다  
차등(Differential)은 정보가 절대적인 상태로 운반되지 않는다   
또한 몇몇 경우에 천이에 제한이 있다. 반송파 궤도가 원점을 통과하지 않는   
pi/4 DQPSK에서 발생한다. DQPSK 전송시스템은 어떤 심볼 위치에서  
다른심볼 위치로 천이할 수 있다. 

pi/4 DQPSK의 변조 형식은 45도(pi/4 라디안) 만큼의 두개의   
QPSK constellation offset을 사용한다  
천이는 한 constellation에서 다른 constellation으로 일어나야 한다. 이것은  
각각의 심볼에서의 위상에서 항상 변화가 있다는 것을 말한다  
(클럭 복구를 더 쉽게 하는) 데이터는 constellation상에서 위상 편이의  
크기와 방향에서 부호화되는 것이지, 절대 위치에서 부호화되는 것은 아니다  

**pi/4 DQPSK의 한가지 이점**
 
1. 신호궤도가 원점을 통과하지 않는다는 것이다.
2. 송신기 설계를 단순하게 한다.
3. root raised cosine filtering(상승코사인필터 TETRA표준에 있다.)를 갖는 pi/4 DQPSK는 
GMSK, 다른 일반적인 셀룰러 변조 형식보다 스펙트럼 효율이 좋다.

[참고및출처](http://ebook.pldworld.com/_eBook/%EB%94%94%EC%A7%80%ED%84%B8%EB%B3%80%EC%A1%B0.pdf)



