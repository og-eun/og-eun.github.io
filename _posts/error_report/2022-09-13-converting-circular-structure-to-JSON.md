---
title: "ERROR: Converting circular structure to JSON"
subtitle: "순환 참조 시 발생하는 에러"
layout: post
author: "OG"
header-style: text
catalog: true
tags:
- error
- java-script
- 에러
- 자바스크립트
---

### Converting circular structure to JSON
테스트를 하다 위 에러를 발견하였다.
구글링을 통해 순환 참조 시 발생하는 에러임을 확인하였다.

### 주로 발생하는 상황
다른 사람들의 얘기를 들어보니 주로 `Object` 를 `JSON.stringify()` 할 때 발생하였고 역시나 내 상황도 마찬가지였다.

에러를 파싱할 때 객체 자체를 `JSON.stringify()` 하고 있었는데 이때 해당 에러가 발생했다.

`JSON.stringify()` 부분을 해결하고 나니 진짜 에러가 나는 원인을 알 수 있었다.


### What

선회하는 구조를 `JSON` 으로 변환하려고 해서 발생하는 에러


### Why

순환 참조 시 발생


### How to

1. 순환 종속성 제거
2. `flatted package` 사용
3. `console.log()` 제거

