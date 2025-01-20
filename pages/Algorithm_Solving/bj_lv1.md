---
title: Baekjoon Lv.1
keywords: Algorithm, Baekjoon
summary: "Baekjoon의 브론즈 단계 문제를 풀었던 기록을 적는 곳. 풀이 과정과 사담만 남기고 문제 내용은 링크로 대체합니다."
sidebar: Algorithm_sidebar
permalink: bj_lv1.html
folder: Algorithm_Solving
---

---

## BaekJ Brz) 1271. 엄청난 부자2

[Top Page](#)  

#### 문제 링크

 [Baekjoon 1271](https://www.acmicpc.net/problem/1271)  

#### 풀이 언어

Python

#### 답안 코드

```python
T = list(map(int,input().split()))
Answer = list()
Answer.append(T[0]//T[1])
Answer.append(T[0]%T[1])

print(*Answer)
```

#### 풀이 과정에 대한 사담  
연산자 기초 활용 능력을 테스트 하는 문제인 것 같다.  
list를 사용하여 값을 저장하고 각 요구 출력 별로 각각 구한 뒤,  
append를 사용하여 추가하고,  
애스터리스크 리스트로 마무리.  

---
