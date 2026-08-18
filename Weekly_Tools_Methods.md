---
title: "FANR 3800: Weekly ArcGIS Pro Tools & Methods"
subtitle: "Tools and methods introduced each week (ArcGIS Pro v3.7x)"
author: "Dr. Tripp Lowe"
date: "Fall 2026"
---

# Weekly ArcGIS Pro Tools & Methods

Tracks the ArcGIS Pro **tools** and the **methods/concepts** *first introduced* each week (not cumulative). Target software: **ArcGIS Pro v3.7x**.

## Notation Convention (Applies to All Course Documents)

- **ArcGIS Pro tools** are written in `ALL-CAPS INSIDE BACKTICKS`, e.g. `BUFFER`, `SELECT BY LOCATION`, `RASTER CALCULATOR`.
- **Methods and concepts** (things you *do* or *understand*, not a specific tool) are written in *Proper-Case Italics*, e.g. *Digitizing*, *Attribute Query*, *Map Algebra*.

## Verification Note

Tool names below are standard ArcGIS Pro geoprocessing tool names. **Verify spelling, toolbox location, license level, and the `PAIRWISE` vs. classic variant against your v3.7x install** before finalizing, these change across versions. Items marked *(ribbon/pane)* are interactive workflows on a ribbon or pane rather than a single geoprocessing tool.

---

## Arc A: Build a Base You Can Trust

| Wk | ArcGIS Pro tools (`ALL-CAPS`) | Methods & concepts (*Proper-Case italic*) |
|----|-------------------------------|--------------------------------------------|
| 1 | *(none, project creation & interface navigation)* | *Spatial Thinking*, *Vector Data Model*, *Raster Data Model* |
| 2 | *(none, `SYMBOLOGY` pane & `LAYOUT` view are ribbon/pane; `EXPORT LAYOUT`)* | *Symbology* (*Categorized*, *Graduated*, *Unique Values*), *Map Layout*, *Cartographic Communication* |
| 3 | `PROJECT`, `DEFINE PROJECTION` | *Coordinate System Specification*, *Datum Transformation*, *Projection Selection* |
| 4 | `CREATE FEATURES` *(editing, ribbon/pane)*, `GPX TO FEATURES`, `XY TABLE TO POINT`, `GEOREFERENCE` *(ribbon toolset)* | *Digitizing*, *Vector Editing*, *GPS Data Collection* (*Static*, *Dynamic*), *Air-Photo Interpretation*, *Georeferencing* |

---

## Arc B: Ask Questions of Your Data

| Wk | ArcGIS Pro tools (`ALL-CAPS`) | Methods & concepts (*Proper-Case italic*) |
|----|-------------------------------|--------------------------------------------|
| 5 | `SELECT BY ATTRIBUTES` (`SELECT LAYER BY ATTRIBUTE`), `SELECT BY LOCATION` (`SELECT LAYER BY LOCATION`), `ADD JOIN`, `CALCULATE GEOMETRY`, `SUMMARY STATISTICS` | *Attribute Query*, *Spatial Query*, *Table Join*, *Inventory Summary*, *Area Calculation* |

---

## Arc C: Where Should Something Happen? (Vector)

| Wk | ArcGIS Pro tools (`ALL-CAPS`) | Methods & concepts (*Proper-Case italic*) |
|----|-------------------------------|--------------------------------------------|
| 6 | `BUFFER` (`PAIRWISE BUFFER`), `CLIP` (`PAIRWISE CLIP`), `ERASE` (`PAIRWISE ERASE`) | *Proximity Analysis*, *Constraint Application*, *Feature Extraction*, *Dissolve* |
| 7 | `INTERSECT` (`PAIRWISE INTERSECT`), `UNION`, `UPDATE` | *Topological Overlay*, *Cross-Tabulation*, *Multi-Criteria Combination* |
| 8 | `MODELBUILDER` *(workflow documentation; optional)* | *Workflow Decomposition*, *Problem-to-Workflow Translation*, *Analysis Verification*, **Lecture Exam 1 (Wed)** |

---

## Arc D: Conditions That Vary Across the Land (Raster)

| Wk | ArcGIS Pro tools (`ALL-CAPS`) | Methods & concepts (*Proper-Case italic*) |
|----|-------------------------------|--------------------------------------------|
| 9 | *(none, raster display & `RASTER PROPERTIES`; Spatial Analyst environment)* | *Raster Data Model* (in depth), *Spatial Resolution*, *Cell Size Selection*, **Lab Exam 1 (Wed/Thu)** |
| 10 | `RECLASSIFY`, `EUCLIDEAN DISTANCE` | *Reclassification*, *Distance Surface*, *Binary Suitability* |
| 11 | `SLOPE`, `ASPECT`, `HILLSHADE` | *Terrain Analysis*, *Surface Derivatives* |
| 12 | `RASTER CALCULATOR`, `WEIGHTED OVERLAY` | *Map Algebra*, *Weighted Overlay*, *Suitability Modeling* |
| 13 | `CLASSIFICATION WIZARD` *(Imagery ribbon)*, `CLASSIFY RASTER`, `TRAIN ... CLASSIFIER` | *Image Interpretation*, *Supervised Classification*, *Unsupervised Classification*, *Change Detection* |

---

## Arc E: Real Problems Mix Everything

| Wk | ArcGIS Pro tools (`ALL-CAPS`) | Methods & concepts (*Proper-Case italic*) |
|----|-------------------------------|--------------------------------------------|
| 14 | `FEATURE TO RASTER`, `POLYGON TO RASTER`, `RASTER TO POLYGON`, `EXTRACT BY MASK` | *Data Model Conversion*, *Integrated Workflow*, *Scenario Analysis*, **Lecture Exam 2 (Wed); Lab Exam 2 (Wed/Thu)** |
| 15 | *(Thanksgiving, no class)* | - |
| 16 | *(none, synthesis & course overview)* | *Method Selection & Sequencing*, *Synthesis* |

---

## Quick Alphabetical Tool Index

For fast lookup of where each tool first appears.

| Tool | First introduced |
|------|------------------|
| `ADD JOIN` | Wk 5 |
| `ASPECT` | Wk 11 |
| `BUFFER` / `PAIRWISE BUFFER` | Wk 6 |
| `CALCULATE GEOMETRY` | Wk 5 |
| `CLASSIFICATION WIZARD` / `CLASSIFY RASTER` | Wk 13 |
| `CLIP` / `PAIRWISE CLIP` | Wk 6 |
| `CREATE FEATURES` | Wk 4 |
| `DEFINE PROJECTION` | Wk 3 |
| `ERASE` / `PAIRWISE ERASE` | Wk 6 |
| `EUCLIDEAN DISTANCE` | Wk 10 |
| `EXTRACT BY MASK` | Wk 14 |
| `FEATURE TO RASTER` | Wk 14 |
| `GEOREFERENCE` | Wk 4 |
| `GPX TO FEATURES` | Wk 4 |
| `HILLSHADE` | Wk 11 |
| `INTERSECT` / `PAIRWISE INTERSECT` | Wk 7 |
| `MODELBUILDER` | Wk 8 |
| `POLYGON TO RASTER` | Wk 14 |
| `PROJECT` | Wk 3 |
| `RASTER CALCULATOR` | Wk 12 |
| `RASTER TO POLYGON` | Wk 14 |
| `RECLASSIFY` | Wk 10 |
| `SELECT BY ATTRIBUTES` | Wk 5 |
| `SELECT BY LOCATION` | Wk 5 |
| `SLOPE` | Wk 11 |
| `SUMMARY STATISTICS` | Wk 5 |
| `UNION` | Wk 7 |
| `UPDATE` | Wk 7 |
| `WEIGHTED OVERLAY` | Wk 12 |
| `XY TABLE TO POINT` | Wk 4 |
