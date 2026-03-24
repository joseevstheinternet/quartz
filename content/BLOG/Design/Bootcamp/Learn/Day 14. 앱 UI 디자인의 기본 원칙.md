---
date: 2026-03-18
---
앱 UI 디자인에서 중요한 원칙 세 가지와, 실제 앱 화면이 어떻게 구성되는지를 배웠다.

---

### 원칙 1: 사용자 중심 디자인

디자인은 디자이너를 위한 것이 아니라 사용자에게 의미가 있어야 한다. 사용자의 목표, 행동, 감정을 깊이 이해하고 반영하는 것이 핵심이다. 기능보다 사용 경험을 우선하는 사고방식이 필요하다.

**에어비앤비**가 대표적인 사례다. 에어비앤비의 UI는 단순히 숙소를 검색하고 예약하는 기능을 담는 것을 넘어서, 여행에 대한 설렘과 신뢰를 화면에 담아내는 방식으로 설계되어 있다. 기능이 같아도 경험이 다르면 사용자가 느끼는 것이 달라진다.

---

### 원칙 2: 시각적 계층 구조 (Visual Hierarchy)

"사용자가 어디를 먼저 봐야 할지 자연스럽게 알 수 있어야 한다."

정보는 중요도에 따라 크기, 색상, 배치로 구분되어야 한다. 강약 조절이 되어야 사용자 흐름이 매끄럽게 흘러간다. DAY 2에서 타이포그래피로 위계를 만드는 법을 배웠는데, 그게 화면 전체로 확장된 개념이다.

**유튜브**가 좋은 사례다. 썸네일 크기, 제목 굵기, 채널명과 조회수의 크기 차이가 자연스럽게 "이것부터 봐라"는 신호를 만들어 낸다.

<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <!-- 계층 없는 경우 -->
  <rect x="20" y="20" width="270" height="120" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="40" y="48" font-size="10" fill="#888780">계층 구조 없음 ✗</text>
  <rect x="40" y="58" width="180" height="14" rx="3" fill="#B4B2A9"/>
  <rect x="40" y="78" width="160" height="12" rx="3" fill="#B4B2A9"/>
  <rect x="40" y="96" width="170" height="12" rx="3" fill="#B4B2A9"/>
  <rect x="40" y="114" width="150" height="12" rx="3" fill="#B4B2A9"/>
  <text x="155" y="148" text-anchor="middle" font-size="10" fill="#888780">모든 정보가 같은 크기</text>

  <!-- 계층 있는 경우 -->
  <rect x="350" y="20" width="270" height="120" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="370" y="48" font-size="10" fill="#534AB7">계층 구조 있음 ✓</text>
  <rect x="370" y="56" width="200" height="20" rx="3" fill="#3C3489"/>
  <rect x="370" y="84" width="160" height="13" rx="3" fill="#7F77DD"/>
  <rect x="370" y="103" width="140" height="10" rx="3" fill="#AFA9EC"/>
  <rect x="370" y="119" width="120" height="8" rx="3" fill="#CEC BF6"/>
  <text x="485" y="152" text-anchor="middle" font-size="10" fill="#534AB7">크기 차이로 우선순위가 명확함</text>
</svg>

---

### 원칙 3: 일관성

한 번 배운 사용 방식이 앱 전체에서 통하게 만드는 것이다. 버튼 스타일, 폰트, 색상, 아이콘의 의미 등이 앱 전체에서 일관성 있게 반복되어야 한다. 익숙함이 생기면 사용자는 더 빠르고 편하게 앱을 사용할 수 있다.

**인스타그램**이 대표적이다. 하트는 좋아요, 말풍선은 댓글, 화살표는 공유. 어떤 화면에 가도 이 아이콘들은 항상 같은 의미로 쓰인다. 앱 안의 버튼을 누를 때 다른 화면의 버튼들과 똑같은 룰을 따르고 있는지 확인해 보는 습관이 필요하다.

<svg width="100%" viewBox="0 0 640 120" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="180" height="80" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="110" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">버튼 스타일</text>
  <text x="110" y="66" text-anchor="middle" font-size="11" fill="#3B6D11">크기·색상·radius가</text>
  <text x="110" y="82" text-anchor="middle" font-size="11" fill="#3B6D11">모든 화면에서 동일</text>

  <rect x="230" y="20" width="180" height="80" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="320" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">아이콘 의미</text>
  <text x="320" y="66" text-anchor="middle" font-size="11" fill="#3B6D11">하트 = 좋아요</text>
  <text x="320" y="82" text-anchor="middle" font-size="11" fill="#3B6D11">어디서나 동일하게</text>

  <rect x="440" y="20" width="180" height="80" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="530" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">타이포·컬러</text>
  <text x="530" y="66" text-anchor="middle" font-size="11" fill="#3B6D11">서체·색상 규칙이</text>
  <text x="530" y="82" text-anchor="middle" font-size="11" fill="#3B6D11">앱 전체에서 유지</text>
</svg>

---

### 앱 화면의 종류: 온보딩

앱을 처음 설치했을 때 사용자를 환영하고 핵심 기능을 소개하는 화면이다. 슬라이드 형식의 설명, 로그인/회원가입 유도, 일러스트나 아이콘으로 직관적으로 이해할 수 있게 구성하는 것이 기본이다.

좋은 온보딩을 분석할 때 체크할 포인트는 세 가지다. 메시지가 명확한가, 지나치게 길거나 복잡하지 않은가, 스킵 기능이 있는가. 듀오링고가 좋은 사례로 꼽힌다.

---

### 앱 화면의 주요 구성 요소

화면 하나는 크게 세 영역으로 나뉜다.

<svg width="100%" viewBox="0 0 640 220" xmlns="http://www.w3.org/2000/svg">
  <!-- 모바일 프레임 -->
  <rect x="220" y="10" width="200" height="200" rx="16" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1.5"/>

  <!-- 헤더 -->
  <rect x="220" y="10" width="200" height="44" rx="16" fill="#3C3489" stroke="none"/>
  <rect x="220" y="38" width="200" height="16" rx="0" fill="#3C3489" stroke="none"/>
  <text x="320" y="37" text-anchor="middle" font-size="11" font-weight="600" fill="#EEEDFE">헤더 (Header)</text>

  <!-- 메인 콘텐츠 -->
  <rect x="228" y="58" width="184" height="108" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <text x="320" y="108" text-anchor="middle" font-size="11" font-weight="600" fill="#0C447C">메인 콘텐츠 영역</text>
  <text x="320" y="124" text-anchor="middle" font-size="10" fill="#185FA5">사용자가 가장 자주</text>
  <text x="320" y="138" text-anchor="middle" font-size="10" fill="#185FA5">상호작용하는 영역</text>

  <!-- 푸터 -->
  <rect x="220" y="166" width="200" height="44" rx="0" fill="#534AB7" stroke="none"/>
  <rect x="220" y="166" width="200" height="16" rx="0" fill="#534AB7" stroke="none"/>
  <rect x="220" y="178" width="200" height="32" rx="16" fill="#534AB7" stroke="none"/>
  <text x="320" y="198" text-anchor="middle" font-size="11" font-weight="600" fill="#EEEDFE">푸터 (Footer)</text>

  <!-- 설명 레이블 -->
  <text x="30" y="38" font-size="11" fill="#3C3489" font-weight="600">타이틀 + 네비게이션</text>
  <line x1="218" y1="32" x2="130" y2="32" stroke="#B4B2A9" stroke-width="0.8"/>

  <text x="30" y="118" font-size="11" fill="#185FA5" font-weight="600">핵심 콘텐츠</text>
  <line x1="218" y1="112" x2="90" y2="112" stroke="#B4B2A9" stroke-width="0.8"/>

  <text x="30" y="198" font-size="11" fill="#534AB7" font-weight="600">하단 내비게이션</text>
  <line x1="218" y1="192" x2="138" y2="192" stroke="#B4B2A9" stroke-width="0.8"/>

  <text x="460" y="198" font-size="10" fill="#888780">네이버가 좋은 사례</text>
</svg>

---

> [!tip]
> 사용자 중심 디자인, 시각적 계층 구조, 일관성. 이 세 가지가 잘 갖춰지면 사용자는 앱을 배우지 않아도 자연스럽게 쓸 수 있게 된다.

여기에서 오늘의 실습 내용을 볼 수 있어요! [[13. 에어비앤비를 뜯어 만들면서 배운 것]]