---
title: "「Effective Java」 Class n Interface : 클래스와 인터페이스 (2)"
subtitle: "public 클래스에서는 public 필드가 아닌 접근자 메서드를 사용하라"
layout: post
author: "OG"
header-style: text
tags:
- java
- effective-java
- 자바
- 이팩티브자바
---

```
class Point {
    public double x;
    public double y;
}
```

데이터 필드에 직접 접근이 가능하다.

이는 캡슐화 이점을 제공하지 못한다는 것이다.


필드를 `private` 으로 변경하고 `public` 접근자 (`getter`) 를 추가하는 방법으로 이러한 문제를 해결할 수 있다.

```java
class Point {
    private double x;
    private double y;
    
    public double getX() {return x;}
    public double getY() {return y;}
    
    public void setX(double x) {this.x = x;}
    public void setY(double y) {this.y = y;}
}
```

클래스가 `public` 이라면 이 방식을 사용해야 한다.

접근자 메서드를 제공함으로써 클래수 내부의 유연성을 획득하였다.


