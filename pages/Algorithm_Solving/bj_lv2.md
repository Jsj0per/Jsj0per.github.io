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

## BaekJ sil) 9012. 균형잡힌 세상

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
