# Space Invaders 확장 프로젝트 — Group 2 (Gameplay HUD)

> 2022년 2학기 한양대학교 ERICA 수업에서 **9개 팀, 약 45명**이 하나의 Java 게임 저장소를 Fork·Pull Request로 나눠 확장한 협업 프로젝트입니다.
> 이 저장소는 그중 **Group 2 (5명, Gameplay HUD 담당)** 의 작업 포크입니다.

## 내 역할

- **신기록 "new" 표시 기능을 팀원과 함께 개발**: 게임 중 점수가 저장된 최고 기록을 넘으면 점수 앞에 `new`를 표시 (`DrawManager.drawScore()`)
- 개인 Fork → 팀 저장소 → 중앙 저장소로 이어지는 PR 흐름으로 다른 팀과 같은 코드베이스에서 협업

## Group 2가 만든 기능

1. 인터페이스 색상 선택 (초록 외 빨강·파랑)
2. 생명 포인트 아이콘 변경
3. 신기록 달성 시 `new` 표시
4. 점수 옆 `score` 라벨
5. 난이도(easy·normal·hard)별 5개 스테이지 선택
6. 게임 중 획득 코인 표시

## 2026년 포트폴리오 정리 때 고친 것

- **빌드 오류 수정**: 2022-10-27 커밋(`f33da29`)에서 `drawScore()`의 `catch` 블록과 점수 출력이 함께 지워져 컴파일이 되지 않던 문제를 고치고 `new` 표시를 복구했습니다.
- **인코딩 통일**: `PracticeScreen.java`만 MS949로 저장돼 있던 것을 UTF-8로 바꿔 어느 환경에서나 빌드되게 했습니다.

## 다시 본다면 개선할 점

- `drawScore()`가 화면을 그릴 때마다 최고 기록 파일을, `drawCoin()`이 코인 이미지를 매번 디스크에서 읽습니다. 게임 시작 시 한 번 읽어 캐시해야 합니다.
- 코인 이미지 경로가 Windows 전용(`icon\\coin-icon.png`)이라 다른 OS에서 동작하지 않습니다.

## 실행

```bash
javac -encoding UTF-8 -d out $(find src -name "*.java")
java -cp out:res Main        # Windows는 out;res
```

---

# Space Invaders

This is a project that extends the [Space Invaders](https://en.wikipedia.org/wiki/Space_Invaders) clone ([RobertoIA/Invaders](https://github.com/RobertoIA/Invaders)).

## Teams
_Thursday Class (22-2-23359)_

| No. | Name        | Members                     | Requirements      |   
|-----|-------------|-----------------------------|-------------------|
| 0   | [Instructors](teams/instructors.md) | Scott Uk-Jin Lee, [Hansae Ju](https://github.com/Verssae/Verssae) | Instruct students |
| 1   |[Group1](https://github.com/Farhiya11/thu-space-invaders-group1/blob/main/teams/group1.md)     | [Farhiya](https://github.com/Farhiya11/Farhiya11) ,  [조해초](https://github.com/haechojo/haechojo), [서엽](https://github.com/xuyu0916/xuyu0916-gmail.com), [하가휘](https://github.com/qlask1/-/tree/main), [Zhou Junlei](https://github.com/LouisChow0306/LouisChow)                   |  [SoundEffects&BGM](https://github.com/Farhiya11/thu-space-invaders-group1/blob/main/teams/group1.md)                  |
| 2   |  [Group2](teams/group2.md)   |  [Jaehyeok Jo](https://github.com/poer2424/poer2424), [Yoonyoung Kim](https://github.com/rladbsdud123/rladbsdud123), [Hoseung Nam](https://github.com/hsnam99/hsnam99), [Hyeongil Lee](https://github.com/201HI/201HI), [Woonyoung Kim](https://github.com/woon325/woon325)      |  [Gameplay HUD](teams/group2.md)  |
| 3   |[Group3](teams/group3.md)|[Seunghye Jeon](https://github.com/Jeon-sh/Jeon-sh/blob/main/README.md), [Yunjae Kim](https://github.com/jerryfly1/jerryfly1/blob/main/README.md), [Junyeong Kim](https://github.com/trueu1120/Info/blob/main/README.md), [Ahyeon Lee](https://github.com/ahyns62/ahyns62/blob/main/README.md), [Seojun Moon](https://github.com/tsalt1026/tsalt1026/blob/main/README.md)| [Visual Effect System](https://github.com/Jeon-sh/Jeon-sh/blob/main/Group3.md)|
| 4   | [599100](https://github.com/CSE2024-SDP-Team4/thu-space-invaders) | [안도형](https://github.com/andohyung/andohyung) [윤성빈](https://github.com/SeongBinYoon/SeongBinYoon) [전현우](https://github.com/Jeonhyeonwoo/Jeonhyeonwoo) [최진영](https://github.com/orca10/orca10) [한정우](https://github.com/jeongulupe/jeongulupe) [홍진수](https://github.com/bakukun/bakukun) | [Main menu / Setting](https://github.com/Verssae/thu-space-invaders/blob/main/teams/group4.md) |  
| 5   | [Group5](teams/group5.md)   |  [Kim TaeHyeon](https://github.com/DevTae/DevTae/blob/main/README.md), [Kim SunYub](https://github.com/goggi772/goggi772/blob/main/README.md), [Lee YeBeom](https://github.com/beom-i/beom-i/blob/main/README.md), [Kim JeongWoo](https://github.com/wookim0719/wookim0719/blob/main/README.md), [Lee ChanYoung](https://github.com/diligentcoder7/diligentcoder7/blob/main/README.md) | [Records System](teams/group5.md) |
| 6   | [Group6](teams/group6.md) | [Hyeonsoo Kim](https://github.com/hsoo3844/hsoo3844), [Soyeon Kwon](https://github.com/annkwon1123/annkwon1123), [Taeyoon Lee](https://github.com/TYParrot/TYParrot), [Jeongwoo Eum](https://github.com/jeongwoo99/jeongwoo99), [Jaeho Sin](https://github.com/sjh7535/sjh7535)       | [Various player ship & enemies](teams/group6.md) |
| 7   | [Dropship](teams/dropship.md) | [Jeahyeon Jeong](https://github.com/jjangjjh2222/jjangjjh2222.git), [Joonghyeon Park](https://github.com/pjh2976/Joonghyeon.git), [Myeongin Jin](https://github.com/myeonginjin/myeonginjin.git), [Jinsung Sim](https://github.com/Sims0212/Sims0212.git), [Jongha Kim](https://github.com/hanyangduck/hanyangduck.git) | Item System |
|  8   | [Team 8](teams/team8.md)     |[Jun Young Lee](https://github.com/intelli21c/intelli21c), [Jeong Min Park](https://github.com/snavellib/snavellib), [Yeon Ju Ko](https://github.com/koyeonju126/koyeonju126), [Jae Wan Choi](https://github.com/Jaewan0/Jaewan0), [Ji Yoon Jeong](https://github.com/j1037/j1037)| Currency System             |
| 9   | [Java Chip Frappuccino](https://github.com/devITae/thu-space-invaders) | [이재형](https://github.com/devITae/devITae/) [박선빈](https://github.com/whaleflyingsky/whaleflyingsky/) [이선우](https://github.com/tjsdn1204/tjsdn1204/) [정성우](https://github.com/jsw3285/jsw3285/) [정연욱](https://github.com/dhfpdhaos/dhfpdhaos/) [D.Bat_Undrakh](https://github.com/Bat-Undrakh/Bat-Undrakh/) | [Level Design System](https://github.com/devITae/thu-space-invaders/blob/main/teams/JavaChipFrappuccino.md) |

## Screenshots
 

Title Screen               |  Game Screen              | Score Screen
:-------------------------:|:-------------------------:|:---------
![image](https://user-images.githubusercontent.com/69495129/136980139-7ad6adab-3f11-4711-b0a6-341080aa3361.png)   |  ![image](https://user-images.githubusercontent.com/69495129/136980236-c5d9ef85-f09a-47a7-b9d9-948f7b624002.png)|![image](https://user-images.githubusercontent.com/69495129/136980681-93dcadaf-08cb-48d8-90c9-68c651a115c9.png)


## Development

- IDE : IntelliJ IDEA


## System Requirements
Requires Java 7 or better.
