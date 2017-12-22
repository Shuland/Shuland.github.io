---
layout: post
title:  "[C]malloc"
date:   2017-12-19 08:43:59
author: Shuu
categories: C_language
---

# **malloc함수?** 
## 동적으로 메모리를 할당하는 함수(heap 영역에 메모리를 할당)
 
	#include<stdlib.h>
	
	void* malloc(size_t size) //malloc 함수의 원형
end

함수를 호출할 때 
할당하고자 하는 메모리의 크기를
 
바이트 단위로 전달하면 원하는 크기만큼 메모리를 할당하게 된다.

그리고 할당한 메모리의 주소(첫 번째 바이트의 주소)를 리턴한다.

메모리 할당에 실패하면 NULL이 리턴된다.

리턴형이 void인 이유는 단순 메모리 할당 함수이기 때문에 어떠한 데이터 형을 저장하는지 예측할 수 없기 때문이다.
개발자가 알맞은 용도로 변환하여 사용해야함.

![malloc](/img/malloc.png)

1. int는 4바이트이기 때문에 sizeof(int)는 4이다 힙영역에 4를 넣어준다.
2. 할당된 4바이트가 return되어서 int*형으로 변환하여
3. 포인터 변수 i에 대입

## **malloc 함수 ex)**

	#include <stdio.h> 
	#include <stdlib.h>
	
	int main() { 
		int arr_1[5];	// 배열 선언 
		int *arr_2;	// 포인터 변수 선언 
		int i; 
		
		for(i = 0; i < 5; i++) { 
			arr_1[i] = i+1;	// 배열에 값 대입 
		} 
	
			arr_2 = (int*) malloc(sizeof(int)*5);	// 메모리 할당, 배열의 크기만큼 할당하기 위해 5를 곱함 
	
		for(i = 0; i < 5; i++) { 
			arr_2[i] = arr_1[i]; 
			printf("%d ", arr_2[i]); 
			} 
			return 0; 
		}
end



[참고및출처](http://dsnight.tistory.com/51)






