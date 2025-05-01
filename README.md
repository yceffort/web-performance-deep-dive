# web-performance-deep-dive

## [서문](./posts/intro.md)

## Part 1: 웹 성능의 기초 다지기

### [1장. 시작하며](./posts/chapter1/1-0.intro.md)

- [1-1. 왜 웹 성능이 중요한가?](./posts/chapter1/1-1.왜_웹_성능이_중요한가.md)
  - 성능이 사용자 경험 및 비즈니스 가치에 미치는 영향
  - 개인 학습 및 실무 적용의 장점
- [1-2. 책의 구성 및 학습 가이드](./posts/chapter1/1-2.책의_구성_및_학습_가이드.md)
  - 각 장에서 다루는 범위와 학습 순서
  - 예시 코드, 실습 환경, 자료 활용 방법

### [2장. 웹 성능, 어떻게 측정하고 이해할까?](./posts/chapter2/2-0.intro.md)

- [2-1. 핵심 웹 지표 (LCP, INP, CLS) 깊이 알기](./posts/chapter2/2-1.핵심_웹_지표.md)
- [2-2. 주요 성능 지표 (TTFB, FCP, TTI 등) 와 그 의미](./posts/chapter2/2-2.주요_성능_지표.md)
- [2-3. 성능 측정 환경: Lab vs Field (RUM)](./posts/chapter2/2-3.측정_환경.md)
- [2-4. 핵심 측정 도구 사용법 (Chrome DevTools, Lighthouse, WebPageTest)](./posts/chapter2/2-4.측정_도구.md)
- [2-5. 지속적인 측정과 개선의 중요성](./posts/chapter2/2-5.지속적_측정.md)

### [3장. 브라우저 렌더링, 성능의 시작점](./posts/chapter3/3-0.intro.md)

- [3-1. 브라우저는 어떻게 웹페이지를 그리는가? (Critical Rendering Path)](./posts/chapter3/3-1.렌더링_과정.md)
- [3-2. DOM, CSSOM, Render Tree 생성 과정](./posts/chapter3/3-2.DOM_CSSOM_RenderTree.md)
- [3-3. Reflow, Repaint 그리고 성능 영향](./posts/chapter3/3-3.Reflow_Repaint.md)
- [3-4. GPU 가속과 합성(Compositing) 이해](./posts/chapter3/3-4.GPU_가속.md)

## Part 2: 웹 성능 최적화 핵심 전략

### [4장. CSS 렌더링 최적화와 시각적 안정성 확보](./posts/chapter4/4-0.intro.md)

- [4-1. CSS 파싱과 렌더링 블로킹 최적화](./posts/chapter4/4-1.CSS_파싱_블로킹.md)
- [4-2. 효율적인 CSS 작성법](./posts/chapter4/4-2.효율적_CSS.md)
- [4-3. 레이아웃과 페인트 최적화 (will-change, transform 등)](./posts/chapter4/4-3.레이아웃_페인트_최적화.md)
- [4-4. Critical CSS 인라이닝 전략](./posts/chapter4/4-4.Critical_CSS.md)
- [4-5. CLS 문제 해결: 레이아웃 이동 방지 기법](./posts/chapter4/4-5.CLS_개선.md)

### [5장. 네트워크 전송 병목 제거하기](./posts/chapter5/5-0.intro.md)

- [5-1. HTTP/1.1, HTTP/2, HTTP/3 특징과 최적화](./posts/chapter5/5-1.HTTP_비교.md)
- [5-2. HTTPS/TLS 핸드셰이크와 성능](./posts/chapter5/5-2.HTTPS_TLS_최적화.md)
- [5-3. 리소스 압축 전략 (Gzip, Brotli)](./posts/chapter5/5-3.압축.md)
- [5-4. 강력한 캐싱 활용법 (HTTP 캐시, Service Worker 캐시)](./posts/chapter5/5-4.캐싱.md)
- [5-5. 리소스 힌트 활용 (Preload, Prefetch, Preconnect 등)](./posts/chapter5/5-5.리소스_힌트.md)

### [6장. 이미지, 폰트, 미디어 리소스 다이어트](./posts/chapter6/6-0.intro.md)

- [6-1. 최적의 이미지 포맷 선택과 기법 (WebP, AVIF, Responsive Images)](./posts/chapter6/6-1.이미지_최적화.md)
- [6-2. 웹 폰트 로딩 최적화 (FOIT/FOUT 방지, Preload, Subset)](./posts/chapter6/6-2.웹폰트_최적화.md)
- [6-3. 비디오/오디오 리소스 최적화 (Lazy Loading, 스트리밍)](./posts/chapter6/6-3.미디어_최적화.md)

### [7장. 자바스크립트 실행 효율 극대화](./posts/chapter7/7-0.intro.md)

- [7-1. 이벤트 루프와 비동기 처리 성능 관점](./posts/chapter7/7-1.이벤트루프_비동기.md)
- [7-2. 효율적인 DOM 조작과 업데이트](./posts/chapter7/7-2.DOM_조작_최적화.md)
- [7-3. 자바스크립트 메모리 관리와 누수 추적](./posts/chapter7/7-3.메모리_관리.md)
- [7-4. 긴 작업(Long Tasks) 분할과 메인 스레드 확보](./posts/chapter7/7-4.Long_Tasks_분할.md)

### [8장. 모던 빌드 시스템과 코드 최적화](./posts/chapter8/8-0.intro.md)

- [8-1. 코드 스플리팅 전략과 구현](./posts/chapter8/8-1.코드_스플리팅.md)
- [8-2. 트리 쉐이킹으로 사용하지 않는 코드 제거](./posts/chapter8/8-2.트리_쉐이킹.md)
- [8-3. 효과적인 Lazy Loading 적용법](./posts/chapter8/8-3.Lazy_Loading.md)
- [8-4. 서드파티 라이브러리 분석과 최적화](./posts/chapter8/8-4.서드파티_최적화.md)
- [8-5. Polyfill 최적화와 모던 빌드 전략](./posts/chapter8/8-5.Polyfill_최적화.md)
- [8-6. 번들 분석 도구 활용](./posts/chapter8/8-6.번들_분석.md)

## Part 3: 프레임워크, 아키텍처, 그리고 고급 주제

### [9장. 프레임워크 환경에서의 성능 최적화](./posts/chapter9/9-0.intro.md)

- [9-1. 프레임워크 성능 최적화 공통 원칙](./posts/chapter9/9-1.공통_원칙.md)
- [9-2. React 성능 개선 패턴](./posts/chapter9/9-2.React_최적화.md)
- [9-3. Vue 성능 개선 패턴](./posts/chapter9/9-3.Vue_최적화.md)
- [9-4. (선택적) 기타 프레임워크 고려 사항](./posts/chapter9/9-4.기타_프레임워크.md)

### [10장. 서버 렌더링(SSR/SSG) 성능 완전 정복](./posts/chapter10/10-0.intro.md)

- [10-1. SSR과 SSG의 작동 원리와 성능적 장단점](./posts/chapter10/10-1.SSR_SSG_원리.md)
- [10-2. 초기 로딩 성능 개선 전략 (Hydration 최적화)](./posts/chapter10/10-2.Hydration_최적화.md)
- [10-3. 데이터 Fetching 및 캐싱 최적화](./posts/chapter10/10-3.Data_Fetching_캐싱.md)
- [10-4. 주요 프레임워크 기반 SSR/SSG 최적화 예시](./posts/chapter10/10-4.프레임워크_예시.md)

### [11장. 실시간 및 대규모 데이터 처리 성능](./posts/chapter11/11-0.intro.md)

- [11-1. WebSocket/SSE 통신 최적화 전략](./posts/chapter11/11-1.WebSocket_SSE.md)
- [11-2. 대규모 DOM 렌더링 최적화](./posts/chapter11/11-2.대규모_DOM.md)
- [11-3. 데이터 시각화 성능 개선 기법](./posts/chapter11/11-3.데이터_시각화.md)

### [12장. 모바일 환경 성능 특성과 최적화](./posts/chapter12/12-0.intro.md)

- [12-1. 모바일 네트워크 및 하드웨어 제약 극복](./posts/chapter12/12-1.모바일_특성.md)
- [12-2. 반응형 디자인과 리소스 최적화 연동](./posts/chapter12/12-2.반응형_최적화.md)
- [12-3. PWA를 통한 성능 및 사용자 경험 향상](./posts/chapter12/12-3.PWA.md)

## Part 4: 지속적인 성능 관리와 미래

### [13장. 보안과 성능, 두 마리 토끼 잡기](./posts/chapter13/13-0.intro.md)

- [13-1. HTTPS/TLS 성능 영향 최소화](./posts/chapter13/13-1.HTTPS_TLS.md)
- [13-2. 보안 헤더(CSP, SRI 등)와 성능의 균형](./posts/chapter13/13-2.보안_헤더.md)
- [13-3. 인증/세션 관리 최적화](./posts/chapter13/13-3.인증_세션.md)

### [14장. 성능 테스트 자동화와 실시간 모니터링](./posts/chapter14/14-0.intro.md)

- [14-1. 성능 예산 설정과 관리](./posts/chapter14/14-1.성능_예산.md)
- [14-2. CI/CD 파이프라인 연동 테스트](./posts/chapter14/14-2.CI_CD_테스트.md)
- [14-3. 프런트엔드 부하 테스트 기초](./posts/chapter14/14-3.부하_테스트.md)
- [14-4. RUM 데이터를 활용한 실시간 성능 모니터링](./posts/chapter14/14-4.RUM_모니터링.md)

### [15장. 실전! 웹 성능 개선 프로젝트](./posts/chapter15/15-0.intro.md)

- TBD
- <https://yceffort.kr/2025/04/web-performance-help>

### [16장. 미래를 향한 웹 성능 기술](./posts/chapter16/16-0.intro.md)

- [16-1. 차세대 웹 기술 동향](./posts/chapter16/16-1.차세대_기술.md)
- [16-2. 서버리스, 엣지 컴퓨팅과 성능 패러다임 변화](./posts/chapter16/16-2.서버리스_엣지.md)

### [17장. 마치며](./posts/chapter17/17-0.intro.md)

- [17-1. 핵심 내용 요약 및 성능 개선 로드맵](./posts/chapter17/17-1.핵심_요약.md)
- [17-2. 지속적인 학습을 위한 제언](./posts/chapter17/17-2.마지막_메시지.md)

## [부록](./posts/appendix/appendix.md)

- [부록-1. 성능 튜닝 체크리스트](./posts/appendix/appendix-1.checklist.md)
- [부록-2. 용어 정리(Glossary)](./posts/appendix/appendix-2.glossary.md)
