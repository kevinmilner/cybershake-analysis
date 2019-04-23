# rundir2585_1myr Rotated Rupture Variability, M6.6 Reverse

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M6.6, Reverse, Dip=45, Ztor=3). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

We then  perform various rotations. We rotate the rupture in place around its centroid, holding the site-to-source centroid path and Rrup constant (henceforth 'Rupture Strike'). We also rotate ruptures around the site, holding Rrup and source orientation relative to the site constant but sampling different various paths (henceforth 'Path'). We do this for each unique combination of Rupture Strike, Path, Distance, Site, and Rupture.

**Study Details**

| **Name** | RSQSim RotRup 2585 |
|-----|-----|
| **Date** | Mar 2019 |
| **Region** | Los Angeles Box |
| **Description** | RSQSim rotated-rupture variability study with catalog 2585 |
| **Velocity Model** | CVM-S4.26, 4.26 |

## Table Of Contents
* [Rupture Rotation Parameters](#rupture-rotation-parameters)
* [M6.6 Reverse RSQSim Rupture Match Criteria](#m66-reverse-rsqsim-rupture-match-criteria)
* [Sites](#sites)
* [Result Summary Table](#result-summary-table)
  * [Dist-Dependent Plot Table](#dist-dependent-plot-table)
* [Path-to-path Variability](#path-to-path-variability)
  * [Path-to-path Variability Methodology](#path-to-path-variability-methodology)
  * [20.0 km M6.6 Path-to-path Results](#200-km-m66-path-to-path-results)
  * [50.0 km M6.6 Path-to-path Results](#500-km-m66-path-to-path-results)
  * [100.0 km M6.6 Path-to-path Results](#1000-km-m66-path-to-path-results)
* [Source-strike Variability](#source-strike-variability)
  * [Source-strike Variability Methodology](#source-strike-variability-methodology)
  * [20.0 km M6.6 Source-strike Results](#200-km-m66-source-strike-results)
  * [50.0 km M6.6 Source-strike Results](#500-km-m66-source-strike-results)
  * [100.0 km M6.6 Source-strike Results](#1000-km-m66-source-strike-results)
* [Within-event, single-site Variability](#within-event-single-site-variability)
  * [Within-event, single-site Variability Methodology](#within-event-single-site-variability-methodology)
  * [20.0 km M6.6 Within-event, single-site Results](#200-km-m66-within-event-single-site-results)
  * [50.0 km M6.6 Within-event, single-site Results](#500-km-m66-within-event-single-site-results)
  * [100.0 km M6.6 Within-event, single-site Results](#1000-km-m66-within-event-single-site-results)
* [Between-events Variability](#between-events-variability)
  * [Between-events Variability Methodology](#between-events-variability-methodology)
  * [20.0 km M6.6 Between-events Results](#200-km-m66-between-events-results)
  * [50.0 km M6.6 Between-events Results](#500-km-m66-between-events-results)
  * [100.0 km M6.6 Between-events Results](#1000-km-m66-between-events-results)
* [Azumth Dependence](#azumth-dependence)
  * [PAS Azumth Dependence](#pas-azumth-dependence)
    * [PAS Rupture Strike Dependence](#pas-rupture-strike-dependence)
    * [PAS Path Dependence](#pas-path-dependence)
  * [SMCA Azumth Dependence](#smca-azumth-dependence)
    * [SMCA Rupture Strike Dependence](#smca-rupture-strike-dependence)
    * [SMCA Path Dependence](#smca-path-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
    * [USC Rupture Strike Dependence](#usc-rupture-strike-dependence)
    * [USC Path Dependence](#usc-path-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
    * [All Sites Rupture Strike Dependence](#all-sites-rupture-strike-dependence)
    * [All Sites Path Dependence](#all-sites-path-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M6.6, Reverse, Dip=45, Ztor=3](#bbp-partb-m66-reverse-dip45-ztor3)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 100 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 3 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 36 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **583200** | Total number of combinations of the above. |

## M6.6 Reverse RSQSim Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 100 events in the catalog which match the following criteria:

* M=[6.55,6.65]
* Ztor=[1.0,5.0]
* Rake=[80,100]
* Dip=[35.0,55.0]

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| PAS | *34.148426, -118.17119* | 838.8 | 0.01 | 0.68 |
| SMCA | *34.00909, -118.48939* | 500 | 0.59 | 2.45 |
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |

## Result Summary Table

| Type | Notation | Distance | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.3 | 0.28 | 0.17 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.37 | 0.35 | 0.21 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.42 | 0.38 | 0.26 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.32 | 0.37 | 0.32 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.3 | 0.37 | 0.34 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.31 | 0.36 | 0.36 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.38 | 0.4 | 0.33 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.43 | 0.45 | 0.36 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.48 | 0.48 | 0.42 |
| Between-events | &tau; | 20 km | 0.21 | 0.25 | 0.26 |
| Between-events | &tau; | 50 km | 0.22 | 0.26 | 0.27 |
| Between-events | &tau; | 100 km | 0.2 | 0.24 | 0.3 |

### Dist-Dependent Plot Table
*[(top)](#table-of-contents)*

| **&phi;<sub>P2P</sub>** | ![&phi;<sub>P2P</sub>](resources/path_m6.6_dist_periods.png) |
|-----|-----|
| **&phi;<sub>s</sub>** | ![&phi;<sub>s</sub>](resources/source_strike_m6.6_dist_periods.png) |
| **&phi;<sub>SS</sub>** | ![&phi;<sub>SS</sub>](resources/within_event_ss_m6.6_dist_periods.png) |
| **&tau;** | ![&tau;](resources/between_events_m6.6_dist_periods.png) |


## Path-to-path Variability
*[(top)](#table-of-contents)*

### Path-to-path Variability Methodology
*[(top)](#table-of-contents)*

Path-to-path variability, denoted &phi;<sub>P2P</sub> in Al Atik (2010), is computed separately for each:

* Site *[3 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*
* Rupture Strike *[18 unique]*

we compute residuals of the natural-log ground motions (relative to the median), computed across all 36 combinations of:

* Path *[36 unique]*

We take &phi;<sub>P2P</sub> to be the standard deviation of all residuals across each combination of Rupture, Rupture Strike. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.32 | 0.31 | 0.3 | [0.08 0.6] |  | 0.25 | 0.23 | 0.23 | [0.07 0.53] |  | 0.13 | 0.12 | 0.11 | [0.03 0.33] |
| SMCA |  | 0.28 | 0.27 | 0.27 | [0.13 0.51] |  | 0.3 | 0.29 | 0.28 | [0.09 0.56] |  | 0.21 | 0.2 | 0.2 | [0.05 0.4] |
| USC |  | 0.3 | 0.29 | 0.29 | [0.1 0.59] |  | 0.28 | 0.27 | 0.27 | [0.08 0.49] |  | 0.16 | 0.15 | 0.15 | [0.05 0.35] |
| **ALL SITES** |  | **0.3** | **0.29** | **0.28** | **[0.08 0.6]** |  | **0.28** | **0.27** | **0.26** | **[0.07 0.56]** |  | **0.17** | **0.16** | **0.15** | **[0.03 0.4]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_20km_3s_hist.png) | ![5s](resources/path_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_20km_10s_hist.png) |  |


### 50.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.37 | 0.36 | 0.35 | [0.14 0.66] |  | 0.32 | 0.32 | 0.32 | [0.11 0.57] |  | 0.16 | 0.15 | 0.14 | [0.05 0.42] |
| SMCA |  | 0.4 | 0.4 | 0.39 | [0.22 0.6] |  | 0.38 | 0.38 | 0.37 | [0.2 0.65] |  | 0.25 | 0.24 | 0.24 | [0.12 0.45] |
| USC |  | 0.34 | 0.34 | 0.34 | [0.19 0.49] |  | 0.36 | 0.36 | 0.36 | [0.2 0.57] |  | 0.21 | 0.21 | 0.21 | [0.08 0.45] |
| **ALL SITES** |  | **0.37** | **0.37** | **0.36** | **[0.14 0.66]** |  | **0.35** | **0.35** | **0.35** | **[0.11 0.65]** |  | **0.21** | **0.2** | **0.2** | **[0.05 0.45]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_50km_3s_hist.png) | ![5s](resources/path_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_50km_10s_hist.png) |  |


### 100.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.4 | 0.39 | 0.38 | [0.2 0.67] |  | 0.34 | 0.34 | 0.34 | [0.17 0.5] |  | 0.21 | 0.21 | 0.21 | [0.12 0.35] |
| SMCA |  | 0.48 | 0.48 | 0.48 | [0.3 0.71] |  | 0.44 | 0.44 | 0.44 | [0.27 0.61] |  | 0.28 | 0.28 | 0.28 | [0.16 0.45] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.24 0.56] |  | 0.36 | 0.36 | 0.35 | [0.24 0.52] |  | 0.27 | 0.27 | 0.27 | [0.16 0.41] |
| **ALL SITES** |  | **0.42** | **0.41** | **0.4** | **[0.2 0.71]** |  | **0.38** | **0.38** | **0.37** | **[0.17 0.61]** |  | **0.26** | **0.25** | **0.25** | **[0.12 0.45]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_100km_3s_hist.png) | ![5s](resources/path_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_100km_10s_hist.png) |  |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[3 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*
* Path *[36 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 18 combinations of:

* Rupture Strike *[18 unique]*

We take &phi;<sub>s</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture, Path. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Path]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_source_strike.png)


### 20.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.33 | 0.32 | 0.32 | [0.1 0.68] |  | 0.37 | 0.37 | 0.36 | [0.12 0.73] |  | 0.32 | 0.31 | 0.3 | [0.08 0.77] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.1 0.66] |  | 0.38 | 0.37 | 0.37 | [0.11 0.77] |  | 0.32 | 0.31 | 0.3 | [0.08 0.84] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.65] |  | 0.34 | 0.33 | 0.32 | [0.09 0.65] |  | 0.3 | 0.29 | 0.27 | [0.06 0.84] |
| **ALL SITES** |  | **0.32** | **0.31** | **0.31** | **[0.09 0.68]** |  | **0.37** | **0.35** | **0.35** | **[0.09 0.77]** |  | **0.32** | **0.3** | **0.29** | **[0.06 0.84]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_20km_3s_hist.png) | ![5s](resources/source_strike_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_20km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.3 | 0.29 | 0.29 | [0.09 0.68] |  | 0.37 | 0.36 | 0.35 | [0.09 0.71] |  | 0.34 | 0.33 | 0.31 | [0.12 0.81] |
| SMCA |  | 0.32 | 0.31 | 0.3 | [0.07 0.77] |  | 0.39 | 0.38 | 0.37 | [0.09 0.78] |  | 0.33 | 0.32 | 0.31 | [0.08 0.78] |
| USC |  | 0.29 | 0.28 | 0.27 | [0.09 0.67] |  | 0.35 | 0.34 | 0.33 | [0.09 0.72] |  | 0.34 | 0.32 | 0.31 | [0.1 0.88] |
| **ALL SITES** |  | **0.3** | **0.29** | **0.29** | **[0.07 0.77]** |  | **0.37** | **0.36** | **0.35** | **[0.09 0.78]** |  | **0.34** | **0.32** | **0.31** | **[0.08 0.88]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_50km_3s_hist.png) | ![5s](resources/source_strike_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_50km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.31 | 0.3 | 0.29 | [0.07 0.78] |  | 0.35 | 0.34 | 0.34 | [0.09 0.69] |  | 0.37 | 0.36 | 0.35 | [0.07 0.87] |
| SMCA |  | 0.31 | 0.3 | 0.29 | [0.1 0.73] |  | 0.35 | 0.34 | 0.34 | [0.07 0.68] |  | 0.35 | 0.34 | 0.33 | [0.08 0.85] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.85] |
| **ALL SITES** |  | **0.31** | **0.3** | **0.29** | **[0.07 0.78]** |  | **0.36** | **0.34** | **0.34** | **[0.07 0.75]** |  | **0.36** | **0.35** | **0.34** | **[0.07 0.87]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_100km_3s_hist.png) | ![5s](resources/source_strike_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_100km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[3 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 648 combinations of:

* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We take &phi;<sub>SS</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event_ss.png)


### 20.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.41 | 0.41 | 0.4 | [0.33 0.58] |  | 0.41 | 0.4 | 0.4 | [0.26 0.62] |  | 0.33 | 0.31 | 0.3 | [0.17 0.61] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.28 0.55] |  | 0.42 | 0.41 | 0.41 | [0.3 0.59] |  | 0.36 | 0.35 | 0.34 | [0.22 0.65] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.27 0.52] |  | 0.38 | 0.38 | 0.38 | [0.28 0.55] |  | 0.32 | 0.3 | 0.29 | [0.19 0.66] |
| **ALL SITES** |  | **0.38** | **0.38** | **0.37** | **[0.27 0.58]** |  | **0.4** | **0.4** | **0.4** | **[0.26 0.62]** |  | **0.33** | **0.32** | **0.31** | **[0.17 0.66]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_20km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 50.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.42 | 0.42 | 0.41 | [0.3 0.58] |  | 0.43 | 0.43 | 0.42 | [0.29 0.57] |  | 0.34 | 0.33 | 0.31 | [0.22 0.69] |
| SMCA |  | 0.45 | 0.45 | 0.45 | [0.39 0.62] |  | 0.48 | 0.48 | 0.47 | [0.38 0.65] |  | 0.38 | 0.38 | 0.36 | [0.26 0.69] |
| USC |  | 0.4 | 0.4 | 0.39 | [0.34 0.56] |  | 0.45 | 0.44 | 0.44 | [0.35 0.61] |  | 0.37 | 0.36 | 0.35 | [0.25 0.71] |
| **ALL SITES** |  | **0.43** | **0.42** | **0.42** | **[0.3 0.62]** |  | **0.45** | **0.45** | **0.45** | **[0.29 0.65]** |  | **0.36** | **0.36** | **0.34** | **[0.22 0.71]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_50km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 100.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.46 | 0.45 | 0.45 | [0.35 0.67] |  | 0.45 | 0.45 | 0.44 | [0.34 0.57] |  | 0.4 | 0.39 | 0.37 | [0.26 0.77] |
| SMCA |  | 0.53 | 0.53 | 0.53 | [0.43 0.71] |  | 0.52 | 0.52 | 0.51 | [0.42 0.62] |  | 0.42 | 0.42 | 0.4 | [0.33 0.78] |
| USC |  | 0.43 | 0.43 | 0.42 | [0.35 0.64] |  | 0.46 | 0.46 | 0.45 | [0.37 0.59] |  | 0.42 | 0.42 | 0.4 | [0.31 0.79] |
| **ALL SITES** |  | **0.48** | **0.47** | **0.47** | **[0.35 0.71]** |  | **0.48** | **0.47** | **0.47** | **[0.34 0.62]** |  | **0.42** | **0.41** | **0.39** | **[0.26 0.79]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_100km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Site *[3 unique]*
* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[100 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 648 combinations of:

* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We take &tau; to be the standard deviation of all &delta;B<sub>e</sub>. Finally, we compute the median standard deviation across all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_between_events.png)


### 20.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.2 | -4.73 | [-5.21 -4.23] | 0.24 | -5.27 | [-5.88 -4.65] | 0.27 | -6.39 | [-7.07 -5.79] |
| SMCA | 0.21 | -3.36 | [-3.8 -2.83] | 0.25 | -3.86 | [-4.53 -3.25] | 0.25 | -5.38 | [-6.04 -4.81] |
| USC | 0.23 | -3.42 | [-3.99 -2.87] | 0.25 | -4.06 | [-4.67 -3.49] | 0.26 | -5.41 | [-6.1 -4.83] |
| **ALL SITES** | **0.21** | **-3.84** | **[-5.21 -2.83]** | **0.25** | **-4.4** | **[-5.88 -3.25]** | **0.26** | **-5.73** | **[-7.07 -4.81]** |


### 50.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.22 | -5.57 | [-6.05 -5.03] | 0.27 | -5.92 | [-6.59 -5.19] | 0.29 | -6.99 | [-7.74 -6.19] |
| SMCA | 0.19 | -4.26 | [-4.68 -3.79] | 0.26 | -4.61 | [-5.25 -3.88] | 0.25 | -6.04 | [-6.73 -5.34] |
| USC | 0.24 | -4.23 | [-4.75 -3.64] | 0.26 | -4.69 | [-5.4 -3.99] | 0.27 | -6 | [-6.75 -5.26] |
| **ALL SITES** | **0.22** | **-4.69** | **[-6.05 -3.64]** | **0.26** | **-5.07** | **[-6.59 -3.88]** | **0.27** | **-6.34** | **[-7.74 -5.26]** |


### 100.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.2 | -6.17 | [-6.6 -5.73] | 0.24 | -6.57 | [-7.14 -5.92] | 0.32 | -7.39 | [-8.13 -6.57] |
| SMCA | 0.18 | -4.86 | [-5.27 -4.5] | 0.24 | -5.18 | [-5.72 -4.54] | 0.3 | -6.48 | [-7.22 -5.71] |
| USC | 0.21 | -4.87 | [-5.35 -4.37] | 0.26 | -5.23 | [-5.85 -4.55] | 0.3 | -6.44 | [-7.14 -5.67] |
| **ALL SITES** | **0.2** | **-5.3** | **[-6.6 -4.37]** | **0.24** | **-5.66** | **[-7.14 -4.54]** | **0.3** | **-6.77** | **[-8.13 -5.67]** |


## Azumth Dependence
*[(top)](#table-of-contents)*

### PAS Azumth Dependence
*[(top)](#table-of-contents)*

#### PAS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

## BBP PartB Comparison
*[(top)](#table-of-contents)*

Here we attempt to reproduce the SCEC BroadBand Platform "Part B" validation exercise as defined in:

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismic‐hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|-----|
| **M6.6 Reverse** | **PAS** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **SMCA** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **USC** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **2sites_Vs30_500** | **PASS** | **PASS** | *(PASS)* |

### BBP PartB, M6.6, Reverse, Dip=45, Ztor=3
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_PAS.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_SMCA.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_USC.png) |
| **2sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_2sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_2sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_2sites_Vs30_500.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M6.6 | 20.0 km | PAS | [sa_PAS_m6.6_20.0km.csv.gz](resources/sa_PAS_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SMCA | [sa_SMCA_m6.6_20.0km.csv.gz](resources/sa_SMCA_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | USC | [sa_USC_m6.6_20.0km.csv.gz](resources/sa_USC_m6.6_20.0km.csv.gz) |
| M6.6 | 50.0 km | PAS | [sa_PAS_m6.6_50.0km.csv.gz](resources/sa_PAS_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SMCA | [sa_SMCA_m6.6_50.0km.csv.gz](resources/sa_SMCA_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | USC | [sa_USC_m6.6_50.0km.csv.gz](resources/sa_USC_m6.6_50.0km.csv.gz) |
| M6.6 | 100.0 km | PAS | [sa_PAS_m6.6_100.0km.csv.gz](resources/sa_PAS_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SMCA | [sa_SMCA_m6.6_100.0km.csv.gz](resources/sa_SMCA_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | USC | [sa_USC_m6.6_100.0km.csv.gz](resources/sa_USC_m6.6_100.0km.csv.gz) |

