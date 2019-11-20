# rundir2585_1myr Rotated Rupture Variability, M6.6 SS

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M6.6, Vertical Strike-Slip with Surface Rupture). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

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
* [M6.6 SS RSQSim Rupture Match Criteria](#m66-ss-rsqsim-rupture-match-criteria)
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
  * [BBP PartB, M6.6, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m66-vertical-strike-slip-with-surface-rupture)
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

## M6.6 SS RSQSim Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 100 events in the catalog which match the following criteria:

* M=[6.55,6.65]
* Ztor=[0.0,1.0]
* Rake=[-180,-170] or [-10,10] or [170,180]
* Dip=90.0
* Linear rupture (max 0.5km deviation from ideal)

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| Cerro Prieto | 25 |
| San Andreas (Coachella) rev | 23 |
| Garlock (Central) | 8 |
| Mendocino | 4 |
| Hunting Creek - Berryessa 2011 CFM | 4 |
| San Andreas (San Bernardino N) | 4 |
| Hunting Creek - Bartlett Springs connector 2011 | 3 |
| Palos Verdes | 3 |
| Death Valley (So) | 3 |
| San Andreas (Carrizo) rev | 3 |
| Honey Lake 2011 CFM | 2 |
| San Andreas (Creeping Section) 2011 CFM | 2 |
| San Jacinto (San Bernardino) | 2 |
| Earthquake Valley (So Extension) | 1 |
| Cleghorn Pass | 1 |
| San Jacinto (Superstition Mtn) | 1 |
| Owl Lake | 1 |
| San Andreas (San Bernardino S) | 1 |
| San Jacinto (Coyote Creek) | 1 |
| Elmore Ranch | 1 |
| Coronado Bank alt1 | 1 |
| San Diego Trough north alt1 | 1 |
| Earthquake Valley | 1 |
| Garlock (East) | 1 |
| Ortigalita (South) | 1 |
| Owens Valley | 1 |
| Lenwood-Lockhart-Old Woman Springs | 1 |
| Garlock (West) | 1 |

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
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.3 | 0.36 | 0.34 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.38 | 0.45 | 0.39 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.41 | 0.48 | 0.44 | 0.27 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.37 | 0.43 | 0.39 | 0.22 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.33 | 0.35 | 0.35 | 0.25 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.38 | 0.34 | 0.35 | 0.41 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.38 | 0.34 | 0.38 | 0.41 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.36 | 0.34 | 0.36 | 0.37 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.39 | 0.44 | 0.42 | 0.26 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.47 | 0.5 | 0.46 | 0.43 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.51 | 0.53 | 0.52 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.46 | 0.49 | 0.47 | 0.39 |
| Within-event | &phi; | 20 km | 0.61 | 0.65 | 0.62 | 0.53 |
| Within-event | &phi; | 50 km | 0.69 | 0.72 | 0.69 | 0.63 |
| Within-event | &phi; | 100 km | 0.71 | 0.73 | 0.73 | 0.64 |
| Within-event | &phi; | (all) | 0.67 | 0.7 | 0.68 | 0.6 |
| Between-events | &tau; | 20 km | 0.25 | 0.22 | 0.22 | 0.31 |
| Between-events | &tau; | 50 km | 0.25 | 0.21 | 0.25 | 0.29 |
| Between-events | &tau; | 100 km | 0.25 | 0.19 | 0.24 | 0.31 |
| Between-events | &tau; | (all) | 0.25 | 0.21 | 0.24 | 0.31 |

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
| **ALL SITES** |  | **0.36** | **0.34** | **0.31** | **[0.08 0.89]** |  | **0.34** | **0.32** | **0.31** | **[0.05 0.83]** |  | **0.15** | **0.14** | **0.13** | **[0.03 0.53]** |
| PAS |  | 0.34 | 0.33 | 0.32 | [0.11 0.68] |  | 0.3 | 0.29 | 0.29 | [0.07 0.54] |  | 0.13 | 0.12 | 0.12 | [0.03 0.4] |
| SBSM |  | 0.26 | 0.25 | 0.24 | [0.08 0.57] |  | 0.2 | 0.18 | 0.17 | [0.05 0.48] |  | 0.11 | 0.11 | 0.1 | [0.03 0.33] |
| SMCA |  | 0.34 | 0.33 | 0.33 | [0.14 0.65] |  | 0.35 | 0.34 | 0.33 | [0.11 0.61] |  | 0.16 | 0.15 | 0.15 | [0.04 0.4] |
| STNI |  | 0.27 | 0.27 | 0.27 | [0.11 0.48] |  | 0.29 | 0.28 | 0.27 | [0.07 0.6] |  | 0.13 | 0.12 | 0.11 | [0.04 0.35] |
| USC |  | 0.34 | 0.33 | 0.33 | [0.1 0.57] |  | 0.36 | 0.35 | 0.35 | [0.06 0.6] |  | 0.17 | 0.16 | 0.15 | [0.05 0.4] |
| WNGC |  | 0.53 | 0.51 | 0.51 | [0.1 0.89] |  | 0.48 | 0.46 | 0.47 | [0.11 0.83] |  | 0.19 | 0.18 | 0.17 | [0.04 0.53] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.3 | 0.29 | 0.02 | [0.27 0.31] | [0.25 0.33] |
| 3 | 0.36 | 0.35 | 0.03 | [0.33 0.38] | [0.29 0.4] |
| 4 | 0.35 | 0.33 | 0.03 | [0.31 0.36] | [0.29 0.4] |
| 5 | 0.34 | 0.32 | 0.02 | [0.31 0.35] | [0.29 0.38] |
| 7.5 | 0.25 | 0.23 | 0.02 | [0.21 0.26] | [0.19 0.29] |
| 10 | 0.15 | 0.14 | 0.02 | [0.13 0.16] | [0.12 0.18] |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_20km_3.png) |

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
| **ALL SITES** |  | **0.45** | **0.43** | **0.41** | **[0.19 1.04]** |  | **0.39** | **0.38** | **0.37** | **[0.12 0.79]** |  | **0.24** | **0.22** | **0.21** | **[0.06 0.5]** |
| PAS |  | 0.43 | 0.41 | 0.4 | [0.19 0.82] |  | 0.37 | 0.36 | 0.35 | [0.15 0.59] |  | 0.22 | 0.21 | 0.2 | [0.07 0.48] |
| SBSM |  | 0.47 | 0.46 | 0.46 | [0.23 0.78] |  | 0.37 | 0.36 | 0.36 | [0.12 0.64] |  | 0.2 | 0.19 | 0.18 | [0.06 0.46] |
| SMCA |  | 0.48 | 0.47 | 0.47 | [0.26 0.81] |  | 0.4 | 0.39 | 0.38 | [0.18 0.66] |  | 0.25 | 0.24 | 0.23 | [0.11 0.44] |
| STNI |  | 0.33 | 0.33 | 0.33 | [0.2 0.53] |  | 0.37 | 0.36 | 0.37 | [0.18 0.55] |  | 0.23 | 0.22 | 0.21 | [0.08 0.46] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.21 0.63] |  | 0.37 | 0.37 | 0.37 | [0.19 0.55] |  | 0.26 | 0.25 | 0.24 | [0.09 0.5] |
| WNGC |  | 0.58 | 0.56 | 0.55 | [0.24 1.04] |  | 0.47 | 0.46 | 0.45 | [0.22 0.79] |  | 0.25 | 0.24 | 0.23 | [0.08 0.48] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 35 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.38 | 0.37 | 0.02 | [0.35 0.39] | [0.32 0.42] |
| 3 | 0.45 | 0.44 | 0.04 | [0.41 0.48] | [0.37 0.53] |
| 4 | 0.43 | 0.41 | 0.03 | [0.38 0.45] | [0.35 0.48] |
| 5 | 0.39 | 0.38 | 0.03 | [0.36 0.41] | [0.32 0.44] |
| 7.5 | 0.33 | 0.32 | 0.02 | [0.3 0.35] | [0.28 0.37] |
| 10 | 0.24 | 0.23 | 0.03 | [0.2 0.25] | [0.17 0.28] |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_50km_3.png) |

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
| **ALL SITES** |  | **0.48** | **0.46** | **0.44** | **[0.19 0.94]** |  | **0.44** | **0.43** | **0.42** | **[0.15 0.75]** |  | **0.27** | **0.26** | **0.25** | **[0.11 0.58]** |
| PAS |  | 0.4 | 0.4 | 0.39 | [0.2 0.71] |  | 0.4 | 0.39 | 0.38 | [0.21 0.63] |  | 0.22 | 0.22 | 0.21 | [0.12 0.43] |
| SBSM |  | 0.58 | 0.57 | 0.57 | [0.28 0.94] |  | 0.46 | 0.46 | 0.46 | [0.22 0.75] |  | 0.25 | 0.25 | 0.24 | [0.13 0.58] |
| SMCA |  | 0.56 | 0.56 | 0.55 | [0.33 0.85] |  | 0.44 | 0.44 | 0.45 | [0.19 0.61] |  | 0.32 | 0.32 | 0.32 | [0.19 0.52] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.19 0.49] |  | 0.39 | 0.38 | 0.39 | [0.15 0.61] |  | 0.25 | 0.25 | 0.24 | [0.11 0.44] |
| USC |  | 0.37 | 0.37 | 0.37 | [0.26 0.57] |  | 0.4 | 0.4 | 0.39 | [0.22 0.58] |  | 0.3 | 0.29 | 0.3 | [0.13 0.45] |
| WNGC |  | 0.55 | 0.54 | 0.53 | [0.26 0.92] |  | 0.51 | 0.5 | 0.5 | [0.24 0.75] |  | 0.25 | 0.24 | 0.24 | [0.12 0.47] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 47 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 10 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.41 | 0.41 | 0.02 | [0.39 0.44] | [0.36 0.47] |
| 3 | 0.48 | 0.48 | 0.04 | [0.44 0.52] | [0.41 0.55] |
| 4 | 0.47 | 0.47 | 0.03 | [0.43 0.5] | [0.39 0.53] |
| 5 | 0.44 | 0.44 | 0.03 | [0.4 0.47] | [0.36 0.49] |
| 7.5 | 0.38 | 0.38 | 0.02 | [0.36 0.4] | [0.32 0.42] |
| 10 | 0.27 | 0.27 | 0.02 | [0.25 0.29] | [0.23 0.31] |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_100km_3.png) |

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
| **ALL SITES** |  | **0.43** | **0.41** | **0.38** | **[0.08 1.04]** |  | **0.39** | **0.38** | **0.37** | **[0.05 0.83]** |  | **0.22** | **0.21** | **0.2** | **[0.03 0.58]** |
| PAS |  | 0.4 | 0.38 | 0.37 | [0.11 0.82] |  | 0.36 | 0.35 | 0.34 | [0.07 0.63] |  | 0.2 | 0.18 | 0.18 | [0.03 0.48] |
| SBSM |  | 0.46 | 0.43 | 0.44 | [0.08 0.94] |  | 0.36 | 0.33 | 0.34 | [0.05 0.75] |  | 0.2 | 0.18 | 0.18 | [0.03 0.58] |
| SMCA |  | 0.47 | 0.45 | 0.46 | [0.14 0.85] |  | 0.4 | 0.39 | 0.39 | [0.11 0.66] |  | 0.25 | 0.24 | 0.23 | [0.04 0.52] |
| STNI |  | 0.31 | 0.31 | 0.31 | [0.11 0.53] |  | 0.35 | 0.34 | 0.35 | [0.07 0.61] |  | 0.21 | 0.19 | 0.19 | [0.04 0.46] |
| USC |  | 0.36 | 0.35 | 0.35 | [0.1 0.63] |  | 0.38 | 0.37 | 0.37 | [0.06 0.6] |  | 0.25 | 0.23 | 0.23 | [0.05 0.5] |
| WNGC |  | 0.56 | 0.54 | 0.53 | [0.1 1.04] |  | 0.49 | 0.47 | 0.48 | [0.11 0.83] |  | 0.23 | 0.22 | 0.21 | [0.04 0.53] |

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 198 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.37 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.38] |
| 3 | 0.43 | 0.43 | 0.02 | [0.41 0.44] | [0.4 0.46] |
| 4 | 0.42 | 0.41 | 0.01 | [0.39 0.42] | [0.38 0.44] |
| 5 | 0.39 | 0.39 | 0.01 | [0.37 0.4] | [0.36 0.41] |
| 7.5 | 0.32 | 0.32 | 0.01 | [0.31 0.33] | [0.29 0.34] |
| 10 | 0.22 | 0.22 | 0.01 | [0.21 0.23] | [0.2 0.24] |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_all_dists_3.png) |

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
| **ALL SITES** |  | **0.35** | **0.34** | **0.33** | **[0.1 0.78]** |  | **0.35** | **0.34** | **0.33** | **[0.09 0.75]** |  | **0.25** | **0.24** | **0.23** | **[0.05 0.64]** |
| PAS |  | 0.37 | 0.36 | 0.35 | [0.13 0.69] |  | 0.32 | 0.31 | 0.3 | [0.1 0.7] |  | 0.22 | 0.21 | 0.19 | [0.05 0.58] |
| SBSM |  | 0.41 | 0.4 | 0.39 | [0.12 0.78] |  | 0.38 | 0.38 | 0.37 | [0.18 0.67] |  | 0.23 | 0.22 | 0.21 | [0.06 0.51] |
| SMCA |  | 0.33 | 0.33 | 0.32 | [0.1 0.69] |  | 0.36 | 0.35 | 0.35 | [0.1 0.75] |  | 0.25 | 0.24 | 0.23 | [0.06 0.61] |
| STNI |  | 0.31 | 0.31 | 0.3 | [0.1 0.59] |  | 0.33 | 0.32 | 0.32 | [0.1 0.73] |  | 0.28 | 0.27 | 0.26 | [0.07 0.64] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.12 0.73] |  | 0.35 | 0.34 | 0.33 | [0.11 0.65] |  | 0.26 | 0.25 | 0.25 | [0.09 0.61] |
| WNGC |  | 0.33 | 0.32 | 0.32 | [0.11 0.69] |  | 0.35 | 0.34 | 0.33 | [0.09 0.66] |  | 0.26 | 0.25 | 0.24 | [0.06 0.59] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.33 | 0.32 | 0.02 | [0.31 0.34] | [0.29 0.36] |
| 3 | 0.35 | 0.34 | 0.02 | [0.32 0.36] | [0.3 0.39] |
| 4 | 0.37 | 0.36 | 0.02 | [0.34 0.38] | [0.32 0.41] |
| 5 | 0.35 | 0.35 | 0.02 | [0.32 0.36] | [0.3 0.38] |
| 7.5 | 0.31 | 0.31 | 0.02 | [0.29 0.34] | [0.26 0.36] |
| 10 | 0.25 | 0.25 | 0.02 | [0.22 0.28] | [0.21 0.3] |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_20km_3.png) |

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


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.32** | **0.3** | **[0.07 0.85]** |  | **0.35** | **0.34** | **0.33** | **[0.07 0.8]** |  | **0.41** | **0.41** | **0.42** | **[0.07 0.71]** |
| PAS |  | 0.34 | 0.32 | 0.3 | [0.09 0.76] |  | 0.32 | 0.3 | 0.29 | [0.1 0.65] |  | 0.41 | 0.4 | 0.41 | [0.12 0.62] |
| SBSM |  | 0.43 | 0.42 | 0.42 | [0.16 0.81] |  | 0.41 | 0.4 | 0.4 | [0.13 0.7] |  | 0.41 | 0.41 | 0.42 | [0.15 0.66] |
| SMCA |  | 0.33 | 0.32 | 0.3 | [0.09 0.74] |  | 0.35 | 0.34 | 0.34 | [0.1 0.76] |  | 0.4 | 0.4 | 0.4 | [0.09 0.66] |
| STNI |  | 0.26 | 0.26 | 0.25 | [0.07 0.57] |  | 0.32 | 0.31 | 0.29 | [0.09 0.8] |  | 0.44 | 0.43 | 0.43 | [0.1 0.71] |
| USC |  | 0.3 | 0.29 | 0.27 | [0.08 0.68] |  | 0.34 | 0.32 | 0.31 | [0.08 0.76] |  | 0.41 | 0.4 | 0.41 | [0.07 0.69] |
| WNGC |  | 0.34 | 0.32 | 0.29 | [0.09 0.85] |  | 0.38 | 0.36 | 0.35 | [0.07 0.79] |  | 0.42 | 0.41 | 0.42 | [0.08 0.66] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 33 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.38 | 0.37 | 0.02 | [0.34 0.39] | [0.32 0.42] |
| 3 | 0.34 | 0.32 | 0.03 | [0.29 0.37] | [0.27 0.4] |
| 4 | 0.35 | 0.34 | 0.03 | [0.31 0.37] | [0.28 0.4] |
| 5 | 0.35 | 0.34 | 0.03 | [0.31 0.37] | [0.26 0.42] |
| 7.5 | 0.41 | 0.4 | 0.03 | [0.37 0.43] | [0.33 0.47] |
| 10 | 0.41 | 0.4 | 0.03 | [0.38 0.43] | [0.36 0.45] |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_50km_3.png) |

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


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.32** | **0.31** | **[0.07 0.8]** |  | **0.38** | **0.36** | **0.36** | **[0.07 0.88]** |  | **0.41** | **0.4** | **0.41** | **[0.05 0.79]** |
| PAS |  | 0.34 | 0.33 | 0.33 | [0.07 0.66] |  | 0.36 | 0.35 | 0.33 | [0.07 0.77] |  | 0.4 | 0.39 | 0.39 | [0.05 0.73] |
| SBSM |  | 0.42 | 0.41 | 0.4 | [0.08 0.8] |  | 0.44 | 0.43 | 0.44 | [0.1 0.86] |  | 0.41 | 0.41 | 0.41 | [0.1 0.7] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.09 0.72] |  | 0.36 | 0.35 | 0.34 | [0.09 0.81] |  | 0.38 | 0.37 | 0.38 | [0.07 0.73] |
| STNI |  | 0.28 | 0.27 | 0.27 | [0.08 0.63] |  | 0.36 | 0.35 | 0.34 | [0.1 0.81] |  | 0.45 | 0.45 | 0.45 | [0.1 0.79] |
| USC |  | 0.3 | 0.29 | 0.29 | [0.07 0.64] |  | 0.35 | 0.34 | 0.33 | [0.07 0.77] |  | 0.41 | 0.4 | 0.4 | [0.08 0.76] |
| WNGC |  | 0.33 | 0.32 | 0.3 | [0.07 0.78] |  | 0.39 | 0.38 | 0.37 | [0.1 0.88] |  | 0.41 | 0.4 | 0.41 | [0.1 0.78] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 29 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 28 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.38 | 0.38 | 0.03 | [0.36 0.41] | [0.33 0.45] |
| 3 | 0.34 | 0.34 | 0.03 | [0.31 0.36] | [0.26 0.39] |
| 4 | 0.36 | 0.36 | 0.04 | [0.32 0.4] | [0.3 0.44] |
| 5 | 0.38 | 0.38 | 0.04 | [0.34 0.42] | [0.3 0.47] |
| 7.5 | 0.42 | 0.42 | 0.04 | [0.38 0.46] | [0.35 0.51] |
| 10 | 0.41 | 0.41 | 0.03 | [0.38 0.44] | [0.34 0.47] |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_100km_3.png) |

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


### All Distances M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.07 0.85]** |  | **0.36** | **0.35** | **0.34** | **[0.07 0.88]** |  | **0.37** | **0.35** | **0.35** | **[0.05 0.79]** |
| PAS |  | 0.35 | 0.34 | 0.33 | [0.07 0.76] |  | 0.33 | 0.32 | 0.31 | [0.07 0.77] |  | 0.35 | 0.33 | 0.34 | [0.05 0.73] |
| SBSM |  | 0.42 | 0.41 | 0.4 | [0.08 0.81] |  | 0.41 | 0.4 | 0.4 | [0.1 0.86] |  | 0.36 | 0.35 | 0.36 | [0.06 0.7] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.09 0.74] |  | 0.36 | 0.35 | 0.34 | [0.09 0.81] |  | 0.35 | 0.34 | 0.33 | [0.06 0.73] |
| STNI |  | 0.29 | 0.28 | 0.27 | [0.07 0.63] |  | 0.34 | 0.33 | 0.31 | [0.09 0.81] |  | 0.4 | 0.38 | 0.39 | [0.07 0.79] |
| USC |  | 0.31 | 0.3 | 0.29 | [0.07 0.73] |  | 0.35 | 0.33 | 0.32 | [0.07 0.77] |  | 0.37 | 0.35 | 0.35 | [0.07 0.76] |
| WNGC |  | 0.33 | 0.32 | 0.3 | [0.07 0.85] |  | 0.38 | 0.36 | 0.35 | [0.07 0.88] |  | 0.37 | 0.36 | 0.35 | [0.06 0.78] |

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 144 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.36 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.38] |
| 3 | 0.34 | 0.33 | 0.01 | [0.32 0.35] | [0.31 0.37] |
| 4 | 0.36 | 0.35 | 0.01 | [0.34 0.37] | [0.32 0.38] |
| 5 | 0.36 | 0.35 | 0.01 | [0.34 0.37] | [0.33 0.38] |
| 7.5 | 0.39 | 0.38 | 0.01 | [0.36 0.39] | [0.35 0.41] |
| 10 | 0.37 | 0.36 | 0.01 | [0.35 0.37] | [0.33 0.4] |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_all_dists_3.png) |

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
| **ALL SITES** |  | **0.44** | **0.43** | **0.41** | **[0.26 0.77]** |  | **0.42** | **0.41** | **0.4** | **[0.22 0.7]** |  | **0.26** | **0.25** | **0.24** | **[0.1 0.53]** |
| PAS |  | 0.46 | 0.45 | 0.45 | [0.32 0.57] |  | 0.4 | 0.39 | 0.38 | [0.25 0.59] |  | 0.24 | 0.22 | 0.21 | [0.11 0.46] |
| SBSM |  | 0.43 | 0.42 | 0.41 | [0.28 0.61] |  | 0.39 | 0.38 | 0.38 | [0.26 0.63] |  | 0.23 | 0.22 | 0.21 | [0.1 0.42] |
| SMCA |  | 0.4 | 0.39 | 0.38 | [0.27 0.52] |  | 0.41 | 0.41 | 0.4 | [0.29 0.62] |  | 0.26 | 0.25 | 0.24 | [0.15 0.44] |
| STNI |  | 0.35 | 0.35 | 0.34 | [0.26 0.48] |  | 0.37 | 0.37 | 0.37 | [0.22 0.59] |  | 0.28 | 0.27 | 0.25 | [0.13 0.53] |
| USC |  | 0.4 | 0.4 | 0.39 | [0.3 0.53] |  | 0.42 | 0.41 | 0.4 | [0.29 0.61] |  | 0.27 | 0.26 | 0.25 | [0.16 0.45] |
| WNGC |  | 0.57 | 0.56 | 0.55 | [0.39 0.77] |  | 0.53 | 0.52 | 0.52 | [0.32 0.7] |  | 0.29 | 0.28 | 0.27 | [0.16 0.48] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.39 | 0.37 | 0.02 | [0.36 0.39] | [0.34 0.41] |
| 3 | 0.44 | 0.43 | 0.02 | [0.4 0.44] | [0.37 0.48] |
| 4 | 0.44 | 0.42 | 0.02 | [0.4 0.45] | [0.38 0.48] |
| 5 | 0.42 | 0.41 | 0.02 | [0.38 0.43] | [0.36 0.46] |
| 7.5 | 0.35 | 0.33 | 0.02 | [0.31 0.36] | [0.29 0.39] |
| 10 | 0.26 | 0.25 | 0.02 | [0.23 0.28] | [0.21 0.31] |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_3.png) |

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


### 50.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.5** | **0.49** | **0.48** | **[0.3 0.76]** |  | **0.46** | **0.46** | **0.45** | **[0.31 0.68]** |  | **0.43** | **0.42** | **0.43** | **[0.22 0.64]** |
| PAS |  | 0.47 | 0.47 | 0.47 | [0.35 0.6] |  | 0.42 | 0.41 | 0.41 | [0.33 0.57] |  | 0.41 | 0.4 | 0.42 | [0.23 0.54] |
| SBSM |  | 0.56 | 0.55 | 0.55 | [0.41 0.75] |  | 0.49 | 0.49 | 0.48 | [0.36 0.64] |  | 0.43 | 0.42 | 0.43 | [0.29 0.57] |
| SMCA |  | 0.52 | 0.52 | 0.52 | [0.42 0.62] |  | 0.47 | 0.46 | 0.46 | [0.36 0.64] |  | 0.43 | 0.42 | 0.43 | [0.28 0.58] |
| STNI |  | 0.38 | 0.37 | 0.37 | [0.3 0.47] |  | 0.42 | 0.42 | 0.4 | [0.31 0.67] |  | 0.45 | 0.44 | 0.45 | [0.23 0.64] |
| USC |  | 0.4 | 0.39 | 0.39 | [0.31 0.52] |  | 0.43 | 0.42 | 0.42 | [0.32 0.64] |  | 0.43 | 0.42 | 0.43 | [0.22 0.6] |
| WNGC |  | 0.61 | 0.61 | 0.6 | [0.46 0.76] |  | 0.53 | 0.53 | 0.53 | [0.43 0.68] |  | 0.43 | 0.43 | 0.43 | [0.3 0.58] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 35 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.45 | 0.02 | [0.43 0.47] | [0.42 0.49] |
| 3 | 0.5 | 0.48 | 0.03 | [0.44 0.51] | [0.41 0.54] |
| 4 | 0.48 | 0.46 | 0.03 | [0.44 0.49] | [0.42 0.54] |
| 5 | 0.46 | 0.45 | 0.02 | [0.42 0.47] | [0.4 0.49] |
| 7.5 | 0.45 | 0.44 | 0.03 | [0.41 0.46] | [0.38 0.49] |
| 10 | 0.43 | 0.41 | 0.02 | [0.39 0.44] | [0.37 0.47] |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_3.png) |

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


### 100.0 km M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.53** | **0.52** | **0.51** | **[0.32 0.8]** |  | **0.52** | **0.51** | **0.51** | **[0.34 0.76]** |  | **0.45** | **0.44** | **0.44** | **[0.27 0.68]** |
| PAS |  | 0.47 | 0.47 | 0.46 | [0.4 0.59] |  | 0.48 | 0.48 | 0.48 | [0.39 0.66] |  | 0.42 | 0.41 | 0.4 | [0.27 0.59] |
| SBSM |  | 0.65 | 0.64 | 0.65 | [0.48 0.8] |  | 0.58 | 0.58 | 0.58 | [0.43 0.74] |  | 0.45 | 0.44 | 0.44 | [0.31 0.62] |
| SMCA |  | 0.61 | 0.6 | 0.6 | [0.47 0.71] |  | 0.51 | 0.51 | 0.51 | [0.39 0.68] |  | 0.45 | 0.44 | 0.44 | [0.31 0.62] |
| STNI |  | 0.38 | 0.38 | 0.38 | [0.32 0.49] |  | 0.48 | 0.47 | 0.47 | [0.34 0.71] |  | 0.48 | 0.47 | 0.47 | [0.29 0.68] |
| USC |  | 0.42 | 0.42 | 0.42 | [0.36 0.51] |  | 0.47 | 0.47 | 0.46 | [0.37 0.67] |  | 0.46 | 0.45 | 0.44 | [0.29 0.65] |
| WNGC |  | 0.59 | 0.59 | 0.58 | [0.43 0.77] |  | 0.58 | 0.58 | 0.58 | [0.45 0.76] |  | 0.44 | 0.44 | 0.43 | [0.29 0.64] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 57 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.51 | 0.02 | [0.48 0.53] | [0.46 0.55] |
| 3 | 0.53 | 0.53 | 0.03 | [0.5 0.56] | [0.47 0.59] |
| 4 | 0.54 | 0.53 | 0.03 | [0.49 0.56] | [0.47 0.59] |
| 5 | 0.52 | 0.52 | 0.03 | [0.49 0.55] | [0.46 0.57] |
| 7.5 | 0.5 | 0.49 | 0.03 | [0.47 0.52] | [0.45 0.56] |
| 10 | 0.45 | 0.44 | 0.03 | [0.42 0.47] | [0.4 0.5] |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_3.png) |

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


### All Distances M6.6 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m6.6_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.49** | **0.48** | **0.46** | **[0.26 0.8]** |  | **0.47** | **0.46** | **0.46** | **[0.22 0.76]** |  | **0.39** | **0.37** | **0.4** | **[0.1 0.68]** |
| PAS |  | 0.47 | 0.46 | 0.46 | [0.32 0.6] |  | 0.43 | 0.43 | 0.42 | [0.25 0.66] |  | 0.37 | 0.35 | 0.37 | [0.11 0.59] |
| SBSM |  | 0.55 | 0.54 | 0.54 | [0.28 0.8] |  | 0.49 | 0.48 | 0.49 | [0.26 0.74] |  | 0.38 | 0.36 | 0.4 | [0.1 0.62] |
| SMCA |  | 0.52 | 0.51 | 0.52 | [0.27 0.71] |  | 0.47 | 0.46 | 0.46 | [0.29 0.68] |  | 0.39 | 0.37 | 0.4 | [0.15 0.62] |
| STNI |  | 0.37 | 0.37 | 0.36 | [0.26 0.49] |  | 0.43 | 0.42 | 0.41 | [0.22 0.71] |  | 0.41 | 0.4 | 0.42 | [0.13 0.68] |
| USC |  | 0.41 | 0.4 | 0.4 | [0.3 0.53] |  | 0.44 | 0.44 | 0.43 | [0.29 0.67] |  | 0.39 | 0.38 | 0.4 | [0.16 0.65] |
| WNGC |  | 0.59 | 0.59 | 0.58 | [0.39 0.77] |  | 0.55 | 0.54 | 0.54 | [0.32 0.76] |  | 0.39 | 0.38 | 0.4 | [0.16 0.64] |

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 258 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.46 | 0.45 | 0.01 | [0.44 0.46] | [0.43 0.47] |
| 3 | 0.49 | 0.49 | 0.01 | [0.47 0.5] | [0.46 0.52] |
| 4 | 0.49 | 0.48 | 0.01 | [0.47 0.5] | [0.46 0.51] |
| 5 | 0.47 | 0.47 | 0.01 | [0.45 0.47] | [0.44 0.48] |
| 7.5 | 0.44 | 0.43 | 0.01 | [0.42 0.44] | [0.41 0.45] |
| 10 | 0.39 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.41] |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_3.png) |

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
| **5 sites, V<sub>S30</sub>=500** |  | **0.43** | **0.43** | **0.42** | **[0.02 1.13]** |  | **0.43** | **0.43** | **0.42** | **[0.03 1.38]** |  | **0.43** | **0.45** | **0.44** | **[0.04 1.09]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 17 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 20 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.43 | 0.05 | [0.38 0.47] | [0.33 0.54] |
| 3 | 0.43 | 0.42 | 0.08 | [0.34 0.48] | [0.26 0.6] |
| 4 | 0.43 | 0.42 | 0.07 | [0.36 0.51] | [0.29 0.59] |
| 5 | 0.43 | 0.42 | 0.07 | [0.35 0.49] | [0.26 0.6] |
| 7.5 | 0.45 | 0.44 | 0.08 | [0.36 0.51] | [0.27 0.6] |
| 10 | 0.43 | 0.42 | 0.07 | [0.36 0.49] | [0.32 0.6] |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_20km_3.png) |

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
| **5 sites, V<sub>S30</sub>=500** |  | **0.5** | **0.5** | **0.49** | **[0.02 1.38]** |  | **0.48** | **0.48** | **0.47** | **[0.02 1.3]** |  | **0.55** | **0.56** | **0.55** | **[0.03 1.31]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 12 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 23 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.52 | 0.5 | 0.07 | [0.42 0.57] | [0.34 0.63] |
| 3 | 0.5 | 0.47 | 0.11 | [0.35 0.57] | [0.27 0.69] |
| 4 | 0.48 | 0.44 | 0.1 | [0.35 0.54] | [0.24 0.68] |
| 5 | 0.48 | 0.46 | 0.1 | [0.36 0.57] | [0.28 0.66] |
| 7.5 | 0.56 | 0.57 | 0.14 | [0.42 0.7] | [0.28 0.84] |
| 10 | 0.55 | 0.55 | 0.12 | [0.42 0.68] | [0.34 0.8] |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_50km_3.png) |

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
| **5 sites, V<sub>S30</sub>=500** |  | **0.53** | **0.53** | **0.51** | **[0.02 1.45]** |  | **0.53** | **0.53** | **0.52** | **[0.02 1.58]** |  | **0.57** | **0.57** | **0.57** | **[0.04 1.4]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 10 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 47 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.55 | 0.55 | 0.11 | [0.43 0.65] | [0.36 0.76] |
| 3 | 0.53 | 0.51 | 0.15 | [0.38 0.68] | [0.27 0.82] |
| 4 | 0.53 | 0.5 | 0.16 | [0.37 0.69] | [0.28 0.88] |
| 5 | 0.53 | 0.52 | 0.14 | [0.39 0.68] | [0.29 0.84] |
| 7.5 | 0.59 | 0.61 | 0.15 | [0.46 0.74] | [0.33 0.95] |
| 10 | 0.57 | 0.56 | 0.14 | [0.44 0.71] | [0.31 0.89] |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_100km_3.png) |

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
| **5 sites, V<sub>S30</sub>=500** |  | **0.49** | **0.48** | **0.47** | **[0.02 1.45]** |  | **0.48** | **0.48** | **0.46** | **[0.02 1.58]** |  | **0.52** | **0.53** | **0.51** | **[0.03 1.4]** |

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 60 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 26 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.5 | 0.49 | 0.04 | [0.45 0.53] | [0.4 0.57] |
| 3 | 0.49 | 0.48 | 0.05 | [0.43 0.54] | [0.38 0.6] |
| 4 | 0.48 | 0.47 | 0.06 | [0.41 0.53] | [0.36 0.6] |
| 5 | 0.48 | 0.46 | 0.06 | [0.41 0.53] | [0.34 0.59] |
| 7.5 | 0.54 | 0.52 | 0.06 | [0.46 0.57] | [0.41 0.66] |
| 10 | 0.52 | 0.5 | 0.05 | [0.46 0.56] | [0.41 0.63] |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_all_dists_3.png) |

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
| **5 sites, V<sub>S30</sub>=500** | **0.22** | **-3.21** | **[-3.7 -2.66]** | **0.23** | **-3.87** | **[-4.33 -3.42]** | **0.32** | **-5.01** | **[-5.83 -4.41]** |
| PAS | 0.21 | -4.49 | [-4.91 -3.84] | 0.23 | -5.09 | [-5.57 -4.53] | 0.34 | -5.88 | [-6.69 -5.28] |
| SBSM | 0.3 | -3.02 | [-3.65 -2.27] | 0.26 | -3.97 | [-4.73 -3.46] | 0.26 | -5.5 | [-6.2 -4.95] |
| SMCA | 0.2 | -3.18 | [-3.66 -2.63] | 0.24 | -3.71 | [-4.23 -3.23] | 0.32 | -4.95 | [-5.72 -4.34] |
| STNI | 0.22 | -3.2 | [-3.7 -2.7] | 0.23 | -3.73 | [-4.26 -3.22] | 0.37 | -4.44 | [-5.49 -3.81] |
| USC | 0.22 | -3.32 | [-3.81 -2.82] | 0.22 | -3.98 | [-4.4 -3.52] | 0.34 | -4.95 | [-5.84 -4.36] |
| WNGC | 0.23 | -3.35 | [-3.83 -2.82] | 0.24 | -4.01 | [-4.48 -3.54] | 0.32 | -5.12 | [-5.94 -4.52] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.29 | 0.09 | [0.2 0.39] | [0.15 0.51] |
| 3 | 0.22 | 0.25 | 0.13 | [0.12 0.39] | [0.07 0.59] |
| 4 | 0.22 | 0.29 | 0.13 | [0.16 0.41] | [0.05 0.61] |
| 5 | 0.23 | 0.29 | 0.13 | [0.15 0.45] | [0.04 0.56] |
| 7.5 | 0.27 | 0.33 | 0.14 | [0.15 0.45] | [0.09 0.61] |
| 10 | 0.32 | 0.3 | 0.16 | [0.17 0.49] | [0.07 0.69] |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_3.png) |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist.png)


### 50.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.21** | **-4.04** | **[-4.53 -3.56]** | **0.25** | **-4.47** | **[-5.05 -3.97]** | **0.31** | **-5.66** | **[-6.46 -5.04]** |
| PAS | 0.2 | -5.45 | [-5.91 -4.93] | 0.24 | -5.88 | [-6.36 -5.39] | 0.34 | -6.55 | [-7.39 -5.9] |
| SBSM | 0.28 | -3.71 | [-4.35 -3.06] | 0.25 | -4.62 | [-5.24 -4.16] | 0.26 | -6.15 | [-6.82 -5.57] |
| SMCA | 0.19 | -4.16 | [-4.57 -3.69] | 0.23 | -4.52 | [-5.03 -4.03] | 0.32 | -5.65 | [-6.44 -5] |
| STNI | 0.2 | -3.94 | [-4.41 -3.48] | 0.28 | -4.13 | [-4.75 -3.53] | 0.37 | -5.03 | [-5.95 -4.34] |
| USC | 0.22 | -4.12 | [-4.62 -3.6] | 0.25 | -4.54 | [-5.1 -4.03] | 0.35 | -5.56 | [-6.41 -4.9] |
| WNGC | 0.22 | -4.22 | [-4.71 -3.72] | 0.26 | -4.58 | [-5.14 -4.05] | 0.33 | -5.73 | [-6.53 -5.08] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 35 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.26 | 0.3 | 0.11 | [0.19 0.4] | [0.12 0.6] |
| 3 | 0.21 | 0.28 | 0.15 | [0.14 0.44] | [0.03 0.68] |
| 4 | 0.22 | 0.25 | 0.14 | [0.12 0.42] | [0.05 0.65] |
| 5 | 0.25 | 0.29 | 0.16 | [0.13 0.44] | [0.06 0.69] |
| 7.5 | 0.28 | 0.31 | 0.18 | [0.11 0.49] | [0.03 0.76] |
| 10 | 0.31 | 0.34 | 0.17 | [0.18 0.54] | [0.09 0.72] |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_3.png) |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist.png)


### 100.0 km M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.19** | **-4.73** | **[-5.18 -4.28]** | **0.24** | **-5.06** | **[-5.63 -4.54]** | **0.32** | **-6.19** | **[-7 -5.57]** |
| PAS | 0.18 | -6.07 | [-6.48 -5.6] | 0.22 | -6.46 | [-6.89 -5.98] | 0.35 | -7.06 | [-7.96 -6.42] |
| SBSM | 0.27 | -4.43 | [-4.95 -3.77] | 0.24 | -5.24 | [-5.8 -4.76] | 0.27 | -6.68 | [-7.4 -6.1] |
| SMCA | 0.17 | -4.85 | [-5.32 -4.46] | 0.25 | -5.04 | [-5.57 -4.51] | 0.32 | -6.19 | [-6.95 -5.54] |
| STNI | 0.18 | -4.65 | [-5.1 -4.2] | 0.25 | -4.74 | [-5.31 -4.19] | 0.36 | -5.55 | [-6.49 -4.89] |
| USC | 0.19 | -4.82 | [-5.27 -4.35] | 0.25 | -5.11 | [-5.7 -4.59] | 0.34 | -6.11 | [-6.95 -5.45] |
| WNGC | 0.2 | -4.87 | [-5.28 -4.36] | 0.24 | -5.21 | [-5.74 -4.73] | 0.33 | -6.26 | [-7.06 -5.61] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 57 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.23 | 0.12 | [0.13 0.38] | [0.07 0.52] |
| 3 | 0.19 | 0.17 | 0.18 | [0.05 0.42] | [0 0.65] |
| 4 | 0.21 | 0.18 | 0.18 | [0.05 0.44] | [0.01 0.7] |
| 5 | 0.24 | 0.21 | 0.2 | [0.06 0.49] | [0.02 0.77] |
| 7.5 | 0.29 | 0.26 | 0.19 | [0.08 0.47] | [0.01 0.73] |
| 10 | 0.32 | 0.23 | 0.2 | [0.09 0.43] | [0.01 0.78] |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_3.png) |

This plot shows the distribution of period-independent downsampled &tau;.

![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist.png)


### All Distances M6.6 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m6.6_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.21** | **-3.99** | **[-5.18 -2.66]** | **0.24** | **-4.47** | **[-5.63 -3.42]** | **0.32** | **-5.62** | **[-7 -4.41]** |
| PAS | 0.2 | -5.34 | [-6.48 -3.84] | 0.23 | -5.81 | [-6.89 -4.53] | 0.34 | -6.5 | [-7.96 -5.28] |
| SBSM | 0.28 | -3.72 | [-4.95 -2.27] | 0.25 | -4.61 | [-5.8 -3.46] | 0.26 | -6.11 | [-7.4 -4.95] |
| SMCA | 0.18 | -4.06 | [-5.32 -2.63] | 0.24 | -4.42 | [-5.57 -3.23] | 0.32 | -5.59 | [-6.95 -4.34] |
| STNI | 0.2 | -3.93 | [-5.1 -2.7] | 0.26 | -4.2 | [-5.31 -3.22] | 0.37 | -5.01 | [-6.49 -3.81] |
| USC | 0.21 | -4.09 | [-5.27 -2.82] | 0.24 | -4.54 | [-5.7 -3.52] | 0.34 | -5.54 | [-6.95 -4.36] |
| WNGC | 0.22 | -4.15 | [-5.28 -2.82] | 0.24 | -4.6 | [-5.74 -3.54] | 0.33 | -5.7 | [-7.06 -4.52] |

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 258 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.34 | 0.05 | [0.29 0.39] | [0.26 0.48] |
| 3 | 0.21 | 0.32 | 0.07 | [0.25 0.39] | [0.2 0.46] |
| 4 | 0.22 | 0.32 | 0.06 | [0.26 0.4] | [0.21 0.47] |
| 5 | 0.24 | 0.34 | 0.07 | [0.27 0.4] | [0.2 0.53] |
| 7.5 | 0.28 | 0.35 | 0.08 | [0.29 0.44] | [0.25 0.54] |
| 10 | 0.32 | 0.37 | 0.09 | [0.29 0.48] | [0.25 0.6] |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_3.png) |

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
| **&tau;** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&tau;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
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
| **M6.6 SS** | **PAS** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **SBSM** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **SMCA** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 SS** | **STNI** | **PASS** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **USC** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 SS** | **WNGC** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 SS** | **5sites_Vs30_500** | **PASS** | **FAIL** | *(FAIL)* |

### BBP PartB, M6.6, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_PAS.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_WNGC.png) |
| **5sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_5sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_5sites_Vs30_500.png) |

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

