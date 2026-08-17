---
title: "FANR 3800: Week 2 Lecture Plan"
subtitle: "Arc A · Telling the spatial story"
author: "Dr. Tripp Lowe"
date: "Fall 2026 · Aug 24–28"
---

# Week 2 - Telling the Spatial Story

**Arc A: Build a base you can trust.** Two 50-minute lectures (Mon & Wed). Map communication is taught early, deliberately, so students can present every subsequent analysis credibly. The theme: a map is an argument, and design determines whether the argument is believed.

*Notation: ArcGIS Pro tools appear as `ALL-CAPS`; methods and concepts as *Proper-Case italics*.*

---

## Monday: *Symbology*: Making Attributes Visible

**Learning objectives.** Students can (1) match a *Symbology* method to a data type, (2) explain how a symbology choice changes the story a map tells, and (3) avoid the common misreadings caused by poor symbol choices.

**Session outline (~50 min).**

- *(0–10) Why symbology is analysis, not decoration.* Same data, two symbol schemes, two different conclusions. Set up the responsibility that comes with representation.
- *(10–30) The main methods.* *Single Symbol* (location only); *Categorized* / *Unique Values* (qualitative classes, species, ownership, cover type); *Graduated* (quantitative, age, basal area, density) and the effect of classification method and class breaks. Tie each to a data type from Week 1's attribute tables.
- *(30–45) Choosing well.* Color for categories vs. sequences; number of classes; when a choropleth misleads (raw counts vs. normalized rates); accessibility of color choices.
- *(45–50) Setup for Wednesday.* A well-symbolized layer still isn't a finished map, preview *Map Layout*.

**Framing to emphasize.** Landowners and stakeholders act on the map, not the attribute table. *Symbology* is where the data becomes a decision.

*Tools introduced:* none, the `SYMBOLOGY` pane is a ribbon/pane workflow, not a geoprocessing tool. *Methods/concepts introduced:* *Symbology* (*Categorized*, *Graduated*, *Unique Values*), *Cartographic Communication*.

---

## Wednesday: *Map Layout*: The Anatomy of a Credible Map

**Learning objectives.** Students can (1) list the essential map elements and justify each, (2) apply visual hierarchy so the main message reads first, and (3) export a publication-ready map with complete source information.

**Session outline (~50 min).**

- *(0–15) The essential elements.* Title, legend, scale bar, north arrow, and, emphasized, data source and coordinate system metadata. Why each exists and what a missing element costs the reader's trust.
- *(15–30) Composition and hierarchy.* Guiding the eye: figure-ground, balance, what to enlarge and what to subordinate; the difference between a map made for a report page and one made for a wall.
- *(30–42) Credibility and honesty.* Scale and audience; how framing, extent, and class breaks can distort; the professional obligation to represent uncertainty and cite sources.
- *(42–50) Export and delivery.* Formats and resolution for print vs. screen via `EXPORT LAYOUT`; naming and file organization consistent with the course conventions.

**Framing to emphasize.** Good design makes the spatial story clear; poor design obscures it and undermines the analyst's credibility. This is the deliverable skill every arc ends on.

**Connections.** Every arc culminates in a map or summary; the elements introduced here are expected on all lab deliverables and exams.

*Tools introduced:* `EXPORT LAYOUT` (the `LAYOUT` view itself is a ribbon/pane workflow). *Methods/concepts introduced:* *Map Layout*, *Cartographic Communication*.
