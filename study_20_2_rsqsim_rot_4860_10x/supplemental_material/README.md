# 3s RotD50 Rotation Ground Motion CSV Files

CyberShake 3-second RotD50 ground motions for each rupture rotation are supplied for each site and scenario. Files are named `<site-name>_<scenario-name>_rd50s.csv`. Each row corresponds to a different RSQSim rupture rotation, and the columns are:

| Column | Description |
| --- | --- |
| Event ID | Unique RSQSim event ID number |
| DistanceRup (km) | 3D site-source distance |
| Source Rotation Azimuth (degrees) | Strike direction of the rupture following the Aki & Richards (1980) convention |
| Site-To-Source Path Azimuth (degrees) | Direction azimuth from the site to the scalar moment centroid of the rotated RSQSim rupture |
| ln(3.0s RotD50) | Natural-log of the RSQSim-CyberShake 3s RotD50 ground motion |
