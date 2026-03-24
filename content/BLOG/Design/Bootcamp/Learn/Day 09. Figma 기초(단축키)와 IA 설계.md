---
date: 2026-03-11
---
오늘 수업의 핵심은 두 가지였다. 피그마라는 툴을 직접 써보는 것과, 화면을 만들기 전에 서비스의 정보 구조를 먼저 설계하는 IA 개념을 이해하는 것.

UI 디자인은 화면을 만드는 작업이 아니라, 사용자가 어떻게 정보를 탐색할지 설계하는 과정이 먼저다. 그 설계 도구가 IA이고, 그것을 실제로 구현하는 툴이 피그마다.

---

### Figma란

피그마는 UI/UX 디자인에서 가장 많이 사용되는 클라우드 기반 디자인 툴이다. 과거에는 포토샵이나 일러스트레이터 같은 그래픽 툴로 UI 작업을 했지만, 지금은 대부분의 작업이 피그마 중심으로 이루어지고 있다.

브라우저 기반으로 작업할 수 있고, 실시간 협업이 가능하며, 디자인과 프로토타입 제작을 한 툴에서 수행할 수 있다. 개발자와 디자인 스펙을 공유하는 것도 피그마 안에서 해결된다.

---

### Figma 단축키 (Mac)
자주 쓰는 것들을 카테고리별로 정리해 두었다.

<svg width="100%" viewBox="0 0 640 530" xmlns="http://www.w3.org/2000/svg">

  <!-- 도구 선택 -->
  <rect x="20" y="15" width="600" height="28" rx="6" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="36" y="34" font-size="11" font-weight="600" fill="#3C3489">도구 선택</text>

  <rect x="20" y="52" width="133" height="44" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="87" y="70" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">V</text>
  <text x="87" y="86" text-anchor="middle" font-size="10" fill="#5F5E5A">이동 도구</text>

  <rect x="163" y="52" width="133" height="44" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="230" y="70" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">F</text>
  <text x="230" y="86" text-anchor="middle" font-size="10" fill="#5F5E5A">프레임 도구</text>

  <rect x="306" y="52" width="133" height="44" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="373" y="70" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">R / O</text>
  <text x="373" y="86" text-anchor="middle" font-size="10" fill="#5F5E5A">사각형 / 타원</text>

  <rect x="449" y="52" width="171" height="44" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="534" y="70" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">T / P / I</text>
  <text x="534" y="86" text-anchor="middle" font-size="10" fill="#5F5E5A">텍스트 / 펜 / 스포이드</text>

  <!-- 복제 -->
  <rect x="20" y="112" width="600" height="28" rx="6" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="36" y="131" font-size="11" font-weight="600" fill="#0C447C">복제 (가장 많이 쓰는 기능)</text>

  <rect x="20" y="149" width="185" height="60" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="113" y="170" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Option + Drag</text>
  <text x="113" y="186" text-anchor="middle" font-size="10" fill="#5F5E5A">드래그하면서 즉시 복제</text>
  <text x="113" y="200" text-anchor="middle" font-size="10" fill="#5F5E5A">가장 자주 쓰는 방식</text>

  <rect x="218" y="149" width="185" height="60" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="311" y="170" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Shift + Option + Drag</text>
  <text x="311" y="186" text-anchor="middle" font-size="10" fill="#5F5E5A">수평/수직 방향 유지하며</text>
  <text x="311" y="200" text-anchor="middle" font-size="10" fill="#5F5E5A">복제</text>

  <rect x="416" y="149" width="204" height="60" rx="6" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="518" y="170" text-anchor="middle" font-size="11" font-weight="600" fill="#27500A">Cmd + D</text>
  <text x="518" y="186" text-anchor="middle" font-size="10" fill="#3B6D11">마지막 이동/복제 반복</text>
  <text x="518" y="200" text-anchor="middle" font-size="10" fill="#3B6D11">리스트·카드 배열에 유용</text>

  <!-- 레이어·그룹 -->
  <rect x="20" y="226" width="600" height="28" rx="6" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="245" font-size="11" font-weight="600" fill="#27500A">레이어·그룹 관리</text>

  <rect x="20" y="263" width="133" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="87" y="284" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Cmd + G</text>
  <text x="87" y="300" text-anchor="middle" font-size="10" fill="#5F5E5A">그룹 만들기</text>
  <text x="87" y="313" text-anchor="middle" font-size="9" fill="#888780">Cmd+Shift+G 해제</text>

  <rect x="163" y="263" width="133" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="230" y="284" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Cmd + ] / [</text>
  <text x="230" y="300" text-anchor="middle" font-size="10" fill="#5F5E5A">앞으로/뒤로 보내기</text>
  <text x="230" y="313" text-anchor="middle" font-size="9" fill="#888780">레이어 순서 조정</text>

  <rect x="306" y="263" width="133" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="373" y="284" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Cmd + R</text>
  <text x="373" y="300" text-anchor="middle" font-size="10" fill="#5F5E5A">이름 변경</text>
  <text x="373" y="313" text-anchor="middle" font-size="9" fill="#888780">레이어명 정리에 필수</text>

  <rect x="449" y="263" width="171" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="534" y="284" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Shift + S</text>
  <text x="534" y="300" text-anchor="middle" font-size="10" fill="#5F5E5A">Section 생성</text>
  <text x="534" y="313" text-anchor="middle" font-size="9" fill="#888780">화면 영역 구분</text>

  <!-- 오토레이아웃·보기 -->
  <rect x="20" y="336" width="600" height="28" rx="6" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="36" y="355" font-size="11" font-weight="600" fill="#412402">오토 레이아웃·보기</text>

  <rect x="20" y="373" width="185" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="113" y="394" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Shift + A</text>
  <text x="113" y="410" text-anchor="middle" font-size="10" fill="#5F5E5A">오토 레이아웃 생성</text>
  <text x="113" y="423" text-anchor="middle" font-size="9" fill="#888780">Shift+Option+A 해제</text>

  <rect x="218" y="373" width="185" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="311" y="394" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Cmd + Shift + O</text>
  <text x="311" y="410" text-anchor="middle" font-size="10" fill="#5F5E5A">아웃라인 보기</text>
  <text x="311" y="423" text-anchor="middle" font-size="9" fill="#888780">구조 확인에 유용</text>

  <rect x="416" y="373" width="204" height="56" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="518" y="394" text-anchor="middle" font-size="11" font-weight="600" fill="#2C2C2A">Cmd + \</text>
  <text x="518" y="410" text-anchor="middle" font-size="10" fill="#5F5E5A">레이어 패널 숨기기</text>
  <text x="518" y="423" text-anchor="middle" font-size="9" fill="#888780">작업 공간 확보</text>

  <!-- 화면 조작 -->
  <rect x="20" y="446" width="600" height="28" rx="6" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="36" y="465" font-size="11" font-weight="600" fill="#4A1B0C">화면 조작·기타</text>

  <rect x="20" y="483" width="133" height="40" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="87" y="499" text-anchor="middle" font-size="10" font-weight="600" fill="#2C2C2A">Space + Drag</text>
  <text x="87" y="514" text-anchor="middle" font-size="9" fill="#5F5E5A">화면 이동(팬)</text>

  <rect x="163" y="483" width="133" height="40" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="230" y="499" text-anchor="middle" font-size="10" font-weight="600" fill="#2C2C2A">Cmd + +/-</text>
  <text x="230" y="514" text-anchor="middle" font-size="9" fill="#5F5E5A">화면 확대/축소</text>

  <rect x="306" y="483" width="133" height="40" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="373" y="499" text-anchor="middle" font-size="10" font-weight="600" fill="#2C2C2A">Shift + 1</text>
  <text x="373" y="514" text-anchor="middle" font-size="9" fill="#5F5E5A">전체 화면 맞춤</text>

  <rect x="449" y="483" width="171" height="40" rx="6" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="534" y="499" text-anchor="middle" font-size="10" font-weight="600" fill="#2C2C2A">Shift + D</text>
  <text x="534" y="514" text-anchor="middle" font-size="9" fill="#5F5E5A">Dev Mode 전환</text>
</svg>

---

### IA(Information Architecture) — 정보 구조 설계

IA는 서비스에 있는 정보를 체계적으로 구조화하는 작업이다. 사용자가 원하는 정보를 찾을 수 있도록 메뉴와 기능의 관계를 정리하는 것이 핵심이다.

정보 구조가 잘 설계되어 있지 않으면 사용자는 아무리 기능이 좋아도 길을 잃는다. IA는 보통 사이트맵 형태의 다이어그램으로 표현되며, 서비스 전체 구조를 한눈에 볼 수 있게 해 준다.

<svg width="100%" viewBox="0 0 640 180" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="260" y="15" width="120" height="36" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="320" y="38" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">서비스 홈</text>

  <line x1="290" y1="51" x2="120" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="320" y1="51" x2="320" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="350" y1="51" x2="520" y2="85" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="40" y="85" width="120" height="36" rx="6" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="100" y="108" text-anchor="middle" font-size="11" fill="#0C447C">탐색</text>

  <rect x="260" y="85" width="120" height="36" rx="6" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="320" y="108" text-anchor="middle" font-size="11" fill="#0C447C">내 라이브러리</text>

  <rect x="480" y="85" width="120" height="36" rx="6" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="540" y="108" text-anchor="middle" font-size="11" fill="#0C447C">검색</text>

  <line x1="80" y1="121" x2="60" y2="148" stroke="#B4B2A9" stroke-width="0.8" marker-end="url(#arr)"/>
  <line x1="100" y1="121" x2="100" y2="148" stroke="#B4B2A9" stroke-width="0.8" marker-end="url(#arr)"/>
  <line x1="120" y1="121" x2="140" y2="148" stroke="#B4B2A9" stroke-width="0.8" marker-end="url(#arr)"/>

  <rect x="20" y="148" width="80" height="28" rx="4" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="60" y="166" text-anchor="middle" font-size="10" fill="#5F5E5A">차트</text>
  <rect x="60" y="148" width="80" height="28" rx="4" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="100" y="166" text-anchor="middle" font-size="10" fill="#5F5E5A">신보</text>
  <rect x="100" y="148" width="80" height="28" rx="4" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="0.8"/>
  <text x="140" y="166" text-anchor="middle" font-size="10" fill="#5F5E5A">장르/분위기</text>
</svg>

IA 설계의 목적은 서비스 전체 구조를 명확히 정리하고, 기능과 콘텐츠의 관계를 구조적으로 표현해 두는 것이다. 화면을 만들기 전에 이 지도가 있어야 어느 화면에 무엇을 넣을지 결정할 수 있다.

---

> [!tip]
> 화면을 만들기 전에 구조를 먼저 설계해야 한다.
> IA는 서비스라는 건물의 설계도이고, 피그마는 그것을 실제로 짓는 도구다.

여기에서 오늘의 실습 내용을 볼 수 있어요! [[09. 스포티파이 구조를 뜯어보니 보이는 것들]]