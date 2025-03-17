# WISE-Light-Curves

                                                                 |
| Column Name           | d_type   | unit   | Description  |
|----------------------|----------|--------|--------------|
| gaia_id             | object   | -      | Gaia identifier. |
| simbad_name         | object   | -      | Simbad object name. |
| simbad_otype        | object   | -      | Simbad object type. |
| cw2020_source_id    | object   | -      | Source ID from CW2020 catalog. |
| designation         | object   | -      | WISE designation. |
| ra                 | float64  | deg    | Mean RA coordinates calculated from filtered data. |
| ra_err             | float64  | arcsec | Mean RA uncertainty. |
| dec                | float64  | deg    | Mean Dec coordinates calculated from filtered data. |
| dec_err            | float64  | arcsec | Mean Dec uncertainty. |
| w1_mean            | float64  | mag    | Mean W1 magnitude from filtered data. |
| w1_mean_err        | float64  | mag    | Mean W1 magnitude uncertainty. |
| w1_median          | float64  | mag    | Median W1 magnitude from filtered data. |
| w1_median_err      | float64  | mag    | Median W1 magnitude uncertainty. |
| w1_min             | float64  | mag    | Minimum W1 magnitude. |
| w1_min_err         | float64  | mag    | Uncertainty for w1_min. |
| w1_max             | float64  | mag    | Maximum W1 magnitude. |
| w1_max_err         | float64  | mag    | Uncertainty for w1_max. |
| w1_snr             | float64  | number | Mean signal-to-noise ratio for W1. |
| w1_snr_min         | float64  | number | Minimum signal-to-noise ratio for W1. |
| w1_snr_max         | float64  | number | Maximum signal-to-noise ratio for W1. |
| w1_num_pts         | int64    | number | Number of W1 data points after filtering. |
| w1_epochs          | int64    | number | Number of epochs used in W1. |
| w1_amplitude       | float64  | mag    | Total variability in W1 (w1_max - w1_min). |
| w1_var_ratio       | float64  | number | Total variability devided by variability of epoch with highest amplitude. |
| w1_mean_median     | float64  | mag    | Difference between w1_mean and w1_median. |
| w1_M_value         | float64  | mag    | M-test value for W1 variability (Kinemuchi et al. 2006). |
| w1_fap             | float64  | number | Lomb-Scargle False Alarm Probability. (not recommended to use) |
| w1_sde             | float64  | number | Signal Detection Efficiency (Alcock et al. 2000, Kovacs et al. 2002). |
| w1_power           | float64  | number | Highest relative power detected in W1. |
| w1_mean_power      | float64  | number | Mean power of detected W1 signals. |
| w1_median_power    | float64  | number | Median power of detected W1 signals. |
| w1_period          | float64  | days   | Period corresponding to the highest detected W1 signal. |
| w1_baseline        | float64  | mag    | Baseline magnitude where most W1 detections occur. |
| w1_sigp            | float64  | mag    | w1sigp for mean magnitude. |
| w1_in_sigp         | float64  | number | Percentage of data within the sigp range. |
| w1_brighter_sigp   | float64  | number | Percentage of data points brighter than the sigp range. |
| w1_fainter_sigp    | float64  | number | Percentage of data points fainter than the sigp range. |
| w2_mean            | float64  | mag    | Mean W2 magnitude from filtered data. |
| w2_mean_err        | float64  | mag    | Mean W2 magnitude uncertainty. |
| w2_median          | float64  | mag    | Median W2 magnitude from filtered data. |
| w2_median_err      | float64  | mag    | Median W2 magnitude uncertainty. |
| w2_min             | float64  | mag    | Minimum W2 magnitude. |
| w2_min_err         | float64  | mag    | Uncertainty for w2_min. |
| w2_max             | float64  | mag    | Maximum W2 magnitude. |
| w2_max_err         | float64  | mag    | Uncertainty for w2_max. |
| w2_snr             | float64  | number | Mean signal-to-noise ratio for W2. |
| w2_snr_min         | float64  | number | Minimum signal-to-noise ratio for W2. |
| w2_snr_max         | float64  | number | Maximum signal-to-noise ratio for W2. |
| w2_num_pts         | int64    | number | Number of W2 data points after filtering. |
| w2_epochs          | int64    | number | Number of epochs used in W2. |
| w2_amplitude       | float64  | mag    | Total variability in W2 (w2_max - w2_min). |
| w2_var_ratio       | float64  | number | Total variability devided by variability of epoch with highest amplitude. |
| w2_mean_median     | float64  | mag    | Difference between w2_mean and w2_median. |
| w2_M_value         | float64  | mag    | M-test value for W2 variability (Kinemuchi et al. 2006). |
| w2_fap             | float64  | number | Lomb-Scargle False Alarm Probability. |
| w2_sde             | float64  | number | Signal Detection Efficiency (Alcock et al. 2000, Kovacs et al. 2002).  |
| w2_power           | float64  | number | Highest relative power detected in W2. |
| w2_mean_power      | float64  | number | Mean power of detected W2 signals. |
| w2_median_power    | float64  | number | Median power of detected W2 signals. |
| w2_period          | float64  | days   | Period corresponding to the highest detected W2 signal. |
| w2_baseline        | float64  | mag    | Baseline magnitude where most W2 detections occur. |
| w2_sigp            | float64  | mag    | w2sigp for mean magnitude. |
| w2_in_sigp         | float64  | number | Percentage of data within the sigp range. |
| w2_brighter_sigp   | float64  | number | Percentage of data points brighter than the sigp range. |
| w2_fainter_sigp    | float64  | number | Percentage of data points fainter than the sigp range. |
| delta_time         | float64  | days   | Time between first and last WISE observations. |
| cadence           | float64  | days   | Median time between WISE observations. |
| epochs            | int64    | number | Number of total epochs with detections in WISE and NEOWISE missions. |
| mean_offset       | float64  | arcsec    | Mean positional offset between GAIA source and WISE detections.|
| median_offset     | float64  | arcsec    | Median positional offset between GAIA source and WISE detections.|
| qual_flag         | object   | -      | Filtering flags for W1 and W2. A= Data filtered succesfully- Quality of data can be considered as good. B= Default filters returned less than 50 data points and filtering criteria was lowered to obtain more data. Quality of data should be considered unreliable. S= Filtering was skipped by user. |
| GAIA_pmra         | float64  | mas/yr | Gaia proper motion in RA. |
| GAIA_pmra_err     | float64  | mas/yr | Gaia proper motion uncertainty in RA. |
| GAIA_pmdec        | float64  | mas/yr | Gaia proper motion in Dec. |
| GAIA_pmdec_err    | float64  | mas/yr | Gaia proper motion uncertainty in Dec. |
| WISE_pmra         | float64  | mas/yr | WISE proper motion in RA from linear fit. Please refer CATWISE2020(Marocco et al. 2021) for more accurate PM|
| WISE_pmdec        | float64  | mas/yr | WISE proper motion in Dec from linear fit. Please refer CATWISE2020(Marocco et al. 2021) for more accurate PM|
| theta_pm          | float64  | deg    | Proper motion direction angle between Gaia and WISE. |
| wiseview          | object   | -      | Link to WISEView (Caselden et al. 2018). |

Kinemuchi, K., Smith, H. A., Woźniak, P. R., McKay, T. A., & ROTSE Collaboration. (2006). Analysis of RR Lyrae stars in the Northern Sky Variability Survey. The Astronomical Journal, 132(3), 1202–1220. https://doi.org/10.1086/506198

Alcock, C., Allsman, R. A., Alves, D. R., et al. (2001). Erratum: The MACHO Project: Microlensing optical depth toward the Galactic bulge from difference image analysis. The Astrophysical Journal, 557(2), 1035. https://doi.org/10.1086/324099

Kovács, G., Zucker, S., & Mazeh, T. (2002). A box-fitting algorithm in the search for periodic transits. Astronomy & Astrophysics, 391(3), 369–377. https://doi.org/10.1051/0004-6361:20020621

Marocco, F., Eisenhardt, P. R. M., Fowler, J. W., et al. (2020). CatWISE2020 Catalog. NASA IPAC DataSet, IRSA551. https://doi.org/10.26131/IRSA551

Caselden et al. (2018), WiseView: Visualizing motion and variability of faint WISE sources, ASCL, ascl:1806.004. https://ui.adsabs.harvard.edu/abs/2018ascl.soft06004C/abstract



