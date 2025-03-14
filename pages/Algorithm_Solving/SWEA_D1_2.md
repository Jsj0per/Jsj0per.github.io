---
title: SWEA_D1~D2
keywords: [Algorithm, SWEA]
tags: [Algorithm, SWEA]
summary: "SW Expert Academy의 D1,D2 문제를 풀었던 기록을 적는 곳. SWEA는 회원가입이 필수인 사이트이고, 문제에 대한 무단배포가 금지된 사이트라 풀이 과정과 사담만 남기고 문제 내용은 링크로 대체합니다."
sidebar: Algorithm_sidebar
permalink: SWEA_D1_2.html
folder: Algorithm_Solving
---

---

## SWEA D1) 1936. 1:1 가위바위보

[Top Page](#)  

#### 문제 링크

 [SW Expert Academy 1936](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PjKXKALcDFAUq&categoryId=AV5PjKXKALcDFAUq&categoryType=CODE&problemTitle=1936&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)  

#### 풀이 언어

Java  

#### 답안 코드

```java
import java.util.Scanner;

class Solution
{
    public static void main(String args[]) throws Exception
    {
        Scanner jkb = new Scanner(System.in);
        int peopleA = jkb.nextInt(), peopleB = jkb.nextInt();

        if(peopleA == 1 && peopleB == 3)
        {
            System.out.println("A");
        }else if(peopleA == 1 && peopleB == 2)
        {
            System.out.println("B");
        }else if(peopleA == 2 && peopleB == 1)
        {
            System.out.println("A");
        }else if(peopleA == 2 && peopleB == 3)
        {
            System.out.println("B");
        }else if(peopleA == 3 && peopleB == 1)
        {
            System.out.println("B");
        }else if(peopleA == 3 && peopleB == 2)
        {
            System.out.println("A");
        }else if(peopleA == peopleB)
        {
            System.err.println("비길 수 없습니다");
        }else{
            System.err.println("잘못 된 입력입니다.");
        }
    }
}
```

#### 풀이 과정에 대한 사담

SSAFY 입과 전에 푼 알고리즘 문제.  

이때는 파이썬 언어를 몰랐기 때문에 그나마 알고있던 언어인 Java로 풀었다.  

풀이 방식에는 여러가지 있긴한데, 나는 다소 무식한 방식으로 일일이 결과값을 대응하는 방식으로 풀었다.  

결과 출력값 자체가 한정되어있고 많지않은 가위바위보가 예시니까 가능한 풀이방식.  

---

## SWEA D1) 2058. 자릿수 더하기

[Top Page](#)  

#### 문제 링크

[SW Expert Academy 2058](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QPRjqA10DFAUq&categoryId=AV5QPRjqA10DFAUq&categoryType=CODE&problemTitle=2058&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)  

#### 풀이 언어

Java  

#### 답안 코드

```java
import java.util.Scanner;

class Solution
{
    public static void main(String args[]) throws Exception
    {
         Scanner naturalNum = new Scanner(System.in);
        int saveNaNum = naturalNum.nextInt();
        if(saveNaNum<=9999 && saveNaNum>=1)
        {
            int num1000 = saveNaNum / 1000;
            num1000 %= 1000;

            int num100 = saveNaNum / 100;
            num100 %= 10;

            int num10 = saveNaNum / 10;
            num10 %= 10;

            int num1 = saveNaNum;
            num1 %= 10;

            System.out.println(num1000+num100+num10+num1);
        }else{
            System.err.println("잘못된 입력입니다.");
        }
    }
}
```

#### 풀이 과정에 대한 사담

마잔가지로 SSAFY 입과 전에 푼 문제라 JAVA로 풀었다.  

전체적으로 연산자에 대한 기초를 얼마나 기억하고 있느냐를 평가하는 문제 같았다.  

나는 모든 자릿수를 그 자릿수에 맞게 나눈 뒤, 대입연산자 '%='를 활용하는 방식으로 풀었다.  

### 다른 답안 코드

#### 풀이 언어

Python  

#### 답안 코드

```Python
T = int(input())

thousand = int(T // 1000)
hundred_before = int(T // 100)
hundred = int(hundred_before % 10)
ten_before = int(T // 10)
ten = int(ten_before % 10)
one = int(T % 10)
print(thousand+hundred+ten+one)
```

#### 풀이 과정에 대한 사담

위에 내가 구했던 Java 코드를 Python으로 바꾼 것.  

---

## SWEA D1) 2063. 중간값 찾기

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2063](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QPsXKA2UDFAUq&categoryId=AV5QPsXKA2UDFAUq&categoryType=CODE&problemTitle=2063&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Java

#### 답안 코드

```java
import java.util.*;

class Solution
{
    public static void main(String[] args) throws Exception
    {
        Scanner inputNum = new Scanner(System.in);
        int scaleNum = inputNum.nextInt();
        int[] numberBako = new int[scaleNum];
        if(scaleNum<=199 && scaleNum>=9 && scaleNum % 2 == 1)
        {
            for(int i = 0; i<scaleNum; i++)
            {
                numberBako[i] = inputNum.nextInt();
            }
            Arrays.sort(numberBako);
            System.out.println(numberBako[scaleNum/2]);
        }
    }
}
```

#### 풀이 과정에 대한 사담

마잔가지로 SSAFY 입과 전에 푼 문제라 JAVA로 풀었다.  

내가 자바를 공부할 때 배열과 리스트를 얼마나 대충 배웠는지 반성하게 만든 문제.

이 쉬운 문제를 2번이나 틀리고 맞췄다.

배열(array)를 활용하여서(어짜피 입력된 값은 변할 일이 없는 문제니까. 물론 리스트를 써도 되는 것 같아 보였다.), 문제를 풀고 sort 하는 방식으로 정렬한 뒤, 깔끔하게 나누기 2 하였다.

---

## SWEA D1) 2025. N줄 덧셈

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2025](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QFZtaAscDFAUq&categoryId=AV5QFZtaAscDFAUq&categoryType=CODE&problemTitle=2025&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Java

#### 답안 코드

```java
import java.util.Scanner;

class Solution
{
    public static void main(String args[]) throws Exception
    {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt(); 

        int solveNum = T * (T + 1) / 2;

        System.out.println(solveNum);
    }
}
```

#### 풀이 과정에 대한 사담

SSAFY 입과는 하였으나, 파이썬을 배우기 전에 푼 문제.

순간 멍했는데 ~~나는 고딩때 수포자였다~~, 등차수열의 합을 구하는 공식을 코딩으로 짜라는 문제다.

그대로 만들면 끝이다.

---

## SWEA D1) 2068. 최대수 구하기

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2068](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QQhbqA4QDFAUq&categoryId=AV5QQhbqA4QDFAUq&categoryType=CODE&problemTitle=2068&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())
 
for test_case in range(1, T + 1):
    data = list(map(int,input().split()))
    print(f'#{test_case} {max(data)}')
```

#### 풀이 과정에 대한 사담

입과 후 Python으로 가장 먼저 푼 문제.

이 문제도 배열과 리스트를 쓸 수 있는지 푸는 문제.

파이썬의 경우 배열과 리스트를 쓰는 경우 디폴트는 string으로 되기 때문에 map을 써서 내용물을 int로 바꿔주는 처리과정을 거쳐야하는 것 같다.

그 이후에 그대로 만들면 끝이다.

### 다른 답안 코드

```python
T = int(input())

for test_case in range(1, T + 1):
    data = sorted(list(map(int,input().split())))
    print(f'#{test_case} {data[9]}')
```

#### 풀이 과정에 대한 사담

Max를 안 쓰는 경우 Sort를 하여서 구하여한다.  

근데 내가 Java랑 착각한게, 파이썬에서 sort는 **리턴값을 안 뱉는다는 점**을 강사님께 물어봐서야 알았다는 점은 함정.  

이럴 경우에는 sorted를 써야한다는 것 같다.  

굳이 sort를 쓰고싶다면...  

```python
T = int(input())

for test_case in range(1, T + 1):
    data = list(map(int,input().split()))
    data.sort()
    print(f'#{test_case} {data[9]}')
```

이렇게 써야하는 것 같다.  

이거 백퍼 나중에 프로젝트나 포트폴리오 할 때 실수 할 것 같으니까 조심해야겠다.  

---

## SWEA D1) 1545. 거꾸로 출력해 보아요

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1545](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV2gbY0qAAQBBAS0&categoryId=AV2gbY0qAAQBBAS0&categoryType=CODE&problemTitle=1545&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())

numbako = list()
for test_case in reversed(range(0, T + 1)):
    numbako.append(test_case)
numbako.sort(reverse=True)
print(*numbako)
```

#### 풀이 과정에 대한 사담

정렬 기능을 기억하고 있는지 물어보는 문제.  

거꾸로 출력이기 때문에 역순 정렬이 필요하고, for과 append를 써서 자동적으로 값을 집어넣게 하면 된다.  

---

## SWEA D1) 1933. 간단한 N의 약수

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1933](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PhcWaAKIDFAUq&categoryId=AV5PhcWaAKIDFAUq&categoryType=CODE&problemTitle=1933&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())

for test_case in range(1, T + 1):
    data = list(map(int, input().split()))
    print(f'#{test_case} {int(round(sum(data)/10))}')
```

#### 풀이 과정에 대한 사담

파이썬에서는 자바의 printf를 저렇게 표현하는구나를 알게됐다는 점에서 이상하게 핀트가 어긋난 깨닳음을 얻은 것은 나만 그런건가...

---

## SWEA D1) 2071. 평균값 구하기

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2071](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QRnJqA5cDFAUq&categoryId=AV5QRnJqA5cDFAUq&categoryType=CODE&problemTitle=2071&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())

Divisor = list()

for test_case in range(1, T + 1):
    if T % test_case == 0:
        Divisor.append(test_case)
Divisor.sort()

result = map(int,Divisor)

print(*Divisor)
```

#### 풀이 과정에 대한 사담

리스트의 내용을 출력할 때 괄호를 제외하고 출력하고 싶다면 애스터리스크(*)를 붙일 것.  

---

## SWEA D1) 2047. 신문 헤드라인

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2047](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QKsLaAy0DFAUq&categoryId=AV5QKsLaAy0DFAUq&categoryType=CODE&problemTitle=2047&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = input()
result = T.upper()

print(result)
```

#### 풀이 과정에 대한 사담

대문자, 소문자 변환(upper, lower) 활용이 가능한지 묻는 문제.  
그렇기 때문에 코드 자체는 더없이 간단하고 깔끔하게 구현 가능하다.  

---

## SWEA D1) 2072. 홀수만 구하기

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2072](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5QSEhaA5sDFAUq&categoryId=AV5QSEhaA5sDFAUq&categoryType=CODE&problemTitle=2072&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())

for test_case in range(1, T + 1):
    mappingNum = map(int, input().split())
    numBako = list(mappingNum)
    finalSum=0
    for odd_finder in numBako:
        if odd_finder % 2 !=0:
             finalSum += odd_finder
    print(f'#{test_case} {finalSum}')
```

#### 풀이 과정에 대한 사담

이 문제는 풀이 과정에서 명령어 숙지 미숙으로 인하여 다른 분들의 코드를 많이 참조하였다.  
리스트 내 특정 값만 계산하는 행동 자체는 겉보기엔 간단해 보이던데 생각보다 코드로 구성시키려하니 와닿지 않았다.  
반드시 나중에 다시 한번 풀어봐야겠다.  

---

## SWEA D1) 2070. 큰 놈, 작은 놈, 같은 놈

[Top Page](#)

#### 문제 링크

[SW Expert Academy 2070](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QQ6qqA40DFAUq&categoryId=AV5QQ6qqA40DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
T = int(input())

for test_case in range(1, T + 1):
    two_num = list(map(int, input().split()))
    bigger = '?'
    if two_num[0] > two_num[1]:
        bigger = '>'
    elif two_num[0] < two_num[1]:
        bigger = '<'
    elif two_num[0] == two_num[1]:
        bigger = '='
    print(f'#{test_case} {bigger}')
```

#### 풀이 과정에 대한 사담

이 문제는 비교 연산자를 잘 쓸 수 있는가를 확인하는 문제로 보여짐.
고로 비교연산자 활용을 적절한 위치에 적절하게 하면된다.

---

## SWEA D1) 9367. 점점 커지는 당근의 개수

[Top Page](#)

#### 문제 링크

[SW Expert Academy 9367](https://swexpertacademy.com/main/code/userProblem/userProblemDetail.do?contestProbId=AW_nY2m6OLADFARY&categoryId=AW_nY2m6OLADFARY&categoryType=CODE)

#### 풀이 언어

Python

#### 답안 코드

```python
test_case = int(input())
for tc_index in range(1,test_case+1):
    carrot_len = int(input()) # 당근 갯수 입력
    carrot_list = list(map(int,input().split())) # 당근 리스트 입력

    before_carrot = carrot_list[0] # 비교군이 될 0번 당근 값 먼저 저장
    max_counting = 1 # 최대 연속 증가값 저장
    counting = 1 # 연속 증가값 저장

    for c_idx in range(1, carrot_len): # 0번 당근은 비교군으로 빼뒀으니 1번부터 확인
        if max_counting < counting:  # 현 최대값과 비교하여 값이 더 크면
            max_counting = counting  # 갱신한다.
        if carrot_list[c_idx] > before_carrot: # 만약 커진다면
            counting += 1 # 카운팅한다.
        else: # 연속하지 않는다면
            counting = 1 # 그리고 초기화한다.
        before_carrot = carrot_list[c_idx] # 비교군을 교체한다.

    if max_counting < counting:  # 종료전 마지막 갱신, 현 최대값과 비교하여 값이 더 크면
        max_counting = counting  # 갱신한다.
    print(f'#{tc_index} {max_counting}')
```

#### 풀이 과정에 대한 사담

헷갈리면 안 되는 부분이 연속으로 증가하는 값이지, 1씩 증가하는 값을 구하는 문제가 아니다.  
이걸 깨닫는데 무려 30분이 걸렸다.  
나는 멍충하다.  

---

## SWEA D2) 1926. 간단한 369문제

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1926](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PTeo6AHUDFAUq&categoryId=AV5PTeo6AHUDFAUq&categoryType=CODE&problemTitle=1926&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=&pageSize=10&pageIndex=1)

#### 풀이 언어

Python

#### 답안 코드

```python
num = int(input()) # 반복할 숫자 입력

num_list = [] # 출력할 숫자를 담을 리스트

for i in range(1, num+1): # 하이픈을 입력시키기 위한 반복문
    hypen_num = 0 # 하이픈 수 판별기
    if i // 100 in (3,6,9): # 100의 자리 숫자 판별
        hypen_num += 1
    if (i % 100) // 10 in (3,6,9): # 10의 숫자를 판별
        hypen_num += 1
    if (i % 10) in (3,6,9): # 1의 숫자를 판별
        hypen_num += 1
    if hypen_num >= 1: # 확인된 숫자만큼 하이픈을 여러개 출력
        num_list.append('-' * hypen_num)
    else: # 이외에는 원래 숫자 입력
        num_list.append(str(i))

print(*num_list) # 언패킹으로 출력
```

#### 풀이 과정에 대한 사담
앞서 푼 자릿수 더하기 문제의 한단계 업그레이드 판.  
이지만 여전히 어렵지는 않은 문제다.  
각 자리 수를 3, 6, 9인지 확인하게만 하고 그걸 하이픈으로 치환시키면 된다.  
치환시키는 방식은 hypen_num 변수가 1,2,3의 경우에 맞게 각각 정의해줘도 되고(왜냐하면 최대값이 1000으로 고정되어 있어 많이 나와봐야 3이기 때문),  
string 곱하기를 이용해도 된다.  

---

## SWEA D2) 1979. 어디에 단어가 들어갈 수 있을까

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1979](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PuPq6AaQDFAUq)

#### 풀이 언어

Python

#### 답안 코드

```python
def blk_word_finder(puzzle_map, map_len):
    global blk_word_list # 전역 변수 선언으로 편집
    for verti_idx in range(len(puzzle_map)): # 가로 구하기
        len_finder = 0
        for horiz_idx in range(len(puzzle_map[verti_idx])): # 하나하나 선형검색하여 구하는 방식을 채택.
            if puzzle_map[verti_idx][horiz_idx] == 1: # 1이 등장하면 칸수 판별기에 1씩 추가
                len_finder += 1
                if horiz_idx+1 == map_len: # 끝칸이면
                    if len_finder > 1: # len_finder가 1 이상일 시
                        blk_word_list.append(len_finder) # 리스트 추가 
                        len_finder = 0
            elif puzzle_map[verti_idx][horiz_idx] == 0: # 값이 0일시
                if len_finder > 1: # len_finder가 1 이상일 시
                    blk_word_list.append(len_finder) # 리스트 추가
                    len_finder = 0
                else: # 그게 아니면 그냥 초기화
                    len_finder = 0
 
    verti_map = list(zip(*puzzle_map)) # 놀랍게도 이 코드를 쓰면 세로줄이랑 가로줄이 뒤바뀐답니다. 대신 내부 코드는 튜플로 처리되니 주의.
    for verti_idx in range(len(verti_map)): # 세로 구하기
        len_finder = 0
        for horiz_idx in range(len(verti_map[verti_idx])):
            if verti_map[verti_idx][horiz_idx] == 1: # 1이 등장하면 칸수 판별기에 1씩 추가
                len_finder += 1
                if horiz_idx+1 == map_len:
                    if len_finder > 1: # len_finder가 1 이상일 시
                        blk_word_list.append(len_finder)  # 리스트 추가
                        len_finder = 0
            elif verti_map[verti_idx][horiz_idx] == 0:
                if len_finder > 1: # len_finder가 1 이상일 시
                    blk_word_list.append(len_finder) # 리스트 추가
                    len_finder = 0
                else: # 그게 아니면 그냥 초기화
                    len_finder = 0
 
 
 
testcase = int(input())
 
for tc_idx in range(1, testcase + 1):
    puzzle_map = []
    blk_word_list = [] # 2칸 이상의 빈줄을 수집하는 리스트
    ans = 0 # 빈칸으로 주어진 칸과 딱 맞게 일치하는 수를 구하는 변수
 
    map_len, word_len = map(int, input().split()) # 가로 세로 길이 N과 단어의 길이 K
    for map_maker_idx in range(map_len): # 지도 제작
        map_maker = list(map(int, input().split()))
        puzzle_map.append(map_maker)
 
    blk_word_finder(puzzle_map, map_len) # def 호출
 
    for i in range(len(blk_word_list)): # 2칸 이상의 빈칸을 조사해둔 리스트를 대상으로
        if blk_word_list[i] == word_len: # 제시된 단어 길이와 완전 일치하는 수 만큼
            ans += 1 # 답 1 추가
 
    print(f'#{tc_idx} {ans}')
```

#### 풀이 과정에 대한 사담
해당 문제의 중요한 점은, 딱 그 빈칸에 맞는 단어가 들어가게 해야한다는 점이다.  
다 들어가고나서 빈칸이 남으면 안 된다.  
나는 일일이 선형검색하는 식으로 길이 비교해서 맞으면 변수에 1더하는 식으로 대응했다.  

---

## SWEA D1) 9367. 점점 커지는 당근의 개수

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1926](https://swexpertacademy.com/main/code/userProblem/userProblemDetail.do?contestProbId=AW_nY2m6OLADFARY)

#### 풀이 언어

Python

#### 답안 코드

```python
test_case = int(input())
for tc_index in range(1,test_case+1):
    carrot_len = int(input()) # 당근 갯수 입력
    carrot_list = list(map(int,input().split())) # 당근 리스트 입력
 
    before_carrot = carrot_list[0] # 비교군이 될 0번 당근 값 먼저 저장
    max_counting = 1 # 최대 연속 증가값 저장
    counting = 1 # 연속 증가값 저장
 
    for c_idx in range(1, carrot_len): # 0번 당근은 비교군으로 빼뒀으니 1번부터 확인
        if max_counting < counting:  # 현 최대값과 비교하여 값이 더 크면
            max_counting = counting  # 갱신한다.
        if carrot_list[c_idx] > before_carrot: # 만약 커진다면
            counting += 1 # 카운팅한다.
        else: # 연속하지 않는다면
            counting = 1 # 그리고 초기화한다.
        before_carrot = carrot_list[c_idx] # 비교군을 교체한다.
 
    if max_counting < counting:  # 종료전 마지막 갱신, 현 최대값과 비교하여 값이 더 크면
        max_counting = counting  # 갱신한다.
    print(f'#{tc_index} {max_counting}')

```

#### 풀이 과정에 대한 사담
당근을 비교해서 값이 커지면 카운팅하고 연속해서 커지지 않으면 초기화 한다.  
설명 끝.

---

## SWEA D2) 1954. 달팽이 숫자

[Top Page](#)

#### 문제 링크

[SW Expert Academy 1954](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PobmqAPoDFAUq)

#### 풀이 언어

Python

#### 답안 코드

```python
testcase = int(input())
 
for tc_index in range(1, testcase+1):
    N = int(input())
    arr = [[0]*N for _ in range(N)] # 달팽이 그림을 그릴 빈 지도를 만든다.
    r, c = 0, 0     # 현재 위치
    # 달팽이 숫자의 방향 순서 : 우하좌상
    # dr, dc의 인덱스 의미 >> 0: 우, 1: 하, 2: 좌, 3:상
    dr = [0, 1, 0, -1]
    dc = [1, 0, -1, 0]
 
    # 오른쪽으로 이동하면서 1, 2, 3, 4, 5 넣기
    num = 1
    d = 0
 
    while True:
        arr[r][c] = num # 지금 있는 곳에 num값을 넣는다.
        num += 1 # 1에서 부터 시작하여 1, 2, 3, 4, 5 계속 증가시켜서 넣게 작동한다.
        if num == (N*N+1): # 더 이상 진행할 곳이 없다면 멈춘다.
            break
        r = r + dr[d] # 진행할 곳이 있다면 델타 좌표 값인 dr,dc를 참조하면서 계속 이동시킨다.
        c = c + dc[d]
        if c >= N or r >= N or c < 0 or r < 0 or arr[r][c]: # 델타검색 할때 벽을 만나거나 이미 값이 있는 칸은 만났다
            r -= dr[d] 
            c -= dc[d] # 방향을 바꾸기 전 마지막 유효한 위치로 되돌리는 코드, 후진기어 박고 1칸 뒤로
            d = (d + 1) % 4 # 0에서 3까지 순환시켜서 방향을 바꾸는 부분 (0에서 3까지 순환시켜서 방향을 바꾸는 부분)
            r += dr[d]
            c += dc[d] # 새로운 방향으로 이동한 후, r += dr[d]와 c += dc[d]로 새 방향으로 이동
 
    print(f'#{tc_index}')
    for i in range(N):
        print(*arr[i])
```

#### 풀이 과정에 대한 사담
델타 검색을 사용하는 방법.  

벽이나 이미 값을 채워놓은 칸을 만났다면 한칸 뒤로 이동한 뒤, 방향을 바꾸어 다른 방향으로 계속 진행시키게 바꾸면 된다.  

---



