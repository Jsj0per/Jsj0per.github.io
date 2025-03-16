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

## BaekJ sil) 10845. 큐

[Top Page](#)  

#### 문제 링크

[Baekjoon 10845](https://www.acmicpc.net/problem/10845)  

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

## BaekJ sil) 2606. 바이러스

[Top Page](#)  

#### 문제 링크

[Baekjoon 2606](https://www.acmicpc.net/problem/2606)  

[풀이 답안](http://boj.kr/fc84d67bcee147d1a0bf9c5814351760)

#### 풀이 언어

Python

#### 답안 코드

```python
def dfs(edge_graph_list, v, visited):
    visited[v] = True # 방문했으니 True로 바꿈
    for i in edge_graph_list[v]:
        if not visited[i]: # 해당 노드에 방문하지 않았다면...
            dfs(edge_graph_list, i, visited) # 그 노드를 기준으로 다시 dfs 실행(재귀)

node_num = int(input())

edge_num = int(input())

edge_graph_list = [[] for _ in range(node_num + 1)] # 그래프 초기화

for _ in range(edge_num): # 엣지 입력
    a, b = list(map(int, input().split()))
    edge_graph_list[a].append(b)
    edge_graph_list[b].append(a) # 양방향 연결

visited = [False] * (node_num + 1) # visit 노드의 수는 공백인 0을 제외시킬거라 총 길이 +1 을 한다.
infected_pc = 0 # 감염된 pc 수

dfs(edge_graph_list, 1, visited) # 1번 pc가 고정 감염 숙주이므로 여기서부터 시작.

for i in range(len(visited)):
    if visited[i] == True:
        infected_pc += 1 # 감염된 상태라면 변수에 +1

print(infected_pc - 1) # 1번 컴퓨터는 최초 숙주이므로 바이러스에 걸리게되는 컴퓨터 수에서 제외
```

#### 풀이 과정에 대한 사담

DFS 문제 익숙해지기 프로젝트.  
핵심은 1번 컴퓨터와 연결이 되어있는 컴퓨터'만' 감염시키게 되므로,  
독립된 네트워크의 변수가 True가 되지 않도록 코드를 짜는 것이 포인트로 보여진다.  
아직 DFS가 안 익숙한 상태이므로 좀 더 다른 문제를 풀어봐야 할 것 같다.

---

## BaekJ sil) 32979. 아파트

[Top Page](#)  

#### 문제 링크

[Baekjoon 32979](https://www.acmicpc.net/problem/32979)  

[풀이 답안](http://boj.kr/73d2b820b0a54862a108cb9526f1b7fc)

#### 풀이 언어

Python

#### 답안 코드

```python
from collections import deque

player = int(input())  # 플레이어 수
apartment_game = int(input())  # 아파트 게임 횟수
hand_position = list(map(int, input().split()))  # 손 위치
gyosun = list(map(int, input().split()))  # 사실상 이게 게임 횟수(교선이가 부른 수)

lose_people = []

game_start_position = deque(hand_position) # 게임 시작 직후 포지션
for i in gyosun: # 게임 시작
    for j in range(1, i): # 3이라 불렀으면 1, 2, 3 게임을 함
        game_start_position.append(game_start_position.popleft()) # 맨 아랫손을 꺼내서 맨 위로 둠
    lose_people.append(game_start_position[0]) # 3을 부를때 맨 아랫자리에 있는 사람이 패배 그래서 i+1이 아니다.

print(*lose_people) # 진 사람 언패킹해서 출력
```

#### 풀이 과정에 대한 사담

덱, 큐 문제 익숙해지기 프로젝트.  
진짜 엄청난 비문학 스타일 문제지만 간단히 말하면 손을 뺴고 더하는 과정을 거쳐서,  
마지막 손에 있는 사람이 패배하게 큐를 이용해서 짜라는 문제다.  
popleft와 append를 동시에 할 수 있게 코드를 짜면 풀리는 복잡한 지문에 비해 간단한 문제다.  

---

## BaekJ sil) 28278. 스택 2

[Top Page](#)  

#### 문제 링크

[Baekjoon 28278](https://www.acmicpc.net/problem/28278)  

[풀이 답안](http://boj.kr/29d89460e3ac456994d8d75a4a329d4b)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys

command_num = int(sys.stdin.readline()) # 명령 갯수

stack = [] # 스택
top = -1 # 스택의 가장 윗 값 인덱스

for cn_idx in range(1, command_num+1):
    command_input = list(sys.stdin.readline().split()) # 명령 입력

    if command_input[0] == '2': # 스택에 정수가 있다면 맨 위의 정수를 빼고 출력한다. 없다면 -1을 대신 출력한다.
        if top == -1:
            print(-1)
        else:
            print(stack.pop())
            top -= 1
    elif command_input[0] == '3': # 3: 스택에 들어있는 정수의 개수를 출력한다.
        print(len(stack))
    elif command_input[0] == '4': # 4: 스택이 비어있으면 1, 아니면 0을 출력한다.
        if top == -1:
            print(1)
        else:
            print(0)
    elif command_input[0] == '5': # 5: 스택에 정수가 있다면 맨 위의 정수를 출력한다. 없다면 -1을 대신 출력한다.
        if top == -1:
            print(-1)
        else:
            print(stack[len(stack)-1])
    else: #  X: 정수 X를 스택에 넣는다. (1 ≤ X ≤ 100,000)
        stack.append(command_input[1])
        top +=1

```

#### 풀이 과정에 대한 사담

스택 문제 익숙해지기 프로젝트.  
마찬가지로 sys.stdin.readline()을 쓰지 않는다면, 맞는 코드더라도 오류가 나는 문제다.  
스택의 push pop 등 명령어를 입력받으면 수행하게 하는 코드기 때문에, 그대로 만들어주면 된다.  

---

## BaekJ sil) 12789. 도키도키 간식드리미

[Top Page](#)  

#### 문제 링크

[Baekjoon 12789](https://www.acmicpc.net/problem/12789)  

[풀이 답안](http://boj.kr/bd608de6f444417491ddbcf6e56c27d1)

#### 풀이 언어

Python

#### 답안 코드

```python
from collections import deque
import sys

member_num = int(sys.stdin.readline()) # 전체 줄 서있는 사람 수

# 대기 줄 리스트, 대기줄에서는 맨 앞사람이 나가야하므로, deque를 활용해보기로 하였음.
mem_list = deque(map(int, sys.stdin.readline().split()))

enter_num = 1 # 다음에 들어갈 사람을 알려주는 index 번호

waiting_num = -1 # 대기 zone index 번호(top 역할)
waiting_list = [] # 대기 zone 구역 리스트

escape_code = 0 # 반복문 탈출용

while True:
    if waiting_list:  # waiting zone에 사람이 있다면
        escape_code += 1 # 여기 if문 지나감
        if waiting_list[waiting_num] == enter_num:  # 만약 제일 뒤에 있는 사람이 입장 번호랑 같다면...
            waiting_list.pop()  # 빼고 입장시키기
            waiting_num -= 1  # 대기 top -1
            enter_num += 1  # 다음 번호 호출
            escape_code = 0
            continue

    if mem_list: # 본래 줄에 사람이 있다면
        escape_code += 1 # 여기 if문 지나감
        if mem_list[0] == enter_num: # 줄에 맨 앞에 서있는 번호가 들어가야할 번호랑 같다면...
            mem_list.popleft() # mem_list에서 제거하고, entered_list에 추가
            enter_num += 1 # 다음 번호 호출
            escape_code = 0
            continue

        elif mem_list[0] != enter_num: # 줄에 맨 앞에 서있는 번호가 들어가야할 번호랑 다르다면
            waiting_list.append(mem_list.popleft())  # 아닐 시 waiting_list 추가
            waiting_num += 1  # 대기 top +1
            escape_code = 0
            continue

    if not mem_list and not waiting_list : # 전부 제대로 받았다면
        break

    if escape_code == member_num: # 전부 제대로 받을 수 없는 상태라면
        break

if enter_num - 1 == member_num: # 만약 전부 제대로 받았다면
    print('Nice')
else: # 만약 전부 제대로 받을 수 없는 상태라면, 만약 mem_list에 없는데도 waiting_list 만 있는 경우를 고려한 코드
    print('Sad')
```

#### 풀이 과정에 대한 사담

스택 문제 익숙해지기 프로젝트.  
생각보다 빡빡한 문제였는데, 너무 중첩 if문이나 중첩 for문을 남발하면 시간 제한에 정말 잘 걸리는 경우가 많았고,  
또한, 반례가 꽤 발생할 가능성이 높은 문제인 편이라,  
예) 4 2 1 3 (4 2 까지는 waiting zone에 잘 들어가지만 1이 통과하고나서 바로 waiting zone에 나갈 수 있는 수가 있는지 체크하는 반례)  
꽤 고생한 문제이고, 실제로 꽤 질문게시판을 들락날락 거렸다.  
그런 끝에 내가 생각한 코드의 스토리는 유지시키면서(즉, 내 코딩 스타일은 우직하게 지키면서) 나름 다이어트에 성공한 코드가 나왔다.  

내가 푼 방식의 핵심은 mem_list에서 pop된 경우라면 어디로 갔든 바로 continue 처리시켜서 오류를 일으킬 수 있는 다른 코드 조회를 즉시 차단시키고,  
무한 루프를 방지하기 위해 escape_code라는 별도의 변수를 사용하였다.
member_num을 조건으로 걸어둔 건 별다른 의미는 없고, 그냥 최대값 이전까지만 반복시키면 어지간하면 오류를 일으킬 염려가 없을 것같아,  
설정해뒀다.  

또한, 이 문제의 경우 정확하게 원하는 명령을 처리하는 것이 중요할 것 같아 되도록 반복문 내부에는 else를 쓰는 것을 지양했다.  


---

## BaekJ sil) 11866. 요세푸스 문제 0

[Top Page](#)  

#### 문제 링크

[Baekjoon 11866](https://www.acmicpc.net/problem/11866)  

[풀이 답안](http://boj.kr/5ee1d3f1f6ae497f8a47586f9bed2820)

#### 풀이 언어

Python

#### 답안 코드

```python
from collections import deque

people_len, delete_num = map(int, input().split()) # 전체 인원수, 삭제시킬 단위 숫자

josephus_que = deque() # 큐 선언

answer = [] # 빈 정답 리스트

for i in range(1, people_len + 1):
    josephus_que.append(str(i)) # 요세푸스 맵 제작

index = delete_num - 1 # 인덱스는 -1해야 정답.

while josephus_que: # 큐가 전부 없어질때 까지 반복
    for _ in range(index):
        josephus_que.append(josephus_que.popleft()) # pop 시킬 지점까지 원형 큐 형태 사용.
    answer.append(josephus_que.popleft()) # 삭제시킬 지점이 오면 answer로 pop시키기.

answer = ', '.join(answer) # 출력 형식을 맞추기 위한 언패킹

print(f'<{answer}>')
```

#### 풀이 과정에 대한 사담

큐 문제 익숙해지기 프로젝트.  
요세푸스 순열을 직접 구현해보는 문제인데, 원형 큐 원리를 이용하면 쉽다.  
원하는 지점이 나올때 까지 append(popleft)해주고,  
원하는 지점이 나왔다면 answer 리스트쪽으로 popleft 하는 방식으로 답이 나올때까지 뺑뻉이 돌려주면 문제가 풀려진다.  

---

## BaekJ sil) 1966. 프린트 큐

[Top Page](#)  

#### 문제 링크

[Baekjoon 1966](https://www.acmicpc.net/problem/1966)  

[풀이 답안](http://boj.kr/ba67c469124a429a9ee521a60a5a9fb3)

#### 풀이 언어

Python

#### 답안 코드

```python
from collections import deque

testcase = int(input())

for tc_idx in range(1, testcase + 1):
    total_page, target_page = map(int, input().split()) # 총 페이지 수와 목표 페이지 수를 받음
    print_list = deque(map(int, input().split())) # 프린트 대기 내역을 queue로 받음
    print_cnt = 0 # 지금까지 출력한 양을 기록할 변수

    while True: # 목표치에 닿을때까지 무한 반복
        if print_list[0] < max(print_list): # 만약 우선순위가 더 높은게 있다면
            print_list.append(print_list.popleft()) # 뒷 순서로 미룬다.
            if target_page == 0: # 만약 지금 페이지가 목표 페이지 였다면
                target_page += len(print_list) - 1 # 밀려난 만큼 인덱스도 재지정한다.
            else: # 아니라면
                target_page -= 1 # 앞으로 순서가 당겨졌을테니 1씩 감소시킨다.
        else: # 만약 우선순위가 더 높은게 없다면(즉, 출력해야한다면)
            if target_page == 0: # 만약 목표 페이지라면
                print_list.popleft() # 출력하고
                print_cnt += 1 # 프린트 수에 1 추가 후
                break # 반복문을 종료시킨다.
            print_list.popleft() # 아니라면, 출력하고
            target_page -= 1 # 순서가 당겨졌으니 1 마이너스 하고
            print_cnt += 1 # 프린트 수에 1 추가한다.

    print(print_cnt)

```

#### 풀이 과정에 대한 사담

큐 문제 익숙해지기 프로젝트.  ~~이쯤되면 사실 이미 익숙해져있다.~~  
프린트 순서를 뒤로 미루거나 당기는 변형이 있는 큐 문제다.  
따라서 목표 문서의 인덱스를 계속 변동 시켜줘야할 것을 요구하는 문제이고,  
그 부분을 해결 할 수 있다면 어려운 문제는 아니라고 생각된다.  

---

## BaekJ sil) 14248. 점프점프

[Top Page](#)  

#### 문제 링크

[Baekjoon 14248](https://www.acmicpc.net/problem/14248)  

[풀이 답안](http://boj.kr/b1247a7dabab4cda9ea9d248da2c9512)

#### 풀이 언어

Python

#### 답안 코드

```python
def solve(start):
    global cnt
    visited[start] = 1 # 현재 방문한 돌다리를 1로 바꾼다.
    if start + jump_len[start] < len(jump_len) and visited[start + jump_len[start]] != 1: # 오른쪽 돌로 가게 만드는 if문
        cnt += 1 # 방문 돌 갯수 추가
        solve(start + jump_len[start]) # 재귀로 다음 방문할 돌 찾기
    if start - jump_len[start] > -1 and visited[start - jump_len[start]] != 1: # 왼쪽 돌로 가게 만드는 if문
        cnt += 1 # 방문 돌 갯수 추가
        solve(start - jump_len[start]) # 재귀로 다음 방문할 돌 찾기
    return # 더 이상 갈 수 있는 돌이 없거나 방문할 돌이 없다면 return


stone_bridge = int(input()) # 돌다리 갯수
jump_len = list(map(int, input().split())) # 돌다리당 표시된 점프 거리
start = int(input()) - 1 # 시작지점. 인덱스로 쓰일거라 -1 처리

cnt = 1 # 방문한 돌 갯수. 무조건 시작점인 첫번째 돌다리는 건넌다.

visited = [0] * stone_bridge # 방문한 돌다리 확인용

solve(start) # def 호출

print(cnt)
```

#### 풀이 과정에 대한 사담

DFS, BFS 문제 익숙해지기 프로젝트.  
오늘은 평소쓰던 스택,큐를 활용한 DFS, BFS가 아닌 오늘 배운 재귀를 활용한 완전 탐색 방식을 이용하여 풀었다.  
시작점 돌은 무조건 포함되니 cnt는 1에서 시작한다.  
문제에서 주어진 예시는 3번째 돌에서 시작하니까, -1한 2가 첫 시작 인덱스가 될꺼고,  
거기서 좌 우로 2칸은 갈 수 있으니 3칸은 방문 완료.
그리고 나머지 2개의 돌도 방문할 수 있으니 5개가 나오게 된다.  

---

## BaekJ sil) 2563. 색종이

[Top Page](#)  

#### 문제 링크

[Baekjoon 2563](https://www.acmicpc.net/problem/2563)  

[풀이 답안](http://boj.kr/d4a325ec2a5a44cab31b785eb930efc5)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys

white_square = [[0] * 101 for _ in range(101)] # 백지장 제작, 101로 설정한 이유는 0인덱스 줄,칸은 안 쓸 예정이라서.
square_num = int(sys.stdin.readline()) # 사각형 갯수
cnt = 0 # 값 변수

for s_num in range(square_num): # 사각형 갯수만큼 반복
    x_start, y_start = map(int, sys.stdin.readline().split()) # X축, Y축 시작점 입력
    for i in range(y_start, y_start+10): # 사각형은 10칸씩 ( 세로 )
        for j in range(x_start, x_start+10): # 사각형은 10칸씩 ( 가로 )
            white_square[i][j] = 1 # 해당 칸은 1로 입력

for i in range(1, 101):
    for j in range(1, 101):
        if white_square[i][j] == 1: # 만약 해당 칸이 1이었다면,
            cnt += 1 # 색칠된 칸 수 1 추가

print(cnt)
```

#### 풀이 과정에 대한 사담

완전 탐색을 이용하는 문제.  
단순하게 시작 지점에서부터 가로세로 10칸씩 1로 채워넣고,  
다 채워넣었다면 완전탐색으로 전부 검색하게 하면 된다.  
100 x 100 칸으로 한정되어있어 완전탐색을 하더라도 시간 초과는 발생하지 않는다.

---

## BaekJ sil) 10451. 순열 사이클

[Top Page](#)  

#### 문제 링크

[Baekjoon 10451](https://www.acmicpc.net/problem/10451)  

[풀이 답안](http://boj.kr/91f5323569614477b8d1ab471b2cdd39)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys

def dfs(start):
    global cnt
    visited[start] = 1 # 도착한 곳에 1 추가.
    if visited[indexed_list[start]] == 1: # 만약 순환순열이 끝났다면 cnt를 1 추가하고 멈춘다.
        cnt += 1
        return
    else:
        dfs(indexed_list[start]) # 재귀하여 순열을 완성환다.


testcase = int(sys.stdin.readline())

for tc_idx in range(1, testcase + 1):
    num_len = int(sys.stdin.readline())
    num_list = list(map(int, sys.stdin.readline().split()))
    indexed_list = [x - 1 for x in num_list] # num_list에서 입력받은 값들을 전부 index 값에 맞게 변환시켜준다.
    visited = [0] * num_len # DFS를 위한 visited 정의

    cnt = 0  # 순환하는 순열의 갯수를 저장하는 변수.  즉, 이 문제의 답.

    for i in range(len(indexed_list)):
        if visited[i] == 0: # 1이면 그 변수는 시작지점이 아니므로 패스
            dfs(i) # dfs def 호출

    print(cnt)

```

#### 풀이 과정에 대한 사담

순열 문제를 나는 재귀 방식의 DFS 방식으로 풀기로 했다.  
주의할 점은 입력 예제로 1000 크기까지 주어지는데, 재귀를 활용할 경우 심심하면 히든 케이스로 런타임 에러를 일으킬 것이다.  
이를 피하기 위하여, 마지막 노드를 조회할 때는 다음 재귀로 넘어가지 않고 현재의 재귀 상태에서 조회가 가능하도록 짰다.  
실제로 이렇게 하니, 귀신같이 runtime Error를 피할 수 있었다.  
참고로 추가로 꼼수를 썼는데, 인덱스 값이랑 수열 입력값이 어긋나는게 보기 싫어서 아예 1씩 다 빼버렸다.  

---
