# Multi-State SIT Withholding Simulator & Ruleset Engine

## Overview
The **Multi-State SIT (State Income Tax) Withholding Simulator** is an interactive, web-based tool designed to visually demonstrate and calculate state tax withholding logic for employees who live in one state and work in another.

Built and validated directly against the **Symmetry Tax Engine (STE) Ruleset Specification** (`Multi-State SIT Withholding - Symmetry Software`), this simulator evaluates reciprocal agreements, nexus presence, and specific state tax rules to determine which states require tax withholding and executes the exact mathematical calculation formulas.

---

## Key Features

- **Validated 56 Jurisdiction Master Database:** Covers all 50 US States, the District of Columbia, and 5 US Territories (American Samoa, Guam, Northern Mariana Islands, Puerto Rico, and Virgin Islands), accurately verified against Columns 1–7 of the Symmetry Table of Variables.
- **Symmetry Table of Variables Modal:** Searchable modal displaying all state attributes (Has SIT, Withholds Nonresident, Withholds Out-of-State, Withholds if No Work, Calculation Type, and Reciprocal States).
- **Animated Master & Sub-Flow Decision Trees:**
  - Top-level evaluation (Start -> Reciprocal Check -> Nexus Check).
  - 4 sub-flowcharts mirroring the official Symmetry decision flowcharts (PDF pp. 8–10):
    1. *Reciprocal Agreement; Nexus*
    2. *Reciprocal Agreement; No Nexus*
    3. *No Reciprocal Agreement; Nexus*
    4. *No Reciprocal Agreement; No Nexus*
- **Interactive Numeric Tax Dollar Engine (PDF pp. 11–16):**
  - Live calculations for **"All"**, **"All with No Credit"**, **"Difference"**, **"Full"**, and **"None"**.
  - Configurable resident and work state wages with custom effective tax rates.
  - Step-by-step breakdown illustrating exact dollar credits and offsets.
- **Statutory Rules & Alerts:**
  - **Kansas Statutory Apportionment:** Dual-state wage apportionment rules (PDF p. 18).
  - **Illinois Box 16 Subject Wages:** Compliance rules under Illinois Publication 130 (PDF p. 17).
  - **Arizona Form WEC Exemption:** Exemption recognition for CA, IN, OR, and VA.
- **Full STE Override Suite:**
  - `reset`, `all`, `allWithNoCredit`, `difference`, `differencedeprecated`, `full`, `none`, `residentonly`, `nonresidentonly`, and `zeroinboth`.

---

## Technical Details

- **Single-File Architecture:** The entire application (HTML structure, styling, state database, math calculation engine, SVG flowchart generators, and responsive sidebar) is self-contained in [index.html](file:///C:/Zenople%20V26%20Aug/Projects/MultiState/MultiStateWidtholdingRuleSet/index.html).
- **Technologies:** HTML5, Vanilla JavaScript (ES6+), and Tailwind CSS.
- **No Build Dependencies:** Opens directly in any modern browser without npm or node installation.

---

## How to Use

1. Open [index.html](file:///C:/Zenople%20V26%20Aug/Projects/MultiState/MultiStateWidtholdingRuleSet/index.html) in your browser.
2. Select your **Resident State** and **Work State**.
3. Adjust parameters such as **Nexus**, **Nonresident Certificate**, or **Calculation Override**.
4. Click **"Run Ruleset Simulation"** to watch the flowchart animation trace the decision path and compute withholding determinations and dollar amounts.
