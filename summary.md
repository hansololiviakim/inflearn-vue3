# Vue.js 알아보기

## Vue.js란?

- 간단한 화면 UI 개발부터 라우팅, SSR 등의 애플리케이션 레벨의 개발을 지원하는 프레임워크

- Vue.js는 점진적 채택 가능성, 모듈화, 유연성, 점진적 강화를 통해 기능을 확장하고 기존 프로젝트와 쉽게 통합할 수 있어 프로그레시브 프레임워크(Progressive Framework)라고 불림

<br /><br />

## Vue.js의 핵심 기능 및 특징

### 선언적 렌더링(Declarative Rendering)

- 표준 HTML을 템플릿 문법으로 확장하여 JavaScript 상태(State)를 기반으로 화면에 출력될 HTML을 선언적으로 작성할 수 있음

<br />

### 반응성(Reactivity)

- JavaScript 상태(State) 변경을 추적하고, 변경이 발생하면 DOM을 효율적으로 업데이트하는 것을 자동적으로 수행함

<br />

### 싱글 파일 컴포넌트(SFC)

- Vue 컴포넌트를 논리(JavaScript), 템플릿(HTML), 스타일(CSS)을 하나의 파일에 캡슐화

- SFC는 Vue를 빌드 방식으로 사용하는 경우 컴포넌트를 만들고 정의하는데 권장되는 방법

<br />

### API 스타일

| `옵션 API`

- 객체 내 data, methods, lifecycle hooks 사용

- 컴포넌트 인스턴스를 가리키는 'this' 사용

- OOP 언어 배경의 사용자에게 친숙함

<br />

| `컴포지션 API`

- 'ref', 'onMounted' 등 함수로 상태와 로직 정의

- '&#60;script setup&#62;'을 사용해 템플릿에 직접 변수 및 함수 사용 가능

- 유연하고 로직 재사용 용이

<br /><br />

# Vue2와 Vue3의 차이점

- 라이브러리 내부 로직이 TypeScript로 재작성됨

- 주요 개발 도구들 변경: 뷰 개발자 도구, 플러그인 Vetur → Volar, Vite 기반 프로젝트 생성 등

- 컴포지션 API, Teleport 등 새로운 문법 지원

- 리액티비티 시스템 기반 API 변경

<br />

## 표로 다시 보기

| **구분** | **Vue 2** | **Vue 3** |
|---|---|---|
| **성능** | 컴파일러와 런타임 최적화 부족 | 컴파일러와 런타임 최적화로 성능 향상 |
| **Composition API** | 지원하지 않음 (`@vue/composition-api` 패키지를 통해 일부 사용 가능) | 새로운 Composition API 도입, React Hooks와 유사 |
| **반응성** | `Object.defineProperty` 기반 | `Proxy` 기반 반응성, 성능 및 기능 개선 |
| **트리 쉐이킹** | 기본적으로 지원하지 않음 | 트리 쉐이킹 지원, 빌드 크기 감소 및 성능 향상 |
| **TypeScript 지원**  제한적 지원, 추가 설정 필요 | TypeScript와의 호환성 개선, 쉽게 개발 가능 |
| **프래그먼트** | 단일 루트 엘리먼트만 허용 | 여러 루트 엘리먼트를 가질 수 있는 프래그먼트 지원 |
| **Custom Renderer API**  | 지원하지 않음 | Custom Renderer API 도입, 웹이 아닌 플랫폼에서도 렌더링 가능 |
| **Teleport** | 지원하지 않음 | 새로운 `Teleport` 기능으로 다른 DOM 노드로 쉽게 렌더링 가능  |
| **생명주기 훅** | 기존 생명주기 훅 (`beforeDestroy`, `destroyed`) 사용 | 생명주기 훅 이름 변경 (`beforeUnmount`, `unmounted`) |
| **글로벌 API** | `Vue` 생성자 사용 | 새로운 글로벌 API (`app.component` 등) 사용 |
| **Template Directives**  | `v-model` 지시자가 제한적 | `v-model` 지시자가 다양한 사용 사례 지원 |

<br />

<details>
  <summary><b>[참고] 용어 설명</b></summary>

- Composition API

  - Vue 3에서 도입된 새로운 API로, 컴포넌트 로직을 함수 단위로 작성하여 재사용성과 코드 구조를 개선함

- 트리 쉐이킹

  - 사용하지 않는 코드(모듈)를 빌드 과정에서 제거하여 최종 번들 크기를 줄이는 최적화 기법

- 프래그먼트

  - 여러 루트 엘리먼트를 하나의 컴포넌트에서 반환할 수 있게 하는 기능으로 불필요한 래퍼 엘리먼트를 피할 수 있음

- Custom Renderer API

  - 웹이 아닌 플랫폼(예: 네이티브 모바일, WebGL)에서도 Vue를 사용할 수 있게 해주는 API

- Teleport

  - 특정 DOM 노드로 컴포넌트의 내용을 렌더링할 수 있는 기능, 모달, 툴팁 등을 구현할 때 유용

</details>
