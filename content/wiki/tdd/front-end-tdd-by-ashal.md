---
title: "아샬님 프론트엔드 TDD"
date: "2019-12-10 11:29:30 +0900"
template: "wiki"
draft: false
slug: "/wiki/front-end-tdd-by-ashal"
category: ""
tags:
---

## 아샬 프론트엔드 TDD

### GOAL

- 핵심 아이디어 이해
- TDD 도입 출발점 마련

### TDD란 무엇인가

- 피드백 주기를 최대한 짧게 하는게 핵심 -> 두려움 제어

### 중복을 몰아낸다는 건 어떤 의미인가

- 재사용 가능한 코드를 만드는 것.

### 좋은 설계란 무엇인가

- 변경이 쉬운 코드.

### 어떻게 배울 수 있는가

- 팀 안에서 서로 얘기를 해보며 배울 수 있음.

### 작게 시작한다는 건 어떤 의미인가

- 복잡하게 얽혀있는 기능을 분석하여 단순화하는 것.

### 리팩토링의 전제 조건은 무엇인가

- 회귀 테스트가 있어야 함. 문제가 생겼을 때 알아챌 수 있도록.

### SoC(Separation of Concerns)

### SRP

- 변경해야되는 이유가 오직 한 개여야 함.

### Reactive Programming

- 선언형 프로그래밍: SQL (의도를 쓰면 결과가 나옴)
- 명령형 프로그래밍: for - if - if - for ...
- Reactive Programming은 선언형 프로그래밍

### Unit Test

- Code 레벨 테스트

### Integration Test

- 아키텍쳐, 설계 레벨 테스트

### Mocking

- UI 레이어는 Application, Domain 레이어와 같은 하위 레이어를 의존하기 때문에 Mocking이 필요함.

### Redux, Vuex

- 테스트 코드만 잘 쓰면 모든게 끝나도록 만들어진 녀석들.
- UI 레이어가 많은 일을 하지 않도록 만듦.
