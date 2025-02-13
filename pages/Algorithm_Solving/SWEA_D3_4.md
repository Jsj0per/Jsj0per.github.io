---
title: SWEA_D3_4
keywords: [Algorithm, SWEA]
tags: [Algorithm, SWEA]
summary: "SW Expert Academy의 D3-4 문제를 풀었던 기록을 적는 곳. SWEA는 회원가입이 필수인 사이트이고, 문제에 대한 무단배포가 금지된 사이트라 풀이 과정과 사담만 남기고 문제 내용은 링크로 대체합니다."
sidebar: Algorithm_sidebar
permalink: SWEA_D3_4.html
folder: Algorithm_Solving
---

---

## SWEA D3) 22795. 일곱 부하의 평균

[Top Page](#)  

#### 문제 링크

 [SW Expert Academy 22795](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AZND_Dyq8SUDFAWB&categoryId=AZND_Dyq8SUDFAWB&categoryType=CODE&problemTitle=%EB%B6%80%ED%95%98&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)  

#### 풀이 언어

Python

#### 답안 코드

```python
import copy # 깊은 복사를 위한 임포트
 
test_case = int(input())
 
for tc_index in range(1, test_case+1):
    a,b,c,d,e,f = map(int, input().split())  # 6명의 부하 입력
    kobon_list = [a,b,c,d,e,f] # 리스트에 담기
    lost_kobon = max(kobon_list)+1 # 7번째 부하 설정
 
    while True:
        inside_kobon_list = copy.deepcopy(kobon_list)  # deepcopy를 해서 리스트를 복사
        inside_kobon_list.append(lost_kobon) # 7번째 맴버를 추가
 
        if sum(inside_kobon_list) % 7 == 0: # 6명보다 키가 크고, 나눴을 때 정수가 나온다면,
            print(lost_kobon) # 가장 먼저 입력되는 사람이 가장 최솟값일테니...
            break
        else:
            lost_kobon +=1 # 아닐 시 1추가하고 반복 지속
```

#### 풀이 과정에 대한 사담

겉보기엔 쉬워보이는데 진~~~~짜 고생해서 푼 문제.  
D3 문제 자체는 수업시간중에도 많이 풀어서 에이, 풀겠지 하면서 생각하고 풀려다가 무려 4시간 소모하여서, 다른 분들 답안을 보고 원리를 이해하고 나서야 풀 수 있었다.  
그렇다고 다른 분의 소중한 답안을 치팅하면 안 되니, 내가 안 되었던 부분을 개조하는 식으로 활용하였다.  
간단히 말하자면 7번쨰 부하를 설정할때, 1부터 차례차례 거슬러 올라가게 while문을 사용하면 되는 문제였다.  
사실 for문으로 풀어보고 싶었는데, 도저히 안 되어서 아예 조건을 걸지말고 while을 이용해서 무한반복하게 한 뒤,  
최초의 값이 나오면 즉시 break하고 값이 안 나오면 나올때까지 7번째 키를 1추가하는 방식으로 풀이를 하였다.  

---
