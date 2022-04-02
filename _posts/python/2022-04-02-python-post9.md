---
layout: post
title: 파이썬 기초
description: >
    파이썬 기초
sitemap: false
hide_last_modified: false
categories:
  - python
---

# 6- 함수와 메서드

* toc
{:toc .larg-only}

## 목표

1. 함수가 무엇인지 이해한다.
2. 내장 함수를 사용하고, 함수를 직접 만들 수 있다.
3. 메서드와 함수의 차이를 이해한다.

# 함수

### 프로그래밍의 기본틀

컴퓨터에게 정보를 입력하고.
컴퓨터가 작업을 하고
컴퓨터가 작업 결과를 출력한다.

![titled8](/assets/img/python3/titled8.png)

### 함수

특정 기능을 수행하는 코드(들의 모임)

### 함수의 구조

1. len() : 자료를 넣으면 그 자료의 길이를 알려준다
2. int() :  자료를 넣으면 정수형으로 변환해서 알려준다
3. str() :  자료를 넣으면 문자열로 변환해서 알려준다

## 함수의 종류

### 내장 함수

파이썬 개발자들이 이미 만들어 둔 함수들
편리하게 가져다 쓰면 된다

```jsx
print()
len()
max()
int()
```

### input()과 print()

1. input( ) ‒ 자료를 입력하는 함수
2. print( ) ‒ 자료를 출력하는 함수

```jsx
a = input() # Hello 입력
print(a) # Hello
```

### max()와 min()

1. max( ) ‒ 시퀀스 자료의 최댓값을 구하는 함수
2. min( ) ‒ 시퀀스 자료의 최솟값을 구하는 함수

```jsx
print(max(1, 2, 3, 4, 5)) # 5
print(min([1, 2, 3, 4, 5])) # 1
```

### sum()과 len()

1. sum( ) ‒ 숫자 원소로 이루어진 시퀀스 자료의 합
2. len( ) ‒ 시퀀스 자료의 길이를 구하는 함수

```jsx
print(sum(1, 2, 3, 4, 5)) # 15
print(len(“Triangle”)) # 8
```

## 사용자 지정 함수

사용자가 여러 코드를 묶어서 새로 만든 함수

```jsx
def plusDouble(a, b):
c = a+b
return 2*c
print(plus(3, 4)) # 14
```

## 함수 만들기

define(정의하다) 키워드를 이용해서 함수 정의

```jsx
def 함수이름 (매개변수):
		<수행할 명령>
		...
		return 반환값
```

## 함수의 입력

매개변수를 이용해서 함수 내부로 값을 전달

```jsx
def 함수이름 (매개변수):
		<수행할 명령>
		...
		return 반환값
```

## 함수 속 명령 작성

같은 들여쓰기를 통해 명령 작성

```jsx
def 함수이름 (매개변수):
_ _  _ _		<수행할 명령>
_ _  _ _		...
_ _  _ _		return 반환값
```

## 함수의 반환(출력)

return을 이용해서 함수 외부로 값을 전달

## 왜 반환이 필요할까?

함수 내부에서 일어난 일은 함수 외부에서 알 수 없다!
→ 반환을 통해 외부로 전달!

```jsx
def plus(a, b):
c = a+b
return c
print(plus(3,4))
```

```jsx
def plus(a, b):
c = a+b
return c
print(7)
```

# 전역 변수와 지역 변수

### 함수와 변수

왜 x가 출력 되지 않을까?
함수 안에서 일어난 일은 함수 밖에 영향을 끼치지 않는다

```jsx
def my_func(a):
x = “Hi!”
print(a)

a = 3
my_func(a) # 3
print(x) # error!
```

### 전역 변수

어디서든지 사용할 수 있는 변수

```jsx
x = “Hi!”
def my_func():
print(x)
my_func() # Hi!
print(x) # Hi!
```

### 지역 변수

특정 구문(for문, 함수 …) 안에서 정의한 변수
변수를 정의한 범위에서만 사용이 가능!

```jsx
def my_func():
x = “Hi?”
print(x)
my_func() # Hi?
print(x) # error
```

## Method(메서드)

### 메서드(Method)

특정 자료에 대해 특정 기능을 하는 코드

```jsx
my_list = [1, 2, 3]
my_list.append(4)
my_list.count(2)
my_list.pop()
```

### 함수 vs 메서드

1. 함수는 특정 기능을 한다
(매개변수를 이용해 자료를 전달해준다)

```jsx
my_list = [1, 2, 3]
len(my_list)
sum(my_list)
min(my_list)
```

1. 메서드는 특정 자료와 연관 지어 기능을 한다
(자료 뒤에 .을 찍어 사용한다)

```jsx
my_list = [1, 2, 3]
my_list.sort()
my_list.pop()
my_list.clear()
```

## 요약

### 요약

함수는 특정 기능을 수행하는 코드의 모임!
내장 함수와 외장 함수
전역 변수와 지역 변수의 차이
메서드의 특징
