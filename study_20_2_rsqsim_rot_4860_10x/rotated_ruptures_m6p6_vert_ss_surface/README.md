# rundir4860_multi_combine Rotated Rupture Variability, M6.6 SS

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M6.6, Vertical Strike-Slip with Surface Rupture). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

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
* [M6.6 SS Rupture Match Criteria](#m66-ss-rupture-match-criteria)
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
  * [BBP PartB, M6.6, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m66-vertical-strike-slip-with-surface-rupture)
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

## M6.6 SS Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 50 events which match the following criteria:

* M=[6.55,6.65]
* Ztor=[0.0,1.0]
* Rake=[-180,-170] or [-10,10] or [170,180]
* Dip=90.0
* Linear rupture (max 0.5km deviation from ideal)

In the case of more than 50 available matches, we use the Sect Variability filter method: Minimizes parent fault section duplication

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| Hunting Creek - Bartlett Springs connector 2011 | 1 |
| Earthquake Valley (So Extension) | 1 |
| San Jacinto (Superstition Mtn) | 1 |
| San Diego Trough south | 1 |
| Emerson-Copper Mtn 2011 | 1 |
| Gravel Hills-Harper Lk | 1 |
| Rose Canyon | 1 |
| Honey Lake 2011 CFM | 1 |
| Brawley (Seismic Zone) alt 1 | 1 |
| San Andreas (Cholame) rev | 1 |
| Goldstone Lake | 1 |
| Owl Lake | 1 |
| Pinto Mtn | 1 |
| Coyote Lake | 1 |
| San Gregorio (North) 2011 CFM | 1 |
| San Andreas (San Bernardino S) | 1 |
| San Jacinto (Coyote Creek) | 1 |
| Coronado Bank alt1 | 1 |
| Death Valley (So) | 1 |
| Earthquake Valley | 1 |
| San Jacinto (San Bernardino) | 1 |
| Garlock (East) | 1 |
| Ortigalita (South) | 1 |
| Ludlow | 1 |
| Hunting Creek - Berryessa 2011 CFM | 1 |
| Newport-Inglewood (Offshore) | 1 |
| San Andreas (San Bernardino N) | 1 |
| Owens Valley | 1 |
| Johnson Valley (No) 2011 rev | 1 |
| Concord 2011 CFM | 1 |
| Garlock (West) | 1 |
| Laguna Salada | 1 |
| Superstition Hills | 1 |
| Garberville - Briceland 2011 CFM | 1 |
| San Andreas (Parkfield) | 1 |
| Homestead Valley 2011 | 1 |
| San Andreas (Coachella) rev | 1 |
| San Jacinto (Clark) rev | 1 |
| Garlock (Central) | 1 |
| San Andreas (Creeping Section) 2011 CFM | 1 |
| Calico-Hidalgo | 1 |
| Mendocino | 1 |
| Ash Hill | 1 |
| Death Valley (No) | 1 |
| Palos Verdes | 1 |
| Elmore Ranch | 1 |
| Bartlett Springs 2011 CFM | 1 |
| Ortigalita (North) | 1 |
| Little Lake | 1 |
| Eureka Peak | 1 |
| Cerro Prieto | 1 |
| San Andreas (Offshore) 2011 CFM | 1 |
| TOTAL # PARENTS | 52 |

Actual magnitude range: [6.5510917,6.6451483], average: 6.5999436, stdDev: 0.028095247

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
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.29 | 0.34 | 0.33 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.35 | 0.41 | 0.38 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.4 | 0.46 | 0.43 | 0.28 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.35 | 0.41 | 0.38 | 0.23 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.39 | 0.36 | 0.43 | 0.34 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.45 | 0.37 | 0.45 | 0.48 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.46 | 0.38 | 0.47 | 0.48 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.43 | 0.37 | 0.45 | 0.44 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.43 | 0.44 | 0.48 | 0.34 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.51 | 0.49 | 0.52 | 0.5 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.55 | 0.54 | 0.57 | 0.51 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.5 | 0.49 | 0.53 | 0.46 |
| Within-event | &phi; | 20 km | 0.55 | 0.51 | 0.57 | 0.52 |
| Within-event | &phi; | 50 km | 0.64 | 0.57 | 0.66 | 0.65 |
| Within-event | &phi; | 100 km | 0.69 | 0.62 | 0.72 | 0.67 |
| Within-event | &phi; | (all) | 0.63 | 0.57 | 0.65 | 0.62 |
| Between-events | &tau; | 20 km | 0.21 | 0.17 | 0.22 | 0.24 |
| Between-events | &tau; | 50 km | 0.22 | 0.17 | 0.24 | 0.24 |
| Between-events | &tau; | 100 km | 0.22 | 0.16 | 0.23 | 0.25 |
| Between-events | &tau; | (all) | 0.22 | 0.17 | 0.23 | 0.25 |

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
| **ALL SITES** |  | **0.34** | **0.32** | **0.3** | **[0.09 0.94]** |  | **0.33** | **0.31** | **0.29** | **[0.04 0.87]** |  | **0.15** | **0.14** | **0.13** | **[0.03 0.59]** |
| LAF |  | 0.34 | 0.33 | 0.33 | [0.11 0.62] |  | 0.38 | 0.37 | 0.36 | [0.07 0.65] |  | 0.16 | 0.15 | 0.14 | [0.05 0.36] |
| OSI |  | 0.25 | 0.24 | 0.24 | [0.09 0.49] |  | 0.19 | 0.18 | 0.17 | [0.06 0.42] |  | 0.1 | 0.09 | 0.08 | [0.03 0.26] |
| PDE |  | 0.3 | 0.3 | 0.29 | [0.09 0.48] |  | 0.29 | 0.28 | 0.28 | [0.08 0.51] |  | 0.13 | 0.13 | 0.12 | [0.04 0.34] |
| SBSM |  | 0.28 | 0.27 | 0.26 | [0.11 0.52] |  | 0.2 | 0.19 | 0.18 | [0.04 0.52] |  | 0.11 | 0.11 | 0.1 | [0.03 0.3] |
| SMCA |  | 0.34 | 0.34 | 0.32 | [0.13 0.66] |  | 0.37 | 0.36 | 0.35 | [0.1 0.64] |  | 0.17 | 0.16 | 0.15 | [0.05 0.44] |
| STNI |  | 0.26 | 0.26 | 0.26 | [0.12 0.46] |  | 0.3 | 0.29 | 0.29 | [0.07 0.57] |  | 0.13 | 0.12 | 0.12 | [0.04 0.3] |
| USC |  | 0.34 | 0.33 | 0.32 | [0.14 0.58] |  | 0.38 | 0.37 | 0.37 | [0.11 0.63] |  | 0.17 | 0.16 | 0.16 | [0.06 0.36] |
| WNGC |  | 0.57 | 0.56 | 0.55 | [0.14 0.94] |  | 0.51 | 0.5 | 0.5 | [0.09 0.87] |  | 0.2 | 0.19 | 0.18 | [0.04 0.59] |
| WSS |  | 0.36 | 0.36 | 0.35 | [0.1 0.61] |  | 0.29 | 0.28 | 0.28 | [0.08 0.51] |  | 0.12 | 0.12 | 0.11 | [0.04 0.49] |
| s022 |  | 0.26 | 0.26 | 0.25 | [0.1 0.46] |  | 0.26 | 0.26 | 0.25 | [0.07 0.45] |  | 0.19 | 0.19 | 0.18 | [0.06 0.35] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_20km_3s_hist.png) | ![5s](resources/path_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.29 | 0.28 | 0.01 | [0.27 0.3] | [0.26 0.31] |
| 3 | 0.34 | 0.33 | 0.02 | [0.32 0.36] | [0.3 0.38] |
| 4 | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.29 0.37] |
| 5 | 0.33 | 0.32 | 0.02 | [0.3 0.34] | [0.28 0.36] |
| 7.5 | 0.24 | 0.23 | 0.02 | [0.22 0.25] | [0.2 0.27] |
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
| **ALL SITES** |  | **0.41** | **0.4** | **0.37** | **[0.14 1]** |  | **0.38** | **0.37** | **0.36** | **[0.12 0.76]** |  | **0.24** | **0.23** | **0.22** | **[0.07 0.65]** |
| LAF |  | 0.36 | 0.36 | 0.36 | [0.19 0.6] |  | 0.35 | 0.35 | 0.35 | [0.15 0.64] |  | 0.26 | 0.24 | 0.23 | [0.1 0.47] |
| OSI |  | 0.35 | 0.35 | 0.34 | [0.15 0.62] |  | 0.31 | 0.3 | 0.3 | [0.15 0.54] |  | 0.2 | 0.2 | 0.2 | [0.07 0.38] |
| PDE |  | 0.38 | 0.37 | 0.37 | [0.19 0.64] |  | 0.33 | 0.33 | 0.32 | [0.14 0.59] |  | 0.24 | 0.22 | 0.22 | [0.07 0.5] |
| SBSM |  | 0.5 | 0.49 | 0.49 | [0.19 0.82] |  | 0.38 | 0.37 | 0.37 | [0.13 0.67] |  | 0.2 | 0.19 | 0.18 | [0.07 0.44] |
| SMCA |  | 0.47 | 0.47 | 0.47 | [0.21 0.77] |  | 0.41 | 0.41 | 0.39 | [0.17 0.76] |  | 0.27 | 0.26 | 0.25 | [0.09 0.5] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.14 0.51] |  | 0.37 | 0.37 | 0.37 | [0.14 0.58] |  | 0.23 | 0.22 | 0.21 | [0.08 0.45] |
| USC |  | 0.35 | 0.35 | 0.35 | [0.2 0.63] |  | 0.38 | 0.37 | 0.37 | [0.15 0.61] |  | 0.26 | 0.25 | 0.24 | [0.09 0.5] |
| WNGC |  | 0.59 | 0.58 | 0.58 | [0.23 1] |  | 0.47 | 0.46 | 0.45 | [0.17 0.76] |  | 0.25 | 0.24 | 0.23 | [0.07 0.49] |
| WSS |  | 0.38 | 0.38 | 0.38 | [0.21 0.61] |  | 0.41 | 0.4 | 0.4 | [0.19 0.7] |  | 0.21 | 0.21 | 0.21 | [0.08 0.39] |
| s022 |  | 0.27 | 0.27 | 0.27 | [0.14 0.42] |  | 0.32 | 0.32 | 0.31 | [0.12 0.59] |  | 0.26 | 0.25 | 0.23 | [0.09 0.65] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_50km_3s_hist.png) | ![5s](resources/path_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 33 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.35 | 0.35 | 0.01 | [0.33 0.36] | [0.32 0.38] |
| 3 | 0.41 | 0.4 | 0.02 | [0.38 0.43] | [0.36 0.46] |
| 4 | 0.39 | 0.38 | 0.02 | [0.37 0.41] | [0.34 0.43] |
| 5 | 0.38 | 0.37 | 0.02 | [0.35 0.39] | [0.33 0.41] |
| 7.5 | 0.32 | 0.32 | 0.02 | [0.31 0.34] | [0.29 0.36] |
| 10 | 0.24 | 0.24 | 0.02 | [0.22 0.26] | [0.2 0.27] |

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
| **ALL SITES** |  | **0.46** | **0.45** | **0.42** | **[0.19 1.01]** |  | **0.43** | **0.43** | **0.42** | **[0.15 0.81]** |  | **0.28** | **0.28** | **0.28** | **[0.09 0.56]** |
| LAF |  | 0.42 | 0.42 | 0.42 | [0.24 0.65] |  | 0.39 | 0.39 | 0.39 | [0.21 0.58] |  | 0.29 | 0.29 | 0.29 | [0.12 0.45] |
| OSI |  | 0.41 | 0.41 | 0.4 | [0.22 0.64] |  | 0.38 | 0.38 | 0.38 | [0.17 0.61] |  | 0.28 | 0.27 | 0.27 | [0.1 0.56] |
| PDE |  | 0.36 | 0.36 | 0.36 | [0.19 0.61] |  | 0.38 | 0.37 | 0.37 | [0.15 0.65] |  | 0.29 | 0.29 | 0.28 | [0.11 0.47] |
| SBSM |  | 0.6 | 0.6 | 0.6 | [0.29 0.91] |  | 0.48 | 0.47 | 0.47 | [0.22 0.78] |  | 0.25 | 0.25 | 0.24 | [0.09 0.54] |
| SMCA |  | 0.53 | 0.53 | 0.52 | [0.35 0.76] |  | 0.42 | 0.42 | 0.42 | [0.24 0.63] |  | 0.33 | 0.33 | 0.33 | [0.19 0.48] |
| STNI |  | 0.34 | 0.34 | 0.34 | [0.2 0.5] |  | 0.39 | 0.39 | 0.39 | [0.16 0.58] |  | 0.25 | 0.24 | 0.24 | [0.09 0.44] |
| USC |  | 0.41 | 0.42 | 0.41 | [0.26 0.61] |  | 0.43 | 0.44 | 0.43 | [0.23 0.65] |  | 0.3 | 0.3 | 0.31 | [0.15 0.45] |
| WNGC |  | 0.63 | 0.63 | 0.62 | [0.28 1.01] |  | 0.53 | 0.52 | 0.53 | [0.25 0.81] |  | 0.25 | 0.25 | 0.24 | [0.1 0.43] |
| WSS |  | 0.4 | 0.4 | 0.4 | [0.22 0.69] |  | 0.45 | 0.45 | 0.44 | [0.22 0.74] |  | 0.28 | 0.27 | 0.27 | [0.15 0.46] |
| s022 |  | 0.35 | 0.36 | 0.35 | [0.2 0.58] |  | 0.4 | 0.4 | 0.4 | [0.19 0.61] |  | 0.28 | 0.28 | 0.28 | [0.16 0.44] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_100km_3s_hist.png) | ![5s](resources/path_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 29 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 28 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.4 | 0.4 | 0.02 | [0.39 0.42] | [0.37 0.44] |
| 3 | 0.46 | 0.46 | 0.02 | [0.43 0.48] | [0.41 0.5] |
| 4 | 0.45 | 0.45 | 0.02 | [0.42 0.47] | [0.39 0.48] |
| 5 | 0.43 | 0.43 | 0.02 | [0.41 0.45] | [0.38 0.48] |
| 7.5 | 0.38 | 0.38 | 0.02 | [0.36 0.39] | [0.35 0.42] |
| 10 | 0.28 | 0.28 | 0.01 | [0.27 0.29] | [0.25 0.31] |

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
| **ALL SITES** |  | **0.41** | **0.39** | **0.37** | **[0.09 1.01]** |  | **0.38** | **0.37** | **0.37** | **[0.04 0.87]** |  | **0.23** | **0.22** | **0.21** | **[0.03 0.65]** |
| LAF |  | 0.38 | 0.37 | 0.37 | [0.11 0.65] |  | 0.37 | 0.37 | 0.37 | [0.07 0.65] |  | 0.24 | 0.23 | 0.22 | [0.05 0.47] |
| OSI |  | 0.34 | 0.33 | 0.33 | [0.09 0.64] |  | 0.3 | 0.29 | 0.29 | [0.06 0.61] |  | 0.21 | 0.19 | 0.19 | [0.03 0.56] |
| PDE |  | 0.35 | 0.35 | 0.34 | [0.09 0.64] |  | 0.34 | 0.33 | 0.32 | [0.08 0.65] |  | 0.23 | 0.21 | 0.21 | [0.04 0.5] |
| SBSM |  | 0.48 | 0.46 | 0.47 | [0.11 0.91] |  | 0.37 | 0.35 | 0.36 | [0.04 0.78] |  | 0.2 | 0.18 | 0.18 | [0.03 0.54] |
| SMCA |  | 0.46 | 0.45 | 0.45 | [0.13 0.77] |  | 0.4 | 0.39 | 0.39 | [0.1 0.76] |  | 0.26 | 0.25 | 0.25 | [0.05 0.5] |
| STNI |  | 0.31 | 0.31 | 0.31 | [0.12 0.51] |  | 0.36 | 0.35 | 0.36 | [0.07 0.58] |  | 0.21 | 0.19 | 0.18 | [0.04 0.45] |
| USC |  | 0.37 | 0.37 | 0.37 | [0.14 0.63] |  | 0.4 | 0.39 | 0.39 | [0.11 0.65] |  | 0.25 | 0.24 | 0.23 | [0.06 0.5] |
| WNGC |  | 0.6 | 0.59 | 0.59 | [0.14 1.01] |  | 0.5 | 0.49 | 0.49 | [0.09 0.87] |  | 0.23 | 0.22 | 0.22 | [0.04 0.59] |
| WSS |  | 0.38 | 0.38 | 0.38 | [0.1 0.69] |  | 0.39 | 0.38 | 0.38 | [0.08 0.74] |  | 0.21 | 0.2 | 0.2 | [0.04 0.49] |
| s022 |  | 0.3 | 0.3 | 0.29 | [0.1 0.58] |  | 0.33 | 0.33 | 0.32 | [0.07 0.61] |  | 0.25 | 0.24 | 0.24 | [0.06 0.65] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_3s_hist.png) | ![5s](resources/path_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 204 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 54 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.35 | 0.35 | 0.01 | [0.35 0.36] | [0.34 0.36] |
| 3 | 0.41 | 0.41 | 0.01 | [0.4 0.41] | [0.39 0.42] |
| 4 | 0.4 | 0.39 | 0.01 | [0.39 0.4] | [0.38 0.41] |
| 5 | 0.38 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.4] |
| 7.5 | 0.32 | 0.32 | 0.01 | [0.31 0.32] | [0.31 0.33] |
| 10 | 0.23 | 0.23 | 0.01 | [0.22 0.24] | [0.22 0.24] |

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
| **ALL SITES** |  | **0.36** | **0.35** | **0.34** | **[0.09 0.88]** |  | **0.43** | **0.42** | **0.41** | **[0.11 0.79]** |  | **0.34** | **0.32** | **0.31** | **[0.06 0.75]** |
| LAF |  | 0.35 | 0.33 | 0.32 | [0.1 0.71] |  | 0.43 | 0.42 | 0.41 | [0.13 0.79] |  | 0.36 | 0.35 | 0.34 | [0.1 0.71] |
| OSI |  | 0.38 | 0.37 | 0.36 | [0.17 0.74] |  | 0.4 | 0.39 | 0.4 | [0.14 0.66] |  | 0.28 | 0.26 | 0.26 | [0.06 0.56] |
| PDE |  | 0.34 | 0.33 | 0.32 | [0.13 0.75] |  | 0.44 | 0.43 | 0.42 | [0.18 0.77] |  | 0.32 | 0.31 | 0.3 | [0.08 0.61] |
| SBSM |  | 0.43 | 0.42 | 0.4 | [0.18 0.88] |  | 0.45 | 0.44 | 0.43 | [0.18 0.78] |  | 0.3 | 0.29 | 0.28 | [0.07 0.56] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.15 0.7] |  | 0.44 | 0.43 | 0.42 | [0.19 0.76] |  | 0.34 | 0.33 | 0.33 | [0.1 0.66] |
| STNI |  | 0.35 | 0.34 | 0.33 | [0.15 0.66] |  | 0.42 | 0.41 | 0.4 | [0.17 0.74] |  | 0.37 | 0.35 | 0.34 | [0.12 0.75] |
| USC |  | 0.36 | 0.35 | 0.34 | [0.11 0.74] |  | 0.43 | 0.42 | 0.42 | [0.16 0.74] |  | 0.35 | 0.34 | 0.33 | [0.1 0.7] |
| WNGC |  | 0.38 | 0.36 | 0.35 | [0.14 0.76] |  | 0.44 | 0.43 | 0.42 | [0.13 0.78] |  | 0.34 | 0.33 | 0.32 | [0.09 0.65] |
| WSS |  | 0.36 | 0.35 | 0.34 | [0.13 0.69] |  | 0.43 | 0.42 | 0.41 | [0.16 0.76] |  | 0.32 | 0.31 | 0.3 | [0.09 0.57] |
| s022 |  | 0.31 | 0.3 | 0.29 | [0.09 0.64] |  | 0.39 | 0.37 | 0.36 | [0.11 0.71] |  | 0.35 | 0.33 | 0.32 | [0.1 0.63] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_20km_3s_hist.png) | ![5s](resources/source_strike_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.39 | 0.38 | 0.02 | [0.37 0.4] | [0.35 0.42] |
| 3 | 0.36 | 0.36 | 0.02 | [0.34 0.38] | [0.32 0.4] |
| 4 | 0.4 | 0.4 | 0.02 | [0.37 0.42] | [0.35 0.44] |
| 5 | 0.43 | 0.42 | 0.02 | [0.4 0.45] | [0.37 0.46] |
| 7.5 | 0.41 | 0.4 | 0.02 | [0.38 0.43] | [0.36 0.45] |
| 10 | 0.34 | 0.33 | 0.02 | [0.31 0.35] | [0.29 0.38] |

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
| **ALL SITES** |  | **0.37** | **0.35** | **0.34** | **[0.08 1]** |  | **0.45** | **0.43** | **0.42** | **[0.09 0.9]** |  | **0.48** | **0.48** | **0.49** | **[0.09 0.78]** |
| LAF |  | 0.34 | 0.32 | 0.31 | [0.08 0.73] |  | 0.45 | 0.44 | 0.42 | [0.13 0.9] |  | 0.5 | 0.5 | 0.51 | [0.14 0.77] |
| OSI |  | 0.37 | 0.36 | 0.36 | [0.1 0.78] |  | 0.41 | 0.39 | 0.39 | [0.13 0.76] |  | 0.46 | 0.46 | 0.47 | [0.15 0.67] |
| PDE |  | 0.38 | 0.36 | 0.35 | [0.13 1] |  | 0.47 | 0.46 | 0.45 | [0.12 0.84] |  | 0.51 | 0.51 | 0.52 | [0.13 0.77] |
| SBSM |  | 0.46 | 0.45 | 0.44 | [0.15 0.85] |  | 0.49 | 0.48 | 0.46 | [0.18 0.89] |  | 0.47 | 0.47 | 0.47 | [0.21 0.69] |
| SMCA |  | 0.38 | 0.36 | 0.35 | [0.09 0.83] |  | 0.45 | 0.44 | 0.42 | [0.12 0.88] |  | 0.49 | 0.48 | 0.5 | [0.09 0.78] |
| STNI |  | 0.31 | 0.3 | 0.28 | [0.1 0.67] |  | 0.42 | 0.4 | 0.38 | [0.09 0.8] |  | 0.51 | 0.51 | 0.52 | [0.21 0.75] |
| USC |  | 0.35 | 0.33 | 0.32 | [0.09 0.82] |  | 0.43 | 0.41 | 0.4 | [0.09 0.85] |  | 0.49 | 0.48 | 0.5 | [0.12 0.73] |
| WNGC |  | 0.37 | 0.35 | 0.32 | [0.1 0.89] |  | 0.46 | 0.44 | 0.44 | [0.12 0.88] |  | 0.49 | 0.49 | 0.5 | [0.13 0.74] |
| WSS |  | 0.35 | 0.34 | 0.32 | [0.1 0.72] |  | 0.43 | 0.42 | 0.4 | [0.1 0.83] |  | 0.46 | 0.46 | 0.47 | [0.15 0.74] |
| s022 |  | 0.35 | 0.34 | 0.32 | [0.11 0.77] |  | 0.45 | 0.43 | 0.42 | [0.11 0.9] |  | 0.45 | 0.43 | 0.45 | [0.09 0.73] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_50km_3s_hist.png) | ![5s](resources/source_strike_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 33 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.45 | 0.44 | 0.02 | [0.42 0.47] | [0.4 0.49] |
| 3 | 0.37 | 0.36 | 0.03 | [0.34 0.39] | [0.32 0.42] |
| 4 | 0.41 | 0.41 | 0.03 | [0.38 0.44] | [0.35 0.48] |
| 5 | 0.45 | 0.44 | 0.03 | [0.42 0.48] | [0.39 0.52] |
| 7.5 | 0.51 | 0.51 | 0.03 | [0.47 0.53] | [0.45 0.56] |
| 10 | 0.48 | 0.48 | 0.02 | [0.46 0.5] | [0.44 0.52] |

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
| **ALL SITES** |  | **0.38** | **0.36** | **0.35** | **[0.08 0.9]** |  | **0.47** | **0.46** | **0.45** | **[0.11 1]** |  | **0.48** | **0.47** | **0.48** | **[0.07 0.86]** |
| LAF |  | 0.35 | 0.33 | 0.31 | [0.09 0.78] |  | 0.47 | 0.45 | 0.44 | [0.12 0.85] |  | 0.5 | 0.49 | 0.49 | [0.12 0.8] |
| OSI |  | 0.38 | 0.37 | 0.37 | [0.13 0.75] |  | 0.44 | 0.43 | 0.43 | [0.12 0.9] |  | 0.45 | 0.44 | 0.45 | [0.1 0.76] |
| PDE |  | 0.38 | 0.37 | 0.36 | [0.12 0.88] |  | 0.48 | 0.46 | 0.45 | [0.11 0.96] |  | 0.47 | 0.46 | 0.47 | [0.14 0.81] |
| SBSM |  | 0.46 | 0.45 | 0.44 | [0.14 0.9] |  | 0.52 | 0.51 | 0.51 | [0.12 1] |  | 0.48 | 0.47 | 0.48 | [0.16 0.81] |
| SMCA |  | 0.37 | 0.36 | 0.34 | [0.11 0.84] |  | 0.44 | 0.43 | 0.42 | [0.12 0.79] |  | 0.46 | 0.45 | 0.47 | [0.07 0.78] |
| STNI |  | 0.34 | 0.32 | 0.31 | [0.11 0.74] |  | 0.47 | 0.45 | 0.44 | [0.15 0.85] |  | 0.53 | 0.53 | 0.53 | [0.15 0.85] |
| USC |  | 0.36 | 0.34 | 0.33 | [0.1 0.79] |  | 0.47 | 0.45 | 0.44 | [0.12 0.88] |  | 0.49 | 0.48 | 0.49 | [0.14 0.81] |
| WNGC |  | 0.39 | 0.37 | 0.35 | [0.1 0.86] |  | 0.49 | 0.47 | 0.46 | [0.13 0.95] |  | 0.49 | 0.49 | 0.49 | [0.17 0.78] |
| WSS |  | 0.36 | 0.35 | 0.34 | [0.08 0.85] |  | 0.46 | 0.44 | 0.44 | [0.11 0.87] |  | 0.45 | 0.44 | 0.45 | [0.09 0.8] |
| s022 |  | 0.37 | 0.35 | 0.35 | [0.08 0.79] |  | 0.48 | 0.46 | 0.46 | [0.15 0.86] |  | 0.48 | 0.48 | 0.47 | [0.18 0.86] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_100km_3s_hist.png) | ![5s](resources/source_strike_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 29 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 28 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.46 | 0.46 | 0.02 | [0.44 0.49] | [0.41 0.52] |
| 3 | 0.38 | 0.38 | 0.03 | [0.35 0.41] | [0.31 0.44] |
| 4 | 0.43 | 0.43 | 0.04 | [0.4 0.46] | [0.36 0.52] |
| 5 | 0.47 | 0.47 | 0.04 | [0.44 0.52] | [0.4 0.55] |
| 7.5 | 0.52 | 0.53 | 0.03 | [0.49 0.56] | [0.46 0.59] |
| 10 | 0.48 | 0.48 | 0.03 | [0.45 0.51] | [0.43 0.54] |

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
| **ALL SITES** |  | **0.37** | **0.36** | **0.34** | **[0.08 1]** |  | **0.45** | **0.43** | **0.42** | **[0.09 1]** |  | **0.44** | **0.42** | **0.43** | **[0.06 0.86]** |
| LAF |  | 0.34 | 0.33 | 0.31 | [0.08 0.78] |  | 0.45 | 0.43 | 0.42 | [0.12 0.9] |  | 0.46 | 0.44 | 0.45 | [0.1 0.8] |
| OSI |  | 0.38 | 0.37 | 0.36 | [0.1 0.78] |  | 0.42 | 0.41 | 0.4 | [0.12 0.9] |  | 0.41 | 0.39 | 0.41 | [0.06 0.76] |
| PDE |  | 0.37 | 0.36 | 0.34 | [0.12 1] |  | 0.46 | 0.45 | 0.44 | [0.11 0.96] |  | 0.44 | 0.43 | 0.44 | [0.08 0.81] |
| SBSM |  | 0.45 | 0.44 | 0.43 | [0.14 0.9] |  | 0.49 | 0.48 | 0.46 | [0.12 1] |  | 0.42 | 0.41 | 0.42 | [0.07 0.81] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.09 0.84] |  | 0.45 | 0.43 | 0.42 | [0.12 0.88] |  | 0.44 | 0.42 | 0.43 | [0.07 0.78] |
| STNI |  | 0.33 | 0.32 | 0.31 | [0.1 0.74] |  | 0.44 | 0.42 | 0.41 | [0.09 0.85] |  | 0.48 | 0.47 | 0.48 | [0.12 0.85] |
| USC |  | 0.36 | 0.34 | 0.33 | [0.09 0.82] |  | 0.44 | 0.43 | 0.42 | [0.09 0.88] |  | 0.45 | 0.43 | 0.44 | [0.1 0.81] |
| WNGC |  | 0.38 | 0.36 | 0.34 | [0.1 0.89] |  | 0.47 | 0.45 | 0.44 | [0.12 0.95] |  | 0.45 | 0.44 | 0.45 | [0.09 0.78] |
| WSS |  | 0.36 | 0.35 | 0.33 | [0.08 0.85] |  | 0.44 | 0.43 | 0.42 | [0.1 0.87] |  | 0.42 | 0.4 | 0.41 | [0.09 0.8] |
| s022 |  | 0.34 | 0.33 | 0.32 | [0.08 0.79] |  | 0.44 | 0.42 | 0.41 | [0.11 0.9] |  | 0.43 | 0.41 | 0.41 | [0.09 0.86] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m6.6_3s_hist.png) | ![5s](resources/source_strike_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 204 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 54 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.43 | 0.01 | [0.42 0.44] | [0.41 0.45] |
| 3 | 0.37 | 0.37 | 0.01 | [0.36 0.38] | [0.34 0.39] |
| 4 | 0.41 | 0.41 | 0.01 | [0.4 0.42] | [0.39 0.44] |
| 5 | 0.45 | 0.45 | 0.01 | [0.43 0.46] | [0.42 0.47] |
| 7.5 | 0.48 | 0.48 | 0.01 | [0.47 0.49] | [0.46 0.5] |
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
| **ALL SITES** |  | **0.44** | **0.42** | **0.4** | **[0.22 0.8]** |  | **0.48** | **0.47** | **0.46** | **[0.24 0.85]** |  | **0.34** | **0.33** | **0.31** | **[0.11 0.6]** |
| LAF |  | 0.42 | 0.41 | 0.4 | [0.32 0.62] |  | 0.51 | 0.5 | 0.5 | [0.25 0.73] |  | 0.37 | 0.35 | 0.34 | [0.18 0.56] |
| OSI |  | 0.41 | 0.4 | 0.39 | [0.28 0.62] |  | 0.41 | 0.4 | 0.4 | [0.24 0.6] |  | 0.28 | 0.27 | 0.26 | [0.11 0.45] |
| PDE |  | 0.38 | 0.38 | 0.37 | [0.28 0.58] |  | 0.46 | 0.44 | 0.44 | [0.3 0.7] |  | 0.33 | 0.31 | 0.3 | [0.14 0.52] |
| SBSM |  | 0.46 | 0.45 | 0.43 | [0.31 0.74] |  | 0.46 | 0.45 | 0.43 | [0.29 0.68] |  | 0.3 | 0.29 | 0.29 | [0.12 0.5] |
| SMCA |  | 0.42 | 0.42 | 0.41 | [0.32 0.61] |  | 0.49 | 0.48 | 0.48 | [0.29 0.68] |  | 0.35 | 0.34 | 0.33 | [0.17 0.52] |
| STNI |  | 0.38 | 0.37 | 0.36 | [0.24 0.58] |  | 0.45 | 0.44 | 0.44 | [0.28 0.67] |  | 0.37 | 0.35 | 0.33 | [0.17 0.6] |
| USC |  | 0.42 | 0.42 | 0.41 | [0.31 0.6] |  | 0.49 | 0.48 | 0.48 | [0.31 0.7] |  | 0.36 | 0.34 | 0.33 | [0.16 0.55] |
| WNGC |  | 0.62 | 0.61 | 0.6 | [0.46 0.8] |  | 0.62 | 0.61 | 0.62 | [0.32 0.85] |  | 0.37 | 0.36 | 0.34 | [0.15 0.55] |
| WSS |  | 0.45 | 0.45 | 0.44 | [0.34 0.6] |  | 0.47 | 0.47 | 0.46 | [0.32 0.68] |  | 0.33 | 0.31 | 0.31 | [0.14 0.5] |
| s022 |  | 0.33 | 0.33 | 0.32 | [0.22 0.53] |  | 0.41 | 0.4 | 0.39 | [0.25 0.61] |  | 0.36 | 0.34 | 0.32 | [0.18 0.55] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.42 | 0.02 | [0.4 0.44] | [0.39 0.47] |
| 3 | 0.44 | 0.42 | 0.02 | [0.4 0.44] | [0.38 0.47] |
| 4 | 0.46 | 0.45 | 0.03 | [0.42 0.48] | [0.4 0.51] |
| 5 | 0.48 | 0.46 | 0.03 | [0.44 0.49] | [0.42 0.53] |
| 7.5 | 0.44 | 0.42 | 0.02 | [0.4 0.45] | [0.38 0.48] |
| 10 | 0.34 | 0.33 | 0.02 | [0.31 0.35] | [0.29 0.39] |

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
| **ALL SITES** |  | **0.49** | **0.47** | **0.45** | **[0.26 0.78]** |  | **0.52** | **0.51** | **0.5** | **[0.3 0.79]** |  | **0.5** | **0.49** | **0.49** | **[0.24 0.68]** |
| LAF |  | 0.43 | 0.43 | 0.42 | [0.33 0.63] |  | 0.5 | 0.49 | 0.48 | [0.35 0.71] |  | 0.52 | 0.51 | 0.5 | [0.29 0.67] |
| OSI |  | 0.44 | 0.44 | 0.44 | [0.36 0.61] |  | 0.45 | 0.45 | 0.43 | [0.32 0.64] |  | 0.46 | 0.46 | 0.46 | [0.28 0.59] |
| PDE |  | 0.47 | 0.47 | 0.46 | [0.36 0.69] |  | 0.51 | 0.5 | 0.48 | [0.35 0.73] |  | 0.51 | 0.5 | 0.5 | [0.29 0.64] |
| SBSM |  | 0.6 | 0.59 | 0.58 | [0.43 0.78] |  | 0.57 | 0.56 | 0.55 | [0.38 0.79] |  | 0.48 | 0.48 | 0.47 | [0.28 0.64] |
| SMCA |  | 0.54 | 0.54 | 0.53 | [0.44 0.72] |  | 0.54 | 0.54 | 0.53 | [0.41 0.74] |  | 0.51 | 0.5 | 0.5 | [0.28 0.64] |
| STNI |  | 0.4 | 0.39 | 0.39 | [0.31 0.6] |  | 0.49 | 0.48 | 0.48 | [0.3 0.69] |  | 0.52 | 0.52 | 0.5 | [0.3 0.68] |
| USC |  | 0.42 | 0.42 | 0.42 | [0.32 0.63] |  | 0.5 | 0.49 | 0.47 | [0.32 0.7] |  | 0.5 | 0.49 | 0.49 | [0.27 0.65] |
| WNGC |  | 0.64 | 0.64 | 0.64 | [0.47 0.76] |  | 0.58 | 0.58 | 0.56 | [0.42 0.74] |  | 0.5 | 0.5 | 0.49 | [0.3 0.67] |
| WSS |  | 0.45 | 0.44 | 0.44 | [0.35 0.64] |  | 0.53 | 0.52 | 0.51 | [0.38 0.74] |  | 0.47 | 0.47 | 0.46 | [0.26 0.6] |
| s022 |  | 0.39 | 0.38 | 0.36 | [0.26 0.65] |  | 0.49 | 0.47 | 0.46 | [0.3 0.75] |  | 0.47 | 0.46 | 0.45 | [0.24 0.65] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 35 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.5 | 0.02 | [0.48 0.52] | [0.46 0.56] |
| 3 | 0.49 | 0.48 | 0.02 | [0.45 0.5] | [0.43 0.53] |
| 4 | 0.5 | 0.49 | 0.03 | [0.46 0.52] | [0.45 0.56] |
| 5 | 0.52 | 0.5 | 0.03 | [0.48 0.54] | [0.46 0.6] |
| 7.5 | 0.54 | 0.53 | 0.03 | [0.51 0.56] | [0.47 0.59] |
| 10 | 0.5 | 0.49 | 0.03 | [0.46 0.52] | [0.43 0.54] |

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
| **ALL SITES** |  | **0.54** | **0.52** | **0.5** | **[0.31 0.88]** |  | **0.57** | **0.57** | **0.56** | **[0.37 0.87]** |  | **0.51** | **0.5** | **0.5** | **[0.25 0.74]** |
| LAF |  | 0.5 | 0.5 | 0.49 | [0.4 0.68] |  | 0.55 | 0.54 | 0.51 | [0.39 0.78] |  | 0.53 | 0.52 | 0.52 | [0.32 0.71] |
| OSI |  | 0.49 | 0.48 | 0.48 | [0.37 0.67] |  | 0.52 | 0.51 | 0.5 | [0.4 0.71] |  | 0.47 | 0.46 | 0.45 | [0.25 0.68] |
| PDE |  | 0.45 | 0.44 | 0.43 | [0.35 0.67] |  | 0.52 | 0.52 | 0.5 | [0.37 0.76] |  | 0.49 | 0.48 | 0.47 | [0.27 0.69] |
| SBSM |  | 0.68 | 0.68 | 0.66 | [0.54 0.88] |  | 0.64 | 0.63 | 0.63 | [0.46 0.85] |  | 0.51 | 0.5 | 0.5 | [0.32 0.71] |
| SMCA |  | 0.6 | 0.6 | 0.58 | [0.49 0.77] |  | 0.55 | 0.55 | 0.53 | [0.42 0.75] |  | 0.51 | 0.51 | 0.51 | [0.33 0.68] |
| STNI |  | 0.43 | 0.43 | 0.41 | [0.31 0.63] |  | 0.56 | 0.55 | 0.53 | [0.37 0.78] |  | 0.55 | 0.55 | 0.54 | [0.34 0.74] |
| USC |  | 0.5 | 0.49 | 0.48 | [0.41 0.7] |  | 0.58 | 0.57 | 0.56 | [0.4 0.81] |  | 0.53 | 0.52 | 0.51 | [0.34 0.71] |
| WNGC |  | 0.69 | 0.68 | 0.68 | [0.54 0.86] |  | 0.65 | 0.65 | 0.65 | [0.49 0.87] |  | 0.51 | 0.5 | 0.51 | [0.3 0.69] |
| WSS |  | 0.48 | 0.48 | 0.46 | [0.38 0.71] |  | 0.6 | 0.59 | 0.59 | [0.48 0.79] |  | 0.48 | 0.48 | 0.47 | [0.29 0.65] |
| s022 |  | 0.46 | 0.46 | 0.45 | [0.35 0.69] |  | 0.56 | 0.55 | 0.53 | [0.41 0.77] |  | 0.52 | 0.51 | 0.49 | [0.35 0.72] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 57 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.55 | 0.55 | 0.02 | [0.53 0.57] | [0.51 0.6] |
| 3 | 0.54 | 0.53 | 0.03 | [0.51 0.55] | [0.49 0.6] |
| 4 | 0.56 | 0.55 | 0.03 | [0.53 0.58] | [0.5 0.61] |
| 5 | 0.57 | 0.57 | 0.03 | [0.54 0.6] | [0.52 0.64] |
| 7.5 | 0.58 | 0.57 | 0.03 | [0.55 0.61] | [0.52 0.64] |
| 10 | 0.51 | 0.51 | 0.03 | [0.48 0.54] | [0.46 0.58] |

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
| **ALL SITES** |  | **0.49** | **0.47** | **0.45** | **[0.22 0.88]** |  | **0.53** | **0.51** | **0.5** | **[0.24 0.87]** |  | **0.46** | **0.44** | **0.45** | **[0.11 0.74]** |
| LAF |  | 0.45 | 0.45 | 0.44 | [0.32 0.68] |  | 0.52 | 0.51 | 0.5 | [0.25 0.78] |  | 0.48 | 0.46 | 0.48 | [0.18 0.71] |
| OSI |  | 0.45 | 0.44 | 0.44 | [0.28 0.67] |  | 0.46 | 0.45 | 0.45 | [0.24 0.71] |  | 0.41 | 0.39 | 0.42 | [0.11 0.68] |
| PDE |  | 0.44 | 0.43 | 0.42 | [0.28 0.69] |  | 0.5 | 0.49 | 0.47 | [0.3 0.76] |  | 0.45 | 0.43 | 0.45 | [0.14 0.69] |
| SBSM |  | 0.59 | 0.57 | 0.59 | [0.31 0.88] |  | 0.56 | 0.55 | 0.55 | [0.29 0.85] |  | 0.44 | 0.42 | 0.45 | [0.12 0.71] |
| SMCA |  | 0.53 | 0.52 | 0.53 | [0.32 0.77] |  | 0.53 | 0.52 | 0.51 | [0.29 0.75] |  | 0.46 | 0.45 | 0.46 | [0.17 0.68] |
| STNI |  | 0.4 | 0.4 | 0.39 | [0.24 0.63] |  | 0.5 | 0.49 | 0.48 | [0.28 0.78] |  | 0.49 | 0.47 | 0.49 | [0.17 0.74] |
| USC |  | 0.45 | 0.44 | 0.43 | [0.31 0.7] |  | 0.52 | 0.52 | 0.5 | [0.31 0.81] |  | 0.47 | 0.45 | 0.46 | [0.16 0.71] |
| WNGC |  | 0.65 | 0.64 | 0.64 | [0.46 0.86] |  | 0.62 | 0.61 | 0.61 | [0.32 0.87] |  | 0.47 | 0.45 | 0.46 | [0.15 0.69] |
| WSS |  | 0.46 | 0.46 | 0.45 | [0.34 0.71] |  | 0.53 | 0.52 | 0.51 | [0.32 0.79] |  | 0.43 | 0.42 | 0.44 | [0.14 0.65] |
| s022 |  | 0.4 | 0.39 | 0.38 | [0.22 0.69] |  | 0.49 | 0.47 | 0.47 | [0.25 0.77] |  | 0.45 | 0.44 | 0.44 | [0.18 0.72] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 774 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.5 | 0.5 | 0.01 | [0.49 0.51] | [0.48 0.52] |
| 3 | 0.49 | 0.49 | 0.01 | [0.48 0.5] | [0.47 0.51] |
| 4 | 0.51 | 0.51 | 0.01 | [0.49 0.52] | [0.48 0.53] |
| 5 | 0.53 | 0.52 | 0.01 | [0.51 0.53] | [0.5 0.55] |
| 7.5 | 0.52 | 0.52 | 0.02 | [0.51 0.53] | [0.49 0.55] |
| 10 | 0.46 | 0.46 | 0.01 | [0.44 0.47] | [0.43 0.48] |

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
| **10 sites, V<sub>S30</sub>=500** |  | **0.51** | **0.52** | **0.51** | **[0.13 1.08]** |  | **0.57** | **0.58** | **0.57** | **[0.14 1.18]** |  | **0.52** | **0.53** | **0.52** | **[0.21 1.05]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 31 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 6 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.55 | 0.55 | 0.06 | [0.48 0.61] | [0.41 0.66] |
| 3 | 0.51 | 0.51 | 0.07 | [0.43 0.59] | [0.37 0.66] |
| 4 | 0.56 | 0.58 | 0.08 | [0.47 0.65] | [0.43 0.72] |
| 5 | 0.57 | 0.58 | 0.09 | [0.47 0.67] | [0.4 0.73] |
| 7.5 | 0.57 | 0.56 | 0.07 | [0.48 0.65] | [0.41 0.72] |
| 10 | 0.52 | 0.51 | 0.06 | [0.46 0.57] | [0.39 0.64] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_3s.png) |


### 50.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.57** | **0.57** | **0.57** | **[0.15 1.24]** |  | **0.66** | **0.66** | **0.65** | **[0.2 1.39]** |  | **0.65** | **0.66** | **0.66** | **[0.21 1.16]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 22 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 13 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.64 | 0.64 | 0.09 | [0.56 0.74] | [0.48 0.82] |
| 3 | 0.57 | 0.57 | 0.09 | [0.48 0.67] | [0.41 0.79] |
| 4 | 0.62 | 0.62 | 0.11 | [0.5 0.74] | [0.45 0.86] |
| 5 | 0.66 | 0.67 | 0.11 | [0.55 0.79] | [0.47 0.88] |
| 7.5 | 0.71 | 0.71 | 0.12 | [0.6 0.85] | [0.51 1] |
| 10 | 0.65 | 0.65 | 0.1 | [0.55 0.77] | [0.47 0.87] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_3s.png) |


### 100.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.62** | **0.63** | **0.62** | **[0.14 1.37]** |  | **0.72** | **0.73** | **0.72** | **[0.23 1.48]** |  | **0.67** | **0.68** | **0.67** | **[0.19 1.3]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 20 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 37 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.69 | 0.66 | 0.07 | [0.6 0.75] | [0.55 0.82] |
| 3 | 0.62 | 0.59 | 0.1 | [0.51 0.71] | [0.4 0.84] |
| 4 | 0.68 | 0.64 | 0.1 | [0.57 0.75] | [0.48 0.87] |
| 5 | 0.72 | 0.71 | 0.1 | [0.62 0.82] | [0.52 0.93] |
| 7.5 | 0.75 | 0.73 | 0.1 | [0.63 0.84] | [0.55 0.95] |
| 10 | 0.67 | 0.64 | 0.09 | [0.55 0.75] | [0.49 0.84] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_3s.png) |


### All Distances M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.57** | **0.57** | **0.56** | **[0.13 1.37]** |  | **0.65** | **0.66** | **0.64** | **[0.14 1.48]** |  | **0.62** | **0.62** | **0.61** | **[0.19 1.3]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_3s_hist.png) | ![5s](resources/within_event_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 132 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 126 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.63 | 0.62 | 0.03 | [0.59 0.66] | [0.56 0.69] |
| 3 | 0.57 | 0.56 | 0.04 | [0.53 0.6] | [0.49 0.65] |
| 4 | 0.62 | 0.61 | 0.04 | [0.58 0.65] | [0.53 0.71] |
| 5 | 0.65 | 0.65 | 0.04 | [0.61 0.68] | [0.57 0.72] |
| 7.5 | 0.68 | 0.68 | 0.05 | [0.62 0.71] | [0.58 0.77] |
| 10 | 0.62 | 0.61 | 0.04 | [0.57 0.65] | [0.53 0.69] |

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
| **10 sites, V<sub>S30</sub>=500** | **0.17** | **-2.93** | **[-3.31 -2.64]** | **0.22** | **-3.5** | **[-3.99 -3.17]** | **0.24** | **-4.64** | **[-5.11 -4.12]** |
| LAF | 0.18 | -3.11 | [-3.53 -2.75] | 0.22 | -3.49 | [-4.09 -3.19] | 0.25 | -4.44 | [-4.95 -3.96] |
| OSI | 0.16 | -3.62 | [-3.98 -3.11] | 0.22 | -4.41 | [-4.86 -3.98] | 0.25 | -5.39 | [-5.95 -4.95] |
| PDE | 0.18 | -2.92 | [-3.33 -2.57] | 0.24 | -3.49 | [-4.05 -3.15] | 0.25 | -4.69 | [-5.23 -4.25] |
| SBSM | 0.2 | -2.54 | [-2.97 -2.18] | 0.27 | -3.46 | [-4.11 -3.05] | 0.21 | -4.98 | [-5.46 -4.53] |
| SMCA | 0.16 | -2.81 | [-3.17 -2.51] | 0.24 | -3.22 | [-3.76 -2.82] | 0.26 | -4.44 | [-4.98 -3.94] |
| STNI | 0.18 | -2.77 | [-3.17 -2.46] | 0.2 | -3.23 | [-3.72 -2.97] | 0.27 | -3.92 | [-4.52 -3.46] |
| USC | 0.17 | -2.9 | [-3.27 -2.62] | 0.2 | -3.49 | [-3.96 -3.2] | 0.25 | -4.45 | [-5 -3.99] |
| WNGC | 0.17 | -2.93 | [-3.32 -2.64] | 0.21 | -3.51 | [-4.06 -3.16] | 0.25 | -4.61 | [-5.12 -4.16] |
| WSS | 0.17 | -3.21 | [-3.55 -2.94] | 0.24 | -3.68 | [-4.2 -3.31] | 0.26 | -4.98 | [-5.51 -4.54] |
| s022 | 0.19 | -2.7 | [-3.14 -2.34] | 0.23 | -3.27 | [-3.85 -2.95] | 0.24 | -4.28 | [-4.86 -3.85] |

#### 20.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 37 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.3 | 0.09 | [0.22 0.37] | [0.15 0.51] |
| 3 | 0.17 | 0.26 | 0.11 | [0.16 0.39] | [0.08 0.54] |
| 4 | 0.21 | 0.27 | 0.12 | [0.18 0.4] | [0.06 0.6] |
| 5 | 0.22 | 0.3 | 0.11 | [0.19 0.42] | [0.09 0.56] |
| 7.5 | 0.24 | 0.31 | 0.13 | [0.18 0.46] | [0.11 0.6] |
| 10 | 0.24 | 0.29 | 0.12 | [0.19 0.44] | [0.12 0.6] |

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
| **10 sites, V<sub>S30</sub>=500** | **0.17** | **-3.75** | **[-4.11 -3.45]** | **0.24** | **-4.13** | **[-4.66 -3.78]** | **0.24** | **-5.29** | **[-5.86 -4.73]** |
| LAF | 0.17 | -3.78 | [-4.17 -3.48] | 0.26 | -3.92 | [-4.48 -3.52] | 0.26 | -5.03 | [-5.64 -4.46] |
| OSI | 0.14 | -4.53 | [-4.82 -4.25] | 0.18 | -5.22 | [-5.67 -4.94] | 0.24 | -6.06 | [-6.59 -5.54] |
| PDE | 0.16 | -3.82 | [-4.17 -3.51] | 0.24 | -4.24 | [-4.79 -3.89] | 0.24 | -5.38 | [-5.93 -4.85] |
| SBSM | 0.22 | -3.28 | [-3.7 -2.92] | 0.25 | -4.14 | [-4.67 -3.74] | 0.21 | -5.67 | [-6.21 -5.2] |
| SMCA | 0.16 | -3.75 | [-4.08 -3.44] | 0.22 | -4.05 | [-4.57 -3.7] | 0.24 | -5.17 | [-5.8 -4.65] |
| STNI | 0.17 | -3.52 | [-3.91 -3.15] | 0.28 | -3.62 | [-4.25 -3.19] | 0.28 | -4.52 | [-5.18 -3.9] |
| USC | 0.17 | -3.7 | [-4.08 -3.39] | 0.25 | -4.05 | [-4.64 -3.68] | 0.27 | -5.06 | [-5.69 -4.5] |
| WNGC | 0.16 | -3.8 | [-4.13 -3.5] | 0.25 | -4.08 | [-4.69 -3.69] | 0.26 | -5.24 | [-5.85 -4.66] |
| WSS | 0.16 | -4.02 | [-4.37 -3.69] | 0.21 | -4.49 | [-4.95 -4.15] | 0.22 | -5.74 | [-6.29 -5.25] |
| s022 | 0.17 | -3.46 | [-3.86 -3.13] | 0.23 | -3.84 | [-4.42 -3.49] | 0.26 | -4.72 | [-5.31 -4.2] |

#### 50.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 35 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.22 | 0.31 | 0.13 | [0.21 0.47] | [0.13 0.7] |
| 3 | 0.17 | 0.24 | 0.14 | [0.13 0.4] | [0.07 0.56] |
| 4 | 0.21 | 0.3 | 0.16 | [0.15 0.5] | [0.07 0.61] |
| 5 | 0.24 | 0.32 | 0.17 | [0.19 0.52] | [0.05 0.74] |
| 7.5 | 0.26 | 0.34 | 0.22 | [0.15 0.58] | [0.03 0.88] |
| 10 | 0.24 | 0.34 | 0.19 | [0.17 0.55] | [0.08 0.88] |

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
| **10 sites, V<sub>S30</sub>=500** | **0.16** | **-4.48** | **[-4.83 -4.11]** | **0.23** | **-4.74** | **[-5.28 -4.39]** | **0.25** | **-5.83** | **[-6.37 -5.26]** |
| LAF | 0.17 | -4.52 | [-4.89 -4.15] | 0.26 | -4.47 | [-5.05 -4.02] | 0.27 | -5.57 | [-6.13 -4.99] |
| OSI | 0.14 | -5.32 | [-5.6 -4.99] | 0.18 | -5.95 | [-6.41 -5.62] | 0.25 | -6.62 | [-7.18 -6.09] |
| PDE | 0.16 | -4.54 | [-4.87 -4.19] | 0.22 | -4.92 | [-5.45 -4.6] | 0.24 | -5.94 | [-6.47 -5.42] |
| SBSM | 0.22 | -4 | [-4.36 -3.59] | 0.24 | -4.78 | [-5.32 -4.38] | 0.22 | -6.22 | [-6.69 -5.68] |
| SMCA | 0.16 | -4.46 | [-4.84 -4.07] | 0.24 | -4.55 | [-5.16 -4.18] | 0.26 | -5.69 | [-6.23 -5.13] |
| STNI | 0.16 | -4.28 | [-4.65 -3.92] | 0.24 | -4.26 | [-4.85 -3.91] | 0.27 | -5.07 | [-5.69 -4.46] |
| USC | 0.17 | -4.41 | [-4.76 -4.06] | 0.24 | -4.61 | [-5.21 -4.22] | 0.26 | -5.6 | [-6.17 -5] |
| WNGC | 0.16 | -4.44 | [-4.78 -4.08] | 0.22 | -4.69 | [-5.28 -4.33] | 0.25 | -5.77 | [-6.37 -5.17] |
| WSS | 0.16 | -4.77 | [-5.13 -4.44] | 0.2 | -5.17 | [-5.6 -4.79] | 0.25 | -6.26 | [-6.79 -5.71] |
| s022 | 0.17 | -4.17 | [-4.5 -3.81] | 0.22 | -4.49 | [-5.02 -4.18] | 0.26 | -5.29 | [-5.89 -4.73] |

#### 100.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 2 events and a total of 57 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.22 | 0.22 | 0.11 | [0.13 0.35] | [0.06 0.51] |
| 3 | 0.16 | 0.18 | 0.14 | [0.03 0.36] | [0 0.5] |
| 4 | 0.2 | 0.19 | 0.15 | [0.07 0.41] | [0 0.63] |
| 5 | 0.23 | 0.23 | 0.17 | [0.06 0.4] | [0.01 0.67] |
| 7.5 | 0.27 | 0.18 | 0.2 | [0.05 0.47] | [0.01 0.73] |
| 10 | 0.25 | 0.24 | 0.19 | [0.08 0.47] | [0.01 0.7] |

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
| **10 sites, V<sub>S30</sub>=500** | **0.17** | **-3.72** | **[-4.83 -2.64]** | **0.23** | **-4.12** | **[-5.28 -3.17]** | **0.25** | **-5.25** | **[-6.37 -4.12]** |
| LAF | 0.18 | -3.81 | [-4.89 -2.75] | 0.25 | -3.96 | [-5.05 -3.19] | 0.26 | -5.01 | [-6.13 -3.96] |
| OSI | 0.15 | -4.49 | [-5.6 -3.11] | 0.19 | -5.19 | [-6.41 -3.98] | 0.25 | -6.02 | [-7.18 -4.95] |
| PDE | 0.17 | -3.76 | [-4.87 -2.57] | 0.23 | -4.22 | [-5.45 -3.15] | 0.25 | -5.34 | [-6.47 -4.25] |
| SBSM | 0.21 | -3.27 | [-4.36 -2.18] | 0.25 | -4.13 | [-5.32 -3.05] | 0.21 | -5.63 | [-6.69 -4.53] |
| SMCA | 0.16 | -3.67 | [-4.84 -2.51] | 0.23 | -3.94 | [-5.16 -2.82] | 0.25 | -5.1 | [-6.23 -3.94] |
| STNI | 0.17 | -3.52 | [-4.65 -2.46] | 0.24 | -3.71 | [-4.85 -2.97] | 0.27 | -4.5 | [-5.69 -3.46] |
| USC | 0.17 | -3.67 | [-4.76 -2.62] | 0.23 | -4.05 | [-5.21 -3.2] | 0.26 | -5.03 | [-6.17 -3.99] |
| WNGC | 0.16 | -3.72 | [-4.78 -2.64] | 0.23 | -4.09 | [-5.28 -3.16] | 0.25 | -5.21 | [-6.37 -4.16] |
| WSS | 0.16 | -4 | [-5.13 -2.94] | 0.22 | -4.45 | [-5.6 -3.31] | 0.24 | -5.66 | [-6.79 -4.54] |
| s022 | 0.18 | -3.44 | [-4.5 -2.34] | 0.23 | -3.87 | [-5.02 -2.95] | 0.25 | -4.76 | [-5.89 -3.85] |

#### All Distances M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 5 events and a total of 774 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.22 | 0.27 | 0.04 | [0.23 0.3] | [0.19 0.34] |
| 3 | 0.17 | 0.22 | 0.04 | [0.18 0.27] | [0.12 0.32] |
| 4 | 0.21 | 0.25 | 0.05 | [0.2 0.29] | [0.15 0.36] |
| 5 | 0.23 | 0.28 | 0.05 | [0.24 0.32] | [0.17 0.4] |
| 7.5 | 0.25 | 0.31 | 0.06 | [0.24 0.36] | [0.18 0.42] |
| 10 | 0.25 | 0.28 | 0.06 | [0.22 0.34] | [0.17 0.42] |

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
| **50 km** | *N/A* | *N/A* | *N/A* |
| **100 km** | *N/A* | *N/A* | *N/A* |
## Azumth Dependence
*[(top)](#table-of-contents)*

### LAF Azumth Dependence
*[(top)](#table-of-contents)*

#### LAF Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/LAF_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### LAF Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/LAF_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### OSI Azumth Dependence
*[(top)](#table-of-contents)*

#### OSI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/OSI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### OSI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/OSI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### PDE Azumth Dependence
*[(top)](#table-of-contents)*

#### PDE Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PDE_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PDE Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PDE_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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
| **&tau;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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
| **&tau;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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

### WSS Azumth Dependence
*[(top)](#table-of-contents)*

#### WSS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WSS_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WSS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WSS_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### s022 Azumth Dependence
*[(top)](#table-of-contents)*

#### s022 Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/s022_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### s022 Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&tau;** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **Median SA** | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/s022_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
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

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismicâ€�hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|-----|
| **M6.6 SS** | **LAF** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **OSI** | **PASS** | **PASS** | *(PASS)* |
| **M6.6 SS** | **PDE** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **SBSM** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **SMCA** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **STNI** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **USC** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **WNGC** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **WSS** | **PASS** | **FAIL** | *(PASS)* |
| **M6.6 SS** | **s022** | **FAIL** | **FAIL** | *(FAIL)* |
| **M6.6 SS** | **10sites_Vs30_500** | **FAIL** | **FAIL** | *(FAIL)* |

### BBP PartB, M6.6, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **LAF** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_LAF.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_LAF.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_LAF.png) |
| **OSI** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_OSI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_OSI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_OSI.png) |
| **PDE** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_PDE.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_PDE.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_PDE.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_WNGC.png) |
| **WSS** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_WSS.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_WSS.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_WSS.png) |
| **s022** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_s022.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_s022.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_s022.png) |
| **10sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_20km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_50km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m6p6_vert_ss_surface_100km_10sites_Vs30_500.png) |

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

