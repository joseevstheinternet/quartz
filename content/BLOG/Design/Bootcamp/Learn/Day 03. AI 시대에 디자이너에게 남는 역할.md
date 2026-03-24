---
date: 2026-03-03
---
AI가 이미지를 만들고, 영상을 만들고, 코드를 짜는 시대에 디자이너는 뭘 하는 사람인가 — 이것이 DAY 3 수업의 중심 질문이었다.

결론부터 말하면, AI는 제작 속도를 높여주는 도구이지 문제를 정의해주는 도구가 아니다. "어떤 문제를 풀 것인가"는 여전히 사람이 결정해야 한다. 아무리 좋은 AI 도구가 있어도 방향이 잘못 설정된 채로 빠르게 만들면, 그냥 잘못된 걸 빠르게 만드는 것뿐이다.

---

### AI 도구의 종류와 역할

요즘 AI 도구들이 너무 많이 나와서 뭐가 뭔지 헷갈리는데, 수업에서는 크게 두 가지 방식으로 정리했다.

<svg width="100%" viewBox="0 0 640 150" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <!-- 딥 리서치 -->
  <rect x="20" y="20" width="270" height="110" rx="10" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="36" y="50" font-size="13" font-weight="600" fill="#0C447C">딥 리서치 (Deep Research)</text>
  <text x="36" y="72" font-size="12" fill="#185FA5">흩어진 자료에서 핵심 정보를</text>
  <text x="36" y="89" font-size="12" fill="#185FA5">찾아 구조화해주는 방식.</text>
  <text x="36" y="113" font-size="11" fill="#378ADD">→ 리서치·정보 수집 중심</text>

  <!-- 추론 모델 -->
  <rect x="350" y="20" width="270" height="110" rx="10" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="366" y="50" font-size="13" font-weight="600" fill="#3C3489">추론 모델 (Reasoning)</text>
  <text x="366" y="72" font-size="12" fill="#534AB7">단순 검색이 아니라 논리를</text>
  <text x="366" y="89" font-size="12" fill="#534AB7">기반으로 결론을 도출하는 모델.</text>
  <text x="366" y="113" font-size="11" fill="#7F77DD">→ 사고 보조·의사결정 도구</text>
</svg>

두 가지 모두 디자이너가 쓸 수 있는 도구이지만, 결국 어떤 질문을 던지느냐에 따라 결과가 갈린다. AI한테 "뭘 만들어야 해?"라고 물어봤자 답이 안 나온다. "이 사용자의 이 문제를 이런 방식으로 풀고 싶은데, 어떤 레퍼런스가 있어?"라고 물어야 쓸 만한 대답이 나온다.

---

### 프롬프트가 곧 기획이다

수업에서 **메타 프롬프트** 개념을 배웠다. 단순히 "이거 만들어 줘"라고 입력하는 게 아니라, 원하는 결과를 얻기 위한 프롬프트 구조 자체를 먼저 설계하는 방식이다.

이걸 들으면서 든 생각은, 프롬프트를 잘 쓰는 능력이 결국 기획 능력이랑 크게 다르지 않다는 거였다. 맥락을 정확히 설정하고, 조건을 구체적으로 제시하고, 원하는 결과의 형식을 명시하는 것 — AI한테도, 팀원한테도 잘 전달하는 방식이다.

---

### AI 시대 디자이너의 역할 변화

수업에서 본 메타 AI 관련 영상이 인상적이었던 건 단순히 AI 기술 이야기가 아니라 디자이너의 역할이 어떻게 바뀌는지에 대한 힌트가 담겨 있었기 때문이다.

<svg width="100%" viewBox="0 0 640 240" xmlns="http://www.w3.org/2000/svg">
  <!-- as-is -->
  <rect x="20" y="20" width="280" height="200" rx="10" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="160" y="50" text-anchor="middle" font-size="12" font-weight="600" fill="#5F5E5A">기존 UX의 중심</text>
  <text x="160" y="78" text-anchor="middle" font-size="13" fill="#2C2C2A">버튼, 화면, 흐름</text>
  <text x="160" y="100" text-anchor="middle" font-size="13" fill="#2C2C2A">정보 구조 설계</text>
  <text x="160" y="122" text-anchor="middle" font-size="13" fill="#2C2C2A">인터랙션 패턴</text>
  <text x="160" y="144" text-anchor="middle" font-size="13" fill="#2C2C2A">시각적 일관성</text>
  <text x="160" y="200" text-anchor="middle" font-size="11" fill="#888780">인터페이스 중심</text>

  <!-- to-be -->
  <rect x="340" y="20" width="280" height="200" rx="10" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="480" y="50" text-anchor="middle" font-size="12" font-weight="600" fill="#534AB7">AI 시대 UX의 중심</text>
  <text x="480" y="78" text-anchor="middle" font-size="13" fill="#26215C">추천, 예측, 자동 생성</text>
  <text x="480" y="100" text-anchor="middle" font-size="13" fill="#26215C">개인화 경험 설계</text>
  <text x="480" y="122" text-anchor="middle" font-size="13" fill="#26215C">AI 행동의 이해 가능성</text>
  <text x="480" y="144" text-anchor="middle" font-size="13" fill="#26215C">데이터 기반 경험</text>
  <text x="480" y="200" text-anchor="middle" font-size="11" fill="#7F77DD">지능 중심</text>
</svg>

결국 디자이너가 설계하는 대상이 '화면'에서 '지능이 작동하는 경험'으로 이동하고 있다는 거다. 그리고 그 변화 속에서 기술 이해도가 높은 디자이너—AI 모델이 어떻게 작동하는지, 데이터가 어떻게 흐르는지를 아는 디자이너—가 제품 전략에 더 깊이 참여할 수 있게 된다.

나는 개발자 경력이 있으니까, 그 경험이 여기서 연결될 수도 있겠다는 생각이 들었다.

---

### 사례 분석 — 왓챠피디아의 AI 추천 시스템

![[Pasted image 20260323213912.png|400]]

[왓챠피디아](https://pedia.watcha.com/ko-KR)는 사용자가 평가한 콘텐츠 데이터를 기반으로 특정 작품에 줄 가능성이 높은 별점을 예측해 준다. 단순한 추천 기능처럼 보이지만, UX 관점에서 보면 꽤 흥미로운 설계다.

몇십 개만 평가해도 개인 취향에 맞는 콘텐츠 추천이 가능하고, 추천 정확도가 높아질수록 사용자는 더 많이 평가하게 된다. 평가가 쌓일수록 추천이 더 정확해지는 구조라 데이터가 UX를 만들고, 그 UX가 다시 데이터를 만드는 루프다. 이 시스템은 이후 OTT 서비스 왓챠의 콘텐츠 큐레이션에도 그대로 연결됐다.

AI 서비스에서 **데이터 품질 = UX 품질**이라는 말이 여기에서 실감됐다.

---

### 영상 리뷰 — 우아한형제들의 AI 디자인 활용

우아한형제들 디자인 팀이 생성형 AI Firefly를 어떻게 쓰는지에 대한 웨비나 영상을 봤다.
[https://www.youtube.com/watch?v=DSeJR0G88yk](https://www.youtube.com/watch?v=DSeJR0G88yk)

기존에는 촬영 → 수천 장 중 선택 → 수백 번 채널 테스트 → 반복 수정이 필요했는데, Firefly를 활용하면서 한 장의 사진으로 다양한 배리에이션을 만들고, 기존 캐릭터 자산을 기반으로 새로운 오브젝트를 빠르게 제작할 수 있게 됐다고 한다.

인상적이었던 건 AI가 브랜드 아이덴티티를 **대체**하는 게 아니라 **확장** 도구로 쓰인다는 점이었다. 배민의 스컬피 스타일을 유지하면서 AI로 다양한 실험이 가능해진 것처럼, 결국 결과물을 선택하고 방향을 잡는 건 여전히 사람의 역할이다.

<svg width="100%" viewBox="0 0 640 120" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="20" y="25" width="160" height="60" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="100" y="50" text-anchor="middle" font-size="12" font-weight="600" fill="#2C2C2A">브랜드 아이덴티티</text>
  <text x="100" y="68" text-anchor="middle" font-size="11" fill="#5F5E5A">디자이너가 정의</text>

  <line x1="182" y1="55" x2="218" y2="55" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="220" y="15" width="180" height="80" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="310" y="45" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">AI (Firefly)</text>
  <text x="310" y="63" text-anchor="middle" font-size="11" fill="#3B6D11">배리에이션 생성</text>
  <text x="310" y="79" text-anchor="middle" font-size="11" fill="#3B6D11">실험 속도 ↑</text>

  <line x1="402" y1="55" x2="438" y2="55" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="440" y="25" width="175" height="60" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="527" y="50" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">최종 선택·판단</text>
  <text x="527" y="68" text-anchor="middle" font-size="11" fill="#534AB7">다시 디자이너의 역할</text>
</svg>
---

> [!tip]
> AI가 제작을 담당하는 시대일수록, 디자이너에게 남는 건 "무엇을 만들 것인가"를 결정하는 능력이다.

여기에서 오늘의 실습 내용을 볼 수 있어요! [[03. 집중 앱을 기획하면서 발견한 것]]