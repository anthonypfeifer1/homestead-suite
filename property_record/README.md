# Property Record

## What This Is

The property record is the single source of truth for everything
specific to one property. Every other piece of software in the
homestead suite reads from it. Nothing is hardcoded anywhere else.

If a value belongs to a specific property — location, climate,
soil type, jurisdiction, supplier region — it lives here and
only here.

## How It Works

The property record has two files per property:

**template.md** — the master field list. Every possible field
defined. No values filled in. Used to create a new property record.

**[property_name].md** — one file per real property. All fields
from the template filled in with real values for that property.

## The Substitution Rule

Every file in the suite that references a property-specific value
does so with a tag rather than a hardcoded value:

[PROPERTY RECORD: field_name]

When a new Claude session loads a file it reads the property record
first and substitutes all tagged values automatically. The file
logic stays generic. The property values stay in one place.

## Adding a New Property

1. Copy template.md
2. Rename it to [property_name].md
3. Fill in all fields — leave unknown fields blank,
   they will be flagged amber by the flag system
4. Save in this folder
5. Register the property name in registry.md

## International Use

The property record supports any country. The country field
drives everything — unit system, building code framework,
climate zone framework, electrical system, and which data
sources the site planner uses.

Adding a property in a new country requires:
1. A completed property record for that country
2. A regional file in cost_sourcing/regional/[country_code]/
3. Data source files in site_planner/data_sources/[country_code]/

No other files need to change.

## Files in This Folder

| File | Purpose |
|------|---------|
| README.md | This file — how the property record works |
| template.md | Master field list — copy to create new property |
| miami_county_ks.md | Kansas farm property — first real record |

## Flags

Fields left blank in a property record are flagged automatically
by the suite when that field is needed:

🟢 Complete — value present and verified
🟡 Missing — value needed, instructions provided
🔴 Blocking — value required before next step can proceed

The suite never stops the user from working. Missing fields
are flagged and tracked until resolved.

## Design Rules

This file is read first in every Claude session.
Every property-specific value lives here and nowhere else.
A value hardcoded anywhere else in the suite is an error.
One property = one file in this folder.
```

---

Once saved push it to GitHub:
```
cd ~/OneDrive/Desktop/homestead-suite
git add .
git commit -m "Add property_record README"
git push origin main