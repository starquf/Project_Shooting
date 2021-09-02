# Project_Shooting

[영상링크](https://www.youtube.com/watch?v=CpcIrIVJCRc&t=1s)

## 1. 게임 설명
>동방 프로젝트의 시스템을 참고하여 유니티로 만든 탄막 슈팅게임입니다.

1. 플레이어를 조종하여 주어진 목숨안에 적들의 공격을 피하고 공격을 하여 최대한 고득점을 하는 것이 목표인 게임입니다.
2. 총 2스테이지로 구성되어있고 게임시작전에 2개의 캐릭터중 하나를 선택해서 플레이할 수 있습니다.
3. 캐릭터는 서로 다른 플레이스타일을 가지고 있고 폭탄의 이펙트도 다릅니다.

***

## 2. 코드 설명
### 2.1. 탄막
다양한 탄막을 구현해보려고 노력하였고 대부분의 탄막들은 삼각함수, 코루틴, 이동속도 변경, 각도 변경 등을 활용하여 구현하였습니다.

### 2.2. 적 패턴
수많은 적을 만들기 위해 코드를 재활용할 수 있는 FSM을 구현하였습니다.

인터페이스를 활용하여 필요한 기능들을 만들어 AddComponent로 추가해서 사용하고
곂치는 코드(예를 들어 원을 그리며 쏘는 패턴)는 재활용 할 수 있습니다.

### 2.3. 랭킹 시스템
게임이 끝나면 점수, 플레이한 캐릭터, 클리어한 스테이지 수 등을 JSON형태로 저장하고 랭킹 배열에 들어가게 됩니다. 

랭킹은 LINQ를 활용하여 내림차순으로 정렬을 하고 8위까지 보여줍니다.
