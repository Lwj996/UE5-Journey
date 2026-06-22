# UE5-Journey · Indie Co-op Horror Devlog

> **One person + AI building a small-scale co-op horror game in Unreal Engine 5, targeting Steam in 18 months.**
> Inspired by Lethal Company / REPO / Content Warning / Phasmophobia.

[![Status](https://img.shields.io/badge/status-active-brightgreen)]()
[![Phase](https://img.shields.io/badge/phase-0%20engine%20intro-blue)]()
[![Engine](https://img.shields.io/badge/UE-5.7-black)]()
[![Target](https://img.shields.io/badge/target-Steam%20by%202027--12-purple)]()

English | [简体中文](./README.zh-CN.md)

---

## About

I'm a **25-year-old frontend developer** with 3 years of React experience, pivoting into solo indie game dev. After two false starts (originally aiming for a remote gameplay-programmer job), I refocused on **2026-06-22**:

> **I'm not chasing a job offer. I'm building a game I want to ship on Steam.**

This repo is my public devlog: code, lessons, life-journal entries — all kept in one place so 5/10/30-year-future-me can read them.

**Background**
- 3 years professional frontend (JavaScript / React)
- Built a 2D game in Godot to near-completion (abandoned for lack of art — now AI-solved)
- Heavy player of co-op horror games (Lethal Company, REPO, Phasmophobia, Devour)
- Starting UE5 from scratch in April 2026

---

## The Real Goal

**Ship a small-scale 3D co-op horror game on Steam within 18 months** (target: 2027-12).

Reference titles:

| Game | Team size | Dev time | Result |
|---|---|---|---|
| Lethal Company | **1 person** | ~2 yrs side-project | ~$40M in 4 months |
| Content Warning | 9 ppl | ~1 yr | 6M downloads from a free 24h promo |
| REPO | small team | ~1.5 yr | 2025 Q1 hit |

The pattern: **4-8 player co-op · physics interaction · horror + comedy · low-poly art · solo-dev reachable**.

Full plan: [`docs/03-indie-coop-roadmap.md`](./docs/03-indie-coop-roadmap.md).

---

## 18-month Roadmap (high level)

| Phase | Months | Output |
|---|---|---|
| 0 · Engine intro | 2026-07 ~ 08 | 3 players walking around in a multiplayer level |
| 1 · Prototype #1 | 2026-09 ~ 10 | Minimal "pick up & return" core loop on itch.io |
| 2 · Prototype #2 | 2026-11 ~ 2027-01 | Add horror layer (dark, sound, 1 monster) |
| 3 · Demo v0 | 2027-02 ~ 06 | **Steam Next Fest entry** |
| 4 · Full release | 2027-07 ~ 12 | **Ship on Steam, $5-10** |

---

## Why "One Person + AI" Is Viable in 2026

| Task | AI tool |
|---|---|
| Code (BP / C++ debugging) | Cursor + Claude |
| Art (concept → 3D) | Midjourney → Meshy |
| Sound effects | ElevenLabs |
| Music | Suno / Udio |
| Trailer / store page | Runway / Veo + Claude |
| Localization | Claude |

Total tooling budget over 18 months: **~$1200**. Recoup point: ~200 copies at $5 on Steam.

---

## Weekly Pace (project-driven)

```
Workdays   1-2 evenings × 30-60min   (optional, bonus)
Saturday   ≥ 4h     (iron rule)
Sunday     3-5h
─────────────────────────────────
Total      8-12h / week (grows during project phases)
```

**Iron rule**: Saturday ≥ 4h. Without this the 18-month plan does not work.

---

## Roadmap

| Phase | Months | Focus |
|-------|--------|-------|
| 1. Foundations | 1 - 2 | Editor, Blueprint, Actor framework |
| 2. C++ Entry | 3 | UE-flavored C++ (UCLASS, UPROPERTY, UFUNCTION) |
| 3. First Real Project | 4 - 6 | Top-down Roguelike (playable + published) |
| 4. Industrial Skills | 7 - 9 | GAS, Replication, Unreal Insights |
| 5. Job Hunt | 10 - 12 | Portfolio polish, applications, interviews |

Full plan: [`docs/00-roadmap.md`](./docs/00-roadmap.md)

---

## Current Progress

- [x] Environment setup (UE 5.7 + Visual Studio 2022)
- [x] GitHub linked with Epic for source access
- [x] Editor basics: interface, view modes, snap, duplicate
- [x] **Direction confirmed (2026-06-22)**: solo indie co-op horror, not job-hunt
- [ ] Phase 0 · Finish first tutorial project end-to-end (target: weekend 6/27-6/28)
- [ ] Phase 0 · 3-player multiplayer "walk around" demo
- [ ] Phase 1 · First playable prototype on itch.io
- [ ] Phase 3 · Steam Next Fest entry
- [ ] **Phase 4 · Ship on Steam**

---

## Repo Map · 仓库导航

| I'm looking for... | Go to |
|---|---|
| Today's / a specific day's UE log | [`journal/`](./journal/) |
| Roadmap, weekly plan, project architecture | [`docs/`](./docs/) |
| Topic notes (UE concepts, C++, English vocab) | [`notes/`](./notes/) |
| AI tool reviews · industry observations · learning-method reflections | [`scratchpad/`](./scratchpad/) |
| **Life decisions · core fears · turning points** (kept for 5-30 years) | [`scratchpad/life/`](./scratchpad/life/) |
| Screenshots / GIFs / diagrams | [`assets/`](./assets/) |

Routing rules and authoring conventions: see [`AGENTS.md`](./AGENTS.md).

## Repository Structure

```
UE5-Journey/
├── docs/                 Long-form plans (roadmap, cadence, architecture)
├── journal/              Daily / weekly learning logs (bilingual)
├── notes/                Topic notes (UE concepts, C++, English vocab)
├── scratchpad/           Loose observations not tied to UE5 learning
│   └── life/             Life journal: decisions, fears, turning points
└── assets/               Images, GIFs, diagrams
```

---

## Tech Stack (focused for solo co-op horror)

**Engine**: Unreal Engine 5.7 · Blueprint-first · C++ only at bottlenecks
**Multiplayer**: Listen Server (2-4 players) · Online Subsystem Steam
**AI workflow**: Cursor · Claude · Midjourney · Meshy · ElevenLabs · Suno
**Tooling**: Visual Studio 2022 · Git · Steam Direct

**Intentionally NOT learning** (not needed for small co-op): Nanite/Lumen deep optimization · GAS · World Partition · console porting · anti-cheat.

---

## Contact

- GitHub: this page
- Email: _add yours_
- LinkedIn: _coming soon_

---

## License

Code snippets in this repository are released under the [MIT License](./LICENSE).  
Written notes are shared under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
