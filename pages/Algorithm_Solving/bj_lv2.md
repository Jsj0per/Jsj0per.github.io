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

## BaekJ sil) 1260. DFS와 BFS

[Top Page](#)  

#### 문제 링크

[Baekjoon 1260](https://www.acmicpc.net/problem/1260)  

[풀이 답안](http://boj.kr/be6078503d3342b49398fed337a14f0a)

#### 풀이 언어

Python

#### 답안 코드

```python
from collections import deque


def dfs(start_dfs):
    dfs_result.append(start_dfs) # 현재 노드 리스트에 추가
    visited_dfs[start_dfs] = 1 # 방문한 노드의 visited 주소를 1로 변경
    for i in node_map_list[start_dfs]: # node_map_list에서 다음 노드로 갈 좌표를 찾기
        if visited_dfs[i] == 0: # 만약 해당 노드가 방문한 적 없는 노드라면
            dfs(i) # 재귀한다.


def bfs(start_bfs):
    bfs_deque = deque() # 빈 덱 생성
    bfs_deque.append(start_bfs) # 현재 위치를 덱에 추가
    visited_bfs[start_bfs] = 1 # 방문한 노드의 visited 주소를 1로 변경
    while bfs_deque: # 덱이 계속 존재하는 한 반복됨
        current = bfs_deque.popleft() # 현 위치를 popleft해서 받음
        bfs_result.append(current) # 그리고 현 노드를 리스트에 추가
        for i in node_map_list[current]: # node_map_list에서 다음 노드로 갈 좌표를 찾기
            if visited_bfs[i] == 0: # 만약 방문한 적 없는 노드라면
                visited_bfs[i] = 1 # 해당 노드를 방문처리하고
                bfs_deque.append(i) # deque에 append한다.


node_num, edge_num, start_node = map(int, input().split())

node_map_list = [[] for _ in range(node_num + 1)]  # 빈 리스트를 만든다. +1을 한 이유는 0번째 칸을 쓰지않음으로서 인덱스와 일치시키기 위함

for _ in range(edge_num):
    start, end = map(int, input().split())  # 시작지점 종료지점을 각각 입력
    node_map_list[start].append(end)
    node_map_list[end].append(start)  # 양방향 에지 설정

for i in range(node_num + 1):
    node_map_list[i].sort()  # 내림 차순으로 정렬

visited_dfs = [0] * (node_num + 1) # dfs의 방문 리스트를 만든다
dfs_result = [] # 출력 저장용으로 빈 리스트 제작
dfs(start_node) # def 호출

print(*dfs_result) # 형변환 한 후 출력

visited_bfs = [0] * (node_num + 1) # bfs의 방문 리스트를 만든다.
bfs_result = [] # 출력 저장용으로 빈 리스트를 제작
bfs(start_node) # def 호출

print(*bfs_result) # 형변환 후 출력

```

#### 풀이 과정에 대한 사담

일부로 정석에 가까운 방식으로 풀어보려고 노력하였다.  
나도 아직은 이 방식에 익숙하지 않은데다 최근에 다른 알고리즘을 공부하고 있어서 완전히 내 실력으로 푼 문제는 아니라는 점이 아쉬운 점.   
그래도 직후 코드리딩을 해보니 구조 자체는 리마인드 되었기때문에 큰 문제는 아니다.  
dfs는 아는 방식인 재귀형식으로 풀었다.  
bfs의 경우 간만에 풀다보니 좀 헷갈렸는데, while 반복문 형식을 이용하여,  
연결된 노드들을 전부 순회하며 deque에 추가한 뒤, 다시 deque에서 차례차례 확인하여 다음 노드를 찾는 방식을 하였다.  

---

## BaekJ sil) 1012. 유기농 배추

[Top Page](#)  

#### 문제 링크

[Baekjoon 1012](https://www.acmicpc.net/problem/1012)  

[풀이 답안](http://boj.kr/d19e93cd7e414e6bb7c68ca910eddb3d)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys
sys.setrecursionlimit(10**6) # 재귀 허용 용량을 늘린다.

def delta_worm(start_x, start_y): # 지렁이가 투입될 장소 주변에 양배추가 추가로 더 있는지 확인하기 위한 def
    visited[start_y][start_x] = 1 # 일단 그 장소에 양배추가 심어져 있으니 방문했다 치고,

    delta_x = [1, -1, 0, 0]
    delta_y = [0, 0, 1, -1] # 델타 탐색을 위한 좌표 0 - 오른쪽, 1 - 왼쪽, 2 - 위쪽, 3 - 아래쪽

    for dir in range(4): # 네 방향 확인
        if start_x + delta_x[dir] >= 0 and start_x + delta_x[dir] < len_x and start_y + delta_y[dir] >= 0 and start_y + delta_y[dir] < len_y: # 리스트를 벗어나지 마렴.
            new_x = start_x + delta_x[dir] # 탐색할 x 좌표
            new_y = start_y + delta_y[dir] # 탐색할 y 좌표
            if cab_map[new_y][new_x] == 1 and visited[new_y][new_x] == 0: # 만약 해당 좌표에 양배추가 있고 방문한 적이 없다면,
                delta_worm(new_x, new_y) # 그 좌표를 중심점을 바꾸고 재귀한다.

testcase = int(sys.stdin.readline()) # 테스트 케이스 입력

for _ in range(1, testcase + 1): # 이 문제는 테스트 케이스를 따로 출력할 필요가 없으므로 _ 로 지정한다.
    len_x, len_y, cab_num = map(int, sys.stdin.readline().split()) # 배추밭의 가로갈이, 배추밭의 세로길이, 양배추 갯수
    cab_map = [[0] * len_x for _ in range(len_y)] # 양배추 지도
    visited = [[0] * len_x for _ in range(len_y)] # 방문 여부 지도

    for i in range(cab_num): # 양배추를 심어보자
        cab_x, cab_y = map(int, sys.stdin.readline().split()) # 양배추의 좌표를 입력
        cab_map[cab_y][cab_x] = 1 # 그 좌표에 양배추 심기(1 넣기)

    cnt = 0 # 필요한 지렁이의 갯수를 저장할 변수

    for y in range(len_y):
        for x in range(len_x):
            if visited[y][x] == 0 and cab_map[y][x] == 1: # 만약 방문한 적이 없고 양배추가 심어져 있다면
                delta_worm(x, y) # def 호출
                cnt += 1 # 지렁이 필요 갯수 1 추가

    print(cnt) # 결과 출력
```

#### 풀이 과정에 대한 사담

배추가 심어진 곳에 인접한 배추가 있다면 그 배추는 하나의 지렁이로 커버가 가능하다.  
그걸 구현하면 되는데, 델타 탐색 방식을 접목시켜서 한번의 def로 주변 배추까지 다 방문처리를 시키고 cnt를 1 추가하는 방식으로 대응했다.  
참고로 재귀 DFS 방식으로 푼 문제라 recursionlimit을 1000개 이상으로 조회 가능하게 해금해놨다.  
왜냐하면 저렇게 해금해놓더라도 일정량 코드에서 가지치기를 해두었기 때문에 과도한 조회를 안 하도록 짠 코드기 때문.  

---

## BaekJ sil) 16953. A → B

[Top Page](#)  

#### 문제 링크

[Baekjoon 16953](https://www.acmicpc.net/problem/16953)  

[풀이 답안](http://boj.kr/fb9133a991604ba1956de386dbecaa47)

#### 풀이 언어

Python

#### 답안 코드

```python
import sys

def solve(current_num):
    global cnt, min_cnt

    if current_num > end: # 만약 재귀를 통하여 값이 end 값보다 높아지면 안 되므로 높아지는 즉시 return처리한다.
        return

    if current_num == end: # 만약 원하는 값이 되었을 떄
        if cnt < min_cnt: # min_cnt값이 현 cnt값보다 높은경우
            min_cnt = cnt # 그 값으로 교체한 후 return한다.
            return

    cnt += 1 # 재귀를 한번 시킬때마다 1씩 더하고
    one_add = int(str(current_num)+str(1)) # 오른쪽에 1을 계속 붙이는 경우 str로 형변환 시켜서 진행하면 편하다.
    solve(one_add) # 이 재귀는 끝자리에 1을 더한 경우의 재귀
    cnt -= 1 # return 되었다면 cnt를 다시 -1 한다. 잘못된 재귀를 취소처리하였으니.

    cnt += 1 # 다시 1을 더하고
    solve(current_num*2) # 2를 곱한 값으로 재귀한다.
    cnt -= 1 # 그래도 없으면 위와 같은 이유로 cnt를 -1한다.


start, end = map(int, sys.stdin.readline().split()) # 시작값과 끝값을 받는다.

cnt = 1 # A를 B로 바꾸는데 필요한 연산의 최솟값에 1을 더한 값을 출력한다...라는데 그냥 1부터 시작하면 된다.

min_cnt = 0xfffff # 셀수없는 최댓값을 무작위로 작성하였다.

solve(start) # 재귀 def 시작

if min_cnt == 0xfffff : # 만약 min_cnt 값이 변하지 않았다면,
    print(-1) # 그건 구할 수 없는 값이었으므로 -1로 출력한다.
else: # 그리고 답이 구해졌다면,
    print(min_cnt) # 그 min_cnt의 값을 출력한다.
```

#### 풀이 과정에 대한 사담

재귀의 구조를 이해한다면 푸는데 큰 어려움이 없는 문제다.  
문제 구조상 시간초과가 날 일도 없는 문제이기에, 마음놓고 재귀를 신나게 굴렸다.  
먼저 조건중에 오른쪽에 1을 붙이는 것(즉 자릿수가 1자리씩 계속 늘어나는 것)과 곱하기 2를 계속 시키는 것 중,  
가장먼저 end에 가까워지는 것은 전자이다.  
그래서 재귀시 전자의 경우의 수를 먼저 재귀시키고, end의 값보다 커지는 경우에 return 시키도록 하고,  
후자를 재귀시키는 구조로 하면 된다.  

---

## BaekJ sil) 20920. 영단어 암기는 괴로워

[Top Page](#)  

#### 문제 링크

[Baekjoon 20920](https://www.acmicpc.net/problem/20920)  

[풀이 답안](http://boj.kr/0dba68c36e5b4729897fe0d8eb2b95ff)

#### 풀이 언어

Pypy3 (Python 인터프리터)

#### 답안 코드

```python
import sys

input_num, min_len = map(int, sys.stdin.readline().split())

word_dict = {}

final_list = [] # 마지막 값을 저장하는 리스트

for i in range(input_num):
    input_word = input()
    if len(input_word) < min_len: # 만약 이 단어가 최소 요건 길이보다 짧다면
        pass # 무시
    elif input_word in word_dict: # 만약 dict안에 해당 값이 있다면
        word_dict[input_word] += 1 # value를 +1 한다.
    else: # 없다면
        word_dict[input_word] = 1 # 해당 key를 추가한다.

# 람다식을 이용해 정렬한다. 람다식에서 '-' 를 붙히면 내림차순으로 정렬된다.
sorted_list = sorted(word_dict.items(), key=lambda words: (-words[1], -len(words[0]), words[0]))

for i in sorted_list:
    print(i[0])
```

#### 풀이 과정에 대한 사담

진짜 안 풀려서 스터디 동기들에게 힌트를 좀 얻어서 푼 문제.  
일단은 이 역시 푸는 방법이 더 있는지 아닌지 모르겠지만, 람다를 이용해서 3가지 조건을 걸고 풀었다.  
해석을 하자면 sorted(1회성 리턴값을 뱉는 sort) word_dict items(키 밸류값 모두 조회), key값을 문제에서 제시한 순서대로 걸어서,  
차례대로 재정렬하게 시켰다.  

---
