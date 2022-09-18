---
title: "「Functional Programming for Java Developers」 함수형 프로그래밍 (1)"
subtitle: "기본 원리 : 변경 가능한 상태 피하기"
layout: post
author: "OG"
header-style: text
catalog: true
tags:
- java
- functional-programming
- functional-programming-for-java-developers
- 함수형프로그래밍
---

#### 변경 가능한 상태 피하기

함수형 프로그래밍에는 기본 원리들이 있다.

그 중 첫번째는 변경 불가능한 값(immutable value)을 이용하는 것이다.

값이 변경되는 것을 허용할 경우 멀티스레드 프로그래밍이 어려워지기 때문이다.

따라서 값을 변경 불가능하게 만들어서 동기화와 관련된 문제를 없앨 수 있다.
