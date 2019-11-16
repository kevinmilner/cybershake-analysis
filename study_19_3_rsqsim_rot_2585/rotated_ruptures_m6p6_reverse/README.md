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
  * [GMPE Table](#gmpe-table)
  * [Dist-Dependent Plot Table](#dist-dependent-plot-table)
* [Path-to-path Variability](#path-to-path-variability)
  * [Path-to-path Variability Methodology](#path-to-path-variability-methodology)
  * [20.0 km M6.6 Path-to-path Results](#200-km-m66-path-to-path-results)
  * [50.0 km M6.6 Path-to-path Results](#500-km-m66-path-to-path-results)
  * [100.0 km M6.6 Path-to-path Results](#1000-km-m66-path-to-path-results)
  * [All Distances M6.6 Path-to-path Results](#all-distances-m66-path-to-path-results)
* [Source-strike Variability](#source-strike-variability)
  * [Source-strike Variability Methodology](#source-strike-variability-methodology)
  * [20.0 km M6.6 Source-strike Results](#200-km-m66-source-strike-results)
  * [50.0 km M6.6 Source-strike Results](#500-km-m66-source-strike-results)
  * [100.0 km M6.6 Source-strike Results](#1000-km-m66-source-strike-results)
  * [All Distances M6.6 Source-strike Results](#all-distances-m66-source-strike-results)
* [Within-event, single-site Variability](#within-event-single-site-variability)
  * [Within-event, single-site Variability Methodology](#within-event-single-site-variability-methodology)
  * [20.0 km M6.6 Within-event, single-site Results](#200-km-m66-within-event-single-site-results)
  * [50.0 km M6.6 Within-event, single-site Results](#500-km-m66-within-event-single-site-results)
  * [100.0 km M6.6 Within-event, single-site Results](#1000-km-m66-within-event-single-site-results)
  * [All Distances M6.6 Within-event, single-site Results](#all-distances-m66-within-event-single-site-results)
* [Within-event Variability](#within-event-variability)
  * [Within-event Variability Methodology](#within-event-variability-methodology)
  * [20.0 km M6.6 Within-event Results](#200-km-m66-within-event-results)
  * [50.0 km M6.6 Within-event Results](#500-km-m66-within-event-results)
  * [100.0 km M6.6 Within-event Results](#1000-km-m66-within-event-results)
  * [All Distances M6.6 Within-event Results](#all-distances-m66-within-event-results)
* [Between-events Variability](#between-events-variability)
  * [Between-events Variability Methodology](#between-events-variability-methodology)
  * [20.0 km M6.6 Between-events Results](#200-km-m66-between-events-results)
  * [50.0 km M6.6 Between-events Results](#500-km-m66-between-events-results)
  * [100.0 km M6.6 Between-events Results](#1000-km-m66-between-events-results)
  * [All Distances M6.6 Between-events Results](#all-distances-m66-between-events-results)
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
  * [BBP PartB, M6.6, Reverse, Dip=45, Ztor=3](#bbp-partb-m66-reverse-dip45-ztor3)
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
| SBSM | *34.064987, -117.29201* | 500 | 0.33 | 1.82 |
| SMCA | *34.00909, -118.48939* | 500 | 0.59 | 2.45 |
| STNI | *33.93088, -118.17881* | 500 | 0.88 | 5.57 |
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |
| WNGC | *34.041824, -118.0653* | 500 | 0.5 | 3.49 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.25 | 0.32 | 0.27 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.32 | 0.4 | 0.34 | 0.2 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.37 | 0.44 | 0.38 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.32 | 0.39 | 0.33 | 0.2 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.34 | 0.32 | 0.36 | 0.31 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.34 | 0.31 | 0.37 | 0.33 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.35 | 0.32 | 0.36 | 0.36 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.34 | 0.32 | 0.37 | 0.34 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.38 | 0.4 | 0.4 | 0.32 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.43 | 0.46 | 0.45 | 0.36 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.47 | 0.5 | 0.48 | 0.41 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.43 | 0.45 | 0.44 | 0.36 |
| Within-event | &phi; | 20 km | 0.62 | 0.65 | 0.62 | 0.55 |
| Within-event | &phi; | 50 km | 0.66 | 0.7 | 0.66 | 0.59 |
| Within-event | &phi; | 100 km | 0.69 | 0.71 | 0.71 | 0.61 |
| Within-event | &phi; | (all) | 0.65 | 0.69 | 0.66 | 0.58 |
| Between-events | &tau; | 20 km | 0.24 | 0.23 | 0.25 | 0.24 |
| Between-events | &tau; | 50 km | 0.25 | 0.22 | 0.27 | 0.25 |
| Between-events | &tau; | 100 km | 0.24 | 0.2 | 0.25 | 0.28 |
| Between-events | &tau; | (all) | 0.25 | 0.21 | 0.25 | 0.26 |

### GMPE Table
*[(top)](#table-of-contents)*

| Type | Notation | Distance | ASK2014 3s | ASK2014 5s | ASK2014 10s | BSSA2014 3s | BSSA2014 5s | BSSA2014 10s | CB2014 3s | CB2014 5s | CB2014 10s | CY2014 3s | CY2014 5s | CY2014 10s |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Source-strike | &phi;<sub>SS</sub> | 20 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Source-strike | &phi;<sub>SS</sub> | 50 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Source-strike | &phi;<sub>SS</sub> | 100 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.57 | 0.55 | 0.55 | 0.54 | 0.54 | 0.54 | 0.49 | 0.47 | 0.46 | 0.52 | 0.51 | 0.51 |
| Within-event | &phi; | 20 km | 0.64 | 0.63 | 0.63 | 0.62 | 0.62 | 0.62 | 0.58 | 0.56 | 0.55 | 0.6 | 0.6 | 0.59 |
| Within-event | &phi; | 50 km | 0.64 | 0.63 | 0.63 | 0.62 | 0.62 | 0.62 | 0.58 | 0.56 | 0.55 | 0.6 | 0.6 | 0.59 |
| Within-event | &phi; | 100 km | 0.64 | 0.63 | 0.63 | 0.62 | 0.62 | 0.62 | 0.58 | 0.56 | 0.55 | 0.6 | 0.6 | 0.59 |
| Between-events | &tau; | 20 km | 0.38 | 0.38 | 0.38 | 0.34 | 0.35 | 0.34 | 0.42 | 0.39 | 0.42 | 0.34 | 0.34 | 0.34 |
| Between-events | &tau; | 50 km | 0.38 | 0.38 | 0.38 | 0.34 | 0.35 | 0.34 | 0.42 | 0.39 | 0.42 | 0.34 | 0.34 | 0.34 |
| Between-events | &tau; | 100 km | 0.38 | 0.38 | 0.38 | 0.34 | 0.35 | 0.34 | 0.42 | 0.39 | 0.42 | 0.34 | 0.34 | 0.34 |

### Dist-Dependent Plot Table
*[(top)](#table-of-contents)*

| **&phi;<sub>P2P</sub>** | ![&phi;<sub>P2P</sub>](resources/path_m6.6_dist_periods.png) |
|-----|-----|
| **&phi;<sub>s</sub>** | ![&phi;<sub>s</sub>](resources/source_strike_m6.6_dist_periods.png) |
| **&phi;<sub>SS</sub>** | ![&phi;<sub>SS</sub>](resources/within_event_ss_m6.6_dist_periods.png) |
| **&phi;** | ![&phi;](resources/within_event_m6.6_dist_periods.png) |
| **&tau;** | ![&tau;](resources/between_events_m6.6_dist_periods.png) |


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

We also compute distance-independent &phi;<sub>P2P</sub>, which is computed as the standard deviation of all residuals across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.3** | **0.28** | **[0.07 0.84]** |  | **0.27** | **0.25** | **0.25** | **[0.03 0.66]** |  | **0.15** | **0.14** | **0.13** | **[0.03 0.4]** |
| PAS |  | 0.32 | 0.31 | 0.3 | [0.08 0.6] |  | 0.25 | 0.23 | 0.23 | [0.07 0.53] |  | 0.13 | 0.12 | 0.11 | [0.03 0.33] |
| SBSM |  | 0.25 | 0.24 | 0.23 | [0.08 0.52] |  | 0.19 | 0.17 | 0.17 | [0.03 0.41] |  | 0.14 | 0.13 | 0.12 | [0.03 0.33] |
| SMCA |  | 0.28 | 0.27 | 0.27 | [0.13 0.51] |  | 0.3 | 0.29 | 0.28 | [0.09 0.56] |  | 0.21 | 0.2 | 0.2 | [0.05 0.4] |
| STNI |  | 0.25 | 0.24 | 0.24 | [0.07 0.44] |  | 0.24 | 0.23 | 0.23 | [0.06 0.5] |  | 0.12 | 0.11 | 0.11 | [0.03 0.27] |
| USC |  | 0.3 | 0.29 | 0.29 | [0.1 0.59] |  | 0.28 | 0.27 | 0.27 | [0.08 0.49] |  | 0.16 | 0.15 | 0.15 | [0.05 0.35] |
| WNGC |  | 0.46 | 0.45 | 0.45 | [0.1 0.84] |  | 0.33 | 0.31 | 0.31 | [0.11 0.66] |  | 0.15 | 0.14 | 0.13 | [0.03 0.36] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 88 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 17 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.25 | 0.01 | [0.24 0.26] | [0.23 0.28] |
| 3 | 0.32 | 0.32 | 0.02 | [0.3 0.34] | [0.27 0.36] |
| 4 | 0.3 | 0.3 | 0.02 | [0.29 0.32] | [0.27 0.35] |
| 5 | 0.27 | 0.27 | 0.02 | [0.25 0.29] | [0.23 0.3] |
| 7.5 | 0.18 | 0.18 | 0.02 | [0.16 0.2] | [0.14 0.21] |
| 10 | 0.15 | 0.15 | 0.01 | [0.14 0.16] | [0.13 0.17] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/path_m6.6_20km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/path_m6.6_20km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

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
| **ALL SITES** |  | **0.4** | **0.39** | **0.37** | **[0.14 0.78]** |  | **0.34** | **0.33** | **0.33** | **[0.11 0.65]** |  | **0.2** | **0.19** | **0.18** | **[0.05 0.45]** |
| PAS |  | 0.37 | 0.36 | 0.35 | [0.14 0.66] |  | 0.32 | 0.32 | 0.32 | [0.11 0.57] |  | 0.16 | 0.15 | 0.14 | [0.05 0.42] |
| SBSM |  | 0.43 | 0.43 | 0.43 | [0.21 0.67] |  | 0.29 | 0.28 | 0.28 | [0.12 0.53] |  | 0.18 | 0.17 | 0.15 | [0.06 0.43] |
| SMCA |  | 0.4 | 0.4 | 0.39 | [0.22 0.6] |  | 0.38 | 0.38 | 0.37 | [0.2 0.65] |  | 0.25 | 0.24 | 0.24 | [0.12 0.45] |
| STNI |  | 0.3 | 0.3 | 0.3 | [0.16 0.46] |  | 0.3 | 0.3 | 0.29 | [0.18 0.44] |  | 0.17 | 0.16 | 0.16 | [0.07 0.36] |
| USC |  | 0.34 | 0.34 | 0.34 | [0.19 0.49] |  | 0.36 | 0.36 | 0.36 | [0.2 0.57] |  | 0.21 | 0.21 | 0.21 | [0.08 0.45] |
| WNGC |  | 0.5 | 0.5 | 0.5 | [0.27 0.78] |  | 0.37 | 0.37 | 0.36 | [0.21 0.57] |  | 0.2 | 0.19 | 0.18 | [0.08 0.42] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 77 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 4 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.32 | 0.32 | 0.01 | [0.31 0.33] | [0.3 0.34] |
| 3 | 0.4 | 0.39 | 0.02 | [0.37 0.41] | [0.35 0.43] |
| 4 | 0.37 | 0.36 | 0.02 | [0.35 0.38] | [0.33 0.41] |
| 5 | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.31 0.37] |
| 7.5 | 0.27 | 0.27 | 0.02 | [0.26 0.29] | [0.24 0.31] |
| 10 | 0.2 | 0.2 | 0.01 | [0.18 0.21] | [0.16 0.22] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/path_m6.6_50km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/path_m6.6_50km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

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
| **ALL SITES** |  | **0.44** | **0.43** | **0.41** | **[0.19 0.83]** |  | **0.38** | **0.38** | **0.37** | **[0.17 0.61]** |  | **0.24** | **0.24** | **0.23** | **[0.1 0.46]** |
| PAS |  | 0.4 | 0.39 | 0.38 | [0.2 0.67] |  | 0.34 | 0.34 | 0.34 | [0.17 0.5] |  | 0.21 | 0.21 | 0.21 | [0.12 0.35] |
| SBSM |  | 0.54 | 0.54 | 0.54 | [0.25 0.83] |  | 0.41 | 0.41 | 0.41 | [0.22 0.58] |  | 0.22 | 0.22 | 0.2 | [0.1 0.46] |
| SMCA |  | 0.48 | 0.48 | 0.48 | [0.3 0.71] |  | 0.44 | 0.44 | 0.44 | [0.27 0.61] |  | 0.28 | 0.28 | 0.28 | [0.16 0.45] |
| STNI |  | 0.31 | 0.31 | 0.31 | [0.19 0.51] |  | 0.35 | 0.35 | 0.35 | [0.21 0.49] |  | 0.24 | 0.24 | 0.23 | [0.13 0.43] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.24 0.56] |  | 0.36 | 0.36 | 0.35 | [0.24 0.52] |  | 0.27 | 0.27 | 0.27 | [0.16 0.41] |
| WNGC |  | 0.49 | 0.48 | 0.47 | [0.26 0.83] |  | 0.37 | 0.37 | 0.37 | [0.18 0.57] |  | 0.22 | 0.22 | 0.21 | [0.13 0.41] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 83 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 62 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.37 | 0.37 | 0.01 | [0.35 0.38] | [0.34 0.4] |
| 3 | 0.44 | 0.44 | 0.02 | [0.41 0.46] | [0.4 0.49] |
| 4 | 0.42 | 0.42 | 0.02 | [0.4 0.44] | [0.38 0.46] |
| 5 | 0.38 | 0.38 | 0.02 | [0.36 0.4] | [0.35 0.41] |
| 7.5 | 0.32 | 0.31 | 0.01 | [0.3 0.33] | [0.29 0.35] |
| 10 | 0.24 | 0.24 | 0.01 | [0.23 0.26] | [0.22 0.27] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/path_m6.6_100km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/path_m6.6_100km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_100km_3s_hist.png) | ![5s](resources/path_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_100km_10s_hist.png) |  |


### All Distances M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.37** | **0.35** | **[0.07 0.84]** |  | **0.33** | **0.32** | **0.32** | **[0.03 0.66]** |  | **0.2** | **0.19** | **0.19** | **[0.03 0.46]** |
| PAS |  | 0.36 | 0.35 | 0.34 | [0.08 0.67] |  | 0.31 | 0.3 | 0.3 | [0.07 0.57] |  | 0.17 | 0.16 | 0.16 | [0.03 0.42] |
| SBSM |  | 0.43 | 0.4 | 0.41 | [0.08 0.83] |  | 0.31 | 0.29 | 0.28 | [0.03 0.58] |  | 0.18 | 0.17 | 0.16 | [0.03 0.46] |
| SMCA |  | 0.4 | 0.38 | 0.39 | [0.13 0.71] |  | 0.38 | 0.37 | 0.37 | [0.09 0.65] |  | 0.25 | 0.24 | 0.24 | [0.05 0.45] |
| STNI |  | 0.29 | 0.29 | 0.29 | [0.07 0.51] |  | 0.3 | 0.29 | 0.3 | [0.06 0.5] |  | 0.18 | 0.17 | 0.17 | [0.03 0.43] |
| USC |  | 0.33 | 0.33 | 0.33 | [0.1 0.59] |  | 0.34 | 0.33 | 0.33 | [0.08 0.57] |  | 0.22 | 0.21 | 0.21 | [0.05 0.45] |
| WNGC |  | 0.49 | 0.48 | 0.47 | [0.1 0.84] |  | 0.36 | 0.35 | 0.35 | [0.11 0.66] |  | 0.19 | 0.18 | 0.18 | [0.03 0.42] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 384 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 66 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.32 | 0.32 | 0.01 | [0.31 0.32] | [0.3 0.33] |
| 3 | 0.39 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.4] |
| 4 | 0.37 | 0.36 | 0.01 | [0.36 0.37] | [0.35 0.38] |
| 5 | 0.33 | 0.33 | 0.01 | [0.32 0.34] | [0.31 0.35] |
| 7.5 | 0.26 | 0.26 | 0.01 | [0.26 0.27] | [0.25 0.28] |
| 10 | 0.2 | 0.2 | 0.01 | [0.19 0.21] | [0.18 0.21] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/path_m6.6_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/path_m6.6_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/path_m6.6_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_3s_hist.png) | ![5s](resources/path_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_10s_hist.png) |  |


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

We also compute distance-independent &phi;<sub>s</sub>, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Path]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_source_strike.png)


### 20.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.31** | **0.31** | **[0.09 0.68]** |  | **0.36** | **0.35** | **0.34** | **[0.08 0.77]** |  | **0.31** | **0.3** | **0.29** | **[0.06 0.84]** |
| PAS |  | 0.33 | 0.32 | 0.32 | [0.1 0.68] |  | 0.37 | 0.37 | 0.36 | [0.12 0.73] |  | 0.32 | 0.31 | 0.3 | [0.08 0.77] |
| SBSM |  | 0.36 | 0.35 | 0.34 | [0.14 0.68] |  | 0.38 | 0.37 | 0.36 | [0.11 0.68] |  | 0.31 | 0.3 | 0.3 | [0.15 0.56] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.1 0.66] |  | 0.38 | 0.37 | 0.37 | [0.11 0.77] |  | 0.32 | 0.31 | 0.3 | [0.08 0.84] |
| STNI |  | 0.29 | 0.28 | 0.27 | [0.1 0.6] |  | 0.32 | 0.31 | 0.3 | [0.09 0.72] |  | 0.3 | 0.28 | 0.26 | [0.06 0.83] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.65] |  | 0.34 | 0.33 | 0.32 | [0.09 0.65] |  | 0.3 | 0.29 | 0.27 | [0.06 0.84] |
| WNGC |  | 0.33 | 0.32 | 0.31 | [0.1 0.65] |  | 0.37 | 0.36 | 0.35 | [0.08 0.71] |  | 0.31 | 0.3 | 0.28 | [0.07 0.74] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 52 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 53 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.3 0.37] |
| 3 | 0.32 | 0.32 | 0.02 | [0.3 0.34] | [0.27 0.36] |
| 4 | 0.34 | 0.33 | 0.02 | [0.31 0.36] | [0.28 0.37] |
| 5 | 0.36 | 0.36 | 0.02 | [0.33 0.38] | [0.31 0.41] |
| 7.5 | 0.36 | 0.36 | 0.02 | [0.33 0.38] | [0.31 0.41] |
| 10 | 0.31 | 0.31 | 0.02 | [0.29 0.33] | [0.27 0.38] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_20km_3s_hist.png) | ![5s](resources/source_strike_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_20km_10s_hist.png) |  |

Here are plots of the &phi;<sub>s</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.31** | **0.3** | **0.29** | **[0.07 0.77]** |  | **0.37** | **0.36** | **0.35** | **[0.06 0.78]** |  | **0.33** | **0.33** | **0.31** | **[0.08 0.89]** |
| PAS |  | 0.3 | 0.29 | 0.29 | [0.09 0.68] |  | 0.37 | 0.36 | 0.35 | [0.09 0.71] |  | 0.34 | 0.33 | 0.31 | [0.12 0.81] |
| SBSM |  | 0.38 | 0.37 | 0.36 | [0.11 0.75] |  | 0.4 | 0.39 | 0.38 | [0.1 0.7] |  | 0.33 | 0.32 | 0.32 | [0.11 0.71] |
| SMCA |  | 0.32 | 0.31 | 0.3 | [0.07 0.77] |  | 0.39 | 0.38 | 0.37 | [0.09 0.78] |  | 0.33 | 0.32 | 0.31 | [0.08 0.78] |
| STNI |  | 0.28 | 0.27 | 0.26 | [0.09 0.62] |  | 0.35 | 0.34 | 0.33 | [0.09 0.74] |  | 0.35 | 0.34 | 0.32 | [0.13 0.89] |
| USC |  | 0.29 | 0.28 | 0.27 | [0.09 0.67] |  | 0.35 | 0.34 | 0.33 | [0.09 0.72] |  | 0.34 | 0.32 | 0.31 | [0.1 0.88] |
| WNGC |  | 0.3 | 0.29 | 0.28 | [0.08 0.69] |  | 0.37 | 0.35 | 0.35 | [0.06 0.68] |  | 0.33 | 0.32 | 0.31 | [0.1 0.76] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 56 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 25 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.34 | 0.34 | 0.02 | [0.33 0.36] | [0.31 0.38] |
| 3 | 0.31 | 0.31 | 0.02 | [0.29 0.33] | [0.27 0.36] |
| 4 | 0.34 | 0.34 | 0.03 | [0.31 0.36] | [0.29 0.39] |
| 5 | 0.37 | 0.37 | 0.03 | [0.34 0.4] | [0.32 0.42] |
| 7.5 | 0.36 | 0.36 | 0.03 | [0.33 0.38] | [0.3 0.41] |
| 10 | 0.33 | 0.33 | 0.03 | [0.31 0.36] | [0.29 0.39] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_50km_3s_hist.png) | ![5s](resources/source_strike_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_50km_10s_hist.png) |  |

Here are plots of the &phi;<sub>s</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.07 0.78]** |  | **0.36** | **0.35** | **0.35** | **[0.06 0.75]** |  | **0.36** | **0.35** | **0.34** | **[0.07 0.94]** |
| PAS |  | 0.31 | 0.3 | 0.29 | [0.07 0.78] |  | 0.35 | 0.34 | 0.34 | [0.09 0.69] |  | 0.37 | 0.36 | 0.35 | [0.07 0.87] |
| SBSM |  | 0.35 | 0.34 | 0.33 | [0.1 0.77] |  | 0.36 | 0.35 | 0.35 | [0.1 0.7] |  | 0.33 | 0.33 | 0.32 | [0.1 0.78] |
| SMCA |  | 0.31 | 0.3 | 0.29 | [0.1 0.73] |  | 0.35 | 0.34 | 0.34 | [0.07 0.68] |  | 0.35 | 0.34 | 0.33 | [0.08 0.85] |
| STNI |  | 0.3 | 0.29 | 0.29 | [0.09 0.73] |  | 0.36 | 0.35 | 0.35 | [0.08 0.71] |  | 0.38 | 0.37 | 0.36 | [0.1 0.94] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.85] |
| WNGC |  | 0.32 | 0.31 | 0.3 | [0.09 0.78] |  | 0.38 | 0.37 | 0.36 | [0.06 0.69] |  | 0.36 | 0.35 | 0.34 | [0.08 0.86] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 47 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 98 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.35 | 0.35 | 0.02 | [0.33 0.37] | [0.32 0.39] |
| 3 | 0.32 | 0.31 | 0.02 | [0.3 0.34] | [0.27 0.37] |
| 4 | 0.34 | 0.34 | 0.02 | [0.32 0.36] | [0.29 0.4] |
| 5 | 0.36 | 0.36 | 0.02 | [0.34 0.39] | [0.31 0.41] |
| 7.5 | 0.37 | 0.38 | 0.03 | [0.35 0.41] | [0.31 0.43] |
| 10 | 0.36 | 0.36 | 0.03 | [0.34 0.39] | [0.31 0.43] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_100km_3s_hist.png) | ![5s](resources/source_strike_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_100km_10s_hist.png) |  |

Here are plots of the &phi;<sub>s</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/source_strike_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/source_strike_scatter__v_prop_3s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_5s_residual.png) | ![Scatter](resources/source_strike_scatter__v_prop_10s_residual.png) |


### All Distances M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.07 0.78]** |  | **0.37** | **0.35** | **0.35** | **[0.06 0.78]** |  | **0.34** | **0.32** | **0.31** | **[0.06 0.94]** |
| PAS |  | 0.31 | 0.31 | 0.3 | [0.07 0.78] |  | 0.37 | 0.35 | 0.35 | [0.09 0.73] |  | 0.34 | 0.33 | 0.32 | [0.07 0.87] |
| SBSM |  | 0.36 | 0.35 | 0.35 | [0.1 0.77] |  | 0.38 | 0.37 | 0.36 | [0.1 0.7] |  | 0.32 | 0.32 | 0.31 | [0.1 0.78] |
| SMCA |  | 0.32 | 0.31 | 0.3 | [0.07 0.77] |  | 0.38 | 0.36 | 0.36 | [0.07 0.78] |  | 0.34 | 0.33 | 0.31 | [0.08 0.85] |
| STNI |  | 0.29 | 0.28 | 0.27 | [0.09 0.73] |  | 0.35 | 0.33 | 0.33 | [0.08 0.74] |  | 0.34 | 0.33 | 0.32 | [0.06 0.94] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.75] |  | 0.35 | 0.34 | 0.33 | [0.09 0.75] |  | 0.33 | 0.32 | 0.31 | [0.06 0.88] |
| WNGC |  | 0.32 | 0.31 | 0.3 | [0.08 0.78] |  | 0.37 | 0.36 | 0.35 | [0.06 0.71] |  | 0.33 | 0.32 | 0.31 | [0.07 0.86] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 222 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 228 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.34 | 0.34 | 0.01 | [0.33 0.34] | [0.33 0.35] |
| 3 | 0.32 | 0.31 | 0.01 | [0.3 0.32] | [0.29 0.34] |
| 4 | 0.34 | 0.33 | 0.01 | [0.32 0.34] | [0.31 0.36] |
| 5 | 0.37 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.38] |
| 7.5 | 0.36 | 0.35 | 0.01 | [0.35 0.37] | [0.33 0.38] |
| 10 | 0.34 | 0.33 | 0.01 | [0.32 0.34] | [0.31 0.36] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/source_strike_m6.6_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/source_strike_m6.6_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_3s_hist.png) | ![5s](resources/source_strike_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_10s_hist.png) |  |


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

We also compute distance-independent &phi;<sub>SS</sub>, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event_ss.png)


### 20.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.4** | **0.39** | **0.37** | **[0.24 0.66]** |  | **0.4** | **0.39** | **0.39** | **[0.24 0.63]** |  | **0.32** | **0.31** | **0.3** | **[0.13 0.67]** |
| PAS |  | 0.41 | 0.41 | 0.4 | [0.33 0.58] |  | 0.41 | 0.4 | 0.4 | [0.26 0.62] |  | 0.33 | 0.31 | 0.3 | [0.17 0.61] |
| SBSM |  | 0.39 | 0.39 | 0.38 | [0.28 0.59] |  | 0.4 | 0.39 | 0.38 | [0.24 0.61] |  | 0.32 | 0.31 | 0.31 | [0.21 0.47] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.28 0.55] |  | 0.42 | 0.41 | 0.41 | [0.3 0.59] |  | 0.36 | 0.35 | 0.34 | [0.22 0.65] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.24 0.47] |  | 0.35 | 0.35 | 0.35 | [0.25 0.49] |  | 0.3 | 0.28 | 0.27 | [0.13 0.67] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.27 0.52] |  | 0.38 | 0.38 | 0.38 | [0.28 0.55] |  | 0.32 | 0.3 | 0.29 | [0.19 0.66] |
| WNGC |  | 0.51 | 0.51 | 0.5 | [0.41 0.66] |  | 0.45 | 0.44 | 0.44 | [0.29 0.63] |  | 0.32 | 0.3 | 0.29 | [0.18 0.62] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.38 | 0.38 | 0.01 | [0.36 0.39] | [0.35 0.4] |
| 3 | 0.4 | 0.4 | 0.02 | [0.38 0.41] | [0.36 0.43] |
| 4 | 0.4 | 0.39 | 0.02 | [0.38 0.41] | [0.35 0.43] |
| 5 | 0.4 | 0.4 | 0.02 | [0.38 0.41] | [0.35 0.43] |
| 7.5 | 0.37 | 0.37 | 0.02 | [0.35 0.39] | [0.32 0.41] |
| 10 | 0.32 | 0.32 | 0.02 | [0.3 0.34] | [0.28 0.36] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_20km_10s_hist.png) |  |

Here are plots of the &phi;<sub>SS</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 50.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.46** | **0.45** | **0.44** | **[0.3 0.74]** |  | **0.45** | **0.44** | **0.44** | **[0.29 0.65]** |  | **0.36** | **0.35** | **0.34** | **[0.22 0.77]** |
| PAS |  | 0.42 | 0.42 | 0.41 | [0.3 0.58] |  | 0.43 | 0.43 | 0.42 | [0.29 0.57] |  | 0.34 | 0.33 | 0.31 | [0.22 0.69] |
| SBSM |  | 0.52 | 0.52 | 0.52 | [0.38 0.74] |  | 0.46 | 0.45 | 0.44 | [0.31 0.64] |  | 0.35 | 0.35 | 0.33 | [0.22 0.59] |
| SMCA |  | 0.45 | 0.45 | 0.45 | [0.39 0.62] |  | 0.48 | 0.48 | 0.47 | [0.38 0.65] |  | 0.38 | 0.38 | 0.36 | [0.26 0.69] |
| STNI |  | 0.36 | 0.36 | 0.36 | [0.31 0.53] |  | 0.41 | 0.41 | 0.4 | [0.31 0.55] |  | 0.36 | 0.35 | 0.33 | [0.23 0.77] |
| USC |  | 0.4 | 0.4 | 0.39 | [0.34 0.56] |  | 0.45 | 0.44 | 0.44 | [0.35 0.61] |  | 0.37 | 0.36 | 0.35 | [0.25 0.71] |
| WNGC |  | 0.54 | 0.54 | 0.53 | [0.44 0.64] |  | 0.46 | 0.46 | 0.45 | [0.37 0.58] |  | 0.35 | 0.34 | 0.33 | [0.24 0.65] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.42 | 0.02 | [0.41 0.44] | [0.39 0.45] |
| 3 | 0.46 | 0.45 | 0.02 | [0.43 0.47] | [0.41 0.49] |
| 4 | 0.45 | 0.44 | 0.02 | [0.42 0.46] | [0.4 0.48] |
| 5 | 0.45 | 0.44 | 0.02 | [0.42 0.47] | [0.4 0.48] |
| 7.5 | 0.41 | 0.4 | 0.02 | [0.38 0.43] | [0.36 0.47] |
| 10 | 0.36 | 0.36 | 0.03 | [0.33 0.38] | [0.32 0.43] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_50km_10s_hist.png) |  |

Here are plots of the &phi;<sub>SS</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### 100.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.5** | **0.49** | **0.48** | **[0.32 0.77]** |  | **0.48** | **0.48** | **0.48** | **[0.34 0.63]** |  | **0.41** | **0.4** | **0.39** | **[0.25 0.82]** |
| PAS |  | 0.46 | 0.45 | 0.45 | [0.35 0.67] |  | 0.45 | 0.45 | 0.44 | [0.34 0.57] |  | 0.4 | 0.39 | 0.37 | [0.26 0.77] |
| SBSM |  | 0.6 | 0.59 | 0.6 | [0.43 0.77] |  | 0.51 | 0.5 | 0.5 | [0.41 0.63] |  | 0.38 | 0.37 | 0.36 | [0.25 0.67] |
| SMCA |  | 0.53 | 0.53 | 0.53 | [0.43 0.71] |  | 0.52 | 0.52 | 0.51 | [0.42 0.62] |  | 0.42 | 0.42 | 0.4 | [0.33 0.78] |
| STNI |  | 0.39 | 0.39 | 0.38 | [0.32 0.62] |  | 0.46 | 0.46 | 0.45 | [0.35 0.6] |  | 0.42 | 0.41 | 0.4 | [0.3 0.82] |
| USC |  | 0.43 | 0.43 | 0.42 | [0.35 0.64] |  | 0.46 | 0.46 | 0.45 | [0.37 0.59] |  | 0.42 | 0.42 | 0.4 | [0.31 0.79] |
| WNGC |  | 0.55 | 0.54 | 0.53 | [0.41 0.75] |  | 0.48 | 0.48 | 0.48 | [0.38 0.6] |  | 0.4 | 0.39 | 0.37 | [0.28 0.76] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.46 | 0.01 | [0.45 0.48] | [0.44 0.5] |
| 3 | 0.5 | 0.5 | 0.02 | [0.47 0.51] | [0.45 0.55] |
| 4 | 0.5 | 0.5 | 0.02 | [0.48 0.51] | [0.46 0.54] |
| 5 | 0.48 | 0.48 | 0.02 | [0.46 0.5] | [0.44 0.52] |
| 7.5 | 0.45 | 0.45 | 0.02 | [0.43 0.47] | [0.41 0.5] |
| 10 | 0.41 | 0.4 | 0.02 | [0.38 0.43] | [0.37 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_100km_10s_hist.png) |  |

Here are plots of the &phi;<sub>SS</sub> as a function of various parameters for disaggregation.

| 3s | 5s | 10s |
|-----|-----|-----|
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_std_dev.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_std_dev.png) |
| ![Scatter](resources/within_event_ss_scatter__v_prop_3s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_5s_residual.png) | ![Scatter](resources/within_event_ss_scatter__v_prop_10s_residual.png) |


### All Distances M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.45** | **0.44** | **0.43** | **[0.24 0.77]** |  | **0.44** | **0.44** | **0.44** | **[0.24 0.65]** |  | **0.36** | **0.35** | **0.35** | **[0.13 0.82]** |
| PAS |  | 0.43 | 0.43 | 0.42 | [0.3 0.67] |  | 0.43 | 0.42 | 0.43 | [0.26 0.62] |  | 0.36 | 0.35 | 0.34 | [0.17 0.77] |
| SBSM |  | 0.51 | 0.5 | 0.51 | [0.28 0.77] |  | 0.46 | 0.45 | 0.45 | [0.24 0.64] |  | 0.35 | 0.34 | 0.34 | [0.21 0.67] |
| SMCA |  | 0.46 | 0.45 | 0.45 | [0.28 0.71] |  | 0.47 | 0.47 | 0.47 | [0.3 0.65] |  | 0.39 | 0.38 | 0.37 | [0.22 0.78] |
| STNI |  | 0.36 | 0.36 | 0.35 | [0.24 0.62] |  | 0.41 | 0.4 | 0.4 | [0.25 0.6] |  | 0.36 | 0.35 | 0.34 | [0.13 0.82] |
| USC |  | 0.4 | 0.39 | 0.39 | [0.27 0.64] |  | 0.43 | 0.43 | 0.43 | [0.28 0.61] |  | 0.37 | 0.36 | 0.35 | [0.19 0.79] |
| WNGC |  | 0.53 | 0.53 | 0.52 | [0.41 0.75] |  | 0.46 | 0.46 | 0.46 | [0.29 0.63] |  | 0.35 | 0.34 | 0.34 | [0.18 0.76] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 1350 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.42 | 0.01 | [0.42 0.43] | [0.41 0.44] |
| 3 | 0.45 | 0.45 | 0.01 | [0.44 0.46] | [0.44 0.47] |
| 4 | 0.45 | 0.45 | 0.01 | [0.44 0.46] | [0.44 0.47] |
| 5 | 0.44 | 0.44 | 0.01 | [0.44 0.45] | [0.43 0.46] |
| 7.5 | 0.41 | 0.41 | 0.01 | [0.4 0.42] | [0.38 0.44] |
| 10 | 0.36 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.39] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_PAS_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SBSM_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SMCA_downsampled_hist.png) |
| **STNI** | **USC** | **WNGC** |
| ![Dowmsampled Histogram](resources/within_event_ss_m6.6_STNI_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WNGC_downsampled_hist.png) |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_10s_hist.png) |  |


## Within-event Variability
*[(top)](#table-of-contents)*

### Within-event Variability Methodology
*[(top)](#table-of-contents)*

Within-event variability, denoted &phi; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[100 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 3888 combinations of:

* Site *[6 unique]* (Singleton)
* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We subdivide residual sets such that there is only a single unique value of each quantity marked '(Singleton)' above.

We take &phi; to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture. This is done separately for each set of sites with the same V<sub>S30</sub> value.

We also compute distance-independent &phi;, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event.png)


### 20.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_20km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.39** | **0.39** | **0.38** | **[0.02 1.1]** |  | **0.41** | **0.4** | **0.39** | **[0.02 1.25]** |  | **0.44** | **0.45** | **0.43** | **[0.03 1.19]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 20 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 85 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.42 | 0.43 | 0.05 | [0.38 0.47] | [0.32 0.56] |
| 3 | 0.39 | 0.39 | 0.07 | [0.31 0.45] | [0.25 0.52] |
| 4 | 0.38 | 0.38 | 0.07 | [0.32 0.47] | [0.27 0.58] |
| 5 | 0.41 | 0.4 | 0.08 | [0.33 0.49] | [0.25 0.59] |
| 7.5 | 0.48 | 0.5 | 0.08 | [0.41 0.56] | [0.3 0.67] |
| 10 | 0.44 | 0.45 | 0.07 | [0.37 0.51] | [0.32 0.63] |

This plot shows the distribution of period-independent downsampled &phi;.

![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist.png)

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_20km_10s_hist.png) |  |


### 50.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.46** | **0.46** | **0.45** | **[0.03 1.28]** |  | **0.46** | **0.46** | **0.44** | **[0.02 1.4]** |  | **0.49** | **0.5** | **0.49** | **[0.04 1.48]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 17 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 64 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.48 | 0.46 | 0.07 | [0.4 0.53] | [0.35 0.61] |
| 3 | 0.46 | 0.43 | 0.08 | [0.33 0.51] | [0.29 0.6] |
| 4 | 0.44 | 0.42 | 0.09 | [0.33 0.51] | [0.24 0.6] |
| 5 | 0.46 | 0.45 | 0.09 | [0.34 0.54] | [0.28 0.63] |
| 7.5 | 0.53 | 0.51 | 0.1 | [0.42 0.61] | [0.34 0.75] |
| 10 | 0.49 | 0.47 | 0.1 | [0.41 0.58] | [0.33 0.72] |

This plot shows the distribution of period-independent downsampled &phi;.

![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist.png)

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_50km_10s_hist.png) |  |


### 100.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.49** | **0.49** | **0.48** | **[0.02 1.47]** |  | **0.5** | **0.5** | **0.49** | **[0.02 1.3]** |  | **0.53** | **0.53** | **0.52** | **[0.01 1.52]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 15 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 130 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.52 | 0.52 | 0.06 | [0.45 0.57] | [0.38 0.65] |
| 3 | 0.49 | 0.49 | 0.1 | [0.39 0.6] | [0.32 0.72] |
| 4 | 0.49 | 0.48 | 0.11 | [0.36 0.59] | [0.27 0.74] |
| 5 | 0.5 | 0.51 | 0.09 | [0.41 0.61] | [0.32 0.69] |
| 7.5 | 0.57 | 0.58 | 0.1 | [0.45 0.66] | [0.38 0.79] |
| 10 | 0.53 | 0.53 | 0.09 | [0.42 0.6] | [0.34 0.75] |

This plot shows the distribution of period-independent downsampled &phi;.

![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist.png)

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_100km_10s_hist.png) |  |


### All Distances M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.45** | **0.44** | **0.43** | **[0.02 1.47]** |  | **0.46** | **0.45** | **0.44** | **[0.02 1.4]** |  | **0.49** | **0.49** | **0.48** | **[0.01 1.52]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 87 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 363 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.45 | 0.03 | [0.42 0.49] | [0.4 0.51] |
| 3 | 0.45 | 0.42 | 0.04 | [0.38 0.47] | [0.34 0.51] |
| 4 | 0.44 | 0.42 | 0.04 | [0.39 0.46] | [0.34 0.5] |
| 5 | 0.46 | 0.44 | 0.04 | [0.41 0.49] | [0.38 0.54] |
| 7.5 | 0.53 | 0.51 | 0.05 | [0.46 0.56] | [0.41 0.61] |
| 10 | 0.49 | 0.47 | 0.04 | [0.43 0.51] | [0.39 0.55] |

This plot shows the distribution of period-independent downsampled &phi;.

![Dowmsampled Histogram](resources/within_event_m6.6_downsampled_hist.png)

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_3s_hist.png) | ![5s](resources/within_event_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_10s_hist.png) |  |


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[100 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 3888 combinations of:

* Site *[6 unique]*
* Rupture Strike *[18 unique]*
* Path *[36 unique]*

We take &tau; to be the standard deviation of all &delta;B<sub>e</sub>. This is done separately for each set of sites with the same V<sub>S30</sub> value. Single-site values are also reported.

We also compute distance-independent &tau;, which we take to be the mean value across all distances.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_between_events.png)


### 20.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.23** | **-3.34** | **[-3.86 -2.8]** | **0.25** | **-4.02** | **[-4.63 -3.42]** | **0.25** | **-5.45** | **[-6.14 -4.89]** |
| PAS | 0.2 | -4.73 | [-5.21 -4.23] | 0.24 | -5.27 | [-5.88 -4.65] | 0.27 | -6.39 | [-7.07 -5.79] |
| SBSM | 0.28 | -3.19 | [-3.85 -2.5] | 0.27 | -4.2 | [-4.85 -3.5] | 0.22 | -5.94 | [-6.64 -5.51] |
| SMCA | 0.21 | -3.36 | [-3.8 -2.83] | 0.25 | -3.86 | [-4.53 -3.25] | 0.25 | -5.38 | [-6.04 -4.81] |
| STNI | 0.21 | -3.3 | [-3.78 -2.81] | 0.23 | -3.89 | [-4.44 -3.41] | 0.27 | -5.01 | [-5.7 -4.38] |
| USC | 0.23 | -3.42 | [-3.99 -2.87] | 0.25 | -4.06 | [-4.67 -3.49] | 0.26 | -5.41 | [-6.1 -4.83] |
| WNGC | 0.23 | -3.48 | [-3.97 -2.93] | 0.27 | -4.1 | [-4.68 -3.47] | 0.25 | -5.55 | [-6.22 -4.99] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.26 | 0.06 | [0.19 0.32] | [0.14 0.39] |
| 3 | 0.23 | 0.24 | 0.1 | [0.14 0.35] | [0.07 0.44] |
| 4 | 0.25 | 0.24 | 0.1 | [0.15 0.37] | [0.06 0.48] |
| 5 | 0.25 | 0.27 | 0.1 | [0.15 0.36] | [0.08 0.49] |
| 7.5 | 0.27 | 0.26 | 0.1 | [0.17 0.4] | [0.09 0.49] |
| 10 | 0.25 | 0.26 | 0.11 | [0.14 0.37] | [0.07 0.47] |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist.png)


### 50.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.23** | **-4.14** | **[-4.62 -3.6]** | **0.27** | **-4.63** | **[-5.35 -3.9]** | **0.26** | **-6.07** | **[-6.8 -5.37]** |
| PAS | 0.22 | -5.57 | [-6.05 -5.03] | 0.27 | -5.92 | [-6.59 -5.19] | 0.29 | -6.99 | [-7.74 -6.19] |
| SBSM | 0.31 | -3.89 | [-4.53 -3.2] | 0.28 | -4.83 | [-5.55 -4.08] | 0.23 | -6.55 | [-7.26 -6] |
| SMCA | 0.19 | -4.26 | [-4.68 -3.79] | 0.26 | -4.61 | [-5.25 -3.88] | 0.25 | -6.04 | [-6.73 -5.34] |
| STNI | 0.2 | -4.02 | [-4.5 -3.56] | 0.26 | -4.36 | [-5.04 -3.67] | 0.29 | -5.51 | [-6.23 -4.71] |
| USC | 0.24 | -4.23 | [-4.75 -3.64] | 0.26 | -4.69 | [-5.4 -3.99] | 0.27 | -6 | [-6.75 -5.26] |
| WNGC | 0.23 | -4.29 | [-4.81 -3.71] | 0.27 | -4.68 | [-5.41 -3.95] | 0.26 | -6.18 | [-6.9 -5.46] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.29 | 0.09 | [0.22 0.4] | [0.14 0.46] |
| 3 | 0.23 | 0.28 | 0.13 | [0.18 0.43] | [0.08 0.61] |
| 4 | 0.26 | 0.31 | 0.12 | [0.18 0.41] | [0.08 0.62] |
| 5 | 0.27 | 0.3 | 0.14 | [0.17 0.44] | [0.1 0.59] |
| 7.5 | 0.25 | 0.29 | 0.13 | [0.17 0.44] | [0.07 0.64] |
| 10 | 0.26 | 0.27 | 0.14 | [0.13 0.4] | [0.04 0.57] |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist.png)


### 100.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.2** | **-4.77** | **[-5.24 -4.3]** | **0.25** | **-5.23** | **[-5.83 -4.57]** | **0.29** | **-6.52** | **[-7.22 -5.76]** |
| PAS | 0.2 | -6.17 | [-6.6 -5.73] | 0.24 | -6.57 | [-7.14 -5.92] | 0.32 | -7.39 | [-8.13 -6.57] |
| SBSM | 0.3 | -4.6 | [-5.16 -3.87] | 0.26 | -5.51 | [-6.2 -4.87] | 0.25 | -7.03 | [-7.71 -6.4] |
| SMCA | 0.18 | -4.86 | [-5.27 -4.5] | 0.24 | -5.18 | [-5.72 -4.54] | 0.3 | -6.48 | [-7.22 -5.71] |
| STNI | 0.18 | -4.65 | [-5.08 -4.22] | 0.25 | -4.92 | [-5.5 -4.23] | 0.3 | -5.97 | [-6.67 -5.18] |
| USC | 0.21 | -4.87 | [-5.35 -4.37] | 0.26 | -5.23 | [-5.85 -4.55] | 0.3 | -6.44 | [-7.14 -5.67] |
| WNGC | 0.2 | -4.88 | [-5.36 -4.43] | 0.25 | -5.32 | [-5.94 -4.66] | 0.29 | -6.58 | [-7.27 -5.81] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.27 | 0.1 | [0.19 0.35] | [0.09 0.5] |
| 3 | 0.2 | 0.21 | 0.12 | [0.1 0.34] | [0.03 0.47] |
| 4 | 0.24 | 0.24 | 0.12 | [0.13 0.4] | [0.03 0.48] |
| 5 | 0.25 | 0.24 | 0.15 | [0.11 0.42] | [0.02 0.59] |
| 7.5 | 0.26 | 0.32 | 0.15 | [0.15 0.49] | [0.03 0.63] |
| 10 | 0.29 | 0.33 | 0.16 | [0.16 0.5] | [0.06 0.64] |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist.png)


### All Distances M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.22** | **-4.09** | **[-5.24 -2.8]** | **0.25** | **-4.63** | **[-5.83 -3.42]** | **0.26** | **-6.01** | **[-7.22 -4.89]** |
| PAS | 0.21 | -5.49 | [-6.6 -4.23] | 0.25 | -5.92 | [-7.14 -4.65] | 0.29 | -6.93 | [-8.13 -5.79] |
| SBSM | 0.3 | -3.89 | [-5.16 -2.5] | 0.27 | -4.85 | [-6.2 -3.5] | 0.23 | -6.51 | [-7.71 -5.51] |
| SMCA | 0.19 | -4.16 | [-5.27 -2.83] | 0.25 | -4.55 | [-5.72 -3.25] | 0.27 | -5.96 | [-7.22 -4.81] |
| STNI | 0.2 | -3.99 | [-5.08 -2.81] | 0.25 | -4.39 | [-5.5 -3.41] | 0.29 | -5.5 | [-6.67 -4.38] |
| USC | 0.22 | -4.17 | [-5.35 -2.87] | 0.26 | -4.66 | [-5.85 -3.49] | 0.28 | -5.95 | [-7.14 -4.83] |
| WNGC | 0.22 | -4.22 | [-5.36 -2.93] | 0.27 | -4.7 | [-5.94 -3.47] | 0.27 | -6.1 | [-7.27 -4.99] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 1350 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.31 | 0.04 | [0.28 0.35] | [0.25 0.41] |
| 3 | 0.22 | 0.28 | 0.06 | [0.24 0.35] | [0.17 0.41] |
| 4 | 0.25 | 0.3 | 0.05 | [0.25 0.35] | [0.2 0.41] |
| 5 | 0.25 | 0.31 | 0.06 | [0.26 0.38] | [0.21 0.42] |
| 7.5 | 0.26 | 0.32 | 0.06 | [0.28 0.39] | [0.23 0.46] |
| 10 | 0.26 | 0.32 | 0.06 | [0.27 0.39] | [0.21 0.46] |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist.png)


## Azumth Dependence
*[(top)](#table-of-contents)*

### PAS Azumth Dependence
*[(top)](#table-of-contents)*

#### PAS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
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
| **M6.6 Reverse** | **SBSM** | **PASS** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **SMCA** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **STNI** | **PASS** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **USC** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **WNGC** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **5sites_Vs30_500** | **PASS** | **PASS** | *(PASS)* |

### BBP PartB, M6.6, Reverse, Dip=45, Ztor=3
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_PAS.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_WNGC.png) |
| **5sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_5sites_Vs30_500.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M6.6 | 20.0 km | PAS | [sa_PAS_m6.6_20.0km.csv.gz](resources/sa_PAS_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SBSM | [sa_SBSM_m6.6_20.0km.csv.gz](resources/sa_SBSM_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SMCA | [sa_SMCA_m6.6_20.0km.csv.gz](resources/sa_SMCA_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | STNI | [sa_STNI_m6.6_20.0km.csv.gz](resources/sa_STNI_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | USC | [sa_USC_m6.6_20.0km.csv.gz](resources/sa_USC_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | WNGC | [sa_WNGC_m6.6_20.0km.csv.gz](resources/sa_WNGC_m6.6_20.0km.csv.gz) |
| M6.6 | 50.0 km | PAS | [sa_PAS_m6.6_50.0km.csv.gz](resources/sa_PAS_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SBSM | [sa_SBSM_m6.6_50.0km.csv.gz](resources/sa_SBSM_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SMCA | [sa_SMCA_m6.6_50.0km.csv.gz](resources/sa_SMCA_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | STNI | [sa_STNI_m6.6_50.0km.csv.gz](resources/sa_STNI_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | USC | [sa_USC_m6.6_50.0km.csv.gz](resources/sa_USC_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | WNGC | [sa_WNGC_m6.6_50.0km.csv.gz](resources/sa_WNGC_m6.6_50.0km.csv.gz) |
| M6.6 | 100.0 km | PAS | [sa_PAS_m6.6_100.0km.csv.gz](resources/sa_PAS_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SBSM | [sa_SBSM_m6.6_100.0km.csv.gz](resources/sa_SBSM_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SMCA | [sa_SMCA_m6.6_100.0km.csv.gz](resources/sa_SMCA_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | STNI | [sa_STNI_m6.6_100.0km.csv.gz](resources/sa_STNI_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | USC | [sa_USC_m6.6_100.0km.csv.gz](resources/sa_USC_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | WNGC | [sa_WNGC_m6.6_100.0km.csv.gz](resources/sa_WNGC_m6.6_100.0km.csv.gz) |

