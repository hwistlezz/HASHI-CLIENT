<img width="1010" height="316" alt="hashi_logo" src="https://github.com/user-attachments/assets/4ca8bfba-0d37-4b37-90f2-cb549c4874b0" />

## 🍽️ 발견부터 예약까지, 포기 없이 🍽️

### **HASHI**는 한국인 여행자를 위한 일본 맛집 큐레이션 및 예약 에이전트 서비스입니다.

- 일본 여행자가 식당을 발견한 순간부터 실제 방문하는 순간까지의 과정을 하나의 경험으로 연결합니다.

  > 직접 선별한 맛집 큐레이션, 지역별 추천, 테마별 맛집 리스트, 인기 순위 등을 통해 새로운 식당을 발견할 수 있도록 돕고, 발견한 식당은 별도의 플랫폼 이동 없이 바로 예약으로 이어질 수 있습니다.

- 예약이 불가능한 경우에는 비슷한 분위기와 경험을 제공하는 다른 식당을 추천하여 여행자가 식사 경험 자체를 포기하지 않도록 돕습니다.

- 단순히 예약을 대신해주는 서비스가 아니라, 발견부터 예약, 차선책, 리뷰까지 여행자의 식사 경험 전체를 연결하는 올인원 식사 경험 플랫폼입니다.

## ⚒️ Tech Stack

| Area             | Stack                                   |
| ---------------- | --------------------------------------- |
| Package Manager  | pnpm                                    |
| Monorepo         | pnpm workspace, pnpm catalog, Turborepo |
| Language         | React, TypeScript                       |
| Bundler          | Vite                                    |
| Routing          | React Router                            |
| Styling          | Tailwind CSS, class-variance-authority  |
| Design System    | HDS UI, HDS Icons, HDS Tokens           |
| API Client       | ky                                      |
| Server State     | TanStack Query                          |
| Test             | Vitest, Playwright                      |
| UI Docs          | Storybook, Chromatic                    |
| Error Monitoring | Sentry                                  |
| Deploy           | Vercel                                  |

자세한 기술 스택과 버전 기준은 [Tech Stack](./docs/architecture/tech-stack.md)을 따릅니다.

## 📖 Convention

### Coding Convention

- 컴포넌트는 arrow function과 named export를 사용합니다.
- 컴포넌트 파일은 `PascalCase`, 일반 `.ts` 파일과 폴더는 `camelCase`를 사용합니다.
- 의미 없는 `div` 사용을 지양하고 가능한 semantic tag를 사용합니다.
- 버튼 역할은 `button` 요소를 사용하고, 텍스트가 없는 아이콘 버튼에는 `aria-label`을 제공합니다.
- 타입 이름은 `PascalCase`, Props 타입은 `Props` 접미사를 사용합니다.
- 이벤트 핸들러에는 `handle` 접두사를 사용합니다.
- boolean 값은 `is`, `has`, `check` 등의 접두사로 의미를 드러냅니다.
- 스타일은 기본적으로 Tailwind CSS utility class를 사용합니다.
- 반복되는 variant 조합은 `class-variance-authority`의 `cva`와 `VariantProps`를 사용합니다.
- 공통 디자인 값은 HDS token을 우선 사용합니다.

자세한 기준은 [Coding Convention](./docs/conventions/coding.md)을 따릅니다.

### Package Management

- 패키지 매니저는 `pnpm`을 사용합니다.
- `npm`, `yarn`, `bun` lockfile을 추가하지 않습니다.
- 외부 패키지 버전은 `pnpm-workspace.yaml`의 catalog에서 관리합니다.
- 내부 workspace 의존성은 `workspace:*`를 사용합니다.
- 새 패키지를 추가하면 `package.json`, `pnpm-lock.yaml`, 필요 시 `pnpm-workspace.yaml`을 함께 갱신합니다.

자세한 기준은 [Package Management](./docs/conventions/package-management.md)을 따릅니다.

## 🤖 AI

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

### Architecture

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
