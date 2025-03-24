# WISE L1b variability Catalogue of white dwarfs in Gaia EDR3 (Gentile+, 2021)

# Latest version with enhanced periodogram and latest NEOWISE epochs is now released (Public_main_catalog.csv)

This folder contains lombscargle analysis of ~3637~ 4478 white dwarfs cross matched between CATWISE2020 and Catalogue of white dwarfs in Gaia EDR3.
:

## Matching Procedure
1. **CatWISE Catalog Match:**
   - **Search Radius**: 3 arcseconds (2015.5 Epoch)
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
         (w1mpro < 15.5 AND w1snr > 30)
         OR
         (w2mpro < 15.5 AND w2snr > 30)
     )
     ```

## Filtering and Periodogram Analysis

### Position Filtering
- Each source with GAIA PM < 50mas are included within 1" radius.
- Sources within > 1 - 3" are included if CATWISE2020 PM vector behaves well with GAIA PM direction.
- 
- **Top Panels**: Raw data is plotted without additional filters.

### Other Filtering:
- Sources with < 100 datapoints after filtering were discarded. 
- Data was sigma clipped for periodogram with parameters: upper = 3, lower = 3.

### Periodogram Settings
  - Periods that were close to median WISE observation cadence recalculated we're removed to avoid false positives. However aliasing might still occure in some cases.
  - Known aliasing periods remaining are: 0.028
  - Aliasing fractions are indicated with gray triangles in the **Best Period** figure.
  - Minimum period: 0.5 hours
  - The periodogram is run twice for improved accuracy.
  - Each band is analyzed independently.


This work benefits from:
- VizieR Online Data Catalog: Catalogue of white dwarfs in Gaia EDR3 (Gentile+, 2021)
- ASTROPY
- WISEVIEW
- 
