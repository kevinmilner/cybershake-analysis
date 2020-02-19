# RSQSim 4860 10x/ASK2014 GMPE Comparisons

**GMPE: Abrahamson, Silva & Kamai (2014)**

**Vs30 Source: Simulation Value**

**Study Details**

| **Name** | RSQSim 4860 10x |
|-----|-----|
| **Date** | Feb 2020 |
| **Region** | Los Angeles Box |
| **Description** | RSQSim prototype with catalog 4860 (10x, 270kyr) |
| **Velocity Model** | CVM-S4.26, 4.26 |

Ruptures are binned by their moment magnitude (**Mw**) and the Joyner-Boore distance (**rJB**), the shortest horizontal distance from a site to the surface projection of the rupture surface

## Table Of Contents
* [Site Scatters/z-Score Histograms](#site-scattersz-score-histograms)
  * [Bundled z-scores](#bundled-z-scores)
    * [Vs30=500 z-scores](#vs30500-z-scores)
    * [LA Vs30=500 Initial Set z-scores](#la-vs30500-initial-set-z-scores)
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
  * [Site OSI](#site-osi)
    * [OSI, 6 < Mw < 6.5](#osi-6--mw--65)
    * [OSI, 6.5 < Mw < 7](#osi-65--mw--7)
    * [OSI, 7 < Mw < 7.5](#osi-7--mw--75)
    * [OSI, 7.5 < Mw < 8](#osi-75--mw--8)
    * [OSI, 8 < Mw < 9](#osi-8--mw--9)
    * [OSI, All Ruptures, Z-Score Histograms](#osi-all-ruptures-z-score-histograms)
  * [Site SMCA](#site-smca)
    * [SMCA, 6 < Mw < 6.5](#smca-6--mw--65)
    * [SMCA, 6.5 < Mw < 7](#smca-65--mw--7)
    * [SMCA, 7 < Mw < 7.5](#smca-7--mw--75)
    * [SMCA, 7.5 < Mw < 8](#smca-75--mw--8)
    * [SMCA, 8 < Mw < 9](#smca-8--mw--9)
    * [SMCA, All Ruptures, Z-Score Histograms](#smca-all-ruptures-z-score-histograms)
  * [Site SBSM](#site-sbsm)
    * [SBSM, 6 < Mw < 6.5](#sbsm-6--mw--65)
    * [SBSM, 6.5 < Mw < 7](#sbsm-65--mw--7)
    * [SBSM, 7 < Mw < 7.5](#sbsm-7--mw--75)
    * [SBSM, 7.5 < Mw < 8](#sbsm-75--mw--8)
    * [SBSM, 8 < Mw < 9](#sbsm-8--mw--9)
    * [SBSM, All Ruptures, Z-Score Histograms](#sbsm-all-ruptures-z-score-histograms)
  * [Site WSS](#site-wss)
    * [WSS, 6 < Mw < 6.5](#wss-6--mw--65)
    * [WSS, 6.5 < Mw < 7](#wss-65--mw--7)
    * [WSS, 7 < Mw < 7.5](#wss-7--mw--75)
    * [WSS, 7.5 < Mw < 8](#wss-75--mw--8)
    * [WSS, 8 < Mw < 9](#wss-8--mw--9)
    * [WSS, All Ruptures, Z-Score Histograms](#wss-all-ruptures-z-score-histograms)
  * [Site WNGC](#site-wngc)
    * [WNGC, 6 < Mw < 6.5](#wngc-6--mw--65)
    * [WNGC, 6.5 < Mw < 7](#wngc-65--mw--7)
    * [WNGC, 7 < Mw < 7.5](#wngc-7--mw--75)
    * [WNGC, 7.5 < Mw < 8](#wngc-75--mw--8)
    * [WNGC, 8 < Mw < 9](#wngc-8--mw--9)
    * [WNGC, All Ruptures, Z-Score Histograms](#wngc-all-ruptures-z-score-histograms)
  * [Site STNI](#site-stni)
    * [STNI, 6 < Mw < 6.5](#stni-6--mw--65)
    * [STNI, 6.5 < Mw < 7](#stni-65--mw--7)
    * [STNI, 7 < Mw < 7.5](#stni-7--mw--75)
    * [STNI, 7.5 < Mw < 8](#stni-75--mw--8)
    * [STNI, 8 < Mw < 9](#stni-8--mw--9)
    * [STNI, All Ruptures, Z-Score Histograms](#stni-all-ruptures-z-score-histograms)
  * [Site PDE](#site-pde)
    * [PDE, 6 < Mw < 6.5](#pde-6--mw--65)
    * [PDE, 6.5 < Mw < 7](#pde-65--mw--7)
    * [PDE, 7 < Mw < 7.5](#pde-7--mw--75)
    * [PDE, 7.5 < Mw < 8](#pde-75--mw--8)
    * [PDE, 8 < Mw < 9](#pde-8--mw--9)
    * [PDE, All Ruptures, Z-Score Histograms](#pde-all-ruptures-z-score-histograms)
  * [Site LAF](#site-laf)
    * [LAF, 6 < Mw < 6.5](#laf-6--mw--65)
    * [LAF, 6.5 < Mw < 7](#laf-65--mw--7)
    * [LAF, 7 < Mw < 7.5](#laf-7--mw--75)
    * [LAF, 7.5 < Mw < 8](#laf-75--mw--8)
    * [LAF, 8 < Mw < 9](#laf-8--mw--9)
    * [LAF, All Ruptures, Z-Score Histograms](#laf-all-ruptures-z-score-histograms)
  * [Site s022](#site-s022)
    * [s022, 6 < Mw < 6.5](#s022-6--mw--65)
    * [s022, 6.5 < Mw < 7](#s022-65--mw--7)
    * [s022, 7 < Mw < 7.5](#s022-7--mw--75)
    * [s022, 7.5 < Mw < 8](#s022-75--mw--8)
    * [s022, 8 < Mw < 9](#s022-8--mw--9)
    * [s022, All Ruptures, Z-Score Histograms](#s022-all-ruptures-z-score-histograms)
  * [Site PAS](#site-pas)
    * [PAS, 6 < Mw < 6.5](#pas-6--mw--65)
    * [PAS, 6.5 < Mw < 7](#pas-65--mw--7)
    * [PAS, 7 < Mw < 7.5](#pas-7--mw--75)
    * [PAS, 7.5 < Mw < 8](#pas-75--mw--8)
    * [PAS, 8 < Mw < 9](#pas-8--mw--9)
    * [PAS, All Ruptures, Z-Score Histograms](#pas-all-ruptures-z-score-histograms)
* [Hazard Curves](#hazard-curves)
* [GMPE Residuals](#gmpe-residuals)
  * [Period-Dependent Residual Components](#period-dependent-residual-components)
  * [Detrended Period-Dependent Residual Components](#detrended-period-dependent-residual-components)
  * [GMPE Magnitude Residuals](#gmpe-magnitude-residuals)
  * [GMPE rJB Residuals](#gmpe-rjb-residuals)
  * [GMPE rRup Residuals](#gmpe-rrup-residuals)
  * [GMPE Vs30 Residuals](#gmpe-vs30-residuals)
  * [GMPE Z10 Residuals](#gmpe-z10-residuals)
  * [GMPE Z25 Residuals](#gmpe-z25-residuals)
  * [GMPE Occurrence Time Residuals](#gmpe-occurrence-time-residuals)
## Site Scatters/z-Score Histograms
*[(top)](#table-of-contents)*

### Bundled z-scores
*[(top)](#table-of-contents)*

#### Vs30=500 z-scores
*[(top)](#table-of-contents)*


Site bundle with 10 sites.

z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/site_bundle_Vs30_500_std_norm.png) | ![Standard Normal Plot](resources/site_bundle_Vs30_500_std_norm_source_contrib.png) |
#### LA Vs30=500 Initial Set z-scores
*[(top)](#table-of-contents)*


Site bundle with 10 sites.

z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/site_bundle_LA_Vs30_500_Initial_Set_std_norm.png) | ![Standard Normal Plot](resources/site_bundle_LA_Vs30_500_Initial_Set_std_norm_source_contrib.png) |
### All Sites Aggregated
*[(top)](#table-of-contents)*

**11 sites**

| Name | Location | # Ruptures | Vs30 (m/s) | Z1.0 (km) | Z2.5 (km) |
|-----|-----|-----|-----|-----|-----|
| USC | *34.0192, -118.286* | 31699 (31699 sims) | 500 | 0.58 | 4.1 |
| OSI | *34.6145, -118.7235* | 29623 (29623 sims) | 500 | 0.31 | 0.31 |
| SMCA | *34.00909, -118.48939* | 31339 (31339 sims) | 500 | 0.59 | 2.45 |
| SBSM | *34.064987, -117.29201* | 37185 (37185 sims) | 500 | 0.33 | 1.82 |
| WSS | *34.1717, -118.64971* | 28587 (28587 sims) | 500 | 0.09 | 2.42 |
| WNGC | *34.041824, -118.0653* | 31534 (31534 sims) | 500 | 0.5 | 3.49 |
| STNI | *33.93088, -118.17881* | 30772 (30772 sims) | 500 | 0.88 | 5.57 |
| PDE | *34.44199, -118.58215* | 29725 (29725 sims) | 500 | 0.15 | 1.84 |
| LAF | *33.86889, -118.33143* | 30675 (30675 sims) | 500 | 0.71 | 3.42 |
| s022 | *34.24505, -119.18086* | 25027 (25027 sims) | 500 | 0.51 | 4.24 |
| PAS | *34.148426, -118.17119* | 32705 (32705 sims) | 838.8 | 0.01 | 0.68 |

42104 ruptures within 200 km of *any* site
#### All Sites, 6 < Mw < 6.5
0 Ruptures
##### All Sites, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### All Sites, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### All Sites, 6.5 < Mw < 7
19778 Ruptures
##### All Sites, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### All Sites, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 7 < Mw < 7.5
17171 Ruptures
##### All Sites, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### All Sites, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 7.5 < Mw < 8
5153 Ruptures
##### All Sites, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### All Sites, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, 8 < Mw < 9
2 Ruptures
##### All Sites, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/All_Sites_mag_8_9_dist_160_200_10s_ASK2014_scatter.png) |
##### All Sites, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | ![Standard Normal Plot](resources/All_Sites_mag_8_9_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_mag_8_9_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/All_Sites_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | ![Standard Normal Plot](resources/All_Sites_mag_8_9_dist_160_200_ASK2014_std_norm.png) |
#### All Sites, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/All_Sites_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/All_Sites_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site USC
*[(top)](#table-of-contents)*

*Location: 34.0192, -118.286*
31699 ruptures within 200.0 km
#### USC, 6 < Mw < 6.5
0 Ruptures
##### USC, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### USC, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### USC, 6.5 < Mw < 7
19778 Ruptures
##### USC, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### USC, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### USC, 7 < Mw < 7.5
17171 Ruptures
##### USC, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### USC, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### USC, 7.5 < Mw < 8
5153 Ruptures
##### USC, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### USC, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### USC, 8 < Mw < 9
2 Ruptures
##### USC, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/USC_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/USC_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### USC, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/USC_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### USC, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/USC_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/USC_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site OSI
*[(top)](#table-of-contents)*

*Location: 34.6145, -118.7235*
29623 ruptures within 200.0 km
#### OSI, 6 < Mw < 6.5
0 Ruptures
##### OSI, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### OSI, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### OSI, 6.5 < Mw < 7
19778 Ruptures
##### OSI, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### OSI, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### OSI, 7 < Mw < 7.5
17171 Ruptures
##### OSI, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### OSI, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### OSI, 7.5 < Mw < 8
5153 Ruptures
##### OSI, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### OSI, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | ![Standard Normal Plot](resources/OSI_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/OSI_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### OSI, 8 < Mw < 9
2 Ruptures
##### OSI, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/OSI_mag_8_9_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_8_9_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_8_9_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/OSI_mag_8_9_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_8_9_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/OSI_mag_8_9_dist_160_200_10s_ASK2014_scatter.png) |
##### OSI, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | ![Standard Normal Plot](resources/OSI_mag_8_9_dist_10_20_ASK2014_std_norm.png) | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | ![Standard Normal Plot](resources/OSI_mag_8_9_dist_160_200_ASK2014_std_norm.png) |
#### OSI, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/OSI_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/OSI_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site SMCA
*[(top)](#table-of-contents)*

*Location: 34.00909, -118.48939*
31339 ruptures within 200.0 km
#### SMCA, 6 < Mw < 6.5
0 Ruptures
##### SMCA, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### SMCA, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### SMCA, 6.5 < Mw < 7
19778 Ruptures
##### SMCA, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### SMCA, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### SMCA, 7 < Mw < 7.5
17171 Ruptures
##### SMCA, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### SMCA, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### SMCA, 7.5 < Mw < 8
5153 Ruptures
##### SMCA, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### SMCA, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### SMCA, 8 < Mw < 9
2 Ruptures
##### SMCA, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SMCA_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SMCA_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### SMCA, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SMCA_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### SMCA, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/SMCA_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SMCA_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site SBSM
*[(top)](#table-of-contents)*

*Location: 34.064987, -117.29201*
37185 ruptures within 200.0 km
#### SBSM, 6 < Mw < 6.5
0 Ruptures
##### SBSM, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### SBSM, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### SBSM, 6.5 < Mw < 7
19778 Ruptures
##### SBSM, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### SBSM, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### SBSM, 7 < Mw < 7.5
17171 Ruptures
##### SBSM, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### SBSM, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### SBSM, 7.5 < Mw < 8
5153 Ruptures
##### SBSM, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### SBSM, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### SBSM, 8 < Mw < 9
2 Ruptures
##### SBSM, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/SBSM_mag_8_9_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_8_9_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/SBSM_mag_8_9_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### SBSM, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | ![Standard Normal Plot](resources/SBSM_mag_8_9_dist_10_20_ASK2014_std_norm.png) | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### SBSM, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/SBSM_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/SBSM_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site WSS
*[(top)](#table-of-contents)*

*Location: 34.1717, -118.64971*
28587 ruptures within 200.0 km
#### WSS, 6 < Mw < 6.5
0 Ruptures
##### WSS, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### WSS, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### WSS, 6.5 < Mw < 7
19778 Ruptures
##### WSS, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### WSS, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### WSS, 7 < Mw < 7.5
17171 Ruptures
##### WSS, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### WSS, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### WSS, 7.5 < Mw < 8
5153 Ruptures
##### WSS, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### WSS, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | ![Standard Normal Plot](resources/WSS_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WSS_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### WSS, 8 < Mw < 9
2 Ruptures
##### WSS, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WSS_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WSS_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### WSS, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WSS_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### WSS, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/WSS_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WSS_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site WNGC
*[(top)](#table-of-contents)*

*Location: 34.041824, -118.0653*
31534 ruptures within 200.0 km
#### WNGC, 6 < Mw < 6.5
0 Ruptures
##### WNGC, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### WNGC, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### WNGC, 6.5 < Mw < 7
19778 Ruptures
##### WNGC, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### WNGC, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 7 < Mw < 7.5
17171 Ruptures
##### WNGC, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### WNGC, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 7.5 < Mw < 8
5153 Ruptures
##### WNGC, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### WNGC, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### WNGC, 8 < Mw < 9
2 Ruptures
##### WNGC, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/WNGC_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/WNGC_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### WNGC, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/WNGC_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### WNGC, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/WNGC_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/WNGC_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site STNI
*[(top)](#table-of-contents)*

*Location: 33.93088, -118.17881*
30772 ruptures within 200.0 km
#### STNI, 6 < Mw < 6.5
0 Ruptures
##### STNI, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### STNI, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### STNI, 6.5 < Mw < 7
19778 Ruptures
##### STNI, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### STNI, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### STNI, 7 < Mw < 7.5
17171 Ruptures
##### STNI, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### STNI, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### STNI, 7.5 < Mw < 8
5153 Ruptures
##### STNI, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### STNI, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### STNI, 8 < Mw < 9
2 Ruptures
##### STNI, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/STNI_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/STNI_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### STNI, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/STNI_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### STNI, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/STNI_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/STNI_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site PDE
*[(top)](#table-of-contents)*

*Location: 34.44199, -118.58215*
29725 ruptures within 200.0 km
#### PDE, 6 < Mw < 6.5
0 Ruptures
##### PDE, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### PDE, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### PDE, 6.5 < Mw < 7
19778 Ruptures
##### PDE, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### PDE, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### PDE, 7 < Mw < 7.5
17171 Ruptures
##### PDE, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### PDE, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### PDE, 7.5 < Mw < 8
5153 Ruptures
##### PDE, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### PDE, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### PDE, 8 < Mw < 9
2 Ruptures
##### PDE, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PDE_mag_8_9_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_8_9_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PDE_mag_8_9_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | N/A | N/A | N/A |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### PDE, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | ![Standard Normal Plot](resources/PDE_mag_8_9_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### PDE, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/PDE_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PDE_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site LAF
*[(top)](#table-of-contents)*

*Location: 33.86889, -118.33143*
30675 ruptures within 200.0 km
#### LAF, 6 < Mw < 6.5
0 Ruptures
##### LAF, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### LAF, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### LAF, 6.5 < Mw < 7
19778 Ruptures
##### LAF, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### LAF, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### LAF, 7 < Mw < 7.5
17171 Ruptures
##### LAF, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### LAF, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### LAF, 7.5 < Mw < 8
5153 Ruptures
##### LAF, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### LAF, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### LAF, 8 < Mw < 9
2 Ruptures
##### LAF, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/LAF_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/LAF_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### LAF, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/LAF_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### LAF, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/LAF_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/LAF_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site s022
*[(top)](#table-of-contents)*

*Location: 34.24505, -119.18086*
25027 ruptures within 200.0 km
#### s022, 6 < Mw < 6.5
0 Ruptures
##### s022, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### s022, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### s022, 6.5 < Mw < 7
19778 Ruptures
##### s022, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/s022_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### s022, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### s022, 7 < Mw < 7.5
17171 Ruptures
##### s022, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/s022_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### s022, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### s022, 7.5 < Mw < 8
5153 Ruptures
##### s022, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/s022_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### s022, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### s022, 8 < Mw < 9
2 Ruptures
##### s022, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/s022_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/s022_mag_8_9_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_8_9_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/s022_mag_8_9_dist_160_200_10s_ASK2014_scatter.png) |
##### s022, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/s022_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | ![Standard Normal Plot](resources/s022_mag_8_9_dist_160_200_ASK2014_std_norm.png) |
#### s022, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/s022_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/s022_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
### Site PAS
*[(top)](#table-of-contents)*

*Location: 34.148426, -118.17119*
32705 ruptures within 200.0 km
#### PAS, 6 < Mw < 6.5
0 Ruptures
##### PAS, 6 < Mw < 6.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
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
##### PAS, 6 < Mw < 6.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| N/A | N/A | N/A |
#### PAS, 6.5 < Mw < 7
19778 Ruptures
##### PAS, 6.5 < Mw < 7, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_6.5_7_dist_160_200_10s_ASK2014_scatter.png) |
##### PAS, 6.5 < Mw < 7, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_6.5_7_dist_160_200_ASK2014_std_norm.png) |
#### PAS, 7 < Mw < 7.5
17171 Ruptures
##### PAS, 7 < Mw < 7.5, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7_7.5_dist_160_200_10s_ASK2014_scatter.png) |
##### PAS, 7 < Mw < 7.5, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7_7.5_dist_160_200_ASK2014_std_norm.png) |
#### PAS, 7.5 < Mw < 8
5153 Ruptures
##### PAS, 7.5 < Mw < 8, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_0_10_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_0_10_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_0_10_10s_ASK2014_scatter.png) |
| **10 km < rJB < 20 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_10_20_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_10_20_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_10_20_10s_ASK2014_scatter.png) |
| **20 km < rJB < 40 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_20_40_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_20_40_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_20_40_10s_ASK2014_scatter.png) |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_80_160_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_80_160_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_80_160_10s_ASK2014_scatter.png) |
| **160 km < rJB < 200 km** | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_160_200_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_160_200_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_7.5_8_dist_160_200_10s_ASK2014_scatter.png) |
##### PAS, 7.5 < Mw < 8, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_0_10_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_10_20_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_20_40_ASK2014_std_norm.png) |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_40_80_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_80_160_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_mag_7.5_8_dist_160_200_ASK2014_std_norm.png) |
#### PAS, 8 < Mw < 9
2 Ruptures
##### PAS, 8 < Mw < 9, Scatter Plots
*[(top)](#table-of-contents)*

**Legend**
* Red +: GMPE Mean/RSQSim 4860 10x single rupture comparison
* Yellow Region: Factor of 2 above & below
* Green Line: Linear Regression

| **Distance Bin** | **3 s** | **5 s** | **10 s** |
|-----|-----|-----|-----|
| **0 km < rJB < 10 km** | N/A | N/A | N/A |
| **10 km < rJB < 20 km** | N/A | N/A | N/A |
| **20 km < rJB < 40 km** | N/A | N/A | N/A |
| **40 km < rJB < 80 km** | ![Scatter Plot](resources/PAS_mag_8_9_dist_40_80_3s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_8_9_dist_40_80_5s_ASK2014_scatter.png) | ![Scatter Plot](resources/PAS_mag_8_9_dist_40_80_10s_ASK2014_scatter.png) |
| **80 km < rJB < 160 km** | N/A | N/A | N/A |
| **160 km < rJB < 200 km** | N/A | N/A | N/A |
##### PAS, 8 < Mw < 9, z-Score Histograms
*[(top)](#table-of-contents)*

These plots compare RSQSim 4860 10x to the full GMPE log-normal distributions. Each rupture's GMPE distribution is converted to a standard log-normal distribution, and the z-score is computed for each rupture:

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| **0 km < rJB < 10 km** | **10 km < rJB < 20 km** | **20 km < rJB < 40 km** |
|-----|-----|-----|
| N/A | N/A | N/A |
| **40 km < rJB < 80 km** | **80 km < rJB < 160 km** | **160 km < rJB < 200 km** |
| ![Standard Normal Plot](resources/PAS_mag_8_9_dist_40_80_ASK2014_std_norm.png) | N/A | N/A |
#### PAS, All Ruptures, Z-Score Histograms
*[(top)](#table-of-contents)*


z-score standard normal plots across all magnitudes/distances

**z-score**: (ln(*RSQSim 4860 10x*) - ln(*GMPE-mean*)) / *GMPE-sigma*

**Legend**
* Black Line: Standard Normal distribution (in natural log space)
* Gray Histogram: z-score for each rupture
* Blue Dashed Line: RSQSim 4860 10x Mean

| Total | Source Contributions |
|-----|-----|
| ![Standard Normal Plot](resources/PAS_all_mags_all_dists_ASK2014_std_norm.png) | ![Standard Normal Plot](resources/PAS_all_mags_all_dists_ASK2014_std_norm_source_contrib.png) |
## Hazard Curves
*[(top)](#table-of-contents)*

**Legend**:
* **Simulation Curves** *(truncated below lowest possible y-value)*
  * Black Solid Line: RSQSim 4860 10x
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
| **OSI** | ![Hazard Curve](resources/OSI_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/OSI_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/OSI_curves_10.0s_ASK2014.png) |
| **SMCA** | ![Hazard Curve](resources/SMCA_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/SMCA_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/SMCA_curves_10.0s_ASK2014.png) |
| **SBSM** | ![Hazard Curve](resources/SBSM_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/SBSM_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/SBSM_curves_10.0s_ASK2014.png) |
| **WSS** | ![Hazard Curve](resources/WSS_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/WSS_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/WSS_curves_10.0s_ASK2014.png) |
| **WNGC** | ![Hazard Curve](resources/WNGC_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/WNGC_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/WNGC_curves_10.0s_ASK2014.png) |
| **STNI** | ![Hazard Curve](resources/STNI_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/STNI_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/STNI_curves_10.0s_ASK2014.png) |
| **PDE** | ![Hazard Curve](resources/PDE_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/PDE_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/PDE_curves_10.0s_ASK2014.png) |
| **LAF** | ![Hazard Curve](resources/LAF_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/LAF_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/LAF_curves_10.0s_ASK2014.png) |
| **s022** | ![Hazard Curve](resources/s022_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/s022_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/s022_curves_10.0s_ASK2014.png) |
| **PAS** | ![Hazard Curve](resources/PAS_curves_3.0s_ASK2014.png) | ![Hazard Curve](resources/PAS_curves_5.0s_ASK2014.png) | ![Hazard Curve](resources/PAS_curves_10.0s_ASK2014.png) |
## GMPE Residuals
*[(top)](#table-of-contents)*

Residuals of simulation data (RSQSim 4860 10x) in log space relative to GMPE log-mean

**Legend**
* Black Thick Line: Linear Least-Squares Fit to Residuals
* Black Circles: Binned Linear Least-Squares Fit to Residuals
  * Black Thin Dashes: binned mean ± data sigma
  * Blue Thin Dotted: binned mean ± GMPE sigma

GMPE Residuals use the following values, averaged among all ruptures, for all paremeters which are not varied. All other parameters set to GMPE defaults

| Name | Average Value |
|-----|-----|
| Magnitude | 7.08 |
| rRup | 113.07 |
| rJB | 113.86 |
| Vs30 | 532.7 |
| Z10 | 422.22 |
| Z25 | 2.72 |
| Occurrence Time | 139910.49 |

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
### GMPE Vs30 Residuals
*[(top)](#table-of-contents)*


| **3 s** | **5 s** | **10 s** |
|-----|-----|-----|
| ![Scatter](resources/gmpe_residuals_VS30_3s_scatter.png) | ![Scatter](resources/gmpe_residuals_VS30_5s_scatter.png) | ![Scatter](resources/gmpe_residuals_VS30_10s_scatter.png) |
| ![2-D Hist](resources/gmpe_residuals_VS30_3s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_VS30_5s_hist2d.png) | ![2-D Hist](resources/gmpe_residuals_VS30_10s_hist2d.png) |
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
