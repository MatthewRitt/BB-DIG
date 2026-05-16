# Voter Registration 2024 General Cleaning Documentation

## Overview
This script reads the Alabama Voter Registration (ALVR) October 2024 sheet along with the Redistricting Data Hub (RDH) voter file and the cleaned eligible population dataset to produce a cleaned voter registration dataset for the 2024 General Election. The script calculates active and inactive registration counts by race and rates to flag purge risk. The script is narrowed down to the 17 Black Belt Counties detailed in the README file in this repository.

## Data Sources
Secretary of State Alabama Voter Registration (https://www.sos.alabama.gov/)
* ../../data_storage/raw_data/voter_data/2024_votereg_data_AlSoS.xlsx

Redistricting Hub (https://redistrictingdatahub.org/)
* ../../data_storage/raw_data/voter_data/AL_l2_2024_gen_stats_2020county.csv

Cleaned Eligible Population Dataset (produced by eligible_pop_2020_2024_cleaning.ipynb)
* ../../data_storage/clean_data/eligible_population_2024_general/eligible_population_2024_general.csv

## How to Use
The code outputs have already been generated for your convenience. The script produces one CSV file in the clean_data folder.

* `inactive_rate` displays the share of all registered voters who are inactive, flagging overall purge risk in the county
* `active_share_black`, `active_share_white`, `active_share_latinx` displays the share of registered voters in good standing by race. Lower value indicates higher purge risk
* `inactive_rate_black`, `inactive_rate_white`, `inactive_rate_latinx` displays the share of registered voters flagged for potential removal by race