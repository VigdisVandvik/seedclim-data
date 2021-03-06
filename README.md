
<style>
p.caption {
  font-size: 0.8em;
}
</style>

This is the GitHub repository for the SeedClim project. Data paper:
Vandvik et al….

## PROJECT AND SITE INFORMATION

This project reports on…

## DATASETS, CODE AND ANALYSES

The raw and cleaned datasets are stored on OSF…

The data was processed and analysed using R. All code is stored on
github:…

### Download data

To download the data, the following function can be used: …

### Data sets

Describe relationships of the data sets…

<div class="figure">

<img src="ChinaDatabase.png" alt="Relationship of all data sets." width="60%" />

<p class="caption">

Relationship of all data sets.

</p>

</div>

### SITES

| Variable name                  | Variable type | Variable range or levels | Units/treatment level | Description                                                            | How measured |
| :----------------------------- | :------------ | :----------------------- | :-------------------- | :--------------------------------------------------------------------- | :----------- |
| siteID                         | categorical   | Alrust - Vikesland       | Alrust                | Unique site ID                                                         | defined      |
| norwegian\_name                | categorical   | NA - NA                  | NA                    | Norwegian species name                                                 | recorded     |
| site\_code                     | categorical   | alp1 - sub4              | Alp1                  | Site ID as a combination of biogeographic zone and precipitation level | defined      |
| latitude                       | numeric       | 60.5445 - 61.0866        | decimal degree        | coordinate of site                                                     | measured     |
| longitude                      | numeric       | 5.96487 - 9.07876        | decimal degree        | coordinate of site                                                     | measured     |
| elevation                      | numeric       | 346 - 1213               | meter above sea level | elevation derived from DEM                                             | measured     |
| biogeographic\_zone            | categorical   | Low-alpine - Sub-alpine  | Low-alpine            | Biogeographic zone                                                     | defined      |
| biogeographic\_section         | categorical   | O1 - OC                  | O2                    | Biogeographic section                                                  | defined      |
| annual\_precipitation\_gridded | numeric       | 596.348 - 3028.69        | mm                    | Downscaled annual precipitation                                        | measured     |
| temperature\_level             | numeric       | 1 - 3                    | 1-3                   | Numeric value for temperature level                                    | defined      |
| summer\_temperature\_gridded   | numeric       | 5.86638 - 10.7775        | degree celcius        | Downscaled summer temperature                                          | measured     |
| precipitation\_level           | numeric       | 1 - 4                    | 1-4                   | Numeric value for precipitation level                                  | defined      |

### BLOCK

| Variable name | Variable type | Variable range or levels | Units/treatment level | Description                                                               | How measured |
| :------------ | :------------ | :----------------------- | :-------------------- | :------------------------------------------------------------------------ | :----------- |
| blockID       | categorical   | Alr1 - Vik5              | Alr1                  | Unique block ID as combination of three letter site code and block number | defined      |
| siteID        | categorical   | Alrust - Vikesland       | Alrust                | Unique site ID                                                            | defined      |
| slope         | numeric       | NA - NA                  | degree                | Slope of the block                                                        | measured     |
| aspect        | numeric       | NA - NA                  | degree                | Aspect of the block                                                       | measured     |
| comment       | categorical   | NA - NA                  | NA                    | NA                                                                        | NA           |

### PLOT

| Variable name | Variable type | Variable range or levels | Units/treatment level | Description                                                               | How measured |
| :------------ | :------------ | :----------------------- | :-------------------- | :------------------------------------------------------------------------ | :----------- |
| plotID        | numeric       | \-168 - 30610            | 1                     | Unique numeric plot ID for geographic location of the turf                | defined      |
| blockID       | categorical   | Alr1 - Vik5              | Alr1                  | Unique block ID as combination of three letter site code and block number | defined      |
| aspect        | numeric       | 0 - 0                    | degree                | Aspect of the block                                                       | measured     |
| slope         | numeric       | 0 - 0                    | degree                | Slope of the block                                                        | measured     |

### TURF

| Variable name     | Variable type | Variable range or levels | Units/treatment level | Description                                                                   | How measured |
| :---------------- | :------------ | :----------------------- | :-------------------- | :---------------------------------------------------------------------------- | :----------- |
| turfID            | categorical   | 1 TT2 28 - Vik5RTG       | 1 TT2 28              | Unique ID of vegetation turf as originplotID, treatment and destinationplotID | defined      |
| TTtreat           | categorical   | TT1 - TTC                | TT2                   | Treatment of turf transplant                                                  | defined      |
| RTtreat           | categorical   | \- RTS                   | RTC                   | Treatment of recruit tag                                                      | defined      |
| GRtreat           | categorical   | \- TTC                   | RTC                   | Treatment of graminoids removal                                               | defined      |
| originPlotID      | numeric       | \-145 - 30610            | 1                     | Origin location of the turf                                                   | defined      |
| destinationPlotID | numeric       | \-168 - 30610            | 28                    | Destination location of the turf                                              | defined      |

### TAXON

| Variable name | Variable type | Variable range or levels               | Units/treatment level | Description                                    | How measured |
| :------------ | :------------ | :------------------------------------- | :-------------------- | :--------------------------------------------- | :----------- |
| species       | categorical   | Ach.mil - X….1                         | Ach.mil               | three letter codes for genus and species names | identified   |
| species\_name | categorical   | ??? - Viscaria vulgaris                | Achillea millefolium  | full genus and species names                   | identified   |
| authority     | categorical   | NA - NA                                | NA                    | taxanomic authority                            | defined      |
| family        | categorical   | ?? - Woodsiaceae                       | Asteraceae            | Plant family name                              | identified   |
| comment       | categorical   | New name? - Synonym: Kalmia procumbens | NA                    | NA                                             | NA           |

### TURF COMMUNITY

| Variable name | Variable type | Variable range or levels                                                                  | Units/treatment level | Description                                                                   | How measured |
| :------------ | :------------ | :---------------------------------------------------------------------------------------- | :-------------------- | :---------------------------------------------------------------------------- | :----------- |
| turfID        | categorical   | 1 TT2 28 - Vik5RTG                                                                        | 1 TT2 28              | Unique ID of vegetation turf as originplotID, treatment and destinationplotID | defined      |
| year          | numeric       | 2009 - 2019                                                                               | 2009                  | Year of the sampling                                                          | defined      |
| species       | categorical   | Ach.mil - X….1                                                                            | Ach.mil               | three letter codes for genus and species names                                | identified   |
| cover         | numeric       | 0.04 - 100                                                                                | percentage            | Percent cover of a species in a turf                                          | measured     |
| cf            | numeric       | 0 - 1                                                                                     | NA                    | Uncertain species identification                                              | defined      |
| flag          | categorical   | imputed from NID.seedling presence - Subturf w/o cover. Imputed as mean of adjacent years | NA                    | Values flagged for possible error                                             | NA           |

### SUBTURF COMMUNITY

| Variable name | Variable type | Variable range or levels | Units/treatment level | Description                                                                   | How measured |
| :------------ | :------------ | :----------------------- | :-------------------- | :---------------------------------------------------------------------------- | :----------- |
| turfID        | categorical   | 1 TT2 28 - Vik5RTG       | 1 TT2 28              | Unique ID of vegetation turf as originplotID, treatment and destinationplotID | defined      |
| subturf       | numeric       | 1 - 25                   | 1                     | Location of subturf within the turf                                           | defined      |
| year          | numeric       | 2009 - 2019              | 2009                  | Year of the sampling                                                          | defined      |
| species       | categorical   | Ach.mil - X….1           | Ach.mil               | three letter codes for genus and species names                                | identified   |
| presence      | categorical   | \- VV                    | 0-1                   | Presence of species                                                           | measured     |
| seedlings     | numeric       | 0 - 12                   | 0-1                   | Presence of seedlings where cotyledons are visible                            | measured     |
| juvenile      | numeric       | 0 - 12                   | 0-1                   | Presence of juveniles that are not fully grown plants                         | measured     |
| adult         | numeric       | 0 - 1                    | 0-1                   | Presence of adults                                                            | measured     |
| fertile       | numeric       | 0 - 1                    | 0-1                   | Presence of fertile                                                           | measured     |
| vegetative    | numeric       | 0 - 1                    | 0-1                   | Presence of vegetative                                                        | measured     |
| dominant      | numeric       | 0 - 1                    | 0-1                   | Species cover more than 50 percent of subturf                                 | measured     |
| cf            | numeric       | 0 - 1                    | NA                    | Uncertain species identification                                              | defined      |
| flag          | categorical   | NA - NA                  | NA                    | Values flagged for possible error                                             | NA           |

### TURF ENVIRONMENT

| Variable name      | Variable type | Variable range or levels | Units/treatment level | Description                                                                   | How measured |
| :----------------- | :------------ | :----------------------- | :-------------------- | :---------------------------------------------------------------------------- | :----------- |
| turfID             | categorical   | 1 TT2 28 - Vik5RTG       | 1 TT2 28              | Unique ID of vegetation turf as originplotID, treatment and destinationplotID | defined      |
| year               | numeric       | 2009 - 2019              | 2009                  | Year of the sampling                                                          | defined      |
| pleuro             | numeric       | 0 - 100                  | percentage            | Cover of pleurocarp per (sub)turf                                             | measured     |
| acro               | numeric       | 0 - 66                   | percentage            | Cover of acrocarp per (sub)turf                                               | measured     |
| liver              | numeric       | 0 - 34.12                | percentage            | Cover of liverworth per (sub)turf                                             | measured     |
| lichen             | numeric       | 0 - 75                   | percentage            | Cover of lichen per (sub)turf                                                 | measured     |
| litter             | numeric       | 0 - 95                   | percentage            | Cover of litter per (sub)turf                                                 | measured     |
| soil               | numeric       | 0 - 95                   | percentage            | Cover of soil per (sub)turf                                                   | measured     |
| rock               | numeric       | 0 - 40                   | percentage            | Cover of rock per (sub)turf                                                   | measured     |
| total\_vascular    | numeric       | 1 - 100                  | percent               | Total percent cover by vascular plants                                        | measured     |
| total\_bryophytes  | numeric       | 0 - 100                  | percent               | Total percent cover by bryophytes                                             | measured     |
| total\_lichen      | numeric       | 0 - 90                   | percent               | Total percent cover by lichens                                                | measured     |
| vegetation\_height | numeric       | 0 - 237.5                | cm                    | Average height of the vascular vegetation in the plot                         | measured     |
| moss\_height       | numeric       | 0 - 75                   | cm                    | Average height of the mosses                                                  | measured     |
| litter\_thickness  | numeric       | Inf - -Inf               | NA                    | NA                                                                            | NA           |
| comment            | categorical   | \- X1c                   | NA                    | NA                                                                            | NA           |
| recorder           | categorical   | \- W/KK                  | NA                    | Observer of the vegetation                                                    | defined      |
| date               | categorical   | \- missing data          | yyyy-mm-dd            | Date of observation                                                           | recorded     |

### SUBTURF ENVIRONMENT

| Variable name | Variable type | Variable range or levels | Units/treatment level | Description                                                                   | How measured |
| :------------ | :------------ | :----------------------- | :-------------------- | :---------------------------------------------------------------------------- | :----------- |
| turfID        | categorical   | 1 TT2 28 - Vik5RTG       | 1 TT2 28              | Unique ID of vegetation turf as originplotID, treatment and destinationplotID | defined      |
| subturf       | numeric       | 1 - 25                   | 1                     | Location of subturf within the turf                                           | defined      |
| year          | numeric       | 2009 - 2019              | 2009                  | Year of the sampling                                                          | defined      |
| pleuro        | numeric       | 0 - 100                  | percentage            | Cover of pleurocarp per (sub)turf                                             | measured     |
| acro          | numeric       | 0 - 95                   | percentage            | Cover of acrocarp per (sub)turf                                               | measured     |
| liver         | numeric       | 0 - 99                   | percentage            | Cover of liverworth per (sub)turf                                             | measured     |
| lichen        | numeric       | 0 - 100                  | percentage            | Cover of lichen per (sub)turf                                                 | measured     |
| litter        | numeric       | 0 - 100                  | percentage            | Cover of litter per (sub)turf                                                 | measured     |
| soil          | numeric       | 0 - 100                  | percentage            | Cover of soil per (sub)turf                                                   | measured     |
| rock          | numeric       | 0 - 100                  | percentage            | Cover of rock per (sub)turf                                                   | measured     |
| comment       | categorical   | \- X                     | NA                    | NA                                                                            | NA           |
| bad           | categorical   | \- x                     | NA                    | Comment on damaged subturfs                                                   | NA           |

### SITE ATTRIBUTES

| Variable name    | Variable type | Variable range or levels    | Units/treatment level | Description    | How measured      |
| :--------------- | :------------ | :-------------------------- | :-------------------- | :------------- | :---------------- |
| siteID           | categorical   | Alrust - Vikesland          | Alrust                | Unique site ID | defined           |
| attribute        | categorical   | aspect - total\_N\_red\_oxi | NA                    | NA             | NA                |
| value\_numeric   | numeric       | 0 - 607                     | Number                | Numeric values | measured-recorded |
| value\_character | categorical   | Ålrust - Vikesland          | NA                    | NA             | NA                |

### SPECIES ATTRIBUTES

| Variable name    | Variable type | Variable range or levels  | Units/treatment level | Description                                    | How measured      |
| :--------------- | :------------ | :------------------------ | :-------------------- | :--------------------------------------------- | :---------------- |
| species          | categorical   | Ach.mil - Vis.vul         | Ach.mil               | three letter codes for genus and species names | identified        |
| attribute        | categorical   | boreal\_nemoral - wetland | NA                    | NA                                             | NA                |
| value\_numeric   | numeric       | 0.5 - 4800                | Number                | Numeric values                                 | measured-recorded |
| value\_character | categorical   | SBor (MBor-NBor) - woody  | NA                    | NA                                             | NA                |
