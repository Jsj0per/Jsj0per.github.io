---
title: SWEA_D1
keywords: Algorithm, SWEA
summary: "SW Expert Academy의 D1 문제를 풀었던 기록을 적는 곳. SWEA는 회원가입이 필수인 사이트이고, 문제에 대한 무단배포가 금지된 사이트라 풀이 과정과 사담만 남기고 문제 내용은 링크로 대체합니다."
sidebar: Algorithm_sidebar
permalink: SWEA_D1.html
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

### 다른 풀이

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
리스트 내 특정 값만 계산하는 행동 자체눈 겉보기엔 간단해 보이던데 생각보다 코드로 구성시키려하니 와닿지 않았다.  
반드시 나중에 다시 한번 풀어봐야겠다.  

---
