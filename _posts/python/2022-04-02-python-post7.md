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
# 1~4 내용 예시 문제 풀이

* toc
{:toc .larg-only}

# 1~4 내용 예시 문제 풀이

## 1. 문제

![titled4](/assets/img/python3/titled4.png)
### 답

```jsx
A = len(sentence)
B = int(A/2)
C = input()
sentence = sentence[:B]+C+sentence[B:]

결과
input(@)
ABC@DEF
```

### 풀이

len()함수로 “sentence” 의 길이를 구한다.

len(sentence)의 값을 반으로 나누어 중간을 찾아 B에 저장한다.
중간에 넣을 문자를 input()함수를 통해 C에 받아준다.
문자의 길이의 중간의 위치를 찾은 B 값을 이용하여, 슬라이싱을 이용해 중간에 입력값 C를 넣어준다.

## 2. 문제

![titled5](/assets/img/python3/titled5.png)
### 답

```jsx
i= int(input())
a=0, b=0, d=0, e=0
while a <= i:
	b = b+a
	a = a+1
c = b*b

while d <= i:
	e = e + (d*d)
  d = d+1

f= c-e
print(f)

결과
input(10)
2640
```

### 풀이

값이 0인 a가 1씩 더해지고, 입력한 값과 같아 질 때 까지 그 수를 모두 더 한 뒤

제곱 하는 while 문을 만든다.

값이 0인 d가 1씩 더해지고, 입력한 값과 같아 질 때 까지 d를 제곱하고 더한다.

그 두 값의 결과의 차(-)의 값을 f로 두고 출력한다.

## 3. 문제

![titled6](/assets/img/python3/titled6.png)
### 답

```jsx
odd_list = []
even_list = []
i = int(inpit())
while i!=0:
	if i%2 ==0:
					even_list.append(i)
	else:
					odd_list.append(i)
	i = int(input())

print(odd_list)
print(even_list)

결과
input(1), input(2), input(3), input(4), input(5), input(6) input(0)
[1,3,5]
[2,4,6]
```

### 풀이

while 사용하여, i가 0이 아닐때만 실행하여  0은 리스트에 들어가지 않는다.

i가 짝수이면 나머지가 0이기 때문에 나머지가 0이면 even리스트에 넣어준다.

그게아닌 나머지 경우인 홀수이면 odd리스트에 넣어준다.

0이 나올때까지 반복문이 계속되어야하고 입력값을 새로 받아줘야한다.

i값을 반복문 마지막 부분에서 새로 받아주게 해준다.

0값이 입력되면 반복문은 종료된다.

## 4. 문제

![titled7](/assets/img/python3/titled7.png)
### 답

```jsx
a= int(input())
b= int(input())
av = (a + b)/2

if a==0 or b==0:
				print('F')
elif av>100:
				print("잘못 입력했습니다. 평균이 100점을 넘을 순 없습니다.")
elif av>=80:
				print('A+')
elif av>=60:
				print('A0')
elif av>=40:
				print('B+')
elif av<40:
				print('B0')

결과
a = 50 b = 50
B+
```

### 풀이

input()으로 입력값을 받고,  if를 사용해서 단계별로 출력값을 다르게 했다.
