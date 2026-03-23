---
found: "[[05. 너구리 닌자 쿠로를 만들면서 배운 것]]"
date: 2026-03-05
---
DAY 4에 이미지를 만들었다면, DAY 5는 영상이었다. 도구는 [Sora](https://sora.chatgpt.com/explore)로, OpenAI가 만든 텍스트 기반 영상 생성 모델이다. 텍스트나 이미지를 입력하면 짧은 영상 클립을 생성해 준다.

---

### 핵심 개념 1 — 문제 정의는 여전히 인간의 영역

DAY 3, 4에 이어 DAY 5에서도 같은 결론이 반복되었다. AI 도구가 아무리 발전해도 "어떤 문제를 해결할 것인가"를 정의하는 과정은 디자이너의 역할이라는 것이다. 
영상 생성도 마찬가지였다. 어떤 이야기를 담을지, 어떤 캐릭터를 만들지 방향을 먼저 잡지 않으면 Sora는 그냥 아무 영상이나 만들어 낼 뿐이다.

---

### 핵심 개념 2 — 고정 프롬프트로 일관성을 만든다

영상은 이미지와 다르게 여러 장면이 이어지기 때문에 **캐릭터 일관성**이 중요하다. 장면마다 프롬프트를 새로 쓰면 같은 캐릭터라도 매번 다르게 생성될 수 있다. 
이를 해결하는 방법이 **고정 프롬프트**다. 캐릭터의 외형, 스타일, 분위기를 한 번 정의해두고 모든 장면 프롬프트에 공통으로 포함시키는 방식이다.

<svg width="100%" viewBox="0 0 640 150" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="20" y="30" width="160" height="80" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="100" y="62" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">고정 프롬프트</text>
  <text x="100" y="80" text-anchor="middle" font-size="11" fill="#534AB7">캐릭터 외형·스타일</text>
  <text x="100" y="96" text-anchor="middle" font-size="11" fill="#534AB7">분위기 정의</text>

  <line x1="182" y1="70" x2="218" y2="55" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="182" y1="70" x2="218" y2="95" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="220" y="20" width="160" height="45" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="300" y="40" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">장면 1 프롬프트</text>
  <text x="300" y="56" text-anchor="middle" font-size="10" fill="#185FA5">고정 프롬프트 + 장면 설명</text>

  <rect x="220" y="80" width="160" height="45" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="300" y="100" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">장면 2 프롬프트</text>
  <text x="300" y="116" text-anchor="middle" font-size="10" fill="#185FA5">고정 프롬프트 + 장면 설명</text>

  <line x1="382" y1="42" x2="418" y2="70" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="382" y1="102" x2="418" y2="76" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="420" y="45" width="180" height="55" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1.5"/>
  <text x="510" y="68" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">캐릭터 일관성 유지</text>
  <text x="510" y="86" text-anchor="middle" font-size="11" fill="#3B6D11">장면이 바뀌어도 같은 캐릭터</text>
</svg>

---

### AI 산업 이해 — 메타 영상 리뷰

[메타의 AI 전략에 관한 영상](https://www.youtube.com/watch?v=HHmie_P3ykY)을 보고 정리했다.

**1. AI 경쟁은 자본 + 인재 전쟁**
지금 AI 경쟁의 핵심은 기술력만이 아니다. GPU 확보, 데이터 확보, 연구 인재 확보가 동시에 요구되는 초거대 자본 산업으로 변하고 있다. 메타는 AI 인프라 투자, 데이터 라벨링 기업 투자, 글로벌 연구자 영입을 동시에 진행하고 있다.

**2. 나이가 아닌 문제 해결 능력 중심 리더십**
메타 AI 조직의 핵심 인물 중에는 1997년생 창업자도 포함되어 있다. 실리콘밸리에서는 연차나 나이보다 기술과 실행력이 리더십의 기준이 된다는 점이 인상적이었다.

**3. AGI 경쟁은 아직 베팅 단계**
기술 경쟁, 투자 경쟁, 규제 논쟁이 동시에 진행 중인 상황이다. 아직 확실한 승자가 없는 초기 경쟁 단계라고 볼 수 있다.

---

### 디자이너 관점에서 본 AI 변화

영상을 보면서 디자이너로서 정리한 변화다.

<svg width="100%" viewBox="0 0 640 260" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="185" height="80" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">① 모든 제품에 AI 탑재</text>
  <text x="112" y="60" text-anchor="middle" font-size="11" fill="#185FA5">앞으로 서비스는 AI 기능을</text>
  <text x="112" y="76" text-anchor="middle" font-size="11" fill="#185FA5">전제로 설계될 가능성이 높다</text>

  <rect x="228" y="15" width="185" height="80" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="320" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">② UX 중심의 이동</text>
  <text x="320" y="60" text-anchor="middle" font-size="11" fill="#185FA5">인터페이스 중심 →</text>
  <text x="320" y="76" text-anchor="middle" font-size="11" fill="#185FA5">추천·예측·개인화 중심</text>

  <rect x="436" y="15" width="184" height="80" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="528" y="42" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">③ 데이터 = UX 품질</text>
  <text x="528" y="60" text-anchor="middle" font-size="11" fill="#185FA5">AI 서비스에서 데이터 품질이</text>
  <text x="528" y="76" text-anchor="middle" font-size="11" fill="#185FA5">곧 경험의 품질이 된다</text>

  <rect x="20" y="115" width="185" height="80" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="112" y="142" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">④ 속도와 실험이 경쟁력</text>
  <text x="112" y="160" text-anchor="middle" font-size="11" fill="#3B6D11">빠른 프로토타이핑이 가능해진</text>
  <text x="112" y="176" text-anchor="middle" font-size="11" fill="#3B6D11">만큼 반복 실험 능력이 중요</text>

  <rect x="228" y="115" width="390" height="80" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1.5"/>
  <text x="423" y="142" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">⑤ 기술 이해도가 높은 디자이너의 가치 상승</text>
  <text x="423" y="160" text-anchor="middle" font-size="11" fill="#534AB7">AI 모델, 추천 시스템, 데이터 구조를 이해하는 디자이너는</text>
  <text x="423" y="176" text-anchor="middle" font-size="11" fill="#534AB7">제품 전략에 더 깊이 참여할 수 있다</text>
</svg>
---

> [!tip]
> AI 시대의 디자이너는 화면을 만드는 사람이 아니라 지능이 작동하는 경험을 설계하는 사람으로 변화하고 있다.