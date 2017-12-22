---
layout:  post
title:  pthread in visualstudio/windows
subtitle:   pthread
categories:  Language
date:   2017-12-21 10:17 +0900
tags:  c
---

# visualstudio/windows 에서 pthread 사용하기 

## pthread를 visualstudio/windows 에서 사용하려 하였지만 되지않았다.

pthread.h를 찾아서 다운받아서 빌드하였다. 

1. 다운받은 디렉토리내의 dll 파일들을 C:\windows\System32 디렉토리에 모두 복사한다.
  **하지만 pthreadVC2.dll 오류가 나서 C:\Program Files (x86)\Microsoft Visual Studio 10.0\VC\bin 이곳에 dll 파일을 넣어주었다.**

2. 비주얼 스튜디오를 연다.

3. 프로젝트 -> 속성 -> VC++ 디렉터리를 연다.

4. 포함디렉터리에 include 디렉터리의 경로를 입력한다.

5. 라이브러리 디렉터리에 lib 디렉터리의 경로를 입력한다.

6. 프로젝트 -> 속성 -> 링커 -> 입력 -> 추가 종속성에 lib 파일들의 파일명을 모두 입력해 준다.

7. 프로젝트 -> 속성 -> C/C++ -> 일반 -> 추가 포함 디렉터리에 include과 lib의 경로를 모두 입력해 준다.



