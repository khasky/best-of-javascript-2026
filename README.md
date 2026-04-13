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

- [Node.js](https://nodejs.org/) — The default runtime for most production JavaScript backends.
- [Bun](https://bun.com/) — Fast, ambitious, and increasingly credible as a runtime + package manager + test runner + bundler.
- [Deno](https://deno.com/) — Clean developer experience, modern defaults, and a thoughtful runtime model.
- [Cloudflare Workers](https://developers.cloudflare.com/workers/) — A serious edge runtime, not just a niche deployment target anymore.

### Package managers

- [pnpm](https://pnpm.io/) — My default recommendation for most teams, especially monorepos.
- [npm](https://www.npmjs.com/) — The universal baseline that works everywhere.
- [Bun Package Manager](https://bun.com/docs/pm/cli/install) — Worth trying when you want one binary for install, scripts, and runtime.

### Version management

- [nvm](https://github.com/nvm-sh/nvm) — Still the familiar choice for switching Node versions.
- [Volta](https://volta.sh/) — Excellent when you want per-project tool pinning with less shell friction.

---

## Build, Monorepo & Release Engineering

### Core foundations

- [TypeScript](https://www.typescriptlang.org/) — The language layer most serious JS projects now assume.
- [TypeScript Project References](https://www.typescriptlang.org/docs/handbook/project-references.html) — Important once your repo starts growing sideways.
- [Vite](https://vite.dev/) — The best general-purpose starting point for modern frontend apps.

### Builders, compilers, bundlers

- [Vite](https://vite.dev/) — Still the best default for most new frontend apps.
- [esbuild](https://esbuild.github.io/) — Extremely fast and still one of the best "get out of my way" tools.
- [SWC](https://swc.rs/) — Great when you want speed plus compiler-oriented extensibility.
- [Rspack](https://rspack.dev/) — Strong option when you want webpack-compatible ergonomics with much faster Rust-backed performance.
- [Turbopack](https://turbo.build/pack) — Fast and strategically important in the Next.js world, though still more opinionated than Vite.
- [Rollup](https://rollupjs.org/) — Still excellent for library builds.
- [Rolldown](https://rolldown.rs/) — One of the most important emerging build tools to watch, especially around the Vite ecosystem.
- [webpack](https://webpack.js.org/) — Not the default for new projects anymore, but still everywhere in real codebases.

### Monorepos & release flows

- [Turborepo](https://turbo.build/repo) — Strong fit for frontend-heavy monorepos and fast incremental builds.
- [Nx](https://nx.dev/) — Excellent when you want deeper workspace tooling and bigger-team structure.
- [Changesets](https://github.com/changesets/changesets) — Versioning and changelog sanity for package-based repos.

### Commit-time hygiene

- [Husky](https://typicode.github.io/husky/) — Git hooks with minimal drama.
- [Lefthook](https://github.com/evilmartians/lefthook) — Very fast alternative, especially nice in bigger repos.
- [commitlint](https://commitlint.js.org/) — Useful when commit conventions actually matter in your release process.

---

## Frontend & Full-Stack Frameworks

### Frontend-first

- [React](https://react.dev/) — The ecosystem center of gravity.
- [Vue](https://vuejs.org/) — Excellent developer experience and a strong all-in-one ecosystem.
- [Svelte](https://svelte.dev/) — Still one of the cleanest authoring experiences in UI development.
- [Solid](https://www.solidjs.com/) — Great when you want fine-grained reactivity and a different mental model from React.

### Full-stack / app frameworks

- [Next.js](https://nextjs.org/) — Still the default full-stack React framework for many teams.
- [Astro](https://astro.build/) — A standout choice for content-driven sites, docs, marketing pages, and hybrid content/app builds.
- [Nuxt](https://nuxt.com/) — The obvious full-stack default if your team prefers Vue.
- [SvelteKit](https://kit.svelte.dev/) — Great full-stack option if you are already in the Svelte world.
- [Remix](https://remix.run/) — Worth knowing for web-native routing and form-first thinking.

### Backend / edge-friendly frameworks

- [Hono](https://hono.dev/) — One of the best modern defaults when you want edge-friendly or multi-runtime APIs.
- [Fastify](https://fastify.io/) — A great default for Node APIs when you want speed and structure without a framework tax.
- [NestJS](https://nestjs.com/) — Strong fit for enterprise teams that like architecture, modules, decorators, and convention.
- [Express](https://expressjs.com/) — Old, familiar, and still absolutely alive in existing codebases.

---

## UI, Styling & Design Systems

### CSS & styling systems

- [Tailwind CSS](https://tailwindcss.com/) — Still the most widely adopted utility-first styling system in modern JS apps.
- [vanilla-extract](https://vanilla-extract.style/) — Great when you want typed, file-based styles without runtime overhead.
- [Panda CSS](https://panda-css.com/) — Worth a look if you want design-token-driven styling with static extraction.

### Component systems

- [shadcn/ui](https://ui.shadcn.com/) — A very practical starting point for teams that want ownership over their components.
- [daisyUI](https://daisyui.com/) — A fast, pragmatic Tailwind component layer when you want to ship styled UI without building every primitive yourself.
- [Radix UI](https://www.radix-ui.com/) — Accessible unstyled primitives that play well with real design systems.
- [Mantine](https://mantine.dev/) — One of the nicest batteries-included React UI kits.
- [Material UI](https://mui.com/) — Still common in enterprise products and dashboard-heavy apps.
- [Chakra UI](https://www.chakra-ui.com/) — Friendly ergonomics and a coherent component model.
- [Ant Design](https://ant.design/) — Still a major option for business applications and data-dense interfaces.

### Icons & docs for component work

- [lucide](https://lucide.dev/) — Clean icon set and one of the easiest defaults for modern UIs.
- [react-icons](https://react-icons.github.io/react-icons/) — Useful when you need breadth more than purity.
- [Storybook](https://storybook.js.org/) — Still the standard workshop for components, states, and design-system documentation.

---

## Routing, State, Forms & Validation

### Routing

- [React Router](https://reactrouter.com/) — The classic, still important.
- [TanStack Router](https://tanstack.com/router) — A strong modern choice if type-safe routing matters to you.

### State management

- [Zustand](https://zustand.docs.pmnd.rs/) — Lightweight, minimal, and a great default for many React apps.
- [Redux Toolkit](https://redux-toolkit.js.org/) — Still the right answer when state complexity is real and long-lived.
- [XState](https://stately.ai/docs/xstate) — Best when your problem is workflow complexity, not just state storage.

### Server state & data fetching

- [TanStack Query](https://tanstack.com/query) — The default recommendation for async server-state management.
- [SWR](https://swr.vercel.app/) — Still elegant for simpler React data-fetching patterns.
- [axios](https://axios-http.com/) — Popular and familiar; still useful, even in a fetch-first world.
- [ky](https://github.com/sindresorhus/ky) — Small, modern, pleasant fetch wrapper.

### Forms & validation

- [React Hook Form](https://react-hook-form.com/) — The best default for most React forms.
- [TanStack Form](https://tanstack.com/form) — Strong modern alternative when you want deeper type inference or are already committed to the TanStack ecosystem.
- [Zod](https://zod.dev/) — The current center of gravity for TypeScript-first schema validation.
- [Ajv](https://ajv.js.org/) — Great when JSON Schema is the right abstraction.
- [Joi](https://joi.dev/) — Still useful in backend and validation-heavy codebases.
- [Yup](https://github.com/jquense/yup) — Common in older React form stacks, but less of a new-project default now.

### React hooks

- [usehooks-ts](https://usehooks-ts.com/) — The strongest TypeScript-first default when you want a practical set of reusable React hooks.
- [ahooks](https://ahooks.js.org/) — Great when you want a broader, more enterprise-shaped hooks toolkit.
- [react-use](https://github.com/streamich/react-use) — Still a useful grab-bag of hooks, especially in older or utility-heavy React codebases.

### Localization

- [react-i18next](https://react.i18next.com/) — Still the safest default when a React app needs serious localization.

### Dates & IDs

- [date-fns](https://date-fns.org/) — The best general-purpose date utility default for most JavaScript and TypeScript apps.
- [Day.js](https://day.js.org/) — A lightweight alternative when you want a smaller Moment-like API surface.
- [Luxon](https://moment.github.io/luxon/) — Strong choice when timezone-heavy date handling matters more than minimal bundle size.
- [Temporal](https://tc39.es/proposal-temporal/docs/) — The long-term native direction for safer date and time handling in JavaScript.
- [nanoid](https://github.com/ai/nanoid) — My default pick for compact, modern ID generation.
- [uuid](https://github.com/uuidjs/uuid) — Still the standard option when interoperability and familiar UUID formats matter.

---

## Backend, APIs & Data

### API layers

- [Hono](https://hono.dev/) — Lean, modern, edge-friendly, and increasingly hard to ignore.
- [Fastify](https://fastify.io/) — Excellent for structured Node APIs.
- [NestJS](https://nestjs.com/) — Strong for teams that want architecture spelled out.
- [Express](https://expressjs.com/) — Still important to know because so much Node infrastructure and legacy code still assumes it.
- [tRPC](https://trpc.io/) — Worth evaluating when you want end-to-end TypeScript without hand-written API clients.

When the contract is **OpenAPI** and the client is **React + TypeScript**, generate types (and optionally clients) instead of duplicating shapes by hand — this lines up with the [backend](https://github.com/khasky/backend-architecture-playbook) and [frontend](https://github.com/khasky/frontend-architecture-playbook) playbooks:

- [openapi-typescript](https://github.com/drwpow/openapi-typescript) — Types from OpenAPI; works well with hand-written `fetch` or TanStack Query.
- [Hey API OpenAPI TS](https://github.com/hey-api/openapi-ts) — Codegen for clients and types with active maintenance.
- [Orval](https://orval.dev/) — OpenAPI → clients, mocks, and hooks (including TanStack Query).

### ORMs & query builders

- [Prisma](https://www.prisma.io/) — Still one of the best choices for productivity and onboarding speed.
- [Drizzle ORM](https://orm.drizzle.team/) — One of the strongest choices when you want SQL closer to the surface.
- [Kysely](https://kysely.dev/) — Great when you want type-safe SQL query building without a full ORM.
- [Knex](https://knexjs.org/) — Old but still useful in many backend projects.
- [Mongoose](https://mongoosejs.com/) — Still the obvious entry in MongoDB-heavy Node stacks.

### Queues, cache, streaming

- [BullMQ](https://bullmq.io/) — The default queueing choice for many Redis-backed Node systems.
- [Redis for JavaScript](https://github.com/redis/node-redis) — Standard Redis client for Node.
- [Apache Kafka](https://kafka.apache.org/) — Still the heavyweight event-streaming answer when scale and durability matter.
- [RabbitMQ](https://www.rabbitmq.com/) — Worth knowing where traditional messaging patterns are a better fit than event logs.
- [Amazon SQS](https://aws.amazon.com/sqs/) — Boring in the best possible way for many cloud-native job pipelines.

### Email & notifications

- [Nodemailer](https://nodemailer.com/) — Still the practical default when you need to send email directly from Node services.

### GraphQL & adjacent tools

- [Apollo Client](https://www.apollographql.com/docs/react/) — Still important if your frontend lives in GraphQL.
- [Relay](https://relay.dev/) — Worth it when you want serious GraphQL discipline.
- [GraphQL](https://graphql.org/) — Not a default for everything, but still the right tool in some domains.

---

## Authentication & Security

### Auth

- [Better Auth](https://www.better-auth.com/) — One of the strongest new defaults for TypeScript-first, self-hosted authentication.
- [Auth.js](https://authjs.dev/) — Still a very practical choice, especially in the Next.js ecosystem.
- [Clerk](https://clerk.com/) — Worth considering when a managed auth platform is the right tradeoff.
- [Passport](https://www.passportjs.org/) — Old, flexible, and still found everywhere in established Node apps.
- [Lucia](https://lucia-auth.com/) — More notable as a minimalist approach and reference point than as the obvious default for new apps.
- [Amazon Cognito](https://aws.amazon.com/cognito/) — Useful when managed identity is the right tradeoff.

### Tokens & credentials

- [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) — The familiar JWT implementation everyone has seen.
- [paseto](https://github.com/panva/paseto) — Worth knowing when you want a stronger alternative to raw JWT habits.
- [argon2](https://github.com/ranisalt/node-argon2) — A better modern default for new password-hashing code than older bcrypt habits.
- [bcrypt.js](https://github.com/dcodeIO/bcrypt.js) — Still extremely common, but more of a compatibility choice than the best new-project default.

### Sanitization & frontend security

- [DOMPurify](https://github.com/cure53/DOMPurify) — The obvious default for sanitizing HTML in frontend contexts.
- [sanitize-html](https://github.com/apostrophecms/sanitize-html) — Good when you need configurable HTML sanitization.

### SEO & metadata

- [react-helmet-async](https://github.com/staylor/react-helmet-async) — The safer React-era replacement for `react-helmet` in SPA-style apps.

---

## Testing & Code Quality

### Unit & component testing

- [Vitest](https://vitest.dev/) — The best default for modern Vite-flavored JS/TS projects.
- [Jest](https://jestjs.io/) — Still important, especially in large existing codebases.
- [Node Test Runner](https://nodejs.org/api/test.html) — Worth watching when you want a built-in, dependency-light testing baseline.
- [bun test](https://bun.com/docs/cli/test) — Increasingly interesting if your stack is already Bun-first.
- [Testing Library](https://testing-library.com/) — The right mental model for UI tests in most apps.
- [MSW](https://mswjs.io/) — Excellent for API mocking without contaminating your components.
- [Supertest](https://github.com/ladjs/supertest) — Still a simple and effective way to test HTTP servers.

### End-to-end & browser automation

- [Playwright](https://playwright.dev/) — The current default recommendation for serious end-to-end browser testing.
- [Cypress](https://www.cypress.io/) — Still widely used and worth knowing well, especially in existing suites.
- [BrowserStack](https://www.browserstack.com/) — Useful when cross-browser reality needs to be tested on actual infrastructure.
- [Sauce Labs](https://saucelabs.com/) — Another established option for broader browser/device coverage.

### Linting, formatting, repo hygiene

- [Biome](https://biomejs.dev/) — Fast, modern, and increasingly compelling as a formatter + linter combo.
- [ESLint](https://eslint.org/) — Still the standard linting tool most teams know and trust.
- [Prettier](https://prettier.io/) — Still the default formatter in countless repos.
- [Oxlint / Oxc](https://oxc.rs/) — Worth tracking as an ultra-fast linting layer, especially in CI-heavy repos.
- [lint-staged](https://github.com/lint-staged/lint-staged) — Simple, effective pre-commit filtering.

---

## Content, Docs, Editors & Media

### CMS & content platforms

- [Payload](https://payloadcms.com/) — One of the most compelling TypeScript-first CMS/app-platform choices for modern Next.js stacks.
- [Strapi](https://strapi.io/) — Still one of the most recognizable headless CMS options in JS land.
- [Keystone](https://keystonejs.com/) — Great when you want a customizable app + CMS foundation.
- [Ghost](https://ghost.org/) — Strong publishing platform with a mature product story behind it.

### Documentation

- [Docusaurus](https://docusaurus.io/) — Great docs portal and content site framework.
- [VitePress](https://vitepress.dev/) — One of the cleanest choices for docs sites in the Vite ecosystem.
- [TypeDoc](https://typedoc.org/) — Still the obvious API docs option for TypeScript libraries.

### Rich text & code editing

- [Monaco Editor](https://microsoft.github.io/monaco-editor/) — Best for VS Code-like editing in the browser.
- [CodeMirror](https://codemirror.net/) — Flexible and lightweight code editing foundation.
- [Tiptap](https://tiptap.dev/) — One of the strongest modern rich-text editor choices in React and full-stack content apps.
- [TinyMCE](https://www.tiny.cloud/) — Mature rich text editor.
- [Quill](https://quilljs.com/) — Still a familiar choice for rich text editing.

### Files, PDF, uploads, images

- [react-pdf](https://react-pdf.org/) — Useful for both generating and rendering PDFs in React workflows.
- [PDF.js](https://mozilla.github.io/pdf.js/) — The classic for browser PDF rendering.
- [jsPDF](https://github.com/parallax/jsPDF) — Still useful for client-side PDF generation.
- [react-dropzone](https://react-dropzone.js.org/) — The best default when you want a headless drag-and-drop file upload foundation.
- [Uppy](https://uppy.io/) — Great when uploads need resumability, remote sources, or a more full-featured upload workflow.
- [UploadThing](https://uploadthing.com/) — Strong option for modern TypeScript and Next.js stacks that want an integrated upload backend story.
- [FilePond](https://pqina.nl/filepond/) — Great UX for uploads.
- [Sharp](https://sharp.pixelplumbing.com/) — The default serious image-processing library for Node.
- [imagemin](https://github.com/imagemin/imagemin) — Handy for asset optimization pipelines.
- [blurhash](https://blurha.sh/) — Still a nice touch for image placeholders.
- [Papa Parse](https://www.papaparse.com/) — Reliable CSV parsing in the browser.

---

## Infrastructure, Delivery & Observability

### Dev environment & containers

- [Git](https://git-scm.com/) — Still the one tool nobody gets to avoid.
- [Docker](https://www.docker.com/) — The default container story for local dev and many deployments.
- [Docker Compose](https://docs.docker.com/compose/) — Still the easiest way to boot app-shaped local environments.

### Container orchestration

- [Kubernetes](https://kubernetes.io/) — Still the default orchestration layer once your deployment model becomes cluster-shaped.
- [Amazon ECS / Fargate](https://aws.amazon.com/fargate/) — Great when you want AWS-native container orchestration with less Kubernetes overhead.

### Hosting & platforms

- [Vercel](https://vercel.com/) — Still the default deployment answer for many Next.js-heavy teams.
- [Cloudflare](https://www.cloudflare.com/) — Strong choice when edge runtimes, caching, and global performance matter a lot.
- [Netlify](https://www.netlify.com/) — Still very good for static-heavy sites, docs, and simpler frontend deployments.
- [Railway](https://railway.com/) — Great default when you want to ship a full-stack app quickly without much platform ceremony.
- [Render](https://render.com/) — Good practical platform for web apps, APIs, workers, and managed services.
- [Fly.io](https://fly.io/) — Strong option when you want more infrastructure control and global placement.

### CI/CD

- [GitHub Actions](https://github.com/features/actions) — The default CI/CD answer for a lot of GitHub-native teams.
- [GitLab CI/CD](https://docs.gitlab.com/ee/ci/) — Strong option when your repo and deployment flow already live in GitLab.

### Infrastructure as code & secrets

- [AWS CDK](https://aws.amazon.com/cdk/) — Great fit if your team thinks in code and already lives in AWS.
- [Terraform](https://www.terraform.io/) — Still the standard multi-cloud IaC reference point.
- [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) — The obvious managed choice when you are already deep in AWS.
- [Infisical](https://infisical.com/) — Modern secrets management worth knowing.
- [Vault](https://www.vaultproject.io/) — Still the heavyweight name in secrets infrastructure.

### Monitoring, logs & product visibility

- [Sentry](https://sentry.io/) — The default frontend and full-stack error-monitoring answer for many teams.
- [TrackJS](https://trackjs.com/) — Focused browser error monitoring when you want a tight, JS-first product.
- [Datadog](https://www.datadoghq.com/) — Still a major observability platform in production backends.
- [Grafana](https://grafana.com/) — Strong for dashboards and metrics visibility.
- [Better Stack](https://betterstack.com/) — Logs, uptime, and incident tooling in a cleaner modern package.
- [Axiom](https://axiom.co/) — Worth considering for developer-friendly logs and analytics.
- [LogRocket](https://logrocket.com/) — Very useful when product teams need session replay in web apps.
- [OpenReplay](https://openreplay.com/) — Good open-source-minded alternative in the replay space.

---

## Cross-Platform Apps

### Desktop

- [Tauri](https://tauri.app/) — My first stop when a desktop shell should stay lean.
- [Electron](https://www.electronjs.org/) — Bigger footprint, bigger ecosystem, still a reality when compatibility matters more than size.

### Mobile

- [Expo](https://expo.dev/) — The best default starting point for most React Native teams.
- [React Native](https://reactnative.dev/) — Still the default cross-platform native conversation in JS.
- [Capacitor](https://capacitorjs.com/) — Great when your team is fundamentally building a web app that also needs native packaging.
- [Ionic](https://ionicframework.com/) — Still relevant in hybrid app workflows.

---

## AI / ML for JavaScript Apps

### LLM app tooling

- [OpenAI SDK](https://github.com/openai/openai-node) — Official JS/TS SDK for OpenAI APIs.
- [AI SDK by Vercel](https://ai-sdk.dev/) — One of the best ways to build streaming AI UX in modern JS apps.
- [LangChain.js](https://js.langchain.com/) — Useful when you want chain / agent abstractions in TypeScript.
- [Mastra](https://mastra.ai/) — Worth watching if you want a TypeScript-native framework for AI agents and workflows.
- [Transformers.js](https://huggingface.co/docs/transformers.js/) — Strong option for running transformer models in JavaScript environments.

### Traditional ML in JS

- [TensorFlow.js](https://www.tensorflow.org/js/) — Still the most recognizable ML framework in JS.
- [ml5.js](https://ml5js.org/) — Great for friendlier creative-coding and educational workflows.
- [Brain.js](https://github.com/BrainJS/brain.js) — Lightweight neural-net tooling worth knowing exists.

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
