---
date: 2026-03-23
---
DAY 16에서 아토믹 디자인의 개념을 배웠다면, DAY 17에서는 그 구조를 실제로 피그마에서 어떻게 구현하는지, 특히 디자인 토큰을 어떻게 관리하는지를 깊이 다루었다.

---

### 디자인 토큰을 더 깊게

디자인 토큰은 단순히 색상 코드를 변수로 저장하는 것을 넘어선다. 잘 설계된 토큰 시스템은 계층 구조를 갖는다.

<svg width="100%" viewBox="0 0 640 180" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>

  <!-- Global Token -->
  <rect x="20" y="20" width="175" height="130" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="107" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">Global Token</text>
  <text x="107" y="68" text-anchor="middle" font-size="11" fill="#5F5E5A">raw 값 그대로 저장</text>
  <text x="107" y="88" text-anchor="middle" font-size="10" fill="#888780">blue-500: #3B82F6</text>
  <text x="107" y="104" text-anchor="middle" font-size="10" fill="#888780">space-4: 16px</text>
  <text x="107" y="120" text-anchor="middle" font-size="10" fill="#888780">font-size-md: 16px</text>
  <text x="107" y="140" text-anchor="middle" font-size="10" fill="#888780">의미 없는 이름</text>
  <line x1="197" y1="85" x2="223" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Alias Token -->
  <rect x="225" y="20" width="175" height="130" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="312" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">Alias Token</text>
  <text x="312" y="68" text-anchor="middle" font-size="11" fill="#185FA5">역할 기반 이름</text>
  <text x="312" y="88" text-anchor="middle" font-size="10" fill="#378ADD">color-primary: blue-500</text>
  <text x="312" y="104" text-anchor="middle" font-size="10" fill="#378ADD">spacing-md: space-4</text>
  <text x="312" y="120" text-anchor="middle" font-size="10" fill="#378ADD">text-body: font-size-md</text>
  <text x="312" y="140" text-anchor="middle" font-size="10" fill="#378ADD">의미 있는 이름</text>
  <line x1="402" y1="85" x2="428" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Component Token -->
  <rect x="430" y="20" width="185" height="130" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="522" y="48" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">Component Token</text>
  <text x="522" y="68" text-anchor="middle" font-size="11" fill="#534AB7">컴포넌트 전용</text>
  <text x="522" y="88" text-anchor="middle" font-size="10" fill="#7F77DD">btn-bg: color-primary</text>
  <text x="522" y="104" text-anchor="middle" font-size="10" fill="#7F77DD">btn-padding: spacing-md</text>
  <text x="522" y="120" text-anchor="middle" font-size="10" fill="#7F77DD">btn-label: text-body</text>
  <text x="522" y="140" text-anchor="middle" font-size="10" fill="#7F77DD">컴포넌트 맥락</text>
</svg>

토큰이 이렇게 계층화되어 있으면 나중에 테마가 바뀌거나 다크 모드를 추가할 때, Global Token의 값만 바꿔도 Alias → Component Token까지 자동으로 반영된다.

---

### 원자부터 페이지까지 — 실제 구성 예시

인스타그램을 아토믹 디자인으로 분석하면 이렇게 나뉜다. Brad Frost도 책에서 인스타그램을 예시로 들었는데, 피드 포스트 하나(유기체)가 아이콘 원자들, 텍스트 원자, 이미지 원자, 좋아요/댓글 분자들로 구성되어 있다. 그리고 이 유기체가 반복되면서 무한 스크롤 피드가 만들어지는 구조다.

<svg width="100%" viewBox="0 0 640 200" xmlns="http://www.w3.org/2000/svg">
  <!-- 원자들 -->
  <rect x="20" y="20" width="130" height="160" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="85" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">원자</text>
  <rect x="35" y="56" width="100" height="18" rx="4" fill="#F0997B"/>
  <text x="85" y="70" text-anchor="middle" font-size="9" fill="#4A1B0C">하트 아이콘</text>
  <rect x="35" y="82" width="100" height="18" rx="4" fill="#F0997B"/>
  <text x="85" y="96" text-anchor="middle" font-size="9" fill="#4A1B0C">댓글 아이콘</text>
  <rect x="35" y="108" width="100" height="18" rx="4" fill="#F0997B"/>
  <text x="85" y="122" text-anchor="middle" font-size="9" fill="#4A1B0C">사용자 이름</text>
  <rect x="35" y="134" width="100" height="18" rx="4" fill="#F0997B"/>
  <text x="85" y="148" text-anchor="middle" font-size="9" fill="#4A1B0C">이미지</text>
  <rect x="35" y="160" width="100" height="14" rx="4" fill="#F0997B"/>
  <text x="85" y="171" text-anchor="middle" font-size="9" fill="#4A1B0C">아바타</text>

  <!-- 분자들 -->
  <rect x="170" y="20" width="130" height="160" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="235" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">분자</text>
  <rect x="185" y="56" width="100" height="28" rx="4" fill="#EF9F27"/>
  <text x="235" y="74" text-anchor="middle" font-size="9" fill="#412402">액션바</text>
  <text x="235" y="84" text-anchor="middle" font-size="8" fill="#633806">(하트+댓글+공유)</text>
  <rect x="185" y="96" width="100" height="28" rx="4" fill="#EF9F27"/>
  <text x="235" y="114" text-anchor="middle" font-size="9" fill="#412402">사용자 헤더</text>
  <text x="235" y="124" text-anchor="middle" font-size="8" fill="#633806">(아바타+이름)</text>
  <rect x="185" y="136" width="100" height="28" rx="4" fill="#EF9F27"/>
  <text x="235" y="154" text-anchor="middle" font-size="9" fill="#412402">캡션 영역</text>
  <text x="235" y="164" text-anchor="middle" font-size="8" fill="#633806">(이름+텍스트)</text>

  <!-- 유기체 -->
  <rect x="320" y="20" width="130" height="160" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1.5"/>
  <text x="385" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">유기체</text>
  <rect x="335" y="56" width="100" height="112" rx="4" fill="#C0DD97" stroke="#3B6D11" stroke-width="0.5"/>
  <text x="385" y="108" text-anchor="middle" font-size="10" font-weight="600" fill="#173404">피드 포스트</text>
  <text x="385" y="124" text-anchor="middle" font-size="8" fill="#27500A">사용자 헤더</text>
  <text x="385" y="136" text-anchor="middle" font-size="8" fill="#27500A">+ 이미지</text>
  <text x="385" y="148" text-anchor="middle" font-size="8" fill="#27500A">+ 액션바</text>
  <text x="385" y="160" text-anchor="middle" font-size="8" fill="#27500A">+ 캡션</text>

  <!-- 페이지 -->
  <rect x="470" y="20" width="150" height="160" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="545" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#3C3489">페이지</text>
  <rect x="485" y="56" width="120" height="38" rx="4" fill="#AFA9EC"/>
  <text x="545" y="78" text-anchor="middle" font-size="9" fill="#26215C">피드 포스트 1</text>
  <rect x="485" y="98" width="120" height="38" rx="4" fill="#AFA9EC"/>
  <text x="545" y="120" text-anchor="middle" font-size="9" fill="#26215C">피드 포스트 2</text>
  <rect x="485" y="140" width="120" height="30" rx="4" fill="#CEC BF6"/>
  <text x="545" y="159" text-anchor="middle" font-size="9" fill="#26215C">피드 포스트 3...</text>
</svg>

---

### 아토믹 디자인은 선형 프로세스가 아니다

중요한 오해가 하나 있다. 아토믹 디자인을 "1단계: 원자 만들기 → 2단계: 분자 만들기 → 3단계: 유기체 만들기"처럼 순서대로 따라가는 프로세스로 생각하면 안 된다는 것이다.

실제로는 페이지를 먼저 설계하면서 어떤 유기체가 필요한지 파악하고, 유기체를 만들면서 어떤 분자가 필요한지 정의하고, 분자를 만들면서 어떤 원자가 필요한지 발견하는 방식으로 진행된다. 위아래를 동시에 오가면서 설계하는 것이 자연스럽다.

> [!tip]
> 아토믹 디자인의 진짜 가치는 명칭 체계에 있는 게 아니라, UI를 부분과 전체로 동시에 생각하게 만드는 사고 방식에 있다.

