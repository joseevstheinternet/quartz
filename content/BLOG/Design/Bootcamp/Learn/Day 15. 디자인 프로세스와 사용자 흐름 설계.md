---
date: 2026-03-19
---
좋은 UI를 만들기 위해서는 화면을 예쁘게 꾸미는 것보다 사용자의 문제를 제대로 이해하고 검증하는 과정이 먼저다. 오늘은 수면 앱을 예시로 디자인 프로세스 4단계를 배웠다.

---

### 디자인 프로세스 4단계

<svg width="100%" viewBox="0 0 640 100" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="10" y="20" width="130" height="56" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="75" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">① 사용자 요구 분석</text>
  <text x="75" y="64" text-anchor="middle" font-size="10" fill="#712B13">무엇이 불편해?</text>
  <line x1="142" y1="48" x2="165" y2="48" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="167" y="20" width="130" height="56" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="232" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">② 와이어프레임</text>
  <text x="232" y="64" text-anchor="middle" font-size="10" fill="#633806">뼈대 그리기</text>
  <line x1="299" y1="48" x2="322" y2="48" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="324" y="20" width="130" height="56" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="389" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">③ UI 스타일 가이드</text>
  <text x="389" y="64" text-anchor="middle" font-size="10" fill="#3B6D11">외형 통일하기</text>
  <line x1="456" y1="48" x2="479" y2="48" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="481" y="20" width="150" height="56" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="556" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#3C3489">④ 프로토타입 제작</text>
  <text x="556" y="64" text-anchor="middle" font-size="10" fill="#534AB7">진짜처럼 눌러 보기</text>
</svg>

---

### 1단계 — 사용자 요구 분석

문제를 정의하기 전에 먼저 사용자를 만나야 한다. 수면 앱 예시에서는 밤마다 잠드는 시간이 들쑥날쑥해서 피곤하다는 20대 직장인 8명을 인터뷰했다. 동시에 앱스토어에서 인기 수면 관리 앱 5개의 기능을 비교 분석했다.

이 두 가지를 종합한 결과 "취침 30분 전 알림 + 수면 점수 시각화"가 가장 필요한 기능으로 정리되었다. 직관이 아니라 데이터로 문제를 정의하는 것이다.

---

### 2단계 — 와이어프레임 작성

문제가 정의되면 뼈대를 먼저 그린다. 홈 → 알림 세팅 → 수면 기록 보기, 3단계 사용자 플로우를 스케치한 뒤 피그마로 박스와 회색 톤만 사용해 6개 화면을 빠르게 제작한다. 이 단계에서 팀 동료 3명이 직접 클릭해 보며 "버튼 위치가 헷갈린다"는 피드백을 받는다.

Lo-fi 단계에서 구조적인 문제를 잡아야 나중에 수정 비용이 적다. DAY 8에서 배운 내용이 여기서 그대로 연결된다.

---

### 3단계 — UI 스타일 가이드

구조가 잡히면 외형을 통일한다. 수면 앱 예시에서는 인디고 + 라벤더 2색 팔레트와 Noto Sans 서체를 결정했다. 둥근 카드와 그림자 2dp로 일관된 높이감을 설정하고, 색 대비도 체크했다. 배경 `#1a1a2e`에 글자 `#ffffff`로 WCAG AA 기준을 통과시켰다.

접근성(Accessibility) 기준인 **WCAG**는 텍스트가 배경 대비 충분히 잘 보이는지를 수치로 검증하는 기준이다. 예뻐 보이는 색 조합이 실제로 읽기 어려운 경우가 있기 때문에, 스타일 가이드 단계에서 반드시 확인해야 한다.

---

### 4단계 — 프로토타입 제작과 테스트

하이파이 화면에 슬라이드 전환과 프로그레스 애니메이션을 추가해 실제처럼 작동하도록 만든다. 그다음 목표 사용자 5명에게 TestFlight로 배포해서 SUS(System Usability Scale) 설문을 진행했고, 평균 78점을 받았다.

테스트 결과에서 "아침 리포트 화면 스크롤이 길다"는 지적이 나왔고, 다시 2단계 와이어프레임으로 돌아가 개선했다. 디자인 프로세스는 순서대로 진행하고 끝나는 게 아니라 피드백을 받으면 이전 단계로 돌아가서 반복하는 구조다.

<svg width="100%" viewBox="0 0 640 120" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr2" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#639922" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
    <marker id="arr3" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#E24B4A" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="20" y="30" width="120" height="44" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="80" y="57" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">분석 → 설계</text>
  <line x1="142" y1="52" x2="168" y2="52" stroke="#639922" stroke-width="1" marker-end="url(#arr2)"/>

  <rect x="170" y="30" width="120" height="44" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="230" y="57" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">제작 → 테스트</text>
  <line x1="292" y1="52" x2="318" y2="52" stroke="#639922" stroke-width="1" marker-end="url(#arr2)"/>

  <rect x="320" y="30" width="120" height="44" rx="8" fill="#FCEBEB" stroke="#E24B4A" stroke-width="1"/>
  <text x="380" y="50" text-anchor="middle" font-size="11" font-weight="600" fill="#A32D2D">피드백 발견</text>
  <text x="380" y="66" text-anchor="middle" font-size="10" fill="#791F1F">"스크롤이 길다"</text>

  <path d="M380 74 Q380 100 230 100 Q130 100 130 74" fill="none" stroke="#E24B4A" stroke-width="1" stroke-dasharray="4 3" marker-end="url(#arr3)"/>
  <text x="255" y="97" text-anchor="middle" font-size="10" fill="#E24B4A">이전 단계로 돌아가 개선</text>
</svg>

---

### 피그마 플러그인 추천

작업 속도를 높여 주는 플러그인들이다.

| 플러그인 | 용도 |
|---|---|
| Unsplash | 고퀄리티 무료 이미지 바로 삽입 |
| Iconify | 수천 개 아이콘을 피그마에서 바로 사용 |
| Material Design Icons | 구글 Material Design 아이콘 |
| 3Dicons | 3D 아이콘 제작 |
| Content Reel | 더미 텍스트 및 데이터 제공 |
| Lorem Ipsum | 더미 텍스트 제공 |
| Design Doc [Spectral] | 디자인 작업 문서화 지원 |
| Auto flow | 두 프레임 사이를 자동으로 화살표로 연결 |
| Wireframe designer | 와이어프레임을 빠르고 쉽게 제작 |
| Figmap - Map maker | 지도 기반 디자인 구현 |
| html.to.design | 실제 웹사이트 HTML을 피그마 디자인으로 자동 변환 |

---

> [!tip]
> 디자인 프로세스는 순서대로 진행하고 끝나는 게 아니다. 피드백이 나오면 이전 단계로 돌아가는 것이 맞는 방향이다.

여기에서 오늘의 실습 내용을 볼 수 있어요! [[13. 에어비앤비를 뜯어 만들면서 배운 것]]