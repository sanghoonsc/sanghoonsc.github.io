---
layout: post
title:  Cross Site Scripting
description: >
    XSS
sitemap: false
hide_last_modified: false
categories:
  - Hacking
  - dictionary
---
# Cross Site Scripting (XSS)
* toc
{:toc .larg-only}

### XSS란?
 <a>xss</a>는 클라이언트 사이드 취약점중 하나이며, 공격자가 웹 리소스에 악성 스크립트를 삽입해 이용자의 웹 브라우저에서 해당 스크립트를 실행하게 한다.
 공격자는 취약점을 통해 특정 계정의 세션 정보를 탈취하고 해당 계정으로 임의의 기능을 수행할 수 있다.

### 약어가 XSS인 이유  
Cross Site Scripting 라고 명시되어있는데
왜 약어가 XSS인지 궁금해 할 수 있다.
본래에는 CSS가 맞지만 스타일시트를 정의하는 언어인 CSS와 중복으로 인해서 혼동되어 사용될 수 있어서 XSS로 명명되었다.

### XSS공격의 발생

<a>XSS 공격</a>은 이용자가 삽입한 내용을 출력하는 기능에서 발생합니다.
~~~
ex) 게시물 등록 또는 로그인 시 출력되는 문구
~~~
클라이언트는 HTTP 형식으로 웹 서버에 리소스를 요청하고 서버로부터 받은 응답, 즉 HTML, CSS, JS 등의 웹 리소스를 시각화하여 이용자에게 보여주게된다. 이때, HTML, CSS, JS와 같은 코드가 포함된 게시물을 조회할 경우 이용자는 변조된 페이지를 보거나 스크립트가 실행될 수 있다.

### XSS 종류

XSS는 발생 형태에 따라서 다양한 종류로 구분되는데, XSS 종류와 악성 스크립트가 삽입되는 위치를 확인해보자.

1. <kbd>Stored XSS</kbd> : XSS에 사용되는 악성 스크립트가 서버에 저장되고 서버의 응답에 담겨오는 XSS
2. <kbd>Reaflected XSS</kbd> : XSS에 사용되는 악성 스크립트가 URL에 삽입되고 서버의 응답에 담겨오는 XSS
3. <kbd>DOM-based XSS</kbd> : XSS에 사용되는 악성 스크립트가 URL Fragment에 삽입되는 XSS
* Fragment는 서버 요청/응답에 포함되지 않는다.
4. <kbd>Universal XSS</kbd> : 클라이언트의 브라우저 혹은 브라우저의 플러그인에서 발생하는 취약점으로 SOP 정책을 우회하는 XSS
