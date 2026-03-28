---
date: 2026-03-24
---
디자인 토큰 개념을 배웠으니, 이제 그것을 피그마에서 실제로 구현하는 방법을 배울 차례였다. 피그마 Variable과 Mode를 활용하면 라이트모드와 다크모드를 버튼 하나로 전환할 수 있다.

참고: [Figma — Guide to variables](https://help.figma.com/hc/en-us/articles/15339657135383) / [Figma — Modes for variables](https://help.figma.com/hc/en-us/articles/15343816063383)

---

### Variable이란

Variable은 재사용 가능한 값을 저장해 두고 다양한 디자인 속성에 적용하는 기능이다. DAY 17에서 배운 디자인 토큰 개념을 피그마 안에서 직접 구현한 것이라고 보면 된다. 색상, 숫자, 문자열, Boolean 네 가지 타입을 지원한다.

<svg width="100%" viewBox="0 0 640 100" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="135" height="70" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="87" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#4A1B0C">Color</text>
  <text x="87" y="60" text-anchor="middle" font-size="10" fill="#712B13">색상값 저장</text>
  <text x="87" y="76" text-anchor="middle" font-size="10" fill="#712B13">#1976D2 등</text>

  <rect x="172" y="15" width="135" height="70" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="239" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#412402">Number</text>
  <text x="239" y="60" text-anchor="middle" font-size="10" fill="#633806">숫자값 저장</text>
  <text x="239" y="76" text-anchor="middle" font-size="10" fill="#633806">spacing, radius 등</text>

  <rect x="324" y="15" width="135" height="70" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="391" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">String</text>
  <text x="391" y="60" text-anchor="middle" font-size="10" fill="#3B6D11">문자값 저장</text>
  <text x="391" y="76" text-anchor="middle" font-size="10" fill="#3B6D11">텍스트 카피 등</text>

  <rect x="476" y="15" width="144" height="70" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="548" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">Boolean</text>
  <text x="548" y="60" text-anchor="middle" font-size="10" fill="#185FA5">참/거짓 저장</text>
  <text x="548" y="76" text-anchor="middle" font-size="10" fill="#185FA5">요소 표시/숨김</text>
</svg>
![[Pasted image 20260328234108.png]]

---

### Mode란: 같은 Variable, 다른 값

Mode는 Variable 하나에 여러 개의 값을 저장하는 기능이다. 예를 들어 `color/background`라는 Variable 하나에 Light 모드에서는 `#FFFFFF`, Dark 모드에서는 `#1A1A2E`를 저장할 수 있다. 그러면 화면 전체에서 이 Variable을 쓰는 모든 요소가 모드 전환 한 번으로 자동으로 바뀐다.

모드 없이 다크모드를 만들면 라이트모드 화면을 전부 복사한 뒤 색상을 하나하나 바꿔야 한다. 모드를 쓰면 Variable 컬렉션에 Dark 모드를 하나 추가하고 값을 입력하는 것으로 끝난다.

---

### 라이트/다크모드 구축 순서

<svg width="100%" viewBox="0 0 640 310" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>

  <!-- Step 1 -->
  <rect x="20" y="15" width="600" height="52" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="36" y="38" font-size="12" font-weight="600" fill="#4A1B0C">① Variable 컬렉션 만들기</text>
  <text x="36" y="56" font-size="11" fill="#712B13">Local variables 패널 열기 → 새 컬렉션 생성 → 컬러 Variable 추가</text>
  <line x1="320" y1="68" x2="320" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Step 2 -->
  <rect x="20" y="87" width="600" height="52" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="36" y="110" font-size="12" font-weight="600" fill="#412402">② Mode 추가하기</text>
  <text x="36" y="128" font-size="11" fill="#633806">컬렉션에서 Mode 추가 → Light / Dark 두 모드 생성</text>
  <line x1="320" y1="140" x2="320" y2="157" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Step 3 -->
  <rect x="20" y="159" width="600" height="70" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="182" font-size="12" font-weight="600" fill="#27500A">③ 각 Mode에 값 입력하기</text>
  <text x="36" y="200" font-size="11" fill="#3B6D11">color/bg-primary    Light: #FFFFFF    Dark: #121212</text>
  <text x="36" y="218" font-size="11" fill="#3B6D11">color/text-primary  Light: #1A1A1A    Dark: #FFFFFF</text>
  <line x1="320" y1="230" x2="320" y2="247" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- Step 4 -->
  <rect x="20" y="249" width="600" height="52" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="36" y="272" font-size="12" font-weight="600" fill="#0C447C">④ 디자인에 Variable 적용하기</text>
  <text x="36" y="290" font-size="11" fill="#185FA5">색상 속성 클릭 → Variable 아이콘 → 만들어 둔 Variable 선택</text>
</svg>

---

### Mode 전환 방법
Variable을 적용한 뒤 모드를 전환하는 방법은 두 가지다.

**오브젝트(레이어) 단위**: 프레임이나 섹션을 선택한 뒤 우측 패널 Appearance에서 Apply variable mode 클릭 → 컬렉션 hover → 원하는 모드 선택. 선택한 오브젝트와 그 하위 요소 전체에 적용된다.
![[Pasted image 20260328234217.png]]

**페이지 단위**: 캔버스 빈 곳을 클릭해서 아무것도 선택하지 않은 상태에서 우측 패널 Page 섹션에서 Apply variable mode 클릭. 페이지 전체에 한 번에 적용된다.

<svg width="100%" viewBox="0 0 640 140" xmlns="http://www.w3.org/2000/svg">
  <!-- 라이트모드 화면 -->
  <rect x="20" y="20" width="270" height="100" rx="8" fill="#FFFFFF" stroke="#B4B2A9" stroke-width="1"/>
  <rect x="20" y="20" width="270" height="32" rx="8" fill="#1976D2"/>
  <rect x="20" y="40" width="270" height="12" rx="0" fill="#1976D2"/>
  <text x="155" y="42" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">헤더</text>
  <rect x="36" y="66" width="230" height="10" rx="3" fill="#E0E0E0"/>
  <rect x="36" y="82" width="180" height="10" rx="3" fill="#E0E0E0"/>
  <rect x="36" y="98" width="200" height="10" rx="3" fill="#E0E0E0"/>
  <text x="155" y="132" text-anchor="middle" font-size="10" fill="#639922">Light Mode</text>

  <!-- 화살표 -->
  <text x="320" y="78" text-anchor="middle" font-size="20" fill="#888780">⇄</text>
  <text x="320" y="96" text-anchor="middle" font-size="9" fill="#888780">모드 전환</text>

  <!-- 다크모드 화면 -->
  <rect x="350" y="20" width="270" height="100" rx="8" fill="#121212" stroke="#534AB7" stroke-width="1"/>
  <rect x="350" y="20" width="270" height="32" rx="8" fill="#1565C0"/>
  <rect x="350" y="40" width="270" height="12" rx="0" fill="#1565C0"/>
  <text x="485" y="42" text-anchor="middle" font-size="11" font-weight="600" fill="#fff">헤더</text>
  <rect x="366" y="66" width="230" height="10" rx="3" fill="#333333"/>
  <rect x="366" y="82" width="180" height="10" rx="3" fill="#333333"/>
  <rect x="366" y="98" width="200" height="10" rx="3" fill="#333333"/>
  <text x="485" y="132" text-anchor="middle" font-size="10" fill="#7F77DD">Dark Mode</text>
</svg>

---

### Styles와 Variables의 차이

비슷해 보이지만 다르다. Styles는 색상이나 텍스트 스타일을 저장하지만 모드 전환 기능이 없다. Variables는 모드를 지원하기 때문에 라이트/다크모드처럼 컨텍스트에 따라 값이 달라지는 디자인 토큰을 구현하는 데 적합하다. 새 프로젝트라면 Variables로 시작하는 것이 좋고, 기존 Styles 기반 파일은 Variables로 전환하는 작업이 필요하다.

---

### Auto 모드: 부모로부터 상속

오브젝트의 모드를 명시적으로 설정하지 않으면 Auto 상태가 된다. Auto는 부모 컨테이너의 모드를 그대로 상속한다. 부모도 Auto면 더 위의 부모를 찾아가고, 아무도 모드를 설정하지 않았으면 컬렉션의 기본값(Default Mode)을 따른다. 이 계층 구조 덕분에 최상위 프레임 하나에만 Dark 모드를 적용해도 그 안의 모든 요소가 자동으로 다크모드로 바뀐다.

---

> [!tip]
> Variable Mode의 핵심은 하나의 컴포넌트 세트로 라이트/다크 두 가지 모드를 동시에 관리한다는 것이다.

여기에서 오늘 실습 내용을 볼 수 있어요! [[16. Boo!에 다크모드를 입히다]]