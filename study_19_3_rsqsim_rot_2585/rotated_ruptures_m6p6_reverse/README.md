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
  * [Mid-Seismogenic Mean Slip Event Term Scatters](#mid-seismogenic-mean-slip-event-term-scatters)
* [Azumth Dependence](#azumth-dependence)
  * [SBSM Azumth Dependence](#sbsm-azumth-dependence)
  * [SMCA Azumth Dependence](#smca-azumth-dependence)
  * [STNI Azumth Dependence](#stni-azumth-dependence)
  * [USC Azumth Dependence](#usc-azumth-dependence)
  * [WNGC Azumth Dependence](#wngc-azumth-dependence)
  * [All Sites Azumth Dependence](#all-sites-azumth-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M6.6, Reverse, Dip=45, Ztor=3](#bbp-partb-m66-reverse-dip45-ztor3)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 100 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 5 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 36 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **972000** | Total number of combinations of the above. |

## M6.6 Reverse RSQSim Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 100 events in the catalog which match the following criteria:

* M=[6.55,6.65]
* Ztor=[1.0,5.0]
* Rake=[80,100]
* Dip=[35.0,55.0]

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| McKinleyville (alt1) | 23 |
| Cucamonga | 13 |
| San Luis Range 2011 CFM | 10 |
| Sierra Madre | 9 |
| Clamshell-Sawpit | 7 |
| Mad River (alt1) | 6 |
| Mount Diablo Thrust South | 6 |
| Los Osos 2011 | 6 |
| Table Bluff | 5 |
| Pleito | 4 |
| Big Lagoon - Bald Mtn 2011 CFM | 3 |
| Fickle Hill (alt1) | 3 |
| San Luis Range - Oceano 2011 CFM | 3 |
| Pine Mtn | 2 |
| Great Valley 06 (Midland) 2011 CFM alt1 | 2 |
| North Frontal  (East) | 1 |
| Trinidad (alt1) | 1 |
| Mount Diablo Thrust North CFM | 1 |
| TOTAL # PARENTS | 105 |

Actual magnitude range: [6.562098,6.637935], average: 6.5983825, stdDev: 0.022250667

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| SBSM | *34.064987, -117.29201* | 500 | 0.33 | 1.82 |
| SMCA | *34.00909, -118.48939* | 500 | 0.59 | 2.45 |
| STNI | *33.93088, -118.17881* | 500 | 0.88 | 5.57 |
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |
| WNGC | *34.041824, -118.0653* | 500 | 0.5 | 3.49 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.26 | 0.32 | 0.27 | 0.16 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.33 | 0.4 | 0.34 | 0.2 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.37 | 0.45 | 0.39 | 0.25 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.32 | 0.39 | 0.34 | 0.21 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.34 | 0.32 | 0.36 | 0.31 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.34 | 0.31 | 0.37 | 0.33 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.35 | 0.32 | 0.36 | 0.36 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.34 | 0.32 | 0.37 | 0.33 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.38 | 0.4 | 0.4 | 0.32 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.43 | 0.46 | 0.45 | 0.36 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.47 | 0.51 | 0.49 | 0.41 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.43 | 0.46 | 0.45 | 0.37 |
| Within-event | &phi; | 20 km | 0.42 | 0.39 | 0.41 | 0.44 |
| Within-event | &phi; | 50 km | 0.48 | 0.46 | 0.46 | 0.49 |
| Within-event | &phi; | 100 km | 0.52 | 0.49 | 0.5 | 0.53 |
| Within-event | &phi; | (all) | 0.47 | 0.45 | 0.46 | 0.49 |
| Between-events | &tau; | 20 km | 0.25 | 0.23 | 0.25 | 0.25 |
| Between-events | &tau; | 50 km | 0.25 | 0.23 | 0.27 | 0.26 |
| Between-events | &tau; | 100 km | 0.25 | 0.2 | 0.25 | 0.29 |
| Between-events | &tau; | (all) | 0.25 | 0.22 | 0.25 | 0.26 |

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

* Site *[5 unique]*
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
| **ALL SITES** |  | **0.32** | **0.3** | **0.28** | **[0.07 0.84]** |  | **0.27** | **0.26** | **0.25** | **[0.03 0.66]** |  | **0.16** | **0.15** | **0.14** | **[0.03 0.4]** |
| SBSM |  | 0.25 | 0.24 | 0.23 | [0.08 0.52] |  | 0.19 | 0.17 | 0.17 | [0.03 0.41] |  | 0.14 | 0.13 | 0.12 | [0.03 0.33] |
| SMCA |  | 0.28 | 0.27 | 0.27 | [0.13 0.51] |  | 0.3 | 0.29 | 0.28 | [0.09 0.56] |  | 0.21 | 0.2 | 0.2 | [0.05 0.4] |
| STNI |  | 0.25 | 0.24 | 0.24 | [0.07 0.44] |  | 0.24 | 0.23 | 0.23 | [0.06 0.5] |  | 0.12 | 0.11 | 0.11 | [0.03 0.27] |
| USC |  | 0.3 | 0.29 | 0.29 | [0.1 0.59] |  | 0.28 | 0.27 | 0.27 | [0.08 0.49] |  | 0.16 | 0.15 | 0.15 | [0.05 0.35] |
| WNGC |  | 0.46 | 0.45 | 0.45 | [0.1 0.84] |  | 0.33 | 0.31 | 0.31 | [0.11 0.66] |  | 0.15 | 0.14 | 0.13 | [0.03 0.36] |

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
| T-independent | 0.26 | 0.25 | 0.01 | [0.24 0.27] | [0.23 0.28] |
| 3 | 0.32 | 0.32 | 0.02 | [0.29 0.33] | [0.27 0.36] |
| 4 | 0.3 | 0.3 | 0.02 | [0.28 0.32] | [0.26 0.35] |
| 5 | 0.27 | 0.27 | 0.02 | [0.25 0.29] | [0.23 0.32] |
| 7.5 | 0.19 | 0.19 | 0.02 | [0.17 0.2] | [0.15 0.23] |
| 10 | 0.16 | 0.15 | 0.02 | [0.14 0.17] | [0.12 0.19] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_20km_WNGC_downsampled_hist_3s.png) |  |


### 50.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.4** | **0.39** | **0.38** | **[0.16 0.78]** |  | **0.34** | **0.34** | **0.33** | **[0.12 0.65]** |  | **0.2** | **0.2** | **0.19** | **[0.06 0.45]** |
| SBSM |  | 0.43 | 0.43 | 0.43 | [0.21 0.67] |  | 0.29 | 0.28 | 0.28 | [0.12 0.53] |  | 0.18 | 0.17 | 0.15 | [0.06 0.43] |
| SMCA |  | 0.4 | 0.4 | 0.39 | [0.22 0.6] |  | 0.38 | 0.38 | 0.37 | [0.2 0.65] |  | 0.25 | 0.24 | 0.24 | [0.12 0.45] |
| STNI |  | 0.3 | 0.3 | 0.3 | [0.16 0.46] |  | 0.3 | 0.3 | 0.29 | [0.18 0.44] |  | 0.17 | 0.16 | 0.16 | [0.07 0.36] |
| USC |  | 0.34 | 0.34 | 0.34 | [0.19 0.49] |  | 0.36 | 0.36 | 0.36 | [0.2 0.57] |  | 0.21 | 0.21 | 0.21 | [0.08 0.45] |
| WNGC |  | 0.5 | 0.5 | 0.5 | [0.27 0.78] |  | 0.37 | 0.37 | 0.36 | [0.21 0.57] |  | 0.2 | 0.19 | 0.18 | [0.08 0.42] |

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
| T-independent | 0.33 | 0.32 | 0.01 | [0.31 0.33] | [0.3 0.35] |
| 3 | 0.4 | 0.4 | 0.02 | [0.37 0.42] | [0.36 0.45] |
| 4 | 0.37 | 0.36 | 0.02 | [0.34 0.38] | [0.33 0.4] |
| 5 | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.31 0.37] |
| 7.5 | 0.28 | 0.28 | 0.02 | [0.26 0.29] | [0.24 0.3] |
| 10 | 0.2 | 0.2 | 0.01 | [0.19 0.22] | [0.17 0.23] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_50km_WNGC_downsampled_hist_3s.png) |  |


### 100.0 km M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.45** | **0.43** | **0.42** | **[0.19 0.83]** |  | **0.39** | **0.38** | **0.38** | **[0.18 0.61]** |  | **0.25** | **0.25** | **0.24** | **[0.1 0.46]** |
| SBSM |  | 0.54 | 0.54 | 0.54 | [0.25 0.83] |  | 0.41 | 0.41 | 0.41 | [0.22 0.58] |  | 0.22 | 0.22 | 0.2 | [0.1 0.46] |
| SMCA |  | 0.48 | 0.48 | 0.48 | [0.3 0.71] |  | 0.44 | 0.44 | 0.44 | [0.27 0.61] |  | 0.28 | 0.28 | 0.28 | [0.16 0.45] |
| STNI |  | 0.31 | 0.31 | 0.31 | [0.19 0.51] |  | 0.35 | 0.35 | 0.35 | [0.21 0.49] |  | 0.24 | 0.24 | 0.23 | [0.13 0.43] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.24 0.56] |  | 0.36 | 0.36 | 0.35 | [0.24 0.52] |  | 0.27 | 0.27 | 0.27 | [0.16 0.41] |
| WNGC |  | 0.49 | 0.48 | 0.47 | [0.26 0.83] |  | 0.37 | 0.37 | 0.37 | [0.18 0.57] |  | 0.22 | 0.22 | 0.21 | [0.13 0.41] |

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
| T-independent | 0.37 | 0.37 | 0.01 | [0.36 0.38] | [0.35 0.4] |
| 3 | 0.45 | 0.44 | 0.02 | [0.43 0.47] | [0.4 0.49] |
| 4 | 0.42 | 0.42 | 0.02 | [0.41 0.44] | [0.38 0.47] |
| 5 | 0.39 | 0.39 | 0.02 | [0.37 0.4] | [0.35 0.43] |
| 7.5 | 0.32 | 0.32 | 0.02 | [0.3 0.34] | [0.29 0.35] |
| 10 | 0.25 | 0.25 | 0.01 | [0.23 0.26] | [0.22 0.27] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_100km_WNGC_downsampled_hist_3s.png) |  |


### All Distances M6.6 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m6.6_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.38** | **0.36** | **[0.07 0.84]** |  | **0.34** | **0.33** | **0.33** | **[0.03 0.66]** |  | **0.21** | **0.2** | **0.19** | **[0.03 0.46]** |
| SBSM |  | 0.43 | 0.4 | 0.41 | [0.08 0.83] |  | 0.31 | 0.29 | 0.28 | [0.03 0.58] |  | 0.18 | 0.17 | 0.16 | [0.03 0.46] |
| SMCA |  | 0.4 | 0.38 | 0.39 | [0.13 0.71] |  | 0.38 | 0.37 | 0.37 | [0.09 0.65] |  | 0.25 | 0.24 | 0.24 | [0.05 0.45] |
| STNI |  | 0.29 | 0.29 | 0.29 | [0.07 0.51] |  | 0.3 | 0.29 | 0.3 | [0.06 0.5] |  | 0.18 | 0.17 | 0.17 | [0.03 0.43] |
| USC |  | 0.33 | 0.33 | 0.33 | [0.1 0.59] |  | 0.34 | 0.33 | 0.33 | [0.08 0.57] |  | 0.22 | 0.21 | 0.21 | [0.05 0.45] |
| WNGC |  | 0.49 | 0.48 | 0.47 | [0.1 0.84] |  | 0.36 | 0.35 | 0.35 | [0.11 0.66] |  | 0.19 | 0.18 | 0.18 | [0.03 0.42] |

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
| T-independent | 0.32 | 0.32 | 0.01 | [0.32 0.33] | [0.31 0.34] |
| 3 | 0.39 | 0.39 | 0.01 | [0.38 0.4] | [0.37 0.42] |
| 4 | 0.37 | 0.37 | 0.01 | [0.36 0.37] | [0.35 0.39] |
| 5 | 0.34 | 0.33 | 0.01 | [0.33 0.34] | [0.32 0.35] |
| 7.5 | 0.27 | 0.27 | 0.01 | [0.26 0.28] | [0.25 0.28] |
| 10 | 0.21 | 0.21 | 0.01 | [0.2 0.21] | [0.19 0.22] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m6.6_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m6.6_WNGC_downsampled_hist_3s.png) |  |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[5 unique]*
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
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.09 0.68]** |  | **0.36** | **0.35** | **0.34** | **[0.08 0.77]** |  | **0.31** | **0.3** | **0.28** | **[0.06 0.84]** |
| SBSM |  | 0.36 | 0.35 | 0.34 | [0.14 0.68] |  | 0.38 | 0.37 | 0.36 | [0.11 0.68] |  | 0.31 | 0.3 | 0.3 | [0.15 0.56] |
| SMCA |  | 0.33 | 0.32 | 0.31 | [0.1 0.66] |  | 0.38 | 0.37 | 0.37 | [0.11 0.77] |  | 0.32 | 0.31 | 0.3 | [0.08 0.84] |
| STNI |  | 0.29 | 0.28 | 0.27 | [0.1 0.6] |  | 0.32 | 0.31 | 0.3 | [0.09 0.72] |  | 0.3 | 0.28 | 0.26 | [0.06 0.83] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.65] |  | 0.34 | 0.33 | 0.32 | [0.09 0.65] |  | 0.3 | 0.29 | 0.27 | [0.06 0.84] |
| WNGC |  | 0.33 | 0.32 | 0.31 | [0.1 0.65] |  | 0.37 | 0.36 | 0.35 | [0.08 0.71] |  | 0.31 | 0.3 | 0.28 | [0.07 0.74] |

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
| T-independent | 0.34 | 0.33 | 0.02 | [0.32 0.35] | [0.3 0.37] |
| 3 | 0.32 | 0.32 | 0.02 | [0.29 0.34] | [0.28 0.36] |
| 4 | 0.33 | 0.33 | 0.02 | [0.31 0.35] | [0.28 0.39] |
| 5 | 0.36 | 0.36 | 0.03 | [0.33 0.38] | [0.3 0.41] |
| 7.5 | 0.36 | 0.35 | 0.03 | [0.32 0.38] | [0.3 0.42] |
| 10 | 0.31 | 0.3 | 0.02 | [0.28 0.33] | [0.26 0.37] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_20km_WNGC_downsampled_hist_3s.png) |  |


### 50.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.31** | **0.3** | **0.3** | **[0.07 0.77]** |  | **0.37** | **0.36** | **0.35** | **[0.06 0.78]** |  | **0.33** | **0.33** | **0.31** | **[0.08 0.89]** |
| SBSM |  | 0.38 | 0.37 | 0.36 | [0.11 0.75] |  | 0.4 | 0.39 | 0.38 | [0.1 0.7] |  | 0.33 | 0.32 | 0.32 | [0.11 0.71] |
| SMCA |  | 0.32 | 0.31 | 0.3 | [0.07 0.77] |  | 0.39 | 0.38 | 0.37 | [0.09 0.78] |  | 0.33 | 0.32 | 0.31 | [0.08 0.78] |
| STNI |  | 0.28 | 0.27 | 0.26 | [0.09 0.62] |  | 0.35 | 0.34 | 0.33 | [0.09 0.74] |  | 0.35 | 0.34 | 0.32 | [0.13 0.89] |
| USC |  | 0.29 | 0.28 | 0.27 | [0.09 0.67] |  | 0.35 | 0.34 | 0.33 | [0.09 0.72] |  | 0.34 | 0.32 | 0.31 | [0.1 0.88] |
| WNGC |  | 0.3 | 0.29 | 0.28 | [0.08 0.69] |  | 0.37 | 0.35 | 0.35 | [0.06 0.68] |  | 0.33 | 0.32 | 0.31 | [0.1 0.76] |

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
| T-independent | 0.34 | 0.34 | 0.02 | [0.32 0.36] | [0.3 0.38] |
| 3 | 0.31 | 0.31 | 0.03 | [0.29 0.34] | [0.26 0.38] |
| 4 | 0.34 | 0.34 | 0.03 | [0.31 0.36] | [0.28 0.39] |
| 5 | 0.37 | 0.37 | 0.03 | [0.34 0.4] | [0.31 0.42] |
| 7.5 | 0.36 | 0.36 | 0.03 | [0.33 0.38] | [0.3 0.41] |
| 10 | 0.33 | 0.33 | 0.03 | [0.3 0.36] | [0.28 0.39] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_50km_WNGC_downsampled_hist_3s.png) |  |


### 100.0 km M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.09 0.78]** |  | **0.36** | **0.35** | **0.35** | **[0.06 0.75]** |  | **0.36** | **0.35** | **0.34** | **[0.08 0.94]** |
| SBSM |  | 0.35 | 0.34 | 0.33 | [0.1 0.77] |  | 0.36 | 0.35 | 0.35 | [0.1 0.7] |  | 0.33 | 0.33 | 0.32 | [0.1 0.78] |
| SMCA |  | 0.31 | 0.3 | 0.29 | [0.1 0.73] |  | 0.35 | 0.34 | 0.34 | [0.07 0.68] |  | 0.35 | 0.34 | 0.33 | [0.08 0.85] |
| STNI |  | 0.3 | 0.29 | 0.29 | [0.09 0.73] |  | 0.36 | 0.35 | 0.35 | [0.08 0.71] |  | 0.38 | 0.37 | 0.36 | [0.1 0.94] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.75] |  | 0.36 | 0.35 | 0.34 | [0.09 0.85] |
| WNGC |  | 0.32 | 0.31 | 0.3 | [0.09 0.78] |  | 0.38 | 0.37 | 0.36 | [0.06 0.69] |  | 0.36 | 0.35 | 0.34 | [0.08 0.86] |

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
| T-independent | 0.35 | 0.35 | 0.02 | [0.33 0.37] | [0.31 0.41] |
| 3 | 0.32 | 0.31 | 0.03 | [0.28 0.34] | [0.26 0.37] |
| 4 | 0.34 | 0.34 | 0.03 | [0.31 0.37] | [0.28 0.4] |
| 5 | 0.36 | 0.37 | 0.02 | [0.34 0.39] | [0.32 0.43] |
| 7.5 | 0.37 | 0.38 | 0.03 | [0.34 0.41] | [0.32 0.46] |
| 10 | 0.36 | 0.36 | 0.03 | [0.34 0.4] | [0.31 0.45] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_100km_WNGC_downsampled_hist_3s.png) |  |


### All Distances M6.6 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m6.6_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.31** | **0.3** | **[0.07 0.78]** |  | **0.37** | **0.35** | **0.35** | **[0.06 0.78]** |  | **0.33** | **0.32** | **0.31** | **[0.06 0.94]** |
| SBSM |  | 0.36 | 0.35 | 0.35 | [0.1 0.77] |  | 0.38 | 0.37 | 0.36 | [0.1 0.7] |  | 0.32 | 0.32 | 0.31 | [0.1 0.78] |
| SMCA |  | 0.32 | 0.31 | 0.3 | [0.07 0.77] |  | 0.38 | 0.36 | 0.36 | [0.07 0.78] |  | 0.34 | 0.33 | 0.31 | [0.08 0.85] |
| STNI |  | 0.29 | 0.28 | 0.27 | [0.09 0.73] |  | 0.35 | 0.33 | 0.33 | [0.08 0.74] |  | 0.34 | 0.33 | 0.32 | [0.06 0.94] |
| USC |  | 0.3 | 0.29 | 0.28 | [0.09 0.75] |  | 0.35 | 0.34 | 0.33 | [0.09 0.75] |  | 0.33 | 0.32 | 0.31 | [0.06 0.88] |
| WNGC |  | 0.32 | 0.31 | 0.3 | [0.08 0.78] |  | 0.37 | 0.36 | 0.35 | [0.06 0.71] |  | 0.33 | 0.32 | 0.31 | [0.07 0.86] |

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
| T-independent | 0.34 | 0.34 | 0.01 | [0.33 0.35] | [0.33 0.36] |
| 3 | 0.32 | 0.32 | 0.01 | [0.3 0.33] | [0.3 0.34] |
| 4 | 0.34 | 0.33 | 0.01 | [0.32 0.35] | [0.32 0.36] |
| 5 | 0.37 | 0.36 | 0.01 | [0.35 0.38] | [0.34 0.38] |
| 7.5 | 0.36 | 0.36 | 0.01 | [0.35 0.38] | [0.34 0.39] |
| 10 | 0.33 | 0.33 | 0.01 | [0.32 0.34] | [0.31 0.36] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m6.6_WNGC_downsampled_hist_3s.png) |  |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[5 unique]*
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
| **ALL SITES** |  | **0.4** | **0.39** | **0.36** | **[0.24 0.66]** |  | **0.4** | **0.39** | **0.39** | **[0.24 0.63]** |  | **0.32** | **0.31** | **0.3** | **[0.13 0.67]** |
| SBSM |  | 0.39 | 0.39 | 0.38 | [0.28 0.59] |  | 0.4 | 0.39 | 0.38 | [0.24 0.61] |  | 0.32 | 0.31 | 0.31 | [0.21 0.47] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.28 0.55] |  | 0.42 | 0.41 | 0.41 | [0.3 0.59] |  | 0.36 | 0.35 | 0.34 | [0.22 0.65] |
| STNI |  | 0.32 | 0.32 | 0.32 | [0.24 0.47] |  | 0.35 | 0.35 | 0.35 | [0.25 0.49] |  | 0.3 | 0.28 | 0.27 | [0.13 0.67] |
| USC |  | 0.36 | 0.36 | 0.35 | [0.27 0.52] |  | 0.38 | 0.38 | 0.38 | [0.28 0.55] |  | 0.32 | 0.3 | 0.29 | [0.19 0.66] |
| WNGC |  | 0.51 | 0.51 | 0.5 | [0.41 0.66] |  | 0.45 | 0.44 | 0.44 | [0.29 0.63] |  | 0.32 | 0.3 | 0.29 | [0.18 0.62] |

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
| T-independent | 0.38 | 0.37 | 0.02 | [0.36 0.39] | [0.35 0.42] |
| 3 | 0.4 | 0.39 | 0.02 | [0.38 0.42] | [0.35 0.44] |
| 4 | 0.4 | 0.39 | 0.02 | [0.37 0.42] | [0.36 0.44] |
| 5 | 0.4 | 0.4 | 0.02 | [0.38 0.42] | [0.36 0.44] |
| 7.5 | 0.37 | 0.37 | 0.03 | [0.35 0.4] | [0.31 0.45] |
| 10 | 0.32 | 0.32 | 0.03 | [0.29 0.35] | [0.28 0.38] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_20km_WNGC_downsampled_hist_3s.png) |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.46** | **0.45** | **0.44** | **[0.31 0.74]** |  | **0.45** | **0.45** | **0.44** | **[0.31 0.65]** |  | **0.36** | **0.35** | **0.34** | **[0.22 0.77]** |
| SBSM |  | 0.52 | 0.52 | 0.52 | [0.38 0.74] |  | 0.46 | 0.45 | 0.44 | [0.31 0.64] |  | 0.35 | 0.35 | 0.33 | [0.22 0.59] |
| SMCA |  | 0.45 | 0.45 | 0.45 | [0.39 0.62] |  | 0.48 | 0.48 | 0.47 | [0.38 0.65] |  | 0.38 | 0.38 | 0.36 | [0.26 0.69] |
| STNI |  | 0.36 | 0.36 | 0.36 | [0.31 0.53] |  | 0.41 | 0.41 | 0.4 | [0.31 0.55] |  | 0.36 | 0.35 | 0.33 | [0.23 0.77] |
| USC |  | 0.4 | 0.4 | 0.39 | [0.34 0.56] |  | 0.45 | 0.44 | 0.44 | [0.35 0.61] |  | 0.37 | 0.36 | 0.35 | [0.25 0.71] |
| WNGC |  | 0.54 | 0.54 | 0.53 | [0.44 0.64] |  | 0.46 | 0.46 | 0.45 | [0.37 0.58] |  | 0.35 | 0.34 | 0.33 | [0.24 0.65] |

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
| T-independent | 0.43 | 0.42 | 0.02 | [0.41 0.45] | [0.39 0.47] |
| 3 | 0.46 | 0.46 | 0.02 | [0.43 0.49] | [0.42 0.51] |
| 4 | 0.45 | 0.44 | 0.02 | [0.42 0.46] | [0.4 0.51] |
| 5 | 0.45 | 0.45 | 0.02 | [0.42 0.47] | [0.4 0.51] |
| 7.5 | 0.41 | 0.41 | 0.03 | [0.39 0.44] | [0.37 0.47] |
| 10 | 0.36 | 0.36 | 0.03 | [0.33 0.39] | [0.31 0.44] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_50km_WNGC_downsampled_hist_3s.png) |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.51** | **0.5** | **0.5** | **[0.32 0.77]** |  | **0.49** | **0.48** | **0.48** | **[0.35 0.63]** |  | **0.41** | **0.4** | **0.39** | **[0.25 0.82]** |
| SBSM |  | 0.6 | 0.59 | 0.6 | [0.43 0.77] |  | 0.51 | 0.5 | 0.5 | [0.41 0.63] |  | 0.38 | 0.37 | 0.36 | [0.25 0.67] |
| SMCA |  | 0.53 | 0.53 | 0.53 | [0.43 0.71] |  | 0.52 | 0.52 | 0.51 | [0.42 0.62] |  | 0.42 | 0.42 | 0.4 | [0.33 0.78] |
| STNI |  | 0.39 | 0.39 | 0.38 | [0.32 0.62] |  | 0.46 | 0.46 | 0.45 | [0.35 0.6] |  | 0.42 | 0.41 | 0.4 | [0.3 0.82] |
| USC |  | 0.43 | 0.43 | 0.42 | [0.35 0.64] |  | 0.46 | 0.46 | 0.45 | [0.37 0.59] |  | 0.42 | 0.42 | 0.4 | [0.31 0.79] |
| WNGC |  | 0.55 | 0.54 | 0.53 | [0.41 0.75] |  | 0.48 | 0.48 | 0.48 | [0.38 0.6] |  | 0.4 | 0.39 | 0.37 | [0.28 0.76] |

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
| T-independent | 0.47 | 0.47 | 0.02 | [0.45 0.49] | [0.44 0.51] |
| 3 | 0.51 | 0.5 | 0.02 | [0.48 0.53] | [0.47 0.55] |
| 4 | 0.5 | 0.5 | 0.02 | [0.48 0.52] | [0.47 0.54] |
| 5 | 0.49 | 0.48 | 0.02 | [0.46 0.51] | [0.45 0.53] |
| 7.5 | 0.45 | 0.45 | 0.03 | [0.43 0.47] | [0.41 0.52] |
| 10 | 0.41 | 0.4 | 0.03 | [0.37 0.43] | [0.36 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_100km_WNGC_downsampled_hist_3s.png) |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **ALL SITES** |  | **0.46** | **0.45** | **0.43** | **[0.24 0.77]** |  | **0.45** | **0.44** | **0.44** | **[0.24 0.65]** |  | **0.37** | **0.35** | **0.35** | **[0.13 0.82]** |
| SBSM |  | 0.51 | 0.5 | 0.51 | [0.28 0.77] |  | 0.46 | 0.45 | 0.45 | [0.24 0.64] |  | 0.35 | 0.34 | 0.34 | [0.21 0.67] |
| SMCA |  | 0.46 | 0.45 | 0.45 | [0.28 0.71] |  | 0.47 | 0.47 | 0.47 | [0.3 0.65] |  | 0.39 | 0.38 | 0.37 | [0.22 0.78] |
| STNI |  | 0.36 | 0.36 | 0.35 | [0.24 0.62] |  | 0.41 | 0.4 | 0.4 | [0.25 0.6] |  | 0.36 | 0.35 | 0.34 | [0.13 0.82] |
| USC |  | 0.4 | 0.39 | 0.39 | [0.27 0.64] |  | 0.43 | 0.43 | 0.43 | [0.28 0.61] |  | 0.37 | 0.36 | 0.35 | [0.19 0.79] |
| WNGC |  | 0.53 | 0.53 | 0.52 | [0.41 0.75] |  | 0.46 | 0.46 | 0.46 | [0.29 0.63] |  | 0.35 | 0.34 | 0.34 | [0.18 0.76] |

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
| T-independent | 0.43 | 0.43 | 0.01 | [0.42 0.43] | [0.41 0.44] |
| 3 | 0.46 | 0.46 | 0.01 | [0.45 0.47] | [0.44 0.48] |
| 4 | 0.45 | 0.45 | 0.01 | [0.44 0.46] | [0.43 0.47] |
| 5 | 0.45 | 0.44 | 0.01 | [0.43 0.46] | [0.43 0.47] |
| 7.5 | 0.41 | 0.41 | 0.01 | [0.4 0.43] | [0.39 0.44] |
| 10 | 0.37 | 0.36 | 0.01 | [0.35 0.38] | [0.34 0.39] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **SBSM** | **SMCA** | **STNI** |
|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SBSM_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_STNI_downsampled_hist_period_indep.png) |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SBSM_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_STNI_downsampled_hist_3s.png) |
| Period-Indep | **USC** | **WNGC** |  |
| Period | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WNGC_downsampled_hist_period_indep.png) |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m6.6_WNGC_downsampled_hist_3s.png) |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (648), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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

* Rupture *[100 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 3240 combinations of:

* Site *[5 unique]* (Singleton)
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
| **5 sites, V<sub>S30</sub>=500** |  | **0.39** | **0.39** | **0.38** | **[0.01 1.07]** |  | **0.41** | **0.4** | **0.39** | **[0.03 1.21]** |  | **0.44** | **0.45** | **0.44** | **[0.01 1.18]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_20km_3s_hist.png) | ![5s](resources/within_event_m6.6_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_20km_10s_hist.png) |  |

#### 20.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 20 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 85 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.42 | 0.41 | 0.05 | [0.36 0.46] | [0.32 0.53] |
| 3 | 0.39 | 0.38 | 0.08 | [0.3 0.46] | [0.23 0.56] |
| 4 | 0.38 | 0.37 | 0.08 | [0.31 0.45] | [0.24 0.55] |
| 5 | 0.41 | 0.4 | 0.07 | [0.34 0.47] | [0.28 0.59] |
| 7.5 | 0.48 | 0.46 | 0.08 | [0.38 0.54] | [0.32 0.64] |
| 10 | 0.44 | 0.43 | 0.07 | [0.37 0.5] | [0.31 0.6] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_20km_downsampled_hist_3s.png) |


### 50.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.46** | **0.46** | **0.45** | **[0.02 1.25]** |  | **0.46** | **0.46** | **0.44** | **[0.03 1.47]** |  | **0.49** | **0.5** | **0.49** | **[0.01 1.36]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_50km_3s_hist.png) | ![5s](resources/within_event_m6.6_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_50km_10s_hist.png) |  |

#### 50.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 17 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 64 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.48 | 0.46 | 0.06 | [0.39 0.53] | [0.34 0.59] |
| 3 | 0.46 | 0.45 | 0.08 | [0.38 0.51] | [0.27 0.62] |
| 4 | 0.44 | 0.42 | 0.08 | [0.34 0.5] | [0.23 0.58] |
| 5 | 0.46 | 0.44 | 0.1 | [0.34 0.55] | [0.23 0.64] |
| 7.5 | 0.53 | 0.53 | 0.11 | [0.41 0.62] | [0.32 0.75] |
| 10 | 0.49 | 0.48 | 0.09 | [0.41 0.56] | [0.3 0.68] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_50km_downsampled_hist_3s.png) |


### 100.0 km M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.49** | **0.49** | **0.48** | **[0.03 1.6]** |  | **0.5** | **0.5** | **0.49** | **[0.01 1.37]** |  | **0.53** | **0.53** | **0.52** | **[0.04 1.46]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_100km_3s_hist.png) | ![5s](resources/within_event_m6.6_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_100km_10s_hist.png) |  |

#### 100.0 km M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 15 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 130 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.52 | 0.51 | 0.08 | [0.43 0.6] | [0.36 0.68] |
| 3 | 0.49 | 0.48 | 0.11 | [0.36 0.59] | [0.3 0.68] |
| 4 | 0.49 | 0.49 | 0.1 | [0.39 0.58] | [0.31 0.73] |
| 5 | 0.5 | 0.49 | 0.12 | [0.4 0.63] | [0.3 0.79] |
| 7.5 | 0.57 | 0.57 | 0.11 | [0.47 0.67] | [0.3 0.81] |
| 10 | 0.53 | 0.54 | 0.1 | [0.42 0.63] | [0.35 0.72] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m6.6_100km_downsampled_hist_3s.png) |


### All Distances M6.6 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m6.6_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **5 sites, V<sub>S30</sub>=500** |  | **0.45** | **0.44** | **0.43** | **[0.01 1.6]** |  | **0.46** | **0.45** | **0.44** | **[0.01 1.47]** |  | **0.49** | **0.49** | **0.48** | **[0.01 1.46]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m6.6_3s_hist.png) | ![5s](resources/within_event_m6.6_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m6.6_10s_hist.png) |  |

#### All Distances M6.6 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 93 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 1254 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.47 | 0.46 | 0.03 | [0.44 0.49] | [0.4 0.51] |
| 3 | 0.45 | 0.44 | 0.03 | [0.41 0.48] | [0.37 0.5] |
| 4 | 0.44 | 0.43 | 0.03 | [0.39 0.45] | [0.35 0.51] |
| 5 | 0.46 | 0.45 | 0.03 | [0.42 0.48] | [0.36 0.53] |
| 7.5 | 0.53 | 0.51 | 0.04 | [0.47 0.55] | [0.43 0.6] |
| 10 | 0.49 | 0.48 | 0.04 | [0.44 0.51] | [0.41 0.56] |

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

* Rupture *[100 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 3240 combinations of:

* Site *[5 unique]*
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
| SBSM | 0.28 | -3.19 | [-3.85 -2.5] | 0.27 | -4.2 | [-4.85 -3.5] | 0.22 | -5.94 | [-6.64 -5.51] |
| SMCA | 0.21 | -3.36 | [-3.8 -2.83] | 0.25 | -3.86 | [-4.53 -3.25] | 0.25 | -5.38 | [-6.04 -4.81] |
| STNI | 0.21 | -3.3 | [-3.78 -2.81] | 0.23 | -3.89 | [-4.44 -3.41] | 0.27 | -5.01 | [-5.7 -4.38] |
| USC | 0.23 | -3.42 | [-3.99 -2.87] | 0.25 | -4.06 | [-4.67 -3.49] | 0.26 | -5.41 | [-6.1 -4.83] |
| WNGC | 0.23 | -3.48 | [-3.97 -2.93] | 0.27 | -4.1 | [-4.68 -3.47] | 0.25 | -5.55 | [-6.22 -4.99] |

#### 20.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 105 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.27 | 0.07 | [0.2 0.35] | [0.17 0.4] |
| 3 | 0.23 | 0.24 | 0.1 | [0.14 0.35] | [0.06 0.42] |
| 4 | 0.25 | 0.25 | 0.11 | [0.17 0.4] | [0.09 0.48] |
| 5 | 0.25 | 0.27 | 0.11 | [0.17 0.4] | [0.12 0.51] |
| 7.5 | 0.27 | 0.3 | 0.11 | [0.19 0.4] | [0.07 0.51] |
| 10 | 0.25 | 0.29 | 0.1 | [0.16 0.36] | [0.08 0.46] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **5 sites, V<sub>S30</sub>=500** | **0.23** | **-4.14** | **[-4.62 -3.6]** | **0.27** | **-4.63** | **[-5.35 -3.9]** | **0.26** | **-6.07** | **[-6.8 -5.37]** |
| SBSM | 0.31 | -3.89 | [-4.53 -3.2] | 0.28 | -4.83 | [-5.55 -4.08] | 0.23 | -6.55 | [-7.26 -6] |
| SMCA | 0.19 | -4.26 | [-4.68 -3.79] | 0.26 | -4.61 | [-5.25 -3.88] | 0.25 | -6.04 | [-6.73 -5.34] |
| STNI | 0.2 | -4.02 | [-4.5 -3.56] | 0.26 | -4.36 | [-5.04 -3.67] | 0.29 | -5.51 | [-6.23 -4.71] |
| USC | 0.24 | -4.23 | [-4.75 -3.64] | 0.26 | -4.69 | [-5.4 -3.99] | 0.27 | -6 | [-6.75 -5.26] |
| WNGC | 0.23 | -4.29 | [-4.81 -3.71] | 0.27 | -4.68 | [-5.41 -3.95] | 0.26 | -6.18 | [-6.9 -5.46] |

#### 50.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 81 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.29 | 0.08 | [0.21 0.37] | [0.15 0.46] |
| 3 | 0.23 | 0.25 | 0.11 | [0.15 0.39] | [0.06 0.55] |
| 4 | 0.26 | 0.27 | 0.13 | [0.16 0.44] | [0.06 0.58] |
| 5 | 0.27 | 0.28 | 0.12 | [0.17 0.43] | [0.06 0.57] |
| 7.5 | 0.25 | 0.28 | 0.11 | [0.18 0.39] | [0.11 0.55] |
| 10 | 0.26 | 0.29 | 0.11 | [0.19 0.41] | [0.1 0.55] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **5 sites, V<sub>S30</sub>=500** | **0.2** | **-4.77** | **[-5.24 -4.3]** | **0.25** | **-5.23** | **[-5.83 -4.57]** | **0.29** | **-6.52** | **[-7.22 -5.76]** |
| SBSM | 0.3 | -4.6 | [-5.16 -3.87] | 0.26 | -5.51 | [-6.2 -4.87] | 0.25 | -7.03 | [-7.71 -6.4] |
| SMCA | 0.18 | -4.86 | [-5.27 -4.5] | 0.24 | -5.18 | [-5.72 -4.54] | 0.3 | -6.48 | [-7.22 -5.71] |
| STNI | 0.18 | -4.65 | [-5.08 -4.22] | 0.25 | -4.92 | [-5.5 -4.23] | 0.3 | -5.97 | [-6.67 -5.18] |
| USC | 0.21 | -4.87 | [-5.35 -4.37] | 0.26 | -5.23 | [-5.85 -4.55] | 0.3 | -6.44 | [-7.14 -5.67] |
| WNGC | 0.2 | -4.88 | [-5.36 -4.43] | 0.25 | -5.32 | [-5.94 -4.66] | 0.29 | -6.58 | [-7.27 -5.81] |

#### 100.0 km M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 145 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.24 | 0.08 | [0.16 0.32] | [0.1 0.4] |
| 3 | 0.2 | 0.2 | 0.11 | [0.11 0.34] | [0.03 0.49] |
| 4 | 0.24 | 0.25 | 0.13 | [0.12 0.39] | [0.05 0.51] |
| 5 | 0.25 | 0.22 | 0.12 | [0.12 0.37] | [0.04 0.57] |
| 7.5 | 0.26 | 0.24 | 0.13 | [0.11 0.39] | [0.02 0.55] |
| 10 | 0.29 | 0.23 | 0.14 | [0.11 0.4] | [0.05 0.62] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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
| **5 sites, V<sub>S30</sub>=500** | **0.22** | **-4.09** | **[-5.24 -2.8]** | **0.25** | **-4.63** | **[-5.83 -3.42]** | **0.26** | **-6.01** | **[-7.22 -4.89]** |
| SBSM | 0.3 | -3.89 | [-5.16 -2.5] | 0.27 | -4.85 | [-6.2 -3.5] | 0.23 | -6.51 | [-7.71 -5.51] |
| SMCA | 0.19 | -4.16 | [-5.27 -2.83] | 0.25 | -4.55 | [-5.72 -3.25] | 0.27 | -5.96 | [-7.22 -4.81] |
| STNI | 0.2 | -3.99 | [-5.08 -2.81] | 0.25 | -4.39 | [-5.5 -3.41] | 0.29 | -5.5 | [-6.67 -4.38] |
| USC | 0.22 | -4.17 | [-5.35 -2.87] | 0.26 | -4.66 | [-5.85 -3.49] | 0.28 | -5.95 | [-7.14 -4.83] |
| WNGC | 0.22 | -4.22 | [-5.36 -2.93] | 0.27 | -4.7 | [-5.94 -3.47] | 0.27 | -6.1 | [-7.27 -4.99] |

#### All Distances M6.6 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [6.4 6.8], and all distances. We throw out any events with only 1 recording, leaving us with 7 events and a total of 4041 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.27 | 0.03 | [0.23 0.3] | [0.2 0.34] |
| 3 | 0.22 | 0.24 | 0.04 | [0.2 0.27] | [0.17 0.33] |
| 4 | 0.25 | 0.26 | 0.04 | [0.22 0.31] | [0.19 0.37] |
| 5 | 0.25 | 0.28 | 0.05 | [0.23 0.32] | [0.19 0.38] |
| 7.5 | 0.26 | 0.28 | 0.05 | [0.23 0.33] | [0.19 0.39] |
| 10 | 0.26 | 0.28 | 0.05 | [0.22 0.33] | [0.18 0.41] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m6.6_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (100), varying the number of recordings per event.

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

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m6.6_100km_5sites_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_mag_m6.6_100km_5sites_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_area_m6.6_100km_5sites_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m6.6_100km_5sites_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m6.6_100km_5sites_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

| Distance | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_5sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_5sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_20km_5sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_5sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_5sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_50km_5sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_5sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_5sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m6.6_100km_5sites_10s.png) |
## Azumth Dependence
*[(top)](#table-of-contents)*

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **Median SA** | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m6.6_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **&phi;** | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m6.6_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
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
| M6.6 | 20.0 km | SBSM | [sa_SBSM_m6.6_20.0km.csv.gz](resources/sa_SBSM_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | SMCA | [sa_SMCA_m6.6_20.0km.csv.gz](resources/sa_SMCA_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | STNI | [sa_STNI_m6.6_20.0km.csv.gz](resources/sa_STNI_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | USC | [sa_USC_m6.6_20.0km.csv.gz](resources/sa_USC_m6.6_20.0km.csv.gz) |
| M6.6 | 20.0 km | WNGC | [sa_WNGC_m6.6_20.0km.csv.gz](resources/sa_WNGC_m6.6_20.0km.csv.gz) |
| M6.6 | 50.0 km | SBSM | [sa_SBSM_m6.6_50.0km.csv.gz](resources/sa_SBSM_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | SMCA | [sa_SMCA_m6.6_50.0km.csv.gz](resources/sa_SMCA_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | STNI | [sa_STNI_m6.6_50.0km.csv.gz](resources/sa_STNI_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | USC | [sa_USC_m6.6_50.0km.csv.gz](resources/sa_USC_m6.6_50.0km.csv.gz) |
| M6.6 | 50.0 km | WNGC | [sa_WNGC_m6.6_50.0km.csv.gz](resources/sa_WNGC_m6.6_50.0km.csv.gz) |
| M6.6 | 100.0 km | SBSM | [sa_SBSM_m6.6_100.0km.csv.gz](resources/sa_SBSM_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | SMCA | [sa_SMCA_m6.6_100.0km.csv.gz](resources/sa_SMCA_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | STNI | [sa_STNI_m6.6_100.0km.csv.gz](resources/sa_STNI_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | USC | [sa_USC_m6.6_100.0km.csv.gz](resources/sa_USC_m6.6_100.0km.csv.gz) |
| M6.6 | 100.0 km | WNGC | [sa_WNGC_m6.6_100.0km.csv.gz](resources/sa_WNGC_m6.6_100.0km.csv.gz) |

