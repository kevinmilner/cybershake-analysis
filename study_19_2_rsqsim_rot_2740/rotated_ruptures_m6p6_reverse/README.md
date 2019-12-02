# rundir2740 Rotated Rupture Variability, M6.6 Reverse

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M6.6, Reverse, Dip=45, Ztor=3). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

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
* [M6.6 Reverse RSQSim Rupture Match Criteria](#m66-reverse-rsqsim-rupture-match-criteria)
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
  * [PAS Azumth Dependence](#pas-azumth-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M6.6, Reverse, Dip=45, Ztor=3](#bbp-partb-m66-reverse-dip45-ztor3)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 49 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 2 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 36 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **190512** | Total number of combinations of the above. |

## M6.6 Reverse RSQSim Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 49 events in the catalog which match the following criteria:

* M=[6.55,6.65]
* Ztor=[1.0,5.0]
* Rake=[80,100]
* Dip=[35.0,55.0]

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| McKinleyville (alt1) | 14 |
| Cucamonga | 11 |
| Fickle Hill (alt1) | 6 |
| Table Bluff | 5 |
| San Luis Range 2011 CFM | 3 |
| Mount Diablo Thrust South | 3 |
| Carlsbad | 2 |
| Mad River (alt1) | 2 |
| Big Lagoon - Bald Mtn 2011 CFM | 1 |
| Sierra Madre | 1 |
| San Luis Range - Oceano 2011 CFM | 1 |
| Mount Diablo Thrust North CFM | 1 |
| Los Osos 2011 | 1 |
| TOTAL # PARENTS | 51 |

Actual magnitude range: [6.552737,6.6489244], average: 6.5978293, stdDev: 0.026210476

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| PAS | *34.148426, -118.17119* | 838.8 | 0.05 | 0.65 |
| USC | *34.0192, -118.286* | 313.1 | 0.6 | 4.05 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.25 | 0.32 | 0.27 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.31 | 0.36 | 0.35 | 0.19 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.34 | 0.38 | 0.35 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.3 | 0.35 | 0.33 | 0.2 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.4 | 0.34 | 0.42 | 0.39 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.4 | 0.33 | 0.43 | 0.42 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.41 | 0.34 | 0.43 | 0.44 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.4 | 0.34 | 0.43 | 0.42 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.43 | 0.41 | 0.45 | 0.4 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.46 | 0.43 | 0.49 | 0.43 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.49 | 0.46 | 0.51 | 0.47 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.46 | 0.43 | 0.48 | 0.43 |
| Between-events | &tau; | 20 km | 0.2 | 0.17 | 0.2 | 0.21 |
| Between-events | &tau; | 50 km | 0.21 | 0.2 | 0.22 | 0.22 |
| Between-events | &tau; | 100 km | 0.21 | 0.17 | 0.21 | 0.24 |
| Between-events | &tau; | (all) | 0.21 | 0.18 | 0.21 | 0.22 |

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
| Between-events | &tau; | 20 km | 0.38 | 0.38 | 0.38 |
| Between-events | &tau; | 50 km | 0.38 | 0.38 | 0.38 |
| Between-events | &tau; | 100 km | 0.38 | 0.38 | 0.38 |

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

* Site *[2 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[49 unique]*
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
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.1 0.56]** |  | **0.27** | **0.26** | **0.26** | **[0.08 0.54]** |  | **0.15** | **0.14** | **0.13** | **[0.02 0.42]** |
| PAS |  | 0.32 | 0.31 | 0.31 | [0.1 0.56] |  | 0.25 | 0.24 | 0.24 | [0.11 0.48] |  | 0.13 | 0.12 | 0.12 | [0.02 0.38] |
| USC |  | 0.31 | 0.3 | 0.29 | [0.1 0.56] |  | 0.3 | 0.29 | 0.29 | [0.08 0.54] |  | 0.16 | 0.15 | 0.15 | [0.03 0.42] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_20km_3s_hist.png) | ![5s](resources/path_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 88 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 17 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.25 | 0.02 | [0.23 0.28] | [0.21 0.31] |
| 3 | 0.32 | 0.31 | 0.04 | [0.27 0.36] | [0.26 0.41] |
| 4 | 0.31 | 0.31 | 0.04 | [0.27 0.35] | [0.24 0.39] |
| 5 | 0.27 | 0.27 | 0.03 | [0.25 0.3] | [0.22 0.33] |
| 7.5 | 0.17 | 0.16 | 0.03 | [0.14 0.19] | [0.11 0.23] |
| 10 | 0.15 | 0.14 | 0.02 | [0.12 0.16] | [0.1 0.2] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.36** | **0.35** | **0.34** | **[0.16 0.69]** |  | **0.35** | **0.34** | **0.34** | **[0.12 0.6]** |  | **0.19** | **0.18** | **0.18** | **[0.06 0.46]** |
| PAS |  | 0.38 | 0.36 | 0.35 | [0.16 0.69] |  | 0.33 | 0.32 | 0.32 | [0.12 0.59] |  | 0.16 | 0.15 | 0.15 | [0.06 0.43] |
| USC |  | 0.34 | 0.34 | 0.34 | [0.22 0.49] |  | 0.36 | 0.36 | 0.36 | [0.22 0.6] |  | 0.22 | 0.21 | 0.21 | [0.08 0.46] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_50km_3s_hist.png) | ![5s](resources/path_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 77 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 4 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.31 | 0.31 | 0.02 | [0.29 0.34] | [0.27 0.36] |
| 3 | 0.36 | 0.35 | 0.04 | [0.32 0.4] | [0.29 0.44] |
| 4 | 0.36 | 0.36 | 0.03 | [0.32 0.39] | [0.29 0.42] |
| 5 | 0.35 | 0.34 | 0.03 | [0.32 0.38] | [0.29 0.4] |
| 7.5 | 0.28 | 0.28 | 0.03 | [0.25 0.3] | [0.23 0.33] |
| 10 | 0.19 | 0.19 | 0.02 | [0.16 0.22] | [0.15 0.25] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.38** | **0.38** | **0.37** | **[0.18 0.67]** |  | **0.35** | **0.35** | **0.35** | **[0.17 0.53]** |  | **0.24** | **0.24** | **0.23** | **[0.11 0.4]** |
| PAS |  | 0.4 | 0.4 | 0.38 | [0.18 0.67] |  | 0.34 | 0.34 | 0.34 | [0.17 0.51] |  | 0.2 | 0.2 | 0.2 | [0.11 0.34] |
| USC |  | 0.36 | 0.36 | 0.36 | [0.25 0.58] |  | 0.36 | 0.36 | 0.36 | [0.24 0.53] |  | 0.27 | 0.27 | 0.27 | [0.15 0.4] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_100km_3s_hist.png) | ![5s](resources/path_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 83 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 62 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.34 | 0.34 | 0.02 | [0.31 0.36] | [0.3 0.37] |
| 3 | 0.38 | 0.38 | 0.04 | [0.35 0.42] | [0.3 0.45] |
| 4 | 0.38 | 0.37 | 0.03 | [0.34 0.4] | [0.32 0.44] |
| 5 | 0.35 | 0.35 | 0.02 | [0.33 0.38] | [0.31 0.4] |
| 7.5 | 0.32 | 0.32 | 0.03 | [0.3 0.35] | [0.26 0.36] |
| 10 | 0.24 | 0.24 | 0.02 | [0.21 0.26] | [0.2 0.28] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_3s.png) |


### All Distances M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.35** | **0.35** | **0.34** | **[0.1 0.69]** |  | **0.33** | **0.32** | **0.32** | **[0.08 0.6]** |  | **0.2** | **0.19** | **0.18** | **[0.02 0.46]** |
| PAS |  | 0.37 | 0.36 | 0.34 | [0.1 0.69] |  | 0.31 | 0.3 | 0.3 | [0.11 0.59] |  | 0.17 | 0.16 | 0.16 | [0.02 0.43] |
| USC |  | 0.34 | 0.33 | 0.33 | [0.1 0.58] |  | 0.34 | 0.34 | 0.34 | [0.08 0.6] |  | 0.22 | 0.21 | 0.21 | [0.03 0.46] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m6.6_3s_hist.png) | ![5s](resources/path_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 492 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 855 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.3 | 0.3 | 0.01 | [0.29 0.31] | [0.29 0.32] |
| 3 | 0.35 | 0.35 | 0.01 | [0.34 0.37] | [0.33 0.39] |
| 4 | 0.35 | 0.35 | 0.01 | [0.33 0.36] | [0.32 0.38] |
| 5 | 0.33 | 0.32 | 0.01 | [0.31 0.34] | [0.3 0.35] |
| 7.5 | 0.26 | 0.26 | 0.01 | [0.25 0.27] | [0.24 0.29] |
| 10 | 0.2 | 0.2 | 0.01 | [0.19 0.2] | [0.18 0.22] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m6.6_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_3s.png) |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[2 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[49 unique]*
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
| **ALL SITES** |  | **0.34** | **0.34** | **0.33** | **[0.13 0.62]** |  | **0.42** | **0.4** | **0.4** | **[0.13 0.86]** |  | **0.39** | **0.38** | **0.37** | **[0.1 0.8]** |
| PAS |  | 0.35 | 0.35 | 0.35 | [0.15 0.61] |  | 0.43 | 0.42 | 0.41 | [0.15 0.8] |  | 0.4 | 0.39 | 0.38 | [0.11 0.77] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.13 0.62] |  | 0.41 | 0.39 | 0.38 | [0.13 0.86] |  | 0.39 | 0.37 | 0.36 | [0.1 0.8] |

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
| T-independent | 0.4 | 0.39 | 0.03 | [0.35 0.42] | [0.33 0.47] |
| 3 | 0.34 | 0.34 | 0.03 | [0.31 0.37] | [0.27 0.42] |
| 4 | 0.37 | 0.37 | 0.04 | [0.32 0.41] | [0.3 0.46] |
| 5 | 0.42 | 0.41 | 0.05 | [0.37 0.46] | [0.32 0.52] |
| 7.5 | 0.45 | 0.43 | 0.05 | [0.38 0.48] | [0.33 0.54] |
| 10 | 0.39 | 0.38 | 0.05 | [0.33 0.44] | [0.29 0.48] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.33** | **0.32** | **0.31** | **[0.1 0.71]** |  | **0.43** | **0.41** | **0.4** | **[0.11 0.8]** |  | **0.42** | **0.4** | **0.39** | **[0.13 0.81]** |
| PAS |  | 0.33 | 0.33 | 0.31 | [0.11 0.65] |  | 0.44 | 0.42 | 0.42 | [0.11 0.8] |  | 0.41 | 0.4 | 0.38 | [0.16 0.78] |
| USC |  | 0.32 | 0.31 | 0.31 | [0.1 0.71] |  | 0.42 | 0.4 | 0.39 | [0.12 0.8] |  | 0.42 | 0.41 | 0.39 | [0.13 0.81] |

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
| T-independent | 0.4 | 0.4 | 0.03 | [0.36 0.43] | [0.33 0.47] |
| 3 | 0.33 | 0.32 | 0.04 | [0.29 0.37] | [0.24 0.41] |
| 4 | 0.37 | 0.37 | 0.04 | [0.33 0.42] | [0.28 0.46] |
| 5 | 0.43 | 0.43 | 0.05 | [0.38 0.47] | [0.31 0.53] |
| 7.5 | 0.44 | 0.44 | 0.06 | [0.39 0.5] | [0.35 0.57] |
| 10 | 0.42 | 0.41 | 0.05 | [0.36 0.47] | [0.33 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.1 0.8]** |  | **0.43** | **0.41** | **0.39** | **[0.1 0.82]** |  | **0.44** | **0.43** | **0.42** | **[0.11 0.81]** |
| PAS |  | 0.34 | 0.33 | 0.32 | [0.11 0.8] |  | 0.42 | 0.41 | 0.39 | [0.1 0.8] |  | 0.44 | 0.43 | 0.42 | [0.13 0.78] |
| USC |  | 0.33 | 0.32 | 0.32 | [0.1 0.77] |  | 0.43 | 0.41 | 0.39 | [0.11 0.82] |  | 0.44 | 0.43 | 0.42 | [0.11 0.81] |

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
| T-independent | 0.41 | 0.4 | 0.04 | [0.37 0.45] | [0.35 0.49] |
| 3 | 0.34 | 0.33 | 0.04 | [0.29 0.38] | [0.26 0.42] |
| 4 | 0.38 | 0.38 | 0.05 | [0.33 0.44] | [0.3 0.49] |
| 5 | 0.43 | 0.42 | 0.05 | [0.37 0.47] | [0.33 0.54] |
| 7.5 | 0.47 | 0.45 | 0.06 | [0.39 0.52] | [0.36 0.57] |
| 10 | 0.44 | 0.43 | 0.05 | [0.39 0.49] | [0.35 0.53] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_3s.png) |


### All Distances M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.34** | **0.33** | **0.32** | **[0.1 0.8]** |  | **0.43** | **0.41** | **0.4** | **[0.1 0.86]** |  | **0.42** | **0.4** | **0.39** | **[0.1 0.81]** |
| PAS |  | 0.34 | 0.34 | 0.33 | [0.11 0.8] |  | 0.43 | 0.41 | 0.41 | [0.1 0.8] |  | 0.42 | 0.41 | 0.4 | [0.11 0.78] |
| USC |  | 0.33 | 0.32 | 0.31 | [0.1 0.77] |  | 0.42 | 0.4 | 0.39 | [0.11 0.86] |  | 0.42 | 0.4 | 0.39 | [0.1 0.81] |

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
| T-independent | 0.4 | 0.4 | 0.01 | [0.39 0.41] | [0.37 0.44] |
| 3 | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.3 0.36] |
| 4 | 0.37 | 0.37 | 0.02 | [0.35 0.39] | [0.34 0.41] |
| 5 | 0.43 | 0.42 | 0.02 | [0.4 0.45] | [0.38 0.47] |
| 7.5 | 0.45 | 0.45 | 0.02 | [0.43 0.47] | [0.4 0.51] |
| 10 | 0.42 | 0.42 | 0.02 | [0.4 0.43] | [0.37 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m6.6_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_3s.png) |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[2 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[49 unique]*

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
| **ALL SITES** |  | **0.41** | **0.41** | **0.41** | **[0.3 0.52]** |  | **0.45** | **0.44** | **0.43** | **[0.3 0.64]** |  | **0.4** | **0.38** | **0.38** | **[0.19 0.66]** |
| PAS |  | 0.43 | 0.43 | 0.43 | [0.36 0.52] |  | 0.45 | 0.44 | 0.44 | [0.31 0.64] |  | 0.4 | 0.38 | 0.39 | [0.22 0.64] |
| USC |  | 0.39 | 0.38 | 0.38 | [0.3 0.5] |  | 0.45 | 0.44 | 0.41 | [0.3 0.64] |  | 0.39 | 0.37 | 0.38 | [0.19 0.66] |

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
| T-independent | 0.43 | 0.42 | 0.03 | [0.4 0.45] | [0.37 0.49] |
| 3 | 0.41 | 0.41 | 0.02 | [0.38 0.44] | [0.36 0.45] |
| 4 | 0.43 | 0.43 | 0.03 | [0.39 0.46] | [0.37 0.48] |
| 5 | 0.45 | 0.44 | 0.04 | [0.41 0.48] | [0.36 0.53] |
| 7.5 | 0.45 | 0.43 | 0.05 | [0.39 0.49] | [0.34 0.56] |
| 10 | 0.4 | 0.38 | 0.05 | [0.33 0.43] | [0.29 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.43** | **0.43** | **0.43** | **[0.32 0.56]** |  | **0.49** | **0.48** | **0.47** | **[0.34 0.68]** |  | **0.43** | **0.42** | **0.4** | **[0.27 0.71]** |
| PAS |  | 0.44 | 0.44 | 0.44 | [0.32 0.56] |  | 0.48 | 0.48 | 0.47 | [0.34 0.65] |  | 0.41 | 0.4 | 0.37 | [0.27 0.67] |
| USC |  | 0.41 | 0.41 | 0.41 | [0.33 0.55] |  | 0.5 | 0.49 | 0.47 | [0.38 0.68] |  | 0.44 | 0.43 | 0.41 | [0.3 0.71] |

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
| T-independent | 0.46 | 0.46 | 0.03 | [0.42 0.49] | [0.39 0.53] |
| 3 | 0.43 | 0.42 | 0.03 | [0.39 0.45] | [0.36 0.49] |
| 4 | 0.45 | 0.44 | 0.03 | [0.41 0.48] | [0.39 0.51] |
| 5 | 0.49 | 0.49 | 0.05 | [0.44 0.54] | [0.4 0.59] |
| 7.5 | 0.48 | 0.48 | 0.05 | [0.43 0.54] | [0.4 0.6] |
| 10 | 0.43 | 0.43 | 0.05 | [0.38 0.48] | [0.34 0.54] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.46** | **0.46** | **0.45** | **[0.34 0.6]** |  | **0.51** | **0.5** | **0.49** | **[0.35 0.7]** |  | **0.47** | **0.46** | **0.46** | **[0.31 0.7]** |
| PAS |  | 0.48 | 0.47 | 0.47 | [0.37 0.6] |  | 0.5 | 0.49 | 0.48 | [0.35 0.67] |  | 0.46 | 0.45 | 0.44 | [0.31 0.65] |
| USC |  | 0.45 | 0.45 | 0.45 | [0.34 0.57] |  | 0.52 | 0.51 | 0.5 | [0.36 0.7] |  | 0.49 | 0.48 | 0.46 | [0.35 0.7] |

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
| T-independent | 0.49 | 0.49 | 0.03 | [0.46 0.52] | [0.44 0.54] |
| 3 | 0.46 | 0.46 | 0.03 | [0.43 0.49] | [0.42 0.53] |
| 4 | 0.49 | 0.49 | 0.03 | [0.45 0.52] | [0.42 0.56] |
| 5 | 0.51 | 0.51 | 0.04 | [0.47 0.55] | [0.42 0.57] |
| 7.5 | 0.53 | 0.52 | 0.05 | [0.47 0.57] | [0.44 0.62] |
| 10 | 0.47 | 0.47 | 0.04 | [0.43 0.52] | [0.39 0.55] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.43** | **0.43** | **0.43** | **[0.3 0.6]** |  | **0.48** | **0.47** | **0.46** | **[0.3 0.7]** |  | **0.43** | **0.42** | **0.41** | **[0.19 0.71]** |
| PAS |  | 0.45 | 0.45 | 0.44 | [0.32 0.6] |  | 0.48 | 0.47 | 0.46 | [0.31 0.67] |  | 0.42 | 0.41 | 0.4 | [0.22 0.67] |
| USC |  | 0.42 | 0.41 | 0.41 | [0.3 0.57] |  | 0.49 | 0.48 | 0.47 | [0.3 0.7] |  | 0.44 | 0.43 | 0.41 | [0.19 0.71] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m6.6_3s_hist.png) | ![5s](resources/within_event_ss_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 4041 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.46 | 0.46 | 0.02 | [0.44 0.48] | [0.43 0.5] |
| 3 | 0.43 | 0.43 | 0.01 | [0.42 0.45] | [0.41 0.46] |
| 4 | 0.46 | 0.46 | 0.02 | [0.44 0.47] | [0.42 0.49] |
| 5 | 0.48 | 0.48 | 0.02 | [0.46 0.51] | [0.44 0.54] |
| 7.5 | 0.49 | 0.49 | 0.03 | [0.45 0.52] | [0.42 0.55] |
| 10 | 0.43 | 0.43 | 0.03 | [0.4 0.47] | [0.38 0.5] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **PAS** | **USC** |
|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_PAS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_PAS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_all_dists_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_all_dists_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[6.4,6.8].

![Histogram](resources/within_event_ss_event_recordings_hist_all_dists.png)


## Between-events Variability
*[(top)](#table-of-contents)*

### Between-events Variability Methodology
*[(top)](#table-of-contents)*

Between-events variability, denoted &tau; in Al Atik (2010), is computed separately for each:

* Distance *[3 unique]*

We first compute the median natural-log ground motion, &delta;B<sub>e</sub>, for each combination of:

* Rupture *[49 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 1296 combinations of:

* Site *[2 unique]*
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
| PAS | 0.16 | -4.4 | [-4.69 -3.96] | 0.21 | -4.94 | [-5.33 -4.5] | 0.23 | -5.98 | [-6.49 -5.44] |
| USC | 0.18 | -3.12 | [-3.45 -2.69] | 0.21 | -3.76 | [-4.1 -3.34] | 0.22 | -5.02 | [-5.51 -4.49] |

#### 20.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.2 | 0.22 | 0.06 | [0.16 0.28] | [0.11 0.39] |
| 3 | 0.16 | 0.18 | 0.07 | [0.11 0.26] | [0.07 0.36] |
| 4 | 0.17 | 0.19 | 0.08 | [0.1 0.29] | [0.05 0.35] |
| 5 | 0.21 | 0.21 | 0.1 | [0.12 0.32] | [0.06 0.43] |
| 7.5 | 0.24 | 0.25 | 0.11 | [0.14 0.37] | [0.07 0.53] |
| 10 | 0.23 | 0.24 | 0.1 | [0.14 0.33] | [0.06 0.51] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| PAS | 0.18 | -5.26 | [-5.57 -4.82] | 0.24 | -5.6 | [-5.96 -5.06] | 0.24 | -6.63 | [-7.16 -6.02] |
| USC | 0.19 | -3.92 | [-4.25 -3.47] | 0.23 | -4.36 | [-4.76 -3.83] | 0.23 | -5.64 | [-6.17 -5.05] |

#### 50.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.22 | 0.24 | 0.06 | [0.19 0.31] | [0.15 0.38] |
| 3 | 0.18 | 0.2 | 0.09 | [0.11 0.31] | [0.05 0.43] |
| 4 | 0.21 | 0.23 | 0.09 | [0.15 0.33] | [0.07 0.44] |
| 5 | 0.24 | 0.26 | 0.1 | [0.17 0.38] | [0.12 0.5] |
| 7.5 | 0.23 | 0.24 | 0.11 | [0.15 0.35] | [0.08 0.5] |
| 10 | 0.24 | 0.24 | 0.11 | [0.15 0.35] | [0.1 0.54] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| PAS | 0.16 | -5.86 | [-6.12 -5.47] | 0.22 | -6.25 | [-6.65 -5.74] | 0.26 | -6.99 | [-7.51 -6.33] |
| USC | 0.16 | -4.56 | [-4.85 -4.16] | 0.24 | -4.9 | [-5.4 -4.39] | 0.24 | -6.06 | [-6.51 -5.42] |

#### 100.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.19 | 0.08 | [0.14 0.27] | [0.08 0.41] |
| 3 | 0.16 | 0.15 | 0.09 | [0.07 0.26] | [0.02 0.36] |
| 4 | 0.19 | 0.2 | 0.09 | [0.11 0.29] | [0.05 0.43] |
| 5 | 0.22 | 0.2 | 0.11 | [0.1 0.32] | [0.03 0.45] |
| 7.5 | 0.23 | 0.19 | 0.13 | [0.09 0.35] | [0.02 0.51] |
| 10 | 0.26 | 0.21 | 0.15 | [0.09 0.39] | [0.04 0.61] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| PAS | 0.17 | -5.17 | [-6.12 -3.96] | 0.22 | -5.6 | [-6.65 -4.5] | 0.24 | -6.53 | [-7.51 -5.44] |
| USC | 0.18 | -3.87 | [-4.85 -2.69] | 0.23 | -4.34 | [-5.4 -3.34] | 0.23 | -5.58 | [-6.51 -4.49] |

#### All Distances M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 4041 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.21 | 0.23 | 0.03 | [0.21 0.26] | [0.19 0.3] |
| 3 | 0.17 | 0.19 | 0.03 | [0.16 0.23] | [0.14 0.26] |
| 4 | 0.19 | 0.22 | 0.03 | [0.18 0.25] | [0.15 0.28] |
| 5 | 0.22 | 0.24 | 0.04 | [0.2 0.29] | [0.16 0.34] |
| 7.5 | 0.23 | 0.26 | 0.04 | [0.22 0.3] | [0.18 0.35] |
| 10 | 0.24 | 0.26 | 0.05 | [0.21 0.31] | [0.16 0.34] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (1296), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (49), varying the number of recordings per event.

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
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_PAS_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_PAS_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_PAS_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_PAS_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_PAS_10s.png) |
### Slip Std Dev Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m6.6_100km_PAS_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_PAS_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_PAS_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_PAS_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_PAS_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_PAS_10s.png) |
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
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PAS_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
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

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
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
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
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
| **M6.6 Reverse** | **PAS** | **FAIL** | **PASS** | *(PASS)* |
| **M6.6 Reverse** | **USC** | **PASS** | **PASS** | *(PASS)* |

### BBP PartB, M6.6, Reverse, Dip=45, Ztor=3
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **PAS** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_PAS.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_PAS.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m6p6_reverse_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m6p6_reverse_100km_USC.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M6.6 | 20.0 km | PAS | [sa_PAS_m6.6_20.0km.csv.gz](resources/sa_PAS_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | USC | [sa_USC_m6.6_20.0km.csv.gz](resources/sa_USC_m6.6_20.0km.csv.gz) |
| M6.6 | 50.0 km | PAS | [sa_PAS_m6.6_50.0km.csv.gz](resources/sa_PAS_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | USC | [sa_USC_m6.6_50.0km.csv.gz](resources/sa_USC_m6.6_50.0km.csv.gz) |
| M6.6 | 100.0 km | PAS | [sa_PAS_m6.6_100.0km.csv.gz](resources/sa_PAS_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | USC | [sa_USC_m6.6_100.0km.csv.gz](resources/sa_USC_m6.6_100.0km.csv.gz) |

