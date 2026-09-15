# PROGRESS.md — 2-Week Learning Project Tracker

## Phase A — Vue Fundamentals (days 1-3)
- [~] **ref() counter** — can explain why `.value` is needed, Proxy mechanism, and how it differs from React `useState` (1x) — taught 9/13
- [~] **v-model form** — can desugar to `:model-value` + `@update:model-value`, why it matters for custom components (1x) — taught 9/13
- [ ] **v-for + :key** — why stable keys prevent state leaking, what breaks without one
- [ ] **computed formatter** — caching behavior vs watch, when each is the wrong tool
- [ ] **watch side effect** — async timing, immediate vs deferred, watchEffect vs watch
- [ ] **one composable** — function that returns Vue APIs, not a special construct

## Phase B — Build Blind Then Diff (days 4-5)
- [ ] **ListingCard** — built from scratch, then diffed against AI version
- [ ] **ListingFilters** — built from scratch, then diffed against AI version
- [ ] **ListingForm** — built from scratch, then diffed against AI version

## Phase C — API Replacement (days 6-10)
- [ ] **Real API call** — replaced seed-data.html/localStorage with actual fetch

## Phase D — CodeRabbit Fixes (days 11-12)
- [ ] **PR #3 fixes** — dark theme, aspect ratio, badge position/colors, btn-primary contrast

## Phase E — Review + Mock Interview (days 13-14)
- [ ] **Mock interview** — examiner covers all [x] items

## CURRICULUM.md Checkbox Tracker
(See docs/CURRICULUM.md for full list. Mark items as [ ], [~], or [x] below.)

### Section 2 — Vue 3 core (priority)
- [ ] Reactivity system — why `ref()` needs `.value`, Proxy vs `Object.defineProperty`
- [ ] Composition API vs Options API — logic reuse without mixin collisions
- [ ] `computed` vs `watch` vs `watchEffect` — caching behavior, wrong tool warnings
- [ ] Component lifecycle — why API calls belong in `onMounted`, not top-level `setup()`
- [ ] `v-model` — desugaring, why it matters for custom form components
- [ ] `v-for` + `:key` — diffing algorithm need, state leaking without stable key
- [ ] Props vs emits vs provide/inject — prop-drilling smell, escape hatches
- [ ] Composables — Vue equivalent of React custom hook, just functions not special

### Section 4 — Consuming APIs (priority)
- [ ] `fetch` vs `axios` — interceptors, auto JSON, better error handling
- [ ] Async error handling — try/catch around `await`, unhandled rejection danger
- [ ] CORS — browser-enforced policy, not a server bug, proxy in dev
- [ ] Loading/error/empty states — all three needed, not just happy path

### Section 1 — JavaScript fundamentals (incidental)
- [ ] Closures — function keeps access to variables after scope exits
- [ ] `this` binding — arrow vs regular functions in event handlers
- [ ] Promises / async-await — microtask, why `await` doesn't block
- [ ] Array methods — immutability for reactivity
- [ ] Event loop — `setTimeout(fn, 0)` runs after sync code

### Section 3 — Styling / Bootstrap (incidental)
- [ ] Bootstrap grid — 12-column, breakpoints, `col-md-6` vs `col-6`
- [ ] CSS specificity — `!important` signals framework fighting
- [ ] Responsive design — mobile-first rationale

### Section 5 — Git (incidental)
- [ ] Staging area — `git add` vs commit separation
- [ ] Branching model — why branch, fast-forward vs merge commit
- [ ] Merge vs rebase — history impact, team policy
- [ ] `.gitignore` — `node_modules` and `.env` never in repo
- [ ] Commit messages — one logical change per commit

### Section 6 — Django templates (stretch)
- [ ] Template engine — `{{ variable }}` vs `{% tag %}`, no arbitrary Python
- [ ] Context — data from view into template
- [ ] Static files — `static/` separation from templates

### Section 7 — Soft skills (last 2-3 days)
- [ ] 60-second project description
- [ ] Bug root cause explanation
- [ ] Honest gap assessment