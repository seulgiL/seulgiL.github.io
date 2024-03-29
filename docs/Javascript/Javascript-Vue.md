---
layout: default
title: Vue
parent: Javascript
nav_order: 1
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc .fs-3 }

---


# Vue 이론
{: .no_toc }

{:toc}

---

## Vue란?

- Evan You가 2014년 발표

- 사용자 인터페이스를 만들기 위한 자바스크립트 프레임워크, SPA를지원함.

- Vanilla JS를 사용했을 때, 데이터의 변경이 있다면 그 데이터를 사용하는 모든 요소들를 선택해서 데이터를 변경해야 했지만, Vue.js를 통해 Data를 변경하면 이에 연결된 DOM은 알아서 변경되도록 할 수 있다.

  

<hr>

## SPA

- Single Page Application (단일 페이지 애플리케이션)
- 데이터가 바뀔 때 마다 서버와 html파일을 주고 받는 것이 아니라, 필요한 데이터만 주고받아 하나의 html에서  필요한 부분만 동적으로 다시 작성 하는 것

- 연속되는 페이지 간의 사용자 경험(UX)를 향상 시킬 수 있음
- 모바일 네이티브 앱과 같은 형태의 웹 페이지로 모바일 최적화를 할 수 있음(1개 웹 페이지에서 여러 동작 가능)
- 동작 원리의 일부가 CSR의 구조를 따름



<hr>

## SFC 

- Single File Component
- Vue의 컴포넌트 기반 개발의 핵심 특징
- Vue 컴포넌트 === Vue 인스턴스 === .vue파일
- 각 기능별로 파일을 나눠서 개발하면 이후 변수 관리가 용이하며 기능 별로 유지 & 보수 비용 감소



<hr>

## CSR

- Client Side Rendering
- 서버에서 화면을 구성하는 SSR방식과 달리 클라이언트 쪽에서 화면을 구성
- 최초 요청시에 HTML, CSS, JS등 데이터를 제외한 각종 리소스를 응답받고, 이후에 필요한 데이터만 요청해 클라이언트의 브라우저에서 동적으로 DOM을 구성
- 단점 : SSR에 비해 전체 페이지 최종 렌더링이 느림, 검색엔진 최적화(SEO)에 어려움이 있음
- 장점 : 서버와 클라이언트간 트래픽 감소, 사용자경험(UX) 향상<br>

<span style="color:gray; font-size:80%">Vue.js, React등의 SPA프레임워크에서 SSR을 지원하는 SEO 대응 기술이 존재한다.  이를 통해 SEO 대응이 필요한 페이지에 대해 선별적 SEO 대응이 가능하다.</span>



<hr>

## SSR

- 서버에서 페이지를 모두 구성하여 클라이언트에게 주는 방식
- 단점 : 모든 요청만다 새로운 페이지를 구성하여 전달
- 장점 : 초기 구동 속도가 빠름, 검색엔진 최적화(SEO)에 적합



<hr>

## SEO

- 검색 엔진 최적화 : 웹 페이지 검색 결과의 상위에 노출될 수 있도록 하는 작업

  (참고)  Google 검색 센터<br>

  https://developers.google.com/search/docs/beginner/seo-starter-guide?hl=ko





<hr>

## MVVM

- **Model :** (== JavaScript Object) Vue Instance 내부에서 <strong style="color:Blueviolet">data</strong>라는 이름으로 존재한다.
- **View** : (==<strong style="color:Blueviolet">DOM</strong>(HTML))
- **Model View** : (== <strong style="color:Blueviolet">Vue Instance</strong>) : View와 Model 사이를 연결



<hr>

## This

- Vue 함수 객체 내에서 vue 인스턴스를 가리킴
- 함수에서 this를 쓸 때는 화살표 함수를 쓰면 안됨



<hr>

## <span style="color:Blueviolet">computed</span> vs <span style="color:Blueviolet">watch</span>

### computed

- 데이터를 기반으로 하는 계산된 '속성'
- 종속된 데이터가 변경될 때만 함수를 실행
- 반드시 반환 값이 있어야 하며, 함수가 아닌 함수의 반환값이 바인딩 된다.
- **선언형 프로그래밍 방식**

### watch

- 데이터에 변화가 일어났을 때 실행되는 함수

- function()의 인자로 데이터를 넘겨주는 것이 아니라 함수 안에서 this.dataName으로 데이터를 쓴다.
- 특정 데이터의 변화 상황에 맞춰 다른 data등이 바뀌어야 할 때 주로 사용.
- **명령형 프로그래밍 방식**



<hr>

## Lifecycle Hooks

- created -> mounted->updated->destroyed



<hr>

## 

