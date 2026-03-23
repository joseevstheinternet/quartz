---
found: "[[08. 와이어프레임을 만들다 Lo-fi의 의미를 알았다]]"
date: 2026-03-10
---
오늘 수업의 핵심은 화면을 만들기 전에 먼저 구조를 설계해야 한다는 것이었다. UX/UI 디자인은 바로 화면을 만드는 것이 아니라 사용자 흐름과 정보 구조를 먼저 잡은 뒤, 이를 기반으로 와이어프레임을 만드는 과정으로 진행된다.

---

### 디자인 시스템

디자인 시스템은 버튼, 색상, 레이아웃, 컴포넌트 등 UI 요소에 대한 규칙을 정리한 가이드다. 여러 디자이너와 개발자가 함께 작업할 때 일관된 경험을 유지하기 위해 필요하다.

대표적인 디자인 시스템으로는 구글의 [Material Design 3](https://m3.material.io/get-started)과 애플의 [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)이 있다. 두 가이드 모두 색상, 컴포넌트, 인터랙션, 레이아웃에 대한 기준을 상세하게 제공한다.

디자인 시스템을 활용하면 서비스 전체 UI의 일관성 유지, 디자이너와 개발자 간 협업 효율 향상, 새로운 기능 추가 시 빠른 확장이 가능해진다. 대부분의 서비스는 이를 참고하거나 자체 디자인 시스템을 갖추고 있다.

---

### 8pt 그리드 시스템

UI 디자인에서 레이아웃을 정리할 때 가장 중요한 기준 중 하나가 그리드 시스템이다. 특히 4배수 또는 8배수 그리드가 널리 쓰인다.

<svg width="100%" viewBox="0 0 640 190" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="185" height="150" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="44" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">① 디자인 일관성</text>
  <text x="112" y="64" text-anchor="middle" font-size="11" fill="#185FA5">모든 요소가 같은 규칙을</text>
  <text x="112" y="80" text-anchor="middle" font-size="11" fill="#185FA5">따르면 화면 전체가</text>
  <text x="112" y="96" text-anchor="middle" font-size="11" fill="#185FA5">정돈되고 안정적으로 보인다</text>
  <text x="112" y="148" text-anchor="middle" font-size="10" fill="#378ADD">13px, 17px → 어색함</text>
  <text x="112" y="163" text-anchor="middle" font-size="10" fill="#378ADD">8px, 16px, 24px → 자연스러움</text>

  <rect x="228" y="15" width="185" height="150" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="320" y="44" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">② 화면 크기 대응</text>
  <text x="320" y="64" text-anchor="middle" font-size="11" fill="#3B6D11">8px 단위는 대부분의</text>
  <text x="320" y="80" text-anchor="middle" font-size="11" fill="#3B6D11">해상도와 디바이스 스케일에</text>
  <text x="320" y="96" text-anchor="middle" font-size="11" fill="#3B6D11">자연스럽게 맞는 값이다</text>
  <text x="320" y="148" text-anchor="middle" font-size="10" fill="#639922">레티나, 고해상도 디스플레이</text>
  <text x="320" y="163" text-anchor="middle" font-size="10" fill="#639922">모두 대응 가능</text>

  <rect x="436" y="15" width="184" height="150" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="528" y="44" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">③ 협업 효율</text>
  <text x="528" y="64" text-anchor="middle" font-size="11" fill="#534AB7">값이 규칙을 따르면</text>
  <text x="528" y="80" text-anchor="middle" font-size="11" fill="#534AB7">개발자가 "23px인가요</text>
  <text x="528" y="96" text-anchor="middle" font-size="11" fill="#534AB7">24px인가요?" 물을 필요가 없다</text>
  <text x="528" y="148" text-anchor="middle" font-size="10" fill="#7F77DD">항상 8의 배수로 결정됨</text>
  <text x="528" y="163" text-anchor="middle" font-size="10" fill="#7F77DD">디자인 시스템 구축에도 필수</text>
</svg>

폰트 사이즈는 반드시 이 규칙을 따르지 않아도 되지만, 간격과 레이아웃 구조에서는 그리드 규칙을 지키는 것이 중요하다.

---

### Column Grid 시스템

그리드 시스템은 화면을 여러 개의 컬럼으로 나누어 콘텐츠를 정렬하는 방식이다. 세 가지 요소로 구성된다.

<svg width="100%" viewBox="0 0 640 130" xmlns="http://www.w3.org/2000/svg">
  <!-- 그리드 시각화 -->
  <rect x="20" y="20" width="600" height="90" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>

  <!-- Margin 표시 -->
  <rect x="20" y="20" width="50" height="90" rx="0" fill="#FCEBEB" opacity="0.6"/>
  <rect x="570" y="20" width="50" height="90" rx="0" fill="#FCEBEB" opacity="0.6"/>
  <text x="45" y="70" text-anchor="middle" font-size="10" fill="#A32D2D">Margin</text>
  <text x="595" y="70" text-anchor="middle" font-size="10" fill="#A32D2D">Margin</text>

  <!-- Column 표시 -->
  <rect x="78" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="148" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="218" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="288" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="358" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="428" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>
  <rect x="498" y="28" width="60" height="74" rx="4" fill="#E6F1FB" stroke="#378ADD" stroke-width="0.5"/>

  <text x="108" y="70" text-anchor="middle" font-size="10" fill="#0C447C">Column</text>
  <text x="178" y="70" text-anchor="middle" font-size="10" fill="#0C447C">Column</text>

  <!-- Gutter 표시 -->
  <text x="140" y="118" text-anchor="middle" font-size="10" fill="#888780">← Gutter →</text>
</svg>

**Margin**은 화면 가장자리와 콘텐츠 사이의 여백, **Column**은 콘텐츠가 배치되는 영역, **Gutter**는 컬럼과 컬럼 사이의 간격이다.

웹에서는 12 Column Grid가 가장 널리 쓰인다. 12라는 숫자는 2, 3, 4, 6으로 나누기 쉬워서 다양한 레이아웃을 유연하게 만들 수 있기 때문이다. 6+6이면 2열, 4+4+4면 3열, 8+4면 메인 콘텐츠와 사이드바 구조가 된다. 
모바일에서는 화면 폭이 좁기 때문에 4~6컬럼이 일반적이다.
![[Pasted image 20260323230004.png]]

---

### 와이어프레임 — Lo-fi vs Hi-fi

와이어프레임은 서비스 화면을 만들기 전에 UI 구조를 간단하게 설계하는 단계다. 색상이나 이미지 같은 시각 요소보다 레이아웃 구조와 정보 배치에 집중한다.

<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="280" height="120" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="160" y="48" text-anchor="middle" font-size="13" font-weight="600" fill="#2C2C2A">Lo-fi Wireframe</text>
  <text x="160" y="70" text-anchor="middle" font-size="11" fill="#5F5E5A">손으로 그린 스케치 느낌</text>
  <text x="160" y="88" text-anchor="middle" font-size="11" fill="#5F5E5A">단순한 레이아웃 중심</text>
  <text x="160" y="106" text-anchor="middle" font-size="11" fill="#5F5E5A">아이디어를 빠르게 정리</text>
  <text x="160" y="128" text-anchor="middle" font-size="10" fill="#888780">박스 + 선 + 텍스트만으로 구성</text>

  <rect x="340" y="20" width="280" height="120" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="480" y="48" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">Hi-fi Wireframe</text>
  <text x="480" y="70" text-anchor="middle" font-size="11" fill="#534AB7">실제 UI와 유사한 구조</text>
  <text x="480" y="88" text-anchor="middle" font-size="11" fill="#534AB7">정리된 컴포넌트 사용</text>
  <text x="480" y="106" text-anchor="middle" font-size="11" fill="#534AB7">프로토타입 제작 단계에 가까움</text>
  <text x="480" y="128" text-anchor="middle" font-size="10" fill="#7F77DD">Lo-fi에서 점진적으로 발전</text>
</svg>

피그마에서는 Wireframe Plugin이나 AI 기반 와이어프레임 생성 기능을 활용하면 기본 UI 구조를 빠르게 만들 수 있다. 모바일 와이어프레임 작업 시 기준이 되는 화면 사이즈는 **375 × 812**로, 아이폰 화면 비율을 기준으로 한 모바일 UI 디자인 기본 사이즈다.

---

> [!tip]
> 디자인 시스템과 그리드는 제약이 아니라 자유다
> 규칙이 있어야 빠르게 결정하고, 일관되게 확장할 수 있다