---
layout: post
title: 파이썬 flask
description: >
    파이썬 flask
sitemap: false
hide_last_modified: false
categories:
  - python
---

## 파이썬 플라스크 이해

#### Flask

Flask는 Python의 마이크로 웹 프레임워크다.
특정도구나 라이브러리를 필요로 하지않기 때문에 마이크로 프레임워크로 분류한다.

##### Flask 사용하는 이유
1. 다양한 웹 엔진과 결합하여 사용할 수 있다.
2. 비슷한 프레임워크인 Django보다 가볍다.
3. 코드가 단순하고, 추가 컴포넌트가 없다.
4. API 서버를 만들기에 편리하다.
5. 관련된 확장기능들이 많다.
6. 빠르고 쉽게 시작할 수 있다.

##### Flask 설치

터미널에 접속하여
~~~
pip install Flask 또는 pip3 install Flask 입력
~~~
![flask0](/assets/img/flask/flask0.PNG)

###### Flask 이해하기

직접 Flsak를 통해 서버를 실행하여 url 접속해보자.

![flask1](/assets/img/flask/flask1.PNG)

파일에서 Flask를 불러와 app 변수에담고 이 app을 이용해 Flask를 사용하게 된다.

app.route는 어떤 url 받는지에 대해 말한다.
'/'는 기본을 이야기한다.

app.route가 다른 url을 받는 경우를 보고 이해해보자.

![flask2](/assets/img/flask/flask2.PNG)

이경우 app.route에 url을 '/haha'로 설정해주어 실행된 url을 확인해 보면 /haha를 확인 해 볼 수있다.

* 웹해킹 문제에서, app.route()의 url 선언 부분에
app.route(/admin)를 선언해 admin 정보를 기입해놓기도 하며, 이것을 통해서 admin정보를 탈취하는 문제가 출제되기도 한다.
