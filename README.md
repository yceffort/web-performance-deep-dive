# web-performance-deep-dive

## 1장. 시작하며

1. 왜 웹 퍼포먼스인가?
   - 성능이 사용자 경험 및 비즈니스 가치에 미치는 영향
   - 개인 학습 및 실무 적용의 장점
2. 책의 구성 및 목표
   - 각 장에서 다루는 범위와 학습 순서
   - 예시 코드, 실습 환경, 자료 활용 방법

## 2장. 웹 성능 지표와 측정 기초

1. 브라우저 퍼포먼스 지표
   - FCP, LCP, TTI, CLS 등 핵심 웹 지표
   - TTFB, Speed Index 등 핵심 웹 지표는 아니지만 눈여겨 봐야할 추가 지표
2. 타이밍 API와 퍼포먼스 로깅
   - Navigation Timing, Resource Timing API
   - 성능 측정 자동화 (예: Lighthouse, WebPageTest)
3. 실무/개인 프로젝트에서 측정 적용
   - Chrome DevTools 활용
   - CI 연동 없이도 가능한 로컬 자동 측정 스크립트 예시

## 3장. 브라우저 렌더링 과정 이해

1. DOM, CSSOM, Render Tree
   - 크리티컬 렌더링 경로(Critical Rendering Path)
   - 파싱 과정, 블로킹 리소스
2. Reflow(Recalculate Style)와 Repaint
   - 렌더 트리 업데이트 메커니즘
   - 레이아웃 스래싱(Layout Thrashing) 방지 기법
3. GPU 가속과 브라우저 렌더링 최적화
   - 브라우저의 자바스크립트 실행/DOM 업데이트 흐름
   - GPU 합성 계층(Compositing Layer)과 애니메이션에 미치는 영향

## 4장. 네트워크 최적화와 HTTP/2, HTTP/3

1. HTTP/1.1 vs HTTP/2 vs HTTP/3(QUIC)
   - 멀티플렉싱, 헤더 압축, 전송 성능 비교
2. HTTPS/TLS 성능 고려
   - 인증서, 핸드셰이크, HSTS 등
   - 성능 임팩트와 최적화 방안
3. 리소스 전송 효율화
   - 압축(Gzip, Brotli), 캐싱 헤더(Cache-Control, ETag)
   - Preload, Prefetch, DNS Prefetch, Preconnect 등 리소스 힌트

## 5장. 프론트엔드 빌드와 번들링 최적화

1. 모듈 번들러 개요
   - Webpack, Rollup, Parcel, esbuild 비교
   - 모듈 시스템(ES Modules, CommonJS) 이해
2. 번들 사이즈 관리
   - 코드 스플리팅, 트리 쉐이킹, Lazy Loading
   - 서드파티 라이브러리 분리 및 번들 분석
3. Modern Build 전략
   - ESNext 기반의 빌드
   - Polyfill 최소화, 브라우저 타겟 자동 설정(Browserslist)

## 6장. 자바스크립트 퍼포먼스 집중 공략

1. 이벤트 루프와 비동기 처리
   - 싱글 스레드 모델, 콜 스택, 메시지 큐
   - 콜백, 프로미스, `async/await`의 성능 관점
2. DOM 조작 최소화
   - 가상 DOM(React), Incremental DOM(Angular), Vue 가상 DOM
   - Batch updates, re-render 최적화
3. 메모리 관리와 최적화 기법
   - 스코프, 클로저, 가비지 컬렉션 이해
   - Performance API를 통한 메모리 사용량 추적

## 7장. CSS 퍼포먼스 최적화

1. CSS 파싱 및 렌더링 특징
   - CSSOM 생성, 블로킹 리소스 처리
   - @import, @font-face 지연 로딩 시 이슈
2. 레이아웃/페인트 최적화
   - `will-change`, `transform`, `opacity` 활용
   - GPU 가속 애니메이션 vs CPU 렌더링
3. Critical CSS와 분할 로딩
   - 초기 렌더링 속도 개선
   - CSS 병합, 중복 제거, 코드 스플리팅

## 8장. 이미지와 폰트, 미디어 리소스 최적화

1. 이미지 최적화 전략
   - WebP, AVIF, JPEG, PNG, SVG 등 선택 가이드
   - Responsive Images(`srcset`, `<picture>`) 활용
2. 웹폰트 로딩 최적화
   - Preload, Font Display(`swap`, `fallback` 등)
   - 서브셋(Subsetting)으로 폰트 파일 다이어트
3. 동영상/오디오 스트리밍
   - Adaptive Bitrate, HLS/DASH 개념
   - Lazy Loading, 미디어 CDN 적용

## 9장. 프론트엔드 프레임워크별 성능 팁

1. 리액트

   - Hooks와 리렌더링 최적화
     - `useMemo`, `useCallback` 등 메모이제이션 기법
     - 컴포넌트 분리, `memo` 활용
   - 리액트 Suspense와 Concurrent Mode 개요
     - Suspense를 통한 비동기 데이터 로딩
     - Concurrent Rendering이 실제 성능에 미치는 영향 (개념적인 소개)

2. Vue
   - 반응성(Reactivity) 시스템 이해
     - Vue 2 vs Vue 3의 차이 (Proxy 기반 vs `defineProperty` 기반)
     - 반응성 주기가 DOM 업데이트와 렌더링에 끼치는 영향
   - Vuex/Pinia에서의 성능 고려
     - 상태 관리 시 렌더링 범위 최소화
     - 대규모 SPA에서 모듈 구조 최적화

## 10장. SSR(서버 사이드 렌더링)과 SSG(정적 사이트 생성)

1. Next.js를 활용한 SSR

   - SSR의 기본 메커니즘
     - 초기 렌더링 속도, SEO와의 관계
     - `getServerSideProps`, `getStaticProps` 개념
   - 성능 측면에서의 이점
     - TTFB 개선, 퍼포먼스 측정 지표
     - CDN 배포와 SSR 캐싱 전략(간단한 적용 예시)

2. Nuxt.js를 활용한 SSR

   - Nuxt.js 구조와 페이지 렌더링
     - `pages/`, `asyncData()` 등 핵심 개념
     - Vue SPA와 Nuxt SSR의 차이
   - 실무 적용 예시
     - 프로젝트 구성, 라우팅, Vuex/Pinia 연계
     - 배포 시 최적화(Static Export 등)

3. 간단한 SSG 활용
   - Next.js / Nuxt.js에서의 정적 사이트 생성
     - (Next) `getStaticProps`, Incremental Static Regeneration
     - (Nuxt) `nuxt generate` 명령어, 정적 빌드 & 배포
   - 성능 및 SEO 효과
     - CDN 캐싱, 빌드 타임 렌더링이 주는 장점
     - 예시 코드나 참고 링크 안내

## 11장. Real-Time & 고급 시나리오 최적화

1. 실시간 통신 기초
   - WebSocket, SSE(Server-Sent Events), WebRTC 개념
   - 폴링 vs 푸시 전략 비교
2. WebSocket 성능과 부하 분산
   - 메시지 형식(JSON, 바이너리) 선택
   - 서버 리소스, 로드 밸런싱 고려
3. 대규모 DOM 및 데이터 시각화
   - 가상 스크롤, OffscreenCanvas, Web Workers
   - D3.js, Chart.js에서의 성능 팁

## 12장. 테스트와 모니터링, 디버깅

1. 성능 테스트 자동화
   - Lighthouse CI, Jest+Puppeteer, Cypress
   - 스크립트 기반 성능 지표 수집
2. 부하 테스트 기초
   - k6, Gatling, JMeter를 통한 API 부하
   - 프론트엔드 개발자의 관점에서 체크할 항목
3. 실시간 모니터링과 알림
   - RUM 도구(Sentry, Datadog) 사용
   - 로그, 에러 리포팅과 퍼포먼스 연계

## 13장. 모바일 환경 퍼포먼스 최적화

1. 모바일 디바이스 특성
   - 네트워크 제약, CPU/GPU 스펙
   - 뷰포트, 터치 이벤트 성능
2. 반응형 디자인과 CSS/JS 최적화
   - 미디어 쿼리, IntersectionObserver 활용
   - 이벤트 디바운스/스로틀 등
3. PWA(Progressive Web Apps)
   - Service Worker, Offline 캐싱
   - 성능 측면에서의 전략(Fallback, Cache-first 등)

## 14장. 보안과 성능의 균형

1. HTTPS/TLS 적용에 따른 성능 영향
   - 인증서 최적화, [OCSP Stapling](https://en.wikipedia.org/wiki/OCSP_stapling) 등
2. CSP, SRI, 보안 헤더
   - XSS 방어와 리소스 무결성(SRI)이 성능에 주는 영향
3. 인증과 세션 관리
   - JWT, 쿠키, 로컬 스토리지
   - 페이로드 크기와 성능 고려

## 15장. 간단 실전 예제 둘러보기

1. 싱글 페이지 포트폴리오 예제
   - 리액트 중 하나를 활용해 구조 잡기
   - Lighthouse로 측정한 성능 지표 전후 비교
   - CSS/JS/이미지 최적화 과정을 순서대로 요약
2. 작은 규모 이커머스 예제
   - 제품 리스트 페이지와 상세 페이지 구현
   - Lazy Loading, 코드 스플리팅 적용 예시
   - CDN(무료 계정) 사용해서 정적 리소스 배포 시도
3. 정리
   - 간단 예제라도 실제로 적용해본 후 배운 점
   - 독자가 확장해서 더 해볼 만한 아이디어

## 16장. 향후 기술 동향

1. 차세대 웹 기술
   - WebAssembly, WebGPU, OffscreenCanvas
   - AI/ML 기반 사용자 분석과 퍼포먼스 자동 최적화
2. 서버리스와 엣지 컴퓨팅
   - AWS Lambda@Edge, Cloudflare Workers
   - Edge-first 아키텍처가 프론트엔드 성능에 미치는 영향

## 17장. 마치며

1. 이 책에서 다룬 내용의 핵심 정리

   - 전반부(기초 지표·브라우저 렌더링·네트워크)부터 후반부(프레임워크·SSR·실전 예제·미래 기술)까지,
     각 장에서 꼭 기억해야 할 핵심 포인트를 짧게 다시 짚어봄
   - 성능 최적화는 단순히 몇 가지 테크닉으로 끝나는 것이 아니라, 지속적인 측정과 개선의 과정임을 강조

2. 학습을 이어가는 방법

   - 공식 문서와 커뮤니티: React/Vue, Next/Nuxt, Web 성능 측정 도구 등 각종 공식 문서의 업데이트 소식 체크
   - 스터디/오픈소스 참여: 오픈소스 프로젝트에서 성능 관련 이슈를 탐색하고 기여해보는 방법
   - 세미나·컨퍼런스: 국내외 웹 퍼포먼스 컨퍼런스, 온라인 세미나 정보
   - 개인 프로젝트에서 반복 실습: 예제 확장, 다른 기술 스택 적용, 성능 개선 전후 지표 비교

3. 마치는 글
   - 독자에게 감사 인사
   - 성능은 결국 사용자 경험을 개선하고, 더 나은 웹 서비스를 만드는 핵심 요소”라는 점을 되새김
   - 앞으로도 꾸준히 새로운 툴과 기법을 학습하면서, 실무에 적용하고 피드백을 얻어가길 권장

## 부록

1. 퍼포먼스 튜닝 체크리스트
   - 프론트 중심(HTML, CSS, JS, 이미지, 폰트, 네트워크 등)
2. 용어 정리(Glossary)
   - 주요 성능·네트워크·보안 용어 설명
