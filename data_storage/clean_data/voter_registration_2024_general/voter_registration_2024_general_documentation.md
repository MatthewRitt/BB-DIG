# Voter Registration 2024 General Documentation

## Overview
* This dataset shows voter registration data for the 2024 General Election across the 17 Alabama Black Belt counties. Each row represents one county. This dataset answers the question of everyone who could vote, how many actually registered, and how many are at risk of being removed from the rolls. The data is broken down by race.
* This dataset is one of six datasets covering civic participation in the Alabama Black Belt. Each dataset uses a different denominator to answer a different question. The eligiblepop files measure participation using the CVAP eligible population as the denominator. The voter_registration files measure registration access and purge risk using ALVR active and inactive counts. The voter_turnout files measure turnout using ALVR total registered voters (active plus inactive) as the denominator. Each file should be used together for the complete picture of civic participation in the region. See the data dictionaries for the other files for full details on their methodology
* This file uses ALVR data only for calculations to avoid CVAP undercount issues. The eligible population from CVAP is included for reference but not used as a denominator. For registration rates against the eligible population, see the eligiblepop files, which calculate participation rates.

## Sources
* Alabama Voter Registration (ALVR) October 2024 sheet (primary source for active and inactive registration counts by race)
* Census Bureau Citizen Voting Age Population (CVAP) 2024 file pulled through demographics_2024_general.csv (source for the eligible population reference)
* Redistricting Data Hub (RDH) 2024 voter file (source for FIPS codes only)

## Limitations
* We limited race columns to include only Black, White, and Latinx per project scope aligned with SPLC's focus on African American and Latinx communities. Asian, American Indian, Korean, Federally Registered, Other, and Not Identified categories were excluded from the calculated columns, but their counts remain in active_total and inactive_total.
* We initially calculated registration rates by dividing ALVR registration counts by the CVAP eligible population. This produced rates above 100% in most Black Belt counties because CVAP survey estimates appear to undercount eligible voters in rural majority-minority communities. We chose to remove those rates from the final output and instead include active_share columns calculated entirely from ALVR data, which avoids the CVAP discrepancy. Eligible population counts from CVAP are still included in the dataset for users who wish to calculate their own rates with a denominator they consider appropriate.
* ALVR October snapshot may differ slightly from Election Day registration totals, as we chose October to be the month to get registration data from.
* Some counties have very small Latinx registered populations, which can make active_share_latinx and inactive_rate_latinx unstable. For example, Wilcox has 9 registered Latinx voters, and Sumter has 13. Rates from these small samples should be interpreted with caution.

## Methodology Notes
* The Hispanic category from CVAP and ALVR source data was renamed to Latinx to align with SPLC language.
* FIPS codes are stored as 4-digit integers as provided by RDH. Standard practice is 5-digit codes with a leading zero (01005 instead of 1005).
* Missing values are stored as the literal string "null" from our project standardization document.
* Inactive status means a voter is on the polls but is flagged for potential removal due to possibly not voting in recent elections or not responding to confirmation mailings. Inactive voters can still vote, but may need to update their information or cast a provisional ballot.
* County names standardized across all files
* We took the ALVR October sheet, selected as the pre-election snapshot
* The ALVR dataset has a broken two-row header, so column names were manually set in the cleaning script
* The total registered by race is calculated by summing active and inactive counts
* The active share by race is calculated as active divided by total registered using ALVR data only, which avoids the CVAP undercount issue
* The inactive rate is calculated as inactive divided by total registered to show the overall purge risk
* The inactive rate per race was calculated to highlight equity concerns relevant to SPLC's voting rights work
* All percentages are stored as decimals between 0 and 1 for data analysis purposes
* Final dataset sorted alphabetically by county name, with one row per county

## Intended Use
This dataset is intended for SPLC's voting rights litigation, policy work, and community outreach in terms of identifying registration access gaps and voter purge risks in the Black Belt. It supports analysis of who registered out of the eligible population and which communities are most at risk of being removed from the rolls. The inactive rate columns per race are particularly useful for highlighting racial equity issues in voter purge practices. This dataset should be used alongside our other datasets for the complete picture of civic participation in the Black Belt region.
