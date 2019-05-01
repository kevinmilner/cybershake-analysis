# rundir2585_1myr Rotated Rupture Variability, M7.2 SS

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M7.2, Vertical Strike-Slip with Surface Rupture). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

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
* [M7.2 SS RSQSim Rupture Match Criteria](#m72-ss-rsqsim-rupture-match-criteria)
* [Sites](#sites)
* [Result Summary Table](#result-summary-table)
  * [Dist-Dependent Plot Table](#dist-dependent-plot-table)
* [Path-to-path Variability](#path-to-path-variability)
  * [Path-to-path Variability Methodology](#path-to-path-variability-methodology)
  * [20.0 km M7.2 Path-to-path Results](#200-km-m72-path-to-path-results)
  * [50.0 km M7.2 Path-to-path Results](#500-km-m72-path-to-path-results)
  * [100.0 km M7.2 Path-to-path Results](#1000-km-m72-path-to-path-results)
* [Source-strike Variability](#source-strike-variability)
  * [Source-strike Variability Methodology](#source-strike-variability-methodology)
  * [20.0 km M7.2 Source-strike Results](#200-km-m72-source-strike-results)
  * [50.0 km M7.2 Source-strike Results](#500-km-m72-source-strike-results)
  * [100.0 km M7.2 Source-strike Results](#1000-km-m72-source-strike-results)
* [Within-event, single-site Variability](#within-event-single-site-variability)
  * [Within-event, single-site Variability Methodology](#within-event-single-site-variability-methodology)
  * [20.0 km M7.2 Within-event, single-site Results](#200-km-m72-within-event-single-site-results)
  * [50.0 km M7.2 Within-event, single-site Results](#500-km-m72-within-event-single-site-results)
  * [100.0 km M7.2 Within-event, single-site Results](#1000-km-m72-within-event-single-site-results)
* [Between-events Variability](#between-events-variability)
  * [Between-events Variability Methodology](#between-events-variability-methodology)
  * [20.0 km M7.2 Between-events Results](#200-km-m72-between-events-results)
  * [50.0 km M7.2 Between-events Results](#500-km-m72-between-events-results)
  * [100.0 km M7.2 Between-events Results](#1000-km-m72-between-events-results)
* [Azumth Dependence](#azumth-dependence)
  * [PAS Azumth Dependence](#pas-azumth-dependence)
    * [PAS Rupture Strike Dependence](#pas-rupture-strike-dependence)
    * [PAS Path Dependence](#pas-path-dependence)
  * [SBSM Azumth Dependence](#sbsm-azumth-dependence)
    * [SBSM Rupture Strike Dependence](#sbsm-rupture-strike-dependence)
    * [SBSM Path Dependence](#sbsm-path-dependence)
  * [SMCA Azumth Dependence](#smca-azumth-dependence)
    * [SMCA Rupture Strike Dependence](#smca-rupture-strike-dependence)
    * [SMCA Path Dependence](#smca-path-dependence)
  * [STNI Azumth Dependence](#stni-azumth-dependence)
    * [STNI Rupture Strike Dependence](#stni-rupture-strike-dependence)
    * [STNI Path Dependence](#stni-path-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
    * [USC Rupture Strike Dependence](#usc-rupture-strike-dependence)
    * [USC Path Dependence](#usc-path-dependence)
  * [WNGC Azumth Dependence](#wngc-azumth-dependence)
    * [WNGC Rupture Strike Dependence](#wngc-rupture-strike-dependence)
    * [WNGC Path Dependence](#wngc-path-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
    * [All Sites Rupture Strike Dependence](#all-sites-rupture-strike-dependence)
    * [All Sites Path Dependence](#all-sites-path-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m72-vertical-strike-slip-with-surface-rupture)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 100 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 6 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 36 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **1166400** | Total number of combinations of the above. |

## M7.2 SS RSQSim Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 100 events in the catalog which match the following criteria:

* M=[7.15,7.25]
* Ztor=[0.0,1.0]
* Rake=[-180,-170] or [-10,10] or [170,180]
* Dip=90.0
* Linear rupture (max 5.0% deviation from ideal)

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| PAS | *34.148426, -118.17119* | 838.8 | 0.01 | 0.68 |
| SBSM | *34.064987, -117.29201* | 500 | 0.33 | 1.82 |
| SMCA | *34.00909, -118.48939* | 500 | 0.59 | 2.45 |
| STNI | *33.93088, -118.17881* | 500 | 0.88 | 5.57 |
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |
| WNGC | *34.041824, -118.0653* | 500 | 0.5 | 3.49 |

## Result Summary Table

| Type | Notation | Distance | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.36 | 0.32 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.45 | 0.38 | 0.23 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.49 | 0.43 | 0.27 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.38 | 0.38 | 0.31 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.36 | 0.39 | 0.44 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.34 | 0.4 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.46 | 0.43 | 0.32 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.51 | 0.48 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.54 | 0.52 | 0.48 |
| Between-events | &tau; | 20 km | 0.11 | 0.17 | 0.22 |
| Between-events | &tau; | 50 km | 0.11 | 0.17 | 0.21 |
| Between-events | &tau; | 100 km | 0.11 | 0.17 | 0.22 |

### Dist-Dependent Plot Table
*[(top)](#table-of-contents)*

| **&phi;<sub>P2P</sub>** | ![&phi;<sub>P2P</sub>](resources/path_m7.2_dist_periods.png) |
|-----|-----|
| **&phi;<sub>s</sub>** | ![&phi;<sub>s</sub>](resources/source_strike_m7.2_dist_periods.png) |
| **&phi;<sub>SS</sub>** | ![&phi;<sub>SS</sub>](resources/within_event_ss_m7.2_dist_periods.png) |
| **&tau;** | ![&tau;](resources/between_events_m7.2_dist_periods.png) |


## Path-to-path Variability
*[(top)](#table-of-contents)*

### Path-to-path Variability Methodology
*[(top)](#table-of-contents)*

Path-to-path variability, denoted &phi;<sub>P2P</sub> in Al Atik (2010), is computed separately for each:

* Site *[6 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*
* Rupture Strike *[18 unique]*

we compute residuals of the natural-log ground motions (relative to the median), computed across all 36 combinations of:

* Path *[36 unique]*

We take &phi;<sub>P2P</sub> to be the standard deviation of all residuals across each combination of Rupture, Rupture Strike. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.36 | 0.35 | 0.33 | [0.11 0.75] |  | 0.31 | 0.3 | 0.29 | [0.08 0.63] |  | 0.14 | 0.13 | 0.12 | [0.03 0.39] |
| SBSM |  | 0.28 | 0.27 | 0.26 | [0.1 0.6] |  | 0.21 | 0.2 | 0.18 | [0.05 0.49] |  | 0.13 | 0.12 | 0.11 | [0.03 0.32] |
| SMCA |  | 0.32 | 0.3 | 0.29 | [0.11 0.65] |  | 0.31 | 0.29 | 0.28 | [0.12 0.59] |  | 0.16 | 0.15 | 0.15 | [0.04 0.38] |
| STNI |  | 0.26 | 0.25 | 0.25 | [0.11 0.47] |  | 0.27 | 0.27 | 0.26 | [0.06 0.5] |  | 0.13 | 0.12 | 0.12 | [0.03 0.32] |
| USC |  | 0.3 | 0.3 | 0.29 | [0.1 0.57] |  | 0.32 | 0.31 | 0.3 | [0.08 0.61] |  | 0.16 | 0.15 | 0.14 | [0.05 0.37] |
| WNGC |  | 0.56 | 0.54 | 0.54 | [0.21 0.96] |  | 0.45 | 0.44 | 0.43 | [0.16 0.84] |  | 0.19 | 0.18 | 0.17 | [0.05 0.46] |
| **ALL SITES** |  | **0.36** | **0.34** | **0.3** | **[0.1 0.96]** |  | **0.32** | **0.3** | **0.29** | **[0.05 0.84]** |  | **0.15** | **0.14** | **0.13** | **[0.03 0.46]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_20km_3s_hist.png) | ![5s](resources/path_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_20km_10s_hist.png) |  |


### 50.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.4 | 0.39 | 0.38 | [0.18 0.75] |  | 0.35 | 0.34 | 0.33 | [0.15 0.6] |  | 0.2 | 0.19 | 0.18 | [0.06 0.43] |
| SBSM |  | 0.5 | 0.5 | 0.49 | [0.28 0.88] |  | 0.4 | 0.4 | 0.39 | [0.18 0.75] |  | 0.23 | 0.22 | 0.21 | [0.07 0.43] |
| SMCA |  | 0.47 | 0.46 | 0.46 | [0.23 0.74] |  | 0.38 | 0.37 | 0.36 | [0.19 0.66] |  | 0.25 | 0.25 | 0.24 | [0.11 0.45] |
| STNI |  | 0.29 | 0.29 | 0.28 | [0.17 0.48] |  | 0.33 | 0.33 | 0.32 | [0.18 0.54] |  | 0.21 | 0.2 | 0.19 | [0.06 0.43] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.17 0.61] |  | 0.35 | 0.34 | 0.34 | [0.18 0.54] |  | 0.25 | 0.24 | 0.23 | [0.08 0.49] |
| WNGC |  | 0.59 | 0.58 | 0.58 | [0.27 0.94] |  | 0.46 | 0.45 | 0.45 | [0.19 0.75] |  | 0.23 | 0.22 | 0.22 | [0.08 0.47] |
| **ALL SITES** |  | **0.45** | **0.42** | **0.41** | **[0.17 0.94]** |  | **0.38** | **0.37** | **0.36** | **[0.15 0.75]** |  | **0.23** | **0.22** | **0.21** | **[0.06 0.49]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_50km_3s_hist.png) | ![5s](resources/path_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_50km_10s_hist.png) |  |


### 100.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.42 | 0.42 | 0.41 | [0.23 0.7] |  | 0.38 | 0.38 | 0.37 | [0.2 0.64] |  | 0.22 | 0.21 | 0.21 | [0.09 0.41] |
| SBSM |  | 0.58 | 0.57 | 0.57 | [0.3 0.92] |  | 0.44 | 0.44 | 0.44 | [0.22 0.7] |  | 0.26 | 0.26 | 0.25 | [0.11 0.46] |
| SMCA |  | 0.55 | 0.55 | 0.55 | [0.31 0.85] |  | 0.43 | 0.43 | 0.43 | [0.26 0.62] |  | 0.31 | 0.31 | 0.31 | [0.16 0.49] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.2 0.51] |  | 0.39 | 0.39 | 0.38 | [0.18 0.62] |  | 0.27 | 0.26 | 0.26 | [0.09 0.51] |
| USC |  | 0.38 | 0.38 | 0.38 | [0.26 0.66] |  | 0.41 | 0.41 | 0.4 | [0.24 0.62] |  | 0.3 | 0.3 | 0.3 | [0.13 0.51] |
| WNGC |  | 0.58 | 0.58 | 0.58 | [0.34 0.9] |  | 0.49 | 0.48 | 0.49 | [0.25 0.79] |  | 0.26 | 0.25 | 0.25 | [0.1 0.46] |
| **ALL SITES** |  | **0.49** | **0.47** | **0.46** | **[0.2 0.92]** |  | **0.43** | **0.42** | **0.41** | **[0.18 0.79]** |  | **0.27** | **0.27** | **0.26** | **[0.09 0.51]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_100km_3s_hist.png) | ![5s](resources/path_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_100km_10s_hist.png) |  |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[6 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*
* Path *[36 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 18 combinations of:

* Rupture Strike *[18 unique]*

We take &phi;<sub>s</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture, Path. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Path]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_source_strike.png)


### 20.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.41 | 0.4 | 0.4 | [0.15 0.74] |  | 0.39 | 0.38 | 0.37 | [0.14 0.78] |  | 0.3 | 0.29 | 0.28 | [0.1 0.59] |
| SBSM |  | 0.43 | 0.42 | 0.41 | [0.15 0.81] |  | 0.41 | 0.4 | 0.38 | [0.14 0.8] |  | 0.3 | 0.29 | 0.28 | [0.11 0.61] |
| SMCA |  | 0.38 | 0.38 | 0.38 | [0.16 0.68] |  | 0.4 | 0.39 | 0.37 | [0.15 0.86] |  | 0.32 | 0.31 | 0.3 | [0.1 0.68] |
| STNI |  | 0.31 | 0.31 | 0.3 | [0.09 0.59] |  | 0.32 | 0.32 | 0.3 | [0.13 0.74] |  | 0.32 | 0.31 | 0.3 | [0.1 0.66] |
| USC |  | 0.36 | 0.35 | 0.35 | [0.11 0.7] |  | 0.36 | 0.35 | 0.34 | [0.12 0.79] |  | 0.31 | 0.31 | 0.3 | [0.1 0.67] |
| WNGC |  | 0.36 | 0.36 | 0.35 | [0.11 0.75] |  | 0.37 | 0.36 | 0.35 | [0.15 0.78] |  | 0.31 | 0.3 | 0.29 | [0.09 0.59] |
| **ALL SITES** |  | **0.38** | **0.37** | **0.36** | **[0.09 0.81]** |  | **0.38** | **0.37** | **0.35** | **[0.12 0.86]** |  | **0.31** | **0.3** | **0.29** | **[0.09 0.68]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_20km_3s_hist.png) | ![5s](resources/source_strike_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_20km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 50.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.36 | 0.34 | 0.32 | [0.12 0.77] |  | 0.36 | 0.34 | 0.32 | [0.11 0.81] |  | 0.44 | 0.43 | 0.43 | [0.19 0.82] |
| SBSM |  | 0.45 | 0.45 | 0.45 | [0.17 0.88] |  | 0.45 | 0.44 | 0.43 | [0.2 0.79] |  | 0.43 | 0.43 | 0.42 | [0.23 0.76] |
| SMCA |  | 0.35 | 0.34 | 0.33 | [0.1 0.71] |  | 0.39 | 0.38 | 0.36 | [0.09 0.85] |  | 0.44 | 0.43 | 0.42 | [0.16 0.83] |
| STNI |  | 0.3 | 0.3 | 0.29 | [0.1 0.64] |  | 0.36 | 0.35 | 0.33 | [0.11 0.82] |  | 0.47 | 0.46 | 0.46 | [0.2 0.91] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.11 0.69] |  | 0.37 | 0.36 | 0.34 | [0.11 0.84] |  | 0.44 | 0.43 | 0.42 | [0.12 0.92] |
| WNGC |  | 0.37 | 0.35 | 0.32 | [0.11 0.84] |  | 0.41 | 0.39 | 0.37 | [0.13 0.87] |  | 0.44 | 0.43 | 0.43 | [0.18 0.86] |
| **ALL SITES** |  | **0.36** | **0.35** | **0.33** | **[0.1 0.88]** |  | **0.39** | **0.38** | **0.36** | **[0.09 0.87]** |  | **0.44** | **0.43** | **0.43** | **[0.12 0.92]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_50km_3s_hist.png) | ![5s](resources/source_strike_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_50km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 100.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.34 | 0.33 | 0.33 | [0.12 0.67] |  | 0.38 | 0.36 | 0.35 | [0.11 0.85] |  | 0.45 | 0.44 | 0.44 | [0.13 0.87] |
| SBSM |  | 0.42 | 0.42 | 0.41 | [0.1 0.91] |  | 0.45 | 0.44 | 0.43 | [0.12 0.85] |  | 0.43 | 0.43 | 0.43 | [0.13 0.78] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.08 0.8] |  | 0.39 | 0.37 | 0.36 | [0.1 0.78] |  | 0.43 | 0.42 | 0.42 | [0.12 0.88] |
| STNI |  | 0.29 | 0.28 | 0.28 | [0.1 0.56] |  | 0.38 | 0.37 | 0.36 | [0.12 0.85] |  | 0.49 | 0.49 | 0.48 | [0.16 0.93] |
| USC |  | 0.31 | 0.31 | 0.3 | [0.1 0.63] |  | 0.38 | 0.37 | 0.36 | [0.11 0.89] |  | 0.45 | 0.44 | 0.44 | [0.17 0.91] |
| WNGC |  | 0.34 | 0.33 | 0.31 | [0.1 0.84] |  | 0.41 | 0.39 | 0.38 | [0.09 0.89] |  | 0.45 | 0.45 | 0.44 | [0.16 0.97] |
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.08 0.91]** |  | **0.4** | **0.38** | **0.37** | **[0.09 0.89]** |  | **0.45** | **0.44** | **0.44** | **[0.12 0.97]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_100km_3s_hist.png) | ![5s](resources/source_strike_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_100km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[6 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 648 combinations of:

* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We take &phi;<sub>SS</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event_ss.png)


### 20.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.49 | 0.48 | 0.47 | [0.38 0.62] |  | 0.45 | 0.44 | 0.43 | [0.33 0.7] |  | 0.31 | 0.29 | 0.28 | [0.17 0.5] |
| SBSM |  | 0.45 | 0.44 | 0.44 | [0.29 0.67] |  | 0.42 | 0.41 | 0.39 | [0.26 0.66] |  | 0.3 | 0.29 | 0.28 | [0.15 0.49] |
| SMCA |  | 0.43 | 0.43 | 0.42 | [0.33 0.53] |  | 0.43 | 0.42 | 0.4 | [0.31 0.68] |  | 0.32 | 0.31 | 0.3 | [0.19 0.53] |
| STNI |  | 0.34 | 0.34 | 0.34 | [0.27 0.45] |  | 0.35 | 0.34 | 0.34 | [0.26 0.53] |  | 0.32 | 0.31 | 0.3 | [0.15 0.59] |
| USC |  | 0.41 | 0.4 | 0.39 | [0.32 0.53] |  | 0.4 | 0.4 | 0.38 | [0.3 0.59] |  | 0.32 | 0.31 | 0.3 | [0.17 0.56] |
| WNGC |  | 0.6 | 0.6 | 0.6 | [0.49 0.7] |  | 0.52 | 0.51 | 0.5 | [0.41 0.69] |  | 0.33 | 0.32 | 0.32 | [0.2 0.53] |
| **ALL SITES** |  | **0.46** | **0.45** | **0.43** | **[0.27 0.7]** |  | **0.43** | **0.42** | **0.41** | **[0.26 0.7]** |  | **0.32** | **0.3** | **0.3** | **[0.15 0.59]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_20km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_20km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 50.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.47 | 0.47 | 0.47 | [0.37 0.57] |  | 0.43 | 0.43 | 0.41 | [0.32 0.62] |  | 0.44 | 0.43 | 0.43 | [0.28 0.71] |
| SBSM |  | 0.61 | 0.61 | 0.6 | [0.49 0.74] |  | 0.55 | 0.55 | 0.53 | [0.42 0.75] |  | 0.46 | 0.45 | 0.44 | [0.36 0.68] |
| SMCA |  | 0.52 | 0.52 | 0.52 | [0.44 0.6] |  | 0.46 | 0.46 | 0.45 | [0.34 0.66] |  | 0.45 | 0.45 | 0.43 | [0.31 0.71] |
| STNI |  | 0.37 | 0.36 | 0.36 | [0.3 0.48] |  | 0.41 | 0.41 | 0.39 | [0.31 0.63] |  | 0.48 | 0.46 | 0.46 | [0.3 0.81] |
| USC |  | 0.39 | 0.39 | 0.39 | [0.32 0.47] |  | 0.43 | 0.43 | 0.41 | [0.32 0.65] |  | 0.45 | 0.44 | 0.45 | [0.3 0.74] |
| WNGC |  | 0.64 | 0.63 | 0.64 | [0.53 0.73] |  | 0.54 | 0.54 | 0.53 | [0.43 0.71] |  | 0.45 | 0.44 | 0.43 | [0.33 0.73] |
| **ALL SITES** |  | **0.51** | **0.5** | **0.5** | **[0.3 0.74]** |  | **0.48** | **0.47** | **0.46** | **[0.31 0.75]** |  | **0.45** | **0.45** | **0.44** | **[0.28 0.81]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_50km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_50km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 100.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS |  | 0.49 | 0.49 | 0.48 | [0.41 0.56] |  | 0.48 | 0.48 | 0.47 | [0.38 0.66] |  | 0.46 | 0.45 | 0.45 | [0.29 0.73] |
| SBSM |  | 0.65 | 0.65 | 0.65 | [0.53 0.76] |  | 0.57 | 0.57 | 0.56 | [0.45 0.73] |  | 0.47 | 0.47 | 0.46 | [0.36 0.68] |
| SMCA |  | 0.6 | 0.6 | 0.6 | [0.5 0.66] |  | 0.52 | 0.52 | 0.51 | [0.42 0.72] |  | 0.48 | 0.47 | 0.47 | [0.33 0.76] |
| STNI |  | 0.38 | 0.38 | 0.38 | [0.31 0.46] |  | 0.49 | 0.48 | 0.46 | [0.38 0.71] |  | 0.51 | 0.51 | 0.5 | [0.33 0.82] |
| USC |  | 0.44 | 0.44 | 0.43 | [0.36 0.52] |  | 0.5 | 0.49 | 0.48 | [0.39 0.7] |  | 0.49 | 0.49 | 0.48 | [0.32 0.78] |
| WNGC |  | 0.63 | 0.63 | 0.63 | [0.53 0.72] |  | 0.58 | 0.57 | 0.56 | [0.46 0.76] |  | 0.48 | 0.47 | 0.46 | [0.32 0.75] |
| **ALL SITES** |  | **0.54** | **0.53** | **0.54** | **[0.31 0.76]** |  | **0.52** | **0.52** | **0.52** | **[0.38 0.76]** |  | **0.48** | **0.48** | **0.47** | **[0.29 0.82]** |

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_100km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_100km_10s_hist.png) |  |

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Site *[6 unique]*
* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[100 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 648 combinations of:

* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We take &tau; to be the standard deviation of all &delta;B<sub>e</sub>. Finally, we compute the median standard deviation across all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_between_events.png)


### 20.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.12 | -3.37 | [-3.78 -3.1] | 0.16 | -4.06 | [-4.42 -3.68] | 0.24 | -5.01 | [-5.61 -4.45] |
| SBSM | 0.14 | -1.74 | [-2.26 -1.46] | 0.16 | -2.86 | [-3.32 -2.45] | 0.18 | -4.54 | [-4.98 -4.08] |
| SMCA | 0.11 | -2.07 | [-2.41 -1.86] | 0.17 | -2.64 | [-3.1 -2.27] | 0.21 | -4.06 | [-4.6 -3.53] |
| STNI | 0.11 | -2.02 | [-2.34 -1.82] | 0.17 | -2.57 | [-2.97 -2.2] | 0.24 | -3.56 | [-4.23 -2.93] |
| USC | 0.11 | -2.15 | [-2.49 -1.94] | 0.16 | -2.85 | [-3.26 -2.5] | 0.22 | -4.06 | [-4.63 -3.48] |
| WNGC | 0.12 | -2.15 | [-2.58 -1.92] | 0.17 | -2.88 | [-3.3 -2.52] | 0.21 | -4.21 | [-4.71 -3.66] |
| **ALL SITES** | **0.11** | **-2.25** | **[-3.78 -1.46]** | **0.17** | **-2.98** | **[-4.42 -2.2]** | **0.22** | **-4.24** | **[-5.61 -2.93]** |


### 50.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.11 | -4.27 | [-4.64 -4.05] | 0.16 | -4.78 | [-5.17 -4.38] | 0.23 | -5.62 | [-6.2 -5.03] |
| SBSM | 0.13 | -2.43 | [-2.83 -2.14] | 0.17 | -3.51 | [-3.98 -3.12] | 0.17 | -5.16 | [-5.59 -4.73] |
| SMCA | 0.11 | -2.94 | [-3.29 -2.75] | 0.16 | -3.4 | [-3.8 -2.97] | 0.2 | -4.71 | [-5.23 -4.12] |
| STNI | 0.11 | -2.75 | [-3.08 -2.49] | 0.19 | -2.98 | [-3.38 -2.56] | 0.24 | -4.08 | [-4.65 -3.44] |
| USC | 0.11 | -2.89 | [-3.23 -2.62] | 0.17 | -3.4 | [-3.82 -2.96] | 0.22 | -4.62 | [-5.14 -4.02] |
| WNGC | 0.11 | -3 | [-3.36 -2.77] | 0.18 | -3.46 | [-3.88 -3.02] | 0.21 | -4.77 | [-5.29 -4.14] |
| **ALL SITES** | **0.11** | **-3.05** | **[-4.64 -2.14]** | **0.17** | **-3.59** | **[-5.17 -2.56]** | **0.21** | **-4.83** | **[-6.2 -3.44]** |


### 100.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| PAS | 0.11 | -4.83 | [-5.2 -4.6] | 0.15 | -5.32 | [-5.68 -4.95] | 0.24 | -6.07 | [-6.7 -5.56] |
| SBSM | 0.13 | -3.1 | [-3.51 -2.79] | 0.16 | -4.09 | [-4.54 -3.69] | 0.18 | -5.67 | [-6.08 -5.27] |
| SMCA | 0.11 | -3.62 | [-3.96 -3.4] | 0.17 | -3.9 | [-4.3 -3.5] | 0.21 | -5.19 | [-5.75 -4.68] |
| STNI | 0.11 | -3.36 | [-3.72 -3.08] | 0.18 | -3.56 | [-3.97 -3.09] | 0.24 | -4.55 | [-5.18 -3.98] |
| USC | 0.11 | -3.53 | [-3.89 -3.24] | 0.17 | -3.95 | [-4.36 -3.53] | 0.22 | -5.1 | [-5.67 -4.58] |
| WNGC | 0.11 | -3.59 | [-3.96 -3.32] | 0.17 | -4.02 | [-4.39 -3.63] | 0.22 | -5.24 | [-5.79 -4.78] |
| **ALL SITES** | **0.11** | **-3.67** | **[-5.2 -2.79]** | **0.17** | **-4.14** | **[-5.68 -3.09]** | **0.22** | **-5.3** | **[-6.7 -3.98]** |


## Azumth Dependence
*[(top)](#table-of-contents)*

### PAS Azumth Dependence
*[(top)](#table-of-contents)*

#### PAS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

## BBP PartB Comparison
*[(top)](#table-of-contents)*

Here we attempt to reproduce the SCEC BroadBand Platform "Part B" validation exercise as defined in:

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismic‐hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|-----|
| **M7.2 SS** | **PAS** | *(PASS)* | *(PASS)* | *(PASS)* |
| **M7.2 SS** | **SBSM** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **SMCA** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **STNI** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **USC** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **WNGC** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **5sites_Vs30_500** | *(FAIL)* | *(FAIL)* | *(FAIL)* |

### BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_PAS.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_WNGC.png) |
| **5sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_5sites_Vs30_500.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M7.2 | 20.0 km | PAS | [sa_PAS_m7.2_20.0km.csv.gz](resources/sa_PAS_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | SBSM | [sa_SBSM_m7.2_20.0km.csv.gz](resources/sa_SBSM_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | SMCA | [sa_SMCA_m7.2_20.0km.csv.gz](resources/sa_SMCA_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | STNI | [sa_STNI_m7.2_20.0km.csv.gz](resources/sa_STNI_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | USC | [sa_USC_m7.2_20.0km.csv.gz](resources/sa_USC_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | WNGC | [sa_WNGC_m7.2_20.0km.csv.gz](resources/sa_WNGC_m7.2_20.0km.csv.gz) |
| M7.2 | 50.0 km | PAS | [sa_PAS_m7.2_50.0km.csv.gz](resources/sa_PAS_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | SBSM | [sa_SBSM_m7.2_50.0km.csv.gz](resources/sa_SBSM_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | SMCA | [sa_SMCA_m7.2_50.0km.csv.gz](resources/sa_SMCA_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | STNI | [sa_STNI_m7.2_50.0km.csv.gz](resources/sa_STNI_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | USC | [sa_USC_m7.2_50.0km.csv.gz](resources/sa_USC_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | WNGC | [sa_WNGC_m7.2_50.0km.csv.gz](resources/sa_WNGC_m7.2_50.0km.csv.gz) |
| M7.2 | 100.0 km | PAS | [sa_PAS_m7.2_100.0km.csv.gz](resources/sa_PAS_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | SBSM | [sa_SBSM_m7.2_100.0km.csv.gz](resources/sa_SBSM_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | SMCA | [sa_SMCA_m7.2_100.0km.csv.gz](resources/sa_SMCA_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | STNI | [sa_STNI_m7.2_100.0km.csv.gz](resources/sa_STNI_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | USC | [sa_USC_m7.2_100.0km.csv.gz](resources/sa_USC_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | WNGC | [sa_WNGC_m7.2_100.0km.csv.gz](resources/sa_WNGC_m7.2_100.0km.csv.gz) |

