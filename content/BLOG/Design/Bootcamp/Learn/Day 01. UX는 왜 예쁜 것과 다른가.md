---
date: 2026-02-26
---
UX 수업 첫날, 강사님이 이런 질문을 던졌다.
"디자인이 뭐라고 생각하세요?"

나는 잠깐 멈췄다. 디자인을 공부했고, 지금 다시 디자인을 배우러 왔는데, 정작 이 질문에 바로 답이 나오지 않았다. '보기 좋게 만드는 것'이라고 말하려다가 그게 아닌 것 같아서.

첫날 수업의 핵심은 이 한 문장으로 요약된다.
> **디자인은 문제를 해결하는 과정이다. 예쁘게 만드는 일이 아니다.**

---

### 첫날 배운 네 가지 개념

<svg width="100%" height="320" viewBox="0 0 640 300" xmlns="http://www.w3.org/2000/svg">
  <!-- Lock-in -->
  <rect x="20" y="20" width="280" height="110" rx="10" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="36" y="50" font-size="13" font-weight="600" fill="#0C447C">🔒  Lock-in 효과</text>
  <text x="36" y="72" font-size="12" fill="#185FA5">사용자를 생태계 안에</text>
  <text x="36" y="89" font-size="12" fill="#185FA5">머물게 만드는 설계.</text>
  <text x="36" y="110" font-size="11" fill="#378ADD">예: 애플 기기 여러 개 → 나가기 싫어짐</text>

  <!-- 다크 패턴 -->
  <rect x="340" y="20" width="280" height="110" rx="10" fill="#FCEBEB" stroke="#E24B4A" stroke-width="1"/>
  <text x="356" y="50" font-size="13" font-weight="600" fill="#A32D2D">⚠️  다크 패턴</text>
  <text x="356" y="72" font-size="12" fill="#791F1F">사용자를 의도적으로</text>
  <text x="356" y="89" font-size="12" fill="#791F1F">헷갈리게 만드는 UI.</text>
  <text x="356" y="110" font-size="11" fill="#E24B4A">예: 탈퇴 버튼을 찾기 어렵게 숨김</text>

  <!-- 계층 구조 -->
  <rect x="20" y="165" width="280" height="110" rx="10" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="36" y="195" font-size="13" font-weight="600" fill="#27500A">📐  계층 구조 (Hierarchy)</text>
  <text x="36" y="217" font-size="12" fill="#3B6D11">무엇을 먼저 보여줄지</text>
  <text x="36" y="234" font-size="12" fill="#3B6D11">결정하는 설계 원칙.</text>
  <text x="36" y="255" font-size="11" fill="#639922">예: 크기·색·여백으로 우선순위 표현</text>

  <!-- 데이터 vs 미학 -->
  <rect x="340" y="165" width="280" height="110" rx="10" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="356" y="195" font-size="13" font-weight="600" fill="#412402">⚖️  데이터 vs 미학</text>
  <text x="356" y="217" font-size="12" fill="#633806">둘 중 하나만 믿으면</text>
  <text x="356" y="234" font-size="12" fill="#633806">위험하다. 균형이 핵심.</text>
  <text x="356" y="255" font-size="11" fill="#BA7517">예: 스포티파이의 디자인 실험들</text>
</svg>

---

### UX가 '예쁨'과 다른 이유

기능과 미학은 분리되지 않는다. **쓸 수 있어야 하고, 쓰고 싶어야 한다.** 
디터 람스는 "좋은 디자인은 가능한 한 덜 디자인된다"고 말했다. 장식이 없다는 게 아니라, 사용자의 목적 앞에 불필요한 것이 없다는 뜻이다.

카카오톡이 성공한 이유는 예뻐서가 아니라, 메시지를 전달하는 불편함을 빠르게 줄였기 때문이다.

---

### 데이터와 미학 사이

수업에서 함께 본 TED 강연 — [Rochelle King의 *The complex relationship between data and design in UX*](https://www.youtube.com/watch?v=YTRIeWI0EGQ) — 에서 이런 맥락이 나왔다. 디자이너가 데이터만 쫓으면 실험하는 용기를 잃고, 미학만 쫓으면 실제 사용자와 멀어진다. 아래는 그 균형을 나타낸 구조다.

<svg width="100%" viewBox="0 0 640 130" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <!-- 데이터 박스 -->
  <rect x="20" y="30" width="160" height="64" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="100" y="57" text-anchor="middle" font-size="13" font-weight="600" fill="#0C447C">데이터</text>
  <text x="100" y="76" text-anchor="middle" font-size="11" fill="#185FA5">사용자 행동 / 검증</text>

  <!-- 화살표 양방향 -->
  <line x1="182" y1="62" x2="248" y2="62" stroke="#888780" stroke-width="1" marker-end="url(#arr)" marker-start="url(#arr)"/>

  <!-- 균형 박스 -->
  <rect x="250" y="20" width="140" height="84" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="320" y="52" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">균형</text>
  <text x="320" y="70" text-anchor="middle" font-size="11" fill="#534AB7">좋은 UX의</text>
  <text x="320" y="86" text-anchor="middle" font-size="11" fill="#534AB7">출발점</text>

  <!-- 화살표 양방향 -->
  <line x1="392" y1="62" x2="458" y2="62" stroke="#888780" stroke-width="1" marker-end="url(#arr)" marker-start="url(#arr)"/>

  <!-- 미학 박스 -->
  <rect x="460" y="30" width="160" height="64" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="540" y="57" text-anchor="middle" font-size="13" font-weight="600" fill="#412402">미학</text>
  <text x="540" y="76" text-anchor="middle" font-size="11" fill="#633806">가설 / 영감 / 실험</text>
</svg>
---

> [!abstract] 
> - UX는 사람의 불안을 줄이는 일이다
> - 예쁜 화면이 아니라, 사용자가 지금 어디 있는지 알 수 있는 화면

여기에서 오늘의 실습 내용을 볼 수 있어요! [[01. 공동현관 인터폰이 불편한 진짜 이유 (애플 페이와 비교)]]