# rundir4860_multi_combine Rotated Rupture Variability, M6.6 Reverse

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M6.6, Reverse, Dip=45, Ztor=3). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

We then  perform various rotations. We rotate the rupture in place around its centroid, holding the site-to-source centroid path and Rrup constant (henceforth 'Rupture Strike'). We also rotate ruptures around the site, holding Rrup and source orientation relative to the site constant but sampling different various paths (henceforth 'Path'). We do this for each unique combination of Rupture Strike, Path, Distance, Site, and Rupture.

**Study Details**

| **Name** | RSQSim RotRup 4860 10X |
|-----|-----|
| **Date** | Mar 2019 |
| **Region** | Los Angeles Box |
| **Description** | RSQSim rotated-rupture variability study with catalog 4860 10X |
| **Velocity Model** | CVM-S4.26, 4.26 |

## Table Of Contents
* [Rupture Rotation Parameters](#rupture-rotation-parameters)
* [M6.6 Reverse Rupture Match Criteria](#m66-reverse-rupture-match-criteria)
  * [Fault Section Counts](#fault-section-counts)
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
* [Event Term Scatters](#event-term-scatters)
  * [Propagation Velocity Event Term Scatters](#propagation-velocity-event-term-scatters)
  * [Mag Event Term Scatters](#mag-event-term-scatters)
  * [Log10(Area) Event Term Scatters](#log10area-event-term-scatters)
  * [Max Slip Event Term Scatters](#max-slip-event-term-scatters)
  * [Mean Slip Event Term Scatters](#mean-slip-event-term-scatters)
  * [Slip Std Dev Event Term Scatters](#slip-std-dev-event-term-scatters)
  * [Mid-Seismogenic Mean Slip Event Term Scatters](#mid-seismogenic-mean-slip-event-term-scatters)
* [Directivity Comparisons](#directivity-comparisons)
* [Azumth Dependence](#azumth-dependence)
  * [LAF Azumth Dependence](#laf-azumth-dependence)
  * [OSI Azumth Dependence](#osi-azumth-dependence)
  * [PDE Azumth Dependence](#pde-azumth-dependence)
  * [SBSM Azumth Dependence](#sbsm-azumth-dependence)
  * [SMCA Azumth Dependence](#smca-azumth-dependence)
  * [STNI Azumth Dependence](#stni-azumth-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
  * [WNGC Azumth Dependence](#wngc-azumth-dependence)
  * [WSS Azumth Dependence](#wss-azumth-dependence)
  * [s022 Azumth Dependence](#s022-azumth-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M6.6, Reverse, Dip=45, Ztor=3](#bbp-partb-m66-reverse-dip45-ztor3)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 50 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 10 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 18 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **486000** | Total number of combinations of the above. |

## M6.6 Reverse Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 50 events which match the following criteria:

* M=[6.55,6.65]
* Ztor=[1.0,5.0]
* Rake=[80,100]
* Dip=[35.0,55.0]

In the case of more than 50 available matches, we use the Sect Variability filter method: Minimizes parent fault section duplication

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| Table Bluff | 10 |
| Fickle Hill (alt1) | 9 |
| Mad River (alt1) | 9 |
| McKinleyville (alt1) | 7 |
| Cucamonga | 5 |
| Big Lagoon - Bald Mtn 2011 CFM | 2 |
| Sierra Madre | 2 |
| Point Reyes 2011 connector | 2 |
| Point Reyes 2011 CFM | 2 |
| San Cayetano | 1 |
| North Frontal  (East) | 1 |
| San Luis Range - Oceano 2011 CFM | 1 |
| Trinidad (alt1) | 1 |
| Clamshell-Sawpit | 1 |
| SUM OF PARENT PARTICIPATIONS | 53 |
| # UNIQUE PARENTS | 14 |

Actual magnitude range: [6.5510902,6.6497498], average: 6.598717, stdDev: 0.027291495

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| LAF | *33.86889, -118.33143* | 500 | 0.71 | 3.42 |
| OSI | *34.6145, -118.7235* | 500 | 0.31 | 0.31 |
| PDE | *34.44199, -118.58215* | 500 | 0.15 | 1.84 |
| SBSM | *34.064987, -117.29201* | 500 | 0.33 | 1.82 |
| SMCA | *34.00909, -118.48939* | 500 | 0.59 | 2.45 |
| STNI | *33.93088, -118.17881* | 500 | 0.88 | 5.57 |
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |
| WNGC | *34.041824, -118.0653* | 500 | 0.5 | 3.49 |
| WSS | *34.1717, -118.64971* | 500 | 0.09 | 2.42 |
| s022 | *34.24505, -119.18086* | 500 | 0.51 | 4.24 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.25 | 0.32 | 0.27 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.31 | 0.37 | 0.33 | 0.2 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.35 | 0.42 | 0.36 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.31 | 0.37 | 0.32 | 0.2 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.45 | 0.41 | 0.49 | 0.42 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.47 | 0.43 | 0.52 | 0.43 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.48 | 0.44 | 0.51 | 0.47 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.47 | 0.43 | 0.51 | 0.44 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.47 | 0.46 | 0.51 | 0.43 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.51 | 0.51 | 0.56 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.55 | 0.56 | 0.58 | 0.5 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.51 | 0.51 | 0.55 | 0.46 |
| Within-event | &phi; | 20 km | 0.58 | 0.52 | 0.61 | 0.57 |
| Within-event | &phi; | 50 km | 0.64 | 0.59 | 0.68 | 0.61 |
| Within-event | &phi; | 100 km | 0.68 | 0.64 | 0.72 | 0.64 |
| Within-event | &phi; | (all) | 0.64 | 0.59 | 0.67 | 0.61 |
| Between-events | &tau; | 20 km | 0.21 | 0.18 | 0.22 | 0.22 |
| Between-events | &tau; | 50 km | 0.21 | 0.18 | 0.22 | 0.23 |
| Between-events | &tau; | 100 km | 0.21 | 0.16 | 0.21 | 0.25 |
| Between-events | &tau; | (all) | 0.21 | 0.17 | 0.22 | 0.23 |

### GMPE Table
*[(top)](#table-of-contents)*

| Type | Notation | Distance | ASK2014 3s | ASK2014 5s | ASK2014 10s |
|-----|-----|-----|-----|-----|-----|
| Source-strike | &phi;<sub>SS</sub> | 20 km | 0.57 | 0.55 | 0.55 |
| Source-strike | &phi;<sub>SS</sub> | 50 km | 0.57 | 0.55 | 0.55 |
| Source-strike | &phi;<sub>SS</sub> | 100 km | 0.57 | 0.55 | 0.55 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.57 | 0.55 | 0.55 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.57 | 0.55 | 0.55 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.57 | 0.55 | 0.55 |
| Within-event | &phi; | 20 km | 0.64 | 0.63 | 0.63 |
| Within-event | &phi; | 50 km | 0.64 | 0.63 | 0.63 |
| Within-event | &phi; | 100 km | 0.64 | 0.63 | 0.63 |
| Between-events | &tau; | 20 km | 0.38 | 0.38 | 0.38 |
| Between-events | &tau; | 50 km | 0.38 | 0.38 | 0.38 |
| Between-events | &tau; | 100 km | 0.38 | 0.38 | 0.38 |

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

* Site *[10 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*
* Rupture Strike *[18 unique]*

we compute residuals of the natural-log ground motions (relative to the median), computed across all 18 combinations of:

* Path *[18 unique]*

We take &phi;<sub>P2P</sub> to be the standard deviation of all residuals across each combination of Rupture, Rupture Strike. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

We also compute distance-independent &phi;<sub>P2P</sub>, which is computed as the standard deviation of all residuals across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.3** | **0.29** | **[0.08 0.83]** |  | **0.27** | **0.25** | **0.25** | **[0.05 0.72]** |  | **0.15** | **0.14** | **0.13** | **[0.02 0.56]** |
| LAF |  | 0.32 | 0.31 | 0.31 | [0.11 0.67] |  | 0.29 | 0.28 | 0.27 | [0.07 0.66] |  | 0.15 | 0.15 | 0.14 | [0.05 0.51] |
| OSI |  | 0.26 | 0.25 | 0.23 | [0.08 0.55] |  | 0.18 | 0.18 | 0.18 | [0.05 0.42] |  | 0.12 | 0.11 | 0.11 | [0.04 0.37] |
| PDE |  | 0.29 | 0.29 | 0.28 | [0.11 0.49] |  | 0.23 | 0.22 | 0.21 | [0.07 0.56] |  | 0.16 | 0.15 | 0.14 | [0.04 0.44] |
| SBSM |  | 0.27 | 0.25 | 0.24 | [0.08 0.66] |  | 0.19 | 0.18 | 0.17 | [0.05 0.46] |  | 0.13 | 0.12 | 0.11 | [0.02 0.32] |
| SMCA |  | 0.3 | 0.3 | 0.29 | [0.14 0.52] |  | 0.31 | 0.31 | 0.3 | [0.11 0.72] |  | 0.2 | 0.19 | 0.19 | [0.06 0.56] |
| STNI |  | 0.27 | 0.26 | 0.25 | [0.1 0.49] |  | 0.26 | 0.25 | 0.25 | [0.06 0.63] |  | 0.12 | 0.12 | 0.11 | [0.04 0.39] |
| USC |  | 0.32 | 0.32 | 0.31 | [0.1 0.53] |  | 0.31 | 0.3 | 0.29 | [0.1 0.59] |  | 0.16 | 0.16 | 0.15 | [0.04 0.48] |
| WNGC |  | 0.47 | 0.47 | 0.47 | [0.16 0.83] |  | 0.32 | 0.31 | 0.31 | [0.08 0.55] |  | 0.14 | 0.13 | 0.12 | [0.04 0.46] |
| WSS |  | 0.33 | 0.33 | 0.33 | [0.13 0.56] |  | 0.27 | 0.26 | 0.26 | [0.07 0.67] |  | 0.13 | 0.12 | 0.12 | [0.04 0.33] |
| s022 |  | 0.26 | 0.26 | 0.25 | [0.11 0.51] |  | 0.25 | 0.24 | 0.24 | [0.09 0.49] |  | 0.18 | 0.18 | 0.17 | [0.06 0.47] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_20km_3s_hist.png) | ![5s](resources/path_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 52 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 53 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.25 | 0.01 | [0.24 0.26] | [0.23 0.28] |
| 3 | 0.32 | 0.32 | 0.02 | [0.3 0.33] | [0.28 0.35] |
| 4 | 0.3 | 0.3 | 0.02 | [0.29 0.32] | [0.27 0.34] |
| 5 | 0.27 | 0.27 | 0.01 | [0.25 0.28] | [0.24 0.31] |
| 7.5 | 0.18 | 0.18 | 0.01 | [0.17 0.2] | [0.16 0.21] |
| 10 | 0.15 | 0.15 | 0.01 | [0.14 0.16] | [0.13 0.18] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_s022_downsampled_hist_3s.png) |  |  |


### 50.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.37** | **0.36** | **0.35** | **[0.16 0.8]** |  | **0.33** | **0.32** | **0.31** | **[0.14 0.77]** |  | **0.2** | **0.2** | **0.19** | **[0.05 0.52]** |
| LAF |  | 0.31 | 0.31 | 0.3 | [0.16 0.54] |  | 0.31 | 0.3 | 0.29 | [0.14 0.72] |  | 0.19 | 0.19 | 0.18 | [0.06 0.45] |
| OSI |  | 0.36 | 0.36 | 0.35 | [0.17 0.63] |  | 0.28 | 0.28 | 0.28 | [0.16 0.5] |  | 0.18 | 0.17 | 0.17 | [0.06 0.42] |
| PDE |  | 0.33 | 0.33 | 0.32 | [0.16 0.52] |  | 0.28 | 0.27 | 0.27 | [0.14 0.6] |  | 0.22 | 0.21 | 0.2 | [0.08 0.52] |
| SBSM |  | 0.46 | 0.45 | 0.46 | [0.2 0.77] |  | 0.3 | 0.3 | 0.3 | [0.14 0.49] |  | 0.17 | 0.16 | 0.15 | [0.05 0.35] |
| SMCA |  | 0.39 | 0.39 | 0.39 | [0.23 0.64] |  | 0.38 | 0.38 | 0.37 | [0.19 0.71] |  | 0.25 | 0.25 | 0.24 | [0.11 0.5] |
| STNI |  | 0.3 | 0.3 | 0.3 | [0.16 0.51] |  | 0.31 | 0.31 | 0.3 | [0.14 0.77] |  | 0.18 | 0.17 | 0.17 | [0.06 0.38] |
| USC |  | 0.33 | 0.33 | 0.33 | [0.16 0.52] |  | 0.36 | 0.36 | 0.35 | [0.17 0.72] |  | 0.22 | 0.21 | 0.21 | [0.07 0.47] |
| WNGC |  | 0.5 | 0.5 | 0.49 | [0.23 0.8] |  | 0.37 | 0.37 | 0.37 | [0.18 0.65] |  | 0.2 | 0.19 | 0.19 | [0.06 0.38] |
| WSS |  | 0.37 | 0.37 | 0.37 | [0.2 0.57] |  | 0.34 | 0.34 | 0.34 | [0.18 0.64] |  | 0.17 | 0.17 | 0.16 | [0.07 0.44] |
| s022 |  | 0.28 | 0.28 | 0.28 | [0.16 0.44] |  | 0.3 | 0.3 | 0.29 | [0.14 0.67] |  | 0.23 | 0.23 | 0.22 | [0.08 0.43] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_50km_3s_hist.png) | ![5s](resources/path_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 56 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 25 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.31 | 0.31 | 0.01 | [0.3 0.32] | [0.29 0.33] |
| 3 | 0.37 | 0.37 | 0.01 | [0.36 0.38] | [0.34 0.4] |
| 4 | 0.35 | 0.35 | 0.01 | [0.33 0.36] | [0.32 0.37] |
| 5 | 0.33 | 0.32 | 0.01 | [0.31 0.34] | [0.3 0.36] |
| 7.5 | 0.29 | 0.29 | 0.01 | [0.27 0.3] | [0.26 0.31] |
| 10 | 0.2 | 0.2 | 0.01 | [0.19 0.21] | [0.18 0.23] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_s022_downsampled_hist_3s.png) |  |  |


### 100.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.42** | **0.41** | **0.39** | **[0.14 0.9]** |  | **0.36** | **0.36** | **0.36** | **[0.16 0.68]** |  | **0.24** | **0.24** | **0.23** | **[0.07 0.49]** |
| LAF |  | 0.36 | 0.36 | 0.36 | [0.2 0.56] |  | 0.34 | 0.34 | 0.34 | [0.21 0.57] |  | 0.22 | 0.22 | 0.21 | [0.09 0.44] |
| OSI |  | 0.4 | 0.4 | 0.39 | [0.19 0.69] |  | 0.32 | 0.32 | 0.31 | [0.16 0.52] |  | 0.2 | 0.2 | 0.19 | [0.1 0.42] |
| PDE |  | 0.37 | 0.36 | 0.35 | [0.14 0.64] |  | 0.34 | 0.34 | 0.34 | [0.17 0.66] |  | 0.27 | 0.27 | 0.26 | [0.14 0.49] |
| SBSM |  | 0.55 | 0.55 | 0.55 | [0.29 0.83] |  | 0.4 | 0.4 | 0.4 | [0.18 0.64] |  | 0.21 | 0.2 | 0.2 | [0.07 0.42] |
| SMCA |  | 0.47 | 0.47 | 0.47 | [0.32 0.7] |  | 0.4 | 0.4 | 0.4 | [0.22 0.66] |  | 0.26 | 0.26 | 0.26 | [0.17 0.38] |
| STNI |  | 0.33 | 0.33 | 0.32 | [0.18 0.53] |  | 0.35 | 0.35 | 0.35 | [0.19 0.62] |  | 0.24 | 0.23 | 0.22 | [0.14 0.44] |
| USC |  | 0.41 | 0.41 | 0.41 | [0.25 0.62] |  | 0.39 | 0.39 | 0.39 | [0.2 0.65] |  | 0.31 | 0.31 | 0.31 | [0.18 0.47] |
| WNGC |  | 0.55 | 0.55 | 0.55 | [0.22 0.9] |  | 0.41 | 0.4 | 0.41 | [0.17 0.68] |  | 0.22 | 0.22 | 0.22 | [0.14 0.45] |
| WSS |  | 0.34 | 0.34 | 0.34 | [0.18 0.54] |  | 0.35 | 0.35 | 0.34 | [0.16 0.55] |  | 0.19 | 0.19 | 0.19 | [0.09 0.38] |
| s022 |  | 0.34 | 0.34 | 0.34 | [0.16 0.56] |  | 0.34 | 0.34 | 0.33 | [0.19 0.67] |  | 0.25 | 0.25 | 0.25 | [0.16 0.45] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_100km_3s_hist.png) | ![5s](resources/path_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 47 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 98 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.35 | 0.35 | 0.01 | [0.34 0.36] | [0.33 0.37] |
| 3 | 0.42 | 0.42 | 0.02 | [0.4 0.44] | [0.39 0.45] |
| 4 | 0.39 | 0.39 | 0.01 | [0.38 0.4] | [0.36 0.42] |
| 5 | 0.36 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.39] |
| 7.5 | 0.3 | 0.3 | 0.01 | [0.29 0.32] | [0.28 0.33] |
| 10 | 0.24 | 0.24 | 0.01 | [0.23 0.25] | [0.22 0.26] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_s022_downsampled_hist_3s.png) |  |  |


### All Distances M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.37** | **0.36** | **0.34** | **[0.08 0.9]** |  | **0.32** | **0.31** | **0.31** | **[0.05 0.77]** |  | **0.2** | **0.19** | **0.19** | **[0.02 0.56]** |
| LAF |  | 0.33 | 0.33 | 0.33 | [0.11 0.67] |  | 0.31 | 0.31 | 0.31 | [0.07 0.72] |  | 0.19 | 0.18 | 0.18 | [0.05 0.51] |
| OSI |  | 0.35 | 0.34 | 0.33 | [0.08 0.69] |  | 0.27 | 0.26 | 0.26 | [0.05 0.52] |  | 0.17 | 0.16 | 0.16 | [0.04 0.42] |
| PDE |  | 0.33 | 0.32 | 0.32 | [0.11 0.64] |  | 0.29 | 0.28 | 0.27 | [0.07 0.66] |  | 0.22 | 0.21 | 0.21 | [0.04 0.52] |
| SBSM |  | 0.44 | 0.42 | 0.43 | [0.08 0.83] |  | 0.31 | 0.29 | 0.3 | [0.05 0.64] |  | 0.17 | 0.16 | 0.16 | [0.02 0.42] |
| SMCA |  | 0.39 | 0.39 | 0.39 | [0.14 0.7] |  | 0.37 | 0.36 | 0.36 | [0.11 0.72] |  | 0.24 | 0.23 | 0.23 | [0.06 0.56] |
| STNI |  | 0.3 | 0.3 | 0.3 | [0.1 0.53] |  | 0.31 | 0.31 | 0.3 | [0.06 0.77] |  | 0.19 | 0.18 | 0.17 | [0.04 0.44] |
| USC |  | 0.36 | 0.35 | 0.35 | [0.1 0.62] |  | 0.35 | 0.35 | 0.35 | [0.1 0.72] |  | 0.24 | 0.23 | 0.22 | [0.04 0.48] |
| WNGC |  | 0.51 | 0.5 | 0.5 | [0.16 0.9] |  | 0.37 | 0.36 | 0.36 | [0.08 0.68] |  | 0.19 | 0.18 | 0.18 | [0.04 0.46] |
| WSS |  | 0.35 | 0.35 | 0.35 | [0.13 0.57] |  | 0.32 | 0.32 | 0.32 | [0.07 0.67] |  | 0.17 | 0.16 | 0.16 | [0.04 0.44] |
| s022 |  | 0.3 | 0.29 | 0.29 | [0.11 0.56] |  | 0.3 | 0.29 | 0.29 | [0.09 0.67] |  | 0.22 | 0.22 | 0.22 | [0.06 0.47] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_3s_hist.png) | ![5s](resources/path_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 288 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 1059 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.31 | 0.31 | 0 | [0.3 0.31] | [0.3 0.32] |
| 3 | 0.37 | 0.37 | 0.01 | [0.36 0.38] | [0.36 0.38] |
| 4 | 0.35 | 0.35 | 0.01 | [0.34 0.35] | [0.34 0.36] |
| 5 | 0.32 | 0.32 | 0.01 | [0.31 0.33] | [0.31 0.33] |
| 7.5 | 0.26 | 0.26 | 0.01 | [0.26 0.27] | [0.25 0.28] |
| 10 | 0.2 | 0.2 | 0 | [0.2 0.2] | [0.19 0.21] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_s022_downsampled_hist_3s.png) |  |  |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[10 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*
* Path *[18 unique]*

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
| **ALL SITES** |  | **0.41** | **0.39** | **0.39** | **[0.1 0.86]** |  | **0.49** | **0.47** | **0.45** | **[0.12 1.16]** |  | **0.42** | **0.4** | **0.38** | **[0.07 0.92]** |
| LAF |  | 0.41 | 0.39 | 0.38 | [0.1 0.77] |  | 0.51 | 0.49 | 0.49 | [0.18 1.07] |  | 0.43 | 0.41 | 0.39 | [0.07 0.87] |
| OSI |  | 0.4 | 0.39 | 0.39 | [0.16 0.68] |  | 0.45 | 0.43 | 0.42 | [0.18 0.83] |  | 0.4 | 0.39 | 0.37 | [0.12 0.75] |
| PDE |  | 0.4 | 0.38 | 0.37 | [0.12 0.83] |  | 0.49 | 0.47 | 0.46 | [0.18 0.98] |  | 0.42 | 0.39 | 0.37 | [0.11 0.79] |
| SBSM |  | 0.46 | 0.45 | 0.45 | [0.17 0.82] |  | 0.5 | 0.48 | 0.46 | [0.19 0.94] |  | 0.41 | 0.4 | 0.38 | [0.19 0.76] |
| SMCA |  | 0.43 | 0.42 | 0.41 | [0.16 0.77] |  | 0.51 | 0.49 | 0.47 | [0.12 1.16] |  | 0.44 | 0.41 | 0.4 | [0.12 0.89] |
| STNI |  | 0.4 | 0.38 | 0.37 | [0.16 0.78] |  | 0.45 | 0.43 | 0.41 | [0.17 1.05] |  | 0.42 | 0.4 | 0.37 | [0.09 0.92] |
| USC |  | 0.41 | 0.39 | 0.38 | [0.12 0.81] |  | 0.48 | 0.46 | 0.44 | [0.14 1.08] |  | 0.42 | 0.4 | 0.38 | [0.11 0.85] |
| WNGC |  | 0.44 | 0.42 | 0.41 | [0.11 0.86] |  | 0.51 | 0.49 | 0.48 | [0.21 1.01] |  | 0.42 | 0.4 | 0.39 | [0.13 0.86] |
| WSS |  | 0.39 | 0.38 | 0.37 | [0.1 0.73] |  | 0.49 | 0.47 | 0.46 | [0.18 0.97] |  | 0.42 | 0.4 | 0.39 | [0.14 0.88] |
| s022 |  | 0.35 | 0.33 | 0.32 | [0.11 0.66] |  | 0.46 | 0.43 | 0.42 | [0.12 1.05] |  | 0.42 | 0.39 | 0.37 | [0.1 0.92] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_20km_3s_hist.png) | ![5s](resources/source_strike_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 52 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 53 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.45 | 0.44 | 0.02 | [0.42 0.47] | [0.4 0.49] |
| 3 | 0.41 | 0.41 | 0.02 | [0.38 0.42] | [0.36 0.45] |
| 4 | 0.45 | 0.44 | 0.03 | [0.42 0.47] | [0.39 0.49] |
| 5 | 0.49 | 0.49 | 0.03 | [0.45 0.51] | [0.43 0.54] |
| 7.5 | 0.47 | 0.47 | 0.03 | [0.43 0.49] | [0.42 0.53] |
| 10 | 0.42 | 0.42 | 0.03 | [0.39 0.45] | [0.36 0.47] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_s022_downsampled_hist_3s.png) |  |  |


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.43** | **0.41** | **0.4** | **[0.1 0.88]** |  | **0.52** | **0.49** | **0.48** | **[0.11 1.17]** |  | **0.43** | **0.42** | **0.4** | **[0.11 0.97]** |
| LAF |  | 0.42 | 0.4 | 0.39 | [0.13 0.77] |  | 0.52 | 0.49 | 0.47 | [0.13 1.09] |  | 0.44 | 0.43 | 0.41 | [0.16 0.89] |
| OSI |  | 0.42 | 0.4 | 0.38 | [0.14 0.8] |  | 0.49 | 0.47 | 0.45 | [0.16 0.97] |  | 0.4 | 0.39 | 0.38 | [0.16 0.74] |
| PDE |  | 0.45 | 0.43 | 0.42 | [0.14 0.88] |  | 0.54 | 0.52 | 0.5 | [0.18 1.06] |  | 0.44 | 0.43 | 0.41 | [0.19 0.97] |
| SBSM |  | 0.51 | 0.5 | 0.49 | [0.17 0.85] |  | 0.56 | 0.54 | 0.53 | [0.19 1.02] |  | 0.43 | 0.42 | 0.41 | [0.18 0.8] |
| SMCA |  | 0.43 | 0.41 | 0.39 | [0.16 0.81] |  | 0.52 | 0.5 | 0.49 | [0.11 1.1] |  | 0.44 | 0.42 | 0.41 | [0.17 0.89] |
| STNI |  | 0.4 | 0.38 | 0.37 | [0.14 0.76] |  | 0.5 | 0.48 | 0.47 | [0.18 1.02] |  | 0.45 | 0.43 | 0.41 | [0.13 0.86] |
| USC |  | 0.42 | 0.4 | 0.39 | [0.12 0.84] |  | 0.5 | 0.48 | 0.46 | [0.16 1.06] |  | 0.44 | 0.42 | 0.4 | [0.13 0.88] |
| WNGC |  | 0.41 | 0.39 | 0.38 | [0.1 0.74] |  | 0.52 | 0.49 | 0.48 | [0.15 0.98] |  | 0.43 | 0.41 | 0.4 | [0.13 0.9] |
| WSS |  | 0.42 | 0.4 | 0.38 | [0.13 0.79] |  | 0.51 | 0.48 | 0.46 | [0.16 1.17] |  | 0.41 | 0.39 | 0.38 | [0.11 0.86] |
| s022 |  | 0.4 | 0.39 | 0.37 | [0.12 0.74] |  | 0.51 | 0.48 | 0.46 | [0.14 1.13] |  | 0.43 | 0.41 | 0.39 | [0.12 0.94] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_50km_3s_hist.png) | ![5s](resources/source_strike_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 56 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 25 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.46 | 0.02 | [0.45 0.49] | [0.43 0.52] |
| 3 | 0.43 | 0.42 | 0.02 | [0.4 0.45] | [0.38 0.48] |
| 4 | 0.47 | 0.47 | 0.03 | [0.44 0.5] | [0.41 0.54] |
| 5 | 0.52 | 0.51 | 0.03 | [0.48 0.55] | [0.46 0.58] |
| 7.5 | 0.49 | 0.48 | 0.03 | [0.46 0.51] | [0.44 0.56] |
| 10 | 0.43 | 0.43 | 0.02 | [0.4 0.45] | [0.38 0.48] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_s022_downsampled_hist_3s.png) |  |  |


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.44** | **0.42** | **0.4** | **[0.09 0.99]** |  | **0.51** | **0.49** | **0.48** | **[0.08 1.18]** |  | **0.47** | **0.45** | **0.43** | **[0.07 0.99]** |
| LAF |  | 0.44 | 0.42 | 0.41 | [0.12 0.85] |  | 0.53 | 0.51 | 0.5 | [0.16 1.1] |  | 0.48 | 0.46 | 0.44 | [0.17 0.91] |
| OSI |  | 0.43 | 0.41 | 0.4 | [0.1 0.85] |  | 0.48 | 0.46 | 0.45 | [0.08 0.98] |  | 0.46 | 0.44 | 0.43 | [0.16 0.84] |
| PDE |  | 0.43 | 0.41 | 0.4 | [0.12 0.89] |  | 0.52 | 0.49 | 0.48 | [0.13 1.06] |  | 0.46 | 0.44 | 0.42 | [0.12 0.91] |
| SBSM |  | 0.5 | 0.47 | 0.47 | [0.09 0.99] |  | 0.52 | 0.5 | 0.5 | [0.15 0.97] |  | 0.45 | 0.44 | 0.43 | [0.15 0.88] |
| SMCA |  | 0.42 | 0.4 | 0.39 | [0.15 0.82] |  | 0.5 | 0.48 | 0.46 | [0.1 1.08] |  | 0.47 | 0.45 | 0.43 | [0.14 0.92] |
| STNI |  | 0.42 | 0.4 | 0.39 | [0.12 0.83] |  | 0.53 | 0.5 | 0.5 | [0.13 1.08] |  | 0.49 | 0.48 | 0.46 | [0.18 0.92] |
| USC |  | 0.44 | 0.41 | 0.4 | [0.11 0.85] |  | 0.52 | 0.49 | 0.48 | [0.09 1.03] |  | 0.47 | 0.45 | 0.43 | [0.16 0.9] |
| WNGC |  | 0.45 | 0.43 | 0.42 | [0.12 0.96] |  | 0.53 | 0.51 | 0.5 | [0.13 1.18] |  | 0.47 | 0.46 | 0.43 | [0.15 0.93] |
| WSS |  | 0.43 | 0.41 | 0.4 | [0.1 0.73] |  | 0.5 | 0.47 | 0.46 | [0.1 1.05] |  | 0.46 | 0.44 | 0.42 | [0.07 0.97] |
| s022 |  | 0.42 | 0.4 | 0.39 | [0.14 0.8] |  | 0.51 | 0.49 | 0.48 | [0.17 1.07] |  | 0.49 | 0.47 | 0.45 | [0.13 0.99] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_100km_3s_hist.png) | ![5s](resources/source_strike_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 47 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 98 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.48 | 0.48 | 0.03 | [0.45 0.51] | [0.43 0.54] |
| 3 | 0.44 | 0.43 | 0.02 | [0.41 0.46] | [0.39 0.49] |
| 4 | 0.48 | 0.48 | 0.03 | [0.45 0.51] | [0.43 0.54] |
| 5 | 0.51 | 0.51 | 0.03 | [0.48 0.54] | [0.46 0.59] |
| 7.5 | 0.5 | 0.5 | 0.03 | [0.46 0.53] | [0.44 0.58] |
| 10 | 0.47 | 0.47 | 0.03 | [0.43 0.5] | [0.41 0.53] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_s022_downsampled_hist_3s.png) |  |  |


### All Distances M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.43** | **0.41** | **0.4** | **[0.09 0.99]** |  | **0.51** | **0.48** | **0.47** | **[0.08 1.18]** |  | **0.44** | **0.42** | **0.4** | **[0.07 0.99]** |
| LAF |  | 0.42 | 0.4 | 0.39 | [0.1 0.85] |  | 0.52 | 0.5 | 0.49 | [0.13 1.1] |  | 0.45 | 0.43 | 0.41 | [0.07 0.91] |
| OSI |  | 0.42 | 0.4 | 0.39 | [0.1 0.85] |  | 0.48 | 0.45 | 0.44 | [0.08 0.98] |  | 0.42 | 0.41 | 0.39 | [0.12 0.84] |
| PDE |  | 0.43 | 0.41 | 0.4 | [0.12 0.89] |  | 0.52 | 0.49 | 0.48 | [0.13 1.06] |  | 0.44 | 0.42 | 0.4 | [0.11 0.97] |
| SBSM |  | 0.49 | 0.47 | 0.47 | [0.09 0.99] |  | 0.53 | 0.51 | 0.49 | [0.15 1.02] |  | 0.43 | 0.42 | 0.4 | [0.15 0.88] |
| SMCA |  | 0.43 | 0.41 | 0.4 | [0.15 0.82] |  | 0.51 | 0.49 | 0.47 | [0.1 1.16] |  | 0.45 | 0.43 | 0.41 | [0.12 0.92] |
| STNI |  | 0.41 | 0.39 | 0.38 | [0.12 0.83] |  | 0.49 | 0.47 | 0.46 | [0.13 1.08] |  | 0.46 | 0.44 | 0.41 | [0.09 0.92] |
| USC |  | 0.42 | 0.4 | 0.39 | [0.11 0.85] |  | 0.5 | 0.48 | 0.46 | [0.09 1.08] |  | 0.44 | 0.42 | 0.4 | [0.11 0.9] |
| WNGC |  | 0.44 | 0.41 | 0.41 | [0.1 0.96] |  | 0.52 | 0.5 | 0.48 | [0.13 1.18] |  | 0.44 | 0.42 | 0.4 | [0.13 0.93] |
| WSS |  | 0.41 | 0.39 | 0.38 | [0.1 0.79] |  | 0.5 | 0.48 | 0.46 | [0.1 1.17] |  | 0.43 | 0.41 | 0.39 | [0.07 0.97] |
| s022 |  | 0.39 | 0.37 | 0.36 | [0.11 0.8] |  | 0.49 | 0.47 | 0.45 | [0.12 1.13] |  | 0.45 | 0.42 | 0.4 | [0.1 0.99] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_3s_hist.png) | ![5s](resources/source_strike_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 288 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 1059 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.46 | 0.01 | [0.46 0.47] | [0.45 0.48] |
| 3 | 0.43 | 0.42 | 0.01 | [0.41 0.43] | [0.4 0.45] |
| 4 | 0.47 | 0.46 | 0.01 | [0.45 0.48] | [0.44 0.48] |
| 5 | 0.51 | 0.5 | 0.01 | [0.49 0.52] | [0.48 0.53] |
| 7.5 | 0.49 | 0.49 | 0.01 | [0.48 0.5] | [0.47 0.51] |
| 10 | 0.44 | 0.44 | 0.01 | [0.43 0.45] | [0.42 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_s022_downsampled_hist_3s.png) |  |  |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[10 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 324 combinations of:

* Rupture Strike *[18 unique]*
* Path *[18 unique]*

We take &phi;<sub>SS</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture. We also compute the total standard deviation across all residuals from all sites. This total value is reported as **ALL SITES** and in summary plots/tables.

We also compute distance-independent &phi;<sub>SS</sub>, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event_ss.png)


### 20.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.46** | **0.45** | **0.45** | **[0.24 0.78]** |  | **0.51** | **0.49** | **0.48** | **[0.28 0.91]** |  | **0.43** | **0.4** | **0.38** | **[0.16 0.79]** |
| LAF |  | 0.46 | 0.45 | 0.46 | [0.31 0.65] |  | 0.54 | 0.52 | 0.52 | [0.34 0.91] |  | 0.44 | 0.41 | 0.39 | [0.2 0.79] |
| OSI |  | 0.42 | 0.42 | 0.42 | [0.28 0.53] |  | 0.45 | 0.44 | 0.42 | [0.29 0.71] |  | 0.4 | 0.38 | 0.37 | [0.22 0.66] |
| PDE |  | 0.43 | 0.42 | 0.42 | [0.25 0.58] |  | 0.49 | 0.48 | 0.47 | [0.3 0.85] |  | 0.42 | 0.4 | 0.37 | [0.24 0.74] |
| SBSM |  | 0.49 | 0.48 | 0.49 | [0.32 0.65] |  | 0.51 | 0.49 | 0.46 | [0.31 0.77] |  | 0.42 | 0.4 | 0.37 | [0.25 0.65] |
| SMCA |  | 0.46 | 0.45 | 0.46 | [0.33 0.62] |  | 0.53 | 0.52 | 0.5 | [0.37 0.9] |  | 0.45 | 0.43 | 0.4 | [0.27 0.79] |
| STNI |  | 0.42 | 0.41 | 0.42 | [0.26 0.6] |  | 0.47 | 0.45 | 0.44 | [0.28 0.8] |  | 0.42 | 0.39 | 0.36 | [0.16 0.79] |
| USC |  | 0.46 | 0.45 | 0.46 | [0.31 0.63] |  | 0.51 | 0.5 | 0.48 | [0.31 0.84] |  | 0.42 | 0.4 | 0.37 | [0.21 0.77] |
| WNGC |  | 0.59 | 0.59 | 0.58 | [0.4 0.78] |  | 0.55 | 0.54 | 0.52 | [0.41 0.85] |  | 0.43 | 0.4 | 0.38 | [0.21 0.76] |
| WSS |  | 0.45 | 0.44 | 0.45 | [0.34 0.58] |  | 0.52 | 0.5 | 0.48 | [0.35 0.83] |  | 0.43 | 0.4 | 0.39 | [0.24 0.72] |
| s022 |  | 0.37 | 0.36 | 0.35 | [0.24 0.5] |  | 0.47 | 0.45 | 0.42 | [0.31 0.87] |  | 0.42 | 0.4 | 0.38 | [0.23 0.77] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.46 | 0.02 | [0.44 0.49] | [0.41 0.51] |
| 3 | 0.46 | 0.45 | 0.02 | [0.43 0.47] | [0.4 0.49] |
| 4 | 0.48 | 0.47 | 0.02 | [0.45 0.5] | [0.42 0.53] |
| 5 | 0.51 | 0.49 | 0.03 | [0.47 0.52] | [0.44 0.55] |
| 7.5 | 0.48 | 0.47 | 0.03 | [0.44 0.51] | [0.41 0.53] |
| 10 | 0.43 | 0.42 | 0.03 | [0.39 0.45] | [0.36 0.48] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_s022_downsampled_hist_3s.png) |  |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_20km.png)


### 50.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.51** | **0.5** | **0.49** | **[0.3 0.81]** |  | **0.56** | **0.54** | **0.54** | **[0.35 1]** |  | **0.45** | **0.43** | **0.41** | **[0.24 0.8]** |
| LAF |  | 0.46 | 0.45 | 0.45 | [0.32 0.67] |  | 0.55 | 0.53 | 0.53 | [0.36 0.95] |  | 0.45 | 0.43 | 0.41 | [0.28 0.8] |
| OSI |  | 0.49 | 0.49 | 0.49 | [0.33 0.67] |  | 0.52 | 0.51 | 0.5 | [0.36 0.78] |  | 0.41 | 0.4 | 0.38 | [0.26 0.64] |
| PDE |  | 0.5 | 0.49 | 0.49 | [0.35 0.68] |  | 0.56 | 0.54 | 0.53 | [0.38 0.89] |  | 0.46 | 0.45 | 0.43 | [0.29 0.78] |
| SBSM |  | 0.63 | 0.62 | 0.63 | [0.4 0.81] |  | 0.6 | 0.59 | 0.56 | [0.39 0.84] |  | 0.44 | 0.43 | 0.41 | [0.28 0.66] |
| SMCA |  | 0.52 | 0.51 | 0.51 | [0.37 0.71] |  | 0.58 | 0.57 | 0.55 | [0.38 0.98] |  | 0.47 | 0.45 | 0.43 | [0.3 0.79] |
| STNI |  | 0.45 | 0.44 | 0.43 | [0.3 0.64] |  | 0.54 | 0.53 | 0.51 | [0.37 0.94] |  | 0.45 | 0.44 | 0.4 | [0.26 0.79] |
| USC |  | 0.47 | 0.46 | 0.46 | [0.33 0.66] |  | 0.56 | 0.54 | 0.54 | [0.39 0.92] |  | 0.46 | 0.44 | 0.42 | [0.27 0.78] |
| WNGC |  | 0.59 | 0.59 | 0.59 | [0.42 0.73] |  | 0.57 | 0.56 | 0.54 | [0.42 0.87] |  | 0.44 | 0.42 | 0.4 | [0.28 0.75] |
| WSS |  | 0.5 | 0.49 | 0.49 | [0.37 0.69] |  | 0.56 | 0.54 | 0.52 | [0.39 0.92] |  | 0.41 | 0.39 | 0.37 | [0.24 0.73] |
| s022 |  | 0.44 | 0.43 | 0.43 | [0.3 0.65] |  | 0.54 | 0.52 | 0.51 | [0.35 1] |  | 0.45 | 0.44 | 0.41 | [0.27 0.78] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.51 | 0.02 | [0.48 0.53] | [0.47 0.55] |
| 3 | 0.51 | 0.5 | 0.02 | [0.48 0.52] | [0.45 0.54] |
| 4 | 0.53 | 0.52 | 0.02 | [0.5 0.54] | [0.48 0.57] |
| 5 | 0.56 | 0.55 | 0.03 | [0.52 0.59] | [0.51 0.6] |
| 7.5 | 0.52 | 0.51 | 0.03 | [0.49 0.54] | [0.48 0.58] |
| 10 | 0.45 | 0.44 | 0.03 | [0.41 0.47] | [0.39 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_s022_downsampled_hist_3s.png) |  |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_50km.png)


### 100.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.56** | **0.54** | **0.54** | **[0.33 0.86]** |  | **0.58** | **0.57** | **0.56** | **[0.35 0.99]** |  | **0.5** | **0.48** | **0.46** | **[0.28 0.86]** |
| LAF |  | 0.53 | 0.52 | 0.51 | [0.38 0.76] |  | 0.58 | 0.57 | 0.56 | [0.4 0.96] |  | 0.5 | 0.48 | 0.46 | [0.29 0.83] |
| OSI |  | 0.53 | 0.52 | 0.53 | [0.35 0.69] |  | 0.52 | 0.51 | 0.51 | [0.35 0.84] |  | 0.47 | 0.45 | 0.43 | [0.28 0.75] |
| PDE |  | 0.5 | 0.49 | 0.49 | [0.35 0.67] |  | 0.55 | 0.53 | 0.53 | [0.37 0.92] |  | 0.5 | 0.48 | 0.47 | [0.31 0.78] |
| SBSM |  | 0.68 | 0.68 | 0.68 | [0.47 0.84] |  | 0.61 | 0.6 | 0.6 | [0.46 0.81] |  | 0.48 | 0.46 | 0.45 | [0.32 0.73] |
| SMCA |  | 0.58 | 0.58 | 0.57 | [0.43 0.77] |  | 0.59 | 0.58 | 0.57 | [0.43 0.96] |  | 0.51 | 0.49 | 0.48 | [0.32 0.81] |
| STNI |  | 0.49 | 0.48 | 0.48 | [0.35 0.7] |  | 0.59 | 0.57 | 0.56 | [0.39 0.99] |  | 0.51 | 0.5 | 0.47 | [0.33 0.86] |
| USC |  | 0.55 | 0.55 | 0.54 | [0.42 0.77] |  | 0.6 | 0.59 | 0.57 | [0.44 0.95] |  | 0.53 | 0.52 | 0.5 | [0.34 0.83] |
| WNGC |  | 0.67 | 0.66 | 0.67 | [0.42 0.86] |  | 0.62 | 0.61 | 0.6 | [0.45 0.97] |  | 0.49 | 0.48 | 0.46 | [0.29 0.82] |
| WSS |  | 0.49 | 0.48 | 0.49 | [0.33 0.7] |  | 0.56 | 0.55 | 0.54 | [0.38 0.91] |  | 0.47 | 0.45 | 0.43 | [0.29 0.77] |
| s022 |  | 0.5 | 0.49 | 0.48 | [0.35 0.7] |  | 0.56 | 0.55 | 0.55 | [0.37 0.93] |  | 0.51 | 0.5 | 0.47 | [0.31 0.84] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.55 | 0.54 | 0.02 | [0.52 0.56] | [0.5 0.57] |
| 3 | 0.56 | 0.55 | 0.02 | [0.53 0.57] | [0.5 0.6] |
| 4 | 0.56 | 0.55 | 0.02 | [0.53 0.58] | [0.5 0.6] |
| 5 | 0.58 | 0.57 | 0.02 | [0.55 0.59] | [0.53 0.61] |
| 7.5 | 0.55 | 0.54 | 0.02 | [0.51 0.56] | [0.48 0.58] |
| 10 | 0.5 | 0.49 | 0.03 | [0.46 0.51] | [0.43 0.53] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_s022_downsampled_hist_3s.png) |  |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_100km.png)


### All Distances M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.51** | **0.5** | **0.49** | **[0.24 0.86]** |  | **0.55** | **0.53** | **0.52** | **[0.28 1]** |  | **0.46** | **0.44** | **0.42** | **[0.16 0.86]** |
| LAF |  | 0.48 | 0.47 | 0.47 | [0.31 0.76] |  | 0.56 | 0.54 | 0.53 | [0.34 0.96] |  | 0.46 | 0.44 | 0.42 | [0.2 0.83] |
| OSI |  | 0.48 | 0.47 | 0.47 | [0.28 0.69] |  | 0.5 | 0.48 | 0.47 | [0.29 0.84] |  | 0.43 | 0.41 | 0.39 | [0.22 0.75] |
| PDE |  | 0.47 | 0.46 | 0.46 | [0.25 0.68] |  | 0.54 | 0.52 | 0.51 | [0.3 0.92] |  | 0.46 | 0.44 | 0.43 | [0.24 0.78] |
| SBSM |  | 0.61 | 0.59 | 0.6 | [0.32 0.84] |  | 0.58 | 0.56 | 0.55 | [0.31 0.84] |  | 0.45 | 0.43 | 0.42 | [0.25 0.73] |
| SMCA |  | 0.52 | 0.51 | 0.52 | [0.33 0.77] |  | 0.57 | 0.56 | 0.55 | [0.37 0.98] |  | 0.48 | 0.46 | 0.45 | [0.27 0.81] |
| STNI |  | 0.45 | 0.44 | 0.44 | [0.26 0.7] |  | 0.53 | 0.52 | 0.5 | [0.28 0.99] |  | 0.46 | 0.44 | 0.43 | [0.16 0.86] |
| USC |  | 0.49 | 0.48 | 0.48 | [0.31 0.77] |  | 0.56 | 0.54 | 0.54 | [0.31 0.95] |  | 0.47 | 0.45 | 0.44 | [0.21 0.83] |
| WNGC |  | 0.62 | 0.61 | 0.6 | [0.4 0.86] |  | 0.58 | 0.57 | 0.56 | [0.41 0.97] |  | 0.45 | 0.43 | 0.42 | [0.21 0.82] |
| WSS |  | 0.48 | 0.47 | 0.47 | [0.33 0.7] |  | 0.54 | 0.53 | 0.51 | [0.35 0.92] |  | 0.44 | 0.42 | 0.4 | [0.24 0.77] |
| s022 |  | 0.44 | 0.43 | 0.42 | [0.24 0.7] |  | 0.53 | 0.51 | 0.49 | [0.31 1] |  | 0.46 | 0.44 | 0.42 | [0.23 0.84] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 2556 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.51 | 0.01 | [0.5 0.52] | [0.49 0.54] |
| 3 | 0.51 | 0.51 | 0.01 | [0.5 0.52] | [0.49 0.53] |
| 4 | 0.53 | 0.52 | 0.01 | [0.51 0.53] | [0.5 0.55] |
| 5 | 0.55 | 0.55 | 0.01 | [0.53 0.56] | [0.52 0.58] |
| 7.5 | 0.52 | 0.51 | 0.02 | [0.5 0.53] | [0.49 0.55] |
| 10 | 0.46 | 0.45 | 0.02 | [0.44 0.47] | [0.43 0.49] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_s022_downsampled_hist_3s.png) |  |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8].

![Histogram](resources/within_event_ss_event_recordings_hist_all_dists.png)


## Within-event Variability
*[(top)](#table-of-contents)*

### Within-event Variability Methodology
*[(top)](#table-of-contents)*

Within-event variability, denoted &phi; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 3240 combinations of:

* Site *[10 unique]* (Singleton)
* Rupture Strike *[18 unique]*
* Path *[18 unique]*

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
| **10 sites, V<sub>S30</sub>=500** |  | **0.52** | **0.53** | **0.52** | **[0.12 1.13]** |  | **0.61** | **0.61** | **0.6** | **[0.17 1.39]** |  | **0.57** | **0.57** | **0.56** | **[0.19 1.31]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 36 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 69 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.58 | 0.57 | 0.06 | [0.52 0.65] | [0.48 0.71] |
| 3 | 0.52 | 0.52 | 0.06 | [0.46 0.58] | [0.41 0.67] |
| 4 | 0.57 | 0.57 | 0.07 | [0.51 0.65] | [0.47 0.72] |
| 5 | 0.61 | 0.61 | 0.08 | [0.53 0.71] | [0.48 0.76] |
| 7.5 | 0.63 | 0.63 | 0.08 | [0.56 0.72] | [0.49 0.8] |
| 10 | 0.57 | 0.56 | 0.07 | [0.49 0.64] | [0.43 0.72] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_3s.png) |


### 50.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.59** | **0.59** | **0.58** | **[0.14 1.29]** |  | **0.68** | **0.68** | **0.67** | **[0.19 1.49]** |  | **0.61** | **0.62** | **0.61** | **[0.21 1.34]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 32 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 49 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.65 | 0.63 | 0.08 | [0.56 0.72] | [0.49 0.8] |
| 3 | 0.59 | 0.58 | 0.08 | [0.51 0.65] | [0.43 0.77] |
| 4 | 0.64 | 0.62 | 0.09 | [0.52 0.73] | [0.45 0.81] |
| 5 | 0.68 | 0.66 | 0.1 | [0.56 0.76] | [0.46 0.88] |
| 7.5 | 0.7 | 0.68 | 0.09 | [0.6 0.79] | [0.52 0.89] |
| 10 | 0.61 | 0.6 | 0.08 | [0.54 0.7] | [0.48 0.8] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_3s.png) |


### 100.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.64** | **0.64** | **0.63** | **[0.16 1.4]** |  | **0.72** | **0.72** | **0.71** | **[0.17 1.52]** |  | **0.64** | **0.64** | **0.63** | **[0.17 1.35]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 30 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 115 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.68 | 0.67 | 0.08 | [0.59 0.74] | [0.49 0.81] |
| 3 | 0.64 | 0.63 | 0.09 | [0.53 0.73] | [0.45 0.79] |
| 4 | 0.68 | 0.67 | 0.09 | [0.58 0.77] | [0.47 0.85] |
| 5 | 0.72 | 0.73 | 0.1 | [0.62 0.81] | [0.48 0.9] |
| 7.5 | 0.73 | 0.71 | 0.09 | [0.64 0.81] | [0.49 0.9] |
| 10 | 0.64 | 0.63 | 0.08 | [0.56 0.7] | [0.47 0.82] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_3s.png) |


### All Distances M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.59** | **0.59** | **0.57** | **[0.12 1.4]** |  | **0.67** | **0.67** | **0.66** | **[0.17 1.52]** |  | **0.61** | **0.61** | **0.59** | **[0.17 1.35]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_3s_hist.png) | ![5s](resources/within_event_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 168 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 1179 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.64 | 0.63 | 0.03 | [0.6 0.67] | [0.56 0.7] |
| 3 | 0.59 | 0.58 | 0.04 | [0.55 0.62] | [0.52 0.68] |
| 4 | 0.63 | 0.63 | 0.04 | [0.6 0.67] | [0.56 0.71] |
| 5 | 0.67 | 0.67 | 0.04 | [0.63 0.71] | [0.59 0.75] |
| 7.5 | 0.68 | 0.68 | 0.04 | [0.64 0.72] | [0.59 0.75] |
| 10 | 0.61 | 0.6 | 0.04 | [0.57 0.64] | [0.52 0.68] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_downsampled_hist_3s.png) |


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[50 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 3240 combinations of:

* Site *[10 unique]*
* Rupture Strike *[18 unique]*
* Path *[18 unique]*

We take &tau; to be the standard deviation of all &delta;B<sub>e</sub>. This is done separately for each set of sites with the same V<sub>S30</sub> value. Single-site values are also reported.

We also compute distance-independent &tau;, which we take to be the mean value across all distances.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_between_events.png)


### 20.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** | **0.18** | **-3.09** | **[-3.51 -2.7]** | **0.22** | **-3.77** | **[-4.33 -3.27]** | **0.22** | **-5.01** | **[-5.79 -4.62]** |
| LAF | 0.19 | -3.17 | [-3.63 -2.78] | 0.26 | -3.65 | [-4.28 -3.18] | 0.23 | -4.78 | [-5.64 -4.38] |
| OSI | 0.16 | -3.82 | [-4.15 -3.57] | 0.17 | -4.78 | [-5.18 -4.43] | 0.21 | -5.81 | [-6.55 -5.45] |
| PDE | 0.2 | -3.11 | [-3.54 -2.74] | 0.22 | -3.86 | [-4.46 -3.37] | 0.23 | -5.11 | [-5.9 -4.74] |
| SBSM | 0.25 | -2.81 | [-3.32 -2.32] | 0.22 | -3.87 | [-4.45 -3.49] | 0.18 | -5.43 | [-5.95 -5.06] |
| SMCA | 0.18 | -2.99 | [-3.41 -2.68] | 0.24 | -3.47 | [-4.08 -2.96] | 0.22 | -4.82 | [-5.58 -4.47] |
| STNI | 0.18 | -2.94 | [-3.36 -2.58] | 0.23 | -3.45 | [-4 -3.01] | 0.23 | -4.46 | [-5.41 -4.06] |
| USC | 0.2 | -3.04 | [-3.52 -2.64] | 0.24 | -3.67 | [-4.25 -3.16] | 0.22 | -4.85 | [-5.71 -4.45] |
| WNGC | 0.21 | -3.08 | [-3.52 -2.65] | 0.25 | -3.74 | [-4.32 -3.24] | 0.21 | -5 | [-5.78 -4.64] |
| WSS | 0.19 | -3.35 | [-3.83 -3.02] | 0.22 | -4 | [-4.59 -3.57] | 0.22 | -5.34 | [-6.11 -4.99] |
| s022 | 0.18 | -2.89 | [-3.33 -2.46] | 0.22 | -3.59 | [-4.18 -3.06] | 0.23 | -4.68 | [-5.58 -4.32] |

#### 20.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.25 | 0.09 | [0.19 0.36] | [0.13 0.48] |
| 3 | 0.18 | 0.21 | 0.1 | [0.12 0.33] | [0.06 0.45] |
| 4 | 0.21 | 0.26 | 0.11 | [0.15 0.37] | [0.07 0.49] |
| 5 | 0.22 | 0.28 | 0.11 | [0.17 0.4] | [0.08 0.54] |
| 7.5 | 0.24 | 0.3 | 0.12 | [0.17 0.41] | [0.08 0.57] |
| 10 | 0.22 | 0.25 | 0.12 | [0.15 0.38] | [0.08 0.57] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_20km.png)


### 50.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** | **0.18** | **-3.89** | **[-4.33 -3.53]** | **0.22** | **-4.39** | **[-4.94 -3.84]** | **0.23** | **-5.67** | **[-6.46 -5.25]** |
| LAF | 0.18 | -3.91 | [-4.36 -3.6] | 0.23 | -4.21 | [-4.77 -3.66] | 0.23 | -5.48 | [-6.29 -5.06] |
| OSI | 0.18 | -4.7 | [-5.12 -4.39] | 0.2 | -5.48 | [-5.96 -5.04] | 0.24 | -6.46 | [-7.26 -6.01] |
| PDE | 0.19 | -3.95 | [-4.4 -3.58] | 0.23 | -4.52 | [-5.08 -4.04] | 0.21 | -5.83 | [-6.58 -5.42] |
| SBSM | 0.26 | -3.53 | [-4.1 -3.03] | 0.24 | -4.47 | [-5.05 -3.99] | 0.17 | -6.08 | [-6.62 -5.72] |
| SMCA | 0.16 | -3.88 | [-4.29 -3.48] | 0.24 | -4.22 | [-4.84 -3.68] | 0.22 | -5.54 | [-6.35 -5.15] |
| STNI | 0.18 | -3.63 | [-4.02 -3.2] | 0.22 | -3.95 | [-4.47 -3.42] | 0.26 | -4.98 | [-5.9 -4.5] |
| USC | 0.19 | -3.83 | [-4.29 -3.45] | 0.23 | -4.28 | [-4.88 -3.72] | 0.23 | -5.49 | [-6.31 -5.07] |
| WNGC | 0.21 | -3.86 | [-4.38 -3.47] | 0.23 | -4.27 | [-4.91 -3.73] | 0.22 | -5.67 | [-6.45 -5.26] |
| WSS | 0.16 | -4.2 | [-4.55 -3.82] | 0.22 | -4.78 | [-5.34 -4.23] | 0.22 | -6.08 | [-6.8 -5.68] |
| s022 | 0.16 | -3.65 | [-4.06 -3.29] | 0.22 | -4.17 | [-4.76 -3.61] | 0.25 | -5.13 | [-6.08 -4.69] |

#### 50.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.28 | 0.1 | [0.21 0.4] | [0.14 0.55] |
| 3 | 0.18 | 0.26 | 0.12 | [0.15 0.41] | [0.08 0.53] |
| 4 | 0.21 | 0.28 | 0.13 | [0.18 0.42] | [0.08 0.62] |
| 5 | 0.22 | 0.3 | 0.14 | [0.18 0.45] | [0.09 0.66] |
| 7.5 | 0.22 | 0.31 | 0.13 | [0.16 0.43] | [0.1 0.64] |
| 10 | 0.23 | 0.26 | 0.13 | [0.15 0.43] | [0.07 0.54] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_50km.png)


### 100.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** | **0.16** | **-4.59** | **[-4.99 -4.28]** | **0.21** | **-5.02** | **[-5.51 -4.51]** | **0.25** | **-6.13** | **[-7.01 -5.67]** |
| LAF | 0.17 | -4.56 | [-4.97 -4.23] | 0.22 | -4.77 | [-5.25 -4.25] | 0.26 | -5.87 | [-6.79 -5.38] |
| OSI | 0.15 | -5.51 | [-5.84 -5.25] | 0.18 | -6.21 | [-6.66 -5.8] | 0.27 | -6.93 | [-7.91 -6.45] |
| PDE | 0.17 | -4.68 | [-5.11 -4.41] | 0.2 | -5.17 | [-5.67 -4.69] | 0.25 | -6.27 | [-7.15 -5.83] |
| SBSM | 0.26 | -4.24 | [-4.83 -3.7] | 0.21 | -5.14 | [-5.66 -4.68] | 0.21 | -6.56 | [-7.28 -6.17] |
| SMCA | 0.15 | -4.54 | [-4.92 -4.22] | 0.2 | -4.83 | [-5.29 -4.31] | 0.26 | -5.99 | [-6.9 -5.53] |
| STNI | 0.16 | -4.35 | [-4.75 -4.04] | 0.22 | -4.56 | [-5.08 -4.02] | 0.27 | -5.48 | [-6.46 -5.02] |
| USC | 0.17 | -4.52 | [-4.96 -4.14] | 0.22 | -4.85 | [-5.37 -4.26] | 0.26 | -5.95 | [-6.85 -5.47] |
| WNGC | 0.17 | -4.5 | [-4.94 -4.15] | 0.21 | -4.94 | [-5.44 -4.45] | 0.26 | -6.07 | [-6.96 -5.62] |
| WSS | 0.16 | -4.86 | [-5.21 -4.63] | 0.21 | -5.42 | [-5.9 -4.93] | 0.26 | -6.53 | [-7.42 -6.09] |
| s022 | 0.16 | -4.32 | [-4.68 -4.02] | 0.2 | -4.8 | [-5.26 -4.37] | 0.25 | -5.71 | [-6.66 -5.25] |

#### 100.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.22 | 0.09 | [0.15 0.31] | [0.11 0.47] |
| 3 | 0.16 | 0.17 | 0.1 | [0.09 0.32] | [0.04 0.39] |
| 4 | 0.19 | 0.2 | 0.11 | [0.11 0.3] | [0.04 0.49] |
| 5 | 0.21 | 0.21 | 0.11 | [0.12 0.36] | [0.06 0.47] |
| 7.5 | 0.23 | 0.24 | 0.14 | [0.14 0.39] | [0.06 0.64] |
| 10 | 0.25 | 0.24 | 0.16 | [0.14 0.42] | [0.07 0.71] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_100km.png)


### All Distances M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** | **0.17** | **-3.86** | **[-4.99 -2.7]** | **0.22** | **-4.39** | **[-5.51 -3.27]** | **0.23** | **-5.6** | **[-7.01 -4.62]** |
| LAF | 0.18 | -3.88 | [-4.97 -2.78] | 0.23 | -4.21 | [-5.25 -3.18] | 0.24 | -5.38 | [-6.79 -4.38] |
| OSI | 0.16 | -4.68 | [-5.84 -3.57] | 0.18 | -5.49 | [-6.66 -4.43] | 0.24 | -6.4 | [-7.91 -5.45] |
| PDE | 0.19 | -3.91 | [-5.11 -2.74] | 0.22 | -4.52 | [-5.67 -3.37] | 0.23 | -5.74 | [-7.15 -4.74] |
| SBSM | 0.26 | -3.53 | [-4.83 -2.32] | 0.22 | -4.5 | [-5.66 -3.49] | 0.19 | -6.02 | [-7.28 -5.06] |
| SMCA | 0.16 | -3.8 | [-4.92 -2.68] | 0.23 | -4.17 | [-5.29 -2.96] | 0.23 | -5.45 | [-6.9 -4.47] |
| STNI | 0.17 | -3.64 | [-4.75 -2.58] | 0.22 | -3.99 | [-5.08 -3.01] | 0.25 | -4.97 | [-6.46 -4.06] |
| USC | 0.19 | -3.8 | [-4.96 -2.64] | 0.23 | -4.26 | [-5.37 -3.16] | 0.24 | -5.43 | [-6.85 -4.45] |
| WNGC | 0.2 | -3.81 | [-4.94 -2.65] | 0.23 | -4.31 | [-5.44 -3.24] | 0.23 | -5.58 | [-6.96 -4.64] |
| WSS | 0.17 | -4.14 | [-5.21 -3.02] | 0.22 | -4.73 | [-5.9 -3.57] | 0.23 | -5.98 | [-7.42 -4.99] |
| s022 | 0.17 | -3.62 | [-4.68 -2.46] | 0.21 | -4.19 | [-5.26 -3.06] | 0.24 | -5.17 | [-6.66 -4.32] |

#### All Distances M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 4041 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.27 | 0.03 | [0.23 0.3] | [0.2 0.33] |
| 3 | 0.17 | 0.23 | 0.04 | [0.19 0.27] | [0.15 0.32] |
| 4 | 0.2 | 0.25 | 0.04 | [0.21 0.3] | [0.17 0.36] |
| 5 | 0.22 | 0.27 | 0.05 | [0.22 0.33] | [0.18 0.38] |
| 7.5 | 0.23 | 0.29 | 0.05 | [0.23 0.34] | [0.2 0.37] |
| 10 | 0.23 | 0.28 | 0.05 | [0.22 0.33] | [0.18 0.39] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8].

![Histogram](resources/between_events_event_recordings_hist_all_dists.png)


## Event Term Scatters
*[(top)](#table-of-contents)*

### Propagation Velocity Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_10sites_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_10sites_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_10sites_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_10sites_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_10sites_10s.png) |
### Slip Std Dev Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_10sites_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_10sites_10s.png) |
## Directivity Comparisons
*[(top)](#table-of-contents)*

Directivity comparisons for individual ruptures can be found [here](resources/directivity_debug/README.md).

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/directivity_20km_3s.png) | ![plot](resources/directivity_20km_5s.png) | ![plot](resources/directivity_20km_10s.png) |
| **50 km** | ![plot](resources/directivity_50km_3s.png) | ![plot](resources/directivity_50km_5s.png) | ![plot](resources/directivity_50km_10s.png) |
| **100 km** | *N/A* | *N/A* | *N/A* |
## Azumth Dependence
*[(top)](#table-of-contents)*

### LAF Azumth Dependence
*[(top)](#table-of-contents)*

#### LAF Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### LAF Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### OSI Azumth Dependence
*[(top)](#table-of-contents)*

#### OSI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### OSI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### PDE Azumth Dependence
*[(top)](#table-of-contents)*

#### PDE Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PDE Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WSS Azumth Dependence
*[(top)](#table-of-contents)*

#### WSS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WSS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### s022 Azumth Dependence
*[(top)](#table-of-contents)*

#### s022 Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### s022 Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

## BBP PartB Comparison
*[(top)](#table-of-contents)*

Here we attempt to reproduce the SCEC BroadBand Platform "Part B" validation exercise as defined in:

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismicâ€�hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|-----|
| **M6.6 Reverse** | **LAF** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **OSI** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **PDE** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **SBSM** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **SMCA** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **STNI** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **USC** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **WNGC** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **WSS** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **s022** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 Reverse** | **10sites_Vs30_500** | **FAIL** | **FAIL** | *(FAIL)* |

### BBP PartB, M6.6, Reverse, Dip=45, Ztor=3
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **LAF** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_LAF.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_LAF.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_LAF.png) |
| **OSI** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_OSI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_OSI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_OSI.png) |
| **PDE** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_PDE.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_PDE.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_PDE.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_WNGC.png) |
| **WSS** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_WSS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_WSS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_WSS.png) |
| **s022** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_s022.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_s022.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_s022.png) |
| **10sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_10sites_Vs30_500.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M6.6 | 20.0 km | LAF | [sa_LAF_m6.6_20.0km.csv.gz](resources/sa_LAF_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | OSI | [sa_OSI_m6.6_20.0km.csv.gz](resources/sa_OSI_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | PDE | [sa_PDE_m6.6_20.0km.csv.gz](resources/sa_PDE_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SBSM | [sa_SBSM_m6.6_20.0km.csv.gz](resources/sa_SBSM_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SMCA | [sa_SMCA_m6.6_20.0km.csv.gz](resources/sa_SMCA_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | STNI | [sa_STNI_m6.6_20.0km.csv.gz](resources/sa_STNI_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | USC | [sa_USC_m6.6_20.0km.csv.gz](resources/sa_USC_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | WNGC | [sa_WNGC_m6.6_20.0km.csv.gz](resources/sa_WNGC_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | WSS | [sa_WSS_m6.6_20.0km.csv.gz](resources/sa_WSS_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | s022 | [sa_s022_m6.6_20.0km.csv.gz](resources/sa_s022_m6.6_20.0km.csv.gz) |
| M6.6 | 50.0 km | LAF | [sa_LAF_m6.6_50.0km.csv.gz](resources/sa_LAF_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | OSI | [sa_OSI_m6.6_50.0km.csv.gz](resources/sa_OSI_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | PDE | [sa_PDE_m6.6_50.0km.csv.gz](resources/sa_PDE_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SBSM | [sa_SBSM_m6.6_50.0km.csv.gz](resources/sa_SBSM_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SMCA | [sa_SMCA_m6.6_50.0km.csv.gz](resources/sa_SMCA_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | STNI | [sa_STNI_m6.6_50.0km.csv.gz](resources/sa_STNI_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | USC | [sa_USC_m6.6_50.0km.csv.gz](resources/sa_USC_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | WNGC | [sa_WNGC_m6.6_50.0km.csv.gz](resources/sa_WNGC_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | WSS | [sa_WSS_m6.6_50.0km.csv.gz](resources/sa_WSS_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | s022 | [sa_s022_m6.6_50.0km.csv.gz](resources/sa_s022_m6.6_50.0km.csv.gz) |
| M6.6 | 100.0 km | LAF | [sa_LAF_m6.6_100.0km.csv.gz](resources/sa_LAF_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | OSI | [sa_OSI_m6.6_100.0km.csv.gz](resources/sa_OSI_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | PDE | [sa_PDE_m6.6_100.0km.csv.gz](resources/sa_PDE_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SBSM | [sa_SBSM_m6.6_100.0km.csv.gz](resources/sa_SBSM_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SMCA | [sa_SMCA_m6.6_100.0km.csv.gz](resources/sa_SMCA_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | STNI | [sa_STNI_m6.6_100.0km.csv.gz](resources/sa_STNI_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | USC | [sa_USC_m6.6_100.0km.csv.gz](resources/sa_USC_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | WNGC | [sa_WNGC_m6.6_100.0km.csv.gz](resources/sa_WNGC_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | WSS | [sa_WSS_m6.6_100.0km.csv.gz](resources/sa_WSS_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | s022 | [sa_s022_m6.6_100.0km.csv.gz](resources/sa_s022_m6.6_100.0km.csv.gz) |

