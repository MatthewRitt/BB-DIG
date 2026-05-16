# Eligible Population 2020 General Documentation

## Overview
* This dataset shows the full picture of the eligible voting population in the 2020 General Election across the 17 Alabama Black Belt counties. Each row represents one county. The dataset details those eligible to vote, those who actually voted, and those who did not, all split up by race (Black, White, and Latinx).
* This dataset is one of six datasets covering civic participation in the Alabama Black Belt. Each dataset uses a different denominator to answer a different question. The eligible_population files measure participation using the CVAP eligible population as the denominator. The voter_registration files measure registration access and purge risk using ALVR active and inactive counts. The voter_turnout files measure turnout using ALVR total registered voters (active plus inactive) as the denominator. Each file should be used together for the complete picture of civic participation in the region. See the data dictionaries for the other files for full details on their methodology
* This file calculates participation using the CVAP eligible population as the denominator. This is different from voter turnout, which uses registered voters as the denominator and is found in the voter_turnout_2024_general.csv.

## Sources
* Census Bureau Citizen Voting Age Population (CVAP) 2020 file (primary source for eligible population by race)
* Alabama Secretary of State (SoS) 2020 race file (source for actual ballot counts by race)
* Redistricting Data Hub (RDH) 2024 voter file (source for FIPS codes only)

## Limitations
* We limited race columns to include only Black, White, and Latinx per project scope, which aligns with SPLC's focus on African American and Latinx communities. Asian and other race categories were excluded.
* For very small Latinx populations, CVAP survey estimates may differ from actual SoS turnout counts. CVAP is a Census Bureau survey with margins of error, while SoS counts actual ballots. In a few counties, this results in voted_latinx exceeding eligible_latinx, which causes missing_voters to be set to 0. The affected county for 2020 is Hale, with 10 eligible vs 10 voted, resulting in a 0 rate. Rates should be interpreted with caution when the eligible populations are under 100.
* CVAP estimates have margins of error, which are not included in this file but are available in the original Census Bureau source.

## Extra Notes
* The Hispanic category from CVAP and SoS source data was renamed to Latinx to align with SPLC language.
* FIPS codes are stored as 4-digit integers. Standard practice is 5-digit codes with a leading zero (01005 instead of 1005).
* Missing values are stored as the literal string "null" per our project standardization document.
* County names standardized across all files
* We pulled FIPS codes from RDH and used them as the primary key for joining CVAP-eligible population data
* The eligible population by race is pulled from CVAP and joined on the FIPS code
* The vote counts by race were pulled from the SoS race turnout file and joined on county name
* The missing voters are calculated as eligible minus voted, with negative results set to 0 to handle source misalignment.
* The missing voter rate is calculated as missing voters divided by the eligible population
* The not-voted gap is calculated as Black missing rate minus White missing rate
* All of the percentages are stored as decimals between 0 and 1 for data analysis purposes
* The final dataset is sorted alphabetically by county name, with one row per county

## Intended Use
This dataset is intended for SPLC’s voting rights litigation, policy work, and community involvement in terms of all civic participation. It supports analysis of who could have voted but did not, including people who never made it onto the voter rolls in the first place. The not_voted_gap column is useful for highlighting racial equity issues in civic participation. This dataset should be used alongside our other datasets for the complete picture of civic participation in the Black Belt region.
