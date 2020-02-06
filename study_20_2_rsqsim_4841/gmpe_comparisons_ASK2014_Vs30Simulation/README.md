# RSQSim 4841/ASK2014 GMPE Comparisons

**GMPE: Abrahamson, Silva & Kamai (2014)**

**Vs30 Source: Simulation Value**

**Study Details**

| **Name** | RSQSim 4841 |
|-----|-----|
| **Date** | Feb 2020 |
| **Region** | Los Angeles Box |
| **Description** | RSQSim prototype with catalog 4841 (134kyr) |
| **Velocity Model** | CVM-S4.26, 4.26 |

Ruptures are binned by their moment magnitude (**Mw**) and the Joyner-Boore distance (**rJB**), the shortest horizontal distance from a site to the surface projection of the rupture surface

## Table Of Contents
* [Site Scatters/Z-Score Histograms](#site-scattersz-score-histograms)
  * [All Sites Aggregated](#all-sites-aggregated)
    * [All Sites, 6 < Mw < 6.5](#all-sites-6--mw--65)
    * [All Sites, 6.5 < Mw < 7](#all-sites-65--mw--7)
    * [All Sites, 7 < Mw < 7.5](#all-sites-7--mw--75)
    * [All Sites, 7.5 < Mw < 8](#all-sites-75--mw--8)
    * [All Sites, 8 < Mw < 9](#all-sites-8--mw--9)
    * [All Sites, All Ruptures, Z-Score Histograms](#all-sites-all-ruptures-z-score-histograms)
  * [Site USC](#site-usc)
    * [USC, 6 < Mw < 6.5](#usc-6--mw--65)
    * [USC, 6.5 < Mw < 7](#usc-65--mw--7)
    * [USC, 7 < Mw < 7.5](#usc-7--mw--75)
    * [USC, 7.5 < Mw < 8](#usc-75--mw--8)
    * [USC, 8 < Mw < 9](#usc-8--mw--9)
    * [USC, All Ruptures, Z-Score Histograms](#usc-all-ruptures-z-score-histograms)
  * [Site WNGC](#site-wngc)
    * [WNGC, 6 < Mw < 6.5](#wngc-6--mw--65)
    * [WNGC, 6.5 < Mw < 7](#wngc-65--mw--7)
    * [WNGC, 7 < Mw < 7.5](#wngc-7--mw--75)
    * [WNGC, 7.5 < Mw < 8](#wngc-75--mw--8)
    * [WNGC, 8 < Mw < 9](#wngc-8--mw--9)
    * [WNGC, All Ruptures, Z-Score Histograms](#wngc-all-ruptures-z-score-histograms)
* [Hazard Curves](#hazard-curves)
* [GMPE Residuals](#gmpe-residuals)
  * [Period-Dependent Residual Components](#period-dependent-residual-components)
  * [Detrended Period-Dependent Residual Components](#detrended-period-dependent-residual-components)
  * [GMPE Magnitude Residuals](#gmpe-magnitude-residuals)
  * [GMPE rJB Residuals](#gmpe-rjb-residuals)
  * [GMPE rRup Residuals](#gmpe-rrup-residuals)
  * [GMPE Z10 Residuals](#gmpe-z10-residuals)
  * [GMPE Z25 Residuals](#gmpe-z25-residuals)
  * [GMPE Occurrence Time Residuals](#gmpe-occurrence-time-residuals)
## Site Scatters/Z-Score Histograms
*[(top)](#table-of-contents)*

### All Sites Aggregated
*[(top)](#table-of-contents)*

**2 sites**

| Name | Location | # Ruptures | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|-----|
| USC | *34.0192, -118.286* | 13976 (13976 sims) | 500 | 0.58 | 4.1 |
| WNGC | *34.041824, -118.0653* | 13980 (13980 sims) | 500 | 0.5 | 3.49 |

14321 ruptures within 200 km of *any* site
#### All Sites, 6 < Mw < 6.5
0 Ruptures
##### All Sites, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### All Sites, 6 < Mw < 6.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### All Sites, 6.5 < Mw < 7
6974 Ruptures
##### All Sites, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### All Sites, 6.5 < Mw < 7, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 7 < Mw < 7.5
5087 Ruptures
##### All Sites, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### All Sites, 7 < Mw < 7.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 7.5 < Mw < 8
2260 Ruptures
##### All Sites, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### All Sites, 7.5 < Mw < 8, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 8 < Mw < 9
0 Ruptures
##### All Sites, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### All Sites, 8 < Mw < 9, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### All Sites, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site USC
*[(top)](#table-of-contents)*

*Location: 34.0192, -118.286*
13976 ruptures within 200.0 km
#### USC, 6 < Mw < 6.5
0 Ruptures
##### USC, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### USC, 6 < Mw < 6.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### USC, 6.5 < Mw < 7
6974 Ruptures
##### USC, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/USC_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### USC, 6.5 < Mw < 7, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### USC, 7 < Mw < 7.5
5087 Ruptures
##### USC, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/USC_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### USC, 7 < Mw < 7.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### USC, 7.5 < Mw < 8
2260 Ruptures
##### USC, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/USC_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### USC, 7.5 < Mw < 8, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### USC, 8 < Mw < 9
0 Ruptures
##### USC, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### USC, 8 < Mw < 9, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### USC, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/USC_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site WNGC
*[(top)](#table-of-contents)*

*Location: 34.041824, -118.0653*
13980 ruptures within 200.0 km
#### WNGC, 6 < Mw < 6.5
0 Ruptures
##### WNGC, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### WNGC, 6 < Mw < 6.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### WNGC, 6.5 < Mw < 7
6974 Ruptures
##### WNGC, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### WNGC, 6.5 < Mw < 7, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 7 < Mw < 7.5
5087 Ruptures
##### WNGC, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### WNGC, 7 < Mw < 7.5, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 7.5 < Mw < 8
2260 Ruptures
##### WNGC, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### WNGC, 7.5 < Mw < 8, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 8 < Mw < 9
0 Ruptures
##### WNGC, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4841 single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### WNGC, 8 < Mw < 9, Z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4841 to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### WNGC, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4841*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4841 Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/WNGC_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
## Hazard Curves
*[(top)](#table-of-contents)*

**Legend**:
* **Simulation Curves** *(truncated below lowest possible y-value)*
  * Black Solid Line: RSQSim 4841
* **GMPE Curves**
  * Blue Solid Line: ASK2014 full curves
  * Blue Dashed Line: ASK2014, 3-sigma truncation
  * Blue Dotted Line: ASK2014, 2-sigma truncation
  * Blue Dotted and dashed Line: ASK2014, 1-sigma truncation
  * Green Dashed Line: ASK2014, Fixed sigma=0
* Gray Dashed Lines: 1000 yr, 2500 yr, 10000 yr return periods

| Site | 3s | 5s | 10s |
|-----|-----|-----|-----|
| **USC** | ![Hazard Curve](resources/USC_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/USC_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/USC_curves_10.0s_ASK2014.png) |
| **WNGC** | ![Hazard Curve](resources/WNGC_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/WNGC_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/WNGC_curves_10.0s_ASK2014.png) |
## GMPE Residuals
*[(top)](#table-of-contents)*

Residuals of simulation data (RSQSim 4841) in log space relative to GMPE log-mean

**Legend**
* Black Thick Line: Linear Least-Squares Fit to Residuals
* Black Circles: Binned Linear Least-Squares Fit to Residuals
  * Black Thin Dashes: binned mean ± data sigma
  * Blue Thin Dotted: binned mean ± GMPE sigma

GMPE Residuals use the following values, averaged among all ruptures, for all paremeters which are not varied. All other parameters set to GMPE defaults

| Name | Average Value |
|-----|-----|
| Magnitude | 7.06 |
| rRup | 111.88 |
| rJB | 112.36 |
| Vs30 | 500 |
| Z10 | 539.99 |
| Z25 | 3.79 |
| Occurrence Time | 69389.38 |

### Period-Dependent Residual Components
*[(top)](#table-of-contents)*

**Note: These are not corrected for covariance. Currently only useful for comparing relative phi and tau, not absolute values**

![Residual Components](resources/period_residual_components.png)

### Detrended Period-Dependent Residual Components
*[(top)](#table-of-contents)*

**Note: These are not yet corrected for covariance. Currently only useful for comparing relative phi and tau, not absolute values**

Residuals shown here are first detrended according to the following magnitude & log-distance dependent average residuals

| **3s** | **5s** | **10s** |
|-----|-----|-----|
| ![Detrend XYZ](resources/detrend_residuals_3s.png) | ![Detrend XYZ](resources/detrend_residuals_5s.png) | ![Detrend XYZ](resources/detrend_residuals_10s.png) |
| ![Detrend Std Dev XYZ](resources/detrend_std_dev_3s.png) | ![Detrend Std Dev XYZ](resources/detrend_std_dev_5s.png) | ![Detrend Std Dev XYZ](resources/detrend_std_dev_10s.png) |

![Residual Components](resources/period_residual_detrend_components.png)

### GMPE Magnitude Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_MAG_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_MAG_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_MAG_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_MAG_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_MAG_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_MAG_10s_hist2d.png) |
### GMPE rJB Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_DIST_JB_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_DIST_JB_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_DIST_JB_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_DIST_JB_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_DIST_JB_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_DIST_JB_10s_hist2d.png) |
### GMPE rRup Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_DIST_RUP_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_DIST_RUP_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_DIST_RUP_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_DIST_RUP_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_DIST_RUP_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_DIST_RUP_10s_hist2d.png) |
### GMPE Z10 Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_Z10_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_Z10_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_Z10_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_Z10_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_Z10_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_Z10_10s_hist2d.png) |
### GMPE Z25 Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_Z25_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_Z25_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_Z25_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_Z25_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_Z25_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_Z25_10s_hist2d.png) |
### GMPE Occurrence Time Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_OCCUR_TIME_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_OCCUR_TIME_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_OCCUR_TIME_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_OCCUR_TIME_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_OCCUR_TIME_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_OCCUR_TIME_10s_hist2d.png) |
