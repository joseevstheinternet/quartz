---
found: "[[02. 글자 크기 2포인트가 바꾼 것들]]"
date: 2026-02-27
---
색과 타이포그래피를 배우기 전까지, 나는 이 둘을 '분위기를 만드는 도구'라고 생각했다.

수업을 듣고 나서 관점이 바뀌었다. 색과 타이포그래피는 **구조**를 만드는 도구다. 무엇이 먼저 보일지, 어떤 순서로 읽힐지 — 그걸 결정하는 것이 이 둘이다.

---

### 컬러의 역할: 감정보다 먼저 '신호'

컬러는 감정을 전달하기도 하지만, UI에서는 그보다 먼저 **신호**로 작동한다. 
버튼이 빨갛다면 '위험' 또는 '삭제'. 초록이라면 '완료' 또는 '안전'. 사용자는 글을 읽기 전에 색으로 먼저 판단한다.

그래서 컬러 팔레트를 만들 때는 '예쁜 조합'보다 **대비(contrast)** 와 **역할 분리**가 먼저다.

<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <!-- Primary -->
  <rect x="20" y="30" width="140" height="90" rx="10" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="90" y="68" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">Primary</text>
  <text x="90" y="88" text-anchor="middle" font-size="11" fill="#534AB7">브랜드 컬러</text>
  <text x="90" y="106" text-anchor="middle" font-size="11" fill="#534AB7">핵심 행동 유도</text>

  <line x1="162" y1="75" x2="188" y2="75" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Secondary -->
  <rect x="190" y="40" width="130" height="70" rx="10" fill="#E1F5EE" stroke="#1D9E75" stroke-width="1"/>
  <text x="255" y="72" text-anchor="middle" font-size="13" font-weight="600" fill="#04342C">Secondary</text>
  <text x="255" y="90" text-anchor="middle" font-size="11" fill="#0F6E56">보조·강조</text>

  <line x1="322" y1="75" x2="348" y2="75" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Neutral -->
  <rect x="350" y="40" width="130" height="70" rx="10" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="415" y="72" text-anchor="middle" font-size="13" font-weight="600" fill="#2C2C2A">Neutral</text>
  <text x="415" y="90" text-anchor="middle" font-size="11" fill="#5F5E5A">배경·텍스트</text>

  <line x1="482" y1="75" x2="508" y2="75" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Semantic -->
  <rect x="510" y="30" width="110" height="90" rx="10" fill="#FCEBEB" stroke="#E24B4A" stroke-width="1"/>
  <text x="565" y="62" text-anchor="middle" font-size="13" font-weight="600" fill="#A32D2D">Semantic</text>
  <text x="565" y="80" text-anchor="middle" font-size="11" fill="#791F1F">성공·경고</text>
  <text x="565" y="98" text-anchor="middle" font-size="11" fill="#791F1F">오류·정보</text>
</svg>

---

### 타이포그래피의 역할: 읽는 순서를 설계한다

타이포그래피는 단순히 폰트를 고르는 일이 아니다. **크기, 굵기, 여백, 색상**의 조합으로 '이걸 먼저 읽어라'는 신호를 만드는 일이다.

이걸 **하이라키(Hierarchy)** 라고 부른다. 화면에서 정보의 우선순위를 시각적으로 표현하는 구조다.

<svg width="100%" viewBox="0 0 640 230" xmlns="http://www.w3.org/2000/svg">
  <!-- 배경 카드 -->
  <rect x="20" y="20" width="290" height="190" rx="10" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="40" y="50" font-size="10" fill="#888780">계층 구조 없음 ✗</text>
  <text x="40" y="78" font-size="14" fill="#2C2C2A">제목입니다</text>
  <text x="40" y="103" font-size="13" fill="#2C2C2A">소제목입니다</text>
  <text x="40" y="128" font-size="12" fill="#2C2C2A">본문 내용이 들어갑니다</text>
  <text x="40" y="153" font-size="12" fill="#2C2C2A">보조 설명 텍스트</text>
  <text x="40" y="185" font-size="11" fill="#888780">크기가 비슷해서 뭐가 중요한지 모름</text>

  <!-- 개선된 카드 -->
  <rect x="330" y="20" width="290" height="190" rx="10" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="350" y="50" font-size="10" fill="#534AB7">계층 구조 있음 ✓</text>
  <text x="350" y="82" font-size="20" font-weight="700" fill="#26215C">제목입니다</text>
  <text x="350" y="107" font-size="14" font-weight="600" fill="#3C3489">소제목입니다</text>
  <text x="350" y="130" font-size="12" fill="#534AB7">본문 내용이 들어갑니다</text>
  <text x="350" y="152" font-size="11" fill="#7F77DD">보조 설명 텍스트</text>
  <text x="350" y="185" font-size="11" fill="#534AB7">크기·굵기·색으로 순서가 명확함</text>
</svg>

---

### 타이포그래피의 7가지 공식 (요약)

좋은 디지털 타이포그래피를 만드는 기본 원칙들이다.

<svg width="100%" viewBox="0 0 640 310" xmlns="http://www.w3.org/2000/svg">
  <!-- 1 -->
  <rect x="20" y="15" width="185" height="64" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.8"/>
  <text x="36" y="38" font-size="11" font-weight="600" fill="#0C447C">① 크기로 위계를 만든다</text>
  <text x="36" y="56" font-size="10" fill="#185FA5">제목-소제목-본문 크기 차이</text>
  <text x="36" y="70" font-size="10" fill="#185FA5">최소 2pt 이상 차이를 둔다</text>

  <!-- 2 -->
  <rect x="225" y="15" width="185" height="64" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.8"/>
  <text x="241" y="38" font-size="11" font-weight="600" fill="#0C447C">② 굵기로 강조한다</text>
  <text x="241" y="56" font-size="10" fill="#185FA5">Regular / Medium / Bold</text>
  <text x="241" y="70" font-size="10" fill="#185FA5">2단계 이상 차이를 두면 명확</text>

  <!-- 3 -->
  <rect x="430" y="15" width="190" height="64" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.8"/>
  <text x="446" y="38" font-size="11" font-weight="600" fill="#0C447C">③ 색으로 보조한다</text>
  <text x="446" y="56" font-size="10" fill="#185FA5">주요 텍스트는 진하게</text>
  <text x="446" y="70" font-size="10" fill="#185FA5">보조 텍스트는 회색으로</text>

  <!-- 4 -->
  <rect x="20" y="100" width="185" height="64" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="0.8"/>
  <text x="36" y="123" font-size="11" font-weight="600" fill="#27500A">④ 줄 간격은 1.5~1.7배</text>
  <text x="36" y="141" font-size="10" fill="#3B6D11">너무 좁으면 답답, 너무 넓으면</text>
  <text x="36" y="155" font-size="10" fill="#3B6D11">연결이 끊긴 느낌이 난다</text>

  <!-- 5 -->
  <rect x="225" y="100" width="185" height="64" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="0.8"/>
  <text x="241" y="123" font-size="11" font-weight="600" fill="#27500A">⑤ 한 줄 최대 60~80자</text>
  <text x="241" y="141" font-size="10" fill="#3B6D11">너무 길면 눈이 다음 줄</text>
  <text x="241" y="155" font-size="10" fill="#3B6D11">시작점을 찾기 어렵다</text>

  <!-- 6 -->
  <rect x="430" y="100" width="190" height="64" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="0.8"/>
  <text x="446" y="123" font-size="11" font-weight="600" fill="#27500A">⑥ 폰트 종류는 2개 이하</text>
  <text x="446" y="141" font-size="10" fill="#3B6D11">제목용 serif + 본문용 sans</text>
  <text x="446" y="155" font-size="10" fill="#3B6D11">조합이 기본. 3개 이상은 혼잡</text>

  <!-- 7 -->
  <rect x="120" y="190" width="400" height="64" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="0.8"/>
  <text x="320" y="213" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">⑦ 정렬은 일관되게</text>
  <text x="320" y="231" text-anchor="middle" font-size="10" fill="#633806">왼쪽 정렬이 기본. 가운데 정렬은 짧은 제목·슬로건에만.</text>
  <text x="320" y="246" text-anchor="middle" font-size="10" fill="#633806">섞어 쓰면 화면이 흔들려 보인다</text>
</svg>

---


> [!tip]
> 색은 감정을, 타이포그래피는 순서를 만든다. UI 디자인은 결국 "사용자가 어떤 순서로 화면을 읽게 할 것인가"를 설계하는 일이다.