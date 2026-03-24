---
date: 2026-03-17
---
반복되는 UI 요소를 매번 새로 만드는 게 아니라, 한 번 잘 만들어 두고 계속 쓰는 방식을 배우는 것. 그것이 컴포넌트이고, 그 컴포넌트들을 체계적으로 관리하는 구조가 디자인 시스템이다.

---

### 컴포넌트와 인스턴스

**컴포넌트**는 반복적으로 사용하는 UI 요소를 하나의 기준 형태로 만들어 재사용 가능하게 묶은 단위다. 버튼, 카드, 입력창 같은 것들을 매번 새로 그리는 게 아니라 하나를 만들어 두고 계속 갖다 쓰는 방식이다. 수정할 때 컴포넌트 하나만 바꾸면 그것을 사용하는 모든 곳이 자동으로 바뀐다.

**인스턴스**는 컴포넌트를 복사해서 실제로 화면에 배치한 것이다. 컴포넌트(원본)는 다이아몬드 4개 아이콘, 인스턴스(복사본)는 다이아몬드 1개 아이콘으로 구분된다.

<svg width="100%" viewBox="0 0 640 170" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>

  <!-- 컴포넌트 -->
  <rect x="20" y="30" width="170" height="110" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="105" y="58" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">컴포넌트 (원본)</text>
  <text x="105" y="78" text-anchor="middle" font-size="11" fill="#534AB7">◆◆◆◆ 아이콘</text>
  <text x="105" y="98" text-anchor="middle" font-size="11" fill="#534AB7">수정하면 모든</text>
  <text x="105" y="114" text-anchor="middle" font-size="11" fill="#534AB7">인스턴스에 반영</text>
  <text x="105" y="132" text-anchor="middle" font-size="10" fill="#7F77DD">에셋 패널에서 관리</text>

  <line x1="192" y1="85" x2="228" y2="70" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="192" y1="85" x2="228" y2="100" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <!-- 인스턴스 1 -->
  <rect x="230" y="20" width="170" height="50" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="315" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">인스턴스 A</text>
  <text x="315" y="58" text-anchor="middle" font-size="11" fill="#185FA5">◆ 아이콘 / 텍스트·색상 변경 가능</text>

  <!-- 인스턴스 2 -->
  <rect x="230" y="90" width="170" height="50" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="315" y="112" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">인스턴스 B</text>
  <text x="315" y="128" text-anchor="middle" font-size="11" fill="#185FA5">◆ 아이콘 / Override 적용 가능</text>

  <!-- 주의사항 -->
  <rect x="420" y="20" width="200" height="120" rx="8" fill="#FFF8F0" stroke="#BA7517" stroke-width="0.8"/>
  <text x="520" y="46" text-anchor="middle" font-size="11" font-weight="600" fill="#412402">알아 두면 좋은 것</text>
  <text x="520" y="66" text-anchor="middle" font-size="10" fill="#633806">Override한 요소는</text>
  <text x="520" y="82" text-anchor="middle" font-size="10" fill="#633806">컴포넌트 변경 시 안 바뀜</text>
  <text x="520" y="102" text-anchor="middle" font-size="10" fill="#633806">Reset → 원래대로 복구</text>
  <text x="520" y="118" text-anchor="middle" font-size="10" fill="#633806">Detach → 완전히 독립</text>
  <text x="520" y="134" text-anchor="middle" font-size="10" fill="#633806">(새 컴포넌트로 만들기 가능)</text>
</svg>
![[Pasted image 20260324120908.png|445]]
![[Pasted image 20260324120928.png|462]]
![[Pasted image 20260324120948.png|462]]
![[Pasted image 20260324121003.png|464]]

---

### Component Property 4가지

컴포넌트를 더 유연하게 쓸 수 있도록 속성을 설정하는 기능이다. 인스턴스에서 클릭 몇 번으로 상태나 내용을 바꿀 수 있게 해 준다.

<svg width="100%" viewBox="0 0 640 230" xmlns="http://www.w3.org/2000/svg">
  <!-- Variant -->
  <rect x="20" y="15" width="290" height="95" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="36" y="42" font-size="12" font-weight="600" fill="#0C447C">① Variant</text>
  <text x="36" y="62" font-size="11" fill="#185FA5">컴포넌트의 상태 변형을 만든다</text>
  <text x="36" y="80" font-size="11" fill="#185FA5">Default / Hover / Selected 등</text>
  <text x="36" y="98" font-size="10" fill="#378ADD">인스턴스에서 드롭다운으로 상태 전환 가능</text>

  <!-- Text -->
  <rect x="330" y="15" width="290" height="95" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="346" y="42" font-size="12" font-weight="600" fill="#0C447C">② Text</text>
  <text x="346" y="62" font-size="11" fill="#185FA5">컴포넌트 내부 텍스트를 속성으로 등록</text>
  <text x="346" y="80" font-size="11" fill="#185FA5">인스턴스에서 직접 클릭 없이</text>
  <text x="346" y="98" font-size="10" fill="#378ADD">패널에서 바로 텍스트 수정 가능</text>

  <!-- Boolean -->
  <rect x="20" y="128" width="290" height="95" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="155" font-size="12" font-weight="600" fill="#27500A">③ Boolean</text>
  <text x="36" y="175" font-size="11" fill="#3B6D11">요소의 표시/숨김을 토글로 설정</text>
  <text x="36" y="193" font-size="11" fill="#3B6D11">값을 true/false 또는 on/off로 설정</text>
  <text x="36" y="211" font-size="10" fill="#639922">아이콘 유무, 배지 표시 등에 활용</text>

  <!-- Instance Swap -->
  <rect x="330" y="128" width="290" height="95" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="346" y="155" font-size="12" font-weight="600" fill="#27500A">④ Instance Swap</text>
  <text x="346" y="175" font-size="11" fill="#3B6D11">내부 아이콘/이미지를 다른 컴포넌트로</text>
  <text x="346" y="193" font-size="11" fill="#3B6D11">교체할 수 있게 설정</text>
  <text x="346" y="211" font-size="10" fill="#639922">각 아이콘을 먼저 컴포넌트화해야 함</text>
</svg>

![[Pasted image 20260324121038.png|288]]

![[Pasted image 20260324121109.png|485]]
버튼 컴포넌트를 만들고, Default / Hover / Selected 세 가지 Variant를 설정했다. 컴포넌트 하나를 만들고 거기서 상태를 분기시키는 방식이었다.

그런데 Hover 상태에서 버튼 색을 조금 진하게 바꿨더니, 화면에 배치된 모든 버튼 인스턴스의 Hover 상태가 한 번에 바뀌는 걸 봤다. 당연한 거지만 처음 보는 순간 뭔가 이상하게 시원한 느낌이 들었다.
지금까지는 버튼 하나를 수정하면 나머지는 직접 찾아가서 하나하나 바꿨다. 이게 얼마나 비효율적인 방식이었는지 이제 와서 실감했다.

![[Pasted image 20260324121207.png|507]]

![[Pasted image 20260324121232.png]]
![[Pasted image 20260324121249.png]]
Boolean 속성으로 아이콘 유무를 설정하는 것도 재미있었다. 인스턴스 패널에서 토글 하나로 아이콘이 나타났다 사라졌다 하는 걸 보면서, 디자인을 구조적으로 만든다는 게 어떤 의미인지 체감이 됐다.

UI를 배치하는 게 아니라 상태를 설계하는 것이다.

![[Pasted image 20260324121305.png|501]]
Instance Swap은 신기했다. 아이콘들을 미리 컴포넌트로 만들어 두고, 버튼 안에 들어가는 아이콘을 인스턴스 패널에서 드롭다운으로 바꿀 수 있게 설정하는 것이었다.

처음에는 왜 이렇게 복잡하게 만드나 싶었는데, 막상 써 보니 아이콘을 일일이 지우고 다시 가져다 놓는 것보다 훨씬 빠르고 실수도 없었다. 처음에 설정하는 데 공을 들이면 나중에 훨씬 편해지는 구조였다.

---

### 디자인 시스템의 5단계 구조
디자인 시스템은 디자인을 '규칙 + 부품' 형태로 관리하는 구조다. 아래에서 위로 쌓아 올라가는 방식으로 이해하면 된다.

<svg width="100%" viewBox="0 0 640 280" xmlns="http://www.w3.org/2000/svg">
  <!-- 피라미드 구조 -->
  <!-- Style Guidelines (최상단) -->
  <rect x="210" y="15" width="220" height="42" rx="8" fill="#3C3489" stroke="none"/>
  <text x="320" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#EEEDFE">Style Guidelines</text>

  <!-- Templates -->
  <rect x="160" y="68" width="320" height="42" rx="8" fill="#534AB7" stroke="none"/>
  <text x="320" y="88" text-anchor="middle" font-size="12" font-weight="600" fill="#EEEDFE">Templates</text>
  <text x="320" y="102" text-anchor="middle" font-size="10" fill="#CEC BF6">화면 전체 구조 / 페이지 레벨 설계</text>

  <!-- Patterns -->
  <rect x="100" y="121" width="440" height="42" rx="8" fill="#7F77DD" stroke="none"/>
  <text x="320" y="141" text-anchor="middle" font-size="12" font-weight="600" fill="#EEEDFE">Patterns</text>
  <text x="320" y="155" text-anchor="middle" font-size="10" fill="#EEEDFE">여러 컴포넌트를 묶은 UX 흐름 단위</text>

  <!-- Components -->
  <rect x="50" y="174" width="540" height="42" rx="8" fill="#AFA9EC" stroke="none"/>
  <text x="320" y="194" text-anchor="middle" font-size="12" font-weight="600" fill="#26215C">Components</text>
  <text x="320" y="208" text-anchor="middle" font-size="10" fill="#26215C">Button · Input · Checkbox · Modal · Card 등 재사용 부품</text>

  <!-- Foundation -->
  <rect x="20" y="227" width="600" height="42" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="320" y="247" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">Foundation</text>
  <text x="320" y="261" text-anchor="middle" font-size="10" fill="#534AB7">타이포그래피 · 컬러 · 간격 · 아이콘 등 디자인의 기본 언어</text>
</svg>
![[Pasted image 20260324121427.png|425]]


한 줄로 정리하면, 컴포넌트는 재사용, 인스턴스는 실제 사용, 디자인 시스템은 그것을 구조화된 방식으로 관리하는 틀이다.

---

> [!tip]
> 컴포넌트를 만드는 것보다 중요한 건 언제 만들지를 아는 것이다.
> 두 번 이상 쓰는 것이라면 컴포넌트로 만들어 두는 게 맞다.

여기에서 관련 실습을 볼 수 있어요! [[12. 카드 결제, 계산기, 리뷰 UI 제작]]