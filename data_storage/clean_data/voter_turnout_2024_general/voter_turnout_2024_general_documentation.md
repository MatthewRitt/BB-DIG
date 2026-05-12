# Voter Turnout 2024 General Documentation

## Overview
* This dataset shows voter turnout for the 2024 General Election across the 17 Alabama Black Belt counties. Each row represents one county. The dataset contains information regarding registered voters and ballots, broken down by gender, age, and race.
* This dataset is one of three datasets covering civic participation in the Alabama Black Belt. Each dataset uses a different denominator to answer a different question. The eligiblepop files measure participation using the CVAP eligible population as the denominator. The voter_registration files measure registration access and purge risk using ALVR active and inactive counts. The voter_turnout files measure turnout using ALVR total registered voters (active plus inactive) as the denominator. Each file should be used together for the complete picture of civic participation in the region. See the data dictionaries for the other files for full details on their methodology.
* Turnout in this file is calculated as ballots divided by total registered voters from ALVR (active plus inactive). This is different from the eligiblepop files, which use the CVAP eligible population as the denominator.

## Sources
* Alabama Secretary of State turnout files: total, gender, age, and race breakdown (primary source for ballot counts)
* Alabama Voter Registration (ALVR) October 2024 sheet (source for race-based registered voter denominators)
* Redistricting Data Hub (RDH) 2024 voter file (source for FIPS codes only)

## Limitations
* We limited race columns to include only Black, White, and Latinx per project scope aligned with SPLC's focus on African American and Latinx communities. Asian, American Indian, Korean, Federally Registered, Other, and Not Identified categories were excluded. Race columns will not sum to total_ballots_cast, as total_ballots_cast is an overview of each county's voting participation as a whole.
* Butler County has a 418 ballot discrepancy between the SoS gender/age breakdown files and the SOS total file. All other counties have a much smaller discrepancy
* We noticed small discrepancies between SOS breakdown files (gender, age, race) and the SOS total file across most counties. These are documented in the team's verification scripts that we ran when verifying our data.
* ALVR October snapshot may differ slightly from Election Day registration totals, as we chose October to be the month to get registration data from.
* FIPS codes are stored as 4-digit integers as provided by RDH. Standard practice is 5-digit codes with a leading zero (01005 instead of 1005).
* The Hispanic category from the SoS source data was renamed to Latinx to align with SPLC language.
* SoS race categories are self-reported at the time of voter registration.
* Missing values are stored as the literal string "null" per our project standardization document.

## Extra Notes
* County names standardized across all files
* All four SoS files merged on county_name
* Active and inactive registered voters by race were summed from the ALVR October sheet to create total registered race denominators.
* Race-based turnout rates calculated by dividing race ballot counts from the SOS by total registered race counts from ALVR
* Age 80+ column created by summing SOS buckets 80-89, 90-99, and 100+
* All percentages are stored as decimals between 0 and 1 for data analysis purposes
* Final dataset sorted alphabetically by county name, with one row per county

## Intended Use
This dataset is intended for SPLC’s voting rights litigation, policy work, and community involvement in terms of all civic participation. It supports analysis of who voted in the 2024 General Election, broken down by demographics, but specifically who participated that was registered. This dataset should be used alongside our other datasets for the complete picture of civic participation in the Black Belt region.
