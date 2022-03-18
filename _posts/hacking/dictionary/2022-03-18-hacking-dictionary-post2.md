---
layout: post
title: XSS 우회기법
description: >
    XSS 우회기법
sitemap: false
hide_last_modified: false
categories:
  - Hacking
  - dictionary
---

# XSS 우회기법 (Dreamhack xss-2)

여기선 XSS우회기법에 대해서 깊게 다루지않고,
Dreamhack xss-2 문제를 예로 들어 얕게만 알아보려고한다.

![dictionary](/assets/img/dictionary/dictionary.PNG)

위 사진은 xss-2 문제의 한 부분이며 주소창을 보면, 접속 시
alert(1) 을 출력하게 되어있지만 출력되지 않는 모습을 보아
script는 필터링 되어있다는걸 알 수있다.
* 'script'로 필터링이 되어 있는 경우 대문자와 함께 사용해 xss를 우회할 수 있다.
~~~
ex)  <sCriPt>alert(1)</sCRIpt>
~~~

* script 문이 아닌 다른 html 속성들을 이용해서 alert문을 실행시킬 수 있다.
~~~
ex) <img src=about: onerror=alert("test")>
    <svg src=about: onload=alert("test")>
    <body onload=alert("test")>
    <video><source onerror=alert("test")></video>
~~~

더 많은 방법들이 있지만, 현재 문제에선 이 내용으로 해결이 가능하다.
깊은 방안들과 세세한 내용들은 후에 다루도록 할 예정이다.
