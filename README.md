# MARS-Hardware-dev

**Multi-Agent Robot System (MARS) — Hardware Platform Development & Documentation Repository**

[![Current Phase](https://img.shields.io/badge/Phase-Requirements%20Engineering-blue?style=flat-square)](#project-status)
[![Document Format](https://img.shields.io/badge/Format-PDF-red?style=flat-square)](#document-management--traceability)
[![GitHub Pages](https://img.shields.io/badge/Portal-Launch%20Page-success?style=flat-square)](./index.html)

---

## Overview

**MARS-Hardware-dev** is the central repository for project tracking, hardware engineering documentation, and revision traceability for the **Multi-Agent Robot System (MARS)** hardware platform.

When new specification or design documents are committed, the **GitHub Pages Launch Portal** (`index.html`) surfaces the latest document versions while preserving direct references to older revisions and a complete changelog for end-to-end engineering traceability.

---

## Project Status

> **Current Phase:** `Requirements Engineering`

| Phase | Milestone | Status | Primary Deliverable |
| :--- | :--- | :--- | :--- |
| **01** | **Requirements Engineering** | **In Progress** | System & Subsystem Requirements Specification (SRS / HRS) |
| **02** | Conceptual & Architecture Design | Planned | System Architecture & Trade-off Analysis |
| **03** | Detailed Hardware Design | Planned | Mechanical CAD, Schematics, PCB Layout, BOM |
| **04** | Integration & Verification | Planned | Prototype Bring-up & Hardware Verification Reports |

---

## Repository Structure

```text
MARS-Hardware-dev/
├── docs/
│   ├── latest/                 # Latest active PDF specifications
│   └── archive/                # Historical PDF versions kept for traceability
├── index.html                  # GitHub Pages Launch Page & Document Portal
├── documents.json              # Document registry, version history & changelogs
└── README.md                   # Repository overview and workflow guide
```

---

## Document Management & Traceability

All primary engineering deliverables are published and archived in **PDF format** to guarantee layout fidelity across reviews and manufacturing handoffs.

### Versioning Convention

Documents follow the naming convention:

```text
MARS-<CATEGORY>-<DOC_ID>_v<MAJOR>.<MINOR>.pdf
```

- **`<CATEGORY>`**:
  - `REQ` — Requirements Engineering (System & Hardware Requirements)
  - `ARC` — System Architecture & Interface Control (ICD)
  - `MEC` — Mechanical & Chassis Design
  - `ELE` — Electrical, Power & PCB Design
  - `SEN` — Sensors, Compute & Communication
- **`v<MAJOR>.<MINOR>`**:
  - `MAJOR`: Approved baseline release
  - `MINOR`: Iterative review draft or incremental update

### Traceability Workflow (Adding or Updating a Document)

1. **Place the new PDF** in `docs/latest/` (and move superseded versions to `docs/archive/`).
2. **Record the revision** in `documents.json` (or the `DOCUMENT_REGISTRY` inside `index.html`) with:
   - Version number and release date
   - Author / reviewer metadata
   - Detailed **Change List** summarizing added, modified, or deprecated requirements
   - Links to both the **latest PDF** and **archived versions**
3. **Commit and push** to the main branch. The GitHub Pages Launch Portal will automatically reflect the new release while maintaining full historical links.

---

## Launch Portal (GitHub Pages)

The interactive launch page ([index.html](./index.html)) provides:

- **Active Baseline Spotlight**: Quick access and inline preview for the latest Requirements Engineering PDF documents.
- **Version History & Traceability Matrix**: Expandable revision history for every document with side-by-side changelog notes and links to archived PDFs.
- **Category & Keyword Filtering**: Filter specifications by subsystem (`REQ`, `ARC`, `MEC`, `ELE`, `SEN`) or search across changelogs.
- **Built-in PDF Preview**: Inspect documents directly inside the browser or download them for offline review.

### Enabling GitHub Pages

1. Go to your repository on GitHub -> **Settings** -> **Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Select the `main` branch and `/ (root)` folder, then click **Save**.
