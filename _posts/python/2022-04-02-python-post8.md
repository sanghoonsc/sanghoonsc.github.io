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


# 5- 기초자료형 II

* toc
{:toc .larg-only}

## 목표

1. 문자열과 리스트를 더 활용할 수 있다
2. 튜플이 무엇인지 알고, 리스트와의 차이점을 이해한다
3. 딕셔너리를 이해하고 이를 직접 만들 수 있다

## 문자열 / 리스트활용

### list.pop(i)

인덱스 i의 원소를 제거 후 그 원소를 반환
(괄호를 비울 시 마지막 원소)

```jsx
my_list = [1, 2, 3, 4, 5]
print(my_list.pop(0)) # 1
print(my_list.pop()) # 5
```

### seq.count(d)

시퀀스 내부의 자료 d의 개수를 반환

```jsx
my_seq = [2, 2, 2, 4, 4]
print(my_seq.count(2)) # 3
```

### str.split(c)

c를 기준으로 문자열을 쪼개서 리스트를 반환
(괄호를 비울 시 공백)

```jsx
my_str = “1 2 3 4 5”
print(my_str.split()) # [‘1’, ‘2’, ‘3’, ‘4’, ‘5’]
element = “Na,Mg,Al,Si”
print(element.split(‘,’)) # [‘Na’, ‘Mg’, ‘Al’, ‘Si’]
```

### str.join(list)

str을 기준으로 리스트를 합쳐서 문자열을 반환
(괄호를 비울 시 공백)

```jsx
my_list = [‘a’, ‘p’, ‘p’, ‘l’, ‘e’]
print(‘’.join(my_list)) # apple
friend = [‘Pat’, ‘Mat’]
print(‘&’.join(friend)) # Pat&Mat
```

## Tuple(튜플)

여러 자료를 담는 자료형이 필요하면?
대부분 리스트를 이용
그러나 값이 바뀔 위험이 있다!

```jsx
my_list = [‘l’, ‘i’, ‘s’, ‘t’]
my_list[1] = ‘a’
print(my_list) # [‘l’, ‘a’, ‘s’, ‘t’]
```

### Tuple의 필요성

값을 바꿀 수 없으면서도
여러 자료를 담을 순 없을까?
→ Tuple(튜플)!

### Tuple(튜플)

여러 자료를 함께 담을 수 있는 자료형
( ) ‒ 소괄호로 묶어서 표현

```jsx
tuple_zero = ()
tuple_one = (1,)
tuple_ = (1, 2, 3, 4, 5)
tuple_ = 1, 2, 3, 4, 5
```

### Tuple의 특징

1. 시퀀스 자료형으로
Index를 이용한 인덱싱, 슬라이싱이 가능

```jsx
my_tuple = (‘t’, ‘w’, ‘i’, ‘c’, ‘e’)
print(my_tuple[1]) # ‘w’
print(my_tuple[2:4]) # (‘i’, ‘c’)
```

1.  +연산자로 Tuple과 Tuple을 연결

        *연산자로 Tuple을 반복

```jsx
my_tuple = (‘i’, ‘c’, ‘e’)
print((‘e’, ‘l’) + my_tuple) # (‘e’, ‘l’, ‘i’, ‘c’, ‘e’)
print(my_tuple * 2) # (‘i’, ‘c’, ‘e’, ‘i’, ‘c’, ‘e’)
```

1. 자료 추가, 삭제, 변경 불가
한 번 만들어지면 고정!

```jsx
my_tuple = (‘t’, ‘w’, ‘i’, ‘c’, ‘e’)
print(my_tuple.append(‘!’)) # Error
print(my_tuple.remove(‘w’)) # Error
my_tuple[1] = ‘s’ # Error
```

## Dictionary(딕셔너리)

### Dictionary

1. Dictionary → 사전
     짝꿍이 있는 자료형!
2. { } ‒ 중괄호로 묶어서 표현
3. 짝꿍이 있는 자료형
{key : value}의 형식 : key를 알면 value를 알 수 있음

```jsx
dict_zero = {}
person = {‘name’:‘Michael’, ‘age’:10}
```

## Key

열쇠처럼 자료를 꺼낼 수 있는 도구

```jsx
dict_zero = {}
person = {‘name’:‘Michael’, ‘age’:10}
```

## Value

Dictionary에서 Key로 꺼낸 자료

```jsx
dict_zero = {}
person = {‘name’:‘Michael’, ‘age’:10}
```

## Dictionary[key]

1. Dictionary에서 자료를 꺼내기

```jsx
person = {‘name’:‘Michael’, ‘age’:10}
print(person[‘name’]) # Michael
print(person[‘age’]) # 10
```

1. Dictionary에서 자료를 추가하기

```jsx
person = {‘name’:‘Michael’, ‘age’:10}
person[‘hometown’] = Seoul
```

## Del

del 함수로 Dictionary의 원소 삭제

```jsx
person = {‘name’:‘Michael’, ‘age’:10}
del person[‘age’]
print(person) # {‘name’:‘Michael’}
```

## Dictionary의 특징

Key는 변할 수 없는 자료형
→ 리스트는 안되고, 튜플은 된다!

```jsx
datas = {[1, 2, 3]:‘Alphabet’} # Error
datas = {(1, 2, 3):‘Number’} # OK
```

## 요약

문자열과 리스트의 활용
Tuple과 리스트의 차이점을 통해 그 특성을 이해
Dictionary 속 Key와 Value 짝꿍

1. list.pop()
2. str.split()
3. sequence.count()
4. str.join()
