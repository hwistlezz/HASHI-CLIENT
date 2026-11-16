<div align="center">

<img width="300" alt="h" src="https://github.com/user-attachments/assets/5298892e-9135-49bb-b2ac-5ea650c8ea88" />

# [HASHI](https://www.hashi.kr/)

> 발견부터 예약까지, 포기 없이

![HASHI](https://img.shields.io/badge/HASHI-Japanese%20Restaurant%20Reservation-FF5A5F?style=for-the-badge)

</div>

---

## 🍽️ About Hashi

<img width="7680" height="4320" alt="최종 디벨롭 후보" src="https://github.com/user-attachments/assets/cdb8f00b-8e43-41a9-9e03-c152bc3c5a9e" />

<img width="7680" height="4320" alt="기존 서비스의 한계" src="https://github.com/user-attachments/assets/66913dff-dc2f-4c9f-894d-075095479c49" />

---

## ✨ Main Features

| Feature      | Description                                                                |
| ------------ | -------------------------------------------------------------------------- |
| 홈           | 오늘의 식당, 하시픽, 인기 맛집, 매거진 등 주요 콘텐츠를 제공합니다.        |
| 검색         | 키워드와 음식 장르, 정렬 필터를 통해 일본 맛집을 탐색할 수 있습니다.       |
| 식당 상세    | 식당 정보, 메뉴, 리뷰, 매장 정보를 확인할 수 있습니다.                     |
| 오늘의 식당  | 랜덤 추천 식당을 확인하고 다시 추천받을 수 있습니다.                       |
| 예약 신청    | 식당 예약 정보를 입력하고 포인트 기반 수수료를 확인할 수 있습니다.         |
| 내 예약 정보 | 진행 중, 방문 예정, 방문 완료, 예약 취소 상태별 예약을 확인할 수 있습니다. |
| 예약 상세    | 예약 정보 확인과 예약 취소를 지원합니다.                                   |
| 리뷰         | 방문 완료 예약에 대해 리뷰를 작성하고, 작성한 리뷰를 관리할 수 있습니다.   |
| 마이페이지   | 사용자 프로필, 보유 포인트, 마이 리뷰 정보를 확인할 수 있습니다.           |
| 매거진       | 일본 맛집과 여행 관련 콘텐츠를 제공합니다.                                 |
| PWA          | 모바일 웹 환경에서 앱처럼 사용할 수 있도록 PWA를 지원합니다.               |

## ⚒️ Tech Stack

> 자세한 기술 스택과 버전 기준은 [Tech Stack](./docs/architecture/tech-stack.md)을 따릅니다.

<div align="center">

### Core

<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=000" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=fff" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=fff" />

<br />

### Styling

<img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=fff" />
<img src="https://img.shields.io/badge/CVA-2D3A3F?style=for-the-badge" />

<br />

### State & API

<img src="https://img.shields.io/badge/TanStack%20Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=fff" />
<img src="https://img.shields.io/badge/ky-2D3A3F?style=for-the-badge" />
<img src="https://img.shields.io/badge/openapi--typescript-6BA539?style=for-the-badge" />

<br />

### Monorepo

<img src="https://img.shields.io/badge/pnpm-F69220?style=for-the-badge&logo=pnpm&logoColor=fff" />
<img src="https://img.shields.io/badge/Turborepo-EF4444?style=for-the-badge&logo=turborepo&logoColor=fff" />

<br />

### Test & Docs

<img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=fff" />
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=fff" />
<img src="https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=fff" />

<br />

### Monitoring & Deploy

<img src="https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=fff" />
<img src="https://img.shields.io/badge/Google%20Analytics-E37400?style=for-the-badge&logo=googleanalytics&logoColor=fff" />
<img src="https://img.shields.io/badge/Vercel-000?style=for-the-badge&logo=vercel&logoColor=fff" />

</div>

## 📁 Folder Responsibility

> 자세한 기준은 [App Structure](./docs/architecture/app-structure.md)를 따릅니다.

| Folder     | Responsibility                                     |
| ---------- | -------------------------------------------------- |
| `app`      | 전역 Provider, Router, Layout 등 앱 실행 조립 코드 |
| `pages`    | route 단위 화면, 페이지 전용 UI와 상태 조합        |
| `features` | 여러 페이지에서 재사용되는 도메인 기능             |
| `shared`   | 도메인과 무관하게 앱 내부에서 공유되는 공통 코드   |
| `test`     | 테스트 환경 설정과 공통 mock 유틸                  |

### Placement Rule

- 특정 route에서만 사용하는 코드는 pages/{pageName}에 둡니다.
- 여러 페이지에서 재사용되는 도메인 기능은 features/{domain}으로 승격합니다.
- 도메인 의미가 없는 공통 hook, util, component는 shared에 둡니다.
- page끼리는 서로의 내부 파일을 직접 import하지 않습니다.
- UI primitive는 packages/hds-ui, icon은 packages/hds-icons, token은 packages/hds-tokens에서 관리합니다.

## 🧭 Workspace Apps

| App                   | Package             | Description             |
| --------------------- | ------------------- | ----------------------- |
| `apps/client`         | `@hashi/client`     | 사용자 서비스 앱        |
| `apps/admin`          | `@hashi/admin`      | 관리자 앱               |
| `packages/hds-ui`     | `@hashi/hds-ui`     | 공통 UI 컴포넌트 패키지 |
| `packages/hds-icons`  | `@hashi/hds-icons`  | 공통 아이콘 패키지      |
| `packages/hds-tokens` | `@hashi/hds-tokens` | 디자인 토큰 패키지      |

### App Commands

| Target | Dev               | Build               | Preview               |
| ------ | ----------------- | ------------------- | --------------------- |
| Client | `pnpm dev:client` | `pnpm build:client` | `pnpm preview:client` |
| Admin  | `pnpm dev:admin`  | `pnpm build:admin`  | `pnpm preview:admin`  |
| All    | -                 | `pnpm build`        | -                     |

기본 `vercel.json`은 client 배포용입니다. Admin은 별도 Vercel project에서 `vercel.admin.json`을 사용합니다.

GitHub Actions는 client와 admin 배포 workflow를 분리합니다. Admin workflow는
`VERCEL_ADMIN_PROJECT_ID` repository secret으로 Admin Vercel project를 선택하고,
`vercel.admin.json`을 명시적으로 사용합니다.

```bash
pnpm exec vercel build --local-config vercel.admin.json
pnpm exec vercel deploy --prebuilt --local-config vercel.admin.json
```

## 📖 Convention

### Coding Convention

> 자세한 기준은 [Coding Convention](./docs/conventions/coding.md)을 따릅니다.

- 컴포넌트는 arrow function과 named export를 사용합니다.
- 컴포넌트 파일은 PascalCase, 일반 .ts 파일과 폴더는 camelCase를 사용합니다.
- 의미 없는 div 사용을 지양하고 가능한 semantic tag를 사용합니다.
- 버튼 역할은 button 요소를 사용하고, 텍스트가 없는 아이콘 버튼에는 aria-label을 제공합니다.
- 타입 이름은 PascalCase, Props 타입은 Props 접미사를 사용합니다.
- 이벤트 핸들러에는 handle 접두사를 사용합니다.
- boolean 값은 is, has, check 등의 접두사로 의미를 드러냅니다.
- 컴포넌트 파일은 PascalCase, 일반 .ts 파일과 폴더는 camelCase를 사용합니다.
- 의미 없는 div 사용을 지양하고 가능한 semantic tag를 사용합니다.
- 버튼 역할은 button 요소를 사용하고, 텍스트가 없는 아이콘 버튼에는 aria-label을 제공합니다.
- 타입 이름은 PascalCase, Props 타입은 Props 접미사를 사용합니다.
- 이벤트 핸들러에는 handle 접두사를 사용합니다.
- boolean 값은 is, has, check 등의 접두사로 의미를 드러냅니다.
- 스타일은 기본적으로 Tailwind CSS utility class를 사용합니다.
- 반복되는 variant 조합은 class-variance-authority의 cva와 VariantProps를 사용합니다.
- 반복되는 variant 조합은 class-variance-authority의 cva와 VariantProps를 사용합니다.
- 공통 디자인 값은 HDS token을 우선 사용합니다.

### Package Management

- 패키지 매니저는 `pnpm`을 사용합니다.
- `npm`, `yarn`, `bun` lockfile을 추가하지 않습니다.
- 외부 패키지 버전은 `pnpm-workspace.yaml`의 catalog에서 관리합니다.
- 내부 workspace 의존성은 `workspace:*`를 사용합니다.
- 새 패키지를 추가하면 `package.json`, `pnpm-lock.yaml`, 필요 시 `pnpm-workspace.yaml`을 함께 갱신합니다.

자세한 기준은 [Package Management](./docs/conventions/package-management.md)을 따릅니다.

## 🤖 AI Harness

> HASHI는 AI와 함께 개발하기 위해 spec, convention, workflow, skill 문서를 함께 관리합니다.

### Docs

- [Coding Convention](./docs/conventions/coding.md)
- [Git Convention](./docs/conventions/git.md)
- [Package Management](./docs/conventions/package-management.md)
- [Agent Skills](./docs/agent/skills.md)
- [Codex Hooks](./docs/agent/hooks.md)
- [Serena MCP](./docs/agent/serena-mcp.md)

### Rules

- [Design System Instructions](./docs/rules/design-system-instructions.md)

### Workflows

- [Local Development](./docs/workflows/local-development.md)
- [PR Checklist](./docs/workflows/pr-checklist.md)
- [Spec Writing](./docs/workflows/spec-writing.md)
- [Spec Templates](./docs/workflows/spec-templates/README.md)
- [Turbo Generators](./docs/workflows/turbo-generators.md)

#### Architecture

<img width="1672" height="941" alt="architecture" src="https://github.com/user-attachments/assets/fecb81dc-0a34-4f42-a502-fddb122ee227" />

- [Tech Stack](./docs/architecture/tech-stack.md)
- [Monorepo](./docs/architecture/monorepo.md)
- [App Structure](./docs/architecture/app-structure.md)
- [Data Layer](./docs/architecture/data-layer.md)
- [Design System](./docs/architecture/design-system.md)
- [Design System Components](./docs/architecture/design-system-components.md)
- [Design System Component Plan](./docs/architecture/design-system-component-plan.md)
- [Design System Icons](./docs/architecture/design-system-icons.md)
- [Styling And Design Tokens](./docs/architecture/styling-and-design-tokens.md)
- [Mobile WebView](./docs/architecture/mobile-webview.md)

---

<img width="7680" height="4320" alt="24  마지막장" src="https://github.com/user-attachments/assets/5c58e290-0a69-492c-9efc-8c3b911504db" />
