# Brand Evidence Log — CourseLi Brand Architecture Process

**Task:** REGISTER_EXISTING_BRAND_WORK
**Mission:** strategist-track | **Process:** brand-architecture
**Logged:** 2026-07-20
**Type:** Registration / indexing only — no new creative work performed.

---

## Evidence Entry

| Field | Value |
|---|---|
| **Source file** | `CourseLi-brand-identity.html` |
| **Format** | Standalone interactive HTML deck (self-contained, no build step) — 13 numbered sections, scroll-driven presentation |
| **Title** | CourseLi — Brand Identity System, Phase 1 |
| **Status** | ✅ Complete — Phase 1 brand identity. Design tokens explicitly pulled from the live product's `css/style.css` so doc and product can't drift apart. |
| **Classification** | Strategic + visual deliverable — covers naming, logo, typography, color, and application mockups in one artifact |

---

## Index of Contents (by section)

| # | Section | Content logged |
|---|---|---|
| 01 | Foundation — Company History | Origin (2021, Alger Centre), the problem (diploma/skills gap), the model (in-person, small cohorts, no video), current state (1,200+ students, 5 categories) |
| 02 | Direction — Vision | Company vision statement, business model (100% in-person, ≤25/cohort, WhatsApp-first support), brand promise |
| 03 | Exploration — Brainstorm | Field-vocabulary word list (bilingual FR/EN/AR terms the naming process drew from) |
| 04 | Candidates — Philosophy | **10 naming candidates evaluated and rejected/selected**, with rationale for each: MASSAR, TAKWIN, MAHARA, ATELIA, CURSA, NAJAHI, FORMATIS, SKILLA, PROGRESSA, and **COURSELI (selected)** |
| 05 | Decision — Naming | Naming rationale for CourseLi: bilingual construction (COURSE + Arabic لي "li"/mine), pronunciation logic across FR/EN/AR, deconstruction of both halves, mark concept (open ring = C / play triangle / progress ring) |
| 06 | Typography — Type System | Single-family decision (Inter), rationale (screen-native, one voice across marketing site + product), weight usage table (Light 300 / Medium 500 / Bold 700 / Black 900), type hierarchy specimens |
| 07 | Process — Logo Development | **3 logo directions explored and 2 rejected**: (1) C-as-open-book — rejected, expected; (2) C-as-mortarboard — rejected, backward-looking; (3) C-as-progress-ring+play — **selected**. Brand slogan (primary EN + secondary FR) |
| 08 | Result — Final Logo | Primary (blue-on-light), Reversed (white-on-dark), Mark-only versions and their approved use contexts |
| 09 | Identity — Color Palette | 4-color system (Blue #1558F6, Blue Dark #0D3FCC, Ink #0A0F1E, Blue Light #EEF3FF), rationale for the blue, usage ratios (White 55% / Blue 30% / Ink 10% / Blue Light 5%) |
| 10 | Symbol — Icon & Mark | Geometric logic of the mark (ring-opening angle = triangle angle, rounded terminals matching product UI radius), triple-reading rationale (C / play / progress), scale usage from billboard to 16px favicon |
| 11 | Typography System | Tabular numerals for stat displays, Arabic-companion typeface recommendation (Cairo/Tajawal/IBM Plex Sans Arabic) — flagged as **not yet adopted in production**, specimen only |
| 12 / 12b | Applications — Mockups | Business card, certificate, app icon, certificate seal, letterhead, email signature, student ID badge — photorealistic + flat mockups |
| 13 | Rules — Usage & Clear Space | Minimum clear space rule, 4 explicit "do not" rules (no distortion, no unapproved colors, no wordmark below 16px, no squared-off ring) |

---

## Cross-Check Against Existing Evidence Base

Searched all other uploaded process documents for references to brand-identity work to confirm no orphaned dependency. Result: **consistent, no conflicts, no missing links.**

| Reference found in other docs | Where | Relationship to this evidence |
|---|---|---|
| `REC-040` — "open brand & communication guide from a dedicated button" (🟢 MVP) | `courseli-فهرس-الوظائف-1-1.md` | Product-side consumer of the brand guide; the *content* of that guide is what this HTML doc defines |
| `MKT-017`–`MKT-021` — AI-assisted brand-guide builder, progressive refinement, asset upload, reception-guide derivation, publish/notify (all ⚪ unlabeled) | `courseli-فهرس-الوظائف-1-1.md` | Functional spec for the *tool* that would let a school build a brand guide like this one — this HTML doc is the reference example/output of that workflow, not a duplicate of it |
| `BrandGuide` entity (#41) — `structured_content`, `uploaded_assets`, `communication_guide`, `version`, `last_published_at` | `courseli-مخطط-البيانات-المنطقي-2-1.md` | Data model that would store a guide of this shape. Noted as a genuine gap fix ("سهو حقيقي صُحِّح الآن" — real oversight, now corrected), not related to the visual identity content itself |
| "دليل التواصل الخاص بالاستقبال مُشتق من BrandGuide" — reception comms tone deferred until BrandGuide ready | `CourseLi-العمل-بلا-انتظار.md` | Downstream dependency on the brand voice/tone this doc establishes (slogan, tone words) — no conflict, just a noted sequencing dependency already tracked elsewhere |

**Finding:** every cross-reference to "brand guide" elsewhere in the evidence base describes the *product feature* for schools to build their own brand guide (MKT-017–021) — a different, later-stage concern from CourseLi's own Phase-1 identity work indexed here. Nothing in `CourseLi-brand-identity.html` is referenced by any other file as unresolved or pending; the one explicitly flagged open item is internal to the doc itself (Arabic companion typeface — see below).

---

## Self-Reported Open Item (from within the source doc)

The brand doc flags exactly one item as not yet finalized, in its own words:

- **Arabic companion typeface** — recommended (Cairo, Tajawal, or IBM Plex Sans Arabic) but explicitly marked "not yet adopted in production," shown only as a typographic specimen (افتح إمكاناتك). This is a known, self-declared open point in the source artifact, not a gap in the evidence base — it doesn't need any evidence-base action, just carries forward as-is.

No other gaps identified. All naming candidates, the logo exploration history (including rejected directions), typography system, and color system are captured in the source document and now indexed above.

---

## Conclusion

`CourseLi-brand-identity.html` is registered as evidence for the **brand-architecture** process. The process is confirmed substantially complete: naming (10 candidates evaluated, 1 selected with rationale), logo (3 directions explored, 1 selected with rationale), typography, and color are all documented in the source file with no unresolved references elsewhere in the evidence base. No further creative work required at this time.