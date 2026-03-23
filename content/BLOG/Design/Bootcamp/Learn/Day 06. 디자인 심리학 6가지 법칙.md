---
found: "[[06. 유튜브가 탭 한 번에 컨트롤러를 숨기는 이유]]"
date: 2026-03-06
---
좋은 디자인은 보기 좋은 화면을 만드는 것이 아니라, 사람의 인지 방식에 맞춰 경험을 설계하는 일이다. 이번 수업에서는 디자인 심리학 법칙들을 배우면서, 사용자가 인터페이스를 어떻게 보고 이해하고 기억하는지 생각해 볼 수 있었다.

사용자는 화면을 요소 하나하나로 읽지 않는다. 익숙한 방식으로 예측하고, 덩어리로 이해하고, 강렬했던 순간과 마지막 순간을 더 오래 기억한다.

---

### 법칙 1 — 제이콥의 법칙 (Jakob's Law)

익숙한 것이 더 쉽게 느껴진다.

사람들은 대부분의 시간을 다른 앱이나 웹사이트를 사용하면서 보내기 때문에, 새로운 서비스도 이미 익숙한 방식으로 작동하길 기대한다. 그래서 완전히 새로운 구조를 만드는 것보다 사용자가 이미 알고 있는 인터페이스 패턴을 존중하는 것이 중요하다.

로고를 클릭하면 홈으로 돌아가는 패턴이 대표적인 예다. 사용자는 이미 이 패턴을 학습해 두었기 때문에, 새로운 서비스에서도 같은 방식으로 작동할 것이라고 기대한다. 이 기대를 무시하면 기능이 있어도 불편하게 느껴진다.

---

### 법칙 2 — 힉의 법칙 (Hick's Law)

선택지가 많아질수록 결정은 느려진다.

선택지가 많으면 사용자는 무엇을 골라야 할지 고민하게 되고, 그만큼 행동까지 이어지는 시간이 길어진다. 반대로 필요한 선택지만 명확하게 보여 주면 사용자는 더 빠르게 행동할 수 있다. 
핵심은 무조건 적게 보여 주는 것이 아니라, 불필요한 선택을 줄이고 필요한 선택은 구조화해서 보여 주는 것이다.

---

### 법칙 3 — 밀러의 법칙 (Miller's Law)

사람은 정보를 덩어리로 기억한다.

많은 정보를 개별 항목으로 처리하기보다, 의미 있는 청크(chunk)로 묶어서 이해할 때 더 쉽게 기억한다. 카드형 UI, 리스트 그룹, 단계별 프로세스처럼 정보를 작은 덩어리로 나누어 보여 주는 방식이 여기서 나온다. 
정보 설계에서 중요한 것은 '어떻게 묶어서 보여 주는가'다.

---

### 법칙 4 — 피크-엔드 법칙 (Peak-End Rule)

사람은 모든 순간을 똑같이 기억하지 않는다.

어떤 경험 전체를 균등하게 기억하기보다 가장 강렬했던 순간과 마지막 순간을 중심으로 기억한다. 그래서 서비스 경험을 설계할 때는 기능이 잘 작동하는 것뿐 아니라 사용자가 기억하게 될 순간을 어떻게 만들 것인지도 중요하다. 
듀오링고가 학습이 끝났을 때 축하 애니메이션을 보여 주는 것이 이 원리를 잘 활용한 사례다. 
좋은 서비스는 하이라이트가 있고 끝맺음이 좋은 경험을 만든 서비스다.

---

### 법칙 5 — 폰 레스토프 효과 (Von Restorff Effect)

다른 하나는 더 잘 기억된다.

비슷한 항목들이 늘어선 상황에서 유독 다르게 보이는 하나가 더 쉽게 눈에 들어오고 기억에 남는다. CTA 버튼, 강조 배지, 핵심 가격 정보가 튀게 설계되는 이유도 여기에 있다. 강조 디자인은 단순한 장식이 아니라 사용자의 시선을 안내하는 역할을 한다.

---

### 법칙 6 — 게슈탈트 이론 (Gestalt Principles)

사람은 조각보다 패턴을 먼저 본다.

사람들은 사물을 개별 요소의 합으로 보기보다 전체적인 패턴이나 구조로 인식한다. 그래서 요소들을 단순히 나열하기보다 관계를 고려해 배치하는 것이 중요하다.

<svg width="100%" viewBox="0 0 640 280" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="185" height="75" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="40" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">근접성</text>
  <text x="112" y="58" text-anchor="middle" font-size="11" fill="#185FA5">가까운 요소는 같은 그룹으로</text>
  <text x="112" y="74" text-anchor="middle" font-size="11" fill="#185FA5">인식된다</text>

  <rect x="228" y="15" width="185" height="75" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="320" y="40" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">유사성</text>
  <text x="320" y="58" text-anchor="middle" font-size="11" fill="#185FA5">비슷하게 생긴 것들은</text>
  <text x="320" y="74" text-anchor="middle" font-size="11" fill="#185FA5">같은 그룹으로 묶인다</text>

  <rect x="436" y="15" width="184" height="75" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="528" y="40" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">대응성</text>
  <text x="528" y="58" text-anchor="middle" font-size="11" fill="#185FA5">같은 방향으로 움직이는</text>
  <text x="528" y="74" text-anchor="middle" font-size="11" fill="#185FA5">요소는 같은 그룹으로 인식</text>

  <rect x="20" y="110" width="185" height="75" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="112" y="135" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">연속성</text>
  <text x="112" y="153" text-anchor="middle" font-size="11" fill="#3B6D11">시선을 끊기지 않고</text>
  <text x="112" y="169" text-anchor="middle" font-size="11" fill="#3B6D11">자연스럽게 안내한다</text>

  <rect x="228" y="110" width="185" height="75" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="320" y="135" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">폐쇄성</text>
  <text x="320" y="153" text-anchor="middle" font-size="11" fill="#3B6D11">불완전한 정보를 뇌가</text>
  <text x="320" y="169" text-anchor="middle" font-size="11" fill="#3B6D11">스스로 완성해서 인식한다</text>

  <rect x="436" y="110" width="184" height="75" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="528" y="135" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">전경-배경</text>
  <text x="528" y="153" text-anchor="middle" font-size="11" fill="#3B6D11">사용자 시선을 어디에</text>
  <text x="528" y="169" text-anchor="middle" font-size="11" fill="#3B6D11">집중시킬지 결정한다</text>

  <rect x="120" y="205" width="400" height="60" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="0.8"/>
  <text x="320" y="228" text-anchor="middle" font-size="12" font-weight="600" fill="#412402">요소들을 나열하는 것이 아니라</text>
  <text x="320" y="248" text-anchor="middle" font-size="11" fill="#633806">관계를 고려해 배치해야 사용자가 자연스럽게 이해한다</text>
</svg>

---

### 인지부하와 디자인

최고의 사용자 경험은 사용자가 디자인에 대해 생각하지 않도록 만드는 것에서 시작된다. 
인지부하(Cognitive Load)란 뇌가 정보를 처리하는 데 드는 정신적 노력의 양을 말한다. 서비스가 복잡하고 혼란스러울수록 사용자는 끊임없이 "이 버튼은 무슨 기능이지?", "다음 단계로 가려면 뭘 해야 하지?" 같은 질문을 던지게 된다.

좋은 UX 디자인은 사용자가 문제를 해결하도록 강요하는 것이 아니라, 문제가 생기지 않도록 미리 예방한다. 인지부하를 줄이는 방법은 위에서 배운 법칙들과 그대로 연결된다. 
힉의 법칙처럼 선택지를 줄이고, 게슈탈트 원리처럼 시각적 계층 구조를 명확히 하고, 제이콥의 법칙처럼 익숙한 패턴을 존중하는 것. 
유튜브에서 영상 시청 중 화면을 한 번 탭하면 컨트롤러가 나타나고 다시 탭하면 사라지는 것처럼, 사용자가 필요한 순간에 필요한 것이 자연스럽게 나타나는 경험이 그것이다.

---

### TED 강연 리뷰 — 도널드 노먼, 좋은 디자인이 행복을 만드는 3가지 방법
[강연 영상](https://www.ted.com/talks/don_norman_3_ways_good_design_makes_you_happy)
디자인 비평가 도널드 노먼은 좋은 디자인이 사람에게 행복감을 주는 이유를 세 가지 감정적 경험 수준으로 설명한다.
<svg width="100%" viewBox="0 0 640 160" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="20" y="30" width="175" height="90" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="107" y="62" text-anchor="middle" font-size="13" font-weight="600" fill="#4A1B0C">본능적 디자인</text>
  <text x="107" y="80" text-anchor="middle" font-size="11" fill="#712B13">처음 봤을 때 느끼는</text>
  <text x="107" y="96" text-anchor="middle" font-size="11" fill="#712B13">즉각적인 감정</text>
  <text x="107" y="112" text-anchor="middle" font-size="10" fill="#D85A30">색상, 형태, 질감</text>

  <line x1="197" y1="75" x2="223" y2="75" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="225" y="20" width="175" height="110" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="312" y="55" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">행동적 디자인</text>
  <text x="312" y="73" text-anchor="middle" font-size="11" fill="#534AB7">실제 사용하는 과정에서</text>
  <text x="312" y="89" text-anchor="middle" font-size="11" fill="#534AB7">느끼는 경험</text>
  <text x="312" y="112" text-anchor="middle" font-size="10" fill="#7F77DD">쉽고 직관적인 사용감</text>

  <line x1="402" y1="75" x2="428" y2="75" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="430" y="30" width="185" height="90" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="522" y="62" text-anchor="middle" font-size="13" font-weight="600" fill="#27500A">반성적 디자인</text>
  <text x="522" y="80" text-anchor="middle" font-size="11" fill="#3B6D11">사용 후에 남는</text>
  <text x="522" y="96" text-anchor="middle" font-size="11" fill="#3B6D11">기억과 의미</text>
  <text x="522" y="112" text-anchor="middle" font-size="10" fill="#639922">브랜드, 가치관과의 연결</text>
</svg>
강연을 보면서 디자인은 단순히 문제를 해결하는 기술이 아니라 사용자의 감정과 기억을 설계하는 일이라는 점을 다시 느꼈다. 기능이 좋아도 첫인상이 차갑거나, 사용 과정이 번거롭거나, 사용 후에 아무 기억도 남지 않는다면 그 경험은 오래 남지 않는다. 
특히 오늘 배운 피크-엔드 법칙과도 연결되는 지점이었다. 
결국 디자인은 기능만 잘 작동하게 만드는 데서 끝나는 것이 아니라, 어디에서 감정을 만들고 어떻게 마무리할 것인가까지 고민해야 한다.


> [!tip]
> 디자이너는 화면을 정리하는 사람이 아니라 사람의 인지와 감정을 다루는 설계자에 더 가깝다