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
  * [Fault Section Counts](#fault-section-counts)
* [Sites](#sites)
* [Result Summary Table](#result-summary-table)
  * [GMPE Table](#gmpe-table)
  * [Dist-Dependent Plot Table](#dist-dependent-plot-table)
* [Path-to-path Variability](#path-to-path-variability)
  * [Path-to-path Variability Methodology](#path-to-path-variability-methodology)
  * [20.0 km M7.2 Path-to-path Results](#200-km-m72-path-to-path-results)
  * [50.0 km M7.2 Path-to-path Results](#500-km-m72-path-to-path-results)
  * [100.0 km M7.2 Path-to-path Results](#1000-km-m72-path-to-path-results)
  * [All Distances M7.2 Path-to-path Results](#all-distances-m72-path-to-path-results)
* [Source-strike Variability](#source-strike-variability)
  * [Source-strike Variability Methodology](#source-strike-variability-methodology)
  * [20.0 km M7.2 Source-strike Results](#200-km-m72-source-strike-results)
  * [50.0 km M7.2 Source-strike Results](#500-km-m72-source-strike-results)
  * [100.0 km M7.2 Source-strike Results](#1000-km-m72-source-strike-results)
  * [All Distances M7.2 Source-strike Results](#all-distances-m72-source-strike-results)
* [Within-event, single-site Variability](#within-event-single-site-variability)
  * [Within-event, single-site Variability Methodology](#within-event-single-site-variability-methodology)
  * [20.0 km M7.2 Within-event, single-site Results](#200-km-m72-within-event-single-site-results)
  * [50.0 km M7.2 Within-event, single-site Results](#500-km-m72-within-event-single-site-results)
  * [100.0 km M7.2 Within-event, single-site Results](#1000-km-m72-within-event-single-site-results)
  * [All Distances M7.2 Within-event, single-site Results](#all-distances-m72-within-event-single-site-results)
* [Within-event Variability](#within-event-variability)
  * [Within-event Variability Methodology](#within-event-variability-methodology)
  * [20.0 km M7.2 Within-event Results](#200-km-m72-within-event-results)
  * [50.0 km M7.2 Within-event Results](#500-km-m72-within-event-results)
  * [100.0 km M7.2 Within-event Results](#1000-km-m72-within-event-results)
  * [All Distances M7.2 Within-event Results](#all-distances-m72-within-event-results)
* [Between-events Variability](#between-events-variability)
  * [Between-events Variability Methodology](#between-events-variability-methodology)
  * [20.0 km M7.2 Between-events Results](#200-km-m72-between-events-results)
  * [50.0 km M7.2 Between-events Results](#500-km-m72-between-events-results)
  * [100.0 km M7.2 Between-events Results](#1000-km-m72-between-events-results)
  * [All Distances M7.2 Between-events Results](#all-distances-m72-between-events-results)
* [Azumth Dependence](#azumth-dependence)
  * [PAS Azumth Dependence](#pas-azumth-dependence)
  * [SBSM Azumth Dependence](#sbsm-azumth-dependence)
  * [SMCA Azumth Dependence](#smca-azumth-dependence)
  * [STNI Azumth Dependence](#stni-azumth-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
  * [WNGC Azumth Dependence](#wngc-azumth-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
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

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| Cerro Prieto | 30 |
| San Jacinto (Clark) rev | 9 |
| San Jacinto (Coyote Creek) | 9 |
| Garlock (West) | 9 |
| Brawley (Seismic Zone) alt 1 | 5 |
| Death Valley (No) | 5 |
| San Andreas (Creeping Section) 2011 CFM | 4 |
| San Juan | 4 |
| Mendocino | 4 |
| San Andreas (Offshore) 2011 CFM | 3 |
| San Andreas (Parkfield) | 2 |
| Gravel Hills-Harper Lk | 2 |
| Pisgah-Bullion Mtn-Mesquite Lk | 2 |
| Earthquake Valley (No  Extension) | 2 |
| Blackwater | 2 |
| Ash Hill | 2 |
| San Gregorio (North) 2011 CFM | 2 |
| Earthquake Valley | 2 |
| San Andreas (Coachella) rev | 1 |
| San Diego Trough south | 1 |
| Emerson-Copper Mtn 2011 | 1 |
| Eaton Roughs 2011 CFM | 1 |
| San Jacinto (Borrego) | 1 |
| San Jacinto (Stepovers Combined) | 1 |
| San Jacinto (San Jacinto Valley) rev | 1 |
| San Jacinto (San Bernardino) | 1 |
| Johnson Valley (No) 2011 rev | 1 |
| Camp Rock 2011 | 1 |

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
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.29 | 0.36 | 0.32 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.37 | 0.45 | 0.38 | 0.23 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.41 | 0.49 | 0.43 | 0.27 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.36 | 0.43 | 0.38 | 0.22 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.36 | 0.38 | 0.38 | 0.31 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.4 | 0.36 | 0.39 | 0.44 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.4 | 0.34 | 0.4 | 0.45 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.39 | 0.36 | 0.39 | 0.41 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.41 | 0.46 | 0.43 | 0.32 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.48 | 0.51 | 0.48 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.52 | 0.54 | 0.52 | 0.48 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.47 | 0.51 | 0.48 | 0.42 |
| Within-event | &phi; | 20 km | 0.64 | 0.69 | 0.65 | 0.55 |
| Within-event | &phi; | 50 km | 0.71 | 0.74 | 0.71 | 0.65 |
| Within-event | &phi; | 100 km | 0.73 | 0.75 | 0.74 | 0.67 |
| Within-event | &phi; | (all) | 0.69 | 0.72 | 0.7 | 0.62 |
| Between-events | &tau; | 20 km | 0.15 | 0.1 | 0.15 | 0.19 |
| Between-events | &tau; | 50 km | 0.16 | 0.11 | 0.17 | 0.19 |
| Between-events | &tau; | 100 km | 0.16 | 0.11 | 0.16 | 0.2 |
| Between-events | &tau; | (all) | 0.16 | 0.11 | 0.16 | 0.19 |

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
| Between-events | &tau; | 20 km | 0.36 | 0.36 | 0.36 |
| Between-events | &tau; | 50 km | 0.36 | 0.36 | 0.36 |
| Between-events | &tau; | 100 km | 0.36 | 0.36 | 0.36 |

### Dist-Dependent Plot Table
*[(top)](#table-of-contents)*

| **&phi;<sub>P2P</sub>** | ![&phi;<sub>P2P</sub>](resources/path_m7.2_dist_periods.png) |
|-----|-----|
| **&phi;<sub>s</sub>** | ![&phi;<sub>s</sub>](resources/source_strike_m7.2_dist_periods.png) |
| **&phi;<sub>SS</sub>** | ![&phi;<sub>SS</sub>](resources/within_event_ss_m7.2_dist_periods.png) |
| **&phi;** | ![&phi;](resources/within_event_m7.2_dist_periods.png) |
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

We also compute distance-independent &phi;<sub>P2P</sub>, which is computed as the standard deviation of all residuals across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.36** | **0.34** | **0.3** | **[0.1 0.96]** |  | **0.32** | **0.3** | **0.29** | **[0.05 0.84]** |  | **0.15** | **0.14** | **0.13** | **[0.03 0.46]** |
| PAS |  | 0.36 | 0.35 | 0.33 | [0.11 0.75] |  | 0.31 | 0.3 | 0.29 | [0.08 0.63] |  | 0.14 | 0.13 | 0.12 | [0.03 0.39] |
| SBSM |  | 0.28 | 0.27 | 0.26 | [0.1 0.6] |  | 0.21 | 0.2 | 0.18 | [0.05 0.49] |  | 0.13 | 0.12 | 0.11 | [0.03 0.32] |
| SMCA |  | 0.32 | 0.3 | 0.29 | [0.11 0.65] |  | 0.31 | 0.29 | 0.28 | [0.12 0.59] |  | 0.16 | 0.15 | 0.15 | [0.04 0.38] |
| STNI |  | 0.26 | 0.25 | 0.25 | [0.11 0.47] |  | 0.27 | 0.27 | 0.26 | [0.06 0.5] |  | 0.13 | 0.12 | 0.12 | [0.03 0.32] |
| USC |  | 0.3 | 0.3 | 0.29 | [0.1 0.57] |  | 0.32 | 0.31 | 0.3 | [0.08 0.61] |  | 0.16 | 0.15 | 0.14 | [0.05 0.37] |
| WNGC |  | 0.56 | 0.54 | 0.54 | [0.21 0.96] |  | 0.45 | 0.44 | 0.43 | [0.16 0.84] |  | 0.19 | 0.18 | 0.17 | [0.05 0.46] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_20km_3s_hist.png) | ![5s](resources/path_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.29 | 0.29 | 0.02 | [0.27 0.31] | [0.25 0.33] |
| 3 | 0.36 | 0.36 | 0.03 | [0.32 0.39] | [0.3 0.41] |
| 4 | 0.34 | 0.34 | 0.03 | [0.31 0.37] | [0.28 0.39] |
| 5 | 0.32 | 0.32 | 0.02 | [0.3 0.35] | [0.28 0.36] |
| 7.5 | 0.24 | 0.24 | 0.02 | [0.22 0.26] | [0.2 0.28] |
| 10 | 0.15 | 0.15 | 0.02 | [0.13 0.17] | [0.13 0.19] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/path_event_recordings_hist_20km.png)


### 50.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.45** | **0.42** | **0.41** | **[0.17 0.94]** |  | **0.38** | **0.37** | **0.36** | **[0.15 0.75]** |  | **0.23** | **0.22** | **0.21** | **[0.06 0.49]** |
| PAS |  | 0.4 | 0.39 | 0.38 | [0.18 0.75] |  | 0.35 | 0.34 | 0.33 | [0.15 0.6] |  | 0.2 | 0.19 | 0.18 | [0.06 0.43] |
| SBSM |  | 0.5 | 0.5 | 0.49 | [0.28 0.88] |  | 0.4 | 0.4 | 0.39 | [0.18 0.75] |  | 0.23 | 0.22 | 0.21 | [0.07 0.43] |
| SMCA |  | 0.47 | 0.46 | 0.46 | [0.23 0.74] |  | 0.38 | 0.37 | 0.36 | [0.19 0.66] |  | 0.25 | 0.25 | 0.24 | [0.11 0.45] |
| STNI |  | 0.29 | 0.29 | 0.28 | [0.17 0.48] |  | 0.33 | 0.33 | 0.32 | [0.18 0.54] |  | 0.21 | 0.2 | 0.19 | [0.06 0.43] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.17 0.61] |  | 0.35 | 0.34 | 0.34 | [0.18 0.54] |  | 0.25 | 0.24 | 0.23 | [0.08 0.49] |
| WNGC |  | 0.59 | 0.58 | 0.58 | [0.27 0.94] |  | 0.46 | 0.45 | 0.45 | [0.19 0.75] |  | 0.23 | 0.22 | 0.22 | [0.08 0.47] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_50km_3s_hist.png) | ![5s](resources/path_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.37 | 0.34 | 0.02 | [0.32 0.37] | [0.3 0.39] |
| 3 | 0.45 | 0.42 | 0.03 | [0.38 0.45] | [0.35 0.48] |
| 4 | 0.42 | 0.39 | 0.03 | [0.36 0.43] | [0.34 0.45] |
| 5 | 0.38 | 0.36 | 0.03 | [0.33 0.39] | [0.31 0.42] |
| 7.5 | 0.31 | 0.3 | 0.02 | [0.27 0.32] | [0.25 0.34] |
| 10 | 0.23 | 0.22 | 0.02 | [0.2 0.24] | [0.17 0.25] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/path_event_recordings_hist_50km.png)


### 100.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.49** | **0.47** | **0.46** | **[0.2 0.92]** |  | **0.43** | **0.42** | **0.41** | **[0.18 0.79]** |  | **0.27** | **0.27** | **0.26** | **[0.09 0.51]** |
| PAS |  | 0.42 | 0.42 | 0.41 | [0.23 0.7] |  | 0.38 | 0.38 | 0.37 | [0.2 0.64] |  | 0.22 | 0.21 | 0.21 | [0.09 0.41] |
| SBSM |  | 0.58 | 0.57 | 0.57 | [0.3 0.92] |  | 0.44 | 0.44 | 0.44 | [0.22 0.7] |  | 0.26 | 0.26 | 0.25 | [0.11 0.46] |
| SMCA |  | 0.55 | 0.55 | 0.55 | [0.31 0.85] |  | 0.43 | 0.43 | 0.43 | [0.26 0.62] |  | 0.31 | 0.31 | 0.31 | [0.16 0.49] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.2 0.51] |  | 0.39 | 0.39 | 0.38 | [0.18 0.62] |  | 0.27 | 0.26 | 0.26 | [0.09 0.51] |
| USC |  | 0.38 | 0.38 | 0.38 | [0.26 0.66] |  | 0.41 | 0.41 | 0.4 | [0.24 0.62] |  | 0.3 | 0.3 | 0.3 | [0.13 0.51] |
| WNGC |  | 0.58 | 0.58 | 0.58 | [0.34 0.9] |  | 0.49 | 0.48 | 0.49 | [0.25 0.79] |  | 0.26 | 0.25 | 0.25 | [0.1 0.46] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_100km_3s_hist.png) | ![5s](resources/path_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.41 | 0.41 | 0.02 | [0.39 0.43] | [0.38 0.45] |
| 3 | 0.49 | 0.48 | 0.03 | [0.46 0.52] | [0.44 0.54] |
| 4 | 0.47 | 0.46 | 0.02 | [0.44 0.49] | [0.42 0.51] |
| 5 | 0.43 | 0.42 | 0.02 | [0.4 0.46] | [0.38 0.47] |
| 7.5 | 0.36 | 0.37 | 0.02 | [0.34 0.39] | [0.32 0.4] |
| 10 | 0.27 | 0.27 | 0.02 | [0.26 0.29] | [0.24 0.31] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/path_event_recordings_hist_100km.png)


### All Distances M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.43** | **0.41** | **0.39** | **[0.1 0.96]** |  | **0.38** | **0.36** | **0.36** | **[0.05 0.84]** |  | **0.22** | **0.21** | **0.2** | **[0.03 0.51]** |
| PAS |  | 0.39 | 0.38 | 0.38 | [0.11 0.75] |  | 0.35 | 0.34 | 0.33 | [0.08 0.64] |  | 0.19 | 0.18 | 0.18 | [0.03 0.43] |
| SBSM |  | 0.47 | 0.45 | 0.47 | [0.1 0.92] |  | 0.37 | 0.34 | 0.36 | [0.05 0.75] |  | 0.21 | 0.2 | 0.2 | [0.03 0.46] |
| SMCA |  | 0.46 | 0.44 | 0.45 | [0.11 0.85] |  | 0.38 | 0.37 | 0.37 | [0.12 0.66] |  | 0.25 | 0.24 | 0.24 | [0.04 0.49] |
| STNI |  | 0.29 | 0.29 | 0.29 | [0.11 0.51] |  | 0.33 | 0.33 | 0.32 | [0.06 0.62] |  | 0.21 | 0.19 | 0.19 | [0.03 0.51] |
| USC |  | 0.34 | 0.33 | 0.33 | [0.1 0.66] |  | 0.36 | 0.35 | 0.35 | [0.08 0.62] |  | 0.24 | 0.23 | 0.22 | [0.05 0.51] |
| WNGC |  | 0.58 | 0.57 | 0.56 | [0.21 0.96] |  | 0.47 | 0.46 | 0.45 | [0.16 0.84] |  | 0.23 | 0.22 | 0.22 | [0.05 0.47] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_3s_hist.png) | ![5s](resources/path_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 489 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 73 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.36 | 0.36 | 0.01 | [0.35 0.37] | [0.35 0.37] |
| 3 | 0.43 | 0.44 | 0.01 | [0.42 0.44] | [0.41 0.45] |
| 4 | 0.41 | 0.41 | 0.01 | [0.4 0.42] | [0.39 0.43] |
| 5 | 0.38 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.4] |
| 7.5 | 0.31 | 0.31 | 0.01 | [0.3 0.32] | [0.29 0.32] |
| 10 | 0.22 | 0.22 | 0.01 | [0.22 0.23] | [0.21 0.24] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/path_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>P2P</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (36), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/path_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/path_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/path_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/path_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/path_event_recordings_hist_all_dists.png)


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


### 20.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.38** | **0.37** | **0.36** | **[0.09 0.81]** |  | **0.38** | **0.37** | **0.35** | **[0.12 0.86]** |  | **0.31** | **0.3** | **0.29** | **[0.09 0.68]** |
| PAS |  | 0.41 | 0.4 | 0.4 | [0.15 0.74] |  | 0.39 | 0.38 | 0.37 | [0.14 0.78] |  | 0.3 | 0.29 | 0.28 | [0.1 0.59] |
| SBSM |  | 0.43 | 0.42 | 0.41 | [0.15 0.81] |  | 0.41 | 0.4 | 0.38 | [0.14 0.8] |  | 0.3 | 0.29 | 0.28 | [0.11 0.61] |
| SMCA |  | 0.38 | 0.38 | 0.38 | [0.16 0.68] |  | 0.4 | 0.39 | 0.37 | [0.15 0.86] |  | 0.32 | 0.31 | 0.3 | [0.1 0.68] |
| STNI |  | 0.31 | 0.31 | 0.3 | [0.09 0.59] |  | 0.32 | 0.32 | 0.3 | [0.13 0.74] |  | 0.32 | 0.31 | 0.3 | [0.1 0.66] |
| USC |  | 0.36 | 0.35 | 0.35 | [0.11 0.7] |  | 0.36 | 0.35 | 0.34 | [0.12 0.79] |  | 0.31 | 0.31 | 0.3 | [0.1 0.67] |
| WNGC |  | 0.36 | 0.36 | 0.35 | [0.11 0.75] |  | 0.37 | 0.36 | 0.35 | [0.15 0.78] |  | 0.31 | 0.3 | 0.29 | [0.09 0.59] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_20km_3s_hist.png) | ![5s](resources/source_strike_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 49 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.36 | 0.36 | 0.02 | [0.34 0.38] | [0.33 0.4] |
| 3 | 0.38 | 0.37 | 0.02 | [0.35 0.39] | [0.32 0.43] |
| 4 | 0.39 | 0.39 | 0.02 | [0.36 0.41] | [0.34 0.44] |
| 5 | 0.38 | 0.37 | 0.03 | [0.35 0.41] | [0.32 0.43] |
| 7.5 | 0.35 | 0.35 | 0.03 | [0.33 0.38] | [0.3 0.41] |
| 10 | 0.31 | 0.31 | 0.02 | [0.29 0.33] | [0.27 0.36] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/source_strike_event_recordings_hist_20km.png)


### 50.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.36** | **0.35** | **0.33** | **[0.1 0.88]** |  | **0.39** | **0.38** | **0.36** | **[0.09 0.87]** |  | **0.44** | **0.43** | **0.43** | **[0.12 0.92]** |
| PAS |  | 0.36 | 0.34 | 0.32 | [0.12 0.77] |  | 0.36 | 0.34 | 0.32 | [0.11 0.81] |  | 0.44 | 0.43 | 0.43 | [0.19 0.82] |
| SBSM |  | 0.45 | 0.45 | 0.45 | [0.17 0.88] |  | 0.45 | 0.44 | 0.43 | [0.2 0.79] |  | 0.43 | 0.43 | 0.42 | [0.23 0.76] |
| SMCA |  | 0.35 | 0.34 | 0.33 | [0.1 0.71] |  | 0.39 | 0.38 | 0.36 | [0.09 0.85] |  | 0.44 | 0.43 | 0.42 | [0.16 0.83] |
| STNI |  | 0.3 | 0.3 | 0.29 | [0.1 0.64] |  | 0.36 | 0.35 | 0.33 | [0.11 0.82] |  | 0.47 | 0.46 | 0.46 | [0.2 0.91] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.11 0.69] |  | 0.37 | 0.36 | 0.34 | [0.11 0.84] |  | 0.44 | 0.43 | 0.42 | [0.12 0.92] |
| WNGC |  | 0.37 | 0.35 | 0.32 | [0.11 0.84] |  | 0.41 | 0.39 | 0.37 | [0.13 0.87] |  | 0.44 | 0.43 | 0.43 | [0.18 0.86] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_50km_3s_hist.png) | ![5s](resources/source_strike_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.4 | 0.39 | 0.02 | [0.35 0.4] | [0.34 0.43] |
| 3 | 0.36 | 0.35 | 0.03 | [0.32 0.37] | [0.29 0.4] |
| 4 | 0.38 | 0.36 | 0.03 | [0.33 0.39] | [0.31 0.42] |
| 5 | 0.39 | 0.36 | 0.03 | [0.34 0.4] | [0.3 0.43] |
| 7.5 | 0.42 | 0.41 | 0.03 | [0.37 0.44] | [0.33 0.48] |
| 10 | 0.44 | 0.43 | 0.03 | [0.4 0.45] | [0.37 0.49] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/source_strike_event_recordings_hist_50km.png)


### 100.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.08 0.91]** |  | **0.4** | **0.38** | **0.37** | **[0.09 0.89]** |  | **0.45** | **0.44** | **0.44** | **[0.12 0.97]** |
| PAS |  | 0.34 | 0.33 | 0.33 | [0.12 0.67] |  | 0.38 | 0.36 | 0.35 | [0.11 0.85] |  | 0.45 | 0.44 | 0.44 | [0.13 0.87] |
| SBSM |  | 0.42 | 0.42 | 0.41 | [0.1 0.91] |  | 0.45 | 0.44 | 0.43 | [0.12 0.85] |  | 0.43 | 0.43 | 0.43 | [0.13 0.78] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.08 0.8] |  | 0.39 | 0.37 | 0.36 | [0.1 0.78] |  | 0.43 | 0.42 | 0.42 | [0.12 0.88] |
| STNI |  | 0.29 | 0.28 | 0.28 | [0.1 0.56] |  | 0.38 | 0.37 | 0.36 | [0.12 0.85] |  | 0.49 | 0.49 | 0.48 | [0.16 0.93] |
| USC |  | 0.31 | 0.31 | 0.3 | [0.1 0.63] |  | 0.38 | 0.37 | 0.36 | [0.11 0.89] |  | 0.45 | 0.44 | 0.44 | [0.17 0.91] |
| WNGC |  | 0.34 | 0.33 | 0.31 | [0.1 0.84] |  | 0.41 | 0.39 | 0.38 | [0.09 0.89] |  | 0.45 | 0.45 | 0.44 | [0.16 0.97] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_100km_3s_hist.png) | ![5s](resources/source_strike_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 41 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 20 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.4 | 0.4 | 0.03 | [0.38 0.43] | [0.35 0.47] |
| 3 | 0.34 | 0.34 | 0.02 | [0.31 0.37] | [0.29 0.38] |
| 4 | 0.38 | 0.38 | 0.03 | [0.35 0.41] | [0.31 0.44] |
| 5 | 0.4 | 0.39 | 0.04 | [0.36 0.44] | [0.32 0.48] |
| 7.5 | 0.44 | 0.43 | 0.04 | [0.41 0.47] | [0.38 0.54] |
| 10 | 0.45 | 0.45 | 0.03 | [0.42 0.48] | [0.38 0.54] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/source_strike_event_recordings_hist_100km.png)


### All Distances M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.36** | **0.35** | **0.34** | **[0.08 0.91]** |  | **0.39** | **0.37** | **0.36** | **[0.09 0.89]** |  | **0.41** | **0.39** | **0.39** | **[0.09 0.97]** |
| PAS |  | 0.37 | 0.36 | 0.35 | [0.12 0.77] |  | 0.38 | 0.36 | 0.35 | [0.11 0.85] |  | 0.4 | 0.39 | 0.39 | [0.1 0.87] |
| SBSM |  | 0.44 | 0.43 | 0.42 | [0.1 0.91] |  | 0.44 | 0.43 | 0.41 | [0.12 0.85] |  | 0.39 | 0.38 | 0.39 | [0.11 0.78] |
| SMCA |  | 0.36 | 0.35 | 0.34 | [0.08 0.8] |  | 0.39 | 0.38 | 0.37 | [0.09 0.86] |  | 0.4 | 0.38 | 0.38 | [0.1 0.88] |
| STNI |  | 0.3 | 0.29 | 0.29 | [0.09 0.64] |  | 0.36 | 0.34 | 0.33 | [0.11 0.85] |  | 0.43 | 0.42 | 0.42 | [0.1 0.93] |
| USC |  | 0.33 | 0.33 | 0.32 | [0.1 0.7] |  | 0.37 | 0.36 | 0.35 | [0.11 0.89] |  | 0.41 | 0.39 | 0.39 | [0.1 0.92] |
| WNGC |  | 0.36 | 0.35 | 0.33 | [0.1 0.84] |  | 0.39 | 0.38 | 0.36 | [0.09 0.89] |  | 0.4 | 0.39 | 0.39 | [0.09 0.97] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_3s_hist.png) | ![5s](resources/source_strike_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 273 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 289 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.39 | 0.39 | 0.01 | [0.38 0.4] | [0.37 0.4] |
| 3 | 0.36 | 0.36 | 0.01 | [0.35 0.37] | [0.34 0.38] |
| 4 | 0.38 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.4] |
| 5 | 0.39 | 0.39 | 0.01 | [0.38 0.4] | [0.37 0.41] |
| 7.5 | 0.41 | 0.41 | 0.01 | [0.39 0.42] | [0.38 0.42] |
| 10 | 0.41 | 0.4 | 0.01 | [0.39 0.42] | [0.38 0.43] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/source_strike_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>s</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (18), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/source_strike_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/source_strike_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/source_strike_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/source_strike_event_recordings_hist_all_dists.png)


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


### 20.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.46** | **0.45** | **0.43** | **[0.27 0.7]** |  | **0.43** | **0.42** | **0.41** | **[0.26 0.7]** |  | **0.32** | **0.3** | **0.3** | **[0.15 0.59]** |
| PAS |  | 0.49 | 0.48 | 0.47 | [0.38 0.62] |  | 0.45 | 0.44 | 0.43 | [0.33 0.7] |  | 0.31 | 0.29 | 0.28 | [0.17 0.5] |
| SBSM |  | 0.45 | 0.44 | 0.44 | [0.29 0.67] |  | 0.42 | 0.41 | 0.39 | [0.26 0.66] |  | 0.3 | 0.29 | 0.28 | [0.15 0.49] |
| SMCA |  | 0.43 | 0.43 | 0.42 | [0.33 0.53] |  | 0.43 | 0.42 | 0.4 | [0.31 0.68] |  | 0.32 | 0.31 | 0.3 | [0.19 0.53] |
| STNI |  | 0.34 | 0.34 | 0.34 | [0.27 0.45] |  | 0.35 | 0.34 | 0.34 | [0.26 0.53] |  | 0.32 | 0.31 | 0.3 | [0.15 0.59] |
| USC |  | 0.41 | 0.4 | 0.39 | [0.32 0.53] |  | 0.4 | 0.4 | 0.38 | [0.3 0.59] |  | 0.32 | 0.31 | 0.3 | [0.17 0.56] |
| WNGC |  | 0.6 | 0.6 | 0.6 | [0.49 0.7] |  | 0.52 | 0.51 | 0.5 | [0.41 0.69] |  | 0.33 | 0.32 | 0.32 | [0.2 0.53] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_20km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.41 | 0.4 | 0.02 | [0.39 0.42] | [0.38 0.44] |
| 3 | 0.46 | 0.45 | 0.02 | [0.43 0.47] | [0.41 0.5] |
| 4 | 0.46 | 0.44 | 0.02 | [0.43 0.46] | [0.41 0.49] |
| 5 | 0.43 | 0.42 | 0.03 | [0.4 0.45] | [0.37 0.48] |
| 7.5 | 0.37 | 0.37 | 0.02 | [0.34 0.4] | [0.32 0.42] |
| 10 | 0.32 | 0.31 | 0.02 | [0.29 0.34] | [0.26 0.37] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_20km.png)


### 50.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.51** | **0.5** | **0.5** | **[0.3 0.74]** |  | **0.48** | **0.47** | **0.46** | **[0.31 0.75]** |  | **0.45** | **0.45** | **0.44** | **[0.28 0.81]** |
| PAS |  | 0.47 | 0.47 | 0.47 | [0.37 0.57] |  | 0.43 | 0.43 | 0.41 | [0.32 0.62] |  | 0.44 | 0.43 | 0.43 | [0.28 0.71] |
| SBSM |  | 0.61 | 0.61 | 0.6 | [0.49 0.74] |  | 0.55 | 0.55 | 0.53 | [0.42 0.75] |  | 0.46 | 0.45 | 0.44 | [0.36 0.68] |
| SMCA |  | 0.52 | 0.52 | 0.52 | [0.44 0.6] |  | 0.46 | 0.46 | 0.45 | [0.34 0.66] |  | 0.45 | 0.45 | 0.43 | [0.31 0.71] |
| STNI |  | 0.37 | 0.36 | 0.36 | [0.3 0.48] |  | 0.41 | 0.41 | 0.39 | [0.31 0.63] |  | 0.48 | 0.46 | 0.46 | [0.3 0.81] |
| USC |  | 0.39 | 0.39 | 0.39 | [0.32 0.47] |  | 0.43 | 0.43 | 0.41 | [0.32 0.65] |  | 0.45 | 0.44 | 0.45 | [0.3 0.74] |
| WNGC |  | 0.64 | 0.63 | 0.64 | [0.53 0.73] |  | 0.54 | 0.54 | 0.53 | [0.43 0.71] |  | 0.45 | 0.44 | 0.43 | [0.33 0.73] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_50km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.48 | 0.46 | 0.03 | [0.43 0.49] | [0.42 0.52] |
| 3 | 0.51 | 0.49 | 0.04 | [0.46 0.53] | [0.43 0.57] |
| 4 | 0.5 | 0.47 | 0.04 | [0.44 0.52] | [0.42 0.55] |
| 5 | 0.48 | 0.45 | 0.04 | [0.42 0.5] | [0.4 0.54] |
| 7.5 | 0.46 | 0.44 | 0.03 | [0.4 0.47] | [0.38 0.5] |
| 10 | 0.45 | 0.44 | 0.03 | [0.41 0.47] | [0.38 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_50km.png)


### 100.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.54** | **0.53** | **0.54** | **[0.31 0.76]** |  | **0.52** | **0.52** | **0.52** | **[0.38 0.76]** |  | **0.48** | **0.48** | **0.47** | **[0.29 0.82]** |
| PAS |  | 0.49 | 0.49 | 0.48 | [0.41 0.56] |  | 0.48 | 0.48 | 0.47 | [0.38 0.66] |  | 0.46 | 0.45 | 0.45 | [0.29 0.73] |
| SBSM |  | 0.65 | 0.65 | 0.65 | [0.53 0.76] |  | 0.57 | 0.57 | 0.56 | [0.45 0.73] |  | 0.47 | 0.47 | 0.46 | [0.36 0.68] |
| SMCA |  | 0.6 | 0.6 | 0.6 | [0.5 0.66] |  | 0.52 | 0.52 | 0.51 | [0.42 0.72] |  | 0.48 | 0.47 | 0.47 | [0.33 0.76] |
| STNI |  | 0.38 | 0.38 | 0.38 | [0.31 0.46] |  | 0.49 | 0.48 | 0.46 | [0.38 0.71] |  | 0.51 | 0.51 | 0.5 | [0.33 0.82] |
| USC |  | 0.44 | 0.44 | 0.43 | [0.36 0.52] |  | 0.5 | 0.49 | 0.48 | [0.39 0.7] |  | 0.49 | 0.49 | 0.48 | [0.32 0.78] |
| WNGC |  | 0.63 | 0.63 | 0.63 | [0.53 0.72] |  | 0.58 | 0.57 | 0.56 | [0.46 0.76] |  | 0.48 | 0.47 | 0.46 | [0.32 0.75] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_100km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.52 | 0.52 | 0.02 | [0.5 0.54] | [0.49 0.56] |
| 3 | 0.54 | 0.54 | 0.02 | [0.51 0.56] | [0.49 0.58] |
| 4 | 0.54 | 0.54 | 0.02 | [0.52 0.56] | [0.49 0.59] |
| 5 | 0.52 | 0.52 | 0.02 | [0.5 0.55] | [0.48 0.57] |
| 7.5 | 0.51 | 0.5 | 0.02 | [0.48 0.53] | [0.46 0.55] |
| 10 | 0.48 | 0.48 | 0.02 | [0.45 0.51] | [0.43 0.53] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_100km.png)


### All Distances M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.51** | **0.49** | **0.48** | **[0.27 0.76]** |  | **0.48** | **0.47** | **0.47** | **[0.26 0.76]** |  | **0.42** | **0.41** | **0.42** | **[0.15 0.82]** |
| PAS |  | 0.48 | 0.48 | 0.48 | [0.37 0.62] |  | 0.46 | 0.45 | 0.44 | [0.32 0.7] |  | 0.41 | 0.39 | 0.4 | [0.17 0.73] |
| SBSM |  | 0.58 | 0.57 | 0.59 | [0.29 0.76] |  | 0.52 | 0.51 | 0.52 | [0.26 0.75] |  | 0.42 | 0.4 | 0.42 | [0.15 0.68] |
| SMCA |  | 0.52 | 0.52 | 0.52 | [0.33 0.66] |  | 0.47 | 0.46 | 0.46 | [0.31 0.72] |  | 0.42 | 0.41 | 0.42 | [0.19 0.76] |
| STNI |  | 0.37 | 0.36 | 0.36 | [0.27 0.48] |  | 0.42 | 0.41 | 0.41 | [0.26 0.71] |  | 0.44 | 0.43 | 0.44 | [0.15 0.82] |
| USC |  | 0.41 | 0.41 | 0.41 | [0.32 0.53] |  | 0.45 | 0.44 | 0.43 | [0.3 0.7] |  | 0.43 | 0.41 | 0.42 | [0.17 0.78] |
| WNGC |  | 0.63 | 0.62 | 0.62 | [0.49 0.73] |  | 0.55 | 0.54 | 0.54 | [0.41 0.76] |  | 0.42 | 0.41 | 0.41 | [0.2 0.75] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.47 | 0.01 | [0.47 0.48] | [0.46 0.49] |
| 3 | 0.51 | 0.51 | 0.01 | [0.5 0.51] | [0.49 0.52] |
| 4 | 0.5 | 0.5 | 0.01 | [0.49 0.51] | [0.48 0.53] |
| 5 | 0.48 | 0.48 | 0.01 | [0.47 0.49] | [0.46 0.51] |
| 7.5 | 0.45 | 0.45 | 0.01 | [0.44 0.47] | [0.42 0.48] |
| 10 | 0.42 | 0.42 | 0.01 | [0.41 0.44] | [0.39 0.45] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **SBSM** | **SMCA** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SMCA_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SMCA_downsampled_hist_3s.png) |
| Period-Indep | **STNI** | **USC** | **WNGC** |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WNGC_downsampled_hist_period_indep.png) |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WNGC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/within_event_ss_event_recordings_hist_all_dists.png)


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


### 20.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_20km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.46** | **0.46** | **0.45** | **[0.01 1.16]** |  | **0.42** | **0.42** | **0.41** | **[0.02 1.16]** |  | **0.44** | **0.45** | **0.45** | **[0.02 1.14]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_20km_3s_hist.png) | ![5s](resources/within_event_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 19 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 32 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.44 | 0.44 | 0.05 | [0.38 0.5] | [0.34 0.54] |
| 3 | 0.46 | 0.44 | 0.08 | [0.36 0.53] | [0.26 0.62] |
| 4 | 0.44 | 0.42 | 0.08 | [0.35 0.5] | [0.29 0.58] |
| 5 | 0.42 | 0.42 | 0.08 | [0.35 0.51] | [0.26 0.57] |
| 7.5 | 0.46 | 0.45 | 0.08 | [0.38 0.54] | [0.31 0.6] |
| 10 | 0.44 | 0.45 | 0.07 | [0.37 0.54] | [0.33 0.61] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_20km_downsampled_hist_3s.png) |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_event_recordings_hist_20km.png)


### 50.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.52** | **0.52** | **0.51** | **[0.03 1.35]** |  | **0.5** | **0.49** | **0.48** | **[0.02 1.48]** |  | **0.57** | **0.57** | **0.56** | **[0.03 1.54]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_50km_3s_hist.png) | ![5s](resources/within_event_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 18 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 8 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.53 | 0.51 | 0.06 | [0.45 0.58] | [0.41 0.65] |
| 3 | 0.52 | 0.51 | 0.1 | [0.42 0.62] | [0.31 0.76] |
| 4 | 0.5 | 0.5 | 0.08 | [0.42 0.58] | [0.33 0.68] |
| 5 | 0.5 | 0.49 | 0.09 | [0.39 0.56] | [0.32 0.68] |
| 7.5 | 0.56 | 0.54 | 0.1 | [0.46 0.63] | [0.36 0.81] |
| 10 | 0.57 | 0.55 | 0.09 | [0.45 0.63] | [0.38 0.78] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_50km_downsampled_hist_3s.png) |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_event_recordings_hist_50km.png)


### 100.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.54** | **0.54** | **0.53** | **[0.04 1.44]** |  | **0.54** | **0.54** | **0.52** | **[0.04 1.39]** |  | **0.59** | **0.6** | **0.59** | **[0.03 1.5]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_100km_3s_hist.png) | ![5s](resources/within_event_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 15 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 46 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.56 | 0.55 | 0.08 | [0.48 0.62] | [0.4 0.72] |
| 3 | 0.54 | 0.52 | 0.12 | [0.41 0.64] | [0.31 0.79] |
| 4 | 0.54 | 0.51 | 0.1 | [0.42 0.61] | [0.31 0.74] |
| 5 | 0.54 | 0.54 | 0.11 | [0.43 0.64] | [0.29 0.75] |
| 7.5 | 0.6 | 0.6 | 0.12 | [0.47 0.72] | [0.37 0.84] |
| 10 | 0.59 | 0.61 | 0.11 | [0.46 0.71] | [0.39 0.83] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_100km_downsampled_hist_3s.png) |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_event_recordings_hist_100km.png)


### All Distances M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.51** | **0.51** | **0.49** | **[0.01 1.44]** |  | **0.49** | **0.48** | **0.47** | **[0.02 1.48]** |  | **0.54** | **0.54** | **0.52** | **[0.02 1.54]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_3s_hist.png) | ![5s](resources/within_event_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 87 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 475 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.51 | 0.03 | [0.48 0.54] | [0.45 0.58] |
| 3 | 0.51 | 0.5 | 0.04 | [0.47 0.55] | [0.42 0.6] |
| 4 | 0.49 | 0.48 | 0.04 | [0.45 0.53] | [0.4 0.6] |
| 5 | 0.49 | 0.48 | 0.04 | [0.44 0.52] | [0.39 0.57] |
| 7.5 | 0.54 | 0.54 | 0.04 | [0.5 0.58] | [0.44 0.63] |
| 10 | 0.54 | 0.54 | 0.04 | [0.49 0.57] | [0.45 0.6] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_downsampled_hist_3s.png) |

These plots show the dependence of &phi; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/within_event_event_recordings_hist_all_dists.png)


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


### 20.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.11** | **-2.02** | **[-2.38 -1.82]** | **0.16** | **-2.75** | **[-3.17 -2.38]** | **0.2** | **-4.11** | **[-4.66 -3.64]** |
| PAS | 0.12 | -3.37 | [-3.78 -3.1] | 0.16 | -4.06 | [-4.42 -3.68] | 0.24 | -5.01 | [-5.61 -4.45] |
| SBSM | 0.14 | -1.74 | [-2.26 -1.46] | 0.16 | -2.86 | [-3.32 -2.45] | 0.18 | -4.54 | [-4.98 -4.08] |
| SMCA | 0.11 | -2.07 | [-2.41 -1.86] | 0.17 | -2.64 | [-3.1 -2.27] | 0.21 | -4.06 | [-4.6 -3.53] |
| STNI | 0.11 | -2.02 | [-2.34 -1.82] | 0.17 | -2.57 | [-2.97 -2.2] | 0.24 | -3.56 | [-4.23 -2.93] |
| USC | 0.11 | -2.15 | [-2.49 -1.94] | 0.16 | -2.85 | [-3.26 -2.5] | 0.22 | -4.06 | [-4.63 -3.48] |
| WNGC | 0.12 | -2.15 | [-2.58 -1.92] | 0.17 | -2.88 | [-3.3 -2.52] | 0.21 | -4.21 | [-4.71 -3.66] |

#### 20.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.21 | 0.05 | [0.15 0.26] | [0.12 0.34] |
| 3 | 0.11 | 0.17 | 0.08 | [0.09 0.25] | [0.05 0.32] |
| 4 | 0.13 | 0.2 | 0.08 | [0.11 0.27] | [0.05 0.35] |
| 5 | 0.16 | 0.18 | 0.09 | [0.13 0.28] | [0.08 0.43] |
| 7.5 | 0.18 | 0.22 | 0.1 | [0.12 0.35] | [0.05 0.47] |
| 10 | 0.2 | 0.23 | 0.1 | [0.14 0.36] | [0.07 0.45] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_20km.png)


### 50.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_50km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.11** | **-2.82** | **[-3.17 -2.57]** | **0.17** | **-3.34** | **[-3.76 -2.92]** | **0.2** | **-4.69** | **[-5.18 -4.22]** |
| PAS | 0.11 | -4.27 | [-4.64 -4.05] | 0.16 | -4.78 | [-5.17 -4.38] | 0.23 | -5.62 | [-6.2 -5.03] |
| SBSM | 0.13 | -2.43 | [-2.83 -2.14] | 0.17 | -3.51 | [-3.98 -3.12] | 0.17 | -5.16 | [-5.59 -4.73] |
| SMCA | 0.11 | -2.94 | [-3.29 -2.75] | 0.16 | -3.4 | [-3.8 -2.97] | 0.2 | -4.71 | [-5.23 -4.12] |
| STNI | 0.11 | -2.75 | [-3.08 -2.49] | 0.19 | -2.98 | [-3.38 -2.56] | 0.24 | -4.08 | [-4.65 -3.44] |
| USC | 0.11 | -2.89 | [-3.23 -2.62] | 0.17 | -3.4 | [-3.82 -2.96] | 0.22 | -4.62 | [-5.14 -4.02] |
| WNGC | 0.11 | -3 | [-3.36 -2.77] | 0.18 | -3.46 | [-3.88 -3.02] | 0.21 | -4.77 | [-5.29 -4.14] |

#### 50.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.3 | 0.08 | [0.22 0.39] | [0.17 0.53] |
| 3 | 0.11 | 0.27 | 0.13 | [0.15 0.38] | [0.06 0.65] |
| 4 | 0.14 | 0.27 | 0.11 | [0.17 0.38] | [0.1 0.58] |
| 5 | 0.17 | 0.3 | 0.13 | [0.16 0.42] | [0.08 0.58] |
| 7.5 | 0.19 | 0.32 | 0.14 | [0.18 0.47] | [0.09 0.64] |
| 10 | 0.2 | 0.29 | 0.14 | [0.2 0.49] | [0.12 0.66] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_50km.png)


### 100.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_100km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.11** | **-3.45** | **[-3.81 -3.17]** | **0.17** | **-3.89** | **[-4.29 -3.48]** | **0.2** | **-5.17** | **[-5.69 -4.73]** |
| PAS | 0.11 | -4.83 | [-5.2 -4.6] | 0.15 | -5.32 | [-5.68 -4.95] | 0.24 | -6.07 | [-6.7 -5.56] |
| SBSM | 0.13 | -3.1 | [-3.51 -2.79] | 0.16 | -4.09 | [-4.54 -3.69] | 0.18 | -5.67 | [-6.08 -5.27] |
| SMCA | 0.11 | -3.62 | [-3.96 -3.4] | 0.17 | -3.9 | [-4.3 -3.5] | 0.21 | -5.19 | [-5.75 -4.68] |
| STNI | 0.11 | -3.36 | [-3.72 -3.08] | 0.18 | -3.56 | [-3.97 -3.09] | 0.24 | -4.55 | [-5.18 -3.98] |
| USC | 0.11 | -3.53 | [-3.89 -3.24] | 0.17 | -3.95 | [-4.36 -3.53] | 0.22 | -5.1 | [-5.67 -4.58] |
| WNGC | 0.11 | -3.59 | [-3.96 -3.32] | 0.17 | -4.02 | [-4.39 -3.63] | 0.22 | -5.24 | [-5.79 -4.78] |

#### 100.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.22 | 0.08 | [0.16 0.33] | [0.1 0.39] |
| 3 | 0.11 | 0.2 | 0.11 | [0.08 0.32] | [0.03 0.44] |
| 4 | 0.14 | 0.21 | 0.11 | [0.1 0.35] | [0.05 0.45] |
| 5 | 0.17 | 0.24 | 0.11 | [0.13 0.37] | [0.04 0.48] |
| 7.5 | 0.2 | 0.24 | 0.14 | [0.12 0.38] | [0.03 0.62] |
| 10 | 0.2 | 0.23 | 0.14 | [0.09 0.37] | [0.02 0.55] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_100km.png)


### All Distances M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** | **0.11** | **-2.76** | **[-3.81 -1.82]** | **0.17** | **-3.33** | **[-4.29 -2.38]** | **0.2** | **-4.66** | **[-5.69 -3.64]** |
| PAS | 0.11 | -4.16 | [-5.2 -3.1] | 0.16 | -4.72 | [-5.68 -3.68] | 0.24 | -5.57 | [-6.7 -4.45] |
| SBSM | 0.13 | -2.42 | [-3.51 -1.46] | 0.17 | -3.49 | [-4.54 -2.45] | 0.18 | -5.12 | [-6.08 -4.08] |
| SMCA | 0.11 | -2.88 | [-3.96 -1.86] | 0.17 | -3.31 | [-4.3 -2.27] | 0.21 | -4.65 | [-5.75 -3.53] |
| STNI | 0.11 | -2.71 | [-3.72 -1.82] | 0.18 | -3.04 | [-3.97 -2.2] | 0.24 | -4.06 | [-5.18 -2.93] |
| USC | 0.11 | -2.86 | [-3.89 -1.94] | 0.17 | -3.4 | [-4.36 -2.5] | 0.22 | -4.59 | [-5.67 -3.48] |
| WNGC | 0.12 | -2.91 | [-3.96 -1.92] | 0.17 | -3.45 | [-4.39 -2.52] | 0.21 | -4.74 | [-5.79 -3.66] |

#### All Distances M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.2 | 0.02 | [0.17 0.22] | [0.16 0.24] |
| 3 | 0.11 | 0.16 | 0.03 | [0.12 0.19] | [0.1 0.24] |
| 4 | 0.14 | 0.18 | 0.03 | [0.15 0.21] | [0.12 0.24] |
| 5 | 0.17 | 0.2 | 0.03 | [0.17 0.24] | [0.13 0.27] |
| 7.5 | 0.19 | 0.22 | 0.04 | [0.18 0.26] | [0.14 0.3] |
| 10 | 0.2 | 0.22 | 0.04 | [0.18 0.27] | [0.15 0.31] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3888), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/between_events_event_recordings_hist_all_dists.png)


## Azumth Dependence
*[(top)](#table-of-contents)*

### PAS Azumth Dependence
*[(top)](#table-of-contents)*

#### PAS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&phi;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
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

