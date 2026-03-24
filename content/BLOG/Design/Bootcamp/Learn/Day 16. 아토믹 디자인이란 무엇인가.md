---
date: 2026-03-20
---
Brad Frost의 [Atomic Design](https://atomicdesign.bradfrost.com/chapter-2/)에서 시작된 개념이다. 우주의 모든 물질이 원자로 나뉘듯, 인터페이스도 같은 방식으로 쪼갤 수 있다는 아이디어에서 출발했다. 디자인도 개발처럼 모듈화되어야 한다는 것이 핵심 철학이다.

---

### 전체 구조 한눈에 보기

<svg width="100%" viewBox="0 0 640 72" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="4"   y="16" width="88" height="40" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="48"  y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">디자인 토큰</text>
  <line x1="94"  y1="36" x2="108" y2="36" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="110" y="16" width="80" height="40" rx="6" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="150" y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">원자</text>
  <line x1="192" y1="36" x2="206" y2="36" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="208" y="16" width="80" height="40" rx="6" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="248" y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">분자</text>
  <line x1="290" y1="36" x2="304" y2="36" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="306" y="16" width="80" height="40" rx="6" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="346" y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">유기체</text>
  <line x1="388" y1="36" x2="402" y2="36" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="404" y="16" width="80" height="40" rx="6" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="444" y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#0C447C">템플릿</text>
  <line x1="486" y1="36" x2="500" y2="36" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="502" y="16" width="132" height="40" rx="6" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="568" y="41" text-anchor="middle" font-size="11" font-weight="600" fill="#3C3489">페이지</text>
</svg>

---

### 0. 디자인 토큰 — 원자보다 더 작은 단위

타이포그래피, 색상, 여백 같은 디자인의 기본 재료에 이름을 붙여 변수로 관리하는 것이다. `#3B82F6` 같은 색상 코드 대신 `color-primary`라는 이름으로 저장해 두면, 나중에 브랜드 컬러가 바뀔 때 이 값 하나만 수정해도 토큰을 사용하는 모든 원자·분자·유기체가 자동으로 바뀐다.

<svg width="100%" viewBox="0 0 640 130" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="180" height="100" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="110" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">색상 토큰</text>
  <rect x="36" y="54" width="20" height="20" rx="4" fill="#3C3489"/>
  <text x="64" y="69" font-size="10" fill="#5F5E5A">color-primary</text>
  <rect x="36" y="80" width="20" height="20" rx="4" fill="#E24B4A"/>
  <text x="64" y="95" font-size="10" fill="#5F5E5A">color-danger</text>
  <rect x="36" y="106" width="20" height="20" rx="4" fill="#639922"/>
  <text x="64" y="121" font-size="10" fill="#5F5E5A">color-success</text>

  <rect x="230" y="15" width="180" height="100" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="320" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">간격 토큰</text>
  <text x="246" y="68" font-size="10" fill="#5F5E5A">spacing-xs  →  4px</text>
  <text x="246" y="86" font-size="10" fill="#5F5E5A">spacing-sm  →  8px</text>
  <text x="246" y="104" font-size="10" fill="#5F5E5A">spacing-md  →  16px</text>
  <text x="246" y="122" font-size="10" fill="#5F5E5A">spacing-lg  →  24px</text>

  <rect x="440" y="15" width="180" height="100" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="530" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">타이포 토큰</text>
  <text x="456" y="68" font-size="10" fill="#5F5E5A">text-xs  →  12px</text>
  <text x="456" y="86" font-size="10" fill="#5F5E5A">text-sm  →  14px</text>
  <text x="456" y="104" font-size="10" fill="#5F5E5A">text-md  →  16px</text>
  <text x="456" y="122" font-size="10" fill="#5F5E5A">text-lg  →  20px</text>
</svg>

---

### 1. 원자 (Atoms) — 더 이상 쪼갤 수 없는 최소 단위

원자는 아토믹 디자인에서 가장 핵심적인 개념이다. 버튼을 반으로 나누면 버튼이 아닌 무의미한 조각이 된다. 이것이 원자의 정의다.

원자는 세 가지 핵심 특성을 갖는다. 첫째, 더 이상 쪼갤 수 없다. 둘째, 고유한 속성을 갖는다(색상, 크기, 상태 등). 셋째, 혼자서는 맥락이 없다. 버튼 하나만 있으면 "뭘 제출하는 버튼인지" 알 수 없다.

<svg width="100%" viewBox="0 0 640 180" xmlns="http://www.w3.org/2000/svg">
  <!-- 버튼 원자 -->
  <rect x="20" y="15" width="175" height="150" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="107" y="40" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">버튼 (Button)</text>

  <rect x="40" y="52" width="135" height="30" rx="6" fill="#3C3489"/>
  <text x="107" y="72" text-anchor="middle" font-size="11" font-weight="600" fill="#EEEDFE">Primary</text>

  <rect x="40" y="90" width="135" height="30" rx="6" fill="none" stroke="#3C3489" stroke-width="1.5"/>
  <text x="107" y="110" text-anchor="middle" font-size="11" font-weight="600" fill="#3C3489">Secondary</text>

  <rect x="40" y="128" width="135" height="30" rx="6" fill="#D3D1C7"/>
  <text x="107" y="148" text-anchor="middle" font-size="11" fill="#888780">Disabled</text>

  <!-- 입력창 원자 -->
  <rect x="215" y="15" width="175" height="150" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="302" y="40" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">입력창 (Input)</text>

  <rect x="235" y="52" width="135" height="30" rx="6" fill="none" stroke="#B4B2A9" stroke-width="1"/>
  <text x="255" y="72" font-size="10" fill="#B4B2A9">placeholder</text>

  <rect x="235" y="90" width="135" height="30" rx="6" fill="none" stroke="#3C3489" stroke-width="2"/>
  <text x="255" y="110" font-size="10" fill="#2C2C2A">입력 중...</text>

  <rect x="235" y="128" width="135" height="30" rx="6" fill="none" stroke="#E24B4A" stroke-width="1.5"/>
  <text x="255" y="148" font-size="10" fill="#E24B4A">오류 상태</text>

  <!-- 레이블 원자 -->
  <rect x="410" y="15" width="175" height="150" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="497" y="40" text-anchor="middle" font-size="11" font-weight="600" fill="#4A1B0C">레이블·텍스트</text>
  <text x="430" y="68" font-size="18" font-weight="700" fill="#2C2C2A">제목</text>
  <text x="430" y="92" font-size="14" font-weight="600" fill="#2C2C2A">소제목</text>
  <text x="430" y="114" font-size="12" fill="#2C2C2A">본문 텍스트</text>
  <text x="430" y="133" font-size="11" fill="#5F5E5A">보조 텍스트</text>
  <text x="430" y="151" font-size="10" fill="#888780">캡션</text>
</svg>

원자들을 한 곳에 모아둔 것이 **스타일 가이드** 혹은 **디자인 토큰**이다. 팀 전체가 같은 버튼, 같은 색상, 같은 폰트를 쓸 수 있도록 공통 재료 창고 역할을 한다.

---

### 2. 분자 (Molecules) — 원자가 모여 의미를 갖게 되는 단위

여러 원자가 결합해 하나의 기능을 갖는 단위다. 레이블 + 입력창 + 버튼이 합쳐지면 "검색 폼"이라는 의미가 생긴다. 원자는 분자가 될 때 진짜 쓸모가 생긴다.

<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr2" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#BA7517" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>

  <!-- 원자들 -->
  <rect x="20" y="30" width="70" height="28" rx="4" fill="#FAECE7" stroke="#D85A30" stroke-width="0.8"/>
  <text x="55" y="49" text-anchor="middle" font-size="10" fill="#4A1B0C">레이블</text>

  <rect x="20" y="68" width="70" height="28" rx="4" fill="#FAECE7" stroke="#D85A30" stroke-width="0.8"/>
  <text x="55" y="87" text-anchor="middle" font-size="10" fill="#4A1B0C">입력창</text>

  <rect x="20" y="106" width="70" height="28" rx="4" fill="#FAECE7" stroke="#D85A30" stroke-width="0.8"/>
  <text x="55" y="125" text-anchor="middle" font-size="10" fill="#4A1B0C">버튼</text>

  <line x1="92" y1="82" x2="116" y2="82" stroke="#BA7517" stroke-width="1.2" marker-end="url(#arr2)"/>

  <!-- 검색 폼 분자 -->
  <rect x="118" y="20" width="200" height="120" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1.5"/>
  <text x="218" y="42" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">검색 폼 (분자)</text>
  <text x="134" y="64" font-size="10" fill="#633806">검색어</text>
  <rect x="134" y="70" width="165" height="24" rx="4" fill="none" stroke="#B4B2A9" stroke-width="1"/>
  <text x="142" y="87" font-size="10" fill="#B4B2A9">입력하세요</text>
  <rect x="134" y="102" width="165" height="24" rx="4" fill="#3C3489"/>
  <text x="218" y="119" text-anchor="middle" font-size="10" font-weight="600" fill="#EEEDFE">검색</text>

  <!-- 사용자 카드 분자 -->
  <rect x="348" y="20" width="270" height="120" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1.5"/>
  <text x="483" y="42" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">사용자 카드 (분자)</text>
  <circle cx="385" cy="90" r="24" fill="#D3D1C7"/>
  <text x="385" y="95" text-anchor="middle" font-size="10" fill="#888780">아바타</text>
  <text x="420" y="78" font-size="12" font-weight="600" fill="#2C2C2A">홍길동</text>
  <text x="420" y="96" font-size="10" fill="#5F5E5A">Product Designer</text>
  <text x="420" y="112" font-size="10" fill="#888780">서울, 한국</text>
</svg>

분자를 만들 때 핵심은 **단일 책임 원칙**이다. 하나의 분자는 하나의 일만 잘해야 한다.

---

### 3. 유기체 (Organisms) — 독립적인 한 섹션

분자들과 원자들이 모여 페이지에서 독립적인 한 구역을 이루는 단위다. 헤더, 상품 그리드, 댓글 섹션처럼 그 자체로 독립적이어서 어느 페이지에 올려놔도 작동한다.

<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <!-- 헤더 유기체 -->
  <rect x="20" y="20" width="600" height="120" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1.5"/>
  <text x="320" y="44" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">헤더 (유기체)</text>

  <!-- 로고 분자 -->
  <rect x="40" y="56" width="80" height="40" rx="6" fill="#C0DD97" stroke="#3B6D11" stroke-width="0.8"/>
  <text x="80" y="80" text-anchor="middle" font-size="10" fill="#173404">로고 (분자)</text>

  <!-- 메뉴 분자 -->
  <rect x="240" y="56" width="260" height="40" rx="6" fill="#C0DD97" stroke="#3B6D11" stroke-width="0.8"/>
  <text x="290" y="76" font-size="10" fill="#173404">홈</text>
  <text x="330" y="76" font-size="10" fill="#173404">탐색</text>
  <text x="370" y="76" font-size="10" fill="#173404">저장</text>
  <text x="410" y="76" font-size="10" fill="#173404">프로필</text>
  <text x="310" y="90" text-anchor="middle" font-size="9" fill="#3B6D11">메뉴 (분자)</text>

  <!-- 검색 분자 -->
  <rect x="520" y="56" width="80" height="40" rx="6" fill="#C0DD97" stroke="#3B6D11" stroke-width="0.8"/>
  <text x="560" y="80" text-anchor="middle" font-size="10" fill="#173404">검색 (분자)</text>

  <text x="320" y="140" text-anchor="middle" font-size="10" fill="#3B6D11">로고 분자 + 메뉴 분자 + 검색 분자 → 헤더 유기체</text>
</svg>

---

### 4. 템플릿 (Templates) — 콘텐츠 없는 레이아웃 뼈대

유기체들을 레이아웃에 배치한 설계도다. 실제 콘텐츠 없이 더미 텍스트와 회색 박스로만 구성된다. 여기서 중요한 것은 콘텐츠의 **구조**를 정의하는 것이다. 이미지 크기, 텍스트 길이 제한 등을 이 단계에서 정한다.

<svg width="100%" viewBox="0 0 640 240" xmlns="http://www.w3.org/2000/svg">
  <!-- 전체 프레임 -->
  <rect x="20" y="15" width="600" height="215" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="320" y="36" text-anchor="middle" font-size="11" font-weight="600" fill="#888780">템플릿 (콘텐츠 없는 뼈대)</text>

  <!-- 헤더 영역 -->
  <rect x="36" y="46" width="568" height="36" rx="4" fill="#D3D1C7"/>
  <text x="320" y="69" text-anchor="middle" font-size="10" fill="#888780">헤더 유기체 영역</text>

  <!-- 메인 콘텐츠 -->
  <rect x="36" y="92" width="380" height="120" rx="4" fill="#D3D1C7"/>
  <text x="226" y="156" text-anchor="middle" font-size="10" fill="#888780">메인 콘텐츠 영역</text>

  <!-- 사이드바 -->
  <rect x="428" y="92" width="176" height="120" rx="4" fill="#D3D1C7"/>
  <text x="516" y="156" text-anchor="middle" font-size="10" fill="#888780">사이드바</text>

  <!-- 설명 -->
  <text x="320" y="228" text-anchor="middle" font-size="10" fill="#888780">실제 텍스트·이미지 없이 구조만 정의한 상태</text>
</svg>

---

### 5. 페이지 (Pages) — 실제 콘텐츠가 채워진 완성본

템플릿에 실제 텍스트, 이미지, 데이터를 채운 최종 결과물이다. 사용자가 실제로 보게 되는 화면이고, 디자인 시스템이 실제로 잘 작동하는지 검증하는 단계이기도 하다. 실제 콘텐츠를 넣어보면 예상치 못한 문제들이 드러나고, 그때 하위 단계로 돌아가 수정한다.

<svg width="100%" viewBox="0 0 640 240" xmlns="http://www.w3.org/2000/svg">
  <!-- 전체 프레임 -->
  <rect x="20" y="15" width="600" height="215" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="320" y="36" text-anchor="middle" font-size="11" font-weight="600" fill="#3C3489">페이지 (실제 콘텐츠 채운 완성본)</text>

  <!-- 헤더 -->
  <rect x="36" y="46" width="568" height="36" rx="4" fill="#7F77DD"/>
  <text x="80" y="69" font-size="11" font-weight="600" fill="#EEEDFE">🔮 Connecting Dots</text>
  <text x="340" y="69" font-size="10" fill="#EEEDFE">홈  탐색  프로젝트  소개</text>

  <!-- 메인 콘텐츠 -->
  <rect x="36" y="92" width="380" height="120" rx="4" fill="#AFA9EC"/>
  <text x="226" y="136" text-anchor="middle" font-size="12" font-weight="600" fill="#26215C">개발자에서 디자이너로</text>
  <text x="226" y="156" text-anchor="middle" font-size="10" fill="#3C3489">3년간의 개발 경험을 바탕으로</text>
  <text x="226" y="172" text-anchor="middle" font-size="10" fill="#3C3489">프로덕트 디자이너로 전향하는 기록</text>

  <!-- 사이드바 -->
  <rect x="428" y="92" width="176" height="120" rx="4" fill="#CEC BF6"/>
  <text x="516" y="128" text-anchor="middle" font-size="10" fill="#26215C">최신 글</text>
  <text x="516" y="148" text-anchor="middle" font-size="9" fill="#3C3489">DAY 16 — 아토믹...</text>
  <text x="516" y="164" text-anchor="middle" font-size="9" fill="#3C3489">DAY 15 — 디자인...</text>

  <text x="320" y="228" text-anchor="middle" font-size="10" fill="#534AB7">실제 텍스트와 이미지가 채워진 완성 화면</text>
</svg>

---

### 아토믹 디자인의 핵심 가치

아토믹 디자인이 유용한 이유는 **부분과 전체를 동시에 볼 수 있게 해 주기 때문**이다. Brad Frost는 화가가 캔버스에 가까이 다가가 붓질을 하다가 뒤로 물러나 전체를 보는 것과 같다고 설명했다. 원자 단위로 세밀하게 작업하면서도, 그것이 전체 UI에서 어떻게 작동하는지 동시에 확인할 수 있는 구조다.

> [!tip]
> 아토믹 디자인은 단계별 순서가 아니라 사고 모델이다. 버튼 하나를 만들 때도 그것이 시스템 전체에서 어떻게 작동하는지 함께 생각하는 것이 핵심이다

여기에서 오늘의 실습 내용을 볼 수 있어요! [[14. 파일 업로드 창을 만들다 상태 설계를 이해했다]]