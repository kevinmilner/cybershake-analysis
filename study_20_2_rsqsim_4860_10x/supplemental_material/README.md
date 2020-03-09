# 3s RotD50 Ground Motion CSV Files

CyberShake 3-second RotD50 ground motions are supplied for each site, along with log-median and standard deviations from the ASK2014 empirical GMM. Files are named `<site-name>_rd50s.csv`. Each row corresponds to a different RSQSim event, and the columns are:

| Column | Description |
| --- | --- |
| Event ID | Unique RSQSim event ID number |
| Magnitude | RSQSim rupture magnitude |
| DistanceRup (km) | 3D site-source distance used in GMM parameterization |
| DistanceJB (km) | Joyner-Boore horizontal surface projection site-source distance used in GMM parameterization |
| Annual Rate | Annual rate of the rupture |
| RSQSim 4860 10x ln(3.0s RotD50) | Natural-log of the RSQSim-CyberShake 3s RotD50 ground motion |
| ASK2014 ln(3.0s Median RotD50) | Natural-log median ASK2014 3s RotD50 ground motion |
| ASK2014 3.0s Standard Deviation | ASK2014 standard deviation of the natural-log 3s RotD50 ground motion |
