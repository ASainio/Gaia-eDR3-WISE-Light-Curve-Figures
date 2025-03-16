# WISE-Light-Curves

| Column Name   | d_type   | unit   | Description                                                                                         |
|---------------|----------|--------|-----------------------------------------------------------------------------------------------------|
| name          | object   | -      | Common identifier from source file. Can be used as join key.                                       |
| designation   | object   | -      | WISE designation calculated from mean coordinates.                                                  |
| ra            | float64  | deg    | Mean ra coordinates calculated from filtered data.                                                  |
| ra_err        | float64  | arcsec | Mean ra uncertainty calculated from filtered data.                                                  |
| dec           | float64  | deg    | Mean dec coordinates calculated from filtered data.                                                  |
| dec_err       | float64  | arcsec | Mean dec uncertainty calculated from filtered data.                                                  |
| w1_mean       | float64  | mag    | Mean w1mpro calculated from filtered data.                                                          |
| w1_mean_err   | float64  | mag    | Mean w1sigmpro calculated from filtered data.                                                       |
| w1_median     | float64  | mag    | Median w1mpro calculated from filtered data.                                                        |
| w1_median_err | float64  | mag    | Median w1sigmpro calculated from filtered data.                                                     |
| w1_min        | float64  | mag    | Minimum w1mpro calculated from filtered data.                                                       |
| w1_min_err    | float64  | mag    | Uncertainty for w1_min.                                                                            |
| w1_max        | float64  | mag    | Maximum w1mpro calculated from filtered data.                                                       |
| w1_max_err    | float64  | mag    | Uncertainty for w1_max.                                                                            |
| w1_snr        | float64  | number | Mean S/N ratio for W1.                                                                              |
| w1_snr_min    | float64  | number | Minimum S/N ratio for W1_mpro.                                                                       |
| w1_snr_max    | float64  | number | Maximum S/N ratio for W1_mpro.                                                                       |
| w1_num_pts    | int64    | number | Number of datapoints used in W1 after filtering.                                                    |
| w1_amplitude  | float64  | mag    | Total variability in W1 from filtered data (w1_max-w1_min).                                          |
| w1_var_ratio      | float64  | number | Total variability devided by variability of epoch with highest amplitude |
| w1_mean_median| float64  | mag    | w1_mean - w1_median from filtered data                                          |
| w1_M_value    | float64  | mag    | M test value to test variabilty in W1 (Kinemuchi et al. 2006).                                          |
| w1_fap        | float64  | number | Lomb-Scargle False Alarm Probability (EXPERIMENTAL STAGE).                                           |
| w1_sde        | float64  | number | Signal Detection Efficiency (Alcock et al. 2000, Kovacs et al. 2002).                                |
| w1_power      | float64  | number | Highest relative power from signals detected in W1.                                                  |
| w1_period     | float64  | days   | Period matching highest detected signal from W1.                                                      |
| w1_baseline     | float64  | mag   | Magnitude where AllWISE 0-hypothesis range for mean fits largest amount of w1 detections.                 |
| w1_sigp    | float64  | mag   | w1sigp for mean mag from https://wise2.ipac.caltech.edu/docs/release/allsky/expsup/data/w1sigp1_int.tbl      |
| w1_in_sigp      | float64  | number | % of data with in sigp range after filtering                                               |
| w1_brighter_sigp      | float64  | number | % of data points brighter than sigp range.                                                  |
| w1_fainter_sigp      | float64  | number | % of datapoints fainter than sigp range.                                                  |
| w2_mean       | float64  | mag    | Mean w2mpro calculated from filtered data.                                                          |
| w2_mean_err   | float64  | mag    | Mean w2sigmpro calculated from filtered data.                                                        |
| w2_median     | float64  | mag    | Median w2mpro calculated from filtered data.                                                         |
| w2_median_err | float64  | mag    | Median w2sigmpro calculated from filtered data.                                                       |
| w2_min        | float64  | mag    | Minimum w2mpro calculated from filtered data.                                                        |
| w2_min_err    | float64  | mag    | Uncertainty for w2_min.                                                                             |
| w2_max        | float64  | mag    | Maximum w2mpro calculated from filtered data.                                                        |
| w2_max_err    | float64  | mag    | Uncertainty for w2_max.                                                                             |
| w2_snr        | float64  | number | Mean S/N ratio for W2.                                                                              |
| w2_snr_min    | float64  | number | Minimum S/N ratio for W2_mpro.                                                                       |
| w2_snr_max    | float64  | number | Maximum S/N ratio for W2_mpro.                                                                       |
| w2_num_pts    | int64    | number | Amount of datapoints after filtering.                                                                |
| w2_amplitude  | float64  | mag    | Total variability in W2 from filtered data (w2_max-w2_min).                                          |
| w2_var_ratio      | float64  | number | Total variability devided by variability of epoch with highest amplitude                                                  |
| w2_mean_median| float64  | mag    | w2_mean - w2_median from filtered data                                          |
| w2_M_value    | float64  | mag    | M test value to test variabilty in W2 (Kinemuchi et al. 2006).                                          |
| w2_fap        | float64  | number | Lomb-Scargle False Alarm Probability (EXPERIMENTAL STAGE).                                           |
| w2_sde        | float64  | number | Signal Detection Efficiency (Alcock et al. 2000, Kovacs et al. 2002).                                |
| w2_power      | float64  | number | Highest relative power from signals detected in W2.                                                   |
| w2_period     | float64  | days   | Period matching highest detected signal from W2.                                                       |
| w2_baseline     | float64  | days   | Magnitude where AllWISE 0-hypothesis range for mean fits largest amount of w2 detections.                 |
| w2_sigp    | float64  | mag   | w2sigp for mean mag from https://wise2.ipac.caltech.edu/docs/release/allsky/expsup/data/w2sigp1_int.tbl      |
| w2_in_sigp      | float64  | number | Highest relative power from signals detected in w2.                                                  |
| w2_brighter_sigp      | float64  | number | Highest relative power from signals detected in w2.                                                  |
| w2_fainter_sigp      | float64  | number | Highest relative power from signals detected in w2.                                                  |
| w3_mean       | object   | mag    | Mean w3mpro magnitude from l1b tables.                                                               |
| w3_mean_err   | object   | mag    | Mean w3sigmpro from l1b tables.                                                                     |
| w3_snr        | object   | number | Mean w3snr from l1b tables.                                                                         |
| w4_mean       | object   | mag    | Mean W4mpro magnitude from l1b tables.                                                               |
| w4_mean_err   | object   | mag    | Mean w4sigmpro from l1b tables.                                                                     |
| w4_snr        | object   | number | Mean w3snr from l1b tables.                                                                         |
| w1_w2         | float64  | mag    | W1_mpro - W2_mpro from filtered data.                                                                |
| delta_time    | float64  | days   | Time between first and last data points.                                                             |
| cadence    | float64  | days   | Median time between detections.                                                             |
| filter_flags  | object   | -      | Filtering flags for W1 and W2. A= Data filtered succesfully- Quality of data can be considered as good. B= Default filters returned less than 50 data points and filtering criteria was lowered to obtain more data. Quality of data should be considered unreliable. S= Filtering was skipped by user.|
| in65 | float64  | number    | ![Alt text](https://github.com/ASainio/WISE-Light-Curves/blob/main/null-hyph.png) 0-hypothesis values are first counted from mean magnitude of filtered data. Then Baseline is estimated by finding the magnitude where 65 range cover most of datapoints. Datapoints in, below and over are counted and expressed as %. These values can be used to compare variability and it might indicate type of variability (dimming or brightening compared to baseline). In light curve figures this estimated baseline is showen with purple dotted line|
| below65     | float64  | number    | |
| over65     | float64  | number    | |
| wiseview        | object   | link | Link to WISEView (Caselden et al. 2018).                                                                     |


Here’s the table with the new column names in the correct order:  

| Column Name           | d_type   | unit   | Description  |
|----------------------|----------|--------|--------------|
| gaia_id             | object   | -      | Gaia identifier. |
| simbad_name         | object   | -      | Simbad object name. |
| simbad_otype        | object   | -      | Simbad object type. |
| cw2020_source_id    | object   | -      | Source ID from CW2020 catalog. |
| designation         | object   | -      | WISE designation calculated from mean coordinates. |
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
| w1_var_ratio       | float64  | number | Variability divided by the highest amplitude epoch variability. |
| w1_mean_median     | float64  | mag    | Difference between w1_mean and w1_median. |
| w1_M_value         | float64  | mag    | M-test value for W1 variability (Kinemuchi et al. 2006). |
| w1_fap             | float64  | number | Lomb-Scargle False Alarm Probability. |
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
| w2_var_ratio       | float64  | number | Variability divided by the highest amplitude epoch variability. |
| w2_mean_median     | float64  | mag    | Difference between w2_mean and w2_median. |
| w2_M_value         | float64  | mag    | M-test value for W2 variability (Kinemuchi et al. 2006). |
| w2_fap             | float64  | number | Lomb-Scargle False Alarm Probability. |
| w2_sde             | float64  | number | Signal Detection Efficiency. |
| w2_power           | float64  | number | Highest relative power detected in W2. |
| w2_mean_power      | float64  | number | Mean power of detected W2 signals. |
| w2_median_power    | float64  | number | Median power of detected W2 signals. |
| w2_period          | float64  | days   | Period corresponding to the highest detected W2 signal. |
| w2_baseline        | float64  | mag    | Baseline magnitude where most W2 detections occur. |
| w2_sigp            | float64  | mag    | w2sigp for mean magnitude. |
| w2_in_sigp         | float64  | number | Percentage of data within the sigp range. |
| w2_brighter_sigp   | float64  | number | Percentage of data points brighter than the sigp range. |
| w2_fainter_sigp    | float64  | number | Percentage of data points fainter than the sigp range. |
| delta_time         | float64  | days   | Time between first and last data points. |
| cadence           | float64  | days   | Median time between detections. |
| epochs            | int64    | number | Number of total epochs used. |
| mean_offset       | float64  | mag    | Mean offset of magnitude measurements. |
| median_offset     | float64  | mag    | Median offset of magnitude measurements. |
| qual_flag         | object   | -      | Quality flag for data reliability. |
| GAIA_pmra         | float64  | mas/yr | Gaia proper motion in RA. |
| GAIA_pmra_err     | float64  | mas/yr | Gaia proper motion uncertainty in RA. |
| GAIA_pmdec        | float64  | mas/yr | Gaia proper motion in Dec. |
| GAIA_pmdec_err    | float64  | mas/yr | Gaia proper motion uncertainty in Dec. |
| WISE_pmra         | float64  | mas/yr | WISE proper motion in RA. |
| WISE_pmdec        | float64  | mas/yr | WISE proper motion in Dec. |
| theta_pm          | float64  | deg    | Proper motion direction angle. |
| wiseview          | object   | -      | WiseView identifier. |

This is the complete table with the new column names and the correct order. Let me know if you need any corrections!



