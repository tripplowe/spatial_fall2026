---
title: "FANR 3800: Week 1 Lecture Plan"
subtitle: "Arc A · Why does everything have a spatial component?"
author: "Dr. Tripp Lowe"
date: "Fall 2026 · Aug 17–21"
---

# Week 1 - All Things Have a Spatial Component?

**Arc A: Build a base you can trust.** Two 50-minute lectures (Mon & Wed). Week 1 sets the intellectual frame for the whole semester and plants the vocabulary (spatial data, the two data models) that every later arc reuses. It is also the setup week, so protect a few minutes for the ESRI environment.

*Notation: ArcGIS Pro tools appear as `ALL-CAPS`; methods and concepts as *Proper-Case italics*.*

---

## Monday: What GIS Is, and Why Your Problems Are Spatial

**Learning objectives.** Students can (1) state what GIS is as an analytical framework rather than a program, (2) give an example from their own discipline where a management question is really a spatial question, and (3) describe how the course's five arcs move from data to decision.

**Session outline (~50 min).**

- *(0–10) The hook.* Open with a management question from each Warnell track, "Which stands should we thin?" (silviculture), "Where is the deer herd concentrating?" (wildlife), "Which reaches need streamside protection?" (fisheries), "Where are trails eroding?" (parks). Draw out that each contains a hidden *where*.
- *(10–25) What GIS actually is.* Data + software + methods + people for asking and answering spatial questions. Distinguish the *analytical framework* from the *software*; ArcGIS Pro is one tool for a way of thinking.
- *(25–40) The course as a story.* Walk the five arcs at one sentence each: build a trustworthy base (A) → ask questions of data (B) → decide where things go, vector (C) → model conditions that vary, raster (D) → combine everything (E). Emphasize that tools serve questions, not the reverse.
- *(40–50) Logistics.* Syllabus highlights, the lecture/lab rhythm, the weekly ESRI-module expectation, and how notes/handwritten work fit in. Assign the Week 2 ESRI module and the account setup.

**Framing to emphasize.** "Every natural resource decision has a spatial component." Return to this sentence all semester.

*Tools introduced:* none, project creation and interface navigation only. *Methods/concepts introduced:* *Spatial Thinking*.

---

## Wednesday: How We Represent the World: The Two Data Models

**Learning objectives.** Students can (1) distinguish discrete features from continuous phenomena, (2) name the vector geometry types and the raster grid concept, and (3) predict which model fits a given natural resource dataset.

**Session outline (~50 min).**

- *(0–5) Setup check.* Confirm ESRI accounts and ArcGIS Pro access; note who needs the GIS lab. Flag that unresolved access must be fixed before Week 2.
- *(5–25) The *Vector Data Model*.* Points, lines, polygons, each carrying an attribute table (one row per feature). Natural resource examples: sample plots and nests (points); streams, roads, boundaries (lines); stands, compartments, watersheds (polygons). Strengths (discrete features, attribute richness, precise edges) and limits (poor for gradients).
- *(25–40) The *Raster Data Model*.* A regular grid of cells, one value each; cell size = *Spatial Resolution*; integer (categories) vs. floating-point (continuous) vs. multiband (imagery). Examples: elevation, temperature, land cover, satellite bands. Strengths (continuous phenomena, fast math across large areas) and limits (jagged boundaries, one value per cell).
- *(40–50) Choosing a model.* Discrete-with-hard-edges → vector; gradient or many-factor surface → raster; most real problems → both. Preview that Arcs A–C live mostly in vector and Arc D introduces raster in earnest.

**Framing to emphasize.** The model you choose is a modeling *decision* with consequences, not a technical default. Plant the vector↔raster parallel now so it pays off in Arc D.

**Connections.** Vocabulary here underpins every week; the vector/raster choice returns explicitly in Weeks 9–12.

*Tools introduced:* none, interface navigation only. *Methods/concepts introduced:* *Vector Data Model*, *Raster Data Model*, *Spatial Resolution*.
