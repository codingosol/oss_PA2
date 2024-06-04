# personal_project - 벽돌 부수기 게임

# 구현 목표
본 프로젝트는 "스와이프 벽돌 깨기" 와 기존의 벽돌 부수기 게임에서 착안하여, 공으로 내려오는 벽돌들을 맞혀서 높은 점수를 얻는 것이 이 게임의 목표입니다. 벽돌을 부술 때마다 1점씩 점수를 얻게 되며, 공이 바를 맞지 않고 바닥으로 떨어지는 순간 게임은 종료됩니다. 매 게임마다 점수를 측정하며 가장 높은 점수는 최고기록으로 기록됩니다. 최선을 다해 고득점을 노려보세요.

#구현 기능
* pygame 기반 게임 환경 구현
* 좌,우 키보드를 통해 공을 받는 기능
* 각 벽돌마다 난수 생성, 해당 난수만큼 벽돌을 맞혀야 벽돌이 부서지는 기능
* 점수를 기록하고 최고점을 갱신하는 기능
  
# reference
[1] https://github.com/pygame/pygame "pygame"
[2] https://github.com/attreyabhatt/Space-Invaders-Pygame 
[3] https://ai-creator.tistory.com/534

# 지원 Operating Systems 및 실행 방법
## 지원 Operating Systems
|OS| 지원 여부 |
|-----|--------|
|windows | :o:  |
| Linux  | :x: |
|MacOS  | :x:  |

# 코드 설명
## main.py
### class Brick
- Description : 벽돌을 생성하고 입력받은 강도를 벽돌에 출력하는 클래
  1. Def __init__ : 벽돌을 생성 및 초기화하는 단계, 좌표와 벽돌의 너비, 높이, 강도를 입력받아 초기화
  2. Def print_value : 입력받은 강도를 벽돌 내부에 텍스트로 표현하는 함수.

### def make_brick()
- COLUMN(10), LOW(2) 형태에 맞게 벽돌을 생성한 후, random.randint(1,5)로 1~5사이 난수를 생성하여 벽돌에 강도를 할당하는 함수

### def print_score(), def print_max_score()
- 화면에 현재 점수와 최고 점수를 출력하는 함수로, point, max_point 변수가 바뀔 때마다 바뀐 값을 출력하도록 동작

### def move_bricks_down()
- 기존에 있던 벽돌들을 한 칸 아래로 내리고, 맨 위에 새로운 벽돌 한 줄을 생성하는 함수. 호출 조건은 공이 바에 5번 맞았을 때 호출

### while True:
- 게임을 시작하는 무한 루프.
  1.


# TODO List
* 처음에 공을 발사할 때 각도를 조절할 수 있는 기능
* easy, normal, hard mode로 구분하여 공의 빠르기와 벽돌이 내려오는 속도 조절 기능
* 아이템 추가 - 몇개의 벽돌이 바로 제거되는 아이템, 10초동안 공이 벽돌을 맞힐 시 강도가 2씩 줄어드는 아이템, 바의 크기가 몇 초간 커지는 아이템 등
* 게임 시작부터 플레이한 점수를 저장하여 게임이 끝날 시 top 5 점수 및 걸린 시간을 등수표로 출력하는 기능  
