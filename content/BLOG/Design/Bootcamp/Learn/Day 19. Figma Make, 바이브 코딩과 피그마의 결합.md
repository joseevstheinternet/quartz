---
date: 2026-03-25
---
참고: [8 essential tips for using Figma Make](https://www.figma.com/blog/8-ways-to-build-with-figma-make/) / [Figma Make 살펴보기](https://help.figma.com/hc/ko/articles/31304412302231)

최근 **바이브 코딩**이라는 단어가 많이 들려온다. 바이브 코딩을 한 줄로 요약하면 코드를 한 줄 한 줄 짜는 대신 만들고 싶은 것의 의도와 느낌을 AI에게 전달하고 나머지는 AI가 알아서 하게 두는 방식이다.

나도 커플 앱 Boo!를 Claude Code 바이브 코딩으로 만드는 중이다. 코드를 직접 짜는 게 아니라, "이 화면에서 메시지를 보내면 상대방에게 실시간으로 보이게 해 줘" 같은 방식으로 대화하면서 앱을 만들어 가고 있다. 나는 디자인만 담당하는 셈이다.

Figma Make는 이 바이브 코딩의 방식을 피그마로 가져온 것이다. Claude Code가 개발자의 코드 작업에 바이브 코딩을 적용했다면, Figma Make는 디자이너의 UI 작업에 같은 방식을 적용했다. 프롬프트 몇 줄을 입력하면 실제로 작동하는 프로토타입이 되고, 필요하면 전용 URL로 바로 배포까지 할 수 있다.

![[Pasted image 20260329001550.png]]

---

### Figma Make가 등장한 배경

지금까지 디자인과 개발 사이에는 항상 간극이 있었다. 디자이너가 화면을 만들면 개발자가 그것을 코드로 다시 구현해야 했고, 그 과정에서 의도가 달라지거나 시간이 소요되었다. Figma Make는 이 간극을 줄이는 것을 목표로 한다. 디자이너가 직접 작동하는 프로토타입을 만들고, 팀이 더 빠르게 아이디어를 검증할 수 있게 하는 것이다.

---

### Figma Make의 핵심 기능

<svg width="100%" viewBox="0 0 640 280" xmlns="http://www.w3.org/2000/svg">
  <!-- 프롬프트 투 코드 -->
  <rect x="20" y="15" width="290" height="110" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="36" y="42" font-size="12" font-weight="600" fill="#3C3489">프롬프트 → 코드</text>
  <text x="36" y="62" font-size="11" fill="#534AB7">자연어로 UI와 인터랙션 요청</text>
  <text x="36" y="80" font-size="11" fill="#534AB7">"로그인 버튼 누르면 대시보드로</text>
  <text x="36" y="96" font-size="11" fill="#534AB7">이동하게 해줘"</text>
  <text x="36" y="114" font-size="10" fill="#7F77DD">코딩 지식 없이도 기능 구현 가능</text>

  <!-- 디자인 연결 -->
  <rect x="330" y="15" width="290" height="110" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="346" y="42" font-size="12" font-weight="600" fill="#3C3489">기존 디자인 연결</text>
  <text x="346" y="62" font-size="11" fill="#534AB7">피그마 프레임·컴포넌트를</text>
  <text x="346" y="80" font-size="11" fill="#534AB7">프롬프트 창에 붙여넣으면</text>
  <text x="346" y="96" font-size="11" fill="#534AB7">그 구조를 유지하며 작동하게 변환</text>
  <text x="346" y="114" font-size="10" fill="#7F77DD">Attach Design 버튼으로 파일 연결 가능</text>

  <!-- Point & Edit -->
  <rect x="20" y="145" width="290" height="110" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="172" font-size="12" font-weight="600" fill="#27500A">Point & Edit</text>
  <text x="36" y="192" font-size="11" fill="#3B6D11">미리보기에서 요소를 직접 클릭해</text>
  <text x="36" y="210" font-size="11" fill="#3B6D11">색상·폰트·간격 등 속성을</text>
  <text x="36" y="228" font-size="11" fill="#3B6D11">즉시 수정</text>
  <text x="36" y="246" font-size="10" fill="#639922">Go to source로 코드 직접 수정도 가능</text>

  <!-- 퍼블리싱 -->
  <rect x="330" y="145" width="290" height="110" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="346" y="172" font-size="12" font-weight="600" fill="#27500A">퍼블리싱</text>
  <text x="346" y="192" font-size="11" fill="#3B6D11">완성된 결과물을 전용 URL로</text>
  <text x="346" y="210" font-size="11" fill="#3B6D11">즉시 배포 가능</text>
  <text x="346" y="228" font-size="11" fill="#3B6D11">코드 없이 웹에 공개할 수 있음</text>
  <text x="346" y="246" font-size="10" fill="#639922">Full Seat 요금제 사용자만 가능 (현재)</text>
</svg>

<svg width="100%" viewBox="0 0 640 90" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="4"   y="20" width="100" height="50" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="54"  y="43" text-anchor="middle" font-size="10" font-weight="600" fill="#2C2C2A">디자인 파일</text>
  <text x="54"  y="58" text-anchor="middle" font-size="9" fill="#5F5E5A">또는 아이디어</text>
  <line x1="106" y1="45" x2="120" y2="45" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="122" y="20" width="100" height="50" rx="6" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="172" y="43" text-anchor="middle" font-size="10" font-weight="600" fill="#3C3489">프롬프트 입력</text>
  <text x="172" y="58" text-anchor="middle" font-size="9" fill="#534AB7">자연어로 요청</text>
  <line x1="224" y1="45" x2="238" y2="45" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="240" y="20" width="100" height="50" rx="6" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="290" y="43" text-anchor="middle" font-size="10" font-weight="600" fill="#3C3489">AI 코드 생성</text>
  <text x="290" y="58" text-anchor="middle" font-size="9" fill="#534AB7">Claude Sonnet</text>
  <line x1="342" y1="45" x2="356" y2="45" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="358" y="20" width="100" height="50" rx="6" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="408" y="43" text-anchor="middle" font-size="10" font-weight="600" fill="#27500A">수정·반복</text>
  <text x="408" y="58" text-anchor="middle" font-size="9" fill="#3B6D11">Point & Edit</text>
  <line x1="460" y1="45" x2="474" y2="45" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="476" y="20" width="158" height="50" rx="6" fill="#EAF3DE" stroke="#639922" stroke-width="1.5"/>
  <text x="555" y="43" text-anchor="middle" font-size="10" font-weight="600" fill="#27500A">퍼블리싱</text>
  <text x="555" y="58" text-anchor="middle" font-size="9" fill="#3B6D11">전용 URL로 배포</text>
</svg>

---

### 잘 쓰는 법
피그마 공식 블로그에서 정리한 핵심 팁들이다.

**① 첫 프롬프트에 디테일을 담아라**
두루뭉술하게 시작하면 수정 프롬프트가 많아진다. 처음부터 과업, 맥락, 핵심 디자인 요소, 예상 동작, 제약 조건을 함께 적는 것이 좋다. 실패하면 프롬프트를 다듬어서 새 파일로 다시 시작하는 것도 방법이다.

**② 디자인 파일을 정리하고 가져와라**
Auto Layout이 잘 세팅된 프레임은 Make에서도 잘 작동한다. 레이어 이름도 정리해 두면 AI가 구조를 더 정확하게 해석한다.

**③ 복잡한 요청은 단계별로 쪼개라**
한 번에 다 요청하는 것보다 작은 단위로 나눠서 순차적으로 요청하는 편이 결과가 좋다.

**④ 내 컴포넌트를 붙여 넣어라**
라이브러리의 컴포넌트를 프롬프트 창에 붙여 넣으면 Make가 해당 스타일과 간격을 참고해서 비슷한 분위기로 생성한다.

**⑤ Point & Edit으로 세부 조정하라**
색상, 폰트 크기 같은 시각적인 수정은 프롬프트보다 Point & Edit이 더 빠르다.

**⑥ 코드 탭에서 직접 수정도 가능하다**
코딩을 몰라도 Go to source로 특정 요소의 코드를 찾아가서 숫자 값을 바꾸는 정도는 가능하다. 수정 사항이 미리보기에 즉시 반영된다.

**⑦ 실제 데이터를 넣어서 테스트하라**
CSV 파일을 업로드하거나 실시간 API를 연결하면 더 현실적인 프로토타입 테스트가 가능하다.

**⑧ 개발자 핸드오프 도구로 쓸 수 있다**
Make에게 "이 인터랙션을 pseudocode로 설명해줘"라고 요청하면 개발자에게 넘겨줄 수 있는 설명을 생성할 수 있다.

---

### 기존 프로토타입과의 차이

<svg width="100%" viewBox="0 0 640 140" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="280" height="110" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="160" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">기존 피그마 프로토타입</text>
  <text x="160" y="62" text-anchor="middle" font-size="11" fill="#5F5E5A">화면 전환만 가능</text>
  <text x="160" y="80" text-anchor="middle" font-size="11" fill="#5F5E5A">실제 로직 구현 불가</text>
  <text x="160" y="98" text-anchor="middle" font-size="11" fill="#5F5E5A">클릭 흐름 시뮬레이션 수준</text>
  <text x="160" y="116" text-anchor="middle" font-size="10" fill="#888780">배포 불가</text>

  <rect x="340" y="15" width="280" height="110" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="480" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">Figma Make</text>
  <text x="480" y="62" text-anchor="middle" font-size="11" fill="#534AB7">실제 코드로 작동하는 UI</text>
  <text x="480" y="80" text-anchor="middle" font-size="11" fill="#534AB7">데이터 연동·조건 분기 가능</text>
  <text x="480" y="98" text-anchor="middle" font-size="11" fill="#534AB7">실사용 가능한 수준의 프로토타입</text>
  <text x="480" y="116" text-anchor="middle" font-size="10" fill="#7F77DD">전용 URL로 배포 가능</text>
</svg>

---

> [!tip]
> Figma Make는 디자이너가 개발자를 거치지 않고 아이디어를 검증할 수 있게 해 준다. 완벽한 앱을 만드는 도구가 아니라 빠르게 실험하는 도구로 이해하는 것이 좋다.

여기에서 오늘 실습 내용을 볼 수 있어요! [[17. Figma make를 사용해 보다]]