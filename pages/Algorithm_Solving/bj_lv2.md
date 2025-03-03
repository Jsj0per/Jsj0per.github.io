---
title: Baekjoon Lv.2
keywords: [Algorithm, Baekjoon]
tags: [Algorithm, Baekjoon]
summary: "Baekjoon의 실버 단계 문제를 풀었던 기록을 적는 곳. 풀이 과정과 사담만 남기고 문제 내용은 링크로 대체합니다."
sidebar: Algorithm_sidebar
permalink: bj_lv2.html
folder: Algorithm_Solving
---

---

## BaekJ sil) 4949. 균형잡힌 세상

[Top Page](#)  

#### 문제 링크

[Baekjoon 4949](https://www.acmicpc.net/problem/4949)  

[풀이 답안](http://boj.kr/ba60966d23654f98a23d18cf01fcc96e)

#### 풀이 언어

Python

#### 답안 코드

```python
def push(bracket):
    global top
    if top < 100:
        top += 1
        stack[top] = bracket # def 밖에서 괄호를 가려 받게 했으므로 push에 따로 조건걸 필요 X

def small_pop():
    global top
    global nope
    if top == -1:
        nope = True
        return

    if stack[top] == '(':
        top -= 1 # 여는 괄호와 일치하면 균형하므로 top -1
    else:
        nope = True # 아님 불균형

def big_pop():
    global top
    global nope
    if top == -1:
        nope = True
        return

    if stack[top] == '[':
        top -= 1 # 여는 괄호와 일치하면 균형하므로 top -1
    else:
        nope = True # 아님 불균형

while True:
    word_line = input() # 한줄씩 입력
    stack = [0] * 101 # 100칸을 넘는 경우가 없다고 했으므로...
    top = -1
    nope = False

    if word_line == '.':
        break  # . 이 나오면 break.

    for i in word_line:
        if i == '(' or i == '[':
            push(i) # 새로운 여는 괄호면 스택에 추가
        elif i == ')':
            small_pop() # 소괄호 판독기
        elif i == ']':
            big_pop() # 대괄호 판독기

    if top != -1:
        nope = True # top이 남아있으면 불균형함

    if nope == True:
        print('no') # 불균형하면 no 출력
        nope = False
    else:
        print('yes') # 균형이면 yes 출력
        nope = False
```

#### 풀이 과정에 대한 사담

난 정말 스택, 큐를 싫어하는 사람이다. 유독 이 알고리즘은 코드가 눈에 들어오지 않는다.  
하지만 싫어하는 것과 별개로 이걸 피하면 프로그래머로서 실격이니까 앞으로 좋아할 수 있도록 노력해보겠다.  
이 문제는 스택을 이용해서 푸는 문제로 여는 괄호를 스택에 집어넣고 닫는 괄호가 나오면 들어있는 스택의 정보랑 비교해서 팝을 할지 불균형한 문제인지 판단하게 하였다.  
참고로 착지점을 잘못 해석해서 계속 7문제만 풀도록 조건을 거는바람에 한참동안 틀렸습니다 파티를 벌였다.  
진짜 싫다...  

---

## BaekJ sil) 9012. 괄호

[Top Page](#)  

#### 문제 링크

[Baekjoon 9012](https://www.acmicpc.net/problem/9012)  

[풀이 답안](http://boj.kr/0de942a27c67468c9793487219e7c7a0)

#### 풀이 언어

Python

#### 답안 코드

```python
def stack_machine(par_text):

    global answer, top

    if par_text == '(': # 만약 여는 괄호라면
        stack.append(par_text) # 스택에 추가
        top += 1 # 스택의 제일 높은 위치 갱신
        return answer
    elif par_text == ')': # 만약 닫는 괄호라면
        if top < 0: # 스택이 비어있는데 추가할려하면 불균형 하므로 No 리턴
            answer = 'NO'
            return answer
        else: # 스택이 있다면
            stack.pop() # 꺼내고
            top -= 1 # 제일 높은 위치 갱신
            return answer

testcase = int(input())

for _ in range(testcase):
    par_input = input()

    stack = [] # 초기 설정: stack
    top = -1  # 초기 설정: top
    answer = 'YES' # 초기 설정: answer

    for i in par_input:
        answer = stack_machine(i) # 답 입력 받음, def 호출
        if answer == 'NO': # 이미 NO로 판단되었다면 break.
            break

    if top != -1: # 스택이 남아있다면 불균형하므로 NO
        answer = 'NO'

    print(answer)
```

#### 풀이 과정에 대한 사담

스택 문제 익숙해지기 프로젝트.  
간단한 괄호를 활용한 스택 사용 문제이다.  
여는 괄호가 소괄호만 있기 때문에 어렵지는 않다.  
이 문제를 업그레이드 한 문제가 바로 위 문제.  

---

## BaekJ sil) 10828. 스택

[Top Page](#)  

#### 문제 링크

[Baekjoon 10828](https://www.acmicpc.net/problem/10828)  

[풀이 답안](http://boj.kr/b6953638fdef4b4f9032344ea53910b8)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys

testcase = int(sys.stdin.readline())

stack = []
for _ in range(testcase):
    input_commend = sys.stdin.readline().split()

    if input_commend[0] == 'pop':
        if len(stack) < 1:
            print('-1')  # 없으면 -1
        else:
            print(stack.pop())  # 있으면 그 값을 pop 하고 top -1
    elif input_commend[0] == 'size':
        print(len(stack))  # 현재 사이즈는 top+1(top은 현재 스택 제일 윗값의 인덱스(주소값)이므로 항상 1이 적다. 따라서 1 더하면 지금 현재 저장값이다)
    elif input_commend[0] == 'empty':
        if len(stack) == 0:
            print('1')  # 비어있으면 1
        else:
            print('0')  # 뭔가 있으면 0
    elif input_commend[0] == 'top':
        if len(stack) < 1:
            print('-1')  # 없으면 -1
        else:
            print(stack[len(stack)-1])  # 스택의 탑값을 인덱스로 불러와서 출력
    else:
        stack.append(input_commend[1])  # push 하고 top +1
```

#### 풀이 과정에 대한 사담

스택 문제 익숙해지기 프로젝트, 이제 스택은 꽤 익숙해졌으니 다른 걸로 나아가도 될 듯 하다.  
이 문젠 골 떄리게도 sys를 안 쓰면 무조건 틀린다.  
그거 이외에는 요구하는 방식대로 코드를 작성해서 풀면 된다.  

---

## BaekJ sil) 10828. 스택

[Top Page](#)  

#### 문제 링크

[Baekjoon 10828](https://www.acmicpc.net/problem/10828)  

[풀이 답안](http://boj.kr/b6953638fdef4b4f9032344ea53910b8)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys
from collections import deque

testcase = int(sys.stdin.readline())

que_list = deque([])

for _ in range(testcase):
    commend_input = sys.stdin.readline().split()

    if commend_input[0] == 'pop':
        if len(que_list) < 1: # 만약 큐에 들어있는 정수가 없는 경우에는 -1을 출력한다.
            print('-1')
        else: # 큐에서 가장 앞에 있는 정수를 빼고, 그 수를 출력한다.
            print(que_list.popleft())
    elif commend_input[0] == 'size': # 큐에 들어있는 정수의 개수를 출력한다.
        print(len(que_list))
    elif commend_input[0] == 'empty':
        if len(que_list) < 1:
            print('1') # 큐가 비어있으면 1
        else:
            print('0') # 아니면 0을 출력한다.
    elif commend_input[0] == 'front': # 큐의 가장 앞에 있는 정수를 출력한다.
        if len(que_list) < 1: # 만약 큐에 들어있는 정수가 없는 경우에는 -1을 출력한다.
            print('-1')
        else:
            print(que_list[0])
    elif commend_input[0] == 'back': # 큐의 가장 뒤에 있는 정수를 출력한다
        if len(que_list) < 1: # 만약 큐에 들어있는 정수가 없는 경우에는 -1을 출력한다.
            print('-1')
        else:
            print(que_list[len(que_list)-1])
    else:
        que_list.append(commend_input[1]) # 정수 X를 큐에 넣는 연산이다.
```

#### 풀이 과정에 대한 사담

큐 문제 익숙해지기 프로젝트.  
스택이 익숙해지니 자동적으로 큐도 이해해버렸다.  
내가 이걸 이해못하서 2주간 마음고생 심했던거 생각하니 너무 허무하게 풀리고 이해해버려서 좀 싱숭생숭하다.  
큐 문제는 deque라는 좋은 함수가 있기 때문에 이를 이용해서 풀면 된다.  

---
