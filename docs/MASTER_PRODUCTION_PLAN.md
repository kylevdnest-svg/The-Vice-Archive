# The Vice Archive — Master Production Plan

**Plan version:** 1.0 (2026-11-06, Africa/Johannesburg)  
**Owner:** SableInk  
**Stage:** VA-P0 pre-production; **no playable game**.  
**Purpose:** Complete, ordered path from current art feasibility tests to a finished commercial Windows release and post-launch care.  
**Authority:** This plan is the production sequence. `GAME_VISION.md`, `DECISIONS_AND_SCOPE.md`, `ART_PIPELINE.md`, `PROGRESS.md`, and the author's latest explicit approvals remain authoritative for their topics.

**Guiding promise:** "The adult content is fantastic, and the gameplay makes unlocking it worthwhile."

## How to use this plan

- Work **one numbered task at a time** within the current gate. Record technical evidence, visual feedback, and acceptance in `PROGRESS.md`.
- The author approves major decisions. A technically passing test is not necessarily artistically accepted.
- Each task state is one of: NOT STARTED, IN PROGRESS, BLOCKED, VERIFIED, ACCEPTED. Gate state is ACCEPTED only when all blocking requirements are accepted.
- A failed gate triggers a **small correction or deliberate scope reduction**, not a new system.
- Do not mark planned content as implemented. Do not promise a launch date while primary art and gameplay feasibility remain unknown.
- The art path and mechanics spike can overlap **only** when doing so avoids idle time; don't produce bulk art before art consistency and licensing are proven.
- Distinguish **hard gates** from **marketing research that can run in parallel**. Do not block the first gameplay prototype waiting for a Steam page.
- Maintain a change log of additions/removals affecting art workload, scenes, code and commercial claims; require author sign-off for expansion.
- "R0" is an **art/production cost target**, not a guarantee that commercial distribution can be free.

## Non-negotiable project constraints

1. Original adult cast; finite single-player campaign; one modern luxurious gothic-influenced theatre/fantasy studio; not a cyberpunk city sandbox.
2. Audience focus: heterosexual male players first, with limited deliberately scoped appeal for female and gay players. No promise of equivalent routes or content before approval.
3. Core differentiator: satisfying **fantasy configuration / matching** of client requests, adult performers and limited room/theme choices.
4. **Very controlled variation**, small simple stats, authored outcomes and rewards. No complex emergent psychology, multiplayer, server, runtime LLM or endless procedural economy.
5. Offline Windows release; readable, scalable UI; stable local saves.
6. Mature illustrated 2D with expressive faces, original character design and restrained animation; broad inspiration from *The Coffin of Andy and Leyley*, **not imitation of protected characters or assets**.
7. Current proposed stack: TypeScript + React + Tauri; **not yet locked by prototype acceptance**.
8. Zero-budget art attempts: assistant-generated **non-explicit** original character references, local ComfyUI tests, Krita editing. End-to-end production and adult variants **not proven**.
9. Commercial licences and platform eligibility are essential gates, not optional polish.
10. No named performer is canon. Use a **real online name generator** for proposals, avoid the rejected recurring surnames Vale and Sable, and get explicit author approval before recording names.

---

# PHASE VA-P0 — Establish art and product feasibility (CURRENT)

**Goal:** Prove that one commercially attractive original character can be reproduced and that the proposed fantasy-matching mechanic is narrow enough to build. **Do not build the full game yet.**

### VA-001 — Capture the visual target
- Create a small style specification: shapes, line thickness, eye design, palette, face proportions, clothing, background treatment and UI mood.
- Record examples of **principles** admired from the visual reference, not images to copy into shipped assets.
- Mark what is *not* acceptable: inconsistent eyes, multiple unwanted portraits, ornate generic anime decoration, unintended signatures.
- **Output:** `art/ART_DIRECTION.md` or equivalent approved visual notes.
- **Accept when:** author confirms the intended look in words and one or more concept images.

### VA-002 — Make one original adult lead-character concept
- Create a clothed, non-explicit, original adult performer concept with face clearly visible and front/three-quarter views suitable for later production.
- Iterate on **design**, not name. No canonical name until generator consultation and approval.
- **Output:** author-approved baseline portrait and a short character reference description.
- **Accept when:** character looks right and is visually distinct from the inspiration.

### VA-003 — Build the identity reference sheet
- Record face, eyes, hair, skin, height/proportions, colour swatches, silhouette, outfit and a neutral pose.
- Save original assets and prompt/seed/model provenance outside the game's runtime assets.
- **Output:** reference sheet + asset manifest.
- **Accept when:** the author can identify what must remain unchanged across variations.

### VA-004 — Local editing consistency test
- Import approved references into ComfyUI and test **one alternate facial expression**, **one alternate outfit**, and **one second pose**, keeping the character clearly the same adult person.
- Use Krita to fix small defects and standardise linework/eyes.
- Track attempts, parameters, manual time and failures.
- **Output:** reference + three variants, workflow JSON, editing notes.
- **Accept when:** same recognisable identity, acceptable eyes/proportions, practical editing effort. Do not pretend success from one lucky generation.

### VA-005 — Production-asset feasibility and compliance test
- Test whether the proposed local editing process can produce a **non-explicit-to-adult artwork pipeline** consistent enough for intended adult rewards without destroying character identity. Keep experimental adult variations private and distinct from store promotional assets.
- Evaluate whether production quality is achievable on local hardware without expensive or prohibited services. Explicit imagery is **not** required in the repository to record an acceptance result.
- Inspect checkpoint/tool licences (including output/commercial limitations), reference provenance, applicable Steam and other storefront content rules; save links and dates.
- **Output:** quality/cost/licence decision log, feasible asset types and required/manual intervention.
- **Accept when:** the author approves both commercial viability and repeatability. If not viable, **reduce scene/style scope or choose a new lawful asset-production approach** before content scaling.

### VA-006 — Micro-specify fantasy matching
- Define 3–4 bounded request tags, 3–4 performer attributes, 2–3 experience configuration choices, and a handful of authored outcome tiers **as a prototype proposal**, not production canon.
- Produce a one-page decision example explaining success/failure visibly to player.
- Keep actor boundaries and eligibility clear. No random chains of dozens of probabilities.
- **Output:** `docs/FANTASY_MATCHING_SPEC.md`.
- **Accept when:** author understands the loop and confirms it is appealing and feasible.

### VA-P0 gate
**Approved unique art direction + one approved adult character design + reproducible controlled variants + verified production/licensing feasibility + one-page fantasy-matching spec.**

**Fallback:** If art feasibility fails, stop bulk production; revise art process/style, or consider cutting scene count/visual demands. Technical ability to generate any image is not enough.

---

# PHASE VA-P1 — Build and validate the mechanics prototype

**Goal:** Prove the minute-to-minute interaction is interesting **before** authoring dozens of scenes or characters.

### VA-007 — Select and lock the prototype stack
- Compare TypeScript/React/Tauri against a dedicated engine only for actual needs: 2D layered illustration, scene transitions, offline save and packaging.
- Prefer existing stack if it meets prototype requirements. Document the choice; do not re-platform without a clear failed requirement.
- **Output:** one-page architecture decision and smoke-test specification.

### VA-008 — Create minimal project skeleton
- TypeScript data and pure rules separated from React presentation; Tauri integration only where needed.
- Set up repository structure, scripts, formatter, tests and Windows launch/build commands.
- Keep code/design/assets separate; avoid any Cities 2077 dependencies unless explicitly approved.
- **Output:** runnable placeholder app + passing minimal test/build gates.

### VA-009 — Implement one complete fantasy appointment
- One client, one performer, one room, one request, a few choices.
- Evaluate the request against performer skills/preferences and preparation with **simple deterministic rules**.
- Show result, reason, payment and a placeholder reward; allow the player to return to choose another action.
- **Output:** fully playable single-session loop without commercial art.

### VA-010 — Add save, accessibility and reproducibility foundations
- Persist one local game state; load and resume.
- Provide UI scaling and readable text immediately.
- Add unit tests that reproduce the same result from the same inputs/seed; ensure no duplicate payout/reward on reload.
- **Output:** tested save and accessible UI scaling.

### VA-011 — Internal fun test
- Have the author play several short appointment variations *without* an explanation from the developer.
- Check: can they predict plausible outcomes? Do decisions matter? Is matching fun or just clicks before an adult reward?
- Record friction, boredom and missing feedback; cut unnecessary choices.
- **Output:** test report and small list of fixes.

### VA-P1 gate
**A small, replayable, saved one-client/one-performer loop that is clear, meaningfully interactive and fun enough to develop.**

**Fallback:** If the matching feels like busywork, simplify/shorten it, add satisfying reveal/feedback or reconsider the mechanic. Do not expand the cast.

---

# PHASE VA-P2 — One polished vertical slice

**Goal:** Prove that the whole experience — art + UX + progression + payoff — feels worth buying.

### VA-012 — Author one polished scenario and reward
- One coherent request, choices, outcomes and a meaningful authored adult-content reward (using licensed, approved art).
- Keep all named characters uncanonical until author-approved naming process has run.
- **Output:** short complete narrative/scene package, with content tracking.

### VA-013 — Integrate one approved character art set
- Neutral expression, reaction expressions, one outfit variant, necessary scene art, in-game background and simple layered transitions.
- Avoid elaborate animations until the basic visual experience is compelling.
- **Output:** consistent art displayed in the actual game and tested at multiple resolutions.

### VA-014 — Polish the smallest UI
- Main venue hub, client request, performer choice, fantasy configuration, result, reward, day-end summary.
- Add concise onboarding/tutorial and explicit status/error states.
- **Output:** complete onboarding-to-payoff loop with no placeholder instructions.

### VA-015 — Add tiny progression arc
- A few repeatable appointments, one upgrade, one character beat and a clear mini-goal.
- Ensure reward pacing makes gameplay worthwhile without excessive grinding.
- **Output:** 20–40 minute *test slice* (duration is a test target, not a content promise).

### VA-016 — External blind playtest
- Small group of consenting adult testers, with clear feedback form.
- Ask whether **the fantasy matching is enjoyable**, whether art is compelling, where players struggle, how long to reward and what would make them pay.
- Track reproducible defects and feature requests separately.
- **Output:** evidence-informed vertical-slice acceptance decision.

### VA-P2 gate
**The author approves a polished, enjoyable, representative slice; target audience can understand it and values the art/reward experience.**

**Fallback:** Fix the top 2–3 barriers or reduce scope. Do not commit to full content production until the slice is convincing.

---

# PHASE VA-P3A — Production lock (before mass content)

**Goal:** Freeze a complete, small game that can actually ship.

### VA-017 — Lock campaign structure
- Define start, milestones, final goal and ending for a finite business progression, not a sandbox.
- Determine chapter/day cadence by playtest pace rather than arbitrary simulation length.
- **Output:** campaign outline and end-state condition.

### VA-018 — Set HARD scope budgets
- Approve maximum adult performer count, client types, request tags, room upgrades, authored scenario types, scene count, expressions, outfits, and optional identity-specific content.
- Initial earlier examples (4 performers, 3 rooms, 4 request categories, 20–30 days, 2–4h) are **unapproved candidates**, not commitments.
- Count how many unique art assets and variants this implies; reduce before approving.
- **Output:** dated `docs/SCOPE_LOCK.md` with an art/feature cost estimate.

### VA-019 — Approve character canon and content boundaries
- Approve names from verifiable online-generator results; record source and author acceptance.
- Define each adult performer's personality, work specialties, design reference, boundaries, relationship beats and scene checklist.
- Check all material against the target storefront's legal/content rules. Avoid promising broader audience routes before defined.
- **Output:** cast bible + scene inventory, adult ages established.

### VA-020 — Author complete content map
- List every critical appointment, outcome text, unlock, character scene, upgrade, campaign milestone, onboarding text, and credits.
- Distinguish essential content from optional stretch extras.
- **Output:** production backlog with unique IDs and acceptance criteria.

### VA-P3A gate
**Every shipped mechanic and piece of content is counted; no new character, scene or system without a recorded trade-off removing equivalent work.**

---

# PHASE VA-P3B — Full production, in vertical batches

**Goal:** Finish the approved game without uncontrolled expansion. Iterate by playable sections, never by piling up unintegrated assets.

### VA-021 — Complete core rules and gameplay state
- Only implement approved match scoring, constraints, upgrades, campaign state, unlock flags, inventory/currency if essential.
- Unit tests, reproducible outcomes and save migration/versioning.

### VA-022 — Finish management screens and UX
- Hub, appointment flow, performer detail, upgrade screen, story/reward viewer, settings, credits, pause/exit.
- Keyboard/mouse, readable typography, UI-scale setting, error feedback and straightforward navigation.

### VA-023 — Produce character packs, one at a time
- For each approved adult performer: reference -> expressions -> outfits -> selected reward art -> local consistency check -> final Krita cleanup -> integrate -> author accept.
- Save source and finished assets separately. If an asset remains inconsistent, **repair it before starting more**.

### VA-024 — Produce narrative and event packs
- Write concise character arcs and scenario variations to the locked content map.
- Playtest tone, choice clarity, pacing and whether text supports rather than slows down rewards.

### VA-025 — Add restrained presentation
- Fades, expression swaps, subtle idle/lighting effects, UI feedback, no fully animated scene requirement unless explicitly traded into scope.
- Add legally usable audio/music/ambient effects with licence/provenance ledger; allow volume control.

### VA-026 — Integrate campaign batches
- For each campaign section, verify progression from new game through that section with no softlocks.
- Record acceptance evidence, screenshots and relevant tests. Save complete build snapshots at each accepted milestone.

### VA-P3B gate
**Full planned campaign playable start-to-finish, all required rewards and endings reachable, no placeholder content.**

---

# PHASE VA-P3C — Quality assurance and release candidate

### VA-027 — Functional and deterministic QA
- Fresh game, successful/failed appointment combinations, upgrade dependencies, unlocks, ending, reload/restart, repeated day loops, edge cases and missing assets.
- Automated tests for scoring, reward gating, negative money/overspending protection and save validity.

### VA-028 — Windows packaging and performance QA
- Release build runs outside development environment on a clean Windows machine/profile.
- Test installation/extraction, antivirus warnings, crashes, save location and behaviour after updates.
- Test performance on the author's hardware and at lower display resolutions; no claim of broad compatibility without testing.

### VA-029 — Accessibility and usability QA
- Multiple UI-scale levels, window sizes, keyboard navigation, contrast, readable dialogue, no clipped text, basic audio controls.
- Re-test on a smaller screen; the UI-scale problems reported in Cities 2077 must not recur.

### VA-030 — Content, provenance and compliance QA
- All characters depicted as adults, no accidental third-party intellectual property, no unapproved models/assets, source and licence inventory complete.
- Verify current rules of desired storefronts **before** submission; audit pre-generated AI content disclosures and adult-content survey.
- Ensure Steam-facing screenshots/capsules and demo assets comply; don't assume that permitted in-game content can appear in unrestricted marketing.

### VA-031 — Release candidate and freeze
- Author plays the entire game, verifies tone/rewards/ending, signs off on known-issues list.
- Bug fixes only after freeze, unless an author-approved trade-off is documented.
- **Output:** reproducible, versioned Windows release-candidate build.

### VA-P3C gate
**No release-blocking defects, all content accepted, licensing/disclosure audit done, complete campaign and save tested.**

---

# PARALLEL TRACK VA-M — Research, storefront and audience building

**This track runs alongside production but has its own approvals. Nothing is made public automatically.**

### VA-M01 — Competitor research (begin after P0 starts; refine before scope lock)
- Dated comparison of adult management games: premise, art, pricing, reviews, observed strengths/complaints, time-to-reward, gameplay friction, supported languages.
- Reviews and third-party revenue estimates are **not verified sales**.
- Write assumptions and counterexamples; challenge whether fantasy matching is truly differentiated.

### VA-M02 — Commercial identity and packaging
- Confirm title clearance/search for "The Vice Archive" (store and trademark checks appropriate to release regions).
- Prepare original logo, capsules, game screenshots and short hook that correctly describes the *actual* playable content.
- Determine real list price after quality/competitor review; $9.99 remains a **proposal**.

### VA-M03 — Steamworks onboarding and eligibility
- Review current Steam Direct fee, tax/banking details, agreements, local currency/payout matters and eligibility of adult content and AI-assisted assets.
- **As checked 2026-11-06:** Steam documents a US$100 fee per app, a 30-day minimum after payment before first release, and a public Coming Soon page at least two weeks before release (recheck at onboarding). Adult-only content store page/build review may need additional time.
- Budget the required costs; no need to pay before feasibility is credible, but **do not leave the platform waiting period until the end**.
- Treat Steam approval as a real external gate, not a formality.

### VA-M04 — Coming Soon page and wishlists
- Once vertical slice and promotional material are approved, submit required store content and build where required for adult review; publish Coming Soon after approval.
- Track wishlist metrics and feedback rather than assuming likes equal sales.
- Share transparent progress via SableInk channels; separate Cities 2077 and HEMOCODE.

### VA-M05 — Demo preparation
- Author-approved free demo: use representative gameplay, limited content, strong onboarding and satisfying payoff without giving away the entire campaign.
- Build a separate demo configuration/app as needed for Steam, and test that demo content/trailers/screenshots match claims.
- **Current Steam docs:** if a demo precedes full launch, Coming Soon must be visible to support wishlists; Steam notes that early demos are a strategic choice, not automatically best.

### VA-M06 — Demo feedback and marketing revision
- Gather actual player reports (pacing, art, price sensitivity, wishlists, defects); fix blockers and improve screenshots/trailer/title copy.
- Don't promise extra content based on individual comments.
- Determine launch timing only after platform gate and release candidate are realistically achievable.

**Storefront rule:** A Steam page is not publicly guaranteed until Valve review is complete. Public content/price/releases need the author's approval.

---

# PHASE VA-P4 — Commercial launch

### VA-032 — Finalise Steam/store submission
- Submit approved store copy, screenshots, mature-content and generative-AI disclosures, packages/build and pricing.
- Account for review timelines and possible rejection or required changes.
- Conduct clean install/download test through the actual platform once accessible.

### VA-033 — Launch readiness
- Check achievements/cloud only if deliberately scoped (neither is required by this plan).
- Verify support contact/channel, bug-report intake, release notes, backup upload, save-compatibility handling and rollback path.
- Author approves exact release date, pricing and messaging.

### VA-034 — Release and communicate
- Publish only after store approval, time gates, approved release build and author signoff.
- Post succinct changelog + purchase link + clear game description in permitted communities.
- Do not describe future features as present.

### VA-P4 gate
**A purchasable, complete Windows game exists on the approved storefront and support/reporting channels work.**

---

# PHASE VA-P5 — Post-launch support and commercial learning

### VA-035 — Monitor the launch
- Track crash reports, save corruption, download/install problems, UI accessibility and misunderstood mechanics.
- Classify and prioritise issues: critical, high, cosmetic, feature request.

### VA-036 — Ship focused patches
- Reproduce -> fix -> regression test -> package -> verify save compatibility -> publish notes.
- Avoid introducing new systems as a substitute for addressing reliability.

### VA-037 — Evaluate commercial outcome
- Record verified platform metrics available to the author: sales, refunds, revenue after platform deductions, wishlists, conversion, regional patterns, reviews and support costs.
- Compare actual earnings against costs/time and plausible opportunity cost; don't infer revenue from review counts.

### VA-038 — Decide the game's long-term future
- Choose among small content update, localisation, art polish, discount strategy, expansion (only if supported by data), or moving to next SableInk commercial game.
- Archive production lessons, reusable UI/asset workflow, build/test templates, and marketing insights for the catalogue.

### VA-P5 gate
**Launch is supported, commercial results are understood, and the next product decision is evidence-based.**

---

## Risk register and early kill switches

| Risk | Earliest detection | Response |
| --- | --- | --- |
| Local AI cannot maintain character likeness / scene quality | VA-004/005 | Change process/style, reduce unique poses/scenes, or pause until an affordable lawful workflow exists; don't brute-force hundreds of inconsistent images. |
| Model licences or adult-content output rights are unclear | VA-005 | Don't ship affected outputs; document/commercially clear alternatives. |
| Steam rejects content / AI disclosure / adult presentation | VA-M03/VA-030 | Confirm rules early; revise content/store approach or evaluate viable alternative distribution. |
| Fantasy matching feels like busywork | VA-011/016 | Shorten decisions, show clear consequences, reduce repetitions, improve reward pacing. |
| Art count grows faster than production time | VA-018 | Hard asset budget; replace one planned asset for every additional asset. |
| User identity options multiply scene workload | VA-018/019 | Scope small cosmetic choices or authored variants; don't promise all route permutations. |
| Overengineering | Every phase | Prototype simplest rule, test, reject nice-to-have complexity. |
| Scope becomes a never-ending sandbox | VA-017/018 | Keep campaign milestones and ending mandatory. |
| Lack of marketing/wishlists | VA-M01/M04 | Test store hook and art early, not after release. |
| AI generation yields accidental artifacts / third-party lookalikes | VA-023/030 | Reject or rework before integration, keep provenance. |
| Real cost exceeds zero-budget expectations | VA-005/M03 | Record actual spend and decide if project remains financially viable before committing. |

## Simple recurring package workflow

For each task:
1. **Preflight:** read current docs, confirm previous gate and correct branch/files, list intended changes.
2. **Implement one bounded task** and preserve backups/commits.
3. **Verify:** automated checks for code; side-by-side comparison and author review for art; playtest for gameplay.
4. **Accept or reject:** record outcome with reproducible evidence. No silent promotions from "generated" to "approved".
5. **Sync:** update `PROGRESS.md`, relevant canonical document, `CHANGELOG.md` and commit. Use a new chat handoff pointing to these documents if needed.

**Mandatory definition of done for each feature:** starts from a clean build; works end-to-end; handles errors; doesn't break save/progression; readable at intended UI scales; author approves output; documentation/status matches reality.

## Immediate next three moves (in order)

1. **VA-001:** Agree the original look (eyes/linework/palette/expression) based on examples and one generated concept.
2. **VA-002:** Approve **one unnamed adult lead character** in non-explicit reference art.
3. **VA-003/004:** Build identity sheet and verify an expression + outfit + pose variation through local ComfyUI/Krita with consistent face.

**Do not begin bulk character creation, Steam spending, or game-engine expansion until the first art/identity feasibility gate is actually accepted.**

## Reference policy checks (as of 2026-11-06; verify again before submission)

- Steam Direct and waiting periods: https://partner.steamgames.com/steamdirect
- Mature and AI content survey: https://partner.steamgames.com/doc/gettingstarted/contentsurvey
- Store and build review: https://partner.steamgames.com/doc/store/Review_Process
- Release options and Coming Soon: https://partner.steamgames.com/doc/store/types
- Demos: https://partner.steamgames.com/doc/store/application/demos
