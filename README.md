# WISE L1b Folded Light Curves of Modified Catalogue of white dwarfs in Gaia EDR3 (Gentile+, 2021)

# New version with enhanced periodogram and latest NEOWISE epochs will be released 2/2024.

This folder contains lombscargle analysis of 3637 folded infra red light curves from a modified white dwarf sample.

## Source Selection
The white dwarf candidates were sourced from the **Gaia DR2** white dwarf candidate catalog (Gentile Fusillo+, 2019) using the following criteria:

- **Parallax** >= 1
- **Proper Motion (PM)** >= 0 mas
- **White Dwarf Probability** >= 50%

## Matching Procedure
1. **CatWISE Catalog Match:**
   - **Search Radius**: 2 arcseconds (2016 Epoch)
   - **Filters**:
     ```sql
     (cc_flags NOT LIKE 'D___')
     AND (cc_flags NOT LIKE 'H___')
     AND (cc_flags NOT LIKE 'O___')
     AND (cc_flags NOT LIKE 'P___')
     AND (cc_flags NOT LIKE '_D__')
     AND (cc_flags NOT LIKE '_H__')
     AND (cc_flags NOT LIKE '_O__')
     AND (cc_flags NOT LIKE '_P__')
     AND ab_flags = '00'
     AND (
         (w1mpro < 15 AND w1snr > 30)
         OR
         (w2mpro < 15 AND w2snr > 30)
     )
     ```

## Filtering and Periodogram Analysis

### Position Filtering
- Each data point is cross-checked against the source’s expected position based on Gaia proper motions, with generous 1 arcsecond radius.
- **Top Panels**: Raw data is plotted without additional filters.

### Sigma Clipping for Periodogram
- Sources with < 50 datapoints after filtering were discarded. 
- Data was sigma clipped for periodogram with parameters: upper = 3, lower = 3.

### Periodogram Settings
- **Period Adjustments**:
  - If the periods close to the WISE interval (~0.066 days) or its fractions were recalculated to avoid aliasing. However aliasing might still occure in some cases.
  - Aliasing fractions are indicated with gray triangles in the **Best Period** figure.
- **Period Range**:
  - Minimum period: 0.5 hours
  - Maximum period: 7 days
- **Execution**: The periodogram is run twice for improved accuracy.
- **Separate Solutions**: Each band is analyzed independently.


This work benefits from VizieR Online Data Catalog: Catalogue of white dwarfs in Gaia EDR3 (Gentile+, 2021)
