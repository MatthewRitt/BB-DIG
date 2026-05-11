# Data Sources and Attribution

This project uses publicly available data from the following sources. Each source has its own terms of use which apply to the raw data files included in this repository and any data pulled from them.

## Alabama Secretary of State

**What we use** Voter turnout files (total, gender, age, race breakdowns) and voter registration files (ALVR monthly snapshots)

**URL** https://www.sos.alabama.gov/

**Files in this repository**
- 2020_total_gen_election.xlsx, 2020_gender_gen_election.xlsx, 2020_age_gen_election.xlsx, 2020_race_gen_election.xlsx
- 2024_total_gen_election.xlsx, 2024_gender_gen_election.xlsx, 2024_age_gen_election.xlsx, 2024_race_gen_election.xlsx
- 2024_votereg_data_AlSoS.xlsx (Alabama Voter Registration October 2024 snapshot)

**Terms** These are public records published by the Alabama Secretary of State office. Available for public use including analysis and redistribution.

## Census Bureau Citizen Voting Age Population (CVAP)

**What we use** Eligible voter population estimates by race for Alabama counties (2020 and 2024 5-year estimates)

**URL** https://www.census.gov/programs-surveys/decennial-census/about/voting-rights/cvap.html

**Files in this repository**
- al_cvap_2020_cnty.csv
- al_cvap_2024_cnty.csv

**Terms** Census Bureau data is in the public domain and free to use including redistribution. Standard attribution requested when used in publications.

## Redistricting Data Hub (RDH)

**What we use** Alabama voter file data processed from L2 (a national voter file vendor). We use this primarily for FIPS codes and verification.

**URL** https://redistrictingdatahub.org/

**Files in this repository**
- AL_l2_2024_gen_stats_2020county.csv

**Terms** RDH data is licensed for noncommercial and nonpartisan use only. Per RDH terms of use:
- Cannot be used for commercial purposes
- Cannot be used for partisan political activity
- Cannot be used for gerrymandering
- Anyone using this data agrees to RDH's full terms of use available at https://redistrictingdatahub.org/terms-and-conditions/

**Required Attribution** "This data was obtained from the Redistricting Data Hub" and "This analysis was conducted using data from the Redistricting Data Hub"

## Project Outputs

The cleaned datasets (eligible_population, voter_registration, and voter_turnout files for 2020 and 2024) are derived from the above sources. Use of these derived datasets is also subject to the original sources' terms of use, particularly RDH's noncommercial and nonpartisan restrictions.

The cleaning scripts, data dictionaries, and standardization documentation are the work of the BB-DIG Team and are released under the MIT License. See LICENSE.md.

## Acknowledgment

This project was completed as part of INST490 at the University of Maryland in partnership with the Southern Poverty Law Center(SPLC).