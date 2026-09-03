<h1 align="center">Tarek Hasan</h1>

<p align="center">
<em>B.Sc. Mobility &amp; Logistics @ Rhine-Waal University of Applied Sciences (HSRW)<br>
Material-flow simulation · production logistics · enterprise systems</em>
</p>

<p align="center">
<img alt="Location" src="https://img.shields.io/badge/Kleve-Germany-1B4F9C?style=flat-square">
<img alt="Programme" src="https://img.shields.io/badge/B.Sc.-Mobility%20%26%20Logistics-005CA9?style=flat-square">
<img alt="Simulation" src="https://img.shields.io/badge/Siemens%20Tecnomatix-Plant%20Simulation%202404-0098A1?style=flat-square">
<img alt="SAP" src="https://img.shields.io/badge/SAP-S%2F4HANA%20certified-E67E22?style=flat-square">
<img alt="Methods" src="https://img.shields.io/badge/Methods-VDI%203633%20%C2%B7%20PERT%20%C2%B7%20SWOT-2E7D46?style=flat-square">
</p>

---

## About

I study **Mobility and Logistics** at Hochschule Rhein-Waal, and the work I care about sits where logistics meets software: building a model of how material actually moves through a production system, then testing it hard enough that the numbers survive someone else checking them.

Two rules run through every repository below.

- **A result that rests on one run is not a result.** Every accept-or-reject decision in my simulation work uses a five-observation mean. That rule is what caught a buffer configuration that passed on a lucky single run and failed by 53 parts on the mean.
- **The documentation has to let someone rebuild the work.** Each project ships the models, the source methods, the raw experiment tables and a click-by-click build guide — not just a report claiming it worked.

---

## Featured projects

### 🏭 [Rework Paint Shop Simulation](https://github.com/tarekhasan9828/rework-paint-shop-simulation) — discrete-event study of an automotive line

<p>
<img alt="Tool" src="https://img.shields.io/badge/Siemens%20Tecnomatix-Plant%20Simulation%202404-0098A1?style=flat-square">
<img alt="SimTalk" src="https://img.shields.io/badge/SimTalk-control%20methods-1B4F9C?style=flat-square">
<img alt="Method" src="https://img.shields.io/badge/VDI%203633-Part%201-2E7D46?style=flat-square">
<img alt="Semester" src="https://img.shields.io/badge/SS%202026-Group%205-005CA9?style=flat-square">
</p>

A 23-object model of an automotive rework paint shop — topcoat line, quality station, random-access rework store and ReRun loop — built and run to the VDI 3633 phase model to answer three questions **in that order**: can the line hit its throughput target, how slowly may the rework stations run and still hit it, and how little buffer capacity does it then need?

| Objective | Target | Achieved |
|---|---|---|
| Throughput | 16,907 parts/month | **16,917.8** (5-observation mean) |
| Rate | 53.00 UPH | **53.03 UPH** |
| Total rework process time *(maximise)* | — | **3,890 s** (+300 s over the safe start) |
| Total capacity *(minimise)* | 83 places | **67 places** (−16) |

**What I built.** The full model — buffers, stations, shift calendar, and the topcoat line represented as a parallel station of 8 × 62.5 s so that each part stays 500 s inside while one leaves every 62.5 s. Both SimTalk control methods: `QualityCheck`, which routes parts by colour-dependent rework probability that the built-in percentage strategy cannot express, and `DispatchRework`, the dispatcher that makes the rework store genuinely random-access rather than FIFO — with no connectors out of the store at all, so a part cannot structurally escape into the wrong lane.

**What I ran.** The coarse and refined `ExperimentManager` studies and their search ranges, the Prio 1–3 experiments, the part-by-part flow traces and warm-up handling behind verification, and the bottleneck analysis that put Major-Repair at 43.82 % of simulated working time — high, but with the target still met, so no unacceptable bottleneck remains.

➡️ Two model files · both SimTalk methods as readable source · raw experiment tables · ExperimentManager report · a click-by-click rebuild guide

<sub>Coursework with Group 5 (Logistic Simulations, SS 2026). The report and presentation stay unpublished — they carry personal university details — but every figure in them is reproduced in the repository README.</sub>

---

### 🎓 [HSRW UniCard](https://github.com/tarekhasan9828/HSRW-UniCard) — one credential for four campus services

<p>
<img alt="Module" src="https://img.shields.io/badge/Project%20Management%20%26%20Intercultural%20Competence-1B4F9C?style=flat-square">
<img alt="Semester" src="https://img.shields.io/badge/SS%202026-Group%206-005CA9?style=flat-square">
<img alt="Prototype" src="https://img.shields.io/badge/prototype-live-2E7D46?style=flat-square">
</p>

Student ID, Mensa payment, library access and VRR/NIAG transit are four separate credentials at HSRW today. This study unified them into one — an NFC card plus a digital wallet pass — designed, prototyped and evaluated end to end across a semester under a single constraint: **a phone with a dead battery must never lock a student out of their own campus.**

| | |
|---|---|
| **4 → 1** | services per credential |
| **27** | time-units on the critical path (σ 1.56) |
| **474 h** | logged against 440 planned (+7.7 %) |
| **20 / 25** | usability tasks completed unaided, rated 4.6 / 5 |

The concept, the architecture and the prototype all landed. What stopped live integration was not technical: the risk scored highest at kick-off — bureaucratic inertia, 16/25 — is exactly the one that materialised. It is written up as a failure rather than buried, because a risk register you never check against the outcome is decoration.

➡️ **[Live prototype](https://unicard-hsrw-main-1.vercel.app/portal)** · 20-page report · three presentations · Gantt workbook · full PERT calculation · five external usability-test records

---

## Certification

### SAP S/4HANA Exercise — SAP University Alliances / SAP UCC

<p>
<img alt="SAP" src="https://img.shields.io/badge/SAP-S%2F4HANA-0FAAFF?style=flat-square">
<img alt="Issuer" src="https://img.shields.io/badge/SAP%20University%20Alliances-UCC-E67E22?style=flat-square">
<img alt="Where" src="https://img.shields.io/badge/Hochschule%20Rhein--Waal-Summer%20semester%202025-005CA9?style=flat-square">
</p>

A minimum of 16 school hours of hands-on exercises on the SAP S/4HANA system, working in both **SAP GUI** and **SAP Fiori**, with the practice test passed.

| Module | Area |
|---|---|
| **MM** | Material Management |
| **SD** | Sales &amp; Distribution |
| **FI** | Finance |
| **PP** | Production and Planning |

<sub>Issued at Hochschule Rhein-Waal by Prof. Dr. Mona Wappler · Lecturer: Norbert Itgenshorst</sub>

---

## Toolbox

**Simulation &amp; modelling** · Siemens Tecnomatix Plant Simulation 2404 · SimTalk control methods · ExperimentManager designed experiments · VDI 3633 Part 1 · bottleneck and material-flow analysis · verification &amp; validation protocols

**Production logistics** · takt and capacity dimensioning · buffer sizing · shift-calendar modelling · availability and MTTR modelling · throughput and utilisation analysis

**Enterprise systems** · SAP S/4HANA (MM · SD · FI · PP) · SAP GUI · SAP Fiori

**Project management** · SMART objectives · work-package breakdown · Gantt baselining and planned-vs-actual control · PERT three-point estimation, forward and backward passes, slack and variance

**Analysis** · SWOT with weighted IFAS/EFAS scoring · Ishikawa 6M root-cause decomposition · stakeholder mapping · probability × impact risk registers

---

## What I'm focused on

Early-career work in **material-flow simulation** and **production and logistics planning** — the kind of problem where the answer is a number someone will act on, so the method behind it has to hold up. Currently extending that toward geoinformation systems and data-driven analysis alongside my studies.

---

<p align="center">
📍 Kleve, Germany · 🎓 Rhine-Waal University of Applied Sciences
</p>
