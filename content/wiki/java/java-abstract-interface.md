---
title: "Java Abstract & Interface"
date: "2019-12-06 15:43:08 +0900"
template: "wiki"
draft: false
slug: "/wiki/java-abstract-interface"
category: ""
tags:
---

## 결국 얘네들이 있는 이유는 코드의 중복을 제거하기 위함이다.

### abstract

- 일반 메소드 or 멤버변수 가질 수 있다.
- 미완성 설계도.
- 하나라도 추상 메소드를 포함해야 된다면 해당 클래스는 추상 클래스여야 한다.
- 달라질 가능성이 있으면 추상 메소드, 달라질 가능성이 없으면 일반 메소드.

### interface

- 거의 밑그림 수준(추상 클래스보다 추상화 정도가 높음)
- 일반 메소드, 멤버변수를 가질 수 없다.
- 인터페이스가 구현될 클래스에 대한 명세서 같은 역할.
