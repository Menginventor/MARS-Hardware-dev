# MARS-Hardware-dev

**Multi-Agent Robotic Systems (MARS) — Hardware Platform Development & Documentation Repository**

- **Author:** Dhamdhawach Horsuwan
- **Current Phase:** `Phase 01: Requirements Engineering`
- **Primary Document Format:** `PDF` (with version history & change-list traceability)

[![Current Phase](https://img.shields.io/badge/Phase-Requirements%20Engineering-E97F1D?style=flat-square)](#project-status)
[![Author](https://img.shields.io/badge/Author-Dhamdhawach%20Horsuwan-293952?style=flat-square)](#overview)
[![Document Format](https://img.shields.io/badge/Format-PDF-379DC0?style=flat-square)](#active-specifications)
[![GitHub Pages](https://img.shields.io/badge/Portal-Launch%20Page-293952?style=flat-square)](./index.html)

---

## Overview

**MARS-Hardware-dev** is the central repository for project tracking, hardware engineering documentation, and revision traceability for the **Multi-Agent Robotic Systems (MARS)** hardware platform.

When new specification or design documents are committed, the **GitHub Pages Launch Portal** ([index.html](./index.html)) surfaces the latest document versions while preserving direct references to older revisions and a complete changelog for end-to-end engineering traceability.

---

## Active Specifications

| Document ID | Title | Latest Version | Author | Files |
| :--- | :--- | :--- | :--- | :--- |
| **`MARS-REQ-001`** | **Stakeholder Needs and Requirements** | `v1.0` (Baseline) | Dhamdhawach Horsuwan | [PDF (v1.0)](./docs/latest/MARS-REQ-001_v1.0.pdf) · [Markdown Source](./docs/source/MARS-REQ-001_Stakeholder-Needs-and-Requirements.md) |
| **`MARS-REQ-002`** | **Concept of Operations (CONOPS): Requirements for a Mobile Robot Platform in MARS Research** | `v1.0` (Baseline) | Dhamdhawach Horsuwan | [PDF (v1.0)](./docs/latest/MARS-REQ-002_v1.0.pdf) · [Markdown Source](./docs/source/MARS-REQ-002_CONOPS.md) |

---

## Project Status

| Phase | Milestone | Status | Primary Deliverable |
| :--- | :--- | :--- | :--- |
| **01** | **Requirements Engineering** | **In Progress** | Stakeholder Needs (`MARS-REQ-001`), CONOPS (`MARS-REQ-002`) & System Requirements |
| **02** | Conceptual & Architecture Design | Planned | System Architecture & Interface Control (ICD) |
| **03** | Detailed Hardware Design | Planned | Mechanical CAD, Schematics, PCB Layout, BOM |
| **04** | Integration & Verification | Planned | Prototype Bring-up & Fleet Verification Reports |

---

## Platform Color Scheme

The MARS hardware platform, documentation deliverables, and web portal follow a standardized industrial color palette:

| Color | HEX | Application |
| :--- | :--- | :--- |
| **Arctic White** | `#F6F6F5` | Primary armor |
| **Deep Navy** | `#293952` | Secondary armor |
| **Research Blue** | `#379DC0` | Technical accents |
| **Engineering Orange** | `#E97F1D` | Safety markings |

---

## Repository Structure

```text
MARS-Hardware-dev/
├── docs/
│   ├── latest/                                             # Latest active PDF specifications
│   │   ├── MARS-REQ-001_v1.0.pdf                           # Stakeholder Needs and Requirements (v1.0 PDF)
│   │   └── MARS-REQ-002_v1.0.pdf                           # Concept of Operations - CONOPS (v1.0 PDF)
│   ├── archive/                                            # Historical PDF versions kept for traceability
│   └── source/                                             # Editable Markdown source documents
│       ├── MARS-REQ-001_Stakeholder-Needs-and-Requirements.md
│       └── MARS-REQ-002_CONOPS.md
├── index.html                                              # GitHub Pages Launch Page & Document Portal
├── documents.json                                          # Document registry, version history & changelogs
└── README.md                                               # Repository overview and workflow guide
```

---

## Document Management & Traceability

All primary engineering deliverables are published and archived in **PDF format** to guarantee layout fidelity across reviews and hardware handoffs.

### Versioning Convention

Documents follow the naming convention:

```text
MARS-<CATEGORY>-<DOC_ID>_v<MAJOR>.<MINOR>.pdf
```

- **`<CATEGORY>`**:
  - `REQ` — Requirements Engineering (Stakeholder Needs, CONOPS, System & Hardware Requirements)
  - `ARC` — System Architecture & Interface Control (ICD)
  - `MEC` — Mechanical & Chassis Design
  - `ELE` — Electrical, Power & PCB Design
  - `SEN` — Sensors, Compute & Communication
- **`v<MAJOR>.<MINOR>`**:
  - `MAJOR`: Approved baseline release
  - `MINOR`: Iterative review draft or incremental update

### Traceability Workflow (Adding or Updating a Document via Git)

1. **Place the new PDF** in `docs/latest/` (and move superseded versions to `docs/archive/`).
2. **Record the revision** in `documents.json` with:
   - Version number and release date
   - Author (`Dhamdhawach Horsuwan`)
   - Detailed **Change List** summarizing added, modified, or refined requirements
   - Links to both the **latest PDF** and **archived versions**
3. **Commit and push** via Git to the `main` branch. The GitHub Pages Launch Portal will automatically reflect the new release while maintaining full historical links.
