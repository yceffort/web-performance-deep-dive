# web-performance-deep-dive

## 1장. 시작하며

### 1-1. 왜 웹 성능이 중요한가?

- 성능이 사용자 경험 및 비즈니스 가치에 미치는 영향
- 개인 학습 및 실무 적용의 장점

### 1-2. 책의 구성 및 목표

- 각 장에서 다루는 범위와 학습 순서
- 예시 코드, 실습 환경, 자료 활용 방법

## 2장. 웹 성능 지표와 측정 기초

### 2-1. 브라우저 성능 지표

- FCP, LCP, TTI, CLS 등 핵심 웹 지표
- TTFB, Speed Index 등 부가적인 참고 지표

### 2-2. 타이밍 API와 성능 로깅

- Navigation Timing, Resource Timing API
- 성능 측정 자동화 도구 소개 (Lighthouse, WebPageTest)

### 2-3. 실무/개인 프로젝트에서 측정 적용

- Chrome DevTools 실습
- 로컬 환경에서 성능 측정 스크립트 작성

## 3장. 브라우저 렌더링 과정 이해

### 3-1. DOM, CSSOM, Render Tree

- 크리티컬 렌더링 경로 이해
- 파싱 과정과 블로킹 리소스 분석

### 3-2. Reflow와 Repaint

- 렌더 트리 업데이트 메커니즘
- 레이아웃 스래싱 방지 기법

### 3-3. GPU 가속과 렌더링 최적화

- 자바스크립트 실행 흐름
- GPU 합성 계층과 애니메이션 최적화

## 4장. 네트워크 최적화와 HTTP/2, HTTP/3

### 4-1. HTTP/1.1 vs HTTP/2 vs HTTP/3

- 멀티플렉싱, 헤더 압축, 전송 최적화

### 4-2. HTTPS/TLS 성능 최적화

- 인증서 관리, 핸드셰이크 최적화

### 4-3. 리소스 전송 효율화

- 압축, 캐싱, 리소스 프리로딩 전략
- Preload, Prefetch, DNS Prefetch, Preconnect 등 리소스 힌트

## 5장. 빌드와 번들 최적화

### 5-1. 코드 스플리팅과 트리 쉐이킹

- Dynamic Import, 트리 쉐이킹 적용법

### 5-2. Lazy Loading 전략

- 라우트/컴포넌트 기반 Lazy Loading 실습

### 5-3. 서드파티 라이브러리 다이어트

- moment.js 교체, lodash 최적화 전략

### 5-4. ESNext 기반 빌드 전략과 Polyfill 최소화

- ES2020+ 빌드, Browserslist, polyfill 전략

### 5-5. 번들 분석과 병목 제거

- Webpack Bundle Analyzer 실습
- 무거운 모듈 식별 및 대처

## 6장. 자바스크립트 성능 집중 공략

### 6-1. 이벤트 루프와 비동기 처리

- 싱글 스레드 모델과 async/await 성능 관점

### 6-2. DOM 조작 최소화

- 가상 DOM 및 Batch 업데이트 전략

### 6-3. 메모리 관리와 최적화

- 클로저, 가비지 컬렉션 이해 및 메모리 추적

## 7장. CSS 성능 최적화

### 7-1. CSS 파싱 및 렌더링 특징

- CSSOM, 블로킹 리소스 최적화

### 7-2. 레이아웃과 페인트 최적화

- will-change, transform, opacity 활용

### 7-3. Critical CSS와 분할 로딩

- 초기 렌더링 최적화, CSS 코드 스플리팅

## 8장. 이미지와 폰트, 미디어 리소스 최적화

### 8-1. 이미지 최적화 전략

- 포맷 선택, Responsive Images 실습

### 8-2. 웹폰트 최적화

- Preload, Font Display, 서브셋 전략

### 8-3. 소규모 동영상/오디오 스트리밍 최적화

- 웹 페이지 삽입용 미디어 최적화 전략
- Lazy Loading 및 미디어 CDN 활용

## 9장. 프런트엔드 프레임워크별 성능 팁

### 9-1. React 성능 최적화

- Hooks 리렌더링 최적화
- Suspense와 Concurrent Mode 소개

### 9-2. Vue 성능 최적화

- Pinia 중심 상태 관리 최적화
- Vue 반응성 시스템 최적화 전략

## 10장. SSR과 SSG 최적화

### 10-1. Next.js 기반 SSR 최적화

- SSR의 성능 이점과 측정 방법

### 10-2. Nuxt.js 기반 SSR 최적화

- Static Export 활용과 최적화 기법

### 10-3. 정적 사이트 생성(SSG) 전략

- 정적 생성과 CDN 배포 최적화

## 11장. 실시간 통신 및 대규모 DOM 최적화

### 11-1. WebSocket과 SSE 통신 최적화

- WebSocket/SSE 개념 및 최적화 전략

### 11-2. WebSocket 부하 분산

- 메시지 포맷 선택과 서버 확장 전략

### 11-3. 대규모 DOM 및 데이터 시각화

- 가상 스크롤, Web Workers, OffscreenCanvas

## 12장. 테스트와 모니터링, 디버깅

### 12-1. 성능 테스트 자동화

- Lighthouse CI, Puppeteer, Cypress 실습

### 12-2. 부하 테스트 기초

- k6, Gatling, JMeter 도구 소개

### 12-3. 실시간 모니터링과 알림

- Sentry, Datadog을 활용한 실시간 성능 모니터링

## 13장. 모바일 환경 성능 최적화

### 13-1. 모바일 디바이스 성능 특성

- 네트워크와 하드웨어 제약 이해

### 13-2. 반응형 디자인 및 최적화

- 미디어 쿼리, IntersectionObserver 전략

### 13-3. PWA(Progressive Web Apps)

- Offline 캐싱 및 Fallback 전략

## 14장. 보안과 성능의 균형

### 14-1. HTTPS/TLS 성능 최적화

- 인증서 최적화, OCSP Stapling 활용

### 14-2. CSP, SRI, 보안 헤더

- 리소스 무결성과 성능 균형 전략

### 14-3. 인증과 세션 관리 최적화

- JWT, 쿠키 저장 및 전송 최적화

## 15장. 간단 실전 예제 둘러보기

### 15-1. 포트폴리오 웹사이트 최적화 실습

- 성능 측정 및 개선 흐름 실습

### 15-2. 소규모 이커머스 사이트 최적화 실습

- Lazy Loading, 코드 스플리팅, CDN 적용

### 15-3. 결과 정리 및 추가 아이디어 제안

- 적용 결과 분석 및 확장 방향 제안

## 16장. 향후 웹 기술 동향

### 16-1. 차세대 웹 기술 동향

- WebAssembly, WebGPU, AI 기반 최적화

### 16-2. 서버리스와 엣지 컴퓨팅

- Edge-first 아키텍처가 성능에 미치는 영향

## 17장. 마치며

### 17-1. 핵심 내용 요약

- 주요 학습 포인트 정리

### 17-2. 마지막 메시지

- 다음 학습 방향 제안

## 부록

### 부록-1. 성능 튜닝 체크리스트

- HTML, CSS, JS, 이미지, 폰트, 네트워크 항목 정리

### 부록-2. 용어 정리(Glossary)

- 이 책에서 다룬 주요 용어 설명
