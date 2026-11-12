# MARS-Hardware-dev

**Multi-Agent Robotic Systems (MARS) — Hardware Platform Development & Documentation Repository**

- **Author:** Dhamdhawach Horsuwan
- **Current Phase:** `Phase 01: Requirements Engineering`
- **Primary Document Format:** `PDF` (with version history & change-list traceability)

[![Current Phase](https://img.shields.io/badge/Phase-Requirements%20Engineering-blue?style=flat-square)](#project-status)
[![Author](https://img.shields.io/badge/Author-Dhamdhawach%20Horsuwan-0284c7?style=flat-square)](#overview)
[![Document Format](https://img.shields.io/badge/Format-PDF-red?style=flat-square)](#active-specifications)
[![GitHub Pages](https://img.shields.io/badge/Portal-Launch%20Page-success?style=flat-square)](./index.html)

---

## Overview

**MARS-Hardware-dev** is the central repository for project tracking, hardware engineering documentation, and revision traceability for the **Multi-Agent Robotic Systems (MARS)** hardware platform.

When new specification or design documents are committed, the **GitHub Pages Launch Portal** ([index.html](./index.html)) surfaces the latest document versions while preserving direct references to older revisions and a complete changelog for end-to-end engineering traceability.

---

## Active Specifications

| Document ID | Title | Latest Version | Author | Files |
| :--- | :--- | :--- | :--- | :--- |
| **`MARS-REQ-001`** | **Research Needs — Multi-Agent Robotic Systems (MARS) Platform** | `v1.0` (Baseline) | Dhamdhawach Horsuwan | [PDF (v1.0)](./docs/latest/MARS-REQ-001_v1.0.pdf) · [Markdown Source](./docs/source/MARS-REQ-001_Research-Needs.md) |

---

## Project Status

| Phase | Milestone | Status | Primary Deliverable |
| :--- | :--- | :--- | :--- |
| **01** | **Requirements Engineering** | **In Progress** | Research Needs (`MARS-REQ-001`) & System Requirements Specification |
| **02** | Conceptual & Architecture Design | Planned | System Architecture & Interface Control (ICD) |
| **03** | Detailed Hardware Design | Planned | Mechanical CAD, Schematics, PCB Layout, BOM |
| **04** | Integration & Verification | Planned | Prototype Bring-up & Fleet Verification Reports |

---

## Repository Structure

```text
MARS-Hardware-dev/
├── docs/
│   ├── latest/                                 # Latest active PDF specifications
│   │   └── MARS-REQ-001_v1.0.pdf               # Research Needs (v1.0 PDF)
│   ├── archive/                                # Historical PDF versions kept for traceability
│   └── source/                                 # Editable Markdown source documents
│       └── MARS-REQ-001_Research-Needs.md
├── index.html                                  # GitHub Pages Launch Page & Document Portal
├── documents.json                              # Document registry, version history & changelogs
└── README.md                                   # Repository overview and workflow guide
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
  - `REQ` — Requirements Engineering (Research Needs, System & Hardware Requirements)
  - `ARC` — System Architecture & Interface Control (ICD)
  - `MEC` — Mechanical & Chassis Design
  - `ELE` — Electrical, Power & PCB Design
  - `SEN` — Sensors, Compute & Communication
- **`v<MAJOR>.<MINOR>`**:
  - `MAJOR`: Approved baseline release
  - `MINOR`: Iterative review draft or incremental update

### Traceability Workflow (Adding or Updating a Document)

1. **Place the new PDF** in `docs/latest/` (and move superseded versions to `docs/archive/`).
2. **Record the revision** in `documents.json` (or use the **+ New Revision Entry** button on `index.html`) with:
   - Version number and release date
   - Author (`Dhamdhawach Horsuwan`)
   - Detailed **Change List** summarizing added, modified, or refined requirements
   - Links to both the **latest PDF** and **archived versions**
3. **Commit and push** to the main branch. The GitHub Pages Launch Portal will automatically reflect the new release while maintaining full historical links.
