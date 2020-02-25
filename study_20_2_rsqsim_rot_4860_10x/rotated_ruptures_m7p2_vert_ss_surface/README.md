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
  * [BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture](#bbp-partb-m72-vertical-strike-slip-with-surface-rupture)
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
| SUM OF PARENT PARTICIPATIONS | 62 |
| # UNIQUE PARENTS | [Earthquake Valley (No  Extension), Blackwater, San Jacinto (Borrego), San Jacinto (Coyote Creek), Earthquake Valley, Garlock (West), San Andreas (Parkfield), San Andreas (Creeping Section) 2011 CFM, McLean Lake, Cerro Prieto, San Andreas (Offshore) 2011 CFM, Elsinore (Stepovers Combined), Manix-Afton Hills, San Andreas (North Coast) 2011 CFM, San Diego Trough south, Emerson-Copper Mtn 2011, Gravel Hills-Harper Lk, San Andreas (Mojave N), Rose Canyon, Pisgah-Bullion Mtn-Mesquite Lk, Honey Lake 2011 CFM, Brawley (Seismic Zone) alt 1, San Andreas (Cholame) rev, San Juan, Sargent 2011 CFM, San Gregorio (North) 2011 CFM, San Andreas (Big Bend), San Jacinto (San Jacinto Valley) rev, Coronado Bank alt1, Death Valley (So), San Diego Trough north alt1, San Jacinto (San Bernardino), Garlock (East), San Andreas (Mojave S), Newport-Inglewood (Offshore), Elsinore (Temecula) rev, Owens Valley, Johnson Valley (No) 2011 rev, Camp Rock 2011, Lenwood-Lockhart-Old Woman Springs, Paradise, San Andreas (Coachella) rev, San Jacinto (Clark) rev, Garlock (Central), Calico-Hidalgo, Mendocino, Ash Hill, Death Valley (No), Palos Verdes, White Mountains, Blue Cut] |

Actual magnitude range: [7.150965,7.249807], average: 7.20166, stdDev: 0.033809364

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
| Path-to-path | &phi;<sub>P2P</sub> | 20 km | 0.27 | 0.32 | 0.3 | 0.15 |
| Path-to-path | &phi;<sub>P2P</sub> | 50 km | 0.33 | 0.39 | 0.35 | 0.22 |
| Path-to-path | &phi;<sub>P2P</sub> | 100 km | 0.39 | 0.45 | 0.4 | 0.27 |
| Path-to-path | &phi;<sub>P2P</sub> | (all) | 0.33 | 0.39 | 0.35 | 0.22 |
| Source-strike | &phi;<sub>s</sub> | 20 km | 0.37 | 0.36 | 0.38 | 0.36 |
| Source-strike | &phi;<sub>s</sub> | 50 km | 0.42 | 0.39 | 0.41 | 0.47 |
| Source-strike | &phi;<sub>s</sub> | 100 km | 0.44 | 0.39 | 0.43 | 0.49 |
| Source-strike | &phi;<sub>s</sub> | (all) | 0.41 | 0.38 | 0.41 | 0.44 |
| Within-event, single-site | &phi;<sub>SS</sub> | 20 km | 0.4 | 0.41 | 0.41 | 0.36 |
| Within-event, single-site | &phi;<sub>SS</sub> | 50 km | 0.47 | 0.47 | 0.46 | 0.48 |
| Within-event, single-site | &phi;<sub>SS</sub> | 100 km | 0.52 | 0.53 | 0.52 | 0.51 |
| Within-event, single-site | &phi;<sub>SS</sub> | (all) | 0.46 | 0.48 | 0.47 | 0.45 |
| Within-event | &phi; | 20 km | 0.53 | 0.5 | 0.53 | 0.53 |
| Within-event | &phi; | 50 km | 0.62 | 0.57 | 0.63 | 0.64 |
| Within-event | &phi; | 100 km | 0.66 | 0.61 | 0.67 | 0.66 |
| Within-event | &phi; | (all) | 0.6 | 0.56 | 0.61 | 0.61 |
| Between-events | &tau; | 20 km | 0.25 | 0.18 | 0.25 | 0.29 |
| Between-events | &tau; | 50 km | 0.27 | 0.2 | 0.28 | 0.31 |
| Between-events | &tau; | 100 km | 0.28 | 0.21 | 0.29 | 0.32 |
| Between-events | &tau; | (all) | 0.27 | 0.2 | 0.27 | 0.31 |

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


### 20.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.32** | **0.3** | **0.27** | **[0.06 1.01]** |  | **0.3** | **0.28** | **0.26** | **[0.04 0.9]** |  | **0.15** | **0.14** | **0.13** | **[0.02 0.47]** |
| LAF |  | 0.3 | 0.29 | 0.27 | [0.12 0.6] |  | 0.32 | 0.31 | 0.29 | [0.09 0.67] |  | 0.17 | 0.15 | 0.14 | [0.04 0.38] |
| OSI |  | 0.24 | 0.23 | 0.21 | [0.06 0.56] |  | 0.18 | 0.17 | 0.16 | [0.04 0.44] |  | 0.1 | 0.1 | 0.09 | [0.02 0.35] |
| PDE |  | 0.28 | 0.27 | 0.26 | [0.11 0.59] |  | 0.26 | 0.26 | 0.25 | [0.09 0.53] |  | 0.14 | 0.13 | 0.12 | [0.04 0.35] |
| SBSM |  | 0.3 | 0.29 | 0.27 | [0.1 0.67] |  | 0.22 | 0.21 | 0.19 | [0.05 0.55] |  | 0.12 | 0.11 | 0.1 | [0.04 0.3] |
| SMCA |  | 0.33 | 0.32 | 0.3 | [0.12 0.66] |  | 0.33 | 0.32 | 0.3 | [0.13 0.66] |  | 0.16 | 0.15 | 0.14 | [0.03 0.43] |
| STNI |  | 0.25 | 0.24 | 0.24 | [0.11 0.5] |  | 0.28 | 0.27 | 0.27 | [0.07 0.57] |  | 0.14 | 0.13 | 0.12 | [0.04 0.32] |
| USC |  | 0.29 | 0.29 | 0.28 | [0.11 0.52] |  | 0.32 | 0.31 | 0.3 | [0.1 0.61] |  | 0.17 | 0.16 | 0.15 | [0.05 0.42] |
| WNGC |  | 0.54 | 0.53 | 0.51 | [0.18 1.01] |  | 0.44 | 0.42 | 0.41 | [0.1 0.9] |  | 0.17 | 0.16 | 0.15 | [0.04 0.44] |
| WSS |  | 0.33 | 0.33 | 0.32 | [0.14 0.58] |  | 0.28 | 0.27 | 0.26 | [0.09 0.59] |  | 0.12 | 0.11 | 0.1 | [0.04 0.34] |
| s022 |  | 0.25 | 0.24 | 0.24 | [0.11 0.48] |  | 0.26 | 0.25 | 0.24 | [0.11 0.57] |  | 0.19 | 0.18 | 0.17 | [0.05 0.47] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_20km_3s_hist.png) | ![5s](resources/path_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 49 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 2 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.27 | 0.27 | 0.01 | [0.25 0.28] | [0.24 0.29] |
| 3 | 0.32 | 0.32 | 0.02 | [0.3 0.34] | [0.29 0.37] |
| 4 | 0.31 | 0.3 | 0.02 | [0.29 0.32] | [0.27 0.34] |
| 5 | 0.3 | 0.29 | 0.02 | [0.28 0.31] | [0.25 0.33] |
| 7.5 | 0.23 | 0.23 | 0.02 | [0.21 0.24] | [0.2 0.26] |
| 10 | 0.15 | 0.15 | 0.01 | [0.14 0.16] | [0.13 0.17] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_20km_s022_downsampled_hist_3s.png) |  |  |


### 50.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.37** | **0.34** | **[0.12 1]** |  | **0.35** | **0.34** | **0.33** | **[0.11 0.77]** |  | **0.22** | **0.21** | **0.2** | **[0.05 0.53]** |
| LAF |  | 0.31 | 0.3 | 0.29 | [0.15 0.56] |  | 0.32 | 0.32 | 0.32 | [0.15 0.58] |  | 0.24 | 0.23 | 0.22 | [0.08 0.49] |
| OSI |  | 0.34 | 0.34 | 0.33 | [0.16 0.62] |  | 0.29 | 0.28 | 0.27 | [0.14 0.66] |  | 0.2 | 0.19 | 0.18 | [0.05 0.41] |
| PDE |  | 0.35 | 0.34 | 0.33 | [0.13 0.67] |  | 0.31 | 0.31 | 0.29 | [0.11 0.64] |  | 0.22 | 0.21 | 0.2 | [0.07 0.46] |
| SBSM |  | 0.49 | 0.49 | 0.47 | [0.24 0.87] |  | 0.38 | 0.38 | 0.36 | [0.17 0.77] |  | 0.19 | 0.19 | 0.18 | [0.07 0.4] |
| SMCA |  | 0.46 | 0.45 | 0.44 | [0.22 0.78] |  | 0.38 | 0.38 | 0.36 | [0.17 0.71] |  | 0.25 | 0.24 | 0.24 | [0.09 0.52] |
| STNI |  | 0.29 | 0.29 | 0.28 | [0.13 0.47] |  | 0.35 | 0.34 | 0.33 | [0.12 0.62] |  | 0.21 | 0.2 | 0.19 | [0.06 0.49] |
| USC |  | 0.32 | 0.31 | 0.3 | [0.12 0.6] |  | 0.35 | 0.34 | 0.34 | [0.16 0.64] |  | 0.24 | 0.24 | 0.23 | [0.1 0.53] |
| WNGC |  | 0.57 | 0.56 | 0.55 | [0.25 1] |  | 0.44 | 0.43 | 0.41 | [0.18 0.77] |  | 0.22 | 0.21 | 0.21 | [0.07 0.46] |
| WSS |  | 0.34 | 0.34 | 0.33 | [0.17 0.59] |  | 0.37 | 0.36 | 0.34 | [0.16 0.74] |  | 0.21 | 0.2 | 0.2 | [0.09 0.38] |
| s022 |  | 0.25 | 0.25 | 0.24 | [0.12 0.47] |  | 0.3 | 0.29 | 0.29 | [0.14 0.6] |  | 0.25 | 0.24 | 0.22 | [0.08 0.53] |

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
| T-independent | 0.33 | 0.32 | 0.01 | [0.31 0.34] | [0.29 0.35] |
| 3 | 0.39 | 0.37 | 0.02 | [0.35 0.4] | [0.33 0.42] |
| 4 | 0.37 | 0.36 | 0.02 | [0.34 0.38] | [0.32 0.4] |
| 5 | 0.35 | 0.34 | 0.02 | [0.32 0.36] | [0.3 0.38] |
| 7.5 | 0.3 | 0.29 | 0.02 | [0.28 0.31] | [0.26 0.33] |
| 10 | 0.22 | 0.22 | 0.01 | [0.2 0.23] | [0.18 0.25] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_50km_s022_downsampled_hist_3s.png) |  |  |


### 100.0 km M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.45** | **0.43** | **0.41** | **[0.15 1]** |  | **0.4** | **0.4** | **0.39** | **[0.12 0.81]** |  | **0.27** | **0.26** | **0.26** | **[0.08 0.64]** |
| LAF |  | 0.4 | 0.4 | 0.39 | [0.21 0.64] |  | 0.36 | 0.36 | 0.35 | [0.12 0.58] |  | 0.26 | 0.26 | 0.25 | [0.12 0.46] |
| OSI |  | 0.4 | 0.4 | 0.4 | [0.24 0.65] |  | 0.36 | 0.35 | 0.34 | [0.18 0.63] |  | 0.26 | 0.25 | 0.24 | [0.11 0.6] |
| PDE |  | 0.37 | 0.37 | 0.36 | [0.17 0.68] |  | 0.36 | 0.35 | 0.34 | [0.16 0.72] |  | 0.27 | 0.25 | 0.24 | [0.09 0.61] |
| SBSM |  | 0.57 | 0.57 | 0.57 | [0.25 0.9] |  | 0.45 | 0.44 | 0.44 | [0.22 0.75] |  | 0.23 | 0.23 | 0.22 | [0.11 0.41] |
| SMCA |  | 0.54 | 0.55 | 0.54 | [0.27 0.77] |  | 0.41 | 0.41 | 0.41 | [0.21 0.65] |  | 0.29 | 0.29 | 0.29 | [0.15 0.46] |
| STNI |  | 0.32 | 0.33 | 0.32 | [0.15 0.52] |  | 0.38 | 0.38 | 0.37 | [0.18 0.67] |  | 0.26 | 0.26 | 0.24 | [0.08 0.49] |
| USC |  | 0.39 | 0.39 | 0.38 | [0.21 0.61] |  | 0.42 | 0.41 | 0.4 | [0.19 0.75] |  | 0.3 | 0.3 | 0.29 | [0.14 0.49] |
| WNGC |  | 0.61 | 0.61 | 0.6 | [0.3 1] |  | 0.49 | 0.49 | 0.48 | [0.21 0.81] |  | 0.25 | 0.24 | 0.24 | [0.09 0.43] |
| WSS |  | 0.4 | 0.4 | 0.39 | [0.23 0.6] |  | 0.41 | 0.41 | 0.39 | [0.23 0.79] |  | 0.25 | 0.25 | 0.24 | [0.09 0.45] |
| s022 |  | 0.32 | 0.33 | 0.32 | [0.18 0.52] |  | 0.37 | 0.37 | 0.36 | [0.19 0.63] |  | 0.29 | 0.29 | 0.29 | [0.15 0.64] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_100km_3s_hist.png) | ![5s](resources/path_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 41 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 20 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.39 | 0.38 | 0.01 | [0.37 0.39] | [0.35 0.41] |
| 3 | 0.45 | 0.44 | 0.02 | [0.42 0.46] | [0.41 0.49] |
| 4 | 0.43 | 0.42 | 0.02 | [0.4 0.44] | [0.38 0.47] |
| 5 | 0.4 | 0.4 | 0.02 | [0.38 0.42] | [0.36 0.44] |
| 7.5 | 0.35 | 0.35 | 0.02 | [0.33 0.36] | [0.31 0.38] |
| 10 | 0.27 | 0.26 | 0.02 | [0.25 0.28] | [0.24 0.31] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_100km_s022_downsampled_hist_3s.png) |  |  |


### All Distances M7.2 Path-to-path Results
*[(top)](#table-of-contents)*

![Path-to-path Variability](resources/path_m7.2_std_dev.png)

| Site | 3s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 5s &phi;<sub>P2P</sub> | Total | Mean | Median | Range | 10s &phi;<sub>P2P</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.37** | **0.34** | **[0.06 1.01]** |  | **0.35** | **0.34** | **0.33** | **[0.04 0.9]** |  | **0.22** | **0.2** | **0.2** | **[0.02 0.64]** |
| LAF |  | 0.34 | 0.33 | 0.33 | [0.12 0.64] |  | 0.33 | 0.33 | 0.32 | [0.09 0.67] |  | 0.23 | 0.21 | 0.21 | [0.04 0.49] |
| OSI |  | 0.34 | 0.32 | 0.33 | [0.06 0.65] |  | 0.29 | 0.27 | 0.27 | [0.04 0.66] |  | 0.2 | 0.18 | 0.17 | [0.02 0.6] |
| PDE |  | 0.33 | 0.33 | 0.32 | [0.11 0.68] |  | 0.31 | 0.31 | 0.29 | [0.09 0.72] |  | 0.22 | 0.2 | 0.19 | [0.04 0.61] |
| SBSM |  | 0.47 | 0.45 | 0.46 | [0.1 0.9] |  | 0.36 | 0.34 | 0.35 | [0.05 0.77] |  | 0.19 | 0.17 | 0.17 | [0.04 0.41] |
| SMCA |  | 0.45 | 0.44 | 0.44 | [0.12 0.78] |  | 0.38 | 0.37 | 0.37 | [0.13 0.71] |  | 0.24 | 0.23 | 0.23 | [0.03 0.52] |
| STNI |  | 0.29 | 0.29 | 0.29 | [0.11 0.52] |  | 0.34 | 0.33 | 0.32 | [0.07 0.67] |  | 0.21 | 0.19 | 0.18 | [0.04 0.49] |
| USC |  | 0.34 | 0.33 | 0.33 | [0.11 0.61] |  | 0.36 | 0.36 | 0.35 | [0.1 0.75] |  | 0.24 | 0.23 | 0.23 | [0.05 0.53] |
| WNGC |  | 0.57 | 0.56 | 0.56 | [0.18 1.01] |  | 0.46 | 0.45 | 0.43 | [0.1 0.9] |  | 0.22 | 0.21 | 0.2 | [0.04 0.46] |
| WSS |  | 0.36 | 0.36 | 0.35 | [0.14 0.6] |  | 0.36 | 0.35 | 0.34 | [0.09 0.79] |  | 0.2 | 0.19 | 0.18 | [0.04 0.45] |
| s022 |  | 0.28 | 0.27 | 0.27 | [0.11 0.52] |  | 0.31 | 0.3 | 0.3 | [0.11 0.63] |  | 0.25 | 0.24 | 0.23 | [0.05 0.64] |

Here are plots of the histogram of &phi;<sub>P2P</sub> for each individual rupture, from which we compute a total &phi;<sub>P2P</sub>

| 3s | 5s |
|-----|-----|
| ![3s](resources/path_m7.2_3s_hist.png) | ![5s](resources/path_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/path_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Path-to-path Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi;<sub>P2P</sub> through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 273 recordings. We then downsample our simulated data 100 times for each site, and compute &phi;<sub>P2P</sub> from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 289 fewer data points.*

| Period (s) | Full &phi;<sub>P2P</sub> | Downsampled median &phi;<sub>P2P</sub> | Downsampled &phi;<sub>P2P</sub> std. dev. | Downsampled &phi;<sub>P2P</sub> 68% conf range | Downsampled &phi;<sub>P2P</sub> 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.33 | 0.33 | 0.01 | [0.33 0.34] | [0.32 0.34] |
| 3 | 0.39 | 0.39 | 0.01 | [0.38 0.4] | [0.37 0.41] |
| 4 | 0.37 | 0.37 | 0.01 | [0.36 0.38] | [0.36 0.38] |
| 5 | 0.35 | 0.35 | 0.01 | [0.35 0.36] | [0.34 0.37] |
| 7.5 | 0.3 | 0.3 | 0.01 | [0.29 0.3] | [0.29 0.31] |
| 10 | 0.22 | 0.22 | 0.01 | [0.21 0.22] | [0.21 0.23] |

These plots show the distribution of period-independent downsampled &phi;<sub>P2P</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/path_m7.2_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/path_m7.2_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/path_m7.2_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/path_m7.2_s022_downsampled_hist_3s.png) |  |  |


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


### 20.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.36** | **0.36** | **0.34** | **[0.12 0.81]** |  | **0.38** | **0.37** | **0.36** | **[0.11 0.86]** |  | **0.36** | **0.34** | **0.32** | **[0.1 0.84]** |
| LAF |  | 0.33 | 0.32 | 0.31 | [0.15 0.65] |  | 0.38 | 0.37 | 0.36 | [0.15 0.72] |  | 0.37 | 0.35 | 0.33 | [0.14 0.84] |
| OSI |  | 0.37 | 0.36 | 0.35 | [0.15 0.72] |  | 0.35 | 0.35 | 0.34 | [0.17 0.62] |  | 0.33 | 0.31 | 0.3 | [0.1 0.74] |
| PDE |  | 0.36 | 0.35 | 0.33 | [0.17 0.81] |  | 0.38 | 0.38 | 0.37 | [0.13 0.72] |  | 0.35 | 0.33 | 0.31 | [0.12 0.73] |
| SBSM |  | 0.41 | 0.4 | 0.39 | [0.17 0.8] |  | 0.39 | 0.38 | 0.37 | [0.18 0.75] |  | 0.31 | 0.3 | 0.29 | [0.1 0.65] |
| SMCA |  | 0.37 | 0.36 | 0.35 | [0.16 0.68] |  | 0.4 | 0.4 | 0.39 | [0.19 0.71] |  | 0.36 | 0.34 | 0.32 | [0.11 0.82] |
| STNI |  | 0.33 | 0.32 | 0.31 | [0.13 0.64] |  | 0.36 | 0.35 | 0.34 | [0.16 0.76] |  | 0.38 | 0.37 | 0.34 | [0.13 0.83] |
| USC |  | 0.36 | 0.35 | 0.34 | [0.12 0.69] |  | 0.38 | 0.37 | 0.36 | [0.11 0.79] |  | 0.37 | 0.35 | 0.33 | [0.12 0.82] |
| WNGC |  | 0.4 | 0.39 | 0.38 | [0.18 0.81] |  | 0.4 | 0.39 | 0.39 | [0.13 0.86] |  | 0.36 | 0.35 | 0.33 | [0.14 0.8] |
| WSS |  | 0.37 | 0.37 | 0.36 | [0.13 0.7] |  | 0.38 | 0.38 | 0.37 | [0.17 0.66] |  | 0.34 | 0.33 | 0.3 | [0.11 0.73] |
| s022 |  | 0.33 | 0.32 | 0.31 | [0.14 0.74] |  | 0.37 | 0.36 | 0.35 | [0.14 0.72] |  | 0.38 | 0.36 | 0.34 | [0.14 0.78] |

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
| T-independent | 0.37 | 0.37 | 0.02 | [0.35 0.38] | [0.33 0.41] |
| 3 | 0.36 | 0.36 | 0.02 | [0.34 0.38] | [0.32 0.41] |
| 4 | 0.37 | 0.36 | 0.02 | [0.34 0.38] | [0.32 0.41] |
| 5 | 0.38 | 0.38 | 0.02 | [0.36 0.4] | [0.34 0.43] |
| 7.5 | 0.38 | 0.37 | 0.02 | [0.35 0.39] | [0.33 0.42] |
| 10 | 0.36 | 0.35 | 0.02 | [0.33 0.37] | [0.3 0.4] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_20km_s022_downsampled_hist_3s.png) |  |  |


### 50.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_50km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.37** | **0.36** | **[0.08 0.9]** |  | **0.41** | **0.4** | **0.39** | **[0.14 0.9]** |  | **0.47** | **0.46** | **0.45** | **[0.15 0.88]** |
| LAF |  | 0.35 | 0.34 | 0.32 | [0.13 0.79] |  | 0.41 | 0.4 | 0.39 | [0.18 0.8] |  | 0.48 | 0.47 | 0.46 | [0.21 0.87] |
| OSI |  | 0.4 | 0.39 | 0.38 | [0.17 0.78] |  | 0.38 | 0.37 | 0.36 | [0.17 0.72] |  | 0.47 | 0.47 | 0.45 | [0.23 0.8] |
| PDE |  | 0.4 | 0.39 | 0.38 | [0.15 0.79] |  | 0.43 | 0.42 | 0.41 | [0.16 0.75] |  | 0.49 | 0.48 | 0.47 | [0.22 0.86] |
| SBSM |  | 0.47 | 0.47 | 0.45 | [0.2 0.86] |  | 0.44 | 0.44 | 0.43 | [0.19 0.78] |  | 0.45 | 0.45 | 0.44 | [0.25 0.82] |
| SMCA |  | 0.38 | 0.37 | 0.36 | [0.15 0.89] |  | 0.41 | 0.4 | 0.39 | [0.15 0.82] |  | 0.47 | 0.46 | 0.45 | [0.22 0.86] |
| STNI |  | 0.33 | 0.32 | 0.31 | [0.13 0.79] |  | 0.41 | 0.39 | 0.38 | [0.14 0.82] |  | 0.49 | 0.49 | 0.49 | [0.24 0.86] |
| USC |  | 0.37 | 0.36 | 0.34 | [0.14 0.76] |  | 0.41 | 0.4 | 0.39 | [0.14 0.76] |  | 0.47 | 0.46 | 0.45 | [0.22 0.87] |
| WNGC |  | 0.41 | 0.39 | 0.37 | [0.1 0.9] |  | 0.43 | 0.42 | 0.41 | [0.15 0.73] |  | 0.47 | 0.46 | 0.45 | [0.24 0.82] |
| WSS |  | 0.37 | 0.36 | 0.35 | [0.16 0.81] |  | 0.41 | 0.41 | 0.39 | [0.14 0.9] |  | 0.45 | 0.45 | 0.44 | [0.17 0.88] |
| s022 |  | 0.36 | 0.34 | 0.32 | [0.08 0.74] |  | 0.4 | 0.39 | 0.37 | [0.15 0.89] |  | 0.46 | 0.45 | 0.44 | [0.15 0.85] |

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
| T-independent | 0.42 | 0.41 | 0.02 | [0.38 0.43] | [0.37 0.45] |
| 3 | 0.39 | 0.37 | 0.02 | [0.35 0.4] | [0.32 0.42] |
| 4 | 0.39 | 0.37 | 0.02 | [0.35 0.4] | [0.33 0.42] |
| 5 | 0.41 | 0.4 | 0.03 | [0.37 0.43] | [0.36 0.45] |
| 7.5 | 0.44 | 0.43 | 0.03 | [0.4 0.45] | [0.38 0.49] |
| 10 | 0.47 | 0.45 | 0.03 | [0.43 0.48] | [0.4 0.51] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_50km_s022_downsampled_hist_3s.png) |  |  |


### 100.0 km M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_100km_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.39** | **0.38** | **0.36** | **[0.1 0.88]** |  | **0.43** | **0.42** | **0.41** | **[0.12 0.9]** |  | **0.49** | **0.48** | **0.47** | **[0.12 1.07]** |
| LAF |  | 0.36 | 0.35 | 0.32 | [0.11 0.8] |  | 0.42 | 0.41 | 0.4 | [0.13 0.84] |  | 0.49 | 0.49 | 0.48 | [0.19 0.9] |
| OSI |  | 0.41 | 0.4 | 0.39 | [0.17 0.73] |  | 0.41 | 0.4 | 0.4 | [0.12 0.84] |  | 0.48 | 0.47 | 0.46 | [0.12 0.93] |
| PDE |  | 0.4 | 0.38 | 0.37 | [0.12 0.85] |  | 0.44 | 0.42 | 0.42 | [0.14 0.87] |  | 0.48 | 0.47 | 0.46 | [0.18 0.91] |
| SBSM |  | 0.47 | 0.46 | 0.45 | [0.2 0.88] |  | 0.47 | 0.46 | 0.46 | [0.15 0.78] |  | 0.47 | 0.47 | 0.45 | [0.23 0.86] |
| SMCA |  | 0.38 | 0.37 | 0.35 | [0.11 0.74] |  | 0.41 | 0.4 | 0.39 | [0.16 0.8] |  | 0.47 | 0.46 | 0.46 | [0.18 0.87] |
| STNI |  | 0.34 | 0.33 | 0.31 | [0.13 0.8] |  | 0.42 | 0.41 | 0.39 | [0.16 0.75] |  | 0.52 | 0.51 | 0.51 | [0.22 0.89] |
| USC |  | 0.37 | 0.36 | 0.34 | [0.15 0.82] |  | 0.42 | 0.41 | 0.4 | [0.16 0.79] |  | 0.49 | 0.48 | 0.48 | [0.18 0.87] |
| WNGC |  | 0.41 | 0.39 | 0.37 | [0.1 0.84] |  | 0.44 | 0.43 | 0.42 | [0.14 0.9] |  | 0.49 | 0.48 | 0.47 | [0.15 0.84] |
| WSS |  | 0.38 | 0.37 | 0.35 | [0.14 0.79] |  | 0.43 | 0.42 | 0.42 | [0.17 0.82] |  | 0.47 | 0.46 | 0.45 | [0.17 0.83] |
| s022 |  | 0.36 | 0.36 | 0.34 | [0.12 0.67] |  | 0.43 | 0.42 | 0.41 | [0.15 0.86] |  | 0.49 | 0.48 | 0.47 | [0.19 1.07] |

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
| T-independent | 0.44 | 0.43 | 0.02 | [0.41 0.45] | [0.38 0.49] |
| 3 | 0.39 | 0.39 | 0.03 | [0.36 0.42] | [0.34 0.44] |
| 4 | 0.4 | 0.4 | 0.03 | [0.37 0.42] | [0.35 0.46] |
| 5 | 0.43 | 0.43 | 0.02 | [0.41 0.45] | [0.37 0.48] |
| 7.5 | 0.46 | 0.46 | 0.03 | [0.43 0.48] | [0.4 0.52] |
| 10 | 0.49 | 0.48 | 0.02 | [0.46 0.5] | [0.43 0.54] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_100km_s022_downsampled_hist_3s.png) |  |  |


### All Distances M7.2 Source-strike Results
*[(top)](#table-of-contents)*

![Source-strike Variability](resources/source_strike_m7.2_std_dev.png)

| Site | 3s &phi;<sub>s</sub> | Total | Mean | Median | Range | 5s &phi;<sub>s</sub> | Total | Mean | Median | Range | 10s &phi;<sub>s</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.38** | **0.37** | **0.35** | **[0.08 0.9]** |  | **0.41** | **0.4** | **0.39** | **[0.11 0.9]** |  | **0.44** | **0.43** | **0.42** | **[0.1 1.07]** |
| LAF |  | 0.35 | 0.34 | 0.32 | [0.11 0.8] |  | 0.41 | 0.4 | 0.38 | [0.13 0.84] |  | 0.45 | 0.44 | 0.43 | [0.14 0.9] |
| OSI |  | 0.39 | 0.38 | 0.37 | [0.15 0.78] |  | 0.38 | 0.38 | 0.36 | [0.12 0.84] |  | 0.43 | 0.41 | 0.41 | [0.1 0.93] |
| PDE |  | 0.39 | 0.38 | 0.36 | [0.12 0.85] |  | 0.42 | 0.41 | 0.4 | [0.13 0.87] |  | 0.44 | 0.43 | 0.43 | [0.12 0.91] |
| SBSM |  | 0.45 | 0.44 | 0.43 | [0.17 0.88] |  | 0.43 | 0.43 | 0.41 | [0.15 0.78] |  | 0.42 | 0.41 | 0.41 | [0.1 0.86] |
| SMCA |  | 0.38 | 0.37 | 0.35 | [0.11 0.89] |  | 0.41 | 0.4 | 0.39 | [0.15 0.82] |  | 0.44 | 0.42 | 0.42 | [0.11 0.87] |
| STNI |  | 0.33 | 0.32 | 0.31 | [0.13 0.8] |  | 0.39 | 0.38 | 0.37 | [0.14 0.82] |  | 0.47 | 0.46 | 0.46 | [0.13 0.89] |
| USC |  | 0.37 | 0.36 | 0.34 | [0.12 0.82] |  | 0.41 | 0.4 | 0.39 | [0.11 0.79] |  | 0.45 | 0.43 | 0.43 | [0.12 0.87] |
| WNGC |  | 0.4 | 0.39 | 0.37 | [0.1 0.9] |  | 0.42 | 0.41 | 0.4 | [0.13 0.9] |  | 0.44 | 0.43 | 0.43 | [0.14 0.84] |
| WSS |  | 0.38 | 0.37 | 0.35 | [0.13 0.81] |  | 0.41 | 0.4 | 0.39 | [0.14 0.9] |  | 0.42 | 0.41 | 0.41 | [0.11 0.88] |
| s022 |  | 0.35 | 0.34 | 0.32 | [0.08 0.74] |  | 0.4 | 0.39 | 0.37 | [0.14 0.89] |  | 0.45 | 0.43 | 0.42 | [0.14 1.07] |

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
| T-independent | 0.41 | 0.41 | 0.01 | [0.4 0.42] | [0.4 0.42] |
| 3 | 0.38 | 0.38 | 0.01 | [0.37 0.39] | [0.36 0.4] |
| 4 | 0.38 | 0.38 | 0.01 | [0.38 0.39] | [0.36 0.4] |
| 5 | 0.41 | 0.41 | 0.01 | [0.4 0.42] | [0.39 0.43] |
| 7.5 | 0.43 | 0.43 | 0.01 | [0.42 0.44] | [0.41 0.45] |
| 10 | 0.44 | 0.44 | 0.01 | [0.43 0.45] | [0.43 0.46] |

These plots show the distribution of period-independent downsampled &phi;<sub>s</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/source_strike_m7.2_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/source_strike_m7.2_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/source_strike_m7.2_s022_downsampled_hist_3s.png) |  |  |


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


### 20.0 km M7.2 Within-event, single-site Results
*[(top)](#table-of-contents)*

![Within-event, single-site Variability](resources/within_event_ss_m7.2_20km_std_dev.png)

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.41** | **0.4** | **0.37** | **[0.24 0.76]** |  | **0.41** | **0.4** | **0.39** | **[0.25 0.65]** |  | **0.36** | **0.34** | **0.32** | **[0.13 0.72]** |
| LAF |  | 0.38 | 0.38 | 0.35 | [0.29 0.58] |  | 0.41 | 0.41 | 0.4 | [0.3 0.59] |  | 0.38 | 0.36 | 0.34 | [0.2 0.7] |
| OSI |  | 0.39 | 0.38 | 0.35 | [0.24 0.59] |  | 0.36 | 0.35 | 0.34 | [0.25 0.5] |  | 0.33 | 0.31 | 0.3 | [0.13 0.61] |
| PDE |  | 0.38 | 0.37 | 0.34 | [0.28 0.6] |  | 0.39 | 0.38 | 0.36 | [0.26 0.53] |  | 0.35 | 0.33 | 0.31 | [0.17 0.63] |
| SBSM |  | 0.44 | 0.43 | 0.42 | [0.33 0.69] |  | 0.4 | 0.39 | 0.38 | [0.27 0.59] |  | 0.32 | 0.3 | 0.28 | [0.14 0.55] |
| SMCA |  | 0.41 | 0.41 | 0.39 | [0.3 0.59] |  | 0.42 | 0.42 | 0.41 | [0.32 0.6] |  | 0.36 | 0.35 | 0.32 | [0.17 0.67] |
| STNI |  | 0.35 | 0.34 | 0.32 | [0.25 0.55] |  | 0.38 | 0.37 | 0.36 | [0.27 0.6] |  | 0.38 | 0.36 | 0.34 | [0.18 0.72] |
| USC |  | 0.39 | 0.38 | 0.36 | [0.29 0.57] |  | 0.41 | 0.4 | 0.4 | [0.29 0.58] |  | 0.37 | 0.36 | 0.33 | [0.19 0.68] |
| WNGC |  | 0.59 | 0.58 | 0.57 | [0.45 0.76] |  | 0.51 | 0.51 | 0.5 | [0.36 0.65] |  | 0.37 | 0.35 | 0.34 | [0.19 0.67] |
| WSS |  | 0.42 | 0.42 | 0.4 | [0.31 0.58] |  | 0.41 | 0.41 | 0.4 | [0.3 0.55] |  | 0.34 | 0.32 | 0.29 | [0.14 0.64] |
| s022 |  | 0.34 | 0.33 | 0.31 | [0.25 0.55] |  | 0.38 | 0.37 | 0.35 | [0.26 0.64] |  | 0.39 | 0.37 | 0.34 | [0.19 0.7] |

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
| T-independent | 0.4 | 0.39 | 0.02 | [0.37 0.41] | [0.35 0.43] |
| 3 | 0.41 | 0.41 | 0.02 | [0.39 0.43] | [0.37 0.45] |
| 4 | 0.41 | 0.4 | 0.02 | [0.38 0.42] | [0.36 0.45] |
| 5 | 0.41 | 0.4 | 0.02 | [0.38 0.42] | [0.36 0.45] |
| 7.5 | 0.39 | 0.38 | 0.02 | [0.36 0.41] | [0.34 0.43] |
| 10 | 0.36 | 0.36 | 0.03 | [0.32 0.38] | [0.3 0.41] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_20km_s022_downsampled_hist_3s.png) |  |  |

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

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.47** | **0.46** | **0.43** | **[0.25 0.78]** |  | **0.46** | **0.46** | **0.45** | **[0.28 0.69]** |  | **0.48** | **0.47** | **0.46** | **[0.32 0.79]** |
| LAF |  | 0.4 | 0.39 | 0.38 | [0.3 0.61] |  | 0.44 | 0.44 | 0.42 | [0.32 0.65] |  | 0.49 | 0.48 | 0.47 | [0.33 0.76] |
| OSI |  | 0.45 | 0.45 | 0.44 | [0.36 0.58] |  | 0.41 | 0.41 | 0.4 | [0.31 0.55] |  | 0.47 | 0.46 | 0.45 | [0.33 0.7] |
| PDE |  | 0.46 | 0.45 | 0.43 | [0.34 0.64] |  | 0.45 | 0.45 | 0.43 | [0.31 0.6] |  | 0.49 | 0.48 | 0.47 | [0.34 0.75] |
| SBSM |  | 0.6 | 0.6 | 0.59 | [0.46 0.77] |  | 0.53 | 0.52 | 0.51 | [0.37 0.67] |  | 0.47 | 0.46 | 0.45 | [0.33 0.64] |
| SMCA |  | 0.53 | 0.52 | 0.51 | [0.41 0.72] |  | 0.47 | 0.47 | 0.45 | [0.35 0.68] |  | 0.48 | 0.47 | 0.46 | [0.34 0.75] |
| STNI |  | 0.38 | 0.37 | 0.35 | [0.28 0.58] |  | 0.45 | 0.44 | 0.42 | [0.33 0.65] |  | 0.5 | 0.49 | 0.49 | [0.33 0.75] |
| USC |  | 0.41 | 0.4 | 0.38 | [0.31 0.62] |  | 0.45 | 0.44 | 0.43 | [0.31 0.62] |  | 0.49 | 0.47 | 0.46 | [0.33 0.76] |
| WNGC |  | 0.63 | 0.62 | 0.61 | [0.49 0.78] |  | 0.53 | 0.53 | 0.52 | [0.41 0.67] |  | 0.47 | 0.46 | 0.46 | [0.33 0.72] |
| WSS |  | 0.43 | 0.43 | 0.42 | [0.34 0.63] |  | 0.47 | 0.46 | 0.45 | [0.33 0.62] |  | 0.46 | 0.45 | 0.44 | [0.32 0.72] |
| s022 |  | 0.38 | 0.37 | 0.35 | [0.25 0.58] |  | 0.42 | 0.42 | 0.4 | [0.28 0.69] |  | 0.48 | 0.46 | 0.44 | [0.32 0.79] |

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
| T-independent | 0.47 | 0.44 | 0.02 | [0.42 0.47] | [0.4 0.5] |
| 3 | 0.47 | 0.45 | 0.03 | [0.42 0.48] | [0.39 0.5] |
| 4 | 0.46 | 0.44 | 0.03 | [0.41 0.46] | [0.38 0.49] |
| 5 | 0.46 | 0.44 | 0.03 | [0.41 0.47] | [0.39 0.5] |
| 7.5 | 0.47 | 0.45 | 0.03 | [0.42 0.47] | [0.4 0.51] |
| 10 | 0.48 | 0.45 | 0.03 | [0.43 0.49] | [0.41 0.52] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_50km_s022_downsampled_hist_3s.png) |  |  |

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

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.53** | **0.52** | **0.48** | **[0.33 0.82]** |  | **0.52** | **0.51** | **0.51** | **[0.34 0.74]** |  | **0.51** | **0.5** | **0.48** | **[0.32 0.85]** |
| LAF |  | 0.49 | 0.48 | 0.47 | [0.39 0.7] |  | 0.49 | 0.48 | 0.47 | [0.34 0.62] |  | 0.51 | 0.5 | 0.48 | [0.36 0.8] |
| OSI |  | 0.5 | 0.49 | 0.49 | [0.4 0.65] |  | 0.47 | 0.47 | 0.46 | [0.38 0.62] |  | 0.48 | 0.47 | 0.45 | [0.32 0.79] |
| PDE |  | 0.46 | 0.45 | 0.45 | [0.36 0.6] |  | 0.47 | 0.47 | 0.46 | [0.37 0.63] |  | 0.49 | 0.47 | 0.45 | [0.34 0.8] |
| SBSM |  | 0.66 | 0.66 | 0.65 | [0.56 0.8] |  | 0.58 | 0.58 | 0.57 | [0.44 0.71] |  | 0.49 | 0.49 | 0.48 | [0.36 0.72] |
| SMCA |  | 0.61 | 0.61 | 0.6 | [0.53 0.77] |  | 0.51 | 0.51 | 0.51 | [0.4 0.67] |  | 0.51 | 0.5 | 0.48 | [0.37 0.79] |
| STNI |  | 0.42 | 0.41 | 0.4 | [0.33 0.58] |  | 0.5 | 0.5 | 0.48 | [0.39 0.63] |  | 0.54 | 0.53 | 0.51 | [0.38 0.81] |
| USC |  | 0.48 | 0.47 | 0.46 | [0.39 0.67] |  | 0.53 | 0.52 | 0.51 | [0.42 0.66] |  | 0.53 | 0.52 | 0.49 | [0.39 0.79] |
| WNGC |  | 0.67 | 0.67 | 0.67 | [0.58 0.82] |  | 0.59 | 0.59 | 0.57 | [0.47 0.74] |  | 0.5 | 0.49 | 0.48 | [0.35 0.76] |
| WSS |  | 0.49 | 0.48 | 0.47 | [0.37 0.67] |  | 0.52 | 0.52 | 0.51 | [0.4 0.64] |  | 0.48 | 0.47 | 0.45 | [0.34 0.75] |
| s022 |  | 0.43 | 0.43 | 0.42 | [0.35 0.6] |  | 0.49 | 0.48 | 0.47 | [0.37 0.66] |  | 0.52 | 0.51 | 0.49 | [0.4 0.85] |

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
| T-independent | 0.52 | 0.51 | 0.02 | [0.49 0.53] | [0.47 0.54] |
| 3 | 0.53 | 0.52 | 0.02 | [0.5 0.54] | [0.47 0.56] |
| 4 | 0.52 | 0.51 | 0.02 | [0.48 0.53] | [0.47 0.55] |
| 5 | 0.52 | 0.51 | 0.02 | [0.49 0.54] | [0.47 0.55] |
| 7.5 | 0.51 | 0.51 | 0.02 | [0.49 0.54] | [0.46 0.56] |
| 10 | 0.51 | 0.5 | 0.03 | [0.47 0.52] | [0.45 0.56] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_100km_s022_downsampled_hist_3s.png) |  |  |

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

| Site | 3s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 5s &phi;<sub>SS</sub> | Total | Mean | Median | Range | 10s &phi;<sub>SS</sub> | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **ALL SITES** |  | **0.48** | **0.46** | **0.44** | **[0.24 0.82]** |  | **0.47** | **0.46** | **0.45** | **[0.25 0.74]** |  | **0.45** | **0.43** | **0.44** | **[0.13 0.85]** |
| LAF |  | 0.43 | 0.42 | 0.4 | [0.29 0.7] |  | 0.45 | 0.44 | 0.43 | [0.3 0.65] |  | 0.46 | 0.45 | 0.45 | [0.2 0.8] |
| OSI |  | 0.45 | 0.44 | 0.45 | [0.24 0.65] |  | 0.42 | 0.41 | 0.41 | [0.25 0.62] |  | 0.43 | 0.41 | 0.41 | [0.13 0.79] |
| PDE |  | 0.43 | 0.42 | 0.41 | [0.28 0.64] |  | 0.44 | 0.43 | 0.42 | [0.26 0.63] |  | 0.45 | 0.43 | 0.43 | [0.17 0.8] |
| SBSM |  | 0.58 | 0.56 | 0.58 | [0.33 0.8] |  | 0.51 | 0.5 | 0.51 | [0.27 0.71] |  | 0.43 | 0.42 | 0.43 | [0.14 0.72] |
| SMCA |  | 0.53 | 0.51 | 0.53 | [0.3 0.77] |  | 0.47 | 0.47 | 0.46 | [0.32 0.68] |  | 0.45 | 0.44 | 0.44 | [0.17 0.79] |
| STNI |  | 0.38 | 0.37 | 0.36 | [0.25 0.58] |  | 0.44 | 0.43 | 0.43 | [0.27 0.65] |  | 0.48 | 0.46 | 0.47 | [0.18 0.81] |
| USC |  | 0.43 | 0.42 | 0.41 | [0.29 0.67] |  | 0.46 | 0.46 | 0.44 | [0.29 0.66] |  | 0.47 | 0.45 | 0.46 | [0.19 0.79] |
| WNGC |  | 0.63 | 0.63 | 0.62 | [0.45 0.82] |  | 0.55 | 0.54 | 0.53 | [0.36 0.74] |  | 0.45 | 0.44 | 0.44 | [0.19 0.76] |
| WSS |  | 0.45 | 0.44 | 0.43 | [0.31 0.67] |  | 0.47 | 0.46 | 0.45 | [0.3 0.64] |  | 0.43 | 0.41 | 0.41 | [0.14 0.75] |
| s022 |  | 0.39 | 0.38 | 0.37 | [0.25 0.6] |  | 0.43 | 0.42 | 0.41 | [0.26 0.69] |  | 0.47 | 0.45 | 0.45 | [0.19 0.85] |

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
| T-independent | 0.46 | 0.46 | 0.01 | [0.45 0.47] | [0.44 0.48] |
| 3 | 0.48 | 0.47 | 0.01 | [0.46 0.48] | [0.46 0.5] |
| 4 | 0.46 | 0.46 | 0.01 | [0.45 0.47] | [0.44 0.48] |
| 5 | 0.47 | 0.46 | 0.01 | [0.46 0.48] | [0.45 0.48] |
| 7.5 | 0.46 | 0.46 | 0.01 | [0.45 0.47] | [0.44 0.49] |
| 10 | 0.45 | 0.45 | 0.01 | [0.44 0.47] | [0.42 0.48] |

These plots show the distribution of period-independent downsampled &phi;<sub>SS</sub> for each site.

| Period | **LAF** | **OSI** | **PDE** | **SBSM** |
|-----|-----|-----|-----|-----|
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_LAF_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_OSI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PDE_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SBSM_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_LAF_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_OSI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_PDE_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SBSM_downsampled_hist_3s.png) |
| Period | **SMCA** | **STNI** | **USC** | **WNGC** |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SMCA_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_STNI_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WNGC_downsampled_hist_period_indep.png) |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_SMCA_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_STNI_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_USC_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WNGC_downsampled_hist_3s.png) |
| Period | **WSS** | **s022** |  |  |
| Period-Indep | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WSS_downsampled_hist_period_indep.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_s022_downsampled_hist_period_indep.png) |  |  |
| 3s | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_WSS_downsampled_hist_3s.png) | ![Dowmsampled Histogram](resources/within_event_ss_m7.2_s022_downsampled_hist_3s.png) |  |  |

These plots show the dependence of &phi;<sub>SS</sub> to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (324), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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


### 20.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_20km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.5** | **0.5** | **0.49** | **[0.13 1.04]** |  | **0.53** | **0.54** | **0.53** | **[0.15 1.12]** |  | **0.53** | **0.53** | **0.51** | **[0.18 1.28]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_20km_3s_hist.png) | ![5s](resources/within_event_m7.2_20km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_20km_10s_hist.png) |  |

#### 20.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 34 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 17 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.53 | 0.51 | 0.05 | [0.46 0.57] | [0.41 0.63] |
| 3 | 0.5 | 0.5 | 0.07 | [0.43 0.57] | [0.37 0.61] |
| 4 | 0.52 | 0.51 | 0.07 | [0.46 0.58] | [0.39 0.7] |
| 5 | 0.53 | 0.53 | 0.07 | [0.45 0.59] | [0.39 0.68] |
| 7.5 | 0.55 | 0.54 | 0.07 | [0.47 0.6] | [0.41 0.68] |
| 10 | 0.53 | 0.52 | 0.07 | [0.44 0.6] | [0.41 0.67] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_20km_downsampled_hist_3s.png) |


### 50.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_50km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.57** | **0.57** | **0.56** | **[0.14 1.23]** |  | **0.63** | **0.63** | **0.63** | **[0.18 1.31]** |  | **0.64** | **0.64** | **0.63** | **[0.19 1.46]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_50km_3s_hist.png) | ![5s](resources/within_event_m7.2_50km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_50km_10s_hist.png) |  |

#### 50.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.62 | 0.61 | 0.07 | [0.53 0.67] | [0.48 0.75] |
| 3 | 0.57 | 0.56 | 0.09 | [0.48 0.65] | [0.38 0.78] |
| 4 | 0.59 | 0.57 | 0.08 | [0.5 0.67] | [0.43 0.77] |
| 5 | 0.63 | 0.61 | 0.08 | [0.52 0.69] | [0.46 0.81] |
| 7.5 | 0.66 | 0.65 | 0.09 | [0.56 0.74] | [0.46 0.86] |
| 10 | 0.64 | 0.64 | 0.1 | [0.53 0.73] | [0.43 0.85] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_50km_downsampled_hist_3s.png) |


### 100.0 km M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_100km_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.61** | **0.61** | **0.6** | **[0.17 1.39]** |  | **0.67** | **0.68** | **0.67** | **[0.19 1.34]** |  | **0.66** | **0.67** | **0.66** | **[0.09 1.46]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_100km_3s_hist.png) | ![5s](resources/within_event_m7.2_100km_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_100km_10s_hist.png) |  |

#### 100.0 km M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 25 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 36 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.66 | 0.65 | 0.08 | [0.57 0.75] | [0.51 0.86] |
| 3 | 0.61 | 0.6 | 0.11 | [0.49 0.71] | [0.43 0.87] |
| 4 | 0.64 | 0.63 | 0.1 | [0.55 0.75] | [0.45 0.91] |
| 5 | 0.67 | 0.66 | 0.1 | [0.57 0.77] | [0.52 0.9] |
| 7.5 | 0.7 | 0.7 | 0.1 | [0.6 0.81] | [0.52 0.89] |
| 10 | 0.66 | 0.65 | 0.09 | [0.56 0.75] | [0.48 0.87] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_100km_downsampled_hist_3s.png) |


### All Distances M7.2 Within-event Results
*[(top)](#table-of-contents)*

![Within-event Variability](resources/within_event_m7.2_std_dev.png)

| Site | 3s &phi; | Total | Mean | Median | Range | 5s &phi; | Total | Mean | Median | Range | 10s &phi; | Total | Mean | Median | Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** |  | **0.56** | **0.56** | **0.55** | **[0.13 1.39]** |  | **0.61** | **0.62** | **0.61** | **[0.15 1.34]** |  | **0.61** | **0.61** | **0.6** | **[0.09 1.46]** |

Here are plots of the histogram of &phi; for each individual rupture, from which we compute a total &phi;

| 3s | 5s |
|-----|-----|
| ![3s](resources/within_event_m7.2_3s_hist.png) | ![5s](resources/within_event_m7.2_5s_hist.png) |
| 10s |  |
| ![10s](resources/within_event_m7.2_10s_hist.png) |  |

#### All Distances M7.2 Within-event Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &phi; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 162 recordings. We then downsample our simulated data 100 times for each site, and compute &phi; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

*WARNING: Some real events had more recordings than we have rotations per event, so our dataset for this test is smaller. We are using 400 fewer data points.*

| Period (s) | Full &phi; | Downsampled median &phi; | Downsampled &phi; std. dev. | Downsampled &phi; 68% conf range | Downsampled &phi; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.6 | 0.6 | 0.03 | [0.57 0.63] | [0.54 0.68] |
| 3 | 0.56 | 0.56 | 0.04 | [0.53 0.59] | [0.48 0.64] |
| 4 | 0.59 | 0.59 | 0.04 | [0.55 0.62] | [0.51 0.66] |
| 5 | 0.61 | 0.61 | 0.03 | [0.58 0.64] | [0.55 0.7] |
| 7.5 | 0.64 | 0.64 | 0.04 | [0.6 0.68] | [0.57 0.73] |
| 10 | 0.61 | 0.61 | 0.04 | [0.58 0.65] | [0.54 0.7] |

This plot shows the distribution of period-independent downsampled &phi;.

| Period-Indep | ![Dowmsampled Histogram](resources/within_event_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/within_event_m7.2_downsampled_hist_3s.png) |


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


### 20.0 km M7.2 Between-events Results
*[(top)](#table-of-contents)*

![Between-events Variability](resources/between_events_m7.2_20km_std_dev.png)

| Site | 3s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 5s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range | 10s &tau; | Mean &delta;B<sub>e</sub> | &delta;B<sub>e</sub> Range |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **10 sites, V<sub>S30</sub>=500** | **0.18** | **-2.31** | **[-2.65 -1.85]** | **0.25** | **-2.92** | **[-3.39 -2.38]** | **0.29** | **-4.08** | **[-4.78 -3.49]** |
| LAF | 0.17 | -2.51 | [-2.86 -2.09] | 0.24 | -2.89 | [-3.36 -2.45] | 0.3 | -3.91 | [-4.6 -3.31] |
| OSI | 0.18 | -3.01 | [-3.35 -2.48] | 0.25 | -3.9 | [-4.33 -3.23] | 0.28 | -4.81 | [-5.48 -4.28] |
| PDE | 0.19 | -2.31 | [-2.67 -1.83] | 0.27 | -2.96 | [-3.45 -2.36] | 0.3 | -4.15 | [-4.87 -3.57] |
| SBSM | 0.21 | -1.92 | [-2.37 -1.32] | 0.28 | -2.95 | [-3.43 -2.26] | 0.29 | -4.47 | [-5.13 -3.84] |
| SMCA | 0.19 | -2.2 | [-2.55 -1.72] | 0.26 | -2.69 | [-3.16 -2.11] | 0.31 | -3.94 | [-4.65 -3.32] |
| STNI | 0.18 | -2.18 | [-2.52 -1.73] | 0.23 | -2.61 | [-3.02 -2.19] | 0.33 | -3.42 | [-4.23 -2.79] |
| USC | 0.18 | -2.28 | [-2.62 -1.79] | 0.24 | -2.89 | [-3.37 -2.42] | 0.32 | -3.92 | [-4.65 -3.3] |
| WNGC | 0.17 | -2.29 | [-2.64 -1.86] | 0.24 | -2.93 | [-3.46 -2.41] | 0.3 | -4.08 | [-4.78 -3.5] |
| WSS | 0.19 | -2.56 | [-2.88 -2.05] | 0.27 | -3.16 | [-3.64 -2.48] | 0.29 | -4.45 | [-5.13 -3.86] |
| s022 | 0.17 | -2.08 | [-2.41 -1.69] | 0.24 | -2.7 | [-3.16 -2.25] | 0.29 | -3.67 | [-4.36 -3.12] |

#### 20.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [10.0 30.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 51 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.25 | 0.28 | 0.1 | [0.19 0.39] | [0.12 0.5] |
| 3 | 0.18 | 0.24 | 0.1 | [0.13 0.34] | [0.05 0.46] |
| 4 | 0.23 | 0.26 | 0.11 | [0.14 0.38] | [0.08 0.48] |
| 5 | 0.25 | 0.29 | 0.12 | [0.16 0.41] | [0.07 0.54] |
| 7.5 | 0.28 | 0.32 | 0.13 | [0.21 0.47] | [0.06 0.65] |
| 10 | 0.29 | 0.32 | 0.13 | [0.2 0.47] | [0.1 0.62] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_20km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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
| **10 sites, V<sub>S30</sub>=500** | **0.2** | **-3.05** | **[-3.39 -2.56]** | **0.28** | **-3.48** | **[-4.11 -2.91]** | **0.31** | **-4.65** | **[-5.42 -4.01]** |
| LAF | 0.2 | -3.11 | [-3.45 -2.61] | 0.29 | -3.29 | [-3.87 -2.73] | 0.33 | -4.41 | [-5.21 -3.72] |
| OSI | 0.18 | -3.86 | [-4.18 -3.34] | 0.24 | -4.62 | [-5.06 -4.06] | 0.31 | -5.4 | [-6.18 -4.79] |
| PDE | 0.2 | -3.13 | [-3.46 -2.61] | 0.28 | -3.64 | [-4.21 -3.08] | 0.32 | -4.74 | [-5.57 -4.1] |
| SBSM | 0.22 | -2.57 | [-2.95 -2.04] | 0.29 | -3.55 | [-4.21 -2.91] | 0.29 | -5.04 | [-5.71 -4.47] |
| SMCA | 0.2 | -3.05 | [-3.4 -2.55] | 0.26 | -3.39 | [-4.01 -2.83] | 0.31 | -4.55 | [-5.32 -3.91] |
| STNI | 0.2 | -2.84 | [-3.18 -2.37] | 0.3 | -3 | [-3.63 -2.4] | 0.35 | -3.91 | [-4.8 -3.19] |
| USC | 0.2 | -2.99 | [-3.3 -2.49] | 0.29 | -3.4 | [-3.97 -2.8] | 0.33 | -4.46 | [-5.3 -3.8] |
| WNGC | 0.21 | -3.08 | [-3.43 -2.5] | 0.28 | -3.43 | [-3.93 -2.86] | 0.32 | -4.62 | [-5.41 -3.93] |
| WSS | 0.2 | -3.34 | [-3.65 -2.79] | 0.27 | -3.86 | [-4.42 -3.22] | 0.3 | -5.09 | [-5.81 -4.46] |
| s022 | 0.2 | -2.77 | [-3.13 -2.26] | 0.29 | -3.22 | [-3.82 -2.64] | 0.33 | -4.12 | [-5 -3.48] |

#### 50.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [40.0 60.0] km. We throw out any events with only 1 recording, leaving us with 4 events and a total of 26 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.27 | 0.37 | 0.13 | [0.25 0.51] | [0.16 0.66] |
| 3 | 0.2 | 0.29 | 0.12 | [0.18 0.4] | [0.09 0.6] |
| 4 | 0.25 | 0.35 | 0.15 | [0.19 0.5] | [0.07 0.67] |
| 5 | 0.28 | 0.39 | 0.18 | [0.2 0.57] | [0.1 0.78] |
| 7.5 | 0.32 | 0.43 | 0.19 | [0.24 0.6] | [0.14 0.87] |
| 10 | 0.31 | 0.41 | 0.17 | [0.26 0.57] | [0.13 0.83] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_50km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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
| **10 sites, V<sub>S30</sub>=500** | **0.21** | **-3.73** | **[-4.1 -3.21]** | **0.29** | **-4.05** | **[-4.73 -3.45]** | **0.32** | **-5.14** | **[-5.87 -4.5]** |
| LAF | 0.22 | -3.82 | [-4.19 -3.31] | 0.31 | -3.84 | [-4.56 -3.22] | 0.33 | -4.9 | [-5.66 -4.22] |
| OSI | 0.18 | -4.54 | [-4.81 -4.07] | 0.24 | -5.25 | [-5.75 -4.7] | 0.32 | -5.92 | [-6.69 -5.3] |
| PDE | 0.2 | -3.78 | [-4.14 -3.25] | 0.27 | -4.25 | [-4.79 -3.73] | 0.32 | -5.25 | [-6.04 -4.61] |
| SBSM | 0.23 | -3.25 | [-3.63 -2.7] | 0.29 | -4.12 | [-4.76 -3.49] | 0.3 | -5.57 | [-6.21 -4.92] |
| SMCA | 0.21 | -3.74 | [-4.12 -3.22] | 0.29 | -3.89 | [-4.52 -3.32] | 0.32 | -5.04 | [-5.77 -4.43] |
| STNI | 0.21 | -3.53 | [-3.9 -3.02] | 0.31 | -3.57 | [-4.29 -2.98] | 0.34 | -4.39 | [-5.21 -3.72] |
| USC | 0.21 | -3.67 | [-4.01 -3.14] | 0.3 | -3.96 | [-4.67 -3.34] | 0.33 | -4.95 | [-5.71 -4.31] |
| WNGC | 0.22 | -3.72 | [-4.12 -3.14] | 0.3 | -3.99 | [-4.65 -3.36] | 0.32 | -5.11 | [-5.85 -4.45] |
| WSS | 0.2 | -4.03 | [-4.39 -3.51] | 0.28 | -4.44 | [-5.07 -3.83] | 0.32 | -5.57 | [-6.32 -4.92] |
| s022 | 0.2 | -3.4 | [-3.76 -2.89] | 0.3 | -3.77 | [-4.46 -3.17] | 0.33 | -4.62 | [-5.42 -3.96] |

#### 100.0 km M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and distance within the range [80.0 120.0] km. We throw out any events with only 1 recording, leaving us with 3 events and a total of 61 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.28 | 0.31 | 0.12 | [0.2 0.48] | [0.14 0.6] |
| 3 | 0.21 | 0.24 | 0.13 | [0.13 0.41] | [0.03 0.55] |
| 4 | 0.26 | 0.28 | 0.15 | [0.13 0.43] | [0.06 0.71] |
| 5 | 0.29 | 0.35 | 0.16 | [0.18 0.51] | [0.09 0.7] |
| 7.5 | 0.31 | 0.39 | 0.16 | [0.23 0.55] | [0.08 0.75] |
| 10 | 0.32 | 0.37 | 0.17 | [0.2 0.57] | [0.07 0.78] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_100km_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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
| **10 sites, V<sub>S30</sub>=500** | **0.2** | **-3.03** | **[-4.1 -1.85]** | **0.27** | **-3.48** | **[-4.73 -2.38]** | **0.31** | **-4.62** | **[-5.87 -3.49]** |
| LAF | 0.2 | -3.15 | [-4.19 -2.09] | 0.28 | -3.34 | [-4.56 -2.45] | 0.32 | -4.41 | [-5.66 -3.31] |
| OSI | 0.18 | -3.8 | [-4.81 -2.48] | 0.25 | -4.59 | [-5.75 -3.23] | 0.3 | -5.38 | [-6.69 -4.28] |
| PDE | 0.2 | -3.07 | [-4.14 -1.83] | 0.27 | -3.61 | [-4.79 -2.36] | 0.31 | -4.71 | [-6.04 -3.57] |
| SBSM | 0.22 | -2.58 | [-3.63 -1.32] | 0.29 | -3.54 | [-4.76 -2.26] | 0.29 | -5.03 | [-6.21 -3.84] |
| SMCA | 0.2 | -3 | [-4.12 -1.72] | 0.27 | -3.32 | [-4.52 -2.11] | 0.31 | -4.51 | [-5.77 -3.32] |
| STNI | 0.2 | -2.85 | [-3.9 -1.73] | 0.28 | -3.06 | [-4.29 -2.19] | 0.34 | -3.91 | [-5.21 -2.79] |
| USC | 0.2 | -2.98 | [-4.01 -1.79] | 0.27 | -3.41 | [-4.67 -2.42] | 0.32 | -4.44 | [-5.71 -3.3] |
| WNGC | 0.2 | -3.03 | [-4.12 -1.86] | 0.27 | -3.45 | [-4.65 -2.41] | 0.31 | -4.6 | [-5.85 -3.5] |
| WSS | 0.2 | -3.31 | [-4.39 -2.05] | 0.28 | -3.82 | [-5.07 -2.48] | 0.3 | -5.03 | [-6.32 -3.86] |
| s022 | 0.19 | -2.75 | [-3.76 -1.69] | 0.27 | -3.23 | [-4.46 -2.25] | 0.32 | -4.14 | [-5.42 -3.12] |

#### All Distances M7.2 Between-events Downsampled Results
*[(top)](#table-of-contents)*

We compute uncertainties on &tau; through downsampling the rotational synthetic data to match the sample sizes used in the ASK 2014 regressions. We search the ASK dataset for ruptures with the same mechanism, magnitude in the range [7.0 7.4], and all distances. We throw out any events with only 1 recording, leaving us with 6 events and a total of 1686 recordings. We then downsample our simulated data 100 times for each site, and compute &tau; from each sample. The 95% confidence range from these samples is plotted as a shaded region above, and listed in the table below. Weighted standard deviations are calculated, weighted by the square-root of the number of recordings in each event.

| Period (s) | Full &tau; | Downsampled median &tau; | Downsampled &tau; std. dev. | Downsampled &tau; 68% conf range | Downsampled &tau; 95% conf range |
|-----|-----|-----|-----|-----|-----|
| T-independent | 0.27 | 0.28 | 0.05 | [0.23 0.33] | [0.2 0.36] |
| 3 | 0.2 | 0.21 | 0.04 | [0.17 0.27] | [0.14 0.3] |
| 4 | 0.24 | 0.26 | 0.05 | [0.21 0.31] | [0.14 0.36] |
| 5 | 0.27 | 0.29 | 0.05 | [0.23 0.33] | [0.2 0.38] |
| 7.5 | 0.3 | 0.32 | 0.06 | [0.26 0.38] | [0.21 0.44] |
| 10 | 0.31 | 0.33 | 0.07 | [0.25 0.39] | [0.18 0.46] |

This plot shows the distribution of period-independent downsampled &tau;.

| Period-Indep | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_period_indep.png) |
|-----|-----|
| 3s | ![Dowmsampled Histogram](resources/between_events_m7.2_downsampled_hist_3s.png) |

These plots show the dependence of &tau; to the number of events included and the number of recordings per event. The left plot holds the number of recordings per event fixed at the full set of simulated recordings (3240), varying the number of events. The right plot holds the number of events fixed at the full set of simulated events (50), varying the number of recordings per event.

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
| **20 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_v_prop_m7.2_100km_10sites_10s.png) |
### Mag Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mag_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mag_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mag_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mag_m7.2_100km_10sites_10s.png) |
### Log10(Area) Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_area_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_area_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_area_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_area_m7.2_100km_10sites_10s.png) |
### Max Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_max_slip_m7.2_100km_10sites_10s.png) |
### Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mean_slip_m7.2_100km_10sites_10s.png) |
### Slip Std Dev Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_slip_std_dev_m7.2_100km_10sites_10s.png) |
### Mid-Seismogenic Mean Slip Event Term Scatters
*[(top)](#table-of-contents)*

|  | 3 s | 5 s | 10 s |
|-----|-----|-----|-----|
| **20 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_20km_10sites_10s.png) |
| **50 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_50km_10sites_10s.png) |
| **100 km** | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_10sites_3s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_10sites_5s.png) | ![plot](resources/event_term_scatter_mid_seis_mean_slip_m7.2_100km_10sites_10s.png) |
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
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/LAF_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### LAF Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/LAF_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### OSI Azumth Dependence
*[(top)](#table-of-contents)*

#### OSI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/OSI_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### OSI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/OSI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### PDE Azumth Dependence
*[(top)](#table-of-contents)*

#### PDE Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/PDE_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### PDE Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/PDE_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SBSM Azumth Dependence
*[(top)](#table-of-contents)*

#### SBSM Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SBSM_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SBSM Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SBSM_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### SMCA Azumth Dependence
*[(top)](#table-of-contents)*

#### SMCA Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/SMCA_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### SMCA Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/SMCA_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### STNI Azumth Dependence
*[(top)](#table-of-contents)*

#### STNI Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/STNI_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### STNI Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/STNI_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### USC Azumth Dependence
*[(top)](#table-of-contents)*

#### USC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/USC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### USC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/USC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WNGC Azumth Dependence
*[(top)](#table-of-contents)*

#### WNGC Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WNGC_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WNGC Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WNGC_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### WSS Azumth Dependence
*[(top)](#table-of-contents)*

#### WSS Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/WSS_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### WSS Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/WSS_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### s022 Azumth Dependence
*[(top)](#table-of-contents)*

#### s022 Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/s022_m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### s022 Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/s022_m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

### All Sites Azumth Dependence
*[(top)](#table-of-contents)*

#### All Sites Rupture Strike Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event_ss.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_between_events.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_within_event.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_within_event.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>P2P</sub>** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_path.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_path.png) |
| **Median SA** | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_3s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_5s_median_sa.png) | ![Rupture Strike](resources/m7.2_dist_SOURCE_AZIMUTH_10s_median_sa.png) |

#### All Sites Path Dependence
*[(top)](#table-of-contents)*

| Type | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **&phi;<sub>SS</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event_ss.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event_ss.png) |
| **&tau;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_between_events.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_between_events.png) |
| **&phi;** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_within_event.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_within_event.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_within_event.png) |
| **&phi;<sub>s</sub>** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_source_strike.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_source_strike.png) |
| **Median SA** | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_3s_median_sa.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_5s_median_sa.png) | ![Path](resources/m7.2_dist_SITE_TO_SOURTH_AZIMUTH_10s_median_sa.png) |

## BBP PartB Comparison
*[(top)](#table-of-contents)*

Here we attempt to reproduce the SCEC BroadBand Platform "Part B" validation exercise as defined in:

*Goulet, C. A., Abrahamson, N. A., Somerville, P. G., & Wooddell, K. E. (2014). The SCEC broadband platform validation exercise: Methodology for code validation in the context of seismicâ€�hazard analyses. Seismological Research Letters, 86(1), 17-26.* [(link)](https://pubs.geoscienceworld.org/ssa/srl/article/86/1/17/315438/the-scec-broadband-platform-validation-exercise)

The BBP exercise positioned sites in a 'racetrack' around the ruptures. Here, we instead position and rotate the ruptures around the site in order to work in 3-D with CyberShake reciprical calculations. Results for official scenarios and distances are in **bold**, results for additional magnitudes or distances not defined in the Goulet et. al. (2014) are *italicised*.

### BBP PartB Summary Table
*[(top)](#table-of-contents)*

| Scenario | Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|-----|
| **M7.2 SS** | **LAF** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **OSI** | *(PASS)* | *(PASS)* | *(PASS)* |
| **M7.2 SS** | **PDE** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **SBSM** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **SMCA** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **STNI** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **USC** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **WNGC** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **WSS** | *(FAIL)* | *(FAIL)* | *(PASS)* |
| **M7.2 SS** | **s022** | *(FAIL)* | *(FAIL)* | *(FAIL)* |
| **M7.2 SS** | **10sites_Vs30_500** | *(FAIL)* | *(FAIL)* | *(FAIL)* |

### BBP PartB, M7.2, Vertical Strike-Slip with Surface Rupture
*[(top)](#table-of-contents)*

| Site | 20.0 km | 50.0 km | 100.0 km |
|-----|-----|-----|-----|
| **LAF** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_LAF.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_LAF.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_LAF.png) |
| **OSI** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_OSI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_OSI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_OSI.png) |
| **PDE** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_PDE.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_PDE.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_PDE.png) |
| **SBSM** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_SBSM.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_SBSM.png) |
| **SMCA** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_SMCA.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_SMCA.png) |
| **STNI** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_STNI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_STNI.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_STNI.png) |
| **USC** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_USC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_USC.png) |
| **WNGC** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_WNGC.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_WNGC.png) |
| **WSS** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_WSS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_WSS.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_WSS.png) |
| **s022** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_s022.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_s022.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_s022.png) |
| **10sites_Vs30_500** | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_20km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_50km_10sites_Vs30_500.png) | ![PartB Plot](resources/bbp_partB_m7p2_vert_ss_surface_100km_10sites_Vs30_500.png) |

## CSV Files
*[(top)](#table-of-contents)*

| Magnitude | Distance | Site | CSV File |
|-----|-----|-----|-----|
| M7.2 | 20.0 km | LAF | [sa_LAF_m7.2_20.0km.csv.gz](resources/sa_LAF_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | OSI | [sa_OSI_m7.2_20.0km.csv.gz](resources/sa_OSI_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | PDE | [sa_PDE_m7.2_20.0km.csv.gz](resources/sa_PDE_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | SBSM | [sa_SBSM_m7.2_20.0km.csv.gz](resources/sa_SBSM_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | SMCA | [sa_SMCA_m7.2_20.0km.csv.gz](resources/sa_SMCA_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | STNI | [sa_STNI_m7.2_20.0km.csv.gz](resources/sa_STNI_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | USC | [sa_USC_m7.2_20.0km.csv.gz](resources/sa_USC_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | WNGC | [sa_WNGC_m7.2_20.0km.csv.gz](resources/sa_WNGC_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | WSS | [sa_WSS_m7.2_20.0km.csv.gz](resources/sa_WSS_m7.2_20.0km.csv.gz) |
| M7.2 | 20.0 km | s022 | [sa_s022_m7.2_20.0km.csv.gz](resources/sa_s022_m7.2_20.0km.csv.gz) |
| M7.2 | 50.0 km | LAF | [sa_LAF_m7.2_50.0km.csv.gz](resources/sa_LAF_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | OSI | [sa_OSI_m7.2_50.0km.csv.gz](resources/sa_OSI_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | PDE | [sa_PDE_m7.2_50.0km.csv.gz](resources/sa_PDE_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | SBSM | [sa_SBSM_m7.2_50.0km.csv.gz](resources/sa_SBSM_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | SMCA | [sa_SMCA_m7.2_50.0km.csv.gz](resources/sa_SMCA_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | STNI | [sa_STNI_m7.2_50.0km.csv.gz](resources/sa_STNI_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | USC | [sa_USC_m7.2_50.0km.csv.gz](resources/sa_USC_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | WNGC | [sa_WNGC_m7.2_50.0km.csv.gz](resources/sa_WNGC_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | WSS | [sa_WSS_m7.2_50.0km.csv.gz](resources/sa_WSS_m7.2_50.0km.csv.gz) |
| M7.2 | 50.0 km | s022 | [sa_s022_m7.2_50.0km.csv.gz](resources/sa_s022_m7.2_50.0km.csv.gz) |
| M7.2 | 100.0 km | LAF | [sa_LAF_m7.2_100.0km.csv.gz](resources/sa_LAF_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | OSI | [sa_OSI_m7.2_100.0km.csv.gz](resources/sa_OSI_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | PDE | [sa_PDE_m7.2_100.0km.csv.gz](resources/sa_PDE_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | SBSM | [sa_SBSM_m7.2_100.0km.csv.gz](resources/sa_SBSM_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | SMCA | [sa_SMCA_m7.2_100.0km.csv.gz](resources/sa_SMCA_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | STNI | [sa_STNI_m7.2_100.0km.csv.gz](resources/sa_STNI_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | USC | [sa_USC_m7.2_100.0km.csv.gz](resources/sa_USC_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | WNGC | [sa_WNGC_m7.2_100.0km.csv.gz](resources/sa_WNGC_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | WSS | [sa_WSS_m7.2_100.0km.csv.gz](resources/sa_WSS_m7.2_100.0km.csv.gz) |
| M7.2 | 100.0 km | s022 | [sa_s022_m7.2_100.0km.csv.gz](resources/sa_s022_m7.2_100.0km.csv.gz) |

