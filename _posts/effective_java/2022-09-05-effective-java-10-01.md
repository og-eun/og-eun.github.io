---
title: "「Effective Java」10 예외 (1)"
subtitle: "예외는 진짜 예외 상황에만 사용하라"
layout: post
author: "OG"
header-style: text
tags:
- java
- effective-java
- 자바
- 이팩티브자바
---


저자가 얘기하는 운이 없는 경우 마주치게 될 코드는 아래와 같다.

```java
try {
    int i = 0;
    while(true)
        range[i++].climb();
}catch (ArrayIndexOutOfBoundsException e) {
}
```

위 코드가 운 없는 사람이 마주하게 되는 이유

1. 가독성
2. 무한루프를 돌고 돌아 배열 끝에서야 예외를 마주한다.

그런데 위 코드에서 예외가 필요할까?

아래 코드와 위 코드는 다른 일을 하지 않는다.

```java
for (Mountain m : range)
    m.climb();
```

일반적 반복문도 배열의 끝에 도달하면 종료된다.

따라서

1. 예외는 말 그대로 예외 상황에서만 써야 한다
2. 잘 설계된 API 라면 클라이언트가 정상적 제어 흐름에서 예외를 사용할 일이 없게 해야 한다.

결론 : 아무때나 예외를 남발하지 말자.
