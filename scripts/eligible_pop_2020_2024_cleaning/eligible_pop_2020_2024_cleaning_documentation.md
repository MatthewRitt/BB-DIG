# Eligible Population 2020 and 2024 Cleaning Documentation

## Overview
This script reads the Census Bureau Citizen Voting Age Population (CVAP) files for 2020 and 2024 along with the Alabama Secretary of State (SoS) race files and Redistricting Data Hub (RDH) voter file to produce cleaned eligible population datasets. The script calculates how many eligible voters by race actually voted and how many did not, broken down by Black, White, and Latinx. The script is narrowed down to the 17 Black Belt Counties detailed in the README file in this repository. The output is two cleaned CSVs, one for 2020 and one for 2024.

## Data Sources
Census Bureau Citizen Voting Age Population (https://www.census.gov/programs-surveys/decennial-census/about/voting-rights/cvap.html)
* ../../data_storage/raw_data/demographic_data/al_cvap_2024_cnty.csv
* ../../data_storage/raw_data/demographic_data/al_cvap_2020_cnty.csv

Secretary of State (https://www.sos.alabama.gov/)
* ../../data_storage/raw_data/voter_data/2024_race_gen_election.xlsx
* ../../data_storage/raw_data/voter_data/2020_race_gen_election.xlsx

Redistricting Hub (https://redistrictingdatahub.org/)
* ../../data_storage/raw_data/voter_data/AL_l2_2024_gen_stats_2020county.csv

## How to Use
The code outputs have already been generated for your convenience. The script produces two CSV files in the clean_data folder, one for each election year.

* `missing_voters_rate_black` `missing_voters_rate_white` `missing_voters_rate_latinx` displays the share of eligible voters by race who did not vote
* `not_voted_gap` displays the difference between Black and White non-participation rates. A positive value means Black non-participation is higher than White