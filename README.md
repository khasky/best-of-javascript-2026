# Best of JavaScript

A hand-picked list of **JavaScript** and **TypeScript** tools that matter for serious product work.

> *If I were building, shipping, or maintaining a serious JS/TS product today — what tools are actually worth my attention?*

---

## Table of Contents

- [Best of JavaScript](#best-of-javascript)
  - [Table of Contents](#table-of-contents)
  - [Philosophy](#philosophy)
  - [Companion playbooks](#companion-playbooks)
  - [The Defaults I'd Reach for First](#the-defaults-id-reach-for-first)
  - [Developer Experience \& AI Coding](#developer-experience--ai-coding)
    - [Editors](#editors)
    - [AI coding tools](#ai-coding-tools)
    - [VS Code / Cursor extensions](#vs-code--cursor-extensions)
      - [Must-have](#must-have)
      - [Nice-to-have](#nice-to-have)
  - [Runtimes \& Package Management](#runtimes--package-management)
    - [Runtimes](#runtimes)
    - [Package managers](#package-managers)
    - [Version management](#version-management)
  - [Build, Monorepo \& Release Engineering](#build-monorepo--release-engineering)
    - [Core foundations](#core-foundations)
    - [Builders, compilers, bundlers](#builders-compilers-bundlers)
    - [Monorepos \& release flows](#monorepos--release-flows)
    - [Commit-time hygiene](#commit-time-hygiene)
  - [Frontend \& Full-Stack Frameworks](#frontend--full-stack-frameworks)
    - [Frontend-first](#frontend-first)
    - [Full-stack / app frameworks](#full-stack--app-frameworks)
    - [Backend / edge-friendly frameworks](#backend--edge-friendly-frameworks)
  - [UI, Styling \& Design Systems](#ui-styling--design-systems)
    - [CSS \& styling systems](#css--styling-systems)
    - [Component systems](#component-systems)
    - [Tables \& data grids](#tables--data-grids)
    - [Virtualization \& large lists](#virtualization--large-lists)
    - [Icons \& docs for component work](#icons--docs-for-component-work)
  - [Routing, State, Forms \& Validation](#routing-state-forms--validation)
    - [Routing](#routing)
    - [State management](#state-management)
    - [Server state \& data fetching](#server-state--data-fetching)
    - [Forms \& validation](#forms--validation)
    - [React hooks](#react-hooks)
    - [Localization](#localization)
    - [Dates \& IDs](#dates--ids)
  - [Backend, APIs \& Data](#backend-apis--data)
    - [API layers](#api-layers)
    - [ORMs \& query builders](#orms--query-builders)
    - [Queues, cache, streaming](#queues-cache-streaming)
    - [Email \& notifications](#email--notifications)
    - [GraphQL \& adjacent tools](#graphql--adjacent-tools)
  - [Authentication \& Security](#authentication--security)
    - [Auth](#auth)
    - [Tokens \& credentials](#tokens--credentials)
    - [Sanitization \& frontend security](#sanitization--frontend-security)
    - [SEO \& metadata](#seo--metadata)
  - [Testing \& Code Quality](#testing--code-quality)
    - [Unit \& component testing](#unit--component-testing)
    - [End-to-end \& browser automation](#end-to-end--browser-automation)
    - [Linting, formatting, repo hygiene](#linting-formatting-repo-hygiene)
  - [Content, Docs, Editors \& Media](#content-docs-editors--media)
    - [CMS \& content platforms](#cms--content-platforms)
    - [Documentation](#documentation)
    - [Rich text \& code editing](#rich-text--code-editing)
    - [Files, PDF, uploads, images](#files-pdf-uploads-images)
  - [Infrastructure, Delivery \& Observability](#infrastructure-delivery--observability)
    - [Dev environment \& containers](#dev-environment--containers)
    - [Container orchestration](#container-orchestration)
    - [Hosting \& platforms](#hosting--platforms)
    - [CI/CD](#cicd)
    - [Infrastructure as code \& secrets](#infrastructure-as-code--secrets)
    - [Monitoring, logs \& product visibility](#monitoring-logs--product-visibility)
  - [Cross-Platform Apps](#cross-platform-apps)
    - [Desktop](#desktop)
    - [Mobile](#mobile)
  - [AI / ML for JavaScript Apps](#ai--ml-for-javascript-apps)
    - [LLM app tooling](#llm-app-tooling)
    - [Traditional ML in JS](#traditional-ml-in-js)
  - [Worth Reading](#worth-reading)
  - [License](#license)

---

## Philosophy

A good curated list should do more than collect links. This one tries to:

- favor **defaults over novelty**;
- include **battle-tested tools first**, then interesting challengers;
- prefer tools with strong docs, healthy adoption, and a clear place in a modern stack.

---

## Companion playbooks

These repositories form one playbook suite:

- [Auth & Identity Playbook](https://github.com/khasky/auth-identity-playbook) — sessions, tokens, OAuth, and identity boundaries across the stack
- [Backend Architecture Playbook](https://github.com/khasky/backend-architecture-playbook) — APIs, boundaries, OpenAPI, persistence, and errors
- **Best of JavaScript** — curated JS/TS tooling and stack defaults
- [Caching Playbook](https://github.com/khasky/caching-playbook) — HTTP, CDN, and application caches; consistency and invalidation
- [Code Review Playbook](https://github.com/khasky/code-review-playbook) — PR quality, ownership, and review culture
- [DevOps Delivery Playbook](https://github.com/khasky/devops-delivery-playbook) — CI/CD, environments, rollout safety, and observability
- [Engineering Lead Playbook](https://github.com/khasky/engineering-lead-playbook) — standards, RFCs, and technical leadership habits
- [Frontend Architecture Playbook](https://github.com/khasky/frontend-architecture-playbook) — React structure, performance, and consuming API contracts
- [Marketing and SEO Playbook](https://github.com/khasky/marketing-and-seo-playbook) — growth, SEO, experimentation, and marketing surfaces
- [Monorepo Architecture Playbook](https://github.com/khasky/monorepo-architecture-playbook) — workspaces, package boundaries, and shared code at scale
- [Node.js Runtime & Performance Playbook](https://github.com/khasky/nodejs-runtime-performance-playbook) — event loop, streams, memory, and production Node performance
- [Testing Strategy Playbook](https://github.com/khasky/testing-strategy-playbook) — unit, integration, contract, E2E, and CI-friendly test layers

---

## The Defaults I'd Reach for First

If I were starting a modern JS/TS project today, I would usually begin with something close to this:

- **Editor / AI:** [Cursor](https://cursor.com/) or [VS Code](https://code.visualstudio.com/) + [Claude Code](https://www.anthropic.com/claude-code) or [Codex](https://chatgpt.com/codex)
- **Runtime / package manager:** [Node.js](https://nodejs.org/) + [pnpm](https://pnpm.io/)
- **Language / build:** [TypeScript](https://www.typescriptlang.org/) + [Vite](https://vite.dev/)
- **Frontend:** [React](https://react.dev/) or [Astro](https://astro.build/) depending on dynamic vs static
- **Full-stack:** [Next.js](https://nextjs.org/) for React-heavy apps, [Hono](https://hono.dev/) or [Fastify](https://fastify.io/) for lean APIs
- **Forms & validation:** [React Hook Form](https://react-hook-form.com/) + [Zod](https://zod.dev/)
- **Server state:** [TanStack Query](https://tanstack.com/query)
- **Database:** [Drizzle ORM](https://orm.drizzle.team/) or [Prisma](https://www.prisma.io/)
- **Auth:** [Better Auth](https://www.better-auth.com/) or [Auth.js](https://authjs.dev/) depending on self-hosted vs ecosystem fit
- **Testing:** [Vitest](https://vitest.dev/) + [Playwright](https://playwright.dev/)
- **Code quality:** [Biome](https://biomejs.dev/) or [ESLint](https://eslint.org/) + [Prettier](https://prettier.io/)
- **UI:** [Tailwind CSS](https://tailwindcss.com/) + [shadcn/ui](https://ui.shadcn.com/) or [Material UI](https://mui.com/)
- **Tables & virtualization:** [TanStack Table](https://tanstack.com/table) + [TanStack Virtual](https://tanstack.com/virtual), or [react-virtuoso](https://virtuoso.dev/) when you want richer list primitives out of the box
- **Hosting:** [Vercel](https://vercel.com/) for Next.js-heavy apps, [Cloudflare](https://www.cloudflare.com/) for edge-first apps, [Railway](https://railway.com/) or [Render](https://render.com/) for simple full-stack deployments
- **Pipelines:** [GitHub Actions](https://github.com/features/actions) or [GitLab CI/CD](https://gitlab.com)

---

## Developer Experience & AI Coding

### Editors

- [Cursor](https://cursor.com/) — The strongest all-around AI-native editor pick for many JS/TS teams today.
- [Visual Studio Code](https://code.visualstudio.com/) — Still the universal baseline editor with the broadest extension ecosystem.

### AI coding tools

- [Claude Code](https://www.anthropic.com/claude-code) — One of the strongest coding agents for repository-aware implementation, refactors, and terminal-heavy workflows.
- [Codex](https://chatgpt.com/codex) — Worth using when you want cloud-executed coding tasks tied to GitHub workflows.
- [Gemini](https://gemini.google.com/) — Worth considering when you want a strong general-purpose coding assistant with a large context window and multimodal strengths.

### VS Code / Cursor extensions

These all work naturally in VS Code, and the same extension ecosystem is one of Cursor's practical advantages too.

#### Must-have

- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) — Still the best overall Git extension for understanding blame, history, and changes without leaving the editor.
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) — Still the most important extension when your repo relies on ESLint for fast feedback and autofix.
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) — The obvious formatter extension when your team is still on Prettier rather than Biome-only workflows.
- [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens) — One of the fastest ways to notice lint and TypeScript problems without constantly opening the problems panel.
- [Pretty TypeScript Errors](https://marketplace.visualstudio.com/items?itemName=yoavbls.pretty-ts-errors) — Makes complex TypeScript diagnostics much more readable in everyday work.
- [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss) — A must-have if you write Tailwind regularly and want class completion, previews, and validation.
- [Playwright Test for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright) — One of the most useful testing extensions in the JS ecosystem thanks to run/debug integration, locator tools, and trace support.
- [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) — The strongest fully free in-editor default for HTTP, GraphQL, and `.http`-file-based API workflows in VS Code or Cursor.
- [Prisma](https://marketplace.visualstudio.com/items?itemName=prisma.prisma) — Essential if your stack uses Prisma, adding schema autocomplete, diagnostics, formatting, and better database-model navigation.

#### Nice-to-have

- [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark) — A popular default theme if you want a proven, easy-on-the-eyes setup.
- [JavaScript and TypeScript Nightly](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next) — Great when you want newer TypeScript language-service improvements before they fully land in stable editor builds.
- [npm IntelliSense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense) — Small but genuinely useful import autocomplete for package-heavy Node and frontend repos.
- [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode) — Still useful if you want lightweight AI-assisted completion without depending entirely on external coding agents.
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) — Tiny extension, big quality-of-life win when editing JSX, HTML, and component templates.
- [Highlight Matching Tag](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag) — Makes nested markup easier to scan in large React or template files.
- [CSS Peek](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek) — Handy when you still work in CSS or CSS Modules and want quick selector navigation.
- [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight) — Simple visual feedback that is still useful in CSS-heavy frontend work.
- [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) — Makes deeply nested JSX, config, and JSON files easier to parse at a glance.
- [SVG](https://marketplace.visualstudio.com/items?itemName=jock.svg) — Nice quality-of-life extension when frontend repos frequently include inline or asset-based SVG work.
- [Version Lens](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens) — Very useful in dependency-heavy JS repos when you want package version drift to be visible in `package.json`.
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) — Great for README-heavy repos, docs work, and faster markdown editing.
- [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) — Worth using when built-in markdown preview is not enough for docs-heavy workflows.
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) — The obvious markdown quality extension when your project treats docs as first-class output.
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight) — Simple but still useful for scanning unfinished work in large codebases.
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) — Still one of the most practical extensions when your app ships with containers.
- [Kubernetes](https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-kubernetes-tools) — Useful once your stack actually touches Kubernetes, though not a must-have for every JavaScript project.

---

## Runtimes & Package Management

### Runtimes

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Node.js](https://nodejs.org/) | The default runtime for most production JavaScript backends. | — |
| [Bun](https://bun.com/) | Fast, ambitious, and increasingly credible as a runtime + package manager + test runner + bundler. | — |
| [Deno](https://deno.com/) | Clean developer experience, modern defaults, and a thoughtful runtime model. | — |
| [Cloudflare Workers](https://developers.cloudflare.com/workers/) | A serious edge runtime, not just a niche deployment target anymore. | — |

### Package managers

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [pnpm](https://pnpm.io/) | My default recommendation for most teams, especially monorepos. | ![GitHub Repo stars](https://img.shields.io/github/stars/pnpm/pnpm?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/pnpm?style=flat-square&logo=npm&label=npm%2Fweek) |
| [npm](https://www.npmjs.com/) | The universal baseline that works everywhere. | ![GitHub Repo stars](https://img.shields.io/github/stars/npm/cli?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/npm?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Bun Package Manager](https://bun.com/docs/pm/cli/install) | Worth trying when you want one binary for install, scripts, and runtime. | — |

### Version management

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [nvm](https://github.com/nvm-sh/nvm) | Still the familiar choice for switching Node versions. | — |
| [Volta](https://volta.sh/) | Excellent when you want per-project tool pinning with less shell friction. | — |

---

## Build, Monorepo & Release Engineering

### Core foundations

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [TypeScript](https://www.typescriptlang.org/) | The language layer most serious JS projects now assume. | ![GitHub Repo stars](https://img.shields.io/github/stars/microsoft/TypeScript?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/typescript?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TypeScript Project References](https://www.typescriptlang.org/docs/handbook/project-references.html) | Important once your repo starts growing sideways. | — |
| [Vite](https://vite.dev/) | The best general-purpose starting point for modern frontend apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/vitejs/vite?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/vite?style=flat-square&logo=npm&label=npm%2Fweek) |

### Builders, compilers, bundlers

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Vite](https://vite.dev/) | Still the best default for most new frontend apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/vitejs/vite?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/vite?style=flat-square&logo=npm&label=npm%2Fweek) |
| [esbuild](https://esbuild.github.io/) | Extremely fast and still one of the best "get out of my way" tools. | ![GitHub Repo stars](https://img.shields.io/github/stars/evanw/esbuild?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/esbuild?style=flat-square&logo=npm&label=npm%2Fweek) |
| [SWC](https://swc.rs/) | Great when you want speed plus compiler-oriented extensibility. | ![GitHub Repo stars](https://img.shields.io/github/stars/swc-project/swc?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40swc%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Rspack](https://rspack.dev/) | Strong option when you want webpack-compatible ergonomics with much faster Rust-backed performance. | ![GitHub Repo stars](https://img.shields.io/github/stars/web-infra-dev/rspack?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40rspack%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Turbopack](https://turbo.build/pack) | Fast and strategically important in the Next.js world, though still more opinionated than Vite. | — |
| [Rollup](https://rollupjs.org/) | Still excellent for library builds. | ![GitHub Repo stars](https://img.shields.io/github/stars/rollup/rollup?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/rollup?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Rolldown](https://rolldown.rs/) | One of the most important emerging build tools to watch, especially around the Vite ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/rolldown/rolldown?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/rolldown?style=flat-square&logo=npm&label=npm%2Fweek) |
| [webpack](https://webpack.js.org/) | Not the default for new projects anymore, but still everywhere in real codebases. | ![GitHub Repo stars](https://img.shields.io/github/stars/webpack/webpack?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/webpack?style=flat-square&logo=npm&label=npm%2Fweek) |

### Monorepos & release flows

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Turborepo](https://turbo.build/repo) | Strong fit for frontend-heavy monorepos and fast incremental builds. | ![GitHub Repo stars](https://img.shields.io/github/stars/vercel/turborepo?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/turbo?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Nx](https://nx.dev/) | Excellent when you want deeper workspace tooling and bigger-team structure. | ![GitHub Repo stars](https://img.shields.io/github/stars/nrwl/nx?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/nx?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Changesets](https://github.com/changesets/changesets) | Versioning and changelog sanity for package-based repos. | ![GitHub Repo stars](https://img.shields.io/github/stars/changesets/changesets?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40changesets%2Fcli?style=flat-square&logo=npm&label=npm%2Fweek) |

### Commit-time hygiene

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Husky](https://typicode.github.io/husky/) | Git hooks with minimal drama. | ![GitHub Repo stars](https://img.shields.io/github/stars/typicode/husky?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/husky?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Lefthook](https://github.com/evilmartians/lefthook) | Very fast alternative, especially nice in bigger repos. | ![GitHub Repo stars](https://img.shields.io/github/stars/evilmartians/lefthook?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/lefthook?style=flat-square&logo=npm&label=npm%2Fweek) |
| [commitlint](https://commitlint.js.org/) | Useful when commit conventions actually matter in your release process. | ![GitHub Repo stars](https://img.shields.io/github/stars/conventional-changelog/commitlint?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40commitlint%2Fcli?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Frontend & Full-Stack Frameworks

### Frontend-first

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [React](https://react.dev/) | The ecosystem center of gravity. | ![GitHub Repo stars](https://img.shields.io/github/stars/facebook/react?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Vue](https://vuejs.org/) | Excellent developer experience and a strong all-in-one ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/vuejs/core?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/vue?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Svelte](https://svelte.dev/) | Still one of the cleanest authoring experiences in UI development. | ![GitHub Repo stars](https://img.shields.io/github/stars/sveltejs/svelte?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/svelte?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Solid](https://www.solidjs.com/) | Great when you want fine-grained reactivity and a different mental model from React. | ![GitHub Repo stars](https://img.shields.io/github/stars/solidjs/solid?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/solid-js?style=flat-square&logo=npm&label=npm%2Fweek) |

### Full-stack / app frameworks

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Next.js](https://nextjs.org/) | Still the default full-stack React framework for many teams. | ![GitHub Repo stars](https://img.shields.io/github/stars/vercel/next.js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/next?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Astro](https://astro.build/) | A standout choice for content-driven sites, docs, marketing pages, and hybrid content/app builds. | ![GitHub Repo stars](https://img.shields.io/github/stars/withastro/astro?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/astro?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Nuxt](https://nuxt.com/) | The obvious full-stack default if your team prefers Vue. | ![GitHub Repo stars](https://img.shields.io/github/stars/nuxt/nuxt?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/nuxt?style=flat-square&logo=npm&label=npm%2Fweek) |
| [SvelteKit](https://kit.svelte.dev/) | Great full-stack option if you are already in the Svelte world. | ![GitHub Repo stars](https://img.shields.io/github/stars/sveltejs/kit?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40sveltejs%2Fkit?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Remix](https://remix.run/) | Worth knowing for web-native routing and form-first thinking. | ![GitHub Repo stars](https://img.shields.io/github/stars/remix-run/remix?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40remix-run%2Freact?style=flat-square&logo=npm&label=npm%2Fweek) |

### Backend / edge-friendly frameworks

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Hono](https://hono.dev/) | One of the best modern defaults when you want edge-friendly or multi-runtime APIs. | ![GitHub Repo stars](https://img.shields.io/github/stars/honojs/hono?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/hono?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Fastify](https://fastify.io/) | A great default for Node APIs when you want speed and structure without a framework tax. | ![GitHub Repo stars](https://img.shields.io/github/stars/fastify/fastify?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/fastify?style=flat-square&logo=npm&label=npm%2Fweek) |
| [NestJS](https://nestjs.com/) | Strong fit for enterprise teams that like architecture, modules, decorators, and convention. | ![GitHub Repo stars](https://img.shields.io/github/stars/nestjs/nest?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40nestjs%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Express](https://expressjs.com/) | Old, familiar, and still absolutely alive in existing codebases. | ![GitHub Repo stars](https://img.shields.io/github/stars/expressjs/express?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/express?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## UI, Styling & Design Systems

### CSS & styling systems

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Tailwind CSS](https://tailwindcss.com/) | Still the most widely adopted utility-first styling system in modern JS apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/tailwindlabs/tailwindcss?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/tailwindcss?style=flat-square&logo=npm&label=npm%2Fweek) |
| [vanilla-extract](https://vanilla-extract.style/) | Great when you want typed, file-based styles without runtime overhead. | ![GitHub Repo stars](https://img.shields.io/github/stars/vanilla-extract-css/vanilla-extract?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40vanilla-extract%2Fcss?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Panda CSS](https://panda-css.com/) | Worth a look if you want design-token-driven styling with static extraction. | ![GitHub Repo stars](https://img.shields.io/github/stars/chakra-ui/panda?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40pandacss%2Fdev?style=flat-square&logo=npm&label=npm%2Fweek) |

### Component systems

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [shadcn/ui](https://ui.shadcn.com/) | A very practical starting point for teams that want ownership over their components. | ![GitHub Repo stars](https://img.shields.io/github/stars/shadcn-ui/ui?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/shadcn?style=flat-square&logo=npm&label=npm%2Fweek) |
| [daisyUI](https://daisyui.com/) | A fast, pragmatic Tailwind component layer when you want to ship styled UI without building every primitive yourself. | ![GitHub Repo stars](https://img.shields.io/github/stars/saadeghi/daisyui?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/daisyui?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Radix UI](https://www.radix-ui.com/) | Accessible unstyled primitives that play well with real design systems. | ![GitHub Repo stars](https://img.shields.io/github/stars/radix-ui/primitives?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40radix-ui%2Freact-slot?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Mantine](https://mantine.dev/) | One of the nicest batteries-included React UI kits. | ![GitHub Repo stars](https://img.shields.io/github/stars/mantinedev/mantine?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40mantine%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Material UI](https://mui.com/) | Still common in enterprise products and dashboard-heavy apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/mui/material-ui?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40mui%2Fmaterial?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Chakra UI](https://www.chakra-ui.com/) | Friendly ergonomics and a coherent component model. | ![GitHub Repo stars](https://img.shields.io/github/stars/chakra-ui/chakra-ui?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40chakra-ui%2Freact?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Ant Design](https://ant.design/) | Still a major option for business applications and data-dense interfaces. | ![GitHub Repo stars](https://img.shields.io/github/stars/ant-design/ant-design?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/antd?style=flat-square&logo=npm&label=npm%2Fweek) |

### Tables & data grids

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [TanStack Table](https://tanstack.com/table) | The headless default when you want powerful table logic, full markup control, and a good fit with the wider TanStack ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/TanStack/table?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tanstack%2Freact-table?style=flat-square&logo=npm&label=npm%2Fweek) |
| [AG Grid](https://www.ag-grid.com/) | The feature-rich grid to know for data-heavy products, especially when Excel-like behavior, enterprise features, or very large datasets matter. | ![GitHub Repo stars](https://img.shields.io/github/stars/ag-grid/ag-grid?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ag-grid-community?style=flat-square&logo=npm&label=npm%2Fweek) |
| [MUI X Data Grid](https://mui.com/x/react-data-grid/) | Strong choice when a React dashboard already uses Material UI and wants a polished component with sorting, filtering, pagination, and virtualization. | ![GitHub Repo stars](https://img.shields.io/github/stars/mui/mui-x?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40mui%2Fx-data-grid?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-data-grid](https://github.com/Comcast/react-data-grid) | Practical React grid for editable, spreadsheet-style tables without taking on the full AG Grid surface area. | ![GitHub Repo stars](https://img.shields.io/github/stars/Comcast/react-data-grid?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-data-grid?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Handsontable](https://handsontable.com/) | Best known for spreadsheet-like editing, copy/paste workflows, formulas, and dense business-data interfaces. | ![GitHub Repo stars](https://img.shields.io/github/stars/handsontable/handsontable?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/handsontable?style=flat-square&logo=npm&label=npm%2Fweek) |

### Virtualization & large lists

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [TanStack Virtual](https://tanstack.com/virtual) | Headless, framework-agnostic virtualization for custom lists, grids, tables, and scroll behavior with minimal UI opinions. | ![GitHub Repo stars](https://img.shields.io/github/stars/TanStack/virtual?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tanstack%2Freact-virtual?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-virtuoso](https://virtuoso.dev/) | The pragmatic React default when you want dynamic heights, grouped lists, sticky headers, tables, and infinite scroll with less wiring. | ![GitHub Repo stars](https://img.shields.io/github/stars/petyosi/react-virtuoso?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-virtuoso?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-window](https://github.com/bvaughn/react-window) | Still common and tiny for simple fixed-size list virtualization, but more of a maintenance choice than a new-project default. | ![GitHub Repo stars](https://img.shields.io/github/stars/bvaughn/react-window?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-window?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-virtualized](https://github.com/bvaughn/react-virtualized) | Important legacy option for older React apps with large lists and grids, though heavier and less attractive for greenfield work. | ![GitHub Repo stars](https://img.shields.io/github/stars/bvaughn/react-virtualized?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-virtualized?style=flat-square&logo=npm&label=npm%2Fweek) |

### Icons & docs for component work

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [lucide](https://lucide.dev/) | Clean icon set and one of the easiest defaults for modern UIs. | ![GitHub Repo stars](https://img.shields.io/github/stars/lucide-icons/lucide?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/lucide-react?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-icons](https://react-icons.github.io/react-icons/) | Useful when you need breadth more than purity. | ![GitHub Repo stars](https://img.shields.io/github/stars/react-icons/react-icons?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-icons?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Storybook](https://storybook.js.org/) | Still the standard workshop for components, states, and design-system documentation. | ![GitHub Repo stars](https://img.shields.io/github/stars/storybookjs/storybook?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/storybook?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Routing, State, Forms & Validation

### Routing

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [React Router](https://reactrouter.com/) | The classic, still important. | ![GitHub Repo stars](https://img.shields.io/github/stars/remix-run/react-router?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-router?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TanStack Router](https://tanstack.com/router) | A strong modern choice if type-safe routing matters to you. | ![GitHub Repo stars](https://img.shields.io/github/stars/TanStack/router?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tanstack%2Freact-router?style=flat-square&logo=npm&label=npm%2Fweek) |

### State management

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Zustand](https://zustand.docs.pmnd.rs/) | Lightweight, minimal, and a great default for many React apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/pmndrs/zustand?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/zustand?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Redux Toolkit](https://redux-toolkit.js.org/) | Still the right answer when state complexity is real and long-lived. | ![GitHub Repo stars](https://img.shields.io/github/stars/reduxjs/redux-toolkit?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40reduxjs%2Ftoolkit?style=flat-square&logo=npm&label=npm%2Fweek) |
| [XState](https://stately.ai/docs/xstate) | Best when your problem is workflow complexity, not just state storage. | ![GitHub Repo stars](https://img.shields.io/github/stars/statelyai/xstate?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/xstate?style=flat-square&logo=npm&label=npm%2Fweek) |

### Server state & data fetching

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [TanStack Query](https://tanstack.com/query) | The default recommendation for async server-state management. | ![GitHub Repo stars](https://img.shields.io/github/stars/TanStack/query?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tanstack%2Freact-query?style=flat-square&logo=npm&label=npm%2Fweek) |
| [SWR](https://swr.vercel.app/) | Still elegant for simpler React data-fetching patterns. | ![GitHub Repo stars](https://img.shields.io/github/stars/vercel/swr?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/swr?style=flat-square&logo=npm&label=npm%2Fweek) |
| [axios](https://axios-http.com/) | Popular and familiar; still useful, even in a fetch-first world. | ![GitHub Repo stars](https://img.shields.io/github/stars/axios/axios?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/axios?style=flat-square&logo=npm&label=npm%2Fweek) |
| [ky](https://github.com/sindresorhus/ky) | Small, modern, pleasant fetch wrapper. | ![GitHub Repo stars](https://img.shields.io/github/stars/sindresorhus/ky?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ky?style=flat-square&logo=npm&label=npm%2Fweek) |

### Forms & validation

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [React Hook Form](https://react-hook-form.com/) | The best default for most React forms. | ![GitHub Repo stars](https://img.shields.io/github/stars/react-hook-form/react-hook-form?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-hook-form?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TanStack Form](https://tanstack.com/form) | Strong modern alternative when you want deeper type inference or are already committed to the TanStack ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/TanStack/form?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tanstack%2Freact-form?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Zod](https://zod.dev/) | The current center of gravity for TypeScript-first schema validation. | ![GitHub Repo stars](https://img.shields.io/github/stars/colinhacks/zod?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/zod?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Ajv](https://ajv.js.org/) | Great when JSON Schema is the right abstraction. | ![GitHub Repo stars](https://img.shields.io/github/stars/ajv-validator/ajv?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ajv?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Joi](https://joi.dev/) | Still useful in backend and validation-heavy codebases. | ![GitHub Repo stars](https://img.shields.io/github/stars/hapijs/joi?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/joi?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Yup](https://github.com/jquense/yup) | Common in older React form stacks, but less of a new-project default now. | ![GitHub Repo stars](https://img.shields.io/github/stars/jquense/yup?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/yup?style=flat-square&logo=npm&label=npm%2Fweek) |

### React hooks

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [usehooks-ts](https://usehooks-ts.com/) | The strongest TypeScript-first default when you want a practical set of reusable React hooks. | ![GitHub Repo stars](https://img.shields.io/github/stars/juliencrn/usehooks-ts?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/usehooks-ts?style=flat-square&logo=npm&label=npm%2Fweek) |
| [ahooks](https://ahooks.js.org/) | Great when you want a broader, more enterprise-shaped hooks toolkit. | ![GitHub Repo stars](https://img.shields.io/github/stars/alibaba/hooks?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ahooks?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-use](https://github.com/streamich/react-use) | Still a useful grab-bag of hooks, especially in older or utility-heavy React codebases. | ![GitHub Repo stars](https://img.shields.io/github/stars/streamich/react-use?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-use?style=flat-square&logo=npm&label=npm%2Fweek) |

### Localization

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [react-i18next](https://react.i18next.com/) | Still the safest default when a React app needs serious localization. | ![GitHub Repo stars](https://img.shields.io/github/stars/i18next/react-i18next?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-i18next?style=flat-square&logo=npm&label=npm%2Fweek) |

### Dates & IDs

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [date-fns](https://date-fns.org/) | The best general-purpose date utility default for most JavaScript and TypeScript apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/date-fns/date-fns?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/date-fns?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Day.js](https://day.js.org/) | A lightweight alternative when you want a smaller Moment-like API surface. | ![GitHub Repo stars](https://img.shields.io/github/stars/iamkun/dayjs?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/dayjs?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Luxon](https://moment.github.io/luxon/) | Strong choice when timezone-heavy date handling matters more than minimal bundle size. | ![GitHub Repo stars](https://img.shields.io/github/stars/moment/luxon?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/luxon?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Temporal](https://tc39.es/proposal-temporal/docs/) | The long-term native direction for safer date and time handling in JavaScript. | — |
| [nanoid](https://github.com/ai/nanoid) | My default pick for compact, modern ID generation. | ![GitHub Repo stars](https://img.shields.io/github/stars/ai/nanoid?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/nanoid?style=flat-square&logo=npm&label=npm%2Fweek) |
| [uuid](https://github.com/uuidjs/uuid) | Still the standard option when interoperability and familiar UUID formats matter. | ![GitHub Repo stars](https://img.shields.io/github/stars/uuidjs/uuid?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/uuid?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Backend, APIs & Data

### API layers

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Hono](https://hono.dev/) | Lean, modern, edge-friendly, and increasingly hard to ignore. | ![GitHub Repo stars](https://img.shields.io/github/stars/honojs/hono?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/hono?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Fastify](https://fastify.io/) | Excellent for structured Node APIs. | ![GitHub Repo stars](https://img.shields.io/github/stars/fastify/fastify?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/fastify?style=flat-square&logo=npm&label=npm%2Fweek) |
| [NestJS](https://nestjs.com/) | Strong for teams that want architecture spelled out. | ![GitHub Repo stars](https://img.shields.io/github/stars/nestjs/nest?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40nestjs%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Express](https://expressjs.com/) | Still important to know because so much Node infrastructure and legacy code still assumes it. | ![GitHub Repo stars](https://img.shields.io/github/stars/expressjs/express?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/express?style=flat-square&logo=npm&label=npm%2Fweek) |
| [tRPC](https://trpc.io/) | Worth evaluating when you want end-to-end TypeScript without hand-written API clients. | ![GitHub Repo stars](https://img.shields.io/github/stars/trpc/trpc?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40trpc%2Fserver?style=flat-square&logo=npm&label=npm%2Fweek) |

When the contract is **OpenAPI** and the client is **React + TypeScript**, generate types (and optionally clients) instead of duplicating shapes by hand — this lines up with the [backend](https://github.com/khasky/backend-architecture-playbook) and [frontend](https://github.com/khasky/frontend-architecture-playbook) playbooks:

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [openapi-typescript](https://github.com/drwpow/openapi-typescript) | Types from OpenAPI; works well with hand-written `fetch` or TanStack Query. | ![GitHub Repo stars](https://img.shields.io/github/stars/drwpow/openapi-typescript?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/openapi-typescript?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Hey API OpenAPI TS](https://github.com/hey-api/openapi-ts) | Codegen for clients and types with active maintenance. | ![GitHub Repo stars](https://img.shields.io/github/stars/hey-api/openapi-ts?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40hey-api%2Fopenapi-ts?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Orval](https://orval.dev/) | OpenAPI → clients, mocks, and hooks (including TanStack Query). | ![GitHub Repo stars](https://img.shields.io/github/stars/orval-labs/orval?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/orval?style=flat-square&logo=npm&label=npm%2Fweek) |

### ORMs & query builders

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Prisma](https://www.prisma.io/) | Still one of the best choices for productivity and onboarding speed. | ![GitHub Repo stars](https://img.shields.io/github/stars/prisma/prisma?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/prisma?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Drizzle ORM](https://orm.drizzle.team/) | One of the strongest choices when you want SQL closer to the surface. | ![GitHub Repo stars](https://img.shields.io/github/stars/drizzle-team/drizzle-orm?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/drizzle-orm?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Kysely](https://kysely.dev/) | Great when you want type-safe SQL query building without a full ORM. | ![GitHub Repo stars](https://img.shields.io/github/stars/kysely-org/kysely?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/kysely?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Knex](https://knexjs.org/) | Old but still useful in many backend projects. | ![GitHub Repo stars](https://img.shields.io/github/stars/knex/knex?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/knex?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Mongoose](https://mongoosejs.com/) | Still the obvious entry in MongoDB-heavy Node stacks. | ![GitHub Repo stars](https://img.shields.io/github/stars/Automattic/mongoose?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/mongoose?style=flat-square&logo=npm&label=npm%2Fweek) |

### Queues, cache, streaming

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [BullMQ](https://bullmq.io/) | The default queueing choice for many Redis-backed Node systems. | ![GitHub Repo stars](https://img.shields.io/github/stars/taskforcesh/bullmq?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/bullmq?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Redis for JavaScript](https://github.com/redis/node-redis) | Standard Redis client for Node. | ![GitHub Repo stars](https://img.shields.io/github/stars/redis/node-redis?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/redis?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Apache Kafka](https://kafka.apache.org/) | Still the heavyweight event-streaming answer when scale and durability matter. | — |
| [RabbitMQ](https://www.rabbitmq.com/) | Worth knowing where traditional messaging patterns are a better fit than event logs. | — |
| [Amazon SQS](https://aws.amazon.com/sqs/) | Boring in the best possible way for many cloud-native job pipelines. | — |

### Email & notifications

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Nodemailer](https://nodemailer.com/) | Still the practical default when you need to send email directly from Node services. | ![GitHub Repo stars](https://img.shields.io/github/stars/nodemailer/nodemailer?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/nodemailer?style=flat-square&logo=npm&label=npm%2Fweek) |

### GraphQL & adjacent tools

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Apollo Client](https://www.apollographql.com/docs/react/) | Still important if your frontend lives in GraphQL. | ![GitHub Repo stars](https://img.shields.io/github/stars/apollographql/apollo-client?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40apollo%2Fclient?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Relay](https://relay.dev/) | Worth it when you want serious GraphQL discipline. | ![GitHub Repo stars](https://img.shields.io/github/stars/facebook/relay?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-relay?style=flat-square&logo=npm&label=npm%2Fweek) |
| [GraphQL](https://graphql.org/) | Not a default for everything, but still the right tool in some domains. | ![GitHub Repo stars](https://img.shields.io/github/stars/graphql/graphql-js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/graphql?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Authentication & Security

### Auth

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Better Auth](https://www.better-auth.com/) | One of the strongest new defaults for TypeScript-first, self-hosted authentication. | ![GitHub Repo stars](https://img.shields.io/github/stars/better-auth/better-auth?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/better-auth?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Auth.js](https://authjs.dev/) | Still a very practical choice, especially in the Next.js ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/nextauthjs/next-auth?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/next-auth?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Clerk](https://clerk.com/) | Worth considering when a managed auth platform is the right tradeoff. | ![GitHub Repo stars](https://img.shields.io/github/stars/clerk/javascript?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40clerk%2Fnextjs?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Passport](https://www.passportjs.org/) | Old, flexible, and still found everywhere in established Node apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/jaredhanson/passport?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/passport?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Lucia](https://lucia-auth.com/) | More notable as a minimalist approach and reference point than as the obvious default for new apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/lucia-auth/lucia?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/lucia?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Amazon Cognito](https://aws.amazon.com/cognito/) | Useful when managed identity is the right tradeoff. | — |

### Tokens & credentials

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) | The familiar JWT implementation everyone has seen. | ![GitHub Repo stars](https://img.shields.io/github/stars/auth0/node-jsonwebtoken?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/jsonwebtoken?style=flat-square&logo=npm&label=npm%2Fweek) |
| [paseto](https://github.com/panva/paseto) | Worth knowing when you want a stronger alternative to raw JWT habits. | ![GitHub Repo stars](https://img.shields.io/github/stars/panva/paseto?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/paseto?style=flat-square&logo=npm&label=npm%2Fweek) |
| [argon2](https://github.com/ranisalt/node-argon2) | A better modern default for new password-hashing code than older bcrypt habits. | ![GitHub Repo stars](https://img.shields.io/github/stars/ranisalt/node-argon2?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/argon2?style=flat-square&logo=npm&label=npm%2Fweek) |
| [bcrypt.js](https://github.com/dcodeIO/bcrypt.js) | Still extremely common, but more of a compatibility choice than the best new-project default. | ![GitHub Repo stars](https://img.shields.io/github/stars/dcodeIO/bcrypt.js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/bcryptjs?style=flat-square&logo=npm&label=npm%2Fweek) |

### Sanitization & frontend security

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [DOMPurify](https://github.com/cure53/DOMPurify) | The obvious default for sanitizing HTML in frontend contexts. | ![GitHub Repo stars](https://img.shields.io/github/stars/cure53/DOMPurify?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/dompurify?style=flat-square&logo=npm&label=npm%2Fweek) |
| [sanitize-html](https://github.com/apostrophecms/sanitize-html) | Good when you need configurable HTML sanitization. | ![GitHub Repo stars](https://img.shields.io/github/stars/apostrophecms/sanitize-html?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/sanitize-html?style=flat-square&logo=npm&label=npm%2Fweek) |

### SEO & metadata

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [react-helmet-async](https://github.com/staylor/react-helmet-async) | The safer React-era replacement for `react-helmet` in SPA-style apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/staylor/react-helmet-async?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-helmet-async?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Testing & Code Quality

### Unit & component testing

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Vitest](https://vitest.dev/) | The best default for modern Vite-flavored JS/TS projects. | ![GitHub Repo stars](https://img.shields.io/github/stars/vitest-dev/vitest?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/vitest?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Jest](https://jestjs.io/) | Still important, especially in large existing codebases. | ![GitHub Repo stars](https://img.shields.io/github/stars/jestjs/jest?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/jest?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Node Test Runner](https://nodejs.org/api/test.html) | Worth watching when you want a built-in, dependency-light testing baseline. | — |
| [bun test](https://bun.com/docs/cli/test) | Increasingly interesting if your stack is already Bun-first. | — |
| [Testing Library](https://testing-library.com/) | The right mental model for UI tests in most apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/testing-library/react-testing-library?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40testing-library%2Freact?style=flat-square&logo=npm&label=npm%2Fweek) |
| [MSW](https://mswjs.io/) | Excellent for API mocking without contaminating your components. | ![GitHub Repo stars](https://img.shields.io/github/stars/mswjs/msw?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/msw?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Supertest](https://github.com/ladjs/supertest) | Still a simple and effective way to test HTTP servers. | ![GitHub Repo stars](https://img.shields.io/github/stars/ladjs/supertest?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/supertest?style=flat-square&logo=npm&label=npm%2Fweek) |

### End-to-end & browser automation

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Playwright](https://playwright.dev/) | The current default recommendation for serious end-to-end browser testing. | ![GitHub Repo stars](https://img.shields.io/github/stars/microsoft/playwright?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/playwright?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Cypress](https://www.cypress.io/) | Still widely used and worth knowing well, especially in existing suites. | ![GitHub Repo stars](https://img.shields.io/github/stars/cypress-io/cypress?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/cypress?style=flat-square&logo=npm&label=npm%2Fweek) |
| [BrowserStack](https://www.browserstack.com/) | Useful when cross-browser reality needs to be tested on actual infrastructure. | — |
| [Sauce Labs](https://saucelabs.com/) | Another established option for broader browser/device coverage. | — |

### Linting, formatting, repo hygiene

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Biome](https://biomejs.dev/) | Fast, modern, and increasingly compelling as a formatter + linter combo. | ![GitHub Repo stars](https://img.shields.io/github/stars/biomejs/biome?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40biomejs%2Fbiome?style=flat-square&logo=npm&label=npm%2Fweek) |
| [ESLint](https://eslint.org/) | Still the standard linting tool most teams know and trust. | ![GitHub Repo stars](https://img.shields.io/github/stars/eslint/eslint?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/eslint?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Prettier](https://prettier.io/) | Still the default formatter in countless repos. | ![GitHub Repo stars](https://img.shields.io/github/stars/prettier/prettier?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/prettier?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Oxlint / Oxc](https://oxc.rs/) | Worth tracking as an ultra-fast linting layer, especially in CI-heavy repos. | ![GitHub Repo stars](https://img.shields.io/github/stars/oxc-project/oxc?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/oxlint?style=flat-square&logo=npm&label=npm%2Fweek) |
| [lint-staged](https://github.com/lint-staged/lint-staged) | Simple, effective pre-commit filtering. | ![GitHub Repo stars](https://img.shields.io/github/stars/lint-staged/lint-staged?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/lint-staged?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Content, Docs, Editors & Media

### CMS & content platforms

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Payload](https://payloadcms.com/) | One of the most compelling TypeScript-first CMS/app-platform choices for modern Next.js stacks. | ![GitHub Repo stars](https://img.shields.io/github/stars/payloadcms/payload?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/payload?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Strapi](https://strapi.io/) | Still one of the most recognizable headless CMS options in JS land. | ![GitHub Repo stars](https://img.shields.io/github/stars/strapi/strapi?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40strapi%2Fstrapi?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Keystone](https://keystonejs.com/) | Great when you want a customizable app + CMS foundation. | ![GitHub Repo stars](https://img.shields.io/github/stars/keystonejs/keystone?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40keystone-6%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Ghost](https://ghost.org/) | Strong publishing platform with a mature product story behind it. | ![GitHub Repo stars](https://img.shields.io/github/stars/TryGhost/Ghost?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ghost?style=flat-square&logo=npm&label=npm%2Fweek) |

### Documentation

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Docusaurus](https://docusaurus.io/) | Great docs portal and content site framework. | ![GitHub Repo stars](https://img.shields.io/github/stars/facebook/docusaurus?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40docusaurus%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [VitePress](https://vitepress.dev/) | One of the cleanest choices for docs sites in the Vite ecosystem. | ![GitHub Repo stars](https://img.shields.io/github/stars/vuejs/vitepress?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/vitepress?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TypeDoc](https://typedoc.org/) | Still the obvious API docs option for TypeScript libraries. | ![GitHub Repo stars](https://img.shields.io/github/stars/TypeStrong/typedoc?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/typedoc?style=flat-square&logo=npm&label=npm%2Fweek) |

### Rich text & code editing

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Monaco Editor](https://microsoft.github.io/monaco-editor/) | Best for VS Code-like editing in the browser. | ![GitHub Repo stars](https://img.shields.io/github/stars/microsoft/monaco-editor?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/monaco-editor?style=flat-square&logo=npm&label=npm%2Fweek) |
| [CodeMirror](https://codemirror.net/) | Flexible and lightweight code editing foundation. | ![GitHub Repo stars](https://img.shields.io/github/stars/codemirror/dev?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/codemirror?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Tiptap](https://tiptap.dev/) | One of the strongest modern rich-text editor choices in React and full-stack content apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/ueberdosis/tiptap?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tiptap%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TinyMCE](https://www.tiny.cloud/) | Mature rich text editor. | ![GitHub Repo stars](https://img.shields.io/github/stars/tinymce/tinymce?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/tinymce?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Quill](https://quilljs.com/) | Still a familiar choice for rich text editing. | ![GitHub Repo stars](https://img.shields.io/github/stars/slab/quill?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/quill?style=flat-square&logo=npm&label=npm%2Fweek) |

### Files, PDF, uploads, images

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [react-pdf](https://react-pdf.org/) | Useful for both generating and rendering PDFs in React workflows. | ![GitHub Repo stars](https://img.shields.io/github/stars/diegomura/react-pdf?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40react-pdf%2Frenderer?style=flat-square&logo=npm&label=npm%2Fweek) |
| [PDF.js](https://mozilla.github.io/pdf.js/) | The classic for browser PDF rendering. | ![GitHub Repo stars](https://img.shields.io/github/stars/mozilla/pdf.js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/pdfjs-dist?style=flat-square&logo=npm&label=npm%2Fweek) |
| [jsPDF](https://github.com/parallax/jsPDF) | Still useful for client-side PDF generation. | ![GitHub Repo stars](https://img.shields.io/github/stars/parallax/jsPDF?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/jspdf?style=flat-square&logo=npm&label=npm%2Fweek) |
| [react-dropzone](https://react-dropzone.js.org/) | The best default when you want a headless drag-and-drop file upload foundation. | ![GitHub Repo stars](https://img.shields.io/github/stars/react-dropzone/react-dropzone?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-dropzone?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Uppy](https://uppy.io/) | Great when uploads need resumability, remote sources, or a more full-featured upload workflow. | ![GitHub Repo stars](https://img.shields.io/github/stars/transloadit/uppy?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40uppy%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [UploadThing](https://uploadthing.com/) | Strong option for modern TypeScript and Next.js stacks that want an integrated upload backend story. | ![GitHub Repo stars](https://img.shields.io/github/stars/pingdotgg/uploadthing?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/uploadthing?style=flat-square&logo=npm&label=npm%2Fweek) |
| [FilePond](https://pqina.nl/filepond/) | Great UX for uploads. | ![GitHub Repo stars](https://img.shields.io/github/stars/pqina/filepond?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/filepond?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Sharp](https://sharp.pixelplumbing.com/) | The default serious image-processing library for Node. | ![GitHub Repo stars](https://img.shields.io/github/stars/lovell/sharp?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/sharp?style=flat-square&logo=npm&label=npm%2Fweek) |
| [imagemin](https://github.com/imagemin/imagemin) | Handy for asset optimization pipelines. | ![GitHub Repo stars](https://img.shields.io/github/stars/imagemin/imagemin?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/imagemin?style=flat-square&logo=npm&label=npm%2Fweek) |
| [blurhash](https://blurha.sh/) | Still a nice touch for image placeholders. | ![GitHub Repo stars](https://img.shields.io/github/stars/woltapp/blurhash?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/blurhash?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Papa Parse](https://www.papaparse.com/) | Reliable CSV parsing in the browser. | ![GitHub Repo stars](https://img.shields.io/github/stars/mholt/PapaParse?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/papaparse?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Infrastructure, Delivery & Observability

### Dev environment & containers

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Git](https://git-scm.com/) | Still the one tool nobody gets to avoid. | — |
| [Docker](https://www.docker.com/) | The default container story for local dev and many deployments. | — |
| [Docker Compose](https://docs.docker.com/compose/) | Still the easiest way to boot app-shaped local environments. | — |

### Container orchestration

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Kubernetes](https://kubernetes.io/) | Still the default orchestration layer once your deployment model becomes cluster-shaped. | — |
| [Amazon ECS / Fargate](https://aws.amazon.com/fargate/) | Great when you want AWS-native container orchestration with less Kubernetes overhead. | — |

### Hosting & platforms

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Vercel](https://vercel.com/) | Still the default deployment answer for many Next.js-heavy teams. | — |
| [Cloudflare](https://www.cloudflare.com/) | Strong choice when edge runtimes, caching, and global performance matter a lot. | — |
| [Netlify](https://www.netlify.com/) | Still very good for static-heavy sites, docs, and simpler frontend deployments. | — |
| [Railway](https://railway.com/) | Great default when you want to ship a full-stack app quickly without much platform ceremony. | — |
| [Render](https://render.com/) | Good practical platform for web apps, APIs, workers, and managed services. | — |
| [Fly.io](https://fly.io/) | Strong option when you want more infrastructure control and global placement. | — |

### CI/CD

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [GitHub Actions](https://github.com/features/actions) | The default CI/CD answer for a lot of GitHub-native teams. | — |
| [GitLab CI/CD](https://docs.gitlab.com/ee/ci/) | Strong option when your repo and deployment flow already live in GitLab. | — |

### Infrastructure as code & secrets

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [AWS CDK](https://aws.amazon.com/cdk/) | Great fit if your team thinks in code and already lives in AWS. | ![GitHub Repo stars](https://img.shields.io/github/stars/aws/aws-cdk?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/aws-cdk-lib?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Terraform](https://www.terraform.io/) | Still the standard multi-cloud IaC reference point. | — |
| [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) | The obvious managed choice when you are already deep in AWS. | — |
| [Infisical](https://infisical.com/) | Modern secrets management worth knowing. | — |
| [Vault](https://www.vaultproject.io/) | Still the heavyweight name in secrets infrastructure. | — |

### Monitoring, logs & product visibility

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Sentry](https://sentry.io/) | The default frontend and full-stack error-monitoring answer for many teams. | ![GitHub Repo stars](https://img.shields.io/github/stars/getsentry/sentry-javascript?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40sentry%2Fbrowser?style=flat-square&logo=npm&label=npm%2Fweek) |
| [TrackJS](https://trackjs.com/) | Focused browser error monitoring when you want a tight, JS-first product. | ![GitHub Repo stars](https://img.shields.io/github/stars/TrackJs/trackjs-package?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/trackjs?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Datadog](https://www.datadoghq.com/) | Still a major observability platform in production backends. | ![GitHub Repo stars](https://img.shields.io/github/stars/DataDog/browser-sdk?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40datadog%2Fbrowser-rum?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Grafana](https://grafana.com/) | Strong for dashboards and metrics visibility. | — |
| [Better Stack](https://betterstack.com/) | Logs, uptime, and incident tooling in a cleaner modern package. | — |
| [Axiom](https://axiom.co/) | Worth considering for developer-friendly logs and analytics. | ![GitHub Repo stars](https://img.shields.io/github/stars/axiomhq/axiom-js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40axiomhq%2Fjs?style=flat-square&logo=npm&label=npm%2Fweek) |
| [LogRocket](https://logrocket.com/) | Very useful when product teams need session replay in web apps. | — |
| [OpenReplay](https://openreplay.com/) | Good open-source-minded alternative in the replay space. | ![GitHub Repo stars](https://img.shields.io/github/stars/openreplay/openreplay?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40openreplay%2Ftracker?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Cross-Platform Apps

### Desktop

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Tauri](https://tauri.app/) | My first stop when a desktop shell should stay lean. | ![GitHub Repo stars](https://img.shields.io/github/stars/tauri-apps/tauri?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tauri-apps%2Fcli?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Electron](https://www.electronjs.org/) | Bigger footprint, bigger ecosystem, still a reality when compatibility matters more than size. | ![GitHub Repo stars](https://img.shields.io/github/stars/electron/electron?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/electron?style=flat-square&logo=npm&label=npm%2Fweek) |

### Mobile

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [Expo](https://expo.dev/) | The best default starting point for most React Native teams. | ![GitHub Repo stars](https://img.shields.io/github/stars/expo/expo?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/expo?style=flat-square&logo=npm&label=npm%2Fweek) |
| [React Native](https://reactnative.dev/) | Still the default cross-platform native conversation in JS. | ![GitHub Repo stars](https://img.shields.io/github/stars/facebook/react-native?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/react-native?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Capacitor](https://capacitorjs.com/) | Great when your team is fundamentally building a web app that also needs native packaging. | ![GitHub Repo stars](https://img.shields.io/github/stars/ionic-team/capacitor?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40capacitor%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Ionic](https://ionicframework.com/) | Still relevant in hybrid app workflows. | ![GitHub Repo stars](https://img.shields.io/github/stars/ionic-team/ionic-framework?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40ionic%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## AI / ML for JavaScript Apps

### LLM app tooling

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [OpenAI SDK](https://github.com/openai/openai-node) | Official JS/TS SDK for OpenAI APIs. | ![GitHub Repo stars](https://img.shields.io/github/stars/openai/openai-node?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/openai?style=flat-square&logo=npm&label=npm%2Fweek) |
| [AI SDK by Vercel](https://ai-sdk.dev/) | One of the best ways to build streaming AI UX in modern JS apps. | ![GitHub Repo stars](https://img.shields.io/github/stars/vercel/ai?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ai?style=flat-square&logo=npm&label=npm%2Fweek) |
| [LangChain.js](https://js.langchain.com/) | Useful when you want chain / agent abstractions in TypeScript. | ![GitHub Repo stars](https://img.shields.io/github/stars/langchain-ai/langchainjs?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/langchain?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Mastra](https://mastra.ai/) | Worth watching if you want a TypeScript-native framework for AI agents and workflows. | ![GitHub Repo stars](https://img.shields.io/github/stars/mastra-ai/mastra?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40mastra%2Fcore?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Transformers.js](https://huggingface.co/docs/transformers.js/) | Strong option for running transformer models in JavaScript environments. | ![GitHub Repo stars](https://img.shields.io/github/stars/huggingface/transformers.js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40huggingface%2Ftransformers?style=flat-square&logo=npm&label=npm%2Fweek) |

### Traditional ML in JS

| Tool | Why it matters | Signals |
| --- | --- | --- |
| [TensorFlow.js](https://www.tensorflow.org/js/) | Still the most recognizable ML framework in JS. | ![GitHub Repo stars](https://img.shields.io/github/stars/tensorflow/tfjs?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/%40tensorflow%2Ftfjs?style=flat-square&logo=npm&label=npm%2Fweek) |
| [ml5.js](https://ml5js.org/) | Great for friendlier creative-coding and educational workflows. | ![GitHub Repo stars](https://img.shields.io/github/stars/ml5js/ml5-library?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/ml5?style=flat-square&logo=npm&label=npm%2Fweek) |
| [Brain.js](https://github.com/BrainJS/brain.js) | Lightweight neural-net tooling worth knowing exists. | ![GitHub Repo stars](https://img.shields.io/github/stars/BrainJS/brain.js?style=flat-square&logo=github&label=stars) ![npm downloads](https://img.shields.io/npm/dw/brain.js?style=flat-square&logo=npm&label=npm%2Fweek) |

---

## Worth Reading

- [You Don't Know JS Yet](https://github.com/getify/You-Dont-Know-JS) — Still one of the best deep dives into how JavaScript actually works.
- [Clean Code JavaScript](https://github.com/ryanmcdermott/clean-code-javascript) — Useful when you want pragmatic readability rules for day-to-day code.
- [javascript-algorithms](https://github.com/trekhleb/javascript-algorithms) — Excellent reference repo for algorithms and data structures in JS.
- [Roadmap.sh — JavaScript](https://roadmap.sh/javascript) — Good bird's-eye view of the learning surface area.
- [JS: The Right Way](https://github.com/braziljs/js-the-right-way) — Still a worthwhile reference list.

---

## License

MIT is a sensible default for a repository like this, but choose the license that fits how you want others to reuse the material.
