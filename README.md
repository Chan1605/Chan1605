<div align="center">

# 👋 안녕하세요, 김종찬입니다

**유저의 니즈를 파악하고 소통에 중점을 두는 게임 클라이언트 개발자**

Unity · C#으로 조작감과 게임 흐름이 자연스러운 게임을 만드는 데 관심이 있습니다.

<a href="mailto:qkqhoe@naver.com"><img src="https://img.shields.io/badge/Email-qkqhoe@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white"/></a>
<a href="https://github.com/Chan1605"><img src="https://img.shields.io/badge/GitHub-Chan1605-181717?style=flat-square&logo=github&logoColor=white"/></a>

</div>

<br/>

## 🛠 Tech Stack

| 분야 | 기술 |
|---|---|
| **Engine** | <img src="https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white"/> |
| **Language** | <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white"/> <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"/> |
| **Network · Backend** | <img src="https://img.shields.io/badge/Mirror-4A90E2?style=for-the-badge"/> <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white"/> <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white"/> <img src="https://img.shields.io/badge/PlayFab-FF6C37?style=for-the-badge"/> |
| **Tools** | <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/DOTween-8A2BE2?style=for-the-badge"/> |

<br/>

## 📂 Projects

### 🃏 Bluff Table · 4인 온라인 멀티플레이 카드 게임 (팀 프로젝트)
> 카드로 블러핑하고 거짓말이 들키면 러시안 룰렛을 돌리는 *Liar's Bar* 모작 · 3인 팀 · Mirror · MariaDB · AWS · **담당: UI · 인게임 연출**

- 서버가 결과 · 타이밍을 정하고 UI · 연출은 **이벤트만 구독**하는 구조로, 네 플레이어가 같은 장면을 같은 순서로 보도록 설계
- LIAR 판정 · 리볼버 장전 · 룰렛 · 승리(커서를 따라가는 고개) 연출 재현, 원작 애니메이션 · 셰이더 이식을 **에디터 도구로 자동화**
- MariaDB 연동 **전적 UI**(승률 · 칭호), 음성 채팅 대신 대사 번호만 주고받는 **퀵챗**, 한국어 / 영어 현지화
- 통합 QA에서 네트워크 응답 순서로 생긴 손패 잠김, 해상도별 UI 틀어짐, 듀얼 모니터 커서 이탈 해결

[📁 Repository](https://github.com/Chan1605/Bluff_table) · [🎬 소개 영상](https://drive.google.com/file/d/1tfH6swDd5QVY0sufP1ab8DT2HlPhxjSa/view?usp=drive_link) · [📄 기술개발서 (PDF)](docs/BluffTable_TechDoc.pdf)

<br/>

### 🔦 BLACKOUT · 3D 스텔스 액션 (팀 프로젝트)
> 낮에는 탈출 재료를 모으고, 밤에는 교도관을 제압하며 탈출하는 4인 팀 프로젝트 · **담당: 적 AI**

- 순찰 → 약한 의심 → 강한 의심 → 발견(추적), 시체 발견까지 **5개 상태를 상태 패턴**으로 분리해 조건문 얽힘 방지
- 순찰 · 둘러보기 · 공격을 **커맨드 패턴**으로 구성해, 코드 수정 없이 명령 조합만으로 적마다 다른 순찰 루틴 설정
- 시야 · 청각을 **점수로 환산하는 감지 시스템**, 병 · 경보기 소리로 적을 유인하는 플레이 설계
- **ScriptableObject**로 적 스탯 45개 항목을 인스펙터에서 조정, 도달 불가 위치는 시간 제한 후 복귀해 NavMesh 경로 재계산 방지
- NPC 대화 시스템, 라이팅 · 스카이박스 담당

[📁 Repository](https://github.com/Chan1605/StealthActionGame_N) · [🎬 플레이 영상](https://drive.google.com/file/d/1jy8kzmyJzCUdjQFjE6hJTXUDssYSgHic/view?usp=drive_link) · [📄 기술개발서 (PDF)](docs/BLACKOUT_EnemyAI_TechDoc.pdf)

<br/>

### 🌟 Ori and the Blind Forest 모작 · 2D 액션 플랫포머
> 원작의 이동·전투 메커닉을 분석해 재구현한 1인 개발 프로젝트

- 바쉬(Bash), 벽 점프(입력 버퍼 + 코요테 타임), 대시, 패러세일 등 원작 이동 스킬 재현
- bool 플래그 기반 플레이어를 **열거형 상태 머신 + partial class** 구조로 리팩토링
- 소울 파밍 → 세이브 포인트 생성 → 체크포인트 복원 루프, 이벤트 기반 튜토리얼 시스템

[📁 Repository](https://github.com/Chan1605/Ori_style_platformer) ·[🎬 플레이 영상](https://drive.google.com/file/d/1eERrvVx9vkvWJPrnRWenEZG5UQG7Oirw/view?usp=drive_link) · [📄 기술개발서 (PDF)](docs/Ori_TechDoc.pdf)

<br/>

### 🐔 Chicken Royale · 3D TPS 슈팅
> PlayFab 연동 랭킹 시스템을 갖춘 PC · Mac 슈팅 게임

- FSM 기반 몬스터 AI, 조준 · 사격 · 수류탄 투척, 대시 · 스태미너 시스템
- PlayFab 로그인 · 닉네임 · 최고 기록 · 랭킹 연동, 아이템 드롭 & 인벤토리

[📁 Repository](https://github.com/Chan1605/Chicken-Royale) · [🎬 플레이 영상](https://youtu.be/cAq-W0X-D7M) · [💾 Windows](https://drive.google.com/file/d/1As4TtGGFFEUW4Lsp4gfaKbw4A5it5-iG/view?usp=drive_link) · [💾 Mac](https://drive.google.com/file/d/18TPozFCqR7o2zRArwAGxigz77zB_Qn92/view?usp=drive_link)

<br/>

### 🌳 Summoner Forest · 3D 액션
> 마우스 피킹 이동과 QWER 스킬 시스템을 구현한 개인 프로젝트

- 마우스 피킹 이동, 휠 줌, 근접 공격 및 4종 스킬, 스킬 설명 툴팁 UI
- FSM 기반 몬스터 AI, 오브젝트 풀링 리스폰, Mixamo 오토리깅 애니메이션

[📁 Repository](https://github.com/Chan1605/SummonerFroest3D) · [🎬 플레이 영상](https://www.youtube.com/watch?v=SlehHQ2Nek8)

<br/>

### 🎮 Other Projects

| 프로젝트 | 소개 | 링크 |
|---|---|---|
| GIGDC | 2D 횡스크롤 팀 프로젝트 | [🎬 영상](https://www.youtube.com/watch?v=UDCFjSiuVYs) |
| Need Turret Here | 3D 타워디펜스 팀 프로젝트 | [🎬 영상](https://www.youtube.com/watch?v=MvEQOiWDvIQ) |

<br/>

<div align="center">

[📁 전체 레포지토리 보기](https://github.com/Chan1605?tab=repositories)

</div>
