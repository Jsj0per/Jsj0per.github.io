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

 [답안 링크](http://boj.kr/5f7d002cdc2e49edaf2343559dc12370)

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

알고리즘 스터디 그룹 1주차의 4일차 문제, 문제 선택자는 나.  

각 자릿수 별로 곱셈이 이루어지게 하고, 그걸 출력하면 끝인 간단한 알고리즘이다.  
다양한 방법이 있지만, 나는 가장 간단하게 str(문자열)의 성질을 활용하여 그걸 반복하게 하고,  
int로 형변환 시킨 상태로 한자리씩 구하는 방식으로 solving했다.  

---

## BaekJ Brz) 2480. 주사위 세개

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2480](https://www.acmicpc.net/problem/2480)  

 [답안 링크](http://boj.kr/6c6afd4d623f47e4b8455b2308efe956)

#### 풀이 언어

Python

#### 답안 코드

```python
data = list(map(int, input().split())) # 받아 적을 공간을 만든다.

if data[0] == data[1] and data[1] == data[2]: # 3개가 다 똑같을 경우 간단하다. 1?000점을 만들 식 1개만 만들면 된다.
    print(f'{10000+data[0]*1000}')
elif data[0] == data[1] or data[1] == data[2] or data[0] == data[2]: # 2개일 경우 각각의 경우의 수를 다 나열한다.
    if data[0] == data[1] and data[1] == data[2]:
        same_Value = data[1] # 1번 데이터를 키값으로 밸류에 저장
    elif data[1] == data[2] or data[0] == data[2]:
        same_Value = data[2] # 2번 데이터를 키값으로 밸류에 저장
    else:
        same_Value = data[0] # 0번 데이터를 키값으로 밸류에 저장
    print(1000+same_Value*100) # 그리고 키값으로 저장된 중복된 밸류를 집어넣어서 출력하면 된다.
else:
    print(f'{max(data)*100}') # 간단하다 가장 높은 수가 출력되게 max를 이용하면 끝!
```

#### 풀이 과정에 대한 사담

알고리즘 스터디 그룹 1주차의 1일차 문제, 문제 선택자는 J1학우님.  

3개 다 같은 숫자의 주사위이거나, 다 다른 주사위인 경우의 수를 출력하는 것은 매우 쉽다.  
문제는 2개만 같을 경우인데, 다양한 방법이 있을것으로 추측되나, 나는 다소 무식한 방법을 쓰기로 하였다.  
간단히 말하자면 모든 경우의 수를 if문을 사용하여 same_Value 값에 저장하고 그 값을 집어넣게 하면 된다.  

---

## BaekJ Brz) 25304. 영수증

[Top Page](#)  

#### 문제 링크

 [Baekjoon 25304](https://www.acmicpc.net/problem/25304)  

 [답안 링크](http://boj.kr/d8876504d11c4cfc98c56d9c5cde1733)

#### 풀이 언어

Python

#### 답안 코드

```python
total_Price = int(input()) # 총액 입력

total_Goods = int(input()) # 물건의 종류 수 입력

goods_list = [] # 굿즈 가격을 저장할 리스트 추가

for goods_Index in range(0, total_Goods): # 물건의 종류 수에 따라 반복 실행
    
    goods = list(map(int, input().split())) # 굿즈의 가격과 갯수를 입력받음
    goods_Total_Price = goods[0] * goods[1] # 가격 X 갯수 저장
    goods_list.append(goods_Total_Price) # 리스트에 추가

if total_Price == sum(goods_list): # 처음 입력한 총액이 리스트내 물건들의 총액과 같을시
    print('Yes') # 예스 예스 예스!
else:
    print('No') # 아님 말고.
```

#### 풀이 과정에 대한 사담

알고리즘 스터디 그룹의 2일차 문제, 문제 선택자는 J2학우님.  

주어진 조건이 꽤나 많지만, 실제로는 간단하다.  
그냥 영수증 내역을 입력시켜서 총액과 같은지 아닌지 구현시키는 알고리즘을 만드는 문제다.  
가장 성가실 수 있는 부분은 물건 가액과 갯수를 입력시키는 목록이 가변이라서 이를 구현해야 된다는 점인데,  
for문을 사용하여서 물건 종류 갯수에 따라 가변할 수 있도록 구현시키면, 이외에 어려운 점은 없어보인다.  

---

## BaekJ Brz) 5086. 배수와 약수

[Top Page](#)  

#### 문제 링크

 [Baekjoon 5086](https://www.acmicpc.net/problem/5086)  

 [답안 링크](http://boj.kr/76eace83d4d5406faab44d0b58891f19)

#### 풀이 언어

Python

#### 답안 코드

```python
while True: # 0 0 이 입력되어야 종료된다는 조건이 붙었으므로 While 문을 사용하여 무한 반복한다.
    nums = list(map(int, input().split())) # 2가지 숫자를 받아야 하므로 list, map을 사용

    if nums[1] > nums[0] and nums[1] % nums[0] == 0: # factor의 경우
        print("factor")
    elif nums[0] > nums[1] and nums[0] % nums[1] == 0: # multiple의의 경우
        print("multiple")
    elif nums[0] == 0 and nums[1] == 0: # 탈출코드
        break # while 조건문 관계없이 탈출함.
    else:
        print("neither") # 이외의 경우는 neither
```

#### 풀이 과정에 대한 사담

알고리즘 스터디 그룹의 3일차 문제, 문제 선택자는 P학우님.  

모르고 지나칠 뻔 했는데 조건문에 0 0 으로 끝내라는 조건이 있다.  
나도 이것때문에 첫번째 시도에서는 실패했는듯.  
그러므로 while문을 써서 무한 반복하게 만든다음, list-map 구조로 숫자를 받고,  
0 0이 나올때까지 무한반복하는 코드를 짰다.  

---

## BaekJ Brz) 2845. 파티가 끝나고 난 뒤

[Top Page](#)  

#### 문제 링크

 [Baekjoon 2845](https://www.acmicpc.net/problem/2845)  

 [답안 링크](http://boj.kr/c1ce6e56f7e447b48eb44f51f5945460)

#### 풀이 언어

Python

#### 답안 코드

```python
how_many_people = list(map(int, input().split())) # 상근이가 생각하고 있는 사람 수
mess_media = list(map(int, input().split())) # 신문 기사에 나온 사람 수

fact_check = [] # 참가자의 수가 몇 명 만큼 잘못 되었는지 검색

for fact_checker in mess_media: # 신문 마다 팩트 체크 개시
    if fact_checker == how_many_people[0] * how_many_people[1]: # 일치하면
        fact_check.append(0)
        # 0 출력. 사실 그냥 if-else 없이 fact_check.append(fact_checker - how_many_people[0] * how_many_people[1]) 만 해도 되긴할듯.
    else:
        fact_check.append(fact_checker - how_many_people[0] * how_many_people[1]) # 차이가 발생하면 차이만큼 입력

print(*fact_check) # 언패킹하면서 출력
```

#### 풀이 과정에 대한 사담

알고리즘 스터디 그룹의 5일차 문제, 문제 선택자는 G학우님.  

상근이가 생각하고있는 사람의 수와 신문 기사에 나온 사람의 수를 단순히 비교하여서 그 차이만큼 출력하면 그만인 간단한 문제.  

주의할 점은 'fact_checker - how_many_people[0] * how_many_people[1]' 를  
'how_many_people[0] * how_many_people[1] - fact_checker'로 잘못 입력시키는 일이 없도록 하는 정도?  

---
