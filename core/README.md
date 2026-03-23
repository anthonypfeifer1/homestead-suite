# Core — Homestead Suite

## What This Folder Is

The core folder contains the rules, protocols, and shared
systems that every piece of software in the suite follows.
Every file in every other folder reads from core.
Nothing in core is property-specific.
Nothing in core is building-style-specific.
Core is the foundation everything else is built on.

## Files in This Folder

| File | Purpose |
|------|---------|
| README.md | This file — what core is and how it works |
| flag_rules.md | Amber and red flagging system used by all tools |
| user_roles.md | User tiers, permissions, multi-tenant rules |
| glossary.md | Universal trade term glossary — tooltip system |
| session_handoff.md | How to start a new Claude session |
| github_sync.md | Repository structure and push process |
| data_backup.md | Backup triggers and recovery process |
| prompt_governance.md | When and how Claude is called |
| validation/ | Testing and compliance validation |

## The Design Rules

These rules govern every file written in the suite.
A new file that violates a design rule is an error.

Rule 1 — One project = one structure
  All structures live beneath the homestead wrapper.
  Never duplicate the wrapper.

Rule 2 — Load only what the current task requires
  Never load the full suite in one session.
  The property record is always loaded first.
  Then only the files relevant to the current task.

Rule 3 — Every branch has three matched files
  branch file — construction logic
  roof file — roof design logic for that style
  visual file — appearance and rendering for that style
  Written together. Registered together. Tested together.
  A branch without all three files is incomplete.

Rule 4 — Base branches define structure above grade
  Modifiers define what gets added to any branch.
  Never put modifier logic inside a base branch.
  Never put base branch logic inside a modifier.

Rule 5 — Form modifiers first, function modifiers second
  Form modifiers define physical attachment.
  Function modifiers define zone purpose.
  They stack in pairs — form first, function second.

Rule 6 — Visualization is bidirectional
  Every visual change updates the data model.
  Every data model change updates the visual.
  They are always in sync.
  There is no one-way relationship between
  answers and the building.

Rule 7 — Roof manipulation is first class
  Every roof handle connects to the structural layer,
  the compliance layer, the cost layer,
  and the pre-pour document simultaneously.
  A roof change that affects the foundation must be
  visible in the foundation view before the user
  releases the handle.

Rule 8 — Claude is called at development time only
  Claude is never called automatically during
  user interaction.
  Anything that can be a lookup table should be
  a lookup table.
  Anything that can be pure calculation should be
  pure calculation.
  Reserve Claude calls for decisions that genuinely
  require intelligence — not ones that require
  arithmetic.

Rule 9 — User is always in the loop
  The software assembles prompts from project data.
  The user copies the prompt to Claude.ai.
  The user pastes the response back.
  The software parses the response automatically.
  Nothing is sent to Claude without the user seeing it.
  Nothing comes from Claude without the user
  reviewing it.

Rule 10 — Only legitimate data sources
  Public APIs with documented terms of use.
  User-initiated Claude.ai sessions with web browsing.
  Data entered directly by the user.
  No scraping. No disguised requests.
  No terms of service violations.

Rule 11 — Missing data generates a request sheet
  When data cannot be gathered automatically
  the software generates a structured request
  document for the user to send to the source.
  No data request goes out without a clear path
  for the answer to come back in.

Rule 12 — All quotes normalized before comparison
  Every material has a defined unit conversion path.
  Supplier quotes are always normalized to project
  units before comparison.
  The user sees consistent units — always.
  No comparison is presented until all quotes are
  expressed in the same unit.

Rule 13 — Every supplier interaction compounds
  Supplier behavior knowledge is regional and shared
  across projects.
  Customer quote data is private.
  Price history is never discarded.
  The suite gets smarter with every quote.

Rule 14 — Nothing blocks unless it absolutely must
  The user is always moving forward.
  The system tracks what is unresolved.
  Nothing is hidden.
  🔴 Red flags block only when physically or
  legally required.
  🟡 Amber flags warn but never block.
  🟢 Green means complete and verified.

Rule 15 — The property record is the single source
  of truth for all property-specific values.
  A value hardcoded anywhere else in the suite
  is an error.
  Tag format: [PROPERTY RECORD: field_name]

## The Pipeline
```
Site Planner → Space Planner → Structural → Homestead Planner
     [0]            [1]            [2]              [3]
          ↓               ↓              ↓                ↓
     Cost & Sourcing → Document Generator → Build Tracker
          [4]                  [5]               [6]

     Compliance runs alongside all pieces.
     Visualization updates at every stage.
```

## How to Start a New Session

1. Paste the session startup prompt from
   core/session_handoff.md into a new Claude chat
2. Claude reads the property record and confirms context
3. Claude identifies the next file to write
4. Write files in the order defined in session_handoff.md
5. Push to GitHub after every file

## How to Add a New Building Style

1. Invoke the Branch Generator in a new Claude session
2. Claude writes three matched files:
   homestead_planner/branches/[style].md
   structural/roof/styles/[style]_roof.md
   visualization/styles/[style]_visual.md
3. Register all three in registry.md
4. Push to GitHub

## How to Add a New Modifier

1. Invoke the Modifier Generator in a new Claude session
2. Declare whether it is a form or function modifier
3. Claude writes the modifier file
4. Register in registry.md
5. Push to GitHub

## Version

core_version: 1.0
created: 2026-03-22
created_by: Anthony Pfeifer + Claude
last_updated: 2026-03-22
changelog: core/changelog.md