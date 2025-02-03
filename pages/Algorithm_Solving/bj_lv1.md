---
title: Baekjoon Lv.1
keywords: Algorithm, Baekjoon
tags: Algorithm, Baekjoon
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

## BaekJ Brz) 2338. 긴자리 계산

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2338](https://www.acmicpc.net/problem/2338)  

#### 풀이 언어

Python

#### 답안 코드

```python
A = int(input())
B = int(input())

print(A+B)
print(A-B)
print(A*B)
```

#### 풀이 과정에 대한 사담

그냥 + - * 쓸 줄 아냐를 묻는 정말 기초적인 문제.  

---

## BaekJ Brz) 2420. 사파리 월드

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2420](https://www.acmicpc.net/problem/2420)  

#### 풀이 언어

Python

#### 답안 코드

```python
N, M = map(int,input().split())
print(abs(N-M))
```

#### 풀이 과정에 대한 사담

절대값 명령어(abs)를 몰라서 검색 찬스를 좀 썼다.  
그리고 M, N을 동시에 한 줄에 쓸 수 있다는 것을 처음 알았다(이 또한 검색 찬스)  
이 참에 기억해둬야겠다.  

---

## BaekJ Brz) 2338. 긴자리 계산

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2338](https://www.acmicpc.net/problem/2338)  

#### 풀이 언어

Python

#### 답안 코드

```python
A = int(input())
B = int(input())

print(A+B)
print(A-B)
print(A*B)
```

#### 풀이 과정에 대한 사담

그냥 + - * 쓸 줄 아냐를 묻는 정말 기초적인 문제.  

---

## BaekJ Brz) 2588. 곱셈

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2588](https://www.acmicpc.net/problem/2588)  

#### 풀이 언어

Python

#### 답안 코드

```python
num_01 = str(input()) # 1번 입력
num_02 = str(input()) # 2번 입력

for num_Index in range (len(num_02)-1, -1, -1): # 각 자리별로 계산하게 반복함
    print(f'{int(num_01)*int(num_02[num_Index])}') # 자릿수별 곱셈 구하기
print(f'{int(num_01)*int(num_02)}') # 진짜배기 곱셈 구하기
```

#### 풀이 과정에 대한 사담

알고리즘 스터디 그룹 1주차의 1일차 문제, 출제자는 나.  

각 자릿수 별로 곱셈이 이루어지게 하고, 그걸 출력하면 끝인 간단한 알고리즘이다.  
다양한 방법이 있지만, 나는 가장 간단하게 str(문자열)의 성질을 활용하여 그걸 반복하게 하고,  
int로 형변환 시킨 상태로 한자리씩 구하는 방식으로 solving했다.  

---




https://www.notion.so/_2-18eb1e39fe5f801988fdea215b9be70f
