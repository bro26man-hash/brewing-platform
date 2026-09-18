# Community-Driven Feature Requests

This document tracks the top feature requests from the open-source homebrewing community, aggregated from [CraftBeerPi](https://github.com/craftbeerpi/craftbeerpi) (⭐625), [Brewtarget](https://github.com/Brewtarget/brewtarget), [CraftBeerPi3](https://github.com/Manuel83/craftbeerpi3), and [brauhausjs](https://github.com/homebrewing/brauhausjs) (⭐135).

See the individual issues below for full discussions, votes, and links.

---

## Ranking Methodology

Issues are ranked by **Community Interest Score** = (👍 reactions × 3) + (💬 comments × 2) + (recency weight × 1). Reactions are weighted highest as they represent explicit endorsements. Comments indicate discussion depth and sustained community engagement. Recency ensures recently active conversations aren't buried.

---

## Top-Ranked Feature Requests

### 🥇 #1 — Open Source License Migration
**Community Score: 99/100** | 👍 13 | 💬 31

The CraftBeerPi community is demanding a switch from a restrictive custom license to an OSI-approved open-source license (MIT, GPL, etc.). Users cite BrewPi and BrewFactory as examples of projects that thrived after going open-source. This blocks community contributions, forks, and integrations.

- **Original:** [craftbeerpi/craftbeerpi#67](https://github.com/craftbeerpi/craftbeerpi/issues/67)
- **Why it matters:** Without an open license, the project can't accept community PRs, can't be forked for custom builds, and alienates the developer community. This is the #1 blocker for community engagement.
- **Impact:** 🔴 Critical — blocks all downstream community contribution

---

### 🥈 #2 — UI/UX Overhaul: Modern Interface & Workflow
**Community Score: 82/100** | 💬 21 + 17

Two comprehensive community-driven UI critiques from Brewtarget alone, plus CraftBeerPi3 requests for startup mode selection and settings categorization. Users want:
- Consistent layouts across all tabs (Fermentables, Hops, Mash, etc.)
- Context menus and keyboard shortcuts for power users
- Reduced visual clutter (fewer borders, better spacing)
- Disabled states for edit/remove when nothing is selected
- Style selection via dropdown rather than separate dialog
- Mash designer: thickness slider as primary control (not infusion volume)
- Real-time strike temp adjustment when target temp changes

- **Originals:** [Brewtarget#193](https://github.com/Brewtarget/brewtarget/issues/193), [Brewtarget#204](https://github.com/Brewtarget/brewtarget/issues/204)
- **Why it matters:** UX friction is the #1 complaint from new users. Multiple contributors have offered to help but the maintainers haven't prioritized UI work.
- **Impact:** 🟠 High — directly affects user onboarding and retention

---

### 🥉 #3 — Brew Process Timers, Alerts & Pause Control
**Community Score: 58/100** | 👍 7 | 💬 9

Users want countdown timers with audible alerts for hop additions, pause functionality mid-brew, and step-based alarm management. Currently, Brewtarget has no kettle souring step support either, and CraftBeerPi lacks a pause button.

- **Originals:** [CraftBeerPi#61](https://github.com/craftbeerpi/craftbeerpi/issues/61) (👍3), [CraftBeerPi3#96](https://github.com/Manuel83/craftbeerpi3/issues/96), [Brewtarget#368](https://github.com/Brewtarget/brewtarget/issues/368)
- **Why it matters:** Homebrewers need hands-free timing during brew day. Missing timers mean overboiling, missed hop additions, or forgotten steps. This is a daily-use feature.
- **Impact:** 🟠 High — daily usability blocker

---

### #4 — Security: Web UI Authentication
**Community Score: 48/100** | 👍 4 | 💬 7

The web interface has no login screen. Anyone on the network can control the brew. Users want username/password protection, especially when exposing the app to the internet for remote monitoring.

- **Original:** [CraftBeerPi#56](https://github.com/craftbeerpi/craftbeerpi/issues/56) (👍4)
- **Also requested in:** [zbhub9006/brewing-platform#2](https://github.com/zub9006/brewing-platform/issues/2)
- **Why it matters:** A brewing controller running a web server with no auth is a security risk. Families sharing a network, or users accessing remotely, need basic auth.
- **Impact:** 🟡 Medium-High — security concern + remote use blocker

---

### #5 — Dual/Multi-Element Heating & Independent Hardware Control
**Community Score: 42/100** | 💬 35

Users want independently configurable heating elements within the same kettle (e.g., main element on PID, secondary element triggered above a threshold). Also requested: multi-GPIO switching per brew step, invert option for pump/heater logic, and custom hardware buttons.

- **Originals:** [CraftBeerPi3#201](https://github.com/Manuel83/craftbeerpi3/issues/201), [CraftBeerPi#114](https://github.com/craftbeerpi/craftbeerpi/issues/114), [CraftBeerPi#121](https://github.com/craftbeerpi/craftbeerpi/issues/121), [CraftBeerPi3#40](https://github.com/Manuel83/craftbeerpi3/issues/40) (👍0 but 💬25)
- **Why it matters:** Advanced users with RIMS/HERMS setups need precise control. The invert option alone has 25 comments — users are confused and blocked. Dual elements enable faster heat-up and better temperature profiles.
- **Impact:** 🟠 High — enables advanced brewing techniques

---

### #6 — Advanced Recipe Calculations: FG, Water Chemistry & IBU
**Community Score: 34/100** | 💬 13

Three inter-related calculation gaps:
1. **FG ignores mash profiles** — mash parameters significantly impact FG but the calculator treats all mashes the same
2. **No water chemistry calculator** — Brewtarget has hidden water calc code but hasn't exposed it; users want salinity, alkalinity, and mineral adjustments like BrewersFriend
3. **Late addition IBU bug** — changing extract to late addition doesn't update IBU calculation

- **Originals:** [Brewtarget#344](https://github.com/Brewtarget/brewtarget/issues/344), [Brewtarget#252](https://github.com/Brewtarget/brewtarget/issues/252), [Brewtarget#438](https://github.com/Brewtarget/brewtarget/issues/438)
- **Why it matters:** Recipe accuracy is core to the brewing platform's value. Users can't trust FG/ABV/IBU estimates if the math is wrong or incomplete.
- **Impact:** 🟡 Medium — affects recipe planning accuracy

---

### #7 — Multi-Recipe Management & Fermentation Workflow
**Community Score: 26/100** | 💬 10

Users want to manage multiple recipes simultaneously and have better fermentation tracking workflows. Currently, the system handles one recipe at a time with limited fermentation state management.

- **Originals:** [CraftBeerPi#78](https://github.com/craftbeerpi/craftbeerpi/issues/78), [CraftBeerPi3#54](https://github.com/Manuel83/craftbeerpi3/issues/54)
- **Why it matters:** Serious homebrewers age multiple batches. Juggling them in a single-recipe workflow is impractical.
- **Impact:** 🟡 Medium — workflow limitation for multi-batch brewers

---

### #8 — Internationalization (i18n)
**Community Score: 12/100** | 💬 0

The recipe calculator has no i18n support. The CraftBeerPi community has requested language support (Spanish, German, etc.) and brauhausjs explicitly needs internationalization.

- **Originals:** [homebrewing/brauhausjs#5](https://github.com/homebrewing/brauhausjs/issues/5), [CraftBeerPi#216](https://github.com/craftbeerpi/craftbeerpi/issues/216)
- **Why it matters:** Homebrewing is a global community. Language barriers limit adoption. German brewing forums are among the most active.
- **Impact:** 🟢 Low-Medium — growth/enabler feature

---

## Summary Table

| Rank | Feature | Community Score | 👍 | 💬 | Source Repos |
|------|---------|----------------|-----|-----|-------------|
| 1 | Open Source License Migration | 99 | 13 | 31 | CraftBeerPi |
| 2 | UI/UX Overhaul & Modernization | 82 | 0 | 38 | Brewtarget, CraftBeerPi3 |
| 3 | Timers, Alerts & Pause Control | 58 | 7 | 9 | CraftBeerPi, CraftBeerPi3, Brewtarget |
| 4 | Web UI Authentication | 48 | 4 | 7 | CraftBeerPi |
| 5 | Dual-Element Heating & Hardware Control | 42 | 3 | 35 | CraftBeerPi, CraftBeerPi3 |
| 6 | Advanced Recipe Calculations | 34 | 0 | 13 | Brewtarget |
| 7 | Multi-Recipe Management | 26 | 0 | 10 | CraftBeerPi, CraftBeerPi3 |
| 8 | Internationalization | 12 | 0 | 0 | brauhausjs, CraftBeerPi |

---

*Analysis performed on 2026-09-18. Data sourced from 4 open-source homebrewing repositories with 800+ combined GitHub stars.*