# rundir2740 Rotated Rupture Variability, M7.2 SS

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M7.2, Vertical Strike-Slip with Surface Rupture). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

We then  perform various rotations. We rotate the rupture in place around its centroid, holding the site-to-source centroid path and Rrup constant (henceforth 'Rupture Strike'). We also rotate ruptures around the site, holding Rrup and source orientation relative to the site constant but sampling different various paths (henceforth 'Path'). We do this for each unique combination of Rupture Strike, Path, Distance, Site, and Rupture.

**Study Details**

| **Name** | RSQSim RotRup 2740 |
|-----|-----|
| **Date** | Feb 2019 |
| **Region** | Los Angeles Box |
| **Description** | RSQSim rotated-rupture variability study with catalog 2740 |
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
* [Between-events Variability](#between-events-variability)
  * [Between-events Variability Methodology](#between-events-variability-methodology)
  * [20.0 km M7.2 Between-events Results](#200-km-m72-between-events-results)
  * [50.0 km M7.2 Between-events Results](#500-km-m72-between-events-results)
  * [100.0 km M7.2 Between-events Results](#1000-km-m72-between-events-results)
  * [All Distances M7.2 Between-events Results](#all-distances-m72-between-events-results)
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
  * [PAS Azumth Dependence](#pas-azumth-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m72-vertical-strike-slip-with-surface-rupture)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 100 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 2 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 36 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **388800** | Total number of combinations of the above. |

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
| Cerro Prieto | 61 |
| San Jacinto (Borrego) | 20 |
| San Jacinto (Coyote Creek) | 20 |
| San Andreas (Parkfield) | 9 |
| San Andreas (Creeping Section) 2011 CFM | 9 |
| San Andreas (Cholame) rev | 7 |
| Mendocino | 4 |
| San Andreas (Coachella) rev | 2 |
| Garlock (East) | 1 |
| Little Lake | 1 |
| Blue Cut | 1 |
| Coronado Bank alt1 | 1 |
| TOTAL # PARENTS | 136 |

Actual magnitude range: [7.190785,7.209563], average: 7.200529, stdDev: 0.0055059

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| PAS | *34.148426, -118.17119* | 838.8 | 0.05 | 0.65 |
| USC | *34.0192, -118.286* | 313.1 | 0.6 | 4.05 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.29 | 0.34 | 0.33 | 0.16 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.34 | 0.38 | 0.37 | 0.23 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.37 | 0.39 | 0.4 | 0.27 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.33 | 0.37 | 0.37 | 0.23 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.46 | 0.54 | 0.45 | 0.37 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.48 | 0.5 | 0.47 | 0.49 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.5 | 0.48 | 0.49 | 0.52 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.48 | 0.51 | 0.47 | 0.47 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.49 | 0.59 | 0.49 | 0.37 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.52 | 0.55 | 0.51 | 0.5 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.56 | 0.56 | 0.56 | 0.54 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.52 | 0.57 | 0.52 | 0.48 |
| Between-events | &tau; | 20 km | 0.16 | 0.12 | 0.18 | 0.16 |
| Between-events | &tau; | 50 km | 0.16 | 0.12 | 0.17 | 0.17 |
| Between-events | &tau; | 100 km | 0.15 | 0.11 | 0.15 | 0.17 |
| Between-events | &tau; | (all) | 0.16 | 0.12 | 0.16 | 0.17 |

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
| Between-events | &tau; | 20 km | 0.36 | 0.36 | 0.36 |
| Between-events | &tau; | 50 km | 0.36 | 0.36 | 0.36 |
| Between-events | &tau; | 100 km | 0.36 | 0.36 | 0.36 |

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

* Site *[2 unique]*
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
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.11 0.8]** |  | **0.33** | **0.31** | **0.31** | **[0.1 0.59]** |  | **0.16** | **0.14** | **0.14** | **[0.04 0.48]** |
| PAS |  | 0.35 | 0.34 | 0.33 | [0.11 0.8] |  | 0.32 | 0.3 | 0.3 | [0.1 0.59] |  | 0.15 | 0.13 | 0.13 | [0.04 0.42] |
| USC |  | 0.32 | 0.32 | 0.32 | [0.15 0.56] |  | 0.33 | 0.32 | 0.32 | [0.1 0.55] |  | 0.17 | 0.16 | 0.14 | [0.05 0.48] |

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
| T-independent | 0.29 | 0.28 | 0.02 | [0.26 0.31] | [0.24 0.33] |
| 3 | 0.34 | 0.33 | 0.04 | [0.29 0.37] | [0.26 0.4] |
| 4 | 0.33 | 0.32 | 0.03 | [0.29 0.36] | [0.27 0.38] |
| 5 | 0.33 | 0.32 | 0.04 | [0.29 0.36] | [0.26 0.41] |
| 7.5 | 0.23 | 0.23 | 0.04 | [0.19 0.27] | [0.15 0.3] |
| 10 | 0.16 | 0.15 | 0.03 | [0.13 0.17] | [0.1 0.22] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.38** | **0.36** | **0.34** | **[0.14 0.81]** |  | **0.37** | **0.36** | **0.35** | **[0.17 0.65]** |  | **0.23** | **0.22** | **0.22** | **[0.07 0.47]** |
| PAS |  | 0.42 | 0.4 | 0.38 | [0.17 0.81] |  | 0.38 | 0.37 | 0.35 | [0.18 0.65] |  | 0.21 | 0.2 | 0.2 | [0.07 0.4] |
| USC |  | 0.33 | 0.33 | 0.32 | [0.14 0.56] |  | 0.36 | 0.36 | 0.35 | [0.17 0.55] |  | 0.25 | 0.24 | 0.24 | [0.11 0.47] |

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
| T-independent | 0.34 | 0.32 | 0.03 | [0.29 0.36] | [0.27 0.4] |
| 3 | 0.38 | 0.36 | 0.06 | [0.3 0.41] | [0.26 0.51] |
| 4 | 0.37 | 0.35 | 0.05 | [0.3 0.41] | [0.26 0.48] |
| 5 | 0.37 | 0.35 | 0.04 | [0.32 0.4] | [0.26 0.45] |
| 7.5 | 0.32 | 0.3 | 0.04 | [0.27 0.34] | [0.23 0.38] |
| 10 | 0.23 | 0.22 | 0.03 | [0.19 0.26] | [0.16 0.29] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.39** | **0.38** | **[0.2 0.7]** |  | **0.4** | **0.4** | **0.39** | **[0.18 0.67]** |  | **0.27** | **0.27** | **0.26** | **[0.09 0.54]** |
| PAS |  | 0.4 | 0.4 | 0.39 | [0.2 0.7] |  | 0.39 | 0.38 | 0.37 | [0.18 0.67] |  | 0.23 | 0.23 | 0.22 | [0.09 0.49] |
| USC |  | 0.38 | 0.38 | 0.37 | [0.24 0.6] |  | 0.42 | 0.42 | 0.41 | [0.2 0.63] |  | 0.31 | 0.3 | 0.3 | [0.13 0.54] |

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
| T-independent | 0.37 | 0.36 | 0.03 | [0.34 0.4] | [0.31 0.43] |
| 3 | 0.39 | 0.39 | 0.04 | [0.35 0.43] | [0.31 0.45] |
| 4 | 0.4 | 0.4 | 0.04 | [0.36 0.44] | [0.32 0.49] |
| 5 | 0.4 | 0.4 | 0.04 | [0.36 0.44] | [0.33 0.48] |
| 7.5 | 0.35 | 0.34 | 0.03 | [0.31 0.38] | [0.28 0.41] |
| 10 | 0.27 | 0.27 | 0.03 | [0.23 0.3] | [0.21 0.34] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_3s.png) |


### All Distances M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.37** | **0.36** | **0.35** | **[0.11 0.81]** |  | **0.37** | **0.36** | **0.35** | **[0.1 0.67]** |  | **0.23** | **0.21** | **0.2** | **[0.04 0.54]** |
| PAS |  | 0.39 | 0.38 | 0.37 | [0.11 0.81] |  | 0.36 | 0.35 | 0.34 | [0.1 0.67] |  | 0.2 | 0.19 | 0.19 | [0.04 0.49] |
| USC |  | 0.34 | 0.34 | 0.34 | [0.14 0.6] |  | 0.37 | 0.37 | 0.36 | [0.1 0.63] |  | 0.25 | 0.23 | 0.23 | [0.05 0.54] |

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
| T-independent | 0.33 | 0.33 | 0.01 | [0.32 0.34] | [0.31 0.35] |
| 3 | 0.37 | 0.37 | 0.02 | [0.35 0.39] | [0.34 0.41] |
| 4 | 0.37 | 0.36 | 0.02 | [0.35 0.38] | [0.34 0.4] |
| 5 | 0.37 | 0.36 | 0.01 | [0.35 0.38] | [0.34 0.39] |
| 7.5 | 0.3 | 0.3 | 0.01 | [0.29 0.31] | [0.27 0.32] |
| 10 | 0.23 | 0.23 | 0.01 | [0.21 0.23] | [0.2 0.25] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_3s.png) |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[2 unique]*
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
| **ALL SITES** |  | **0.54** | **0.54** | **0.54** | **[0.17 0.96]** |  | **0.45** | **0.44** | **0.44** | **[0.13 0.8]** |  | **0.37** | **0.35** | **0.33** | **[0.06 0.87]** |
| PAS |  | 0.58 | 0.58 | 0.58 | [0.29 0.96] |  | 0.47 | 0.46 | 0.46 | [0.21 0.8] |  | 0.36 | 0.34 | 0.32 | [0.06 0.82] |
| USC |  | 0.5 | 0.5 | 0.5 | [0.17 0.91] |  | 0.43 | 0.42 | 0.42 | [0.13 0.76] |  | 0.38 | 0.36 | 0.34 | [0.12 0.87] |

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
| T-independent | 0.46 | 0.45 | 0.03 | [0.42 0.48] | [0.4 0.5] |
| 3 | 0.54 | 0.54 | 0.04 | [0.5 0.58] | [0.46 0.64] |
| 4 | 0.5 | 0.49 | 0.05 | [0.44 0.53] | [0.4 0.59] |
| 5 | 0.45 | 0.43 | 0.05 | [0.39 0.49] | [0.35 0.54] |
| 7.5 | 0.4 | 0.4 | 0.04 | [0.35 0.43] | [0.31 0.46] |
| 10 | 0.37 | 0.35 | 0.05 | [0.31 0.41] | [0.28 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.5** | **0.48** | **0.46** | **[0.16 1.05]** |  | **0.47** | **0.45** | **0.44** | **[0.11 0.92]** |  | **0.49** | **0.49** | **0.48** | **[0.15 0.93]** |
| PAS |  | 0.52 | 0.5 | 0.46 | [0.16 1.05] |  | 0.46 | 0.44 | 0.42 | [0.13 0.85] |  | 0.49 | 0.49 | 0.48 | [0.18 0.93] |
| USC |  | 0.48 | 0.47 | 0.46 | [0.18 0.9] |  | 0.48 | 0.46 | 0.46 | [0.11 0.92] |  | 0.5 | 0.49 | 0.49 | [0.15 0.92] |

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
| T-independent | 0.48 | 0.47 | 0.05 | [0.43 0.52] | [0.37 0.57] |
| 3 | 0.5 | 0.49 | 0.07 | [0.43 0.56] | [0.31 0.64] |
| 4 | 0.48 | 0.47 | 0.08 | [0.38 0.55] | [0.33 0.63] |
| 5 | 0.47 | 0.45 | 0.07 | [0.4 0.52] | [0.33 0.59] |
| 7.5 | 0.47 | 0.47 | 0.06 | [0.4 0.52] | [0.35 0.57] |
| 10 | 0.49 | 0.49 | 0.05 | [0.43 0.52] | [0.37 0.6] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.48** | **0.48** | **0.47** | **[0.16 0.86]** |  | **0.49** | **0.47** | **0.47** | **[0.13 0.89]** |  | **0.52** | **0.51** | **0.51** | **[0.13 0.93]** |
| PAS |  | 0.49 | 0.49 | 0.49 | [0.19 0.86] |  | 0.48 | 0.46 | 0.46 | [0.13 0.87] |  | 0.52 | 0.51 | 0.51 | [0.13 0.93] |
| USC |  | 0.47 | 0.46 | 0.46 | [0.16 0.86] |  | 0.49 | 0.49 | 0.48 | [0.18 0.89] |  | 0.52 | 0.52 | 0.52 | [0.24 0.91] |

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
| T-independent | 0.5 | 0.5 | 0.05 | [0.44 0.55] | [0.39 0.59] |
| 3 | 0.48 | 0.48 | 0.05 | [0.43 0.54] | [0.37 0.58] |
| 4 | 0.49 | 0.48 | 0.06 | [0.42 0.55] | [0.36 0.61] |
| 5 | 0.49 | 0.48 | 0.06 | [0.42 0.55] | [0.36 0.59] |
| 7.5 | 0.51 | 0.5 | 0.07 | [0.43 0.58] | [0.37 0.64] |
| 10 | 0.52 | 0.52 | 0.07 | [0.46 0.59] | [0.39 0.66] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_3s.png) |


### All Distances M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.51** | **0.5** | **0.49** | **[0.16 1.05]** |  | **0.47** | **0.46** | **0.45** | **[0.11 0.92]** |  | **0.47** | **0.45** | **0.45** | **[0.06 0.93]** |
| PAS |  | 0.53 | 0.52 | 0.51 | [0.16 1.05] |  | 0.47 | 0.46 | 0.45 | [0.13 0.87] |  | 0.46 | 0.45 | 0.45 | [0.06 0.93] |
| USC |  | 0.49 | 0.48 | 0.47 | [0.16 0.91] |  | 0.47 | 0.46 | 0.45 | [0.11 0.92] |  | 0.47 | 0.45 | 0.46 | [0.12 0.92] |

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
| T-independent | 0.48 | 0.48 | 0.02 | [0.47 0.5] | [0.44 0.51] |
| 3 | 0.51 | 0.51 | 0.02 | [0.48 0.54] | [0.48 0.56] |
| 4 | 0.49 | 0.49 | 0.02 | [0.46 0.52] | [0.44 0.53] |
| 5 | 0.47 | 0.47 | 0.02 | [0.45 0.49] | [0.42 0.5] |
| 7.5 | 0.46 | 0.46 | 0.02 | [0.44 0.48] | [0.42 0.51] |
| 10 | 0.47 | 0.46 | 0.02 | [0.44 0.49] | [0.43 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_3s.png) |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[2 unique]*
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
| **ALL SITES** |  | **0.59** | **0.58** | **0.58** | **[0.4 0.8]** |  | **0.49** | **0.48** | **0.48** | **[0.33 0.71]** |  | **0.37** | **0.35** | **0.33** | **[0.14 0.74]** |
| PAS |  | 0.63 | 0.63 | 0.63 | [0.46 0.8] |  | 0.51 | 0.51 | 0.51 | [0.34 0.71] |  | 0.36 | 0.34 | 0.33 | [0.14 0.73] |
| USC |  | 0.54 | 0.54 | 0.54 | [0.4 0.68] |  | 0.47 | 0.46 | 0.46 | [0.33 0.61] |  | 0.38 | 0.36 | 0.34 | [0.17 0.74] |

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
| T-independent | 0.49 | 0.48 | 0.03 | [0.44 0.51] | [0.41 0.55] |
| 3 | 0.59 | 0.58 | 0.05 | [0.54 0.63] | [0.49 0.67] |
| 4 | 0.54 | 0.52 | 0.05 | [0.48 0.58] | [0.43 0.63] |
| 5 | 0.49 | 0.47 | 0.05 | [0.43 0.52] | [0.39 0.58] |
| 7.5 | 0.41 | 0.4 | 0.05 | [0.35 0.45] | [0.31 0.49] |
| 10 | 0.37 | 0.35 | 0.06 | [0.3 0.41] | [0.26 0.5] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_3s.png) |

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
| **ALL SITES** |  | **0.55** | **0.55** | **0.55** | **[0.41 0.71]** |  | **0.51** | **0.51** | **0.5** | **[0.36 0.69]** |  | **0.5** | **0.49** | **0.48** | **[0.34 0.8]** |
| PAS |  | 0.59 | 0.59 | 0.59 | [0.51 0.71] |  | 0.51 | 0.51 | 0.5 | [0.4 0.64] |  | 0.49 | 0.48 | 0.47 | [0.34 0.8] |
| USC |  | 0.51 | 0.51 | 0.51 | [0.41 0.63] |  | 0.51 | 0.51 | 0.5 | [0.36 0.69] |  | 0.51 | 0.5 | 0.49 | [0.35 0.79] |

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
| T-independent | 0.52 | 0.5 | 0.04 | [0.45 0.53] | [0.42 0.57] |
| 3 | 0.55 | 0.52 | 0.06 | [0.47 0.58] | [0.42 0.65] |
| 4 | 0.53 | 0.51 | 0.06 | [0.46 0.55] | [0.38 0.62] |
| 5 | 0.51 | 0.49 | 0.06 | [0.43 0.54] | [0.39 0.61] |
| 7.5 | 0.49 | 0.47 | 0.06 | [0.42 0.52] | [0.35 0.58] |
| 10 | 0.5 | 0.47 | 0.06 | [0.41 0.54] | [0.37 0.58] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_3s.png) |

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
| **ALL SITES** |  | **0.56** | **0.56** | **0.56** | **[0.44 0.71]** |  | **0.56** | **0.56** | **0.55** | **[0.43 0.75]** |  | **0.54** | **0.53** | **0.52** | **[0.37 0.82]** |
| PAS |  | 0.58 | 0.58 | 0.58 | [0.48 0.71] |  | 0.55 | 0.54 | 0.54 | [0.44 0.68] |  | 0.52 | 0.51 | 0.5 | [0.37 0.82] |
| USC |  | 0.54 | 0.54 | 0.55 | [0.44 0.67] |  | 0.58 | 0.57 | 0.57 | [0.43 0.75] |  | 0.56 | 0.55 | 0.54 | [0.42 0.82] |

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
| T-independent | 0.56 | 0.55 | 0.03 | [0.52 0.59] | [0.5 0.62] |
| 3 | 0.56 | 0.56 | 0.05 | [0.52 0.61] | [0.47 0.65] |
| 4 | 0.57 | 0.56 | 0.04 | [0.52 0.61] | [0.49 0.64] |
| 5 | 0.56 | 0.56 | 0.04 | [0.51 0.61] | [0.48 0.65] |
| 7.5 | 0.55 | 0.55 | 0.05 | [0.5 0.6] | [0.46 0.64] |
| 10 | 0.54 | 0.53 | 0.05 | [0.49 0.59] | [0.44 0.63] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_3s.png) |

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
| **ALL SITES** |  | **0.57** | **0.56** | **0.56** | **[0.4 0.8]** |  | **0.52** | **0.52** | **0.51** | **[0.33 0.75]** |  | **0.48** | **0.46** | **0.47** | **[0.14 0.82]** |
| PAS |  | 0.6 | 0.6 | 0.59 | [0.46 0.8] |  | 0.53 | 0.52 | 0.52 | [0.34 0.71] |  | 0.47 | 0.44 | 0.46 | [0.14 0.82] |
| USC |  | 0.53 | 0.53 | 0.53 | [0.4 0.68] |  | 0.52 | 0.51 | 0.51 | [0.33 0.75] |  | 0.49 | 0.47 | 0.48 | [0.17 0.82] |

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
| T-independent | 0.52 | 0.52 | 0.01 | [0.51 0.54] | [0.49 0.56] |
| 3 | 0.57 | 0.57 | 0.02 | [0.55 0.59] | [0.53 0.61] |
| 4 | 0.55 | 0.55 | 0.02 | [0.53 0.56] | [0.5 0.59] |
| 5 | 0.52 | 0.52 | 0.02 | [0.5 0.55] | [0.49 0.57] |
| 7.5 | 0.49 | 0.49 | 0.02 | [0.47 0.51] | [0.43 0.53] |
| 10 | 0.48 | 0.47 | 0.03 | [0.45 0.51] | [0.42 0.55] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/within_event_ss_event_recordings_hist_all_dists.png)


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[100 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 1296 combinations of:

* Site *[2 unique]*
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
| PAS | 0.12 | -3.11 | [-3.35 -2.82] | 0.15 | -3.74 | [-4.3 -3.39] | 0.18 | -4.7 | [-5.09 -4.21] |
| USC | 0.13 | -1.92 | [-2.21 -1.62] | 0.16 | -2.54 | [-3.05 -2.21] | 0.18 | -3.73 | [-4.17 -3.32] |

#### 20.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.24 | 0.08 | [0.17 0.33] | [0.14 0.46] |
| 3 | 0.12 | 0.28 | 0.11 | [0.17 0.43] | [0.11 0.51] |
| 4 | 0.16 | 0.27 | 0.11 | [0.17 0.39] | [0.09 0.55] |
| 5 | 0.15 | 0.24 | 0.11 | [0.15 0.36] | [0.06 0.55] |
| 7.5 | 0.21 | 0.21 | 0.11 | [0.12 0.34] | [0.05 0.49] |
| 10 | 0.18 | 0.2 | 0.1 | [0.12 0.33] | [0.05 0.45] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| PAS | 0.11 | -4.08 | [-4.35 -3.83] | 0.15 | -4.51 | [-5.06 -4.16] | 0.19 | -5.34 | [-5.78 -4.92] |
| USC | 0.12 | -2.73 | [-3.03 -2.47] | 0.17 | -3.13 | [-3.69 -2.72] | 0.19 | -4.33 | [-4.84 -3.96] |

#### 50.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.27 | 0.07 | [0.19 0.34] | [0.15 0.43] |
| 3 | 0.11 | 0.24 | 0.11 | [0.14 0.38] | [0.07 0.52] |
| 4 | 0.15 | 0.24 | 0.12 | [0.13 0.38] | [0.07 0.52] |
| 5 | 0.15 | 0.23 | 0.1 | [0.16 0.35] | [0.09 0.51] |
| 7.5 | 0.19 | 0.28 | 0.12 | [0.16 0.41] | [0.07 0.53] |
| 10 | 0.19 | 0.3 | 0.12 | [0.18 0.42] | [0.08 0.6] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| PAS | 0.11 | -4.67 | [-4.93 -4.42] | 0.14 | -5.08 | [-5.62 -4.78] | 0.2 | -5.82 | [-6.37 -5.4] |
| USC | 0.11 | -3.38 | [-3.65 -3.17] | 0.17 | -3.71 | [-4.32 -3.31] | 0.19 | -4.84 | [-5.44 -4.44] |

#### 100.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.15 | 0.21 | 0.07 | [0.16 0.29] | [0.11 0.42] |
| 3 | 0.11 | 0.2 | 0.11 | [0.1 0.35] | [0.04 0.48] |
| 4 | 0.13 | 0.2 | 0.1 | [0.1 0.31] | [0.03 0.46] |
| 5 | 0.14 | 0.19 | 0.11 | [0.1 0.32] | [0.03 0.5] |
| 7.5 | 0.19 | 0.23 | 0.13 | [0.1 0.36] | [0.03 0.6] |
| 10 | 0.2 | 0.24 | 0.12 | [0.12 0.37] | [0.04 0.52] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| PAS | 0.11 | -3.95 | [-4.93 -2.82] | 0.15 | -4.44 | [-5.62 -3.39] | 0.19 | -5.29 | [-6.37 -4.21] |
| USC | 0.12 | -2.68 | [-3.65 -1.62] | 0.17 | -3.13 | [-4.32 -2.21] | 0.18 | -4.3 | [-5.44 -3.32] |

#### All Distances M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.16 | 0.2 | 0.02 | [0.17 0.22] | [0.16 0.25] |
| 3 | 0.11 | 0.18 | 0.03 | [0.14 0.2] | [0.12 0.23] |
| 4 | 0.15 | 0.19 | 0.04 | [0.15 0.23] | [0.11 0.27] |
| 5 | 0.15 | 0.18 | 0.03 | [0.15 0.22] | [0.12 0.26] |
| 7.5 | 0.19 | 0.21 | 0.04 | [0.17 0.26] | [0.14 0.3] |
| 10 | 0.19 | 0.21 | 0.04 | [0.17 0.25] | [0.14 0.31] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4].

![Histogram](resources/between_events_event_recordings_hist_all_dists.png)


## Event Term Scatters
*[(top)](#table-of-contents)*

### Propagation Velocity Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_PAS_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_PAS_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_PAS_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_PAS_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_PAS_10s.png) |
### Slip Std Dev Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_PAS_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_PAS_10s.png) |
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

### PAS Azumth Dependence
*[(top)](#table-of-contents)*

#### PAS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PAS_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PAS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PAS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>s</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;<sub>SS</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
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
| **M7.2 SS** | **USC** | *(FAIL)* | *(FAIL)* | *(FAIL)* |

### BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_PAS.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_USC.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M7.2 | 20.0 km | PAS | [sa_PAS_m7.2_20.0km.csv.gz](resources/sa_PAS_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | USC | [sa_USC_m7.2_20.0km.csv.gz](resources/sa_USC_m7.2_20.0km.csv.gz) |
| M7.2 | 50.0 km | PAS | [sa_PAS_m7.2_50.0km.csv.gz](resources/sa_PAS_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | USC | [sa_USC_m7.2_50.0km.csv.gz](resources/sa_USC_m7.2_50.0km.csv.gz) |
| M7.2 | 100.0 km | PAS | [sa_PAS_m7.2_100.0km.csv.gz](resources/sa_PAS_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | USC | [sa_USC_m7.2_100.0km.csv.gz](resources/sa_USC_m7.2_100.0km.csv.gz) |

