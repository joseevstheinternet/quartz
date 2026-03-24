---
date: 2026-03-16
---
웹은 하나의 화면이 아니라 여러 환경에서 동작하는 구조다. 디자인은 고정이 아니라 유동적으로 변해야 한다. 그래서 반응형 + 오토 레이아웃 + 컴포넌트가 필요하다.

---

### 웹의 변화 흐름

웹의 핵심 변화를 한 줄로 요약하면 **소비 → 참여 → 소유** 의 흐름이다. 초기 웹은 정보를 읽기만 하는 공간이었다면, 지금은 사용자가 직접 콘텐츠를 만들고 소유하는 방향으로 진화했다. 이 변화는 UI 설계에도 그대로 영향을 미친다. 읽기 전용 화면을 만드는 것과 상호작용하는 화면을 만드는 것은 설계 방식 자체가 다르다.

---

### 웹의 기본 구조

웹사이트의 구조는 단순한 UI 배치가 아니라 사용자의 이동 경로를 설계하는 일이다. 브레드크럼(Breadcrumb)이 대표적인 예다. "홈 > 카테고리 > 상품"처럼 지금 어디 있는지 알려주는 이 구조는, 사용자가 길을 잃지 않도록 돕는 내비게이션 장치다.

![[Pasted image 20260324115949.png|브레드크럼]]
*브레드크럼 예시*

![[Pasted image 20260324120019.png]]
*웹사이트 구조 예시*

---

### PC vs 모바일

같은 콘텐츠라도 화면마다 다르게 보인다. PC와 모바일은 화면 크기뿐 아니라 조작 방식 자체가 다르다. PC는 마우스 호버, 모바일은 터치. 이 차이가 UI 설계 전체에 영향을 미친다.

<svg width="100%" viewBox="0 0 640 180" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="280" height="140" rx="8" fill="#E6F1FB" stroke="#378ADD" stroke-width="1"/>
  <text x="160" y="50" text-anchor="middle" font-size="13" font-weight="600" fill="#0C447C">PC 웹</text>
  <text x="160" y="74" text-anchor="middle" font-size="11" fill="#185FA5">넓은 화면 → 정보 밀도 높음</text>
  <text x="160" y="92" text-anchor="middle" font-size="11" fill="#185FA5">마우스 호버 인터랙션 가능</text>
  <text x="160" y="110" text-anchor="middle" font-size="11" fill="#185FA5">12컬럼 그리드 활용</text>
  <text x="160" y="128" text-anchor="middle" font-size="11" fill="#185FA5">사이드바·멀티 컬럼 레이아웃</text>
  <text x="160" y="148" text-anchor="middle" font-size="10" fill="#378ADD">기준 너비: 1280px / 1920px</text>

  <rect x="340" y="20" width="280" height="140" rx="8" fill="#EAF3DE" stroke="#639922" stroke-width="1"/>
  <text x="480" y="50" text-anchor="middle" font-size="13" font-weight="600" fill="#27500A">모바일 웹</text>
  <text x="480" y="74" text-anchor="middle" font-size="11" fill="#3B6D11">좁은 화면 → 정보 우선순위 중요</text>
  <text x="480" y="92" text-anchor="middle" font-size="11" fill="#3B6D11">터치 인터랙션 중심</text>
  <text x="480" y="110" text-anchor="middle" font-size="11" fill="#3B6D11">4~6컬럼 그리드 활용</text>
  <text x="480" y="128" text-anchor="middle" font-size="11" fill="#3B6D11">단일 컬럼 레이아웃 중심</text>
  <text x="480" y="148" text-anchor="middle" font-size="10" fill="#639922">기준 너비: 375px / 390px</text>
</svg>

같은 UI가 그대로 유지되지 않기 때문에 레이아웃 깨짐과 정보 전달 실패가 일어난다. 이것을 해결하는 방법이 반응형 디자인이다.

---

### 반응형 vs 적응형

<svg width="100%" viewBox="0 0 640 190" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="15" width="290" height="160" rx="8" fill="#EEEDFE" stroke="#7F77DD" stroke-width="1"/>
  <text x="165" y="46" text-anchor="middle" font-size="13" font-weight="600" fill="#3C3489">반응형 (Responsive)</text>
  <text x="165" y="70" text-anchor="middle" font-size="11" fill="#534AB7">화면 크기에 따라 레이아웃이</text>
  <text x="165" y="86" text-anchor="middle" font-size="11" fill="#534AB7">자동으로 변화한다</text>
  <text x="165" y="110" text-anchor="middle" font-size="11" fill="#534AB7">✓ 하나의 디자인으로 모든 기기 대응</text>
  <text x="165" y="128" text-anchor="middle" font-size="11" fill="#534AB7">✓ 유지보수 쉬움</text>
  <text x="165" y="146" text-anchor="middle" font-size="11" fill="#534AB7">✓ UX 일관성 유지</text>
  <text x="165" y="164" text-anchor="middle" font-size="11" fill="#534AB7">✓ SEO 유리</text>

  <rect x="330" y="15" width="290" height="160" rx="8" fill="#F1EFE8" stroke="#B4B2A9" stroke-width="1"/>
  <text x="475" y="46" text-anchor="middle" font-size="13" font-weight="600" fill="#2C2C2A">적응형 (Adaptive)</text>
  <text x="475" y="70" text-anchor="middle" font-size="11" fill="#5F5E5A">기기별로 따로 디자인을</text>
  <text x="475" y="86" text-anchor="middle" font-size="11" fill="#5F5E5A">따로 만든다</text>
  <text x="475" y="110" text-anchor="middle" font-size="11" fill="#5F5E5A">✓ 초기 설계 쉬움</text>
  <text x="475" y="128" text-anchor="middle" font-size="11" fill="#888780">✗ 유지보수 불리</text>
  <text x="475" y="146" text-anchor="middle" font-size="11" fill="#888780">✗ 변경 시 여러 버전 수정 필요</text>
  <text x="475" y="164" text-anchor="middle" font-size="10" fill="#888780">모바일 전용 도메인: m.사이트주소</text>
</svg>

반응형이 지금의 표준이 된 이유는 유지보수와 일관성 때문이다. 하나의 디자인 파일로 PC·태블릿·모바일을 모두 커버할 수 있고, SEO에도 유리하다. 피그마의 Auto Layout이 반응형 UI 구조를 설계하는 핵심 도구가 되는 이유도 여기 있다.

---

> [!tip]
> 웹의 구조는 단순 UI 배치가 아니라 사용자 이동 경로를 설계하는 일이다
> 디자인은 고정이 아니라 유동적으로 변해야 한다

여기에서 관련 실습을 볼 수 있어요! [[12. 카드 결제, 계산기, 리뷰 UI 제작]]