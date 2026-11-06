# Production workflow

**As of:** 2026-11-06  
**Mode:** small, evidence-based solo production, with author acceptance gates.

## Rules

1. No feature solely because we can build it. Each addition should improve commercial appeal, core gameplay or usability.
2. **Propose -> author approves -> implement -> verify -> accept -> update truth.**
3. Distinguish proposed / approved / in progress / technically verified / art accepted / implemented and tested / published.
4. Avoid high-complexity simulation, sprawling world building, uncontrolled randomness or major engine changes without evidence.
5. Use reproducible workflows, minimal dependencies, narrow milestones and tests. Keep project separate from Cities 2077 code and canon.
6. Preserve the author's chosen visual direction and budget limits; flag licensing and approval risks rather than hiding them.
7. Favor readable, scalable UI from the first vertical slice (lesson from Cities 2077).
8. Do not announce dates, feature availability, pricing or Steam approval based on planning documents.

## Phased plan

### VA-P0 — Commercial/art feasibility (CURRENT)
- Establish vision, decisions, scope limits and source-of-truth documents.
- Validate local AI image generation (technical execution done).
- Accept **one** distinctive original character design and a method for consistent variants (pending).
- Check costs, commercial-use rights and distribution rules.
- Confirm fantasy matching's smallest useful input/output design.

**P0 gate:** approved visual style and reproducible, commercially viable character-asset process, plus a small spec for the core mechanic.

### VA-P1 — Mechanics prototype
- Single client, single adult performer, one room and one request.
- Fixed set of compatibility tags, transparent scoring and authored outcome.
- Short loop: request -> choose -> resolve -> reward -> next step.
- No commercial art required to test fun.

**Gate:** demonstrably understandable, enjoyable decisions in a small repeatable test.

### VA-P2 — Vertical slice
- One polished slice with approved art, legible UI, clear onboarding and simple saved progress.
- Test pacing to adult rewards and limited-player interaction.
- Player feedback, especially whether matching is fun or annoying.

### VA-P3 — Production
- Expand only within approved roster, scenes, rooms and authored events.
- Validate accessible UI, performance, install and save/reload.
- Draft trailer/screenshots/description and build release checklist.

### VA-P4 — Demo and distribution
- Free demo (approved intention), feedback/iteration and Steam storefront if eligible.
- Validate current Steam fees, developer onboarding, adult rules, AI disclosure and regional considerations.
- Author explicitly approves any public release.

## Technology direction

**Candidate:** TypeScript core + React front end + Tauri Windows packaging, simple local saves, offline runtime. Familiarity makes it attractive, but not an irreversible engine decision. No online accounts, multiplayer or in-game LLM API.

## Acceptance evidence

For each milestone record: task ID, intended scope, tangible output, local test result, subjective art/gameplay feedback, unresolved defects, author acceptance and current status in PROGRESS.md.

Keep the process small enough that documentation does not consume production time.
