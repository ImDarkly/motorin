---
project: vue-motoreto-practice
purpose: Practice project mimicking an automotive marketplace, for learning Vue 3 + Bootstrap + API consumption
sources:
  - https://getdesign.md/tesla/design-md
  - https://getdesign.md/bmw/design-md
  - https://getdesign.md/ferrari/design-md
  - https://www.ui-skills.com (playbook rules)
  - https://typeui.sh (pull a base token set with: npx typeui.sh pull modern)
---

# DESIGN.md — Practice Car Marketplace (Vue + Bootstrap)

## How to use this file
Drop this whole file into your OpenCode/Claude prompt or agent context before asking
for any UI code. It replaces re-explaining colors/spacing every time.

## Overview
A clean, trustworthy automotive-listing UI. Not flashy — legible, data-dense,
confidence-inspiring (borrow restraint from Tesla/BMW, not gradients-everywhere
AI-generic style).

## Colors
- `primary` **#1A2E4C** — deep automotive navy (headers, primary buttons)
- `accent` **#D62828** — alert/CTA red, used sparingly (favorite, "contact seller")
- `surface` **#FFFFFF** — cards
- `canvas` **#F5F6F8** — page background
- `border` **#E1E4E8**
- `text-primary` **#111418**
- `text-muted` **#5B6470**
- `success` **#1F883D** — "available now"
- `warning` **#B98900** — "pending"

## Typography
- Font stack: `"Inter", system-ui, sans-serif` (free, close to what most automotive
  SaaS sites use — Tesla/BMW use proprietary fonts you can't legally clone)
- H1 · 32px / 1.2 / 700
- H2 · 24px / 1.25 / 600
- Body · 16px / 1.5 / 400
- Small/meta (price, mileage tags) · 13px / 1.4 / 500, `tabular-nums` (see Playbook)

## Spacing
`4 · 8 · 16 · 24 · 32 · 48` — stick to this scale, don't invent one-off values.

## Radius
- `sm` 4px (inputs, tags) · `md` 8px (cards) · `full` 999px (pills/badges)

## Components
- **Car card**: photo (16:9, `aspect-ratio` reserved — see Playbook), title, price
  (tabular-nums), mileage + year as pill tags, favorite icon button top-right.
- **Filter bar**: Bootstrap `form-select` + `form-range` for price, sticky on scroll.
- **Button**: primary (navy fill), outline (navy border), danger (red, for delete
  in your own admin views).
- **Badge/pill**: full radius, 12px text, colored by status (available/pending/sold).

## Layout rules (from ui-skills.com playbook — concrete, not vibes)
1. **Reserve image space**: set `aspect-ratio: 16/9` on car photo containers so
   the grid doesn't jump while images load.
2. **Tabular numbers**: apply `font-variant-numeric: tabular-nums` to price and
   mileage so digits align in list/grid view.
3. **Balanced headings**: `text-wrap: balance` on card titles and page H1/H2.
4. **44px touch targets**: every button/icon-button min 44×44px — matters more
   once you test on a phone.
5. **Concentric radius**: if a card has 8px radius, its inner image/button should
   use a slightly smaller radius (e.g. 6px), not the same value — avoids the
   "nested rectangle" look.
6. **Press feedback**: buttons get a small `scale(0.97)` on `:active` — cheap and
   makes the UI feel responsive.

## Bootstrap usage notes
- Use Bootstrap's grid + form controls as-is (that's literally in the job spec).
- Override only the CSS variables (`--bs-primary`, `--bs-border-radius`, etc.)
  rather than fighting Bootstrap's classes — faster to learn, closer to how a
  real small team would actually configure Bootstrap.

## Getting real tokens instead of invented ones
If you want to ground any of the above in an actual live site rather than my
estimates, generate it yourself for free:
```
npx typeui.sh list          # browse 50+ curated design systems
npx typeui.sh pull modern   # pulls a DESIGN.md/SKILL.md into your repo
```
or browse https://getdesign.md/tesla/design-md and https://getdesign.md/bmw/design-md
directly and merge anything useful back into this file.
