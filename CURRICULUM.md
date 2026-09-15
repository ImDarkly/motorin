# CURRICULUM.md — Interview-Readiness Checklist

Orchestrator reads this file to plan daily tasks. Teacher references it for
"why would you choose X" prompts. Examiner picks topics marked `[done]` to
re-test with explain-it-back questions. Check off with a one-line note on
*why* you understood it, not just that you did the task.

Mark: `[ ]` not started · `[~]` built something, don't fully get the *why*
yet · `[x]` done — can explain what/why/how out loud.

Append an exposure count to each item as it's taught, e.g. `[~] computed
(2x)` — teacher uses this to pick worked-example vs fill-in-blank vs
extend-partial vs cold-build (see teacher.md's task ladder). Never jump
straight to cold-build on `(1x)`.

## 1. JavaScript fundamentals (assumed known from React, verify anyway)
- [ ] Closures — why a function keeps access to variables after its scope exits
- [ ] `this` binding — arrow functions vs regular functions, why it matters in event handlers
- [ ] Promises / async-await — what a microtask is, why `await` doesn't block the thread
- [ ] Array methods (`map`/`filter`/`reduce`) — why immutability matters for reactivity systems
- [ ] Event loop basics — why a `setTimeout(fn, 0)` still runs after synchronous code

## 2. Vue 3 core (the job's main requirement)
- [~] Reactivity system (1x) — why `ref()` needs `.value`, what a Proxy does that
      `Object.defineProperty` (Vue 2) couldn't — taught 9/13, step 1-4 in progress
- [~] `v-model` (1x) — desugars to `:model-value` + `@update:model-value`, why it matters for custom form components — taught 9/13
- [ ] Composition API vs Options API — why Composition API exists (logic reuse
      across components without mixins' naming collisions)
- [ ] `computed` vs `watch` vs `watchEffect` — caching behavior, when each is
      the wrong tool
- [ ] Component lifecycle (`onMounted`, `onUpdated`, `onUnmounted`) — why API
      calls belong in `onMounted`, not top-level `setup()`
- [ ] `v-for` + `:key` — why Vue's diffing algorithm needs a stable key, what
      breaks without one (state leaking between reordered items)
- [ ] Props vs emits vs `provide`/`inject` — when prop-drilling becomes a
      smell and what each escape hatch costs you
- [ ] Composables (`useXyz()` functions) — the Vue equivalent of a custom
      React hook, why they're just functions and not a special construct

## 3. Styling / Bootstrap
- [ ] Bootstrap grid system — how the 12-column model and breakpoints work,
      why `col-md-6` behaves differently than `col-6`
- [ ] CSS specificity — why overriding Bootstrap sometimes needs `!important`
      and why that's usually a sign of fighting the framework
- [ ] Responsive design — mobile-first vs desktop-first, why Bootstrap chose
      mobile-first

## 4. Consuming APIs
- [ ] `fetch` vs `axios` — what axios adds (interceptors, auto JSON, better
      error handling) and why a small team might still choose plain fetch
- [ ] Async error handling — try/catch around `await`, why an unhandled
      rejection is worse than it looks
- [ ] CORS — what it actually is (a browser-enforced policy, not a server
      bug), why "add a proxy" is the usual fix in dev
- [ ] Loading/error/empty states — why every API-driven component needs all
      three, not just the happy path

## 5. Git
- [ ] Staging area — why `git add` exists as a separate step from commit
- [ ] Branching model — why you branch at all, fast-forward vs merge commit
- [ ] Merge vs rebase — what each does to history, why teams pick one policy
- [ ] `.gitignore` — why `node_modules` and `.env` never belong in a repo
- [ ] Writing a good commit message — what makes one commit "one logical
      change" instead of a dump

## 6. Django templates (stretch — "valorable" not required)
- [ ] Template engine basics — `{{ variable }}` vs `{% tag %}`, why templates
      can't run arbitrary Python (security boundary)
- [ ] Context — how data gets from a view into a template
- [ ] Static files — why Django separates `static/` from templates at all

## 7. The soft-skill layer (interviewers ask this too)
- [ ] Be ready to describe this project in 60 seconds: what it does, what you
      built, one thing you'd do differently now
- [ ] Be ready to explain one bug you hit and how you actually found the root
      cause (not just "I fixed it")
- [ ] Be ready to say, honestly, what you don't know yet — a junior claiming
      false mastery is a worse signal than an honest gap with a learning plan

## How to use this during the 2 weeks
Don't try to finish top-to-bottom. Sections 2 and 4 are the actual job
requirements — spend most days there. Sections 1, 3, 5 get covered
incidentally through the project; check them off as they come up naturally,
don't schedule dedicated days for things you already half-know. Section 6 is
explicitly optional — only touch it if 1-5 are solid with days to spare.
Section 7 gets a pass the night before any real interview, not during
week one.

**If you're starting from zero Vue knowledge with an AI-built repo already in
place** (this project's actual situation): do NOT try to audit/explain the
existing code first — you don't have a baseline to audit against yet. Do
section 2's items as isolated throwaway exercises first (days 1-3, no contact
with the real repo), then rebuild each existing component blind from its
requirements before ever opening the AI-written version (days 4-5). The gap
between what you built and what's already there IS the lesson — see
orchestrator.md's Phase A/B for the exact sequencing.
