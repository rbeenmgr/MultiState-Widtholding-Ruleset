# Multi-State SIT Withholding Simulator

## Overview
The **Multi-State SIT (State Income Tax) Withholding Simulator** is an interactive, web-based tool designed to visually demonstrate and calculate state tax withholding logic for employees who live in one state and work in another. 

Built around the **Symmetry Software Ruleset**, this simulator evaluates reciprocal agreements, nexus presence, and specific state tax rules to determine which states require tax withholding and what the calculation method should be.

## Key Features

- **Interactive State Configuration:** Select any combination of a Resident State and a Work State from a comprehensive built-in US state database.
- **Animated Logic Flowchart:** Watch the decision-making process unfold in real-time. The simulator uses animated SVG paths to trace the exact logic route taken based on your inputs (e.g., checking for reciprocal agreements, evaluating nexus, and nonresident certificates).
- **Advanced Parameter Controls:**
  - **Nexus Toggles:** Force Nexus presence to be True, False, or Auto (based on resident/work state equality).
  - **Nonresident Certificates:** Test scenarios where an employee has filed a nonresident certificate in their work state.
  - **Calculation Overrides:** Force specific state calculation methods (e.g., Difference, Full, All, None) to bypass default rules.
  - **Desired Jurisdiction Matching:** Set a target tax jurisdiction (Resident only, Work only, Both, or None) and see if the ruleset allows for that outcome.
- **Detailed Results Panel:** Clearly displays the final withholding determination for both the Resident State and the Work State, including whether tax is withheld, reciprocity status, and the applied calculation type.

## Technical Details

- **Single-File Architecture:** The entire application (structure, styling, state database, and logic engine) is contained within a single HTML file (`MultiState Widtholding Ruleset.html`).
- **Technologies Used:**
  - **HTML5** & **Vanilla JavaScript** for the core logic and state management.
  - **Tailwind CSS** (via CDN) for a clean, modern, and responsive user interface.
  - **Inline SVG & CSS Animations** for the dynamic flowchart visualization.
- **State Master Database:** Hardcoded within the JavaScript is a `stateMaster` object containing properties for all 50 US states + DC, including rules for non-resident withholding, out-of-state withholding, calculation types, and specific reciprocal state pairs.

## How to Use
Simply open the `MultiState Widtholding Ruleset.html` file in any modern web browser. Use the left-hand configuration panel to set up your scenario, and click **"Run Animated Simulation"** to watch the logic execute and view the final withholding results.
