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

# 4- 파이썬 반복문

* toc
{:toc .larg-only}

## 반복문

### 반복문의 필요성

만약 별을 100개 출력해야 한다면?

```jsx
print("*") # * 출력 코드
print("**") # * 출력 코드
print("***") # * 출력 코드
print("****") # * 출력 코드
print("*****") # * 출력 코드
...
```

시간이 많이 들게됩니다.

같은 명령을 반복하는 코드를 묶어서 표현하는 반복문을 배워보자!

### 반복문

어떠한 **조건**이나, **범위 내**에서 어떠한 명령을
반복적으로 수행하는 것

### 반복문 l - for 문

형식

**[1, 2, 3, 4, 5]에서 원소를 하나씩 가져와서     출력!**

 시퀀스                          for                         명령

### for 문

1) **원소로 반복**하는 방법
시퀀스의 원소를 **하나씩 변수에 넣어가면서** 명령 실행

2) for문에 들어갈 명령들은 **같은 들여쓰기**로 구분!

```jsx
for 변수 in 시퀀스:              ex) sum = 0
_ _<수행할 명령>                        for i in [1, 2, 3]:
                                     _ _sum = sum + i
```

 3)  명령이 **len(시퀀스)**번 만큼 실행!

```jsx
for 변수 in 시퀀스:            ex) length = 0
<수행할 명령>                      for x in 'abcdefg'
                                   _ _length = length + 1
```

### for문 예시

**1, 2, …, 10까지 출력하기**

```jsx
for i in [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]:
print(i)
```

## for-range문

### 반복문 ll - for-range 문

**10회   동안   count를 하나씩 세라!**

횟수      for                 명령

### range

**연속되는 숫자**를 만들어 주는 시퀀스 자료형

```jsx
range(a, b) #a, a+1, a+2, … , b-1
range(0, 9) #0, 1, … , 7, 8
range(5) #range(0, 5) – 0, 1, 2, 3, 4
```

### for-range l

**구간으로 반복**하는 방법
**a이상 b미만의 수**를 변수에 넣어가면서 명령을 수행

```jsx
for 변수 in range(a,b):           ex) a = [1]
<수행할 명령>                         for i in range(2, 4):
					  a.append(i)
                                      print(a) #[1, 2, 3]  

  			    	#이하는 출력값을 나타냅니다.
```

### for-range ll

**횟수로 반복**하는 방법
**a번** 만큼 명령을 수행

```jsx
or 변수 in range(a):           ex) count = 0
<수행할 명령>                       for i in range(10):
				     count = count + 1
				    print(count) 	 #10

				#이하는 출력값을 나타냅니다.
```

## while문

### 반복문 lll - while 문

**count가 0보다 클         동안      count를 출력!**
   조건                  while             명령

### while문

**조건으로 반복**하는 방법
**조건이 True**이면 명령을 수행

```jsx
while 조건:              ex) i = 5
<수행할 명령>                 while i >0:
				print(i)
				i = i - 1
			      print(“Launch!”) # 5 4 3 2 1  Launch!

                              #이하는 출력값을 나타냅니다.
```

### while문 예시

**1부터 4까지 더하기**

```jsx
i = 1
sum = 0
while i<5:
sum = sum + i
i = i + 1
print(sum) #10

#이하는 출력값을 나타냅니다.
```

### 항상 True인 while문

**무한정 코드가 실행된다.**
→ 빠져나올 수 없는 **무한루프**에 빠진다…!

```jsx
i = 1                         # 실행결과
while i>0: #항상 True           1  
print(i)                        2  
i = i + 1                       3
                                …
```

### break문

**if문**으로 조건을 걸어준 다음, break 실행
반복문을 **탈출**하는 역할!

```jsx
= 0                                # 실행결과
while True:                        knock
print(“knock”)                     knock
if i >= 3:                         knock
break                              knock    
i = i + 1
```
