---
date: 2026-03-04
---
[미드저니](https://www.midjourney.com/explore?tab=top)를 처음 써본 날이었다. 텍스트 몇 줄로 이미지가 나온다는 건 알고 있었는데, 막상 해보니 그냥 말 한마디로 뚝딱 되는 게 아니었다. 원하는 걸 만들려면 꽤 알아야 할 게 있었다.

---

### 미드저니 기본 설정

이미지를 생성하기 전에 결과에 영향을 주는 설정들을 먼저 파악해야 한다. 같은 프롬프트라도 이 값들을 어떻게 잡느냐에 따라 결과가 꽤 많이 달라진다.

<svg width="100%" viewBox="0 0 640 260" xmlns="http://www.w3.org/2000/svg">
  <!-- Aspect Ratio -->
  <rect x="20" y="15" width="185" height="100" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="112" y="42" text-anchor="middle" font-size="13" font-weight="600" fill="#0C447C">Aspect Ratio</text>
  <text x="112" y="62" text-anchor="middle" font-size="11" fill="#185FA5">이미지 화면 비율 설정</text>
  <text x="112" y="80" text-anchor="middle" font-size="11" fill="#185FA5">16:9 / 1:1 / 9:16 등</text>
  <text x="112" y="98" text-anchor="middle" font-size="11" fill="#185FA5">용도에 맞게 먼저 설정</text>

  <!-- Model -->
  <rect x="228" y="15" width="185" height="100" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="320" y="42" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">Model</text>
  <text x="320" y="62" text-anchor="middle" font-size="11" fill="#534AB7">standard: 미드저니 감성</text>
  <text x="320" y="80" text-anchor="middle" font-size="11" fill="#534AB7">raw: 프롬프트에 충실</text>
  <text x="320" y="98" text-anchor="middle" font-size="11" fill="#7F77DD">현재 최신 버전 v7</text>

  <!-- Stylization -->
  <rect x="436" y="15" width="184" height="100" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="528" y="42" text-anchor="middle" font-size="13" font-weight="600" fill="#27500A">Stylization</text>
  <text x="528" y="62" text-anchor="middle" font-size="11" fill="#3B6D11">예술적 스타일 강도</text>
  <text x="528" y="80" text-anchor="middle" font-size="11" fill="#3B6D11">높을수록 AI 해석이</text>
  <text x="528" y="98" text-anchor="middle" font-size="11" fill="#3B6D11">강하게 개입됨</text>

  <!-- Weirdness -->
  <rect x="20" y="140" width="185" height="100" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="112" y="167" text-anchor="middle" font-size="13" font-weight="600" fill="#412402">Weirdness</text>
  <text x="112" y="187" text-anchor="middle" font-size="11" fill="#633806">실험적·독특한</text>
  <text x="112" y="205" text-anchor="middle" font-size="11" fill="#633806">표현 정도</text>
  <text x="112" y="223" text-anchor="middle" font-size="11" fill="#633806">높일수록 예측 불가능</text>

  <!-- Variety -->
  <rect x="228" y="140" width="185" height="100" rx="8" fill="#FAECE7" stroke="#D85A30" stroke-width="1"/>
  <text x="320" y="167" text-anchor="middle" font-size="13" font-weight="600" fill="#4A1B0C">Variety (Chaos)</text>
  <text x="320" y="187" text-anchor="middle" font-size="11" fill="#712B13">결과 이미지의 다양성</text>
  <text x="320" y="205" text-anchor="middle" font-size="11" fill="#712B13">높을수록 4개 결과가</text>
  <text x="320" y="223" text-anchor="middle" font-size="11" fill="#712B13">서로 많이 달라짐</text>

  <!-- 팁 박스 -->
  <rect x="436" y="140" width="184" height="100" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="528" y="167" text-anchor="middle" font-size="13" font-weight="600" fill="#2C2C2A">조합의 묘미</text>
  <text x="528" y="187" text-anchor="middle" font-size="11" fill="#5F5E5A">같은 프롬프트라도</text>
  <text x="528" y="205" text-anchor="middle" font-size="11" fill="#5F5E5A">설정값에 따라</text>
  <text x="528" y="223" text-anchor="middle" font-size="11" fill="#5F5E5A">결과가 크게 달라짐</text>
</svg>

---

### 프롬프트 작성법

미드저니 프롬프트는 자연어처럼 쓰기보다 **키워드를 조합하는 방식**이 더 효과적이다. 어떤 피사체인지, 어떤 스타일인지, 카메라·조명 연출은 어떻게 할지를 순서대로 쌓아가는 식이다.

<svg width="100%" viewBox="0 0 640 130" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#888780" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  <rect x="20" y="25" width="110" height="50" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="75" y="47" text-anchor="middle" font-size="12" font-weight="600" fill="#0C447C">피사체</text>
  <text x="75" y="65" text-anchor="middle" font-size="10" fill="#185FA5">무엇을 그릴지</text>
  <line x1="132" y1="50" x2="155" y2="50" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="157" y="25" width="110" height="50" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="212" y="47" text-anchor="middle" font-size="12" font-weight="600" fill="#3C3489">스타일</text>
  <text x="212" y="65" text-anchor="middle" font-size="10" fill="#534AB7">어떤 분위기로</text>
  <line x1="269" y1="50" x2="292" y2="50" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="294" y="25" width="110" height="50" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="349" y="47" text-anchor="middle" font-size="12" font-weight="600" fill="#27500A">조명·카메라</text>
  <text x="349" y="65" text-anchor="middle" font-size="10" fill="#3B6D11">연출 방식</text>
  <line x1="406" y1="50" x2="429" y2="50" stroke="#B4B2A9" stroke-width="1" marker-end="url(#arr)"/>

  <rect x="431" y="25" width="110" height="50" rx="8" fill="#FAEEDA" stroke="#BA7517" stroke-width="1"/>
  <text x="486" y="47" text-anchor="middle" font-size="12" font-weight="600" fill="#412402">품질·비율</text>
  <text x="486" y="65" text-anchor="middle" font-size="10" fill="#633806">4K, --ar 16:9 등</text>

  <text x="320" y="112" text-anchor="middle" font-size="11" fill="#888780">ChatGPT로 프롬프트 문장을 다듬은 뒤 미드저니에 입력하는 방식도 효과적이다</text>
</svg>

---

### 레퍼런스 탐색 → 프롬프트 → 생성 → 선택

이번 수업에서 중요하게 다룬 건 이미지 하나를 생성하는 게 아니라 이 **흐름 전체**를 경험하는 거였다. Pinterest에서 원하는 스타일을 먼저 탐색하고, 그걸 언어로 번역해 프롬프트로 만들고, 여러 결과 중에서 방향에 맞는 이미지를 고르는 판단까지. 이 과정이 디자이너가 AI를 쓰는 방식에 가깝다.

> [!tip]
> 생성형 AI는 디자인을 대신하는 도구가 아니라, 아이디어 실험 속도를 높여주는 도구.
> 결국 중요한 건 무엇을 만들고 싶은지 명확하게 생각하는 능력이다.

여기에서 오늘의 실습 내용을 볼 수 있어요! [[04. 프롬프트를 100번 고치면서 느낀 것]]