---
layout: post
title: 파이썬 기초 데이터타입
description: >
    파이썬 기초 데이터타입
sitemap: false
hide_last_modified: false
categories:
  - python
---

# 파이썬 기초 데이터타입

* toc
{:toc .larg-only}

### 1. 숫자 데이터타입
![python1](/assets/img/python1/python1.PNG)



### 데이터타입 - 정수

위와 같이 -1, 0, 1 정수 integer 라고하며, <mark>Python</mark>에서 int라고 표현한다.



#### 데이터타입 - 실수

실수라고 한다면 소수점이 있는 숫자를 말한다. float이 <mark>Python</mark>에서 실수형 데이터타입을 가르킨다.



#### 사칙연산

이렇게 숫자형 데이터타입이 있으면 숫자형 데이터 타입으로
연산들을 할 수 있다.
제일 기본적인 연산자는 산술연산자 이며 사칙연산이 가능하다.


#### math 로딩
사칙연산 외에 필요한 기능을 로딩해서 사용할 수 있다.
math라고하는 수학과 관련된 여러가지 기능을 가진 모듈을
import.math를 통해 로딩 하게되면

~~~
ex) math.sqrt(제곱근) , math.pow(제곱)
~~~
이러한 math.으로 시작하는 명령어를 사용할 수 있게된다.



#### random 로딩

랜덤한 숫자가 필요하면 import를 통해 random 모듈을 로딩하여
여러 기능을 사용할 수 있다.
~~~
ex) random.random() 0~1 사이 균등 부동 소수점 값 생성.
~~~


### 1. 숫자형 데이터타입의 출력값
![python2](/assets/img/python1/python2.PNG)

설명을 읽어보고, 위 입력값과 출력값을 비교해 보면서 이해해보자.



### 2. 문자형 데이터타입

![python3](/assets/img/python1/python3.PNG)


#### 문자열 인식
1. '', " " 작은 따옴표, 큰 따옴표가 없이 사용되는 문자열은<br>     문자열로 인식되지 않는다
    <br>
2. 따옴표나 큰따옴표로 만들어진 문자열을 출력할 때 줄 바꿈을 이용하면 에러가 발생한다.
<br>
    ~~~
    해결 방법 : print('''
                      hello
                      world
                      '''  ) 와 같이 따옴표또는 큰따옴표를 3개사용한다.
    ~~~
3. 1+1 의 계산이 아닌 '1'+'1' 을 문자열로 나타내고 싶으면,
    큰따옴표로 묶어주면 된다.
    <br>
    ~~~
    ex) "'1'+'1'"
    ~~~
    이 의미는 처음 큰따음표부터 다음 큰따옴표 까지 문자열로 해석한다는 의미를 가진다.



#### 문자열 연산자
1. 문자열 사이에 +는 산술연산자가아닌 문자열과 문자열을 결합하는 결합연산자가 된다.
<br>
    ~~~
    ex) '1'+'1' = 11
    ~~~
2. 곱 연산자를 사용하게 되 문자열이 반복된다.
<br>
    ~~~
    ex) print('Hello world'*3)
    ~~~


#### len() 함수 사용
1. 문자열이 몇개의 문자로 이루어져 있는지 알고싶을 때 <br> len() 함수를 사용하여, 몇개의 글자가 사용 됐는지 알 수 있다.
<br>
    ~~~
    ex) print("len('Hello world'*3)", len('Hello world'*3))
    ~~~




#### 치환 사용


1. 작성한 문자열 중에 바꾸고싶은 문자열이 있다면 다른 대체 문자열로 치환 할 수 있다.
    <br>
2. replace() 함수를 사용한다.
<br>
    ~~~
    ex)print('Hello world'.replace('world', 'universe'))
    ~~~


### 2. 문자열 데이터타입의 출력값


![python4](/assets/img/python1/python4.PNG)

위 사진의 입력값의 대한 출력값 결과이다.
또는 예시들의 출력값 결과이니 비교하며 이해해보자.


### 3. List


![python5](/assets/img/python1/python5.PNG)

#### 리스트 생성


1. 리스트 생성시, 여러 문자열 또는 숫자를 대괄호로 묶어준다.
2. 리스트 생성 후, 이름이 없으면 불러 줄 수 없어 이름을 붙혀준다.
3. 이름 = 변수라고 생각하면 되는데 변수에 대한 이야기는 뒤에서 다루기로 하자.
<br>
    ~~~
    ex) students = ["egoing", "sori", "maru"]
        stuents라는 이름을 가진 리스트
        grades = [2,1,4]
        grades라는 이름을 가진 리스트
    ~~~


#### 리스트 호출


1. list의 순서는 0, 1, 2 순이다.
       sori 학생의 이름을 호출 해보자.
       <br>
    ~~~
    ex)  print("students[1]", students[1])
    ~~~


#### 리스트 수


1. list가 몇개의 list로 구성되어 있나 확인 할 수 있다.
      len() 함수 이용.
      <br>
2. list안의 숫자 중 min() 이용해서 최솟값을 확인 할 수 있다.
    <br>
3. list안의 숫자 중 max() 이용해서 최댓값을 확인 할 수 있다.
<br>
    ~~~
    ex) 1. print("len(students)", len(students))  
        2. print("min(grades)", min(grades))
        3. print("max(grades",max(grades))
    ~~~


#### statistics 로딩


1. 평균을 구해보려고한다. 평균을 구하기 위해선 통계와 관련된 도구들이 모인 묘듈인 statistics를 앞에서 배운 것 처럼 import를 통해 로딩해준다.
<br>
2. statistics를 로딩해준 후 mean()을 사용하여 평균을 구한다.
<br>
    ~~~
    ex) import statistics
        print("statistics.mean(grades)", statistics.mean(grades))
    ~~~


#### random 로딩


1. 앞에서 사용한 random 모듈을 가지고 리스트로 정의된 Students 리스트 안의 학생 중 한명을 랜덤으로 선택해보려고한다.
2. import를 사용하여 random 을 로딩한 후 choice() 를 사용하여  선택 해보자.
  <br>
    ~~~
    ex) import random
        print("random.choice(students)", random.choice(students))
    ~~~



### 3. List의 출력값

![python6](/assets/img/python1/python6.PNG)

  위의 입력값과 출력값을 비교해보며 이해하도록 하자.
