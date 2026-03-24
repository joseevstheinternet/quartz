---
date: 2026-03-12
---
UI는 사용자가 디지털 제품과 상호작용하는 모든 화면 요소를 의미한다. 웹사이트나 앱에서 눈으로 보고 클릭하거나 입력하는 모든 것이 UI다. 오늘 수업에서는 UI를 구성하는 기본 요소들과, 그것을 일관되게 유지하기 위한 디자인 파운데이션 개념을 배웠다.

---

### 좋은 UI의 조건

좋은 UI는 사용자가 복잡하게 생각하지 않아도 직관적으로 이해하고 쉽게 사용할 수 있도록 설계된 것이다. 화면 구조가 명확할수록 사용자는 원하는 정보를 더 빠르게 찾을 수 있다.

<svg width="100%" viewBox="0 0 640 110" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="135" height="70" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="88" y="52" text-anchor="middle" font-size="13" font-weight="600" fill="#0C447C">일관성</text>
  <text x="88" y="70" text-anchor="middle" font-size="11" fill="#185FA5">같은 패턴을 반복해</text>
  <text x="88" y="84" text-anchor="middle" font-size="11" fill="#185FA5">학습 부담을 줄인다</text>

  <rect x="170" y="20" width="135" height="70" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="238" y="52" text-anchor="middle" font-size="13" font-weight="600" fill="#0C447C">직관성</text>
  <text x="238" y="70" text-anchor="middle" font-size="11" fill="#185FA5">설명 없이도</text>
  <text x="238" y="84" text-anchor="middle" font-size="11" fill="#185FA5">조작할 수 있다</text>

  <rect x="320" y="20" width="135" height="70" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="388" y="52" text-anchor="middle" font-size="13" font-weight="600" fill="#27500A">접근성</text>
  <text x="388" y="70" text-anchor="middle" font-size="11" fill="#3B6D11">누구나 사용할 수</text>
  <text x="388" y="84" text-anchor="middle" font-size="11" fill="#3B6D11">있도록 설계한다</text>

  <rect x="470" y="20" width="150" height="70" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="545" y="52" text-anchor="middle" font-size="13" font-weight="600" fill="#27500A">명확한 피드백</text>
  <text x="545" y="70" text-anchor="middle" font-size="11" fill="#3B6D11">행동의 결과를</text>
  <text x="545" y="84" text-anchor="middle" font-size="11" fill="#3B6D11">즉시 알려준다</text>
</svg>

---

### 디자인 파운데이션

디자인 파운데이션은 UI 디자인의 기본 규칙을 의미한다. 디자인 시스템의 가장 밑바닥에 있는 것들로, 이 규칙들이 잘 잡혀 있어야 전체 UI가 일관된 느낌을 갖출 수 있다.

<svg width="100%" viewBox="0 0 640 300" xmlns="http://www.w3.org/2000/svg">
  <!-- 타이포그래피 -->
  <rect x="20" y="15" width="290" height="120" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="36" y="44" font-size="13" font-weight="600" fill="#3C3489">타이포그래피</text>
  <text x="36" y="64" font-size="11" fill="#534AB7">텍스트 크기, 줄 간격, 글꼴 스타일 등</text>
  <text x="36" y="82" font-size="11" fill="#534AB7">텍스트 표현 방식의 규칙</text>
  <text x="36" y="108" font-size="24" font-weight="700" fill="#26215C">Aa</text>
  <text x="80" y="108" font-size="16" font-weight="500" fill="#3C3489">Aa</text>
  <text x="116" y="108" font-size="12" fill="#534AB7">Aa</text>
  <text x="144" y="108" font-size="10" fill="#7F77DD">Aa</text>

  <!-- 컬러 시스템 -->
  <rect x="330" y="15" width="290" height="120" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="346" y="44" font-size="13" font-weight="600" fill="#412402">컬러 시스템</text>
  <text x="346" y="64" font-size="11" fill="#633806">브랜드 컬러, 보조 컬러, 상태 컬러 등</text>
  <text x="346" y="82" font-size="11" fill="#633806">서비스에서 사용하는 색상 체계</text>
  <rect x="346" y="95" width="32" height="20" rx="4" fill="#3C3489"/>
  <rect x="386" y="95" width="32" height="20" rx="4" fill="#639922"/>
  <rect x="426" y="95" width="32" height="20" rx="4" fill="#E24B4A"/>
  <rect x="466" y="95" width="32" height="20" rx="4" fill="#BA7517"/>
  <rect x="506" y="95" width="32" height="20" rx="4" fill="#888780"/>

  <!-- 간격 시스템 -->
  <rect x="20" y="155" width="185" height="130" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="184" font-size="13" font-weight="600" fill="#27500A">간격 시스템</text>
  <text x="36" y="204" font-size="11" fill="#3B6D11">요소 사이의 간격을</text>
  <text x="36" y="220" font-size="11" fill="#3B6D11">일정한 규칙으로 관리</text>
  <text x="36" y="248" font-size="11" fill="#3B6D11">4px · 8px · 16px · 24px · 32px</text>
  <text x="36" y="266" font-size="10" fill="#639922">→ 8pt 그리드 기반</text>

  <!-- 패딩·마진 -->
  <rect x="220" y="155" width="185" height="130" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="236" y="184" font-size="13" font-weight="600" fill="#27500A">패딩과 마진</text>
  <text x="236" y="204" font-size="11" fill="#3B6D11">UI 요소 내부(패딩)와</text>
  <text x="236" y="220" font-size="11" fill="#3B6D11">외부(마진)의 여백</text>
  <rect x="260" y="240" width="80" height="30" rx="4" fill="none" stroke="#639922" stroke-width="1" stroke-dasharray="4 2"/>
  <rect x="270" y="245" width="60" height="20" rx="3" fill="#C0DD97"/>
  <text x="300" y="258" text-anchor="middle" font-size="9" fill="#27500A">padding</text>

  <!-- Border Radius -->
  <rect x="420" y="155" width="200" height="130" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="436" y="184" font-size="13" font-weight="600" fill="#0C447C">Border Radius</text>
  <text x="436" y="204" font-size="11" fill="#185FA5">버튼이나 카드 모서리의</text>
  <text x="436" y="220" font-size="11" fill="#185FA5">둥근 정도</text>
  <rect x="436" y="238" width="48" height="28" rx="0" fill="#B5D4F4" stroke="#378ADD" stroke-width="1"/>
  <rect x="494" y="238" width="48" height="28" rx="6" fill="#85B7EB" stroke="#378ADD" stroke-width="1"/>
  <rect x="552" y="238" width="48" height="28" rx="14" fill="#378ADD" stroke="#378ADD" stroke-width="1"/>
  <text x="460" y="278" text-anchor="middle" font-size="9" fill="#185FA5">0px</text>
  <text x="518" y="278" text-anchor="middle" font-size="9" fill="#185FA5">6px</text>
  <text x="576" y="278" text-anchor="middle" font-size="9" fill="#185FA5">14px</text>
</svg>

이 요소들이 잘 정의되어 있어야 여러 화면에서 UI가 일관된 리듬과 느낌을 갖게 된다. 디자인 파운데이션은 결국 디자인 시스템의 뿌리가 되는 부분이다.

---

> [!tip]
> 좋은 UI를 만들기 위해서는 화면 하나하나를 예쁘게 만드는 것보다 
> 색상, 타이포그래피, 간격 같은 기본 규칙을 먼저 체계적으로 잡아 두는 것이 중요하다

여기에서 오늘의 실습 내용을 볼 수 있어요! [[10. 포트폴리오 첫 화면 하나에 담긴 고민들]]