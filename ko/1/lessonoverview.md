---
title: 레슨 개요
actions: ['정답 확인하기', '힌트 보기']
skipCheckAnswer: true
material:
  saveZombie: false
  zombieResult:
    hideNameField: true
    ignoreZombieCache: true
    answer: 1
---

레슨 1에서 자네는 준비 군대를 건설하기 위한 "좀비 공장"을 만들 걸세.

* 우리 공장은 군대 내 모든 좀비의 데이터베이스를 유지할 걸게
* 우리 공장은 새로운 좀비를 생성하는 함수를 가질 걸세
* 각 좀비는 랜덤하고 독특한 외모를 가질 걸세 

이후 레슨에서 인간이나 다른 좀비를 공격하는 능력 등 더 많은 기능을 추가할 것이네. 그전에 새로운 좀비를 생성하는 기본 기능을 추가해야 하네.

## 좀비 DNA가 활용되는 방법

좀비의 외모는 "좀비 DNA"에 따라 달라질 것이네. 좀비 DNA는 다음과 같이 간단하게 16자리 정수이네:

```
8356281049284737
```

실제 DNA처럼 이 숫자의 각 부분은 좀비가 가진 개별 특성과 매핑이 될 것이네. 처음 2자리 숫자는 좀비의 머리 타입과 연결이 되고, 그 다음 2자리 숫자는 좀비의 눈 모양과 연결이 되지. 

> 참고: 본 튜토리얼에서는 단순화해서 좀비의 머리 타입이 7개만 있을 거네 (2 자리 숫자로 100가지 경우의 수를 구할 수 있지만). 나중에 머리 타입을 다양하게 하고 싶다면 더 많은 머리 타입을 추가할 수도 있을 거네. 

이를테면, 위의 예시 DNA에서 첫 2자리 숫자 `83`이네. 이를 좀비 머리 타입으로 매핑하기 위해 우리는 `83 % 7 + 1` = 7 연산을 하지. 그래서 이 DNA를 가진 좀비는 7번째 좀비 머리 타입을 갖게 되지. 

우측 패널에서 `head gene` 슬라이더를 7번째 머리 타입 (산타 모자)로 이동시킨 다음, `83`에 어떤 특성이 대응되는지 살펴 보게.

# 직접 해보기

1. 페이지 우측의 슬라이드를 가지고 놀아 보게. 다양한 숫자 값에 따라 좀비의 외모가 어떻게 달라지는지 실험해 보게.

자, 충분히 가지고 놀았겠지. 계속 진행할 준비가 되었다면, 아래 "다음 챕터"를 클릭하게. 솔리디티 학습을 본격적으로 시작해 보세!