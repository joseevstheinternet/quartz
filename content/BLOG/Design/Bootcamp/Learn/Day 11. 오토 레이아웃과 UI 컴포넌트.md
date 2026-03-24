---
date: 2026-03-13
---
**Auto layout은 UI를 배치하는 기능이 아니라 구조를 유지하는 기능이다.**

요소를 하나하나 위치시키는 게 아니라 규칙을 만들어 두면 자동으로 정렬·간격·크기가 유지되는 방식. 텍스트 길이나 화면 크기가 바뀌어도 레이아웃이 무너지지 않도록 만드는 것이 핵심이다.

---

### Auto Layout 핵심 속성

<svg width="100%" viewBox="0 0 640 220" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="185" height="90" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">방향 (Direction)</text>
  <text x="112" y="62" text-anchor="middle" font-size="11" fill="#185FA5">Horizontal → 가로 정렬</text>
  <text x="112" y="78" text-anchor="middle" font-size="11" fill="#185FA5">Vertical → 세로 정렬</text>
  <text x="112" y="96" text-anchor="middle" font-size="10" fill="#378ADD">버튼·리스트·카드 구조에 중요</text>

  <rect x="228" y="15" width="185" height="90" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="320" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">Spacing</text>
  <text x="320" y="62" text-anchor="middle" font-size="11" fill="#185FA5">요소 사이 간격을 일정하게 유지</text>
  <text x="320" y="78" text-anchor="middle" font-size="11" fill="#185FA5">Auto 설정 시 공간에 맞게</text>
  <text x="320" y="96" text-anchor="middle" font-size="10" fill="#378ADD">자동 분배. 가장 많이 쓰는 기능</text>

  <rect x="436" y="15" width="184" height="90" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="528" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">Padding</text>
  <text x="528" y="62" text-anchor="middle" font-size="11" fill="#3B6D11">컨테이너와 내부 요소 사이</text>
  <text x="528" y="78" text-anchor="middle" font-size="11" fill="#3B6D11">거리. 상/하/좌/우 각각 설정</text>
  <text x="528" y="96" text-anchor="middle" font-size="10" fill="#639922">버튼·카드·박스 UI에서 필수</text>

  <!-- Hug / Fill / Fixed -->
  <rect x="20" y="125" width="185" height="80" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="112" y="150" text-anchor="middle" font-size="12" font-weight="600" fill="#4A1B0C">Hug contents</text>
  <text x="112" y="168" text-anchor="middle" font-size="11" fill="#712B13">내용에 맞게 크기 변함</text>
  <text x="112" y="184" text-anchor="middle" font-size="10" fill="#D85A30">버튼·태그·라벨에 사용</text>

  <rect x="228" y="125" width="185" height="80" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="320" y="150" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">Fill container</text>
  <text x="320" y="168" text-anchor="middle" font-size="11" fill="#534AB7">부모 영역을 꽉 채움</text>
  <text x="320" y="184" text-anchor="middle" font-size="10" fill="#7F77DD">반응형 레이아웃의 핵심</text>

  <rect x="436" y="125" width="184" height="80" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="528" y="150" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">Fixed size</text>
  <text x="528" y="168" text-anchor="middle" font-size="11" fill="#5F5E5A">크기 고정. 변하지 않음</text>
  <text x="528" y="184" text-anchor="middle" font-size="10" fill="#888780">아이콘·카드·이미지 영역</text>
</svg>

한 줄로 정리하면 Hug는 "내용 기준", Fill은 "부모 기준", Fixed는 "고정값"이다.

---

### Auto Layout과 개발의 연관

Auto Layout을 배우면서 흥미로운 지점이 하나 있었다. 피그마의 Auto Layout이 개발에서 쓰는 CSS Flexbox와 거의 동일한 개념이라는 것.

방향(Direction)은 `flex-direction`, Spacing은 `gap`, Alignment는 `justify-content`와 `align-items`에 대응된다. 예전에는 디자인이 시각적인 작업이었다면, 지금은 점점 동작하는 구조를 설계하는 일에 가까워지고 있다.

---

### UI 컴포넌트 6가지

UI 컴포넌트는 모양이 아니라 **역할**로 구분해야 한다. 적절한 컴포넌트를 선택하는 것이 곧 사용자 행동을 설계하는 일이다.

<svg width="100%" viewBox="0 0 640 380" xmlns="http://www.w3.org/2000/svg">
  <!-- Carousel -->
  <rect x="20" y="15" width="185" height="110" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">Carousel</text>
  <text x="112" y="62" text-anchor="middle" font-size="11" fill="#185FA5">여러 콘텐츠를 좌우로</text>
  <text x="112" y="78" text-anchor="middle" font-size="11" fill="#185FA5">넘겨가며 보여주는 UI</text>
  <text x="112" y="100" text-anchor="middle" font-size="10" fill="#378ADD">⚠ 중요 정보는 반드시 첫 슬라이드</text>
  <text x="112" y="116" text-anchor="middle" font-size="10" fill="#378ADD">자동 슬라이드는 UX 방해 가능</text>

  <!-- Tab -->
  <rect x="228" y="15" width="185" height="110" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="320" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">Tab</text>
  <text x="320" y="62" text-anchor="middle" font-size="11" fill="#185FA5">같은 레벨의 콘텐츠를</text>
  <text x="320" y="78" text-anchor="middle" font-size="11" fill="#185FA5">그룹으로 나눠 전환</text>
  <text x="320" y="100" text-anchor="middle" font-size="10" fill="#378ADD">⚠ 탭 개수 3~5개가 적절</text>
  <text x="320" y="116" text-anchor="middle" font-size="10" fill="#378ADD">현재 탭 명확하게 표시 필요</text>

  <!-- Checkbox -->
  <rect x="436" y="15" width="184" height="110" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="528" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">Checkbox</text>
  <text x="528" y="62" text-anchor="middle" font-size="11" fill="#3B6D11">복수 선택이 가능한</text>
  <text x="528" y="78" text-anchor="middle" font-size="11" fill="#3B6D11">입력 UI</text>
  <text x="528" y="100" text-anchor="middle" font-size="10" fill="#639922">관심사 선택, 필터, 약관 동의</text>
  <text x="528" y="116" text-anchor="middle" font-size="10" fill="#639922">0개 이상 선택 가능</text>

  <!-- Radio -->
  <rect x="20" y="145" width="185" height="110" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="112" y="172" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">Radio Button</text>
  <text x="112" y="192" text-anchor="middle" font-size="11" fill="#3B6D11">하나만 선택 가능한</text>
  <text x="112" y="208" text-anchor="middle" font-size="11" fill="#3B6D11">입력 UI</text>
  <text x="112" y="228" text-anchor="middle" font-size="10" fill="#639922">결제 수단, 배송 옵션, 성별</text>
  <text x="112" y="244" text-anchor="middle" font-size="10" fill="#639922">선택 시 기존 선택 자동 해제</text>

  <!-- Modal -->
  <rect x="228" y="145" width="185" height="110" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="320" y="172" text-anchor="middle" font-size="12" font-weight="600" fill="#412402">Modal</text>
  <text x="320" y="192" text-anchor="middle" font-size="11" fill="#633806">현재 화면 위에 띄워</text>
  <text x="320" y="208" text-anchor="middle" font-size="11" fill="#633806">집중을 유도하는 UI</text>
  <text x="320" y="228" text-anchor="middle" font-size="10" fill="#BA7517">⚠ 과도한 사용 시 UX 방해</text>
  <text x="320" y="244" text-anchor="middle" font-size="10" fill="#BA7517">닫기 버튼 반드시 제공</text>

  <!-- Progress -->
  <rect x="436" y="145" width="184" height="110" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="528" y="172" text-anchor="middle" font-size="12" font-weight="600" fill="#412402">Progress Indicator</text>
  <text x="528" y="192" text-anchor="middle" font-size="11" fill="#633806">진행 상태를 시각적으로</text>
  <text x="528" y="208" text-anchor="middle" font-size="11" fill="#633806">보여주는 UI</text>
  <text x="528" y="228" text-anchor="middle" font-size="10" fill="#BA7517">Linear / Circular / Step형</text>
  <text x="528" y="244" text-anchor="middle" font-size="10" fill="#BA7517">사용자 불안 감소에 효과적</text>

  <!-- 선택 기준 -->
  <rect x="20" y="275" width="600" height="90" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="320" y="302" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">컴포넌트 선택 기준</text>
  <text x="320" y="324" text-anchor="middle" font-size="11" fill="#534AB7">여러 개 선택해야 한다 → Checkbox</text>
  <text x="320" y="342" text-anchor="middle" font-size="11" fill="#534AB7">반드시 하나만 선택해야 한다 → Radio Button</text>
  <text x="320" y="360" text-anchor="middle" font-size="11" fill="#534AB7">흐름을 멈추고 확인이 필요하다 → Modal</text>
</svg>

컴포넌트 선택은 디자인 문제가 아니라 사용자 행동을 설계하는 문제다.

---

> [!tip]
> Auto Layout은 편한 기능이 아니라 디자인을 구조적으로 만드는 사고 방식이다
> Hug·Fill·Fixed를 이해하면 반응형 UI의 절반은 해결된다

여기에서 오늘의 실습 내용을 볼 수 있어요! [[11. 피그마 하다가 갑자기 개발 공부하는 기분이 들었다]]