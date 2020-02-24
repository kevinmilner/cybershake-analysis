# rundir4860_multi_combine Rotated Rupture Variability, M7.2 SS

This exercise uses translations and rotations to estimate ground motion variability from different sources. We begin by selecting a subset of similar ruptures which match a set of criteria (in this case, M7.2, Vertical Strike-Slip with Surface Rupture). Each rupture is then reoriented such that its strike (following the Aki & Richards 1980 convention) is 0 degrees (due North, dipping to the right for normal or reverse ruptures). For each site, ruptures are translated such that their scalar seismic moment centroid is directly North of the site, and their 3-dimensional distance (Rrup) is as specified (we consider 3 distance[s] here).

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
* [M7.2 SS Rupture Match Criteria](#m72-ss-rupture-match-criteria)
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
  * [Rupture Strike Dependence](#rupture-strike-dependence)
  * [Path Dependence](#path-dependence)
* [BBP PartB Comparison](#bbp-partb-comparison)
  * [BBP PartB Summary Table](#bbp-partb-summary-table)
  * [BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m72-vertical-strike-slip-with-surface-rupture)
* [CSV Files](#csv-files)
## Rupture Rotation Parameters

| Quantity | Variations | Description |
|-----|-----|-----|
| Rupture | 50 | Unique (but similar in faulting style and magnitude) ruptures which match the given scenario. |
| Site | 1 | Unique site locations. If 3-d, each will have unique velocity profiles. |
| Rupture Strike | 18 | Rupture strike conforming to the Aki & Richards (1980) convention, where dipping faults dip to the right of the rupture. If path rotation is also performed, this azimuth is relative to the path. |
| Path | 18 | Path from the site to the centroid of the rupture, in azimuthal degrees (0 is North) |
| Distance | 20.0, 50.0, 100.0 km | 3-dimensional distance between the site and the rupture surface. |
| **Total # Simulations** | **48600** | Total number of combinations of the above. |

## M7.2 SS Rupture Match Criteria
*[(top)](#table-of-contents)*

We condisder 50 events which match the following criteria:

* M=[7.15,7.25]
* Ztor=[0.0,1.0]
* Rake=[-180,-170] or [-10,10] or [170,180]
* Dip=90.0
* Linear rupture (max 5.0% deviation from ideal)

In the case of more than 50 available matches, we use the Sect Variability filter method: Minimizes parent fault section duplication

### Fault Section Counts
*[(top)](#table-of-contents)*

This tables gives a list of all fault sections which participate in the ruptures matching the above criteria. Many ruptures include multiple sections, so the sum of counts may be larger than the number of events.

| Section Name | Participation Count |
|-----|-----|
| Earthquake Valley (No  Extension) | 2 |
| Blackwater | 2 |
| San Jacinto (Borrego) | 2 |
| San Jacinto (Coyote Creek) | 2 |
| Earthquake Valley | 2 |
| Garlock (West) | 2 |
| San Andreas (Parkfield) | 2 |
| San Andreas (Creeping Section) 2011 CFM | 2 |
| McLean Lake | 2 |
| Cerro Prieto | 2 |
| San Andreas (Offshore) 2011 CFM | 2 |
| Elsinore (Stepovers Combined) | 1 |
| Manix-Afton Hills | 1 |
| San Andreas (North Coast) 2011 CFM | 1 |
| San Diego Trough south | 1 |
| Emerson-Copper Mtn 2011 | 1 |
| Gravel Hills-Harper Lk | 1 |
| San Andreas (Mojave N) | 1 |
| Rose Canyon | 1 |
| Pisgah-Bullion Mtn-Mesquite Lk | 1 |
| Honey Lake 2011 CFM | 1 |
| Brawley (Seismic Zone) alt 1 | 1 |
| San Andreas (Cholame) rev | 1 |
| San Juan | 1 |
| Sargent 2011 CFM | 1 |
| San Gregorio (North) 2011 CFM | 1 |
| San Andreas (Big Bend) | 1 |
| San Jacinto (San Jacinto Valley) rev | 1 |
| Coronado Bank alt1 | 1 |
| Death Valley (So) | 1 |
| San Diego Trough north alt1 | 1 |
| San Jacinto (San Bernardino) | 1 |
| Garlock (East) | 1 |
| San Andreas (Mojave S) | 1 |
| Newport-Inglewood (Offshore) | 1 |
| Elsinore (Temecula) rev | 1 |
| Owens Valley | 1 |
| Johnson Valley (No) 2011 rev | 1 |
| Camp Rock 2011 | 1 |
| Lenwood-Lockhart-Old Woman Springs | 1 |
| Paradise | 1 |
| San Andreas (Coachella) rev | 1 |
| San Jacinto (Clark) rev | 1 |
| Garlock (Central) | 1 |
| Calico-Hidalgo | 1 |
| Mendocino | 1 |
| Ash Hill | 1 |
| Death Valley (No) | 1 |
| Palos Verdes | 1 |
| White Mountains | 1 |
| Blue Cut | 1 |
| TOTAL # PARENTS | 62 |

Actual magnitude range: [7.150965,7.249807], average: 7.20166, stdDev: 0.033809364

## Sites

| Name | Location | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|
| USC | *34.0192, -118.286* | 500 | 0.58 | 4.1 |

## Result Summary Table

| Type | Notation | Distance | T-independent Std. Dev. | 3s Std. Dev. | 5s Std. Dev. | 10s Std. Dev. |
|-----|-----|-----|-----|-----|-----|-----|
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.27 | 0.29 | 0.32 | 0.17 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.32 | 0.32 | 0.35 | 0.24 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.38 | 0.39 | 0.42 | 0.3 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.33 | 0.34 | 0.36 | 0.24 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.37 | 0.36 | 0.38 | 0.37 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.41 | 0.37 | 0.41 | 0.47 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.43 | 0.37 | 0.42 | 0.49 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.4 | 0.37 | 0.41 | 0.45 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.39 | 0.39 | 0.41 | 0.37 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.45 | 0.41 | 0.45 | 0.49 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.51 | 0.48 | 0.53 | 0.53 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.45 | 0.43 | 0.46 | 0.47 |
| Between-events | &tau; | 20 km | 0.25 | 0.18 | 0.24 | 0.32 |
| Between-events | &tau; | 50 km | 0.28 | 0.2 | 0.29 | 0.33 |
| Between-events | &tau; | 100 km | 0.28 | 0.21 | 0.3 | 0.33 |
| Between-events | &tau; | (all) | 0.27 | 0.2 | 0.27 | 0.32 |

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

* Site *[1 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*
* Rupture Strike *[18 unique]*

we compute residuals of the natural-log ground motions (relative to the median), computed across all 18 combinations of:

* Path *[18 unique]*

We take &phi;<sub>P2P</sub> to be the standard deviation of all residuals across each combination of Rupture, Rupture Strike.

We also compute distance-independent &phi;<sub>P2P</sub>, which is computed as the standard deviation of all residuals across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Rupture Strike]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_path.png)


### 20.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_20km_std_dev.png)

| 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.29 | 0.29 | 0.28 | [0.11 0.52] |  | 0.32 | 0.31 | 0.3 | [0.1 0.61] |  | 0.17 | 0.16 | 0.15 | [0.05 0.42] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_20km_3s_hist.png) | ![5s](resources/path_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 49 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.27 | 0.26 | 0.04 | [0.24 0.31] | [0.19 0.34] |
| 3 | 0.29 | 0.29 | 0.04 | [0.25 0.33] | [0.2 0.38] |
| 4 | 0.3 | 0.29 | 0.05 | [0.24 0.34] | [0.21 0.41] |
| 5 | 0.32 | 0.31 | 0.05 | [0.26 0.37] | [0.22 0.43] |
| 7.5 | 0.26 | 0.24 | 0.06 | [0.19 0.32] | [0.16 0.38] |
| 10 | 0.17 | 0.16 | 0.04 | [0.12 0.22] | [0.09 0.27] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_50km_std_dev.png)

| 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.32 | 0.31 | 0.3 | [0.12 0.6] |  | 0.35 | 0.34 | 0.34 | [0.16 0.64] |  | 0.24 | 0.24 | 0.23 | [0.1 0.53] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_50km_3s_hist.png) | ![5s](resources/path_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.32 | 0.31 | 0.04 | [0.26 0.34] | [0.23 0.4] |
| 3 | 0.32 | 0.31 | 0.06 | [0.26 0.37] | [0.2 0.45] |
| 4 | 0.33 | 0.31 | 0.06 | [0.27 0.39] | [0.2 0.47] |
| 5 | 0.35 | 0.34 | 0.06 | [0.28 0.39] | [0.22 0.49] |
| 7.5 | 0.33 | 0.32 | 0.05 | [0.27 0.36] | [0.22 0.43] |
| 10 | 0.24 | 0.24 | 0.05 | [0.18 0.28] | [0.14 0.35] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_100km_std_dev.png)

| 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.39 | 0.39 | 0.38 | [0.21 0.61] |  | 0.42 | 0.41 | 0.4 | [0.19 0.75] |  | 0.3 | 0.3 | 0.29 | [0.14 0.49] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_100km_3s_hist.png) | ![5s](resources/path_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 41 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 20 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.38 | 0.37 | 0.04 | [0.34 0.42] | [0.3 0.48] |
| 3 | 0.39 | 0.39 | 0.04 | [0.34 0.43] | [0.32 0.49] |
| 4 | 0.41 | 0.41 | 0.06 | [0.35 0.47] | [0.32 0.57] |
| 5 | 0.42 | 0.41 | 0.07 | [0.34 0.49] | [0.27 0.58] |
| 7.5 | 0.37 | 0.37 | 0.05 | [0.32 0.43] | [0.28 0.48] |
| 10 | 0.3 | 0.3 | 0.04 | [0.26 0.35] | [0.21 0.4] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_3s.png) |


### All Distances M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_std_dev.png)

| 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.34 | 0.33 | 0.33 | [0.11 0.61] |  | 0.36 | 0.36 | 0.35 | [0.1 0.75] |  | 0.24 | 0.23 | 0.23 | [0.05 0.53] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_3s_hist.png) | ![5s](resources/path_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 273 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 289 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.33 | 0.33 | 0.02 | [0.31 0.34] | [0.3 0.36] |
| 3 | 0.34 | 0.34 | 0.02 | [0.32 0.35] | [0.29 0.37] |
| 4 | 0.35 | 0.35 | 0.02 | [0.33 0.37] | [0.31 0.39] |
| 5 | 0.36 | 0.37 | 0.02 | [0.35 0.39] | [0.32 0.4] |
| 7.5 | 0.32 | 0.32 | 0.02 | [0.3 0.35] | [0.28 0.37] |
| 10 | 0.24 | 0.24 | 0.02 | [0.23 0.26] | [0.21 0.28] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_3s.png) |


## Source-strike Variability
*[(top)](#table-of-contents)*

### Source-strike Variability Methodology
*[(top)](#table-of-contents)*

Source-strike variability, denoted &phi;<sub>s</sub> in Aki & Richards (1980), is computed separately for each:

* Site *[1 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*
* Path *[18 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 18 combinations of:

* Rupture Strike *[18 unique]*

We take &phi;<sub>s</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture, Path.

We also compute distance-independent &phi;<sub>s</sub>, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture, Path]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_source_strike.png)


### 20.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_20km_std_dev.png)

| 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.36 | 0.35 | 0.34 | [0.12 0.69] |  | 0.38 | 0.37 | 0.36 | [0.11 0.79] |  | 0.37 | 0.35 | 0.33 | [0.12 0.82] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_20km_3s_hist.png) | ![5s](resources/source_strike_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 49 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.37 | 0.36 | 0.05 | [0.31 0.42] | [0.27 0.47] |
| 3 | 0.36 | 0.35 | 0.05 | [0.3 0.41] | [0.26 0.46] |
| 4 | 0.36 | 0.34 | 0.06 | [0.3 0.41] | [0.23 0.49] |
| 5 | 0.38 | 0.37 | 0.06 | [0.32 0.43] | [0.25 0.5] |
| 7.5 | 0.39 | 0.36 | 0.07 | [0.31 0.46] | [0.28 0.54] |
| 10 | 0.37 | 0.35 | 0.09 | [0.27 0.45] | [0.22 0.55] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_3s.png) |


### 50.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_50km_std_dev.png)

| 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.37 | 0.36 | 0.34 | [0.14 0.76] |  | 0.41 | 0.4 | 0.39 | [0.14 0.76] |  | 0.47 | 0.46 | 0.45 | [0.22 0.87] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_50km_3s_hist.png) | ![5s](resources/source_strike_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.41 | 0.41 | 0.06 | [0.34 0.46] | [0.3 0.54] |
| 3 | 0.37 | 0.35 | 0.08 | [0.29 0.44] | [0.24 0.53] |
| 4 | 0.37 | 0.36 | 0.08 | [0.29 0.45] | [0.22 0.52] |
| 5 | 0.41 | 0.4 | 0.08 | [0.35 0.49] | [0.28 0.63] |
| 7.5 | 0.44 | 0.42 | 0.08 | [0.36 0.51] | [0.27 0.62] |
| 10 | 0.47 | 0.46 | 0.08 | [0.39 0.56] | [0.29 0.64] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_3s.png) |


### 100.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_100km_std_dev.png)

| 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.37 | 0.36 | 0.34 | [0.15 0.82] |  | 0.42 | 0.41 | 0.4 | [0.16 0.79] |  | 0.49 | 0.48 | 0.48 | [0.18 0.87] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_100km_3s_hist.png) | ![5s](resources/source_strike_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 41 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 20 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.43 | 0.41 | 0.05 | [0.36 0.46] | [0.33 0.57] |
| 3 | 0.37 | 0.35 | 0.08 | [0.28 0.42] | [0.24 0.58] |
| 4 | 0.38 | 0.37 | 0.07 | [0.31 0.44] | [0.24 0.56] |
| 5 | 0.42 | 0.4 | 0.08 | [0.35 0.49] | [0.29 0.61] |
| 7.5 | 0.46 | 0.43 | 0.07 | [0.36 0.5] | [0.31 0.6] |
| 10 | 0.49 | 0.47 | 0.06 | [0.42 0.54] | [0.38 0.65] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_3s.png) |


### All Distances M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_std_dev.png)

| 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.37 | 0.36 | 0.34 | [0.12 0.82] |  | 0.41 | 0.4 | 0.39 | [0.11 0.79] |  | 0.45 | 0.43 | 0.43 | [0.12 0.87] |

Here are plots of the histogram of &phi;<sub>s</sub> for each individual rupture, from which we compute a total &phi;<sub>s</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/source_strike_m7.2_3s_hist.png) | ![5s](resources/source_strike_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/source_strike_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Source-strike Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>s</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 273 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>s</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 289 fewer data points.*

| Period (s) | Full &phi;<sub>s</sub> | Downsampled median &phi;<sub>s</sub> | Downsampled &phi;<sub>s</sub> std. dev. | Downsampled &phi;<sub>s</sub> 68% conf range | Downsampled &phi;<sub>s</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.4 | 0.41 | 0.02 | [0.38 0.43] | [0.36 0.46] |
| 3 | 0.37 | 0.36 | 0.03 | [0.34 0.39] | [0.32 0.43] |
| 4 | 0.37 | 0.37 | 0.03 | [0.34 0.39] | [0.32 0.43] |
| 5 | 0.41 | 0.41 | 0.03 | [0.38 0.43] | [0.36 0.48] |
| 7.5 | 0.43 | 0.43 | 0.03 | [0.4 0.46] | [0.38 0.51] |
| 10 | 0.45 | 0.45 | 0.03 | [0.42 0.48] | [0.4 0.52] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_3s.png) |


## Within-event, single-site Variability
*[(top)](#table-of-contents)*

### Within-event, single-site Variability Methodology
*[(top)](#table-of-contents)*

Within-event, single-site variability, denoted &phi;<sub>SS</sub> in Al Atik (2010), is computed separately for each:

* Site *[1 unique]*
* Distance *[3 unique]*

Then, for each unique combination of:

* Rupture *[50 unique]*

we compute residuals, &delta;W<sub>es</sub>, of the natural-log ground motions (relative to the median), computed across all 324 combinations of:

* Rupture Strike *[18 unique]*
* Path *[18 unique]*

We take &phi;<sub>SS</sub> to be the standard deviation of all residuals, &delta;W<sub>es</sub>, across each combination of Rupture.

We also compute distance-independent &phi;<sub>SS</sub>, which is computed as the standard deviation of all residuals, &delta;W<sub>es</sub>, across all distances. Each residual is still computed relative to the log-median ground motion at it's distance.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_within_event_ss.png)


### 20.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_20km_std_dev.png)

| 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.39 | 0.38 | 0.36 | [0.29 0.57] |  | 0.41 | 0.4 | 0.4 | [0.29 0.58] |  | 0.37 | 0.36 | 0.33 | [0.19 0.68] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_20km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.39 | 0.38 | 0.05 | [0.33 0.44] | [0.31 0.51] |
| 3 | 0.39 | 0.37 | 0.05 | [0.32 0.43] | [0.29 0.5] |
| 4 | 0.38 | 0.37 | 0.05 | [0.32 0.43] | [0.27 0.51] |
| 5 | 0.41 | 0.4 | 0.06 | [0.34 0.47] | [0.3 0.53] |
| 7.5 | 0.4 | 0.38 | 0.07 | [0.33 0.46] | [0.29 0.57] |
| 10 | 0.37 | 0.36 | 0.08 | [0.3 0.45] | [0.23 0.57] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_20km.png)


### 50.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_50km_std_dev.png)

| 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.41 | 0.4 | 0.38 | [0.31 0.62] |  | 0.45 | 0.44 | 0.43 | [0.31 0.62] |  | 0.49 | 0.47 | 0.46 | [0.33 0.76] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_50km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.45 | 0.43 | 0.06 | [0.36 0.49] | [0.33 0.54] |
| 3 | 0.41 | 0.39 | 0.08 | [0.33 0.48] | [0.25 0.57] |
| 4 | 0.41 | 0.39 | 0.08 | [0.31 0.47] | [0.26 0.57] |
| 5 | 0.45 | 0.43 | 0.07 | [0.35 0.51] | [0.28 0.6] |
| 7.5 | 0.47 | 0.45 | 0.09 | [0.36 0.54] | [0.32 0.64] |
| 10 | 0.49 | 0.45 | 0.08 | [0.38 0.56] | [0.33 0.63] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_50km.png)


### 100.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_100km_std_dev.png)

| 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.48 | 0.47 | 0.46 | [0.39 0.67] |  | 0.53 | 0.52 | 0.51 | [0.42 0.66] |  | 0.53 | 0.52 | 0.49 | [0.39 0.79] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_100km_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.51 | 0.49 | 0.05 | [0.45 0.55] | [0.4 0.62] |
| 3 | 0.48 | 0.46 | 0.06 | [0.4 0.51] | [0.36 0.61] |
| 4 | 0.5 | 0.48 | 0.06 | [0.44 0.54] | [0.38 0.65] |
| 5 | 0.53 | 0.52 | 0.06 | [0.46 0.57] | [0.4 0.66] |
| 7.5 | 0.52 | 0.52 | 0.07 | [0.46 0.57] | [0.39 0.66] |
| 10 | 0.53 | 0.51 | 0.08 | [0.44 0.59] | [0.4 0.72] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/within_event_ss_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/within_event_ss_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/within_event_ss_event_recordings_hist_100km.png)


### All Distances M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_std_dev.png)

| 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  | 0.43 | 0.42 | 0.41 | [0.29 0.67] |  | 0.46 | 0.46 | 0.44 | [0.29 0.66] |  | 0.47 | 0.45 | 0.46 | [0.19 0.79] |

Here are plots of the histogram of &phi;<sub>SS</sub> for each individual rupture, from which we compute a total &phi;<sub>SS</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_ss_m7.2_3s_hist.png) | ![5s](resources/within_event_ss_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_ss_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Within-event, single-site Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>SS</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times, and compute &phi;<sub>SS</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi;<sub>SS</sub> | Downsampled median &phi;<sub>SS</sub> | Downsampled &phi;<sub>SS</sub> std. dev. | Downsampled &phi;<sub>SS</sub> 68% conf range | Downsampled &phi;<sub>SS</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.45 | 0.46 | 0.03 | [0.42 0.48] | [0.4 0.52] |
| 3 | 0.43 | 0.42 | 0.03 | [0.4 0.46] | [0.38 0.5] |
| 4 | 0.43 | 0.43 | 0.03 | [0.4 0.47] | [0.39 0.51] |
| 5 | 0.46 | 0.46 | 0.03 | [0.43 0.5] | [0.4 0.54] |
| 7.5 | 0.47 | 0.46 | 0.04 | [0.43 0.51] | [0.41 0.56] |
| 10 | 0.47 | 0.47 | 0.04 | [0.43 0.52] | [0.4 0.56] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **USC** |
|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_3s.png) |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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

* Rupture *[50 unique]*

That median, &delta;B<sub>e</sub>, is computed across all 324 combinations of:

* Site *[1 unique]*
* Rupture Strike *[18 unique]*
* Path *[18 unique]*

We take &tau; to be the standard deviation of all &delta;B<sub>e</sub>.

We also compute distance-independent &tau;, which we take to be the mean value across all distances.

Here is an exmample with 5 rotations, which would be repeated for each combination of [Rupture]. The site is shown with a blue square, and initially oriented rupture in bold with its hypocenter as a red star and centroid a green circle. Rotations of that rupture are in gray:

![Example](resources/example_between_events.png)


### 20.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_20km_std_dev.png)

| 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0.18 | -2.28 | [-2.62 -1.79] | 0.24 | -2.89 | [-3.37 -2.42] | 0.32 | -3.92 | [-4.65 -3.3] |

#### 20.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.27 | 0.09 | [0.18 0.35] | [0.12 0.46] |
| 3 | 0.18 | 0.21 | 0.09 | [0.11 0.32] | [0.07 0.41] |
| 4 | 0.22 | 0.24 | 0.11 | [0.14 0.36] | [0.09 0.48] |
| 5 | 0.24 | 0.26 | 0.1 | [0.15 0.37] | [0.06 0.47] |
| 7.5 | 0.28 | 0.29 | 0.11 | [0.17 0.4] | [0.09 0.53] |
| 10 | 0.32 | 0.3 | 0.13 | [0.18 0.45] | [0.12 0.63] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_20km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_20km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_20km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [10.0,30.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_20km.png)


### 50.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_50km_std_dev.png)

| 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0.2 | -2.99 | [-3.3 -2.49] | 0.29 | -3.4 | [-3.97 -2.8] | 0.33 | -4.46 | [-5.3 -3.8] |

#### 50.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.28 | 0.28 | 0.12 | [0.19 0.44] | [0.13 0.57] |
| 3 | 0.2 | 0.21 | 0.11 | [0.13 0.36] | [0.08 0.46] |
| 4 | 0.25 | 0.26 | 0.14 | [0.12 0.41] | [0.07 0.59] |
| 5 | 0.29 | 0.27 | 0.15 | [0.17 0.46] | [0.06 0.66] |
| 7.5 | 0.32 | 0.35 | 0.16 | [0.19 0.51] | [0.1 0.67] |
| 10 | 0.33 | 0.36 | 0.16 | [0.21 0.55] | [0.1 0.79] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_50km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_50km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_50km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [40.0,60.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_50km.png)


### 100.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_100km_std_dev.png)

| 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0.21 | -3.67 | [-4.01 -3.14] | 0.3 | -3.96 | [-4.67 -3.34] | 0.33 | -4.95 | [-5.71 -4.31] |

#### 100.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.28 | 0.29 | 0.11 | [0.18 0.41] | [0.11 0.55] |
| 3 | 0.21 | 0.23 | 0.11 | [0.11 0.35] | [0.05 0.47] |
| 4 | 0.26 | 0.24 | 0.14 | [0.13 0.43] | [0.03 0.59] |
| 5 | 0.3 | 0.31 | 0.14 | [0.14 0.45] | [0.05 0.58] |
| 7.5 | 0.32 | 0.32 | 0.15 | [0.17 0.46] | [0.09 0.65] |
| 10 | 0.33 | 0.32 | 0.15 | [0.19 0.49] | [0.05 0.66] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

| Period | Event Count Dependence | Recordings/Event Dependence |
|-----|-----|-----|
| Period Indep. | ![num events dependence](resources/between_events_event_count_dependence_100km_period_indep.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_period_indep.png) |
| 3s | ![num events dependence](resources/between_events_event_count_dependence_100km_3s.png) | ![num recordings dependence](resources/between_events_event_recordings_dependence_100km_3.png) |

This is a histogram of the number of recordings per event from ASK 2014 with M=[7.0,7.4]. The top plot shows the subset with distance in the range [80.0,120.0], and the bottom the whole distribution at all distances.

![Histogram](resources/between_events_event_recordings_hist_100km.png)


### All Distances M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_std_dev.png)

| 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0.2 | -2.98 | [-4.01 -1.79] | 0.27 | -3.41 | [-4.67 -2.42] | 0.32 | -4.44 | [-5.71 -3.3] |

#### All Distances M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.27 | 0.28 | 0.04 | [0.22 0.32] | [0.2 0.35] |
| 3 | 0.2 | 0.21 | 0.04 | [0.17 0.25] | [0.13 0.28] |
| 4 | 0.25 | 0.25 | 0.05 | [0.2 0.3] | [0.16 0.35] |
| 5 | 0.27 | 0.28 | 0.05 | [0.23 0.33] | [0.17 0.38] |
| 7.5 | 0.3 | 0.31 | 0.05 | [0.25 0.37] | [0.2 0.4] |
| 10 | 0.32 | 0.32 | 0.06 | [0.26 0.38] | [0.2 0.43] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_USC_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_USC_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_USC_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_USC_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_USC_10s.png) |
### Slip Std Dev Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_USC_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_USC_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_USC_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_USC_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_USC_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_USC_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_USC_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_USC_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_USC_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_USC_10s.png) |
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

### Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **Median SA** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

### Path Dependence
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

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismicâ€�hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **M7.2 SS** | *(FAIL)* | *(FAIL)* | *(FAIL)* |

### BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|
| ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M7.2 | 20.0 km | USC | [sa_USC_m7.2_20.0km.csv.gz](resources/sa_USC_m7.2_20.0km.csv.gz) |
| M7.2 | 50.0 km | USC | [sa_USC_m7.2_50.0km.csv.gz](resources/sa_USC_m7.2_50.0km.csv.gz) |
| M7.2 | 100.0 km | USC | [sa_USC_m7.2_100.0km.csv.gz](resources/sa_USC_m7.2_100.0km.csv.gz) |

