---
title: "「Multithreaded JavaScript」 Web Worker 웹 워커: 전용 워커, 공유 워커, 서비스 워커"
subtitle: "Concurrency Beyond the Event Loop"
layout: post
author: "OG"
header-style: text
catalog: true
tags:
- multithread-javascript
- javascript
- 자바스크립트
- 웹워커
- 전용워커
- 공유워커
- 서비스워커
---

### 웹 워커
최신 웹 브라우저에서 제공하는 멀티스레딩 API 로 CPU 부하량이 높은 작업을 별도 스레드에서 처리할 수 있다.
웹 워커를 사용하면 독립적인 스레드에서 자바스크립트 코드를 실행시킬 수 있다.

1. 전용 워커 (dedicated worker)
웹 워커의 여러 종류 중 **가장 단순하다.**

2. 공유 워커 (shared worker)
다양한 브라우저 환경에서 접근이 가능한 워커.
공유 워커마다 각각의 self 를 가지고 있다. (SharedWorkerGlobalScope의 인스턴스)

3. 서비스 워커 (service worker)
웹 페이지 사이를 연결하는 프록시 같은 역할을 하는 워커.
여러 개의 페이지와 연결되어 있는 형태로 전용 보다는 공유 워커에 가깝다고 볼 수 있다. 
