---
title: "「Multithreaded JavaScript」 Concurrency vs Parallelism : 동시성 vs 병렬성"
subtitle: "Concurrency Beyond the Event Loop"
layout: post
author: "OG"
header-style: text
catalog: true
tags:
- multithread-javascript
- javascript
- 자바스크립트
- 동시성
- 병렬성
---

### 동시성
*동시성: 여러 작업을 동시에(한꺼번에) 처리하는 것*

### 병렬성
*병렬성: 여러 작업이 실제로 동시에 시작되고, 실행되는 것*

### 동시성과 병렬성의 차이

##### 하나의 작업을 작은 단위로 쪼개어 처리할 때
이는 **동시성은 충족되지만 병렬성은 충족되지 않는다.**
작은 단위의 작업들이 **번갈아** 가면서 실행되는 것이기 때문이다.
병렬성은 완전이 같은 시점에 여러 작업이 시작되어 처리되고 있어야 한다.



