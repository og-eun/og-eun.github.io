---
title: "「Functional Programming for Java Developers」2 What is Functional Programming?"
subtitle: "1등 시민으로서의 함수"
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

#### 1등 시민으로서의 함수

자바에서는 객체와 원시 값들이 1등 시민으로 대접 받는다.

객체와 원시 값들은 메서드에게 전달되고, 그 값은 리턴되고, 리턴된 값을 다른 변수에 할당한다.

자바에서 함수는 1등 시민이 아니다. (자바는 메서드만 포함하고 있다. 메서드는 자바에서 1등 시민이 아니다.)

메서드를 다른 메서드에 인수로 전달할 수 있는가? 리턴 받을 수 있는가? 다른 변수의 값으로 할당할 수 있는가?

가능하지 않다.

대신 익명 내부 클래스가 이런 기능을 보완해주는 wrapper 역할을 수행하공 ㅣㅆ다.

함수형 프로그래밍은 함수가 수행하는 일이 무엇인지만 알게 하면 충분하다.


#### 3. 람다와 클로저

람다는 익명 함수의 다른 표현으로 리터럴 문법을 통해 반복되는 코드를 줄일 수 있다.

클로저는 함수 본문이 인수로 전달될 때, 혹은 함수가 자기 내부에서 정의된 것이 아니라 바깥에서 정의된 변수를 의미하는 자유변수 (free variables) 를 사용할 때 만들어진다.


#### 4. 고계함수

고계함수 (higher-order functions) 란 다른 함수를 인수로 받아들이거나 함수를 리턴하는 함수를 지칭하는 용어이다.


#### 5. 부수효과가 없는 함수


#### 6. 재귀


#### 7. 게으른 vs 부지런한 계산


#### 8. 선언적 vs 명령형 프로그래밍

