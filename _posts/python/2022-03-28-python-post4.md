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

# 2- 파이썬 조건문

* toc
{:toc .larg-only}

## 목표

1.컴퓨터에게 정보를 전달할 수 있다.

2.논리 자료형을 알고, 이를 활용할 수 있다.

3.조건에 따라 문제를 해결할 수 있다.

## 입력 - input()



### 입력

정보를 컴퓨터에게 전달해주도록합시다.

이때, 컴퓨터는 사용자가 전달한 값을
어딘가에 보관해야 합니다.
→ 변수를 사용!

### input()

변수 = input()

```jsx
var = input()
```

이후 실행 시 터미널에 입력값을 넣어줄 수 있습니다.

### input()의 중요한 특징

무엇을 입력하든 “문자열”로 입력이 받아집니다.

만약 숫자를 입력해야 한다면, 입력을 받은 후에 가공해주어야 합니다!

뒤에 바로 가공에 대해 알아봅시다!

## 형 변환

### 형 변환

문자열을 숫자로 바꾸고 싶다면,
자료형 사이의 변환 → 형 변환!

```jsx
바꿀_자료형(바뀔_자료)

integer #숫자(정수)
float #숫자(실수)
string #문자열
list #리스트
```

```jsx
ex)
a = ‘345’
b = int(‘345’)
print(a,b) #345 345
print(type(a)) #<class ‘str’> | 문자열
print(type(b)) #<class ‘int’> | 숫자
```

- **type()**함수는 괄호안의 변수의 자료형을 반환합니다.
- **input()**함수는 입력받은 값을 문자열(string)로 인식합니다.

## 논리형 자료와 비교연산

### 1) 논리 자료형

**참(True)** 혹은 **거짓(False)**을 나타내는
자료형을 **논리 자료형**이라고 합니다.

### 2) 비교 연산자

숫자나 문자의 값을 비교하는 연산자
**주어진 진술이 참이면 True, 거짓이면 False**

```jsx
print(3 < 5) #True
print(7 == 5) #False
print(2 >= 10) #False
print(5 != 10) #True
```

### 비교 연산자의 종류

```jsx
== 같다
!= 다르다
> 왼쪽이 더 크다
< 오른쪽이 더 크다
>= 왼쪽이 같거나 크다
<= 오른쪽이 같거나 크다
```

### 3) 논리 자료형의 연산

True, False밖에 없는 논리 자료형
→ 새로운 연산이 필요합니다!

1. **AND**

각 논리가 **모두** True여야 True!

```jsx
print(3==3 and 4<=5 and 6>2)
#세 항이 모두 True이므로, True!
>>> True
```

1. **OR**

논리들 중 True가 **존재**하면 True!

```jsx
print(3==4 or 4<=5 or 6<2)
# 4<=5가 True이므로, True가 존재하기에 True!
>>> True
```

1. **NOT**

논리값을 뒤집습니다!

```jsx
print(not 3==4)
# False에 Not을 붙였으므로, True!
>>> True
```

## 조건문

어떠한 **특정 조건**에 따라서
**실행되는 명령이 달라지는** 구문입니다!

### if 문

1. (만약)   (i == 1)이면, (i를 출력) 의 형식.
  if          조건              명령

      조건이 **True**일 때, **명령** 실행

2. if문에 들어갈 명령들은 같은 들여쓰기로 구분합니다!

```jsx
if 조건:                      ex) if string[0] == “a”:
_ _<수행할 명령>                    _ _ count = count + 1
_ _<수행할 명령>                    _ _ print(string)
_ _<..>                            
```

### if-else 문

조건이 **True**면 if문 **False**면 else문 실행한다.

```jsx
if 조건:                   ex) if x in [‘a’, ‘e’, ‘i’, ‘o’, ‘u’]:
<수행할 명령>                       print(“모음입니다.”)
	else:                       else:
<수행할 명령>                       print(“자음입니다.”)

```

### if-elif 문

조건 1이 True면 if문
조건 1이 False이면서 조건 2가 True면 elif문 실행한다.

```jsx
if 조건 1:                    ex) x = int(input())
<수행할 명령>                     if x % 2 == 0:
elif 조건 2:                          print(“2의 배수입니다.”)
<수행할 명령>                     elif x % 3 == 0:
                                      print(“3의 배수입니다.”)

```

### if-elif-else 문

```jsx
if 조건 1:                ex) 조건 1 True
do A                           → A 실행
elif 조건 2:                  조건1 False and 조건2 True
do B                           → B 실행
elif 조건 3:                  조건1 False and 조건2 False and 조건3 True
do C                           → C 실행          
. . .                          …
else:                         모든 조건이 False
do X                          → X 실행
```
