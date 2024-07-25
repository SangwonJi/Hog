# 🎲 게임 오브 호그 (Game of Hog)

## 프로젝트 개요
Hog는 턴제 주사위 게임을 시뮬레이션하고 전략을 세우는 프로젝트입니다. 

게임의 주요 목표는 각 턴마다 주사위를 굴리는 횟수를 전략적으로 선택하여 상대보다 먼저 100점을 달성하는 것입니다. 

게임 메커니즘, 확률, 그리고 전략 수립의 다양한 측면을 사용했습니다.

## 사용된 언어
- Python

## 주요 기능

### 주사위 굴리기 메커니즘
- `roll_dice(num_rolls, dice)`: 지정된 횟수만큼 주사위를 굴리고, '1'이 나올 경우 해당 턴의 점수가 '1'이 되는 특수 규칙을 처리

### 특별 규칙
- `boar_brawl(player_score, opponent_score)`: 특정 숫자에 기반하여 0개의 주사위를 굴릴 때 활성화되는 특별 득점 규칙을 구현
- `fuzzy_points(score)`: 플레이어의 점수와 100의 최대 공약수(GCD)를 기준으로 추가 득점을 적용

### 턴 진행 및 점수 업데이트
- `take_turn(num_rolls, player_score, opponent_score, dice)`: 주사위를 굴릴지 Boar Brawl 규칙을 사용할지에 따라 플레이어의 턴에서 얻은 점수를 결정
- `simple_update(num_rolls, player_score, opponent_score, dice)` 및 `fuzzy_update(num_rolls, player_score, opponent_score, dice)`: 턴 후 플레이어의 점수를 업데이트, fuzzy_update는 Fuzzy Factors 규칙을 포함

### 게임 시뮬레이션
- `play(strategy0, strategy1, update, score0, score1, dice, goal)`: 지정된 전략과 득점 규칙을 사용하여 두 플레이어 간의 전체 게임을 시뮬레이션

### 전략 및 실험
- `always_roll(n)`, `catch_up`와 같은 다양한 전략을 구현하고 테스트
- `boar_strategy`와 `fuzzy_strategy`와 같은 맞춤형 전략도 포함
- `run_experiments()` 함수는 여러 게임을 시뮬레이션하고 승률을 계산하여 다양한 전략의 성능을 평가

### 유틸리티 함수
- `hog_gcd(x, y)`: 두 숫자의 최대 공약수를 계산하며, Fuzzy Factors 규칙에서 사용
- `make_averaged(original_function, total_samples)`: 함수를 평균화하여 다양한 전략 및 주사위 굴림의 평균 결과를 평가하는 데 사용

## 인사이트
- 주사위 굴리기와 게임 결과를 통해 확률 및 통계 분석 이해
- Python을 사용한 게임 메커니즘 및 규칙 구현
- 시뮬레이션을 통한 전략 개발 및 평가
- 재귀 함수 (Recursion) 및 고차 함수 (Higher order function) 활용

## 결론
게임 오브 호그 프로젝트에서는 파이썬 프로그래밍, 알고리즘적 사고, 그리고 게임 설계를 주요 기술로 활용하였습니다.

프로젝트를 통해 시뮬레이션, 전략 개발, 확률 분석 등의 분야에서 종합적으로 프로그래밍에 대해서 배웠습니다. 





