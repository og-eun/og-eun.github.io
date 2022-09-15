---
title: "「Effective Java」4 Class n Interface : 클래스와 인터페이스 (1)"
subtitle: "클래스와 멤버의 접근성을 제한하라"
layout: post
author: "OG"
header-style: text
tags:
  - java
  - effective-java
  - 자바
  - 이팩티브자바
---

잘 설계된 컴포넌트의 가장 큰 특징 중 하나는 **캡슐화** 이다.

코드 클래스와 멤버의 **접근성을 가능한 한 좁혀야 한다** 라는 기본 원칙을 지켜야 한다.

***

접근 수준을 `public` 으로 설정하면 공개 API 가 되고,

`package-private` 으로 선언하면 해당 패키지 내에서만 사용할 수 있다.

외부에서 사용하지 않는 클래스나 인터페이스를 `package-private` 으로 설정하면

클라이언트에 영향을 주지 않고 수정이나 교체가 가능해진다.

(이번 결제/환불 원장 프로젝트에서 `public/private` 관리를 통해 장점을 많이 느끼고 있다.)

***

한 클래스에서만 사용하는 `package-private top-level` 클래스/인터페이스 는

이를 사용하는 클래스 안에 `private static` 으로 중첩 시키는 방법이 있다.

*top-level* 로 같은 패키지의 모든 클래스가 접근 가능하지만

`private static` 으로 중첩하면 바깥 클래스 하나에서만 접근이 가능하다.

***

책에서는 이보다 더 중요한 아니 가장 중요한 것으로 **public 일 필요가 없는 클래스의 접근 수준을 `package-private`** 으로 좁히는 것을 뽑는다.

다시 한 번. `public` 은 패키지의 API 이고, `package-private` 은 내부 구현이다.

***

멤버에 부여할 수 있는 접근 수준 4가지를 접근 범위가 좁은 것 부터 다시 살펴보자.
멤버 : 필드, 메서드, 중첩 클래스, 중첩 인터페이스

- `private`: 멤버를 선언한 *top-level* 에서만 접근 가능
- `package-private`: 멤버가 소속된 패키지 내 모든 클래스에서 접근 가능. 접근 제한자가 명시되지 않았을 때 적용되는 `default` 패키지 접근 수준. (인터페이스의 멤버는 `public`)
- `protected`: `package-private` 의 접근 범위를 포함하고, 이 멤버를 선언한 클래스의 하위 클래스에서도 접근 가능.
- `public`: 모든 곳에서 접근 가능.

***

1 : 공개 범위를 설계한 후, 이 외 모든 멤버를 `private` 로 만든다.

2 : 같은 패키지 내 다른 클래스가 접근해야 하는 멤버를 `package-private` 로 풀어준다. (`private` 제한자를 제거한다)

***

테스트를 위해서 클래스, 인터페이스, 멤버 접근 범위를 넓히려 할 때가 있는데 적당 수준까지는 괜찮다.

예를 들면 `public` 클래스의 `private` 멤버를 `package-private` 으로. 그 이상은 안 된다.

+ 테스트 대상을 같은 패키지에 두면 `package-private` 요소에 접근이 가능하기 때문에 이 이상으로 접근할 필요가 없다! (최근 경험담. 꿀팁을 얻었다.)

***

그 외.

`public` 클래스의 인스턴스 필드는 되도록 `public` 이 아니게.

`public` 가변 필드를 갖는 클래스는 일반적으로 *thread safe* 하지 않다.

클래스에서 `public static final` 배열 필드를 두거나, 이 필드를 반환하는 접근자 메서드를 제공해선 안된다.

