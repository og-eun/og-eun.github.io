---
title: "「Functional Programming for Java Developers」2 What is Functional Programming?"
subtitle: "변경 가능한 상태 피하기"
layout: post
author: "OG"
header-style: text
catalog: true
tags:
- java
- functional-programming
- functional-programming-for-java-developers
- O'REILLY
- 함수형프로그래밍
- 오렐리
---

#### 1. 변경 가능한 상태 피하기

함수형 프로그래밍에는 기본 원리들이 있다.

그 중 첫번째는 변경 불가능한 값(immutable value)을 이용하는 것이다.

값이 변경되는 것을 허용할 경우 멀티스레드 프로그래밍이 어려워지기 때문이다.

따라서 값을 변경 불가능하게 만들어서 동기화와 관련된 문제를 없앨 수 있다.


#### 2. 1등 시민으로서의 함수

자바에서는 객체와 원시 값들이 1등 시민으로 대접 받는다.

객체와 원시 값들은 메서드에게 전달되고, 그 값은 리턴되고, 리턴된 값을 다른 변수에 할당한다.

자바에서 함수는 1등 시민이 아니다. (자바는 메서드만 포함하고 있다. 메서드는 자바에서 1등 시민이 아니다.)

메서드를 다른 메서드에 인수로 전달할 수 있는가? 리턴 받을 수 있는가? 다른 변수의 값으로 할당할 수 있는가?

가능하지 않다.

대신 익명 내부 클래스가 이런 기능을 보완해주는 wrapper 역할을 수행하공 ㅣㅆ다.

함수형 프로그래밍은 함수가 수행하는 일이 무엇인지만 알게 하면 충분하다.


#### 3. 람다와 클로저


#### 4. 고계함수


#### 5. 부수효과가 없는 함수


#### 6. 재귀


#### 7. 게으른 vs 부지런한 계산


#### 8. 선언적 vs 명령형 프로그래밍

