# ⚔️ Java RPG - 코드로 싸워라!

> **자바 프로그래밍 개념을 게임으로 배우는 RPG 게임**  
> Java 문제를 풀어서 괴물을 물리치는 인터랙티브 학습 게임

![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-Active-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## 📋 목차

- [프로젝트 소개](#-프로젝트-소개)
- [주요 기능](#-주요-기능)
- [기술 스택](#-기술-스택)
- [게임 규칙](#-게임-규칙)
- [설치 및 실행](#-설치-및-실행)
- [프로젝트 구조](#-프로젝트-구조)
- [코드 예제](#-코드-예제)
- [게임 스크린샷](#-게임-스크린샷)
- [문제 유형](#-문제-유형)
- [성과 시스템](#-성과-시스템)

---

## 🎮 프로젝트 소개

**Java RPG**는 Java 프로그래밍 개념을 게임의 형식으로 학습할 수 있는 웹 기반 RPG 게임입니다.
- 플레이어는 다양한 **Java 문제를 풀어서 보스(빌런)와 전투**합니다
- 문제를 맞추면 보스에게 **대미지**를 입히고, 틀리면 플레이어가 **피해**를 입습니다
- **3개의 스테이지**를 클리어하여 최종 우승을 노려봅시다! 🏆

---

## ✨ 주요 기능

| 기능 | 설명 |
|------|------|
| 🎯 **객관식 문제** | 4개 선택지 중 정답을 선택하는 문제 |
| 💻 **코드 입력** | 빈칸에 들어갈 Java 코드를 직접 입력 |
| ⏱️ **실시간 타이머** | 객관식 30초, 코드 입력 60초 제한 시간 |
| 🔥 **콤보 시스템** | 연속 정답으로 콤보 획득, 특수 효과 발동 |
| 💚 **자동 HP 감소** | 4초마다 1 HP 자동 소진 (플레이어) |
| 🏆 **랭킹 시스템** | 모든 플레이어의 최고 점수 기록 |
| 📊 **다양한 난이도** | 초급, 중급, 고급 문제 (단계별) |
| 📝 **개념별 분류** | 변수, 객체, 컬렉션 등 주제별 문제 |

---

## 🛠️ 기술 스택

### 프론트엔드
| 기술 | 용도 |
|------|------|
| **HTML5** | 마크업, 시맨틱 구조 |
| **CSS3** | 반응형 디자인, 애니메이션 |
| **Vanilla JavaScript** | 게임 로직, DOM 조작 |
| **Google Analytics** | 게임 사용 통계 추적 |

### 백엔드
| 기술 | 용도 |
|------|------|
| **Java** | 서버 백엔드 로직 |
| **Spring Boot** | 웹 애플리케이션 프레임워크 |
| **Railway** | 클라우드 배포 |

### 디자인
- **반응형 웹 디자인** - 모바일, 태블릿, 데스크톱 지원
- **다크 테마** - 시각적 편안함과 몰입감
- **CSS Grid & Flexbox** - 최신 레이아웃 기법

---

## 🎮 게임 규칙

### 게임 흐름

```
시작 화면
   ↓
닉네임 입력
   ↓
스테이지 1 시작 (변수 빌런 🗿)
   ↓
문제 풀기 (4개 문제)
   ├─ 정답 → 보스 대미지 + 점수 획득
   └─ 오답 → 플레이어 피해 20 HP
   ↓
스테이지 1 클리어 (4/4 문제 완료)
   ↓
스테이지 2 시작 (객체 빌런 🐉)
   ↓
스테이지 3 시작 (컬렉션 빌런 👹)
   ↓
최종 결과 화면 (승리/패배) → 랭킹 등록
```

### 승리/패배 조건

| 조건 | 결과 |
|------|------|
| 3개 스테이지 모두 클리어 | 🏆 **승리** |
| 플레이어 HP가 0 이하 | 💀 **패배** |

### 점수 계산

```javascript
// 정답 시 점수 획득
정답 점수 = 기본 점수 + (난이도 × 배수) + (콤보 보너스)

// 콤보 특수 효과
2 Combo: 플레이어 +5 HP 회복
3 Combo: 플레이어 +10 HP 회복 + 보스 -10 HP 추가 대미지
5 Combo: 보스 -20 HP 추가 대미지
```

---

## 🚀 설치 및 실행

### 필수 요구사항
- 최신 웹 브라우저 (Chrome, Firefox, Safari, Edge)
- 인터넷 연결
- (선택) 백엔드 서버 실행: `http://localhost:8080`

### 실행 방법

#### 1️⃣ 온라인 플레이 (권장)
> 백엔드 서버가 배포되어 있으면 바로 시작할 수 있습니다.
```bash
# 저장소 클론
git clone https://github.com/nanemo4168-arch/java-RPG-game.git
cd java-RPG-game

# index.html을 브라우저에서 열기
# 또는 간단한 HTTP 서버로 실행
python -m http.server 8000
# http://localhost:8000 접속
```

#### 2️⃣ 로컬 개발 환경
```bash
# 저장소 클론
git clone https://github.com/nanemo4168-arch/java-RPG-game.git

# 백엔드 서버 실행 (별도 저장소 필요)
# https://github.com/your-backend/rpg-game-backend
java -jar rpg-game-backend.jar

# 프론트엔드 실행
cd java-RPG-game
open index.html
# 또는
python -m http.server
```

---

## 📁 프로젝트 구조

```
java-RPG-game/
├── README.md              # 프로젝트 설명 (이 파일)
├── index.html             # 메인 게임 파일
│   ├── HTML 마크업
│   ├── CSS 스타일 (600+ 줄)
│   └── JavaScript 로직 (850+ 줄)
└── 백엔드 API
    └── https://rpg-game-backend-production.up.railway.app/api/game
```

### 주요 구성 요소

```
index.html 구조
├── 스타일 정의
│   ├── CSS 변수 (색상, 크기)
│   ├── 반응형 레이아웃
│   └── 애니메이션
├── HTML 화면
│   ├── 타이틀 화면 (#screen-title)
│   ├── 게임 화면 (#screen-game)
│   ├── 랭킹 화면 (#screen-ranking)
│   └── 종료 화면 (#screen-end)
└── JavaScript 게임 로직
    ├── 전역 상태 (G 객체)
    ├── API 통신 함수
    ├── 렌더링 함수
    ├── 이벤트 핸들러
    └── 애니메이션 함수
```

---

## 💻 코드 예제

### 1. 전역 상태 관리

```javascript
// 게임 상태를 하나의 객체로 관리
let G = {
  playerId: null,           // 현재 플레이어 ID
  nickname: '',             // 플레이어 닉네임
  playerHp: 100,            // 플레이어 현재 HP
  bossHp: 0,                // 보스 현재 HP
  bossMaxHp: 0,             // 보스 최대 HP
  stage: 1,                 // 현재 스테이지 (1-3)
  score: 0,                 // 누적 점수
  combo: 0,                 // 현재 콤보 카운트
  questionNumber: 0,        // 현재 문제 번호
  totalQuestions: 4,        // 스테이지당 문제 수
  currentQuestion: null,    // 현재 문제 데이터
  bossEmoji: '🗿',         // 현재 보스 이모지
  timerInterval: null,      // 타이머 인터벌
  timerSeconds: 30,         // 남은 시간 (초)
  timerMax: 30,             // 타이머 최대값
  gameOver: false,          // 게임 종료 여부
};
```

### 2. API 통신 - 게임 시작

```javascript
async function startGame() {
  const nickname = document.getElementById('nicknameInput').value.trim();
  
  // 유효성 검사
  if (!nickname) {
    alert('닉네임을 입력해주세요!');
    return;
  }
  
  try {
    // 백엔드에 게임 시작 요청
    const response = await fetch(`${API}/start`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ nickname })
    });
    
    if (!response.ok) throw new Error('서버 오류');
    
    const data = await response.json();
    
    // 전역 상태 업데이트
    G.playerId = data.playerId;
    G.nickname = data.nickname;
    G.playerHp = data.playerHp;
    G.bossHp = data.boss.currentHp;
    G.bossMaxHp = data.boss.maxHp;
    G.bossEmoji = data.boss.emoji;
    
    // UI 업데이트
    document.getElementById('playerNameDisplay').textContent = nickname;
    document.getElementById('bossNameDisplay').textContent = data.boss.name;
    
    // 게임 시작
    showScreen('game');
    startHpDrain();
    loadNextQuestion();
    
  } catch (error) {
    alert('게임을 시작할 수 없습니다: ' + error.message);
  }
}
```

### 3. 답변 처리 및 점수 계산

```javascript
async function processAnswer(answer, questionType) {
  try {
    // 백엔드에 답변 제출
    const response = await fetch(`${API}/answer`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        playerId: G.playerId,
        questionId: G.currentQuestion.questionId,
        answer: answer,
        questionType: questionType
      })
    });
    
    const result = await response.json();
    
    // 게임 상태 동기화
    G.playerHp = result.playerHp;
    G.bossHp = result.bossHp;
    G.bossMaxHp = result.bossMaxHp;
    G.score = result.totalScore;
    G.combo = result.comboCount;
    
    // 시각적 피드백
    if (result.correct) {
      showDamageFloat('-' + result.damageDealt, 'to-boss');
      shakeBoss();
    } else {
      shakePlayer();
      showDamageFloat('-HP', 'to-player');
    }
    
    // 콤보 이펙트 표시
    if (result.comboEffect) {
      showComboToast(result.comboEffect);
    }
    
    // 결과 피드백 표시
    const header = result.correct 
      ? '✅ 정답! +' + result.scoreGained + '점'
      : '❌ 오답! 정답: ' + result.correctAnswer;
    
    showFeedback(
      result.correct,
      header,
      result.explanation,
      result.correctAnswer,
      '다음 문제 →',
      loadNextQuestion
    );
    
    // 게임 종료 조건 확인
    if (result.gameStatus === 'WIN') {
      showEndScreen(true);  // 승리
    } else if (result.gameStatus === 'LOSE') {
      showEndScreen(false); // 패배
    }
    
  } catch (error) {
    console.error('오류:', error);
    alert('답변을 처리할 수 없습니다.');
  }
}
```

### 4. HP 자동 감소 (생존 압박)

```javascript
function startHpDrain() {
  G.hpDrainInterval = setInterval(() => {
    if (G.gameOver) return;
    
    // 4초마다 1 HP 감소
    G.playerHp = Math.max(0, G.playerHp - 1);
    updatePlayerHpDisplay();
    
    // HP가 0 이하면 게임 오버
    if (G.playerHp <= 0) {
      stopHpDrain();
      stopTimer();
      showEndScreen(false);
    }
  }, 4000);
}
```

### 5. 타이머 및 시각적 피드백

```javascript
function updateTimerDisplay() {
  const percentage = (G.timerSeconds / G.timerMax) * 100;
  const timerBar = document.getElementById('timerBar');
  
  // 남은 시간에 따라 색상 변경
  timerBar.style.width = percentage + '%';
  timerBar.className = 'timer-bar-fill ' + 
    (percentage > 60 ? 'time-ok' :      // 녹색 (충분함)
     percentage > 30 ? 'time-warn' :    // 노란색 (경고)
     'time-danger');                    // 빨간색 (위험)
  
  document.getElementById('timerText').textContent = 
    G.timerSeconds + '초';
}
```

### 6. 콤보 시스템

```javascript
function updateComboDisplay(comboCount) {
  const comboEl = document.getElementById('comboDisplay');
  
  if (comboCount >= 2) {
    // 2 콤보 이상일 때만 표시
    comboEl.innerHTML = `
      <div class="combo-badge">
        🔥 ${comboCount} COMBO!
      </div>
    `;
  } else {
    comboEl.innerHTML = '';
  }
}

// 특수 효과 토스트
function showComboToast(effect) {
  const toast = document.getElementById('comboToast');
  
  const icon = effect.type === 'HEAL' ? '💚' : '🔥';
  document.getElementById('comboToastIcon').textContent = icon;
  document.getElementById('comboToastText').textContent = effect.message;
  
  // 1.8초간 표시
  toast.classList.add('show');
  setTimeout(() => toast.classList.remove('show'), 1800);
}
```

---

## 🎬 게임 스크린샷

### 타이틀 화면
```
┌─────────────────────────────────────────┐
│                                         │
│          ⚔️ Java RPG ⚔️                │
│      문제를 맞혀서 괴물을 물리치시오     │
│                                         │
│  🗿 변수빌런  🐉 객체빌런  👹 컬렉션빌런 │
│                                         │
│  ┌────────────────────────────────┐   │
│  │  닉네임을 입력하고 시작하세요   │   │
│  │  [______________________]      │   │
│  │  [⚔️ 게임 시작]               │   │
│  │  [🏆 랭킹 보기]               │   │
│  └────────────────────────────────┘   │
│                                         │
└─────────────────────────────────────────┘
```

### 게임 화면 (전투)
```
┌──────────────────────────────────────────────────┐
│ ⚔️ Java RPG              [🏆 랭킹] [🚪 나가기]   │
├──────────────────────────────────────────────────┤
│ [STAGE 1] 문제 1 / 4          🏆 점수: 2,500    │
├──────────────────────────────────────────────────┤
│ 타이머 ████████░░░░░░░░ 15초                     │
├──────────────┬──────────────────────────────────┤
│              │                                   │
│  플레이어    │  빌런                            │
│   🧙       │  🗿                              │
│   HP ████████│  HP ████████░░░                  │
│   95/100     │  250/300                         │
│              │                                   │
├──────────────┴──────────────────────────────────┤
│ 🔥 2 COMBO!                                      │
├──────────────────────────────────────────────────┤
│ 📌 [변수] [중급] [📝 빈칠 채우기]                │
│                                                   │
│ 다음 코드의 빈칸(_____)에 들어갈 타입은?       │
│ ┌──────────────────────────────────────────────┐│
│ │ int count = 5;                               ││
│ │ _____ result = count + 3.5;                  ││
│ └──────────────────────────────────────────────┘│
│                                                   │
│ 💻 빈칸에 들어갈 코드를 입력하세요:            │
│ ┌──────────────────────────────────────────────┐│
│ │ [_____________________]                      ││
│ │ [✅ 제출] [💡 힌트] Enter로 빠르게 제출    ││
│ └──────────────────────────────────────────────┘│
└──────────────────────────────────────────────────┘
```

### 피드백 모달
```
┌──────────────────────────────────┐
│  ✅ 정답! +100점                 │
├──────────────────────────────────┤
│  ⚔️ 빌런 HP -50                  │
│  🛡️ 내 HP -0                     │
├──────────────────────────────────┤
│  올바른 풀이입니다!              │
│  double 타입은 소수점을 표현하는 │
│  실수형 데이터 타입입니다.       │
│                                  │
│  정답: double                     │
├──────────────────────────────────┤
│         [다음 문제 →]            │
└──────────────────────────────────┘
```

### 스테이지 클리어 화면
```
┌──────────────────────────────────┐
│           💥                     │
│          🗿 (처치됨)             │
│                                  │
│      🎉 STAGE CLEAR! 🎉         │
│     💀 빌런을 처치했다!          │
│                                  │
│  다음 빌런 등장: 🐉 객체 빌런    │
│                                  │
│  ┌──────────────────────────┐   │
│  │         🐉              │   │
│  │    객체 빌런             │   │
│  │  Java의 모든 것은       │   │
│  │  객체입니다             │   │
│  │  HP: 400 / 공격력: 30   │   │
│  └──────────────────────────┘   │
│                                  │
│     [스테이지 2 시작 →]         │
└──────────────────────────────────┘
```

### 랭킹 화면
```
┌────────────────────────────────────────┐
│ ⚔️ Java RPG              [← 뒤로]     │
├────────────────────────────────────────┤
│            🏆 명예의 전당 🏆           │
├────────────────────────────────────────┤
│ 순위│   닉네임   │ 점수  │ 스테이지│결과│
├────┼────────────┼───────┼────────┼────┤
│ 🥇 │ Hero123    │ 5,000 │  3스테이지│승리│
│ 🥈 │ JavaMaster │ 4,200 │  3스테이지│승리│
│ 🥉 │ CodeNinja  │ 3,800 │  2스테이지│패배│
│  4 │ Learner99  │ 2,500 │  1스테이지│패배│
│  5 │ Developer1 │ 1,800 │  1스테이지│패배│
├────────────────────────────────────────┤
│        [🏠 홈으로]                   │
└────────────────────────────────────────┘
```

### 게임 오버 화면
```
┌──────────────────────────────────┐
│           🏆                     │
│                                  │
│     🎉 VICTORY! 🎉              │
│  모든 빌런을 물리쳤습니다!       │
│   Java 마스터가 되었습니다!      │
│                                  │
│  ┌──────────────────────────┐   │
│  │  최종 점수: 12,500       │   │
│  │  도달 스테이지: 3        │   │
│  │  남은 HP: 45            │   │
│  └──────────────────────────┘   │
│                                  │
│    [🔄 다시 하기] [🏆 랭킹 보기] │
└──────────────────────────────────┘
```

---

## 📝 문제 유형

### 1️⃣ 객관식 (Multiple Choice)
- **형식**: 4개의 선택지 중 정답 선택
- **시간 제한**: 30초
- **난이도**: 초급(1), 중급(2), 고급(3)

```
예시 문제:
┌─────────────────────────────────┐
│ 다음 중 변수 선언이 올바른 것은? │
├─────────────────────────────────┤
│ [A] int age = "25";             │
│ [B] int age = 25;               │
│ [C] String age = 25;            │
│ [D] Integer age = "25";         │
└─────────────────────────────────┘
```

### 2️⃣ 코드 입력 (Code Input)
- **형식**: 빈칸(_____)에 들어갈 코드 직접 입력
- **시간 제한**: 60초
- **채점**: 정확한 코드 문자열 매칭
- **힌트**: 선택적 힌트 제공

```
예시 문제:
┌──────────────────────────────────┐
│ 다음 코드의 출력은?              │
├──────────────────────────────────┤
│ for (int i = 0; i < 3; i++) {   │
│   System.out.print(i);           │
│ }                                │
│ // 출력: _____                   │
├──────────────────────────────────┤
│ [_________________]              │
│ [✅ 제출] [💡 힌트]             │
│                                  │
│ 💡 힌트: 0부터 2까지 출력됩니다 │
└──────────────────────────────────┘
```

---

## 🎖️ 성과 시스템

### 점수 획득 방식

| 상황 | 점수 | 설명 |
|------|------|------|
| ✅ 정답 (초급) | +50 | 난이도 1 문제 정답 |
| ✅ 정답 (중급) | +100 | 난이도 2 문제 정답 |
| ✅ 정답 (고급) | +150 | 난이도 3 문제 정답 |
| 🔥 2 콤보 | +25 | 추가 보너스 |
| 🔥 3 콤보 | +50 | 추가 보너스 |
| ❌ 오답 | -20 | HP 피해 |
| ⏰ 시간 초과 | -15 | HP 피해 |

### 콤보 특수 효과

```javascript
2 Combo: 💚 플레이어 +5 HP 회복
   ├─ 체력 조건: 현재 HP < 최대 HP
   └─ 시각 효과: "회복! +5 HP" 토스트

3 Combo: 💚 플레이어 +10 HP + 🔥 보스 -10 HP
   └─ 플레이어와 보스 모두에게 효과

5 Combo: 🔥 보스 -20 HP 추가 대미지
   └─ 보스에게만 추가 대미지
```

### 난이도별 데미지

```
정답 시 보스에게 가하는 데미지:
초급 (Difficulty 1): 30 ~ 50 데미지
중급 (Difficulty 2): 60 ~ 80 데미지
고급 (Difficulty 3): 100 ~ 150 데미지

오답 시 플레이어가 입는 피해:
- 고정 피해: 20 HP
- 보스 공격력: 스테이지별 상이
```

### 보스 정보

| 보스 | 스테이지 | HP | 공격력 | 주제 | 특징 |
|------|---------|-----|-------|------|------|
| 🗿 변수 빌런 | 1 | 300 | 15 | 변수, 타입 | 기초 개념 |
| 🐉 객체 빌런 | 2 | 400 | 25 | 클래스, 객체 | 중급 개념 |
| 👹 컬렉션 빌런 | 3 | 500 | 30 | 배열, List, Map | 고급 개념 |

---

## 🔧 API 엔드포인트

### 게임 시작
```http
POST /api/game/start
Content-Type: application/json

{
  "nickname": "Hero123"
}

응답:
{
  "playerId": "player-uuid",
  "nickname": "Hero123",
  "playerHp": 100,
  "boss": {
    "name": "변수 빌런",
    "emoji": "🗿",
    "currentHp": 300,
    "maxHp": 300,
    "description": "Java의 변수를 담당하는 빌런",
    "stage": 1,
    "attackPower": 15
  },
  "questionsPerStage": 4
}
```

### 문제 조회
```http
GET /api/game/question?playerId=player-uuid

응답:
{
  "questionId": "q-123",
  "questionNumber": 1,
  "totalQuestions": 4,
  "concept": "변수",
  "difficulty": 2,
  "questionType": "MULTIPLE_CHOICE",
  "questionText": "다음 중 변수 선언이 올바른 것은?",
  "optionA": "int age = \"25\";",
  "optionB": "int age = 25;",
  "optionC": "String age = 25;",
  "optionD": "Integer age = \"25\";",
  "hint": "정수 타입 변수에는 정수값을 할당해야 합니다."
}
```

### 답변 제출
```http
POST /api/game/answer
Content-Type: application/json

{
  "playerId": "player-uuid",
  "questionId": "q-123",
  "answer": "B",
  "questionType": "MULTIPLE_CHOICE"
}

응답:
{
  "correct": true,
  "correctAnswer": "B",
  "explanation": "int는 정수를 나타내는 타입입니다.",
  "scoreGained": 100,
  "totalScore": 2500,
  "damageDealt": 75,
  "playerHp": 95,
  "bossHp": 225,
  "bossMaxHp": 300,
  "comboCount": 2,
  "comboEffect": {
    "type": "HEAL",
    "message": "회복! +5 HP"
  },
  "gameStatus": "CONTINUE",
  "questionNumber": 2
}
```

### 랭킹 조회
```http
GET /api/game/ranking

응답:
[
  {
    "rank": 1,
    "nickname": "Hero123",
    "score": 5000,
    "maxStage": 3,
    "result": "WIN"
  },
  {
    "rank": 2,
    "nickname": "JavaMaster",
    "score": 4200,
    "maxStage": 3,
    "result": "WIN"
  }
]
```

---

## 🎨 UI/UX 특징

### 색상 팔레트
```css
--bg:      #0a0e1a  (진한 네이비 - 배경)
--accent:  #6ee7f7  (밝은 시안 - 강조)
--gold:    #fbbf24  (금색 - 특수 효과)
--red:     #f87171  (빨강 - 경고/피해)
--green:   #34d399  (초록 - 긍정/회복)
```

### 애니메이션
| 애니메이션 | 효과 | 사용처 |
|----------|------|-------|
| `shake` | 450ms 진동 | 보스 피해 입음 |
| `playerHurt` | 400ms 흔들림 | 플레이어 피해 입음 |
| `floatUp` | 1s 위로 떠오름 | 데미지 표시 |
| `comboAppear` | 300ms 확대 | 콤보 배지 표시 |
| `slideUp` | 250ms 슬라이드 | 피드백 모달 |

### 반응형 디자인
```css
모바일 (max-width: 600px):
- 1 칼럼 레이아웃 (전투 영역)
- 1 칼럼 선택지 (객관식)
- 수직 정렬 통계

데스크톱:
- 2 칼럼 레이아웃 (플레이어 vs 보스)
- 2x2 선택지 그리드
- 수평 정렬 통계
```

---

## 🐛 문제 해결

### 백엔드 연결 실패
```
에러: "서버에 연결할 수 없습니다. 백엔드(8080) 실행을 확인해주세요."

해결:
1. 백엔드 서버가 실행 중인지 확인
2. http://localhost:8080 접속 가능한지 테스트
3. CORS 설정 확인
4. 네트워크 연결 상태 확인
```

### 게임이 느려질 때
```
원인: 로컬 저장소, 브라우저 캐시
해결:
1. 개발자 도구 → 캐시 삭제
2. 브라우저 재시작
3. 다른 브라우저 시도
4. 백그라운드 실행 중인 탭 종료
```

---

## 📊 기술 통계

```
프로젝트 규모:
├── HTML: ~900 줄
├── CSS: ~600 줄
├── JavaScript: ~850 줄
└── 총합: ~2,350 줄

주요 함수:
├── startGame() - 게임 초기화
├── loadNextQuestion() - 문제 로드
├── processAnswer() - 답변 처리
├── updateTimerDisplay() - 타이머 갱신
├── showFeedback() - 피드백 표시
├── updatePlayerHpDisplay() - HP 표시
└── showEndScreen() - 게임 종료

API 호출:
├── /start - 1회 (게임 시작)
├── /question - 12회 (3스테이지 × 4문제)
├── /answer - 12회 (답변 제출)
└── /ranking - N회 (사용자 요청)
```

---

## 🤝 기여 방법

```bash
# 1. 저장소 포크
git clone https://github.com/your-username/java-RPG-game.git

# 2. 기능 브랜치 생성
git checkout -b feature/새로운-기능

# 3. 변경 사항 커밋
git add .
git commit -m "feat: 새로운 기능 추가"

# 4. 브랜치 푸시
git push origin feature/새로운-기능

# 5. Pull Request 생성



**Happy Coding! 🚀 Java 마스터를 향해 화이팅! ⚔️**
