# Learn Hero

## Overview

Tổng hợp giải thích các khái niệm quan trọng trong Web Development.

---

## Mục lục

### [LEVEL 1: Base](#level-1-base)

| # | Topic |
| --- | --- |
| [1](#1-hydration) | [Hydration](#1-hydration) |
| [2](#2-virtual-dom-diffing-complexity) | [Virtual DOM Diffing Complexity](#2-virtual-dom-diffing-complexity) |
| [3](#3-event-loop-macro-vs-microtasks) | [Event Loop (Macro vs Microtasks)](#3-event-loop-macro-vs-microtasks) |
| [4](#4-critical-rendering-path) | [Critical Rendering Path](#4-critical-rendering-path) |
| [5](#5-code-splitting-strategies) | [Code Splitting Strategies](#5-code-splitting-strategies) |
| [6](#6-dynamic-import-chunking) | [Dynamic Import Chunking](#6-dynamic-import-chunking) |
| [7](#7-preload-vs-prefetch-vs-preconnect) | [Preload vs Prefetch vs Preconnect](#7-preload-vs-prefetch-vs-preconnect) |
| [8](#8-cors-preflight) | [CORS Preflight](#8-cors-preflight) |
| [9](#9-csrf-vs-xss-mitigation) | [CSRF vs XSS Mitigation](#9-csrf-vs-xss-mitigation) |
| [10](#10-web-workers-vs-service-workers) | [Web Workers vs Service Workers](#10-web-workers-vs-service-workers) |

### [LEVEL 2: React Core & Rendering Mechanics](#level-2-react-core--rendering-mechanics)

| # | Topic |
| --- | --- |
| [11](#11-reconciliation-algorithm) | [Reconciliation Algorithm](#11-reconciliation-algorithm) |
| [12](#12-fiber-architecture) | [Fiber Architecture](#12-fiber-architecture) |
| [13](#13-concurrent-rendering) | [Concurrent Rendering](#13-concurrent-rendering) |
| [14](#14-time-slicing) | [Time Slicing](#14-time-slicing) |
| [15](#15-scheduler-priorities) | [Scheduler Priorities](#15-scheduler-priorities) |
| [16](#16-suspense-boundaries) | [Suspense Boundaries](#16-suspense-boundaries) |
| [17](#17-selective-hydration) | [Selective Hydration](#17-selective-hydration) |
| [18](#18-server-components) | [Server Components](#18-server-components) |
| [19](#19-tearing-in-concurrent-ui) | [Tearing in Concurrent UI](#19-tearing-in-concurrent-ui) |
| [20](#20-stale-closure-problem) | [Stale Closure Problem](#20-stale-closure-problem) |

### [LEVEL 3: Performance Nền Tảng Trình Duyệt](#level-3-performance-nền-tảng-trình-duyệt)

| # | Topic |
| --- | --- |
| [21](#21-layout-thrashing) | [Layout Thrashing](#21-layout-thrashing) |
| [22](#22-paint-vs-layout-vs-composite) | [Paint vs Layout vs Composite](#22-paint-vs-layout-vs-composite) |
| [23](#23-browser-compositing-layers) | [Browser Compositing Layers](#23-browser-compositing-layers) |
| [24](#24-gpu-acceleration-in-css) | [GPU Acceleration in CSS](#24-gpu-acceleration-in-css) |
| [25](#25-css-containment) | [CSS Containment](#25-css-containment) |
| [26](#26-render-blocking-resources) | [Render Blocking Resources](#26-render-blocking-resources) |
| [27](#27-render-waterfalls) | [Render Waterfalls](#27-render-waterfalls) |
| [28](#28-subpixel-rendering) | [Subpixel Rendering](#28-subpixel-rendering) |
| [29](#29-detached-dom-nodes) | [Detached DOM Nodes](#29-detached-dom-nodes) |
| [30](#30-garbage-collection-timing) | [Garbage Collection Timing](#30-garbage-collection-timing) |

### [LEVEL 4: Data & State Management Nâng Cao](#level-4-data--state-management-nâng-cao)

| # | Topic |
| --- | --- |
| [31](#31-structural-sharing) | [Structural Sharing](#31-structural-sharing) |
| [32](#32-immutable-data-patterns) | [Immutable Data Patterns](#32-immutable-data-patterns) |
| [33](#33-referential-equality) | [Referential Equality](#33-referential-equality) |
| [34](#34-memoization-pitfalls) | [Memoization Pitfalls](#34-memoization-pitfalls) |
| [35](#35-race-conditions-in-ui-state) | [Race Conditions in UI State](#35-race-conditions-in-ui-state) |
| [36](#36-finite-state-modeling) | [Finite State Modeling](#36-finite-state-modeling) |
| [37](#37-event-sourcing-in-frontend) | [Event Sourcing in Frontend](#37-event-sourcing-in-frontend) |
| [38](#38-optimistic-ui-rollback-strategy) | [Optimistic UI Rollback Strategy](#38-optimistic-ui-rollback-strategy) |
| [39](#39-deterministic-rendering) | [Deterministic Rendering](#39-deterministic-rendering) |
| [40](#40-idempotent-ui-actions) | [Idempotent UI Actions](#40-idempotent-ui-actions) |

### [LEVEL 5: Caching & Networking Chiến Lược](#level-5-caching--networking-chiến-lược)

| # | Topic |
| --- | --- |
| [41](#41-cache-invalidation-strategies) | [Cache Invalidation Strategies](#41-cache-invalidation-strategies) |
| [42](#42-stale-while-revalidate) | [Stale-While-Revalidate](#42-stale-while-revalidate) |
| [43](#43-etag-vs-cache-control) | [ETag vs Cache-Control](#43-etag-vs-cache-control) |
| [44](#44-http3-và-quic) | [HTTP/3 và QUIC](#44-http3-và-quic) |
| [45](#45-backpressure-in-streams-api) | [Backpressure in Streams API](#45-backpressure-in-streams-api) |
| [46](#46-abortcontroller) | [AbortController](#46-abortcontroller) |
| [47](#47-streaming-fetch-response-handling) | [Streaming Fetch Response Handling](#47-streaming-fetch-response-handling) |
| [48](#48-priority-hints) | [Priority Hints](#48-priority-hints) |
| [49](#49-samesite-cookie-modes) | [SameSite Cookie Modes](#49-samesite-cookie-modes) |
| [50](#50-speculative-prerendering) | [Speculative Prerendering](#50-speculative-prerendering) |

### [LEVEL 6: Security](#level-6-security)

| # | Topic |
| --- | --- |
| [51](#51-content-security-policy-csp) | [Content Security Policy (CSP)](#51-content-security-policy-csp) |
| [52](#52-trusted-types) | [Trusted Types](#52-trusted-types) |
| [53](#53-dom-clobbering) | [DOM Clobbering](#53-dom-clobbering) |
| [54](#54-prototype-pollution) | [Prototype Pollution](#54-prototype-pollution) |
| [55](#55-same-origin-policy-nuances) | [Same-Origin Policy Nuances](#55-same-origin-policy-nuances) |
| [56](#56-service-worker-lifecycle-traps) | [Service Worker Lifecycle Traps](#56-service-worker-lifecycle-traps) |
| [57](#57-sharedarraybuffer) | [SharedArrayBuffer](#57-sharedarraybuffer) |
| [58](#58-transferable-objects) | [Transferable Objects](#58-transferable-objects) |
| [59](#59-cors-preflight-internals) | [CORS Preflight Internals](#59-cors-preflight-internals) |
| [60](#60-offline-conflict-resolution) | [Offline Conflict Resolution](#60-offline-conflict-resolution) |

### [LEVEL 7: Web Platform Internals](#level-7-web-platform-internals)

| # | Topic |
| --- | --- |
| [61](#61-islands-architecture) | [Islands Architecture](#61-islands-architecture) |
| [62](#62-partial-hydration) | [Partial Hydration](#62-partial-hydration) |
| [63](#63-streaming-ssr) | [Streaming SSR](#63-streaming-ssr) |
| [64](#64-shadow-dom) | [Shadow DOM](#64-shadow-dom) |
| [65](#65-custom-elements-lifecycle) | [Custom Elements Lifecycle](#65-custom-elements-lifecycle) |
| [66](#66-web-components-interoperability) | [Web Components Interoperability](#66-web-components-interoperability) |
| [67](#67-intersectionobserver-internals) | [IntersectionObserver Internals](#67-intersectionobserver-internals) |
| [68](#68-resizeobserver-loop-limits) | [ResizeObserver Loop Limits](#68-resizeobserver-loop-limits) |
| [69](#69-mutationobserver-cost) | [MutationObserver Cost](#69-mutationobserver-cost) |
| [70](#70-offscreencanvas) | [OffscreenCanvas](#70-offscreencanvas) |

### [LEVEL 8: Concurrency & Streams](#level-8-concurrency--streams)

| # | Topic |
| --- | --- |
| [71](#71-task-starvation) | [Task Starvation](#71-task-starvation) |
| [72](#72-priority-inversion-in-async-code) | [Priority Inversion in Async Code](#72-priority-inversion-in-async-code) |
| [73](#73-scheduler-internals) | [Scheduler Internals](#73-scheduler-internals) |
| [74](#74-concurrent-rendering-tearing) | [Concurrent Rendering Tearing](#74-concurrent-rendering-tearing) |
| [75](#75-backpressure-handling) | [Backpressure Handling](#75-backpressure-handling) |
| [76](#76-streaming-ssr-pipelines) | [Streaming SSR Pipelines](#76-streaming-ssr-pipelines) |
| [77](#77-webrtc-basics) | [WebRTC Basics](#77-webrtc-basics) |
| [78](#78-crdt-basics-for-collaboration) | [CRDT Basics for Collaboration](#78-crdt-basics-for-collaboration) |
| [79](#79-shared-memory-models) | [Shared Memory Models](#79-shared-memory-models) |
| [80](#80-deterministic-ui-under-async) | [Deterministic UI Under Async](#80-deterministic-ui-under-async) |

### [LEVEL 9: Performance Metrics Thực Chiến](#level-9-performance-metrics-thực-chiến)

| # | Topic |
| --- | --- |
| [81](#81-first-input-delay-fid) | [First Input Delay (FID)](#81-first-input-delay-fid) |
| [82](#82-interaction-to-next-paint-inp) | [Interaction to Next Paint (INP)](#82-interaction-to-next-paint-inp) |
| [83](#83-cumulative-layout-shift-cls) | [Cumulative Layout Shift (CLS)](#83-cumulative-layout-shift-cls) |
| [84](#84-largest-contentful-paint-lcp) | [Largest Contentful Paint (LCP)](#84-largest-contentful-paint-lcp) |
| [85](#85-performanceobserver-api) | [PerformanceObserver API](#85-performanceobserver-api) |
| [86](#86-long-tasks-api) | [Long Tasks API](#86-long-tasks-api) |
| [87](#87-browser-memory-leak-detection) | [Browser Memory Leak Detection](#87-browser-memory-leak-detection) |
| [88](#88-accessibility-tree) | [Accessibility Tree](#88-accessibility-tree) |
| [89](#89-aria-live-regions-internals) | [ARIA Live Regions Internals](#89-aria-live-regions-internals) |
| [90](#90-pointer-events-model) | [Pointer Events Model](#90-pointer-events-model) |

### [LEVEL 10: Kiến Trúc Hệ Thống Frontend Hiện Đại](#level-10-kiến-trúc-hệ-thống-frontend-hiện-đại)

| # | Topic |
| --- | --- |
| [91](#91-edge-rendering) | [Edge Rendering](#91-edge-rendering) |
| [92](#92-micro-frontend-orchestration) | [Micro-Frontend Orchestration](#92-micro-frontend-orchestration) |
| [93](#93-module-federation) | [Module Federation](#93-module-federation) |
| [94](#94-webassembly-integration) | [WebAssembly Integration](#94-webassembly-integration) |
| [95](#95-indexeddb-scaling-strategy) | [IndexedDB Scaling Strategy](#95-indexeddb-scaling-strategy) |
| [96](#96-server-components-architecture) | [Server Components Architecture](#96-server-components-architecture) |
| [97](#97-offline-first-design) | [Offline-First Design](#97-offline-first-design) |
| [98](#98-conflict-resolution-models) | [Conflict Resolution Models](#98-conflict-resolution-models) |
| [99](#99-distributed-ui-consistency) | [Distributed UI Consistency](#99-distributed-ui-consistency) |
| [100](#100-frontend-system-design-trade-offs) | [Frontend System Design Trade-offs](#100-frontend-system-design-trade-offs) |

---

## LEVEL 1: Base

## 1. Hydration

**Hydration** là quá trình React "gắn" event listeners và state vào HTML tĩnh đã được server render sẵn (SSR/SSG), biến nó thành một ứng dụng interactive.

**Luồng hoạt động:**

1. Server render HTML → gửi về browser (người dùng thấy nội dung ngay)
2. Browser tải JS bundle
3. React "hydrate" — so sánh DOM hiện có với Virtual DOM, gắn event handlers

**Vấn đề thường gặp — Hydration Mismatch:**

- Xảy ra khi HTML server render khác với kết quả React render phía client
- Nguyên nhân: dùng `Date.now()`, `Math.random()`, hay check `window` trực tiếp trong render
- Hậu quả: React phải render lại toàn bộ, mất lợi ích SSR

```jsx
// ❌ Gây hydration mismatch
function Component() {
  return <div>{Date.now()}</div>;
}

// ✅ Dùng useEffect để xử lý client-only logic
function Component() {
  const [time, setTime] = useState(null);
  useEffect(() => setTime(Date.now()), []);
  return <div>{time}</div>;
}
```

---

### Tài liệu tham khảo

- [React Docs: hydrateRoot](https://react.dev/reference/react-dom/client/hydrateRoot)
- [Next.js: Server-side Rendering](https://nextjs.org/docs/pages/building-your-application/rendering/server-side-rendering)

## 2. Virtual DOM Diffing Complexity

**Virtual DOM (VDOM)** là bản sao nhẹ của DOM thật, lưu trong bộ nhớ dưới dạng JS object. Khi state thay đổi, React tạo VDOM mới và **diff** (so sánh) với VDOM cũ để tìm ra thay đổi nhỏ nhất cần cập nhật lên DOM thật.

**Thuật toán Reconciliation của React:**

- So sánh naïve 2 cây có độ phức tạp **O(n³)** — quá chậm với cây lớn
- React dùng heuristic để đạt **O(n)**:
  1. **Khác type** → xóa cây cũ, tạo cây mới hoàn toàn
  2. **Cùng type** → cập nhật attributes, giữ lại DOM node
  3. **List** → dùng `key` để map element cũ → mới hiệu quả

**Tại sao `key` quan trọng:**

```jsx
// ❌ Dùng index làm key — React không nhận ra thứ tự thay đổi
{items.map((item, i) => <Item key={i} data={item} />)}

// ✅ Dùng ID ổn định
{items.map(item => <Item key={item.id} data={item} />)}
```

**React Fiber** (React 16+): chia nhỏ công việc diff thành các "unit of work", có thể pause/resume, ưu tiên render quan trọng hơn (Concurrent Mode).

---

### Tài liệu tham khảo

- [React Docs: Reconciliation](https://legacy.reactjs.org/docs/reconciliation.html)
- [React Docs: Preserving & Resetting State](https://react.dev/learn/preserving-and-resetting-state)

## 3. Event Loop (Macro vs Microtasks)

JavaScript là single-threaded, Event Loop là cơ chế cho phép xử lý async mà không block UI.

**Thứ tự thực thi trong mỗi "tick":**

1. **Call Stack** — chạy hết synchronous code hiện tại
2. **Microtask Queue** — chạy **tất cả** microtask (Promise `.then`, `queueMicrotask`, `MutationObserver`)
3. **Render** — browser repaint nếu cần
4. **Macrotask Queue** — lấy **1** macrotask (`setTimeout`, `setInterval`, I/O, `MessageChannel`)
5. Quay lại bước 2

**Ví dụ thực tế:**

```js
console.log('1');

setTimeout(() => console.log('2'), 0);   // macrotask

Promise.resolve().then(() => console.log('3'));  // microtask

console.log('4');

// Output: 1 → 4 → 3 → 2
```

**Ứng dụng thực tế:**

- `queueMicrotask()` để defer work mà không delay render
- Tránh long-running macrotask (>50ms) — gây jank UI
- `requestAnimationFrame` chạy trước render, dùng cho animation

---

### Tài liệu tham khảo

- [MDN: Event Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Event_loop)
- [MDN: queueMicrotask](https://developer.mozilla.org/en-US/docs/Web/API/Window/queueMicrotask)
- [HTML Spec: Event Loop](https://html.spec.whatwg.org/multipage/webappapis.html#event-loops)

## 4. Critical Rendering Path

**Critical Rendering Path (CRP)** là chuỗi bước browser thực hiện để chuyển HTML/CSS/JS thành pixels trên màn hình.

**Các bước:**

```text
HTML → DOM Tree
CSS  → CSSOM Tree
         ↓
     Render Tree (DOM + CSSOM)
         ↓
     Layout (tính toán vị trí, kích thước)
         ↓
     Paint (vẽ pixels)
         ↓
     Composite (ghép các layer)
```

**Render-blocking resources:**

- **CSS** luôn block render — browser cần CSSOM đầy đủ trước khi render
- **JS** (không có `async`/`defer`) block cả DOM parsing lẫn render

**Tối ưu CRP:**

```html
<!-- CSS: load sớm nhất có thể -->
<link rel="stylesheet" href="critical.css">

<!-- JS: defer để không block parsing -->
<script defer src="app.js"></script>

<!-- Inline critical CSS cho above-the-fold content -->
<style>/* css cho phần hiển thị đầu tiên */</style>
```

**Metrics liên quan:** FCP (First Contentful Paint), LCP (Largest Contentful Paint), CLS (Cumulative Layout Shift).

---

### Tài liệu tham khảo

- [web.dev: Critical Rendering Path](https://web.dev/articles/critical-rendering-path)
- [MDN: Populating the page: how browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)

## 5. Code Splitting Strategies

**Code Splitting** là kỹ thuật chia JS bundle thành nhiều chunks nhỏ, chỉ tải những gì cần thiết.

**Các chiến lược:**

**1. Route-based splitting** (phổ biến nhất)

```jsx
// Next.js — tự động split theo page
// React Router
const Home = lazy(() => import('./pages/Home'));
const About = lazy(() => import('./pages/About'));
```

**2. Component-based splitting** — lazy load component nặng

```jsx
const HeavyChart = lazy(() => import('./HeavyChart'));

function Dashboard() {
  return (
    <Suspense fallback={<Spinner />}>
      <HeavyChart />
    </Suspense>
  );
}
```

**3. Vendor splitting** — tách third-party libraries

```js
// webpack config
optimization: {
  splitChunks: {
    chunks: 'all',
    cacheGroups: {
      vendor: { test: /node_modules/, name: 'vendors' }
    }
  }
}
```

**4. Feature/conditional splitting** — chỉ load khi user cần

```js
button.addEventListener('click', async () => {
  const { openModal } = await import('./modal');
  openModal();
});
```

---

### Tài liệu tham khảo

- [React Docs: lazy](https://react.dev/reference/react/lazy)
- [Webpack: Code Splitting](https://webpack.js.org/guides/code-splitting/)
- [web.dev: Reduce JavaScript payloads with code splitting](https://web.dev/articles/reduce-javascript-payloads-with-code-splitting)

## 6. Dynamic Import Chunking

Khi dùng `import()` dynamic, bundler (Webpack/Vite) tạo ra các **chunk files** riêng.

**Đặt tên chunk với magic comments:**

```js
// Webpack
const module = await import(/* webpackChunkName: "analytics" */ './analytics');

// Vite
const module = await import('./analytics'); // tự đặt tên theo file
```

**Chunk strategies:**

| Loại         | Mô tả                         | Khi dùng                       |
| ------------ | ----------------------------- | ------------------------------ |
| Async chunk  | Tạo từ dynamic import         | Component lazy, feature        |
| Vendor chunk | node_modules tách riêng       | Libraries ổn định, cache lâu   |
| Common chunk | Code dùng chung nhiều route   | Utilities, shared components   |
| Entry chunk  | Điểm vào ứng dụng             | App shell                      |

**Vite config ví dụ:**

```js
build: {
  rollupOptions: {
    output: {
      manualChunks: {
        'react-vendor': ['react', 'react-dom'],
        'ui-vendor': ['@radix-ui/react-dialog'],
      }
    }
  }
}
```

**Cache strategy:** Vendor chunks ít thay đổi → cache lâu bằng content hash (`vendors.abc123.js`).

---

### Tài liệu tham khảo

- [MDN: import()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/import)
- [Vite: Chunking Strategy](https://vitejs.dev/guide/build#chunking-strategy)
- [Webpack: Module Federation](https://webpack.js.org/concepts/module-federation/)

## 7. Preload vs Prefetch vs Preconnect

Ba kỹ thuật Resource Hints để tối ưu tải tài nguyên:

### `preload` — Tải ngay, ưu tiên cao

```html
<link rel="preload" href="font.woff2" as="font" crossorigin>
<link rel="preload" href="hero.jpg" as="image">
```

- Tải tài nguyên **hiện tại cần** nhưng browser chưa khám phá ra
- Không block render, nhưng tải song song với parser
- **Dùng cho:** fonts, critical images, LCP resource, JS chunk sắp dùng

### `prefetch` — Tải trước, ưu tiên thấp

```html
<link rel="prefetch" href="/next-page.js" as="script">
```

- Tải tài nguyên **trang tiếp theo** (idle time)
- Browser có thể bỏ qua nếu bandwidth thấp
- **Dùng cho:** route tiếp theo mà user likely navigate đến

### `preconnect` — Thiết lập kết nối sớm

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="dns-prefetch" href="https://cdn.example.com">
```

- Thực hiện DNS lookup + TCP handshake + TLS negotiation sớm
- Tiết kiệm ~300-500ms khi request thật sự đến
- **Dùng cho:** CDN, third-party APIs, Google Fonts

**Tóm tắt:**

| Hint          | Timing | Ưu tiên | Dùng cho                   |
| ------------- | ------ | ------- | -------------------------- |
| `preload`     | Ngay   | Cao     | Resource trang hiện tại    |
| `prefetch`    | Idle   | Thấp    | Resource trang tiếp theo   |
| `preconnect`  | Ngay   | -       | Domain của third-party     |

---

### Tài liệu tham khảo

- [web.dev: Preload critical assets](https://web.dev/articles/preload-critical-assets)
- [MDN: rel=preload](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preload)
- [MDN: rel=prefetch](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/prefetch)

## 8. CORS Preflight

**CORS (Cross-Origin Resource Sharing)** là cơ chế browser kiểm soát request từ origin này sang origin khác.

**Simple Request** (không cần preflight): GET/POST với headers cơ bản, Content-Type là `text/plain` / `multipart/form-data` / `application/x-www-form-urlencoded`.

**Preflight Request** xảy ra khi request có:

- Method: PUT, DELETE, PATCH...
- Custom headers: `Authorization`, `Content-Type: application/json`...

**Luồng Preflight:**

```text
Browser                          Server
   |                                |
   |-- OPTIONS /api/data ---------->|
   |   Origin: https://app.com      |
   |   Access-Control-Request-Method: POST
   |   Access-Control-Request-Headers: Authorization
   |                                |
   |<-- 204 No Content ------------|
   |   Access-Control-Allow-Origin: https://app.com
   |   Access-Control-Allow-Methods: POST
   |   Access-Control-Allow-Headers: Authorization
   |   Access-Control-Max-Age: 86400  ← cache preflight
   |                                |
   |-- POST /api/data ------------->|  (actual request)
```

**Server config (Express):**

```js
app.use(cors({
  origin: 'https://app.com',
  methods: ['GET', 'POST', 'PUT'],
  allowedHeaders: ['Authorization', 'Content-Type'],
  maxAge: 86400 // cache preflight 24h
}));
```

---

### Tài liệu tham khảo

- [MDN: Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
- [MDN: Preflight request](https://developer.mozilla.org/en-US/docs/Glossary/Preflight_request)
- [Fetch Spec: CORS-preflight](https://fetch.spec.whatwg.org/#cors-preflight-fetch)

## 9. CSRF vs XSS Mitigation

### CSRF (Cross-Site Request Forgery)

Kẻ tấn công lừa browser của user gửi request đến site khác kèm cookie của user.

```text
User đã login bank.com
→ User visit evil.com
→ evil.com gửi request đến bank.com/transfer (kèm cookie bank.com tự động)
→ Bank xử lý vì cookie hợp lệ
```

**Mitigation:**

```text
1. CSRF Token — server tạo token ngẫu nhiên, embed vào form, verify khi submit
2. SameSite Cookie: Lax/Strict — browser không gửi cookie trong cross-site request
3. Double Submit Cookie — gửi token trong cả cookie lẫn header, verify chúng khớp nhau
4. Verify Origin/Referer header
```

```http
Set-Cookie: session=abc; SameSite=Strict; Secure; HttpOnly
```

### XSS (Cross-Site Scripting)

Kẻ tấn công inject script vào trang, chạy trong context của user.

**3 loại XSS:**

- **Stored XSS**: Script lưu vào DB, render cho mọi user
- **Reflected XSS**: Script trong URL, server reflect vào response
- **DOM XSS**: Script thao túng DOM qua JS (không qua server)

**Mitigation:**

```text
1. Escape output — encode < > & " ' khi render user input
2. Content Security Policy (CSP) — chỉ cho phép script từ nguồn tin cậy
3. Không dùng innerHTML với user input — dùng textContent
4. HttpOnly cookie — JS không thể đọc cookie
5. Sanitize HTML — dùng DOMPurify nếu cần render HTML
```

```html
<!-- CSP Header -->
Content-Security-Policy: default-src 'self'; script-src 'self' 'nonce-{random}'
```

```js
// ❌ XSS vulnerable
element.innerHTML = userInput;

// ✅ Safe
element.textContent = userInput;
// Hoặc nếu cần HTML:
element.innerHTML = DOMPurify.sanitize(userInput);
```

---

### Tài liệu tham khảo

- [OWASP: CSRF](https://owasp.org/www-community/attacks/csrf)
- [MDN: Types of attacks](https://developer.mozilla.org/en-US/docs/Web/Security/Types_of_attacks)
- [MDN: SameSite cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie/SameSite)

## 10. Web Workers vs Service Workers

Cả hai đều chạy trong background thread, không block main thread, nhưng mục đích khác nhau.

### Web Workers — Tính toán nặng

```js
// main.js
const worker = new Worker('./worker.js');
worker.postMessage({ data: hugeArray });
worker.onmessage = (e) => console.log(e.data); // kết quả

// worker.js
self.onmessage = (e) => {
  const result = heavyComputation(e.data);
  self.postMessage(result);
};
```

**Đặc điểm:**

- Không có DOM access
- Giao tiếp qua `postMessage` (copy data)
- Sống theo tab — đóng tab là worker chết
- **Dùng cho:** xử lý ảnh/video, parsing CSV lớn, crypto, WebAssembly

### Service Workers — Network Proxy

```js
// Đăng ký
navigator.serviceWorker.register('/sw.js');

// sw.js — intercept requests
self.addEventListener('fetch', (event) => {
  event.respondWith(
    caches.match(event.request) || fetch(event.request)
  );
});
```

**Đặc điểm:**

- Chạy độc lập với tab (persist sau khi đóng tab)
- Có thể intercept network requests
- Có Cache API
- Cần HTTPS (trừ localhost)
- **Dùng cho:** Offline support (PWA), background sync, push notifications, caching strategy

### So sánh nhanh

| Feature       | Web Worker              | Service Worker           |
| ------------- | ----------------------- | ------------------------ |
| Mục đích      | CPU-heavy tasks         | Network proxy / offline  |
| Vòng đời      | Theo tab                | Độc lập với tab          |
| DOM access    | Không                   | Không                    |
| Network       | Không intercept         | Có thể intercept         |
| Cache API     | Không                   | Có                       |
| Số lượng      | Nhiều                   | 1 per scope              |

### Tài liệu tham khảo

- [MDN: Web Workers API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API)
- [MDN: Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)
- [web.dev: Service workers overview](https://web.dev/articles/service-workers-cache-storage)

## LEVEL 2: React core & rendering mechanics

---

## 11. Reconciliation Algorithm

**Reconciliation** là quá trình React so sánh cây Virtual DOM mới với cây cũ để tìm ra tập hợp thay đổi tối thiểu cần apply lên DOM thật.

**Hai heuristic cốt lõi:**

### 1. Different type → rebuild subtree

```jsx
// Trước
<div><Counter /></div>

// Sau — đổi thành section → React unmount toàn bộ subtree cũ, mount lại mới
<section><Counter /></section>
```

### 2. Same type → update in place

```jsx
// Trước                    // Sau
<div className="old" />  →  <div className="new" />
// React chỉ update attribute, không tạo DOM node mới
```

**List reconciliation với `key`:**

```jsx
// Không có key — React so sánh theo index, thêm đầu list = re-render toàn bộ
[<li>A</li>, <li>B</li>]
→ [<li>X</li>, <li>A</li>, <li>B</li>]  // React thấy: thay A→X, B→A, thêm B

// Có key — React track đúng identity
[<li key="a">A</li>, <li key="b">B</li>]
→ [<li key="x">X</li>, <li key="a">A</li>, <li key="b">B</li>]  // chỉ thêm X
```

**Phases:**

1. **Render phase** (pure, có thể interrupt): tạo "work-in-progress" fiber tree, tính diff
2. **Commit phase** (synchronous, không interrupt): apply changes lên DOM thật, chạy effects

---

### Tài liệu tham khảo

- [React Docs: Reconciliation (legacy)](https://legacy.reactjs.org/docs/reconciliation.html)
- [React Docs: Preserving and Resetting State](https://react.dev/learn/preserving-and-resetting-state)

## 12. Fiber Architecture

**React Fiber** (React 16) là kiến trúc nội bộ hoàn toàn viết lại của React, thay thế stack reconciler cũ.

**Vấn đề của stack reconciler cũ:**

- Reconciliation là một call stack đệ quy, không thể dừng giữa chừng
- Cây lớn → block main thread hàng trăm ms → UI bị lag/drop frame

**Fiber là gì:**

Mỗi React element được ánh xạ thành một **Fiber node** — một JS object chứa:

```js
{
  type,           // component type (div, MyComp...)
  key,
  child,          // fiber con đầu tiên
  sibling,        // fiber anh em kế tiếp
  return,         // fiber cha
  pendingProps,
  memoizedProps,
  memoizedState,
  effectTag,      // INSERT | UPDATE | DELETE
  alternate,      // fiber "bản kia" (double buffering)
}
```

**Double buffering:**

React duy trì 2 fiber trees song song:

- **current tree** — đang hiển thị trên màn hình
- **work-in-progress tree** — đang được build trong render phase

Khi commit xong, hai trees swap vai trò. Nếu bị interrupt, work-in-progress bị discard, không ảnh hưởng current.

**Linked list traversal thay vì đệ quy:**

```text
Fiber A → child → Fiber B → child → Fiber C
                              ↑           |
                              └─ return ──┘
                                 sibling → Fiber D
```

React dùng vòng lặp `while` thay vì đệ quy → có thể `return` ra khỏi vòng lặp bất kỳ lúc nào (preemptible).

---

### Tài liệu tham khảo

- [acdlite: React Fiber Architecture](https://github.com/acdlite/react-fiber-architecture)
- [React Blog: React v18](https://react.dev/blog/2022/03/29/react-v18)

## 13. Concurrent Rendering

**Concurrent Mode** (React 18) cho phép React render nhiều version của UI cùng lúc, có thể interrupt render đang chạy để xử lý update ưu tiên cao hơn.

**Legacy mode vs Concurrent mode:**

```jsx
// Legacy (React 17 trở về)
ReactDOM.render(<App />, root);  // synchronous, blocking

// Concurrent (React 18+)
const root = ReactDOM.createRoot(rootElement);
root.render(<App />);  // concurrent, interruptible
```

**Cơ chế hoạt động:**

```text
User types keystroke (high priority)
  ↓
React đang render heavy list update (low priority)
  ↓
React PAUSE list render
  ↓
React render keystroke update → commit → UI responsive
  ↓
React RESUME list render
```

**APIs khai thác Concurrent rendering:**

```jsx
// startTransition — đánh dấu update là "non-urgent"
import { startTransition } from 'react';

function SearchBar() {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState([]);

  function handleChange(e) {
    setQuery(e.target.value);  // urgent — update input ngay

    startTransition(() => {
      setResults(search(e.target.value));  // non-urgent — có thể delay
    });
  }
}

// useDeferredValue — defer một value cụ thể
const deferredQuery = useDeferredValue(query);
```

---

### Tài liệu tham khảo

- [React Docs: startTransition](https://react.dev/reference/react/startTransition)
- [React WG: New in React 18](https://github.com/reactwg/react-18/discussions/4)

## 14. Time Slicing

**Time Slicing** là kỹ thuật React chia nhỏ render work thành nhiều "slices" nhỏ, yield control về browser giữa các slice để browser có thể xử lý user input và paint frame.

**Vấn đề không có time slicing:**

```text
Frame 1 (16ms):  [──────── JS render (50ms) ──────────────────]  ← JANK
Frame 2 (16ms):  [paint]                                          ← quá muộn
Frame 3 (16ms):  [paint]
```

**Với time slicing:**

```text
Frame 1 (16ms):  [── JS slice 1 (5ms) ──][─ paint ─][─ input ─]
Frame 2 (16ms):  [── JS slice 2 (5ms) ──][─ paint ─]
Frame 3 (16ms):  [── JS slice 3 (5ms) ──][─ paint ─]  ← smooth 60fps
```

**Cơ chế bên trong:**

React Scheduler dùng `MessageChannel` (macrotask) để yield sau mỗi 5ms slice:

```js
// Pseudocode nội bộ của React Scheduler
function workLoop(deadline) {
  while (workInProgress && !shouldYield()) {
    workInProgress = performUnitOfWork(workInProgress);
  }

  if (workInProgress) {
    // Còn việc nhưng hết thời gian → schedule tiếp
    scheduleCallback(workLoop);
  }
}

function shouldYield() {
  return getCurrentTime() - startTime > 5; // yield sau 5ms
}
```

**Lưu ý:** Time slicing chỉ áp dụng cho **render phase**. Commit phase vẫn synchronous (không thể interrupt).

---

### Tài liệu tham khảo

- [React Docs: useTransition](https://react.dev/reference/react/useTransition)
- [web.dev: Optimize Interaction to Next Paint](https://web.dev/articles/optimize-inp)

## 15. Scheduler Priorities

React Scheduler phân loại mọi update thành các mức ưu tiên, quyết định thứ tự và deadline xử lý.

**5 mức ưu tiên (từ cao → thấp):**

| Priority          | Lane                | Timeout  | Ví dụ                              |
| ----------------- | ------------------- | -------- | ---------------------------------- |
| Immediate         | SyncLane            | 0ms      | Flushes synchronously              |
| UserBlocking      | InputContinuousLane | 250ms    | Click, input, hover                |
| Normal            | DefaultLane         | 5000ms   | Fetch data, setTimeout             |
| Low               | TransitionLane      | 10000ms  | `startTransition`, search results  |
| Idle              | IdleLane            | Vô hạn   | Prefetch, analytics                |

**Ví dụ thực tế:**

```jsx
// React tự assign priority dựa theo nguồn gốc của update
element.addEventListener('click', handler);   // → UserBlocking priority
setTimeout(handler, 0);                        // → Normal priority
requestIdleCallback(handler);                  // → Idle priority

// Override manually
startTransition(() => setState(...));          // → Low (Transition) priority
flushSync(() => setState(...));                // → Immediate (synchronous)
```

**Lane model (React 18):**

Mỗi update được gán một "lane" — một bit trong bitmask 31-bit. React có thể batch nhiều updates cùng lane, skip lanes thấp khi lanes cao đang pending.

```js
// Simplified lane constants
const SyncLane          = 0b0000000000000000000000000000001;
const InputContinuous   = 0b0000000000000000000000000000100;
const DefaultLane       = 0b0000000000000000000000000010000;
const TransitionLane1   = 0b0000000000000000000000001000000;
const IdleLane          = 0b0100000000000000000000000000000;
```

---

### Tài liệu tham khảo

- [React Docs: startTransition](https://react.dev/reference/react/startTransition)
- [React Source: Scheduler](https://github.com/facebook/react/tree/main/packages/scheduler)

## 16. Suspense Boundaries

**Suspense** là cơ chế React để "chờ" một điều kiện async (data fetching, lazy import...) và hiển thị fallback UI trong khi chờ.

**Cơ chế hoạt động:**

```jsx
<Suspense fallback={<Spinner />}>
  <UserProfile />   {/* component có thể "suspend" */}
</Suspense>
```

Khi `UserProfile` suspend (throw một Promise), React:

1. Bắt Promise tại Suspense boundary gần nhất
2. Render `fallback` (`<Spinner />`)
3. Khi Promise resolve → re-render `UserProfile`

**Suspend bằng cách nào:**

```jsx
// Thư viện như SWR, React Query, hay use() hook sẽ throw Promise
function UserProfile({ id }) {
  // React 19: use() hook
  const user = use(fetchUser(id));  // throw Promise nếu chưa có data
  return <div>{user.name}</div>;
}

// Hoặc tự implement cache + throw
const cache = new Map();

function fetchWithSuspense(url) {
  if (cache.has(url)) return cache.get(url);

  const promise = fetch(url).then(r => r.json()).then(data => {
    cache.set(url, data);
  });

  throw promise;  // React bắt ở đây
}
```

**Nested Suspense boundaries:**

```jsx
<Suspense fallback={<PageSkeleton />}>
  <Header />
  <Suspense fallback={<FeedSkeleton />}>
    <Feed />          {/* suspend riêng, không ảnh hưởng Header */}
  </Suspense>
  <Suspense fallback={<SidebarSkeleton />}>
    <Sidebar />
  </Suspense>
</Suspense>
```

**Error Boundary + Suspense:**

```jsx
<ErrorBoundary fallback={<ErrorPage />}>
  <Suspense fallback={<Loading />}>
    <DataComponent />
  </Suspense>
</ErrorBoundary>
```

---

### Tài liệu tham khảo

- [React Docs: Suspense](https://react.dev/reference/react/Suspense)
- [React Blog: React v18 Suspense](https://react.dev/blog/2022/03/29/react-v18#suspense-in-react-18)

## 17. Selective Hydration

**Selective Hydration** (React 18) cho phép React hydrate từng phần của trang theo thứ tự ưu tiên, thay vì phải hydrate toàn bộ page trước khi interactive.

**Vấn đề của hydration truyền thống:**

```text
SSR HTML → tải toàn bộ JS → hydrate TOÀN BỘ cây → interactive
                ↑ bottleneck: phải chờ hết, không làm gì được
```

**Với Selective Hydration:**

```jsx
// Wrap sections với Suspense để enable selective hydration
<Layout>
  <NavBar />                    {/* hydrate ngay — không có Suspense */}

  <Suspense fallback={<Skeleton />}>
    <HeavySidebar />            {/* hydrate riêng, async */}
  </Suspense>

  <Suspense fallback={<Skeleton />}>
    <MainContent />             {/* hydrate riêng, async */}
  </Suspense>
</Layout>
```

**Ưu tiên hydration theo user interaction:**

Nếu user click vào `<MainContent>` trong khi `<HeavySidebar>` đang hydrate, React sẽ:

1. Interrupt hydration của Sidebar
2. Hydrate MainContent trước (vì user đang interact)
3. Quay lại hydrate Sidebar sau

```text
Đang hydrate:  [Sidebar ────────]
User click MainContent ↓
React switch:  [MainContent ──] → [Sidebar ────]
```

**Yêu cầu:** Phải dùng `renderToPipeableStream` (Node) hoặc `renderToReadableStream` (Edge) thay vì `renderToString`.

---

### Tài liệu tham khảo

- [React WG: Selective Hydration](https://github.com/reactwg/react-18/discussions/37)
- [React Blog: React v18](https://react.dev/blog/2022/03/29/react-v18)

## 18. Server Components

**React Server Components (RSC)** là components chạy hoàn toàn trên server, không bao giờ được gửi JS sang client.

**So sánh 3 loại component:**

| Loại             | Chạy ở đâu      | JS gửi client | State/Effects | DB access |
| ---------------- | --------------- | ------------- | ------------- | --------- |
| Server Component | Server only     | Không         | Không         | Có        |
| Client Component | Server + Client | Có            | Có            | Không     |
| Shared Component | Cả hai          | Có            | Không         | Không     |

**Ví dụ Server Component (Next.js App Router):**

```jsx
// app/page.tsx — mặc định là Server Component
async function ProductPage({ id }) {
  // Truy cập DB trực tiếp — code này KHÔNG bao giờ xuất hiện ở client
  const product = await db.query(`SELECT * FROM products WHERE id = $1`, [id]);
  const reviews = await fetch(`/api/reviews/${id}`).then(r => r.json());

  return (
    <div>
      <h1>{product.name}</h1>
      <p>{product.description}</p>
      <Reviews data={reviews} />
      <AddToCart id={id} />   {/* Client Component */}
    </div>
  );
}
```

```jsx
// components/AddToCart.tsx — phải opt-in thành Client Component
'use client';

function AddToCart({ id }) {
  const [added, setAdded] = useState(false);
  return (
    <button onClick={() => setAdded(true)}>
      {added ? 'Added!' : 'Add to Cart'}
    </button>
  );
}
```

**Lợi ích:**

- Zero bundle size cho server-only code (lodash, DB clients, markdown parsers...)
- Data fetching trực tiếp, không qua API layer
- Sensitive data (API keys, DB credentials) không bao giờ leak sang client

**Giới hạn:**

- Không dùng `useState`, `useEffect`, event handlers
- Không thể pass functions làm props từ Server → Client Component
- Client Component không thể import Server Component (nhưng có thể nhận làm `children`)

---

### Tài liệu tham khảo

- [React Docs: Server Components](https://react.dev/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023)
- [Next.js: Server Components](https://nextjs.org/docs/app/building-your-application/rendering/server-components)

## 19. Tearing in Concurrent UI

**Tearing** là hiện tượng UI hiển thị dữ liệu không nhất quán — các component khác nhau đọc cùng một external store nhưng thấy các version khác nhau trong một lần render.

**Tại sao Concurrent rendering gây ra tearing:**

```text
React bắt đầu render (đọc store = version 1)
  → render ComponentA → thấy value = 10
  → [React yield — browser xử lý event khác]
  → Store bị update bên ngoài React → value = 20
  → render ComponentB → thấy value = 20  ← TEARING!

UI hiển thị: ComponentA=10, ComponentB=20  (cùng lúc, không nhất quán)
```

**Ví dụ cụ thể:**

```jsx
// Store ngoài React (Redux, Zustand, Jotai...)
let externalStore = { count: 0 };

function ComponentA() {
  return <div>A: {externalStore.count}</div>;  // đọc trực tiếp = nguy hiểm
}

function ComponentB() {
  return <div>B: {externalStore.count}</div>;  // có thể thấy value khác
}
```

**Fix: `useSyncExternalStore`** (React 18)

```jsx
import { useSyncExternalStore } from 'react';

function useStore() {
  return useSyncExternalStore(
    externalStore.subscribe,    // subscribe to changes
    externalStore.getSnapshot,  // read current value (client)
    externalStore.getSnapshot,  // read current value (server)
  );
}

function ComponentA() {
  const { count } = useStore();  // React đảm bảo nhất quán
  return <div>A: {count}</div>;
}
```

**Tại sao `useSyncExternalStore` fix được:**

React force synchronous re-render khi detect store thay đổi trong khi đang render, đảm bảo tất cả components thấy cùng snapshot.

---

### Tài liệu tham khảo

- [React Docs: useSyncExternalStore](https://react.dev/reference/react/useSyncExternalStore)
- [React WG: Tearing discussion](https://github.com/reactwg/react-18/discussions/69)

## 20. Stale Closure Problem

**Stale closure** xảy ra khi một function "bắt" (capture) một giá trị từ scope cũ, và giá trị đó đã thay đổi nhưng function vẫn dùng bản cũ.

**Ví dụ cổ điển:**

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => {
      console.log(count);     // ❌ luôn log 0 — stale closure!
      setCount(count + 1);    // ❌ luôn set 1 — không tăng được
    }, 1000);

    return () => clearInterval(interval);
  }, []);  // [] — effect chỉ chạy 1 lần, capture count=0 mãi mãi
}
```

### Fix 1: Thêm dependency (không phải lúc nào cũng được)

```jsx
useEffect(() => {
  const interval = setInterval(() => {
    setCount(count + 1);
  }, 1000);
  return () => clearInterval(interval);
}, [count]);  // re-create interval mỗi khi count thay đổi — không tối ưu
```

### Fix 2: Functional updater (cách đúng cho state)

```jsx
useEffect(() => {
  const interval = setInterval(() => {
    setCount(c => c + 1);  // ✅ nhận current state, không cần capture count
  }, 1000);
  return () => clearInterval(interval);
}, []);
```

**Fix 3: `useRef` cho giá trị mutable**

```jsx
function useLatest(value) {
  const ref = useRef(value);
  useEffect(() => { ref.current = value; });
  return ref;
}

function Counter() {
  const [count, setCount] = useState(0);
  const latestCount = useLatest(count);

  useEffect(() => {
    const interval = setInterval(() => {
      console.log(latestCount.current);  // ✅ luôn là giá trị mới nhất
    }, 1000);
    return () => clearInterval(interval);
  }, []);
}
```

**Stale closure trong event handlers:**

```jsx
function SearchBar() {
  const [query, setQuery] = useState('');

  // ❌ Mỗi render tạo callback mới nhưng debounce giữ ref cũ
  const handleSearch = debounce((q) => {
    fetch(`/api/search?q=${q}`);
  }, 300);

  // ✅ Dùng useCallback + deps đúng
  const handleSearch = useCallback(
    debounce((q) => fetch(`/api/search?q=${q}`), 300),
    []
  );
}
```

**ESLint plugin `react-hooks/exhaustive-deps`** giúp phát hiện stale closure tự động bằng cách cảnh báo khi dependency array thiếu.

---

### Tài liệu tham khảo

- [React Docs: Removing Effect Dependencies](https://react.dev/learn/removing-effect-dependencies)
- [MDN: Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

## LEVEL 3: Performance nền tảng trình duyệt

---

## 21. Layout Thrashing

**Layout thrashing** (hay **forced synchronous layout**) xảy ra khi JS liên tục xen kẽ đọc và ghi DOM geometry, buộc browser phải recalculate layout nhiều lần trong một frame thay vì một lần.

**Vì sao browser phải recalculate:**

Browser lazy-evaluate layout — nó queue tất cả DOM writes và chỉ recalculate khi cần. Nhưng nếu bạn **đọc** layout property (offsetWidth, getBoundingClientRect...) sau khi **ghi**, browser buộc phải flush queue và tính ngay.

**Ví dụ gây thrashing:**

```js
// ❌ Read → Write → Read → Write... trong vòng lặp
const items = document.querySelectorAll('.item');

items.forEach(item => {
  const width = item.offsetWidth;          // READ — force layout
  item.style.width = (width * 2) + 'px';  // WRITE — invalidate layout
  // Vòng lặp tiếp theo READ lại → force layout lần nữa
});
// Kết quả: N lần layout recalculation thay vì 1
```

**Fix — tách batch reads và writes:**

```js
// ✅ Batch reads trước, writes sau
const widths = Array.from(items).map(item => item.offsetWidth); // batch READ

items.forEach((item, i) => {
  item.style.width = (widths[i] * 2) + 'px';  // batch WRITE
});
// Chỉ 1 lần layout recalculation
```

**Fix với `requestAnimationFrame`:**

```js
// ✅ Đảm bảo write xảy ra ở đầu frame mới
function updateLayout() {
  const width = element.offsetWidth;  // READ

  requestAnimationFrame(() => {
    element.style.width = width * 2 + 'px';  // WRITE ở frame sau
  });
}
```

**Công cụ phát hiện:** Chrome DevTools Performance tab → tìm các "Recalculate Style" / "Layout" màu tím liên tiếp. Library `fastdom` giúp tự động batch read/write.

---

### Tài liệu tham khảo

- [web.dev: Avoid Large, Complex Layouts and Layout Thrashing](https://web.dev/articles/avoid-large-complex-layouts-and-layout-thrashing)
- [Chrome DevTools: Performance](https://developer.chrome.com/docs/devtools/performance)

## 22. Paint vs Layout vs Composite

Ba giai đoạn render pipeline của browser, mỗi giai đoạn có chi phí khác nhau.

**Pipeline đầy đủ:**

```text
JS → Style → Layout → Paint → Composite
           ↑ tốn kém nhất              ↑ rẻ nhất
```

### Layout (Reflow)

Tính toán vị trí và kích thước của tất cả elements.

- **Trigger:** thay đổi bất kỳ property ảnh hưởng geometry
- **Chi phí:** cao — ảnh hưởng toàn bộ cây (hoặc subtree lớn)
- **Ví dụ property:** `width`, `height`, `margin`, `padding`, `top`, `left`, `font-size`, `display`

### Paint

Rasterize pixels vào các layer bitmap (màu sắc, border, shadow...).

- **Trigger:** thay đổi visual property không ảnh hưởng layout
- **Chi phí:** trung bình — chỉ repaint vùng bị thay đổi
- **Ví dụ property:** `color`, `background-color`, `border-color`, `box-shadow`, `outline`

### Composite

Ghép các layer đã paint lại với nhau, thực hiện trên GPU.

- **Trigger:** thay đổi property chạy trên compositor thread
- **Chi phí:** thấp nhất — không chạy trên main thread
- **Ví dụ property:** `transform`, `opacity`, `filter` (một số)

**Bảng so sánh:**

| Property           | Layout | Paint | Composite |
| ------------------ | ------ | ----- | --------- |
| `width` / `height` | Có     | Có    | Có        |
| `background-color` | Không  | Có    | Có        |
| `transform`        | Không  | Không | Có        |
| `opacity`          | Không  | Không | Có        |

**Nguyên tắc tối ưu animation:**

```css
/* ❌ Trigger layout + paint mỗi frame */
.box { animation: move 1s; }
@keyframes move {
  from { left: 0; }
  to   { left: 200px; }
}

/* ✅ Chỉ composite — mượt 60fps */
.box { animation: move 1s; }
@keyframes move {
  from { transform: translateX(0); }
  to   { transform: translateX(200px); }
}
```

---

### Tài liệu tham khảo

- [web.dev: Rendering Performance](https://web.dev/articles/rendering-performance)
- [web.dev: Stick to Compositor-Only Properties](https://web.dev/articles/stick-to-compositor-only-properties-and-manage-layer-count)

## 23. Browser Compositing Layers

Browser chia DOM thành nhiều **compositing layers** (layer bitmap), render từng layer riêng rồi ghép lại trên GPU.

**Khi nào browser tạo layer mới (layer promotion):**

```css
/* Explicit promotion */
transform: translateZ(0);         /* hack cũ */
will-change: transform;           /* cách hiện đại */

/* Browser tự promote */
position: fixed;
video, canvas, iframe;
overflow: scroll (với GPU rasterization);
CSS animations trên transform/opacity;
```

**Lợi ích của separate layer:**

```text
Không có layer riêng:
  Scroll → Repaint toàn trang → Composite

Có layer riêng:
  Scroll → Composite chỉ layer đó (không repaint)
```

**Ví dụ thực tế — sticky header:**

```css
/* ✅ Promote header thành layer riêng để scroll mượt */
.header {
  position: sticky;
  top: 0;
  will-change: transform;
}
```

### Vấn đề: Layer explosion

Tạo quá nhiều layers → tốn VRAM, overhead composite lớn hơn lợi ích.

```css
/* ❌ Promote toàn bộ list items — tốn VRAM */
.list-item {
  will-change: transform;  /* 1000 items = 1000 layers */
}

/* ✅ Chỉ promote khi cần, remove sau khi xong */
.list-item:hover {
  will-change: transform;
}
/* Hoặc add/remove class via JS chỉ khi animate */
```

**Xem layers:** Chrome DevTools → Layers panel (More Tools → Layers).

---

### Tài liệu tham khảo

- [web.dev: Manage Layer Count](https://web.dev/articles/stick-to-compositor-only-properties-and-manage-layer-count)
- [Chrome Blog: GPU Accelerated Compositing](https://developer.chrome.com/blog/gpu-accelerated-compositing-in-chrome)

## 24. GPU Acceleration in CSS

**GPU acceleration** là kỹ thuật chuyển một số render work từ CPU sang GPU, giúp animation mượt hơn và giải phóng main thread.

**Properties chạy trên GPU compositor thread:**

```css
/* Tất cả đều chạy trên GPU, không block JS */
transform: translate/rotate/scale/skew/matrix
opacity: 0 → 1
filter: blur/brightness (hardware accelerated)
backdrop-filter
```

**Cơ chế hoạt động:**

```text
Main thread (CPU):   JS → Style → Layout → Paint → [upload layer to GPU]
Compositor thread (GPU):                                         → Composite
                                                               ↑
                                             Không block JS execution
```

**Khi GPU acceleration thực sự giúp ích:**

```css
/* Slide-in animation — GPU smooth */
.modal {
  transform: translateX(-100%);
  transition: transform 300ms ease;
}
.modal.open {
  transform: translateX(0);
}

/* Fade — GPU smooth */
.overlay {
  opacity: 0;
  transition: opacity 200ms;
}
.overlay.visible {
  opacity: 1;
}
```

**Khi GPU acceleration KHÔNG giúp ích (hoặc có hại):**

```css
/* filter: drop-shadow rất đắt ngay cả trên GPU */
.card:hover {
  filter: drop-shadow(0 10px 20px rgba(0,0,0,0.3));
}

/* Large texture upload — tốn bandwidth CPU↔GPU */
.huge-image {
  will-change: transform;  /* upload texture lớn lên VRAM */
}
```

**Detect GPU layer:** Chrome DevTools → Rendering → Layer borders (hiện border xanh = compositor layer).

---

### Tài liệu tham khảo

- [MDN: will-change](https://developer.mozilla.org/en-US/docs/Web/CSS/will-change)
- [web.dev: Animations Guide](https://web.dev/articles/animations-guide)

## 25. CSS Containment

**CSS Containment** là cơ chế khai báo cho browser biết một element độc lập với phần còn lại của trang, cho phép browser **bỏ qua** phần ngoài scope khi recalculate.

**4 loại containment:**

```css
contain: layout;   /* changes bên trong không ảnh hưởng layout bên ngoài */
contain: style;    /* CSS counters không leak ra ngoài */
contain: paint;    /* nội dung không render ngoài border box */
contain: size;     /* kích thước không phụ thuộc children */

/* Shorthand phổ biến */
contain: layout paint;   /* cả layout + paint */
contain: strict;          /* = layout style paint size */
contain: content;         /* = layout style paint (không có size) */
```

**Ví dụ layout containment:**

```css
/* Không có containment */
.card { /* update 1 card → browser check toàn bộ trang có bị ảnh hưởng không */ }

/* Với containment */
.card {
  contain: layout;
  /* update .card → browser biết chỉ cần recalculate trong .card */
}
```

**`content-visibility`** — dựa trên containment để skip render hoàn toàn:

```css
/* Skip render cho elements ngoài viewport */
.article {
  content-visibility: auto;
  contain-intrinsic-size: 0 500px;  /* placeholder height để scroll đúng */
}
```

Các `.article` ngoài viewport sẽ không paint, giúp initial render nhanh hơn đáng kể với list dài.

**Khi nào dùng:**

```css
/* Widget độc lập: chat box, sidebar, modal */
.chat-widget { contain: strict; }

/* Cards trong list dài */
.product-card { contain: content; }

/* Long document sections */
.page-section { content-visibility: auto; }
```

---

### Tài liệu tham khảo

- [MDN: contain](https://developer.mozilla.org/en-US/docs/Web/CSS/contain)
- [web.dev: CSS Containment](https://web.dev/articles/css-containment)
- [MDN: content-visibility](https://developer.mozilla.org/en-US/docs/Web/CSS/content-visibility)

## 26. Render Blocking Resources

**Render blocking** là khi browser phải dừng construction của render tree để tải và xử lý một resource.

**CSS luôn block render:**

```html
<!-- Browser không render gì cho đến khi CSS này tải xong -->
<link rel="stylesheet" href="styles.css">
```

Browser cần CSSOM hoàn chỉnh để build render tree → bất kỳ CSS nào trong `<head>` đều block.

**JS mặc định block cả parse lẫn render:**

```html
<!-- Dừng HTML parser, tải JS, execute, rồi mới tiếp tục parse -->
<script src="app.js"></script>

<!-- Không block parser, execute sau khi parse xong -->
<script defer src="app.js"></script>

<!-- Không block parser, execute ngay khi tải xong (thứ tự không đảm bảo) -->
<script async src="analytics.js"></script>

<!-- Module: defer by default -->
<script type="module" src="app.js"></script>
```

**So sánh `async` vs `defer`:**

```text
HTML:   [====parse====][===========parse continued=========][DOMContentLoaded]
async:         [fetch][execute]↑ interrupt parse
defer:         [fetch          ][execute after parse]↑ trước DOMContentLoaded
```

**Font blocking:**

```css
/* ❌ FOIT: invisible text cho đến khi font tải xong */
@font-face {
  font-family: 'MyFont';
  src: url('font.woff2');
  /* font-display mặc định là auto → thường block 3s */
}

/* ✅ FOUT: hiện fallback font trước, swap khi load xong */
@font-face {
  font-family: 'MyFont';
  src: url('font.woff2');
  font-display: swap;
}
```

**Checklist loại bỏ render blocking:**

```html
<head>
  <!-- 1. Inline critical CSS -->
  <style>/* above-the-fold styles */</style>

  <!-- 2. Load non-critical CSS async -->
  <link rel="preload" href="non-critical.css" as="style"
        onload="this.rel='stylesheet'">

  <!-- 3. Defer all JS -->
  <script defer src="app.js"></script>

  <!-- 4. Preconnect to font origins -->
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
</head>
```

---

### Tài liệu tham khảo

- [web.dev: Render-Blocking Resources](https://web.dev/articles/render-blocking-resources)
- [MDN: script — defer & async](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)

## 27. Render Waterfalls

**Render waterfall** là chuỗi các requests/operations phụ thuộc nhau tuần tự, mỗi bước phải chờ bước trước hoàn thành trước khi bắt đầu.

**Waterfall điển hình trong React:**

```text
1. Tải HTML
   ↓ (chờ)
2. Parse HTML → phát hiện script → tải JS bundle
   ↓ (chờ)
3. Execute JS → React render → fetch data
   ↓ (chờ)
4. Data về → re-render → fetch data của child component
   ↓ (chờ)
5. Child data về → render final UI
```

**Request waterfall trong components:**

```jsx
// ❌ Sequential waterfall — mỗi component fetch sau khi parent render xong
function App() {
  const user = useFetch('/api/user');
  if (!user) return <Spinner />;
  return <Dashboard userId={user.id} />;
}

function Dashboard({ userId }) {
  const data = useFetch(`/api/dashboard/${userId}`);  // chỉ fetch sau khi có userId
  // ...
}
```

**Fix — Hoist và parallel fetch:**

```jsx
// ✅ Fetch song song ở root, truyền data xuống
async function App() {  // Server Component
  const [user, config] = await Promise.all([
    fetch('/api/user').then(r => r.json()),
    fetch('/api/config').then(r => r.json()),
  ]);

  return <Dashboard user={user} config={config} />;
}
```

**Fix — Parallel Suspense:**

```jsx
// ✅ Nhiều Suspense song song không block nhau
function Page() {
  return (
    <>
      <Suspense fallback={<Skeleton />}>
        <UserPanel />       {/* fetch /api/user */}
      </Suspense>
      <Suspense fallback={<Skeleton />}>
        <FeedPanel />       {/* fetch /api/feed — song song với user */}
      </Suspense>
    </>
  );
}
```

**Các dạng waterfall cần tránh:**

| Loại | Nguyên nhân | Fix |
| ---- | ----------- | --- |
| JS waterfall | Script A load script B load script C | Bundle, dynamic import |
| Data waterfall | Component chain fetch tuần tự | Hoist fetch, Promise.all |
| Font waterfall | CSS → @font-face → font file | `preload` font |
| Image waterfall | JS render → discover images | `preload` LCP image |

---

### Tài liệu tham khảo

- [web.dev: Code-splitting with Suspense](https://web.dev/articles/code-splitting-suspense)
- [Chrome DevTools: Network Waterfall](https://developer.chrome.com/docs/devtools/network/reference)

## 28. Subpixel Rendering

**Subpixel rendering** là kỹ thuật browser dùng các màu con (subpixel) của màn hình LCD để làm cho text và edge trông sắc nét hơn so với độ phân giải thực.

**Cơ chế:**

Màn hình LCD có mỗi pixel gồm 3 subpixel: R-G-B (hoặc B-G-R tùy panel). Browser có thể tô màu từng subpixel riêng để mô phỏng độ phân giải cao hơn 3x theo chiều ngang.

```text
Pixel thật:    [ R | G | B ]  [ R | G | B ]  [ R | G | B ]
Subpixel:       ↑   ↑   ↑      ↑   ↑   ↑      ↑   ↑   ↑
               Điều khiển từng subpixel → "9 điểm" thay vì "3 điểm"
```

**Ảnh hưởng đến CSS:**

```css
/* Subpixel rendering có thể làm layout lệch 0.5px */
.element {
  width: 33.333%;     /* → có thể render thành 133.5px hoặc 134px tùy browser */
  height: 100px;
}

/* Font rendering bị ảnh hưởng bởi GPU layer */
.text {
  /* Khi element được promote lên GPU layer → text có thể blur nhẹ */
  transform: translateZ(0);
  /* Fix: thêm backface-visibility */
  backface-visibility: hidden;
  -webkit-font-smoothing: antialiased;      /* macOS/iOS */
  -moz-osx-font-smoothing: grayscale;       /* Firefox macOS */
}
```

**Subpixel layout issues:**

```css
/* Flexbox/Grid tự handle subpixel tốt hơn float */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);  /* browser tự tính, tránh rounding */
}

/* Nếu cần pixel-perfect */
.item {
  width: calc(100% / 3);
  /* Hoặc dùng integer pixels */
  width: 133px;  /* explicit, predictable */
}
```

**HiDPI / Retina:** Trên màn hình 2x DPR, 1 CSS pixel = 4 physical pixels → subpixel ít quan trọng hơn, nhưng vẫn cần `image-rendering` và SVG thay vì raster cho icon.

---

### Tài liệu tham khảo

- [MDN: font-smooth](https://developer.mozilla.org/en-US/docs/Web/CSS/font-smooth)
- [web.dev: Ensure text remains visible during webfont load](https://web.dev/articles/font-display)

## 29. Detached DOM Nodes

**Detached DOM nodes** là các DOM elements đã bị remove khỏi document nhưng vẫn còn được reference trong JS, khiến Garbage Collector không thể free memory.

**Ví dụ gây memory leak:**

```js
// ❌ Leak 1: Global reference đến removed node
let detachedTree;

function createTree() {
  const ul = document.createElement('ul');
  for (let i = 0; i < 1000; i++) {
    ul.appendChild(document.createElement('li'));
  }
  detachedTree = ul;       // global ref
  document.body.appendChild(ul);
}

function removeTree() {
  document.body.removeChild(detachedTree);
  // detachedTree vẫn giữ ref → toàn bộ subtree không được GC
}
```

```js
// ❌ Leak 2: Event listener giữ ref đến removed node
function setup() {
  const button = document.getElementById('btn');
  const heavyData = new Array(100000).fill('data');

  button.addEventListener('click', () => {
    console.log(heavyData);  // closure giữ heavyData
  });

  button.remove();  // button removed nhưng listener (và heavyData) vẫn sống
}
```

```js
// ❌ Leak 3: Cache Map với DOM nodes
const cache = new Map();

function processElement(el) {
  cache.set(el, computeExpensiveData(el));
  el.remove();
  // Map giữ strong ref → el không được GC
}
```

**Fix:**

```js
// ✅ Null out reference
function removeTree() {
  document.body.removeChild(detachedTree);
  detachedTree = null;  // allow GC
}

// ✅ Remove event listener trước khi remove element
button.removeEventListener('click', handler);
button.remove();

// ✅ WeakMap — không ngăn GC
const cache = new WeakMap();  // key bị GC → entry tự xóa

// ✅ AbortController cho async operations
const controller = new AbortController();
element.addEventListener('click', handler, { signal: controller.signal });
// Khi cleanup:
controller.abort();  // tất cả listeners bị remove
```

**Phát hiện trong Chrome DevTools:**

1. Memory tab → Take heap snapshot
2. Filter "Detached" trong class filter
3. Tìm `Detached HTMLElement` → expand để thấy reference chain

---

### Tài liệu tham khảo

- [Chrome DevTools: Heap Snapshots](https://developer.chrome.com/docs/devtools/memory-problems/heap-snapshots)
- [web.dev: Detached window memory leaks](https://web.dev/articles/detached-window-memory-leaks)

## 30. Garbage Collection Timing

**Garbage Collection (GC)** là quá trình V8 tự động giải phóng memory không còn được reference. Vấn đề là GC có thể chạy **bất kỳ lúc nào**, gây jank nếu xảy ra trong animation frame.

**V8 GC Architecture:**

```text
Heap được chia thành:
├── Young Generation (Nursery + Intermediate) — ~1-8MB
│   └── Minor GC (Scavenge): nhanh (~1ms), chạy thường xuyên
└── Old Generation — có thể hàng GB
    └── Major GC (Mark-Sweep-Compact): chậm (~10-100ms), gây jank
```

**Object lifecycle:**

```text
Allocation → Young Gen → [Minor GC nhiều lần] → survive → Old Gen → [Major GC]
```

**Patterns gây GC pressure:**

```js
// ❌ Tạo nhiều objects tạm thời trong hot path (animation/game loop)
function gameLoop() {
  const velocity = { x: 0, y: 0 };  // new object mỗi frame → GC pressure
  const position = [x, y];           // new array mỗi frame
  // ...
  requestAnimationFrame(gameLoop);
}

// ✅ Reuse objects (object pooling)
const velocity = { x: 0, y: 0 };  // tạo 1 lần

function gameLoop() {
  velocity.x = 0;  // mutate thay vì tạo mới
  velocity.y = 0;
  // ...
  requestAnimationFrame(gameLoop);
}
```

**Object pooling pattern:**

```js
class ParticlePool {
  constructor(size) {
    this.pool = Array.from({ length: size }, () => ({ x: 0, y: 0, active: false }));
  }

  acquire() {
    return this.pool.find(p => !p.active) || null;
  }

  release(particle) {
    particle.active = false;  // trả về pool, không GC
  }
}
```

**Incremental và Concurrent GC (V8):**

V8 dùng incremental marking — chia Mark phase thành nhiều increments nhỏ xen kẽ với JS execution, giảm pause time từ hàng trăm ms xuống còn ~1-5ms.

```text
Trước (stop-the-world):    [JS][==GC 50ms==][JS][JS]
Incremental:               [JS][GC 1ms][JS][GC 1ms][JS][GC 1ms]...
Concurrent (background):   [JS ─────────────────────────────]
                           [   GC chạy song song trên thread khác   ]
```

**Giảm GC pressure trong practice:**

```js
// ✅ String concatenation trong loop → tạo nhiều string tạm
// Dùng array join thay vì +=
const parts = [];
for (let i = 0; i < 1000; i++) parts.push(items[i].name);
const result = parts.join(', ');

// ✅ Avoid closure trong hot loop (mỗi closure = new object)
// ✅ TypedArray cho số lớn thay vì Array (ít GC hơn)
const positions = new Float32Array(1000 * 2);  // không GC như regular array
```

---

### Tài liệu tham khảo

- [V8 Blog: Trash Talk (GC)](https://v8.dev/blog/trash-talk)
- [Chrome DevTools: Memory Problems](https://developer.chrome.com/docs/devtools/memory-problems)

## LEVEL 4: Data & State Management nâng cao

---

## 31. Structural Sharing

**Structural sharing** là kỹ thuật tạo object "mới" khi update mà chỉ copy những phần thực sự thay đổi, các phần còn lại vẫn **trỏ đến cùng reference** với object cũ.

**Tại sao cần:**

```text
Immutability naive:
  state = { a: { x: 1 }, b: { y: 2 }, c: { z: 3 } }
  Update a.x → copy toàn bộ { a, b, c } → tốn memory + phá vỡ referential equality của b, c

Structural sharing:
  Update a.x → tạo object a mới, b và c vẫn là cùng reference
  → b === prevState.b  ✅ → React.memo / selector biết không cần re-render
```

**Ví dụ thủ công:**

```js
const prev = { user: { name: 'Ann', age: 25 }, settings: { theme: 'dark' } };

// ❌ Deep clone — không structural sharing
const next = JSON.parse(JSON.stringify(prev));
next.user.age = 26;
// next.settings !== prev.settings  → reference mới dù không thay đổi

// ✅ Structural sharing — spread chỉ path thay đổi
const next = {
  ...prev,
  user: { ...prev.user, age: 26 },  // user mới
  // settings giữ nguyên reference
};
// next.settings === prev.settings  ✅
```

**Structural sharing trong Immer:**

```js
import produce from 'immer';

const next = produce(prev, draft => {
  draft.user.age = 26;  // Immer tự dùng structural sharing bên trong
});

next.settings === prev.settings;  // ✅ true — không bị clone
next.user === prev.user;          // false — đã thay đổi
```

**Thư viện tối ưu cho structural sharing:**

- **Immer** — mutable syntax, immutable result
- **Immutable.js** — persistent data structures (List, Map, Record)
- **Zustand / Jotai** — dùng structural sharing tự nhiên qua shallow comparison

---

### Tài liệu tham khảo

- [Immer.js Documentation](https://immerjs.github.io/immer/)
- [React Docs: Updating Objects in State](https://react.dev/learn/updating-objects-in-state)

## 32. Immutable Data Patterns

**Immutability** là nguyên tắc không bao giờ mutate data trực tiếp — thay vào đó luôn tạo bản copy mới khi cần thay đổi.

**Tại sao immutability quan trọng trong UI:**

```js
// ❌ Mutate trực tiếp — React không phát hiện thay đổi
const state = { items: [1, 2, 3] };
state.items.push(4);
setState(state);  // cùng reference → React.memo nghĩ không đổi → không re-render

// ✅ Tạo array mới
setState({ items: [...state.items, 4] });  // reference mới → React re-render
```

**Common patterns:**

```js
// Array operations
const arr = [1, 2, 3];

// Thêm phần tử
[...arr, 4]                            // push
[0, ...arr]                            // unshift

// Xóa phần tử
arr.filter(x => x !== 2)              // remove by value
arr.filter((_, i) => i !== 1)         // remove by index

// Update phần tử
arr.map(x => x === 2 ? 99 : x)        // update by value
arr.map((x, i) => i === 1 ? 99 : x)   // update by index

// Object operations
const obj = { a: 1, b: 2, c: 3 };

// Update field
({ ...obj, b: 99 })

// Delete field
const { b, ...rest } = obj;  // rest = { a: 1, c: 3 }

// Nested update
const state = { user: { profile: { name: 'Ann' } } };
({
  ...state,
  user: {
    ...state.user,
    profile: { ...state.user.profile, name: 'Bob' }
  }
})
```

**Immer — viết như mutate, kết quả immutable:**

```js
import produce from 'immer';

const nextState = produce(state, draft => {
  draft.user.profile.name = 'Bob';
  draft.items.push({ id: 4, done: false });
  delete draft.cache['stale-key'];
});
```

**useImmer hook:**

```js
import { useImmer } from 'use-immer';

const [state, updateState] = useImmer({ count: 0, items: [] });

updateState(draft => {
  draft.count += 1;
  draft.items.push('new item');
});
```

---

### Tài liệu tham khảo

- [React Docs: Updating Arrays in State](https://react.dev/learn/updating-arrays-in-state)
- [Immer.js Documentation](https://immerjs.github.io/immer/)

## 33. Referential Equality

**Referential equality** (`===`) so sánh xem hai variables có trỏ đến **cùng một object trong memory** không, không phải so sánh giá trị bên trong.

**Tại sao đây là nguồn gốc của vô số React bugs:**

```js
// Primitive — so sánh giá trị
1 === 1          // true
'abc' === 'abc'  // true

// Object/Array — so sánh reference
{} === {}        // false — hai objects khác nhau trong memory
[] === []        // false

// Vấn đề trong React:
function Parent() {
  const config = { timeout: 3000 };  // object mới mỗi render!
  return <Child config={config} />;  // Child luôn re-render dù config "giống nhau"
}

const Child = React.memo(({ config }) => { ... });
// React.memo dùng === để so sánh → config luôn "khác" → memo vô dụng
```

**Fix với `useMemo` và `useCallback`:**

```jsx
function Parent() {
  // ✅ Stable reference — chỉ tạo lại khi dependency thay đổi
  const config = useMemo(() => ({ timeout: 3000 }), []);
  const handleClick = useCallback(() => { /* ... */ }, []);

  return <Child config={config} onClick={handleClick} />;
}
```

**Shallow equality vs Deep equality:**

```js
// Shallow — so sánh từng key ở level 1
shallowEqual({ a: 1, b: 2 }, { a: 1, b: 2 })   // true
shallowEqual({ a: { x: 1 } }, { a: { x: 1 } }) // false — a là object khác

// Zustand: shallow comparison
import { shallow } from 'zustand/shallow';
const { a, b } = useStore(state => ({ a: state.a, b: state.b }), shallow);
```

**`Object.is` vs `===`:**

```js
// === edge cases
NaN === NaN   // false
+0 === -0     // true

// Object.is (React dùng nội bộ)
Object.is(NaN, NaN)  // true
Object.is(+0, -0)    // false
```

---

### Tài liệu tham khảo

- [React Docs: memo](https://react.dev/reference/react/memo)
- [React Docs: useMemo](https://react.dev/reference/react/useMemo)
- [React Docs: useCallback](https://react.dev/reference/react/useCallback)

## 34. Memoization Pitfalls

**Memoization** là cache kết quả của function dựa theo input. Nhưng dùng sai sẽ gây bugs hoặc không có lợi ích gì.

### Pitfall 1: Over-memoization — thêm chi phí không cần thiết

```jsx
// ❌ Memo cho component cực kỳ đơn giản — overhead > lợi ích
const SimpleLabel = React.memo(({ text }) => <span>{text}</span>);

// ❌ useMemo cho computation rẻ
const doubled = useMemo(() => count * 2, [count]);

// ✅ Chỉ memo khi computation đắt hoặc cần stable reference
const sortedList = useMemo(() => expensiveSort(list), [list]);
```

### Pitfall 2: Stale dependencies

```jsx
// ❌ Thiếu dependency → stale closure
const handleSearch = useCallback(() => {
  fetchData(query);  // query bị capture từ lần đầu
}, []);  // ← thiếu [query]

// ✅
const handleSearch = useCallback(() => {
  fetchData(query);
}, [query]);
```

### Pitfall 3: Object/Array trong dependency array

```jsx
// ❌ options là new object mỗi render → useEffect chạy vô tận
function Component({ options = {} }) {
  useEffect(() => {
    setup(options);
  }, [options]);  // {} !== {} mỗi render

// ✅ Destructure primitives
function Component({ timeout = 3000, retries = 3 }) {
  useEffect(() => {
    setup({ timeout, retries });
  }, [timeout, retries]);
}
```

### Pitfall 4: Memo bị bypass bởi children JSX

```jsx
// ❌ children là JSX mới mỗi render → React.memo bị bypass
const Wrapper = React.memo(({ children }) => <div>{children}</div>);

function Parent() {
  return <Wrapper><span>text</span></Wrapper>;  // JSX object mới mỗi render
}

// ✅ Hoist static children ra ngoài component
const STATIC_CHILDREN = <span>text</span>;
function Parent() {
  return <Wrapper>{STATIC_CHILDREN}</Wrapper>;
}
```

### Pitfall 5: useCallback vô dụng nếu child không React.memo

```jsx
// ❌ useCallback vô ích — Child re-render theo parent dù onClick ổn định
const Child = ({ onClick }) => <button onClick={onClick}>click</button>;

// ✅ Kết hợp useCallback + React.memo mới có hiệu quả
const Child = React.memo(({ onClick }) => <button onClick={onClick}>click</button>);
```

---

### Tài liệu tham khảo

- [React Docs: useMemo](https://react.dev/reference/react/useMemo)
- [React Docs: useCallback](https://react.dev/reference/react/useCallback)
- [React Docs: When to add memo](https://react.dev/reference/react/memo#should-you-add-memo-everywhere)

## 35. Race Conditions in UI State

**Race condition** xảy ra khi nhiều async operations chạy song song và kết quả về theo thứ tự không đoán trước, gây state không nhất quán.

**Ví dụ điển hình — search:**

```text
User gõ "react"   → fetch A bắt đầu
User gõ "reactjs" → fetch B bắt đầu
Fetch B về trước  → setResults(B)
Fetch A về sau    → setResults(A)  ← overwrite kết quả đúng!
```

```jsx
// ❌ Race condition
function Search() {
  const [results, setResults] = useState([]);

  async function handleChange(query) {
    const data = await fetch(`/api/search?q=${query}`).then(r => r.json());
    setResults(data);  // có thể là kết quả của request cũ
  }
}
```

### Fix 1: AbortController

```jsx
useEffect(() => {
  const controller = new AbortController();

  fetch(`/api/search?q=${query}`, { signal: controller.signal })
    .then(r => r.json())
    .then(data => setResults(data))
    .catch(err => {
      if (err.name === 'AbortError') return;  // bị cancel — bỏ qua
      throw err;
    });

  return () => controller.abort();  // cancel khi query thay đổi
}, [query]);
```

### Fix 2: Ignore stale results

```jsx
useEffect(() => {
  let cancelled = false;

  fetchData(query).then(data => {
    if (!cancelled) setResults(data);
  });

  return () => { cancelled = true; };
}, [query]);
```

### Fix 3: React Query — tự động handle

```jsx
const { data } = useQuery({
  queryKey: ['search', query],
  queryFn: () => fetch(`/api/search?q=${query}`).then(r => r.json()),
});
// Tự cancel request cũ, chỉ giữ kết quả query hiện tại
```

---

### Tài liệu tham khảo

- [React Docs: Fetching Data in Effects](https://react.dev/learn/synchronizing-with-effects#fetching-data)
- [MDN: AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)

## 36. Finite State Modeling

**Finite State Machine (FSM)** mô hình hóa UI bằng tập hợp **trạng thái hữu hạn** và **transitions**, thay vì nhiều boolean flags rời rạc tạo ra "impossible states".

**Vấn đề với boolean flags:**

```jsx
// ❌ isLoading=true VÀ isSuccess=true cùng lúc là impossible state
// nhưng code không ngăn điều này xảy ra
const [isLoading, setIsLoading] = useState(false);
const [isSuccess, setIsSuccess] = useState(false);
const [isError, setIsError] = useState(false);
const [data, setData] = useState(null);
```

**Fix — explicit state machine:**

```tsx
type State =
  | { status: 'idle' }
  | { status: 'loading' }
  | { status: 'success'; data: User }
  | { status: 'error'; error: string };

function useUser(id: string) {
  const [state, setState] = useState<State>({ status: 'idle' });

  async function load() {
    setState({ status: 'loading' });
    try {
      const data = await fetchUser(id);
      setState({ status: 'success', data });
    } catch (err) {
      setState({ status: 'error', error: err.message });
    }
  }

  return { state, load };
}

// Render — exhaustive switch
function UserCard({ id }) {
  const { state } = useUser(id);

  switch (state.status) {
    case 'idle':    return <button>Load</button>;
    case 'loading': return <Spinner />;
    case 'success': return <div>{state.data.name}</div>;
    case 'error':   return <div>Error: {state.error}</div>;
  }
}
```

**XState:**

```js
import { createMachine } from 'xstate';
import { useMachine } from '@xstate/react';

const fetchMachine = createMachine({
  initial: 'idle',
  states: {
    idle:    { on: { FETCH: 'loading' } },
    loading: { on: { SUCCESS: 'success', ERROR: 'error' } },
    success: { on: { FETCH: 'loading' } },
    error:   { on: { RETRY: 'loading' } },
  },
});
```

---

### Tài liệu tham khảo

- [XState Documentation](https://xstate.js.org/docs/)
- [Stately: State Machines in React](https://stately.ai/docs)

## 37. Event Sourcing in Frontend

**Event sourcing** lưu trữ **chuỗi events** (những gì đã xảy ra) thay vì lưu trạng thái hiện tại. State được tái tạo bằng cách replay toàn bộ events.

**So sánh:**

```text
State-based: DB lưu { balance: 70 }
  → không biết tiền đến từ đâu, mất khi nào

Event sourcing: DB lưu [Deposit(+200), Withdraw(-50), Transfer(-80)]
  → replay → balance = 70
  → có thể rewind, audit, time-travel debug
```

### Ứng dụng: Undo/Redo

```js
const eventLog = [];

function dispatch(event) {
  eventLog.push(event);
  currentState = applyEvent(currentState, event);
}

function undo() {
  eventLog.pop();
  currentState = eventLog.reduce(applyEvent, initialState);
}
```

**Redux là event sourcing:**

```js
// Actions = events, reducer = applyEvent
const actions = [
  { type: 'ADD_ITEM', payload: { id: 1, name: 'Apple' } },
  { type: 'REMOVE_ITEM', payload: { id: 1 } },
];
// Redux DevTools time-travel = replay events đến điểm bất kỳ
```

**CQRS kết hợp:**

```text
Commands (intent):  AddToCart, Checkout
Events (fact):      ItemAdded, CheckoutCompleted
Queries (read):     getCartItems() = replay(events) → current state
```

---

### Tài liệu tham khảo

- [Redux Docs: Core Concepts](https://redux.js.org/tutorials/fundamentals/part-1-overview)
- [Martin Fowler: Event Sourcing](https://martinfowler.com/eaaDev/EventSourcing.html)

## 38. Optimistic UI Rollback Strategy

**Optimistic UI** cập nhật UI ngay lập tức, giả định server thành công. Nếu server fail → **rollback** về trạng thái trước.

**Luồng:**

```text
User click "Like"
  → 1. Update UI ngay (like += 1)
  → 2. Gửi request server (background)
      ├── OK   → giữ nguyên
      └── FAIL → rollback (like -= 1) + toast error
```

**Implementation cơ bản:**

```jsx
async function handleLike() {
  const prevLiked = liked;
  const prevCount = count;

  // Optimistic update
  setLiked(!liked);
  setCount(c => liked ? c - 1 : c + 1);

  try {
    await toggleLike(postId);
  } catch {
    // Rollback
    setLiked(prevLiked);
    setCount(prevCount);
    toast.error('Thử lại sau.');
  }
}
```

**React Query — built-in optimistic:**

```js
const mutation = useMutation({
  mutationFn: (newTodo) => postTodo(newTodo),

  onMutate: async (newTodo) => {
    await queryClient.cancelQueries({ queryKey: ['todos'] });
    const previousTodos = queryClient.getQueryData(['todos']);  // snapshot

    queryClient.setQueryData(['todos'], old => [...old, newTodo]);  // optimistic

    return { previousTodos };  // pass sang onError
  },

  onError: (err, newTodo, context) => {
    queryClient.setQueryData(['todos'], context.previousTodos);  // rollback
  },

  onSettled: () => {
    queryClient.invalidateQueries({ queryKey: ['todos'] });  // sync server
  },
});
```

---

### Tài liệu tham khảo

- [TanStack Query: Optimistic Updates](https://tanstack.com/query/latest/docs/framework/react/guides/optimistic-updates)
- [React Docs: useOptimistic](https://react.dev/reference/react/useOptimistic)

## 39. Deterministic Rendering

**Deterministic rendering** đảm bảo cùng props + state luôn tạo ra **cùng UI**, bất kể thời điểm hay số lần render.

**Tại sao quan trọng:**

- Hydration mismatch nếu server và client render khác nhau
- Concurrent mode có thể render component nhiều lần trước commit
- Snapshot tests không ổn định

**Anti-patterns vi phạm determinism:**

```jsx
// ❌ Side effects trong render
function Component() {
  analytics.track('viewed');    // chạy nhiều lần trong concurrent mode
  document.title = 'Page';      // DOM mutation trong render

  return <div />;
}

// ❌ Random/time trong render
function Card() {
  return <div id={Math.random()} />;  // khác mỗi lần
}

// ❌ External mutable state không qua React
function UserName() {
  return <span>{window.currentUser.name}</span>;  // thay đổi ngoài React
}
```

**Fix:**

```jsx
// ✅ Side effects → useEffect
useEffect(() => {
  analytics.track('viewed');
  document.title = 'Page';
}, []);

// ✅ External state → useSyncExternalStore
const name = useSyncExternalStore(store.subscribe, () => store.currentUser.name);

// ✅ React StrictMode gọi render 2 lần (dev) để lộ non-determinism
<React.StrictMode><App /></React.StrictMode>
```

---

### Tài liệu tham khảo

- [React Docs: Keeping Components Pure](https://react.dev/learn/keeping-components-pure)
- [React Docs: StrictMode](https://react.dev/reference/react/StrictMode)

## 40. Idempotent UI Actions

**Idempotency**: thực hiện một operation N lần có **kết quả giống như 1 lần**. Quan trọng để tránh duplicate khi user double-click, retry, hay network timeout.

**Non-idempotent vs Idempotent:**

```text
POST /api/order (N lần) → N orders  ← bug
PUT  /api/order/:id (N lần) → 1 order  ✅
POST /api/order + Idempotency-Key (N lần) → 1 order  ✅
```

### Pattern 1: Idempotency key

```js
async function submitOrder(data) {
  const key = crypto.randomUUID();  // tạo 1 lần per intent

  return fetch('/api/orders', {
    method: 'POST',
    headers: { 'Idempotency-Key': key },
    body: JSON.stringify(data),
  });
  // Server dedup: cùng key → trả về kết quả cũ, không tạo mới
}
```

### Pattern 2: Disable sau submit

```jsx
function SubmitButton({ onSubmit }) {
  const [submitted, setSubmitted] = useState(false);

  async function handleClick() {
    if (submitted) return;
    setSubmitted(true);
    try {
      await onSubmit();
    } catch {
      setSubmitted(false);  // allow retry on error
    }
  }

  return (
    <button onClick={handleClick} disabled={submitted}>
      {submitted ? 'Đang xử lý...' : 'Đặt hàng'}
    </button>
  );
}
```

### Pattern 3: Upsert thay vì append

```js
// ❌ Dispatch 2 lần → duplicate
dispatch({ type: 'ADD_NOTIFICATION', payload: notification });

// ✅ Upsert theo id — no-op nếu đã tồn tại
case 'UPSERT_NOTIFICATION': {
  const exists = state.notifications.find(n => n.id === action.payload.id);
  if (exists) return state;
  return { ...state, notifications: [...state.notifications, action.payload] };
}
```

### Pattern 4: Set thay vì toggle

```js
// ❌ Toggle: 2 lần → trạng thái ban đầu (không idempotent)
dispatch({ type: 'TOGGLE_SIDEBAR' });

// ✅ Set: N lần → cùng kết quả
dispatch({ type: 'SET_SIDEBAR', payload: { open: true } });
```

---

### Tài liệu tham khảo

- [MDN: Idempotent](https://developer.mozilla.org/en-US/docs/Glossary/Idempotent)
- [Stripe: Idempotent Requests](https://stripe.com/docs/api/idempotent_requests)

## LEVEL 5: Caching & Networking chiến lược

---

## 41. Cache Invalidation Strategies

**Cache invalidation** là quyết định khi nào dữ liệu cached đã lỗi thời và cần được xóa hoặc refresh. Đây là một trong những bài toán khó nhất trong computer science.

**Các chiến lược chính:**

### TTL (Time-To-Live)

Cache hết hạn sau một khoảng thời gian cố định.

```js
// HTTP header
Cache-Control: max-age=3600  // hết hạn sau 1 giờ

// Redis
await redis.set('user:123', JSON.stringify(user), 'EX', 3600);

// React Query
useQuery({
  queryKey: ['user', id],
  queryFn: fetchUser,
  staleTime: 5 * 60 * 1000,   // fresh 5 phút
  gcTime: 10 * 60 * 1000,     // giữ trong memory 10 phút
});
```

### Event-based invalidation

Xóa cache khi có mutation xảy ra.

```js
// React Query — invalidate sau mutation
const mutation = useMutation({
  mutationFn: updateUser,
  onSuccess: () => {
    queryClient.invalidateQueries({ queryKey: ['user', id] });
    queryClient.invalidateQueries({ queryKey: ['users'] });
  },
});
```

### Cache tags / Surrogate keys

Gắn tag cho cache entries, xóa tất cả entries cùng tag khi cần.

```http
<!-- Server gắn tag -->
Surrogate-Key: user-123 product-456

<!-- Purge tất cả cache liên quan đến user-123 -->
PURGE /api/* Surrogate-Key: user-123
```

### Write-through vs Write-behind

```text
Write-through:  update cache VÀ DB cùng lúc → consistent nhưng chậm hơn
Write-behind:   update cache trước, sync DB sau (async) → nhanh nhưng có thể mất data
Write-around:   bỏ qua cache khi write, chỉ dùng cache cho read → cache miss sau write
```

**Stampede problem — nhiều requests cùng lúc miss cache:**

```js
// ❌ Cache stampede: 1000 requests miss cache cùng lúc → 1000 DB queries
async function getUser(id) {
  const cached = await cache.get(`user:${id}`);
  if (cached) return cached;
  const user = await db.findUser(id);  // tất cả 1000 requests đến đây
  await cache.set(`user:${id}`, user);
  return user;
}

// ✅ Probabilistic early expiration + mutex lock
async function getUser(id) {
  const lock = await mutex.acquire(`user:${id}`);
  try {
    const cached = await cache.get(`user:${id}`);
    if (cached) return cached;
    const user = await db.findUser(id);
    await cache.set(`user:${id}`, user, 'EX', 3600);
    return user;
  } finally {
    lock.release();
  }
}
```

---

### Tài liệu tham khảo

- [MDN: HTTP Caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
- [TanStack Query: Invalidations from Mutations](https://tanstack.com/query/latest/docs/framework/react/guides/invalidations-from-mutations)

## 42. Stale-While-Revalidate

**Stale-While-Revalidate (SWR)** là chiến lược cache: trả về data cũ (stale) ngay lập tức, đồng thời revalidate trong background. User thấy data ngay, data được update sau.

**HTTP Cache-Control header:**

```http
Cache-Control: max-age=60, stale-while-revalidate=300
```

```text
0–60s:    Fresh → serve từ cache, không request
60–360s:  Stale → serve từ cache ngay + gửi request background để refresh
>360s:    Expired → phải chờ request mới
```

**SWR library (Vercel):**

```jsx
import useSWR from 'swr';

function UserProfile({ id }) {
  const { data, error, isLoading } = useSWR(
    `/api/user/${id}`,
    fetcher,
    {
      revalidateOnFocus: true,      // refetch khi tab được focus
      revalidateOnReconnect: true,  // refetch khi online lại
      refreshInterval: 30000,       // polling mỗi 30s
      dedupingInterval: 2000,       // dedup requests trong 2s
    }
  );

  if (isLoading) return <Skeleton />;
  if (error) return <Error />;
  return <div>{data.name}</div>;
}
```

**React Query tương đương:**

```js
useQuery({
  queryKey: ['user', id],
  queryFn: () => fetchUser(id),
  staleTime: 60_000,        // fresh 60s, sau đó stale
  refetchOnWindowFocus: true,
  refetchOnReconnect: true,
});
```

**SWR pattern thủ công:**

```js
async function fetchWithSWR(key, fetcher) {
  const cached = cache.get(key);

  if (cached && !isExpired(cached)) {
    return cached.data;  // fresh — return ngay
  }

  if (cached && isStale(cached)) {
    // Stale — return ngay + revalidate background
    revalidateInBackground(key, fetcher);
    return cached.data;
  }

  // Expired — phải fetch
  const data = await fetcher();
  cache.set(key, { data, timestamp: Date.now() });
  return data;
}
```

---

### Tài liệu tham khảo

- [web.dev: Stale-While-Revalidate](https://web.dev/articles/stale-while-revalidate)
- [SWR Documentation](https://swr.vercel.app/docs/getting-started)

## 43. ETag vs Cache-Control

Hai cơ chế HTTP caching khác nhau: **Cache-Control** kiểm soát *khi nào* fetch lại, **ETag** kiểm soát *liệu có cần* download lại không.

### Cache-Control

Directive header cho browser/CDN biết cách cache response.

```http
# Không cache gì cả (sensitive data)
Cache-Control: no-store

# Cache nhưng luôn revalidate với server trước khi dùng
Cache-Control: no-cache

# Cache public (browser + CDN), hết hạn sau 1 giờ
Cache-Control: public, max-age=3600

# Cache private (chỉ browser, không CDN), 5 phút
Cache-Control: private, max-age=300

# Immutable (content hash trong filename) — cache mãi mãi
Cache-Control: public, max-age=31536000, immutable
```

**Chiến lược cho SPA:**

```text
index.html:         Cache-Control: no-cache  (luôn check version mới)
app.abc123.js:      Cache-Control: max-age=31536000, immutable  (content hash)
images/:            Cache-Control: public, max-age=86400
api responses:      Cache-Control: private, max-age=60, stale-while-revalidate=300
```

### ETag (Entity Tag)

Server gắn "fingerprint" cho response. Browser gửi fingerprint lại để hỏi "có thay đổi không?".

```http
<!-- Server response lần đầu -->
HTTP/1.1 200 OK
ETag: "abc123"
Content-Type: application/json
{ "name": "Ann" }

<!-- Browser request lần sau -->
GET /api/user/1
If-None-Match: "abc123"

<!-- Server: data không đổi → 304, không gửi body -->
HTTP/1.1 304 Not Modified
ETag: "abc123"

<!-- Server: data đã đổi → 200 với data mới -->
HTTP/1.1 200 OK
ETag: "def456"
{ "name": "Bob" }
```

**ETag tiết kiệm bandwidth** (không download body nếu không đổi) nhưng **vẫn tốn round-trip**. Kết hợp cả hai:

```http
Cache-Control: max-age=60    ← tránh request trong 60s
ETag: "abc123"               ← nếu quá 60s, check xem có đổi không trước khi download
```

---

### Tài liệu tham khảo

- [MDN: ETag](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/ETag)
- [MDN: Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)

## 44. HTTP/3 và QUIC

**HTTP/3** là phiên bản mới nhất của HTTP, chạy trên **QUIC** thay vì TCP — giải quyết "head-of-line blocking" của HTTP/2.

**Evolution:**

```text
HTTP/1.1: 1 request/connection → cần nhiều connections song song
HTTP/2:   Multiplexing — nhiều streams trên 1 TCP connection
          → Vẫn có HOL blocking ở TCP layer (1 packet loss = block tất cả streams)
HTTP/3:   Multiplexing trên QUIC (UDP-based)
          → Packet loss chỉ block stream đó, không ảnh hưởng streams khác
```

**QUIC improvements:**

```text
TCP + TLS:                  1.5–2 round trips để establish connection
QUIC (0-RTT resumption):   0 round trips nếu đã kết nối trước đó

TCP HOL blocking:           1 lost packet blocks tất cả streams
QUIC streams:               Mỗi stream độc lập, loss ở stream A không ảnh hưởng stream B

TCP connection migration:   IP thay đổi → phải reconnect
QUIC Connection ID:         IP thay đổi vẫn giữ connection (mobile switching WiFi↔4G)
```

**Tác động thực tế với web:**

```js
// Đo HTTP/3 improvement
// High latency networks (mobile): ~15-20% faster
// Packet loss networks: ~30-40% faster (QUIC handles loss better)
// Low latency networks: ~5% faster (overhead không đáng kể)

// Check HTTP/3 support
const res = await fetch('/api/data');
console.log(res.headers.get('alt-svc'));
// alt-svc: h3=":443"; ma=86400  ← server hỗ trợ HTTP/3
```

**Server Push (deprecated) → Early Hints (103):**

```http
<!-- HTTP/2 Server Push bị xóa khỏi Chrome 2022 -->
<!-- Thay bằng Early Hints (103 status) -->

HTTP/1.1 103 Early Hints
Link: </style.css>; rel=preload; as=style
Link: </script.js>; rel=preload; as=script

HTTP/1.1 200 OK
<!-- ... actual response ... -->
```

---

### Tài liệu tham khảo

- [MDN: HTTP/3](https://developer.mozilla.org/en-US/docs/Glossary/HTTP_3)
- [web.dev: HTTP/2 Performance](https://web.dev/articles/performance-http2)
- [Cloudflare: What is QUIC?](https://www.cloudflare.com/learning/performance/what-is-quic/)

## 45. Backpressure in Streams API

**Backpressure** là cơ chế consumer báo cho producer biết "chậm lại đi, tôi đang bị quá tải" — ngăn producer ghi data nhanh hơn consumer có thể xử lý.

**Vấn đề không có backpressure:**

```text
Producer (server):  gửi 1GB data/s
Consumer (browser): xử lý 10MB data/s
→ Buffer đầy → memory leak → crash
```

**Web Streams API:**

```js
// ReadableStream — đọc data theo chunks
const response = await fetch('/api/large-file');
const reader = response.body.getReader();

while (true) {
  const { done, value } = await reader.read();  // pull-based: chỉ đọc khi sẵn sàng
  if (done) break;
  processChunk(value);  // xử lý chunk trước khi đọc tiếp
}
```

**WritableStream với backpressure:**

```js
const writable = new WritableStream({
  write(chunk, controller) {
    // Trả về Promise → stream đợi resolve trước khi gửi chunk tiếp theo
    return processChunkAsync(chunk);  // backpressure tự động!
  },
  close() { console.log('Done'); },
});

// Pipeline với backpressure tự động
await readableStream.pipeTo(writable);
// pipeTo() tự handle backpressure: đọc từ readable chỉ khi writable sẵn sàng
```

**TransformStream:**

```js
// Ví dụ: stream JSON parsing
const jsonTransform = new TransformStream({
  transform(chunk, controller) {
    const text = new TextDecoder().decode(chunk);
    controller.enqueue(JSON.parse(text));
  },
});

// Pipeline: fetch → parse JSON → process
response.body
  .pipeThrough(new TextDecoderStream())
  .pipeThrough(jsonTransform)
  .pipeTo(processingWritable);
```

**Ứng dụng thực tế:**

```js
// Streaming large response, hiển thị từng phần
async function streamResponse(url, onChunk) {
  const res = await fetch(url);
  const reader = res.body.getReader();
  const decoder = new TextDecoder();

  while (true) {
    const { done, value } = await reader.read();
    if (done) break;
    onChunk(decoder.decode(value, { stream: true }));
    // Browser paint sau mỗi chunk → user thấy nội dung ngay
  }
}
```

---

### Tài liệu tham khảo

- [MDN: Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API)
- [WHATWG Streams Spec](https://streams.spec.whatwg.org/)

## 46. AbortController

**AbortController** là API cho phép cancel các async operations (fetch, event listeners, animations...) theo yêu cầu.

**Cơ chế:**

```js
const controller = new AbortController();
const signal = controller.signal;  // AbortSignal object

// Gắn signal vào operation
fetch('/api/data', { signal });

// Cancel
controller.abort('Reason: user navigated away');

// Check
signal.aborted;       // true
signal.reason;        // 'Reason: user navigated away'
```

**Fetch cancellation:**

```js
function fetchWithTimeout(url, timeoutMs) {
  const controller = new AbortController();

  // Tự cancel sau timeout
  const timeoutId = setTimeout(() => {
    controller.abort(new Error('Request timeout'));
  }, timeoutMs);

  return fetch(url, { signal: controller.signal })
    .then(res => {
      clearTimeout(timeoutId);
      return res.json();
    })
    .catch(err => {
      if (err.name === 'AbortError') throw new Error('Request cancelled');
      throw err;
    });
}
```

**React useEffect cleanup:**

```jsx
useEffect(() => {
  const controller = new AbortController();

  async function loadData() {
    try {
      const data = await fetch(`/api/user/${id}`, {
        signal: controller.signal,
      }).then(r => r.json());
      setUser(data);
    } catch (err) {
      if (err.name !== 'AbortError') setError(err);
    }
  }

  loadData();
  return () => controller.abort();  // cancel khi unmount hoặc id thay đổi
}, [id]);
```

**Cancel nhiều operations cùng lúc:**

```js
// 1 controller cho nhiều fetch
const controller = new AbortController();

Promise.all([
  fetch('/api/users',    { signal: controller.signal }),
  fetch('/api/posts',    { signal: controller.signal }),
  fetch('/api/comments', { signal: controller.signal }),
]);

// Cancel tất cả chỉ với 1 lệnh
controller.abort();
```

**AbortSignal.timeout() — shorthand:**

```js
// Không cần tạo controller thủ công
const res = await fetch('/api/data', {
  signal: AbortSignal.timeout(5000),  // tự cancel sau 5s
});

// Combine: timeout hoặc manual cancel
const signal = AbortSignal.any([
  AbortSignal.timeout(5000),
  controller.signal,
]);
```

---

### Tài liệu tham khảo

- [MDN: AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)
- [MDN: AbortSignal](https://developer.mozilla.org/en-US/docs/Web/API/AbortSignal)

## 47. Streaming Fetch Response Handling

**Streaming fetch** cho phép xử lý response từng chunk khi data đến, không cần đợi toàn bộ response hoàn thành — quan trọng với LLM responses, large file downloads, real-time feeds.

**Đọc stream từng chunk:**

```js
async function streamFetch(url) {
  const response = await fetch(url);

  if (!response.ok) throw new Error(`HTTP ${response.status}`);
  if (!response.body) throw new Error('No body');

  const reader = response.body.getReader();
  const decoder = new TextDecoder();
  let result = '';

  try {
    while (true) {
      const { done, value } = await reader.read();
      if (done) break;

      const chunk = decoder.decode(value, { stream: true });
      result += chunk;
      console.log('Received chunk:', chunk);
    }
  } finally {
    reader.releaseLock();
  }

  return result;
}
```

**Streaming LLM response (ChatGPT style):**

```jsx
async function streamChat(prompt, onToken) {
  const res = await fetch('/api/chat', {
    method: 'POST',
    body: JSON.stringify({ prompt }),
    headers: { 'Content-Type': 'application/json' },
  });

  const reader = res.body.getReader();
  const decoder = new TextDecoder();

  while (true) {
    const { done, value } = await reader.read();
    if (done) break;

    // Server-Sent Events format: "data: {...}\n\n"
    const text = decoder.decode(value, { stream: true });
    const lines = text.split('\n').filter(l => l.startsWith('data: '));

    for (const line of lines) {
      const json = JSON.parse(line.slice(6));
      if (json.token) onToken(json.token);
    }
  }
}

// React component
function ChatMessage({ prompt }) {
  const [text, setText] = useState('');

  useEffect(() => {
    streamChat(prompt, token => {
      setText(prev => prev + token);  // append từng token
    });
  }, [prompt]);

  return <p>{text}<span className="cursor">|</span></p>;
}
```

**Next.js App Router streaming:**

```tsx
// Server Component với streaming
import { Suspense } from 'react';

export default function Page() {
  return (
    <div>
      <h1>Dashboard</h1>
      <Suspense fallback={<Skeleton />}>
        <SlowComponent />  {/* stream riêng, không block phần còn lại */}
      </Suspense>
    </div>
  );
}
```

---

### Tài liệu tham khảo

- [MDN: Using Fetch — Body streams](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
- [MDN: ReadableStream](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStream)

## 48. Priority Hints

**Priority Hints** (`fetchpriority` attribute) cho phép khai báo mức độ ưu tiên tải tài nguyên, giúp browser phân bổ bandwidth tốt hơn.

**Giá trị:**

```html
fetchpriority="high"    <!-- tải ngay, ưu tiên cao -->
fetchpriority="low"     <!-- tải sau, ưu tiên thấp -->
fetchpriority="auto"    <!-- default, browser tự quyết -->
```

**Ảnh — LCP image:**

```html
<!-- ❌ Browser không biết đây là LCP image quan trọng -->
<img src="hero.jpg" alt="Hero">

<!-- ✅ Khai báo priority cao cho LCP image -->
<img src="hero.jpg" alt="Hero" fetchpriority="high">

<!-- ✅ Giảm priority cho images ngoài viewport -->
<img src="banner.jpg" alt="Banner" fetchpriority="low" loading="lazy">
```

**Preload với priority:**

```html
<!-- Font quan trọng — high priority -->
<link rel="preload" href="font.woff2" as="font"
      fetchpriority="high" crossorigin>

<!-- Prefetch trang tiếp theo — low priority -->
<link rel="prefetch" href="/next-page.js"
      fetchpriority="low">
```

**Fetch API:**

```js
// Tải analytics — không quan trọng, không cạnh tranh bandwidth với data chính
fetch('/api/analytics', {
  priority: 'low',
});

// Tải critical config — ưu tiên cao
fetch('/api/config', {
  priority: 'high',
});
```

**Impact thực tế:**

```text
Không có priority hints:
  Browser tải tất cả images cùng bandwidth → LCP image chờ các images khác

Với priority hints:
  hero.jpg (high) → tải trước, LCP nhanh hơn
  below-fold.jpg (low) → tải sau khi LCP xong

Kết quả: LCP cải thiện 10-30% trên slow connections
```

---

### Tài liệu tham khảo

- [web.dev: Priority Hints](https://web.dev/articles/priority-hints)
- [MDN: fetchpriority attribute](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/fetchPriority)

## 49. SameSite Cookie Modes

**SameSite** attribute kiểm soát khi nào browser gửi cookie trong cross-site requests — cơ chế bảo vệ chính chống CSRF.

**Ba mode:**

### `SameSite=Strict`

```http
Set-Cookie: session=abc; SameSite=Strict; Secure
```

- Cookie **không bao giờ** được gửi trong cross-site requests
- Kể cả khi user click link từ trang khác vào site của bạn
- An toàn nhất nhưng UX kém: user click link email → không được đăng nhập

### `SameSite=Lax` (default từ Chrome 80)

```http
Set-Cookie: session=abc; SameSite=Lax; Secure
```

- Cookie được gửi khi user **navigate** đến site (GET top-level navigation)
- Cookie **không** được gửi trong: `<img>`, `<iframe>`, AJAX, POST cross-site
- Cân bằng tốt giữa bảo mật và UX

### `SameSite=None`

```http
Set-Cookie: session=abc; SameSite=None; Secure
```

- Cookie luôn được gửi trong mọi cross-site request
- **Bắt buộc** phải có `Secure` (HTTPS only)
- Dùng cho: embedded widgets, OAuth flows, payment iframes

**So sánh:**

| Scenario                        | Strict | Lax | None |
| ------------------------------- | ------ | --- | ---- |
| User click link từ email        | ❌     | ✅  | ✅   |
| `<form method="POST">` cross    | ❌     | ❌  | ✅   |
| `fetch()` cross-site            | ❌     | ❌  | ✅   |
| `<img src="...">` cross-site    | ❌     | ❌  | ✅   |
| Top-level GET navigation        | ❌     | ✅  | ✅   |

**Double Submit Cookie pattern với Lax:**

```js
// Lax cookie: gửi khi navigate, không gửi trong fetch
// → dùng làm CSRF token qua custom header

// Server set cookie
res.cookie('csrf-token', token, { sameSite: 'Lax', httpOnly: false });

// Client đọc cookie, gửi trong header (cross-site request không thể đọc cookie)
const csrfToken = getCookie('csrf-token');
fetch('/api/action', {
  method: 'POST',
  headers: { 'X-CSRF-Token': csrfToken },
});
```

---

### Tài liệu tham khảo

- [MDN: SameSite cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie/SameSite)
- [web.dev: SameSite cookies explained](https://web.dev/articles/samesite-cookies-explained)

## 50. Speculative Prerendering

**Speculative prerendering** là kỹ thuật browser bắt đầu render trang tiếp theo trong background trước khi user thực sự navigate — navigation gần như instant.

**Speculation Rules API (Chrome 109+):**

```html
<script type="speculationrules">
{
  "prerender": [
    {
      "source": "list",
      "urls": ["/next-page", "/popular-page"]
    }
  ],
  "prefetch": [
    {
      "source": "document",
      "where": { "href_matches": "/products/*" }
    }
  ]
}
</script>
```

**Eagerness levels:**

```html
<script type="speculationrules">
{
  "prerender": [{
    "source": "document",
    "where": { "href_matches": "/*" },
    "eagerness": "moderate"
    // "conservative": chỉ khi hover link (thấp nhất)
    // "moderate": hover hoặc pointer gần link
    // "eager": ngay khi link visible trong viewport
    // "immediate": ngay khi rules được parse (cao nhất, tốn nhất)
  }]
}
</script>
```

**Prerender vs Prefetch:**

```text
Prefetch:   Tải HTML + resources → lưu cache → navigate → parse + execute
Prerender:  Tải HTML → parse → execute JS → render đầy đủ trong hidden tab
            → navigate → swap in (instant!)

Chi phí:
  Prefetch:   1 HTTP request
  Prerender:  Toàn bộ page load (JS, CSS, API calls) nhưng background
```

**Caveats quan trọng:**

```js
// Detect nếu đang được prerendered
if (document.prerendering) {
  // Đừng chạy analytics, ads, side effects
  document.addEventListener('prerenderingchange', () => {
    // Bây giờ user đã thực sự navigate đến
    analytics.track('page_view');
  });
}

// API không safe trong prerender
// ❌ sessionStorage.setItem(...)  → chạy trong context sai
// ❌ navigator.geolocation.getCurrentPosition(...)
// ❌ Payment API, Camera API
// ✅ Đọc data, render UI → OK
```

**Next.js Link prefetch:**

```jsx
// Next.js tự động prefetch (không phải prerender) khi Link vào viewport
<Link href="/about" prefetch={true}>About</Link>

// Disable prefetch cho routes ít dùng
<Link href="/admin" prefetch={false}>Admin</Link>
```

---

### Tài liệu tham khảo

- [Chrome Developers: Prerender pages](https://developer.chrome.com/docs/web-platform/prerender-pages)
- [MDN: Speculation Rules API](https://developer.mozilla.org/en-US/docs/Web/API/Speculation_Rules_API)

## LEVEL 6: Security

---

## 51. Content Security Policy (CSP)

**CSP là gì?**

Content Security Policy là HTTP response header cho phép server khai báo danh sách các nguồn tài nguyên được phép tải trong trang web, giúp ngăn chặn XSS, clickjacking và các injection attacks.

**Cách hoạt động:**

```text
Browser nhận HTML
  → Server gửi header: Content-Security-Policy: ...
  → Browser đọc policy
  → Khi trang cố tải tài nguyên:
      - Nếu nguồn nằm trong whitelist → cho phép
      - Nếu không → chặn + báo cáo vi phạm (nếu có report-uri)
```

**Các directive quan trọng:**

| Directive | Ý nghĩa |
| --- | --- |
| `default-src` | Fallback cho tất cả loại tài nguyên |
| `script-src` | Nguồn JS được phép |
| `style-src` | Nguồn CSS được phép |
| `img-src` | Nguồn ảnh |
| `connect-src` | Fetch/XHR/WebSocket endpoint |
| `frame-src` | iframe nguồn |
| `font-src` | Web fonts |
| `object-src` | Plugin (Flash...) |
| `report-uri` | URL nhận báo cáo vi phạm |

**Ví dụ header CSP thực tế:**

```http
Content-Security-Policy:
  default-src 'self';
  script-src 'self' https://cdn.example.com 'nonce-abc123';
  style-src 'self' 'unsafe-inline';
  img-src 'self' data: https://images.example.com;
  connect-src 'self' https://api.example.com;
  frame-src 'none';
  object-src 'none';
  report-uri /csp-report
```

**Nonce-based CSP (khuyến nghị):**

```html
<!-- Server tạo nonce ngẫu nhiên mỗi request -->
<script nonce="abc123xyz">
  // Code hợp lệ - có nonce khớp với header
  console.log('trusted script');
</script>

<!-- Script inject bởi attacker không có nonce → bị chặn -->
<script>alert('xss')</script>
```

```http
Content-Security-Policy: script-src 'nonce-abc123xyz'
```

**CSP Report-Only (test trước khi enforce):**

```http
Content-Security-Policy-Report-Only:
  default-src 'self';
  script-src 'self';
  report-uri /csp-violations
```

**Next.js CSP setup:**

```js
// next.config.js
const nonce = Buffer.from(crypto.randomUUID()).toString('base64');

const cspHeader = `
  default-src 'self';
  script-src 'self' 'nonce-${nonce}' 'strict-dynamic';
  style-src 'self' 'nonce-${nonce}';
  img-src 'self' blob: data:;
  font-src 'self';
  object-src 'none';
  base-uri 'self';
  form-action 'self';
  frame-ancestors 'none';
`;

// middleware.ts
export function middleware(request) {
  const nonce = Buffer.from(crypto.randomUUID()).toString('base64');
  const headers = new Headers(request.headers);
  headers.set('x-nonce', nonce);
  headers.set('Content-Security-Policy', cspHeader.replace(/\s{2,}/g, ' ').trim());
  return NextResponse.next({ request: { headers } });
}
```

---

### Tài liệu tham khảo

- [MDN: Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
- [web.dev: Content Security Policy](https://web.dev/articles/csp)

## 52. Trusted Types

**Vấn đề DOM XSS:**

Kể cả khi đã có CSP, các injection vào DOM API vẫn nguy hiểm:

```js
// DOM XSS sinks phổ biến
element.innerHTML = userInput;         // ❌ nguy hiểm
element.outerHTML = userInput;         // ❌
document.write(userInput);             // ❌
location.href = userInput;             // ❌ nếu data: hoặc javascript:
element.setAttribute('src', userInput); // ❌ tùy attr
```

**Trusted Types là gì?**

Trusted Types là browser API buộc code phải đi qua "policy" trước khi gán vào DOM sink. Ngăn raw string được inject trực tiếp.

**Cách khai báo policy:**

```js
// Tạo Trusted Types policy
const policy = trustedTypes.createPolicy('myPolicy', {
  createHTML: (input) => {
    // Sanitize trước khi dùng
    return DOMPurify.sanitize(input, { RETURN_TRUSTED_TYPE: true });
  },
  createScriptURL: (input) => {
    const url = new URL(input);
    if (url.hostname === 'trusted.example.com') return input;
    throw new Error('Untrusted script URL');
  },
  createScript: (input) => {
    throw new Error('Dynamic scripts not allowed');
  }
});

// Dùng policy thay vì raw string
element.innerHTML = policy.createHTML(userInput);     // ✅ safe
```

**Bật Trusted Types qua CSP:**

```http
Content-Security-Policy:
  require-trusted-types-for 'script';
  trusted-types myPolicy dompurify
```

**Khi vi phạm:**

```js
// ❌ Sẽ throw TypeError nếu Trusted Types bật
element.innerHTML = '<b>hello</b>';
// TypeError: This document requires 'TrustedHTML' assignment

// ✅ Phải dùng qua policy
element.innerHTML = policy.createHTML('<b>hello</b>');
```

**React và Trusted Types:**

```js
// React hỗ trợ Trusted Types natively từ React 18
// dangerouslySetInnerHTML vẫn hoạt động với policy đúng cách
// Không cần config thêm nếu dùng React đúng cách (không bypass)
```

---

### Tài liệu tham khảo

- [web.dev: Trusted Types](https://web.dev/articles/trusted-types)
- [MDN: Trusted Types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/trusted-types)

## 53. DOM Clobbering

**DOM Clobbering là gì?**

DOM Clobbering là kỹ thuật tấn công khai thác việc browser ánh xạ các element có `id` hoặc `name` vào global object (`window`), ghi đè các biến JS toàn cục.

**Cơ chế:**

```html
<!-- Browser tự động tạo window.foo = element -->
<div id="foo"></div>

<script>
  console.log(window.foo); // HTMLDivElement — không phải undefined!
</script>
```

**Kịch bản tấn công:**

```html
<!-- Attacker inject HTML (qua user content, comment...) -->
<a id="config">payload</a>

<script>
  // Code của developer kiểm tra config
  if (!window.config) {
    window.config = { debug: false, apiUrl: '/api' };
  }
  // window.config bị DOM Clobbering → là HTMLElement, không phải object!
  fetch(window.config.apiUrl); // undefined → error hoặc fetch('undefined')
</script>
```

**Tấn công phức tạp hơn:**

```html
<!-- Clobber thuộc tính lồng nhau bằng form + input -->
<form id="config">
  <input name="apiUrl" value="https://evil.com">
</form>

<script>
  console.log(window.config.apiUrl); // "https://evil.com"
</script>
```

**Phòng chống:**

```js
// ❌ Dễ bị clobber
if (window.config) { ... }

// ✅ Kiểm tra type rõ ràng
if (typeof window.config === 'object' && !(window.config instanceof Element)) {
  // safe
}

// ✅ Dùng const/let thay vì global
const config = { apiUrl: '/api' }; // không bị clobber bởi DOM

// ✅ Namespace variables
window.__APP_CONFIG__ = { ... }; // ít khả năng bị clobber hơn
```

**DOMPurify bảo vệ:**

```js
// DOMPurify loại bỏ id/name attributes nguy hiểm
const clean = DOMPurify.sanitize(userHTML, {
  FORBID_ATTR: ['id', 'name'] // ngăn DOM clobbering
});
```

---

### Tài liệu tham khảo

- [PortSwigger: DOM Clobbering](https://portswigger.net/web-security/dom-based/dom-clobbering)
- [OWASP: DOM Clobbering](https://owasp.org/www-community/attacks/DOM_Clobbering)

## 54. Prototype Pollution

**Prototype Pollution là gì?**

Prototype Pollution là lỗ hổng cho phép attacker thêm/ghi đè thuộc tính trên `Object.prototype`, ảnh hưởng đến TẤT CẢ object trong ứng dụng.

**Cơ chế:**

```js
// Mọi object đều kế thừa từ Object.prototype
const obj = {};
obj.__proto__ === Object.prototype; // true

// Nếu pollute Object.prototype:
Object.prototype.isAdmin = true;

// TẤT CẢ object bị ảnh hưởng
const user = { name: 'alice' };
console.log(user.isAdmin); // true ← nguy hiểm!
```

**Kịch bản tấn công thực tế:**

```js
// Hàm deep merge không an toàn (phổ biến trong lodash cũ)
function merge(target, source) {
  for (let key in source) {
    if (typeof source[key] === 'object') {
      target[key] = merge(target[key] || {}, source[key]);
    } else {
      target[key] = source[key];
    }
  }
  return target;
}

// Attacker gửi JSON độc hại
const malicious = JSON.parse('{"__proto__": {"isAdmin": true}}');
merge({}, malicious);

// Tất cả object trong app bị pollute
const session = {};
console.log(session.isAdmin); // true!
```

**Phòng chống:**

```js
// 1. Object.freeze(Object.prototype)
Object.freeze(Object.prototype); // ngăn modification

// 2. Object.create(null) — object không có prototype
const safeObj = Object.create(null);
safeObj.__proto__; // undefined — không kế thừa Object.prototype

// 3. Kiểm tra key nguy hiểm
function safeMerge(target, source) {
  for (const key of Object.keys(source)) {
    if (key === '__proto__' || key === 'constructor' || key === 'prototype') {
      continue; // bỏ qua
    }
    target[key] = source[key];
  }
  return target;
}

// 4. Dùng Map thay Object cho dynamic keys
const safeMap = new Map();
safeMap.set('__proto__', 'value'); // an toàn, không pollute prototype

// 5. JSON Schema validation
// Validate input trước khi merge
```

**Kiểm tra ứng dụng:**

```js
// Test nhanh prototype pollution
const obj = {};
obj['__proto__']['polluted'] = true;
console.log({}.polluted); // true → bị lỗ hổng
```

---

### Tài liệu tham khảo

- [PortSwigger: Prototype Pollution](https://portswigger.net/web-security/prototype-pollution)
- [MDN: Prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

## 55. Same-Origin Policy Nuances

**Same-Origin Policy (SOP) cơ bản:**

Origin = scheme + hostname + port. Hai URL cùng origin khi cả 3 giống nhau.

```text
https://example.com:443/page1   ←→   https://example.com:443/page2  ✅ same origin
https://example.com             ←→   http://example.com              ❌ khác scheme
https://example.com             ←→   https://sub.example.com         ❌ khác host
https://example.com:443         ←→   https://example.com:8080        ❌ khác port
```

**SOP và các loại request:**

| Loại | SOP áp dụng? | Ghi chú |
| --- | --- | --- |
| `fetch()` / `XMLHttpRequest` | Có | Cần CORS để cross-origin |
| Form submit | Không | Cross-origin POST được phép |
| `<img src>` | Không | Tải được, không đọc được pixel (canvas sẽ tainted) |
| `<script src>` | Không | Chạy được, không đọc source |
| `<link rel=stylesheet>` | Không | Áp dụng được |
| `localStorage` / `sessionStorage` | Có | Per-origin isolation |
| `document.cookie` | Partial | Scope theo domain + path |
| `window.postMessage` | Không | Cross-origin messaging được phép |
| `<iframe>` DOM access | Có | Không thể đọc iframe khác origin |

**Canvas origin taint:**

```js
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
const img = new Image();
img.crossOrigin = 'anonymous'; // cần header CORS từ server
img.src = 'https://other-origin.com/image.png';
img.onload = () => {
  ctx.drawImage(img, 0, 0);
  // Nếu không có CORS header → canvas bị "tainted"
  canvas.toDataURL(); // ❌ SecurityError
};
```

**document.domain (deprecated):**

```js
// Cũ: hai subdomain có thể share DOM
// sub1.example.com
document.domain = 'example.com';
// sub2.example.com
document.domain = 'example.com';
// → Giờ có thể access DOM lẫn nhau

// Nhưng đây là bảo mật kém! Chrome đã block từ 2022
// Dùng postMessage thay thế
```

**Cross-origin isolation:**

```http
# Cho phép SharedArrayBuffer và high-resolution timers
Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Embedder-Policy: require-corp
```

---

### Tài liệu tham khảo

- [MDN: Same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)
- [web.dev: Same-origin policy](https://web.dev/articles/same-origin-policy)

## 56. Service Worker Lifecycle Traps

**Service Worker lifecycle:**

```text
Register → Install → Waiting → Activate → Controlling pages
```

**Các bẫy phổ biến:**

### Trap 1: Old SW vẫn chạy

```js
// SW mới đã install nhưng KHÔNG activate ngay
// Vì tab cũ vẫn đang dùng SW cũ

self.addEventListener('install', (event) => {
  // SW mới install OK
  event.waitUntil(caches.open('v2').then(cache => cache.addAll([...])));

  // ✅ Bỏ qua waiting, kích hoạt ngay (dùng cẩn thận!)
  self.skipWaiting();
});

self.addEventListener('activate', (event) => {
  event.waitUntil(clients.claim()); // Chiếm kiểm soát tất cả tabs ngay
});
```

### Trap 2: Cache cũ không bị xóa

```js
const CACHE_NAME = 'app-cache-v2';
const OLD_CACHES = ['app-cache-v1'];

self.addEventListener('activate', (event) => {
  event.waitUntil(
    caches.keys().then(cacheNames =>
      Promise.all(
        cacheNames
          .filter(name => OLD_CACHES.includes(name))
          .map(name => caches.delete(name))
      )
    )
  );
});
```

### Trap 3: SW intercept trong lúc update

```js
// SW cũ đang intercept request
// User refresh → SW mới install nhưng chưa activate
// → Page vẫn dùng SW cũ → có thể serve stale assets

// Giải pháp: Versioned URLs hoặc cache busting
const ASSETS = [
  '/app.abc123.js', // hash trong filename
  '/style.def456.css'
];
```

### Trap 4: SW không update khi file không đổi

```js
// Browser chỉ fetch lại SW file nếu:
// 1. SW file đã thay đổi (byte-diff)
// 2. Tối thiểu 24h từ lần check cuối

// Nếu SW file không đổi, SW không update
// Giải pháp: Đổi tên file hoặc thêm version comment
// Service Worker v2.1.0
```

### Trap 5: SW scope giới hạn

```js
// SW chỉ control URL trong scope của nó
navigator.serviceWorker.register('/sw.js');
// Scope mặc định: /  (toàn bộ origin)

navigator.serviceWorker.register('/admin/sw.js');
// Scope mặc định: /admin/  (chỉ /admin/ trở xuống)

// Mở rộng scope cần header:
// Service-Worker-Allowed: /
```

---

### Tài liệu tham khảo

- [Chrome Developers: Service Worker Lifecycle](https://developer.chrome.com/docs/workbox/service-worker-lifecycle)
- [MDN: Using Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers)

## 57. SharedArrayBuffer

**SharedArrayBuffer là gì?**

SharedArrayBuffer cho phép chia sẻ vùng nhớ (memory) trực tiếp giữa main thread và Web Workers, không cần copy data — nhanh hơn `postMessage`.

**So sánh với postMessage:**

```js
// postMessage: copy data (structured clone)
worker.postMessage(largeArray); // tốn thời gian clone

// SharedArrayBuffer: chia sẻ vùng nhớ thực sự
const sab = new SharedArrayBuffer(1024 * 1024); // 1MB shared
worker.postMessage(sab); // không copy, chỉ chia sẻ reference
```

**Cách dùng:**

```js
// Main thread
const sab = new SharedArrayBuffer(4 * 4); // 4 integers
const arr = new Int32Array(sab);

arr[0] = 42;
worker.postMessage(sab);

// Worker
self.onmessage = ({ data: sab }) => {
  const arr = new Int32Array(sab);
  console.log(arr[0]); // 42 — đọc từ cùng vùng nhớ
  arr[0] = 100; // Ghi lại, main thread cũng thấy!
};
```

**Atomics — đồng bộ hóa:**

```js
// Race condition nếu không dùng Atomics
arr[0]++; // KHÔNG an toàn khi nhiều thread ghi đồng thời

// ✅ Dùng Atomics.add — atomic operation
Atomics.add(arr, 0, 1); // thread-safe increment

// Atomics.wait — block worker thread
Atomics.wait(arr, 0, 0); // chờ arr[0] thay đổi từ 0

// Atomics.notify — wake up waiting threads
Atomics.notify(arr, 0, 1); // đánh thức 1 thread đang wait
```

**Yêu cầu bảo mật (Cross-Origin Isolation):**

```http
# BẮT BUỘC để dùng SharedArrayBuffer
Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Embedder-Policy: require-corp
```

```js
// Kiểm tra xem cross-origin isolated chưa
if (crossOriginIsolated) {
  const sab = new SharedArrayBuffer(1024);
} else {
  console.warn('SharedArrayBuffer requires cross-origin isolation');
}
```

**Use cases:**

- WebAssembly multi-threading (e.g., ffmpeg.wasm)
- Heavy computation với worker pool
- Real-time audio/video processing

---

### Tài liệu tham khảo

- [MDN: SharedArrayBuffer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer)
- [Chrome Blog: Enabling SharedArrayBuffers](https://developer.chrome.com/blog/enabling-shared-array-buffers)

## 58. Transferable Objects

**Transferable Objects là gì?**

Transferable Objects là các object có thể được "chuyển nhượng" quyền sở hữu giữa các thread (main ↔ worker) thay vì copy — zero-copy transfer.

**Cơ chế:**

```text
postMessage với structured clone:
Main → [COPY DATA] → Worker
  Main vẫn có data gốc

postMessage với Transfer:
Main → [CHUYỂN NHƯỢNG] → Worker
  Main KHÔNG còn access data gốc (detached)
```

**Các loại Transferable:**

| Type | Mô tả |
| --- | --- |
| `ArrayBuffer` | Raw binary data |
| `MessagePort` | Channel 2 chiều |
| `ReadableStream` | Streaming data |
| `WritableStream` | Write stream |
| `TransformStream` | Pipe transform |
| `ImageBitmap` | Bitmap image |
| `OffscreenCanvas` | Canvas off-screen |
| `VideoFrame` | Video frame data |
| `AudioData` | Audio frame data |

**Cách dùng ArrayBuffer transfer:**

```js
// Tạo buffer lớn
const buffer = new ArrayBuffer(1024 * 1024 * 100); // 100MB
const view = new Uint8Array(buffer);
view.fill(1);

// Transfer sang worker — không copy!
worker.postMessage(buffer, [buffer]); // [buffer] = danh sách transfer

// Sau khi transfer, buffer bị detach
console.log(buffer.byteLength); // 0 — không còn dữ liệu ở main thread!
console.log(view[0]); // undefined
```

**OffscreenCanvas — render off main thread:**

```js
// Main thread: chuyển canvas sang worker
const canvas = document.getElementById('myCanvas');
const offscreen = canvas.transferControlToOffscreen();

worker.postMessage({ canvas: offscreen }, [offscreen]);

// Worker: render mà không block main thread
self.onmessage = ({ data: { canvas } }) => {
  const ctx = canvas.getContext('2d');
  // Render heavy animations ở đây
  function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    // ... vẽ phức tạp
    requestAnimationFrame(draw);
  }
  draw();
};
```

**MessagePort transfer:**

```js
// Tạo channel kết nối trực tiếp 2 workers
const { port1, port2 } = new MessageChannel();

worker1.postMessage({ port: port1 }, [port1]);
worker2.postMessage({ port: port2 }, [port2]);

// Giờ worker1 và worker2 có thể communicate trực tiếp
// mà không cần qua main thread
```

---

### Tài liệu tham khảo

- [MDN: Transferable objects](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Transferable_objects)
- [MDN: OffscreenCanvas](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)

## 59. CORS Preflight Internals

**Simple vs Preflighted Request:**

Không phải mọi cross-origin request đều có preflight. Chỉ "non-simple" requests mới cần.

**Simple request (không cần preflight):**

- Method: `GET`, `HEAD`, `POST`
- Headers chỉ: `Accept`, `Accept-Language`, `Content-Language`, `Content-Type`
- Content-Type: `text/plain`, `multipart/form-data`, `application/x-www-form-urlencoded`

**Non-simple → cần preflight:**

```js
// Trigger preflight vì Content-Type: application/json
fetch('https://api.other.com/data', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' }, // ← trigger
  body: JSON.stringify({ key: 'value' })
});

// Trigger vì custom header
fetch('https://api.other.com/data', {
  headers: { 'Authorization': 'Bearer token' } // ← trigger
});

// Trigger vì method PUT/DELETE
fetch('https://api.other.com/data', {
  method: 'DELETE' // ← trigger
});
```

**Luồng preflight chi tiết:**

```text
Browser phát hiện non-simple request
  ↓
Gửi OPTIONS request:
  OPTIONS /data HTTP/1.1
  Host: api.other.com
  Origin: https://app.example.com
  Access-Control-Request-Method: POST
  Access-Control-Request-Headers: Content-Type, Authorization
  ↓
Server phản hồi:
  HTTP/1.1 204 No Content
  Access-Control-Allow-Origin: https://app.example.com
  Access-Control-Allow-Methods: GET, POST, PUT, DELETE
  Access-Control-Allow-Headers: Content-Type, Authorization
  Access-Control-Max-Age: 86400   ← cache preflight 24h
  ↓
Browser kiểm tra policy → OK
  ↓
Gửi actual request
```

**Access-Control-Max-Age — cache preflight:**

```http
# Server set max-age để browser cache preflight result
# Không cần OPTIONS mỗi request
Access-Control-Max-Age: 86400  # 24 giờ

# Browser limit: Chrome max 7200s, Firefox max 86400s
```

**Credentials và CORS:**

```js
// Gửi cookie trong cross-origin request
fetch('https://api.other.com/data', {
  credentials: 'include'
});

// Server PHẢI set:
// Access-Control-Allow-Credentials: true
// Access-Control-Allow-Origin: https://app.example.com (KHÔNG dùng *)
```

**Lỗi CORS phổ biến và giải pháp:**

| Lỗi | Nguyên nhân | Giải pháp |
| --- | --- | --- |
| `No 'Access-Control-Allow-Origin'` | Server thiếu header | Thêm CORS header vào server |
| `Wildcard + credentials` | `*` không dùng với credentials | Dùng explicit origin |
| `Preflight fails` | Server không handle OPTIONS | Thêm OPTIONS handler |
| `Header not allowed` | Custom header không trong Allow-Headers | Thêm vào `Access-Control-Allow-Headers` |

---

### Tài liệu tham khảo

- [MDN: CORS in detail](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
- [Fetch Spec: CORS-preflight fetch](https://fetch.spec.whatwg.org/#cors-preflight-fetch)

## 60. Offline Conflict Resolution

**Bài toán conflict:**

Khi user offline và thay đổi data, sau đó reconnect — data local có thể xung đột với data server đã bị người khác sửa.

**Các chiến lược:**

### 1. Last-Write-Wins (LWW)

```js
// Đơn giản nhất: bên nào có timestamp mới hơn thắng
function resolveConflict(local, remote) {
  return local.updatedAt > remote.updatedAt ? local : remote;
}

// ❌ Vấn đề: mất data nếu hai bên edit cùng lúc
// User A sửa lúc 10:00, User B sửa lúc 10:01 → mất sửa đổi của A
```

### 2. Merge field-level

```js
// Merge từng field thay vì toàn bộ document
function fieldLevelMerge(base, local, remote) {
  const result = { ...base };

  for (const key of Object.keys({ ...local, ...remote })) {
    const localChanged = local[key] !== base[key];
    const remoteChanged = remote[key] !== base[key];

    if (localChanged && !remoteChanged) {
      result[key] = local[key]; // chỉ local đổi → lấy local
    } else if (!localChanged && remoteChanged) {
      result[key] = remote[key]; // chỉ remote đổi → lấy remote
    } else if (localChanged && remoteChanged) {
      // Cả hai đều đổi → conflict thực sự → cần user giải quyết
      result[key] = resolveFieldConflict(key, local[key], remote[key]);
    }
  }

  return result;
}
```

### 3. Operational Transformation (OT)

```js
// Dùng cho real-time collaboration (Google Docs style)
// Transform operations dựa trên lịch sử

// Ví dụ: text editor
// Base: "hello"
// Op A (local): insert " world" at pos 5  → "hello world"
// Op B (remote): delete char at pos 0     → "ello"

// OT transform B relative to A:
// B' = delete char at pos 0 (sau khi A đã insert) → "ello world"
```

### 4. CRDT (Conflict-free Replicated Data Types)

```js
// CRDT tự động merge không cần coordination
// Mọi operation đều commutative, associative, idempotent

// Ví dụ: G-Counter (grow-only counter)
class GCounter {
  constructor(nodeId) {
    this.nodeId = nodeId;
    this.counts = {};
  }

  increment() {
    this.counts[this.nodeId] = (this.counts[this.nodeId] || 0) + 1;
  }

  value() {
    return Object.values(this.counts).reduce((a, b) => a + b, 0);
  }

  // Merge luôn đúng bất kể thứ tự
  merge(other) {
    const merged = { ...this.counts };
    for (const [node, count] of Object.entries(other.counts)) {
      merged[node] = Math.max(merged[node] || 0, count);
    }
    this.counts = merged;
  }
}

// LWW-Element-Set CRDT
class LWWSet {
  constructor() {
    this.addMap = new Map();  // key → timestamp
    this.removeMap = new Map();
  }

  add(key, timestamp = Date.now()) {
    if (!this.addMap.has(key) || this.addMap.get(key) < timestamp) {
      this.addMap.set(key, timestamp);
    }
  }

  remove(key, timestamp = Date.now()) {
    if (!this.removeMap.has(key) || this.removeMap.get(key) < timestamp) {
      this.removeMap.set(key, timestamp);
    }
  }

  has(key) {
    const addTime = this.addMap.get(key) || 0;
    const removeTime = this.removeMap.get(key) || 0;
    return addTime > removeTime;
  }

  merge(other) {
    for (const [key, ts] of other.addMap) this.add(key, ts);
    for (const [key, ts] of other.removeMap) this.remove(key, ts);
  }
}
```

**IndexedDB + sync queue pattern:**

```js
// Lưu operations khi offline
const db = await openDB('myApp', 1);

async function mutateOffline(operation) {
  // Áp dụng optimistic update local
  await db.put('data', operation.payload, operation.key);

  // Queue để sync sau
  await db.add('syncQueue', {
    operation,
    timestamp: Date.now(),
    synced: false
  });
}

// Khi online trở lại
async function syncQueue() {
  const pending = await db.getAllFromIndex('syncQueue', 'synced', false);

  for (const item of pending) {
    try {
      const serverResult = await fetch('/api/sync', {
        method: 'POST',
        body: JSON.stringify(item.operation)
      });

      if (serverResult.ok) {
        const resolved = await serverResult.json();
        // Server trả về resolved data (có thể đã merge)
        await db.put('data', resolved, item.operation.key);
        await db.delete('syncQueue', item.id);
      } else if (serverResult.status === 409) {
        // Conflict — cần user giải quyết
        await showConflictDialog(item.operation, await serverResult.json());
      }
    } catch (e) {
      // Vẫn offline, thử lại sau
    }
  }
}

// Listen for online event
window.addEventListener('online', syncQueue);
```

---

### Tài liệu tham khảo

- [web.dev: Offline Cookbook](https://web.dev/articles/offline-cookbook)
- [MDN: IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)

## LEVEL 7: Web Platform Internals

---

## 61. Islands Architecture

**Islands Architecture là gì?**

Islands Architecture là mô hình rendering trong đó phần lớn trang là HTML tĩnh (server-rendered), chỉ những "đảo" (islands) cần tương tác mới được hydrate thành interactive components.

```text
Trang truyền thống (SPA):
  [==== JS bundle lớn hydrate toàn bộ trang ====]

Islands Architecture:
  [  static HTML  ] [🏝 island1] [  static HTML  ] [🏝 island2] [  static  ]
                         ↑                                ↑
                   hydrate riêng                   hydrate riêng
                   (lazy/eager)                    (lazy/eager)
```

**So sánh với các mô hình khác:**

| Mô hình | HTML ban đầu | JS Load | Interactivity |
| --- | --- | --- | --- |
| CSR (SPA) | Rỗng | Toàn bộ app | Sau khi JS load |
| SSR truyền thống | Đầy đủ | Toàn bộ app | Sau hydration |
| Islands | Đầy đủ | Chỉ islands | Progressive |
| Pure Static | Đầy đủ | Không có | Không có |

**Ưu điểm:**

- HTML hiển thị ngay, không chờ JS
- Ít JS hơn — chỉ load JS cho phần interactive
- Hydration song song, độc lập từng island
- Phù hợp content-heavy sites (blog, marketing, docs)

**Framework hỗ trợ Islands:**

```js
// Astro — khai báo island với client directive
---
import Header from './Header.astro';       // static
import SearchBar from './SearchBar.jsx';   // island
import Counter from './Counter.svelte';    // island
---

<Header />                                         // không JS
<SearchBar client:load />                          // hydrate ngay
<Counter client:idle />                            // hydrate khi browser idle
<HeavyWidget client:visible />                     // hydrate khi vào viewport
<Chart client:media="(min-width: 768px)" />        // hydrate khi media query match
```

**client directives trong Astro:**

| Directive | Khi nào hydrate |
| --- | --- |
| `client:load` | Ngay khi page load |
| `client:idle` | Khi `requestIdleCallback` |
| `client:visible` | Khi vào viewport (IntersectionObserver) |
| `client:media` | Khi media query match |
| `client:only` | Chỉ client-side, không SSR |

**Tự implement islands với vanilla JS:**

```js
// Lazy hydrate component khi vào viewport
function createIsland(selector, importFn) {
  const elements = document.querySelectorAll(selector);

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(async (entry) => {
      if (entry.isIntersecting) {
        observer.unobserve(entry.target);
        const { hydrate } = await importFn();
        hydrate(entry.target);
      }
    });
  });

  elements.forEach(el => observer.observe(el));
}

createIsland('[data-island="counter"]', () => import('./counter.js'));
createIsland('[data-island="chart"]', () => import('./chart.js'));
```

---

### Tài liệu tham khảo

- [Jason Miller: Islands Architecture](https://jasonformat.com/islands-architecture/)
- [Astro: Islands](https://docs.astro.build/en/concepts/islands/)

## 62. Partial Hydration

**Partial Hydration là gì?**

Partial Hydration là kỹ thuật chỉ hydrate một phần của component tree — những phần cần JavaScript — thay vì hydrate toàn bộ như SSR truyền thống.

**Full Hydration vs Partial Hydration:**

```text
Full Hydration (React SSR truyền thống):
  Server: render toàn bộ HTML
  Client: download toàn bộ JS → hydrate toàn bộ cây
    → Tốn JS cho cả những component không interactive

Partial Hydration:
  Server: render toàn bộ HTML
  Client: chỉ download JS cho interactive parts
    → Static parts không cần JS → không hydrate
```

**React Server Components (RSC) — partial hydration pattern:**

```jsx
// app/page.tsx — Server Component (không gửi JS)
import { ProductList } from './ProductList'; // Server Component
import { AddToCart } from './AddToCart';     // Client Component

export default function Page() {
  return (
    <div>
      {/* ProductList chạy trên server, không gửi JS xuống client */}
      <ProductList />

      {/* AddToCart cần interactivity → gửi JS */}
      <AddToCart />
    </div>
  );
}
```

```jsx
// AddToCart.tsx — Client Component (có JS)
'use client';
import { useState } from 'react';

export function AddToCart({ productId }) {
  const [added, setAdded] = useState(false);
  return (
    <button onClick={() => setAdded(true)}>
      {added ? 'Added!' : 'Add to Cart'}
    </button>
  );
}
```

**Progressive hydration — hydrate theo độ ưu tiên:**

```jsx
// Hydrate header ngay (trên màn hình)
// Hydrate sidebar khi idle
// Hydrate footer khi scroll đến

import { lazy, Suspense } from 'react';

const LazySidebar = lazy(() => import('./Sidebar'));
const LazyFooter = lazy(() => import('./Footer'));

function App() {
  return (
    <>
      <Header />   {/* hydrate ngay */}
      <Suspense fallback={<div>Loading sidebar...</div>}>
        <LazySidebar />
      </Suspense>
      <main>{/* content */}</main>
      <Suspense fallback={null}>
        <LazyFooter />
      </Suspense>
    </>
  );
}
```

**React 18 Selective Hydration:**

```jsx
// Với React 18, Suspense boundary tạo "hydration unit" riêng
// Click vào component chưa hydrate → React ưu tiên hydrate nó trước

<Suspense fallback={<Spinner />}>
  <Comments />   {/* hydrate riêng, không block phần khác */}
</Suspense>
```

---

### Tài liệu tham khảo

- [Astro: Partial Hydration](https://docs.astro.build/en/concepts/islands/)
- [React WG: Selective Hydration](https://github.com/reactwg/react-18/discussions/37)

## 63. Streaming SSR

**Streaming SSR là gì?**

Streaming SSR cho phép server gửi HTML từng phần (chunks) đến browser ngay khi chúng được render xong, thay vì chờ toàn bộ trang hoàn thành.

**Truyền thống vs Streaming:**

```text
SSR truyền thống:
  Server render 100% → gửi một lần → browser hiển thị
  [====== server rendering (2s) ======] → [hiển thị ngay toàn bộ]

Streaming SSR:
  Server render từng chunk → gửi ngay → browser hiển thị từng phần
  [chunk1 (0.1s)] → browser nhận, hiển thị header
  [chunk2 (0.5s)] → browser nhận, hiển thị nav
  [chunk3 (2s)]   → browser nhận, hiển thị heavy content
```

**HTTP chunked transfer encoding:**

```http
HTTP/1.1 200 OK
Content-Type: text/html
Transfer-Encoding: chunked

3a
<html><head><title>Page</title></head><body>
...
```

**React 18 renderToPipeableStream:**

```js
// server.js (Node.js)
import { renderToPipeableStream } from 'react-dom/server';
import App from './App';

app.get('/', (req, res) => {
  res.setHeader('Content-Type', 'text/html');

  const { pipe } = renderToPipeableStream(<App />, {
    bootstrapScripts: ['/client.js'],

    onShellReady() {
      // Gửi shell (layout) ngay khi sẵn sàng
      res.statusCode = 200;
      pipe(res);
    },

    onShellError(error) {
      // Nếu shell lỗi → fallback
      res.statusCode = 500;
      res.send('<h1>Something went wrong</h1>');
    },

    onAllReady() {
      // Toàn bộ content đã render
      // (dùng cho crawlers cần full HTML)
    }
  });
});
```

**Suspense + Streaming — lazy data fetching:**

```jsx
// server component với data fetching
async function Comments({ postId }) {
  // Data fetch chậm — nhưng không block phần khác
  const comments = await fetchComments(postId); // chậm
  return <CommentList comments={comments} />;
}

function Page({ postId }) {
  return (
    <>
      <Header />        {/* stream ngay */}
      <MainContent />   {/* stream ngay */}

      {/* Suspense boundary — stream placeholder trước, thay bằng content sau */}
      <Suspense fallback={<CommentsSkeleton />}>
        <Comments postId={postId} />
      </Suspense>
    </>
  );
}
```

**Next.js App Router streaming:**

```jsx
// app/page.tsx
import { Suspense } from 'react';
import { ProductList } from './ProductList';
import { Reviews } from './Reviews'; // chậm

export default function Page() {
  return (
    <div>
      <ProductList />   {/* render ngay */}

      <Suspense fallback={<p>Loading reviews...</p>}>
        <Reviews />     {/* stream sau khi fetch xong */}
      </Suspense>
    </div>
  );
}
```

---

### Tài liệu tham khảo

- [React Docs: renderToPipeableStream](https://react.dev/reference/react-dom/server/renderToPipeableStream)
- [Next.js: Loading UI & Streaming](https://nextjs.org/docs/app/building-your-application/routing/loading-ui-and-streaming)

## 64. Shadow DOM

**Shadow DOM là gì?**

Shadow DOM tạo ra một DOM tree cô lập, đóng gói bên trong một element. CSS và JS bên ngoài không thể xâm nhập vào shadow tree, và ngược lại.

**Cấu trúc:**

```text
Document DOM (Light DOM)
  └── <div id="host">          ← Shadow Host
        #shadow-root (open)    ← Shadow Root
          └── <style>          ← Encapsulated styles
          └── <slot>           ← Slot cho Light DOM content
          └── <div class="internal">  ← Internal elements
```

**Tạo Shadow DOM:**

```js
// Tạo shadow root
const host = document.querySelector('#host');
const shadow = host.attachShadow({ mode: 'open' });   // accessible via el.shadowRoot
// hoặc:
// host.attachShadow({ mode: 'closed' });              // không accessible từ ngoài

// Thêm nội dung vào shadow
shadow.innerHTML = `
  <style>
    /* CSS này CHỈ áp dụng trong shadow DOM */
    p { color: red; }
    :host { display: block; border: 1px solid blue; }
  </style>
  <p>This is inside shadow DOM</p>
  <slot></slot>
`;
```

**CSS encapsulation — không bị leak:**

```html
<my-card>
  <span>Light DOM content</span>
</my-card>

<style>
  /* Style này KHÔNG ảnh hưởng vào shadow DOM của my-card */
  p { color: green; }
</style>

<!-- Bên trong shadow root của my-card: -->
<!-- <p> vẫn màu red theo shadow style, không bị override -->
```

**CSS custom properties xuyên qua shadow boundary:**

```css
/* Light DOM — có thể customize shadow DOM qua CSS variables */
my-card {
  --card-bg: lightblue;
  --card-radius: 8px;
}

/* Bên trong shadow DOM */
:host {
  background: var(--card-bg, white);
  border-radius: var(--card-radius, 4px);
}
```

**Slots — nhận content từ Light DOM:**

```html
<!-- Custom element definition -->
<template id="my-card-template">
  <style>:host { display: block; padding: 16px; }</style>
  <div class="header">
    <slot name="title">Default Title</slot>   <!-- named slot -->
  </div>
  <div class="body">
    <slot></slot>   <!-- default slot -->
  </div>
</template>

<!-- Usage -->
<my-card>
  <h2 slot="title">Card Title</h2>   <!-- vào named slot -->
  <p>Card content</p>                <!-- vào default slot -->
</my-card>
```

**Event retargeting:**

```js
// Events từ shadow DOM bị "retarget" khi bubble ra ngoài
const shadow = host.attachShadow({ mode: 'open' });
shadow.innerHTML = '<button>Click</button>';

shadow.querySelector('button').addEventListener('click', (e) => {
  console.log(e.target); // <button> — bên trong shadow
});

host.addEventListener('click', (e) => {
  console.log(e.target); // <div id="host"> — bị retarget!
});
```

---

### Tài liệu tham khảo

- [MDN: Using Shadow DOM](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_shadow_DOM)
- [web.dev: Shadow DOM v1](https://web.dev/articles/shadowdom-v1)

## 65. Custom Elements Lifecycle

**Custom Elements là gì?**

Custom Elements là Web Components API cho phép tạo HTML tags tùy chỉnh với behavior riêng, tích hợp native vào browser.

**Hai loại Custom Elements:**

```js
// 1. Autonomous custom element (extends HTMLElement)
class MyButton extends HTMLElement { ... }
customElements.define('my-button', MyButton);
// Dùng: <my-button>

// 2. Customized built-in element (extends existing element)
class FancyButton extends HTMLButtonElement { ... }
customElements.define('fancy-button', FancyButton, { extends: 'button' });
// Dùng: <button is="fancy-button">
```

**Lifecycle callbacks đầy đủ:**

```js
class MyComponent extends HTMLElement {
  constructor() {
    super();
    // Gọi khi element được tạo (new MyComponent() hoặc parser gặp tag)
    // KHÔNG truy cập children hay attributes ở đây — chưa có
    this.attachShadow({ mode: 'open' });
  }

  connectedCallback() {
    // Gọi khi element được thêm vào DOM
    // Giống componentDidMount
    // Có thể gọi nhiều lần (move element giữa các DOM)
    this.shadowRoot.innerHTML = `<p>Hello from ${this.tagName}</p>`;
    this._startTimer();
  }

  disconnectedCallback() {
    // Gọi khi element bị xóa khỏi DOM
    // Giống componentWillUnmount
    // Cleanup: timers, listeners, subscriptions
    this._stopTimer();
  }

  adoptedCallback() {
    // Gọi khi element được move sang document khác
    // (e.g., iframe document)
    console.log('Adopted into new document');
  }

  static get observedAttributes() {
    // Khai báo attributes cần theo dõi
    return ['color', 'size', 'disabled'];
  }

  attributeChangedCallback(name, oldValue, newValue) {
    // Gọi khi observed attribute thay đổi
    // Giống getDerivedStateFromProps / useEffect([prop])
    if (name === 'color') {
      this.shadowRoot.querySelector('p').style.color = newValue;
    }
  }
}

customElements.define('my-component', MyComponent);
```

**Thứ tự lifecycle khi parse HTML:**

```text
constructor()
  → parse attributes
  → parse children
connectedCallback()
  → attributeChangedCallback() (nếu có observed attrs)
```

**Upgrade — element tồn tại trước khi define:**

```html
<!-- HTML parse trước khi JS load -->
<my-button>Click</my-button>
<!-- Lúc này là HTMLElement thông thường (unknown element) -->

<script>
  // Sau khi define → browser "upgrade" element
  customElements.define('my-button', MyButton);
  // → constructor và connectedCallback chạy
</script>
```

```js
// Chờ element upgrade xong
await customElements.whenDefined('my-button');
const el = document.querySelector('my-button');
el.doSomething(); // giờ có method từ MyButton class
```

**Property vs Attribute reflection:**

```js
class MyInput extends HTMLElement {
  // Reflect property <-> attribute
  get value() {
    return this.getAttribute('value') || '';
  }
  set value(val) {
    this.setAttribute('value', val);
  }
}
```

---

### Tài liệu tham khảo

- [MDN: Using custom elements](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_custom_elements)
- [HTML Spec: Custom Elements](https://html.spec.whatwg.org/multipage/custom-elements.html)

## 66. Web Components Interoperability

**Vấn đề interoperability:**

Web Components hoạt động với bất kỳ framework nào, nhưng có những edge cases cần chú ý khi tích hợp.

**React và Web Components:**

```jsx
// React 18 và trước: props truyền qua attributes (string only)
// React 19+: tự động map props → properties (fixed!)

// React 18 workaround — dùng ref để set properties
function MyPage() {
  const ref = useRef(null);

  useEffect(() => {
    if (ref.current) {
      ref.current.data = { complex: 'object' }; // set property, không phải attribute
    }
  }, []);

  return <my-chart ref={ref} title="Sales" />;
}

// React 19 — tự động handle
function MyPage() {
  return <my-chart data={{ complex: 'object' }} title="Sales" />;
  // React 19 tự động: string → attribute, non-string → property
}
```

**Event handling trong React:**

```jsx
// Web Component dispatch custom events
// React chỉ listen synthetic events, không tự listen custom events

function App() {
  const ref = useRef(null);

  useEffect(() => {
    const el = ref.current;
    const handler = (e) => console.log('custom event:', e.detail);
    el.addEventListener('my-custom-event', handler);
    return () => el.removeEventListener('my-custom-event', handler);
  }, []);

  return <my-component ref={ref} />;
}
```

**Vue và Web Components:**

```vue
<!-- Vue nhận biết custom elements -->
<!-- vite.config.js: compilerOptions.isCustomElement: tag => tag.includes('-') -->

<template>
  <!-- Vue không cố compile my-slider như Vue component -->
  <my-slider :value="sliderValue" @change="handleChange" />
</template>

<script setup>
import { ref } from 'vue';
const sliderValue = ref(50);
const handleChange = (e) => console.log(e.detail);
</script>
```

**Angular và Web Components:**

```ts
// app.module.ts
@NgModule({
  schemas: [CUSTOM_ELEMENTS_SCHEMA], // cho phép unknown elements
})
export class AppModule {}
```

```html
<!-- Angular template -->
<my-datepicker
  [value]="date"
  (dateSelected)="onDateSelected($event)">
</my-datepicker>
```

**Form participation (ElementInternals):**

```js
class MyInput extends HTMLElement {
  static formAssociated = true; // tham gia vào form

  constructor() {
    super();
    this._internals = this.attachInternals();
  }

  set value(v) {
    this._value = v;
    this._internals.setFormValue(v); // gửi value lên form
  }

  // Validation
  checkValidity() {
    if (!this._value) {
      this._internals.setValidity({ valueMissing: true }, 'Required');
      return false;
    }
    this._internals.setValidity({});
    return true;
  }
}
```

---

### Tài liệu tham khảo

- [Custom Elements Everywhere](https://custom-elements-everywhere.com/)
- [MDN: Web Components](https://developer.mozilla.org/en-US/docs/Web/API/Web_components)

## 67. IntersectionObserver Internals

**IntersectionObserver là gì?**

IntersectionObserver theo dõi khi một element giao nhau (intersect) với viewport hoặc ancestor element — mà không cần scroll event listener tốn kém.

**Cơ chế hoạt động:**

```text
Scroll event (cũ):
  scroll → handler → getBoundingClientRect() → check position
  → Chạy mỗi scroll event (60+ lần/giây) → jank!

IntersectionObserver:
  Browser track intersection nội bộ → gọi callback khi threshold vượt qua
  → Async, off main thread → không gây jank
```

**API cơ bản:**

```js
const observer = new IntersectionObserver(
  (entries, observer) => {
    entries.forEach(entry => {
      console.log(entry.target);           // element được observe
      console.log(entry.isIntersecting);   // true/false
      console.log(entry.intersectionRatio); // 0.0 - 1.0
      console.log(entry.boundingClientRect); // element rect
      console.log(entry.intersectionRect);  // phần giao nhau
      console.log(entry.rootBounds);        // root (viewport) rect
      console.log(entry.time);             // DOMHighResTimeStamp
    });
  },
  {
    root: null,           // null = viewport
    rootMargin: '0px',    // mở rộng/thu nhỏ root
    threshold: [0, 0.5, 1] // gọi callback tại 0%, 50%, 100%
  }
);

observer.observe(element);
observer.unobserve(element);
observer.disconnect();
```

**rootMargin — trigger sớm hơn:**

```js
// Preload khi element còn cách viewport 200px
const observer = new IntersectionObserver(callback, {
  rootMargin: '200px 0px',  // top/bottom 200px, left/right 0
});

// Negative margin — chỉ trigger khi element vào sâu hơn
const stickyObserver = new IntersectionObserver(callback, {
  rootMargin: '-100px 0px',
});
```

**Lazy loading images:**

```js
const imageObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const img = entry.target;
      img.src = img.dataset.src;       // load ảnh thật
      img.classList.remove('lazy');
      imageObserver.unobserve(img);    // không cần observe nữa
    }
  });
}, {
  rootMargin: '50px',   // preload trước 50px
  threshold: 0.01       // trigger khi 1% vào viewport
});

document.querySelectorAll('img[data-src]').forEach(img => {
  imageObserver.observe(img);
});
```

**Infinite scroll:**

```js
const sentinel = document.querySelector('#load-more-sentinel');

const loadMoreObserver = new IntersectionObserver(async ([entry]) => {
  if (entry.isIntersecting && !isLoading) {
    isLoading = true;
    const newItems = await fetchMoreItems();
    appendItems(newItems);
    isLoading = false;
  }
});

loadMoreObserver.observe(sentinel);
```

**Chú ý về timing:**

```js
// IntersectionObserver callback chạy async — KHÔNG synchronous
// Entries có thể được batch lại
// entry.time là thời điểm intersection xảy ra, không phải lúc callback chạy

// Nếu cần synchronous check → dùng getBoundingClientRect() (tốn kém hơn)
```

---

### Tài liệu tham khảo

- [MDN: Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
- [web.dev: IntersectionObserver's coming into view](https://web.dev/articles/intersectionobserver)

## 68. ResizeObserver Loop Limits

**ResizeObserver là gì?**

ResizeObserver theo dõi thay đổi kích thước của elements — thay thế cho việc listen `resize` event trên `window`.

**Cơ chế:**

```js
const observer = new ResizeObserver((entries) => {
  entries.forEach(entry => {
    const { width, height } = entry.contentRect;
    console.log(`Element resized: ${width}x${height}`);

    // ResizeObserverEntry cũng có:
    entry.borderBoxSize;        // [{ blockSize, inlineSize }]
    entry.contentBoxSize;       // nội dung (không border/padding)
    entry.devicePixelContentBoxSize; // pixel device thực
  });
});

observer.observe(element);
observer.observe(element, { box: 'border-box' }); // theo dõi border box
observer.unobserve(element);
observer.disconnect();
```

**ResizeObserver Loop Error:**

```text
Đây là lỗi đặc trưng nhất của ResizeObserver:
"ResizeObserver loop limit exceeded"
hoặc
"ResizeObserver loop completed with undelivered notifications"
```

**Nguyên nhân:**

```js
// ❌ Resize loop: callback thay đổi kích thước element đang observe
const observer = new ResizeObserver((entries) => {
  entries.forEach(entry => {
    // Thay đổi width → trigger ResizeObserver lại → loop!
    entry.target.style.width = entry.contentRect.width + 10 + 'px';
  });
});
```

**Giải pháp:**

```js
// ✅ 1. Wrap trong requestAnimationFrame
const observer = new ResizeObserver((entries) => {
  requestAnimationFrame(() => {
    entries.forEach(entry => {
      entry.target.style.width = entry.contentRect.width + 10 + 'px';
    });
  });
});

// ✅ 2. Observe phần tử khác (không phải phần tử đang resize)
const observer = new ResizeObserver((entries) => {
  entries.forEach(entry => {
    // Thay đổi sibling, không phải entry.target
    entry.target.nextElementSibling.style.height =
      entry.contentRect.height + 'px';
  });
});

// ✅ 3. Dùng CSS thay JS khi có thể
// CSS container queries — không cần JS resize observer
@container (min-width: 400px) {
  .card { flex-direction: row; }
}
```

**Lỗi này không phải lỗi thật:**

```js
// Chrome thêm lỗi này vào console nhưng KHÔNG throw exception
// Nếu bạn thấy lỗi này, có thể:
// 1. Đây là resize loop thật → fix code
// 2. Library bên thứ 3 gây ra → ignore hoặc dùng error boundary

// Suppress nếu biết là false positive
window.addEventListener('error', (e) => {
  if (e.message === 'ResizeObserver loop limit exceeded') {
    e.stopImmediatePropagation();
  }
});
```

**Dùng cho responsive components:**

```js
// Component tự điều chỉnh layout theo kích thước chính nó
// (không phụ thuộc viewport width)
class ResponsiveCard extends HTMLElement {
  connectedCallback() {
    this._observer = new ResizeObserver(([entry]) => {
      const width = entry.contentRect.width;
      this.classList.toggle('compact', width < 300);
      this.classList.toggle('wide', width >= 600);
    });
    this._observer.observe(this);
  }

  disconnectedCallback() {
    this._observer.disconnect();
  }
}
```

---

### Tài liệu tham khảo

- [MDN: ResizeObserver](https://developer.mozilla.org/en-US/docs/Web/API/ResizeObserver)
- [W3C: Resize Observer Spec](https://www.w3.org/TR/resize-observer/)

## 69. MutationObserver Cost

**MutationObserver là gì?**

MutationObserver theo dõi thay đổi trong DOM tree — thêm/xóa nodes, thay đổi attributes, text content.

**API:**

```js
const observer = new MutationObserver((mutations) => {
  mutations.forEach(mutation => {
    console.log(mutation.type);           // 'childList' | 'attributes' | 'characterData'
    console.log(mutation.target);         // node bị thay đổi
    console.log(mutation.addedNodes);     // NodeList các node được thêm
    console.log(mutation.removedNodes);   // NodeList các node bị xóa
    console.log(mutation.attributeName);  // tên attribute thay đổi (nếu type='attributes')
    console.log(mutation.oldValue);       // giá trị cũ (nếu bật attributeOldValue)
  });
});

observer.observe(document.body, {
  childList: true,        // theo dõi thêm/xóa children
  subtree: true,          // bao gồm tất cả descendants
  attributes: true,       // theo dõi attribute changes
  attributeFilter: ['class', 'data-state'], // chỉ observe attrs cụ thể
  attributeOldValue: true, // lưu giá trị cũ của attribute
  characterData: true,    // theo dõi text content
  characterDataOldValue: true
});

observer.disconnect();
observer.takeRecords(); // lấy mutations đang pending, clear queue
```

**Chi phí của MutationObserver:**

```text
Chi phí LOW (OK):
  - Observe node cụ thể, không có subtree: true
  - Observe attributes với attributeFilter cụ thể
  - Callback gọn nhẹ

Chi phí HIGH (cẩn thận):
  - subtree: true trên document.body với DOM phức tạp
  - childList + subtree + attributes cùng lúc
  - Callback thực hiện DOM operations (gây thêm mutations)
  - Nhiều observers trên cùng node
```

**Vòng lặp mutation:**

```js
// ❌ Callback tạo ra thêm mutations → loop!
const observer = new MutationObserver((mutations) => {
  mutations.forEach(m => {
    m.target.setAttribute('data-modified', 'true'); // gây thêm mutation!
  });
});

observer.observe(el, { attributes: true });

// ✅ Ngắt tạm thời hoặc kiểm tra trước khi modify
const observer = new MutationObserver((mutations) => {
  observer.disconnect(); // ngắt observe
  mutations.forEach(m => {
    if (m.attributeName !== 'data-modified') {
      m.target.setAttribute('data-modified', 'true');
    }
  });
  observer.observe(el, { attributes: true }); // bật lại
});
```

**Thực tế sử dụng:**

```js
// 1. Autofocus dynamic content
const focusObserver = new MutationObserver((mutations) => {
  mutations.forEach(mutation => {
    mutation.addedNodes.forEach(node => {
      if (node.nodeType === Node.ELEMENT_NODE) {
        const focusable = node.querySelector('[autofocus]');
        if (focusable) focusable.focus();
      }
    });
  });
});
focusObserver.observe(document.body, { childList: true, subtree: true });

// 2. Polyfill custom attributes
const themeObserver = new MutationObserver((mutations) => {
  mutations.forEach(m => {
    if (m.attributeName === 'data-theme') {
      applyTheme(m.target.dataset.theme);
    }
  });
});
themeObserver.observe(document.documentElement, {
  attributes: true,
  attributeFilter: ['data-theme']
});
```

**Tối ưu:**

```js
// Batch xử lý thay vì xử lý từng mutation riêng
const observer = new MutationObserver((mutations) => {
  // Tất cả mutations trong một microtask được batch
  const addedNodes = mutations
    .filter(m => m.type === 'childList')
    .flatMap(m => [...m.addedNodes]);

  // Xử lý một lần, không phải N lần
  processAddedNodes(addedNodes);
});
```

---

### Tài liệu tham khảo

- [MDN: MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver)
- [MDN: MutationObserver.observe()](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver/observe)

## 70. OffscreenCanvas

**OffscreenCanvas là gì?**

OffscreenCanvas cho phép render canvas ở trong Web Worker — tách biệt hoàn toàn với main thread, không block UI.

**Vấn đề với Canvas thông thường:**

```text
Main thread:
  JS logic → Canvas 2D/WebGL rendering → Paint → Display

  Nếu render nặng → block main thread → jank, frame drops
```

**Hai cách dùng OffscreenCanvas:**

```js
// Cách 1: Transfer canvas sang worker
// Main thread:
const canvas = document.getElementById('myCanvas');
const offscreen = canvas.transferControlToOffscreen();
worker.postMessage({ canvas: offscreen }, [offscreen]);
// Sau đây main thread KHÔNG còn control canvas

// Worker:
self.onmessage = ({ data: { canvas } }) => {
  const ctx = canvas.getContext('2d');
  // Render tự do trong worker — không block main thread!
  renderLoop(ctx);
};
```

```js
// Cách 2: OffscreenCanvas độc lập (không cần DOM canvas)
// Worker:
const offscreen = new OffscreenCanvas(800, 600);
const ctx = offscreen.getContext('2d');

// Render vào offscreen
ctx.fillStyle = 'blue';
ctx.fillRect(0, 0, 800, 600);

// Convert sang ImageBitmap để gửi về main thread
const bitmap = offscreen.transferToImageBitmap();
self.postMessage({ bitmap }, [bitmap]);

// Main thread:
worker.onmessage = ({ data: { bitmap } }) => {
  const canvas = document.getElementById('display');
  const ctx = canvas.getContext('bitmaprenderer');
  ctx.transferFromImageBitmap(bitmap);
};
```

**WebGL trong Worker:**

```js
// OffscreenCanvas hỗ trợ WebGL/WebGL2
// Worker:
self.onmessage = ({ data: { canvas } }) => {
  const gl = canvas.getContext('webgl2');
  if (!gl) return;

  // Full WebGL pipeline trong worker
  const program = createShaderProgram(gl, vertexShader, fragmentShader);
  gl.useProgram(program);

  function frame() {
    gl.clear(gl.COLOR_BUFFER_BIT);
    // draw calls...
    requestAnimationFrame(frame); // có trong worker context!
  }
  frame();
};
```

**Animation loop trong Worker:**

```js
// Worker có requestAnimationFrame — sync với display refresh
// (Không có trong classic workers, chỉ có khi OffscreenCanvas present)

self.onmessage = ({ data: { canvas } }) => {
  const ctx = canvas.getContext('2d');
  let frame = 0;

  function animate() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = `hsl(${frame % 360}, 70%, 50%)`;
    ctx.fillRect(10, 10, 100, 100);
    frame++;
    requestAnimationFrame(animate);
  }
  animate();
};
```

**Use cases:**

```text
✅ Game rendering / particle systems
✅ Real-time data visualization (charts)
✅ Video/image processing (filters, effects)
✅ WebGL 3D scenes
✅ PDF rendering
✅ Map tile rendering (Mapbox, etc.)

❌ Simple UI animations → dùng CSS transforms
❌ Canvas cần đọc DOM → không thể từ worker
```

**Resize OffscreenCanvas:**

```js
// Gửi resize event sang worker
window.addEventListener('resize', () => {
  worker.postMessage({
    type: 'resize',
    width: canvas.clientWidth * devicePixelRatio,
    height: canvas.clientHeight * devicePixelRatio
  });
});

// Worker:
self.onmessage = ({ data }) => {
  if (data.type === 'resize') {
    canvas.width = data.width;
    canvas.height = data.height;
  }
};
```

---

### Tài liệu tham khảo

- [MDN: OffscreenCanvas](https://developer.mozilla.org/en-US/docs/Web/API/OffscreenCanvas)
- [Chrome Blog: OffscreenCanvas](https://developer.chrome.com/blog/offscreen-canvas)

## LEVEL 8: Concurrency & Streams

---

## 71. Task Starvation

**Task Starvation là gì?**

Task starvation xảy ra khi một loại task liên tục bị trì hoãn vì các task có độ ưu tiên cao hơn chiếm hết thời gian của event loop, khiến task thấp ưu tiên không bao giờ chạy.

**Cơ chế event loop và starvation:**

```text
Task Queue:       [taskA] [taskB] [taskC] [taskD] ...
Microtask Queue:  [micro1] [micro2] ...

Sau mỗi task → drain toàn bộ microtask queue
→ Nếu microtask liên tục tạo ra microtask mới → tasks bị starve mãi mãi
```

**Microtask starvation:**

```js
// ❌ Microtask loop vô tận — tasks khác không bao giờ chạy
function infiniteMicrotasks() {
  Promise.resolve().then(() => {
    // Tạo microtask mới trong microtask → queue không bao giờ rỗng
    infiniteMicrotasks();
  });
}

// Hệ quả:
setTimeout(() => console.log('This never runs'), 0); // starved!
infiniteMicrotasks();
```

**Long task starvation:**

```js
// ❌ Task nặng block event loop — render và user input bị starve
function heavySync() {
  const start = Date.now();
  while (Date.now() - start < 2000) {
    // 2 giây block → không render, không input response
  }
}

// ✅ Yield để cho event loop thở
async function heavyAsync(items) {
  for (let i = 0; i < items.length; i++) {
    process(items[i]);

    // Yield sau mỗi 5ms để event loop xử lý tasks khác
    if (i % 100 === 0) {
      await new Promise(resolve => setTimeout(resolve, 0));
      // hoặc: await scheduler.yield(); (Chrome 115+)
    }
  }
}
```

**scheduler.yield() — React 18 dùng cách này:**

```js
// Chrome 115+ Scheduler API
async function processWithYield(items) {
  for (const item of items) {
    process(item);

    if (shouldYield()) {
      await scheduler.yield(); // nhường control, tiếp tục sau
    }
  }
}

function shouldYield() {
  // Dựa trên deadline — tương tự IdleDeadline
  return performance.now() > frameDeadline;
}
```

**Starvation trong React Concurrent Mode:**

```text
React Scheduler ưu tiên:
  ImmediatePriority   → click, input (không bao giờ bị starve)
  UserBlockingPriority → animation
  NormalPriority       → data updates
  LowPriority          → prefetch
  IdlePriority         → analytics, logging

Task IdlePriority có thể bị starve nếu NormalPriority liên tục có việc
→ React có "expiration time" — task quá hạn được nâng priority
```

**Phát hiện starvation:**

```js
// Đo thời gian task chờ
const queueTime = performance.now();
scheduler.postTask(() => {
  const waitTime = performance.now() - queueTime;
  if (waitTime > 1000) {
    console.warn(`Task starved for ${waitTime}ms`);
  }
}, { priority: 'background' });
```

---

### Tài liệu tham khảo

- [web.dev: Optimize Long Tasks](https://web.dev/articles/optimize-long-tasks)
- [MDN: Scheduler API](https://developer.mozilla.org/en-US/docs/Web/API/Scheduler)

## 72. Priority Inversion in Async Code

**Priority Inversion là gì?**

Priority inversion xảy ra khi một task có độ ưu tiên cao bị block bởi task độ ưu tiên thấp hơn đang giữ resource mà task cao cần.

**Ví dụ kinh điển (systems):**

```text
Task HIGH   → cần mutex M → chờ task LOW
Task MEDIUM → chạy vì HIGH đang chờ
Task LOW    → giữ mutex M, bị preempt bởi MEDIUM
             → HIGH chờ LOW → LOW chờ MEDIUM → HIGH bị block bởi MEDIUM!
```

**Priority inversion trong JavaScript async:**

```js
// Task HIGH cần dữ liệu từ cache — cache đang bị lock bởi LOW task
let cacheLock = false;
const cacheData = {};

// LOW priority task đang update cache
async function updateCacheBackground() {
  cacheLock = true;
  await slowDatabaseFetch(); // mất 2 giây
  cacheData.items = await processData();
  cacheLock = false;
}

// HIGH priority — user click → cần cache ngay
async function handleUserClick() {
  // Bị block chờ cacheLock dù HIGH priority!
  while (cacheLock) {
    await sleep(10);
  }
  renderItems(cacheData.items);
}
```

**Giải pháp — Priority inheritance:**

```js
// Khi HIGH task chờ LOW task → tạm thời nâng priority của LOW task
class PriorityAwareLock {
  constructor() {
    this.holder = null;
    this.waiters = [];
  }

  async acquire(priority) {
    if (!this.holder) {
      this.holder = { priority };
      return;
    }

    // Nếu waiter có priority cao hơn holder → nâng priority holder
    if (priority > this.holder.priority) {
      this.holder.priority = priority; // priority inheritance
      // Signal scheduler để chạy holder sớm hơn
    }

    await new Promise(resolve => this.waiters.push({ resolve, priority }));
  }

  release() {
    this.holder = null;
    if (this.waiters.length > 0) {
      // Chọn waiter có priority cao nhất
      this.waiters.sort((a, b) => b.priority - a.priority);
      const next = this.waiters.shift();
      this.holder = { priority: next.priority };
      next.resolve();
    }
  }
}
```

**React Concurrent Mode và priority inversion:**

```js
// startTransition hạ priority của update
// Nếu user tiếp tục type → transition bị interrupt (không invert)

function SearchPage() {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState([]);

  function handleChange(e) {
    setQuery(e.target.value); // HIGH: immediate

    startTransition(() => {
      setResults(search(e.target.value)); // LOW: deferrable
    });
  }
  // LOW không block HIGH → không có priority inversion
}
```

**AbortController để tránh inversion:**

```js
// Thay vì block HIGH task chờ LOW task → cancel LOW task
let lowPriorityController = null;

async function highPriorityTask() {
  // Cancel tất cả low priority work
  lowPriorityController?.abort();

  // Làm HIGH priority work ngay
  await doHighPriorityWork();
}

async function lowPriorityTask() {
  lowPriorityController = new AbortController();
  const { signal } = lowPriorityController;

  for (const item of largeDataset) {
    if (signal.aborted) return; // dừng ngay khi bị cancel
    await processItem(item);
  }
}
```

---

### Tài liệu tham khảo

- [MDN: scheduler.postTask()](https://developer.mozilla.org/en-US/docs/Web/API/Scheduler/postTask)
- [React Docs: startTransition](https://react.dev/reference/react/startTransition)

## 73. Scheduler Internals

**JavaScript Scheduler hoạt động như thế nào?**

Browser có nhiều queue với priority khác nhau, không phải một hàng đợi duy nhất.

**Queue hierarchy:**

```text
1. Microtask Queue (Highest)
   Promise.then, queueMicrotask, MutationObserver callbacks

2. Animation Frame Queue
   requestAnimationFrame callbacks

3. Task Queue (Macrotask)
   setTimeout, setInterval, I/O, MessageChannel, script load

4. Idle Queue (Lowest)
   requestIdleCallback callbacks
```

**Chi tiết vòng lặp event loop:**

```text
1. Lấy một task từ Task Queue
2. Execute task
3. Drain toàn bộ Microtask Queue (bao gồm microtasks được tạo trong bước 3)
4. Nếu có pending rAF và đến lúc render:
   → Run animation frame callbacks
   → Layout + Paint + Composite
5. Nếu còn thời gian idle → run requestIdleCallback
6. Quay lại bước 1
```

**MessageChannel vs setTimeout — ưu tiên hơn:**

```js
// setTimeout(fn, 0) thực ra có delay tối thiểu ~4ms (clamping)
// MessageChannel.port.postMessage → macrotask không có delay

const { port1, port2 } = new MessageChannel();
port1.onmessage = () => {
  // Chạy như macrotask nhưng KHÔNG bị clamp 4ms
  doWork();
};
port2.postMessage(null); // schedule ngay

// React Scheduler dùng MessageChannel thay setTimeout(fn, 0)
```

**scheduler.postTask() API (Chrome 94+):**

```js
// Native Scheduler API với explicit priority
scheduler.postTask(() => {
  updateAnalytics();
}, { priority: 'background' }); // 'user-blocking' | 'user-visible' | 'background'

// Delay + signal
const controller = new TaskController({ priority: 'user-visible' });
scheduler.postTask(doWork, {
  signal: controller.signal,
  delay: 500
});

// Thay đổi priority sau khi schedule
controller.setPriority('background');

// Cancel
controller.abort();
```

**React Scheduler — mini implementation:**

```js
// React dùng heap (min-heap) để sort tasks theo expiration time
// Task gần hết hạn nhất → chạy trước

const taskQueue = []; // min-heap by expirationTime

function scheduleCallback(priorityLevel, callback) {
  const currentTime = performance.now();
  const timeout = getTimeoutByPriority(priorityLevel);
  const expirationTime = currentTime + timeout;

  const task = { callback, expirationTime, priorityLevel };
  push(taskQueue, task); // insert vào heap

  requestHostCallback(flushWork);
}

function flushWork(hasTimeRemaining, initialTime) {
  while (taskQueue.length > 0) {
    const task = peek(taskQueue); // task sắp hết hạn nhất

    if (!hasTimeRemaining && task.expirationTime > initialTime) {
      break; // hết time slice → yield, tiếp tục sau
    }

    task.callback();
    pop(taskQueue);
  }
}
```

**Time slicing — 5ms frame budget:**

```js
// React Scheduler chia work thành 5ms slices
const frameInterval = 5; // ms

function shouldYieldToHost() {
  const timeElapsed = performance.now() - startTime;
  return timeElapsed >= frameInterval; // yield sau 5ms
}
```

---

### Tài liệu tham khảo

- [MDN: Scheduler API](https://developer.mozilla.org/en-US/docs/Web/API/Scheduler)
- [React Source: Scheduler package](https://github.com/facebook/react/tree/main/packages/scheduler)

## 74. Concurrent Rendering Tearing

**Tearing là gì?**

Tearing xảy ra trong concurrent rendering khi React render một component ở giữa chừng, bị interrupt, và khi resume — external store đã thay đổi — dẫn đến UI hiển thị inconsistent state.

**Kịch bản tearing:**

```text
Render lần 1:
  ComponentA đọc store.value = 1 → render "1"
  [React bị interrupt bởi urgent update]
  store.value thay đổi thành 2  ← trong khi render đang dở
  ComponentB đọc store.value = 2 → render "2"

Kết quả: ComponentA hiển thị "1", ComponentB hiển thị "2"
         → Inconsistent! Tearing!
```

**Tại sao React 18 bị tearing với external stores?**

```js
// Redux, Zustand, Jotai dùng external store
// React không biết store thay đổi trong lúc render

// ❌ Tearing có thể xảy ra với concurrent features
const value = externalStore.getSnapshot(); // đọc tại thời điểm render
// Nhưng store có thể đổi trước khi React commit!
```

**useSyncExternalStore — giải pháp chính thức:**

```js
import { useSyncExternalStore } from 'react';

// ✅ Đảm bảo snapshot nhất quán, không tearing
function useStore(store) {
  return useSyncExternalStore(
    store.subscribe,       // listener để React biết khi store đổi
    store.getSnapshot,     // lấy current snapshot
    store.getServerSnapshot // snapshot cho SSR (optional)
  );
}

// Ví dụ với Zustand
const count = useSyncExternalStore(
  zustandStore.subscribe,
  () => zustandStore.getState().count
);
```

**Tại sao useSyncExternalStore ngăn tearing:**

```text
useSyncExternalStore đảm bảo:
1. Đọc snapshot ngay trước khi commit
2. Nếu snapshot thay đổi sau khi render → force synchronous re-render
3. Toàn bộ tree dùng cùng một snapshot trong một commit
→ Không bao giờ thấy 2 giá trị khác nhau
```

**Tearing với transitions:**

```js
// startTransition + external store → cần useSyncExternalStore
// Nếu không → có thể tearing khi concurrent renders

function Counter() {
  // ✅ Safe với concurrent mode
  const count = useSyncExternalStore(
    counterStore.subscribe,
    counterStore.getSnapshot
  );
  return <span>{count}</span>;
}
```

**State trong React (useState, useReducer) không bị tearing:**

```text
React quản lý state nội bộ → biết khi nào state đổi
→ Luôn dùng consistent snapshot trong một render pass
→ Chỉ external stores mới cần lo tearing
```

---

### Tài liệu tham khảo

- [React Docs: useSyncExternalStore](https://react.dev/reference/react/useSyncExternalStore)
- [React WG: Tearing](https://github.com/reactwg/react-18/discussions/69)

## 75. Backpressure Handling

**Backpressure là gì?**

Backpressure là cơ chế producer giảm tốc hoặc dừng lại khi consumer không xử lý kịp dữ liệu, tránh memory overflow và crash.

```text
Không có backpressure:
  Producer ──[data]──[data]──[data]──► Consumer (chậm)
                     ↑ Buffer đầy → memory overflow → crash

Có backpressure:
  Producer ──[data]──(chờ)──[data]──► Consumer
                     ↑ Signal "slow down" ← Consumer
```

**Streams API — backpressure tự động:**

```js
// ReadableStream có built-in backpressure qua queuing strategy
const readableStream = new ReadableStream(
  {
    start(controller) {
      // Producer: push data
    },
    pull(controller) {
      // pull() chỉ được gọi khi consumer cần thêm data
      // → tự động backpressure!
      const chunk = getNextChunk();
      if (chunk) {
        controller.enqueue(chunk);
      } else {
        controller.close();
      }
    }
  },
  new CountQueuingStrategy({ highWaterMark: 5 }) // buffer tối đa 5 chunks
);
```

**WritableStream — desiredSize:**

```js
const writableStream = new WritableStream(
  {
    write(chunk, controller) {
      return processChunk(chunk); // return Promise → backpressure tự động
      // Nếu Promise chưa resolve → writer sẽ chờ trước khi write tiếp
    }
  },
  new ByteLengthQueuingStrategy({ highWaterMark: 1024 }) // 1KB buffer
);

// Writer kiểm tra backpressure thủ công
const writer = writableStream.getWriter();

async function writeWithBackpressure(data) {
  for (const chunk of data) {
    // Chờ nếu stream báo "đầy"
    if (writer.desiredSize <= 0) {
      await writer.ready; // chờ stream ready nhận thêm
    }
    writer.write(chunk);
  }
}
```

**fetch + ReadableStream pipeline:**

```js
// Stream response từ server → xử lý từng chunk → không load toàn bộ vào RAM
const response = await fetch('/large-file');
const reader = response.body.getReader();
const decoder = new TextDecoder();

async function processStream() {
  while (true) {
    const { done, value } = await reader.read();
    if (done) break;

    const text = decoder.decode(value, { stream: true });
    await processChunk(text); // await → backpressure ngược lên fetch
  }
}
```

**Transform Stream — pipeline với backpressure:**

```js
// Producer → Transform → Consumer — backpressure tự động lan truyền
const transformStream = new TransformStream({
  transform(chunk, controller) {
    const processed = heavyProcess(chunk);
    controller.enqueue(processed);
  }
});

// Pipe: nguồn → transform → đích
await readableSource
  .pipeThrough(transformStream)
  .pipeTo(writableSink);
// pipeThrough/pipeTo tự xử lý backpressure
```

**Manual backpressure với async generators:**

```js
async function* producer() {
  for (let i = 0; i < 1000000; i++) {
    yield generateItem(i);
    // yield tự động pause nếu consumer chưa next()
  }
}

async function consumer() {
  for await (const item of producer()) {
    await slowProcess(item); // slowProcess chậm → producer tự pause
  }
}
```

---

### Tài liệu tham khảo

- [MDN: Streams API Concepts](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API/Concepts)
- [WHATWG: Streams Living Standard](https://streams.spec.whatwg.org/)

## 76. Streaming SSR Pipelines

**Streaming SSR Pipeline là gì?**

Một pipeline kết nối server rendering → HTTP streaming → browser progressive hydration, cho phép TTFB thấp và FCP sớm ngay cả với trang phức tạp.

**Kiến trúc pipeline:**

```text
[React Server]
  renderToPipeableStream()
       ↓
  [Node.js Writable Stream]
       ↓ pipe
  [Compression Transform] (gzip/brotli)
       ↓ pipe
  [HTTP Response] (chunked transfer encoding)
       ↓ network
  [Browser Parser]
       ↓ parses chunks incrementally
  [React Client] hydrates Suspense boundaries
```

**Server setup hoàn chỉnh:**

```js
import { renderToPipeableStream } from 'react-dom/server';
import { createGzip } from 'zlib';

app.get('*', (req, res) => {
  const gzip = createGzip();

  res.setHeader('Content-Type', 'text/html');
  res.setHeader('Content-Encoding', 'gzip');
  res.setHeader('Transfer-Encoding', 'chunked');

  let statusCode = 200;
  let error = null;

  const { pipe, abort } = renderToPipeableStream(
    <App url={req.url} />,
    {
      bootstrapScripts: ['/static/js/client.js'],

      onShellReady() {
        // Shell = layout, header, navigation — hiển thị ngay
        res.statusCode = statusCode;
        pipe(gzip);       // pipe React output → gzip → response
        gzip.pipe(res);
      },

      onShellError(err) {
        // Shell thất bại → fallback HTML
        res.statusCode = 500;
        res.send(`<html><body><h1>Error</h1></body></html>`);
      },

      onError(err) {
        // Lỗi bên trong Suspense boundary → show error boundary
        statusCode = 500;
        error = err;
        console.error(err);
      }
    }
  );

  // Timeout phòng trường hợp stream hang
  const timeout = setTimeout(() => abort(), 10000);

  res.on('finish', () => clearTimeout(timeout));
});
```

**Suspense boundary trong pipeline:**

```jsx
// Mỗi Suspense boundary = một "hole" trong stream
// Server gửi placeholder → sau đó inject content khi ready

export default function ProductPage({ id }) {
  return (
    <html>
      <body>
        {/* Phần này stream ngay (không async) */}
        <Header />
        <ProductInfo id={id} />

        {/* Placeholder stream trước, sau đó server inject content */}
        <Suspense fallback={<ReviewsSkeleton />}>
          <Reviews id={id} />   {/* async fetch */}
        </Suspense>

        <Suspense fallback={<RecommendationsSkeleton />}>
          <Recommendations id={id} /> {/* async fetch */}
        </Suspense>
      </body>
    </html>
  );
}
```

**Cơ chế inject HTML sau (out-of-order streaming):**

```html
<!-- Server gửi placeholder trước -->
<!--$?--><template id="B:0"></template><div>Loading reviews...</div><!--/$-->

<!-- Sau đó inject script thay thế placeholder bằng content thực -->
<div hidden id="S:0">
  <ul><li>Review 1</li><li>Review 2</li></ul>
</div>
<script>
  $RC("B:0", "S:0"); // replaceContent: thay B:0 bằng S:0
</script>
```

**Edge streaming với Next.js:**

```js
// app/api/stream/route.ts
export const runtime = 'edge';

export async function GET() {
  const stream = new ReadableStream({
    async start(controller) {
      controller.enqueue(new TextEncoder().encode('<html><body>'));

      const data = await fetchData();
      controller.enqueue(new TextEncoder().encode(renderData(data)));

      controller.enqueue(new TextEncoder().encode('</body></html>'));
      controller.close();
    }
  });

  return new Response(stream, {
    headers: { 'Content-Type': 'text/html' }
  });
}
```

---

### Tài liệu tham khảo

- [React Docs: renderToPipeableStream](https://react.dev/reference/react-dom/server/renderToPipeableStream)
- [Next.js: Streaming](https://nextjs.org/docs/app/building-your-application/routing/loading-ui-and-streaming)

## 77. WebRTC Basics

**WebRTC là gì?**

WebRTC (Web Real-Time Communication) là API cho phép peer-to-peer audio, video, và data communication trực tiếp giữa browsers — không cần server trung gian cho media.

**Kiến trúc tổng quan:**

```text
Browser A ←── Signaling Server (WebSocket) ──→ Browser B
    ↑                                               ↑
    └─────────── P2P Connection (ICE/DTLS) ─────────┘
                    (audio/video/data trực tiếp)
```

**Signaling — trao đổi thông tin kết nối:**

```js
// Bước 1: Tạo peer connection
const pc = new RTCPeerConnection({
  iceServers: [
    { urls: 'stun:stun.l.google.com:19302' },      // STUN server
    { urls: 'turn:turn.example.com', username: 'u', credential: 'p' } // TURN
  ]
});

// Bước 2: Thêm media stream
const stream = await navigator.mediaDevices.getUserMedia({ video: true, audio: true });
stream.getTracks().forEach(track => pc.addTrack(track, stream));

// Bước 3: Tạo offer
const offer = await pc.createOffer();
await pc.setLocalDescription(offer);

// Gửi offer qua signaling server (WebSocket)
signalingSocket.send(JSON.stringify({ type: 'offer', sdp: offer }));

// Bước 4: ICE candidates
pc.onicecandidate = (event) => {
  if (event.candidate) {
    signalingSocket.send(JSON.stringify({
      type: 'ice-candidate',
      candidate: event.candidate
    }));
  }
};
```

**Answerer (phía nhận):**

```js
// Nhận offer → tạo answer
signalingSocket.onmessage = async ({ data }) => {
  const message = JSON.parse(data);

  if (message.type === 'offer') {
    await pc.setRemoteDescription(message.sdp);
    const answer = await pc.createAnswer();
    await pc.setLocalDescription(answer);
    signalingSocket.send(JSON.stringify({ type: 'answer', sdp: answer }));
  }

  if (message.type === 'answer') {
    await pc.setRemoteDescription(message.sdp);
  }

  if (message.type === 'ice-candidate') {
    await pc.addIceCandidate(message.candidate);
  }
};

// Nhận remote stream
pc.ontrack = (event) => {
  const remoteVideo = document.getElementById('remote-video');
  remoteVideo.srcObject = event.streams[0];
};
```

**RTCDataChannel — P2P data:**

```js
// Tạo data channel (offerer side)
const dataChannel = pc.createDataChannel('chat', {
  ordered: true,      // đảm bảo thứ tự (như TCP)
  // ordered: false   // không đảm bảo thứ tự (như UDP) — nhanh hơn
});

dataChannel.onopen = () => dataChannel.send('Hello!');
dataChannel.onmessage = (e) => console.log('Received:', e.data);

// Answerer side
pc.ondatachannel = (event) => {
  const channel = event.channel;
  channel.onmessage = (e) => console.log('Received:', e.data);
};
```

**STUN vs TURN:**

| | STUN | TURN |
| --- | --- | --- |
| Mục đích | Tìm public IP/port | Relay traffic qua server |
| Khi dùng | Direct connection khả thi | NAT/firewall chặn P2P |
| Chi phí | Free, nhẹ | Tốn bandwidth server |
| Độ trễ | Thấp (P2P) | Cao hơn (qua server) |

---

### Tài liệu tham khảo

- [MDN: WebRTC API](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API)
- [WebRTC.org: Getting Started](https://webrtc.org/getting-started/overview)

## 78. CRDT Basics for Collaboration

**CRDT là gì?**

CRDT (Conflict-free Replicated Data Type) là cấu trúc dữ liệu được thiết kế để merge tự động mà không cần coordination — mọi operation đều commutative, associative, idempotent.

**Hai loại CRDT:**

```text
State-based CRDT (CvRDT):
  → Sync toàn bộ state giữa các node
  → Merge function: state1 ⊔ state2 → luôn cho kết quả giống nhau
  → Tốn bandwidth nếu state lớn

Operation-based CRDT (CmRDT):
  → Chỉ gửi operations (delta)
  → Operations phải commutative: op1 ∘ op2 = op2 ∘ op1
  → Cần đảm bảo mỗi op được deliver đúng một lần
```

**G-Counter (Grow-only):**

```js
// Chỉ tăng, không bao giờ giảm → dễ merge
class GCounter {
  constructor(nodeId, peers = []) {
    this.id = nodeId;
    this.vector = {}; // { nodeId: count }
  }

  increment(amount = 1) {
    this.vector[this.id] = (this.vector[this.id] || 0) + amount;
  }

  value() {
    return Object.values(this.vector).reduce((a, b) => a + b, 0);
  }

  // Merge: max của từng node
  merge(remote) {
    for (const [node, count] of Object.entries(remote.vector)) {
      this.vector[node] = Math.max(this.vector[node] || 0, count);
    }
  }
}

// Dù merge theo thứ tự nào → kết quả giống nhau
const a = new GCounter('A'); a.increment(3);
const b = new GCounter('B'); b.increment(2);
a.merge(b); // vector: { A: 3, B: 2 }, value: 5
b.merge(a); // vector: { A: 3, B: 2 }, value: 5 ✅ same
```

**OR-Set (Observed-Remove Set):**

```js
// Set có thể add và remove — dùng unique tag để phân biệt
class ORSet {
  constructor() {
    this.entries = new Map(); // key → Set of unique tags
    this.tombstones = new Map(); // removed tags
  }

  add(key) {
    const tag = crypto.randomUUID(); // unique tag
    if (!this.entries.has(key)) this.entries.set(key, new Set());
    this.entries.get(key).add(tag);
  }

  remove(key) {
    const tags = this.entries.get(key);
    if (tags) {
      for (const tag of tags) {
        if (!this.tombstones.has(key)) this.tombstones.set(key, new Set());
        this.tombstones.get(key).add(tag);
      }
    }
  }

  has(key) {
    const tags = this.entries.get(key) || new Set();
    const removed = this.tombstones.get(key) || new Set();
    return [...tags].some(t => !removed.has(t));
  }

  merge(remote) {
    for (const [key, tags] of remote.entries) {
      if (!this.entries.has(key)) this.entries.set(key, new Set());
      for (const tag of tags) this.entries.get(key).add(tag);
    }
    for (const [key, tags] of remote.tombstones) {
      if (!this.tombstones.has(key)) this.tombstones.set(key, new Set());
      for (const tag of tags) this.tombstones.get(key).add(tag);
    }
  }
}
```

**CRDT cho collaborative text editing (RGA/Logoot):**

```js
// Mỗi character có unique ID (site + clock)
// Insert/delete dựa trên ID → không xung đột

class RGADocument {
  constructor(siteId) {
    this.siteId = siteId;
    this.clock = 0;
    this.nodes = []; // [{ id, char, deleted }]
  }

  insert(index, char) {
    const id = `${this.siteId}-${++this.clock}`;
    const node = { id, char, deleted: false };
    this.nodes.splice(index, 0, node);
    return { type: 'insert', id, char, after: this.nodes[index - 1]?.id };
  }

  applyRemoteInsert({ id, char, after }) {
    const afterIndex = after
      ? this.nodes.findIndex(n => n.id === after)
      : -1;
    // Tìm vị trí đúng (tie-breaking bằng id)
    let insertIndex = afterIndex + 1;
    while (
      insertIndex < this.nodes.length &&
      this.nodes[insertIndex].id > id
    ) insertIndex++;
    this.nodes.splice(insertIndex, 0, { id, char, deleted: false });
  }

  getText() {
    return this.nodes.filter(n => !n.deleted).map(n => n.char).join('');
  }
}
```

**Thư viện CRDT phổ biến:**

```text
Yjs     → CRDT cho text, array, map — dùng trong TipTap, Monaco
Automerge → JSON CRDT, immutable model
Diamond Types → CRDT hiệu năng cao (Rust → WASM)
```

---

### Tài liệu tham khảo

- [crdt.tech](https://crdt.tech/)
- [Yjs Documentation](https://docs.yjs.dev/)

## 79. Shared Memory Models

**Shared Memory là gì?**

Shared memory cho phép nhiều threads đọc/ghi vào cùng vùng nhớ mà không cần copy data. Trong browser, đây là `SharedArrayBuffer` kết hợp với Web Workers.

**Memory models và ordering:**

```text
Sequential Consistency:
  Mọi thread thấy cùng thứ tự operations → đơn giản, an toàn
  → Chậm vì cần synchronization barriers

Relaxed Memory Model:
  CPU/compiler có thể reorder operations để tối ưu
  → Nhanh hơn nhưng phức tạp hơn
  → JavaScript dùng mô hình này (ECMAScript memory model)
```

**Data races và undefined behavior:**

```js
const sab = new SharedArrayBuffer(4);
const arr = new Int32Array(sab);

// Worker 1:
arr[0] = arr[0] + 1; // Read-Modify-Write không atomic!

// Worker 2 (đồng thời):
arr[0] = arr[0] + 1;

// Kết quả: có thể là 1 thay vì 2 (data race!)
```

**Atomics — đảm bảo ordering:**

```js
// Atomic operations:
Atomics.load(arr, 0);               // atomic read
Atomics.store(arr, 0, value);        // atomic write
Atomics.add(arr, 0, 1);             // atomic increment
Atomics.sub(arr, 0, 1);             // atomic decrement
Atomics.and(arr, 0, mask);          // atomic bitwise AND
Atomics.or(arr, 0, mask);           // atomic bitwise OR
Atomics.xor(arr, 0, mask);          // atomic XOR
Atomics.exchange(arr, 0, newVal);   // swap, trả về giá trị cũ
Atomics.compareExchange(arr, 0, expected, replacement); // CAS

// Wait/Notify (blocking — chỉ trong Worker, không dùng trong main thread)
Atomics.wait(arr, 0, expectedValue); // block đến khi arr[0] !== expected
Atomics.notify(arr, 0, count);        // wake up 'count' workers đang wait
```

**Mutex dùng SharedArrayBuffer:**

```js
const MUTEX_IDX = 0;
const UNLOCKED = 0;
const LOCKED = 1;

class Mutex {
  constructor(sab) {
    this.arr = new Int32Array(sab);
  }

  lock() {
    while (true) {
      // CAS: nếu UNLOCKED → set LOCKED, trả về UNLOCKED → thành công
      const old = Atomics.compareExchange(this.arr, MUTEX_IDX, UNLOCKED, LOCKED);
      if (old === UNLOCKED) return; // got lock

      // Đang locked → wait
      Atomics.wait(this.arr, MUTEX_IDX, LOCKED);
    }
  }

  unlock() {
    Atomics.store(this.arr, MUTEX_IDX, UNLOCKED);
    Atomics.notify(this.arr, MUTEX_IDX, 1); // wake 1 waiter
  }
}
```

**Message passing vs Shared Memory:**

| | Message Passing (postMessage) | Shared Memory (SAB) |
| --- | --- | --- |
| Cách truyền | Copy (structured clone) | Zero-copy |
| Đồng bộ | Không cần | Cần Atomics |
| Độ an toàn | High | Low (race conditions) |
| Phù hợp | Tasks nhỏ, simple data | Heavy compute, large buffers |
| Yêu cầu | Không | Cross-Origin Isolation |

**Sequentially consistent fence:**

```js
// Atomics.add với return value → đảm bảo happens-before
Atomics.add(flag, 0, 0); // No-op nhưng tạo memory fence
// Đảm bảo mọi write trước lệnh này visible với thread khác sau fence
```

---

### Tài liệu tham khảo

- [MDN: SharedArrayBuffer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer)
- [MDN: Atomics](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics)

## 80. Deterministic UI Under Async

**Bài toán:**

Trong môi trường async, UI có thể hiển thị khác nhau tùy thứ tự response về — không deterministic. Điều này gây bugs khó reproduce và test.

**Race condition cơ bản:**

```js
// ❌ Non-deterministic — kết quả phụ thuộc network speed
async function loadUser(userId) {
  const user = await fetch(`/api/users/${userId}`).then(r => r.json());
  setUser(user); // Nếu userId đã thay đổi → stale update!
}

// User click user1 → loadUser(1)
// User click user2 → loadUser(2)
// Response user2 về trước → setUser(user2)
// Response user1 về sau → setUser(user1) ← WRONG!
```

**Giải pháp 1 — AbortController:**

```js
let currentController = null;

async function loadUser(userId) {
  // Cancel request trước
  currentController?.abort();
  currentController = new AbortController();

  try {
    const user = await fetch(`/api/users/${userId}`, {
      signal: currentController.signal
    }).then(r => r.json());
    setUser(user);
  } catch (e) {
    if (e.name === 'AbortError') return; // ignore cancelled request
    throw e;
  }
}
```

**Giải pháp 2 — Request ID tracking:**

```js
let latestRequestId = 0;

async function loadUser(userId) {
  const requestId = ++latestRequestId;
  const user = await fetchUser(userId);

  // Chỉ cập nhật nếu đây vẫn là request mới nhất
  if (requestId === latestRequestId) {
    setUser(user);
  }
}
```

**Giải pháp 3 — State machine:**

```js
// Dùng finite state machine → không thể vào trạng thái không hợp lệ
import { createMachine, assign } from 'xstate';

const userMachine = createMachine({
  initial: 'idle',
  context: { user: null, error: null, loadingUserId: null },
  states: {
    idle: {
      on: { FETCH: { target: 'loading', actions: assign({ loadingUserId: (_, e) => e.userId }) } }
    },
    loading: {
      invoke: {
        src: (ctx) => fetchUser(ctx.loadingUserId),
        onDone: { target: 'success', actions: assign({ user: (_, e) => e.data }) },
        onError: { target: 'error', actions: assign({ error: (_, e) => e.data }) }
      },
      // Nếu FETCH lại khi đang loading → cancel cái cũ, start cái mới
      on: { FETCH: { target: 'loading', actions: assign({ loadingUserId: (_, e) => e.userId }) } }
    },
    success: {
      on: { FETCH: 'loading' }
    },
    error: {
      on: { FETCH: 'loading' }
    }
  }
});
```

**React Query — deterministic by design:**

```js
// React Query giải quyết race condition tự động
const { data: user } = useQuery({
  queryKey: ['user', userId],
  queryFn: () => fetchUser(userId),
  // Khi userId thay đổi → query cũ bị cancel
  // Chỉ dùng result của query hiện tại
});
```

**Deterministic rendering với keys:**

```jsx
// Key thay đổi → React unmount và remount component
// → Reset tất cả state, cancel tất cả effects

function App({ userId }) {
  return (
    // key={userId} đảm bảo fresh state khi user thay đổi
    <UserProfile key={userId} userId={userId} />
  );
}
```

**Testing async determinism:**

```js
// Fake timers + mock fetch để test deterministic behavior
test('shows latest user when switching quickly', async () => {
  let resolvers = [];
  jest.spyOn(global, 'fetch').mockImplementation(() =>
    new Promise(resolve => resolvers.push(resolve))
  );

  const { rerender } = render(<UserCard userId={1} />);
  rerender(<UserCard userId={2} />);

  // Resolve theo thứ tự ngược lại (user1 về sau)
  resolvers[1]({ json: () => ({ name: 'User 2' }) }); // user2 về trước
  resolvers[0]({ json: () => ({ name: 'User 1' }) }); // user1 về sau

  await waitFor(() => {
    // Phải hiển thị user2, không phải user1
    expect(screen.getByText('User 2')).toBeInTheDocument();
    expect(screen.queryByText('User 1')).not.toBeInTheDocument();
  });
});
```

---

### Tài liệu tham khảo

- [React Docs: Synchronizing with Effects](https://react.dev/learn/synchronizing-with-effects)
- [TanStack Query: Query Cancellation](https://tanstack.com/query/latest/docs/framework/react/guides/query-cancellation)

## LEVEL 9: Performance Metrics Thực Chiến

---

## 81. First Input Delay (FID)

**FID là gì?**

First Input Delay đo thời gian từ lúc user tương tác lần đầu tiên (click, tap, key press) đến lúc browser thực sự bắt đầu xử lý event handler đó.

```text
User click                      Browser xử lý event
     │                                    │
     ▼                                    ▼
  [t=0ms] ──── [long task 200ms] ──── [t=200ms]
                      ↑
               FID = 200ms (thời gian chờ)
```

**FID đo gì và không đo gì:**

```text
FID ĐO:        Thời gian chờ để event được xử lý (input delay)
FID KHÔNG ĐO:  Thời gian chạy event handler
               Thời gian cập nhật UI sau event

FID chỉ đo LẦN TƯƠNG TÁC ĐẦU TIÊN
→ Không đo các tương tác tiếp theo
→ Thay thế bởi INP từ 2024
```

**Ngưỡng:**

| Giá trị | Đánh giá |
| --- | --- |
| ≤ 100ms | Good |
| 100–300ms | Needs Improvement |
| > 300ms | Poor |

**Đo FID bằng PerformanceObserver:**

```js
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    const fid = entry.processingStart - entry.startTime;
    console.log('FID:', fid, 'ms');
    console.log('Event type:', entry.name); // 'click', 'keydown', ...
    console.log('Target:', entry.target);
  }
}).observe({ type: 'first-input', buffered: true });
```

**Nguyên nhân FID cao:**

```js
// 1. Heavy JavaScript execution khi page load
// Long tasks block main thread → không xử lý input được

// 2. Third-party scripts (analytics, ads)
// → Load sync, chạy nặng khi startup

// 3. Too much JavaScript
// → Parse + compile + execute = block main thread
```

**Cải thiện FID:**

```js
// 1. Break up long tasks
// ❌ Long task
function heavyInit() {
  doTask1(); // 100ms
  doTask2(); // 100ms
  doTask3(); // 100ms
}

// ✅ Yield giữa các tasks
async function heavyInit() {
  doTask1();
  await scheduler.yield();  // Chrome 115+ // hoặc: await new Promise(r => setTimeout(r, 0));
  doTask2();
  await scheduler.yield();
  doTask3();
}

// 2. Defer non-critical JS
<script defer src="analytics.js"></script>
<script type="module" src="app.js"></script>  // modules defer by default

// 3. Remove unused JavaScript
// Tree shaking, code splitting, lazy loading
```

---

### Tài liệu tham khảo

- [web.dev: FID](https://web.dev/articles/fid)
- [web.dev: Core Web Vitals](https://web.dev/articles/vitals)

## 82. Interaction to Next Paint (INP)

**INP là gì?**

INP đo độ trễ của TẤT CẢ interactions trong suốt page lifetime, lấy giá trị percentile 75 (hoặc worst nếu ít interactions). Thay thế FID từ tháng 3/2024.

```text
Interaction = click/tap/keypress
INP = thời gian từ input → next paint

Input event
     │
     ├── Input delay (event không chạy được vì main thread bận)
     │         ↓
     ├── Processing time (event handler chạy)
     │         ↓
     └── Presentation delay (browser render frame)
              │
           Next Paint
```

**INP vs FID:**

| | FID | INP |
| --- | --- | --- |
| Đo gì | Chỉ interaction đầu tiên | Tất cả interactions |
| Phạm vi | Input delay only | Input delay + processing + presentation |
| Khi nào | Load time | Suốt page lifetime |
| Core Web Vital | Bị loại bỏ 3/2024 | Thay thế FID từ 3/2024 |

**Ngưỡng INP:**

| Giá trị | Đánh giá |
| --- | --- |
| ≤ 200ms | Good |
| 200–500ms | Needs Improvement |
| > 500ms | Poor |

**Đo INP:**

```js
// web-vitals library (khuyến nghị)
import { onINP } from 'web-vitals';

onINP(({ value, rating, entries }) => {
  console.log('INP:', value, 'ms');    // giá trị INP (p75)
  console.log('Rating:', rating);      // 'good' | 'needs-improvement' | 'poor'

  // entries chứa worst interactions
  entries.forEach(entry => {
    console.log('Interaction:', entry.name);
    console.log('Input delay:', entry.processingStart - entry.startTime);
    console.log('Processing:', entry.processingEnd - entry.processingStart);
    console.log('Presentation:', entry.duration - entry.processingEnd + entry.startTime);
  });
});
```

**Phân tích INP breakdown:**

```js
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    if (entry.interactionId) { // chỉ lấy interaction events
      const inputDelay = entry.processingStart - entry.startTime;
      const processingTime = entry.processingEnd - entry.processingStart;
      const presentationDelay = entry.startTime + entry.duration - entry.processingEnd;

      if (entry.duration > 200) {
        console.group(`Slow interaction: ${entry.name} (${entry.duration}ms)`);
        console.log('Input delay:', inputDelay.toFixed(1));
        console.log('Processing:', processingTime.toFixed(1));
        console.log('Presentation:', presentationDelay.toFixed(1));
        console.groupEnd();
      }
    }
  }
}).observe({ type: 'event', durationThreshold: 16, buffered: true });
```

**Cải thiện INP:**

```js
// 1. Giảm event handler work
// ❌ Làm tất cả trong handler
button.addEventListener('click', () => {
  updateDatabase();      // 50ms
  reRenderEntireList();  // 100ms
  sendAnalytics();       // 20ms
});

// ✅ Ưu tiên visual feedback trước
button.addEventListener('click', () => {
  // Ngay lập tức: visual feedback
  button.classList.add('loading');

  // Defer heavy work
  startTransition(() => {
    reRenderEntireList();  // deferred, không block paint
  });

  // Non-blocking
  requestIdleCallback(() => sendAnalytics());
  updateDatabase(); // async, không block
});

// 2. Avoid layout thrashing trong event handler
// ❌
element.addEventListener('click', () => {
  const height = element.offsetHeight;  // force layout
  element.style.width = height + 'px'; // invalidate layout
  const width = element.offsetWidth;   // force layout lại
});

// ✅ Batch reads trước writes
element.addEventListener('click', () => {
  const height = element.offsetHeight;  // read
  const width = element.offsetWidth;    // read
  element.style.width = height + 'px'; // write
});
```

---

### Tài liệu tham khảo

- [web.dev: INP](https://web.dev/articles/inp)
- [web.dev: Optimize INP](https://web.dev/articles/optimize-inp)

## 83. Cumulative Layout Shift (CLS)

**CLS là gì?**

CLS đo tổng lượng layout shift bất ngờ trong suốt page lifetime. Layout shift xảy ra khi element visible thay đổi vị trí mà người dùng không trigger.

**Công thức:**

```text
Layout Shift Score = Impact Fraction × Distance Fraction

Impact Fraction = phần viewport bị ảnh hưởng bởi shift
Distance Fraction = khoảng cách shift / chiều cao viewport

CLS = tổng Layout Shift Scores (trong session windows 5s, gap 1s)
```

**Ví dụ tính:**

```text
Viewport: 800×600
Element dịch chuyển: chiếm 50% viewport, dịch 10% xuống dưới

Impact fraction  = 0.5  (50% viewport bị ảnh hưởng)
Distance fraction = 0.1  (dịch 10% viewport height)
Shift score      = 0.5 × 0.1 = 0.05
```

**Ngưỡng CLS:**

| Giá trị | Đánh giá |
| --- | --- |
| ≤ 0.1 | Good |
| 0.1–0.25 | Needs Improvement |
| > 0.25 | Poor |

**Đo CLS:**

```js
import { onCLS } from 'web-vitals';

onCLS(({ value, entries }) => {
  console.log('CLS:', value);

  entries.forEach(entry => {
    if (!entry.hadRecentInput) { // không tính shift do user action
      console.log('Shift:', entry.value);
      console.log('Sources:', entry.sources); // elements bị shift
      entry.sources.forEach(source => {
        console.log('Element:', source.node);
        console.log('Previous rect:', source.previousRect);
        console.log('Current rect:', source.currentRect);
      });
    }
  });
});
```

**Nguyên nhân CLS phổ biến và cách fix:**

```html
<!-- 1. Ảnh không có kích thước → shift khi load xong -->
<!-- ❌ -->
<img src="hero.jpg" alt="Hero">

<!-- ✅ Đặt width/height hoặc aspect-ratio -->
<img src="hero.jpg" alt="Hero" width="800" height="400">

<!-- Hoặc CSS aspect-ratio -->
<style>
  img { aspect-ratio: 2/1; width: 100%; }
</style>
```

```js
// 2. Ads, embeds không có reserved space
// ❌ Inject ad → push content xuống
document.body.insertBefore(adElement, content);

// ✅ Reserve space trước
// <div style="min-height: 250px"><AdComponent /></div>
```

```css
/* 3. Font swap → FOUT → layout shift */
/* ❌ */
@font-face {
  font-family: 'MyFont';
  font-display: swap; /* text thay đổi khi font load */
}

/* ✅ Dùng size-adjust để match fallback font */
@font-face {
  font-family: 'MyFont';
  font-display: optional; /* không swap nếu font chưa load */
}

/* Hoặc font-display: swap + size-adjust fallback */
@font-face {
  font-family: 'MyFont-Fallback';
  src: local('Arial');
  size-adjust: 105%;
  ascent-override: 90%;
}
```

```js
// 4. Dynamic content injection (toast, banner)
// ❌ Inject vào đầu page → push content xuống
showBanner(); // push everything down

// ✅ Inject vào cuối, hoặc dùng fixed positioning
// position: fixed / sticky → không gây shift
```

---

### Tài liệu tham khảo

- [web.dev: CLS](https://web.dev/articles/cls)
- [web.dev: Optimize CLS](https://web.dev/articles/optimize-cls)

## 84. Largest Contentful Paint (LCP)

**LCP là gì?**

LCP đo thời gian render của largest content element trong viewport (image, video poster, text block) — thể hiện khi nội dung chính của trang sẵn sàng.

**Elements được xem xét cho LCP:**

```text
- <img> elements
- <image> trong SVG
- <video> với poster attribute
- Elements với background-image (CSS)
- Block-level text elements (p, h1, div chứa nhiều text)
```

**Ngưỡng LCP:**

| Giá trị | Đánh giá |
| --- | --- |
| ≤ 2.5s | Good |
| 2.5–4s | Needs Improvement |
| > 4s | Poor |

**Đo LCP:**

```js
import { onLCP } from 'web-vitals';

onLCP(({ value, entries }) => {
  const entry = entries[entries.length - 1]; // LCP element cuối cùng
  console.log('LCP:', value, 'ms');
  console.log('LCP element:', entry.element);
  console.log('LCP URL:', entry.url);   // nếu là image
  console.log('Load time:', entry.loadTime);
  console.log('Render time:', entry.renderTime);
  console.log('Size:', entry.size);
});

// Raw PerformanceObserver
new PerformanceObserver((list) => {
  const entries = list.getEntries();
  const last = entries[entries.length - 1];
  console.log('LCP candidate:', last.element, last.startTime);
}).observe({ type: 'largest-contentful-paint', buffered: true });
```

**LCP breakdown — 4 giai đoạn:**

```text
LCP = TTFB + Resource Load Delay + Resource Load Time + Element Render Delay

TTFB:                 Server response time
Resource Load Delay:  Thời gian từ TTFB đến bắt đầu load LCP resource
Resource Load Time:   Thời gian download LCP resource
Element Render Delay: Từ download xong đến paint
```

**Tối ưu LCP:**

```html
<!-- 1. Preload LCP image -->
<link rel="preload" as="image" href="/hero.jpg" fetchpriority="high">

<!-- 2. fetchpriority="high" trên LCP image -->
<img src="/hero.jpg" fetchpriority="high" alt="Hero">

<!-- 3. Không lazy-load LCP image -->
<!-- ❌ -->
<img src="/hero.jpg" loading="lazy">
<!-- ✅ -->
<img src="/hero.jpg" loading="eager">
```

```js
// 4. Optimize TTFB — server-side
// CDN, caching, edge computing

// 5. Tránh render-blocking resources
// <script defer> hoặc <script type="module">
// CSS critical inline, rest defer

// 6. Responsive images
<img
  src="/hero-800.jpg"
  srcset="/hero-400.jpg 400w, /hero-800.jpg 800w, /hero-1200.jpg 1200w"
  sizes="(max-width: 600px) 400px, (max-width: 900px) 800px, 1200px"
  fetchpriority="high"
>
```

---

### Tài liệu tham khảo

- [web.dev: LCP](https://web.dev/articles/lcp)
- [web.dev: Optimize LCP](https://web.dev/articles/optimize-lcp)

## 85. PerformanceObserver API

**PerformanceObserver là gì?**

PerformanceObserver là API để observe các performance entries được browser record — không cần polling, không tốn CPU.

**Kiến trúc:**

```text
Browser tự động record entries:
  navigation, resource, paint, longtask,
  largest-contentful-paint, layout-shift,
  first-input, event, mark, measure...

PerformanceObserver.observe() → nhận entries async khi available
```

**Các entry types quan trọng:**

```js
// Xem tất cả supported entry types
console.log(PerformanceObserver.supportedEntryTypes);
// ['element', 'event', 'first-input', 'largest-contentful-paint',
//  'layout-shift', 'longtask', 'mark', 'measure', 'navigation',
//  'paint', 'resource', 'visibility-state']
```

**Navigation timing:**

```js
new PerformanceObserver((list) => {
  const nav = list.getEntries()[0];
  console.log('DNS lookup:', nav.domainLookupEnd - nav.domainLookupStart);
  console.log('TCP connect:', nav.connectEnd - nav.connectStart);
  console.log('TTFB:', nav.responseStart - nav.requestStart);
  console.log('DOM parse:', nav.domContentLoadedEventEnd - nav.responseEnd);
  console.log('Total load:', nav.loadEventEnd - nav.startTime);
}).observe({ type: 'navigation', buffered: true });
```

**Resource timing:**

```js
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    if (entry.initiatorType === 'img') {
      console.log(`Image: ${entry.name}`);
      console.log(`  Size: ${entry.transferSize} bytes`);
      console.log(`  Load time: ${entry.duration.toFixed(1)}ms`);
      console.log(`  Cache hit: ${entry.transferSize === 0}`);
    }
  }
}).observe({ type: 'resource', buffered: true });
```

**Custom marks và measures:**

```js
// Đánh dấu điểm bắt đầu
performance.mark('my-feature-start');

// Làm gì đó
await doExpensiveWork();

// Đánh dấu điểm kết thúc
performance.mark('my-feature-end');

// Đo khoảng giữa
performance.measure('my-feature', 'my-feature-start', 'my-feature-end');

// Observe measures
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    console.log(`${entry.name}: ${entry.duration.toFixed(2)}ms`);
  }
}).observe({ type: 'measure', buffered: true });
```

**buffered: true — nhận entries trước khi observe:**

```js
// Không có buffered: true → miss entries trước khi observer tạo
new PerformanceObserver(callback).observe({
  type: 'largest-contentful-paint',
  buffered: true  // ✅ nhận cả entries đã xảy ra trước
});
```

**Disconnect và cleanup:**

```js
const observer = new PerformanceObserver(callback);
observer.observe({ type: 'longtask' });

// Lấy entries đang pending và clear
const pending = observer.takeRecords();

// Dừng observe
observer.disconnect();
```

---

### Tài liệu tham khảo

- [MDN: PerformanceObserver](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceObserver)
- [web.dev: Custom Metrics](https://web.dev/articles/custom-metrics)

## 86. Long Tasks API

**Long Task là gì?**

Long Task là bất kỳ task nào block main thread hơn **50ms** — gây jank, delay input response, và tệ FID/INP.

**Tại sao 50ms?**

```text
60fps = 16.6ms per frame
Để đảm bảo smooth:
  → Task ≤ 50ms để còn time cho browser overhead
  → > 50ms = "long task" = likely causes jank
```

**Đo Long Tasks:**

```js
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    console.log('Long Task detected!');
    console.log('Duration:', entry.duration, 'ms');
    console.log('Start time:', entry.startTime, 'ms');

    // Attribution — ai gây ra long task?
    entry.attribution.forEach(attr => {
      console.log('Container:', attr.containerType); // 'window' | 'iframe' | 'embed'
      console.log('Container name:', attr.containerName);
      console.log('Container src:', attr.containerSrc);
    });
  }
}).observe({ type: 'longtask', buffered: true });
```

**Long Animation Frames (LoAF) — API mới hơn:**

```js
// Chrome 123+ — LoAF thay thế Long Tasks, nhiều thông tin hơn
new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    console.log('Long Animation Frame:', entry.duration, 'ms');
    console.log('Block duration:', entry.blockingDuration);
    console.log('Render start:', entry.renderStart);

    // Scripts gây ra long frame
    entry.scripts.forEach(script => {
      console.log('Script source:', script.sourceURL);
      console.log('Function:', script.sourceFunctionName);
      console.log('Duration:', script.duration);
      console.log('Invoker:', script.invoker); // 'IMG.onload', 'setTimeout', etc.
    });
  }
}).observe({ type: 'long-animation-frame', buffered: true });
```

**Phát hiện long tasks trong dev:**

```js
// Wrapper để profile functions
function measureTask(name, fn) {
  const start = performance.now();
  const result = fn();
  const duration = performance.now() - start;

  if (duration > 50) {
    console.warn(`⚠️ Long task: "${name}" took ${duration.toFixed(1)}ms`);
    console.trace(); // stack trace
  }

  return result;
}

// Dùng trong React
const expensiveValue = useMemo(() => {
  return measureTask('compute-expensive-value', () => {
    return computeExpensiveValue(data);
  });
}, [data]);
```

**Phân tách long tasks:**

```js
// ❌ Long task 200ms
function processAll(items) {
  items.forEach(item => heavyProcess(item)); // 200ms total
}

// ✅ Scheduler API — chia thành chunks, yield giữa
async function processAllChunked(items) {
  const CHUNK_SIZE = 50;
  for (let i = 0; i < items.length; i += CHUNK_SIZE) {
    const chunk = items.slice(i, i + CHUNK_SIZE);
    chunk.forEach(item => heavyProcess(item));

    // Yield sau mỗi chunk — cho browser xử lý input/render
    await new Promise(resolve => setTimeout(resolve, 0));
  }
}

// ✅ scheduler.postTask với background priority
for (const item of items) {
  scheduler.postTask(() => heavyProcess(item), { priority: 'background' });
}
```

---

### Tài liệu tham khảo

- [MDN: Long Tasks API](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceLongTaskTiming)
- [web.dev: Optimize Long Tasks](https://web.dev/articles/optimize-long-tasks)

## 87. Browser Memory Leak Detection

**Memory leak trong browser là gì?**

Memory leak xảy ra khi objects không còn cần dùng nhưng vẫn được giữ trong heap — Garbage Collector không thể thu hồi vì vẫn còn reference đến chúng.

**Các nguồn leak phổ biến:**

```js
// 1. Event listeners không được remove
function setupComponent(element) {
  const handler = () => doSomething();
  document.addEventListener('scroll', handler); // ❌ leak nếu component unmount

  // ✅ Cleanup
  return () => document.removeEventListener('scroll', handler);
}

// React version:
useEffect(() => {
  document.addEventListener('scroll', handler);
  return () => document.removeEventListener('scroll', handler); // cleanup
}, []);
```

```js
// 2. Closures giữ reference đến DOM nodes
let detachedNode; // DOM node bị remove nhưng vẫn referenced

function createLeak() {
  const node = document.createElement('div');
  document.body.appendChild(node);
  document.body.removeChild(node);
  detachedNode = node; // ❌ node bị detach nhưng vẫn trong memory
}
```

```js
// 3. Timers không được clear
function startPolling() {
  const intervalId = setInterval(() => {
    fetchData(); // closure giữ reference đến everything
  }, 1000);
  // ❌ Không clearInterval khi unmount → timer chạy mãi → leak

  // ✅
  return () => clearInterval(intervalId);
}
```

```js
// 4. Cache không có eviction policy
const cache = new Map(); // ❌ Map grow unbounded

// ✅ Dùng WeakMap — key bị GC khi không còn reference
const weakCache = new WeakMap();
// Hoặc LRU cache với size limit
```

**Phát hiện leak với Chrome DevTools:**

```text
1. Mở DevTools → Memory tab
2. Chụp heap snapshot lần 1
3. Thực hiện action nghi ngờ leak (navigate, click, ...)
4. Chụp heap snapshot lần 2
5. So sánh: chọn "Comparison" view
6. Tìm objects tăng lên bất thường
```

**Performance.measureUserAgentSpecificMemory():**

```js
// Chrome 89+ — đo memory usage
async function checkMemory() {
  if (!performance.measureUserAgentSpecificMemory) return;

  const result = await performance.measureUserAgentSpecificMemory();
  console.log('Total memory:', result.bytes / 1024 / 1024, 'MB');

  result.breakdown.forEach(entry => {
    console.log(`${entry.types.join(', ')}: ${entry.bytes / 1024}KB`);
  });
}
```

**WeakRef và FinalizationRegistry — track GC:**

```js
// WeakRef — giữ reference không ngăn GC
let obj = { data: 'important' };
const weakRef = new WeakRef(obj);

obj = null; // cho phép GC

// Sau GC:
const deref = weakRef.deref();
if (deref) {
  console.log(deref.data); // vẫn alive
} else {
  console.log('Object was garbage collected');
}

// FinalizationRegistry — callback khi GC thu hồi object
const registry = new FinalizationRegistry((heldValue) => {
  console.log(`Object ${heldValue} was GC'd`);
});

let target = { id: 1 };
registry.register(target, 'target-1'); // đăng ký
target = null; // eligible for GC → callback sẽ được gọi
```

**Detached DOM nodes — leak thường gặp:**

```js
// ❌ DOM node bị remove khỏi document nhưng JS vẫn giữ reference
const nodeCache = {};

function renderItem(id) {
  const el = document.createElement('div');
  nodeCache[id] = el; // cache reference
  container.appendChild(el);
}

function removeItem(id) {
  const el = nodeCache[id];
  container.removeChild(el);
  // ❌ nodeCache[id] vẫn reference → detached node → leak
  delete nodeCache[id]; // ✅ xóa reference
}
```

---

### Tài liệu tham khảo

- [Chrome DevTools: Fix Memory Problems](https://developer.chrome.com/docs/devtools/memory-problems)
- [MDN: Memory Management](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management)

## 88. Accessibility Tree

**Accessibility Tree là gì?**

Accessibility Tree là cấu trúc song song với DOM tree, được browser tạo ra và expose qua Accessibility API cho screen readers, assistive technologies.

**Từ DOM đến Accessibility Tree:**

```text
DOM Tree:
  <button class="btn" onclick="submit()">
    <span class="icon">✓</span>
    Submit
  </button>

Accessibility Tree Node:
  role: "button"
  name: "Submit"        (computed từ text content)
  state: { enabled: true, focusable: true }
  actions: [click, focus]
```

**Computed accessible name — thứ tự ưu tiên:**

```html
<!-- 1. aria-labelledby (cao nhất) -->
<div id="label">Full Name</div>
<input aria-labelledby="label" type="text">
<!-- Name: "Full Name" -->

<!-- 2. aria-label -->
<button aria-label="Close dialog">×</button>
<!-- Name: "Close dialog" (không phải "×") -->

<!-- 3. <label for> (cho form elements) -->
<label for="email">Email Address</label>
<input id="email" type="email">
<!-- Name: "Email Address" -->

<!-- 4. title attribute (fallback) -->
<img src="chart.png" title="Sales Chart 2024">
<!-- Name: "Sales Chart 2024" -->

<!-- 5. Text content (lowest) -->
<button>Delete Account</button>
<!-- Name: "Delete Account" -->
```

**ARIA roles và semantics:**

```html
<!-- Semantic HTML → implicit ARIA roles -->
<button>  → role="button"
<a href>  → role="link"
<h1>      → role="heading" aria-level="1"
<ul>      → role="list"
<nav>     → role="navigation"
<main>    → role="main"

<!-- Explicit ARIA role khi không có semantic HTML -->
<div role="button" tabindex="0" onclick="..." onkeydown="...">
  Custom Button
</div>
```

**Inspect Accessibility Tree trong DevTools:**

```text
Chrome DevTools:
  Elements → Accessibility panel (bên phải)
  Hoặc: Elements → chọn node → computed → Accessibility

Firefox:
  Developer Tools → Accessibility tab
  → Hiển thị full accessibility tree
```

**Hiding từ accessibility tree:**

```html
<!-- Ẩn hoàn toàn (cả visual + accessibility) -->
<div hidden>Hidden from everyone</div>
<div style="display: none">Also hidden</div>

<!-- Ẩn khỏi accessibility tree (vẫn visible) -->
<div aria-hidden="true">Decorative content</div>

<!-- Chỉ visible với screen readers (hidden visually) -->
<span class="sr-only">Additional context for screen readers</span>
<style>
  .sr-only {
    position: absolute;
    width: 1px; height: 1px;
    padding: 0; margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
  }
</style>
```

**Focus management:**

```js
// Quản lý focus khi mở modal
function openModal(modalEl) {
  modalEl.removeAttribute('hidden');
  modalEl.removeAttribute('aria-hidden');

  // Focus vào element đầu tiên trong modal
  const firstFocusable = modalEl.querySelector(
    'button, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])'
  );
  firstFocusable?.focus();
}

function closeModal(modalEl, triggerEl) {
  modalEl.setAttribute('hidden', '');
  modalEl.setAttribute('aria-hidden', 'true');

  // Trả focus về element đã mở modal
  triggerEl?.focus();
}
```

---

### Tài liệu tham khảo

- [MDN: Accessibility Tree](https://developer.mozilla.org/en-US/docs/Glossary/Accessibility_tree)
- [web.dev: Accessibility](https://web.dev/articles/accessibility)
- [Chrome DevTools: Accessibility Panel](https://developer.chrome.com/docs/devtools/accessibility/reference)

## 89. ARIA Live Regions Internals

**ARIA Live Regions là gì?**

Live regions là vùng trong trang mà nội dung thay đổi dynamically. Screen readers cần được thông báo về những thay đổi này mà không cần user focus vào đó.

**Các thuộc tính:**

```html
<!-- aria-live values -->
<div aria-live="off">Không thông báo thay đổi</div>
<div aria-live="polite">Thông báo sau khi user dừng tương tác</div>
<div aria-live="assertive">Thông báo ngay lập tức, ngắt đọc hiện tại</div>

<!-- aria-atomic: đọc toàn bộ region hay chỉ phần thay đổi -->
<div aria-live="polite" aria-atomic="true">
  <!-- Đọc toàn bộ khi bất kỳ phần nào thay đổi -->
  <span>Score: </span><span id="score">0</span>
</div>

<!-- aria-relevant: loại thay đổi nào được thông báo -->
<div aria-live="polite" aria-relevant="additions text">
  <!-- Chỉ thông báo khi thêm nodes hoặc text thay đổi -->
</div>
```

**Predefined live region roles:**

```html
<!-- role="status" = aria-live="polite" aria-atomic="true" -->
<div role="status">Form saved successfully</div>

<!-- role="alert" = aria-live="assertive" aria-atomic="true" -->
<div role="alert">Error: Invalid email address</div>

<!-- role="log" = aria-live="polite" thêm nội dung -->
<div role="log" aria-label="Chat messages">
  <!-- messages append vào đây -->
</div>

<!-- role="timer" -->
<div role="timer" aria-live="off">05:00</div>

<!-- role="progressbar" -->
<div role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">
  75%
</div>
```

**Kỹ thuật announce đúng cách:**

```js
// ❌ Screen reader có thể miss nếu content thay đổi quá nhanh
function announceError(message) {
  errorDiv.textContent = message; // set trực tiếp
}

// ✅ Pattern: clear trước, set sau → đảm bảo announcement
function announce(message, politeness = 'polite') {
  const liveRegion = document.getElementById(`live-${politeness}`);
  liveRegion.textContent = ''; // clear

  // Micro delay để screen reader detect change
  requestAnimationFrame(() => {
    liveRegion.textContent = message;
  });
}

// Setup HTML
// <div id="live-polite" aria-live="polite" aria-atomic="true" class="sr-only"></div>
// <div id="live-assertive" aria-live="assertive" aria-atomic="true" class="sr-only"></div>
```

**Toast notifications accessible:**

```jsx
// React toast với live region
function ToastProvider({ children }) {
  const [toasts, setToasts] = useState([]);

  function addToast(message, type = 'info') {
    const id = Date.now();
    setToasts(prev => [...prev, { id, message, type }]);
    setTimeout(() => removeToast(id), 5000);
  }

  function removeToast(id) {
    setToasts(prev => prev.filter(t => t.id !== id));
  }

  return (
    <ToastContext.Provider value={{ addToast }}>
      {children}

      {/* Live region cho screen readers */}
      <div
        role="status"
        aria-live="polite"
        aria-atomic="false"  // đọc từng toast, không đọc lại tất cả
        className="sr-only"
      >
        {toasts.map(t => (
          <div key={t.id}>{t.message}</div>
        ))}
      </div>

      {/* Visual toasts */}
      <div className="toast-container" aria-hidden="true">
        {toasts.map(t => (
          <Toast key={t.id} {...t} onDismiss={() => removeToast(t.id)} />
        ))}
      </div>
    </ToastContext.Provider>
  );
}
```

**Loading states:**

```html
<!-- Thông báo khi loading bắt đầu/kết thúc -->
<button onclick="loadData()" aria-describedby="load-status">
  Load More
</button>
<div id="load-status" role="status" aria-live="polite">
  <!-- "Loading..." khi fetch, "15 items loaded" khi xong -->
</div>
```

---

### Tài liệu tham khảo

- [MDN: ARIA Live Regions](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions)
- [WAI-ARIA: Live Region Roles](https://www.w3.org/TR/wai-aria-1.2/#live_region_roles)

## 90. Pointer Events Model

**Pointer Events là gì?**

Pointer Events là unified event model xử lý tất cả input device (mouse, touch, stylus) qua một API nhất quán — thay thế cho việc handle mouse events và touch events riêng.

**Pointer Events vs Mouse/Touch Events:**

| | Mouse Events | Touch Events | Pointer Events |
| --- | --- | --- | --- |
| Mouse | ✅ | ❌ | ✅ |
| Touch | ❌ | ✅ | ✅ |
| Stylus/Pen | ❌ | ❌ | ✅ |
| Multi-touch | ❌ | ✅ | ✅ |
| Pressure | ❌ | ❌ | ✅ |

**Pointer Events cơ bản:**

```js
element.addEventListener('pointerdown', (e) => {
  console.log('pointerId:', e.pointerId);    // unique ID cho mỗi pointer
  console.log('pointerType:', e.pointerType); // 'mouse' | 'touch' | 'pen'
  console.log('pressure:', e.pressure);      // 0.0–1.0
  console.log('tiltX:', e.tiltX);            // stylus tilt
  console.log('width:', e.width);            // contact area width
  console.log('height:', e.height);          // contact area height
  console.log('isPrimary:', e.isPrimary);    // primary pointer (first finger)
});

element.addEventListener('pointermove', handler);
element.addEventListener('pointerup', handler);
element.addEventListener('pointercancel', handler); // quan trọng!
element.addEventListener('pointerenter', handler);
element.addEventListener('pointerleave', handler);
element.addEventListener('pointerover', handler);
element.addEventListener('pointerout', handler);
```

**setPointerCapture — track pointer ngoài element:**

```js
// Capture pointer → nhận events kể cả khi pointer ra ngoài element
element.addEventListener('pointerdown', (e) => {
  element.setPointerCapture(e.pointerId);
  // Giờ tất cả pointer events của pointerId này đến element
  // kể cả khi pointer di chuyển ra ngoài element
});

element.addEventListener('pointerup', (e) => {
  element.releasePointerCapture(e.pointerId);
});

// Ví dụ: Drag & Drop
let isDragging = false;
let startX, startY;

el.addEventListener('pointerdown', (e) => {
  isDragging = true;
  startX = e.clientX;
  startY = e.clientY;
  el.setPointerCapture(e.pointerId); // capture để track drag ra ngoài
});

el.addEventListener('pointermove', (e) => {
  if (!isDragging) return;
  const dx = e.clientX - startX;
  const dy = e.clientY - startY;
  el.style.transform = `translate(${dx}px, ${dy}px)`;
});

el.addEventListener('pointerup', () => {
  isDragging = false;
});
```

**Multi-touch với Pointer Events:**

```js
const activePointers = new Map();

canvas.addEventListener('pointerdown', (e) => {
  canvas.setPointerCapture(e.pointerId);
  activePointers.set(e.pointerId, { x: e.clientX, y: e.clientY });

  if (activePointers.size === 2) {
    initPinchZoom([...activePointers.values()]);
  }
});

canvas.addEventListener('pointermove', (e) => {
  if (!activePointers.has(e.pointerId)) return;
  activePointers.set(e.pointerId, { x: e.clientX, y: e.clientY });

  if (activePointers.size === 2) {
    updatePinchZoom([...activePointers.values()]);
  }
});

canvas.addEventListener('pointerup', (e) => {
  activePointers.delete(e.pointerId);
});
```

**touch-action CSS — tối ưu scroll:**

```css
/* Cho phép browser xử lý scroll natively (không qua JS) */
.scrollable { touch-action: pan-y; }      /* chỉ scroll dọc */
.horizontal { touch-action: pan-x; }      /* chỉ scroll ngang */
.zoomable   { touch-action: pinch-zoom; } /* chỉ zoom */
.draggable  { touch-action: none; }       /* handle tất cả trong JS */

/* Mặc định: touch-action: auto → browser handle tất cả */
```

**pointercancel — xử lý đúng:**

```js
// pointercancel xảy ra khi:
// - Browser chiếm pointer (scroll, gesture)
// - Device không còn active (call coming in)
// - setPointerCapture bị cancel

element.addEventListener('pointercancel', (e) => {
  // LUÔN cleanup state khi cancel
  isDragging = false;
  activePointers.delete(e.pointerId);
  resetDragState();
});
```

---

### Tài liệu tham khảo

- [MDN: Pointer Events](https://developer.mozilla.org/en-US/docs/Web/API/Pointer_events)
- [W3C: Pointer Events Spec](https://www.w3.org/TR/pointerevents/)

## LEVEL 10: Kiến Trúc Hệ Thống Frontend Hiện Đại

---

## 91. Edge Rendering

**Edge Rendering là gì?**

Edge Rendering là mô hình render HTML tại các CDN edge nodes — gần user nhất về mặt địa lý — thay vì render tại origin server tập trung.

**So sánh các mô hình rendering:**

```text
CSR (Client-Side):
  Browser ──── CDN (static JS) ──── Browser renders
  Latency: TTFB thấp, nhưng LCP cao (chờ JS)

SSR (Origin Server):
  Browser ──── Long network hop ──── Origin renders HTML
  Latency: TTFB cao nếu origin xa user

Edge SSR:
  Browser ──── Nearest Edge Node (50ms away) ──── renders HTML
  Latency: TTFB rất thấp + full HTML ngay
```

**Edge runtime constraints:**

```text
✅ Có:
  - Fetch API
  - Web Crypto API
  - TextEncoder/Decoder
  - URL, Headers, Request, Response
  - ReadableStream, WritableStream
  - setTimeout (limited)
  - Cache API

❌ Không có:
  - Node.js built-ins (fs, path, net, crypto module)
  - Buffer (dùng Uint8Array)
  - process.env đầy đủ (chỉ một số vars)
  - Native modules (.node files)
  - Khởi động chậm (cold start < 1ms bắt buộc)
```

**Next.js Edge Runtime:**

```js
// app/api/hello/route.ts
export const runtime = 'edge'; // deploy tại Vercel Edge Network

export async function GET(request: Request) {
  const { searchParams } = new URL(request.url);
  const name = searchParams.get('name') ?? 'World';

  return new Response(JSON.stringify({ message: `Hello ${name}` }), {
    headers: { 'Content-Type': 'application/json' }
  });
}

// Middleware chạy tại edge — mọi request
// middleware.ts
export const config = { matcher: ['/((?!_next/static|favicon).*)'] };

export function middleware(request: Request) {
  const country = request.headers.get('cf-ipcountry') ?? 'US';

  // Redirect theo geo
  if (country === 'VN') {
    return Response.redirect(new URL('/vi', request.url));
  }

  return new Response(null, { status: 200 });
}
```

**Personalization tại Edge:**

```js
// A/B testing tại Edge — không cần roundtrip origin
export function middleware(request) {
  const bucket = Math.random() < 0.5 ? 'control' : 'variant';
  const response = NextResponse.next();

  response.cookies.set('ab-bucket', bucket);
  response.headers.set('x-ab-bucket', bucket);

  return response;
}

// Edge caching với personalization
export async function GET(request) {
  const cacheKey = new Request(request.url, {
    headers: { 'x-user-segment': request.headers.get('x-user-segment') }
  });

  const cached = await caches.open('v1').then(c => c.match(cacheKey));
  if (cached) return cached;

  const response = await generatePersonalizedHTML(request);
  await caches.open('v1').then(c => c.put(cacheKey, response.clone()));
  return response;
}
```

**Edge vs Serverless trade-offs:**

| | Edge Functions | Serverless Functions |
| --- | --- | --- |
| Cold start | < 1ms | 100ms–1s |
| Runtime | Web APIs only | Full Node.js |
| Location | Global (50+ nodes) | 1–3 regions |
| Execution limit | 30ms–50ms CPU | 15 phút |
| Memory | 128MB | 3GB |
| DB connections | Cần HTTP API | TCP OK |

---

### Tài liệu tham khảo

- [Vercel: Edge Functions](https://vercel.com/docs/functions/edge-functions)
- [Next.js: Edge and Node.js Runtimes](https://nextjs.org/docs/app/building-your-application/rendering/edge-and-nodejs-runtimes)

## 92. Micro-Frontend Orchestration

**Micro-Frontend là gì?**

Micro-Frontend áp dụng microservices pattern cho frontend — chia một web app lớn thành các ứng dụng nhỏ độc lập, mỗi team sở hữu và deploy một phần.

**Patterns chính:**

```text
1. Build-time integration:
   → Npm packages, import trực tiếp
   → Coupling cao, deploy phải sync
   → Phù hợp: shared component libraries

2. Run-time integration (URL):
   → Mỗi micro-frontend là app riêng tại URL riêng
   → iframe hoặc server-side compose
   → Isolation cao, UX bị gián đoạn

3. Run-time integration (JS):
   → Load JS của micro-frontend dynamically
   → Module Federation (Webpack 5)
   → Balance giữa isolation và UX
```

**Shell / Orchestrator pattern:**

```js
// Shell app — điều phối tất cả micro-frontends
class MicroFrontendOrchestrator {
  constructor() {
    this.registry = new Map();
    this.router = createRouter();
  }

  // Đăng ký micro-frontend
  register(name, config) {
    this.registry.set(name, {
      url: config.url,          // URL của remote entry
      routes: config.routes,    // routes thuộc về MFE này
      mount: config.mount,      // function mount vào DOM
      unmount: config.unmount   // function cleanup
    });
  }

  // Navigate → load và mount đúng MFE
  async navigate(path) {
    const mfe = this.findMFEForRoute(path);
    if (!mfe) return;

    // Unmount MFE hiện tại
    await this.currentMFE?.unmount();

    // Load MFE mới (dynamic import)
    const module = await this.loadMFE(mfe.url);
    this.currentMFE = module;

    // Mount vào shell
    await module.mount(document.getElementById('mfe-container'), {
      path,
      sharedServices: this.getSharedServices()
    });
  }

  async loadMFE(url) {
    // Cache loaded MFEs
    if (this.loadedMFEs.has(url)) return this.loadedMFEs.get(url);

    const module = await import(/* webpackIgnore: true */ url);
    this.loadedMFEs.set(url, module);
    return module;
  }
}
```

**Cross-MFE communication:**

```js
// Event bus — loose coupling giữa MFEs
class EventBus {
  constructor() {
    this.listeners = new Map();
  }

  emit(event, data) {
    window.dispatchEvent(new CustomEvent(`mfe:${event}`, { detail: data }));
  }

  on(event, handler) {
    const wrappedHandler = (e) => handler(e.detail);
    window.addEventListener(`mfe:${event}`, wrappedHandler);
    return () => window.removeEventListener(`mfe:${event}`, wrappedHandler);
  }
}

// MFE A phát event
eventBus.emit('cart:updated', { itemCount: 5 });

// MFE B lắng nghe
const unsubscribe = eventBus.on('cart:updated', ({ itemCount }) => {
  updateCartBadge(itemCount);
});
```

**Shared dependencies:**

```js
// Vấn đề: mỗi MFE có thể bundle React riêng → tốn kém
// Giải pháp: Shell cung cấp shared deps

// Shell expose React cho các MFEs
window.__MFE_SHARED__ = {
  React: require('react'),
  ReactDOM: require('react-dom'),
  // styled-components, router, etc.
};

// MFE dùng shared React thay vì bundle riêng
const React = window.__MFE_SHARED__?.React ?? require('react');
```

---

### Tài liệu tham khảo

- [micro-frontends.org](https://micro-frontends.org/)
- [Martin Fowler: Micro Frontends](https://martinfowler.com/articles/micro-frontends.html)

## 93. Module Federation

**Module Federation là gì?**

Module Federation (Webpack 5) cho phép một JavaScript app dynamically load code từ app khác tại runtime — chia sẻ modules giữa các builds độc lập.

**Khái niệm:**

```text
Host (Shell):          Remote (MFE):
  Consume modules  ←───  Expose modules
  tại runtime           từ build riêng

Remote không cần biết về Host
Host biết URL của Remote để load
```

**Cấu hình Webpack 5:**

```js
// Remote app — webpack.config.js (MFE ProductList)
const { ModuleFederationPlugin } = require('webpack').container;

module.exports = {
  plugins: [
    new ModuleFederationPlugin({
      name: 'productApp',
      filename: 'remoteEntry.js',       // entry point được expose
      exposes: {
        './ProductList': './src/ProductList', // expose component
        './useCart': './src/hooks/useCart',   // expose hook
      },
      shared: {
        react: { singleton: true, requiredVersion: '^18.0.0' },
        'react-dom': { singleton: true, requiredVersion: '^18.0.0' }
      }
    })
  ]
};

// Host app — webpack.config.js (Shell)
module.exports = {
  plugins: [
    new ModuleFederationPlugin({
      name: 'shell',
      remotes: {
        // Tên alias → URL của remoteEntry.js
        productApp: 'productApp@https://products.example.com/remoteEntry.js',
        cartApp: 'cartApp@https://cart.example.com/remoteEntry.js',
      },
      shared: {
        react: { singleton: true },
        'react-dom': { singleton: true }
      }
    })
  ]
};
```

**Dùng remote module trong Host:**

```jsx
// Host app — lazy load từ remote
import React, { lazy, Suspense } from 'react';

// Lazy import từ remote — load lúc runtime, không bundle vào host
const ProductList = lazy(() => import('productApp/ProductList'));
const CartWidget = lazy(() => import('cartApp/CartWidget'));

function App() {
  return (
    <div>
      <Suspense fallback={<div>Loading products...</div>}>
        <ProductList category="electronics" />
      </Suspense>

      <Suspense fallback={<div>Loading cart...</div>}>
        <CartWidget />
      </Suspense>
    </div>
  );
}
```

**Dynamic remotes — URL từ config:**

```js
// Không hardcode URL — load từ config server
async function loadRemote(name, url, module) {
  // Inject remote container dynamically
  await new Promise((resolve, reject) => {
    const script = document.createElement('script');
    script.src = url;
    script.onload = resolve;
    script.onerror = reject;
    document.head.appendChild(script);
  });

  // Init share scope
  await __webpack_init_sharing__('default');

  const container = window[name];
  await container.init(__webpack_share_scopes__.default);

  // Load module từ container
  const factory = await container.get(module);
  return factory();
}

// Dùng
const { ProductList } = await loadRemote(
  'productApp',
  'https://products.example.com/remoteEntry.js',
  './ProductList'
);
```

**Module Federation với Rspack/Vite:**

```js
// Vite — @originjs/vite-plugin-federation
import federation from '@originjs/vite-plugin-federation';

export default {
  plugins: [
    federation({
      name: 'shell',
      remotes: {
        productApp: 'https://products.example.com/assets/remoteEntry.js'
      },
      shared: ['react', 'react-dom']
    })
  ]
};
```

---

### Tài liệu tham khảo

- [Webpack: Module Federation](https://webpack.js.org/concepts/module-federation/)
- [Module Federation Docs](https://module-federation.io/)

## 94. WebAssembly Integration

**WebAssembly là gì?**

WebAssembly (WASM) là binary instruction format chạy trong browser với hiệu năng gần native — cho phép tích hợp code C/C++/Rust vào web app.

**Khi nào dùng WASM:**

```text
✅ Phù hợp:
  - Xử lý ảnh/video (codecs, filters)
  - Crypto/hashing operations
  - 3D rendering, physics simulation
  - PDF generation/parsing
  - Audio processing (DAW, effects)
  - Heavy data processing (CSV, compression)

❌ Không phù hợp:
  - DOM manipulation (WASM không access DOM trực tiếp)
  - Simple business logic
  - Network requests (cần JS bridge)
  - Nhỏ hơn 1MB code
```

**Load và call WASM từ JavaScript:**

```js
// Cách 1: WebAssembly.instantiateStreaming (khuyến nghị)
const { instance } = await WebAssembly.instantiateStreaming(
  fetch('/module.wasm'),
  {
    env: {
      // Import functions từ JS vào WASM
      consoleLog: (ptr, len) => {
        const bytes = new Uint8Array(instance.exports.memory.buffer, ptr, len);
        console.log(new TextDecoder().decode(bytes));
      },
      Math_random: Math.random
    }
  }
);

// Gọi exported functions
const result = instance.exports.add(10, 20); // 30
const fibResult = instance.exports.fibonacci(40);
```

**Rust → WASM với wasm-bindgen:**

```rust
// lib.rs (Rust)
use wasm_bindgen::prelude::*;

#[wasm_bindgen]
pub fn greet(name: &str) -> String {
    format!("Hello, {}!", name)
}

#[wasm_bindgen]
pub fn process_image(pixels: &[u8], width: u32, height: u32) -> Vec<u8> {
    // Heavy image processing in Rust
    apply_grayscale_filter(pixels, width, height)
}
```

```js
// JavaScript side
import init, { greet, process_image } from './pkg/my_module.js';

await init(); // load wasm file

console.log(greet('World')); // "Hello, World!"

// Process image — zero-copy với typed arrays
const canvas = document.querySelector('canvas');
const ctx = canvas.getContext('2d');
const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);

const processed = process_image(imageData.data, canvas.width, canvas.height);
ctx.putImageData(new ImageData(processed, canvas.width, canvas.height), 0, 0);
```

**WASM trong Web Worker — không block main thread:**

```js
// worker.js
import init, { heavyComputation } from './pkg/compute.js';

self.onmessage = async ({ data: { input } }) => {
  await init();
  const result = heavyComputation(input);
  self.postMessage({ result });
};

// main.js
const worker = new Worker('./worker.js', { type: 'module' });

worker.postMessage({ input: largeDataset });
worker.onmessage = ({ data: { result } }) => {
  updateUI(result); // back on main thread
};
```

**WASM memory model:**

```js
// WASM có linear memory — một ArrayBuffer lớn
const memory = instance.exports.memory;
const buffer = new Uint8Array(memory.buffer);

// Viết data vào WASM memory
const str = 'Hello';
const encoded = new TextEncoder().encode(str);
buffer.set(encoded, 0); // write tại offset 0

// Đọc data từ WASM memory
function readString(ptr, len) {
  return new TextDecoder().decode(
    new Uint8Array(memory.buffer, ptr, len)
  );
}

// Grow memory nếu cần
memory.grow(1); // tăng thêm 1 page (64KB)
```

---

### Tài liệu tham khảo

- [MDN: WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly)
- [WebAssembly.org](https://webassembly.org/getting-started/developers-guide/)
- [Rust & WebAssembly Book](https://rustwasm.github.io/docs/book/)

## 95. IndexedDB Scaling Strategy

**IndexedDB là gì?**

IndexedDB là NoSQL database trong browser — hỗ trợ lưu trữ lớn, indexes, transactions, và hoạt động async. Phù hợp cho offline-first apps.

**Kiến trúc IndexedDB:**

```text
Database
  └── Object Store (tương tự "table")
        ├── Records (key-value, value có thể là bất kỳ structured object)
        └── Indexes (để query theo field khác key)
```

**Setup với idb library (wrapper):**

```js
import { openDB } from 'idb';

const db = await openDB('myApp', 3, {
  upgrade(db, oldVersion, newVersion, transaction) {
    // Migration theo version
    if (oldVersion < 1) {
      const store = db.createObjectStore('tasks', { keyPath: 'id' });
      store.createIndex('by-status', 'status');
      store.createIndex('by-created', 'createdAt');
    }

    if (oldVersion < 2) {
      db.createObjectStore('attachments', { keyPath: 'id' });
    }

    if (oldVersion < 3) {
      // Thêm index mới
      transaction.objectStore('tasks').createIndex('by-assignee', 'assigneeId');
    }
  }
});
```

**Patterns nâng cao:**

```js
// 1. Bulk operations với transaction
async function bulkInsert(db, records) {
  const tx = db.transaction('tasks', 'readwrite');

  // Tất cả trong một transaction → atomic, nhanh hơn nhiều
  await Promise.all([
    ...records.map(r => tx.store.put(r)),
    tx.done
  ]);
}

// 2. Cursor để iterate lớn dataset (không load tất cả vào RAM)
async function processLargeDataset(db) {
  const tx = db.transaction('tasks', 'readonly');
  let cursor = await tx.store.openCursor();

  while (cursor) {
    processRecord(cursor.value); // xử lý từng record
    cursor = await cursor.continue();
  }
}

// 3. Index query
async function getTasksByStatus(db, status) {
  return db.getAllFromIndex('tasks', 'by-status', status);
}

// 4. Range query
async function getRecentTasks(db, since) {
  const range = IDBKeyRange.lowerBound(since);
  return db.getAllFromIndex('tasks', 'by-created', range);
}
```

**Sharding — scale IndexedDB:**

```js
// Vấn đề: Object store lớn → slow queries
// Giải pháp: Sharding theo time window

class ShardedStore {
  constructor(db) {
    this.db = db;
  }

  getShardName(timestamp) {
    // Shard theo tháng: 'events-2024-03'
    const date = new Date(timestamp);
    return `events-${date.getFullYear()}-${String(date.getMonth() + 1).padStart(2, '0')}`;
  }

  async put(record) {
    const shard = this.getShardName(record.timestamp);

    // Tạo shard store nếu chưa có (cần version upgrade)
    if (!this.db.objectStoreNames.contains(shard)) {
      await this.addShard(shard);
    }

    return this.db.put(shard, record);
  }

  async query(fromDate, toDate) {
    const shards = this.getShardsInRange(fromDate, toDate);
    const results = await Promise.all(
      shards.map(shard => this.db.getAll(shard))
    );
    return results.flat().filter(r => r.timestamp >= fromDate && r.timestamp <= toDate);
  }
}
```

**Storage quota và eviction:**

```js
// Kiểm tra quota
const { usage, quota } = await navigator.storage.estimate();
console.log(`Used: ${(usage / 1024 / 1024).toFixed(2)} MB`);
console.log(`Quota: ${(quota / 1024 / 1024).toFixed(2)} MB`);
console.log(`Used: ${((usage / quota) * 100).toFixed(1)}%`);

// Request persistent storage — ngăn browser xóa
const isPersisted = await navigator.storage.persist();
if (isPersisted) {
  console.log('Storage will not be cleared automatically');
} else {
  console.log('Storage may be cleared by browser under storage pressure');
}

// Cleanup strategy — xóa data cũ
async function cleanupOldData(db, maxAge = 30 * 24 * 60 * 60 * 1000) {
  const cutoff = Date.now() - maxAge;
  const range = IDBKeyRange.upperBound(cutoff);
  await db.delete('events', range); // xóa records có key < cutoff
}
```

---

### Tài liệu tham khảo

- [MDN: IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
- [web.dev: IndexedDB best practices](https://web.dev/articles/indexeddb-best-practices)

## 96. Server Components Architecture

**React Server Components (RSC) là gì?**

RSC là components chạy hoàn toàn trên server — không gửi JS xuống client, có thể trực tiếp access database/filesystem, và streaming vào client.

**RSC vs Client Components:**

| | Server Component | Client Component |
| --- | --- | --- |
| Render | Server only | Server (initial) + Client |
| JavaScript | Không gửi xuống client | Bundle và ship |
| State/hooks | ❌ Không có | ✅ useState, useEffect... |
| Event handlers | ❌ Không có | ✅ onClick, onChange... |
| DB/FS access | ✅ Trực tiếp | ❌ Qua API |
| Streaming | ✅ | ❌ |
| Default (Next.js) | ✅ | Cần `'use client'` |

**RSC wire format:**

```text
RSC không trả về HTML — trả về RSC Payload (JSON-like format)
→ Client runtime deserializes và reconciles với existing DOM
→ Cho phép streaming updates mà không mất client state

Ví dụ RSC Payload (simplified):
  0:["$","div",null,{"children":[
    ["$","h1",null,{"children":"Hello"}],
    ["$","$Lcomponent",null,{}]   ← Client Component placeholder
  ]}]
  1:I["./ClientButton",["chunk.js"],"ClientButton"]  ← Client Component manifest
```

**Data fetching trong RSC:**

```tsx
// app/products/page.tsx — Server Component
// Không cần useEffect, không cần loading state management
async function ProductsPage({ searchParams }) {
  // Trực tiếp query database — code này KHÔNG chạy trên client
  const products = await db.query(`
    SELECT * FROM products
    WHERE category = $1
    ORDER BY created_at DESC
  `, [searchParams.category]);

  // Parallel data fetching
  const [products, categories] = await Promise.all([
    fetchProducts(searchParams),
    fetchCategories()
  ]);

  return (
    <div>
      <CategoryFilter categories={categories} />  {/* Server Component */}
      <ProductGrid products={products} />          {/* Server Component */}
    </div>
  );
}
```

**Composing Server và Client Components:**

```tsx
// ✅ Đúng: Server Component render Client Component
// ServerLayout.tsx (Server)
import { ClientSidebar } from './ClientSidebar';

async function ServerLayout({ children }) {
  const user = await getUser(); // server-only
  return (
    <div>
      <ClientSidebar user={user} />  {/* pass serializable data */}
      <main>{children}</main>
    </div>
  );
}

// ❌ Sai: Client Component import Server Component trực tiếp
// ClientWrapper.tsx ('use client')
import { ServerComponent } from './ServerComponent'; // ❌ Error!

// ✅ Đúng: dùng children prop để compose
// ClientWrapper.tsx ('use client')
'use client';
function ClientWrapper({ children }) {
  const [open, setOpen] = useState(false);
  return <div onClick={() => setOpen(!open)}>{children}</div>;
}

// Page.tsx (Server)
<ClientWrapper>
  <ServerComponent /> {/* ✅ Server component passed as children */}
</ClientWrapper>
```

**Server Actions:**

```tsx
// app/actions.ts
'use server';

export async function createTask(formData: FormData) {
  const title = formData.get('title') as string;

  // Trực tiếp write database — không cần API endpoint
  const task = await db.tasks.create({ title, userId: getCurrentUser() });

  // Revalidate cache
  revalidatePath('/tasks');
  return task;
}

// Dùng trong component
function TaskForm() {
  return (
    <form action={createTask}>   {/* Server Action — không cần onSubmit handler */}
      <input name="title" />
      <button type="submit">Create Task</button>
    </form>
  );
}
```

---

### Tài liệu tham khảo

- [React Docs: Server Components](https://react.dev/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023)
- [Next.js: Server and Client Composition](https://nextjs.org/docs/app/building-your-application/rendering/composition-patterns)

## 97. Offline-First Design

**Offline-First là gì?**

Offline-First là kiến trúc thiết kế app hoạt động đầy đủ khi không có mạng — local database là source of truth, sync với server khi có kết nối.

**Online-First vs Offline-First:**

```text
Online-First:
  User action → API call → Update UI
  Khi offline: thất bại, show error

Offline-First:
  User action → Update local DB → Update UI (ngay lập tức)
               → Queue sync operation → Sync khi online
  Khi offline: vẫn hoạt động bình thường
```

**Kiến trúc tổng quan:**

```text
┌─────────────────────────────────────────────────────┐
│ Frontend                                             │
│                                                      │
│  UI Layer ←─────────────────── Local DB (IndexedDB) │
│      ↑                               ↑               │
│      │ reads                         │ sync          │
│      │                         Sync Engine           │
│      └──────────── Mutations ──────→     │           │
│                                          │           │
└──────────────────────────────────────────┼───────────┘
                                           │ (when online)
                                     Remote API
                                           │
                                    Server Database
```

**Sync Engine implementation:**

```js
class SyncEngine {
  constructor(localDB, remoteAPI) {
    this.db = localDB;
    this.api = remoteAPI;
    this.syncQueue = [];
    this.isSyncing = false;

    // Listen for online/offline events
    window.addEventListener('online', () => this.sync());
    window.addEventListener('offline', () => this.pauseSync());
  }

  // Mọi mutation đi qua đây
  async mutate(operation) {
    // 1. Apply optimistic update local
    const result = await this.db.apply(operation);

    // 2. Queue để sync
    await this.db.addToSyncQueue({
      id: crypto.randomUUID(),
      operation,
      timestamp: Date.now(),
      retries: 0
    });

    // 3. Trigger sync nếu online
    if (navigator.onLine) this.sync();

    return result;
  }

  async sync() {
    if (this.isSyncing) return;
    this.isSyncing = true;

    try {
      const pending = await this.db.getSyncQueue();

      for (const item of pending) {
        try {
          const serverResult = await this.api.apply(item.operation);

          // Server có thể trả về state đã merge (conflict resolved)
          await this.db.reconcile(item.operation.entityId, serverResult);
          await this.db.removeSyncItem(item.id);

        } catch (error) {
          if (error.status === 409) {
            // Conflict — cần resolution
            const resolved = await this.resolveConflict(item, error.serverState);
            await this.db.removeSyncItem(item.id);
            if (resolved) await this.mutate(resolved);
          } else if (item.retries < 3) {
            await this.db.updateSyncItem(item.id, { retries: item.retries + 1 });
          } else {
            await this.db.markSyncFailed(item.id);
          }
        }
      }
    } finally {
      this.isSyncing = false;
    }
  }
}
```

**Service Worker caching strategy:**

```js
// sw.js — Cache API + sync strategy
const CACHE_VERSION = 'v2';

// Cache-first cho static assets
self.addEventListener('fetch', (event) => {
  const url = new URL(event.request.url);

  if (isStaticAsset(url)) {
    event.respondWith(cacheFirst(event.request));
  } else if (isAPIRequest(url)) {
    event.respondWith(networkFirstWithFallback(event.request));
  }
});

async function networkFirstWithFallback(request) {
  try {
    const response = await fetch(request.clone());
    const cache = await caches.open(CACHE_VERSION);
    cache.put(request, response.clone());
    return response;
  } catch {
    // Offline → serve từ cache
    const cached = await caches.match(request);
    if (cached) return cached;

    // Không có cache → return offline page
    return caches.match('/offline.html');
  }
}
```

---

### Tài liệu tham khảo

- [web.dev: Offline Cookbook](https://web.dev/articles/offline-cookbook)
- [MDN: Progressive Web Apps — Offline](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Offline_and_background_operation)

## 98. Conflict Resolution Models

**Khi nào xảy ra conflict?**

Conflict xảy ra khi cùng một dữ liệu được sửa đổi bởi nhiều client trong khi offline, và khi sync lại — server không biết version nào đúng.

**Các mô hình giải quyết conflict:**

### 1. Server Wins (Override)

```js
// Đơn giản nhất — server luôn đúng
// Mọi local changes bị ghi đè bởi server state

async function syncWithServerWins(localData, serverId) {
  const serverData = await fetch(`/api/items/${serverId}`).then(r => r.json());
  await localDB.put(serverId, serverData); // ghi đè local
}

// ❌ User mất local changes → frustrating
// ✅ Dữ liệu nhất quán 100%
// Dùng khi: data nguồn thực sự là server (config, permissions)
```

### 2. Client Wins (Optimistic)

```js
// Local changes luôn thắng
async function syncWithClientWins(localOp) {
  await fetch('/api/items', {
    method: 'PUT',
    body: JSON.stringify({ ...localOp, force: true })
  });
}

// ❌ Collaboration issues — người sau ghi đè người trước
// ✅ User thấy changes của mình được giữ
// Dùng khi: personal data (user preferences, local notes)
```

### 3. Three-Way Merge

```js
// So sánh: base (common ancestor) + local + remote
function threeWayMerge(base, local, remote) {
  const result = {};

  const allKeys = new Set([
    ...Object.keys(base),
    ...Object.keys(local),
    ...Object.keys(remote)
  ]);

  for (const key of allKeys) {
    const baseVal = base[key];
    const localVal = local[key];
    const remoteVal = remote[key];

    const localChanged = !deepEqual(localVal, baseVal);
    const remoteChanged = !deepEqual(remoteVal, baseVal);

    if (!localChanged && !remoteChanged) {
      result[key] = baseVal;          // không ai đổi → giữ base
    } else if (localChanged && !remoteChanged) {
      result[key] = localVal;         // chỉ local đổi → lấy local
    } else if (!localChanged && remoteChanged) {
      result[key] = remoteVal;        // chỉ remote đổi → lấy remote
    } else {
      result[key] = handleConflict(key, localVal, remoteVal, baseVal);
    }
  }

  return result;
}

function handleConflict(key, local, remote, base) {
  // Chiến lược tùy loại field:
  if (typeof local === 'number' && typeof remote === 'number') {
    // Số: merge bằng delta
    const localDelta = local - base;
    const remoteDelta = remote - base;
    return base + localDelta + remoteDelta; // cộng gộp cả 2 changes
  }

  if (Array.isArray(local) && Array.isArray(remote)) {
    // Array: union (có thể dùng CRDT Set)
    return [...new Set([...local, ...remote])];
  }

  // Fallback: last-write-wins hoặc prompt user
  return remote; // hoặc showConflictUI(key, local, remote)
}
```

### 4. User-Prompted Resolution

```jsx
// Hiển thị conflict dialog cho user quyết định
function ConflictResolutionDialog({ conflicts, onResolve }) {
  return (
    <dialog open>
      <h2>Conflict Detected</h2>
      {conflicts.map(conflict => (
        <div key={conflict.field}>
          <p>Field: <strong>{conflict.field}</strong></p>
          <div className="options">
            <button onClick={() => onResolve(conflict.field, 'local')}>
              Keep your version: {JSON.stringify(conflict.local)}
            </button>
            <button onClick={() => onResolve(conflict.field, 'remote')}>
              Use server version: {JSON.stringify(conflict.remote)}
            </button>
          </div>
        </div>
      ))}
    </dialog>
  );
}
```

**Vector clocks — track causality:**

```js
// Vector clock xác định thứ tự nhân quả giữa events
class VectorClock {
  constructor(nodeId, peers = []) {
    this.nodeId = nodeId;
    this.clock = { [nodeId]: 0 };
    peers.forEach(p => { this.clock[p] = 0; });
  }

  tick() {
    this.clock[this.nodeId]++;
    return { ...this.clock };
  }

  update(remoteClock) {
    for (const [node, time] of Object.entries(remoteClock)) {
      this.clock[node] = Math.max(this.clock[node] || 0, time);
    }
    this.clock[this.nodeId]++;
  }

  // So sánh: concurrent (có thể conflict) hay happened-before (safe)
  compare(a, b) {
    let aBeforeB = true;
    let bBeforeA = true;

    const allNodes = new Set([...Object.keys(a), ...Object.keys(b)]);
    for (const node of allNodes) {
      if ((a[node] || 0) > (b[node] || 0)) bBeforeA = false;
      if ((b[node] || 0) > (a[node] || 0)) aBeforeB = false;
    }

    if (aBeforeB && !bBeforeA) return 'before';
    if (bBeforeA && !aBeforeB) return 'after';
    if (!aBeforeB && !bBeforeA) return 'concurrent'; // → conflict!
    return 'equal';
  }
}
```

---

### Tài liệu tham khảo

- [crdt.tech: CRDT Resources](https://crdt.tech/)
- [Martin Fowler: CQRS](https://martinfowler.com/bliki/CQRS.html)

## 99. Distributed UI Consistency

**Bài toán:**

Khi nhiều users cùng xem và sửa một giao diện — đảm bảo tất cả thấy state nhất quán mà không có stale data, ghost updates, hay inconsistent renders.

**Các mức độ consistency:**

```text
Strong Consistency:
  → Mọi read đều thấy write gần nhất
  → Cần central coordinator, lock
  → Chậm, khó scale

Eventual Consistency:
  → Sau một thời gian, mọi node sẽ hội tụ về cùng state
  → Không cần lock, scale tốt
  → Có thể thấy stale data tạm thời

Causal Consistency:
  → Nếu A causally trước B, mọi node thấy A trước B
  → Balance giữa Strong và Eventual
  → Dùng Vector Clocks để track
```

**Optimistic UI với rollback:**

```js
class OptimisticStore {
  constructor() {
    this.confirmedState = {};
    this.pendingOps = [];
  }

  // Tính UI state = confirmed + apply all pending ops
  getUIState() {
    return this.pendingOps.reduce(
      (state, op) => applyOp(state, op),
      this.confirmedState
    );
  }

  // Optimistic update
  dispatch(op) {
    const tempId = crypto.randomUUID();
    this.pendingOps.push({ ...op, tempId });

    // Gửi lên server
    return sendToServer(op)
      .then(serverOp => this.confirm(tempId, serverOp))
      .catch(err => this.rollback(tempId, err));
  }

  confirm(tempId, serverOp) {
    // Server có thể transform op (rebase)
    this.confirmedState = applyOp(this.confirmedState, serverOp);
    this.pendingOps = this.pendingOps.filter(op => op.tempId !== tempId);
    // Re-apply remaining pending ops on top of new confirmed state
  }

  rollback(tempId, error) {
    this.pendingOps = this.pendingOps.filter(op => op.tempId !== tempId);
    showError('Operation failed, changes reverted', error);
    // UI tự động recompute từ confirmedState + remaining pendingOps
  }
}
```

**Real-time sync với WebSocket:**

```js
class RealtimeConsistencyManager {
  constructor(ws, localStore) {
    this.ws = ws;
    this.store = localStore;
    this.operationLog = [];

    ws.addEventListener('message', ({ data }) => {
      const op = JSON.parse(data);
      this.applyRemoteOperation(op);
    });
  }

  applyRemoteOperation(remoteOp) {
    // Transform remote op relative to pending local ops
    const transformedOp = this.operationLog.reduce(
      (op, localOp) => operationalTransform(op, localOp),
      remoteOp
    );

    this.store.apply(transformedOp);
    this.emitUIUpdate(transformedOp);
  }

  localMutation(op) {
    const timestampedOp = { ...op, clientTime: Date.now(), version: this.version++ };
    this.operationLog.push(timestampedOp);
    this.store.applyOptimistically(op);
    this.ws.send(JSON.stringify(timestampedOp));
  }
}
```

**Presence — ai đang xem/chỉnh sửa:**

```js
// Yjs + awareness cho real-time presence
import * as Y from 'yjs';
import { WebsocketProvider } from 'y-websocket';

const ydoc = new Y.Doc();
const provider = new WebsocketProvider('wss://collab.example.com', 'room-1', ydoc);

// Set presence data
provider.awareness.setLocalStateField('user', {
  name: 'Alice',
  color: '#ff0000',
  cursor: { x: 100, y: 200 } // caret position trong editor
});

// Observe all users' presence
provider.awareness.on('change', () => {
  const states = [...provider.awareness.getStates().values()];
  renderPresenceIndicators(states);
});
```

---

### Tài liệu tham khảo

- [Yjs: Real-time collaboration](https://docs.yjs.dev/)
- [MDN: WebSockets API](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)

## 100. Frontend System Design Trade-offs

**System Design là gì trong Frontend?**

Frontend system design là quá trình đưa ra các quyết định kiến trúc cân bằng giữa nhiều yếu tố mâu thuẫn nhau — performance, developer experience, scalability, maintainability.

**Framework chọn lựa kiến trúc:**

```text
Câu hỏi cần trả lời:
1. Data flows như thế nào?
2. Ai sở hữu state?
3. Rendering xảy ra ở đâu?
4. Caching strategy là gì?
5. Bundle size được kiểm soát như thế nào?
6. Team structure ảnh hưởng thế nào?
```

**Rendering strategy trade-offs:**

| Strategy | TTFB | FCP | Interactivity | SEO | Personalization | Caching |
| --- | --- | --- | --- | --- | --- | --- |
| CSR | Rất nhanh | Chậm (chờ JS) | Sau JS load | Kém | Dễ | CDN static |
| SSR | Chậm (chờ server) | Nhanh | Sau hydration | Tốt | Dễ | Khó |
| SSG | Rất nhanh | Rất nhanh | Sau hydration | Tốt | Khó | CDN |
| ISR | Nhanh | Nhanh | Sau hydration | Tốt | Vừa | CDN + revalidate |
| Streaming SSR | Nhanh (shell) | Nhanh | Progressive | Tốt | Dễ | Partial |
| Islands | Nhanh | Nhanh | Selective | Tốt | Vừa | CDN |

**State management trade-offs:**

```text
useState/useReducer (local):
  ✅ Simple, no boilerplate, colocated
  ❌ Prop drilling, hard to share
  Dùng khi: component-local state

Context API:
  ✅ Built-in, no dependency
  ❌ Re-render khi value thay đổi, không scalable
  Dùng khi: theme, auth, low-frequency updates

Zustand / Jotai:
  ✅ Minimal boilerplate, atomic updates
  ❌ Thêm dependency
  Dùng khi: moderate global state, performance matters

Redux Toolkit:
  ✅ Predictable, devtools, large ecosystem
  ❌ Boilerplate, learning curve
  Dùng khi: complex state, large teams, time-travel debug

React Query / SWR:
  ✅ Server state management, caching, background sync
  ❌ Chỉ cho async/server state
  Dùng khi: API data với caching needs
```

**Monorepo vs Polyrepo:**

```text
Monorepo (Nx, Turborepo):
  ✅ Shared code dễ dàng, atomic commits, unified tooling
  ✅ Refactoring cross-package an toàn
  ❌ Slow CI nếu không có incremental builds
  ❌ Complex setup, steep learning curve
  Dùng khi: nhiều packages chia sẻ code, team lớn

Polyrepo:
  ✅ Simple, isolated, team autonomy
  ✅ Fast CI per repo
  ❌ Versioning hell, breaking changes khó track
  ❌ Code duplication
  Dùng khi: teams hoàn toàn độc lập, microservices
```

**Build tool trade-offs:**

| Tool | Dev Speed | Build Speed | Config | HMR | Ecosystem |
| --- | --- | --- | --- | --- | --- |
| Webpack | Chậm | Chậm | Phức tạp | OK | Lớn nhất |
| Vite | Rất nhanh | Nhanh (Rollup) | Minimal | Xuất sắc | Lớn |
| Rspack | Nhanh | Rất nhanh | Webpack compat | OK | Đang tăng |
| Turbopack | Rất nhanh | Rất nhanh | Minimal | Xuất sắc | Next.js |
| esbuild | Cực nhanh | Cực nhanh | Minimal | Không built-in | Nhỏ |

**Micro-frontend vs Monolith trade-offs:**

```text
Monolith Frontend:
  ✅ Simple deployment, shared state dễ, consistent UX
  ✅ Optimal bundle splitting (shared deps)
  ❌ Team coupling, scale của một codebase
  ❌ Technology lock-in
  Dùng khi: team ≤ 5, product mới, startup

Micro-Frontends:
  ✅ Team autonomy, independent deploy, tech diversity
  ✅ Fault isolation — một MFE crash không down toàn bộ
  ❌ Complex orchestration, network overhead
  ❌ UX consistency khó hơn, duplicate deps
  Dùng khi: nhiều team độc lập, enterprise scale
```

**Checklist System Design Frontend:**

```text
1. Clarify requirements
   □ Scale: DAU, concurrent users, data volume?
   □ Team: số lượng, location, skill?
   □ Constraints: timeline, tech stack existing?

2. High-level architecture
   □ Rendering strategy (CSR/SSR/SSG/Islands)?
   □ State management approach?
   □ Data fetching pattern?
   □ Auth strategy?

3. Component architecture
   □ Design system / component library?
   □ Code sharing strategy?
   □ Bundle splitting approach?

4. Performance
   □ Core Web Vitals targets?
   □ Caching strategy (HTTP cache, service worker, in-memory)?
   □ Lazy loading strategy?

5. Resilience
   □ Error boundaries?
   □ Offline support cần thiết không?
   □ Graceful degradation?

6. Observability
   □ RUM (Real User Monitoring)?
   □ Error tracking (Sentry)?
   □ Performance monitoring?
```

### Tài liệu tham khảo

- [web.dev: Core Web Vitals](https://web.dev/articles/vitals)
- [Next.js: Rendering](https://nextjs.org/docs/app/building-your-application/rendering)
- [Martin Fowler: Micro Frontends](https://martinfowler.com/articles/micro-frontends.html)
