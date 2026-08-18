---
title: "FANR 3800: Week 2 Lecture Plan"
subtitle: "Arc A · Telling the spatial story"
author: "Dr. Tripp Lowe"
date: "Fall 2026 · Aug 24–28"
---

# Week 2 - Telling the Spatial Story

**Arc A: Build a base you can trust.** Two 50-minute lectures (Mon & Wed). Map communication is deliberate.  The theme: a map is an argument, and design determines whether the argument is believed.

*Notation: ArcGIS Pro tools appear as `ALL-CAPS`; methods and concepts as *Proper-Case italics*.*

---

## Monday: *Symbology*: Making Attributes Visible

**Learning objectives.** Students can (1) match a *Symbology* method to a data type, (2) explain how a symbology choice changes the story a map tells, and (3) avoid the common mis-readings caused by poor symbol choices.

**Session outline (~50 min).**

- *(0–10) Why symbology is analysis, not decoration.* Same data, two symbol schemes, two different conclusions.
- *(10–30) The main methods.*
  - *Single Symbol* (location only);
  - *Categorized* / *Unique Values* (qualitative classes, species, ownership, cover type);
  - *Graduated* (quantitative, age, basal area, density) and the effect of classification method and class breaks.
- *(30–45) Choosing well.* Color for categories vs. sequences; number of classes; when a choropleth misleads (raw counts vs. normalized rates); accessibility of color choices.
- *(45–50) Setup for Wednesday.* A well-symbolized layer still isn't a finished map (*Map Layout*).

*Tools introduced:* the `SYMBOLOGY` pane is a ribbon/pane workflow, not a geoprocessing tool.
*Methods/concepts introduced:* *Symbology* (*Categorized*, *Graduated*, *Unique Values*), *Cartographic Communication*.

---

## Wednesday: *Map Layout*: The Anatomy of a Credible Map

**Learning objectives.** Students can (1) list the essential map elements and their purposes, (2) understand the visual hierarchy so the main message reads first, and (3) export a publication-ready map with complete source information.

**Session outline (~50 min).**

- *(0–15) The essential elements.* Title, legend, scale bar, north arrow, neat collar, metadata (name, date, information about data sources). Why each exists and what a missing element costs the reader's trust.
- *(15–30) Composition and hierarchy.* the difference between a map made for a report page and one made for a wall.
- *(30–42) Credibility and honesty.* Scale and audience; how framing, extent, and class breaks can distort.
- *(42–50) Export and delivery.* Formats and resolution for print vs. screen via `EXPORT LAYOUT`; naming and file organization consistent with global naming conventions.

**Framing to emphasize.** Good design makes the spatial story clear; poor design obscures it and undermines the analyst's credibility.


*Tools introduced:* `EXPORT LAYOUT` (the `LAYOUT` view itself is a ribbon/pane workflow). *Methods/concepts introduced:* *Map Layout*, *Cartographic Communication*.
